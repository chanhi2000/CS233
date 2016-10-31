# lect01

## TODAY'S LECTURE
- Basic Boolean expressions 
	- Booleans 
	- AND, OR and NOT 
	- Expressing Boolean func+ons: 
		- as __truth tables__
		- as mathema+cal __expressions__
		- as digital circuits made of __gates__
		- using __hardware descrip1on languages__


## COMPUTING: It's all just ones and zeros
- Computers use voltages to represent informa1on. 
- For reliability and ease of design, however, we  group ranges of voltages into two discrete, or  digital, values: 1 and 0.
	- This two-valued domain is referred to as __BINARY__.
	- Often __1__ is used for __TRUE__ and __0__ for __FALSE__. 
- Everything in digital computers is represented with ones and zeros 


## BOOLEAN VALUES
- If we think of our digital voltages as two logical 
values, true and false, we call these “Booleans”  
	- After the mathema+cian George Boole 
- For simplicity, we oZen s1ll write digits instead:  
	- 1 is true 
	- 0 is false 
- Boolean algebra is the mathema1cs defined over this binary domain. 


## BOOLEAN FUNCTIONS
- Just like in other mathema1cs, we can define func1ons: 
$$
\begin{align*}
y=f(x)
\end{align*}
$$
- The output is specified purely by the func1on & inputs 
- Because there are a finite number (2) of boolean values...
	- There are a finite number of boolean func1ons
- For 1ainput func1ons (*e.g.*, $$f(x)$$) there are only 4 possible
	- (let’s first see how to represent these...)


## TRUTH TABLES
- A __truth table__ shows all possible inputs & outputs of a func1on.  
- Each input variable is either 1 or 0.  (so are the outputs.) 
	- Because there are only a finite number of values (1 and 0), truth tables themselves are finite. 
	- A func+on with n variables has 2n possible combinations of inputs.

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
- A 1-input Boolean func1on has $$2^{1}=2$$ possible inputs:

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
	 	- truth table:
	 - __OR__:	(sum of 2 inputs)
		- notation:
		- truth table:
	 - __NOT__: (complement on one input)
	 	- notation:
	 	- truth table:

## BOOLEAN EXPERSSIONS (formally)
- Use these basic opera1ons to form more complex expressions: 
$$
\begin{align*}
f(x,y,z)&=(x+y\prime)z+x\prime
\end{align*}
$$
- Some terminology and nota1on: 
	- .$$f$$ is the name of the func+on. 
	- .$$(x,y,z)$$ are the __input variables__, each represen+ng 1 or 0. Listing  the inputs is op+onal, but some+mes helpful.
	- A literal is any occurrence of an input variable or complement. The function above has four literals: $$x$$, $$y\prime$$, $$z$$, and $$x\prime$$.
- Precedences are important, but not too difficult. 
	- NOT has the highest precedence, followed by AND, and then OR. 
	- Fully parenthesized, the func+on above would be kind of messy:
	$$
	\begin{align*}
	f(x,y,z)&= \left(\left(\left(x+\left(y\prime\right)\right)z\right)+x\prime\right)
	\end{align*}
	$$


## BOOLEAN EXPRESSIONS TO TRUTH TABLES





