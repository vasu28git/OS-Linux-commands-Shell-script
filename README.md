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

chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty


cat > file2

anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta


### Display the content of the files
cat < file1
## OUTPUT

![WhatsApp Image 2025-03-06 at 09 52 25_8f20116d](https://github.com/user-attachments/assets/b47d9e7f-8f12-4194-b118-d2c5fe6d41c4)


cat < file2
## OUTPUT

![WhatsApp Image 2025-03-06 at 08 30 18_3d5463eb](https://github.com/user-attachments/assets/cae9d00c-7524-4ec2-88e2-c92eccb6ec3b)


# Comparing Files
cmp file1 file2
## OUTPUT
![WhatsApp Image 2025-03-06 at 08 31 43_189f23ea](https://github.com/user-attachments/assets/91e101cb-9e38-41e1-892f-38aca67c9917)


comm file1 file2
 ## OUTPUT
![WhatsApp Image 2025-03-06 at 08 42 28_a4497b6a](https://github.com/user-attachments/assets/40612b78-5466-481c-8688-26202431fc1d)


 
diff file1 file2
## OUTPUT

![WhatsApp Image 2025-03-06 at 08 42 29_9f461f8b](https://github.com/user-attachments/assets/a71609a3-41c5-4c2d-a2b6-053b6c92e410)


#Filters

### Create the following files file11, file22 as follows:

cat > file11

Hello world
This is my world


cat > file22

1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer




cut -c1-3 file11
## OUTPUT

![WhatsApp Image 2025-03-06 at 08 42 26_805b83a4](https://github.com/user-attachments/assets/98844d1b-2e6b-4902-a9d3-5df412746e8f)




cut -d "|" -f 1 file22
## OUTPUT


![WhatsApp Image 2025-03-06 at 08 42 27_b6ba3670](https://github.com/user-attachments/assets/88f4871f-45eb-4c95-8881-2400f657aadd)


cut -d "|" -f 2 file22
## OUTPUT
![WhatsApp Image 2025-03-06 at 08 42 26_3d08651c](https://github.com/user-attachments/assets/ea634112-fe56-4aca-9f86-7f687d7866fe)



cat < newfile 

Balaji's world
balaji's world
`
cat > newfile 
Balaji's world
balaji's world
 
grep Balaji newfile 

grep balaji newfile 
## OUTPUT

![WhatsApp Image 2025-03-06 at 08 42 27_8b8dd54a](https://github.com/user-attachments/assets/a8839c7f-add2-4138-acfc-431167b6961d)




grep -v balaji newfile 

cat newfile | grep -i "balaji"

cat newfile | grep -i -c "balaji"
## OUTPUT

![WhatsApp Image 2025-03-06 at 08 42 27_9fd9de1e](https://github.com/user-attachments/assets/8734e638-ed85-4e91-bd48-2f379996419b)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/cb2cb8a6-a131-4887-89f5-5b732558b27e)



grep -w -n world newfile   
## OUTPUT

![WhatsApp Image 2025-03-06 at 08 56 40_990b81c5](https://github.com/user-attachments/assets/e0c0f7b1-0411-4ab7-9a81-2b539a6a5a79)


cat < newfile 

Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World


cat > newfile

Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
 
egrep -w 'Hello|hello' newfile 

egrep -w '(H|h)ello' newfile 

egrep -w '(H|h)ell[a-z]' newfile 

egrep '(^hello)' newfile 

egrep '(world$)' newfile 

egrep '(World$)' newfile 

egrep '((W|w)orld$)' newfile 

egrep '[1-9]' newfile 

egrep 'Linux.*world' newfile 

egrep 'Linux.*World' newfile 

egrep l{2} newfile

egrep 's{1,2}' newfile
## OUTPUT 

![WhatsApp Image 2025-03-06 at 09 20 59_85e9767f](https://github.com/user-attachments/assets/a0c84a45-0dab-430b-abe7-4795b535bf3c)


cat > file23

1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR




sed -n -e 'p' file23

sed -n -e '$p' file23
## OUTPUT

![WhatsApp Image 2025-03-06 at 09 13 39_5532bd63](https://github.com/user-attachments/assets/e5038619-f474-4fb5-a7b2-8235bf7d8f71)

sed  -e 's/Sam/Ram/' file23

sed  -e '2s/Sam/Ram/' file23

sed  -e '2s/Ram/Sam/' file23

sed  '/Sam/s/5000/6000/' file23
## OUTPUT

![WhatsApp Image 2025-03-06 at 09 13 39_acc5fe99](https://github.com/user-attachments/assets/b7338a4c-415e-4ea8-9bcf-642b858dc082)



sed -n -e '1,5p' file23
## OUTPUT

![WhatsApp Image 2025-03-06 at 09 13 26_484c35e0](https://github.com/user-attachments/assets/e0fc8837-41ca-4dae-b2d7-e10fc5b9db23)



sed -n -e '2,/Joe/p' file23

sed -n -e '/tom/,/Joe/p' file23

sed -n -e '/Ram/,/Joe/p' file23

## OUTPUT

![WhatsApp Image 2025-03-06 at 09 29 14_ca9864b2](https://github.com/user-attachments/assets/708cbb13-86fb-4b95-970b-f7cec674c7c1)



seq 12 

seq 12 | sed -n '4,7p'
## OUTPUT

![WhatsApp Image 2025-03-06 at 09 16 03_a64ae3b9](https://github.com/user-attachments/assets/6f287744-552f-4f2c-a850-39f66571f776)


seq 10 | sed -n '2,~4p'

seq 10 | sed -n '2,~4p'

seq 3 | sed '2a hello'
## OUTPUT

![WhatsApp Image 2025-03-06 at 09 16 03_6fe603e2](https://github.com/user-attachments/assets/710b2463-5ec7-4539-a03d-7634017f2efa)



seq 2 | sed '2i hello'

seq 10 | sed '2,9c hello'
## OUTPUT

![WhatsApp Image 2025-03-06 at 09 16 03_0583f268](https://github.com/user-attachments/assets/efbff654-0156-4f5c-ba45-6f1ac90d0d19)


sed -n '2,4{s/^/$/;p}' file23

sed -n '2,4{s/$/*/;p}' file23

## OUTPUT


![WhatsApp Image 2025-03-06 at 09 34 20_a32c6f32](https://github.com/user-attachments/assets/8acfcb53-6221-438d-bff0-36224d481f16)


#Sorting File content
cat > file21

1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
 
sort file21
## OUTPUT

![WhatsApp Image 2025-03-06 at 09 34 20_675a10c1](https://github.com/user-attachments/assets/c63cee93-26e4-4233-abe6-7e90a73f9097)


cat > file22

1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
 
uniq file22
## OUTPUT

![WhatsApp Image 2025-03-06 at 09 34 20_827143e3](https://github.com/user-attachments/assets/978d8017-a9c8-4fb9-b4b8-e4937eabdb9d)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![WhatsApp Image 2025-03-06 at 09 34 19_6655a39c](https://github.com/user-attachments/assets/4bc4ea3d-fdeb-4aa1-88cf-f62c273010a7)


cat < urllist.txt

www. yahoo. com
www. google. com
www. mrcet.... com

 
cat > urllist.txt

www. yahoo. com
www. google. com
www. mrcet.... com
 
cat urllist.txt | tr -d ' '
 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![WhatsApp Image 2025-03-06 at 13 42 12_22c5b1e5](https://github.com/user-attachments/assets/67951f3d-66ac-42a3-b0f0-ac2f2323a719)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
bench.py file1 file11 file2 file21 file22 file23 hello.c hello.js newfile readme.txt urllist.txt



mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

-rw-r--r-- user/group 0 2024-02-25 14:30:00 file1.txt drwxr-xr-x user/group 0 2024-02-25 14:30:00 directory1/ -rw-r--r-- user/group 1024 2024-02-25 14:30:00 directory1/file2.txt -rw-r--r-- user/group 2048 2024-02-25 14:30:00 directory1/file3.txt
tar -xvf backup.tar
## OUTPUT

x file1.txt x directory1/ x directory1/file2.txt x directory1/file3.txt gzip backup.tar

ls .gz
## OUTPUT
backup.tar.gz 
gunzip backup.tar.gz
## OUTPUT
backup.tar
 
# Shell Script

echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh

chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/468990be-a1b5-486a-99f7-d1466f8267c2)

 
cat << stop > herecheck.txt

hello in this world
i cant stop
for this non stop movement
stop


cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/cf71fe63-4fbb-45f5-b416-8278c7b4514a)

cat < scriptest.sh 
bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " basename $0
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps

 

cat scriptest.sh 
bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " basename $0
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps

 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
File name is ./scriptest.sh File name is scriptest.sh First arg. is 1 Second arg. is 2 Third arg. is 3 Fourth arg. is The @ i s 1 2 3 T h e
## is 

$#
The $

ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/b35e55ac-0ee7-49cf-8bb5-b39020e5eceb)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/142905b0-ad86-4c7f-8af5-9b19d9bf2edb)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT

1
 
# mis-using string comparisons

cat < strcomp.sh 
bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi



cat strcomp.sh 
bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi

## OUTPUT
![image](https://github.com/user-attachments/assets/a11a9d91-54b4-4487-9760-b15feb551665)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
baseball is less than hockey



# check file ownership
cat < psswdperm.sh 
bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi



cat psswdperm.sh 
bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 
./psswdperm.sh
## OUTPUT
You are the owner of the /etc/passwd file


# check if with file location
cat>ifnested.sh 
bash
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


cat ifnested.sh 

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


./ifnested.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/2ced2148-e58d-4e9f-b0fb-c02b65aa8f97)



# using numeric test comparisons
cat > iftest.sh 
bash
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




cat iftest.sh 
bash
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


$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
bash
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



cat ifnested.sh 
bash
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


$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
bash
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


$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/1e03c2e1-e4b1-4c5c-889c-dccfc86bce82)


# testing compound comparisons
cat> ifcompound.sh 
bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi

$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/481d0481-1bc9-4e94-a03e-cdc91a7cbd6a)

# using the case command
cat >casecheck.sh 
bash
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

$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done

$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done

$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done

$ ./forin3.sh 
 
cat forin1.sh 
bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done

$ chmod 755 forin1.sh

## OUTPUT
Welcome Ram Please enjoy your visit Welcome Rahim Please enjoy your visit Special testing account gganesh, Do not forget to logout when you're done Sorry, you are not allowed here
cat forinfile.sh 
bash
#!/bin/bash
# reading values from a file
file="cities"
for state in cat $file
do
echo "Visit beautiful $file“
done

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
bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
`
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done

$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
bash
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

$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 1 - 5 2 - 4 3 - 3 4 - 2 5 - 1


cat forbreak.sh 
bash
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

## OUTPUT
Iteration number: 1 Iteration number: 2 The for loop is completed


$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
bash
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


 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
Iteration number: 1 Iteration number: 2 Iteration number: 4 Iteration number: 5 The for loop is completed 
cat exread.sh 
bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
Enter your name: John Hello John, welcome to my program.



 cat exread1.sh
bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
 
$ chmod 755 exread1.sh 

## OUTPUT
Enter your name: John Hello John, welcome to my program.


$ ./exread1.sh 
 
cat funcex.sh
bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=func $1 $2
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi

## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done

$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
bash
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

$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x

## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
bash
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
 
cat>data.dat
bash
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

awk -f nc.awk data.dat
## OUTPUT 
total characters 75 Number of Lines are 10 No of Words count: 10

 
cat > palindrome.sh
bash
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

## OUTPUT 
Enter the number 121 Number is palindrome Enter the number 69 Number is NOT palindrome

# RESULT:
The Commands are executed successfully.
