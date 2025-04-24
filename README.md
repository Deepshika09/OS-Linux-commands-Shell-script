![Screenshot 2025-04-23 230525](https://github.com/user-attachments/assets/fa8320c2-cfbc-42f3-ae2d-fe451224353a)# OS-Linux-commands-Shell-scripting
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
![Screenshot 2025-04-23 225029](https://github.com/user-attachments/assets/f2337184-0fd0-4391-90d5-64e2e52bb545)



cat < file2
## OUTPUT
![Screenshot 2025-04-23 225039](https://github.com/user-attachments/assets/08eb0f04-d5e9-428b-a98b-66f73aa88192)


# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot 2025-04-23 225045](https://github.com/user-attachments/assets/ea354280-9878-4fe5-bb09-419d85cfb48c)
 
comm file1 file2
 ## OUTPUT
![Screenshot 2025-04-23 235405](https://github.com/user-attachments/assets/d7de986d-304e-4e7e-bd31-b3a6bbf21314)

 
diff file1 file2
## OUTPUT
![Screenshot 2025-04-23 225100](https://github.com/user-attachments/assets/5a15c3d7-a236-4166-95f3-c1af0e8fbfcc)


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
![Screenshot 2025-04-23 225108](https://github.com/user-attachments/assets/a1cc76c2-b63a-4a77-85b9-4885384249e1)





cut -d "|" -f 1 file22
## OUTPUT
![Screenshot 2025-04-23 235639](https://github.com/user-attachments/assets/d4a36b5e-04ae-46b1-b890-a095b37669df)








cut -d "|" -f 2 file22
## OUTPUT
![Screenshot 2025-04-23 225115](https://github.com/user-attachments/assets/8d2bf3b5-faa1-4c66-9c6e-cd824179916b)





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
![Screenshot 2025-04-23 225125](https://github.com/user-attachments/assets/ba8713e6-ecf4-4cac-acdf-c0f53f9da941)



grep hello newfile 
## OUTPUT
![Screenshot 2025-04-24 000257](https://github.com/user-attachments/assets/52f3d480-8952-4cd0-ae48-3bdcde2543e2)





grep -v hello newfile 
## OUTPUT
![Screenshot 2025-04-24 000734](https://github.com/user-attachments/assets/7a1b5bbd-0b41-4139-84e1-f697b1ad9ee6)





cat newfile | grep -i "hello"
## OUTPUT
![Screenshot 2025-04-23 225145](https://github.com/user-attachments/assets/a075bc9c-90e0-40fd-abdd-4f66ccbf89e0)





cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot 2025-04-23 225155](https://github.com/user-attachments/assets/7ced75d4-f6a1-4bcb-bf75-5e906ced7226)




grep -R ubuntu /etc
## OUTPUT
![Screenshot 2025-04-23 225202](https://github.com/user-attachments/assets/bcfe555a-0553-41e2-aeec-bb691145b554)



grep -w -n world newfile   
## OUTPUT
![Screenshot 2025-04-23 225209](https://github.com/user-attachments/assets/42ebf254-e5f4-4bc8-8035-abb6687a09c4)



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
## OUTPUT
![Screenshot 2025-04-23 225217](https://github.com/user-attachments/assets/7f9dd7a5-1058-4652-b492-556f0ad9ac3b)

egrep -w 'Hello|hello' newfile
## OUTPUT
![Screenshot 2025-04-23 225225](https://github.com/user-attachments/assets/e5aec0a5-b736-43e0-9ac3-421cdf703cba)

egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot 2025-04-23 225233](https://github.com/user-attachments/assets/d71f1406-8425-4fd1-b062-1194d15f1def)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot 2025-04-23 225244](https://github.com/user-attachments/assets/0730b24a-ab15-49f9-9004-cbc97ba60104)




egrep '(^hello)' newfile 
## OUTPUT
![image-19](https://github.com/user-attachments/assets/a0aab168-ccb2-4bf4-ba83-c7167cda37f9)




egrep '(world$)' newfile 
## OUTPUT
![image-20](https://github.com/user-attachments/assets/18c8bd69-8e00-4bfe-bca5-6ada7777d03d)



egrep '(World$)' newfile 
## OUTPUT
![image-21](https://github.com/user-attachments/assets/c877dadd-e1bc-4ee3-a917-98002b6fb5f3)



egrep '((W|w)orld$)' newfile 
## OUTPUT
![image-22](https://github.com/user-attachments/assets/886291f5-5be0-4963-a136-292c02272a9f)



egrep '[1-9]' newfile 
## OUTPUT
![image-23](https://github.com/user-attachments/assets/88cda344-7d98-439f-9dab-48088022b8c7)




egrep 'Linux.*world' newfile 
## OUTPUT
![image-24](https://github.com/user-attachments/assets/e7dd7115-619b-459e-81b3-2c919ff5ba3b)


egrep 'Linux.*World' newfile 
## OUTPUT
![image-25](https://github.com/user-attachments/assets/24f32723-e77d-43c2-82e2-17281f756b45)


egrep l{2} newfile
## OUTPUT
![image-26](https://github.com/user-attachments/assets/8af46287-7706-4f8d-b257-eb818978d424)



egrep 's{1,2}' newfile
## OUTPUT 

![image-27](https://github.com/user-attachments/assets/cacf3451-7f1c-4abf-80e9-06f484c7a338)

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
![image-28](https://github.com/user-attachments/assets/93c73fee-4573-43e3-b699-a2a0321120d6)



sed -n -e '$p' file23
## OUTPUT
![image-29](https://github.com/user-attachments/assets/7543f1a9-c42b-46c9-bd2c-3c6219ec3a36)




sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image-30](https://github.com/user-attachments/assets/f29bb24f-4fa1-4b92-a6cc-779ca7d999e9)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image-31](https://github.com/user-attachments/assets/f555b550-f233-4485-9bf5-7c3b75796bcc)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image-32](https://github.com/user-attachments/assets/a313e62c-f018-4a10-9b29-adbba20a70ed)



sed -n -e '1,5p' file23
## OUTPUT
![image-33](https://github.com/user-attachments/assets/c8ded6f2-b1b3-4acf-bc02-351a9db67578)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![image-34](https://github.com/user-attachments/assets/cb284d8e-76fb-4f57-87a6-7897e4c4ff81)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image-35](https://github.com/user-attachments/assets/26eb54d6-3404-4643-b6a4-cd843f4f8c07)


seq 10 
## OUTPUT

![image-36](https://github.com/user-attachments/assets/136ccf3a-1291-44ae-a6b2-4c12f10dd379)


seq 10 | sed -n '4,6p'
## OUTPUT
![image-37](https://github.com/user-attachments/assets/63a487bc-f919-419e-ae7d-c4bf40f6e97a)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image-38](https://github.com/user-attachments/assets/ecb1571b-623b-43d6-84a7-60eba0d66112)



seq 3 | sed '2a hello'
## OUTPUT
![image-39](https://github.com/user-attachments/assets/dae4ca81-045b-4f92-a70f-ec5988864dfa)



seq 2 | sed '2i hello'
## OUTPUT
![image-40](https://github.com/user-attachments/assets/59199e7f-9b91-4808-b5d0-c41598c80509)


seq 10 | sed '2,9c hello'
## OUTPUT

![image-41](https://github.com/user-attachments/assets/93faee7d-c2c3-4a03-be14-78364112fbf7)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image-42](https://github.com/user-attachments/assets/d5366a36-4cf1-49b8-9800-dd22f7792629)



sed -n '2,4{s/$/*/;p}' file23
![image-43](https://github.com/user-attachments/assets/e146a4e5-7b4b-4b35-9944-4ee37a731d86)


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

![image-44](https://github.com/user-attachments/assets/b2265297-7dbb-466d-bc04-9ec7d278466c)

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
![image-45](https://github.com/user-attachments/assets/c70a91f2-573b-4881-9943-af5c690a6af6)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image-46](https://github.com/user-attachments/assets/2c367ccc-44a3-46fb-90c8-196a5845a0a8)

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

![image-48](https://github.com/user-attachments/assets/9c66f797-b2c5-42ce-9f0a-10bd0893963d)



cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image-49](https://github.com/user-attachments/assets/859d5835-6e95-47f6-8344-0cbd04f821f6)



#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image-50](https://github.com/user-attachments/assets/bded481b-dc61-42be-900d-90f3a2c3001f)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image-51](https://github.com/user-attachments/assets/d980d6d9-4232-4d14-8e43-394a7a60518e)



tar -xvf backup.tar
## OUTPUT
![image-53](https://github.com/user-attachments/assets/0b2e626a-8cf4-4e51-be27-1cc7a7584094)



gzip backup.tar

ls .gz
## OUTPUT
![image-55](https://github.com/user-attachments/assets/fe31331f-d862-4a27-b9ea-4c86b7b7ccc7)

gunzip backup.tar.gz
## OUTPUT

 ![image-56](https://github.com/user-attachments/assets/9255958b-1032-4991-bdd8-530d1fbcc8bf)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot 2025-04-23 230129](https://github.com/user-attachments/assets/6c6eb7f4-89f9-4cc9-910d-467792777813)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot 2025-04-23 230142](https://github.com/user-attachments/assets/e63862c0-e116-4aaa-a2b0-e48989275be5)


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
![Screenshot 2025-04-23 230351](https://github.com/user-attachments/assets/4fddc25f-933d-498d-8e41-c28f34f8446e)

 
ls file1
## OUTPUT
![Screenshot 2025-04-23 230358](https://github.com/user-attachments/assets/b4626e90-9fec-4def-874a-c923350c4c76)


 
echo $?
## OUTPUT 
![Screenshot 2025-04-23 230406](https://github.com/user-attachments/assets/63fdbca2-5a76-4888-bbef-d6d135e25452)


abcd
 
echo $?
 ## OUTPUT
![Screenshot 2025-04-23 230414](https://github.com/user-attachments/assets/2e45c5b6-ec65-48ca-a409-32047617be3c)


 
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
#OUTPUT
![Screenshot 2025-04-23 230427](https://github.com/user-attachments/assets/53b4cd42-7035-4dcc-8266-4c7b53bd7374)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot 2025-04-23 230436](https://github.com/user-attachments/assets/ebcd1e21-1b35-436d-b273-5fcc948dc89e)


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
![Screenshot 2025-04-23 230446](https://github.com/user-attachments/assets/b3deb4a0-0d34-497c-bc12-244766c435d4)

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
![Screenshot 2025-04-23 230455](https://github.com/user-attachments/assets/697b9eb9-d7e1-4d3d-8c7a-ba0fa4440a0f)



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

![Screenshot 2025-04-23 230503](https://github.com/user-attachments/assets/33f01a7d-b1be-49fb-97fd-e112f41df276)


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
![Screenshot 2025-04-23 230511](https://github.com/user-attachments/assets/5ab86ff0-de32-47c3-a090-e33d543bf1fd)

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
![Screenshot 2025-04-23 230518](https://github.com/user-attachments/assets/7ff0e39e-6b27-4719-a5f4-c522985a04ef)


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
![Screenshot 2025-04-23 230525](https://github.com/user-attachments/assets/b7457ca7-b517-48c9-95f9-5f43f44828eb)

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
##OUTPUT
 ![image-71](https://github.com/user-attachments/assets/3634dd82-69ba-4f94-b4e7-8c9cd3981c67)

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
 ![image-72](https://github.com/user-attachments/assets/59508d99-0822-41a7-af60-560058ff7ded)

 
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
 ![image-73](https://github.com/user-attachments/assets/602158d2-0318-4a4b-aaf8-52d3629bf372)

 
 
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
 ![image-74](https://github.com/user-attachments/assets/b06e0522-c2f9-4bbf-9bc9-05da62e06b3d)

 
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
 ![image-75](https://github.com/user-attachments/assets/dc095dda-ed81-43a2-9536-3e7499948fb2)

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
