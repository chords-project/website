---
title: Resources
toc: true
weight: 3
---

## Learning Material

### Book: Introduction to Choreographies

<div style="display: inline-flex; flex-wrap: wrap; gap: 0 2rem; align-items: center;">
<img src="/images/itc-cover.webp" alt="Introduction to Choreographies (cover)" width="200" />
<div style="flex: 1 1 300px;">

The book _Introduction to Choreographies_ (Cambridge University Press) is a pedagogical introduction to the principles of choreographic languages, choreographic programming, and their relation to distributed implementations.

[Read more](https://www.fabriziomontesi.com/introduction-to-choreographies/)

</div>
</div>

## Software

### Choral

<div style="display: inline-flex; flex-wrap: wrap; gap: 0 2rem; align-items: center;">
<img src="/images/choral-methodology.png" alt="Programming with Choral" width="300" />
<div style="flex: 1 1 300px;">

[Choral](https://www.choral-lang.org/) is an innovative choreographic programming language that leverages the principles of Object-Oriented Programming (OOP) to enhance the way developers express and implement distributed systems. At its core, Choral introduces a novel data type concept that allows data to be distributed across various participants within a distributed system. This approach redefines choreographic programming by treating choreographies as classes, and their instances as objects that collaboratively manage states and behaviours.

</div>
</div>

One of Choral's standout features is its compiler, which, given a choreography, generates a (decentralised) implementation for each of its participants. These implementations are libraries in pure Java, whose types are under the control of the Choral programmer. This modularity enables developers to seamlessly integrate these libraries into their applications, ensuring correct participation in choreographies. By merging choreographic and object-oriented paradigms, Choral not only simplifies the development of concurrent and distributed software but also enhances the expressivity of choreographic programming with novel features like higher-order choreographies and distributed data structures. This allows for more reusable and flexible choreographies, including the ability to pass objects and parameterize choreographies without central coordination. Overall, Choral represents a significant advancement in making choreographic programming practical and accessible for modern software development.

Learn more by checking the [Choral website](https://www.choral-lang.org/) or by reading [the research article](https://doi.org/10.1145/3632398).

### Ozone

<div style="display: inline-flex; flex-wrap: wrap; gap: 0 2rem; align-items: center;">
<img src="/images/ozone.png" alt="A screenshot from the Ozone article" width="500" />
<div style="flex: 1 1 300px;">

[Ozone](https://github.com/dplyukhin/ozone) is a library that lets programmers safely use Java Futures in Choral code. With Ozone, programmers can write endpoint code that handles requests in parallel or returns values asynchronously.

Learn more by watching [the tutorial](https://www.youtube.com/watch?v=23y1WCdvMX4) or by reading [the research article](https://doi.org/10.4230/LIPIcs.ECOOP.2024.31).

</div>
</div>

<!-- ## Mech -->
