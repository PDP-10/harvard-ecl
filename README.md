# ECL, Eclectic Language or Extensible Computer Language

Tape images from Linköping University's Department of Computer and
Information Science, courtesy of Andreas Johansson. Files were
extracted using `read20 -x -g -b`.

---

Description from the OLD-LANGUAGES.INFO file distributed with TECO
EMACS:

```
ECL: complete programming system

 > Comes from: Harvard
 > Invoke via: 'ecl:ecl', Extension: .ECL (.BIN for compiled modules)
 > System orientation: -10, a little -20 (Tenex, actually)
 > Description (taken from the manual): "The ECL programming system
has been designed as a tool for general applications programming.  Its
emphasis is on providing a powerful linguistic medium and convenient
programming environment for the production of software spanning a
large range of applications areas.  In providing such an environment,
three goals were considered primary: (a) to allow problem-oriented
description of algorithms, data and control over a wide range of
applications areas; (b) to facilitate program construction and
debugging; and (c) to facilitate smooth progression between initial
program construction and the realization of a well-tuned final product.
ECL consists of a programming language, called EL1, and a system
built around this language to realize these goals.  The system allows
on-line interactive construction, testing, and running of programs.
It includes a language-oriented editor, an interpreter, and a fully
compatible compiler.  Utilities include a debugging package, a
source-level frequency profile package, and a source program
formatter..."
 > Debugging: an integral part of the system.
 > References:
   1. "ECL Programmer's Manual", TR 23-74, Center for Research in
       Computing Technology, Harvard University, December 1974.
   2. Wegbreit, "The ECL Programming System", Proc. AFIPS 1971
       FJCC, vol.39.
   3. Wegbreit, "The Treatment of Data Types in EL1", CACM (May 74).
   4. ("The Computer Journal" article by Wegbreit, about closure in
       ECL).

There is no on-line documentation.

Note from RMS:

I was connected with ECL for a while too.  If you imagine Lisp, with
user-defined record and array data types which can be defined at run
time, given an Algolish syntax, you get the idea.

ECL has the right basic idea for how to do data type definitions,
because data types are objects in their own right which can be created
and manipulated at run time.  So a program has a chance of working on
data types which did not exist when the program was written (because
they are part of another program which is also loaded).  This is
essential for writing debuggers, interpreters, etc. in the language
itself.  Unfortunately, ECL fails to make it completely possible to
omit type checking entirely when that is desired, and this must be
programmed around.  It would be easy to fix this.

The Algol-style front end is a bad idea to begin with.  If you can't
adapt to winning Lisp syntax, most Lisp systems come with simple
optional Algol-style syntax front ends which do the same thing that
ECL does, and they can be extended by the user.  ECL's syntax cannot
be.
