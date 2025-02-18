---
layout: page
title: A list of problems
description:
background: '/img/maths_background.png'
mathjax: true
--- 

The problems here are ones that we would eventually like to be able to solve fully automatically. In that respect, they vary considerably in their difficulty, so they are annotated in such a way that we can get a clearer idea of what we will need to do in order to have a realistic chance of solving which problems. Some of the problems also come with links to detailed discussions of how a program might be expected to solve them. The problems in this list are not stated formally, but it should be clear to an experienced mathematician what formal statement is intended in each case. Eventually we would like to create a useful set of benchmark problems against which we can measure our progress. We are not close to that yet: so far, the list is very preliminary.

<h3>Topological spaces.</h3>

A union of two compact sets is compact. <em>[Requires creating an open cover]</em>

A compact subset of a Hausdorff topological space is closed. <em>[Requires creating an open cover. A number of other difficulties, but they seem more technical than conceptual.]</em>

A continuous image of a compact set is compact. <em>[Requires creating an open cover]</em>

A closed subset of a compact set is compact. <em>[Requires creating an open cover]</em>

A composition of continuous functions is continuous. <em>[Very routine -- could be solved easily by ROBOT]</em>

$\overline{\overline{A}}=\overline{A}$ for every set $A$. <em>[Should be routine. Good test problem. Involves library reasoning.]</em>

If $f(\overline{A})\subset\overline{f(A)}$ for every $A$ then $f$ is continuous. <em>[Routine but a bit tricky. Good test problem. Involves library reasoning.]</em>

If $f$ is continuous then $f(\overline{A})\subset\overline{f(A)}$ for every $A$. <em>[Routine but a bit tricky. Good test problem.]</em>

If $f$ is continuous then for every neighbourhood $N$ of $f(x)$ there is a neighbourhood $M$ of $x$ such that $f(M)\subset N$. <em>[Should be routine. Good test problem.]</em>

If for every $x$ and for every neighbourhood $N$ of $f(x)$ there is a neighbourhood $M$ of $x$ such that $f(M)\subset N$, then $f$ is continuous. <em>[Should be routine. Good test problem.]</em>

A continuous bijection from a compact space to a Hausdorff space is a homeomorphism. <em>[Hard to do from first principles, but a good test of library-reasoning capabilities if the program is allowed to use facts such as that a continuous image of a compact set is compact or that a compact subset of a Hausdorff space is closed.]</em>

<h3>Metric spaces.</h3>

A metric space is Hausdorff. <em>[Requires building two open sets. Just beyond ROBOT's capabilities, so good target problem.]</em>

The intersection of two open sets is open. <em>[Routine -- could be solved by ROBOT]</em>

A union of open sets is open. <em>[Routine but requires splitting into cases, so a good test problem for technical reasons.]</em>

If f is continuous and $a_n\to a$ then $f(a_n)\to f(a)$ (where f is a function between metric spaces). <em>[Routine -- could be solved by ROBOT]</em>

If $f(a_n)\to f(a)$ whenever $a_n\to a$ then f is continuous. <em>[Requires building a sequence. Raises interesting issues. Good target problem.]</em>

If f is continuous and $U$ is open then $f^{-1}(U)$ is open. <em>[Routine -- could be solved by ROBOT]</em>

If $f^{-1}(U)$ is open whenever U is open then f is continuous. <em>[Requires creating an open set. Good target problem.]</em>

A uniform limit of continuous functions is continuous. <em>[Beyond what Robot could do, but should be feasible with a bit of help from subtasks and other ideas. An important target problem.]</em>

A sequence (in a metric space) has at most one limit. <em>[Requires choosing an $\epsilon$ to be half the distance between two putative distinct limits. Should be doable with metavariables, and otherwise straightforward, so good target problem.]</em>

A continuous function on a sequentially compact metric space is bounded. <em>[Requires creating a suitable sequence if the function isn't bounded. Raises interesting issues, so good target problem.]</em>

Every sequentially compact metric space is complete. <em>[Routine but slightly tricky, so good target problem.]</em>

A composition of continuous functions is continuous. <em>[Very routine -- I think ROBOT could do this easily.]</em>

Every closed set contains its limit points. <em>[Very routine -- I would expect ROBOT to be able to do this.]</em>

Every set that contains all its limit points is closed. <em>[Requires creating a sequence and use of the Archimedean axiom, so an interesting target problem.]</em>

If X is compact and $f:X\to X$ is a map such that $d(f(x),f(y)) < d(x,y)$ whenever $x\ne y,$ then $f$ has a fixed point. <em>[This has a short and natural proof, but you have to do the right thing at each stage. It would be wonderful if without cheating we could get a fully automatic program to solve this problem.]</em>

Open balls are open. <em>[This requires a slightly tricky choice for the radius of a ball around a point in the open ball. Should be OK with metavariables, but some technical issues concerning dependencies, so a good test problem to check that the program is good on how variables depend on each other.]</em>

<h3>Sets and functions.</h3>

$f^{-1}(A\cup B)\subset f^{-1}(A)\cup f^{-1}(B).$ <em>[Very routine. Should be easily solvable by ROBOT.]</em>

$f(f^{-1}(B))\subset B.$ <em>[Very routine. Should be easily solvable by ROBOT.]</em>

$A\subset f^{-1}(f(A)).$ <em>[Very routine. Should be easily solvable by ROBOT.]</em>

If $f$ is an injection, then $f(A\cap B)=f(A)\cap f(B)$. <em>[Easy, but good test problem to see whether a system can handle equality in a satisfactory way.]</em>

An injection from a non-empty set has a left inverse. <em>[Involves the tricky issue that the left inverse needs to be defined everywhere, even if lots of values don't matter. So a good test problem and possibly hard to solve without cheating.]</em>

A surjection has a right inverse. <em>[Uses choice, so opens up quite a big can of worms. But maybe useful for that reason, particularly if our focus is on "classical" proofs.]</em>

$A\cap(B\cup C)=(A\cap B)\cup(A\cap C)$. <em>[Requires splitting into cases, so good test problem for technical reasons.]</em>

$(A\cap B)^c=A^c\cup B^c$. <em>[Requires splitting into cases, so good test problem for technical reasons.]</em>

<h3>Sequences and series.</h3>

A sequence that is unbounded above has a subsequence that tends to infinity. <em>[Requires building a sequence. Involves induction. This would be quite an ambitious target, though the sort of problem we'll need a system to be able to solve easily if it's going to be able to do even moderately interesting constructions in analysis.]</em>

A sequence of non-negative real numbers that tends to zero has a subsequence that sums to at most 1. <em>[Involves some of the challenges of the previous problem, as well as that of coming up with the idea of getting the $k$th term of the subsequence to be at most $2^{-k}$ (or something similar).]</em>

<h3>Groups.</h3>

Lagrange's theorem. <em>[Probably hard for a fully automatic prover. But one could start with a motivated proof and take things from there.]</em>

The kernel of a homomorphism is a normal subgroup. <em>[Should be pretty easy.]</em>
  
A normal subgroup is the kernel of a homomorphism. <em>[A lot harder, as it involves constructing the quotient group.]</em>

If $ab=ac$ then $b=c$. <em>[A good test of subtasks.]</em>

If $a^2=e$ for every element $a$, then $G$ is Abelian. <em>[Another good test of subtasks, but also of mixing equality with logic.]</em>

$(ab)^{-1}=b^{-1}a^{-1}$. <em>[Another good subtasks exercise]</em>

A normal subgroup of a normal subgroup need not be normal. <em>[A good test for an existence solver.]</em>

A normal subgroup is a union of conjugacy classes. <em>[Should be easy.]</em>

Every finite group is a subgroup of some permutation group $S_n$. <em>[I would hope that this would be easy, but I'm not absolutely sure.]</em>

Two permutations are conjugate in $S_n$ if and only if they have the same cycle type. <em>[I would hope that the only if direction was easy. The if direction could be quite a bit more complicated.]</em>

$A_4$ has no subgroup of index 2. <em>[This needs quite a lot of library reasoning -- to spot that such a subgroup would have to be normal, to see then that it would have to be a union of conjugacy classes, and to work out that it's not possible to find conjugacy classes (including $\\\{e\\\}$) with sizes adding up to 6. Part of this would require showing that the 4-cycles form two conjugacy classes, each of size 3, unless this too could be appealed to as a library result.]</em>

The orbit-stabilizer theorem. <em>[This is a rather good example of a proof that is essentially routine but is found hard by beginners. So it would be a very good test problem for any algebraic reasoner.]</em>

<h3>Fields</h3>

Using just the field axioms, prove that $0x=0$ for every $x$. <em>[Tricky for beginning undergraduates, so likely to be tricky for a non-cheating program.]</em>

Using just the field axioms, prove that $(-x)(-y)=xy$ for every $x$ and $y$. <em>[Similar.]</em>

Prove that $\mathbb Q(\sqrt 2)$ is a field. <em>[The question here is how a program would discover the trick of multiplying numerator and denominator by the conjugate of the denominator.]</em>

Prove that left distributivity implies right distributivity. <em>[This should be a fairly easy question for a subtasks-based algorithm.]</em>

Prove that if $xy=0$ then $x=0$ or $y=0$. <em>[The proof is easy, but this might be slightly tricky for a program, as it involves splitting into cases -- though the cases are obvious. Here I assume that it's allowed to use the result that anything multiplied by 0 gives 0.]</em>

Define $n.1$ inductively by $0.1=0$ and $(n+1).1=n.1 + 1$ (where $n\in\mathbb N$ and the 1 on the right-hand side of the multiplication is the multiplicative identity element of the field). Suppose that there is a positive integer $n$ such that $n.1=0$. Prove that $n.x=0$ for every element $x$ of the field (defined in a similar way). Prove also that the minimal such $n$ is a prime. <em>[It might be a little bit tricky even to formulate these problems in a nice way. The proofs could be quite hard given the inductive definitions of $n.1$ and $n.x$ and the fact that one has to mix elementary number theory with the algebra.]</em>

<h3>Enumerative combinatorics</h3>

<em>This whole area is well out of reach of the approaches we have developed so far, so seems ripe for exploration.</em>

Let $X$ be a set of size $m$ and let $Y$ be a set of size $n$. Prove that the number of functions from $X$ to $Y$ is $n^m$. <em>[This is a trivial problem for an experienced mathematician, but presents a challenge to a program, as a formal proof looks somewhat different from the kind of "for each $x\in X$ we have $n$ choices for $f(x)$" type argument we might be inclined to give in a human context. The problem is harder still if it simply asks how many functions there are from $X$ to $Y$.]</em> 

The number of subsets of size $m$ of a set of size $n$ is $n!/m!(n-m)!$. <em>[This could be a hard problem, as the idea is needed of doing a double count of the number of permutations instead of going directly for combinations.]</em>
