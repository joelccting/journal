# 離散數學

## Ch06

1. Explain what is __Pigeonhole Principle__.
2. What is __birthday paradox__? Explain how to compute the number of people for which the probability is over $50$%?
3. Prove that for every positive integer, there is a multiple of $n$ is consisted of only 0s and 1s. $\color{red}{\text{This is red.}}$
4. What does __Generalized PHP__ say?

---

1. If there are $k$ holes and $k+1$ or more pigeons, there must be a hole containing at least 2 pigeons. 

2. How many people in a room can be found of the same birthday? Count it by contradiction. $N=23$, much less than expected.

3. See example 4 of section 6.2

4. N objects in k boxes. There will be at least one box containing at least $\lceil \frac{N}{k}\rceil$ objects.
   
   ## Ch03

## Ch05

## Ch01

### 1.6 Rules of Inference

1. What is an argument? What is a valid argument?

2. What is an argument form? What makes an argument form valid?

3. List __rules of inference__.

4. Fallacies
   
        - Fallacy of affirming the conclusion
        - Fallacy of denying the hypothesis

5. Qualified statements

---

1. A sequence of propositions. All but the final proposition are called premises. The last statement is the conclusion. 
   The truth of all its premises implies that 
   the conclusion is true. $(p_1 \land p_2 \land p_3 ... p_n) \rightarrow q$

2. A sequence of compound propositions involving propositional variables. Changes in particular propositions for the propositional variables do not change the form.
   in its premises

3. _My hungry dog ate six cookies rapidly_
   
   1. modus ponens $p \land (p \rightarrow q) \rightarrow q$
   2. modus tollens $\neg q \land (p \rightarrow q) \rightarrow \neg p$
   3. hypothetical syllogism $$(p \rightarrow q) \land (q \rightarrow r) \rightarrow (p \rightarrow r)$$
   4. disjunction syllogism $$\neg p \land (p \lor q) \rightarrow q$$
   5. addition $$p \rightarrow (p \land q)$$
   6. simplification $$p \land q \rightarrow p$$
   7. conjunction $$(p) \land (q) \rightarrow p \land q$$
   8. resolution $$(\neg p \lor q) \land (p \lor r) \rightarrow (q \lor r)$$

4. Universal instantiation
   
   Universal generalization
   
   Existential instantiation
   
   Existential generalization

### 1.4 Predicates and Quantifiers

1. De Morgan's law for qualifiers

---

### 1.3 Propositional Equivalences

1. Define the terms **tautology**, **contradiction**, **contingency**.
2. Define **logical equivalences**
3. What are 10 logical equivalences? *Ninjas dance in airports*

---

1. Compound propositions that are always true; always false; neither.
2. Compound propositions that have the same truth table.
3. Add "laws" at the end
   1. Negation 
      $p \lor \neg p \equiv T$
      $p \land \neg p \equiv F$
      Double negation 
      $\neg \neg p \equiv p$
   2. De Morgan's 
      $\neg (p \land q) \equiv \neg p \lor \neg q$
      $\neg (p \lor q) \equiv \neg p \land \neg q$
      Domination
       $p \lor T \equiv T$
      $p \land F \equiv F$
      Distributive
      $p \lor (q \land r) \equiv (p \lor q) \land (p \lor r)$
      $p \land (q \lor r) \equiv (p \land r) \lor (p \land r)$
   3. Identity
      $p \land T \equiv p$
      $p \lor F \equiv p$
      Idempotent 
      $p \lor p \equiv p$
      $p \land p \equiv p$
   4. Absorption
      $p \lor (p \land q) \equiv p$
      $p \land (p \lor q) \equiv p$
      Associative 
      $p \lor (q \lor r) \equiv (p \lor q) \lor r$
      $p \land (q \land r) \equiv (p \land q) \land r$

### 1.1 Propositional Logic

1. What is **proposition**? What is **propositional variables** or **sentential variables**?
2. Explain what are **atomic** proposition and **compound** propositions.
3. What is **propositional logic** or **propositional calculus**.
4. List logic operators and their precedence
5. Truth value of a proposition.
6. Connective or in English
7. Conditional statement or implication
8. How many ways to express $p \rightarrow q$ in English?
9. Tell the difference among the following 3 conditional statements: The **converse** of $p \rightarrow q$, the **contraposition** of $p \rightarrow q$, the **inverse** of $p \rightarrow q$.
10. How many ways to express $p \iff q$ ?
11. What is **equivalent propositions**?

---

1. A declarative sentence which is either true or false. By declarative, it means it declares a fact. Variables used to represent propositions.
2. Propositions that can not be expressed in simpler propositions. Propositions that are formed by existing propositions and logic operators.
3. The area of logic that deals with propositions.
4. Negation $\neg$, conjunction $\land$, disjunction $\lor$, implication $\rightarrow$, bi-implication $\leftrightarrow$
5. $T$ $F$
6. $q \rightarrow p$, $\neg q \rightarrow \neg p$, $\neg p \rightarrow \neg q$ 
7. 
8. Most noticeable twos are $p$ only if $q$, $q$ unless $\neg p$. 
   1. $q$ provided that $p$
   2. $q$ follows from $p$
   3. $p$ is sufficient for $q$
   4. a sufficient condition for $q$ is $p$
   5. $q$ is necessary for $p$
   6. a necessary condition for $p$ is $q$.
   7. $p$ implies $q$.
   8. If $p$, then $q$
   9. If $p$, $q$
   10. $q$ if $p$
   11. $q$ when(ever) $p$.
9. x
10. The propositions that share the same truth table.

## About this subject

1. What does Discrete Math deal with?

---

1. DAMAC (_Don't ask me about coding_): discrete structure, algorithm thinking, mathematical induction, application and modeling, combinational analysis. D: ch02, 09-13; A: ch03-05; M: ch01, 05; A: ch04, 10-11, 13; C: ch06-08. Google. (2026, March 27). Gemini (Gemini 3 Flash version) [Large language model]
