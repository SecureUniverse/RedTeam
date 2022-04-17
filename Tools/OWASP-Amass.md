# OWASP Amass

## Usage
   - Domain Enumeration

## Link
   - https://github.com/OWASP/Amass

## ATT&CK 
   - Reconnaissance
     - Search Open Technical Databases (T1596)
       - DNS/Passive DNS
       - WHOIS
       - Digital Certificates 

## Commands
   - Install
     - ```apt-get install amass``` 
   - Help of a module
     - ```amass enum -h``` 
   - Other
     - ```amass enum -d mysite.com -src -ip -dir mysite```  
       - The path of result is "mysite"
     - ```amass enum -d mysite.com -src -ip -norecursive```
     - ```amass enum -d mysite.com -src -ip -brute -dir mysite```
       - Wordlist path: /usr/share/amass/wordlists
     - ```amass intel -asn 16509```
       - Find ASN number from first command
     - ```amass intel -whois -d mysite.com -dir mysite```
     - ```amass db -dir mysite -list```
       - Show the list of scans 
     - ```amass db -dir mysite -enum 1 -show``` 
       - Show the result of 1`st scan  
     - ```amass viz -dir mysite -d3``` 
       - Create a visualized HTML file of the 1`st scan 
