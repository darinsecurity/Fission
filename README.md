# Fission Math

<p align="center">
  <img src="FissionlogoSpectre.png" alt="Fission Logo">
</p>

---
## Fission Alpha v0
<p align="left">
  <img src="Fissionv0alphaSticker.png" alt="Code example in Fission" width="48%" height="48%">
</p>


**Fission** is a **powerful mathematical interpreter** with support for **arbitrary precision calculation** of common math functions, while having the features of many other programming languages. 

Fission is **a secure language** and does not include any direct code execution compared to Python's *eval()* and supports many mathematical functions. Features / libraries can be toggled and you can create your own programs in Fission that support full and native high precision execution. 


---

## Features

Fission supports Python-like syntax for doing operations on and defining data.
```
>> x = "hello world"
"hello world"
>> x.length()
11
```

Currently, lists, strings, and numbers are implemented, with support to be added for boolean expressions (True/False) and vectors (<>)

## Numbers

Numbers are a universal data type tnat cover both integers, floats, and complex numbers. 

You can convert any string that expresses a float or an integer (with support for complex nums coming soon) into a 'num' type.

```
>> string = "2"
"2"
>> number = 2
2
>> string = num(string)
2
>> number - string
0
```

and vice versa:
```
>> str(2)
"2"
```

You can also express numbers with "_" in the number to replace a comma (comma support is coming soon for numbers, currently conflicts with arguments)
```
>> 2_000_000
2000000
```

### Precision

Inorder to set the precision for a calculation to a given number of digits, you can use the setprec() function:
```
>> setprec(5)
Precision set to 5.0
>> pi
3.1416
>> setprec(2)
Precision set to 20.0
>> pi
3.1415926535897932385
```

You can not set the precision less than 2, and you can set the precision up to about ~ 10 million digits before time becomes a problem.
A preferable range is between 50,000 and 1 million for fast high precision calculations, although at higher precision memory usage may also be a problem.
Calculations are done with mpmath. 

```
>> setprec(1)
ValueError: Precision can not be set less than two.
>> setprec(10_000_000)
Precision set to 10000000.0
>> pi
(8.7s): 3.1415926358979323846...
```


- **Feature 1**: A brief description of this feature.
- **Feature 2**: Explanation of what this feature does and why it's essential.
- **Feature 3**: A quick note on the benefits of this feature.
- ... (continue listing other features)

---

## Installation

1. **Step 1**: Brief description of the first step.
2. **Step 2**: Details about the second step.
3. ... (continue listing other steps)

---

## Code Examples

```fission
// Sample code in Fission
print("Hello, Fission!")
