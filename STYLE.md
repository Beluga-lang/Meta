Notational Conventions
======================

This is the apendix B of the TAPL.


1.  Metavariable Names
---------------------

 Text                    | ML         | Beluga      | Usage
-------------------------|------------|-------------|-----------------------------
                         |            |             |
 p, q, r, s, t, u        | s, t       | M, N        | terms
 x, y, z                 | x, y       | x, y, z     | term variables
 v, w                    | v, w       | V, W        | values
 nv                      | nv         |             | numeric values
 l, j, k                 | l          |             | record/variant field labels
 `\mu`                   | store      |             | stores
                         |            |             |
 M, N, P, Q, S, T, U, V  | tyS, tyT   | T, S, U     | types
 A, B, C                 | tyA, tyB   | A, B        | base types
 `\Sigma`                |            |             | store typings
 X, Y, Z                 | tyX, tyY   |             | type variables
 K, L                    | kK, kL     | K, L        |  kinds
                         |            |             |
 `\sigma`                |            | #S          | substitutions
 `\Gamma`, `\Delta`      | ctx        | gamma, g, h | contexts
 `\mathcal{J}`           |            |             | arbitrary statements
 `\mathcal{D}`           |            |             | typing derivations
 `\mathcal{C}`           |            |             | subtyping derivations


2.  Rule Naming Convention
--------------------------

 Prefix                  | Beluga (LF / Inductive) | Usage
-------------------------|-------------------------|-----------------------------
 B-                      | b- / B-                 | big-step evaluation
 CT-                     |                         | constraint typing
 E-                      | e- / E-                 | evaluation
 K-                      | k- / K-                 | kinding
 M-                      | m- / M-                 | matching
 P-                      | p- / P-                 | pattern typing
 Q-                      |                         | type equivalence
 QR-                     |                         | parallel reduction of types
 S-                      |                         | subtyping
 SA-                     |                         | algorithmic subtyping
 T-                      | t- / T-                 | typing
 TA-                     | ta- / TA-               | algorithmic typing
 XA-                     |                         | exposure

There are two conventions to name rules in Beluga. If the rule is
defined using LF we take the first convention, if the rule is defined
using an inductive type then the naming convention requires a capital
letter so we use the second option from the table.

3.  Naming and Subscripting Conventions
---------------------------------------

The choice  of  metavariable  names,  numeric subscripts,  and primes  is guided
throughout the book by the following principles:

1. In syntax definitions,  the bare metavariable t is used for all terms,  T for
types, v for values, etc.

2. In typing rules,  the main term  (the one whose type is being calculated)  is
always called t,  and its subterms are named  t₁, t₂, etc.  (Occasionally —e.g.,
in reduction rules— we need names  for subterms  of subterms;  for these  we use
t₁₁, t₁₂, etc.)

3. In evaluation rules,  the whole term being reduced  is called t  and the term
it reduces to is t'.

4. The type of a term t is called T. (Similarly, the type of a subterm t₁ is T₁,
etc.)

5. The same conventions are used when stating and proving theorems,  except that
t  is sometimes  replaced  by s (and T by S or R, etc.)  to avoid  name  clashes
between definitions and theorems.

6. For Beluga code, we use these same guidelines, and we use plain
numbers instead of underscripts. So we will use M1 instead of M₁.

There are  a few cases  where these rules  cannot all  be satisfied  at the same
time.  In such cases,  the earlier ones are given priority. (For example, in the
rule T-Proj₁  in Figure 11-5, rule 4  is relaxed:  the type of the subterm t₁ is
T₁×T₂.)  The rules are ignored completely  in a very small  number of cases (for
example,  the record projection rule T-Proj in Figure 11-7) where following them
would yield unacceptably ugly or unreadable results.

4. Inserting todo notes
-----------------------

There are some commands to instert todo lists that will be rendered in
the document when the draft mode is enabled (Draft mode is enabled
when the option `draft` is passed to to the document class).

Commands:

* `\todo{blah}` : Inserts an orange note with something to be done.
* `\usure{blah}` : Inserts a red to signal for things that the author
  is unsure of.
* `\change{blah}` : Inserts a blue notes to remind the author to
  change somehting.
* `\info{blah}` : Inserts a green note to add some information
  to the text.
* `\improvement{blah}` : Inserts a plum colored note to remember the
   author of a needed improvement.

Additionally, after the table of contents there will be a list of all
the todo notes that still remain in the text. Again, this section will
only appear if the document is generated as a draft.
