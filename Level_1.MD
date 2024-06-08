ssh bandit.labs.overthewire.org -p 2220 -l bandit0

---

# ls

# cat readme

Level 0 -> Level 1
Password found: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

---

username : bandit1
password: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

"-" stands for standard output , hence cannot be used directly with cat, hence use cat ./-

# ls

# cat ./-

password found :rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

---

username : bandit2
password : rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

file contains spaces in its name hence use "" with cat

# ls

# cat "spaces in this fielname"

password found: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

---

username : bandit3
passsword: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

hidden files present use ls . to show hidden files

# ls

# cd inhere

# ls .

# cat .hidden

password found : 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

---

username : bandit4
password : 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

"Human readable" things are expected to be in ASCII form. so use file command to list the file type of all fiels

# ls

# cd inhere

# for i in $(ls) ; do file ./$i ; done

password found:lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

---

username : bandit5
password :lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

# ls

# cd inhere

# for i in $(find -size 1033c ! -executable); do file ./$i ; done;

# cat ./.file02

found in maybehere07/.file02

password found: P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

---

username : bandit6
password : P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

return to home directory and then find according to gicven data

# cd ./,.

# find -user bandit6 -group bandit7 -size 33c

(only one file with access permission)

# cd ./var/lib/dpkg/info/

# cat bandit7.password

password found:z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

---

username : bandit7
password : z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

# grep "millionth" data.txt

password found:TESKZC0XvTetK0S9xNwm25STk5iWrBvP

---

username : bandit8
password : TESKZC0XvTetK0S9xNwm25STk5iWrBvP

In order to use uniq -u command we need data file in sorted manner

# sort data.txt | uniq -u

password found: EN632PlfYiZbn3PhVK3XOGSlNInNE00t

---

username : bandit9
password : EN632PlfYiZbn3PhVK3XOGSlNInNE00t

Use strings command to extract non-binary data and then use grep command to find text adjacent to "=="

# strings data.txt | grep -w "=="

password found:G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

---

username : bandit10
password :

password found:

---
