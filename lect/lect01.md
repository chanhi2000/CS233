# lect01

## TODAY'S LECTURE
- Basic Boolean expressions 
	- Booleans 
	- AND, OR and NOT 
	- Expressing Boolean functions: 
		- as __truth tables__
		- as mathematical __expressions__
		- as digital circuits made of __gates__
		- using __hardware description languages__


## COMPUTING: It's all just ones and zeros
- Computers use voltages to represent informa1on. 
- For reliability and ease of design, however, we  group ranges of voltages into two discrete, or  digital, values: 1 and 0.
	- This two-valued domain is referred to as __BINARY__.
	- Often __1__ is used for __TRUE__ and __0__ for __FALSE__. 
	![fig01a][fig01a]
- Everything in digital computers is represented with ones and zeros 


## BOOLEAN VALUES
- If we think of our digital voltages as two logical 
values, true and false, we call these “Booleans”  
	- After the mathematician George Boole
	![fig01b][fig01b]
- For simplicity, we often s1ll write digits instead:  
	- 1 is true 
	- 0 is false 
- Boolean algebra is the mathema1cs defined over this binary domain. 


## BOOLEAN FUNCTIONS
- Just like in other mathema1cs, we can define functions: 
$$
\begin{align*}
y=f(x)
\end{align*}
$$
- The output is specified purely by the function & inputs 
- Because there are a finite number (2) of boolean values...
	- There are a finite number of boolean functions
- For 1-input functions (*e.g.*, $$f(x)$$) there are only 4 possible
	- (let’s first see how to represent these...)


## TRUTH TABLES
- A __truth table__ shows all possible inputs & outputs of a function.  
- Each input variable is either 1 or 0.  (so are the outputs.) 
	- Because there are only a finite number of values (1 and 0), truth tables themselves are finite. 
	- A function with n variables has 2n possible combinations of inputs.

| x | y | z | f(x,y,z) |
| - | - | - | :------: |
| 0 | 0 | 0 | 1 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 1 |

## 1-INPUT BOOLEAN FUNCTIONS
$$
\begin{align*}
y=f(x)
\end{align*}
$$
- A 1-input Boolean function has $$2^{1}=2$$ possible inputs:

| x | f(x) |
| - | :--: |
| 0 | f(0) |
| 1 | f(1) |

- There are $$2^{\text{# of inputs}}$$ possible functions
	- For each input, there are 2 possible outputs 
	- The outputs are independent for each input (hence the multiplication) 
- The 4 possible 1-input Boolean functions.


## 2-INPUT BOOLEAN FUCNTIONS
$$
\begin{align*}
y=f(x,y)
\end{align*}
$$
- 4 possible inputs, 16 possible functions:

| $$(x,y)$$ | f0 | f1 | f2 | f3 | f4 | f5 | f6 | f7 | f8 | f9 | f10 | f11 | f12 | f13 | f14 | f15 |
| :-------: | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | :-: | :-: | :-: | :-: | :-: | :-: |
| $$(0,0)$$ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| $$(0,1)$$ | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 |
| $$(1,0)$$ | 0 | 0 | 1 | 1 | 0 | 0 | 1 | 1 | 0 | 0 | 1 | 1 | 0 | 0 | 1 | 1 |
| $$(1,1)$$ | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 |

- We'll focus on 2 for now.


## BASIC BOOLEAN OPERATIONS
- There are three basic opera1ons for logical values.
	 - __AND__: (product of 2 inputs)
	 	- notation:
	 	$$
	 	\begin{matrix}
	 	xy&&\text{or}x\cdot{y}
	 	\end{matrix}
	 	$$
	 	- truth table:
	 - __OR__:	(sum of 2 inputs)
		- notation:
		$$
		x+y
		$$
		- truth table:
	 - __NOT__: (complement on one input)
	 	- notation:
	 	$$
	 	\begin{matrix}
	 	x^{\prime}&&\text{or}&&\bar{x}
	 	\end{matrix}
	 	$$
	 	- truth table:
## BOOLEAN EXPERSSIONS (formally)
- Use these basic opera1ons to form more complex expressions: 
$$
\begin{align*}
f(x,y,z)&=(x+y^{\prime})z+x^{\prime}
\end{align*}
$$
- Some terminology and nota1on: 
	- .$$f$$ is the name of the function. 
	- .$$(x,y,z)$$ are the __input variables__1-, each representing 1 or 0. Listing  the inputs is op+onal, but some+mes helpful.
	- A literal is any occurrence of an input variable or complement. The function above has four literals: 
	$$
	\begin{matrix}
	x,&&y^{\prime},&&z,&&x^{\prime}
	\end{matrix}
	$$
- Precedences are important, but not too difficult. 
	- NOT has the highest precedence, followed by AND, and then OR. 
	- Fully parenthesized, the function above would be kind of messy:
	$$
	\begin{align*}
	f(x,y,z)&= \left(\left(\left(x+\left(y^{\prime}\right)\right)z\right)+x^{\prime}\right)
	\end{align*}
	$$


## BOOLEAN EXPRESSIONS TO TRUTH TABLES
- To compute a truth table given a Boolean expression: 
	- Evaluate the func+on for every combination of inputs.
	$$
	\begin{align*}
	f(x,y,z)&=\left(x+y^{\prime}\right)z+x^{\prime}\\
	f(0,0,0)&=\left(0+1\right)0+1\\
	&=1\\
	&\vdots\\
	f(1,0,1)&=\left(1+1\right)1+0\\
	&=1\\
	&\vdots
	\end{align*}
	$$

| x | y | z | f(x,y,z) |
| - | - | - | :------: |
| 0 | 0 | 0 | 1 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 1 |


## PRIMITIVE LOGIC GATES
- Each of our basic opera1ons can be implemented in hardware using a 
__primi1ve logic gate__.
	- Symbols for each of the logic gates are shown below. 
	- These gates output the product, sum or complement of their inputs. 

| operation | expression | logic gate |
| :-------: | :--------: | :--------: |
| AND | $$xy$$ | ![fig02a][fig02a] |
| OR | $$x+y$$ | ![fig02b][fig02b] |
| NOT | $$x^{\prime}$$ | ![fig02c][fig02c] |


## BOOLEAN EXPRESSIONS TO CIRCUITS
- *Any* Boolean expression can be converted into a __circuit__ in a  straighorward way.
	- Write a gate for each opera+on in the expression in precedence order.
	- We typically draw circuits with inputs on leP and outputs on right. 


## CONVERTING CIRCUITS TO EXPRESSION
- What Boolean expression does this circuit implement?
![fig03a][fig03a]

__a)__ $$\left(x+y\right)y^{\prime}$$

__b)__ $$x+y+y^{\prime}$$

__c)__ $$xy^{\prime}+y$$

__d)__ $$\left(xy\right)+y^{\prime}$$

__e)__ $$\left(x+y\right)+\left(x+y^{\prime}\right)$$


## HARDWARE DESCRIPTION LANGAUGE
- Textual descriptions of circuits 
	- (We’re very good at manipula+ng text...) 
	
	| A circuit | Verilog HDL Code |
	| :-------: | :--------------: |
	| ![fig03b][fig03b]| ? |

- Not like a normal programming language 
	- Each statement describes one or more gates and/or wires. 


## BOOLEAN FUNCTIONS SUMMARY 
-  We can interpret high and low voltages as true and false.  
-  A Boolean variable can be either 1 or 0. 
-  AND, OR, and NOT are the basic Boolean opera1ons. 
-  We can express Boolean functions in many ways: 
	- Expressions, truth tables, circuits, and HDL code 
	- These are different representations for equivalent things

[fig01a]: lect01/lect01-fig01a.png
[fig01b]: lect01/lect01-fig01b.png
[fig02a]: lect01/lect01-fig02a.png
[fig02b]: lect01/lect01-fig02b.png
[fig02c]: lect01/lect01-fig02c.png
[fig03a]: lect01/lect01-fig03a.png
[fig03b]: lect01/lect01-fig03b.png