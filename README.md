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
<img width="297" height="201" alt="image" src="https://github.com/user-attachments/assets/8a54cadc-9837-409b-947b-9da36b280a16" />



cat < file2
## OUTPUT
<img width="299" height="246" alt="image" src="https://github.com/user-attachments/assets/bb317c3e-5d31-4100-8ae6-e93b90e2b6d5" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="457" height="102" alt="image" src="https://github.com/user-attachments/assets/53828fc9-30b8-48fa-bbec-85cb907a71d6" />
 
comm file1 file2
 ## OUTPUT
<img width="425" height="344" alt="image" src="https://github.com/user-attachments/assets/e130c4ed-2c2f-45d9-adb7-4532770ac10c" />

 
diff file1 file2
## OUTPUT
<img width="347" height="165" alt="Screenshot 2025-09-10 082210" src="https://github.com/user-attachments/assets/77232901-83e2-47ab-976e-acf3b3311d6b" />



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

<img width="395" height="181" alt="image" src="https://github.com/user-attachments/assets/ef567ccf-881d-4ef9-82c0-e9b74057bc20" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="380" height="197" alt="image" src="https://github.com/user-attachments/assets/dc2f21ac-1a81-4d76-a018-93099d140b0b" />



cut -d "|" -f 2 file22
## OUTPUT


<img width="346" height="92" alt="image" src="https://github.com/user-attachments/assets/c3615579-4abe-470b-ab1c-0e0a07c76d0b" />

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

<img width="317" height="237" alt="image" src="https://github.com/user-attachments/assets/5feeeecf-a03f-4d08-9788-02b4c2520966" />



grep hello newfile 
## OUTPUT


<img width="369" height="103" alt="image" src="https://github.com/user-attachments/assets/d032acfd-324c-490c-9c39-a7d1d9b57400" />



grep -v hello newfile 
## OUTPUT


<img width="470" height="131" alt="image" src="https://github.com/user-attachments/assets/642511e9-92e4-4aad-9dc6-73db7139ae09" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="518" height="70" alt="image" src="https://github.com/user-attachments/assets/6ea1f0cc-b65a-4d31-bb8b-bd8b90314b66" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="1025" height="581" alt="image" src="https://github.com/user-attachments/assets/41390e73-b4fa-454d-b9e6-39bd3c028131" />



grep -R ubuntu /etc
## OUTPUT

<img width="396" height="124" alt="image" src="https://github.com/user-attachments/assets/fc3efe53-917a-4089-8201-5b8610b8385b" />



grep -w -n world newfile   
## OUTPUT

<img width="459" height="127" alt="image" src="https://github.com/user-attachments/assets/8c45515a-02e3-4589-861a-24ad00dfe38b" />

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

<img width="468" height="123" alt="image" src="https://github.com/user-attachments/assets/d33f6149-bc7f-4436-9a52-ea9b550f28d4" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="518" height="130" alt="image" src="https://github.com/user-attachments/assets/f14f2093-b410-44d5-bd04-fb261a88784e" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="416" height="99" alt="image" src="https://github.com/user-attachments/assets/7929862e-faa0-48d1-8e52-25d6ddd5922f" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="389" height="122" alt="image" src="https://github.com/user-attachments/assets/726e1c6e-4f46-4cdf-bd02-140c9df93773" />


egrep '(world$)' newfile 
## OUTPUT

<img width="451" height="170" alt="image" src="https://github.com/user-attachments/assets/7199090b-40a2-41f1-af91-16e53507271d" />



egrep '(World$)' newfile 
## OUTPUT

<img width="394" height="101" alt="image" src="https://github.com/user-attachments/assets/d5a1af41-74a9-43ba-909f-6bddcdba6ae6" />


egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="445" height="97" alt="image" src="https://github.com/user-attachments/assets/5d5a3ca6-8cbd-449e-a53d-3fd5603d3074" />


egrep '[1-9]' newfile 
## OUTPUT


<img width="455" height="94" alt="image" src="https://github.com/user-attachments/assets/f9e79214-1819-41b8-9078-94bd46063721" />


egrep 'Linux.*world' newfile 
## OUTPUT


<img width="328" height="136" alt="image" src="https://github.com/user-attachments/assets/00baca6b-7030-47be-81ad-f2e23b6c970e" />


egrep 'Linux.*World' newfile 
## OUTPUT


<img width="364" height="160" alt="image" src="https://github.com/user-attachments/assets/13a4b49b-63d8-42e0-994a-800cd2b807ef" />

egrep l{2} newfile
## OUTPUT


<img width="366" height="104" alt="image" src="https://github.com/user-attachments/assets/1849d66b-5227-4b7c-9ba6-205dc3aed587" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="359" height="106" alt="image" src="https://github.com/user-attachments/assets/6f8e7586-4326-42ea-ab59-22e20115ded3" />


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

<img width="436" height="309" alt="image" src="https://github.com/user-attachments/assets/83419246-bfef-4de1-ad8a-9eebafa0460d" />



sed -n -e '$p' file23
## OUTPUT


<img width="459" height="328" alt="image" src="https://github.com/user-attachments/assets/9ce33a16-2080-4ba4-8dcf-1a4708f715e0" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="472" height="317" alt="image" src="https://github.com/user-attachments/assets/d0e203fd-e7ba-4756-8f25-aa7ebbc93182" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="402" height="224" alt="image" src="https://github.com/user-attachments/assets/28364c0e-2ee5-4493-a9dc-42ce0b7e27a4" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="427" height="165" alt="image" src="https://github.com/user-attachments/assets/2b3c8c4c-2406-4423-aaad-2ab793f08807" />


sed -n -e '1,5p' file23
## OUTPUT


<img width="491" height="125" alt="image" src="https://github.com/user-attachments/assets/425a309c-b0ea-4766-84ca-29dda14fbd4f" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="245" height="375" alt="image" src="https://github.com/user-attachments/assets/10e47057-eddd-4fec-91b6-468880c3471b" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="356" height="152" alt="image" src="https://github.com/user-attachments/assets/2be90f8c-b4d2-4553-9f4c-6ad5ad7c7a8d" />



seq 10 
## OUTPUT

<img width="378" height="153" alt="image" src="https://github.com/user-attachments/assets/87f4907a-f5ea-4cbc-be3e-4b365a0d437f" />



seq 10 | sed -n '4,6p'
## OUTPUT
seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="370" height="197" alt="image" src="https://github.com/user-attachments/assets/86cb79db-d24f-4e19-bedd-eee1782dd9f0" />



seq 3 | sed '2a hello'
## OUTPUT


<img width="381" height="151" alt="image" src="https://github.com/user-attachments/assets/9ec15eb5-202f-4b95-bf2c-4ad70742e71b" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="418" height="159" alt="image" src="https://github.com/user-attachments/assets/3013b786-d097-4304-a672-bca11996e892" />


seq 10 | sed '2,9c hello'
## OUTPUT


<img width="463" height="162" alt="image" src="https://github.com/user-attachments/assets/fdd71ef0-75ec-4e5f-b935-331b11dc7b8e" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="473" height="166" alt="image" src="https://github.com/user-attachments/assets/b3fb5fc4-765a-479d-8ed3-2e462cebefb7" />



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

<img width="380" height="221" alt="image" src="https://github.com/user-attachments/assets/cd3e73f6-45b0-4468-919b-9e102ba68374" />


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

<img width="392" height="225" alt="image" src="https://github.com/user-attachments/assets/7227734a-e7fb-4001-bcc9-bab57410bcc1" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="516" height="305" alt="image" src="https://github.com/user-attachments/assets/d0ae3df9-d8bb-444e-8846-31d3ed5aa5ec" />

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


<img width="438" height="170" alt="image" src="https://github.com/user-attachments/assets/3952097d-4d5b-459b-a4c4-73e4e292b354" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="383" height="89" alt="image" src="https://github.com/user-attachments/assets/665cb8ca-b4ff-44a1-82ba-77d80740ba4f" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="342" height="186" alt="image" src="https://github.com/user-attachments/assets/3da09b1a-d6ce-424c-bcd8-3fc920ee6322" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="794" height="190" alt="image" src="https://github.com/user-attachments/assets/36c44815-2879-4e16-a443-b35f1b2abff1" />


tar -xvf backup.tar
## OUTPUT

<img width="324" height="91" alt="image" src="https://github.com/user-attachments/assets/df8023ba-c1ba-4ce6-a004-24f689ecae61" />

gzip backup.tar

ls .gz
## OUTPUT

<img width="270" height="91" alt="image" src="https://github.com/user-attachments/assets/fb18d8a6-1b9e-4990-9c09-943a0ba6491f" />
 
gunzip backup.tar.gz
## OUTPUT

<img width="492" height="257" alt="image" src="https://github.com/user-attachments/assets/8b3fac5c-2819-491e-ab9e-e50f7d0b9768" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="317" height="94" alt="image" src="https://github.com/user-attachments/assets/49876988-20d9-431f-9c1d-9d9d04c3d92d" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="761" height="160" alt="image" src="https://github.com/user-attachments/assets/548d1676-9dbd-4bfd-9ffe-7adfca9ef1e1" />


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

<img width="608" height="102" alt="image" src="https://github.com/user-attachments/assets/4617b737-ccc8-499f-80bf-638e3919340a" />

 
ls file1
## OUTPUT

<img width="485" height="94" alt="image" src="https://github.com/user-attachments/assets/e4859b8f-9287-47e7-98ec-3b778480d286" />

echo $?
## OUTPUT 

<img width="431" height="166" alt="image" src="https://github.com/user-attachments/assets/049dd14a-c6ab-416d-839c-441c9ffe11c2" />

./one bash: ./one: Permission denied
echo $?
## OUTPUT 

 <img width="448" height="101" alt="image" src="https://github.com/user-attachments/assets/6a1b952f-7e5c-4405-838a-859b33f65032" />

abcd
 
echo $?
 ## OUTPUT

<img width="469" height="166" alt="image" src="https://github.com/user-attachments/assets/a41903fe-c4da-4be4-a442-278f85da2ba7" />


 
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
## OUTPUT

<img width="485" height="159" alt="image" src="https://github.com/user-attachments/assets/a77ad8b3-5aec-460a-a7b2-e2912643d662" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="855" height="376" alt="image" src="https://github.com/user-attachments/assets/7affde39-cd59-46b4-8d5e-8e91a6b30521" />


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

<img width="542" height="352" alt="image" src="https://github.com/user-attachments/assets/19941f14-1fa8-40f2-9f4c-f7a00ae8a6dc" />

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

<img width="804" height="159" alt="image" src="https://github.com/user-attachments/assets/a58ebdbf-0560-48ef-8424-8a084228f45f" />



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
 
$ ./iftest.sh ##OUTPUT

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
 
$ ./ifnested.sh ##OUTPUT

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

<img width="649" height="474" alt="image" src="https://github.com/user-attachments/assets/3d9a0496-a474-4fa0-8ba9-0189c161cb1f" />


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

<img width="833" height="602" alt="image" src="https://github.com/user-attachments/assets/b21c6b82-af88-4a0f-931c-14b8be43e0e7" />

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

<img width="619" height="483" alt="image" src="https://github.com/user-attachments/assets/e7df6cb9-4ae5-4e48-9e24-6f7a5eae009e" />

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

<img width="834" height="663" alt="image" src="https://github.com/user-attachments/assets/bf6c741e-f478-4f46-b4da-c852f46b4f20" />


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

<img width="874" height="439" alt="image" src="https://github.com/user-attachments/assets/8089646d-a194-42ef-8e68-544e5fccebcc" />

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

<img width="631" height="317" alt="image" src="https://github.com/user-attachments/assets/001a148a-fbc0-40e3-9c7b-aebcb144ea3e" />

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

<img width="470" height="97" alt="image" src="https://github.com/user-attachments/assets/2065f83d-b527-45a9-bd05-2fd30c770b41" />

 
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

<img width="458" height="104" alt="image" src="https://github.com/user-attachments/assets/87d09bce-b215-4d0a-8267-434c7e3bc7ef" />

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

<img width="802" height="107" alt="image" src="https://github.com/user-attachments/assets/29ae7bc2-703a-42ef-b631-99ef70115342" />
 
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

<img width="826" height="101" alt="image" src="https://github.com/user-attachments/assets/ab7db06b-b59a-4274-9073-7de912f43552" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="825" height="106" alt="image" src="https://github.com/user-attachments/assets/cbf47c96-e28d-401d-91e5-869394b3a9d6" />



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

<img width="366" height="468" alt="image" src="https://github.com/user-attachments/assets/2e90e766-ee91-402e-8ea9-1a9db96fbaf2" />

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

<img width="830" height="103" alt="image" src="https://github.com/user-attachments/assets/70f0ca93-fa7d-48ce-b76b-fc52d1a47ad3" />

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

<img width="807" height="93" alt="image" src="https://github.com/user-attachments/assets/a9689bd7-ec59-437f-997c-7d3284951a72" />

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

<img width="419" height="464" alt="image" src="https://github.com/user-attachments/assets/1d7fa737-86c0-4e68-a9d3-1897fea3736a" />

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

 ![Uploading image.png…]()

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
