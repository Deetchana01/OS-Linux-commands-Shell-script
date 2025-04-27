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

<img width="1581" alt="cat file1" src="https://github.com/user-attachments/assets/f7962ff8-2c30-41ef-83bd-ee30367ca410" />


cat < file2
## OUTPUT

<img width="1581" alt="cat file2" src="https://github.com/user-attachments/assets/2adb53aa-c506-44be-b821-71115bc71224" />

# Comparing Files
cmp file1 file2
## OUTPUT

<img width="1593" alt="comp" src="https://github.com/user-attachments/assets/2f6b84c7-0117-41bc-b36c-20fd6bf7b2d4" />

 
comm file1 file2
 ## OUTPUT

 <img width="1581" alt="comm" src="https://github.com/user-attachments/assets/80f3bc3f-55ec-429c-a20c-d1da84900ca4" />

diff file1 file2
## OUTPUT

<img width="1581" alt="diff" src="https://github.com/user-attachments/assets/af7d2e20-2453-45f2-b331-f298cb77802d" />

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
<img width="1581" alt="cut-c1-c3file11" src="https://github.com/user-attachments/assets/c1275228-5c60-4a30-96c3-571587799ae7" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="1669" alt="cut-d-f1file22" src="https://github.com/user-attachments/assets/ac50ef6d-0e8e-4d4b-8e2b-91558897489e" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="1669" alt="cut-d-f2file22" src="https://github.com/user-attachments/assets/11d55e62-a9de-40e3-9fe4-ab96fafe6cd3" />

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
<img width="1669" alt="grepHello" src="https://github.com/user-attachments/assets/ea274b3e-a3b7-46d1-8f2e-e83d16970952" />



grep hello newfile 
## OUTPUT
<img width="1669" alt="grep_hello" src="https://github.com/user-attachments/assets/f3d930da-1508-43b8-a449-84dc20a1713a" />




grep -v hello newfile 
## OUTPUT
<img width="1669" alt="grep-v" src="https://github.com/user-attachments/assets/f49f4cc0-1b8d-4980-99fe-b1e0391bee52" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="1781" alt="catgrepi" src="https://github.com/user-attachments/assets/fcc1628a-3dd9-4ee4-a24a-25104370a7e1" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="1827" alt="catgrepic" src="https://github.com/user-attachments/assets/86e26fd1-369d-4336-b6b5-8050c97077cb" />



grep -R ubuntu /etc
## OUTPUT

<img width="1108" alt="grep newworld" src="https://github.com/user-attachments/assets/8c2480f9-7873-490d-a1d4-d2c0f3c70719" />


grep -w -n world newfile   
## OUTPUT
<img width="1108" alt="grep newworld" src="https://github.com/user-attachments/assets/1ad0aa1d-4b44-4237-9551-764812f11a05" />


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

<img width="1172" alt="egrep1" src="https://github.com/user-attachments/assets/69401e8f-0424-425f-8261-ae267934bc09" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="1172" alt="egrep2" src="https://github.com/user-attachments/assets/2e2bd08d-b74d-493f-b539-9a019b7dc7be" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="1191" alt="egrep3" src="https://github.com/user-attachments/assets/7abc66cb-152f-49b7-ad80-ca2881b1aacd" />



egrep '(^hello)' newfile 
## OUTPUT


<img width="1191" alt="egrep4" src="https://github.com/user-attachments/assets/4f96f2bf-f6fe-490f-b8a9-5be0f808a1a3" />

egrep '(world$)' newfile 
## OUTPUT

<img width="1191" alt="egrep6" src="https://github.com/user-attachments/assets/1bc6ee42-25be-4056-9ed0-0e9383a83109" />


egrep '(World$)' newfile 
## OUTPUT
<img width="1191" alt="egrep6" src="https://github.com/user-attachments/assets/ea348714-909c-4d45-98e0-4b822f902e2d" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="1191" alt="egrep7" src="https://github.com/user-attachments/assets/6fbc031d-c5d8-428c-885f-2da210f7d243" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="1191" alt="egrep8" src="https://github.com/user-attachments/assets/5ef5fe82-98f4-4607-9504-14b566ac0317" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="1191" alt="egrep9" src="https://github.com/user-attachments/assets/06bdb2b3-3ac5-4583-a7af-5dd2e7187ee4" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1191" alt="egrep10" src="https://github.com/user-attachments/assets/bd7a5b6f-4249-45a2-ac65-1b5906e3cd76" />


egrep l{2} newfile
## OUTPUT

<img width="1191" alt="egrep11" src="https://github.com/user-attachments/assets/4e3d32d2-4181-40b8-8a7b-98820f78ce37" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="1191" alt="egrep12" src="https://github.com/user-attachments/assets/c59226f8-7a5d-4ce4-9bb6-a581414e1e8e" />



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
<img width="1191" alt="sed1" src="https://github.com/user-attachments/assets/a779be3a-e687-4b66-92d9-74da34fcc9af" />



sed -n -e '$p' file23
## OUTPUT

<img width="1191" alt="sed2" src="https://github.com/user-attachments/assets/919fa1c7-a9e7-4a66-9c08-c268c872333d" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1191" alt="sed3" src="https://github.com/user-attachments/assets/0c452c25-c69c-43d8-a2a9-024879ccdc02" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="1191" alt="sed4" src="https://github.com/user-attachments/assets/c658764c-7bc4-4801-917c-d24902150bcd" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="1191" alt="sed5" src="https://github.com/user-attachments/assets/82b04bfc-8408-4242-a9df-be06c542b777" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="1191" alt="sed6" src="https://github.com/user-attachments/assets/32c7e16b-9b37-40b5-a7b2-9bf10fdca76b" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="1191" alt="sed7" src="https://github.com/user-attachments/assets/d4facac6-4f7c-4fb9-b7f3-f5dea04b0cb1" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="1191" alt="sed8" src="https://github.com/user-attachments/assets/5bbf9ea7-88f9-4f6c-a52d-8e9194f32695" />



seq 10 
## OUTPUT

<img width="1191" alt="seq1" src="https://github.com/user-attachments/assets/d1ef01b3-260e-4abe-bceb-92c59909654c" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="1191" alt="seq2" src="https://github.com/user-attachments/assets/a039817b-c64a-4cfe-b808-b8891988370d" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="1191" alt="seq3" src="https://github.com/user-attachments/assets/b89f41ea-9b65-4a12-beba-7c41179fb46e" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="1191" alt="seq4" src="https://github.com/user-attachments/assets/4cf6de86-f042-49d5-9419-4d8fd010edce" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="1191" alt="seq5" src="https://github.com/user-attachments/assets/34bc8d29-e0d8-4fe9-b725-a6e84c1a8eac" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="1191" alt="seq6" src="https://github.com/user-attachments/assets/99438aee-b175-471b-a0e2-6ebdcc86a7c5" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="1191" alt="seq7" src="https://github.com/user-attachments/assets/f0d2ec80-3278-41c9-b8e2-b33428f5f930" />



sed -n '2,4{s/$/*/;p}' file23

<img width="1191" alt="seq8" src="https://github.com/user-attachments/assets/ab7fe8bb-e10f-4927-9590-b3625921475c" />

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

<img width="1191" alt="sort" src="https://github.com/user-attachments/assets/bc15a88f-3377-46b0-8729-bd00bf7f10e0" />

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

<img width="1191" alt="uniq" src="https://github.com/user-attachments/assets/27d79cbf-bf2a-4fda-bc98-52e56a569912" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1220" alt="catfile23" src="https://github.com/user-attachments/assets/8e0df2ed-b9e9-4b84-8082-081f41dbd672" />

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
<img width="1150" alt="caturl1" src="https://github.com/user-attachments/assets/e1a72ccc-8b64-4933-90f0-f57a8c5ccc55" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1262" alt="caturl2" src="https://github.com/user-attachments/assets/07364a57-7023-4c07-b14b-740c69209feb" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="983" alt="tar1" src="https://github.com/user-attachments/assets/7670366f-e0eb-400d-911a-badb79dbdc92" />


mkdir backupdir
 
mv backup.tar backupdir

<img width="983" alt="mv1" src="https://github.com/user-attachments/assets/a6635164-8826-4f58-87b5-a54bcdbb4b64" />



tar -xvf backup.tar
## OUTPUT
<img width="983" alt="tar2" src="https://github.com/user-attachments/assets/2496985f-c7e3-4272-a845-a0c2a18f8b5a" />


gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT
<img width="983" alt="ls1" src="https://github.com/user-attachments/assets/68bd80e6-96b0-42aa-8b9b-f4a9e247cd2f" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="1303" alt="echo1" src="https://github.com/user-attachments/assets/8d165606-e831-4c2a-973f-14db685a2df3" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="1303" alt="catherecheck" src="https://github.com/user-attachments/assets/50ac0bb8-bca0-46f5-82cd-3d565ce5bef2" />

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
<img width="1303" alt="catscriptcheck" src="https://github.com/user-attachments/assets/942b4ea1-ec6c-43bf-898b-988873f7ae72" />

 
ls file1
## OUTPUT
<img width="1303" alt="ls_1" src="https://github.com/user-attachments/assets/93add8ed-e013-4248-927c-8d03c7541f15" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="1303" alt="echo_1" src="https://github.com/user-attachments/assets/22b3ddc6-a456-4f36-a9af-b55cbcef9bbc" />

abcd
 
echo $?
 ## OUTPUT
<img width="1303" alt="echo_2" src="https://github.com/user-attachments/assets/3a6c452f-5a5e-4a15-8735-bb07fd93440e" />


 
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


<img width="1303" alt="cat_Strcmp" src="https://github.com/user-attachments/assets/40c207f5-f779-40c5-b775-c6503e0314f9" />

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="1303" alt="strcmp" src="https://github.com/user-attachments/assets/e744fe46-4771-40ee-a889-a68fbdec9af4" />


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

<img width="1303" alt="ifnested" src="https://github.com/user-attachments/assets/c33a0e2e-deb9-4b00-b5b8-8e9626c294d9" />


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

<img width="1303" alt="iftest" src="https://github.com/user-attachments/assets/6a6d58dc-79c6-4a06-8a76-bce2cafe5877" />


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

<img width="1303" alt="ifnested" src="https://github.com/user-attachments/assets/6fb30944-fda8-4d86-b051-e86bc3fd7a89" />


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

<img width="1303" alt="elifcheck" src="https://github.com/user-attachments/assets/37534cfc-c78f-471c-b808-569db530689f" />


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
<img width="1303" alt="ifcompound" src="https://github.com/user-attachments/assets/30fe1fd5-71a7-4ffc-825e-0c564f07c78b" />

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

<img width="1303" alt="casecheck" src="https://github.com/user-attachments/assets/f920c16c-d029-49f0-9cac-e587a2018d89" />

 
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
<img width="1303" alt="whiletest" src="https://github.com/user-attachments/assets/c9d64415-c97a-49e8-bdd8-41d2da6a51b0" />

 
 
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
 
 
 <img width="1303" alt="untiltest" src="https://github.com/user-attachments/assets/f549e5df-3afb-4947-8ea6-108b4e7d026a" />

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
 
 <img width="1303" alt="forin1" src="https://github.com/user-attachments/assets/dd712351-1925-4257-acc5-d69dd2c68458" />

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

<img width="1303" alt="forin2" src="https://github.com/user-attachments/assets/0bfc94ce-7428-4842-9e94-65e1c1296b72" />

 
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

<img width="1303" alt="forin2" src="https://github.com/user-attachments/assets/239b8daa-6040-4be3-89c3-f4115d08dea8" />

 
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
 <img width="1303" alt="forin3" src="https://github.com/user-attachments/assets/465ad0e5-7d1f-4108-8c2a-7b7856a0d24f" />
 
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

<img width="1303" alt="forinfile" src="https://github.com/user-attachments/assets/adbd9c85-e097-47f4-9def-d42269e236ac" />


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
<img width="1303" alt="forctype" src="https://github.com/user-attachments/assets/6e521446-5381-4ac4-bd84-220f98c110cd" />

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
<img width="1303" alt="forctype1" src="https://github.com/user-attachments/assets/8117d7d0-079b-4a32-ac57-8c2379973660" />

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
<img width="1303" alt="forneseted1" src="https://github.com/user-attachments/assets/4d3220bf-a789-42f7-b245-318fd39a057d" />

 
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

<img width="1303" alt="forbreak" src="https://github.com/user-attachments/assets/07555fb2-312c-484e-a82e-8139c65877d8" />


$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT


 <img width="1303" alt="forcontinue" src="https://github.com/user-attachments/assets/a1f2b19e-13bc-4051-8dd8-87bc32fa03ac" />

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
<img width="1303" alt="exread" src="https://github.com/user-attachments/assets/c8f06798-8715-4b20-8f07-9cde1aad8f34" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 



$ ./exread1.sh 
<img width="1303" alt="exread1" src="https://github.com/user-attachments/assets/4c4670e1-7db3-493f-b439-827a01fd5b3b" />

 
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

 <img width="1303" alt="funcex" src="https://github.com/user-attachments/assets/70a93c3e-974d-4654-8a7a-4c4ac45b7891" />

 ./funcex.sh 1 2

 <img width="1303" alt="funcex123" src="https://github.com/user-attachments/assets/c6aeb4b1-3284-4957-a213-06ccd06d3203" />

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
 <img width="1303" alt="argshift" src="https://github.com/user-attachments/assets/b244b511-f5da-45a0-9444-8a68f239201a" />

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
<img width="1303" alt="argshift1" src="https://github.com/user-attachments/assets/508da503-fe88-4deb-911e-59b96954fc00" />

 
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
 <img width="1303" alt="argshift3" src="https://github.com/user-attachments/assets/607483fa-bfca-4b71-b5ce-d11b8ed2a692" />

 
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
 <img width="1303" alt="awk" src="https://github.com/user-attachments/assets/892543fa-0a5d-4843-a158-d0566e8b0078" />

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
<img width="1303" alt="pallindrome" src="https://github.com/user-attachments/assets/6ffc5f26-1495-4d67-92a2-adce8d370906" />


# RESULT:
The Commands are executed successfully.
