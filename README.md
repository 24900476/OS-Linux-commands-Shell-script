# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting
### NAME : KABIRA A
### Reg NO : 212224040146
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
<img width="235" height="117" alt="image" src="https://github.com/user-attachments/assets/23dbeddc-5f23-42c6-a33b-ba94e410b7a0" />




cat < file2
## OUTPUT
<img width="277" height="161" alt="image" src="https://github.com/user-attachments/assets/fb2ae2aa-8012-49de-81db-efd26f9e7be4" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="396" height="72" alt="image" src="https://github.com/user-attachments/assets/25047509-258e-4c28-b715-67055684b60c" />

 
comm file1 file2
 ## OUTPUT
 <img width="427" height="245" alt="image" src="https://github.com/user-attachments/assets/18f0bec7-a982-4949-acae-4d1e6fc61568" />


 
diff file1 file2
## OUTPUT
<img width="297" height="247" alt="image" src="https://github.com/user-attachments/assets/4b2c42f3-9fa4-45d8-9766-e02a62bd36cd" />



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
<img width="310" height="118" alt="image" src="https://github.com/user-attachments/assets/1730c154-56d8-4dc9-9c1c-41bd7d11eaf4" />





cut -d "|" -f 1 file22
## OUTPUT
<img width="338" height="112" alt="image" src="https://github.com/user-attachments/assets/97e59753-ab4a-4032-b037-1c48c06efc82" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="312" height="143" alt="image" src="https://github.com/user-attachments/assets/6337195a-22a8-4725-81f3-8cef0be3845d" />



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
<img width="375" height="60" alt="image" src="https://github.com/user-attachments/assets/5a8e3be1-539b-495a-ab08-19305fbc74c8" />




grep hello newfile 
## OUTPUT
<img width="302" height="71" alt="image" src="https://github.com/user-attachments/assets/437c2d37-7a18-4431-83e0-0ecc26b1ee04" />




grep -v hello newfile 
## OUTPUT
<img width="278" height="73" alt="image" src="https://github.com/user-attachments/assets/6cacd9e9-2b65-492d-85ef-7d3542eb2272" />




cat newfile | grep -i "hello"
## OUTPUT
<img width="398" height="102" alt="image" src="https://github.com/user-attachments/assets/61327729-f85d-4327-a891-bad6a87ba021" />





cat newfile | grep -i -c "hello"
## OUTPUT
<img width="383" height="90" alt="image" src="https://github.com/user-attachments/assets/8b9e1e08-1738-4983-a3c4-5e94851cb62c" />





grep -R ubuntu /etc
## OUTPUT
<img width="826" height="325" alt="image" src="https://github.com/user-attachments/assets/7a98a0cf-c7a4-4f8b-9a1f-b20039124801" />




grep -w -n world newfile   
## OUTPUT
<img width="311" height="97" alt="image" src="https://github.com/user-attachments/assets/70e53af8-4b0a-4dd1-9eff-082a18bb42d3" />



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
<img width="492" height="106" alt="image" src="https://github.com/user-attachments/assets/d4850ee6-4947-4214-a6b8-42b1f5fe89b9" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="386" height="120" alt="image" src="https://github.com/user-attachments/assets/df638c58-5557-4c7d-a44e-8ee6b0c60c62" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="427" height="137" alt="image" src="https://github.com/user-attachments/assets/14d944e8-c908-47df-914f-732a168fb61e" />





egrep '(^hello)' newfile 
## OUTPUT
<img width="362" height="116" alt="image" src="https://github.com/user-attachments/assets/1973e76e-d5d4-4134-a2aa-6e9fb5007355" />




egrep '(world$)' newfile 
## OUTPUT
<img width="337" height="112" alt="image" src="https://github.com/user-attachments/assets/6e7e7d05-568c-419b-a595-138e9b063ce2" />




egrep '(World$)' newfile 
## OUTPUT
<img width="355" height="103" alt="image" src="https://github.com/user-attachments/assets/fa62ebb3-e938-4d4b-bed8-543b8d451497" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="343" height="115" alt="image" src="https://github.com/user-attachments/assets/dd268a9a-954f-487f-a9be-eb31dd0304f5" />




egrep '[1-9]' newfile 
## OUTPUT
<img width="396" height="82" alt="image" src="https://github.com/user-attachments/assets/402e4455-270d-4cfc-b14d-07decaa1c6f4" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="372" height="80" alt="image" src="https://github.com/user-attachments/assets/b5af9366-e800-47a6-8247-acdf76bdef5b" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="388" height="100" alt="image" src="https://github.com/user-attachments/assets/6b728e84-847d-4a99-bc61-3f20d61960e5" />



egrep l{2} newfile
## OUTPUT
<img width="375" height="126" alt="image" src="https://github.com/user-attachments/assets/c858d760-df72-4823-8d5d-def57d3bc0be" />




egrep 's{1,2}' newfile
## OUTPUT 
<img width="417" height="112" alt="image" src="https://github.com/user-attachments/assets/54cd0d8a-3891-48fb-ab2a-3a8c1050a503" />



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
<img width="307" height="96" alt="image" src="https://github.com/user-attachments/assets/234ae51e-b767-40c3-98fb-f3a27a2e6f5a" />




sed -n -e '$p' file23
## OUTPUT
<img width="315" height="80" alt="image" src="https://github.com/user-attachments/assets/bf5ccf3a-a4c0-4605-9719-8ef5c0f0ee0a" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="436" height="240" alt="image" src="https://github.com/user-attachments/assets/2529cd39-fd61-4a9c-9392-251d008f4cd5" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="417" height="241" alt="image" src="https://github.com/user-attachments/assets/0fe81744-b191-4262-ac64-fdcb6889aa41" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="453" height="253" alt="image" src="https://github.com/user-attachments/assets/3979e6a1-702c-4fc8-8d48-0c4c5fdc53f6" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="442" height="178" alt="image" src="https://github.com/user-attachments/assets/3a06a269-ac8c-4038-b331-137f1c2fbe5e" />




sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="417" height="110" alt="image" src="https://github.com/user-attachments/assets/9f0ea4f2-32ae-47ad-a5b9-f5adf6071948" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="385" height="107" alt="image" src="https://github.com/user-attachments/assets/d18805e9-32d0-45a1-9ec5-343c3c045c81" />




seq 10 
## OUTPUT
<img width="426" height="295" alt="image" src="https://github.com/user-attachments/assets/5b875736-1f3b-4a30-82b6-f4b7ef820655" />




seq 10 | sed -n '4,6p'
## OUTPUT
<img width="370" height="118" alt="image" src="https://github.com/user-attachments/assets/d6ded925-af34-40ba-86bc-0149f83b963c" />




seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="380" height="121" alt="image" src="https://github.com/user-attachments/assets/725b7b97-1143-4700-bf7f-05a19bd1176a" />




seq 3 | sed '2a hello'
## OUTPUT
<img width="421" height="142" alt="image" src="https://github.com/user-attachments/assets/15c7aa57-3287-41bf-96db-e248985d71d9" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="371" height="132" alt="image" src="https://github.com/user-attachments/assets/b5d77211-6d2b-4c8c-bb37-ac0a781d5813" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="402" height="132" alt="image" src="https://github.com/user-attachments/assets/d6f1e312-61af-4b96-88bf-7d8202c2f16a" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="431" height="133" alt="image" src="https://github.com/user-attachments/assets/f8e3338e-9fa9-4de4-ad5c-f9ec2b7c8bb6" />




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
<img width="406" height="157" alt="image" src="https://github.com/user-attachments/assets/87cb5d18-b8c3-427d-be9c-8ff3ee81853e" />



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
<img width="365" height="165" alt="image" src="https://github.com/user-attachments/assets/6122aaf3-9e19-4895-a0c5-5a9d309b4a91" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="491" height="221" alt="image" src="https://github.com/user-attachments/assets/cf2ac70d-d99f-4d85-91f8-27a15ae78a2e" />


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
 <img width="428" height="142" alt="image" src="https://github.com/user-attachments/assets/0bc2e22b-f717-4bae-b800-166a37db3709" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="435" height="133" alt="image" src="https://github.com/user-attachments/assets/ee27b044-089d-440b-b198-cc82abfed15b" />




#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="367" height="278" alt="image" src="https://github.com/user-attachments/assets/ecdb2c02-b14e-4584-b5d8-63dcb167690c" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="707" height="270" alt="image" src="https://github.com/user-attachments/assets/e4134778-4a53-40f9-87ce-b4c4b7fb1e50" />



tar -xvf backup.tar
## OUTPUT
<img width="297" height="283" alt="image" src="https://github.com/user-attachments/assets/511c8a9c-7ea2-428a-82bc-39a251d56f72" />


gzip backup.tar

ls .gz
## OUTPUT
<img width="206" height="90" alt="image" src="https://github.com/user-attachments/assets/5b8b0ef0-6975-48fd-8d81-67980d7e3077" />

 
gunzip backup.tar.gz
## OUTPUT
<img width="205" height="77" alt="image" src="https://github.com/user-attachments/assets/3ec1f2d5-66d1-4f47-afac-7df0485e4333" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="492" height="151" alt="image" src="https://github.com/user-attachments/assets/984ed3b4-02a1-44e7-973f-2cee08cad1d2" />


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="348" height="123" alt="image" src="https://github.com/user-attachments/assets/fb1638d2-c43c-4fdc-8e50-b5a1d7c9e13e" />



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
<img width="611" height="471" alt="image" src="https://github.com/user-attachments/assets/b704086f-44eb-469c-a9af-56af9d96870e" />


 
ls file1
## OUTPUT
<img width="180" height="87" alt="image" src="https://github.com/user-attachments/assets/c6523a6e-5279-4060-8a09-4038becaff94" />


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
 <img width="198" height="83" alt="image" src="https://github.com/user-attachments/assets/a3ab6617-4036-4e52-af6d-beb0977d9b03" />



 
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
<img width="410" height="263" alt="image" src="https://github.com/user-attachments/assets/d1c1a778-afbf-4f2c-9d49-8297966ea866" />



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
<img width="603" height="188" alt="image" src="https://github.com/user-attachments/assets/2d87e889-d0b1-44cf-985d-4277e9934c5d" />




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
<img width="595" height="142" alt="image" src="https://github.com/user-attachments/assets/537398e9-bd96-4550-941f-e178fc0b94a9" />


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
<img width="576" height="161" alt="image" src="https://github.com/user-attachments/assets/baeae621-8092-4542-8298-77888a86fc95" />


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
<img width="658" height="118" alt="image" src="https://github.com/user-attachments/assets/e640d874-ab2c-44ee-87b3-de1d94922c56" />



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
<img width="651" height="127" alt="image" src="https://github.com/user-attachments/assets/b03e60f4-7a8a-4ce9-80e1-382d9ae9291b" />


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
## OUTPUT
<img width="417" height="107" alt="image" src="https://github.com/user-attachments/assets/8ff466c5-5ffb-4c80-8347-ab472bc59c86" />

 
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
<img width="340" height="297" alt="image" src="https://github.com/user-attachments/assets/e2888e24-070d-4527-ac03-34187fadc2cf" />

 
 
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
<img width="455" height="172" alt="image" src="https://github.com/user-attachments/assets/446b48e7-3071-4804-a43e-7e6029f7ee0c" />

 
 
 
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
## OUTPUT
<img width="300" height="202" alt="image" src="https://github.com/user-attachments/assets/e6b37138-ee4a-4a6e-9d91-436b55f9f66d" />

 
 
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
## OUPTUT
<img width="418" height="155" alt="image" src="https://github.com/user-attachments/assets/38c55ae9-035d-47cb-8ebc-adcaa891b95d" />


 
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
<img width="320" height="210" alt="image" src="https://github.com/user-attachments/assets/2e8484bd-8001-4561-a77f-8419293e53c8" />

 
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
<img width="508" height="372" alt="image" src="https://github.com/user-attachments/assets/b0145c55-b0dc-42e1-8df0-8f3fd966422e" />



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
<img width="342" height="188" alt="image" src="https://github.com/user-attachments/assets/7f685767-b4cf-4ec4-93f1-63325ecf1844" />


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
<img width="322" height="177" alt="image" src="https://github.com/user-attachments/assets/6dc8f7cd-b506-4e13-a15d-a7071b784d92" />


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
 <img width="372" height="325" alt="image" src="https://github.com/user-attachments/assets/35806b85-6167-4370-834e-efba83e81aef" />


 
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
<img width="492" height="175" alt="image" src="https://github.com/user-attachments/assets/934810f7-88c7-4446-a04a-faf50bc2f30d" />


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
<img width="502" height="203" alt="image" src="https://github.com/user-attachments/assets/8206cc82-4b33-409b-b14c-cc2b00050502" />

 
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
<img width="491" height="127" alt="image" src="https://github.com/user-attachments/assets/7e38193f-4973-40f0-911c-7df6adf41863" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="293" height="152" alt="image" src="https://github.com/user-attachments/assets/fdbb47c4-38bd-4c63-8d45-eedb1208476f" />




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
 <img width="387" height="165" alt="image" src="https://github.com/user-attachments/assets/2a7e62df-b409-4276-aed1-5077fe046c0f" />


 
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
<img width="412" height="176" alt="image" src="https://github.com/user-attachments/assets/c93a595d-1524-48c7-9e0f-8c0f03e9b014" />

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
<img width="338" height="167" alt="image" src="https://github.com/user-attachments/assets/55cb799d-5391-4f96-a650-61c075f68c12" />

 
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
 <img width="362" height="386" alt="image" src="https://github.com/user-attachments/assets/80e57031-f638-4b31-bf7a-4293b574e32b" />

 
 
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
<img width="433" height="332" alt="image" src="https://github.com/user-attachments/assets/d5b62ff1-a054-4f43-83c1-2fc65f0f9d1b" />

 
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
<img width="373" height="156" alt="image" src="https://github.com/user-attachments/assets/92aef06d-6f39-475c-aaa7-2a6f92f759e8" />



# RESULT:
The Commands are executed successfully.
