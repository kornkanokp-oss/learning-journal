# learning-journal
To be Penetration Tester
# Week 1 - Completed TryHackMe Pre-Security: Offensive & Defensive Security
  ต้องรู้ว่า blue team คิดว่าอะไร แล้วจะป้องกันและโจมตีคู่ต่อสู้ยังไง ระบุและชี้ได้ว่าอะไรคือสิ่งแปลกปลอมที่จะมาโจมตีและหยุดการโจมตี
  ## Career Role
  1. Security analysts (Blue team -Detail-Focused, Curious and love puzzles ) : These people monitor, investigate and respond to activity taking place on an organisation's devices and network, and play a significant role in an organisation's **defence**.
  2. Security Engineering ( Problem-Solving and Building Things): Build & maintland system and process to protect orgnisation's network and device which know as "cyber secuirty", Assessing Risk and Keeping up-to-date with the lastest.  Intrusion Detection System ( IDS)
  3. Penetration Testing / ethical hacking : Testing the security of system, networks and websites. Performing secuirty assessment, autdits, analysing security pokicies
# Week 1 - Day 6: Network Fundamentals ( IP Address DNS, HTTP, Ports)
- People name = IP Address ( Which can change)
- Figerprinots == A media Access Control (MAC Address): cannot change

## IP Address
<img width="554" height="167" alt="image" src="https://github.com/user-attachments/assets/8f217f3d-60cc-42dc-a98a-38eabc753432" />

Internet
    |
Internet service Provider (ISP) 
    |
Public IP address (we buy home's network)
    |
Router
    |
Private IP @ home (192.168.x.x)
    |
My Laptop

## MAC Addresses
<img width="518" height="206" alt="image" src="https://github.com/user-attachments/assets/9370122c-93fa-4e65-a081-8a1dc6227489" />
- MAC address canbe faked or "**spoofed**" > The network device pretends to identify as another MAC address.
-  MAC address controls "Guest", "Public" in the public place.

## Ping ICP

## DNS
1. Mapping IP address with domain name.
   <img width="1408" height="1142" alt="image" src="https://github.com/user-attachments/assets/efc4510a-ad00-4043-900a-5238cdae8556" />

2. Enhanace Security at DNS when it has enable below featue becuase it has the Encryption.
   - DOH = DNS over HTTPs
   - DOT = DNS over Transport layer
   - DNSSEC
   - DNSCrypt
3.  Case Study
   You buy domain "www.hopdiarysound.com" with company A. Normally company A will default and give DNS server for free. However you can choose. Simplily said that your music company use the specific feature i.e. AWS Route 53, Cloudflare, Google Cloud DNS which under companyB.
    5.1. You should know that company B generate the public IP Address to you. In Case company B also be the Web Hosting or Cloud Hosting.
    5.2. In the setting of Company A, you should change the **NS Record** and point to Company B.
    5.3. Company A = Domain register. Company B = DNS Hosting.
4. DNS Recorder Definition ( From Case Study)
   - Why we need to know DNS Recorder
   - How many DNS Recorder
     - A Record
       - www.hopdiarysound.com map with IP xx.xx.xx.xx which keep with Company B who belong to NS Server (NS)
       - nslookup hopdiarysound.com
     - NS Record
        - nslookup -type=ns google.com
        - Identify which server keep DNS
        - This command will send Company A which acts as operator and then Company B answer.
     - AAAA Record
        - It is like A Record but for iPv6
     - MX Record
        - Mailbox
     - PTR Record
        - Reverse DNS Lookup of A Record
     - CNAME (Canonical Name Record)
        - Set up Alias name of domain for another domain. 

