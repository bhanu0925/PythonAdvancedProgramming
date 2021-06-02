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
