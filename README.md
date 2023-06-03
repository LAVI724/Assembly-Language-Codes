## LAVI's Assembly Language Codes
###### tags: `Course` `Assembly` `LAVI` `2021` 

## Information
- 大二上學期組合語言作業與小考測驗程式

### Details
#### Hw0x1 Find all prime numbers less than an integer N
- Input：an integer N read by scanf() in asmMain() procedure
- Output：all prime numbers less than N using printf().
- Requirement：
	1. Write a C/C++ main() function and it calls the asmMain procedure written in x86 assembly code.
	2. Write  asmMain procedure  (x86 assembly asmMain procedure)
	3. Write a C/C++ function  AllPrimeNumbers(int N) returning the number of prime numbers less than N.
    	- In the function AllPrimeNumbers(), print out all prime numbers less than N.
        - AllPrimeNumbers() must be called in asmMain procedure.       
    4. In the  asmMain procedure, you have to input an integer N and call AllPrimeNumbers(N) which returns the number Cnt of prime numbers less than N. Print out Cnt.
    5.  Use scanf() and printf() for input and output in the asmMain assembly procedure.

#### Hw0x2 Find the Minimum and Maximum Numbers
- Input：Input an integer N followed by N signed  numbers.  N < 200;
- Output：Output the minimum and maximum numbers among N input numbers
- Requirement:
    1. Write an assembly main Procedure.  (You can't use main() written in C/C++.)
     	- Store the input integers into a SDWORD array.
    2. Write two assembly procedures to find the minimum value and maximum value, respectively. You have to pass two parameters denoting the address of the array and the array size. Note that you have to use registers to pass the parameters. No points will be given if you violate this requirement.
    3. You must use irvine32.lib in your program.  (ReadXXX and WriteXXX in Sec. 5.4 of textbook)
        - Note that you can not use scanf(). printf()  and any C functions in your program.
    4. Declare two global signed integers Min and Max to store the minimum and maximum numbers, respectively.
- Important Hint:
    - For signed numbers' comparison, please use jump conditionally statements (Greater and Less than, G and L) shown in Table 6-5
#### Hw0x3 Prime Factorization
- Problem
	- 輸入數字 N (資料型態為 signed number), N < 2^31， 請輸出該數字的所有質因數及其次方。例如 N = 360 = 2^3 \* 3^2 \*5 。此題數字可能會有質數出現。
- Requirement
	- 寫一個副程式可傳入一參數為正數N並處理資因數分解並輸出，無此副程式扣20分。
	- 不可呼叫 scanf() 與 printf()。
- Input
	- 輸入有多列，每列有個整數 N，if N < 0, exit the program。請使用 ReadInt procedure in irvine32.lib，必須使用 ReadInt。
- Output
	- 針對每一組測資數字 N，輸出N的質因數分解，將數字N的所有質因數（及其次方）以小到大方式顯示出來，如質因數之次方數大於 1，以^運算符號顯示，不同質因數間以 * 運算符號互相連接， * 運算符號前後加空格。 請使用 WriteXXX procedures in irvine32.lib, 必須使用 WriteXXX。

#### Hw0x4 GCD (Greatest Common Divisor) and LCM (Least Common Multiple)
- Input：There are many lines of input.  Each line has two integers M and N. Repeat reading pairs of integers until a negative number is read.
- Output：r each pair of positive numbers (M and N), print out GCD(M, N) and LCM(M, N).
- Requirement：
	1. Practice multi-module programming.  main() procedure in main.asm, gcd() procedure in gcd.asm, gcd() prototype in gcd.inc. Minus 40 points if you don't do it. 
	2. All codes are written in x86 assembly language.  Minus 40 points if you don't do it. 
	3. Write a recursive procedure GCD with two input parameters M and N and it returns the GCD of M and N.  Minus 20 points if you don't do it.
	4.  Reserve a local variable Rem (DWORD) in the stack frame. Minus 20 points if you don't do it.
	5. Use ReadInt and WriteDec procedures in irvine32.lib to read and write  integers.

#### Hw0x5 Implementation of Sorting Algorithms
- Problem：mplement a sorting algorithm to sort a set of integers in ascending order.
- Input: 
    - For each test case, input a positive integer N followed by N integer, where 0<= N <= 1000.  If N = 0, exit the program.
- Output:
    - For each test case, print out the float values in ascending order. All float values are separated by a space character. Print also the middle numbers in the list of float  values.  Test cases are separated by a newline.
- Requirement:
    1. 學號最後一碼(檢查碼) % 2 = 0, please write a sorting procedure using   insertion sort algorithm.
    2. 學號最後一碼(檢查碼) % % 2 = 1, please write a sorting procedure using  selection sort algorithm.  
    3. Write a sorting procedure with two input parameters.
    	- The first parameter is the starting (base) address of an integer array.
    	- The second parameter is the number of double values  in the array, i.e., N.
    	- You have to use use stack to pass the parameters.
    4. Use multiple module program. That is, main procedure is in one .asm file and sort procedure in another .asm file.  There is one header .inc file for the prototyping of sort procedure. Your project has two .asm files and one .inc file. Please reference Sec. 8.5 in textbook.
    5. Please also write an array input  procedure in a separate .asm file.
   		- Please also write an array printing procedure in an .asm file.
    6. You can  use scanf() for the input but you can not use printf() for the output in your assembly program. 
    7. If N is odd, print one middle number, otherwise, print two middle numbers.
    8. All source code is written in x86 assembly.