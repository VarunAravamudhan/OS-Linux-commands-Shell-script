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

![Screenshot from 2025-04-29 05-12-44](https://github.com/user-attachments/assets/55740618-64cc-47ab-ba5e-b23b964f29cd)


cat < file2
## OUTPUT
![Screenshot from 2025-04-29 05-13-11](https://github.com/user-attachments/assets/dbc08229-250e-4f0b-b48a-1e16ee2cdd44)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot from 2025-04-29 05-17-03](https://github.com/user-attachments/assets/763b280d-1bac-43c9-93cd-fdb0c1c4a109)

comm file1 file2
 ## OUTPUT
![Screenshot from 2025-04-29 05-17-58](https://github.com/user-attachments/assets/6639c7dd-f525-4c87-a4f6-8128770f41bb)

 
diff file1 file2
## OUTPUT
![Screenshot from 2025-04-29 05-18-24](https://github.com/user-attachments/assets/afadaa10-e95b-466c-9c36-b671cd07ed94)


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

![Screenshot from 2025-04-29 05-20-34](https://github.com/user-attachments/assets/dc92680d-f9f8-4c4f-b1b8-e13e57af8720)



cut -d "|" -f 1 file22
## OUTPUT

![Screenshot from 2025-04-29 05-21-34](https://github.com/user-attachments/assets/5289c95f-295f-4272-9808-7d798fd79323)


cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-04-29 05-22-18](https://github.com/user-attachments/assets/1c97a257-db8c-42d1-b4db-20e3ca70c1fe)


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

![Screenshot from 2025-04-29 05-25-14](https://github.com/user-attachments/assets/9d504c51-cae6-40b3-af07-71293a8d12f1)


grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-04-29 05-25-49](https://github.com/user-attachments/assets/3c307432-7980-4384-9884-21722b1dae28)



cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2025-04-29 05-26-29](https://github.com/user-attachments/assets/40cabd4d-d017-4f76-b4b5-a9070de0ffbf)



cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot from 2025-04-29 05-27-08](https://github.com/user-attachments/assets/bb59503e-beae-4a11-a3ec-9212d887a56b)



grep -R ubuntu /etc
## OUTPUT

![Screenshot from 2025-04-29 05-28-01](https://github.com/user-attachments/assets/9ba78c29-2aea-433b-b24e-92dc2fa1d7b4)


grep -w -n world newfile   
## OUTPUT
![Screenshot from 2025-04-29 05-28-39](https://github.com/user-attachments/assets/c4a7c496-c417-42dc-af68-490ed45b2893)


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

![Screenshot from 2025-04-29 05-30-34](https://github.com/user-attachments/assets/12206c57-f5b0-4614-b984-6b0c9f99f2bd)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot from 2025-04-29 05-30-58](https://github.com/user-attachments/assets/15a6e0e0-a349-4cfe-8eb4-7a03a5076dcd)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2025-04-29 05-31-57](https://github.com/user-attachments/assets/ba345e7f-c6b0-4c4b-a2e1-40089fa222b1)



egrep '(^hello)' newfile 
## OUTPUT

![Screenshot from 2025-04-29 05-44-20](https://github.com/user-attachments/assets/6724ac6f-eed4-4789-a88b-1e7ca7134d86)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot from 2025-04-29 05-45-00](https://github.com/user-attachments/assets/d5b3ba97-51f7-4a2c-8d9c-cb6aa1531b1c)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot from 2025-04-29 05-46-19](https://github.com/user-attachments/assets/55178807-9888-4511-8788-f940c4ba01e5)


egrep '[1-9]' newfile 
## OUTPUT

![Screenshot from 2025-04-29 05-46-49](https://github.com/user-attachments/assets/03bf66eb-eeb2-450c-b6a2-351ca6514549)


egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-04-29 05-47-32](https://github.com/user-attachments/assets/52be21f3-11e3-4608-a93a-63c3aab16c31)



egrep l{2} newfile
## OUTPUT

![Screenshot from 2025-04-29 05-47-52](https://github.com/user-attachments/assets/33fbd317-cdf7-44fe-9153-27bc2946061b)


egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-04-29 05-48-15](https://github.com/user-attachments/assets/0ae398c1-de82-4b66-8c0e-6cea83e59097)


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

![Screenshot from 2025-04-29 05-49-08](https://github.com/user-attachments/assets/6339f62e-5e22-4ec0-afd0-3bf8124f545e)


sed -n -e '$p' file23
## OUTPUT

![Screenshot from 2025-04-29 05-50-21](https://github.com/user-attachments/assets/1c21373d-01fa-431e-a8f7-e5001c97f167)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-04-29 05-51-32](https://github.com/user-attachments/assets/109f06cd-54c8-43d1-bb49-17b65317fac5)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-04-29 05-51-54](https://github.com/user-attachments/assets/35e17f17-fac3-42b1-bd13-c92ee487e797)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot from 2025-04-29 05-52-13](https://github.com/user-attachments/assets/6e520cb2-ba93-4f7c-95f8-b99aeb0b22e8)


sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2025-04-29 05-53-02](https://github.com/user-attachments/assets/5faa1b0a-5700-4d40-b608-fb750c42421c)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-04-29 05-53-37](https://github.com/user-attachments/assets/e05e7cdc-0a46-4900-9028-c1aaae7d34fb)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-04-29 05-54-05](https://github.com/user-attachments/assets/ea4e926c-97e7-4269-a356-74cf272652b0)


seq 10 
## OUTPUT

![Screenshot from 2025-04-29 05-54-30](https://github.com/user-attachments/assets/e38599c4-d147-4a04-9385-45cd9995f0c3)


seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2025-04-29 05-54-55](https://github.com/user-attachments/assets/58da7dde-e000-4afb-94b8-f0c2e047e843)


seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot from 2025-04-29 05-55-16](https://github.com/user-attachments/assets/6e1d2a2c-812a-441a-90eb-df45efa423b7)


seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2025-04-29 05-55-43](https://github.com/user-attachments/assets/d379992d-0430-4884-b8d7-f3d6c4f861b0)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2025-04-29 05-56-03](https://github.com/user-attachments/assets/45373810-12d0-4107-8788-1073274fa1ad)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2025-04-29 05-56-28](https://github.com/user-attachments/assets/5ff743c7-5e4a-4fcf-bf52-14d092313ac5)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot from 2025-04-29 05-56-46](https://github.com/user-attachments/assets/00e2e23e-438e-4155-9580-ff4acb5ca7a0)


sed -n '2,4{s/$/*/;p}' file23
![Screenshot from 2025-04-29 05-57-11](https://github.com/user-attachments/assets/b6fc7459-566e-420b-9004-51a24b70c058)


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
![Screenshot from 2025-04-29 05-58-11](https://github.com/user-attachments/assets/1733de4c-e040-48e0-a265-a8507c64f7fd)


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

![Screenshot from 2025-04-29 05-59-23](https://github.com/user-attachments/assets/3a279896-c6ae-490c-a303-d5933926b81d)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2025-04-29 05-59-44](https://github.com/user-attachments/assets/7bcab91e-8639-4091-8eda-310ad5553e85)

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
![Screenshot from 2025-04-29 06-01-22](https://github.com/user-attachments/assets/c18b0c5f-4bd8-44bd-961c-8e8d542d2f64)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot from 2025-04-29 06-01-40](https://github.com/user-attachments/assets/90e6e5de-f8a0-4345-bba8-c9e3c0942a20)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![Screenshot from 2025-04-29 06-02-16](https://github.com/user-attachments/assets/c1f489b5-adbb-4b7e-9d2b-2c848d9bde34)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot from 2025-04-29 06-17-16](https://github.com/user-attachments/assets/445ccd29-2d94-4391-b4c5-ba9c92b7216f)


tar -xvf backup.tar
## OUTPUT
![Screenshot from 2025-04-29 06-17-58](https://github.com/user-attachments/assets/1759c980-61db-4cdf-945d-d41a595efe7a)

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT
![Screenshot from 2025-04-29 06-19-18](https://github.com/user-attachments/assets/95e90a59-fbb4-4099-a64e-9a6ce6dea386)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![Screenshot from 2025-04-29 06-26-15](https://github.com/user-attachments/assets/0aebd046-07f8-40c4-95f7-3cddca3d852f)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot from 2025-04-29 06-26-59](https://github.com/user-attachments/assets/54a4cd4f-3326-4b06-aaca-f944aa9e707d)


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
![Screenshot from 2025-04-29 06-29-35](https://github.com/user-attachments/assets/2d7996df-196a-4eae-ad7b-73afa11dea2c)

 
ls file1
## OUTPUT
![Screenshot from 2025-04-29 06-31-40](https://github.com/user-attachments/assets/915b25e3-6049-43f4-8867-2ff5c9890e70)

echo $?
## OUTPUT 

![Screenshot from 2025-04-29 06-32-02](https://github.com/user-attachments/assets/6b12d03a-c0e9-43b6-9792-1dc836e5c8bf)
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![Screenshot from 2025-04-29 06-33-17](https://github.com/user-attachments/assets/f94f70e2-7ee2-4c5d-8a89-10385ad8c742)


abcd
 
echo $?
 ## OUTPUT
![Screenshot from 2025-04-29 06-33-17](https://github.com/user-attachments/assets/98acad95-f227-470a-8abe-4dccbfe1737a)


 
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
