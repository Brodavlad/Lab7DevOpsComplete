ssh-keygen -t rsa - створення нового ключа

ssh-add /home/vboxuser/.ssh/id_rsa - підєднюємо приватний ключ до машинки

ssh-copy-id -i /home/vboxuser/.ssh/id_rsa.pub -p5122 root@yoko.ukrtux.com - used to add an ssh key to a remote machine використовується для додавання ссш ключа до
віддаленої машини

ssh -p5122 root@yoko.ukrtux.com - перевірка зєднання (пароль не потрібно вводити)

ssh - D8888 -p5122 root@yoko.ukrtux.com - вхід через порт, котрий відкрили



STEPS: python3 -m http.server 8866 - скористайтеся цією командою, перебуваючи в каталозі з проектом, який ви хочете надіслати.

ssh -R 15122:localhost:8866 -p5122 root@yoko.ukrtux.com - створює зворотне підключення до вашого сервера
