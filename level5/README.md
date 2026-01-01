
in bandit 5 
ACCORIDNT TO THE dOC
the file is stored in the ./inhere DIR
 and it has properties human-readable
1033 bytes in size
not executable




--------

I have found out that the folders here are indentcal and the key will bein one of these but 
I need to find an effiecient way to go throught hem without doing it stp by step .

first let me try my luck since the other room the key was inthe 07 room lucky 7 i will go to the dortwitht the 7 
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
bandit5@bandit:~/inhere$ ^C
bandit5@bandit:~/inhere$ ^C
bandit5@bandit:~/inhere$ ^C
bandit5@bandit:~/inhere$ ^C
bandit5@bandit:~/inhere$ 




'----------------
soo i will have to loop through all folder baed on their identical names
loop through them and find the files with the human redable format usinghtis script below 



 ""
 cd ~/inhere
for d in maybehere*; do
  for f in "$d"/*; do
    file "$f" | grep -i 'text'
  done
done
"""" 

after running the loop i found out that not one but most of the file sin the folders are in human readable format "" 
 bandit5@bandit:~/inhere$ cd ~/inhere
for d in maybehere*; do
  for f in "$d"/*; do
    file "$f" | grep -i 'text'
  done
done
maybehere00/-file1: ASCII text, with very long lines (1038)
maybehere00/-file2: ASCII text, with very long lines (9387)
maybehere00/spaces file1: ASCII text, with very long lines (6117)
maybehere00/spaces file2: ASCII text, with very long lines (6849)
maybehere01/-file1: ASCII text, with very long lines (6027)
maybehere01/-file2: ASCII text
maybehere01/spaces file1: ASCII text, with very long lines (4138)
maybehere01/spaces file2: ASCII text, with very long lines (4542)
maybehere02/-file1: ASCII text, with very long lines (3800)
maybehere02/spaces file1: ASCII text, with very long lines (6745)
maybehere02/spaces file2: ASCII text, with very long lines (8487)
maybehere03/-file1: ASCII text, with very long lines (314)
maybehere03/-file2: ASCII text, with very long lines (6594)
maybehere03/spaces file1: ASCII text, with very long lines (2189)
maybehere03/spaces file2: ASCII text, with very long lines (3384)
maybehere04/-file1: ASCII text, with very long lines (4409)
maybehere04/-file2: ASCII text, with very long lines (2618)
maybehere04/spaces file1: ASCII text, with very long lines (5531)
maybehere04/spaces file2: ASCII text, with very long lines (2490)
maybehere05/-file1: ASCII text, with very long lines (2345)
maybehere05/-file2: ASCII text, with very long lines (5958)
maybehere05/spaces file1: ASCII text, with very long lines (879)
maybehere05/spaces file2: ASCII text, with very long lines (2419)
maybehere06/-file1: ASCII text, with very long lines (5730)
maybehere06/-file2: ASCII text, with very long lines (1075)
maybehere06/spaces file1: ASCII text, with very long lines (4072)
maybehere06/spaces file2: ASCII text, with very long lines (4250)
maybehere07/-file1: ASCII text, with very long lines (3662)
maybehere07/-file2: ASCII text, with very long lines (2487)
maybehere07/spaces file1: ASCII text, with very long lines (4129)
maybehere07/spaces file2: ASCII text, with very long lines (9063)
maybehere08/-file1: ASCII text, with very long lines (1076)
maybehere08/-file2: ASCII text, with very long lines (3824)
maybehere08/spaces file1: ASCII text
maybehere08/spaces file2: ASCII text, with very long lines (3692)
maybehere09/-file1: ASCII text, with very long lines (3627)
maybehere09/-file2: ASCII text, with very long lines (773)
maybehere09/spaces file1: ASCII text, with very long lines (5300)
maybehere09/spaces file2: ASCII text, with very long lines (8715)
maybehere10/-file1: ASCII text, with very long lines (1051)
maybehere10/-file2: ASCII text, with very long lines (1990)
maybehere10/spaces file1: ASCII text, with very long lines (8268)
maybehere10/spaces file2: ASCII text, with very long lines (3569)
maybehere11/-file1: ASCII text, with very long lines (1210)
maybehere11/-file2: ASCII text, with very long lines (4558)
maybehere11/spaces file1: ASCII text, with very long lines (3146)
maybehere11/spaces file2: ASCII text, with very long lines (502)
maybehere12/-file1: ASCII text, with very long lines (9677)
maybehere12/-file2: ASCII text
maybehere12/spaces file1: ASCII text, with very long lines (2156)
maybehere12/spaces file2: ASCII text, with very long lines (2459)
maybehere13/-file1: ASCII text, with very long lines (1358)
maybehere13/-file2: ASCII text, with very long lines (1422)
maybehere13/spaces file1: ASCII text, with very long lines (3951)
maybehere13/spaces file2: ASCII text, with very long lines (951)
maybehere14/-file1: ASCII text, with very long lines (4281)
maybehere14/-file2: ASCII text, with very long lines (8350)
maybehere14/spaces file1: ASCII text, with very long lines (1381)
maybehere14/spaces file2: ASCII text, with very long lines (870)
maybehere15/-file1: ASCII text, with very long lines (8793)
maybehere15/-file2: ASCII text, with very long lines (9498)
maybehere15/spaces file1: ASCII text, with very long lines (1622)
maybehere15/spaces file2: ASCII text
maybehere16/-file1: ASCII text, with very long lines (4276)
maybehere16/-file2: ASCII text, with very long lines (5300)
maybehere16/spaces file1: ASCII text, with very long lines (9772)
maybehere16/spaces file2: ASCII text, with very long lines (3145)
maybehere17/-file1: ASCII text, with very long lines (1132)
maybehere17/-file2: ASCII text, with very long lines (1790)
maybehere17/spaces file1: ASCII text, with very long lines (8360)
maybehere17/spaces file2: ASCII text, with very long lines (3386)
maybehere18/-file1: ASCII text, with very long lines (9696)
maybehere18/-file2: ASCII text
maybehere18/spaces file1: ASCII text, with very long lines (7333)
maybehere18/spaces file2: ASCII text, with very long lines (6347)
maybehere19/-file1: ASCII text, with very long lines (6301)
maybehere19/-file2: ASCII text, with very long lines (5593)
maybehere19/spaces file1: ASCII text, with very long lines (7185)
maybehere19/spaces file2: ASCII text, with very long lines (8784)
bandit5@bandit:~/inhere$ 
:""' 


---I have now realised htat the key is small fils witht hthe smaller disk size is where the kkey is  
