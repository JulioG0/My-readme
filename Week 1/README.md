 # Introduction to programming & Javascript  - week 1
<link> [Week chanllengues (tuesday)]
# week goal 🏁
<div style="text-aling: justify"> For the firt week we are focusing on understandting the programming foundations, how programs work and are read by a computer, typer of programming languages and different areas that you can work on. 
</div>  

---

## week challengues (Tuesday)

## 1. Search and aswerd the question: Java  language is copiled or interpreted?
java is considered both since  it is firt compiled into binary code and then the code runs in the java VM which is usually software-based.

### 2. create an algorithm to calculate the equivalent of your local currency to USD
 1. START
  2. amount <-- GET
  3. USD <-- GET 23,130.80
  4. Resultado <-- Amount * BTC
  5. PRINT Resultado
  9. END
---

## week challenges (Wednesday)
## 1. exercise
 ## 1.1. solution

- Your date of birth in the matrix?
- Date of birth = 2004 

- 2<sup>0</sup> = 1
- 2<sup>1</sup> = 2
- 2<sup>2</sup> = 4
- 2<sup>3</sup> = 8
- 2<sup>4</sup> = 16
- 2<sup>5</sup> = 32
- 2<sup>6</sup> = 64
- 2<sup>7</sup> = 128
- 2<sup>8</sup> = 256
- 2<sup>9</sup> = 512
- 2<sup>10</sup> = 1024
- 2<sup>11</sup> = 2048

| 2^10 | 2^9 | 2^8 | 2^7 | 2^6 | 2^5 | 2^4 | 2^3 | 2^2 | 2^1 | 2^0  |
| ---- | --- | --- | --- | --- | --- | --- | --- | --- | --- | ---  |
| 1    | 1   | 1   | 1   | 1   | 0   | 1   | 0   | 1   | 0   |   0  |
---

## 2. exercise

1. Create a program that adds any two given numbers provided by the user
2. Create a program that displays your name

- 2 solution 
```assembly
  .data
        message: .asciiz "\Julio, Gutierrez!\"
  .text
        main:
              li $v0, 4
              la $a0, message
              syscall
```

```assembly
  .data
	      number1: .asciiz "\nIngrese el primer numero: "
	      number2: .asciiz "\nIngrese el segundo numero: "
	      result_message: .asciiz "\nEl resultado es: "
  .text
	      main:
              li $v0, 4
              la $a0, number1
              syscall
              li $v0, 5
              syscall
              move $t1, $v0
              li $v0, 4
              la $a0, number2
              syscall
              li $v0, 5
              syscall
              move $t2, $v0
              li $v0, 1
              move $a0, $t0
              syscall
              li $t0, 10
              li $t1, 10
              add $t2, $t0, $t1
              li $v0, 4
              la $a0 result_message
              syscall
              li $v0, 1
              move $a0, $t2
              syscall
              
```
              

## Week challenges (Thursday) 

1. ### Print special numbers

<br>

- Description

- In this exercise you must use an iterative flow control to be able to print all the even numbers in the range of numbers from 0 to 100. Remember that you should not print each number, you should use a flow control structure to perform the exercise.

<br>

>*Exercise with FOR*
```JavaScript
let str = '';
for (let i = 0; i <= 100; i++) {
  str = str + i;
}
console.log(str);
```

>*Exercuse with WHILE*
```JavaScript
var i = 0;
while (i <= 100) {
  if (i % 2 == 0) console.log(i);
  i++;
}
```
>*Excercise with do...while*
```JavaScript
let result = '';
let i = 0;
do {
  i = i + 1;
  result = result + i;
} while (i < 100);
console.log(result);
```
<br>

2. ### Bad code

<br>

- Description

- The code shown below is not working in the right way, as a task you must find the error made by the developer who programmed this code and correct it, for this exercise you must explain what the error is and place the correct code.

```JavaScript
var cond = false;
if ((cond)) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
VM156:6 The cond variable is false
```

<br>

3. ### Bad code 2

<br>

- bDescription

- You must create the code that follows the following logic, if the given number is 100, take this number as special and show the following message: "This is a special number!", but if the number is less than 1000, multiple of 10 and different from 100, you must show the following message: "This number is almost special". if none of the given conditions are met show the following message: "Just a regular number". Another developer was trying to program the logic, but apparently couldn't, you need to fix the code to work properly.

```JavaScript
var n = 100;
if (n == 100) {
  console.log('This is a special number!');
} else if (n < 1000 && n % 10 == 0) {
  console.log('This number is almost special');
} else {
  console.log('Just a regular number');
}
```