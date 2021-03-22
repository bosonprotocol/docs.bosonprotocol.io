---
layout: docs
title: "Boson Protocol: Docs: Advanced Topics: Research"
short_title: "Research"
permalink: /advanced-topics/research/
---

# Research

## Linear programming formulation

We specify conditions leading to a desired subgame-perfect equilibrium solution.
The main idea is to have a solution that corresponds to the right play. That is,
subgame-perfect equilibrium moves -- optimal rational moves -- are the same as
honest moves.

Each decision at each _internal_ node of the decision tree gives a linear
constraint on the variable set $$T$$. These are so-called _incentive
compatibility constraints_. There are also _budget-balance constraints_ for each
final state, namely that $$t^s_S+t^s_B\leq D_S+D_B+p$$. Verbally it means that
the mechanism can not add any money into the contract, but it can burn money.

Feasible linear programs normally have more than $$1$$ solution. To pin down the
solution set to one, we need to come up with the objective function. The first
candidate is to minimize the sum of deposits. The friction coming from putting
deposits has to be acknowledged. The obvious cost of putting high deposits for
any (especially long) time period is opportunity cost. Depositing involves an
implicit cost for the participants in the smart contract: This can be the
opportunity cost of not using the deposit while the contract is executed,
borrowing costs of the agent, risk of loss of the deposit if the consensus
protocol fails, etc. In general, mechanisms that use punishment through huge
negative transfers in case of "misbehavior" of agents are impractical. Even
though the punishments are only executed off the equilibrium path, huge deposits
have to be made to make the threat of punishment credible. This would make such
mechanisms very costly to implement as a smart contract. Therefore, minimizing
the sum of deposits can be an objective function. Opportunity cost in smart
contracts and subgame perfect equilibria is a topic of Mamageishvili and
Schlegel (2020). With instant exchange procedures, however, the opportunity cost
is not of first-order importance.

An alternative objective function could be to maximize the money burnt
(transferred to the Boson protocol) off-equilibrium path. The transferred money
could be used to analyze what went wrong in this particular game. This incentive
for network nodes can be useful in the early stages of protocol functioning.

In the first move of the seller, H corresponds to sending a high-quality item,
while L corresponds to sending a low-quality item. In the second move, the buyer
plays either redeem (R) or no redeem (refund or expire - RfE). In the third
move, the buyer complains (C) or does not complain (NC). Finally, the seller
acknowledges a fault (CF) or does not acknowledge the fault (NC).

Suppose the seller is deciding the root vertex S. Then the example incentive
compatibility constraint at the vertex $$S$$ is the following:

$$t*{S_8}^S + u^S*{H, R, NC,NC} \geq t*{S_1}^S + u^S*{L,RfE,C,CF}$$

where $$u^X_{p}$$ denotes the utility of player $$X\in \{S,B\}$$ when the
mechanism takes path $$p$$ from the root to (any) leaf.

We consider quasi-linear utilities. That is, utility of the path for a player
$$X\in \{S,B\}$$ in the decision tree is the sum of utilities of each move.
Formally, $$u_p^{X}=u_{e_1}+\cdots+u_{e_n}$$, where $$p$$ is a path consisting
of edges $$p=\{e_1,\cdots, e_n\}$$.

There are $$15$$ internal nodes of the decision tree. Each node generates one
incentive compatibility constraint of the linear program. Each final state adds
$$1$$ constraint. There are $$2$$ additional _individual rationality_
constraints, $$1$$ for each player. In the subgame-perfect equilibrium solution,
the expected payoff of the player should be non-negative. In other words, any
player may opt-out for not participating in the contract. In total, there are
$$15+8+2=25$$ constraints and $$8$$ (transfer) variables. Optimizing target
function given these constraints determines the values of transfers, and
consequently, smart contract.

[decision_tree.pdf](https://github.com/bosonprotocol/docs.bosonprotocol.io/files/6164651/decision_tree.pdf)

## Discussion

Subgame-perfect implementation can be used with machine-to-machine commerce
since it avoids the behavioral play of humans. Machines are programmed by
rational people, therefore, there is no difference between these two. Machines
are, on the other hand, better than irrational--behavioral players, or even
rational players. Examples include but are not limited to that they do not press
the wrong button by accident, they do not make decisions based on a bad mood
(e.g, to punish other machines), they do not form opinions about other people's
skills depending on how they look (this phenomenon is extensively studied in the
experimental economic literature), etc. Programs just follow the rules rational
people defined for them. Core exchange mechanism could be useful with
machine-to-machine scenarios as long as machines can do proper verification of
the service--item, that the seller provides. Examples include digital goods
(files, codes, passwords), the example of a similar solution is filebounty. With
physical goods commerce, mechanism can still be used in the machine-to-machine
approach. The only difference is that some steps (those that machines can not
perform) will be performed by humans. Integrating machine and human is not the
focus of the protocol. Another advantage of machine-to-machine use of the
mechanism is that moves do not need to be intuitive and have a logical
explanation. All the relevant information is final transfers and that the
subgame-perfect equilibrium corresponds to the correct play. To design transfers
in any game, we apply the same linear programming approach as in section on
**Linear programming formulation**. We need to design how the subgame-perfect
equilibrium solution looks, make appropriate assumptions on the utilities for
both players coming from each move, and solve the linear program to find
transfers in the final states leading to this subgame-perfect equilibrium
solution.

## Related literature

Theoretical importance and applicability of subgame-perfect equilibria solutions
were found much earlier. Moore and Repullo (1988) developed a general mechanism.
The paper proposes subgame perfect implementation of most of the allocation
problems given some mild conditions are satisfied. In other words, the authors
prove that almost all social choice functions can be implemented as a subgame
perfect equilibrium solution of some game. However, the game forms can be
complicated, they have at most $$3$$ stages.

A more recent experiment by Aghion et al. (2018) suggests that participants fail
to play these games correctly and that often subgame-perfect equilibrium
solution is not implemented. The authors argue that the problem is not in the
inability of the participants to use backward induction for calculating the
right solution, but in their beliefs about counterparts' abilities. $$30\%$$ of
the buyers who get a high-quality good lie, while $$10\%$$ of the buyers lie all
the time. In the context of the Boson exchange mechanism, it would be the seller
forming pessimistic beliefs about the buyer.

This mechanism can be easily generalized to general values of $$h$$ and $$l$$,
where $$h$$ denotes the value of the high-quality item/service and $$l$$ denotes
the value of the low-quality item/service. A similar generic example was
developed by Gans (2019), with the difference that the seller has different
costs of sending/providing different quality item/service.

Two additional recent experimental papers, Fehr et al. (2020) and Chen et al.
(2020) test theoretical predictions of how players should play if they were
rational and believed that other players were also rational. The first one
discusses the role of risk-aversion in sequential games. Players act
irrationally if the mechanism introduces too high fines for misbehavior. The
second one claims to have a simpler (2-stage) and more efficient (in the sense
that players deviate from subgame-perfect play very rarely) mechanism.

These experimental papers explain why games with subgame-perfect equilibrium
solutions are not implemented in real life, even though they are efficient and
well understood in the theoretical economic literature. We could argue that one
additional reason for this is the absence of low-cost intermediaries, which can
be replaced by smart contracts and decentralized systems. In the Boson core
exchange mechanism, on the other hand, common knowledge is guaranteed by
informing both parties joining the smart contract by default. Smart contracts
can be seen as a way of generating common knowledge. Informally, common
knowledge of a proposition $$P$$ means: every player knows $$P$$, every player
knows that every other player knows $$P$$, every player knows that every player
knows that every player knows $$P$$, and so on and so forth, infinitely. In our
setting, $$P = \text{\{all players are rational\}}$$.

## Future development

Experimenting exchange mechanisms with different parameters in different
environments, assessing their performance, and finding the best contracts
depending on the application is at the center of the core mechanism development.
Creating a suitable environment for common knowledge in the game is the ultimate
goal to achieve. Such an environment would allow the efficient deployment of not
only exchange mechanisms but also more sophisticated economic mechanisms, which
on its own would save intermediary fees and a negative impact powerful
intermediaries or centralized authorities have on the general ecosystem. Natural
live experiments using Boson's core exchange mechanism should contribute to our
knowledge in experimental economics as well. We have so far analyzed a game
where only the seller makes a hidden move. In some applications, the buyer may
also make a move, before they start reporting to the smart contract. This adds
additional complexity to the analysis since the order of moves is not observed
by the mechanism, therefore, the analysis of both possible sequences is
required. We also need to include mechanism/smart contract fee calculation in
the design and analysis.

## References

- Aghion, P., Fehr, E., Holden, R., and Wilkening, T. (2018). The role of
  bounded rationality and imperfect information in subgame perfect
  implementation – an empirical investigation. Journal of European Economic
  Association, 16(1):232–274.
- Blumrosen, L. and Dobzinski, S. (2016). (Almost) efficient mechanisms for
  bilateral trading. CoRR, abs/1604.04876.
- Chen, Y.-C., Holden, R., Kunimoto, T., Sun, Y., and Wilkening, T. (2020).
  Getting dynamic implementation to work. Working Paper.
- Fehr, E., Powell, M., and Wilkening, T. (2020). Behavioral constraints on the
  design of subgame-perfect implementation mechanisms. Forthcoming at American
  Economic Review.
- Gans, J. S. (2019). The fine print in smart contracts. Working paper.
- Janin, S., Qin, K., Mamageishvili, A., and Gervais, A. (2020). Filebounty:
  Fair data ex-change. In IEEE European Symposium on Security and Privacy
  Workshops, EuroS&PWorkshops 2020, Genoa, Italy, September 7-11, 2020, pages
  357–366. IEEE.
- Mamageishvili, A. and Schlegel, J. C. (2020). Optimal smart contracts with
  costly verification. InIEEE International Conference on Blockchain and
  Cryptocurrency, ICBC 2020,Toronto, ON, Canada, May 2-6, 2020, pages 1–8. IEEE.
- Moore, J. and Repullo, R. (1988). Subgame perfect implementation.
  Econometrica, 56(5):1191–1220.
