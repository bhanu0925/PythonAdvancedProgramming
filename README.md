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


**PythonAdvancedProgramming_6**

1. You are given two strings s and t. String t is generated by randomly
shuffling string s and then adding one more letter at a random position.
Return the letter that was added to t.
Examples
find_the_difference(&quot;abcd&quot;, &quot;abcde&quot;) ➞ &quot;e&quot;
find_the_difference(&quot;&quot;, &quot;y&quot;) ➞ &quot;y&quot;
find_the_difference(&quot;ae&quot;, &quot;aea&quot;) ➞ &quot;a&quot;

2. Given a function that accepts unlimited arguments, check and count how
many data types are in those arguments. Finally return the total in a list.
List order is:
[int, str, bool, list, tuple, dictionary]
Examples
count_datatypes(1, 45, &quot;Hi&quot;, False) ➞ [2, 1, 1, 0, 0, 0]
count_datatypes([10, 20], (&quot;t&quot;, &quot;Ok&quot;), 2, 3, 1) ➞ [3, 0, 0, 1, 1, 0]
count_datatypes(&quot;Hello&quot;, &quot;Bye&quot;, True, True, False, {&quot;1&quot;: &quot;One&quot;, &quot;2&quot;: &quot;Two&quot;}, [1,
3], {&quot;Brayan&quot;: 18}, 25, 23) ➞ [2, 2, 3, 1, 0, 2]
count_datatypes(4, 21, (&quot;ES&quot;, &quot;EN&quot;), (&quot;a&quot;, &quot;b&quot;), False, [1, 2, 3], [4, 5, 6]) ➞ [2,
0, 1, 2, 2, 0]

3. A Fibonacci string is a precedence of the Fibonacci series. It works with
any two characters of the English alphabet (as opposed to the numbers 0 and
1 in the Fibonacci series) as the initial items and concatenates them together
as it progresses in a similar fashion as the Fibonacci series.
Examples
fib_str(3, [&quot;j&quot;, &quot;h&quot;]) ➞ &quot;j, h, hj&quot;
fib_str(5, [&quot;e&quot;, &quot;a&quot;]) ➞ &quot;e, a, ae, aea, aeaae&quot;
fib_str(6, [&quot;n&quot;, &quot;k&quot;]) ➞ &quot;n, k, kn, knk, knkkn, knkknknk&quot;

4. Given an integer between 0 and 26, make a variable (self.answer). That
variable would be assigned to a string in this format:
&quot;nines:your answer, threes:your answer, ones:your answer&quot;
You need to find out how many ones, threes, and nines it would at least take
for the number of each to add up to the given integer when multiplied by one,
three or nine (depends).
Examples
ones_threes_nines(10) ➞ &quot;nines:1, threes:0, ones:1&quot;
ones_threes_nines(15) ➞ &quot;nines:1, threes:2, ones:0&quot;
ones_threes_nines(22) ➞ &quot;nines:2, threes:1, ones:1&quot;

5. The Fibonacci sequence is a classic use case for recursive functions since
the value of the sequence at a given index is dependent on the sum of the
last two values. However, the recursion tree created by solving the Fibonacci
sequence recursively can grow quite fast. Therefore it can be important to
think about the implications of running a function recursively. Depending on
the size of n needed and the capabilities of the system in question you might
want to take a different approach.
Write a non-recursive function that takes an integer n and returns the
Fibonacci sequence&#39;s value at index n.
Examples
fib(6) ➞ 8
 0 + 1 = 1, 1 + 1 = 2, 1 + 2 = 3, 2 + 3 = 5, 3 + 5 = 8
fib(1) ➞ 1
fib(2) ➞ 1


**PythonAdvancedProgramming_7**

1. Write a function that counts how many concentric layers a rug.
Examples
count_layers([
&quot;AAAA&quot;,
&quot;ABBA&quot;,
&quot;AAAA&quot;
]) ➞ 2
count_layers([
&quot;AAAAAAAAA&quot;,
&quot;ABBBBBBBA&quot;,
&quot;ABBAAABBA&quot;,
&quot;ABBBBBBBA&quot;,
&quot;AAAAAAAAA&quot;
]) ➞ 3
count_layers([
&quot;AAAAAAAAAAA&quot;,
&quot;AABBBBBBBAA&quot;,
&quot;AABCCCCCBAA&quot;,
&quot;AABCAAACBAA&quot;,
&quot;AABCADACBAA&quot;,
&quot;AABCAAACBAA&quot;,
&quot;AABCCCCCBAA&quot;,
&quot;AABBBBBBBAA&quot;,
&quot;AAAAAAAAAAA&quot;
]) ➞ 5

2. There are many different styles of music and many albums exhibit multiple
styles. Create a function that takes a list of musical styles from albums and
returns how many styles are unique.
Examples
unique_styles([
&quot;Dub,Dancehall&quot;,
&quot;Industrial,Heavy Metal&quot;,
&quot;Techno,Dubstep&quot;,
&quot;Synth-pop,Euro-Disco&quot;,
&quot;Industrial,Techno,Minimal&quot;
]) ➞ 9
unique_styles([

&quot;Soul&quot;,
&quot;House,Folk&quot;,
&quot;Trance,Downtempo,Big Beat,House&quot;,
&quot;Deep House&quot;,
&quot;Soul&quot;
]) ➞ 7

3. Create a function that finds a target number in a list of prime numbers.
Implement a binary search algorithm in your function. The target number will
be from 2 through 97. If the target is prime then return &quot;yes&quot; else return &quot;no&quot;.
Examples
primes = [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67,
71, 73, 79, 83, 89, 97]

is_prime(primes, 3) ➞ &quot;yes&quot;
is_prime(primes, 4) ➞ &quot;no&quot;
is_prime(primes, 67) ➞ &quot;yes&quot;
is_prime(primes, 36) ➞ &quot;no&quot;

4. Create a function that takes in n, a, b and returns the number of positive
values raised to the nth power that lie in the range [a, b], inclusive.
Examples
power_ranger(2, 49, 65) ➞ 2
 2 squares (n^2) lie between 49 and 65, 49 (7^2) and 64 (8^2)
power_ranger(3, 1, 27) ➞ 3

 3 cubes (n^3) lie between 1 and 27, 1 (1^3), 8 (2^3) and 27 (3^3)
power_ranger(10, 1, 5) ➞ 1
 1 value raised to the 10th power lies between 1 and 5, 1 (1^10)
power_ranger(5, 31, 33) ➞ 1
power_ranger(4, 250, 1300) ➞ 3

5. Given a number, return the difference between the maximum and minimum
numbers that can be formed when the digits are rearranged.
Examples
rearranged_difference(972882) ➞ 760833
 988722 - 227889 = 760833
rearranged_difference(3320707) ➞ 7709823
 7733200 - 23377 = 7709823
rearranged_difference(90010) ➞ 90981
 91000 - 19 = 90981
 
 **PythonAdvancedProgramming_8**
 
 1. Given a sentence as txt, return True if any two adjacent words have this
property: One word ends with a vowel, while the word immediately after
begins with a vowel (a e i o u).
Examples
vowel_links(&quot;a very large appliance&quot;) ➞ True
vowel_links(&quot;go to edabit&quot;) ➞ True
vowel_links(&quot;an open fire&quot;) ➞ False
vowel_links(&quot;a sudden applause&quot;) ➞ False


2. You are given three inputs: a string, one letter, and a second letter.
Write a function that returns True if every instance of the first letter occurs
before every instance of the second letter.
Examples
first_before_second(&quot;a rabbit jumps joyfully&quot;, &quot;a&quot;, &quot;j&quot;) ➞ True
 Every instance of &quot;a&quot; occurs before every instance of &quot;j&quot;.
first_before_second(&quot;knaves knew about waterfalls&quot;, &quot;k&quot;, &quot;w&quot;) ➞ True
first_before_second(&quot;happy birthday&quot;, &quot;a&quot;, &quot;y&quot;) ➞ False
 The &quot;a&quot; in &quot;birthday&quot; occurs after the &quot;y&quot; in &quot;happy&quot;.
first_before_second(&quot;precarious kangaroos&quot;, &quot;k&quot;, &quot;a&quot;) ➞ False


3. Create a function that returns the characters from a list or string r on odd or
even positions, depending on the specifier s. The specifier will be &quot;odd&quot; for
items on odd positions (1, 3, 5, ...) and &quot;even&quot; for items on even positions (2,
4, 6, ...).
Examples
char_at_pos([2, 4, 6, 8, 10], &quot;even&quot;) ➞ [4, 8]
 4 &amp; 8 occupy the 2nd &amp; 4th positions
char_at_pos(&quot;EDABIT&quot;, &quot;odd&quot;) ➞ &quot;EAI&quot;
 &quot;E&quot;, &quot;A&quot; and &quot;I&quot; occupy the 1st, 3rd and 5th positions

char_at_pos([&quot;A&quot;, &quot;R&quot;, &quot;B&quot;, &quot;I&quot;, &quot;T&quot;, &quot;R&quot;, &quot;A&quot;, &quot;R&quot;, &quot;I&quot;, &quot;L&quot;, &quot;Y&quot;], &quot;odd&quot;) ➞ [&quot;A&quot;,
&quot;B&quot;, &quot;T&quot;, &quot;A&quot;, &quot;I&quot;, &quot;Y&quot;]


4. Write a function that returns the greatest common divisor of all list
elements. If the greatest common divisor is 1, return 1.
Examples
GCD([10, 20, 40]) ➞ 10
GCD([1, 2, 3, 100]) ➞ 1
GCD([1024, 192, 2048, 512]) ➞ 64


5. A number/string is a palindrome if the digits/characters are the same when
read both forward and backward. Examples include &quot;racecar&quot; and 12321.
Given a positive number n, check if n or the binary representation of n is
palindromic. Return the following:
- &quot;Decimal only.&quot; if only n is a palindrome.
- &quot;Binary only.&quot; if only the binary representation of n is a palindrome.
- &quot;Decimal and binary.&quot; if both are palindromes.
- &quot;Neither!&quot; if neither are palindromes.
Examples
palindrome_type(1306031) ➞ &quot;Decimal only.&quot;
 decimal = 1306031
 binary = &quot;100111110110110101111&quot;
palindrome_type(427787) ➞ &quot;Binary only.&quot;
 decimal = 427787
 binary = &quot;1101000011100001011&quot;
palindrome_type(313) ➞ &quot;Decimal and binary.&quot;
 decimal = 313
 binary = 100111001
palindrome_type(934) ➞ &quot;Neither!&quot;
 decimal = 934
 binary = &quot;1110100110&quot;
 
  **PythonAdvancedProgramming_9**
 
 1. YouTube offers different playback speed options for users. This allows
users to increase or decrease the speed of the video content. Given the
actual duration and playback speed of the video, calculate the playback
duration of the video.
Examples
playback_duration(&quot;00:30:00&quot;, 2) ➞ &quot;00:15:00&quot;
playback_duration(&quot;01:20:00&quot;, 1.5) ➞ &quot;00:53:20&quot;
playback_duration(&quot;51:20:09&quot;, 0.5) ➞ &quot;102:40:18&quot;

2. We needs your help to construct a building which will be a pile of n cubes.
The cube at the bottom will have a volume of n^3, the cube above will have
volume of (n-1)^3 and so on until the top which will have a volume of 1^3.
Given the total volume m of the building, can you find the number of cubes n
required for the building?
In other words, you have to return an integer n such that:
n^3 + (n-1)^3 + ... + 1^3 == m
Return None if there is no such number.
Examples
pile_of_cubes(1071225) ➞ 45
pile_of_cubes(4183059834009) ➞ 2022
pile_of_cubes(16) ➞ None

3. A fulcrum of a list is an integer such that all elements to the left of it and all
elements to the right of it sum to the same value. Write a function that finds
the fulcrum of a list.
To illustrate:
find_fulcrum([3, 1, 5, 2, 4, 6, -1]) ➞ 2
// Since [3, 1, 5] and [4, 6, -1] both sum to 9
Examples

find_fulcrum([1, 2, 4, 9, 10, -10, -9, 3]) ➞ 4
find_fulcrum([9, 1, 9]) ➞ 1
find_fulcrum([7, -1, 0, -1, 1, 1, 2, 3]) ➞ 0
find_fulcrum([8, 8, 8, 8]) ➞ -1

4. Given a list of integers representing the color of each sock, determine how
many pairs of socks with matching colors there are. For example, there are 7
socks with colors [1, 2, 1, 2, 1, 3, 2]. There is one pair of color 1 and one of
color 2. There are three odd socks left, one of each color. The number of
pairs is 2.
Create a function that returns an integer representing the number of matching
pairs of socks that are available.
Examples
sock_merchant([10, 20, 20, 10, 10, 30, 50, 10, 20]) ➞ 3
sock_merchant([50, 20, 30, 90, 30, 20, 50, 20, 90]) ➞ 4
sock_merchant([]) ➞ 0


5. Create a function that takes a string containing integers as well as other
characters and return the sum of the negative integers only.
Examples
negative_sum(&quot;-12 13%14&amp;-11&quot;) ➞ -23
 -12 + -11 = -23
negative_sum(&quot;22 13%14&amp;-11-22 13 12&quot;) ➞ -33
 -11 + -22 = -33
 
 **PythonAdvanceProgramming_10**
 
 1. Create a function that takes the width, height and character and returns a
picture frame as a 2D list.
Examples
get_frame(4, 5, &quot;#&quot;) ➞ [
[&quot;####&quot;],
[&quot;# #&quot;],
[&quot;# #&quot;],
[&quot;# #&quot;],
[&quot;####&quot;]
]
 Frame is 4 characters wide and 5 characters tall.

get_frame(10, 3, &quot;*&quot;) ➞ [
[&quot;**********&quot;],
[&quot;* *&quot;],
[&quot;**********&quot;]
]
 Frame is 10 characters and wide and 3 characters tall.

get_frame(2, 5, &quot;0&quot;) ➞ &quot;invalid&quot;
 Frame&#39;s width is not more than 2.
 
 
2. Write three functions:
1. boolean_and
2. boolean_or
3. boolean_xor
These functions should evaluate a list of True and False values, starting from
the leftmost element and evaluating pairwise.
Examples
boolean_and([True, True, False, True]) ➞ False
 [True, True, False, True] =&gt; [True, False, True] =&gt; [False, True] =&gt; False
boolean_or([True, True, False, False]) ➞ True
 [True, True, False, True] =&gt; [True, False, False] =&gt; [True, False] =&gt; True
boolean_xor([True, True, False, False]) ➞ False
 [True, True, False, False] =&gt; [False, False, False] =&gt; [False, False] =&gt;
False

3. Create a function that creates a box based on dimension n.
Examples
make_box(5) ➞ [
&quot;#####&quot;,
&quot;# #&quot;,
&quot;# #&quot;,
&quot;# #&quot;,
&quot;#####&quot;
]
make_box(3) ➞ [
&quot;###&quot;,
&quot;# #&quot;,
&quot;###&quot;
]
make_box(2) ➞ [
&quot;##&quot;,
&quot;##&quot;
]
make_box(1) ➞ [
&quot;#&quot;
]


4. Given a common phrase, return False if any individual word in the phrase
contains duplicate letters. Return True otherwise.
Examples
no_duplicate_letters(&quot;Fortune favours the bold.&quot;) ➞ True
no_duplicate_letters(&quot;You can lead a horse to water, but you can&#39;t make him
drink.&quot;) ➞ True
no_duplicate_letters(&quot;Look before you leap.&quot;) ➞ False
Duplicate letters in &quot;Look&quot; and &quot;before&quot;.
no_duplicate_letters(&quot;An apple a day keeps the doctor away.&quot;) ➞ False
Duplicate letters in &quot;apple&quot;, &quot;keeps&quot;, &quot;doctor&quot;, and &quot;away&quot;.

5. Write a regular expression that will match the states that voted yes to
President Trump&#39;s impeachment. You must use RegEx positive lookahead.
Example
txt = &quot;Texas = no, California = yes, Florida = yes, Michigan = no&quot;
pattern = &quot;yourregularexpressionhere&quot;
re.findall(pattern, txt) ➞ [&quot;California&quot;, &quot;Florida&quot;]


**PythonAdvancedProgramming_11**

1. Create a function that takes a list and returns a new list containing only
prime numbers.
Examples
filter_primes([7, 9, 3, 9, 10, 11, 27]) ➞ [7, 3, 11]
filter_primes([10007, 1009, 1007, 27, 147, 77, 1001, 70]) ➞ [10007, 1009]
filter_primes([1009, 10, 10, 10, 3, 33, 9, 4, 1, 61, 63, 69, 1087, 1091, 1093,
1097]) ➞ [1009, 3, 61, 1087, 1091, 1093, 1097]

2. Once a water balloon pops, is soaks the area around it. The ground gets
drier the further away you travel from the balloon.
The effect of a water balloon popping can be modeled using a list. Create a
function that takes a list which takes the pre-pop state and returns the state
after the balloon is popped. The pre-pop state will contain at most a single
balloon, whose size is represented by the only non-zero element.
Examples
pop([0, 0, 0, 0, 4, 0, 0, 0, 0]) ➞ [0, 1, 2, 3, 4, 3, 2, 1, 0]
pop([0, 0, 0, 3, 0, 0, 0]) ➞ [0, 1, 2, 3, 2, 1, 0]
pop([0, 0, 2, 0, 0]) ➞ [0, 1, 2, 1, 0]
pop([0]) ➞ [0]

3. &quot;Loves me, loves me not&quot; is a traditional game in which a person plucks off
all the petals of a flower one by one, saying the phrase &quot;Loves me&quot; and
&quot;Loves me not&quot; when determining whether the one that they love, loves them
back.
Given a number of petals, return a string which repeats the phrases &quot;Loves
me&quot; and &quot;Loves me not&quot; for every alternating petal, and return the last phrase
in all caps. Remember to put a comma and space between phrases.
Examples
loves_me(3) ➞ &quot;Loves me, Loves me not, LOVES ME&quot;
loves_me(6) ➞ &quot;Loves me, Loves me not, Loves me, Loves me not, Loves
me, LOVES ME NOT&quot;
loves_me(1) ➞ &quot;LOVES ME&quot;

4. Write a function that sorts each string in a list by the letter in alphabetic
ascending order (a-z).
Examples
sort_by_letter([&quot;932c&quot;, &quot;832u32&quot;, &quot;2344b&quot;])
➞ [&quot;2344b&quot;, &quot;932c&quot;, &quot;832u32&quot;]
sort_by_letter([&quot;99a&quot;, &quot;78b&quot;, &quot;c2345&quot;, &quot;11d&quot;])
➞ [&quot;99a&quot;, &quot;78b&quot;, &quot;c2345&quot;, &quot;11d&quot;]
sort_by_letter([&quot;572z&quot;, &quot;5y5&quot;, &quot;304q2&quot;])
➞ [&quot;304q2&quot;, &quot;5y5&quot;, &quot;572z&quot;]
sort_by_letter([])
➞ []

5. There are three cups on a table, at positions A, B, and C. At the start, there
is a ball hidden under the cup at position B.

However, I perform several swaps on the cups, which is notated as two
letters. For example, if I swap the cups at positions A and B, I could notate
this as AB or BA.
Create a function that returns the letter position that the ball is at, once I finish
swapping the cups. The swaps will be given to you as a list.

Example
cup_swapping([&quot;AB&quot;, &quot;CA&quot;, &quot;AB&quot;]) ➞ &quot;C&quot;
  Ball begins at position B.
  Cups A and B swap, so the ball is at position A.
  Cups C and A swap, so the ball is at position C.
  Cups A and B swap, but the ball is at position C, so it doesn&#39;t move.
  
  **PythonAdvancedProgramming_12**
  
  1. For this challenge, forget how to add two numbers together. The best
explanation on what to do for this function is this meme:

Examples
meme_sum(26, 39) ➞ 515
 2+3 = 5, 6+9 = 15
 26 + 39 = 515
meme_sum(122, 81) ➞ 1103
 1+0 = 1, 2+8 = 10, 2+1 = 3
 122 + 81 = 1103
meme_sum(1222, 30277) ➞ 31499

2. Given an integer, create a function that returns the next prime. If the
number is prime, return the number itself.
Examples

next_prime(12) ➞ 13
next_prime(24) ➞ 29
next_prime(11) ➞ 11
 11 is a prime, so we return the number itself.
 
 
3. If a person traveled up a hill for 18mins at 20mph and then traveled back
down the same path at 60mph then their average speed traveled was 30mph.
Write a function that returns the average speed traveled given an uphill time,
uphill rate and a downhill rate. Uphill time is given in minutes. Return the rate
as an integer (mph). No rounding is necessary.
Examples
ave_spd(18, 20, 60) ➞ 30
ave_spd(30, 10, 30) ➞ 15
ave_spd(30, 8, 24) ➞ 


4. The Kempner Function, applied to a composite number, permits to find the
smallest integer greater than zero whose factorial is exactly divided by the
number.
kempner(6) ➞ 3
1! = 1 % 6 &gt; 0
2! = 2 % 6 &gt; 0
3! = 6 % 6 === 0
kempner(10) ➞ 5
1! = 1 % 10 &gt; 0
2! = 2 % 10 &gt; 0
3! = 6 % 10 &gt; 0
4! = 24 % 10 &gt; 0
5! = 120 % 10 === 0
A Kempner Function applied to a prime will always return the prime itself.
kempner(2) ➞ 2
kempner(5) ➞ 5

Given an integer n, implement a Kempner Function.
Examples
kempner(6) ➞ 3
kempner(10) ➞ 5
kempner(2) ➞ 2


5. You work in a factory, and your job is to take items from a conveyor belt
and pack them into boxes. Each box can hold a maximum of 10 kgs. Given a
list containing the weight (in kg) of each item, how many boxes would you
need to pack all of the items?
Example
boxes([2, 1, 2, 5, 4, 3, 6, 1, 1, 9, 3, 2]) ➞ 5
 Box 1 = [2, 1, 2, 5] (10kg)
 Box 2 = [4, 3] (7kg)
 Box 3 = [6, 1, 1] (8kg)
 Box 4 = [9] (9kg)
 Box 5 = [3, 2] (5kg)
 
**PythonAdvancedProgramming_13**

1. Create a function that takes a list and string. The function should remove
the letters in the string from the list, and return the list.
Examples
remove_letters([&quot;s&quot;, &quot;t&quot;, &quot;r&quot;, &quot;i&quot;, &quot;n&quot;, &quot;g&quot;, &quot;w&quot;], &quot;string&quot;) ➞ [&quot;w&quot;]
remove_letters([&quot;b&quot;, &quot;b&quot;, &quot;l&quot;, &quot;l&quot;, &quot;g&quot;, &quot;n&quot;, &quot;o&quot;, &quot;a&quot;, &quot;w&quot;], &quot;balloon&quot;) ➞ [&quot;b&quot;, &quot;g&quot;,
&quot;w&quot;]
remove_letters([&quot;d&quot;, &quot;b&quot;, &quot;t&quot;, &quot;e&quot;, &quot;a&quot;, &quot;i&quot;], &quot;edabit&quot;) ➞ []


2. A block sequence in three dimensions. We can write a formula for this one:

Create a function that takes a number (step) as an argument and returns the
amount of blocks in that step.
Examples
blocks(1) ➞ 5
blocks(5) ➞ 39
blocks(2) ➞ 12


3. Create a function that subtracts one positive integer from another, without
using any arithmetic operators such as -, %, /, +, etc.
Examples
my_sub(5, 9) ➞ 4
my_sub(10, 30) ➞ 20
my_sub(0, 0) ➞ 0

4. Create a function that takes a string containing money in dollars and
pounds sterling (seperated by comma) and returns the sum of dollar bills only,
as an integer.
For the input string:
- Each amount is prefixed by the currency symbol: $ for dollars and £ for
pounds.
- Thousands are represented by the suffix k.
i.e. $4k = $4,000 and £40k = £40,000
Examples
add_bill(&quot;d20,p40,p60,d50&quot;) ➞ 20 + 50 = 70
add_bill(&quot;p30,d20,p60,d150,p360&quot;) ➞ 20 + 150 = 170
add_bill(&quot;p30,d2k,p60,d200,p360&quot;) ➞ 2 * 1000 + 200 = 2200

5. Create a function that flips a horizontal list into a vertical list, and a vertical
list into a horizontal list.
In other words, take an 1 x n list (1 row + n columns) and flip it into a n x 1 list
(n rows and 1 column), and vice versa.
Examples
flip_list([1, 2, 3, 4]) ➞ [[1], [2], [3], [4]]
 Take a horizontal list and flip it vertical.
flip_list([[5], [6], [9]]) ➞ [5, 6, 9]
 Take a vertical list and flip it horizontal.
flip_list([]) ➞ []

**PythonAdvancedProgramming_14**

1. Given a list of numbers, create a function that removes 25% from every
number in the list except the smallest number, and adds the total amount
removed to the smallest number.
Examples
show_the_love([4, 1, 4]) ➞ [3, 3, 3]
show_the_love([16, 10, 8]) ➞ [12, 7.5, 14.5]
show_the_love([2, 100]) ➞ [27, 75]

2. Create a function that takes in two words as input and returns a list of three
elements, in the following order:
1.Shared letters between two words.
2.Letters unique to word 1.
3.Letters unique to word 2.
Each element should have unique letters, and have each letter be
alphabetically sorted.
Examples
letters(&quot;sharp&quot;, &quot;soap&quot;) ➞ [&quot;aps&quot;, &quot;hr&quot;, &quot;o&quot;]
letters(&quot;board&quot;, &quot;bored&quot;) ➞ [&quot;bdor&quot;, &quot;a&quot;, &quot;e&quot;]
letters(&quot;happiness&quot;, &quot;envelope&quot;) ➞ [&quot;enp&quot;, &quot;ahis&quot;, &quot;lov&quot;]
letters(&quot;kerfuffle&quot;, &quot;fluffy&quot;) ➞ [&quot;flu&quot;, &quot;ekr&quot;, &quot;y&quot;]
 Even with multiple matching letters (e.g. 3 f&#39;s), there should
 only exist a single &quot;f&quot; in your first element.
letters(&quot;match&quot;, &quot;ham&quot;) ➞ [&quot;ahm&quot;, &quot;ct&quot;, &quot;&quot;]
 &quot;ham&quot; does not contain any letters that are not found already
 in &quot;match&quot;.

3. Write a function that pairs the first number in an array with the last, the
second number with the second to last, etc.
Examples
pairs([1, 2, 3, 4, 5, 6, 7]) ➞ [[1, 7], [2, 6], [3, 5], [4, 4]]

pairs([1, 2, 3, 4, 5, 6]) ➞ [[1, 6], [2, 5], [3, 4]]
pairs([5, 9, 8, 1, 2]) ➞ [[5, 2], [9, 1], [8, 8]]
pairs([]) ➞ []

4. Write a function that adds two numbers. The catch, however, is that the
numbers will be strings.
Examples
add_str_nums(&quot;4&quot;, &quot;5&quot;) ➞ &quot;9&quot;
add_str_nums(&quot;abcdefg&quot;, &quot;3&quot;) ➞ &quot;-1&quot;
add_str_nums(&quot;1&quot;, &quot;&quot;) ➞ &quot;1&quot;
add_str_nums(&quot;1874682736267235927359283579235789257&quot;,
&quot;32652983572985729&quot;) ➞ &quot;1874682736267235927391936562808774986&quot;

5. lPaeesh le pemu mnxit ehess rtnisg! Oh, sorry, that was supposed to say:
Please help me unmix these strings!
Somehow my strings have all become mixed up; every pair of characters has
been swapped. Help me undo this so I can understand my strings again.
Examples
unmix(&quot;123456&quot;) ➞ &quot;214365&quot;
unmix(&quot;hTsii s aimex dpus rtni.g&quot;) ➞ &quot;This is a mixed up string.&quot;
unmix(&quot;badce&quot;) ➞ &quot;abcde&quot;

**PythonAdvancedProgramming_15**

1. Write a function that returns True if a given name can generate an array of
words.
Examples
anagram(&quot;Justin Bieber&quot;, [&quot;injures&quot;, &quot;ebb&quot;, &quot;it&quot;]) ➞ True
anagram(&quot;Natalie Portman&quot;, [&quot;ornamental&quot;, &quot;pita&quot;]) ➞ True
anagram(&quot;Chris Pratt&quot;, [&quot;chirps&quot;, &quot;rat&quot;]) ➞ False
 Not all letters are used
anagram(&quot;Jeff Goldblum&quot;, [&quot;jog&quot;, &quot;meld&quot;, &quot;bluffs&quot;]) ➞ False
&quot;s&quot; does not exist in the original name

2. Given an array of users, each defined by an object with the following
properties: name, score, reputation create a function that sorts the array to
form the correct leaderboard.
The leaderboard takes into consideration the score of each user of course,
but an emphasis is put on their reputation in the community, so to get the
trueScore, you should add the reputation multiplied by 2 to the score.
Once you know the trueScore of each user, sort the array according to it in
descending order.
Examples
leaderboards([
{ &quot;name&quot;: &quot;a&quot;, &quot;score&quot;: 100, &quot;reputation&quot;: 20 },
{ &quot;name&quot;: &quot;b&quot;, &quot;score&quot;: 90, &quot;reputation&quot;: 40 },
{ &quot;name&quot;: &quot;c&quot;, &quot;score&quot;: 115, &quot;reputation&quot;: 30 },
]) ➞ [
{ &quot;name&quot;: &quot;c&quot;, &quot;score&quot;: 115, &quot;reputation&quot;: 30 }, # trueScore = 175
{ &quot;name&quot;: &quot;b&quot;, &quot;score&quot;: 90, &quot;reputation&quot;: 40 }, # trueScore = 170
{ &quot;name&quot;: &quot;a&quot;, &quot;score&quot;: 100, &quot;reputation&quot;: 20 } # trueScore = 140
]

3. Create a function that, given a phrase and a number of letters guessed,
returns a string with hyphens - for every letter of the phrase not guessed, and
each letter guessed in place.
Examples
hangman(&quot;helicopter&quot;, [&quot;o&quot;, &quot;e&quot;, &quot;s&quot;]) ➞ &quot;-e---o--e-&quot;

hangman(&quot;tree&quot;, [&quot;r&quot;, &quot;t&quot;, &quot;e&quot;]) ➞ &quot;tree&quot;
hangman(&quot;Python rules&quot;, [&quot;a&quot;, &quot;n&quot;, &quot;p&quot;, &quot;r&quot;, &quot;z&quot;]) ➞ &quot;P----n r----&quot;
hangman(&quot;He&quot;s a very naughty boy!&quot;, [&quot;e&quot;, &quot;a&quot;, &quot;y&quot;]) ➞ &quot;-e&quot;- a -e-y -a----y –y!&quot;

4. The Collatz sequence is as follows:
- Start with some given integer n.
- If it is even, the next number will be n divided by 2.
- If it is odd, multiply it by 3 and add 1 to make the next number.
- The sequence stops when it reaches 1.
According to the Collatz conjecture, it will always reach 1. If that&#39;s true, you
can construct a finite sequence following the aforementioned method for any
given integer.
Write a function that takes in an integer n and returns the highest integer in
the corresponding Collatz sequence.
Examples
max_collatz(10) ➞ 16
 Collatz sequence: 10, 5, 16, 8, 4, 2, 1
max_collatz(32) ➞ 32
 Collatz sequence: 32, 16, 8, 4, 2, 1
max_collatz(85) ➞ 256
 Collatz sequence: 85, 256, 128, 64, 32, 16, 8, 4, 2, 1
 
5. Write a function that sorts a list of integers by their digit length in
descending order, then settles ties by sorting numbers with the same digit
length in ascending order.
Examples
digit_sort([77, 23, 5, 7, 101])
➞ [101, 23, 77, 5, 7]
digit_sort([1, 5, 9, 2, 789, 563, 444])
➞ [444, 563, 789, 1, 2, 5, 9]
digit_sort([53219, 3772, 564, 32, 1])

➞ [53219, 3772, 564, 32, 1]

**PythonAdvancedProgramming_16**

1. Rondo Form is a type of musical structure, in which there is a recurring
theme/refrain, notated as A. Here are the rules for valid rondo forms:
- Rondo forms always start and end with an A section.
- In between the A sections, there should be contrasting sections notated as
B, then C, then D, etc... No letter should be skipped.
- There shouldn&#39;t be any repeats in the sequence (such as ABBACCA).
Create a function which validates whether a given string is a valid Rondo
Form.
Examples
valid_rondo(&quot;ABACADAEAFAGAHAIAJA&quot;) ➞ True
valid_rondo(&quot;ABA&quot;) ➞ True
valid_rondo(&quot;ABBACCA&quot;) ➞ False
valid_rondo(&quot;ACAC&quot;) ➞ False
valid_rondo(&quot;A&quot;) ➞ False


2. Create a function that returns the whole of the first sentence which
contains a specific word. Include the full stop at the end of the sentence.
Examples
txt = &quot;I have a cat. I have a mat. Things are going swell.&quot;
sentence_searcher(txt, &quot;have&quot;) ➞ &quot;I have a cat.&quot;
sentence_searcher(txt, &quot;MAT&quot;) ➞ &quot;I have a mat.&quot;
sentence_searcher(txt, &quot;things&quot;) ➞ &quot;Things are going swell.&quot;
sentence_searcher(txt, &quot;flat&quot;) ➞ &quot;&quot;


3. Given a number, find the &quot;round &quot;of each digit of the number. An integer is
called &quot;round&quot; if all its digits except the leftmost (most significant) are equal to
zero.
- Round numbers: 4000, 1, 9, 800, 90
- Not round numbers: 110, 707, 222, 1001

Create a function that takes a number and returns the &quot;round&quot; of each digit
(except if the digit is zero) as a string. Check out the following examples for
more clarification.
Examples
sum_round(101) ➞ &quot;1 100&quot;
sum_round(1234) ➞ &quot;4 30 200 1000&quot;
sum_round(54210) ➞ &quot;10 200 4000 50000&quot;

4. Your task, is to create N x N multiplication table, of size n provided in
parameter.
For example, when n is 5, the multiplication table is:
- 1, 2, 3, 4, 5
- 2, 4, 6, 8, 10
- 3, 6, 9, 12, 15
- 4, 8, 12, 16, 20
- 5, 10, 15, 20, 25
This example will result in:
[[1, 2, 3, 4, 5], [2, 4, 6, 8, 10], [3, 6, 9, 12, 15], [4, 8, 12, 16, 20], [5, 10, 15, 20,
25]]
Examples
multiplication_table(1) ➞ [[1]]
multiplication_table(3) ➞ [[1, 2, 3], [2, 4, 6], [3, 6, 9]]

5. Create a function that returns True if two lines rhyme and False otherwise.
For the purposes of this exercise, two lines rhyme if the last word from each
sentence contains the same vowels.
Examples
does_rhyme(&quot;Sam I am!&quot;, &quot;Green eggs and ham.&quot;) ➞ True
does_rhyme(&quot;Sam I am!&quot;, &quot;Green eggs and HAM.&quot;) ➞ True
Capitalization and punctuation should not matter.

does_rhyme(&quot;You are off to the races&quot;, &quot;a splendid day.&quot;) ➞ False
does_rhyme(&quot;and frequently do?&quot;, &quot;you gotta move.&quot;) ➞ False



**PythonAdvancedProgramming_24**

1. Write a function that returns True if a given name can generate an array of
words.
Examples
anagram(&quot;Justin Bieber&quot;, [&quot;injures&quot;, &quot;ebb&quot;, &quot;it&quot;]) ➞ True
anagram(&quot;Natalie Portman&quot;, [&quot;ornamental&quot;, &quot;pita&quot;]) ➞ True
anagram(&quot;Chris Pratt&quot;, [&quot;chirps&quot;, &quot;rat&quot;]) ➞ False
 Not all letters are used
anagram(&quot;Jeff Goldblum&quot;, [&quot;jog&quot;, &quot;meld&quot;, &quot;bluffs&quot;]) ➞ False
 &quot;s&quot; does not exist in the original name
 
2. Given an array of users, each defined by an object with the following
properties: name, score, reputation create a function that sorts the array to
form the correct leaderboard.
The leaderboard takes into consideration the score of each user of course,
but an emphasis is put on their reputation in the community, so to get the
trueScore, you should add the reputation multiplied by 2 to the score.
Once you know the trueScore of each user, sort the array according to it in
descending order.
Examples
leaderboards([
{ &quot;name&quot;: &quot;a&quot;, &quot;score&quot;: 100, &quot;reputation&quot;: 20 },
{ &quot;name&quot;: &quot;b&quot;, &quot;score&quot;: 90, &quot;reputation&quot;: 40 },
{ &quot;name&quot;: &quot;c&quot;, &quot;score&quot;: 115, &quot;reputation&quot;: 30 },
]) ➞ [
{ &quot;name&quot;: &quot;c&quot;, &quot;score&quot;: 115, &quot;reputation&quot;: 30 }, # trueScore = 175
{ &quot;name&quot;: &quot;b&quot;, &quot;score&quot;: 90, &quot;reputation&quot;: 40 }, # trueScore = 170
{ &quot;name&quot;: &quot;a&quot;, &quot;score&quot;: 100, &quot;reputation&quot;: 20 } # trueScore = 140
]

3. Create a function that, given a phrase and a number of letters guessed,
returns a string with hyphens - for every letter of the phrase not guessed, and
each letter guessed in place.
Examples
hangman(&quot;helicopter&quot;, [&quot;o&quot;, &quot;e&quot;, &quot;s&quot;]) ➞ &quot;-e---o--e-&quot;

hangman(&quot;tree&quot;, [&quot;r&quot;, &quot;t&quot;, &quot;e&quot;]) ➞ &quot;tree&quot;
hangman(&quot;Python rules&quot;, [&quot;a&quot;, &quot;n&quot;, &quot;p&quot;, &quot;r&quot;, &quot;z&quot;]) ➞ &quot;P----n r----&quot;
hangman(&quot;He&quot;s a very naughty boy!&quot;, [&quot;e&quot;, &quot;a&quot;, &quot;y&quot;]) ➞ &quot;-e&quot;- a -e-y -a----y –y!&quot;

4. The Collatz sequence is as follows:
- Start with some given integer n.
- If it is even, the next number will be n divided by 2.
- If it is odd, multiply it by 3 and add 1 to make the next number.
- The sequence stops when it reaches 1.
According to the Collatz conjecture, it will always reach 1. If that&#39;s true, you
can construct a finite sequence following the aforementioned method for any
given integer.
Write a function that takes in an integer n and returns the highest integer in
the corresponding Collatz sequence.
Examples
max_collatz(10) ➞ 16
 Collatz sequence: 10, 5, 16, 8, 4, 2, 1
max_collatz(32) ➞ 32
 Collatz sequence: 32, 16, 8, 4, 2, 1
max_collatz(85) ➞ 256
 Collatz sequence: 85, 256, 128, 64, 32, 16, 8, 4, 2, 1

5. Write a function that sorts a list of integers by their digit length in
descending order, then settles ties by sorting numbers with the same digit
length in ascending order.
Examples
digit_sort([77, 23, 5, 7, 101])
➞ [101, 23, 77, 5, 7]
digit_sort([1, 5, 9, 2, 789, 563, 444])
➞ [444, 563, 789, 1, 2, 5, 9]
digit_sort([53219, 3772, 564, 32, 1])
➞ [53219, 3772, 564, 32, 1]


**PythonAdvancedProgramming_25**

1. Write four functions that directly mutate a list:
1. repeat(lst, n): Repeat lst n times.
2. add(lst, x): Adds x to the end of the lst.
3. remove(lst, m, n): Removes all elements between indices m and n
inclusive in lst.
4. concat(lst, x): concatenates lst with x (another list).
Examples
lst = [1, 2, 3, 4]
repeat(lst, 3) ➞ [1, 2, 3, 4, 1, 2, 3, 4, 1, 2, 3, 4]
add(lst, 1) ➞ [1, 2, 3, 4, 1, 2, 3, 4, 1, 2, 3, 4, 1]
remove(lst, 1, 12) ➞ [1]
concat(lst, [3, 4]) ➞ [1, 3, 4]

2. The classic game of Mastermind is played on a tray on which the
Mastermind conceals a code and the Guesser has 10 tries to guess it. The
code is a sequence of 4 (or 6, sometimes more) pegs of different colors. Each
guess is a corresponding sequence of 4 (or more) pegs of different colors. A
guess is 'correct' when the color of every peg in the guess exactly matches
the corresponding peg in the Mastermind's code.
After each guess by the Guesser, the Mastermind will give a score comprising
black & white pegs, not arranged in any order:
- Black peg == guess peg matches the color of a code peg in the same
position.
- White peg == guess peg matches the color of a code peg in another
position.
Create a function that takes two strings, code and guess as arguments, and
returns the score in a dictionary.
- The code and guess are strings of numeric digits
- The color of the pegs are represented by numeric digits
- no 'peg' may be double-scored
Examples
guess_score('1423', '5678') ➞ {'black': 0, 'white': 0}

guess_score('1423', '2222') ➞ {'black': 1, 'white': 0}
guess_score('1423', '1234') ➞ {'black': 1, 'white': 3}
guess_score('1423', '2211') ➞ {'black': 0, 'white': 2}

3. Create a function that takes a list lst and a number N and returns a list of
two integers from lst whose product equals N.
Examples
two_product([1, 2, -1, 4, 5], 20) ➞ [4, 5]
two_product([1, 2, 3, 4, 5], 10) ➞ [2, 5]
two_product([100, 12, 4, 1, 2], 15) ➞ None

4. In this challenge, sort a list containing a series of dates given as strings.
Each date is given in the format DD-MM-YYYY_HH:MM:
'12-02-2012_13:44'
The priority of criteria used for sorting will be:
- Year
- Month
- Day
- Hours
- Minutes
Given a list lst and a string mode, implement a function that returns:
- if mode is equal to 'ASC', the list lst sorted in ascending order.
- if mode is equal to 'DSC', the list lst sorted in descending order.
Examples
sort_dates(['10-02-2018_12:30', '10-02-2016_12:30', '10-02-2018_12:15'],
'ASC') ➞ ['10-02-2016_12:30', '10-02-2018_12:15', '10-02-2018_12:30']
sort_dates(['10-02-2018_12:30', '10-02-2016_12:30', '10-02-2018_12:15'],
'DSC') ➞ ['10-02-2018_12:30', '10-02-2018_12:15', '10-02-2016_12:30']

sort_dates(['09-02-2000_10:03', '10-02-2000_18:29', '01-01-1999_00:55'],
'ASC') ➞ ['01-01-1999_00:55', '09-02-2000_10:03', '10-02-2000_18:29']


5. Write a function that selects all words that have all the same vowels (in any
order and/or number) as the first word, including the first word.
Examples
same_vowel_group(['toe', 'ocelot', 'maniac']) ➞ ['toe', 'ocelot']
same_vowel_group(['many', 'carriage', 'emit', 'apricot', 'animal']) ➞
['many']
same_vowel_group(['hoops', 'chuff', 'bot', 'bottom']) ➞ ['hoops', 'bot',
'bottom']


6. Create a function that takes a list of more than three numbers and returns
the Least Common Multiple (LCM).
Examples
lcm_of_list([1, 2, 3, 4, 5, 6, 7, 8, 9, 10]) ➞ 2520
lcm_of_list([13, 6, 17, 18, 19, 20, 37]) ➞ 27965340
lcm_of_list([44, 64, 12, 17, 65]) ➞ 2333760
