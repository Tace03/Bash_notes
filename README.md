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

```
cat > file
(Input something)
```
Put some data into file

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
Basic structure of if else

**4) Flags/Operators**
```
#comparison flags
## Integer
-eq : is equal to
-ne : not equal to
-gt : is greater than
-ge : is greather than or equal to
-lt : is less then
-le : is less than or equal to

## String
=   : is equal to
==  : is equal to
!=  : is not equal to
<   : less than in ASCII
>   : more than in ASCII
-x  : string is null
```
List of Comparison flags
```
echo -e "Enter the name of file: \c" #
# \c means to keep cursor on same line, -e allows the action to be done
# no -e means no \c applied

if [ -f $filename ]                   # if the file exists : -f
then
  echo "$filename found"
else
  echo "$filename not found"
fi

if [ -d $dirname]                     # if the directory exists: -d
if [ -s $filename]                    # if the file empty or not: -s
if [ -r $filename]                    # if the file has read permission: -r
if [ -w $filename]                    # if the file has write permission: -w
if [ -x $filename]                    # if the file has exe permission: -x 
```
File operators flags

```
echo -e "Enter filename: \c"
read filename

if [ -f $filename ]
then
  if [ -w $filename]
  then
      echo "Type some data, ctrl + d to escape"
      cat >> $file_name
  else
      echo "The file does not allow write permission."
  fi
else
  echo "File not existed."
fi 
```
Append output to txt files









