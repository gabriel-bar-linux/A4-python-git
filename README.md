# A4-python-git

## TD1
### Exercice 1
```
cd /
ls
pwd
mkdir test
cd /home
cd ~
cd ..
cd ..
cd ~
mkdir test
cd test
pwd
```

### Exercice 2
```
cd home
ls
mkdir linux_ex_1
cd linux_ex_1
touch gabriel_bar.txt
mkdir notes
mv gabriel_bar.txt notes
mv gabriel_bar.txt gabriel_bar_2023.txt
ls
cd ..
ls
cd notes
cp -R notes notes_2023
cd ..
```

### Exercice 3
```
cd linux_ex_1
rm -r notes
touch script_1.sh
echo "Script running please waait ..."
echo "Done."

nano scipt_1.sh
cat script_1.sh
bash scipt_1.sh
ls
```

### Exercice 4
```
touch ~/linux_ex_1/credentials
echo "fake personal information" > ~/linux_ex_1/credentials
ls -l ~/linux_ex_1/credentials

chmod 555 ~/linux_ex_1/credentials
ls -l ~/linux_ex_1/credentials
cat ~/linux_ex_1/credentials

chmod 775 ~/linux_ex_1/credentials
ls -l ~/linux_ex_1/credentials
cat ~/linux_ex_1/credentials

chmod 711 ~/linux_ex_1/credentials
ls -l ~/linux_ex_1/credentials

chmod 717 ~/linux_ex_1/credentials
ls -l ~/linux_ex_1/credentials

chmod 777 ~/linux_ex_1/credentials
ls -l ~/linux_ex_1/credentials
```

```
cd /

sudo touch .private_file
echo "private information" > .private_file
ls -al

echo "modified information" >> .private_file
cat .private_file

sudo echo "root-modified information" >> .private_file
cat .private_file

sudo chmod 777 .private_file
echo "final modification" >> .private_file
cat .private_file
```

```
sudo apt update
sudo apt upgrade
sudo apt install cmatrix
cmatrix
"Control" + "C"
sudo apt install tmux
tmux
echo "Hello session 0"
cmatrix 
"Control" + "B" + "D"
tmux new-session
echo "Hello session 1"
"Control" + "B" + "D"
tmux list-sessions
tmux attach -t 0
"Control" + "B" + "D"
tmux attach -t 1
"Control" + "B" + "D"
tmux list-sessions
tmux kill-session -a
tmux list-sessions
```

```
cmatrix --help
cmatrix --colors white
cmatrix --delay=500
cmatrix --delay=500 --colors blue
man cmatrix
tmux --help
man tmux
```
## TD2
### Exercice 1
```
1 : sudo apt-get update && sudo apt-get upgrade
2 : uname -a
    top
    nproc
    lscpu | grep cache
    df -h
    mount | column -t
    lsusb
    hostname
```
### Exercice 2
```
1 : x="piri pimpin"
2 : echo $x
3 : x+=" piri pimpon"
4 : mkdir my_programs
    cd my_programs
5 : echo "pilou pilou" > pilou
6 : bash pilou
7 : chmod +x pilou
8 : ./pilou
9 : echo $PATH
10 : export PATH=$PATH:$(pwd)
11 : echo 'export PATH=$PATH:$(pwd)' >> ~/.bashrc
12 : cd ~
13 : pilou
14 : export PATH=$PATH:/path/to/my_programs
15 : pilou
```
### Exercice 3
```
1 : #!/bin/bash
    echo $(date) - Hello >> hellos.txt
2 : chmod +x say_hello.sh
3 : crontab -e
    * * * * * /path/to/say_hello.sh
```
### Exercice 4
```
1 : mkdir hash_checksum
    cd hash_checksum
2 : touch .sensible_addresses
    touch .sensible_passwords
3 : ls    
4 : #!/bin/bash
    echo "Have a good day"
5 : ./gentle_script.sh
6 : sha256sum gentle_script.sh > log_sha
7 : echo 'rm -rf .sensible*' >> gentle_script.sh
8 : sha256sum gentle_script.sh > log_sha
9 : ./gentle_script.sh
10 : ls
11 : cat log_sha
```
### Exercice 5
```
1 : sudo apt-get install qpdf
2 : mkdir compress
    cd compress
3 : echo "Hello" > hello
4 : zlib-flate -1 < hello > hello.deflate
    ls -l hello.deflate | awk '{print $5}' > log_compress
5 : yes "Hello" | head -n 1000 > hello_multiple
6 : zlib-flate -1 < hello_multiple > hello_multiple.deflate
    ls -l hello_multiple.deflate | awk '{print $5}' >> log_compress
7 : for i in {1..100}; do echo "Hello $i"; done > hello_multiple_i
8 : zlib-flate -1 < hello_multiple_i > hello_multiple_i.deflate
    ls -l hello_multiple_i.deflate | awk '{print $5}' >> log_compress
9 : cat log_compress
10 & 11 ?
```
### Exercice 6
```
1 : sudo useradd client_1 -m -p passwd-client_1
    sudo useradd contributor_1 -m -p passwd-contributor_1
    sudo useradd contributor_2 -m -p passwd-contributor_2
2 : sudo groupadd clients
    sudo groupadd contributors
3 : sudo usermod -aG clients client_1
    sudo usermod -aG contributors contributor_1
    sudo usermod -aG contributors contributor_2
4 : getent passwd
    getent group
5 : sudo mkdir lika_project
    sudo chgrp clients lika_project
    sudo chmod 550 lika_project
    sudo chmod g+rw lika_project
6 : ls -l
7 : su client_1
    rm -r lika_project
8 : su contributor_1
    rm -r lika_project
9 : whoami
```
