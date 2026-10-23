# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting
NAME : SARVAJITH.S.S
REG.NO: 212225220091

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
<img width="270" height="167" alt="image" src="https://github.com/user-attachments/assets/16bd8a28-1423-4892-887d-fed40451f3ee" />



cat < file2
## OUTPUT
<img width="257" height="172" alt="image" src="https://github.com/user-attachments/assets/5e66027b-4def-4614-a25c-8dbaf78fbefa" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="373" height="82" alt="image" src="https://github.com/user-attachments/assets/13bd9b24-cf94-464a-9cb2-8bcae01e65a7" />

comm file1 file2
 ## OUTPUT
<img width="327" height="282" alt="image" src="https://github.com/user-attachments/assets/f19790fb-1fa4-4d9f-9f53-55e4af5dac24" />

 
diff file1 file2
## OUTPUT
<img width="317" height="317" alt="image" src="https://github.com/user-attachments/assets/0d9352a3-4d27-43e8-8d7e-36546818f854" />


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
<img width="323" height="143" alt="image" src="https://github.com/user-attachments/assets/c3d8e1cb-2035-4c60-965d-575d7ec427a6" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="392" height="155" alt="image" src="https://github.com/user-attachments/assets/589b9adc-a28e-4a67-a1ec-8517a8cc4c99" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="400" height="140" alt="image" src="https://github.com/user-attachments/assets/7a3680bc-e0ee-46d7-9008-26cf55420fea" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
```Hello world
hello world
```

grep Hello newfile 
## OUTPUT
<img width="345" height="92" alt="image" src="https://github.com/user-attachments/assets/330c8edf-4be6-4c5a-bb8a-f7991c1fab3b" />



grep hello newfile 
## OUTPUT
<img width="352" height="68" alt="image" src="https://github.com/user-attachments/assets/a4b4bb9b-b818-429f-8a8e-e9e1f753da47" />




grep -v hello newfile 
## OUTPUT
<img width="377" height="97" alt="image" src="https://github.com/user-attachments/assets/2dd25b07-e5ba-44ef-922f-086e7d090479" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="456" height="96" alt="image" src="https://github.com/user-attachments/assets/8621b684-0ac5-4bba-a5a1-57ba21ea47a6" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="498" height="77" alt="image" src="https://github.com/user-attachments/assets/9d6cbedb-f739-472c-8479-32f4e774cf33" />




grep -w -n world newfile   
## OUTPUT
<img width="402" height="105" alt="image" src="https://github.com/user-attachments/assets/273c2f57-a8b5-4153-b827-c30db128c8de" />


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
<img width="461" height="98" alt="image" src="https://github.com/user-attachments/assets/a41db2ee-bf83-4cbf-bbf1-ea4ab299db17" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="450" height="90" alt="image" src="https://github.com/user-attachments/assets/8c79b51f-daa5-446d-a6fd-9f58b0c60519" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="498" height="95" alt="image" src="https://github.com/user-attachments/assets/c0ef3d1b-258b-4004-9985-6e1e0c1219c8" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="425" height="76" alt="image" src="https://github.com/user-attachments/assets/a1c29b5c-b791-4e56-b17c-976f1a59a296" />



egrep '(world$)' newfile 
## OUTPUT
<img width="397" height="90" alt="image" src="https://github.com/user-attachments/assets/a33a0466-c0a2-44b3-9b67-7a75198b8136" />



egrep '(World$)' newfile 
## OUTPUT
<img width="408" height="68" alt="image" src="https://github.com/user-attachments/assets/b31e95b3-f8e0-4aa1-82c4-9cd197f462a4" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="442" height="117" alt="image" src="https://github.com/user-attachments/assets/f26657b8-3961-4680-b916-a27f6bd34e97" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="368" height="67" alt="image" src="https://github.com/user-attachments/assets/364ee874-56f9-41e9-90e2-7b52e55a0ad6" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="450" height="77" alt="image" src="https://github.com/user-attachments/assets/137c10a9-da9c-470f-a473-a7128877ef77" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="437" height="75" alt="image" src="https://github.com/user-attachments/assets/90f207d3-e5cc-453f-ab05-299e0dc59271" />


egrep l{2} newfile
## OUTPUT
<img width="353" height="92" alt="image" src="https://github.com/user-attachments/assets/d24d384f-2546-43f9-9e0e-c5498a042ac3" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="396" height="120" alt="image" src="https://github.com/user-attachments/assets/0d7384c2-c806-4fc6-9df8-dd48b8d1332e" />


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
<img width="367" height="72" alt="image" src="https://github.com/user-attachments/assets/96afb6f0-7321-41a4-a34a-d53b8311141f" />



sed -n -e '$p' file23
## OUTPUT
<img width="382" height="82" alt="image" src="https://github.com/user-attachments/assets/5bd32370-20f5-4cc2-aba2-5d59b332948f" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="465" height="251" alt="image" src="https://github.com/user-attachments/assets/89ba2e24-afa1-4db3-ab6b-6a407f0b9a3e" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="461" height="243" alt="image" src="https://github.com/user-attachments/assets/efc13210-7201-48de-a4c2-06b51704aed5" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="477" height="250" alt="image" src="https://github.com/user-attachments/assets/f1a5675b-b47b-439e-b689-ae25870b726b" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="410" height="163" alt="image" src="https://github.com/user-attachments/assets/dcf3451f-9343-434b-a441-13f1f9424e06" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="428" height="120" alt="image" src="https://github.com/user-attachments/assets/eaea0b28-4bab-4fd6-b68f-625081f71760" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="486" height="95" alt="image" src="https://github.com/user-attachments/assets/1e63b354-723d-490b-9f99-c154f4410287" />



seq 10 
## OUTPUT
<img width="297" height="265" alt="image" src="https://github.com/user-attachments/assets/b4b4c5a9-bcd7-4ad8-b440-57bb34f2b47e" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="376" height="113" alt="image" src="https://github.com/user-attachments/assets/33267421-9578-4d4d-a88b-8ea8606f693d" />



seq 10 | sed -n '2,4p'
## OUTPUT
<img width="402" height="115" alt="image" src="https://github.com/user-attachments/assets/682aa667-6026-4b75-b474-4bc87593897d" />





seq 3 | sed '2a hello'
## OUTPUT
<img width="400" height="148" alt="image" src="https://github.com/user-attachments/assets/bb413d14-a06f-4176-a700-1a52233da490" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="410" height="117" alt="image" src="https://github.com/user-attachments/assets/73691528-b532-48e6-a478-facec0ba0611" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="407" height="125" alt="image" src="https://github.com/user-attachments/assets/dbf7ae57-b363-4a75-b444-fef262495ea7" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="462" height="117" alt="image" src="https://github.com/user-attachments/assets/f26bfae5-b5ae-452c-8926-4d00cfd7c038" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="462" height="112" alt="image" src="https://github.com/user-attachments/assets/256bb8f1-33c9-413c-84de-a6a5b3bd92c1" />


# Sorting File content
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
<img width="327" height="177" alt="image" src="https://github.com/user-attachments/assets/b0502651-7233-4681-9cde-55e70bed5879" />


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
<img width="423" height="150" alt="image" src="https://github.com/user-attachments/assets/ce9848ae-04fb-4c48-aafa-3989d0db406e" />



# Using tr command

cat file23 | tr [:lower:] [:upper:]
## OUTPUT
<img width="532" height="242" alt="image" src="https://github.com/user-attachments/assets/7e7afe8d-311f-4812-b973-3b8d5912e6a1" />

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
<img width="427" height="153" alt="image" src="https://github.com/user-attachments/assets/ba2892f0-efd8-4efe-9c13-832581d4ce78" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="555" height="147" alt="image" src="https://github.com/user-attachments/assets/b2d6e732-7de9-43fe-93df-c18ebc53e966" />



# Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="371" height="251" alt="image" src="https://github.com/user-attachments/assets/0879233f-ad5f-4904-9c8e-a84cf8ca07ca" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="645" height="305" alt="image" src="https://github.com/user-attachments/assets/bbd05c70-5074-4747-9718-68bc7a1ff76b" />


tar -xvf backup.tar
## OUTPUT
<img width="438" height="245" alt="image" src="https://github.com/user-attachments/assets/d93af3a9-08d6-4197-a91e-2538c637bbd6" />



cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="337" height="136" alt="image" src="https://github.com/user-attachments/assets/a826827c-a3e3-4ab0-9530-b9417443d5af" />


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
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
<img width="503" height="865" alt="image" src="https://github.com/user-attachments/assets/fc09dfc8-4f09-4f0b-b674-4eac7034ca73" />
<img width="633" height="375" alt="image" src="https://github.com/user-attachments/assets/b9c071b1-b205-4afd-b380-90bd67548f30" />

 
ls file1
## OUTPUT
<img width="247" height="85" alt="image" src="https://github.com/user-attachments/assets/8bc1c59b-4b5a-4e7e-b641-4dc0f5459e9a" />

echo $?
## OUTPUT 
<img width="220" height="67" alt="image" src="https://github.com/user-attachments/assets/6b75a213-6229-4f1f-abdc-4475a863ff67" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="252" height="73" alt="image" src="https://github.com/user-attachments/assets/4b72fd59-a8f5-4b0c-8d31-9a55c32c968d" />

abcd
echo $?
## OUTPUT
<img width="302" height="87" alt="image" src="https://github.com/user-attachments/assets/fe83c64c-ceef-412d-9bc5-4b6215169d58" />


 
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
<img width="411" height="200" alt="image" src="https://github.com/user-attachments/assets/e54ed64e-59e9-4814-bffc-5b7f3443a36a" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="362" height="111" alt="image" src="https://github.com/user-attachments/assets/9cbc9553-009f-47a3-9660-7e24e702e318" />

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
<img width="388" height="80" alt="image" src="https://github.com/user-attachments/assets/2b7614f2-cacc-4fd5-836e-1d8ab926ffba" />

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
<img width="428" height="90" alt="image" src="https://github.com/user-attachments/assets/f9e73cbe-f545-4890-88ba-d7aa6062eb58" />



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
## OUTPUT
<img width="393" height="127" alt="image" src="https://github.com/user-attachments/assets/1df03820-4868-45db-a46f-c433a1272bdb" />


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
## OUTPUT
<img width="422" height="133" alt="image" src="https://github.com/user-attachments/assets/c9f2e151-f185-4b2c-be1a-3d80e470b35f" />

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
<img width="430" height="182" alt="image" src="https://github.com/user-attachments/assets/4f9a8150-6fb2-4147-ac41-8a6855eb2f05" />



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
<img width="438" height="110" alt="image" src="https://github.com/user-attachments/assets/f082e79e-bce3-4b90-9c44-f3aa12517185" />


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
## OUTPUT
<img width="631" height="256" alt="image" src="https://github.com/user-attachments/assets/e927bf20-5d87-46b9-bac9-cf4f4efd04ef" />


cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$(( $var1 - 1 ))
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
## OUTPUT
<img width="377" height="305" alt="image" src="https://github.com/user-attachments/assets/339ef27a-d189-457f-bdb5-7c08c49da686" />

 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$(( $var1 - 25 ))
done
``` 
$ chmod 755 untiltest.sh
## OUTPUT
<img width="435" height="160" alt="image" src="https://github.com/user-attachments/assets/c5f27224-e045-455d-b687-955a0d206406" />

 
 
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
## OUTPUT
<img width="390" height="210" alt="image" src="https://github.com/user-attachments/assets/e0111325-fcb2-49a9-8b12-57a180580eec" />

 
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
## OUTPUT
<img width="377" height="151" alt="image" src="https://github.com/user-attachments/assets/d20db400-f600-4524-9245-acaa8b015cd2" />

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
## OUTPUT 
<img width="377" height="151" alt="image" src="https://github.com/user-attachments/assets/6ac3f0b1-c754-41d1-b5d8-1c9a2c9b17ab" />

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
## OUTPUT 
<img width="405" height="218" alt="image" src="https://github.com/user-attachments/assets/5ff03e90-d595-4c31-b2c2-6dbcd125d938" />

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
<img width="385" height="210" alt="image" src="https://github.com/user-attachments/assets/c2180c40-8c70-4bd3-90d6-ac04b4817882" />

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
<img width="298" height="71" alt="image" src="https://github.com/user-attachments/assets/9b944145-be4d-4bd1-9e5a-a730d7a89800" />


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
$ bash forctype.sh 
## OUTPUT
<img width="393" height="200" alt="image" src="https://github.com/user-attachments/assets/51a8f699-f45b-49cb-b676-25153caf8941" />

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
$ bash forctype1.sh 
## OUTPUT
<img width="392" height="191" alt="image" src="https://github.com/user-attachments/assets/650c80e0-68e4-4483-854c-84cc77bb0204" />

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
<img width="437" height="335" alt="image" src="https://github.com/user-attachments/assets/f40eaf8c-4dbd-492c-8d75-c031974afe7e" />

 
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
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT
<img width="393" height="142" alt="image" src="https://github.com/user-attachments/assets/ebc9cb64-6d80-46dc-8f4a-8c573c9688cc" />

cat forcontinue.sh 
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
<img width="412" height="182" alt="image" src="https://github.com/user-attachments/assets/0a0e3648-629b-4f5a-aec7-b9c18c4bbfe1" />

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
<img width="440" height="126" alt="image" src="https://github.com/user-attachments/assets/09161aec-172c-42a9-a4db-9bd85ba3a8b2" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 


$ ./exread1.sh 
## OUTPUT
<img width="408" height="127" alt="image" src="https://github.com/user-attachments/assets/aa1c234c-aeef-4256-93e5-57e160eb869c" />

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
 $ chmod 755 funcex.sh
 
 ./funcex.sh 1 2
<img width="376" height="97" alt="image" src="https://github.com/user-attachments/assets/b8aff035-b0ca-481a-978b-1bdf577c56cc" />

 
cat argshift.sh
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
<img width="396" height="143" alt="image" src="https://github.com/user-attachments/assets/fe674029-cf01-492f-acf4-a51c7691d10d" />

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

$ ./argshift.sh 1 2 3
## OUTPUT
<img width="405" height="142" alt="image" src="https://github.com/user-attachments/assets/884d5af6-74c4-41bc-bf97-d3ff14936a8d" />

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

 ./argshift.sh 1 2 3
 ## OUTPUT
 <img width="407" height="350" alt="image" src="https://github.com/user-attachments/assets/4893674e-d6c5-4cc4-a20d-14755841228e" />

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
<img width="376" height="65" alt="image" src="https://github.com/user-attachments/assets/4838c2ce-8685-4f73-9a7f-301c7cecb3ce" />
 
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
<img width="407" height="138" alt="image" src="https://github.com/user-attachments/assets/769415da-6aa6-4d30-9c00-10b29f2232f8" />


# RESULT:
The Commands are executed successfully.
