# A tool for checking the word problem in free orthomodular lattices using reachability analysis

We provide a tool for checking the word problem in free orthomodular lattices (FOM) using rechability analysis. The tools is developed in Maude based on two fundamental theorems: (1) the 96 normal forms of two generators and (2) a theorem describing when the distributive laws can be applied in FOM.

## 1. Features
The tool is written in Maude 3.2.1 with the following features:

- formally specifying free orthomodular lattices (FOM)
- formally specifying a theorem describing when the distributive laws can be applied in FOM using rewrite rules.
- formally specifying `96 normal forms` using equations, which are generated automatically in the tool.

## 2. Requirements

The tool is written in Maude 3.2.1 and uses Full-Maude 3.2.1. Hence, users are required to install them by [the following link](https://maude.cs.illinois.edu/w/index.php/Maude_download_and_installation)

## 3. How to use the tool

- Loading the tool in Maude 3.1 with the following command:

`maude FOM.maude`

- Checking the validity of the axiom (Q2) of quasi-implication algebra

`red (a |-> b) |-> (a |-> c) =?= (b |-> a) |-> (b |-> c) in FOM .`

- Checking the validity of the axiom (O2) of ortho-implication algebra

`red p |~> ((q |~> p) |~> r) =?= p |~> r in FOM .`

- Checking the validity of the axiom (O5) of orthomodular implication algebra

`red (((p |~> q) |~> q) |~> r) |~> (p |~> r) =?= top in FOM .`

- Checking the validity of the axiom (O6) of orthomodular implication algebra

`red ((((((((((p |~> q) |~> q) |~> r) |~> r) |~> r) |~> p) |~> p) |~> r) |~> p) |~> p) =?= (((p |~> q) |~> q) |~> r) |~> r in FOM .`

- Checking the validity of the axiom (J4) of Sasaki implication algebra

`red p |-> ((p |-> ((q |-> ((q |-> r) |-> bot)) |-> bot)) |-> bot) =?= r |-> ((r |-> ((p |-> ((p |-> q) |-> bot)) |-> bot)) |-> bot) in FOM .`

- Checking the validity of the axiom (K5) of Dishkant implication algebra

`red (((p |~> q) |~> q) |~> r) |~> r =?= (p |~> ((q |~> r) |~> r)) |~> ((q |~> r) |~> r) in FOM .`

- Checking the validity of the axiom (L6) of relevance implication algebra

`red (((p |->> q) |->> q) |->> r) |->> r =?= (p |->> ((q |->> r) |->> r)) |->> ((q |->> r) |->> r) in FOM .`

## 4. Papers
TBA
