---
layout: page
title: Lecture 02 - Computational Thinking
permalink: /lec02/
---
# Computational Thinking

## Four pieces of computational thinking
1. Decomposition
2. Pattern Recognition
3. Abstraction
4. Algorithm Design

### Decomposition
Breaking down a big problem into smaller, easier problems.

### Pattern Recognition
Seeing similarities to other problems helps you find the answer.

### Abstraction
Going from the specific to the general.
Why is this important? It gives us **power**!
Instead of solving just your problem, you solve a whole class of problems for
free. This is how all complex software systems work -- it wouldn't be possible
without it.

### Algorithm Design
Algorithms are how we solve problems in computing. Algorithmic thinking is the
ability to express the solution to a problem **precisely** so that the computer
can execute it.

#### Properties of an Algorithm
1. Input/Output: Clearly define what goes in and comes out of the algorithm.
2. Finite: An algorithm must end, not go on forever. Easier to do than you think!
3. Definite: Each step must be defined precisely ('cause computers can't think!)
4. Effective: Each step must make progress towards the solution.
5. General: Solves a class of problems, not just one specific problem.

## Example: Find the Fake

Say we have eight identical looking coins, but one is a fake and weighs one
gram more than the others.  Given that we have a balance scale, how can we
identify the fake in as few measurements as possible?

Let's walk through each of the parts of Computational Thinking to help us solve
this problem.

### Decomposition

This is kind of complicated with so many coins, but let's break it down. What
if we only had two coins to start with? Then things get a lot simpler. We just
weigh each one and whichever is heavier. So the full problem can be broken down
into doing four 1-to-1 weighings.

{: .note }
A lot of problem solving starts with this sort of "wishful thinking". Don't
sleep on this technique, it's really powerful.

### Pattern Recognition

So we know at most we'd have to take four measurements. Can we do better?[^1] We
can see a pattern in our sub-problems, that the four 1-to-1 weighings are a bit
redundant. We could combine those to 2v2 or 4v4[^2]. The heavier group always has
the fake. By recognizing this pattern we've improved to three weighings.

[^1]: You should always be asking this.
[^2]: Repeatedly cutting problems in half to make them easier is one of the most
    important ideas in computer science. You'll learn all about this COSC 220.

### Abstraction

Does our solution work with more coins? Or what if the coins' weight wasn't
different, but their diameter? Do the items need to be coins at all? They could
be diamonds, or counterfeit currency. Our method will still work if we
*abstract* it to situations where we have n identical things with 1 fake, and
some measurement device to tell them apart. Now we can solve all sorts of
problems.

### Algorithm design

So we have the general idea and know how to solve the problem, but we have to
write out the precise steps so that a computer (or weighing robot in this case)
can actually solve the problem. The act of writing the computer code is called
**implementation**.

1. Input: n coins, where n is even[^3].
2. Split the group of coins in half.
3. Put each group on the scale.
4. Keep the group that was heavier, setting aside the lighter group.
5. Repeate steps 1-3 with the heavy group coins until there is one coin left.
6. Output: the remaining coin is the fake.

[^3]: How does the algorithm change if n is odd?
