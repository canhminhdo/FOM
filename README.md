# A tool for checking the word problem in free orthomodular lattices using model checking

## 1. Features
The tool is written in Maude 3.2.1 with the following features:

- formally specifying free orthomodular lattices
- formally specifying `Foulis-Holland theorem` using rewrite rules
- formally specifying `96 normal forms` using equations, which are generated automatically in our tool.

## 2. Requirements

The tool is written in Maude 3.2.1 and uses Full-Maude 3.2.1. Hence, users are required to install them by [the following link](https://maude.cs.illinois.edu/w/index.php/Maude_download_and_installation)

## 3. The use of strategies

We can use the formal specification of free orthomodular lattices with different strategies such as

- (1) `96 normal forms`
- (2) the `Foulis-Holland theorem`
- (3) both `96 normal forms` and the `Foulis-Holland theorem`

(2) is faster than (1) and (3) in most cases, but some cases cannot be solved.
(1) and (3) are still useful to deal with terms that consist of more than two generators.

## 4. How to use the tool

- Loading the tool in Maude 3.1 with the following command:

`maude free-orthomodular-lattice.maude`

- Checking the validity of the axiom (Q2) of quasi-implication algebra with different strategies using the following commands:

`red (a |-> b) |-> (a |-> c) =?= (b |-> a) |-> (b |-> c) in FOM-NF .`

`red (a |-> b) |-> (a |-> c) =?= (b |-> a) |-> (b |-> c) in FOM-FH .`

`red (a |-> b) |-> (a |-> c) =?= (b |-> a) |-> (b |-> c) in FOM-FULL .`

where `FOM-NF`, `FOM-FH`, and `FOM-FULL` denote the use of (1), (2), and (3) strategies, respectively.

- Checking the validity of the axiom (O2) of ortho-implication algebra

`red p |~> ((q |~> p) |~> r) =?= p |~> r in FOM-NF .`

`red p |~> ((q |~> p) |~> r) =?= p |~> r in FOM-FH .`

`red p |~> ((q |~> p) |~> r) =?= p |~> r in FOM-FULL .`

- Checking the validity of the axiom (O5) of orthomodular implication algebra

`red (((p |~> q) |~> q) |~> r) |~> (p |~> r) =?= top in FOM-NF .`

`red (((p |~> q) |~> q) |~> r) |~> (p |~> r) =?= top in FOM-FH .`

`red (((p |~> q) |~> q) |~> r) |~> (p |~> r) =?= top in FOM-FULL .`

- Checking the validity of the axiom (O6) of orthomodular implication algebra

`red ((((((((((p |~> q) |~> q) |~> r) |~> r) |~> r) |~> p) |~> p) |~> r) |~> p) |~> p) =?= (((p |~> q) |~> q) |~> r) |~> r in FOM-NF .`

`red ((((((((((p |~> q) |~> q) |~> r) |~> r) |~> r) |~> p) |~> p) |~> r) |~> p) |~> p) =?= (((p |~> q) |~> q) |~> r) |~> r in FOM-FH .`

`red ((((((((((p |~> q) |~> q) |~> r) |~> r) |~> r) |~> p) |~> p) |~> r) |~> p) |~> p) =?= (((p |~> q) |~> q) |~> r) |~> r in FOM-FULL .`

- Checking the validity of the axiom (J4) of Sasaki implication algebra

`red p |-> ((p |-> ((q |-> ((q |-> r) |-> bot)) |-> bot)) |-> bot) =?= r |-> ((r |-> ((p |-> ((p |-> q) |-> bot)) |-> bot)) |-> bot) in FOM-NF .`

`red p |-> ((p |-> ((q |-> ((q |-> r) |-> bot)) |-> bot)) |-> bot) =?= r |-> ((r |-> ((p |-> ((p |-> q) |-> bot)) |-> bot)) |-> bot) in FOM-FH .`

`red p |-> ((p |-> ((q |-> ((q |-> r) |-> bot)) |-> bot)) |-> bot) =?= r |-> ((r |-> ((p |-> ((p |-> q) |-> bot)) |-> bot)) |-> bot) in FOM-FULL .`

- Checking the validity of the axiom (K5) of Dishkant implication algebra

`red (((p |~> q) |~> q) |~> r) |~> r =?= (p |~> ((q |~> r) |~> r)) |~> ((q |~> r) |~> r) in FOM-NF .`

`red (((p |~> q) |~> q) |~> r) |~> r =?= (p |~> ((q |~> r) |~> r)) |~> ((q |~> r) |~> r) in FOM-FH .`

`red (((p |~> q) |~> q) |~> r) |~> r =?= (p |~> ((q |~> r) |~> r)) |~> ((q |~> r) |~> r) in FOM-FULL .`

- Checking the validity of the axiom (L6) of relevance implication algebra

`red (((p |->> q) |->> q) |->> r) |->> r =?= (p |->> ((q |->> r) |->> r)) |->> ((q |->> r) |->> r) in FOM-NF .`

`red (((p |->> q) |->> q) |->> r) |->> r =?= (p |->> ((q |->> r) |->> r)) |->> ((q |->> r) |->> r) in FOM-FH .`

`red (((p |->> q) |->> q) |->> r) |->> r =?= (p |->> ((q |->> r) |->> r)) |->> ((q |->> r) |->> r) in FOM-FULL .`

## 5. Papers
TBA
