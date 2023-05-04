Download Link: https://assignmentchef.com/product/solved-csce-121-lab-2-practice-writing-functions
<br>
The aim of this lab work is to practice writing functions. They are an essential concept as they allow us to first make building blocks, then use our own building blocks to construct grander things, these themselves becoming building blocks in their own right for even larger things.

How far must I get?

This lab is assigned for the entire week. You should complete the questions that you’re not able to finish in the lab session on your own. If you are finding it tough to keep up the pace, it may be wise to look over the questions and make a first attempt before arriving at your lab session. That way you can use the time most effectively in getting help with the questions that are sticking points for you.

Warm in here?

Write a function that converts temperatures from degrees Fahrenheit to Celsius. Write a second function that converts temperatures from degrees Celsius to Fahrenheit. Now write a function that prompts the user for a temperature and its units, then converts it into the other units.

Here’s a sample of five runs, showing the desired behavior:

:: ./temps Please enter a temperature: 103Is that in Fahrenheit or Celsius? [F/C] FWell, 103F is 39.4444C. :: ./temps Please enter a temperature: 11.1Is that in Fahrenheit or Celsius? [F/C] FWell, 11.1F is -11.6111C. :: ./temps Please enter a temperature: 10Is that in Fahrenheit or Celsius? [F/C] CWell, 10C is 50F. :: ./temps Please enter a temperature: 45Is that in Fahrenheit or Celsius? [F/C] fWell, 45F is 7.22222C. :: ./temps Please enter a temperature: 7.2Is that in Fahrenheit or Celsius? [F/C] cWell, 7.2C is 44.96F.

Use <a href="https://en.wikipedia.org/wiki/Function_composition">mathematical function composition</a> to test both the functions by checking that together they form the identity function.

<h3>Basic Sums</h3>

Write a function SumOfNums that calculates and returns the sum of the numbers from 1 to n (where n is a positive integer parameter). The statement

cout &lt;&lt; SumOfNums(100);

should cause “5050” to be printed since 1+2+⋯+100 = 5050.

<h3>Summing Digits</h3>

Write a function SumOfDigits that takes as a parameter a non-negative integer x and calculates the sum of the (decimal) digits that comprise x. For example, the line

cout &lt;&lt; SumOfDigits(15290);

should print “17” because 1+5+2+9+0 = 17.

For this exercise, it might be helpful to declare some variables of type long rather than int to give you the chance to test some longer, more juicy, instances.

<table>

 <tbody>

  <tr>

   <td>

    <table>

     <tbody>

      <tr>

       <td><strong>?</strong></td>

       <td>HINT</td>

      </tr>

     </tbody>

    </table></td>

   <td>

    <table>

     <tbody>

      <tr>

       <td>You can get the rightmost decimal digit of an integer via the remainder of division by 10. Moreover, first dividing by 10 and then taking the remainder yields the next digit. Repeating this process will give any digit you desire.</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<h3>smuS</h3>

Write a function SumWithDigitsReversed that takes a (non-negative integer) parameter x, and sums x with the number constructed from x with its decimal digits reversed. For example, the line

cout &lt;&lt; SumWithDigitsReversed(15290);

should produce “24541” since 15290 + 09251 = 24541.

<table>

 <tbody>

  <tr>

   <td>

    <table>

     <tbody>

      <tr>

       <td><strong>?</strong></td>

       <td>HINT</td>

      </tr>

     </tbody>

    </table></td>

   <td>

    <table>

     <tbody>

      <tr>

       <td>Build on the techniques used in the previous question. Additionally, for this question it can be useful to write some helper functions, two that are particularly handy are: NumDigits(n) to get the number of digits in a number; PowTen(m) to compute powers of ten easily.</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<h3>Numbers I</h3>

Write a function that determines whether its input is a prime number. The following is how you might start the definition of the function.

bool is_prime(int n){ // returns true if and only if n is a prime number    …}

<h3>Numbers II</h3>

Using your function from the previous question, prompt the user for an upper bound, then print all primes up to that number. Below is an example. You should attempt to match the output format exactly.

Enter an upper limit: 722, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71

<h3>Numbers III</h3>

First asserted in a letter penned to Euler in 1742, Goldbach’s conjecture states that:<em>every positive even number greater than 2 is the sum of two prime numbers</em>.

Examples: <em>42 = 5 + 37, 16 = 3 + 13, 64 = 3 + 61</em>.

Write a program that asks for an integer and, after checking that it is even and greater than 2, prints two primes whose sum is the input.

The statement above, though simple, is one of the most famous facts of number theory whose proof remains elusive. Actually, the wording above isn’t exactly how Goldbach expressed the claim to Euler, you can see the equivalent original statement in the associated <a href="https://en.wikipedia.org/wiki/Goldbach%27s_conjecture">Wikipedia article</a> if you are interested. It has been verified to be true up to enormous numbers (far, far larger than our puny int variables will hold), so if your program can’t find a pair that is a bug in your code.

<h2>Logic</h2>

<h3>Leap Years</h3>

Write a program that prompts the user for a year and then provides an output indicating whether that year is a <a href="https://en.wikipedia.org/wiki/Leap_year">leap year</a> or not. The rule for the Gregorian calendar, is as follows:<em>A year is a leap year if it is divisible by 4, unless it is divisible by 100 in which case it is not, unless it is divisible by 400 in which case it is. </em>

What are good test cases for your program?

<h3>Implementing Nand, Nor, and Exclusive-or</h3>

In class we saw the operations that C++ uses to represent logical <em>and</em>, <em>or</em>, and <em>not</em> operations. Three other common ones are <em>nand</em>, <em>nor</em>, and <em>exclusive-or</em>. Logical operations are often described using tables, which give a value for all possible input combinations. The three tables below specify <em>nand</em>, <em>nor</em>, and <em>exclusive-or</em>, respectively. You read the table as follows: pick the column representing the first input, the row representing the second input, and the value at the intersection of the row and column is the output of the operation.

<table>

 <tbody>

  <tr>

   <td>

    <table>

     <tbody>

      <tr>

       <td colspan="3"><strong>NAND</strong></td>

      </tr>

      <tr>

       <td></td>

       <td><strong>False</strong></td>

       <td><strong>True</strong></td>

      </tr>

      <tr>

       <td><strong>False</strong></td>

       <td>True</td>

       <td>True</td>

      </tr>

      <tr>

       <td><strong>True</strong></td>

       <td>True</td>

       <td>False</td>

      </tr>

     </tbody>

    </table></td>

   <td>

    <table>

     <tbody>

      <tr>

       <td colspan="3"><strong>NOR</strong></td>

      </tr>

      <tr>

       <td></td>

       <td><strong>False</strong></td>

       <td><strong>True</strong></td>

      </tr>

      <tr>

       <td><strong>False</strong></td>

       <td>True</td>

       <td>False</td>

      </tr>

      <tr>

       <td><strong>True</strong></td>

       <td>False</td>

       <td>False</td>

      </tr>

     </tbody>

    </table></td>

   <td>

    <table>

     <tbody>

      <tr>

       <td colspan="3"><strong>EXCLUSIVE-OR</strong></td>

      </tr>

      <tr>

       <td></td>

       <td><strong>False</strong></td>

       <td><strong>True</strong></td>

      </tr>

      <tr>

       <td><strong>False</strong></td>

       <td>False</td>

       <td>True</td>

      </tr>

      <tr>

       <td><strong>True</strong></td>

       <td>True</td>

       <td>False</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

Write functions that compute these operations. Below are three definitions to copy-and-paste into your editor for use as a starting point.

bool nand(bool a, bool b){ // is (a NAND b)    …} bool nor(bool a, bool b){ // is (a NOR b)    …} bool exclusive_or(bool a, bool b){ // is (a EXCLUSIVE-OR b)    …}

<h2>Efficient Integer Powers</h2>

Because multiplication is a fairly involved process, in the interests of speed it is common to seek ways to minimize the number of multiplication operations needed to arrive at some result. Consider the following example, where we’re raising a number to the fifth power.

A naïve approach is simply to multiply a number by itself over and over again:56<sup>5</sup> = 56×56×56×56×56 = 550731776.  Needs a total of 4 multiplications.

Oftentimes we can do better. Here we can see that by using squaring we can save a multiplication. Raising to larger powers can yield larger savings.Step 1: Let <em>u</em> = 56×56Step 2: Now let <em>v</em> = <em>u</em>×<em>u</em>Step 3: Then 56<sup>5</sup> = <em>v</em>×56 = 550731776.  Gives the result in a total of 3 multiplications.

In this exercise you’ll write a function to raise a number to an integer power using this repeated squaring approach. It is broken into pieces to provide some guidance.

<h3>The Easy Powers</h3>

The first step is to ask which powers can we get just by squaring?

Well if we’re given <em>b</em> and <em>m</em> and asked to compute <em>b<sup>m</sup></em> then if <em>m</em> = 2 it is easy. Squaring twice gives the solution easily when <em>m</em> = 4, and doing it three times when <em>m</em> = 8. Obviously the pattern emerging here is that when the exponent is a power of 2 we can get the solution in a straightforward manner.

int raiseExpPow2(int b, int m){ // compute (b^m) when m is a power of two.    …}

<h3>General Powers</h3>

The pattern that shows how to proceed for other exponents may also be obvious if you’re comfortable with numbers in binary (i.e., base 2). In the example given above, the exponent was 5 and, expressing the number in binary, we see that 5<sub>10</sub> = 101<sub>2</sub>. (Where I’ve used the fairly standard practice of having the subscripts indicate the base of the number system.)To get 56<sup>5</sup> we computed it as: 56<sup>5</sup> = (56<sup>2</sup>)<sup>2</sup>  ×  (56).

More generally, you can compute <em>b<sup>m</sup></em> by using your function raiseExpPow2 and the binary digits of <em>m</em>. The really great news is that in the “Summing Digits” exercise above, you were able to pull off the digits of a number. In that case you did it base 10, but the same process will pull them off base 2.

A smart thing to do is generalize the functions you wrote for “Summing Digits” to take the base as a parameter. Next, write a function to raise <em>b</em> to an arbitrary (positive integer) <em>m</em>.

int raiseExpPow(int b, int m){ // compute (b^m) when m is any positive integer    …}

<h3>Smarter Binary Digits</h3>

So far so good but if you’re doing divisions (likely both / and %) to get the binary digits (bits) of the exponent, then you’re actually doing <em>more</em> work, not less.

The trick is that since the machine actually represents the numbers in base 2, it is extremely easy to get the bits directly. (This is like how, when you were in grade school, you didn’t have any trouble with the 10 times table—the base trivializes things.)

Here is a function that will give you the i<sup>th</sup> bit of a number. Be careful. It is especially deceptive because we’ve seen both the &gt;&gt; and the &amp; before (we’ll see much more of that last character). They’re being used to mean entirely new things in this code.

int getBit(int n, int i){ // gets the value of the i’th bit of n  // where they are labeled right to left, starting from 0.  //  The “units” are at 0, (so even or odd numbers alter this entry)  //  The “twos” at 1, etc.    return (n &gt;&gt; i) &amp; 1; }

In the code above, the &gt;&gt; means bitwise <a href="https://en.wikipedia.org/wiki/Logical_shift">right shift</a>.And the &amp; performs the bitwise logical <em>and</em> operation.<a href="https://en.wikipedia.org/wiki/Bitwise_operations_in_C">This page details bitwise operations in C and C++</a>.

Improve your raiseExpPow to use these bitwise operations so as to avoid the divisions by 2.

<h3>Puzzling*</h3>

If you’ve finished the lab early, here’s something to tickle the gray matter:

“Four people need to cross a rickety footbridge; they all begin on the same side. It is dark, and they have one flashlight. A maximum of two people can cross the bridge at one time. Any party that crosses, either one or two people, must have the flashlight with them. The flashlight must be walked back and forth; it cannot be thrown, for example. Person 1 takes 1 minute to cross the bridge, person 2 takes 2 minutes, person 3 takes 5 minutes, and person 4 takes 10 minutes. A pair must walk together at the rate of the slower person’s pace. For example, if person 1 and person 4 walk together, it will take them 10 minutes to get to the other side. If person 4 returns the flashlight, a total of 20 minutes have passed. Can they cross the bridge in 17 minutes?”

— Levitin &amp; Levitin [2011].

* This is material outside the scope for lab quizzes.


