Notational Conventions
======================

This is the apendix B of the TAPL.


1.  Metavariable Names
---------------------

 Text                    | ML         | Beluga    | Usage
-------------------------|------------|-----------|-----------------------------
                         |            |           |
 p, q, r, s, t, u        | s, t       |           | terms
 x, y, z                 | x, y       |           | term variables
 v, w                    | v, w       |           | values
 nv                      | nv         |           | numeric values
 l, j, k                 | l          |           | record/variant field labels
 \mu                     | store      |           | stores
                         |            |           |
 M, N, P, Q, S, T, U, V  | tyS, tyT   |           | types
 A, B, C                 | tyA, tyB   |           | base types
 \Sigma                  |            |           | store typings
 X, Y, Z                 | tyX, tyY   |           | type variables
 K, L                    | kK, kL     |           | kinds
                         |            |           |
 \sigma                  |            |           | substitutions
 \Gamma, \Delta          | ctx        |           | contexts
 \mathcal{J}             |            |           | arbitrary statements
 \mathcal{D}             |            |           | typing derivations
 \mathcal{C}             |            |           | subtyping derivations


2.  Rule Naming Convention
--------------------------

 Prefix                  | Beluga                 | Usage
-------------------------|------------------------|-----------------------------
 B-                      |                        | big-step evaluation
 CT-                     |                        | constraint typing
 E-                      |                        | evaluation
 K-                      |                        | kinding
 M-                      |                        | matching
 P-                      |                        | pattern typing
 Q-                      |                        | type equivalence
 QR-                     |                        | parallel reduction of types
 S-                      |                        | subtyping
 SA-                     |                        | algorithmic subtyping
 T-                      |                        | typing
 TA-                     |                        | algorithmic typing
 XA-                     |                        | exposure


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

There are  a few cases  where these rules  cannot all  be satisfied  at the same
time.  In such cases,  the earlier ones are given priority. (For example, in the
rule T-Proj₁  in Figure 11-5, rule 4  is relaxed:  the type of the subterm t₁ is
T₁×T₂.)  The rules are ignored completely  in a very small  number of cases (for
example,  the record projection rule T-Proj in Figure 11-7) where following them
would yield unacceptably ugly or unreadable results.
