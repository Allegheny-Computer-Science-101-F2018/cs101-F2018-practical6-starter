<!---

TASK LIST:

  * Use cp -rf *.* to copy all of the files and directories in this repository
    to the solution repository for this assignment
  * Change into the directory for the starer repository
  * Update the header (e.g., #) to only give the name of the assignment
  * Update the first paragraph to include the commented-out content
  * Change the link in the # Problems section to point to this lab's solution
  * Create the assignment in the GitHub Classroom, noting the URL
  * Test the assignment by accepting it with your own GitHub account
  * Check to ensure that your GitHub repository is created correctly
  * Share the assignment link with all of the students using email or Slack

PROBLEMS?

  * Contact Gregory M. Kapfhammer by email or Slack
  * Raise an issue in the GitHub repository for this assignment

-->

# cs101-F2018-practical6-starter

Designed for use with [GitHub Classroom](https://classroom.github.com/), this
repository contains the starter for Practical 6 in Computer Science 101. Please
note that, on purpose, the provided source code is missing many key variables
and methods and thus it will not compile correctly! You should carefully read
this document and the assignment sheet to learn more about the steps that you
must complete for this assignment. Since the Travis builds for this repository
will initially fail (as evidenced by a red &#x2717; appearing in the commit logs
instead of a green &#x2714;), the programmer is responsible for completing all
of the steps needed to satisfy the requirements for the assignment, thus causing
a &#x2714; to instead appear in the commit logs.

## Introduction

This assignment requires a programmer to implement and test a benchmarking
framework that supports the empirical evaluation of `IterativeFactorial` and
`RecursiveFactorial`. More details about recursive algorithms are provided in
Sections 5.1 through 5.5. You can also learn about experimental studies by
reviewing the content in Sections 4.1 through 4.3. Please note that this
assignment will also require you to read and use Java classes that contain a
test suite. Also, you can learn more about iterative algorithms by reviewing
Section 1.5.2. Finally, the programmer is also responsible for learning how to
run and extend a test suite written in the JUnit testing framework, as explained
in Section 1.9. As verified by
[Checkstyle](https://github.com/checkstyle/checkstyle), the source code for all
of the Java classes must adhere to all of the requirements in the [Google Java
Style Guide](https://google.github.io/styleguide/javaguide.html).

The source code in the submitted Java source code files must also pass
additional tests set by the [GatorGrader
tool](https://github.com/gkapfham/gatorgrader). For instance, GatorGrader will
check to ensure that `Experiment` and `RunCampaign` have `println` statements
that can produce the output from running a campaign of experiments. Gradle will
also run a JUnit test suite that will perform many checks on your implementation
of the Java classes. More details about the GatorGrader checks are included
later in this document and in the assignment sheet.

When you use the `git commit` command to transfer your source code to your
GitHub repository, [Travis CI](https://travis-ci.com/) will initialize a build
of your assignment, checking to see if it meets all of the requirements. If both
your source code and writing meet all of the established requirements, then you
will see a green &#x2714; in the listing of commits in GitHub. If your
submission does not meet the requirements, a red &#x2717; will appear instead.
The instructor will reduce a programmer's grade for this assignment if the red
&#x2717; appears on the last commit in GitHub immediately before the
assignment's due date.

A carefully formatted assignment sheet for this project provides more details
about the steps that a computer scientist should take to complete this
assignment. You can view this assignment sheet by visiting the listing of
laboratories on the course web site.

## Learning

If you have not done so already, please read all of the relevant [GitHub
Guides](https://guides.github.com/) that explain how to use many of the features
that GitHub provides. In particular, please make sure that you have read the
following GitHub guides: [Mastering
Markdown](https://guides.github.com/features/mastering-markdown/), [Hello
World](https://guides.github.com/activities/hello-world/), and [Documenting Your
Projects on GitHub](https://guides.github.com/features/wikis/). Each of these
guides will help you to understand how to use both [GitHub](http://github.com) and
[GitHub Classroom](https://classroom.github.com/).

To do well on this assignment, you should also Section 1.5.2 to learn more about
iteration constructs. You should also review Sections 4.1 to 4.3, focusing on
the content that explains the steps of both an analytical and empirical
evaluation of an algorithm. To learn more about recursion, please read Sections
5.1 through 5.5, focusing on Section 5.1's introduction to recursion, the
different types of recursion that are highlighted in Section 5.3, and the
strategies for designing recursive algorithms in Section 5.4. Please see the
course instructor or one of the teaching assistants or tutors if you have
questions about any of these reading assignments.

## Commands

To get started in using the GatorGrader tool, you can change into the directory
for this assignment and type the command `gradle grade` in your terminal.
Running this command will produce a lot of output that you should carefully
inspect. If the output indicates that GatorGrader judges that there are no
mistakes in the assignment, then this means that your source code and writing
are passing all of the automated baseline checks. However, if the output
indicates that there are mistakes, then you will need to understand what they
are and then try to fix them.

You can also complete several important Java programming tasks by using the
`gradle` tool. For instance, you can compile (i.e., create bytecode from the
program's source code if it is a correct program) the program using the command
`gradle build`. There are also additional commands that you can type:

- `gradle clean`: clean the project of all the derived files
- `gradle check`: check the quality of the code using Checkstyle
- `gradle build`: create the bytecode from the Java source code
- `gradle run`: run the Java program in the command-line
- `gradle cleanTest`: clean the JUnit test suite of derived files
- `gradle test`: run the JUnit test suite and produce report
- `gradle tasks`: display details about the Gradle system

To run one of these commands, you must be in the home directory for this
assignment where the `build.gradle` file is located. Then, you can type the
command in the terminal and study the output.

## Output

When you type the command `gradle run` in the terminal window it should produce
output from running your version of `practicalsix.experiment.Experiment`.
Critically, the output should contain a table with timing values and order of
growth ratios that may be different than what you see on the screen of your
colleague's computer. Finally, please note that this practical assignment
invites you to create and run a JUnit test suite of Java classes in at least two
packages. While this test suite does not produce any output, you should
carefully inspect its tests so that you understand their strategy.

## Checking

In addition to making the checks that are mentioned in the introduction to this
document, your final submission must meet the following requirements.

- practicalsix/Experiment.java:
  - Contains at least two multi-line comments in the JavaDoc standard
  - Contains exactly 8 `println` statements to produce program output
  - Runs correctly without crashing or producing an error

- practicalsix/RunCampaign.java:
  - Contains at least four multi-line comments in the JavaDoc standard
  - Contains exactly 3 `println` statements to produce program output

- practicalsix/TestArithmeticComputations.java:
  - Contains at least one multi-line comment in the JavaDoc standard
  - Contains exactly six passing test cases designated with the `@Test` marker

- GitHub repository:
  - Contains Java source code that passes all of the provided JUnit tests
  - Contains five commits beyond the repository's starting number of commits

Please note that a primary objective for this practical assignment is for each
student to practice creating their own Java classes and JUnit test cases. As
such, you should carefully review the source code from prior assignments so as
to ensure that you can correctly add to the required `IterativeFactorial` and
`RecursiveFactorial` classes and several test cases in the
`TestArithmeticComputations` JUnit test suite. You should also review the source
code from previous assignments that showed you how to create and run a campaign
of experiments.

## Updates

If the course instructor updates the provided material for this assignment and
you would like to receive these updates, then you can type this command in the
main directory for this assignment:

```
git remote add download git@github.com:Allegheny-Computer-Science-101-F2018/cs101-F2018-lab4-starter.git
```

You should only need to type this command once; typing the command additional
times may yield an error message but will not negatively influence the state of
your repository. Now, you are ready to download the updates provided by the
course instructor by typing:

```
git pull download master
```

This second command can be run whenever the course instructor needs to provide
you with new source code for this assignment. However, please note that, if you
have edited the files that the course instructor updated, running the previous
command may lead to Git merge conflicts. If this happens, you may need to
manually resolve them with the help of the instructor or a teaching assistant.

## Travis

This assignment uses [Travis CI](https://travis-ci.com/) to automatically run
the checking programs every time you commit to your GitHub repository. The
checking will start as soon as you have accepted the assignment, thus creating
your own private repository, and the course instructor enables Travis for it. If
you are using Travis for the first time, you will need to authorize Travis CI to
access the private repositories that you created on GitHub.

## Requirements

The GatorGrader software that supports the checking of this assignment was
developed for the following software and versions:

- Gradle 4.6
- Java 1.8.0
- JUnit 4.9.0
- MDL 0.4.0
- Proselint 0.8.0
- Python 3.6

## Problems

If you have found a problem with this assignment's provided source code, then
you can go to the [Computer Science 101 Practical 6
starter](https://github.com/Allegheny-Computer-Science-101-F2018/cs101-F2018-practical6-starter)
repository and create an issue by clicking the "Issues" tab and then clicking
the green "New Issue" button. If you have found a problem with the [GatorGrader
tool](https://github.com/gkapfham/gatorgrader) and the way that it checks you
assignment, then you can follow the aforementioned steps to create an issue in
its repository. To ensure that your issue is properly resolved, please provide
as many details as is possible about the problem that you experienced. If you
discover a problem with the practical assignment sheet, then please raise an
issue in the
[cs101-F2018-sheets](https://github.com/Allegheny-Computer-Science-101-F2018/cs101-F2018-sheets)
repository and mention this assignment.

Students who find, and use the appropriate GitHub issue tracker to correctly
document, a mistake in any aspect of this practical assignment will receive free
laptop stickers and extra credit towards their grade for it.

## Assistance

If you are having trouble completing any part of this project, then please talk
with either the course instructor or a teaching assistant during the practical
session. Alternatively, you may ask questions in the Slack team for this course.
Finally, you can schedule a meeting during the course instructor's office hours.
