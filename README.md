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
