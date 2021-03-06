## A Programming Language for Logic Circuits

---

### **About**
---
Logically is a scripting language that can derive the combinational logic circuit of any logic expression. Given a set of logic operations, the language is capable of analyzing the resulting function and with a series of computations, a logical circuit will be derived.

### **Introduction**
---
Boolean logic is a branch from algebra in which variables are evaluated with truth tables where said variables have a value of “1” or “0” and certain outcome based on the expression. The operations used for evaluating the logic are OR, AND & NOT. These operations are represented by disjunction(U), conjunction(∩), and negation(-), respectively. With these expressions, it is possible to express and evaluate Boolean Algebra. The following logic can then be used to construct circuits called combinational logic circuits (often referred as logical gates or logic circuits). 

These combinational logic circuits can range from very simple ones to very complicated ones. And so, developers use different techniques to specify the function of these combinational logic circuits like Boolean Algebra, Truth Tables and Logic Diagrams. Common combinational circuits made up that carry out a desired application include: Multiplexers, Encoders, Decoders, Half Adders, Full Adders, etc. Logically looks to simplify the process of designing logic circuits and to provide all the necessary tools used when dealing with logical expresions. Instead of spending a lot of time writing tables and karnaugh maps, users can obtain the same results by typing some simple commands.

### **Language Features**
---
* Design logical circuits by implementing individual logic gates.
* Create complex logical expressions from logic circuits.
* Test circuits by generating truth tables.
* Simplify any logical expression with a single command.
* Generate visual circuit diagrams from generated circuits.
* Display the venn diagram of a given logical expression.

### **How It Works**
---
The following is a video tutorial on how to install and use Logically.
<div align="center">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/V1A-Ig0A0zM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div>

### **Program Examples**
---
##### Example 1: Expression Build, Table Generation and Circuit Drawing
```
>>out = OR a b
Added Expression to:  out
>>a = AND c d 
Added Expression to:  out
>>c = NOT e
Added Expression to:  out
>>b = AND f e
Added Expression to:  out
>>f = NOT d
Added Expression to:  out
>>TABLE out
Generating truth table:

( ( not e ) and d ) or ( e and ( not d ) )
d	e	out
0	0	0
0	1	1
1	0	1
1	1	0
>>CKT out
Generating circuit diagram
```

<p align="center">
  <img src="https://raw.githubusercontent.com/javierramirezzayas/Logically/master/image_examples/logicallyCKT.png" alt="logicallyCKT" height="400" width="400"/></p>
<p align="center">Figure 1: Output from Example 1.</p>

##### **Example 2: Testing the Simplify**
```
>>out = AND x y z
Added Expression to:  out
>>x = AND b c
Added Expression to:  out
>>y = AND c d
Added Expression to:  out
>>z = OR c d
Added Expression to:  out
>>SIMPLIFY out
Simplifying out
( b and c ) and ( c and d ) and ( c or d )
['b', 'c', 'd']
[0, 0, 0, 0, 0, 0, 0, 1]
Result: 
 bcd
```

##### **Example 3: Testing Venn Diagrams**
```
>>exp = OR a x
Added Expression to:  exp
>>x = AND a b
Added Expression to:  exp
>>VENN exp
Generating venn diagram
a or ( a and b )
```

<p align="center">
  <img src="https://raw.githubusercontent.com/javierramirezzayas/Logically/master/image_examples/logicallyVENN.png" alt="logicallyCKT" height="400" width="400"/></p>
<p align="center">Figure 2: Output from Example 3.</p>


### **Installation**
---
##### Dependencies
* Python 3.4 with the following packages:
  * SchemDraw
  * Matplotlib
  * TKinter
  * PLY 
  
##### Instructions
* Download the program to your machine. You can download the code from <a href="https://github.com/javierramirezzayas/Logically/zipball/master"> here </a>
* After downloading the code open a terminal and change to the ```Logically``` directory.
* Change to the ```logically_exe``` directory and run ```python logically.py```.
* Enjoy logically
 
 
### **Developers**
---
The developers of logically are a group of students of the University of Puerto Rico at Mayagüez. The team members are: <a href="https://github.com/JeanOC19"> Jean O. Candelaria</a>, <a href="https://github.com/Gustavohernandez1"> Gustavo A. Hernandez</a>, <a href="https://github.com/YorkiSerrano"> Yorki G. Serrano</a> and <a href="https://github.com/javierramirezzayas"> Javier Ramirez</a>. This project was developed as part of the Programming Language course (ICOM4036) directed by Dr. Wilson Rivera.

Final report for the class project can be found at the link in the top of the website or <a href="https://raw.githubusercontent.com/javierramirezzayas/Logically/master/Documents/Final%20Report%20-%20Logically.pdf"> here </a>.
  
