# wordlist generator
```
crunch -h
```
The following example creates a wordlist containing all possible combinations of 2 characters, including 0-4 and a-d. We can use the -o argument and specify a file to save the output to. 

```
crunch 2 2 01234abcd -o crunch.txt
```
For example, if part of the password is known to us, and we know it starts with pass and follows two numbers, we can use the % symbol from above to match the numbers. Here we generate a wordlist that contains pass followed by 2 numbers:
```
crunch 6 6 -t pass%%
```

```
crunch 8 8 0123456789abcdefABCDEF -o crunch.txt
```
Automatic interactive trool written in Python for creating custom wordlists.
```
git clone https://github.com/Mebus/cupp.git
```
# Offline Dictionary Atack

```
hashcat -a 0 -m 0 f806fc5a2a0d5ba2471600758452799c /usr/share/wordlists/rockyou.txt
```
Crack md5 hash
```
echo "e48e13207341b6bffb7fb1622282247b" > hash2.txt 

 hashcat -a 3 hash2.txt ?d?d?d?d
```
# Rule-Based Attack
Shows john the ripper rules.
```
cat /etc/john/john.conf|grep "List.Rules:" | cut -d"." -f3 | cut -d":" -f2 | cut -d"]" -f1 | awk NF
```
Creates a wordlist with John the Ripper

```
john --wordlist=/tmp/single-password-list.txt --rules=best64 --stdout | wc -l
```
Custom Rules
```
sudo vi /etc/john/john.conf

echo "password" > /tmp/single.lst

john --wordlist=/tmp/single.lst --rules=THM-Password-Attacks --stdout
```
