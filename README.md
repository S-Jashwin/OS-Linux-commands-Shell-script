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

<img width="960" height="794" alt="image" src="https://github.com/user-attachments/assets/bac70728-7ade-4d1d-9243-ad5473b911cf" />







cat < file2
## OUTPUT
<img width="960" height="794" alt="image" src="https://github.com/user-attachments/assets/3e3df7d4-8a28-4da7-b1a5-03a3c1267a11" />




# Comparing Files
cmp file1 file2
## OUTPUT
<img width="1588" height="794" alt="image" src="https://github.com/user-attachments/assets/375d2767-2945-4686-a24d-b70cf4532cc4" />




 
comm file1 file2
 ## OUTPUT
<img width="1588" height="794" alt="image" src="https://github.com/user-attachments/assets/2269c91f-fab4-44b8-b4bb-cada4f92ff73" />

 
diff file1 file2
## OUTPUT
<img width="1540" height="479" alt="image" src="https://github.com/user-attachments/assets/25189baf-7b38-441b-a473-fde8fa740a7f" />


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

<img width="1689" height="375" alt="image" src="https://github.com/user-attachments/assets/83d81dc4-bc3d-4fa2-910a-d28a58d2aedd" />





cut -d "|" -f 1 file22
## OUTPUT
<img width="1013" height="192" alt="image" src="https://github.com/user-attachments/assets/92f8dc85-8b07-4e8c-bf11-bb157c1db8cd" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="963" height="194" alt="image" src="https://github.com/user-attachments/assets/053603c6-2e2e-4a28-890d-6aa1f5cbe86a" />


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
<img width="1664" height="281" alt="image" src="https://github.com/user-attachments/assets/de8e2cab-6895-4534-bb2c-b785b0f34e29" />



grep hello newfile 
## OUTPUT

<img width="1664" height="281" alt="image" src="https://github.com/user-attachments/assets/2a0c82f9-5112-4950-ac7a-cf9896cf00bb" />



grep -v hello newfile 
## OUTPUT

<img width="1470" height="165" alt="image" src="https://github.com/user-attachments/assets/fb40f288-386c-4d0e-b269-7e45fcf2ba03" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="1332" height="180" alt="image" src="https://github.com/user-attachments/assets/ca903541-efb3-4d7a-b5cc-ae8ab58914b7" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="1441" height="164" alt="image" src="https://github.com/user-attachments/assets/6cd74e98-7fa0-4308-8360-9e302f760a13" />



grep -R ubuntu /etc
## OUTPUT
<img width="1499" height="659" alt="image" src="https://github.com/user-attachments/assets/a6ebe2ad-30ec-4cdc-a09a-c321b4c092dd" />

<img width="1638" height="687" alt="image" src="https://github.com/user-attachments/assets/c14a4908-e1af-4307-a605-4de563ea5298" />

<img width="1613" height="661" alt="image" src="https://github.com/user-attachments/assets/2803ea65-1c85-4a2d-bd27-0d7defed6c1a" />

<img width="1570" height="716" alt="image" src="https://github.com/user-attachments/assets/e1393af2-12dc-4a1c-9d7d-181686114010" />




grep -w -n world newfile   
## OUTPUT

<img width="1564" height="310" alt="image" src="https://github.com/user-attachments/assets/de6c6eae-6e9b-43e2-b3c1-49930b0a7f0f" />



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

<img width="1572" height="494" alt="image" src="https://github.com/user-attachments/assets/4e73cdf9-49d5-4f20-aa7a-d37d694511c9" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="1572" height="494" alt="image" src="https://github.com/user-attachments/assets/350fb87b-4d49-4d13-a138-cd827d53432b" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="1656" height="702" alt="image" src="https://github.com/user-attachments/assets/5e2bdd6f-bc81-4f72-8b64-32a43bf10825" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="1656" height="702" alt="image" src="https://github.com/user-attachments/assets/d4470a40-4320-459c-a083-36571d8c803f" />


egrep '(world$)' newfile 
## OUTPUT
<img width="1656" height="702" alt="image" src="https://github.com/user-attachments/assets/9b306876-3838-4de2-a26d-f93bb9f6dce6" />



egrep '(World$)' newfile 
## OUTPUT
<img width="1656" height="702" alt="image" src="https://github.com/user-attachments/assets/c37159b9-79b8-475e-97cb-11cf212e33f9" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="1656" height="702" alt="image" src="https://github.com/user-attachments/assets/51b3015e-d407-4326-9e8d-f6c75b325135" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="1572" height="151" alt="image" src="https://github.com/user-attachments/assets/245823db-168b-4824-913f-04810df60923" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1396" height="423" alt="image" src="https://github.com/user-attachments/assets/4cabda63-cbf0-4277-bbc5-6e39cc6ae074" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1396" height="423" alt="image" src="https://github.com/user-attachments/assets/e11ee5da-2cd3-44df-a8eb-8b64700aee99" />


egrep l{2} newfile
## OUTPUT
<img width="1396" height="423" alt="image" src="https://github.com/user-attachments/assets/086c3549-970f-43f8-a5fb-5861ff942eae" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="1396" height="423" alt="image" src="https://github.com/user-attachments/assets/2aa5f276-ac37-48a1-93e9-644074e997bb" />


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
<img width="1155" height="170" alt="image" src="https://github.com/user-attachments/assets/ae9a65d0-16d5-4be6-a09e-99606ec5167a" />



sed -n -e '$p' file23
## OUTPUT
<img width="1489" height="227" alt="image" src="https://github.com/user-attachments/assets/bab6c19e-98e4-467a-be99-b9cb1a91586e" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1641" height="677" alt="image" src="https://github.com/user-attachments/assets/284c83a4-98e5-49d1-bba9-6f0b368d96af" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="1641" height="677" alt="image" src="https://github.com/user-attachments/assets/2a44d906-8c3c-4245-b14f-b788ffd26151" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="1417" height="487" alt="image" src="https://github.com/user-attachments/assets/58386f80-39f2-4bef-9132-00aa2181ddd6" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="1510" height="331" alt="image" src="https://github.com/user-attachments/assets/d5ba522c-6374-4e13-a74e-1c207687265d" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="1592" height="294" alt="image" src="https://github.com/user-attachments/assets/ad111313-387c-4211-bbfc-7a00a85caae5" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="1574" height="197" alt="image" src="https://github.com/user-attachments/assets/1b4caaec-c5c0-4a0d-871d-85a980eb68f6" />


seq 10 
## OUTPUT

<img width="1474" height="279" alt="image" src="https://github.com/user-attachments/assets/f93559ee-4988-426e-a7bc-2eb37ca1ac2d" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="1474" height="279" alt="image" src="https://github.com/user-attachments/assets/e6daa866-7342-44e3-886c-f740980f4698" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="1492" height="232" alt="image" src="https://github.com/user-attachments/assets/da83e534-ea7d-4fe3-9593-48963977c91a" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="1564" height="275" alt="image" src="https://github.com/user-attachments/assets/8be59e72-fa29-437d-b894-ae1374864a3c" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="1564" height="275" alt="image" src="https://github.com/user-attachments/assets/fed4aeea-9c26-4083-9ff8-a75d15445d11" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="1484" height="268" alt="image" src="https://github.com/user-attachments/assets/0df6155f-502d-47f1-a334-70442a052ba5" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="1235" height="562" alt="image" src="https://github.com/user-attachments/assets/f9867fd4-1c7c-4ba7-86b2-af9f2e018090" />


sed -n '2,4{s/$/*/;p}' file23
<img width="1235" height="562" alt="image" src="https://github.com/user-attachments/assets/086a429a-f77f-427f-ae17-d52a2bb9224a" />


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
<img width="744" height="196" alt="image" src="https://github.com/user-attachments/assets/d988da72-b332-4f2c-9992-ddccde101ed9" />


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
<img width="799" height="187" alt="image" src="https://github.com/user-attachments/assets/2e7a01fc-66e0-4438-aeab-060682d0de9d" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="838" height="258" alt="image" src="https://github.com/user-attachments/assets/aeec3478-d424-433c-a3b6-76047a858e79" />

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
<img width="753" height="175" alt="image" src="https://github.com/user-attachments/assets/4c7ba120-d792-4fc7-abf1-19afdfbe7804" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="711" height="168" alt="image" src="https://github.com/user-attachments/assets/3b74050d-3ade-4599-a5b5-214d67ec51dc" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="933" height="303" alt="image" src="https://github.com/user-attachments/assets/19f7ab60-e59c-495f-b922-3f458e720c28" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="961" height="315" alt="image" src="https://github.com/user-attachments/assets/fb1d9b9d-b7a0-4d4f-be05-cfe721bd87b1" />


tar -xvf backup.tar
## OUTPUT
<img width="902" height="313" alt="image" src="https://github.com/user-attachments/assets/f24a3d21-9bce-468d-bb2b-4603f7bb1282" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="902" height="313" alt="image" src="https://github.com/user-attachments/assets/81e5ddfe-7731-463c-a0c7-e36c3f5fc633" />

gunzip backup.tar.gz
## OUTPUT
<img width="902" height="313" alt="image" src="https://github.com/user-attachments/assets/7797f9e0-64c0-418d-9bb8-56707709d6af" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="838" height="106" alt="image" src="https://github.com/user-attachments/assets/cbebb3b9-b332-4183-9940-e4215f2463a7" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="769" height="160" alt="image" src="https://github.com/user-attachments/assets/d287eae1-eb61-4680-b380-4ee00288e579" />


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
<img width="789" height="380" alt="image" src="https://github.com/user-attachments/assets/b69c934b-27f1-4cdc-bba7-d837462af2a7" />

 
ls file1
## OUTPUT

<img width="755" height="97" alt="image" src="https://github.com/user-attachments/assets/b1d14ff3-9aee-4b41-a8a7-b3d9ccc7a16c" />


echo $?
## OUTPUT 
<img width="786" height="96" alt="image" src="https://github.com/user-attachments/assets/56fd5c57-4504-4e67-ba22-30bfd9589f4d" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT

<img width="786" height="96" alt="image" src="https://github.com/user-attachments/assets/c1bb20e4-76fa-4051-b69a-1a0b56d2effd" />

 
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
<img width="787" height="288" alt="image" src="https://github.com/user-attachments/assets/c8f3bb37-2dec-42b2-b826-2a380f11f15f" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="808" height="151" alt="image" src="https://github.com/user-attachments/assets/3f3aecf1-0a31-4c80-be55-4a34aa39e05d" />

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
<img width="799" height="264" alt="image" src="https://github.com/user-attachments/assets/b1c29cda-894d-434c-8fa4-7ef220663a15" />

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
