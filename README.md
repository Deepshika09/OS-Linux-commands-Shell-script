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
![image](https://github.com/user-attachments/assets/9830e29d-dd61-4073-8e03-3157636bb7c2)



cat < file2
## OUTPUT
![image-1](https://github.com/user-attachments/assets/7efe5f94-f0b2-454f-acca-44d0f94b4643)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image-2](https://github.com/user-attachments/assets/273a80f4-8f12-41f8-a33d-39879ba82f03)

comm file1 file2
 ## OUTPUT
![image-3](https://github.com/user-attachments/assets/51db5c75-d6a3-4e6f-82f5-4cb86244a97b)

 
diff file1 file2
## OUTPUT
![image-4](https://github.com/user-attachments/assets/73619bfd-09b8-4cb1-ac57-65bd706f7e3e)


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
![image-5](https://github.com/user-attachments/assets/fbc640fd-de38-4004-aab5-d790a73e6375)





cut -d "|" -f 1 file22
## OUTPUT

![image-6](https://github.com/user-attachments/assets/e24e6540-efcc-4e97-a246-9615e3dea995)







cut -d "|" -f 2 file22
## OUTPUT

![image-7](https://github.com/user-attachments/assets/9ede83ec-5603-4af7-a0a1-87f5a80f59bd)




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
![image-14](https://github.com/user-attachments/assets/004cb5a3-5d36-4933-adfb-2590cdd05b14)



grep hello newfile 
## OUTPUT
![image-13](https://github.com/user-attachments/assets/e59e9a72-f761-4726-8cd7-41fe35173934)





grep -v hello newfile 
## OUTPUT
![image-12](https://github.com/user-attachments/assets/1140af95-11b7-41dd-97e8-ce7dc2bd4405)





cat newfile | grep -i "hello"
## OUTPUT
![image-11](https://github.com/user-attachments/assets/309a6352-8ac5-4641-a182-e3a81f30f31e)





cat newfile | grep -i -c "hello"
## OUTPUT
![image-10](https://github.com/user-attachments/assets/4a32ab19-52f5-49c3-a6fe-4e369a99b1a2)




grep -R ubuntu /etc
## OUTPUT
![image-9](https://github.com/user-attachments/assets/021e16c8-1a31-4843-ba38-8b32b890ae0d)



grep -w -n world newfile   
## OUTPUT
![image-8](https://github.com/user-attachments/assets/4a0808e4-def8-43d7-aa34-f0008eb9ef29)



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
![image-15](https://github.com/user-attachments/assets/2412b399-4b42-4a7a-bbd9-f2e6a2216216)

egrep -w 'Hello|hello' newfile
## OUTPUT
![image-16](https://github.com/user-attachments/assets/3d63a92a-8024-4034-9133-be13b7d7ad69)

egrep -w '(H|h)ello' newfile 
## OUTPUT
![image-17](https://github.com/user-attachments/assets/7378b3f8-2398-409c-954a-33f6c502cd25)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image-18](https://github.com/user-attachments/assets/bfdc8cba-b8aa-4fa5-978c-903934182dc5)




egrep '(^hello)' newfile 
## OUTPUT
![image-19](https://github.com/user-attachments/assets/45536b70-0b75-40e3-9cff-5f701eb268bb)




egrep '(world$)' newfile 
## OUTPUT
![image-20](https://github.com/user-attachments/assets/06089148-a2a7-4e48-aad7-e34fc217487c)



egrep '(World$)' newfile 
## OUTPUT
![image-21](https://github.com/user-attachments/assets/1d127835-b8a2-456c-9b59-693716664934)



egrep '((W|w)orld$)' newfile 
## OUTPUT



egrep '[1-9]' newfile 
## OUTPUT
![image-23](https://github.com/user-attachments/assets/622fcca5-13d6-4ac8-b392-7e492f47ae02)




egrep 'Linux.*world' newfile 
## OUTPUT
![image-24](https://github.com/user-attachments/assets/9233a0a1-cd63-49c5-a54d-11b2b4cb3ff8)


egrep 'Linux.*World' newfile 
## OUTPUT
![image-25](https://github.com/user-attachments/assets/91e4d718-4c65-4c53-a2f2-f1d6add641d8)


egrep l{2} newfile
## OUTPUT
![image-26](https://github.com/user-attachments/assets/2cee45fc-8818-421f-a8db-bc0cca2e7422)



egrep 's{1,2}' newfile
## OUTPUT 
![image-27](https://github.com/user-attachments/assets/43c08305-d574-4ea2-a86c-7f7b5d909d6b)


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
![image-28](https://github.com/user-attachments/assets/ec9f333b-3449-4052-a650-0271b352a839)



sed -n -e '$p' file23
## OUTPUT
![image-29](https://github.com/user-attachments/assets/9ab435aa-d9e5-474d-b386-0e9039c7638e)




sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image-30](https://github.com/user-attachments/assets/51068a1a-7062-42f7-ad07-1766bf6fdf6c)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image-31](https://github.com/user-attachments/assets/a8dfb7e7-33a7-4dcb-998a-4836ebbf513c)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image-32](https://github.com/user-attachments/assets/118aa05a-83dc-4a26-a425-7b95b05b5917)



sed -n -e '1,5p' file23
## OUTPUT
![image-33](https://github.com/user-attachments/assets/dbb5c64b-26d4-49b2-8723-823726bf11b3)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image-34](https://github.com/user-attachments/assets/7e9e97fa-ce1e-4a42-879e-8f6ccb4ee93a)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image-35](https://github.com/user-attachments/assets/b7c1bad4-4ab9-409e-abf6-979dc7fb8ff4)



seq 10 
## OUTPUT
![image-36](https://github.com/user-attachments/assets/6c8fe54d-cf65-4b31-8ca9-20730d4150dc)



seq 10 | sed -n '4,6p'
## OUTPUT
![image-37](https://github.com/user-attachments/assets/f605014d-4394-490c-b19d-6020825374bf)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image-38](https://github.com/user-attachments/assets/5ad89a7f-7b69-42d7-9e3f-b6785d63e9b6)



seq 3 | sed '2a hello'
## OUTPUT
![image-39](https://github.com/user-attachments/assets/25b395ec-7e6b-41e3-96ba-f12165c601f1)



seq 2 | sed '2i hello'
## OUTPUT
![image-40](https://github.com/user-attachments/assets/d5606124-411a-4cbb-b5bc-417fb07a57a8)


seq 10 | sed '2,9c hello'
## OUTPUT

![image-41](https://github.com/user-attachments/assets/8de47478-61a0-4e16-bc0e-096bc045505f)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image-42](https://github.com/user-attachments/assets/3a36b23d-1ed9-401e-b812-75cc1613c14e)



sed -n '2,4{s/$/*/;p}' file23
![image-43](https://github.com/user-attachments/assets/eebec4e4-38b3-4f48-8ee3-70f8fa03c641)


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
![image-44](https://github.com/user-attachments/assets/9fd46dab-3a8b-4be6-b518-00e1e9746219)


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
![image-45](https://github.com/user-attachments/assets/23ebcd11-fca3-47de-aad1-d55bee92a646)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image-46](https://github.com/user-attachments/assets/49b52620-ee99-4f18-ab2e-dab8f9f76182)


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

![image-47](https://github.com/user-attachments/assets/280fbcfb-4224-4dc5-b5d9-2d8224e05350)



cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image-49](https://github.com/user-attachments/assets/c42961e3-6d12-4e49-99fd-429f7b267dd1)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image-50](https://github.com/user-attachments/assets/eee48db0-a29d-4a39-b224-03837c0f3d09)



mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image-51](https://github.com/user-attachments/assets/7bf4fb05-edbb-45db-b272-e4ea80e6aacd)



tar -xvf backup.tar
## OUTPUT



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

 
ls file1
## OUTPUT


 
echo $?
## OUTPUT 


abcd
 
echo $?
 ## OUTPUT


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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
##OUTPUT

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
## OUTPUT

 
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
