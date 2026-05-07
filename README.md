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
<img width="278" height="145" alt="image" src="https://github.com/user-attachments/assets/7333d0c8-9f3e-4906-8e9a-537d46ae61ac" />



cat < file2
## OUTPUT
<img width="377" height="168" alt="image" src="https://github.com/user-attachments/assets/a01e2b77-34b8-4c1d-8a02-40610c648ecd" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="412" height="97" alt="image" src="https://github.com/user-attachments/assets/821e713b-2a8e-4fce-90bb-52c339176d0d" />

 
comm file1 file2
 ## OUTPUT
 <img width="375" height="228" alt="image" src="https://github.com/user-attachments/assets/41831d56-28f0-476e-99a3-8d06875b3c42" />


 
diff file1 file2
## OUTPUT
<img width="357" height="287" alt="image" src="https://github.com/user-attachments/assets/2e05e21c-3c04-4600-a538-d747818e53ef" />


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
<img width="299" height="111" alt="image" src="https://github.com/user-attachments/assets/481d1d80-91dd-4b75-a5e4-0fa6994282cf" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="318" height="128" alt="image" src="https://github.com/user-attachments/assets/fab657f4-398f-4537-a2da-c99ef9a670a2" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="375" height="131" alt="image" src="https://github.com/user-attachments/assets/a2da8336-6d71-494a-90a6-bd4fa28ad09f" />



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
<img width="305" height="81" alt="image" src="https://github.com/user-attachments/assets/8ed00f4f-d7ac-4f6c-93e1-d30992cbc2cd" />


grep hello newfile 
## OUTPUT
<img width="331" height="102" alt="image" src="https://github.com/user-attachments/assets/41bf6cc7-707c-48e6-b882-a9a437668aa2" />



grep -v hello newfile 
## OUTPUT
<img width="324" height="83" alt="image" src="https://github.com/user-attachments/assets/86dd8d2e-a2f7-4de7-9807-85fc60ab8688" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="443" height="99" alt="image" src="https://github.com/user-attachments/assets/cc053349-7673-46f1-87b5-0c96e9d3509a" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="486" height="82" alt="image" src="https://github.com/user-attachments/assets/53c2509e-38a2-4a78-8e20-b907214d6acc" />



grep -R ubuntu /etc
## OUTPUT

<img width="950" height="292" alt="image" src="https://github.com/user-attachments/assets/fb38b426-774c-467b-968a-b9c3d81962f4" />


grep -w -n world newfile   
## OUTPUT
<img width="470" height="108" alt="image" src="https://github.com/user-attachments/assets/a379a3c6-cfee-4f32-996a-5d02e07e9db9" />


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
<img width="549" height="97" alt="image" src="https://github.com/user-attachments/assets/2f205066-e6c8-4203-a552-5d750cd5591c" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="507" height="126" alt="image" src="https://github.com/user-attachments/assets/d89a6bec-4b21-4859-be52-dcd21662e678" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="577" height="102" alt="image" src="https://github.com/user-attachments/assets/a1eaadb6-22c6-4519-92b8-bd1591ea248f" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="529" height="130" alt="image" src="https://github.com/user-attachments/assets/47f189ae-520e-470e-b969-544099421e20" />



egrep '(world$)' newfile 
## OUTPUT
<img width="518" height="129" alt="image" src="https://github.com/user-attachments/assets/1bffcf87-3f57-4535-abb0-9d8ad368d7d0" />



egrep '(World$)' newfile 
## OUTPUT
<img width="535" height="95" alt="image" src="https://github.com/user-attachments/assets/831334ee-2654-4554-9317-23421d04627b" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="552" height="132" alt="image" src="https://github.com/user-attachments/assets/801a2617-c69a-41b7-a447-6225344aeb97" />



egrep '[1-9]' newfile 
## OUTPUT



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="664" height="77" alt="image" src="https://github.com/user-attachments/assets/ee9e32fd-4fec-4b6c-a904-1cb3b3710baa" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="572" height="92" alt="image" src="https://github.com/user-attachments/assets/f56d8f51-41c4-4851-b314-a3ceb74800eb" />


egrep l{2} newfile
## OUTPUT
<img width="528" height="101" alt="image" src="https://github.com/user-attachments/assets/cdcfc672-2b56-4bb1-af90-e7cac0096d62" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="497" height="127" alt="image" src="https://github.com/user-attachments/assets/aa309b1d-cabe-496f-97c9-4a97d6f8d008" />


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

<img width="486" height="83" alt="image" src="https://github.com/user-attachments/assets/c39f30c4-b651-4b54-85b2-eba3d9b8ec80" />



sed -n -e '$p' file23
## OUTPUT
<img width="571" height="80" alt="image" src="https://github.com/user-attachments/assets/1145d8e7-30c4-477c-87d5-192bc5ce6da4" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="626" height="259" alt="image" src="https://github.com/user-attachments/assets/234a68d8-c763-4062-aa72-7158df0a36ec" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="666" height="260" alt="image" src="https://github.com/user-attachments/assets/9686bb3a-6c97-42d6-aab5-656a0df093d8" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="646" height="264" alt="image" src="https://github.com/user-attachments/assets/b740d508-3c39-4476-b420-e227dba09ea3" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="583" height="189" alt="image" src="https://github.com/user-attachments/assets/8aaf4e6a-c550-4704-b5d9-546ddc985327" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="525" height="140" alt="image" src="https://github.com/user-attachments/assets/c64e1012-0d9d-49e7-9072-61a2b32d5f7c" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="603" height="108" alt="image" src="https://github.com/user-attachments/assets/8811b49f-b5d8-4b17-b903-a9dabd26e6cb" />



seq 10 
## OUTPUT
<img width="544" height="312" alt="image" src="https://github.com/user-attachments/assets/090c9f7c-f4dc-4bef-965a-52bf6aba8297" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="441" height="140" alt="image" src="https://github.com/user-attachments/assets/0692707c-8875-4f7e-b523-e819f42d877a" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="548" height="129" alt="image" src="https://github.com/user-attachments/assets/094f60e3-db37-4f39-8b95-fb01219ed9e9" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="524" height="153" alt="image" src="https://github.com/user-attachments/assets/c8511cc9-2540-4985-b727-1a0f518e6fbb" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="551" height="124" alt="image" src="https://github.com/user-attachments/assets/aebbb666-337a-4f42-8e1d-38d821e3df57" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="587" height="128" alt="image" src="https://github.com/user-attachments/assets/86642e93-66cb-4675-b4b8-92f4cedb2a2b" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="469" height="135" alt="image" src="https://github.com/user-attachments/assets/c4c0738f-9ee6-4990-9489-4ecfa600d3b2" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="583" height="134" alt="image" src="https://github.com/user-attachments/assets/4554240f-36a0-4f3e-873d-6766669b9a01" />


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
<img width="558" height="173" alt="image" src="https://github.com/user-attachments/assets/6a319849-1be1-4b1b-9cb6-936167d97322" />


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
<img width="525" height="189" alt="image" src="https://github.com/user-attachments/assets/b1827e48-332b-4d25-98ef-a4188b77dede" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 <img width="603" height="257" alt="image" src="https://github.com/user-attachments/assets/d0abded6-c160-4947-ade4-671a8349fd64" />


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
<img width="665" height="134" alt="image" src="https://github.com/user-attachments/assets/596a3bee-fefd-4a9c-934c-f291dbe80b09" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="528" height="148" alt="image" src="https://github.com/user-attachments/assets/bc4ee545-d4e4-4d68-a9af-a4b3dbcf9b8e" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="650" height="231" alt="image" src="https://github.com/user-attachments/assets/6ac8df39-0021-45a1-bbec-8a6123304a7a" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="757" height="199" alt="image" src="https://github.com/user-attachments/assets/cb615b4f-b280-40e9-8fc6-c02823875e8b" />


tar -xvf backup.tar
## OUTPUT
<img width="813" height="112" alt="image" src="https://github.com/user-attachments/assets/7685135c-cf8c-435d-93d6-4f17f513806f" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="632" height="88" alt="image" src="https://github.com/user-attachments/assets/44c60f22-a666-4360-b0ea-8a5151a2ca6c" />

gunzip backup.tar.gz
## OUTPUT
<img width="643" height="80" alt="image" src="https://github.com/user-attachments/assets/bf7073b9-773a-4da5-8258-fc916e23b397" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
./my-script.sh
## OUTPUT
<img width="411" height="84" alt="image" src="https://github.com/user-attachments/assets/6e7ecfbc-d99f-45ce-9a41-65066c4cc58e" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="481" height="135" alt="image" src="https://github.com/user-attachments/assets/0644df30-0500-4720-9316-3c590b139746" />


cat > scriptest.sh 
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
<img width="606" height="389" alt="image" src="https://github.com/user-attachments/assets/9701e640-9d0b-4556-8915-63563a7641e8" />

 
ls file1
## OUTPUT
<img width="551" height="84" alt="image" src="https://github.com/user-attachments/assets/cc34c4af-1a37-43d1-9fc7-53e531635ab5" />

echo $?
## OUTPUT 
<img width="502" height="81" alt="image" src="https://github.com/user-attachments/assets/9a13df21-e8be-43a6-a251-6a398b62168b" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="592" height="84" alt="image" src="https://github.com/user-attachments/assets/4991b659-c737-4d56-b9dd-83c76078787b" />

abcd
 
echo $?
 ## OUTPUT
<img width="599" height="78" alt="image" src="https://github.com/user-attachments/assets/9149abfe-71ce-42b2-8d72-d93de9275ede" />


 
# mis-using string comparisons

cat > strcomp.sh 
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

<img width="799" height="286" alt="image" src="https://github.com/user-attachments/assets/090d2f27-8190-4d74-ac0d-f40b768ae527" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="697" height="90" alt="image" src="https://github.com/user-attachments/assets/01124ba9-3cff-48d3-8dde-be2d6494e069" />


# check file ownership
cat > psswdperm.sh 
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
<img width="715" height="80" alt="image" src="https://github.com/user-attachments/assets/5a59efee-08c6-446f-abad-259c89d047e9" />

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
<img width="783" height="147" alt="image" src="https://github.com/user-attachments/assets/83f2846c-5fce-4137-8b88-bf593f556ac9" />



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
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
<img width="626" height="113" alt="image" src="https://github.com/user-attachments/assets/cf548511-d7b5-4d5f-9726-bd8ad07d7725" />

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
<img width="802" height="142" alt="image" src="https://github.com/user-attachments/assets/2622e128-b007-4f16-950e-17a70990d127" />

# looking for a possible value using elif
cat > elifcheck.sh 
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
<img width="565" height="85" alt="image" src="https://github.com/user-attachments/assets/724184de-cbdc-42b8-b309-8135f6092053" />


# testing compound comparisons
cat > ifcompound.sh 
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
<img width="597" height="86" alt="image" src="https://github.com/user-attachments/assets/18f63df2-0089-493c-bb93-315357f6ae37" />

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

## OUTPUT
<img width="688" height="309" alt="image" src="https://github.com/user-attachments/assets/824c680f-8904-4fc8-b496-9d52de2f29b4" />

 
 
cat > untiltest.sh 
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
 
 
 
cat > forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat > forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat > forin2.sh 
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

##OUTPUT
<img width="594" height="153" alt="image" src="https://github.com/user-attachments/assets/28ee9c91-9491-4a07-a7a3-da54a8e0caad" />

 
cat > forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat > forin1.sh 
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
<img width="757" height="214" alt="image" src="https://github.com/user-attachments/assets/5e80c58d-3b82-4adc-86fe-d117909c3a39" />

cat > forinfile.sh 
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
<img width="721" height="235" alt="image" src="https://github.com/user-attachments/assets/07636162-cb29-48e3-ab09-95fd2fe95fe6" />



cat > forctype.sh 
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
<img width="678" height="186" alt="image" src="https://github.com/user-attachments/assets/19aa32df-a2f1-49f4-a884-86e4c2f00a4d" />

cat > forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype1.sh
$ ./forctype1.sh 
## OUTPUT
<img width="636" height="193" alt="image" src="https://github.com/user-attachments/assets/c15fd4a4-63c8-45a0-b03f-facd673b7194" />

cat > fornested1.sh 
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
<img width="839" height="353" alt="image" src="https://github.com/user-attachments/assets/134352ba-c569-4b6d-b5dd-fdd8882676f9" />

 
cat > forbreak.sh 
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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

## OUTPUT
<img width="806" height="134" alt="image" src="https://github.com/user-attachments/assets/fb4d5369-0669-45b2-81e4-fd085e210f9e" />

 
cat > forcontinue.sh 
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
<img width="831" height="214" alt="image" src="https://github.com/user-attachments/assets/5ab0cba2-5452-4731-88e2-07e5abb364ef" />

 
cat > exread.sh 
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
<img width="694" height="112" alt="image" src="https://github.com/user-attachments/assets/cbf893b9-99c3-47dd-b10a-150f6213f52e" />


 cat > exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 
## OUTPUT
<img width="682" height="118" alt="image" src="https://github.com/user-attachments/assets/4991ad96-3130-46e7-8c48-7540bc5ad67e" />

 
 
cat > funcex.sh
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
echo "Usage: badtest1 a b"c
fi
```
 ./funcex.sh 
 ck
## OUTPUT chmod
<img width="762" height="79" alt="image" src="https://github.com/user-attachments/assets/06ba6f1d-38d4-4eca-9b6f-58c4fa6bbb74" />


 
cat > argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3

## OUTPUT
<img width="437" height="121" alt="image" src="https://github.com/user-attachments/assets/cda51196-131a-478d-a4d0-b9ce572fdd7f" />


 
 cat > argshift1.sh
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

$ ./argshift.sh 1 2 3

## OUTPUT
<img width="720" height="137" alt="image" src="https://github.com/user-attachments/assets/316c36a5-7a10-487f-9622-e5bd9fe77d8e" />

 
cat > argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
 ./argshift.sh 1 2 3
## OUTPUT
<img width="703" height="403" alt="image" src="https://github.com/user-attachments/assets/25cbb96e-0d81-4729-9434-17c909a1acb9" />


 
 
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
<img width="832" height="392" alt="image" src="https://github.com/user-attachments/assets/c49da8ad-13a5-4d65-be55-6f4470466dd1" />
 
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
elsech
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
<img width="626" height="132" alt="image" src="https://github.com/user-attachments/assets/134c688a-e5bc-4541-a75a-c159298c15cd" />




# RESULT:
The Commands are executed successfully.
