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
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/990e3c0e-4ef6-4020-be02-e0368ff0707a)


cat < file2
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/43c841ef-f0dd-4ea6-8a90-69c72b029d3a)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/b6e72211-0a4e-4207-b8dc-46f19001e54a)

comm file1 file2
 ## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/af030636-2f36-4ab1-9564-35c11cc4580d)

 
diff file1 file2
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/06f04685-cfbc-4680-b2e6-c04fc76a07ea)


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
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/0915a411-7f72-4864-8de3-926f0fe6c20b)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/308be17e-f10b-4e76-abd3-52888921c6be)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/071f76bd-597a-4f57-ae2b-2fdf268078ce)


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
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/c5b2510f-944f-47a3-877a-193ca86822f7)



grep hello newfile 
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/2c6b423b-58a5-4f33-9458-df04573e9b5d)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/fedad5b0-ff73-465d-86a6-2dfda1efa235)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/7e4e328d-fcc6-4ee6-8c7c-f5a61a624f2c)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/c26b2cf1-5f32-45ec-a988-e729f96cfcdf)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/91d52069-574f-4fba-b34e-6aa2f57e99e7)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/2bb0f288-9350-428f-8bed-ac102457fc2f)


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
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/7a25abda-86c4-4ae3-a123-ee4b42940f9e)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/0c1be946-342b-4799-b2c0-d8c79b6fd21c)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/cc830c5d-7b1d-476d-b4e3-ead91f519797)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/aafde351-2579-43ee-8607-47ca0ece070b)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/e83a27c8-39e8-48db-8b92-379cc2eff5b5)




egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/94398dbe-073c-4368-adcd-f6fc766ddac2)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/dc1f407f-ad2c-493c-ab18-3a57c34e8d85)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/a5254ca3-08e8-427f-864f-f7f1d674a1fc)



egrep 'Linux.*world' newfile 
## OUTPUT
![307819748-1f1213e7-2332-4b09-8e19-848e11e181f0](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/af9a5317-c4da-42d3-8da2-a8ebb0f5c4e4)




egrep 'Linux.*World' newfile 
## OUTPUT
![307819767-ab478792-c42f-4445-b1a2-440ff695da03](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/e267ace2-e9ac-4225-8237-e8576bd4eaf1)


egrep l{2} newfile
## OUTPUT
![307819822-5a44dd5b-69cc-48a5-aea1-0845340a9c61](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/5f7520d6-7ab0-4913-bc4b-c3b3c64eab29)



egrep 's{1,2}' newfile
## OUTPUT 
![307819859-0885bcb9-919a-4121-8b62-74b8c009f624](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/8a201656-263e-4ef8-969d-5ae9e9475cad)


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
![307820049-a513754b-cf31-4ed1-acf3-ef00c43489dc](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/f130e54c-49c0-4cdd-8d26-a0235b338576)



sed -n -e '$p' file23
## OUTPUT
![307820072-2f52bda9-c176-4d5c-8e9b-16e1f6fd9ef7](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/480d68bb-d3f9-4bcc-b56d-410cea0dc912)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![307820093-79c77842-269c-463f-941e-7c0309436900](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/9a5b10e5-e284-4563-9698-703a2992be3f)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![307820147-2466363f-9b1c-43e3-b99e-4ec92e5308b8](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/02591b86-afe9-4f2a-a848-ec1d2a418921)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![307820172-405cd5a4-e05f-4727-83ea-f6342462cee9](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/70e0243c-53b5-4433-aabe-8fdbe636dc5e)



sed -n -e '1,5p' file23
## OUTPUT
![307820217-13796c7c-1769-4f0f-b67f-ec712ea606bd](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/cc85789b-f373-4aa0-9042-83b1e5c57cf1)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![307820241-21d301d2-34a9-4fee-9b1c-f5b2f7ee0c89](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/203158bd-7275-4391-9143-16cf26d0f0ab)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![307820292-a2a87c87-9e0b-4e95-af6c-ea31f54f16a5](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/57fa1047-ecf0-4509-a070-e8608b800ed1)



seq 10 
## OUTPUT
![307820308-bcc3d504-bb73-4dea-96a7-b3f8426171b7](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/4d4ffca0-7d5a-42a6-832f-a75b9ddfcde1)



seq 10 | sed -n '4,6p'
## OUTPUT
![307820349-a5aa4533-52ef-41ef-88dc-5163706d6ba3](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/14b3694b-8244-44d3-8663-5c39e7a04516)



seq 10 | sed -n '2,~4p'
## OUTPUT
![307820384-67dc5a22-14aa-4adc-8517-bd7cfb63c68e](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/0aec1922-1162-4395-8aa8-f9785a1b25e3)



seq 3 | sed '2a hello'
## OUTPUT
![307820399-016e5dcf-ac27-45fc-86e1-6afa139c4cf6](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/5b2b5ed2-86d5-4039-a439-8494d69b233e)



seq 2 | sed '2i hello'
## OUTPUT
![307820429-54518b9c-4627-43ff-83b3-0e18403d5285](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/2aa12bfc-3b23-4449-a5e0-4337572f337b)


seq 10 | sed '2,9c hello'
## OUTPUT
![307820477-33c73d05-ef2c-48e1-a8c5-be4979946e86](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/5a9e1a40-794d-4287-b63e-16ef68a9f9cf)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![307820498-d5ed9af0-a6fa-4950-af0e-c7326f0d23e4](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/f090cbba-f56e-448b-8940-6fe55583a859)



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
![307820945-8d80c952-66f4-41da-a538-bfaa6d2e568d](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/db123eae-c57f-4983-9f3b-938529a4446c)


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
![307820976-949d21fe-620b-4f94-aac3-528743bd4a2e](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/cf4ab5f5-98f9-4512-933c-9495fa723618)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![307821010-bbacc088-5799-46db-a898-b71da63a5d28](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/7334fc18-e767-4963-b8e3-655409814e95)

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
![307821035-c0f73c0b-1055-4c31-8bdd-2a368649eabc](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/d02bc3e0-969c-4eff-8ab3-aef3bbbe6da2)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![307821054-1655fa9a-c163-4677-8fd2-b58545573d3c](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/e542ea8d-523b-4c4e-9be4-bc5192471046)




#Backup commands
tar -cvf backup.tar *
## OUTPUT
bench.py
file1
file11
file2
file21
file22
file23
hello.c
hello.js
newfile
readme.txt
urllist.txt

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
-rw-r--r-- user/group 0 2024-02-25 14:30:00 file1.txt
drwxr-xr-x user/group 0 2024-02-25 14:30:00 directory1/
-rw-r--r-- user/group 1024 2024-02-25 14:30:00 directory1/file2.txt
-rw-r--r-- user/group 2048 2024-02-25 14:30:00 directory1/file3.txt

tar -xvf backup.tar
## OUTPUT
x file1.txt
x directory1/
x directory1/file2.txt
x directory1/file3.txt
gzip backup.tar

ls .gz
## OUTPUT
  backup.tar.gz
gunzip backup.tar.gz
## OUTPUT
backup.tar
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![307824234-cd6aa88e-aa03-4879-8eac-096a80a8bf1a](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/e4b3746a-09ac-4cbf-916a-3503322ac2c8)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![307824796-7449297d-09c9-4e47-9593-2a2ae75545ea](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/d561e3eb-850a-4824-943d-92e5615f72ec)


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
File name is ./scriptest.sh
File name is scriptest.sh
First arg. is 1
Second arg. is 2
Third arg. is 3
Fourth arg. is
The $@ is 1 2 3
The $\# is $#
The $$ is 124
 
ls file1
## OUTPUT
![307825432-c2ffd586-64f4-4d86-814f-53fd3b966af5](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/50e708bb-82d0-461d-8c49-352bc8929aa7)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 ![307826499-e004d6ed-48ab-45a6-bfd8-ab8faa8788b5](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/be1b16a7-4c9c-435b-9198-894f852ed6b2)

echo $?
## OUTPUT 
 ![307826499-e004d6ed-48ab-45a6-bfd8-ab8faa8788b5](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/0ebae798-2dc0-4168-b30e-77643735e826)

abcd
 
echo $?
 ## OUTPUT
1

 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
baseball is less than hockey

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
You are the owner of the /etc/passwd file
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
![307832276-efa998fe-2806-4eca-ace7-1d71dda33cf6](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/de662c39-84e4-4c2c-a0c6-5d4ffd716cbe)



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
![307833052-545398c0-2c77-4e44-b53a-6ef098142c6f](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/29804794-8113-4713-aa4b-f9fd3d48a097)

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
![307833801-3f9abd70-a9ff-43f5-9b46-39fd1f374d55](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/2fd148d4-bb33-420b-a740-46669fe24b68)

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
Welcome Ram
Please enjoy your visit
Welcome Rahim
Please enjoy your visit
Special testing account
gganesh, Do not forget to logout when you're done
Sorry, you are not allowed here

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
![307834688-73bf26c3-76c2-4dbe-8aa4-213a1cef52fb](https://github.com/230131249/OS-Linux-commands-Shell-script/assets/150232701/b186aa90-fa9f-4745-935c-d28d82266e4c)

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
 Welcome Ram/Rahim
Please enjoy your visit
Special testing account
gganesh, Do not forget to logout when you're done
Sorry, you are not allowed here
cat > whiletest
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
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
Visit beautiful Hyderabad
Visit beautiful Alampur
Visit beautiful Basara
Visit beautiful Warangal
Visit beautiful Adilabad
Visit beautiful Bhadrachalam
Visit beautiful Khammam

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
The value of i is 1
The value of i is 2
The value of i is 3
The value of i is 4
The value of i is 5
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
1 - 5
2 - 4
3 - 3
4 - 2
5 - 1
 
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
Iteration number: 1
Iteration number: 2
The for loop is completed 
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
 Iteration number: 1
Iteration number: 2
Iteration number: 4
Iteration number: 5
The for loop is completed
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
Enter your name: sanju
Hello sanju, welcome to my program.


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
$ bash script.sh 1 2
The result is 2
 
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
 1
2
3
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
 1
2
3
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
 1
2
3
 
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
total characters 75
Number of Lines are 10
No of Words count: 10 
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
Enter the number
121
Number is palindrome
Enter the number
69
Number is NOT palindrome

# RESULT:
The Commands are executed successfully.
