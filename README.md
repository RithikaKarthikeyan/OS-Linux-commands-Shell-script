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
<img width="338" height="157" alt="image" src="https://github.com/user-attachments/assets/73b651de-9b2c-41c7-af3d-366b00bc0889" />



cat < file2
## OUTPUT
<img width="295" height="172" alt="image" src="https://github.com/user-attachments/assets/82aff893-8eb3-414b-9b2e-0552145fc274" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="407" height="75" alt="image" src="https://github.com/user-attachments/assets/48105457-c430-4629-852a-f9d20f0b083c" />

comm file1 file2
 ## OUTPUT
<img width="337" height="223" alt="image" src="https://github.com/user-attachments/assets/10e406f2-5849-4dc6-88d7-5110dea22644" />

 
diff file1 file2
## OUTPUT
<img width="360" height="276" alt="image" src="https://github.com/user-attachments/assets/a1c0c1d1-7c40-4da4-bf46-35f44e2a887f" />


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
<img width="337" height="97" alt="image" src="https://github.com/user-attachments/assets/d24a5204-5370-4e3a-afb2-18dfb4f3c77b" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="311" height="125" alt="image" src="https://github.com/user-attachments/assets/630caf9a-b63f-448e-9729-c7f52d68f46b" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="307" height="120" alt="image" src="https://github.com/user-attachments/assets/031ee4b6-8733-419f-a2e2-fee82867e0d2" />


cat > newfile 
```
Hello world
hello world
^d
````
cat < newfile 
## OUTPUT
<img width="315" height="100" alt="image" src="https://github.com/user-attachments/assets/762c0f79-b97d-4f21-a531-71f9d0a64b19" />

 
grep Hello newfile 
## OUTPUT
<img width="297" height="77" alt="image" src="https://github.com/user-attachments/assets/9517a90d-9bf4-4b53-98d8-30361937c656" />



grep hello newfile 
## OUTPUT
<img width="302" height="71" alt="image" src="https://github.com/user-attachments/assets/cf8783c3-1397-48b5-8163-200b99dd3eab" />




grep -v hello newfile 
## OUTPUT
<img width="303" height="75" alt="image" src="https://github.com/user-attachments/assets/442e19aa-3505-452c-ad33-1edbd14e47f2" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="377" height="102" alt="image" src="https://github.com/user-attachments/assets/51f63361-3467-42a0-bbe4-b2919e879488" />


cat newfile | grep -i -c "hello"
## OUTPUT
<img width="387" height="78" alt="image" src="https://github.com/user-attachments/assets/414dc705-be19-4fec-8bd1-43ab6b695642" />


grep -R ubuntu /etc
## OUTPUT
<img width="1481" height="675" alt="image" src="https://github.com/user-attachments/assets/1004e31e-3eef-428e-96b4-69cab43cc46b" />



grep -w -n world newfile   
## OUTPUT
<img width="398" height="102" alt="image" src="https://github.com/user-attachments/assets/1e173bf9-03b6-4a62-87f6-79d01eaab60b" />


cat > newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat < newfile
## OUTPUT
<img width="390" height="175" alt="image" src="https://github.com/user-attachments/assets/5429d9fb-3a1d-4396-b1aa-20c461732e6c" />


egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="402" height="103" alt="image" src="https://github.com/user-attachments/assets/86e6d590-3cec-4cfc-8344-2349eda2ed11" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="422" height="106" alt="image" src="https://github.com/user-attachments/assets/63a6d64a-7c64-45bd-9c6e-60d1faafd0ed" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="400" height="97" alt="image" src="https://github.com/user-attachments/assets/5d85596d-3322-454c-bd10-5db998a1e9f6" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="392" height="80" alt="image" src="https://github.com/user-attachments/assets/09a81b3c-d613-4728-bf7b-b9493144b90a" />



egrep '(world$)' newfile 
## OUTPUT
<img width="347" height="102" alt="image" src="https://github.com/user-attachments/assets/f009743a-9022-4cf3-8c14-1c1a81c578cc" />



egrep '(World$)' newfile 
## OUTPUT
<img width="345" height="77" alt="image" src="https://github.com/user-attachments/assets/f13c2a67-28d1-49c4-823b-e54dd3f46e84" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="382" height="127" alt="image" src="https://github.com/user-attachments/assets/558fba3e-beea-491b-9814-526cc238693f" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="357" height="75" alt="image" src="https://github.com/user-attachments/assets/93e1e18e-6de5-4d8d-a742-24c424ed846a" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="382" height="75" alt="image" src="https://github.com/user-attachments/assets/73ddc3c1-8203-4c69-a09b-e96af350a953" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="411" height="80" alt="image" src="https://github.com/user-attachments/assets/dbdc5abf-d7a8-479e-ae97-3871c2d2d7cc" />


egrep l{2} newfile
## OUTPUT
<img width="357" height="90" alt="image" src="https://github.com/user-attachments/assets/29ec4d27-e31b-4653-bf99-ad971059eebc" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="390" height="122" alt="image" src="https://github.com/user-attachments/assets/39c38c93-8fd8-4f74-914f-96ed7c3fc67b" />


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
<img width="327" height="80" alt="image" src="https://github.com/user-attachments/assets/a5597119-aa9b-4349-a5d7-e719043e306b" />



sed -n -e '$p' file23
## OUTPUT
<img width="322" height="77" alt="image" src="https://github.com/user-attachments/assets/19956923-f875-4d17-9c5d-bc8ce5756976" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="392" height="251" alt="image" src="https://github.com/user-attachments/assets/b61acb42-8285-4fbd-b143-f175efcebd03" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="375" height="251" alt="image" src="https://github.com/user-attachments/assets/25dab2a1-6a71-446d-8a7f-a22d626871ef" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="428" height="248" alt="image" src="https://github.com/user-attachments/assets/45bdc829-8255-4494-ae2b-486ee67d9331" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="341" height="173" alt="image" src="https://github.com/user-attachments/assets/9da2637a-5c9e-4f12-97d5-4eca4cdce940" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="415" height="130" alt="image" src="https://github.com/user-attachments/assets/f828d039-374a-4d2f-aee3-bc56b9bc50ed" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="432" height="103" alt="image" src="https://github.com/user-attachments/assets/43341392-917b-44b9-aaed-7fdc902b3ce0" />



seq 10 
## OUTPUT
<img width="333" height="302" alt="image" src="https://github.com/user-attachments/assets/6dae7f68-44bc-4e37-8099-584872ee4743" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="376" height="122" alt="image" src="https://github.com/user-attachments/assets/24bc6170-01b0-45ff-95b0-b459bad2b77c" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="352" height="122" alt="image" src="https://github.com/user-attachments/assets/3069808b-2e4b-43ae-ab0b-74bda41d313b" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="335" height="153" alt="image" src="https://github.com/user-attachments/assets/133176ce-a2a2-4afa-8ae8-3edf76fffa71" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="332" height="128" alt="image" src="https://github.com/user-attachments/assets/a159dd69-9a2a-407d-8f99-107a790cac2f" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="358" height="121" alt="image" src="https://github.com/user-attachments/assets/f9735c0e-16c1-42f5-a9c4-d5e0eb6dc6fc" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="440" height="122" alt="image" src="https://github.com/user-attachments/assets/1c188697-aff8-4a3c-b432-a2862d7e3747" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="395" height="122" alt="image" src="https://github.com/user-attachments/assets/c8598483-d388-4e9d-92d5-c0cdca82b1ac" />


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
<img width="318" height="172" alt="image" src="https://github.com/user-attachments/assets/14ab562b-5885-43dd-8e5d-576b78c1ddb8" />


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
<img width="352" height="177" alt="image" src="https://github.com/user-attachments/assets/401ae162-ae6b-4d44-82b1-109b1b845c2d" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="442" height="248" alt="image" src="https://github.com/user-attachments/assets/99dfa5f0-52cb-4977-b7ed-2f39a8d16fcc" />

cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat < urllist.txt
## OUTPUT 
<img width="310" height="127" alt="image" src="https://github.com/user-attachments/assets/04e29117-c0dc-4480-be0b-6840148b9921" />


cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="348" height="122" alt="image" src="https://github.com/user-attachments/assets/0888c045-523a-45e4-b707-da78bdd362d9" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="500" height="126" alt="image" src="https://github.com/user-attachments/assets/eadc23b1-31cc-4868-ab92-c9da3c81cb0c" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="436" height="630" alt="image" src="https://github.com/user-attachments/assets/8e173eaf-fad0-494e-b06c-98587b195714" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="613" height="635" alt="image" src="https://github.com/user-attachments/assets/8ad4ca2a-924e-471e-96c8-de0ad33fecbf" />


tar -xvf backup.tar
## OUTPUT
<img width="492" height="631" alt="image" src="https://github.com/user-attachments/assets/b81a7b0e-fab2-4040-aac8-7acbd67c7fbf" />

gzip backup.tar

ls *.gz
## OUTPUT
<img width="463" height="68" alt="image" src="https://github.com/user-attachments/assets/bed9801a-bf3d-4e1c-b9c6-322cfef8ce6d" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="553" height="80" alt="image" src="https://github.com/user-attachments/assets/39480664-8bee-478b-91b2-070ae4c4777f" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.shhellohello
./my-script.shcd
## OUTPUT
<img width="416" height="147" alt="image" src="https://github.com/user-attachments/assets/74f8ab9b-fb31-4e14-97ab-a8ed0105510e" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="401" height="128" alt="image" src="https://github.com/user-attachments/assets/0fbecd68-6ef4-4cf4-a21b-7392c335249f" />


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
<img width="722" height="405" alt="image" src="https://github.com/user-attachments/assets/6c449592-4369-4271-a32f-4ba8576e9115" />

 
ls file1
## OUTPUT
<img width="341" height="68" alt="image" src="https://github.com/user-attachments/assets/4a350351-4dfa-45fb-a60a-d244e487dcf9" />

echo $?
## OUTPUT 
<img width="312" height="72" alt="image" src="https://github.com/user-attachments/assets/5e4a1c15-e695-4457-9aed-f1b39556d4e6" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="401" height="252" alt="image" src="https://github.com/user-attachments/assets/ff39eb45-8974-407d-b440-43142d6b919b" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="401" height="252" alt="image" src="https://github.com/user-attachments/assets/926b32de-f6d9-4f2d-b659-021fe9f12920" />


 
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
<img width="402" height="275" alt="image" src="https://github.com/user-attachments/assets/1fd3010a-1b0f-4e19-beaf-d8bdb34c584e" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="612" height="107" alt="image" src="https://github.com/user-attachments/assets/c40c31dc-8f43-42d5-98d6-f4454a9cabb3" />


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
<img width="630" height="96" alt="image" src="https://github.com/user-attachments/assets/b2b1260e-01f8-43e9-bdc4-04834956ba30" />

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

<img width="632" height="150" alt="image" src="https://github.com/user-attachments/assets/b239b6a9-db10-4d43-9fbd-07e6f0db81fd" />


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
<img width="386" height="107" alt="image" src="https://github.com/user-attachments/assets/b3a81813-a051-4844-b5d8-1630ce68f2dd" />

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
<img width="517" height="122" alt="image" src="https://github.com/user-attachments/assets/cbebf5f1-0726-4783-a2c8-25daf53bdc76" />

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
<img width="388" height="77" alt="image" src="https://github.com/user-attachments/assets/aa619516-6628-4441-8d6d-59f9ade29045" />


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
<img width="477" height="123" alt="image" src="https://github.com/user-attachments/assets/2736efd9-ad92-435b-93d3-50b83b2fed8f" />

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
<img width="373" height="76" alt="image" src="https://github.com/user-attachments/assets/cb588670-396f-4098-afc7-ecdef1f61218" />

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

 <img width="302" height="300" alt="image" src="https://github.com/user-attachments/assets/aa019962-5097-44bc-acd9-aa3d665b53b4" />

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
 
$./untiltest.sh
## OUTPUT
<img width="345" height="147" alt="image" src="https://github.com/user-attachments/assets/c236c418-43bf-4409-b0ff-1b11d088d402" />

 
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
$ ./forin1.sh
## OUTPUT
<img width="611" height="223" alt="image" src="https://github.com/user-attachments/assets/e7e6fc4b-88d2-4bee-a8e3-c72c12180110" />

 
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
<img width="457" height="147" alt="image" src="https://github.com/user-attachments/assets/84e7a084-8e50-4f9f-8d41-97253ca22962" />


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
<img width="368" height="203" alt="image" src="https://github.com/user-attachments/assets/ea3cd9c1-9de5-44be-a85c-5eab429271cd" />

 
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
$./forin1.sh

## OUTPUT
<img width="383" height="202" alt="image" src="https://github.com/user-attachments/assets/332733f7-2a89-4c97-a182-56d5c3499c56" />


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
<img width="380" height="227" alt="image" src="https://github.com/user-attachments/assets/071b4017-f17b-40d4-a2a9-0dbcc507aa75" />


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
<img width="350" height="176" alt="image" src="https://github.com/user-attachments/assets/598f99f9-659d-4324-a8f8-77877d1ea1ee" />


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
<img width="412" height="172" alt="image" src="https://github.com/user-attachments/assets/bc7b50a7-714e-465a-ac63-8358725a28f7" />

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
<img width="422" height="366" alt="image" src="https://github.com/user-attachments/assets/ad08b529-63c8-4f08-8d57-6377d91534bf" />

 
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

<img width="405" height="127" alt="image" src="https://github.com/user-attachments/assets/569c0729-5ff6-438c-83e8-4478c4e43858" />


cat continue.sh 
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

<img width="442" height="175" alt="image" src="https://github.com/user-attachments/assets/812f8197-3603-41b0-9934-2549a3331e94" />

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

<img width="441" height="97" alt="image" src="https://github.com/user-attachments/assets/85d0ec33-c2ac-4ad6-9682-704463df362e" />


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
<img width="416" height="100" alt="image" src="https://github.com/user-attachments/assets/8200ce3e-d864-4df2-a5da-0b05bc951375" />



 
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
<img width="331" height="75" alt="image" src="https://github.com/user-attachments/assets/af48521b-1e7a-4dd9-8a15-36bf04a4d2cb" />

 
 ./funcex.sh 1 2
<img width="370" height="71" alt="image" src="https://github.com/user-attachments/assets/fdd8f3e8-679b-412f-9e54-8bbad70928ce" />

 
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
 <img width="321" height="121" alt="image" src="https://github.com/user-attachments/assets/92cd5f06-9b84-4366-8d11-788371134209" />

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
 <img width="391" height="132" alt="image" src="https://github.com/user-attachments/assets/34e0664b-b5d3-42e1-81f3-53d3c4030d36" />

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
<img width="402" height="402" alt="image" src="https://github.com/user-attachments/assets/1abc3189-c924-4179-a60d-e32b548f755e" />
 
 
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
<img width="395" height="380" alt="image" src="https://github.com/user-attachments/assets/8a839d19-a1b8-4131-a625-0069d0b85aef" />

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
<img width="372" height="257" alt="image" src="https://github.com/user-attachments/assets/666947c1-b555-4c7a-a8f6-b6186c63c022" />


# RESULT:
The Commands are executed successfully.
