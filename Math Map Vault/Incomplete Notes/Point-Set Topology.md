#point-set_topology

# Point-Set Topology

---

Note: rewrite in terms of familes of sets once that note is added.

Say we have a set $X$. Recall that $\mathcal{P}(X)$ - the power set of $X$ - is the set containing all possible subsets of $X$.

Now suppose that we pick certain elements from $\mathcal{P}(X)$ and put them in a set: we've created a subset of $\mathcal{P}(X)$. This subset, if it meets certain conditions, is called a **topology** on $X$, and the elements of this topology are called "open sets".

Thus a **topology** on $X$ is a set whose elements are subsets of $X$ and which satisfies the following conditions:

- the empty set and the entire set $X$ are open sets
- the intersection of any finite collection of open sets must be an open set
- the union of any finite collection of open sets must be an open set
- the union of any infinite collection of open sets must be an open set

Remember that a set being "open" simply means that it's an element of the topology.

Note that *any* subset of $\mathcal{P}(X)$ which satisfies these conditions is a topology on $X$. So there can be many different topologies on $X$.

Let's look at a few different examples of topologies (we normally use a tau ($\tau$), sometimes with a subscript, to denote topologies) on a sample set $X = \{a, b, c, d\}$. Four of these are valid topologies, but one of them is not; see if you can figure out which set isn't a topology on $X$:

- $\tau_1 = \{\emptyset, X\}$
- $\tau_2 = \mathcal{P}(X)$
- $\tau_3 = \{\emptyset, \{c\}, X\}$
- $\tau_4 = \{\emptyset, \{a\}, \{a, b\}, X\}$
- $\tau_5 = \{\emptyset, \{a\}, \{b\}, \{c\}, \{a, b\}, \{b, c\}, \{a, c\}, X\}$

Let's verify that these are valid topologies.

$\tau_1$ contains the empty set and the entire set as elements, so it meets our first condition. We don't have to worry about infinite collections here because $X$ is a finite set. The union of any collection of open sets (in this case the only open sets are $\emptyset$ and $X$) is also open (because $\emptyset \cup X = X$, and $X \in \tau_1$), and the intersection of any two open sets is also open (because $\emptyset \cap X = \emptyset$, and $\emptyset \in \tau_1$). Thus this is a valid topology. This topology is known as the "indiscrete" or "trivial" topology on $X$.

$\tau_2$ is just equal to the powerset of $X$. $\emptyset, X \in \mathcal{P}(X)$, so our first condition is met, and the union or intersection of any collection of sets in the powerset will also be in the powerset, so it satisfies our requirement that the union or intersection of any collection of open sets must be open. Thus this too is a valid topology. This topology also has a special name: the "discrete" topology on $X$.

$\emptyset, X \in \tau_3$, so it satisfies our first requirement. Now, does every union and intersection of open sets (elements in $\tau_3$) give a new open set? We can quickly check and see that yes, that condition is satisfied. So $\tau_3$ is a valid topology on $X$.

For $\tau_4$ we can see that $\emptyset, X \in \tau_4$, and any intersection or union of open sets is also an open set, so it is a valid topology on $X$.

$\tau_5$ is the set which is not a valid topology. Why? Because although $\emptyset, X \in \tau_5$, every intersection or union of open sets is not an open set. For example, take the two open sets $\{a, b\}$ and $\{c\}$: their intersection is the empty set, which is in $\tau_5$ and is thus an open set; however, their union is the set $\{a, b, c\}$, which is not in $\tau_5$, and is thus not an open set. Since $\{a, b\}, \{c\} \in \tau_5$, but $(\{a, b\} \cup \{c\}) \not\in \tau_5$, $\tau_5$ is not a topology on $X$.

So what's the point of all of this? Among other uses, a main function of a topology is that it allows us to partition the power set of $X$ into four groups: open sets, closed sets, sets which are both open and closed, and sets which are neither open nor closed.

So we know that an open set in $X$ under some topology $\tau_X$ is any element of $\tau_X$ (remember that elements of $\tau_X$ are subsets of $X$). What's a closed set? A closed set is any set obtained by subtracting an open set from the set $X$. So given $U \in \tau_X$, a closed set $C = X - U$. In other words, a closed set is the complement in $X$ of an open set.

So if we look at our topology $\tau_3$ from above, we can see that
- $X - \emptyset = X$
- $X - X = \emptyset$
- $X - \{c\} = \{a, b\}$

So $X$, $\emptyset$, and $\{a, b\}$ are closed sets in $X$ under the topology $\tau_3$. Note that because $\emptyset$ and $X$ are in every topology (by definition), they are both open in every topology; additionally, $X - X = \emptyset$ and $X - \emptyset = X$, so the emptyset and the set $X$ are both closed in every topology. So $\emptyset$ and $X$ are both open and closed in every topology.

Also, notice that while $\{a, b\}$ is a closed set in $\tau_3$, the same exact set is actually open in $\tau_4$. So different topologies on the same set offer us different ways to partition the set.

The elements of $X$ when $X$ has a topology on it are called "points".

If we have a set $X$ and a topology on $X$ $\tau_X$, we can create a tuple $(X, \tau_X)$ which we call a **topological space**.

The cofinite topology is the topology where open sets are every set which is cofinite in $X$. The cocountable topology is the topology where open sets are every set which is cocountable in $X$.



---

<html>
	<center>
		<svg width="200" height="200">
			<circle cx="100" cy="100" r="90" stroke="white" stroke-width="4" fill="none"/>
			<ellipse cx="130" cy="70" rx="65" ry='40' stroke="blue" stroke-width="4" fill="none" transform="rotate(45, 130, 70)" />
			<ellipse cx="70" cy="130" rx="65" ry='40' stroke="red" stroke-width="4" fill="none" transform="rotate(45, 70, 130)"/>
			<text x="25" y="25" fill="white">X</text>
			<text x="130" y="160" fill="red">A</text>
			<text x="60" y="50" fill="blue">B</text>
		</svg>
	</center>
</html>

In this case, $A$ and $B$ are both subsets of $X$, so $A$ and $B$ could be elements of some topology $\tau$ on $X$.

---

Topology allows us to make concepts like limits and continuity be much more rigorous rather than the solely intuitive notions we previously held.

Given a set $X$, $\tau \in P(X)$ is a topology on $X$ if $\emptyset, X \in \tau$ and $\tau$ only contains open sets, and if:

- $A, B \in \tau \implies A \cup B \in \tau$
- $A, B \in \tau \implies A \cap B \in \tau$
- finite and infinite unions are open sets in $\tau$
- finite intersections are open sets in $\tau$
- infinite intersections aren't necessarily open sets in $\tau$

$(X, \tau)$ a topological space.

Sets in $P(X)$ can either be:

- open
- closed
- both
- neither

$S \in X$ is open if $S \in \tau$, $S \in X$ is closed if $X - S \in \tau$.

Trivial topology: $X$ is any set; $\tau = \{\emptyset, X\}$.
$X$ is any set; $\tau = P(X)$

Any subset of $X$ is open if it's the union of an infinite amount of open balls, *or* any subset of $X$ is open if every point inside it has an open ball around it.

Metric space $X$ is Hausdorff if $\forall x', x'' \in X, \exists \epsilon', \epsilon'' > 0, B_{\epsilon'}(x') \cup B_{\epsilon''}(x'') = \emptyset$ in other words given any two elements in $X$, you can make two disjoint open balls around them. Every metric space is Hausdorff.

We can induce topologies on the set which has a metric on it, and those topologies are always Hausdorff. Not *every* topology on the set is Hausdorff however (find how to induce).

Topology is Hausdorff if from any two points we can find disjoint, open sets.

Given $(X, \tau)$, $\tau = \{\emptyset, X\}$, $\tau$ is not Hausdorff because no two elements $x', x'' \in X$ will be in disjoint open sets in $\tau$.

$T_0, T_1, T_2, T_3, T_4$ are degrees of separation, and they are invariant under homeomorphisms.

If $(X, \tau_X)$ and $(Y, \tau_Y)$ are topological spaces, we say $F:X$ -> $Y$ is continuous iff $\forall \gamma \in \tau_Y$, the primage of $\gamma$ is an element of $\tau_X$.

In other words, the preimage of every set in $\tau_Y$ (every open set in the topology) must be open for it to be continuous.

Example: $(X, \tau)$, $X =\{1, 2, \pi\}$, $\tau = \{\emptyset, \{1\}, \{1, 2, \pi\}\}$. $F:$
- 1 -> 2
- 2 -> 1
- $\pi$ -> $\pi$

This is not continuous because the preimage of {1} (which is {2}) is not in $\tau_X$.

Another example: $(X, \tau_X)$ -> $(X, \tau_X)$ is trivially continuous.

Another example: $(X, \tau_X)$ -> $(Y, \tau_Y)$; $\exists a \in Y$; $F: \forall x\in X$ -> $a$. 

![[Pasted image 20210323132125.png]]

For any open set in $Y$ which doesn't contain $a$, the preimage is the null set. For any open set in $Y$ which does contain $a$, the preimage is the whole set $X$ unioned with the null set (so just the set $X$). Because $\tau_X$ must by definition contain $X$ and $\emptyset$, this mapping must be continuous, because all preimages are open sets in $\tau_X$.

A continuous function from $(X, \tau_X)$ -> $(Y, \tau_Y)$ is a homeomorphism if and only if the function is a bijection and has a continuous inverse. A homeomorphism is an equivalence relation.

---