---
layout: docs
title: "Boson Protocol: Docs: Advanced Topics: Token Engineering"
short_title: "Token Engineering"
permalink: /advanced-topics/token-engineering/
---

# Boson Token engineering

Boson is a multi-aspect, multi-stakeholder situation. We must **design for
emergence**. We must come equipped with lenses to view multiple scopes. We must
identify leverage points in the system. We will describe the ecosystem value
flows in a common language using systems design and engineering. Our process is
adopted and adapted for token engineering. The Design Space in Token Models is
quite large. Every model is wrong, some are useful; a [map is not the
teritory](https://fs.blog/2015/11/map-and-territory/) - Hence, at Boson Token
Engineering, we start with the following:

1. Identify assumptions
2. Document assumptions
3. Track assumptions

The network's token shall **trace & represent the valueflows** of the network
to enable **coordination** at global scale. Depiction below from [Outlier
Ventures internal
analysis](https://outlierventures.io/research/what-is-the-secret-to-building-valuable-tokens/)
shows the 2 components of token value, speculative, and fundamental.
*Engineering the speculative component is the dark side of the force* -
[Ecosystem Valueflows
Methodology](https://tokenengineeringcommunity.github.io/website/docs/academy-tmg1-ecosystem/)
focuses Token Engineering on the fundamental component. Once fundamental value
flows can be understood, designed, and engineered, then all that's needed to
trigger perpetual token value growth is the initialization of network effects &
sustainable governance.

![Token Value Composition](/images/docs/tokenengineering/1.png)

Boson Protocol invests significantly into maintaining one of the industry's
strongest rosters for token engineering and maintains close relationships with
industry leaders in the space such as advisors Dr. Michael Zargham and Dr.
Trent McConaghy, two foundational researchers who have written seminal
literature for the field and pioneered world changing technology. Dr. Zargham
is the founder of BlockScience and the inventor of cadCAD, and Dr. McConaghy,
co-founder of Ocean Protocol, is also the inventor of TokenSPICE. 

Dr. McConaghy's call for an emergent practice of token engineering and
systematic approach to such a discipline:

https://blog.oceanprotocol.com/towards-a-practice-of-token-engineering-b02feeeff7ca

Dr. Shermin Voshmgir and Dr. Zargham's Foundations of cryptoeconomic systems:

https://epub.wu.ac.at/7782/1/Foundations%20of%20Cryptoeconomic%20Systems.pdf

## Boson TE Methodology
The Token Engineering methodology practised at Boson is heavily influenced by
the work and research of our advisors. Our approach can be understood
essentially as the following four-step process:
1. Write out **Goals** that we are trying to achieve.
2. Explore the **Design** space of tokenized mechanisms that can be composed towards achieving our goals - loop back to update our goals.
3. **Verification** of designs using numerical methods, modelling and simulation, data science and visualization - loop back to update designs
4. Expose mechanism levers and their resulting **Impact** on the bounds and likelihoods of ecosystem outcomes to empower decentralized decision-making towards **Optimization** - loop back to update designs

### Goals for Boson Token Engineering
The objective of our ecosystem is to **maximize the number of quality voucher
redemptions** **facilitated by Boson Protocol**. By injecting a small fee
into protocol usage, value capture is enabled. By routing value back into
ecosystem development, a virtuous cycle of sustainable growth is enabled for
Boson and its surrounding ecosystem. And by guard-railing a compliant path to
progressive decentralization, we can ensure the survival and continuous
improvement of an anti-fragile network to build and deploy the fair and
equitable dCommerce stack. In summary, in addition to optimizing for the
ecosystem objective function as stated above, we are engineering for the
following goals:

- **Fair and equitable** distribution of ownership, value, and control.
- **Capture resistance** from centralized, extractive entities.
- **Regulatory compliance** with legitimate authorities.
- **Community ownership** and operation.

### Design space for Boson Token Engineering
The design space for Boson Token Engineering can be decomposed into three
primary categories, mechanism design, ecosystem value flows, and governance.
Each of which is covered in more detail in it's respective documentation page.
Here, we give a brief introduction to the stock and flow schema that is heavily
utilized by the Boson TE team to design ecosystem value flow models that are
later modelled and verified using cadCAD.

**Stock & Flows**
The Stock & Flow is a system diagram representing the relationship between
different 'stocks' deposits of quantity and 'flows' the change between them.
You can think of a stock as a reserve that if time stops will not move at all;
a flow is the relationship between these different stocks as time passes; if
time stops there will be nothing in the flows and the stocks will not change at
all.

![Stock and Flows](/images/docs/tokenengineering/2.png)

#### Value Flows 

The Value Flow is the stock and flow when applied to the value distribution in
an ecosystem. Value comes in from the inflows and exits through the outflows
through a network of stocks and flows.

#### The Boson Ecosystem ValueFlows

![Value Flows 1](/images/docs/tokenengineering/3.png)
![Value Flows 2](/images/docs/tokenengineering/4.png)

[Full detail on Boson Value flows](../core-concepts/ecosystem-value).

### Numerical Verification - Modelling and Simulation

Our token engineering methodology allows for separation of concerns between
design teams and modelling teams. Ecosystem value flows are the final product
of the design team, and are handed of to the Python gurus for model
implementation, simulations, and analysis. It's early stages for the Boson
token engineering team, but here we present the preliminary results of the Boson ecosystem
modelling. 

Visualization of $BOSON fully diluted token distribution allocations. On the
left is the full breakdown, and on the right, we have consolidated categories.

![Fully Diluted Circulating Supply](/images/docs/tokenengineering/5.png)
![Consolidated Categories - Fully Diluted Circulating Supply](/images/docs/tokenengineering/6.png)

Twelve month snapshots of the $BOSON circulating supply

![5 Year Circulating Supply](/images/docs/tokenengineering/7.png)

The $BOSON distribution allocation over five years, consolidated by category.

![Consolidated Release Schedule](/images/docs/tokenengineering/8.png)

Early considerations of capture resistance and equitable share of value for the
Boson network. Progressive decentralization allows for governance 'guard rails'
in the early stages of network development until network developers and
operators can ensure a majority possesion of the network after the initial
fundraising periods.

![Capture Resistance Analysis](/images/docs/tokenengineering/9.png)

#### cadCAD in Context

cadCAD is an open-source Python library that lets you design, optimize,
validate and understand dynamical complex systems. It is useful because it
allows engineers to ask powerful 'what if?' questions, using simulation features
like A/B Tests, Parameter Sweeps or Monte Carlo Analysis. In our case, we use
cadCAD for simulating the movements of Boson Value Flows over time. We can do this
by assuming the length of a Time Step, say 1 month, and specifying the number
of Time Steps that the system will run for, say 60 steps (5 years). The stocks
act as variables while the flows act as rates of change between them.

Here we model 'Phase-0' of the ecosystem's value flows for the network. This is
a linear model in which Boson network rewards are distributed strategically to
network developers and participants and to fund the production of community
ecosystem products, driving long-term value generation for boson and its
surrounding ecosystem.

![Boson Ecosystem Fund Distribution](/images/docs/tokenengineering/10.png)

Here we model 'Phase-1' of the ecosystems value flows for the network. In this
case, we have a supply of commitment token vouchers being minted by sellers.
Sellers are recruited to the platform by aggregators, for which we assume a
linear growth rate, but a non-linear growth in sellers. In this model, each
seller introduces a single type of product into the marketplace, represented by
a commitment token voucher set (ERC1155). Each product has a quantity
available, a price, an underlying quality, a popularity, and other attributes
such as name. We also assume that the number of buyers in the market will
increase non-linearly as the number of diverse products grows linearly.
Complaints and faults are sampled from a random distribution based on the
underlying value of each commitment voucher item. As items result in complaints
or faults, their public popularity score decreases.

![Phase 1 Things](/images/docs/tokenengineering/11.png)
![Phase 1 Things 2](/images/docs/tokenengineering/12.png)

This work is extremely early stages, but has laid a framework for expansion of
ecosystem introspection. Next steps for the TE team include deeper dives into
mathematical formulations of the rates of change and mechanisms described
above, as well as implementing detailed models on refunds and ecalated
arbitration. Stay tuned for a series of publications on this topic in Q2 of
this year.

The above results do not indicate any sort of expectations of the future. They
are merely models, and we must remember the golden rule "All models are wrong,
but some are useful." We look forward to progressively collaborating with the
community at large in future iterations of our token engineering iterations for
Boson and the dCommerce stack.

### Impact Optimization

The Boson team is currently investigating topics such as optimal protocol fees
for sellers and buyers, and reward mechanisms for supply aggregators. Further
analysis and results will be released in a series of publications in Q2 of this
year. 

## Solving dCommerce challenges

**dCommerce challenges** At the core of dCommerce are a set of challenges which
combine operations, game theory, ecosystem value flows and token engineering. 
It is possible that this set of problems is intractable, which would mean that
commerce will be forever mediated by humans - with all the cost, trust and
friction that this implies.  However, our research indicates that these
problems can be solved, to a significant extent, by unbundling the services
provided by ecommerce and replacing them with composable decentralized
applications and protocols.  Boson’s core mechanism and despatch modules are
examples of these.

**dCommerce research group** We spoke to the token engineering community leads
and agreed to create a research group to attract multi-disciplinary people to
work on hard problems in dCommerce.  This research group will offer funded
bounties for teams to find solutions to problems such as:

- Refunds (via decentralized identity and insurance providers)
- Escalated arbitration (to arbitrators or insurance protocols)
- Quality assessment (via keepers)
- Despatch (enabling buyers to delegate redemption signing)

**dCommerce community outreach**  We will feed this research group with a
funnel of new talent via an industry and academic outreach program.  This
outreach program will incentivize people from specific disciplines such as
insurance, ecommerce and finance to come and work on hard problems in tandem
with people with skills such as token engineering and game theory.

**dCommerce DAO**  Research groups which can apply for funding from the
dCommerce DAO, in order to develop solutions into dApps or protocols which may
be usefu or valuable to the ecosystem.

**dCommerce accelerator** We are in discussion with Outlier Ventures about
creating a track within their Basecamp accelerator, for dCommerce projects. 
Such projects would receive additional grant funding and specialist token,
ecosystem, game theory and dcommerce support from the Boson Protocol team.

Think you've got what it takes to face the dCommerce challenges? Reach out to
Boson's head of community, Alastair Band, on LinkedIn to learn more about the
opportunities.

[Alastair Band - Head of Community - Boson Protocol | LinkedIn](https://www.linkedin.com/in/alastairband/)

## Partnering with the Token Engineering Academy and Token Engineering Commons

Boson Protocol cleaned the cupboards at the token engineering academy by hiring
the majority of top-tier token engineering researchers, teachers, and students
coming out of the programs there. Thus due to the non-extractive mandate of
Boson, replenishments are in order. This is why Boson has committed to
multi-faceted donations to support the token engineering community in the forms
of monetary, human capacity, and collaborative research support. Further
information will be revealed through a series of publications in Q2 2021.

### The Token Engineering Community

If you want to learn about Token Engineering, the best place to start is with
the [Token Engineering Community](https://discord.gg/SC2RyT6VMR). Be sure to
follow TEC founder Angela for the most up do date feeds on token engineering. 

[https://twitter.com/akrtws/status/1357680728000114689](https://twitter.com/akrtws/status/1357680728000114689)

To begin a career in Token Engineering, be sure to enroll in the next cohort of
the [Ecosystem Value Flows
Course](https://tokenengineeringcommunity.github.io/website/docs/academy-tmg1-ecosystem),
as designed by Boson's very own Sebnem, and produced by the [Token Engineering
Academy](https://tokenengineeringcommunity.github.io/website/docs/events-welcome).
For a deeper dive into modelling and simulations using cadCAD, we can only
recommend the wonderful course at cadcad.education. Use any of the sponsors as
a keyword to get a discount on enrollment. 

### The Token Engineering Commons

To participate in collaborative development of the most bleeding-edge token
engineering products for public good, be sure to participate in the Token
Engineering Commons! "The TEC is like a skatepark for brilliant academics,
teachers, hackers, designers, and cultural innovators" - Nico Rodriguez.

[Token Engineering Commons - Medium](https://medium.com/token-engineering-commons)

Boson Protocol's Sebnem hosts the Omega working group bi-weekly working session, getting
to the bottom of assumptions that we hold in the token engineering community,
and addressing the emergent properties of ethics in the field. Boson's Shawn
Anderson hosts a weekly tech lab every Friday for anyone to come and get your
hands dirty in experimenting with the latest and greatest token engineering
toolsets such as cadCAD or TokenSPICE2.

### Stay Tuned for More
And of course, stay tuned for rapid and ground-breaking developments coming out of Boson Protocol 
as we march towards a future where all humans can benefit from the value we generate through collaborative,
decentralized commerce!

[Boson Protocol](https://www.bosonprotocol.io/)
