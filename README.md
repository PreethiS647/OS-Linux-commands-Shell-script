![image](https://github.com/user-attachments/assets/bf0c7f1a-9cfd-4ab8-afbb-bde14ec241c7)# OS-Linux-commands-Shell-scripting
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
![Screenshot 2024-08-29 130613](https://github.com/user-attachments/assets/8a2139b5-7b26-4730-8f67-4de00a143071)



cat < file2
## OUTPUT
![Screenshot 2024-08-29 130627](https://github.com/user-attachments/assets/85565c47-510b-47d3-a7de-58cbc784e153)



# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot 2024-08-29 130652](https://github.com/user-attachments/assets/0e3a24cd-4599-4a39-ba43-8985869695d9)

 
comm file1 file2
 ## OUTPUT
 ![Screenshot 2024-08-29 130722](https://github.com/user-attachments/assets/4859a66d-4dca-42c2-bc9f-1c5d9b9e4124)


 
diff file1 file2
## OUTPUT
![Screenshot 2024-08-29 130749](https://github.com/user-attachments/assets/fc5060ab-4e45-4bd5-8934-350a45fac5a7)



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
![image](https://github.com/user-attachments/assets/99a347cc-bd2b-475b-80b0-5a604c534653)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/84ccc9ea-738d-4335-b31c-f623445b157f)




cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/01ed6b70-2293-4000-8632-a0a32fc3ff54)



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
![image](https://github.com/user-attachments/assets/c03d3427-bd98-4bdb-b3b1-777ba376f712)



grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/4492edde-1b44-4078-aa98-de686b99c59e)





grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/61af03cc-1b56-479d-9e3b-f0432135f913)




cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/1cefedfb-11b9-4435-b654-60b64af6729c)





cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/103a7985-18ca-45b9-ba72-4316dced4430)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/1bda7d43-7ba0-4f1f-a9e6-404a6742eef5)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/3b46d01b-312c-4004-afd1-94c566e5748e)


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
![image](https://github.com/user-attachments/assets/d379c628-254b-4fb4-945c-72b65d557fe0)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/af500807-6530-4481-a74f-5554314dca5f)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/f63f8284-523f-4d29-b46f-52026f2a245d)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/0da7e2dd-1b60-42d3-b54f-3cea35373f87)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/41c22967-09a7-4b12-84a3-a9f0f845f926)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/a2113c41-438c-48b3-a59a-4eb57fd630a9)



egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/ea8a2b78-68d2-439e-bd03-939acf970700)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/84d23897-591e-42fa-b275-e7c23c86209d)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/b2f4ad84-ca1e-4a94-85bd-ec4f6155ba4b)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/db1e76f1-e6f0-4e77-9e31-5b8d5e9e0542)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/c6a07cfa-c843-4c81-9590-ff1f4486e57e)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/e648a0ea-e3e5-4f5a-86cf-48ef570bf32d)


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
![image](https://github.com/user-attachments/assets/fbcec426-18b1-4ae7-ae24-1711b167ee35)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/aa0291e3-d597-4f9a-8a63-8a5ea84c28c2)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/bb087828-7ef1-4c7c-abe6-2c6b1651386a)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/691726a6-3083-496f-b1b7-c24e5bbb7712)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/8d262e5e-59dc-49e6-88bc-7f5140f762a9)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/2869d53e-8b7c-4da0-b93c-0f660b31cd5f)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/8f9bcc39-ed35-4ebf-a1f6-5d3e096e15a1)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/567dbed6-4901-494c-ba6d-5009c635cf73)



seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/e8a609c4-a2ae-4d40-872a-06db5e5dd9cb)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/1635a4d2-fb72-42be-986e-0b9155e0e93f)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/1687b563-1bfe-44ee-bb9c-94d29927765e)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/dd807311-daab-47a3-acb3-39375a07f4b4)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/9bfb99a2-34c1-4a8a-a8e6-c6913f7b117f)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/a3245388-2c74-41eb-801e-2ecbea3c28d9)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/5ff2115d-cedb-4ec0-bf41-a76e608546be)



sed -n '2,4{s/$/*/;p}' file23
![image](https://github.com/user-attachments/assets/add38dfa-5991-47eb-a23a-3de22df1d2e2)


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
![image](https://github.com/user-attachments/assets/32f210b1-665f-4247-a19f-f446d343e543)


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
![image](https://github.com/user-attachments/assets/6a8fdbad-6580-44a6-b918-0e429d5c57ef)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/fefd4ed6-9dcf-4244-a453-e5f6bba421bd)

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
![image](https://github.com/user-attachments/assets/8411388c-565a-4cbc-8171-8a995e35a0bb)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/53b98695-0982-4e0b-aa62-ecef01db5722)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/22c97505-4785-4854-a42d-0d179b3da5c0)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tarch
## OUTPUT
![image](https://github.com/user-attachments/assets/ddefa1ae-0dda-43ec-98fe-6b18bd32f929)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/8d51547e-9bb2-45c3-ad39-3aa54731277a)

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![309631646-8b571dc0-2f93-4ab2-a314-0055d7559ee3](https://github.com/user-attachments/assets/bdbeaba1-6c6d-4aa4-91d8-4d52bfc2f70b)


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


![306541597-f05197ce-9a61-4432-8677-06f9a3f2074d](https://github.com/user-attachments/assets/aa2e68eb-a85b-49d7-8bae-9e8e1ac41a6c)



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

![309631701-66ce463b-a769-4ce7-9701-472a735ec84e](https://github.com/user-attachments/assets/cc956190-634b-44c1-b207-7e5a8a5bd1d5)

 
ls file1
## OUTPUT
![306542056-6d43e64c-5b38-4b4c-953d-15306e4f0962](https://github.com/user-attachments/assets/d58b77db-57bd-4004-b98c-af20e4b04624)

echo $?
## OUTPUT 

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![306542294-e207d92e-1b49-4f24-bf5e-6b509e151ca3](https://github.com/user-attachments/assets/cb731033-7eae-45d8-b9a7-503b3f0e7d29)


abcd
 
echo $?
 ## OUTPUT
![309631818-84516bf6-930b-4545-8031-e8922ded7758](https://github.com/user-attachments/assets/bb57ac5e-bf92-487b-bcc3-bfa86ee7cc3d)


 
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

![307678773-f5691f96-7fb8-405b-aca8-99b245694866](https://github.com/user-attachments/assets/80df37c4-cdc1-47fa-87a1-3d98db73c6a7)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![307678773-f5691f96-7fb8-405b-aca8-99b245694866](https://github.com/user-attachments/assets/60b9e463-fe65-4822-9568-02ce7e04d989)

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
![307679532-9e14508f-e06b-48bd-8335-24ab45869507](https://github.com/user-attachments/assets/e5a3c27d-93c7-4bc7-98db-c8ca4c89c70c)

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

![307680054-a3bbfe31-a584-41fa-bb8e-34f6a8c71c2d](https://github.com/user-attachments/assets/deb67691-1767-4bc2-ab90-bc4ba4522de6)

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
![307680530-f0324dc3-e174-4c13-9e62-2b8e12f0ece8](https://github.com/user-attachments/assets/4c24e2fc-9db2-41b0-aced-8fb495b48bea)

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
![307681129-4d51cbe0-75a7-4c8b-9897-31d80e242b23](https://github.com/user-attachments/assets/6486c565-1a45-4818-9e76-e5b92290c578)

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

![307682021-b23da05d-9057-4155-a3b3-e0d5e1658424](https://github.com/user-attachments/assets/b0236171-6f31-42b0-ba26-ce4f2a4a55fd)

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
![307682427-dd2856b3-6746-4001-9bb5-64248d70cbf2](https://github.com/user-attachments/assets/3a14a83a-ad48-46b4-ba5e-2328aff60e9c)

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
## Output
![307682893-2089b93c-f8f4-4aa2-9a14-7ad18c022649](https://github.com/user-attachments/assets/38ca3490-1f1e-460b-b777-5a414d491840)

 
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
## Output
![309632182-01d121de-472d-4dbd-b7b9-3b02b5273151](https://github.com/user-attachments/assets/9996f8ed-e01a-4134-80c5-56a3bef57f1c)

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
 ## Output
 ![309632243-37852111-38c2-4d5b-b02e-db081bb55911](https://github.com/user-attachments/assets/2e2458d6-7e60-4a50-9e34-a89a4aa5b8fa)

 
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
## Output
 ![308472685-5db0aa23-2b65-47be-845b-d27e71d1cf0e](https://github.com/user-attachments/assets/2818612a-431f-4e09-93e5-e2f8217aad6a)

 
cat forin2.sh 
```
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
## Output
![308473693-e871a57b-eba5-4f24-beaa-b50a1cc05f9d](https://github.com/user-attachments/assets/9823553b-dd23-4e47-b515-5170200ee4b7)

cat forin3.sh

```
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 

 ## Output
 ![308474292-3e502c00-aa25-42d7-94f4-c1cf42abbeb0](https://github.com/user-attachments/assets/b4478b85-9584-4f04-b1e6-3d7ddbfc856c)

 
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
![308474845-57eb9b7e-55ed-4f8a-b04f-299ca7312d54](https://github.com/user-attachments/assets/4a5e1a93-89ca-496c-a041-4514579d846e)


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
## Output
![309632485-a2fc3dd0-6460-481c-93c6-644032cf66bf](https://github.com/user-attachments/assets/3d82255f-17b4-4e92-a775-feeb5596d904)


$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
![308475810-23e57dee-3012-407b-a599-187a55addb7b](https://github.com/user-attachments/assets/1b044ef9-b54e-4cdd-b860-a54c371c2a5a)


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
![308478403-2811cf5c-8f23-497a-8175-1e53557b62ab](https://github.com/user-attachments/assets/ee24f0f1-9e97-4f1e-bcdb-1ed610308f16)

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
![309632774-25c8eba9-2ae6-4b0d-aee8-0f5bdc40756f](https://github.com/user-attachments/assets/1e1c02d2-8e6d-405f-8812-b72e6263d575)

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
![309632814-7ff92879-790a-4e10-b53d-b3f846385518](https://github.com/user-attachments/assets/643e362e-31fe-4f2a-8d43-f7c27a6f5392)

 
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
![308486165-605c7e2c-66cc-4915-b199-f4a7fe1f3dc7](https://github.com/user-attachments/assets/dc5888bb-19f3-45e6-893f-1dfec873577a)

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
![308486693-85d238ab-8b91-4dd4-a8a6-6b840499c3ba](https://github.com/user-attachments/assets/b6377886-a9a5-4485-9aec-7c0486a5976b)


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

![308487155-321f81e4-81c7-499b-b9f5-1cab56f6288f](https://github.com/user-attachments/assets/9e77ecd3-14c8-4782-b001-24cb3c4578bf)


$ ./exread1.sh 
 

## Output
![308487155-321f81e4-81c7-499b-b9f5-1cab56f6288f](https://github.com/user-attachments/assets/98c3adba-24ce-4f45-8ec6-bf569a061b9a)

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
 ./funcex.sh 

 
 ./funcex.sh 1 2
## OUTPUT

![308487638-cdfc76b5-6701-4b9d-ac3a-d01716b50612](https://github.com/user-attachments/assets/18a70dc0-3382-4f19-b9d3-307d9867ac4b)

 
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

![309633105-d16bf8f4-1339-48cf-a69f-099205f74514](https://github.com/user-attachments/assets/094866e6-6f90-4917-a314-30bd06a53b74)

 
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
## Output
![309633163-71f9847b-4423-43ed-9b5a-6fe1b1902839](https://github.com/user-attachments/assets/d545c665-87c7-4d61-8d98-50adf4004a68)


 
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

 ![309633163-71f9847b-4423-43ed-9b5a-6fe1b1902839](https://github.com/user-attachments/assets/1b2b62ae-fb3d-46be-88fd-902a52e6e2e6)

 cat argshift.sh
``` #!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
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
 ![309633292-8a81067c-381e-4a78-a1f8-a6b503c919a4](https://github.com/user-attachments/assets/624c68c7-40b7-43db-9182-20eacfd861d9)
 
![309633318-895da9ca-8150-4a82-907a-1ee93a57e361](https://github.com/user-attachments/assets/02af4c1e-1040-42fb-abff-0f79171f39ca)

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
![369747944-378f9ac8-e25b-47cb-af40-7c43e8bf4c18](https://github.com/user-attachments/assets/aaed910e-8378-4c7d-a076-29b397c86c82)


# RESULT:
The Commands are executed successfully.
