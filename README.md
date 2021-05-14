# PythonAdvancedProgramming

**PythonAdvancedPRogramming_1**

1. Write a function that takes a list of lists and returns the value of all of the
symbols in it, where each symbol adds or takes something from the total
score. Symbol values:
**#** = 5
 O = 3
 X = 1
 ! = -1
 !! = -3
 !!! = -5
A list of lists containing 2 #s, a O, and a !!! would equal (0 + 5 + 5 + 3 - 5) 8.
If the final score is negative, return 0 (e.g. 3 #s, 3 !!s, 2 !!!s and a X would be
(0 + 5 + 5 + 5 - 3 - 3 - 3 - 5 - 5 + 1) -3, so return 0.
Examples
check_score([
[&quot;#&quot;, &quot;!&quot;],
[&quot;!!&quot;, &quot;X&quot;]
]) ➞ 2
check_score([
[&quot;!!!&quot;, &quot;O&quot;, &quot;!&quot;],
[&quot;X&quot;, &quot;#&quot;, &quot;!!!&quot;],
[&quot;!!&quot;, &quot;X&quot;, &quot;O&quot;]
]) ➞ 0
2. Create a function that takes a variable number of arguments, each
argument representing the number of items in a group, and returns the
number of permutations (combinations) of items that you could get by taking
one item from each group.
Examples
combinations(2, 3) ➞ 6
combinations(3, 7, 4) ➞ 84
combinations(2, 3, 4, 5) ➞ 120

3. Create a function that takes a string as an argument and returns the Morse
code equivalent.
Examples
encode_morse(&quot;EDABBIT CHALLENGE&quot;) ➞ &quot;. -.. .- -... -... .. - -.-. .... .- .-.. .-..
. -. --. .&quot;
encode_morse(&quot;HELP ME !&quot;) ➞ &quot;.... . .-.. .--. -- . -.-.--&quot;
This dictionary can be used for coding:
char_to_dots = {
&#39;A&#39;: &#39;.-&#39;, &#39;B&#39;: &#39;-...&#39;, &#39;C&#39;: &#39;-.-.&#39;, &#39;D&#39;: &#39;-..&#39;, &#39;E&#39;: &#39;.&#39;, &#39;F&#39;: &#39;..-.&#39;,
&#39;G&#39;: &#39;--.&#39;, &#39;H&#39;: &#39;....&#39;, &#39;I&#39;: &#39;..&#39;, &#39;J&#39;: &#39;.---&#39;, &#39;K&#39;: &#39;-.-&#39;, &#39;L&#39;: &#39;.-..&#39;,
&#39;M&#39;: &#39;--&#39;, &#39;N&#39;: &#39;-.&#39;, &#39;O&#39;: &#39;---&#39;, &#39;P&#39;: &#39;.--.&#39;, &#39;Q&#39;: &#39;--.-&#39;, &#39;R&#39;: &#39;.-.&#39;,
&#39;S&#39;: &#39;...&#39;, &#39;T&#39;: &#39;-&#39;, &#39;U&#39;: &#39;..-&#39;, &#39;V&#39;: &#39;...-&#39;, &#39;W&#39;: &#39;.--&#39;, &#39;X&#39;: &#39;-..-&#39;,
&#39;Y&#39;: &#39;-.--&#39;, &#39;Z&#39;: &#39;--..&#39;, &#39; &#39;: &#39; &#39;, &#39;0&#39;: &#39;-----&#39;,
&#39;1&#39;: &#39;.----&#39;, &#39;2&#39;: &#39;..---&#39;, &#39;3&#39;: &#39;...--&#39;, &#39;4&#39;: &#39;....-&#39;, &#39;5&#39;: &#39;.....&#39;,
&#39;6&#39;: &#39;-....&#39;, &#39;7&#39;: &#39;--...&#39;, &#39;8&#39;: &#39;---..&#39;, &#39;9&#39;: &#39;----.&#39;,
&#39;&amp;&#39;: &#39;.-...&#39;, &quot;&#39;&quot;: &#39;.----.&#39;, &#39;@&#39;: &#39;.--.-.&#39;, &#39;)&#39;: &#39;-.--.-&#39;, &#39;(&#39;: &#39;-.--.&#39;,
&#39;:&#39;: &#39;---...&#39;, &#39;,&#39;: &#39;--..--&#39;, &#39;=&#39;: &#39;-...-&#39;, &#39;!&#39;: &#39;-.-.--&#39;, &#39;.&#39;: &#39;.-.-.-&#39;,
&#39;-&#39;: &#39;-....-&#39;, &#39;+&#39;: &#39;.-.-.&#39;, &#39;&quot;&#39;: &#39;.-..-.&#39;, &#39;?&#39;: &#39;..--..&#39;, &#39;/&#39;: &#39;-..-.&#39;
}
4. Write a function that takes a number and returns True if it&#39;s a prime; False
otherwise. The number can be 2^64-1 (2 to the power of 63, not XOR). With
the standard technique it would be O(2^64-1), which is much too large for the
10 second time limit.
Examples
prime(7) ➞ True
prime(56963) ➞ True
prime(5151512515524) ➞ False

5. Create a function that converts a word to a bitstring and then to a boolean
list based on the following criteria:
1. Locate the position of the letter in the English alphabet (from 1 to 26).
2. Odd positions will be represented as 1 and 0 otherwise.
3. Convert the represented positions to boolean values, 1 for True and 0
for False.
4. Store the conversions into an array.
Examples
to_boolean_list(&quot;deep&quot;) ➞ [False, True, True, False]
 deep converts to 0110
 d is the 4th alphabet - 0
 e is the 5th alphabet - 1
 e is the 5th alphabet - 1
 p is the 16th alphabet - 0
to_boolean_list(&quot;loves&quot;) ➞ [False, True, False, True, True]
to_boolean_list(&quot;tesh&quot;) ➞ [False, True, True, False]

**PythonAdvancedProgramming_2**

1. Write a function that takes a positive integer num and calculates how many
dots exist in a pentagonal shape around the center dot on the Nth iteration.
In the image below you can see the first iteration is only a single dot. On the
second, there are 6 dots. On the third, there are 16 dots, and on the fourth
there are 31 dots.

Return the number of dots that exist in the whole pentagon on the Nth
iteration.
Examples
pentagonal(1) ➞ 1
pentagonal(2) ➞ 6
pentagonal(3) ➞ 16
pentagonal(8) ➞ 141

2. Make a function that encrypts a given input with these steps:
Input: &quot;apple&quot;
Step 1: Reverse the input: &quot;elppa&quot;
Step 2: Replace all vowels using the following chart:
a =&gt; 0
e =&gt; 1
i =&gt; 2
o =&gt; 2
u =&gt; 3
&quot;1lpp0&quot;

Step 3: Add &quot;aca&quot; to the end of the word: &quot;1lpp0aca&quot;
Output: &quot;1lpp0aca&quot;
Examples
encrypt(&quot;banana&quot;) ➞ &quot;0n0n0baca&quot;
encrypt(&quot;karaca&quot;) ➞ &quot;0c0r0kaca&quot;
encrypt(&quot;burak&quot;) ➞ &quot;k0r3baca&quot;
encrypt(&quot;alpaca&quot;) ➞ &quot;0c0pl0aca&quot;


3. Given the month and year as numbers, return whether that month contains
a Friday 13th.(i.e You can check Python&#39;s datetime module)
Examples
has_friday_13(3, 2020) ➞ True
has_friday_13(10, 2017) ➞ True
has_friday_13(1, 1985) ➞ False

4. Write a regular expression that will help us count how many bad cookies
are produced every day. You must use RegEx negative lookbehind.
Example
lst = [&quot;bad cookie&quot;, &quot;good cookie&quot;, &quot;bad cookie&quot;, &quot;good cookie&quot;, &quot;good cookie&quot;]
pattern = &quot;yourregularexpressionhere&quot;
len(re.findall(pattern, &quot;, &quot;.join(lst))) ➞ 2


5. Given a list of words in the singular form, return a set of those words in the
plural form if they appear more than once in the list.
Examples
pluralize([&quot;cow&quot;, &quot;pig&quot;, &quot;cow&quot;, &quot;cow&quot;]) ➞ { &quot;cows&quot;, &quot;pig&quot; }
pluralize([&quot;table&quot;, &quot;table&quot;, &quot;table&quot;]) ➞ { &quot;tables&quot; }

pluralize([&quot;chair&quot;, &quot;pencil&quot;, &quot;arm&quot;]) ➞ { &quot;chair&quot;, &quot;pencil&quot;, &quot;arm&quot; }


**PythonAdvancedPRogramming_3**

1. Create a function to perform basic arithmetic operations that includes
addition, subtraction, multiplication and division on a string number (e.g. &quot;12 +
24&quot; or &quot;23 - 21&quot; or &quot;12 // 12&quot; or &quot;12 * 21&quot;).
Here, we have 1 followed by a space, operator followed by another space
and 2. For the challenge, we are going to have only two numbers between 1
valid operator. The return value should be a number.
eval() is not allowed. In case of division, whenever the second number equals
&quot;0&quot; return -1.
For example:
&quot;15 // 0&quot; ➞ -1
Examples
arithmetic_operation(&quot;12 + 12&quot;) ➞ 24 // 12 + 12 = 24
arithmetic_operation(&quot;12 - 12&quot;) ➞ 24 // 12 - 12 = 0
arithmetic_operation(&quot;12 * 12&quot;) ➞ 144 // 12 * 12 = 144
arithmetic_operation(&quot;12 // 0&quot;) ➞ -1 // 12 / 0 = -1
2. Write a function that takes the coordinates of three points in the form of a
2d array and returns the perimeter of the triangle. The given points are the
vertices of a triangle on a two-dimensional plane.
Examples
perimeter( [ [15, 7], [5, 22], [11, 1] ] ) ➞ 47.08
perimeter( [ [0, 0], [0, 1], [1, 0] ] ) ➞ 3.42
perimeter( [ [-10, -10], [10, 10 ], [-10, 10] ] ) ➞ 68.28
3. A city skyline can be represented as a 2-D list with 1s representing
buildings. In the example below, the height of the tallest building is 4 (second-
most right column).
[[0, 0, 0, 0, 0, 0],
[0, 0, 0, 0, 1, 0],
[0, 0, 1, 0, 1, 0],
[0, 1, 1, 1, 1, 0],

[1, 1, 1, 1, 1, 1]]
Create a function that takes a skyline (2-D list of 0&#39;s and 1&#39;s) and returns the
height of the tallest skyscraper.
Examples
tallest_skyscraper([
[0, 0, 0, 0],
[0, 1, 0, 0],
[0, 1, 1, 0],
[1, 1, 1, 1]
]) ➞ 3
tallest_skyscraper([
[0, 1, 0, 0],
[0, 1, 0, 0],
[0, 1, 1, 0],
[1, 1, 1, 1]
]) ➞ 4
tallest_skyscraper([
[0, 0, 0, 0],
[0, 0, 0, 0],
[1, 1, 1, 0],
[1, 1, 1, 1]
]) ➞ 2



4. A financial institution provides professional services to banks and claims
charges from the customers based on the number of man-days provided.
Internally, it has set a scheme to motivate and reward staff to meet and
exceed targeted billable utilization and revenues by paying a bonus for each
day claimed from customers in excess of a threshold target.
This quarterly scheme is calculated with a threshold target of 32 days per
quarter, and the incentive payment for each billable day in excess of such
threshold target is shown as follows:
Days Bonus
0 to 32 days Zero
33 to 40 days SGD$325 per billable day
41 to 48 days SGD$550 per billable day
Greater than 48 days SGD$600 per billable day

Please note that incentive payment is calculated progressively. As an
example, if an employee reached total billable days of 45 in a quarter, his/her
incentive payment is computed as follows:
32*0 + 8*325 + 5*550 = 5350
Write a function to read the billable days of an employee and return the bonus
he/she has obtained in that quarter.
Examples
bonus(15) ➞ 0
bonus(37) ➞ 1625
bonus(50) ➞ 8200



5. A number is said to be Disarium if the sum of its digits raised to their
respective positions is the number itself.
Create a function that determines whether a number is a Disarium or not.
Examples
is_disarium(75) ➞ False
7^1 + 5^2 = 7 + 25 = 32
is_disarium(135) ➞ True
1^1 + 3^2 + 5^3 = 1 + 9 + 125 = 135
is_disarium(544) ➞ False
is_disarium(518) ➞ True
is_disarium(466) ➞ False
is_disarium(8) ➞ True

**PythonAdvancedProgramming_4**

1. In mathematics, the Fibonacci numbers, commonly denoted Fn, form a
sequence, called the Fibonacci sequence, such that each number is the sum
of the two preceding ones, starting from 0 and 1:

The beginning of the sequence is this:
0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, ...
The function fastFib(num) returns the fibonacci number Fn, of the given num
as an argument.
Examples
fib_fast(5) ➞ 5
fib_fast(10) ➞ 55
fib_fast(20) ➞ 6765
fib_fast(50) ➞ 12586269025

2. Create a function that takes a strings characters as ASCII and returns each
characters hexadecimal value as a string.
Examples
convert_to_hex(&quot;hello world&quot;) ➞ &quot;68 65 6c 6c 6f 20 77 6f 72 6c 64&quot;
convert_to_hex(&quot;Big Boi&quot;) ➞ &quot;42 69 67 20 42 6f 69&quot;
convert_to_hex(&quot;Marty Poppinson&quot;) ➞ &quot;4d 61 72 74 79 20 50 6f 70 70 69 6e
73 6f 6e&quot;

3. Someone has attempted to censor my strings by replacing every vowel
with a *, l*k* th*s. Luckily, I&#39;ve been able to find the vowels that were
removed.
Given a censored string and a string of the censored vowels, return the
original uncensored string.
Example
uncensor(&quot;Wh*r* d*d my v*w*ls g*?&quot;, &quot;eeioeo&quot;) ➞ &quot;Where did my vowels go?&quot;
uncensor(&quot;abcd&quot;, &quot;&quot;) ➞ &quot;abcd&quot;
uncensor(&quot;*PP*RC*S*&quot;, &quot;UEAE&quot;) ➞ &quot;UPPERCASE&quot;

4. Write a function that takes an IP address and returns the domain name
using PTR DNS records.
Example
get_domain(&quot;8.8.8.8&quot;) ➞ &quot;dns.google&quot;
get_domain(&quot;8.8.4.4&quot;) ➞ &quot;dns.google&quot;

5. Create a function that takes an integer n and returns the factorial of
factorials. See below examples for a better understanding:
Examples
fact_of_fact(4) ➞ 288
4! * 3! * 2! * 1! = 288
fact_of_fact(5) ➞ 34560
fact_of_fact(6) ➞ 24883200

**PythonAdvancedProgramming_5**

1. Create a function that takes a number n (integer greater than zero) as an
argument, and returns 2 if n is odd and 8 if n is even.
You can only use the following arithmetic operators: addition of numbers +,
subtraction of numbers -, multiplication of number *, division of number /, and
exponentiation \**.
You are not allowed to use any other methods in this challenge (i.e. no if
statements, comparison operators, etc).
Examples
f(1) ➞ 2
f(2) ➞ 8
f(3) ➞ 2


2. Create a function that returns the majority vote in a list. A majority vote is
an element that occurs &gt; N/2 times in a list (where N is the length of the list).
Examples
majority_vote([&quot;A&quot;, &quot;A&quot;, &quot;B&quot;]) ➞ &quot;A&quot;
majority_vote([&quot;A&quot;, &quot;A&quot;, &quot;A&quot;, &quot;B&quot;, &quot;C&quot;, &quot;A&quot;]) ➞ &quot;A&quot;
majority_vote([&quot;A&quot;, &quot;B&quot;, &quot;B&quot;, &quot;A&quot;, &quot;C&quot;, &quot;C&quot;]) ➞ None


3. Create a function that takes a string txt and censors any word from a given
list lst. The text removed must be replaced by the given character char.
Examples
censor_string(&quot;Today is a Wednesday!&quot;, [&quot;Today&quot;, &quot;a&quot;], &quot;-&quot;) ➞ &quot;----- is -
Wednesday!&quot;
censor_string(&quot;The cow jumped over the moon.&quot;, [&quot;cow&quot;, &quot;over&quot;], &quot;*&quot;), &quot;The ***
jumped \**** the moon.&quot;)
censor_string(&quot;Why did the chicken cross the road?&quot;, [&quot;Did&quot;, &quot;chicken&quot;,
&quot;road&quot;], &quot;*&quot;) ➞ &quot;Why *** the ******* cross the ****?&quot;

4. In mathematics a Polydivisible Number (or magic number) is a number in a
given number base with digits abcde... that has the following properties:
- Its first digit a is not 0.
- The number formed by its first two digits ab is a multiple of 2.
- The number formed by its first three digits abc is a multiple of 3.
- The number formed by its first four digits abcd is a multiple of 4.
Create a function which takes an integer n and returns True if the given
number is a Polydivisible Number and False otherwise.
Examples
is_polydivisible(1232) ➞ True
 1 / 1 = 1
 12 / 2 = 6
 123 / 3 = 41
 1232 / 4 = 308
is_polydivisible(123220 ) ➞ False
 1 / 1 = 1
 12 / 2 = 6
 123 / 3 = 41
 1232 / 4 = 308
 12322 / 5 = 2464.4 # Not a Whole Number
 123220 /6 = 220536.333... # Not a Whole Number
 
 
5. Create a function that takes a list of numbers and returns the sum of all
prime numbers in the list.
Examples
sum_primes([1, 2, 3, 4, 5, 6, 7, 8, 9, 10]) ➞ 17
sum_primes([2, 3, 4, 11, 20, 50, 71]) ➞ 87
sum_primes([]) ➞ None
