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

<img width="261" height="167" alt="image" src="https://github.com/user-attachments/assets/e0ea0bd5-903a-4e1a-86f8-31c45c3bf7a6" />



cat < file2
## OUTPUT

<img width="251" height="200" alt="image" src="https://github.com/user-attachments/assets/db767bbb-8c6a-4c7d-a11a-0f4b6e5c1c8d" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="390" height="76" alt="image" src="https://github.com/user-attachments/assets/22abc214-2278-49b6-886b-f1b6e633c5ef" />

 
comm file1 file2
 ## OUTPUT

<img width="430" height="374" alt="image" src="https://github.com/user-attachments/assets/e08a04f8-92d3-44ab-84bd-e51f8f001b4d" />

 
diff file1 file2
## OUTPUT

<img width="394" height="328" alt="image" src="https://github.com/user-attachments/assets/a6e6aef6-3fe5-4236-874b-70e249b95018" />


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

<img width="335" height="94" alt="image" src="https://github.com/user-attachments/assets/6aaf0207-51c8-466f-889e-c7b6f5637462" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="410" height="120" alt="image" src="https://github.com/user-attachments/assets/18c26535-f5dd-4ef2-8cf0-ed62ac7f100d" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="386" height="127" alt="image" src="https://github.com/user-attachments/assets/596c4845-338b-4087-993f-a04458f3d98e" />


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

<img width="382" height="71" alt="image" src="https://github.com/user-attachments/assets/37e9cbd5-7364-4d14-ae73-284648541e97" />


grep hello newfile 
## OUTPUT

<img width="393" height="78" alt="image" src="https://github.com/user-attachments/assets/2e677cb0-5932-4b10-b4c3-a68a221911a0" />



grep -v hello newfile 
## OUTPUT

<img width="502" height="77" alt="image" src="https://github.com/user-attachments/assets/61454419-edc3-46fb-a7a1-d6e3151f2d5b" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="576" height="104" alt="image" src="https://github.com/user-attachments/assets/f7956e09-5912-4d26-a3ad-0b92fec90437" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="599" height="77" alt="image" src="https://github.com/user-attachments/assets/17d03960-3c12-4ca8-b0e5-c998bd57a86d" />

grep -R ubuntu /etc
## OUTPUT

<img width="1450" height="896" alt="image" src="https://github.com/user-attachments/assets/b9d4aba0-f24c-4898-887b-10d5d413aa2b" />

<img width="1593" height="923" alt="image" src="https://github.com/user-attachments/assets/cda00d70-21f1-4e57-a1d2-9361eb3bd236" />


grep -w -n world newfile   
## OUTPUT

<img width="478" height="101" alt="image" src="https://github.com/user-attachments/assets/373c71bf-a647-40c2-af48-0064b31223f0" />


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

<img width="440" height="174" alt="image" src="https://github.com/user-attachments/assets/e93cea64-5174-4e85-a97a-d5584946345c" />


egrep -w 'Hello|hello' newfile 
## OUTPUT

<img width="483" height="101" alt="image" src="https://github.com/user-attachments/assets/3d7c5837-dd1f-4259-baed-605427db8a90" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="547" height="101" alt="image" src="https://github.com/user-attachments/assets/08a8377e-b668-453e-9262-daf0d2f3f257" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="540" height="56" alt="image" src="https://github.com/user-attachments/assets/b0703b5d-74f2-48ca-a3dd-892ed42e9c6c" />

egrep '(^hello)' newfile 
## OUTPUT

<img width="494" height="79" alt="image" src="https://github.com/user-attachments/assets/fc5d9dee-709f-492e-91f2-d5e1c4dc6497" />


egrep '(world$)' newfile 
## OUTPUT

<img width="502" height="146" alt="image" src="https://github.com/user-attachments/assets/a07efd48-8a0b-4b8a-a897-f23360af16eb" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="533" height="124" alt="image" src="https://github.com/user-attachments/assets/222e372d-068c-4710-8baf-74ccacca9b34" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="543" height="73" alt="image" src="https://github.com/user-attachments/assets/39a301c3-6e70-4e34-9aa1-3ec0ecdb1054" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="569" height="96" alt="image" src="https://github.com/user-attachments/assets/6ffb656a-680a-403b-91ba-95abc34f9534" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="554" height="103" alt="image" src="https://github.com/user-attachments/assets/dd26876e-157e-489f-a35c-8012660f96ae" />


egrep l{2} newfile
## OUTPUT

<img width="459" height="103" alt="image" src="https://github.com/user-attachments/assets/2cd033ae-acb3-486c-8620-6375d3a733aa" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="527" height="117" alt="image" src="https://github.com/user-attachments/assets/cfabaa7b-62c3-4cc9-aea8-03d4859b9eb0" />


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

<img width="417" height="78" alt="image" src="https://github.com/user-attachments/assets/ad5c9c3f-d9d4-414f-a5e5-e1a099abde6a" />


sed -n -e '$p' file23
## OUTPUT

<img width="440" height="74" alt="image" src="https://github.com/user-attachments/assets/1cfb476d-ed67-4833-a29f-4be653a0bf5f" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="564" height="273" alt="image" src="https://github.com/user-attachments/assets/86d93e0a-7284-4b29-8d04-91d732a4694a" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="550" height="272" alt="image" src="https://github.com/user-attachments/assets/e65ec988-f1a6-4e26-8c03-10631afa9ef8" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="613" height="274" alt="image" src="https://github.com/user-attachments/assets/ce427064-6383-4514-b083-51763302938a" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="571" height="183" alt="image" src="https://github.com/user-attachments/assets/ecfa50f2-7680-42d6-a795-60be73979b7b" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="577" height="222" alt="image" src="https://github.com/user-attachments/assets/30c13a8f-7222-4e77-bd57-98e0305de310" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="499" height="98" alt="image" src="https://github.com/user-attachments/assets/71819210-7b7b-42ec-b324-1e03a8650ba0" />

seq 10 | sed -n '4,6p'
## OUTPUT

<img width="397" height="127" alt="image" src="https://github.com/user-attachments/assets/fe102e71-7220-491b-8e81-ef10949ab2fe" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="499" height="129" alt="image" src="https://github.com/user-attachments/assets/842070e1-e0b3-4700-9762-95cc2e52eecc" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="455" height="145" alt="image" src="https://github.com/user-attachments/assets/cbfec017-7644-4ff8-b3d8-5666d9739df8" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="461" height="120" alt="image" src="https://github.com/user-attachments/assets/cd482329-33bf-475d-902d-2963a73de78d" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="438" height="124" alt="image" src="https://github.com/user-attachments/assets/257fa2f5-cbe8-4f56-a9fe-e4ab6f3d5f75" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="438" height="128" alt="image" src="https://github.com/user-attachments/assets/314c442f-9551-42b6-a74b-2cc778252588" />

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

<img width="533" height="371" alt="image" src="https://github.com/user-attachments/assets/ef1d67af-d58a-4fef-92ef-68d0576b60eb" />



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

<img width="554" height="403" alt="image" src="https://github.com/user-attachments/assets/1f1709d4-95e4-49cc-9681-906ba6bca672" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="604" height="253" alt="image" src="https://github.com/user-attachments/assets/4a8d9f23-5445-4fc3-95d6-568c072d372a" />


cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt

<img width="422" height="317" alt="image" src="https://github.com/user-attachments/assets/c678ec24-ce47-44e9-a82a-91e7e97eb4f8" />


cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="524" height="125" alt="image" src="https://github.com/user-attachments/assets/3c6f2ccd-284d-445f-9f4b-ddd3e8d608db" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="593" height="129" alt="image" src="https://github.com/user-attachments/assets/178a61e1-039d-4ba1-be03-42132d3e2eaa" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="376" height="570" alt="image" src="https://github.com/user-attachments/assets/e69adcf2-30de-444a-82b4-896f08eb7598" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="649" height="474" alt="image" src="https://github.com/user-attachments/assets/fc9e0cd6-3707-4dc4-a7e5-32dab137ce8d" />


tar -xvf backup.tar
## OUTPUT

<img width="436" height="600" alt="image" src="https://github.com/user-attachments/assets/d7b710da-bf7d-463d-9460-9445ab17e5a6" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="504" height="42" alt="image" src="https://github.com/user-attachments/assets/3abfbc17-a861-46f1-a25f-e882d89fb873" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="454" height="274" alt="image" src="https://github.com/user-attachments/assets/4c492025-52a7-4eb0-879f-45118d8232a5" />


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

<img width="264" height="70" alt="image" src="https://github.com/user-attachments/assets/db845d17-1ed0-44a1-859a-665ddf6b137e" />

 
ls file1
## OUTPUT

<img width="318" height="71" alt="image" src="https://github.com/user-attachments/assets/b9335bfa-7cb9-4baa-a4fe-9e2669790110" />


echo $?
## OUTPUT 

<img width="323" height="93" alt="image" src="https://github.com/user-attachments/assets/17fe4465-a9e0-40a1-b92f-607fb2ee9288" /> 

 
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

<img width="401" height="270" alt="image" src="https://github.com/user-attachments/assets/3e79a251-392c-407b-a017-ee035053cc00" />


chmod 755 strcomp.sh
 
./strcomp.sh 

## OUTPUT

<img width="340" height="81" alt="image" src="https://github.com/user-attachments/assets/7133181d-a734-48c4-91dd-04af820c2fd5" />


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

<img width="646" height="128" alt="image" src="https://github.com/user-attachments/assets/dce95808-0791-44e9-9e5a-059b7d4f9769" />


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

<img width="600" height="180" alt="image" src="https://github.com/user-attachments/assets/7e772bbf-cda4-4179-a18e-7f5e78595486" />



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

<img width="522" height="149" alt="image" src="https://github.com/user-attachments/assets/a1260c62-75e5-438d-b67b-b60c7d1ae641" />


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

<img width="581" height="130" alt="image" src="https://github.com/user-attachments/assets/0ee6ab6e-dd3b-4908-941d-b08172dbe7b1" />


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


<img width="413" height="176" alt="image" src="https://github.com/user-attachments/assets/ad339335-22ed-4b0f-a489-a1d375c6f530" />



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

<img width="490" height="94" alt="image" src="https://github.com/user-attachments/assets/56171db0-b7b2-4d3e-9a85-2df433aa300f" />


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
