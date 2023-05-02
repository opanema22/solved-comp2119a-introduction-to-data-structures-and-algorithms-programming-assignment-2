Download Link: https://assignmentchef.com/product/solved-comp2119a-introduction-to-data-structures-and-algorithms-programming-assignment-2
<br>
<strong>[O4]. Implementation</strong>

<strong>[O4] </strong>In this assignment, you are requested write programs to solve two tasks, <strong>A </strong>and <strong>B</strong>.

Your program will be judged by a computer automatically, please follow the exact format. You should read from standard input and write to standard output. e.g, scanf/print,

cin/cout.

<strong>Languages.</strong>

We only accept C/C++ programming languages. Undefined Behavior in C and C++ is not allowed.

<strong>Judging.</strong>

Please note that your solution is automatically judged by a computer.

Solutions that fail to compile or execute get 0 points.

We have designed 20 test cases, 10 for each task. Each test case is 5 points.

The time limit for each test case is 1 second.

<strong>Self Testing.</strong>

You should test your program by yourself using the provided sample input/output file.

The sample input/output is <strong>different </strong>from the ones used to judge your program, and it is designed for you to test your program by your own.

Note that your program should always use standard input/output.

To test your program in Windows:

<ol>

 <li>Compile your program, and get the executable file, “main.exe”</li>

 <li>Put sample input file, “input.txt”, in the same directory as “main.exe”</li>

 <li>Open command line and go to the directory that contains “main.exe” and “input.txt”</li>

 <li>Run “main.exe <em>&lt; </em>txt <em>&gt; </em>myoutput.txt”</li>

 <li>Compare myoutput.txt with sample output file. You may find “fc.exe” tool useful.</li>

 <li>Your output needs to be <strong>exactly </strong>the same as the sample output file.</li>

</ol>

To test your program in Linux or Mac OS X:

<ol>

 <li>Put your source code “main.cpp” and sample input file “input.txt” in the same directory.</li>

 <li>Open a terminal and go to that directory.</li>

 <li>Compile your program by “g++ main.cpp -o main”</li>

 <li>Run your program using the given input file, “./main <em>&lt; </em>txt <em>&gt; </em>myoutput.txt”</li>

 <li>Compare myoutput.txt with sample output file.</li>

 <li>Your output needs to be <strong>exactly </strong>the same as the sample output file.</li>

 <li>You may find the <strong>diff </strong>command useful to help you compare two files. Like “diff -w myOutput.txt sampleOutput.txt”. The −<em>w </em>option ignores all blanks ( SPACE and TAB characters)</li>

</ol>

Note that myoutput.txt file should be <strong>exactly </strong>the same as sample output. Otherwise it will be judged as wrong.

<strong>Submission.</strong>

Please submit your source files through moodle.

You should submit two source files(<strong>without </strong>compression), one for each task.

Please name your files in format UniversityNumber-X.cpp for <em>X </em>in {A, B}, e.g. 1234554321-A.cpp.

<strong>Task A</strong>

Given a binary tree, determine if it is a valid binary search tree (BST).

Assume a BST is defined as follows:

<ul>

 <li>The left subtree of a node contains only nodes with keys strictly <strong>less </strong>than the node’s key.</li>

 <li>The right subtree of a node contains only nodes with keys strictly <strong>greater </strong>than the node’s key.</li>

 <li>Both the left and right subtrees must also be binary search trees.</li>

</ul>

Note: All node values of the tree are positive integers. We use ‘0’ to stand for ‘NULL’.

You can define a binary tree according to the following:

<em>// Definition for a binary tree node. </em>struct TreeNode { int val; TreeNode *left;

TreeNode *right;

TreeNode(int x) : val(x), left(NULL), right(NULL) {}

};

<strong>Input:</strong>

The input contains two lines:

The first line is an integer <em>n</em>, which is the number of integers in the second line. <em>n </em>= 2<em><sup>r </sup></em>− 1<em>,</em>1 ≤ <em>r </em>≤ 20<em>.</em>

The second line are <em>n </em>non-negative integers, standing for nodes of the tree. (You are required to input the node by layer, at each layer, from left to right.)

Note: All nodes are positive integers, and less than 2<sup>31</sup>. You may assume the input always forms a complete binary tree. (0’s mean the tree nodes do not exist.) <strong>Output:</strong>

If the input is a valid BST, output ‘true’; Otherwise, output ‘false’.

<strong>Examples:</strong>

<ol>

 <li>2

  <ul>

   <li>3</li>

  </ul></li>

</ol>

Input:

3

<ul>

 <li>1 3</li>

</ul>

Output: true

<ol start="2">

 <li>5</li>

</ol>

1

3     6

Input:

7

5 1 4 0 0 3 6

Output:

false

<ol start="3">

 <li>5</li>

</ol>

1

3     7

Input:

7

5 1 6 0 0 3 7

Output:

false

<strong>Task B</strong>

Implement an AVL tree. You should implement the operations using exactly the same algorithms as we taught in class. Starting from an empty tree, you should apply the operations to the tree one by one. The operations are described below.

<ol>

 <li>A key <em>x </em>is given, and you need to insert it to the AVL tree. You may assume <em>x </em>is not currently in the tree. Here <em>x </em>is an integer, 0 ≤ <em>x </em>≤ 2<sup>31</sup>− 1.</li>

 <li>A key <em>x </em>is given, and you need to delete it from the current tree. You may assume <em>x </em>is currently in the tree. Here <em>x </em>is an integer.</li>

 <li>Given an integer <em>k</em>, output the k-th smallest element in current tree. You may assume <em>k </em>always satisfies <strong>1 </strong><em>≤ k ≤ number of nodes in AVL tree</em>.</li>

</ol>

<strong>Note: </strong>When deleting a node with two children, you should replace it with its immediate successor. Then you can delete that node.

<strong>Notice for Rotation: </strong>Please read the text-book carefully for the conditions of rotation. Below is one of the conditions that you need to be careful. Suppose node <em>r </em>is not balanced, say <em>height</em>(<em>r.left</em>) == <em>height</em>(<em>r.right</em>) − 2. If we have <em>height</em>(<em>r.right.left</em>) == <em>height</em>(<em>r.right.right</em>), then you should only do a single rotation. A double rotation would break the tree in some cases.

<strong>Notice for Storing Height Information </strong>Balance factors can be kept up-to-date by knowing the previous balance factors and the change in height – it is not necessary to know the absolute height, <strong>two bits per node are sufficient</strong>.

<strong>Input:</strong>

The input contains multiple lines. The last line contains the word “END”, which means end of input. You program should exit after reading this line. Except the last line, each line corresponds to an operation.

The format of each line is described as below.

<ol>

 <li>Character ’A’ followed by a space then an integer <em>x</em>. e.g. “A 10”. You should insert the key <em>x </em>into the AVL tree.</li>

 <li>Character ’D’ followed by a space then an integer <em>x</em>. e.g. “D 10”. You should delete the key <em>x </em>from the AVL tree.</li>

 <li>A single character ’M’ followed by a space then an integer <em>k</em>. e.g. “M 1”. You should output the k-th smallest element in the current tree. Output a newline after <strong>each </strong>element.</li>

</ol>

The number of operations in the input is less than 170000.

<strong>Output:</strong>

Output one integer followed by a newline for each KthMin operation. A sample input/output is given below.

<strong>Example:</strong>

Input:

A 10

A 5

A 1

M 1

A 20

A 19

M 4

D 1

M 1

M 2

M 3

M 4

END

Output:

1

19

5

10

19

20