# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

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
<img width="366" height="153" alt="image" src="https://github.com/user-attachments/assets/1aecd80e-753b-4f1f-9625-6a8239459452" />



cat < file2
## OUTPUT
<img width="336" height="177" alt="image" src="https://github.com/user-attachments/assets/fa54d276-cf0f-4e17-aa79-5bb0a1676952" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="358" height="72" alt="image" src="https://github.com/user-attachments/assets/cdf1fb99-f732-40bf-b01b-95617b672f53" />

comm file1 file2
 ## OUTPUT
<img width="390" height="203" alt="image" src="https://github.com/user-attachments/assets/2ec267d8-0cd4-46d0-8b2b-3b85ebea6206" />

 
diff file1 file2
## OUTPUT
<img width="462" height="270" alt="image" src="https://github.com/user-attachments/assets/9d13837a-1915-453c-b5e2-a4b4cef2f185" />


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
<img width="422" height="97" alt="image" src="https://github.com/user-attachments/assets/cd9c09b3-8bf8-4424-8ab2-2039c5155d36" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="483" height="151" alt="image" src="https://github.com/user-attachments/assets/70cf75aa-2c2d-44d2-8221-56fa2639ce82" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="395" height="155" alt="image" src="https://github.com/user-attachments/assets/138027e2-aa16-4938-ae55-a9ae6e187ea7" />


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
<img width="435" height="71" alt="image" src="https://github.com/user-attachments/assets/be6dd9fa-df8a-406f-89e9-d305729fd3cc" />



grep hello newfile 
## OUTPUT
<img width="397" height="71" alt="image" src="https://github.com/user-attachments/assets/7faeb4cd-b7bc-4144-8a36-7e9eaedcf193" />




grep -v hello newfile 
## OUTPUT
<img width="391" height="92" alt="image" src="https://github.com/user-attachments/assets/177059ca-9224-4409-b435-26fba6e2bdd1" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="390" height="102" alt="image" src="https://github.com/user-attachments/assets/55b1cea4-5ce0-4b76-828d-f374891c8c28" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="440" height="77" alt="image" src="https://github.com/user-attachments/assets/5093b8d7-8d97-41f3-afd0-385c0c2f57eb" />




grep -R ubuntu /etc
## OUTPUT
<img width="852" height="272" alt="image" src="https://github.com/user-attachments/assets/5249a497-b976-43d1-855c-140e0c42ea14" />



grep -w -n world newfile   
## OUTPUT
<img width="420" height="72" alt="image" src="https://github.com/user-attachments/assets/ed59120b-1f0a-4852-9d55-03c07971e2ab" />


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
<img width="510" height="101" alt="image" src="https://github.com/user-attachments/assets/27c4a9ae-1c24-4282-9a0b-ae983ffafa3d" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="408" height="93" alt="image" src="https://github.com/user-attachments/assets/83ba6718-e7a8-4772-97dd-9d8cfac75988" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="393" height="102" alt="image" src="https://github.com/user-attachments/assets/544aee9b-fbde-4c3f-a739-3c83f26137f4" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="420" height="75" alt="image" src="https://github.com/user-attachments/assets/31750902-7274-4d57-84b5-9ef740f03f0c" />



egrep '(world$)' newfile 
## OUTPUT
<img width="395" height="98" alt="image" src="https://github.com/user-attachments/assets/9fe6de7d-99e6-487b-95d7-afaf80a7c179" />



egrep '(World$)' newfile 
## OUTPUT
<img width="386" height="71" alt="image" src="https://github.com/user-attachments/assets/828f9c70-b4a3-4fad-9c9c-d4c2d48d08cd" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="392" height="101" alt="image" src="https://github.com/user-attachments/assets/21a19da2-41a6-49b2-86f7-538a029fc280" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="418" height="70" alt="image" src="https://github.com/user-attachments/assets/7ce2b608-2708-4607-a205-b7e992d46a8f" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="412" height="67" alt="image" src="https://github.com/user-attachments/assets/91bcda90-4962-4d73-bbeb-3f09bd798b41" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="413" height="71" alt="image" src="https://github.com/user-attachments/assets/7f6c5864-febd-41b7-998b-07ba96ebd2fb" />


egrep l{2} newfile
## OUTPUT
<img width="342" height="100" alt="image" src="https://github.com/user-attachments/assets/c89f0e75-0f3a-4d94-9f5d-0b6c56080a4a" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="455" height="128" alt="image" src="https://github.com/user-attachments/assets/4e02ad9b-6b21-495a-9f34-d2ff136aaf6b" />


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
<img width="391" height="78" alt="image" src="https://github.com/user-attachments/assets/5af9b2cc-56e0-446b-9778-c19954252424" />



sed -n -e '$p' file23
## OUTPUT
<img width="372" height="60" alt="image" src="https://github.com/user-attachments/assets/f1b36daa-2759-4c85-840e-65137343e14d" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="498" height="253" alt="image" src="https://github.com/user-attachments/assets/dd76abf2-e43b-465b-a1ef-4da9ebd9e2d9" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="520" height="253" alt="image" src="https://github.com/user-attachments/assets/c1ca844d-3bd7-49c2-9b2d-56075ffd4d0c" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="512" height="252" alt="image" src="https://github.com/user-attachments/assets/93c2fc48-6e04-4cf4-a4f5-a9e77ef1cc06" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="465" height="173" alt="image" src="https://github.com/user-attachments/assets/d90d20c3-7205-4225-80c6-948e282b0c24" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="422" height="135" alt="image" src="https://github.com/user-attachments/assets/c52e2a68-57a3-45f8-a355-86d39b4d0c61" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="522" height="102" alt="image" src="https://github.com/user-attachments/assets/6f8a73bf-8598-47ee-864a-f3ec39f02a4a" />



seq 10 
## OUTPUT
<img width="437" height="295" alt="image" src="https://github.com/user-attachments/assets/18ddf46d-b3b4-4487-8f5c-23d0e561b9b4" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="352" height="127" alt="image" src="https://github.com/user-attachments/assets/c5b32b31-7de7-4a41-b604-898860f08bca" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="380" height="125" alt="image" src="https://github.com/user-attachments/assets/35f83a46-c477-4885-8f4e-721e06b26cd4" />




seq 3 | sed '2a hello'
## OUTPUT
<img width="350" height="141" alt="image" src="https://github.com/user-attachments/assets/6091885f-2e57-4a91-b399-83bd47e916b8" />





seq 2 | sed '2i hello'
## OUTPUT
<img width="337" height="127" alt="image" src="https://github.com/user-attachments/assets/6e075361-e50f-49f2-972f-94e06351c23c" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="377" height="117" alt="image" src="https://github.com/user-attachments/assets/eb67091e-66b6-42e4-85a2-8f784ecd6453" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="497" height="122" alt="image" src="https://github.com/user-attachments/assets/123fae63-b7bc-4ef1-ad62-8f8143ca1642" />

sed -n '2,4{s/$/*/;p}' file23
##OUTPUT
<img width="485" height="132" alt="image" src="https://github.com/user-attachments/assets/0bbb1d4e-ed91-443a-9b77-2e958a445b7c" />


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
<img width="423" height="145" alt="image" src="https://github.com/user-attachments/assets/eff1668c-bfb6-4f03-a8cb-90597bf63d8b" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="522" height="248" alt="image" src="https://github.com/user-attachments/assets/490d76aa-6cc1-4c59-a491-f5375a617126" />

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
<img width="442" height="123" alt="image" src="https://github.com/user-attachments/assets/965424a6-5653-41b0-a080-6ff5c51ee96d" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="541" height="122" alt="image" src="https://github.com/user-attachments/assets/161156f9-ef8c-4434-9b2a-60350bf9131a" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="702" height="568" alt="image" src="https://github.com/user-attachments/assets/5ebfdfb2-cff1-4ea5-9de8-0fa46d79e504" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="813" height="588" alt="image" src="https://github.com/user-attachments/assets/f0dc4ae9-8d55-4392-b093-8cbd2944a5d4" />


tar -xvf backup.tar
## OUTPUT
<img width="698" height="580" alt="image" src="https://github.com/user-attachments/assets/82a9f186-646a-4f84-8524-21c16db439d9" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="517" height="132" alt="image" src="https://github.com/user-attachments/assets/ac1585b4-baf5-4dab-b1b8-f4caf1876a6e" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="521" height="52" alt="image" src="https://github.com/user-attachments/assets/b0aa5342-bcd5-49e5-bafb-14adb2805021" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="490" height="90" alt="image" src="https://github.com/user-attachments/assets/f7ffa2f2-0ab6-43d2-922a-75dc2cd43534" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="442" height="126" alt="image" src="https://github.com/user-attachments/assets/84947073-6873-4ad6-9e52-0c47cc934e41" />


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
.<img width="697" height="427" alt="image" src="https://github.com/user-attachments/assets/7da62ab1-4cd9-4a6f-9e7b-8f504e41c72f" />

 
ls file1
## OUTPUT
<img width="438" height="71" alt="image" src="https://github.com/user-attachments/assets/de160c9e-15ce-49e4-8243-ed5b1f845458" />

echo $?
## OUTPUT 
<img width="486" height="82" alt="image" src="https://github.com/user-attachments/assets/0f55ac9b-95a5-479b-9147-084cf57c636e" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="472" height="70" alt="image" src="https://github.com/user-attachments/assets/89176e62-23df-4a39-be3e-f321c8c356a6" />

abcd
 
echo $?
 ## OUTPUT
<img width="472" height="70" alt="image" src="https://github.com/user-attachments/assets/0bfe34cb-8448-4abe-83d8-4a390b158073" />


 
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

<img width="477" height="270" alt="image" src="https://github.com/user-attachments/assets/1adc3b55-36de-4bb4-b8bf-c49a067eb983" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="697" height="161" alt="image" src="https://github.com/user-attachments/assets/abc7ad40-19ba-430c-8dc6-95a90cb4e6e4" />


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
<img width="627" height="97" alt="image" src="https://github.com/user-attachments/assets/1d6461cd-85f9-42db-a74f-d5bbb2a8163a" />

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
<img width="513" height="477" alt="image" src="https://github.com/user-attachments/assets/9530b69c-681a-4aee-9d66-ae3fa41a2632" />

<img width="648" height="203" alt="image" src="https://github.com/user-attachments/assets/93c4c5e7-17b3-49c3-9a3b-998cc4a2ec65" />


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
<img width="525" height="360" alt="image" src="https://github.com/user-attachments/assets/7b1648c3-9f7f-4671-af4c-df5a7e83a268" />


<img width="637" height="177" alt="image" src="https://github.com/user-attachments/assets/44021fba-8ae3-4c60-b424-75ee5ae2edfb" />


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
<img width="587" height="445" alt="image" src="https://github.com/user-attachments/assets/32c0719c-c9bf-41f4-beae-26822780ce83" />

<img width="645" height="250" alt="image" src="https://github.com/user-attachments/assets/170ec508-b264-455f-be00-634d30a2357b" />

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
<img width="551" height="482" alt="image" src="https://github.com/user-attachments/assets/42ff26dd-0921-45f1-9aeb-59a184e7b4e1" />

<img width="642" height="151" alt="image" src="https://github.com/user-attachments/assets/a915d9c3-c3fd-449b-a58b-411e2a2b977d" />


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
<img width="657" height="351" alt="image" src="https://github.com/user-attachments/assets/e789045f-0edb-428a-8fd5-f4666d114fcd" />

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

<img width="627" height="430" alt="image" src="https://github.com/user-attachments/assets/37df8731-0293-420a-83d3-8213123bd57e" />

 
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
<img width="497" height="250" alt="image" src="https://github.com/user-attachments/assets/e22ffe2b-efaa-402d-8e27-f519fe2f7c19" />

 <img width="437" height="311" alt="image" src="https://github.com/user-attachments/assets/186cc23d-3795-4600-a0d0-161be039f16c" />

 
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
<img width="588" height="427" alt="image" src="https://github.com/user-attachments/assets/1d0e41ac-25c6-44b8-835e-2badfb82c3af" />
 
 
 
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
<img width="757" height="477" alt="image" src="https://github.com/user-attachments/assets/59b3cd88-e942-4ea7-b3ab-4e2ddcbded98" />
 
 
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
<img width="676" height="397" alt="image" src="https://github.com/user-attachments/assets/a777a352-1f13-4a66-8e6d-199b837bbf65" />
 
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
<img width="676" height="397" alt="image" src="https://github.com/user-attachments/assets/0d5a952e-f6f6-4cdc-911e-1a5192c6cf17" />
 
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
 <img width="642" height="486" alt="image" src="https://github.com/user-attachments/assets/921d3485-f09f-4c17-8471-d55b765d7c95" />

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
<img width="653" height="428" alt="image" src="https://github.com/user-attachments/assets/3ee7ec3b-188d-48a3-ad4b-efe431e2fe57" />

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
<img width="402" height="193" alt="image" src="https://github.com/user-attachments/assets/ff1e9356-4b8d-4dd4-9a14-247ed5575a0c" />


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
<img width="437" height="472" alt="image" src="https://github.com/user-attachments/assets/7e222b3f-eb2a-4634-80e0-baf44bd1ee1a" />


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
<img width="377" height="357" alt="image" src="https://github.com/user-attachments/assets/0730301e-493e-4f32-a75b-892311e219f0" />

 
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
<img width="697" height="446" alt="image" src="https://github.com/user-attachments/assets/5970bb93-4714-4cf4-a31a-bd0cd40e1ec7" />

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
<img width="365" height="153" alt="image" src="https://github.com/user-attachments/assets/1c02a529-1714-4fd9-8aee-894ab46b99b6" />
 
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
<img width="442" height="275" alt="image" src="https://github.com/user-attachments/assets/fbe6c7be-23b2-4564-974b-22c1274ffa2a" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="767" height="275" alt="image" src="https://github.com/user-attachments/assets/de158af2-0925-4bd5-93dc-4bc78567fd06" />



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
<img width="492" height="81" alt="image" src="https://github.com/user-attachments/assets/6956dd17-4ed7-4248-a41f-d75269946777" />

 
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
 <img width="513" height="331" alt="image" src="https://github.com/user-attachments/assets/2a724414-2e97-43ea-b9e1-cb235ac739d5" />

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
 <img width="533" height="448" alt="image" src="https://github.com/user-attachments/assets/4b8ea5a8-0fb2-4c81-a3fd-5cfdb025ff9e" />

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
 <img width="555" height="385" alt="image" src="https://github.com/user-attachments/assets/b6d71efe-58cd-4ab7-83f1-40abafd168d7" />

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
<img width="421" height="125" alt="image" src="https://github.com/user-attachments/assets/50ab8cf1-8c15-404e-a786-735d9ac466c6" />


# RESULT:
The Commands are executed successfully.
