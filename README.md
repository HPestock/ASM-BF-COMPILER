# ASM-BF-COMPILER

ASM-BF is a program designed to read input from an interface found in an html file, and convert it to a program able to be run in the BrainF*** programming language. <br>
The following is a list of currently supported instructions; 

Currently supported instructions: <br>
copy a b d<br>
  adds to location b's value with the value found at location a, <br>
  location d used as placeholder<br>
mvp l<br>
  moves the system pointer from its current position to location l. <br>
  requires pointer currently > 0<br>
ifnz l<br>
  open if statement. if condition: location l's cell not equal to zero met, <br>
  runs instructions between endif type statement. <br>
ifnzp<br>
  open if statement. if condition: cell pointed to not equal to zero met, <br>
  runs instructions between endif type statement. <br>
endif<br>
  closes an if statement. <br>
endifl<br>
  ends an if statement at cell 0. change pointer before initializing another<br>
  statement. <br>
endifr<br>
  ends an if statement at the allocated memory boundary. use not advisable in<br>
  regular use. <br>
add l a<br>
  adds a to the value at location l. <br>
subt l a<br>
  subtracts a from the value at location l. <br>
addp a<br>
  adds a to the current pointer location. <br>
subtp a<br>
  subtracts a from the current pointer location. <br>
outp<br>
  outputs character at current pointer location. <br>
inp<br>
  gets input, stores input at current pointer location. <br>
out l<br>
  outputs character at location l. <br>
in l<br>
  gets input, stores input at location l. <br>
setp n<br>
  sets cell at current pointer location to value n. <br>
setpn n<br>
  sets cell at current pointer location to the value of negative n. <br>
set l n<br>
  sets cell at location l to value n. <br>
setn l n<br>
  sets cell at location l to the value of negative n. <br>
setup m<br>
  (where m is the 0u pointer of the furthest cell from 0), initializes a program. (m = tape length - 1)<br>
ifz l d c<br>
  open if statement. if condition: location l's cell equal to zero met, <br>
  runs instructions between endif type statement. <br>
writep s<br>
  outputs string s, uses current pointed cell as placeholder. <br>
write l s<br>
  outputs string s, uses location l cell as placeholder. <br>
cut a b<br>
  adds the value from cell a to cell b, sets cell a value to zero. <br>
sn1zp d<br>
  if the current cell pointed to is equal to -1, sets to zero. <br>
  suggested use for subt comparison. <br>
