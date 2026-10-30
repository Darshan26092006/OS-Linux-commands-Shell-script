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
<img width="270" height="167" alt="image" src="https://github.com/user-attachments/assets/3a9dfce6-dd63-4eb5-a96b-9f554f061dbb" />



cat < file2
## OUTPUT
<img width="257" height="172" alt="image" src="https://github.com/user-attachments/assets/8bbdab02-54c6-4d32-9f46-e79e73acfeef" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="373" height="82" alt="image" src="https://github.com/user-attachments/assets/c9b410cc-3f0b-40ca-8c49-36803339dee7" />
 
comm file1 file2
 ## OUTPUT
<img width="327" height="282" alt="image" src="https://github.com/user-attachments/assets/813f6d99-d877-43d0-913d-1f5c9c4dd781" />

 
diff file1 file2
## OUTPUT
<img width="317" height="317" alt="image" src="https://github.com/user-attachments/assets/256caa1d-4c40-444b-9abc-c52c0c98acfa" />


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
<img width="323" height="143" alt="image" src="https://github.com/user-attachments/assets/ad4a6808-f34b-4275-a896-5d74290cdee5" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="392" height="155" alt="image" src="https://github.com/user-attachments/assets/005fbf9e-354c-48ac-8094-1409df352092" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="400" height="140" alt="image" src="https://github.com/user-attachments/assets/621b4714-aaa9-4bd1-9df5-d636f81d5320" />


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
<img width="345" height="92" alt="image" src="https://github.com/user-attachments/assets/f684f645-ac50-4d5a-97ae-63726df147f9" />



grep hello newfile 
## OUTPUT

<img width="352" height="68" alt="image" src="https://github.com/user-attachments/assets/f350ffc1-07d4-431f-aa88-7e0358e62221" />



grep -v hello newfile 
## OUTPUT
<img width="377" height="97" alt="image" src="https://github.com/user-attachments/assets/5918da41-5788-4859-9e12-b90bd92a2b91" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="456" height="96" alt="image" src="https://github.com/user-attachments/assets/45355a30-b3ea-4dae-bc90-040f6dd06f86" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="402" height="105" alt="image" src="https://github.com/user-attachments/assets/f853e8f5-7efe-4e4c-be01-b3e7d2e1175d" />




grep -w -n world newfile   
## OUTPUT

<img width="402" height="105" alt="image" src="https://github.com/user-attachments/assets/9d2dd3c0-de6c-4e7d-a0ea-0c6e871488f2" />

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

<img width="461" height="98" alt="image" src="https://github.com/user-attachments/assets/c4aee43e-fb12-4e8c-80a0-bdd8085271cf" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="450" height="90" alt="image" src="https://github.com/user-attachments/assets/2900d8b7-81a4-407e-9f0d-20f18f199eb0" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="498" height="95" alt="image" src="https://github.com/user-attachments/assets/125a28f2-e4d1-48af-8635-066867dcdfa2" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="425" height="76" alt="image" src="https://github.com/user-attachments/assets/7a20cbc6-91c3-4ada-8543-ceba306b8fef" />


egrep '(world$)' newfile 
## OUTPUT

<img width="397" height="90" alt="image" src="https://github.com/user-attachments/assets/b2a671f2-32f7-4bad-ac0d-fe37c44855d0" />


egrep '(World$)' newfile 
## OUTPUT
<img width="408" height="68" alt="image" src="https://github.com/user-attachments/assets/be88f079-73e4-403d-b75b-7c8cf6285c4d" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="442" height="117" alt="image" src="https://github.com/user-attachments/assets/603f5e7e-e677-46c6-8399-66bbe515448f" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="368" height="67" alt="image" src="https://github.com/user-attachments/assets/92daa6d2-db7f-4e1b-be77-a1dfadbce9c9" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="450" height="77" alt="image" src="https://github.com/user-attachments/assets/5c8cd385-60d1-463f-b4bd-3fe9b483b218" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="437" height="75" alt="image" src="https://github.com/user-attachments/assets/036f7b5b-2221-452e-916c-f267544ada60" />

egrep l{2} newfile
## OUTPUT

<img width="353" height="92" alt="image" src="https://github.com/user-attachments/assets/1f6f499c-1cb3-4b68-8109-de56ce29bb4e" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="396" height="120" alt="image" src="https://github.com/user-attachments/assets/7e072876-dd6f-46c6-bdf9-b70fac2c618e" />


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

<img width="367" height="72" alt="image" src="https://github.com/user-attachments/assets/16e3893b-58e4-40c0-a755-dc09e0d313aa" />


sed -n -e '$p' file23
## OUTPUT
<img width="382" height="82" alt="image" src="https://github.com/user-attachments/assets/575ee7ec-3947-453e-bbd0-9c2193d1b0d2" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="465" height="251" alt="image" src="https://github.com/user-attachments/assets/6d8e245f-bf26-4510-80c0-a6d05cd59aeb" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="461" height="243" alt="image" src="https://github.com/user-attachments/assets/86c8c6d8-7ead-42d6-8455-f3c74bdda7f5" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="477" height="250" alt="image" src="https://github.com/user-attachments/assets/2a0eee60-e1c6-4844-bf44-6e2262867e3e" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="410" height="163" alt="image" src="https://github.com/user-attachments/assets/866407cb-9fd0-422b-8257-f559ed681bfd" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="428" height="120" alt="image" src="https://github.com/user-attachments/assets/3433e9a4-c7db-4b9b-9020-2b3740fcf895" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="486" height="95" alt="image" src="https://github.com/user-attachments/assets/4a1765db-4adc-4118-81ba-9726eb261a21" />



seq 10 
## OUTPUT
<img width="297" height="265" alt="image" src="https://github.com/user-attachments/assets/1f2d63c2-ca98-466b-9e85-07b715e22844" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="376" height="113" alt="image" src="https://github.com/user-attachments/assets/32940897-e8e0-4553-8ed2-feeba0c878de" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="402" height="115" alt="image" src="https://github.com/user-attachments/assets/4de60cfa-17bd-4d5c-80f0-1629f6e6bf68" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="400" height="148" alt="image" src="https://github.com/user-attachments/assets/7cb81cc4-2488-4c60-b52d-f216cb06f825" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="410" height="117" alt="image" src="https://github.com/user-attachments/assets/feabea92-fa09-4e8f-8db0-da3bc0f7f9c5" />



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
<img width="327" height="177" alt="image" src="https://github.com/user-attachments/assets/133f3fee-dcce-47aa-99af-bd4a1fdc715c" />


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

<img width="423" height="150" alt="image" src="https://github.com/user-attachments/assets/27ae41a2-869d-427d-86c7-46c12438005f" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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

<img width="555" height="147" alt="image" src="https://github.com/user-attachments/assets/83947b96-3dc0-4d5c-99e3-999a16ca15a9" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="555" height="147" alt="image" src="https://github.com/user-attachments/assets/db7880f7-6561-4be4-8e3b-b35acb586aa7" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="371" height="251" alt="image" src="https://github.com/user-attachments/assets/40475081-0b31-4e29-8cc3-25ea91bc7d24" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="645" height="305" alt="image" src="https://github.com/user-attachments/assets/01950493-8ca8-4850-8d4c-f1f9532bed2d" />


tar -xvf backup.tar
## OUTPUT
<img width="438" height="245" alt="image" src="https://github.com/user-attachments/assets/79179af7-f060-41f7-86e9-968a23d223c0" />



 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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
<img width="503" height="865" alt="image" src="https://github.com/user-attachments/assets/7600bad6-d5bd-45c2-89be-24e4ae68891e" />

 
ls file1
## OUTPUT
<img width="247" height="85" alt="image" src="https://github.com/user-attachments/assets/2e5aba82-0222-455d-9b21-21c9855b44e8" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 <img width="252" height="73" alt="image" src="https://github.com/user-attachments/assets/33456702-7840-4037-97d4-4fe50a5bfd61" />


 
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
<img width="411" height="200" alt="image" src="https://github.com/user-attachments/assets/e0e0f766-b51a-4439-8039-dc4ebc2869fd" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="362" height="111" alt="image" src="https://github.com/user-attachments/assets/9a9ed465-6350-4e8a-ab41-0a66b3685a5d" />


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
<img width="388" height="80" alt="image" src="https://github.com/user-attachments/assets/e1cb8e48-155a-4e96-b3dd-f24d93830c8d" />

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

<img width="428" height="90" alt="image" src="https://github.com/user-attachments/assets/a5dcdeb3-793b-4f04-b2bd-1dc552a5cdf0" />


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
<img width="393" height="127" alt="image" src="https://github.com/user-attachments/assets/05bfefa0-0f54-4047-bde5-b07073ad3160" />

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
<img width="422" height="133" alt="image" src="https://github.com/user-attachments/assets/654c9161-ad44-455d-988b-8370d9461b27" />

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
<img width="430" height="182" alt="image" src="https://github.com/user-attachments/assets/e1c9e380-0ed9-47ce-a22c-3512034089d3" />


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
<img width="438" height="110" alt="image" src="https://github.com/user-attachments/assets/6e6f3eb5-5164-4a62-985a-6fe07b01aea3" />

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
<img width="631" height="256" alt="image" src="https://github.com/user-attachments/assets/84a17140-c8b0-45cf-bebf-ed59b4822115" />
 
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
<img width="377" height="305" alt="image" src="https://github.com/user-attachments/assets/06e902bb-29bc-4cf8-871b-f7dc8a6dabdf" />
 
 
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
 <img width="435" height="160" alt="image" src="https://github.com/user-attachments/assets/7abd1e14-02b2-4c27-92e1-c99aaf857194" />

 
 
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
 <img width="390" height="210" alt="image" src="https://github.com/user-attachments/assets/fc9dd4b1-966f-4c16-9ef6-5cc2537f69da" />

 
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
<img width="377" height="151" alt="image" src="https://github.com/user-attachments/assets/dd730dfd-f2d6-42ff-b059-92ae71494b1c" />
 
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
 <img width="405" height="218" alt="image" src="https://github.com/user-attachments/assets/1ab39313-d588-4fd5-bfd4-f1a94538ae8e" />

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
<img width="385" height="210" alt="image" src="https://github.com/user-attachments/assets/1b8572d2-2cc9-4c87-8526-e48f85db7a59" />

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
<img width="393" height="200" alt="image" src="https://github.com/user-attachments/assets/439e27ca-b455-42ce-b9a5-8e46441df34a" />

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
<img width="392" height="191" alt="image" src="https://github.com/user-attachments/assets/402eab64-fdbf-4b1d-9f67-d1a83698af8e" />

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
<img width="437" height="335" alt="image" src="https://github.com/user-attachments/assets/c5479771-02e7-4fe6-bb84-351303926299" />

 
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
<img width="393" height="142" alt="image" src="https://github.com/user-attachments/assets/326aa223-c7c0-4849-9108-a672fdd5a5f1" />

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
<img width="1600" height="534" alt="image" src="https://github.com/user-attachments/assets/28d7669d-6773-4b01-9071-802abd4826ec" />


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
<img width="376" height="97" alt="image" src="https://github.com/user-attachments/assets/612605e8-0fd3-4736-8060-1a383ea0a886" />

 
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
 <img width="396" height="143" alt="image" src="https://github.com/user-attachments/assets/017bbff1-a7a4-4ffa-821e-7b1bfea69d8d" />

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
<img width="405" height="142" alt="image" src="https://github.com/user-attachments/assets/646f7fce-76a6-4e7a-8270-1626c209a666" />

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
<img width="407" height="350" alt="image" src="https://github.com/user-attachments/assets/084ae508-2610-402f-a85c-56d369ae1ddb" />
 
 
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
 <img width="376" height="65" alt="image" src="https://github.com/user-attachments/assets/487f9a9d-b8f0-49f1-b3bb-9d717756d2f6" />

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
<img width="407" height="138" alt="image" src="https://github.com/user-attachments/assets/2ac32bd8-3d69-4094-8801-c1eb25f0df9e" />


# RESULT:
The Commands are executed successfully.
