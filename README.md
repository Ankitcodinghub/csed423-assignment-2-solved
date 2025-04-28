# csed423-assignment-2-solved
**TO GET THIS SOLUTION VISIT:** [CSED423 Assignment 2 Solved](https://www.ankitcodinghub.com/product/csed423-for-this-assignment-you-are-going-to-implement-a-syntax-analyzer-or-parser-for-cool-you-will-use-a-parser-generator-called-bison-to-generate-a-parser-and-build-the-ast-the-output-of-your/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;115706&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSED423 Assignment 2 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
For this assignment, you are going to implement a syntax analyzer or parser for Cool. You will use a parser generator called bison to generate a parser and build the AST. The output of your parser will be an abstract syntax tree (AST). You will construct this AST using semantic actions of the parser generator. Please make sure you get familiar with the syntactic structure of Cool, as described in Figure 1 of the Cool reference manual before you start writing a parser. The documentation for bison is available online (link provided on the course website). You will have to consult A Tour of the Cool Support Code as well to manipulate AST

1 Files and Directories

To get started, download and unpack the pa2 directory under Resources from the course website. This directory contains all the files that you will need for this PA. The files you will need to modify are:

• cool.y

This file contains a start towards a parser description for Cool. The declaration section is mostly complete, but you will need to add additional type declarations for new non-terminals you introduce. We have give you names and type declarations for the terminals. The rule section is very incomplete. We have provided some parts of some rules. You should not need to modify this code to get a working solution, but you are welcome to if you like. However, do not assume that any particular rule is complete.

• test good.cl and test bad.cl

These files test a few features of the grammar. You should add tests to ensure that test good.cl exercises every legal construction of the grammar and that test bad.cl exercises as many types of parsing errors as possible in a single file. To build the parser, type

make or make parser

in the directory pa2/src. This will link more files of support code to your directory and compile your skeleton. Your parser needs as input the output of your completed lexer. Use test good.cl or a working Cool program to test your skeleton parser by typing

lexer test good.cl | parser

2 Parser Result

Your semantic actions should build an AST using the Cool support code tree package, whose interface is defined in pa2/include/cool-tree.h. A Tour of the Cool Support Code contains an extensive discussion of the tree package for Cool abstract syntax trees. You will need most of that information to write a working parser. Read the Tour documentation carefully: it contains explanations, caveats, and other details that will help you avoid a number of pitfalls in understanding and using the AST classes.

The root (and only the root) of the AST should be of type program. For programs that parse successfully, the output of parser is a listing of the AST.

For programs that have errors, the output is the error messages of the parser. We have supplied you with an error reporting routine that prints error messages in a standard format; please do not modify it. You should not invoke this routine directly in the semantic actions; bison automatically invokes it when a problem is detected.

Your parser need only work for programs contained in a single file — don’t worry about compiling multiple files.

3 Error Handling

• Similarly, the parser should recover from errors in features (going on to the next feature), a let binding (going on to the next variable), and an expression inside a {…} block.

Do not overly concerned about the line numbers that appear in the error messages your parser generates. If your parser is working correctly, the line number will generally be the line where the error occurred. For erroneous constructs broken across multiple lines, the line number will probably be the last line of the construct.

4 Notes

• You must declare bison “types” for your non-terminals and terminals that have attributes. For example, in the skeleton cool.y is the declaration:

%type &lt;program&gt; program

This declaration says that the non-terminal program has type &lt;program&gt;. The use of the word “type” is misleading here; what it really means is that the attribute for the non-terminal program is stored in the program member of the union declaration in cool.y, which has type Program. By specifying the type

%type &lt;member name&gt; X Y Z …

you instruct bison that the attributes of non-terminals (or terminals) X, Y, and Z have a type appropriate for the member member name of the union.

All the union members and their types have similar names by design. It is a coincidence in the example above that the non-terminal program has the same name as a union member.

It is critical that you declare the correct types for the attributes of grammar symbols; failure to do so virtually guarantees that your parser won’t work. You do not need to declare types for symbols of your grammar that do not have attributes.

5 Testing the Parser

6 What and How to Turn In

You have to turn in the pa2 directory with your modified version of cool.y, test good.cl, and test bad.cl after compressing it with

tar -cvf pa2 [your student id].tar pa2

You can upload the compressed file to the board for assignment submission at the course website. Please do not copy or modify any part of the support code. The provided files are the ones that will be used in the grading process.
