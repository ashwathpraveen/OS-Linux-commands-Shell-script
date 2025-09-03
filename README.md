# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting
```
Ashwath p
reg no:212224220012
```

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
<img width="397" height="140" alt="Screenshot from 2025-09-03 08-27-22" src="https://github.com/user-attachments/assets/8728b244-46f4-435b-b018-4bc6476ac6f9" />
<img width="397" height="119" alt="Screenshot from 2025-09-03 08-27-47" src="https://github.com/user-attachments/assets/f934c6e8-9c66-4eed-8144-3d56a614e11f" />


cat < file2
## OUTPUT
<img width="397" height="140" alt="Screenshot from 2025-09-03 08-27-34" src="https://github.com/user-attachments/assets/a7845c37-915d-4110-aa2a-06fcb2447053" />
<img width="397" height="119" alt="Screenshot from 2025-09-03 08-28-05" src="https://github.com/user-attachments/assets/5105ae26-ce96-4a45-9068-2c6b9a8083c3" />





# Comparing Files
cmp file1 file2
## OUTPUT
<img width="476" height="53" alt="Screenshot from 2025-09-03 08-28-25" src="https://github.com/user-attachments/assets/d298b8b3-34c8-489a-a8ea-4f63f4171dbe" />

 
comm file1 file2
 ## OUTPUT

 <img width="476" height="266" alt="Screenshot from 2025-09-03 08-28-43" src="https://github.com/user-attachments/assets/82cf0b26-cb97-4a76-ad99-98f61c327e3d" />

diff file1 file2
## OUTPUT
<img width="476" height="248" alt="Screenshot from 2025-09-03 08-29-04" src="https://github.com/user-attachments/assets/ffa9eb50-27f4-41a1-875a-2b4d3e20d5b7" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
<img width="476" height="97" alt="Screenshot from 2025-09-03 08-32-34" src="https://github.com/user-attachments/assets/f3fa2a4c-1a4e-4f33-8b2d-3f13958c60b2" />

<img width="476" height="108" alt="Screenshot from 2025-09-03 08-32-46" src="https://github.com/user-attachments/assets/7fe0b5e2-3b43-46f4-84ae-bd96c3430d68" />

<img width="476" height="79" alt="Screenshot from 2025-09-03 08-32-57" src="https://github.com/user-attachments/assets/b5028a2b-eea7-4de8-ba3c-8ab9255c4e85" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="518" height="93" alt="Screenshot from 2025-09-03 08-34-11" src="https://github.com/user-attachments/assets/aea69a1d-2782-4e21-8fb7-24458861ae2f" />




cut -d "|" -f 2 file22
## OUTPUT
<img width="518" height="93" alt="Screenshot from 2025-09-03 08-34-19" src="https://github.com/user-attachments/assets/10006043-29ee-4d24-b2b0-b2a2fefafd08" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
<img width="518" height="71" alt="Screenshot from 2025-09-03 08-36-46" src="https://github.com/user-attachments/assets/d4c0b661-5fdd-440b-a933-4b991eac08dd" />

<img width="518" height="71" alt="Screenshot from 2025-09-03 08-36-54" src="https://github.com/user-attachments/assets/64039696-90b1-4338-8688-3e7a11b84825" />


grep hello newfile 
## OUTPUT


<img width="518" height="53" alt="Screenshot from 2025-09-03 08-37-04" src="https://github.com/user-attachments/assets/80c87567-3a32-4306-99c9-694f1875921a" />


grep -v hello newfile 
## OUTPUT
<img width="518" height="53" alt="Screenshot from 2025-09-03 08-37-51" src="https://github.com/user-attachments/assets/6c5c4dc4-e5c5-4ae3-9ac3-681ba706a076" />




cat newfile | grep -i "hello"
## OUTPUT

<img width="582" height="73" alt="Screenshot from 2025-09-03 08-38-45" src="https://github.com/user-attachments/assets/e7fbe06d-bd4f-4837-91d7-4cd8f178a53b" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="605" height="56" alt="Screenshot from 2025-09-03 08-38-58" src="https://github.com/user-attachments/assets/e4def517-5175-415b-bdb6-8ab4e0f03ee3" />



grep -R ubuntu /etc
## OUTPUT
<img width="1381" height="1055" alt="Screenshot from 2025-09-03 08-39-43" src="https://github.com/user-attachments/assets/7e64be19-87fe-4c56-bd89-e87ecc422496" />



grep -w -n world newfile   
## OUTPUT
<img width="524" height="51" alt="Screenshot from 2025-09-03 08-40-41" src="https://github.com/user-attachments/assets/238b7a97-1018-4dd9-9ba1-6efd83a555ab" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="530" height="243" alt="Screenshot from 2025-09-03 08-43-32" src="https://github.com/user-attachments/assets/c2ed48b7-dc30-4fbc-8c3d-90c29a3ae055" />
<img width="669" height="73" alt="Screenshot from 2025-09-03 08-47-52" src="https://github.com/user-attachments/assets/805151fe-0322-48c5-90f1-2821ea90d86d" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="669" height="73" alt="Screenshot from 2025-09-03 08-47-58" src="https://github.com/user-attachments/assets/4ab32635-ffc5-44ca-a37c-dd14db442d43" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="669" height="73" alt="Screenshot from 2025-09-03 08-48-07" src="https://github.com/user-attachments/assets/d5df2f0f-fff3-4337-aed1-b0899550f13e" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="669" height="51" alt="Screenshot from 2025-09-03 08-48-15" src="https://github.com/user-attachments/assets/f2bdaafe-aafc-49bb-a581-f86425280337" />


egrep '(world$)' newfile 
## OUTPUT
<img width="669" height="73" alt="Screenshot from 2025-09-03 08-48-23" src="https://github.com/user-attachments/assets/09647369-281a-440d-969e-7516ae3b19dd" />



egrep '(World$)' newfile 
## OUTPUT
<img width="669" height="57" alt="Screenshot from 2025-09-03 08-48-31" src="https://github.com/user-attachments/assets/6b78bc7f-d710-487e-8ca7-5c6281d18bc0" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="669" height="94" alt="Screenshot from 2025-09-03 08-48-42" src="https://github.com/user-attachments/assets/0614b4e2-5495-43e3-8cfc-0f01f8379136" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="669" height="59" alt="Screenshot from 2025-09-03 08-48-51" src="https://github.com/user-attachments/assets/7ce373e5-338f-405e-b5e8-d660d6b426aa" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="669" height="59" alt="Screenshot from 2025-09-03 08-49-59" src="https://github.com/user-attachments/assets/0dde8ff7-f310-41da-b621-e558efeb960f" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="669" height="51" alt="Screenshot from 2025-09-03 08-50-09" src="https://github.com/user-attachments/assets/4ae37041-0675-4ed9-9c00-c6fac54771d6" />


egrep l{2} newfile
## OUTPUT

<img width="669" height="77" alt="Screenshot from 2025-09-03 08-50-17" src="https://github.com/user-attachments/assets/b42563a3-4cf6-47b6-868a-d7d324499bdb" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="669" height="92" alt="Screenshot from 2025-09-03 08-50-25" src="https://github.com/user-attachments/assets/fc0f2a31-6432-4377-97ee-da00bf6ea5d3" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
<img width="669" height="229" alt="Screenshot from 2025-09-03 08-58-31" src="https://github.com/user-attachments/assets/c628fe3d-9da1-4303-8760-42c99e8b7dd3" />

<img width="669" height="52" alt="Screenshot from 2025-09-03 08-58-40" src="https://github.com/user-attachments/assets/e85da8be-e40d-4e74-bd7d-c484f2abc880" />


sed -n -e '$p' file23
## OUTPUT

<img width="669" height="52" alt="Screenshot from 2025-09-03 08-58-55" src="https://github.com/user-attachments/assets/654faf95-87ed-4e5d-b4ca-9bce04d3db64" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="669" height="232" alt="Screenshot from 2025-09-03 08-59-07" src="https://github.com/user-attachments/assets/a75b0c25-bc90-48d6-8f1c-a0fabc9ee939" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="669" height="225" alt="Screenshot from 2025-09-03 08-59-17" src="https://github.com/user-attachments/assets/cd72d455-8ca8-4af8-ae9d-ba13e6ba9b19" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="669" height="225" alt="Screenshot from 2025-09-03 09-00-25" src="https://github.com/user-attachments/assets/2826478a-9c6f-461b-b85a-a91cfa4d78d4" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="669" height="144" alt="Screenshot from 2025-09-03 09-00-34" src="https://github.com/user-attachments/assets/ea266992-ef78-4792-82d3-32c3af112067" />



sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="669" height="93" alt="Screenshot from 2025-09-03 09-00-43" src="https://github.com/user-attachments/assets/2db2edaf-fa46-4514-840c-067967a49c14" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="669" height="70" alt="Screenshot from 2025-09-03 09-00-49" src="https://github.com/user-attachments/assets/bb54e0ce-669b-4396-b8e7-a695bc03375f" />


seq 10 
## OUTPUT

<img width="396" height="243" alt="Screenshot from 2025-09-03 09-01-03" src="https://github.com/user-attachments/assets/b336479e-ff65-41ca-9c7b-edb00d4cfeb9" />



seq 10 | sed -n '4,6p'
## OUTPUT


<img width="494" height="86" alt="Screenshot from 2025-09-03 09-01-17" src="https://github.com/user-attachments/assets/934efe67-5e18-4571-934f-5c76527242d0" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="496" height="97" alt="Screenshot from 2025-09-03 09-01-30" src="https://github.com/user-attachments/assets/1a8b4c4a-7a69-4274-87e4-5bdd20dae059" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="496" height="117" alt="Screenshot from 2025-09-03 09-02-50" src="https://github.com/user-attachments/assets/ef23fdee-cdba-47f8-be06-6a53fdfcae2d" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="496" height="98" alt="Screenshot from 2025-09-03 09-02-59" src="https://github.com/user-attachments/assets/cc72b47f-6314-4a4b-99eb-3247bf1ddc5b" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="524" height="89" alt="Screenshot from 2025-09-03 09-03-10" src="https://github.com/user-attachments/assets/7a929a0b-8aae-475a-aba1-ae281fb6b14d" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="562" height="94" alt="Screenshot from 2025-09-03 09-03-20" src="https://github.com/user-attachments/assets/d66edf21-870f-439c-b56d-837fa31101ea" />

<img width="562" height="94" alt="Screenshot from 2025-09-03 09-03-31" src="https://github.com/user-attachments/assets/e34f9e58-00f8-4acb-9fdc-fd94213a9931" />


sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT

<img width="562" height="155" alt="Screenshot from 2025-09-03 09-03-43" src="https://github.com/user-attachments/assets/56688bfb-5636-4c72-a944-724045ac6a49" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

<img width="562" height="155" alt="Screenshot from 2025-09-03 09-03-43" src="https://github.com/user-attachments/assets/efc041c6-cf34-4d4a-8835-82168ab46c61" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 <img width="674" height="223" alt="Screenshot from 2025-09-03 09-03-53" src="https://github.com/user-attachments/assets/079d90cf-6425-447c-8584-c830085d54bc" />


cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="674" height="96" alt="Screenshot from 2025-09-03 09-08-05" src="https://github.com/user-attachments/assets/ef7e94e6-5bc7-4a5d-8d2f-e26c4dde43dc" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="674" height="96" alt="Screenshot from 2025-09-03 09-08-16" src="https://github.com/user-attachments/assets/ef36d1a2-cec1-47f5-9bb0-6489eaa47bc9" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="847" height="202" alt="Screenshot from 2025-09-03 09-17-21" src="https://github.com/user-attachments/assets/4e706492-14a3-4d50-b134-1542fe20483d" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


<img width="847" height="138" alt="Screenshot from 2025-09-03 09-18-34" src="https://github.com/user-attachments/assets/1e3ff2d9-b2ea-4111-b4f0-9cd471c61e62" />


tar -xvf backup.tar
## OUTPUT

<img width="847" height="97" alt="Screenshot from 2025-09-03 09-20-44" src="https://github.com/user-attachments/assets/87efc0bf-9e99-4aaa-a6c7-18b861fed173" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="847" height="69" alt="Screenshot from 2025-09-03 09-22-22" src="https://github.com/user-attachments/assets/da0bc569-ad8a-41af-b8de-5ffe30209f31" />

gunzip backup.tar.gz
## OUTPUT

<img width="847" height="74" alt="Screenshot from 2025-09-03 09-23-04" src="https://github.com/user-attachments/assets/dc992b8d-c87f-40c9-ac1e-fb2e6c1a751a" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="458" height="115" alt="Screenshot from 2025-09-03 09-33-35" src="https://github.com/user-attachments/assets/9bf8f446-9af3-4e1e-a9b3-02fed4a9ab7b" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="538" height="208" alt="Screenshot from 2025-09-03 09-34-28" src="https://github.com/user-attachments/assets/d5a35bb6-868b-4580-92eb-917f9f0c2689" />


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

<img width="544" height="557" alt="Screenshot from 2025-09-03 09-35-44" src="https://github.com/user-attachments/assets/b698e791-747a-4928-bbd2-cd3bac5862c8" />

 
ls file1
## OUTPUT

<img width="689" height="360" alt="Screenshot from 2025-09-03 09-36-34" src="https://github.com/user-attachments/assets/b13edda9-88b7-4144-92ad-c0032bc146ee" />

echo $?
## OUTPUT 

<img width="459" height="47" alt="Screenshot from 2025-09-03 09-38-38" src="https://github.com/user-attachments/assets/0ccab00a-ee4f-4254-b518-ec99317c0604" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 <img width="600" height="88" alt="Screenshot from 2025-09-03 09-39-18" src="https://github.com/user-attachments/assets/43f2cebb-fdc5-4506-a6fd-60b30c4e5d72" />

abcd
 
echo $?
 ## OUTPUT


<img width="600" height="57" alt="Screenshot from 2025-09-03 09-40-36" src="https://github.com/user-attachments/assets/7898a0a5-6414-4f1a-b6c8-c0e3a297aea4" />

 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


<img width="693" height="554" alt="Screenshot from 2025-09-03 09-42-18" src="https://github.com/user-attachments/assets/1d3a1f33-ef11-413b-9ee2-159e4d708b5c" />

# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

<img width="732" height="424" alt="Screenshot from 2025-09-03 09-43-18" src="https://github.com/user-attachments/assets/6cc43ce3-1c41-4547-b5ff-44f0a5fe739d" />

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT

<img width="818" height="862" alt="Screenshot from 2025-09-03 09-44-12" src="https://github.com/user-attachments/assets/6050c5e4-a6f7-4be0-8883-5c6e14054282" />



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

<img width="686" height="752" alt="Screenshot from 2025-09-03 09-47-32" src="https://github.com/user-attachments/assets/fc4dad89-7c34-46d0-96a6-b65518f947e4" />

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

<img width="717" height="952" alt="Screenshot from 2025-09-03 09-48-49" src="https://github.com/user-attachments/assets/cd9e0273-bd90-4498-a6e1-7b464d886a39" />

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT

<img width="665" height="510" alt="Screenshot from 2025-09-03 15-17-22" src="https://github.com/user-attachments/assets/81308cd5-aefb-42c2-91c9-ac2b803b3529" />


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

<img width="665" height="184" alt="Screenshot from 2025-09-03 15-19-47" src="https://github.com/user-attachments/assets/f38ba6b3-4752-41b8-bad4-39a1726b5383" />

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 


# RESULT:
The Commands are executed successfully.
