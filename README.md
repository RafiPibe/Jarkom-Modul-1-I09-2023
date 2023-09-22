## Jarkom-Modul-1-I09-2023
<p>Praktikum Jaringan Komputer Modul 1 I09</p>
<p>Computer Network Practicum 1st Module I09</p>

| Name                        | NRP        |
|-----------------------------|------------|
|Eric Azka Nugroho            | 5025211064 |
|Faraihan Rafi Adityawarman   | 5025211074 |


# Flag 1
![Part 1](https://media.discordapp.net/attachments/1153305482438660178/1154401068541812807/Screenshot_2023-09-18_211457.png?width=1246&height=702)
![Part 2](https://media.discordapp.net/attachments/1153305482438660178/1154401069108052009/Screenshot_2023-09-18_211641.png?width=1246&height=702)
![Terminal](https://media.discordapp.net/attachments/1153305482438660178/1154401069443579975/Screenshot_2023-09-18_211740.png?width=1110&height=532)

Explanation :
Using query such as below
```
ftp
```
we can check the FTP protocol to see the sequence numbers and acknowledge number.
on point a we are told to answer what is the sequence number (raw) on the packet with the answer being `258040667`.
Then point b, we are told to answer the acknowledge number (raw) on the packet with the answer being `1044861039`.
after that, we are needed to search the response of the activity, that is the number after 147, and that is 149.
with the question the same as before but this time being the response, c and d answer is `1044861039` and `258040696` respectively.

# Flag 2
![Part 1](https://media.discordapp.net/attachments/1153305482438660178/1154404132258582619/Screenshot_2023-09-18_201544.png?width=1248&height=702)
![Terminal](https://media.discordapp.net/attachments/1153305482438660178/1154404132510244865/Screenshot_2023-09-18_193744.png?width=1020&height=150)

Explanation :
Using query such as below
```
ip.addr == 10.21.78.111
```
we can check the ip address, Then we check on the info that have `(text/html)`. On that packet, we check the Hypertext Transfer Protocol and we get the server name that is `gunicorn`

# Flag 3
![Part 1](https://cdn.discordapp.com/attachments/1153305482438660178/1153331540068155452/Screen_Shot_2023-09-18_at_21.06.51.png)
![Terminal](https://cdn.discordapp.com/attachments/1153305482438660178/1153331504689197137/Screen_Shot_2023-09-18_at_21.07.33.png)

Explanation:
Use the query below:
```
ip.dst == 239.255.255.250 && udp.dstport == 3702
```
After filtering the wireshark using the given query, we can see how many package are from ip = 239.255.255.259 and the port is 3702. We can actually see the protocol used in the problem is UDP.

# Flag 4
![Part 1](https://cdn.discordapp.com/attachments/1153305482438660178/1153320386969223269/Screen_Shot_2023-09-18_at_20.23.16.png)
![Terminal](https://cdn.discordapp.com/attachments/1153305482438660178/1153320213769633862/Screen_Shot_2023-09-18_at_20.21.58.png)

Explanation:
To actually solve this problem, we just need to go to number 130 and see the details in the User Datagram Protocol where there is Checksum = 0x18e5



# Flag 5 (Revisi)
![Part 1](https://media.discordapp.net/attachments/1153305482438660178/1154663584513658930/image.png?width=936&height=701)
![Part 2](https://media.discordapp.net/attachments/1153305482438660178/1154663643825319976/image.png?width=705&height=517)
![Part 3](https://media.discordapp.net/attachments/1153305482438660178/1154663827770724362/image.png?width=554&height=701)
![Part 4](https://media.discordapp.net/attachments/1153305482438660178/1154663939393724508/image.png?width=599&height=631)
![Part 5](https://media.discordapp.net/attachments/1153305482438660178/1154664579520024597/image.png?width=612&height=128)
![Terminal](https://media.discordapp.net/attachments/1153305482438660178/1154665179099963413/image.png?width=705&height=219)

In this flag, we need to find the zip password to see the inside of the txt file using the pcap file and export an SMTP file, then decode it using a base64 decoder. 
This is to get the terminal command, which is `nc 10.21.78 1111`, Then we proceeded to answer some of the questions.
The answer to question A is 60 packets. The B answer is 25. With the help of Google, we found that SMPT port is 25. C answer is the public IP which is `74.53.140.153`. 
We can check them because all the IPs other than that is a private.

# Flag 6

# Flag 7
![Part 1](https://media.discordapp.net/attachments/1153305482438660178/1154416089577553970/image.png?width=919&height=702)
![Terminal](https://media.discordapp.net/attachments/1153305482438660178/1154416089908916375/Screenshot_2023-09-18_192001.png?width=899&height=150)

Explanation :
With the query below, we can check how many packets we get from the query
```
ip.dst == 184.87.193.88
```
Then we will know how many packets are inside, with this one being 6

# Flag 8
![Terminal](https://media.discordapp.net/attachments/1153305482438660178/1154416417022681188/image.png?width=583&height=105)

Explanation :
We use the query below to answer the question
```
tcp.dstport == 80 || udp.dstport == 80
```
because we need to find the port of the destination of TCP or UDP either way

# Flag 9
![Terminal](https://cdn.discordapp.com/attachments/1153305482438660178/1153322228977516696/Screen_Shot_2023-09-18_at_20.30.31.png)

Explanation:
In order to find the package that we want, we need to create a query that can sort the IP source and IP destination. The answer can be seen below
```
ip.src == 10.51.40.1 && ip.dst != 10.39.55.34
```
IP.src == 10.51.40.1 means that it filter the IP with the source of 10.51.40.1, while IP.dst != 10.39.55.34 is to filter where the IP destination is not 10.39.55.34

# Flag 10
![Part 1](https://media.discordapp.net/attachments/1153305482438660178/1154417029923737720/image.png?width=1248&height=702)
![Terminal](https://media.discordapp.net/attachments/1153305482438660178/1154417030326394960/image.png?width=1099&height=177)

Explanation :
with the query
```
telnet
```
then we will find the TELNET protocols inside wireshark. then we check the one with the same requirement inside the data being `[username]:[password]` and the correct answer is `dhafin:kesayangannyak0k0`
