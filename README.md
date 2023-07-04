# Bash_notes

**1) Overview**
This directory opens knowledge regarding bash scripting. (on linux etc.)

**2) Commands**

List of useful commands:
```
cat /etc/shells
```
List out available bash versions (?)
```
which bash
```
Give out which is bash
```
clear
```
Delete the previous session
```
touch hello.sh
```
Create bash file named hello.sh
```
chmod u+x hello.sh
```
Allow the file to be executable

```
#this is a comment
```
That is a comment

```
read -p "Name:" name
read -sp "password: " password
echo "password:" $password
```
This command reads input into name variable, -p for same line, -sp for silent display

```
read -a names
echo "Names: $names[0] $names[1]"
```
Read an array of "names", print out names[index]

```
read
echo "Output: $REPLY"
```
$REPLY means everything put in the read command, or shall we say readline

```
echo $1 $2 $3
args = ("$@")

echo {args[1]} {args[2]} {args[3]}
echo $@
#these two work the same way

echo $#
#print out the number of input arguments
```
Print out a list of arguments from the input

**3) More complex structure**

```
count = 10
if [$count -eq 9]      #if the condition is satisfied
then                #do below statement
  echo "Condition is true"
else
  echo "Condition is false"
fi                  #finish if
```




