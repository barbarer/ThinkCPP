Operators for Characters
------------------------

Interestingly, the same mathematical operations that work on integers
also work on characters. For example, observe the following output.

.. activecode:: char_operations_AC_1
   :language: cpp
   :caption: Adding to Characters

   This program performs character addition.  It works by converting
   the character 'a' to ASCII, adding 1 to this value, then converting the
   result from ASCIIs back to a character.
   ~~~~
   #include <iostream>
   using namespace std;

   int main () {
       char letter;
       letter = 'a' + 1;
       cout << letter << endl;
   }

Although it is syntactically legal to multiply characters, it is almost never
useful to do it.

Earlier I said that you can only assign integer values to integer
variables and character values to character variables, but that is not
completely true. In some cases, C++ converts automatically between
types. For example, the following is legal.

.. activecode:: char_operations_AC_2
   :language: cpp
   :caption: Automatic Type Conversion

   This program performs automatic type converstion.  It converts 'a'
   to its ASCII value.
   ~~~~
   #include <iostream>
   using namespace std;

   int main () {
       int number;
       number = 'a';
       cout << number << endl;
   }

The result is 97, which is the number that is used internally by C++ to
represent the letter ’a’. However, it is generally a good idea to treat
characters as characters, and integers as integers, and only convert
from one to the other if there is a good reason.

.. index::
   single: ASCII

.. note::
   Characters in C++ hold **ASCII** values, which range from 0 to 128.  Uppercase
   'A' has an ASCII value of 65, lowercase 'a' has a value of 97, and a space
   has a value of 32.  C++ converts characters to their ASCII values to
   perform automatic type conversion and character arithmetic.


Automatic type conversion is an example of a common problem in designing
a programming language, which is that there is a conflict between
**formalism**, which is the requirement that formal languages should
have simple rules with few exceptions, and **convenience**, which is the
requirement that programming languages be easy to use in practice.

More often than not, convenience wins, which is usually good for expert
programmers, who are spared from rigorous but unwieldy formalism, but
bad for beginning programmers, who are often baffled by the complexity
of the rules and the number of exceptions. In this book I have tried to
simplify things by emphasizing the rules and omitting many of the
exceptions.


.. fillintheblank:: char_operations_1

   What is the value of letter if ``letter = 'c' + 3``?

   - :f: Correct!
     :.*: Try again!


.. parsonsprob:: char_operations_2
   :adaptive:
   :numbered: left

   Construct a main function that uses character operations to generate the output 'r'.
   -----
   int main () {
   =====
    char r;
   =====
    int r; #distractor
   =====
    r = 'p' + 2;
   =====
    r = p + 2; #distractor
   =====
    r = 'p' + 3; #distractor
   =====
    cout << r;
   =====
    cout << "r"; #distractor
   =====
   }
