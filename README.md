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
// git add-h // git commit // git origin
### Display the content of the files
cat < file1
## OUTPUT
![image](https://github.com/user-attachments/assets/7c6c057c-2e22-45e9-a8e1-f3a27a1f283d)




cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/f28ef78b-8790-4490-bfe4-d03e48105c09)



# Comparing Files
cmp file1 file2
## OUTPUT
 
comm file1 file2
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/e6e79679-1e68-4b90-acd3-8fcc89686573)


 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/5c781199-c4ea-4d9e-8d2e-448643511859)


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
![image](https://github.com/user-attachments/assets/6e0f1181-c380-4eaf-8e54-250bfdfd83c0)




cut -d "|" -f 1 file22
## OUTPUT


![image](https://github.com/user-attachments/assets/16cbeea8-bb48-4127-ae85-1003f7a0ffe5)

cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/b8088ffa-3ff0-4b76-ba6c-852e75dddf04)

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

![image](https://github.com/user-attachments/assets/6ce2b0bb-5366-4799-b354-4d21f2cd65ed)


grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/f6b45569-fae7-48ac-a34a-26b6fe3bdc15)




grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/9fd70726-8c02-4474-9959-841d36f4537e)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/2746d902-9183-4e4c-b3bc-f16d837746ee)



cat newfile | grep -i -c "hello"
## OUTPUT


![image](https://github.com/user-attachments/assets/8ef67672-2eca-4379-a61c-e5b8adf7aad6)


grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/68ff0f86-c4b3-4ecb-b6b2-5ef8de892682)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/db2d8883-83fb-4749-a658-c37ffabb5359)


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
![image](https://github.com/user-attachments/assets/db13dba2-e76f-4e7a-b820-e7dab6e436dd)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/71a89697-3d9f-4bab-9f29-2fb7ce2f7fb7)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/343dd23a-78a2-4437-954c-00f6b54fb372)



egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/b0b97273-7bc6-43a2-8103-4e91dd4ce04b)



egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/6d3b1fed-da75-4d43-ac16-5cef4c3af2c0)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/af57e43e-cdad-4570-be37-ddbae525e5c8)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/c121afc7-7b88-4f2f-933d-f90739c9e153)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/55cd3528-1b5e-4ac5-9581-c953df36dc66)


egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/f772b42e-510d-4780-a3c1-0a2bfb1a9cde)

egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/755d3a55-13f8-4328-8a81-e7491a974c63)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/db9d1c5d-5377-4220-ac96-0543766d0467)


egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/user-attachments/assets/88a96262-38f1-46d5-aa6e-7b9ee816d391)


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

![image](https://github.com/user-attachments/assets/7f1cbd2b-5c89-4b20-b454-ab9b5f76032a)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/2ed1cae8-acdb-4078-9d92-3b481fb2916f)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/df07627d-877c-4a3d-bcc1-5d14387bc896)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/61552df4-441b-4b57-9845-41b7e2475d88)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/108a83d4-37ca-4d52-a87e-74522c378a27)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/de1b641c-c6cf-4ed1-b826-53d2d221fb5e)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/4e5b0641-347c-412d-bbdf-9a8d25addec4)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/617efcb8-51a5-42aa-b0f1-92fde56427f3)

seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/fe5e0173-f326-42d9-aa19-cdc1306aa5d9)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/user-attachments/assets/1421c1ef-659e-4f42-96cd-660ecc1ad213)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/f8c92f25-0ba5-438f-a079-eaad9a6cdd6c)


seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/8cfb2f56-9419-4700-93ad-dd3b47ae2f31)


seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/dad52dcc-6633-44c8-9511-4b0f99693fb6)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/0a66306f-0d01-4ed5-b99a-65708d60363b)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/a6f81f47-22c1-4fac-9521-f340c65ed56e)


sed -n '2,4{s/$/*/;p}' file23

![image](https://github.com/user-attachments/assets/8e70d3a3-1172-4ff5-929d-e72cfd7a6dc0)

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

![image](https://github.com/user-attachments/assets/11d857bc-957d-4fd8-b573-1c919593e76c)

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
![image](https://github.com/user-attachments/assets/e534de4b-5437-458b-9813-90f8706d8dc3)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/6fa0adf6-98cd-480a-8522-aa20a306f63b)

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
![image](https://github.com/user-attachments/assets/f4f38888-3bb0-436e-8b0d-614f1e171928)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/92649d19-fa00-4c5c-b441-f985886d426b)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/user-attachments/assets/1f140e59-3ad3-4592-99e3-4123ab5b67fe)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/5bff060c-a0bf-41f4-91e7-17f077c873aa)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/fcd400ca-58ce-4f11-a147-afe01108e94a)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/c7831e7e-62c4-495f-a879-51b70c0a671f)

gunzip backup.tar.gz
## OUTPUT

 ![image](https://github.com/user-attachments/assets/9265c0d2-3fbf-44c3-a834-314fe1f196d4)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/4af920b5-857d-496a-b7a1-96dc8127d348)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/67750d9e-6a15-401a-8f95-0dfdf932cc2a)

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
![image](https://github.com/user-attachments/assets/0c1c41a8-68ed-425b-9d78-9f399dd014e6)

 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/230f8e00-208b-485e-98f1-abe393ba78fc)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/c0a358bc-fce8-4d5e-9ba0-54a1e8cb23f8)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![image](https://github.com/user-attachments/assets/256fda63-42b0-482c-b0b5-08dbbe9ed8ac)

abcd
 
echo $?
 ## OUTPUT
![image](https://github.com/user-attachments/assets/6506050f-6ea8-4ef2-810d-97c88fdce68c)


 
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
![image](https://github.com/user-attachments/assets/cbb0cf92-c8d6-420f-a620-91db0195c6b7)


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
![image](https://github.com/user-attachments/assets/d86ff3c7-ba51-4684-afcc-646d53f8ae0a)

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
![image](https://github.com/user-attachments/assets/e30059cd-7d7f-4286-88a8-b6340164c61d)



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
![image](https://github.com/user-attachments/assets/cbe44f90-9ba1-435e-ad9e-84aa90c834c5)


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
![image](https://github.com/user-attachments/assets/04a65d38-826d-4ea5-9124-6f3ec42cac60)


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
![image](https://github.com/user-attachments/assets/4031756a-c0be-495d-8157-301126928cae)

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
![image](https://github.com/user-attachments/assets/b00fbeda-907f-467b-bd09-ff9be8420e41)

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

![image](https://github.com/user-attachments/assets/6e13d1cd-fa9c-4002-9a1a-e7537c2c0bbd)

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
![image](https://github.com/user-attachments/assets/72c3e75b-3bcc-42c3-be0d-38fad2f13e2e)

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
![image](https://github.com/user-attachments/assets/7e10e4a9-73ea-4fe8-b285-c8869fc9c116)

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
![image](https://github.com/user-attachments/assets/8c1ecf03-fac7-4b6c-917d-b9a0ef616cc5)

 
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
 ![image](https://github.com/user-attachments/assets/56acbc2e-b3f4-4768-b770-950c6aabf99d)

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

![image](https://github.com/user-attachments/assets/8935a75a-367d-4d44-9e17-df42824b5cab)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![image](https://github.com/user-attachments/assets/1ef32fad-69da-4dae-8f92-d66cc6509b50)


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

 ![image](https://github.com/user-attachments/assets/670d40ba-2954-4318-82ab-56508b6c618d)

 ./funcex.sh 1 2
![image](https://github.com/user-attachments/assets/025cee2b-6a8f-4f12-8a41-8ed05ae33443)

 
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
 ![image](https://github.com/user-attachments/assets/7ca7df72-c17e-496b-b5c7-7e35d16f4b83)

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
 ![image](https://github.com/user-attachments/assets/fbefda53-5ac3-47fe-965c-fdefe741690b)

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
 ![image](https://github.com/user-attachments/assets/6d503c74-6253-47f8-a35f-20ccb06f1348)

 
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
 ![image](https://github.com/user-attachments/assets/992bc35c-2a60-4c5c-ae8b-8cf1e0844c42)

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
![image](https://github.com/user-attachments/assets/4e3e77b2-8055-41a0-a54f-3653d6ec11c7)


# RESULT:
The Commands are executed successfully.
