ssh -p4422 root@yoko.ukrtux.com - connect to yoko.ukrtux.com as a root user
>> Enter passwd: Jnf5kh76Bv+ou6 
*next step logout from port and genetate ssh key*
ssh-keygen -t rsa - command to create new key
*after, enter way, where your key will be saved (in my case: /home/vboxuser/.ssh/id_rsa)*
*dont enter any passphrase, just click Enter two times*
ssh-add /home/vboxuser/.ssh/id_rsa - connect generated key to my machine
ssh-copy-id -i /home/vboxuser/.ssh/id_rsa.pub -p4422 root@yoko.ukrtux.com
>> Enter passwd: Jnf5kh76Bv+ou6
Now enter "ssh -p4422 root@yoko.ukrtux.com", you shoud be logged w/o passwd. After logout, and try to connect to your machine 
through a port 8877 
ssh -D8877 -p4422 root@yoko.ukrtux.com - logging through a port we opened.
Check site getip'dap'org, you must be located in Tokyo. 

Open second terminal and enter:
python3 -m http.server 8866 - use, this command, being in catalogue with project you want to open.
Check: localhost:8866
In third terminal type:(can be also first )
ssh -R 14422:localhost:8866 -p4422 root@yoko.ukrtux.com - make reverse connection from yoko.ukrtux on your localhost 8866.
Check: yoko.ukrtux.com:14422 (DONT WORK)
