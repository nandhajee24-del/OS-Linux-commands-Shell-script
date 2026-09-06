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
<img width="380" height="193" alt="image" src="https://github.com/user-attachments/assets/9c09c7b9-fc84-4526-8604-ad7889f041f0" />



cat < file2
## OUTPUT
<img width="271" height="225" alt="image" src="https://github.com/user-attachments/assets/2fd3cc60-d6b3-444e-ab92-ebc7f63351fb" />


# Comparing Files
cmp file1 file2
## OUTPUT
 
comm file1 file2
 ## OUTPUT

 <img width="391" height="127" alt="image" src="https://github.com/user-attachments/assets/24de0ec8-c43b-4b90-9432-b8c7a78841fb" />

diff file1 file2
## OUTPUT
<img width="347" height="321" alt="image" src="https://github.com/user-attachments/assets/a3279d23-7f09-4031-aff0-bfa2c671aae3" />


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


<img width="385" height="175" alt="image" src="https://github.com/user-attachments/assets/6732bbf6-4721-4b94-b9d4-bd90187717ac" />


cut -d "|" -f 1 file22
## OUTPUT
<img width="385" height="175" alt="image" src="https://github.com/user-attachments/assets/6732bbf6-4721-4b94-b9d4-bd90187717ac" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="356" height="173" alt="image" src="https://github.com/user-attachments/assets/e88ee100-1235-4c28-aad4-7145a17fb5d0" />

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

<img width="286" height="75" alt="image" src="https://github.com/user-attachments/assets/5b46a5b0-89bb-4cc5-b037-982652eb5110" />


grep hello newfile 
## OUTPUT

<img width="307" height="76" alt="image" src="https://github.com/user-attachments/assets/69aa226d-5112-4782-9eef-9ea9300fde29" />



grep -v hello newfile 
## OUTPUT
<img width="348" height="77" alt="image" src="https://github.com/user-attachments/assets/9c147482-cfb6-4056-b474-09a7abc9110c" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="370" height="91" alt="image" src="https://github.com/user-attachments/assets/f13277be-734b-4064-88e0-190ccb35d5ff" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="388" height="67" alt="image" src="https://github.com/user-attachments/assets/5046fd6c-f2a9-4689-b019-fba9af8c3d08" />



grep -R ubuntu /etc
## OUTPUT

<img width="810" height="487" alt="image" src="https://github.com/user-attachments/assets/70d2ad1f-9ef5-4398-a6b2-b25b6d5391e4" />


grep -w -n world newfile   
## OUTPUT
<img width="398" height="95" alt="image" src="https://github.com/user-attachments/assets/62d714ed-1fd2-44e3-83e8-d5679855a8b7" />

grep
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
<img width="413" height="100" alt="image" src="https://github.com/user-attachments/assets/8c0c77b6-8c6f-4fea-8487-bac7674e1b64" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="395" height="98" alt="image" src="https://github.com/user-attachments/assets/df19e140-8080-424c-8c53-9245de1d5f70" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT



<img width="467" height="108" alt="image" src="https://github.com/user-attachments/assets/7cc79074-6824-48d4-a9b9-910b6f4bc074" />

egrep '(^hello)' newfile 
## OUTPUT

<img width="358" height="80" alt="image" src="https://github.com/user-attachments/assets/5dc52c1a-6437-4328-9030-0800911b32e0" />


egrep '(world$)' newfile 
## OUTPUT

<img width="340" height="95" alt="image" src="https://github.com/user-attachments/assets/161683ed-d15e-4638-b40c-759666227f18" />


egrep '(World$)' newfile 
## OUTPUT

<img width="426" height="81" alt="image" src="https://github.com/user-attachments/assets/3aff1d59-2997-4e90-a6c2-835e28296ca1" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="432" height="127" alt="image" src="https://github.com/user-attachments/assets/728d9744-fea7-48ae-858a-af3f8b459c6b" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="398" height="75" alt="image" src="https://github.com/user-attachments/assets/646fa151-2fd6-4afe-9aaf-7b9d5a7ffa12" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="427" height="85" alt="image" src="https://github.com/user-attachments/assets/d0143d4d-f935-463b-802c-d49b74707cca" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="457" height="75" alt="image" src="https://github.com/user-attachments/assets/1428d784-17af-4399-883f-2c127f25ac8d" />


egrep l{2} newfile
## OUTPUT

<img width="392" height="145" alt="image" src="https://github.com/user-attachments/assets/881482fe-2e0e-4e1e-ae76-a5cfaa7b9766" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="440" height="128" alt="image" src="https://github.com/user-attachments/assets/3cb6f74c-a213-449d-9230-5c733b127d8c" />


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

<img width="350" height="77" alt="image" src="https://github.com/user-attachments/assets/c66846f2-cd96-44c6-9085-401bb3299166" />


sed -n -e '$p' file23
## OUTPUT

<img width="385" height="72" alt="image" src="https://github.com/user-attachments/assets/ab668a4c-19f1-4162-8b8f-d451ddaef04f" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="451" height="255" alt="image" src="https://github.com/user-attachments/assets/4e472adc-e5bb-4f17-a9d2-458a8b99f30d" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="440" height="261" alt="image" src="https://github.com/user-attachments/assets/cb29a045-f0e0-4b90-9b32-fd3cc70a8215" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="437" height="255" alt="image" src="https://github.com/user-attachments/assets/c37d2dfb-6760-4bdc-8bc5-c7e2e89e40b8" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="543" height="183" alt="image" src="https://github.com/user-attachments/assets/28ab475e-9ce7-47ec-875e-eae724876103" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="422" height="122" alt="image" src="https://github.com/user-attachments/assets/a907579a-dc4b-466d-8dab-dd15f692be40" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="460" height="105" alt="image" src="https://github.com/user-attachments/assets/bf251e06-aaa9-48ce-b9fc-64dda1348f4d" />


seq 10 
## OUTPUT

<img width="456" height="312" alt="image" src="https://github.com/user-attachments/assets/1bfd6b41-d574-498e-8c1e-c5d01ae51129" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="385" height="117" alt="image" src="https://github.com/user-attachments/assets/efdfd3c3-134d-43cc-a642-14951e9abee0" />



seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="412" height="135" alt="image" src="https://github.com/user-attachments/assets/b82e4f41-7a8f-4db5-b0d1-01fb7f00a8d4" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="410" height="162" alt="image" src="https://github.com/user-attachments/assets/450f1f35-0e86-4b36-9263-e95a47333e91" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="352" height="131" alt="image" src="https://github.com/user-attachments/assets/b3c81fa9-eaac-4af4-9517-d072cd64be45" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="385" height="122" alt="image" src="https://github.com/user-attachments/assets/cd0601a8-5084-465b-b947-35c70ea261d7" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="415" height="127" alt="image" src="https://github.com/user-attachments/assets/72ea6537-3bcc-4d0b-bc32-1ec2940c368d" />


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
<img width="421" height="207" alt="image" src="https://github.com/user-attachments/assets/c4b8e60b-e1e7-481e-9a77-45ea0aa20423" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="440" height="267" alt="image" src="https://github.com/user-attachments/assets/540d4e14-b8d9-455e-8d64-779c918f37ba" />

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
<img width="420" height="121" alt="image" src="https://github.com/user-attachments/assets/b389bab9-82ec-4a33-8a1f-d2112476cb0e" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="586" height="122" alt="image" src="https://github.com/user-attachments/assets/7d0efe07-03a2-4c7c-a303-fffd0298ed85" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="641" height="521" alt="image" src="https://github.com/user-attachments/assets/14440903-00dc-435b-b182-3928f8675e29" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="822" height="587" alt="image" src="https://github.com/user-attachments/assets/09307a84-8558-40e1-8e95-2894b05c1524" />


tar -xvf backup.tar
## OUTPUT
<img width="680" height="585" alt="image" src="https://github.com/user-attachments/assets/f89ed50f-11b3-4612-b2a3-773ab9e28bc8" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="615" height="126" alt="image" src="https://github.com/user-attachments/assets/9e793a5a-192d-425b-b128-30dfad930961" />

gunzip backup.tar.gz
## OUTPUT

 <img width="430" height="105" alt="image" src="https://github.com/user-attachments/assets/e3b07b73-f652-467f-8cb6-c2eb62dc49a0" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="760" height="220" alt="image" src="https://github.com/user-attachments/assets/4f428ba3-f3a9-4e52-8fc6-c0bc34718ab6" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="488" height="276" alt="image" src="https://github.com/user-attachments/assets/8544d976-ca77-47d0-a671-ee40b7dab46c" />


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
<img width="642" height="482" alt="image" src="https://github.com/user-attachments/assets/25721b64-19a2-438a-b248-1e0879a20d75" />

 
ls file1
## OUTPUT
<img width="471" height="76" alt="image" src="https://github.com/user-attachments/assets/19706d8c-99e4-4e1a-a9a3-cce8befdf938" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 <img width="582" height="151" alt="image" src="https://github.com/user-attachments/assets/6b297d80-6312-4dfb-8432-b5df37439376" />

echo $?
## OUTPUT 
 <img width="417" height="87" alt="image" src="https://github.com/user-attachments/assets/ddafec51-ca93-4c87-8d41-fa71d4b746b5" />

abcd
 
echo $?
 ## OUTPUT

<img width="417" height="87" alt="image" src="https://github.com/user-attachments/assets/f89ecefc-632f-499e-8cbf-d176c10104c0" />

 
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
<img width="427" height="287" alt="image" src="https://github.com/user-attachments/assets/a31d8c0a-1a46-4774-89cf-0c2570c0e83e" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="742" height="162" alt="image" src="https://github.com/user-attachments/assets/026f4bcd-c43a-402e-911d-2e7946fa9d33" />


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
<img width="660" height="230" alt="image" src="https://github.com/user-attachments/assets/cb9db963-c72c-4dbf-9d98-e20f97da6a68" />

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


<img width="637" height="491" alt="image" src="https://github.com/user-attachments/assets/e4429780-a64a-46ff-8f62-e66d63859284" />

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
<img width="728" height="182" alt="image" src="https://github.com/user-attachments/assets/7cfab92a-a542-4a06-ae8a-ded9440ab164" />

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
<img width="705" height="197" alt="image" src="https://github.com/user-attachments/assets/0ea34fbc-f54e-4234-a235-5d4c6f58bfb2" />

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
<img width="765" height="146" alt="image" src="https://github.com/user-attachments/assets/fed6d9c4-9040-49a4-9571-60937d8986cf" />


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
<img width="755" height="152" alt="image" src="https://github.com/user-attachments/assets/53c01493-cec6-451d-9d42-dfe885e810ae" />

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
 ## OUTPUT:
 <img width="476" height="126" alt="image" src="https://github.com/user-attachments/assets/da13293a-fa5e-4a5d-9902-5c753f206d9c" />

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
 ## OUTPUT:
 <img width="520" height="348" alt="image" src="https://github.com/user-attachments/assets/a53f3777-5f2a-4302-a1a6-429a79de26ac" />

 
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
 ## OUTPUT:
 <img width="702" height="222" alt="image" src="https://github.com/user-attachments/assets/bb41f024-930b-4b42-8447-e323c8241167" />

 
 
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
## OUTPUT:
<img width="745" height="298" alt="image" src="https://github.com/user-attachments/assets/a4c998fa-d793-4eeb-81ca-8870fa263b0e" />

 
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
## OUTPUT:
<img width="691" height="233" alt="image" src="https://github.com/user-attachments/assets/db5d2b6b-8b23-401e-a9b4-965cd8e4c4cf" />

 
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
 ## OUTPUT
 <img width="653" height="306" alt="image" src="https://github.com/user-attachments/assets/a6d5420b-6e3b-4414-bb82-4ee183559713" />

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
<img width="623" height="246" alt="image" src="https://github.com/user-attachments/assets/7b985f36-9e98-4a18-90a1-936d4c209485" />


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
<img width="527" height="228" alt="image" src="https://github.com/user-attachments/assets/7fec054e-4651-48d8-9df3-713e07079cbd" />

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
<img width="513" height="445" alt="image" src="https://github.com/user-attachments/assets/f301d8a2-b157-4f48-89df-d58196ff6cc7" />

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

 <img width="572" height="411" alt="image" src="https://github.com/user-attachments/assets/9fcfcd08-cc5c-473e-a888-ceaed7abad16" />

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
<img width="885" height="150" alt="image" src="https://github.com/user-attachments/assets/85c4f7f9-83b7-4e32-8bad-22abd9e69c77" />

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
<img width="780" height="237" alt="image" src="https://github.com/user-attachments/assets/fdc6406b-e495-4cd4-85bb-d796e2dedd43" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="427" height="162" alt="image" src="https://github.com/user-attachments/assets/6e05cb65-1eb6-45fb-852e-e60550c8184d" />



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
<img width="427" height="162" alt="image" src="https://github.com/user-attachments/assets/962a8644-f7ed-49ee-942b-777c79ad0fd3" />

 ./funcex.sh 

 
 ./funcex.sh 1 2
## OUTPUT
 <img width="512" height="202" alt="image" src="https://github.com/user-attachments/assets/c0b944ea-8169-45bc-b7c0-6bd7de196724" />

 
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
<img width="752" height="368" alt="image" src="https://github.com/user-attachments/assets/669958a0-7e4b-4f40-9496-73434f3ebb95" />


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
$ chmod 777 argshift.shchmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
<img width="447" height="231" alt="image" src="https://github.com/user-attachments/assets/708bee2c-3f6e-42f8-a1f5-7698a81e211f" />


 
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
 
 <img width="465" height="420" alt="image" src="https://github.com/user-attachments/assets/6a314bd7-675b-407a-80ab-301e37a7632c" />

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
 <img width="645" height="368" alt="image" src="https://github.com/user-attachments/assets/b00f2d75-5d5c-41af-b249-f4c0a985423d" />

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
<img width="653" height="497" alt="image" src="https://github.com/user-attachments/assets/ad7df9f4-2476-47e3-8429-6b147ecfedea" />


# RESULT:
The Commands are executed successfully.
