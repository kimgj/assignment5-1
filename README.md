#CS 3251: Intermediate Software Design
##Programming Assignment 5-1

##Overview
This assignment will give you a chance to further explore two important C++ features: templates and operator overloading. You are to implement a Vector class (not an STL Vector, but a mathematical Vector) that supports basic mathematical operations. It would be too boring to only implement three dimensional vectors; therefore, the assignment requires templates so that a Vector class can be instantiated for arbitrary sizes.

Unlike the previous assignments, no header files will be provided. It is your responsibility to analyze the sample (by no means comprehensive) driver file and infer the necessary class public interface, which will let you practice software development in a more realistic manner. After all, some clients do not even know what a header file is, but they do know how they want to use your class.

If you are clever about your design, you should be able to reuse a lot of your methods when defining new ones. Also, please note that since we are “passing” the dimension of the vector as a template parameter, no dynamic memory allocation is required. A good example for you to reference is the StackParam2 example from the Templates lecture from earlier in the semester. 

##Necessary Details
toString() – You need to implement a toString() method that returns a human-readable string representation of your vector in order to simplify the testing of your program. Note that if you do not get this method right, many of the tests will fail. Thus, this method should be one of the first methods implemented and tested.

Functors – You are ***not allowed to use any explicit looping constructs*** in your code. This will force you to use the STL algorithms together with user-defined function objects (functors). You are also ***not to use the functors provided by STL***, nor the vector operations provided in <numeric>. You may use functors that you write yourself; these functors may inherit from std::binary_function.  The reference solution uses only two user-defined functors and one custom iterator - it kind of looks like a back_inserter.

Operator overloading – We want to make the use of our class as natural as possible. Therefore, you will be asked to overload several mathematical operators. You should ensure that commutative operators remain commutative in your class.

Template specialization – Most of the methods you are required to write apply to vectors of all dimensions. Cross products, however, only hold meaning in three (and seven) dimensions. This “weird” behavior will give you the opportunity to explore a feature called template specialization (see the Template lecture). Refer to the test file for the desired results.

Documentation – Since you are designing this class from scratch, it is imperative that you comment your code well. Your intentions of what the method is to do, the required inputs, outputs, etc. must be clear and the documentation must follow the course coding standard. 

Note: It is unlikely that you have done an assignment like this before. Please start early and ask questions if you are unsure of anything. Notice that your design will impact the grading of the Structure and Insightful Programming sections of the rubric.

The testing driver and CMakeLists.txt for the assignment are given to you. Additionally, in the _/docs_ directory we have provided a brief vector mathematics tutorial to assist your understanding of how to implement the necessary methods. You may also access the following tutorial that provides more concrete examples of the necessary mathematics: http://tutorial.math.lamar.edu/Classes/LinAlg/EuclideanSpaceIntro.aspx.

All students have the same assignment and there are no extra tasks for graduate students on this assignment.

###REMINDERS:

* Students are not permitted to use Visual Studio or alternate build systems for your programming assignments.  You must use the supplied _CMakeLists.txt_ file.

* Ensure that your name, vunetid, email address, and the honor code appear in the header comments of all files that are to be graded.

* Your programs(s) must compile locally with no warnings or errors.  We will use Travis-CI to test compilation across both GCC and CLang compilers.

* Your program(s) should always have an exit code of 0.  A non-zero exit code is reason to worry and must be corrected for full points.

* All students are required to use the CS 3251 coding standard, available on the course web page and provided to you on the first day of class. Points will be deducted for not following the coding standard.
  
* When submitting the assignment, all files that are provided to you, plus your solution files have been submitted. All files necessary to compile and run your program must reside in the GitHub.com repository.

* All code that you write must conform to the course coding standard.
