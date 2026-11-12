**May.t.s (I take this note form learning Python Free Course by Turing Programming Training Center, If there was something wrong, that was just my fault in taking note back)**



**Programming** is about using instruction for computer to work.



### **Programming language**

\-**Static type** programming language => cannot change the variable type

\-**Dynamic type** programming language => can assign any value type

but in GO programming language, there is **type-referencing** which means that the compiler know the type of the value.



### **Translator**

|Compiler|translate all program before run<br />save in hard-disk => run faster|eg: source code(.C) => compiler => .obj code (non-executable independent code) => linker => .exe file (runnable code - native code)<br /><br />eg: source code(.java) => compiler => .class file => JVM (platform independent => write once run anywhere)|
|-|-|-|
|Interpreter |execute directly byte code<br />save in memory|eg: source code(.py) => Byte code => Interpreter|
|Assembler|translate assembly code to machine code||
|Transpiler|input high level language(high abstraction) => output high level language (low abstraction)|eg: TypeScript => Babel Transpiler => JS|





Byte code = executable ( interpreter/ VM)

Intermediate code = code between source code and machine code that can run on different platform

Native code = machine code that can run on one platform



platform  = environment that program can run

Physical machine = run on CPU ( JVM is not physical machine)

Pragmatics is about knowing how to use the right instruction, where and when to use it.



JIT = Just In Time = not run the whole program while compiling time

AOT = Ahead Of Time = run the whole program while compiling time



Other Combination with Python

* Cython
* Cpython
* Jython (python run on JVM)
* Ironpython



### **AST = Abstract Syntax tree**

* Lexial

  * Token 

    * Prase

      * Prase Tree

        * Prune

          * AST

            * Traverse ( RLr = pre, LRr = in, LrR = post) R = root, L =  left, r = right





### **VM ( Virtual Machine)**

* Stack-based VM
* Register-based VM

|abstract Byte code => VM for window / VM for Linux|
|-|





### **Variable Naming ( letter / underscore)**

|class|upperCarmelCase|
|-|-|
|static|All CAPITAL|
|non-public method|start with single underscore|





### **Operator Precedence order (PEMDAS)**

* Parentheses (P)
* Exponents (E)
* Multiplication (M)
* Division (D)
* Addition (A)
* Subtraction (S)

Type Casting
- Str + Str
- int + int / int('str') + int => for str inside - can have space, bool, base10 but no complex, no float inside
- float + float
#for both (int+int) and (float+float) accept only str/int type
