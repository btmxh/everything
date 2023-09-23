## random trial, basic event
- **Random trial** (trial) is an action with random outcomes, i.e. one can not forecast the exact outcome. However, one could enumerate all possible outcomes of such trial.

>e.g. Roll a dice: an action
>Take interest in the number of dots on the upper side
>Outcomes: $w_{i}$: "there are $i$ dots on the upper side" for $i\in 1..6$
>=> This is a random trial
>$\Omega=\{ w_{1},w_{2},w_{3},w_{4},w_{5},w_{6} \}$ is the set of all possible outcomes.

The set of all possible outcomes is the **sample space**, denoted as $\Omega$. Every possible outcome, i.e. an element of $\Omega$ is called a **basic event** (sự kiện sơ cấp).

>e.g. Consider the trial "check the life expectancy of a light bulb". Since every real $x\geq 0$ can be its life expectancy, then $\Omega=[0,\infty)$
>(In actuality, $\Omega$ is isomorphic to $[0, \infty)$, since a number can't be an outcome, but rather just the defining factor of the outcome.)

**Event**: An event of a trial is an event whether happens or not depending on the outcome of the trial.
Denoted as uppercase letters $A, B, C, \dots$

Let $A$ be an event, then the basic event $\omega$ is called to be **favorable** for $A$, denoted as $\omega\in A$ iff when $\omega$ is the outcome of the trial then $A$ happens.

If $A$ is an event of the trial, then
- $A$ has an one-to-one correspondence to a subset of $\Omega$, which is also denoted as $A$ for convenience
- The set $A$ contains all favorable basic outcomes of the event $A$

**Impossible event**: An event that could not happen, no matter what the outcome of the trial is, denoted as $\emptyset$

**Definite event**: An event that always happens regardless of the actual outcome of the trial, denoted as $\Omega$

>Because shit notations, we use equality for everything, from mapping events to the corresponding set.

## Relationships and operations of events
**Implication**: $A$ implies $B$, denoted $A\implies B$ or $A\subseteq B$ iff $B$ happens whenever $A$ happens.
**Equivalent**: $A$ and $B$ are equivalent, denoted $A=B$ or $A\iff B$ iff $A$ happens iff $B$ happens.
**Union/Sum** of events $A$ and $B$, denoted $A+B$ or $A\cup B$ is the event that happens iff either $A$ or $B$ happens.
**Intersection/Product** of events $A$ and $B$, denoted $AB$ or $A\cap B$ is the event that happens iff both $A$ and $B$ happen.
**Difference** of events $A$ and $B$, denoted $A\setminus B$, is the event that happens iff $A$ happens and $B$ does not happen.

Event $A$ and $B$ are **mutually exclusive** (xung khắc) if they can't both happen, i.e. $AB=\emptyset$

**Complement** of the event $A$, denoted $\overline A$, is the event that happens iff $A$ doesn't happen.
Then, $A \overline{A}=\emptyset, A+\overline{A}=\Omega$

Events $H_{1},H_{2},\dots,H_{n}$ is a complete group of events iff
- $H_{i}$ and $H_{j}$ are mutually exclusive for all $i\neq j$ (pairwise mutually exclusive, $H_{i}H_{j}=\emptyset$)
- The sum of all events $H_{i}$ is the definite event: $\sum H_{i}=\Omega$
>Note:
>- Each complete set of events correspond to a partition of the sample space.
>- For every outcome of the trial, there exists exactly one $i$ s.t. $H_{i}$ happens.
>- For every event $A$, then $A,\overline {A}$ is a complete group of events.

>e.g. For events $A_{1},A_{2}$, we have $\Omega=\Omega\Omega=(A_{1}+\overline {A_{1}})(A_{2}+\overline {A_{2}})=A_{1}A_{2}+\overline {A_{1}}A_{2}+A_{1}\overline {A_{2}}+\overline {A_{1}}\overline {A_{2}}$
>Then, the group of $A_{1}A_{2},\overline {A_{1}}A_{2},A_{1}\overline {A_{2}},\overline {A_{1}}\overline {A_{2}}$ is actually a complete group of events.



