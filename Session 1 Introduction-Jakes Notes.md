To define a programming language, we define three things:
1: Grammar
2: Equivalences
3: Reductions

Grammar gives us a way to say what is or is not a valid program construction:
  - (P|Q is defined in the Pi Calc, but P*Q has no meaning)
  - See Context Free Grammars

Equivalences give us a way to fix the fact that our grammar is usually "too fined grained" to express our meaning fully:
  - (When we say P|Q, in Pi Calc, we want the "|" to mean "run concurrently with", and have Q|P be another way to say the same thing.)
  - these are defined using bi-directional rewrite rules. we can use these patterns to transform the term of our program without changing the computation that the program performs.

Reductions are what define our meaning of computation. Reductions are expressed as uni-directional rewrite rules.
  - once this pattern is applied to a term, the term "forgets" it's previous form.

-------

Lambda Calculus' term reduction (beta reduction) encodes computation into the idea of applying a function to arguments.

In Milner's paper, "Functions as Processes" Milner gives an expression of the lambda calculus from within the Pi Calculus.

-------

Charles Bennet's work on the Maxwell's Demon problem gives us a perspective on computation: namely that there are entropic or thermodynamic consequenses of compute. Reinforces this idea that uni-directional rewrite or computation entangles this notion of forgetting. 

-------

Category theory has notions that can be mapped to the three things needed to define a programing language:

In the Universal Algebra
 -(which contains things like monoids, groups, rings, fields, linear algebra)
 Grammar:
 - We have generators which are a sort of impovrished grammar consisting of atomic elements. (like the Set atomic element for monoids)
 - our "grammatical rules" consist of concatenation of these elements
 Equivalences:
 - We have associativity relations
 Reductions:
 - These atomic elements don't reduce themselves, our notion of movement in the Universal Algebra is encoded into maps or functions which define relations between elements giving us the dynamics of categories.

-------

A TODO given to us: look up the basic definitions of a category in category theory

-------

Though the shapes of the theory of computation can be found in Category Theory, the two still do not play nicely.

The tension lies in the dynamics of the process elements:
  Cat Theory puts these in structure preserving maps
  Computing puts these in uni-directional, structure forgetting, rewrite rules

???Okay, Greg loses me a bit here, because why must these maps be structure preserving, couldn't we use functions that don't have an inverse, why must these functions be "structure preserving"? (I know next to nothing about Cat Theory)

-------

Not knowing how to "preserve the rewrite rules" prevents category theory and computation theory from being unified.

???I don't know what "preserve the rewrite rules" means. Maybe this was mis-spoken (or mis-heard), in that the difficulty isn't preserving the rewrite rules themselves, but encoding the rewrite rules and deciding via that encoding how much of the original term structure should be preserved when the rewrite happens.

-------

Though the theories aren't unified, you can still push the Pi Calc or other computational frameowrks into Category theory:

See Milner's work on Bigraphs and mobile processes.

You can create a category containing different pi calcs (this might be what the Bigraph work is about?? It was unclear to me)

Things get difficult when pushing comp theory stuff into cat theory because you need to decide what to structures of the original "process" or element you need to preserve when your rewrite rules are applied.

Greg and Mike wrote a paper giving the Categorical semantics of the pi calculus and it was a PITA in terms of how much Advanced Cat theory had to be employed (the PITA part is my interpretation, I'm sure Greg and Mike had fun).

I believe the paper is titled Higher category models of the pi-calculus
