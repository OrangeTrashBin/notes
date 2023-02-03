# Random Stuff
- [Random Stuff](#random-stuff)
  - [Proof on dijkstra algorithm's seperation property](#proof-on-dijkstra-algorithms-seperation-property)


## Proof on dijkstra algorithm's seperation property

We want to prove that seperation property of dijkstra algorithm, that if we have:

$$
\mathbb{E}=\{\text{All Nodes Visited}\}\ \ \mathbb{F}=\{\text{All Nodes Reachable but not visited}\}
$$

and

$$
\mathbb{U}=\{\text{All Nodes Not reachable}\}
$$

we want to show that:

$$
\forall \delta:= \mathbf{e} \to \mathbf{u}, \mathbf{e,u} \in \mathbb{E,U}, \exists \mathbf{f} \in \delta, \mathbf{f} \in \mathbb{F}
$$

To achieve such goal, we choose to prove by contradiction, assume that there exists a path $$\delta$$ such that:

$$
\delta = \mathbf{e} \to \mathbf{u}, \mathbf{e,u} \in \mathbb{E,U}, \forall\mathbf{f} \in \mathbf{F}, \mathbf{f} \notin \delta
$$

And assume that $$\mathbb{N}$$ are the set of all states contained in this path:

$$
\mathbb{N} := \{\mathbf{n},\mathbf{n}\in\delta, \mathbf{n} \text{ is node}\}
$$

assume that $$\mathbb{P}$$ are the set of all the direct paths contained in this path:

$$
\mathbb{P} := \{\mathbf{p},\mathbf{p}\in\delta, \mathbf{n} \text{ is a direct path, a.k.a., edge}\}
$$

And therefore we have path $$\epsilon$$ that's directly from some state in $$\mathbb{E}$$ to $$\mathbb{U}$$:

$$
\epsilon := \mathbf{e_1} \to \mathbf{u_1}, \mathbf{e_1,u_1} \in \mathbb{E,U}, |\mathbb{N_\epsilon}|=2, |\mathbb{P_\epsilon}|=1
$$

This indicates that:

$$
\exists \mathbf{p} \in \mathbb{P_\epsilon}, p = \mathbf{e_1} \to \mathbf{u_1}
$$

However, this is not possible because:

$$
\forall \mathbf{n} \leftarrow \mathbf{e_1}, \mathbf{n} \in \mathbb{E}, \mathbf{n} \notin \mathbb{U}
$$

Thus a contradiction has been created and therefore:

$$\forall \delta:= \mathbf{e} \to \mathbf{u}, \mathbf{e,u} \in \mathbb{E,U}, \exists \mathbf{f} \in \delta, \mathbf{f} \in \mathbb{F}$$