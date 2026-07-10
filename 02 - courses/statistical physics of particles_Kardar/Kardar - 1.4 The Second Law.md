The second law is derived from the understanding of heat engines.

An **[[Idealized Heat Engine|idealized heat engine]]** works by taking a certain amount of heat $Q_{H}$ from a heat source, converting a portion of it to work $W$, and dumping the remaining heat into a heat sink. Its efficiency can be calculated by

$$
\eta = \frac{W}{Q_{H}} = \frac{Q_{H}-Q_{C}}{Q_{H}} = 1-\frac{Q_{C}}{Q_{H}}\leqslant 1
\tag{1}
$$

An **[[Idealized Refrigerator|idealized refrigerator]]** works by using work $W$ to extract heat $Q_{C}$ from a cold system and dumping both the work $W$ and the heat $Q_{C}$ as heat $Q_{H}$ at a higher temperature. The figure of merit for the performance of a refrigerator is defined as

$$
\omega=\frac{Q_{C}}{W}=\frac{Q_{C}}{Q_{H}-Q_{C}}
\tag{2}
$$

The [[First Law of Thermodynamics|first law]] rules out "[[Perpetual Motion Machines of the First Kind|perpetual motion machine of the first kind]]", which can produce work without consuming any energy. However, the conservation of energy is not violated by an engine, for example, which produces work by using the energy released when water freezes into ice. This kind of engine is called "[[Perpetual Motion Machines of the Second Kind|perpetual motion machine of the second kind]]", and its feasibility would still be constrained by the [[Second Law of Thermodynamics|second law]].

The observation that the natural direction of the flow of heat is from hotter to colder bodies is the essence of the second law of thermodynamics. The second law has several different statements, such as the following two statements.

**[[Kelvin-Planck Statement]]**. No heat engine operating in a cycle can have the extraction of heat from a single reservoir and the complete conversion of that heat into work as its sole effect.

**[[Clausius Statement]]**. No process is possible whose sole result is the transfer of heat from a colder to a hotter body.

According to the Kelvin-Planck statement, there is no perfect engine whose efficiency is equal to $1$; according to the Clausius statement, there is no perfect refrigerator whose work input is $0$.

The two statements are equivalent. Assume that there is a perfect refrigerator which violates the Clausius statement, and it can take heat $Q$ from a colder region and dump it to a hotter one. Consider an engine which takes $Q_H$ from the hotter region, produces work $W$, and dumps $Q$ into the colder sink. The combined system acts as a perfect engine, which takes $Q_{H}-Q$ from the hotter region, produces work $W$ equal to $Q_{H}-Q$, dumps no heat into the colder sink, and violates the Kelvin-Planck statement.

Alternatively, assume that there is a perfect engine which violates the Kelvin-Planck statement, and it can take $Q$ from the hotter region and convert it completely into work. Consider a refrigerator using the work $W=Q$ to take $Q_{C}$ from the colder region and dump $Q_{C}+Q$ into the hotter sink. The combined system acts as a perfect refrigerator, which takes $Q_{C}$ from the colder region, dumps $Q_{C}$ into the hotter sink, requires no external work input, and violates the Clausius statement.
