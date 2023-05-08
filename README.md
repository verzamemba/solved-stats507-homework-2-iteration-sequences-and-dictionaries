Download Link: https://assignmentchef.com/product/solved-stats507-homework-2-iteration-sequences-and-dictionaries
<br>
<h1>1         Fun with Strings</h1>

In this problem, you’ll implement a few simple functions for dealing with strings. You need not perform any error checking in any of the functions for this problem.

<ol>

 <li>A palindrome is a word or phrase that reads the same backwards and forwards<a href="https://en.wikipedia.org/wiki/Palindrome">(</a><a href="https://en.wikipedia.org/wiki/Palindrome">https://en.wikipedia.org/wiki/Palindrome</a><a href="https://en.wikipedia.org/wiki/Palindrome">)</a>. So, for example, the words “level”, “kayak” and “pop” are all English palindromes, as are the phrases “rats live on no evil star” and “Was it a car or a cat I saw?”, provided we ignore the spaces and punctuation. Write a function called is_palindrome, which takes a string as its only argument, and returns a Boolean. Your function should return True if the argument is a palindrome, and False For the purposes of this problem, you may assume that the input is a string and will consist only of alphanumeric characters (i.e., the letters, either upper or lower case, and the digits 0 through 9) and spaces. Your function should ignore spaces and capitalization in assessing whether or not a string is a palindrome, so that tacocat and T A C O cat are both considered palindromes.</li>

 <li>Let us say that a word is “abecedarian” if its letters appear in alphabetical order(repeated letters are okay). So, for example, “adder” and “beet” are abecedarian, whereas “dog” and “cat” are not. Write a function is_abecedarian, which takes a single argument in the form of a string and returns True if the argument is abecedarian and False Here you may assume that the input consists only of alphabetic characters and spaces. You function should ignore spaces, so that the string abcd efgh xyz is considered abecedarian.</li>

 <li>Write a function called remove_vowels that takes a string as its only argument and returns that string with all the vowels removed. For the purposes of this question, the vowels are the letters “a e i o u”. Thus, remove_vowels(’cat’) should return ’ct’, remove_vowels(’audio’) should return ’d’, etc. Take care that your function correctly handles a string of all vowels. <strong>Hint: </strong>there is a particularly elegant solution to this problem that makes use of the accumulator pattern we saw in lecture and the fact that Python strings implement the addition operation as string concatenation.</li>

</ol>

<h1>2         Fun with Lists</h1>

In this problem, you’ll implement a few very simple list operations.

<ol>

 <li>Write a function list_reverse that takes a list as an argument and returns that list, reversed. That is, given the list [1,2,3], your function should return the reversed list, [3,2,1]. Your function should raise an appropriate error in the event that the input is not a list.</li>

 <li>Write a function is_sorted that takes a sequence seq as its only argument and returns True if the sequence is sorted in ascending order and returns False You may assume that seq is, in fact, a Python sequence. Your function should require a single traversal of the list, and inefficient solutions (i.e., ones that require more than one traversal) will not receive full credit. You may assume that all elements in the input sequence seq support the comparison operations (==, &lt;/&gt;, &gt;=, etc), so that there is no need for error checking. (Indeed, if you try to make the comparison, say, 1 &lt; ’cat’, Python will raise an error for you, anyway.) <strong>Note: </strong>this problem illustrates a particularly useful aspect of Python’s dynamic typing. It is possible to write this function while being agnostic as to the type of the input variable. It requires only that seq supports indexing and that the elements in seq support the comparison operations.</li>

 <li>This one is a common coding interview question. Write a function called binary_search that takes two arguments, a list of integers t (which is guaranteed to be sorted in ascending order) and an integer elmt, and returns True if elmt appears in list t and False Of course, you could do this with the in operator, but that will be slow when the list is long, for reasons that we discussed in class. Instead, you should use <em>binary search</em>: To look for elmt, first look at the “middle” element of the list t. If it’s a match, return True . If it isn’t a match, compare elmt against the “middle” element, and recurse, searching the first or second half of the list depending on whether elmt is bigger or smaller than the middle element. <strong>Hint: </strong>be careful of the <em>base cases</em>: What should you do when t is empty, length 1, length 2, etc.? <strong>Note: </strong>your solution must actually make use of binary search to receive credit, and your solution must not use any built-in sorting or searching functions. <strong>Note: </strong>we could, if we wanted, use the function is_sorted that we wrote above to do error checking here, but there is a good reason not to do so. This reason will become clear when we make our brief foray into the topic of <em>runtime analysis </em>later in the semester.</li>

</ol>

<h1>3         More Fun with Strings</h1>

In this problem, you’ll implement some very simple counting operations that are common in fields like biostatistics and natural language processing. You need not perform any error checking in the functions for this problem.

<ol>

 <li>Write a function called char_hist that takes a string as its argument and returns a dictionary whose keys are characters and values are the number of times each character appeared in the input. So, for example, given the string “gattaca”, your function should return a dictionary with key-value pairs (<em>g,</em>1)<em>,</em>(<em>a,</em>3)<em>,</em>(<em>t,</em>2)<em>,</em>(<em>c,</em>1). Your function should count <em>all </em>characters in the input (including spaces, tabs, numbers, etc). The dictionary returned by your function should have as its keys all and only the characters that appeared in the input (i.e., you don’t need to have a bunch of keys with value 0!). Your function should count capital and lower-case letters as the same, and key on the lower-case version of the character, so that <em>G </em>and <em>g </em>are both counted as the same character, and the corresponding key in the dictionary is <em>g</em>.</li>

 <li>In natural language processing and bioinformatics, we often want to count how oftencharacters or groups of characters appear. Pairs of words or characters are called “bigrams”. For our purposes in this problem, a bigram is a pair of characters. As an example, the string ’mississippi’ contains the following bigrams, in order:</li>

</ol>

’mi’, ’is’, ’ss’, ’si’, ’is’, ’ss’, ’si’, ’ip’, ’pp’, ’pi’

Write a function called bigram_hist that takes a string as its argument and returns a dictionary whose keys are 2-tuples of characters and values are the number of times that pair of characters appeared in the string. So, for example, when called on the string ’mississippi’, your function should return a dictionary with keys

’mi’,’is’,’ss’,’si’,’ip’,’pp’,’pi’

and respective count values

1<em>,</em>2<em>,</em>2<em>,</em>2<em>,</em>1<em>,</em>1<em>,</em>1<em>.</em>

As another example, if the two-character string ’ab’ occurred four times in the input, then your function should return a dictionary that includes the key-value pair ((<em>a,b</em>)<em>,</em>4). Your function should handle all characters (alphanumerics, spaces, punctuation, etc). So, for example, the string ’cat, dog’ includes the bigrams ’t,’, ’, ’ and ’ d’. As in the previous subproblem, the dictionary produced by your function should only include pairs that actually appeared in the input, so that the absence of a given key implies that the corresponding two-character string did not appear in the input. Also as in the previous subproblem, you should count upper- and lower-case letters as the same, so that ’GA’ and ’ga’ both count for the same tuple, (<em>g,a</em>).

<h1>4         Tuples as Vectors</h1>

In this problem, we’ll see how we can use tuples to represent vectors. Later in the semester, we’ll see the Python numpy and scipy packages, which provide objects specifically meant to enable matrix and vector operations, but for now tuples are all we have. So, for this problem we will represent a <em>d</em>-dimensional vector by a length-<em>d </em>tuple of floats.

<ol>

 <li>Implement a function called vec_scalar_mult, which takes two arguments: a tuple of numbers (floats and/or integers) t and a number (float or integer) s and returns a tuple of the same length as t, with its entries equal to the entries of t multiplied by s. That is, vec_scalar_mult implements multiplication of a vector by a scalar. Your function should check to make sure that the types of the input are appropriate (e.g., that s is a float or integer), and raise a TypeError with a suitable error message if the types are incorrect. However, your function should gracefully handle the case where the input s is an integer rather than a float, or the case where some or all of the entries of the input tuple are integers rather than floats. <strong>Hint: </strong>you may find it useful for this subproblem and the next few that follow it to implement a function that checks whether or not a given tuple is a “valid” vector (i.e., checks if a variable is a tuple and checks that its entries are all floats and/or integers).</li>

 <li>Implement a function called vec_inner_product which takes two “vectors” (i.e., tuples of floats and/or ints) as its inputs and outputs a float corresponding to the inner product of these two vectors. Recall that the inner product of vectors <em>x,y </em>∈R<em><sup>d </sup></em>is given by. Your function should check whether or not the two inputs are of the correct type (i.e., both tuples), and raise a TypeError if not. Your function should also check whether or not the two inputs agree in their dimension (i.e., length, so that the inner product is well-defined), and raise a ValueError if not.</li>

 <li>It is natural, following the above, to extend our scheme to the case of matrices.Recall that a matrix is simply a box of numbers. If you are not already familiar with matrices, feel free to look them up on Wikipedia or in any linear algebra textbook. We will represent a matrix as a <em>tuple of tuples</em>, i.e., a tuple whose entries are themselves tuples. We will represent an <em>m</em>-by-<em>n </em>matrix as an <em>m</em>-tuple of <em>n</em>-tuples. To be more concrete, suppose that we are representing an <em>m</em>-by-<em>n </em>matrix <em>M </em>as a variable my_mx. Then my_mx will be a length-<em>m </em>tuple of <em>n</em>-tuples, so that the <em>i</em>-th row of the matrix is given (as a vector) by the <em>i</em>-th entry of tuple my_mx.</li>

</ol>

Write a function check_valid_mx that takes a single argument and returns a Boolean, which is True if the given argument is a tuple that validly represents a matrix as described above, and returns False otherwise. A valid matrix will be a tuple of tuples such that

<ul>

 <li>Every element of the tuple is itself a tuple,</li>

 <li>each of these tuples is the same length, and</li>

 <li>every element of each of these tuples is a number (i.e., a float or integer).</li>

</ul>

<ol start="4">

 <li>Write a function mx_vec_mult that takes a matrix (i.e., tuple of tuples) and a vector (i.e., a tuple) as its arguments, and returns a vector (i.e., a tuple of numbers) that is the result of multiplying the given vector by the given matrix. Again, if you are not familiar with matrix-vector multiplication, refer to Wikipedia or any linear algebra textbook. Your function should check that all the supplied arguments are reasonable (e.g., using your function check_valid_mx), and raise an appropriate error if not. <strong>Hint: </strong>you may find it useful to make use of the inner-product function that you defined previously.</li>

</ol>

<h1>5         More Fun with Vectors</h1>

In the previous problem, you implemented matrix and vector operations using tuples to represent vectors. In many applications, it is common to have vectors of dimension in the thousands or millions, but in which only a small fraction of the entries are nonzero. Such vectors are called <em>sparse </em>vectors, and if we tried to represent them as tuples, we would be using thousands of entries just to store zeros, which would quickly get out of hand if we needed to store hundreds or thousands of such vectors.

A reasonable solution is to instead represent a sparse vector (or matrix) by only storing its non-zero entries, with (index, value) pairs. We will take this approach in this problem, and represent vectors as dictionaries with positive integer keys (so we index into our vectors starting from 1, just like in MATLAB and R). A <em>valid </em>sparse vector will be a dictionary that has the properties that (1) all its indices are positive integers, and (2) all its values are floats.

<ol>

 <li>Write a function is_valid_sparse_vector that takes one argument, and returns True if and only if the input is a valid sparse vector, and returns False <strong>Note: </strong>your function should <em>not </em>assume that the input is a dictionary.</li>

 <li>Write a function sparse_inner_product that takes two “sparse vectors” as its inputs, and returns a float that is the value of the inner product of the vectors that the inputs represent. Your function should raise an appropriate error in the event that either of the inputs is not a valid sparse vector.</li>

</ol>

<strong>Note: </strong>This may be your first foray into <em>algorithm design</em>, so here’s something I’d like you to think about: there are several distinct ways to perform this inner product operation, depending on how one chooses to iterate over the entries of the two dictionaries. For this specific problem, it doesn’t much matter which you choose, but there is an important point that you should consider: if the indices of our vectors were sorted, there would be an especially fast way to perform this operation that would require that we look at each entry of the two vectors at most once. Unfortunately, there is no guarantee about order of dictionary keys, so we can’t take advantage of this fact, but we’ll come back to it. You <strong>do not </strong>need to write anything about this, but please give it some thought.

<h1>6         More Fun with Tuples</h1>

In this problem, you’ll do a bit more with tuples.

<ol>

 <li>You may recall that the functions min and max take any (positive) number of arguments, but that sum does not behave similarly. Write a function called my_sum that takes any number of numeric (ints and floats) arguments, and returns the sum of its arguments. Your function should correctly handle the case of zero arguments. You need not perform any error checking for this function. <strong>Reminder: </strong>by convention, an empty sum is taken to be 0.</li>

 <li>Write a function called reverse_tuple that takes a tuple as its only argument and returns a tuple that is the reverse of the input. That is, the output should have as its first entry the last entry of the input, the second entry of the output should be the second-to-last entry of the input, and so on. You need not perform any error checking for this function.</li>

 <li>Write a function called rotate_tuple that takes two arguments: a tuple and an integer, in that order. Letting <em>n </em>be the integer given in the input, your function should return a tuple of the same length as the input tuple, but with its entries “rotated” by <em>n</em>. If <em>n </em>is positive, this should mean to “push forward” all the entries of the input tuple by <em>n </em>entries, with entries that “go off the end” of the tuple being wrapped around to the beginning, so that the <em>i</em>-th entry of the input tuple becomes the (<em>i </em>+ <em>n</em>)-th entry of the output, wrapping around to the beginning of the tuple if this index goes off the end. If <em>n </em>is negative, then this corresponds to rotating the entries in the other direction, with entries of the input tuple being “pushed backward”. Your function should perform error checking to ensure that the inputs are of appropriate types. If the user supplies a non-integer, print a message to alert the user that the input was not as expected, and try to recover by casting it to an integer. <strong>Hint: </strong>a try/catch statement will likely be useful here.</li>

</ol>