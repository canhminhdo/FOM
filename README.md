# A tool for checking the word problem in free orthomodular lattices using model checking


## 1. Features
The tool is written in Maude 3.1 with the following features:

- formally specifying free orthomodular lattices
- formally specifying `Foulis-Holland theorem` using rewrite rules
- formally specifying `96 normal forms` using equations, which are generated automatically in our tool.

## 2. How the tool works

We can use the formal specification of free orthomodular lattices with different strategies such as

- (1) `96 normal forms`
- (2) the `Foulis-Holland theorem`
- (3) both `96 normal forms` and the `Foulis-Holland theorem`

(2) is faster than (1) and (3) in most cases, but some cases cannot be solved.
(1) and (3) are still useful to deal with terms that consist of more than two generators.

## 3. How to use the tool

Loading the tool in Maude 3.1 with the following command:

`maude free-orthomodular-lattice.maude`

Checking the validity of Q2 of quasi-implicaiton algebra with different strategies using the following commands:

`red (a |-> b) |-> (a |-> c) =?= (b |-> a) |-> (b |-> c) in FOM-NF .`

`red (a |-> b) |-> (a |-> c) =?= (b |-> a) |-> (b |-> c) in FOM-FH .`

`red (a |-> b) |-> (a |-> c) =?= (b |-> a) |-> (b |-> c) in FOM-FULL .`

where `FOM-NF`, `FOM-FH`, and `FOM-FULL` denote the use of (1), (2), and (3) strategies, respectively.

## 3. Papers
TBA
