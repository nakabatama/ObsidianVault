The time evolution of systems toward equilibrium is governed by the [[Second Law of Thermodynamics|second law]]. For instance, for an **[[Adiabatically Isolated System|adiabatically isolated system]]**, [[Entropy|entropy]] must increase in any spontaneous change and reaches a maximum in equilibrium.

For a system with no heat exchange that approaches mechanical equilibrium with constant externally applied [[Generalized Forces|generalized forces]], the conditions are $\mathrm{\bar{d}}Q$=0 and $\delta \mathbf{J}=0$. For any set of [[Generalized Displacements|generalized displacements]] $\mathbf{x}=\left( x_{1},x_{2},\dots \right)$, at constant externally applied generalized forces $\mathbf{J}=\left( J_{1},J_{2},\dots \right)$, while going through a reversible or irreversible transformation, the work input to the system $\mathrm{\bar{d}}W$ satisfies

$$
\mathrm{\bar{d}}W\leq \mathbf{J} \cdot \delta\mathbf{x}.
\tag{1}
$$

Equality holds for a [[Reversible Transformation|reversible transformation]], for which the applied generalized forces match the internal generalized forces. However, for [[Irreversible Transformation|irreversible transformations]], there is usually some loss of the external work to dissipation. Thus, the actual work contributing to the [[Internal Energy|internal energy]] change of the system $\mathrm{\bar{d}}W$ is generally smaller than $\mathbf{J}\cdot \delta \mathbf{x}$.

Since $\mathrm{\bar{d}}Q=0$, according to the [[First Law of Thermodynamics|first law]], we obtain

$$
\delta E=\mathrm{\bar{d}} W + \mathrm{\bar{d}}Q\leq \mathbf{J}\cdot \delta \mathbf{x}.
\tag{2}
$$

Based on $(2)$, a new state function, so-called **[[Enthalpy|enthalpy]]**, can be defined as

$$
H=E-\mathbf{J}\cdot \mathbf{x},
\tag{3}
$$

which satisfies

$$
\delta H=\delta \left( E-\mathbf{J}\cdot \mathbf{x} \right)=\delta E-\mathbf{J}\cdot \delta \mathbf{x}-\mathbf{x}\cdot \delta \mathbf{J}=\delta E-\mathbf{J}\cdot \delta \mathbf{x} \leq 0
\tag{4}
$$

during an irreversible relaxation toward equilibrium at fixed $\mathbf{J}$. It is worth noting that relation $(4)$ describes the change of enthalpy as a non-equilibrium system relaxes toward equilibrium at fixed applied generalized force.

The variations of $H$ during a reversible transformation are given by

$$
\mathrm{d}H=\mathrm{d}E-\mathrm{d}\left( \mathbf{J}\cdot \mathbf{x} \right)=T\mathrm{d}S+\mathbf{J}\cdot \mathrm{d}\mathbf{x}-\mathbf{J}\cdot \mathrm{d}\mathbf{x}-\mathbf{x}\cdot \mathrm{d}\mathbf{J}=T\mathrm{d}S-\mathbf{x}\cdot \mathrm{d}\mathbf{J},
\tag{5}
$$

which describes a relation between equilibrium coordinates.

It follows from equation $(5)$ that

$$
T=\left( \frac{ \partial H }{ \partial S } \right)_{\mathbf{J}},
\tag{6}
$$
$$
x_{i}=-\left( \frac{ \partial H }{ \partial J_{i} } \right)_{S,J_{j \neq i}}.
\tag{7}
$$

In particular, for an [[Ideal Gas|ideal gas]], Equations $(5)$, $(6)$, and $(7)$ reduce to

$$
\mathrm{d}H=T\mathrm{d}S+V\mathrm{d}P,
\tag{8}
$$
$$
T=\left( \frac{ \partial H }{ \partial S } \right)_{P},
\tag{9}
$$
$$
V=\left( \frac{ \partial H }{ \partial P } \right)_{S}.
\tag{10}
$$

Note that heat capacity at constant pressure can be expressed as

$$
C_{P}=\left( \frac{\mathrm{\bar{d}}Q}{\mathrm{d}T} \right)_{P}=\left( \frac{\mathrm{d}E+P\mathrm{d}V}{\mathrm{d}T} \right)_{P}=\left( \frac{\mathrm{d}\left( E+PV \right) }{\mathrm{d}T} \right)_{P}=\left( \frac{\mathrm{d}H}{\mathrm{d}T} \right)_{P}.
\tag{11}
$$

For a system going through isothermal transformations in the absence of mechanical work, the conditions are $\mathrm{\bar{d}}W=0$ and $\delta T=0$. From [[Clausius Theorem|Clausius theorem]], the heat intake of the system at a constant temperature $T$ satisfies $\mathrm{\bar{d}}Q\leq T\delta S$. Thus, we obtain

$$
\delta E=\mathrm{\bar{d}}Q+\mathrm{\bar{d}}W\leq T\delta S.
\tag{12}
$$

Based on $(12)$, a new state function, so-called **[[Helmholtz Free Energy|Helmholtz free energy]]**, can be defined as

$$
F=E-TS
\tag{13}
$$

which satisfies

$$
\delta F=\delta \left(E-TS \right)=\delta E-T\delta S-S\delta T=\delta E-T\delta S\leq 0
\tag{14}
$$

The variations of $F$ during a reversible transformation are given by

$$
\mathrm{d}F=\mathrm{d}E-\mathrm{d}\left( TS \right)=T\mathrm{d}S+\mathbf{J}\cdot \mathrm{d}\mathbf{x}-T\mathrm{d}S-S\mathrm{d}T =-S\mathrm{d}T+\mathbf{J}\cdot \mathrm{d}\mathbf{x}.
\tag{15}
$$

Similarly, we have

$$
S=-\left( \frac{ \partial F }{ \partial T } \right)_{\mathbf{x}},
\tag{16}
$$
$$
J_{i}=\left( \frac{ \partial F }{ \partial x_{i} } \right)_{T,x_{j\neq i}}.
\tag{17}
$$

For an ideal gas

$$
\mathrm{d}F=-S\mathrm{d}T-P\mathrm{d}V,
\tag{18}
$$
$$
S=-\left( \frac{ \partial F }{ \partial T } \right)_{V},
\tag{19}
$$
$$
p=-\left( \frac{ \partial F }{ \partial V } \right)_{T}.
\tag{20}
$$

The internal energy can also be calculated from $F$ using

$$
E=F+TS=F-T\left( \frac{ \partial F }{ \partial T } \right)_{\mathbf{x}}=-T^{2}\left( \frac{ \partial (F/T)}{ \partial T } \right)_{\mathbf{x}}.
\tag{21}
$$

For a system going through isothermal transformations involving mechanical work at constant external force, the condition is $\delta \mathbf{J}=0$ and $\delta T=0$. Thus we have $\mathrm{\bar{d}}W\leq \mathbf{J}\cdot \delta \mathbf{x}$ and $\mathrm{\bar{d}}Q \leq T\delta S$. Hence $\delta E=\mathrm{\bar{d}}W+\mathrm{\bar{d}}Q\leq \mathbf{J}\cdot \delta \mathbf{x}+T\delta S$. Based on this inequality, we can define a new state function, **[[Gibbs Free Energy|Gibbs free energy]]** $G$, as

$$
G=E-TS-\mathbf{J}\cdot \mathbf{x}
\tag{22}
$$

which satisfies

$$
\delta G=\delta(E-TS-\mathbf{J}\cdot \mathbf{x})=\delta E-T\delta S -\mathbf{J}\cdot \delta \mathbf{x}\leq 0.
\tag{23}
$$

Variations of $G$ during a reversible transformation are given by

$$
\mathrm{d}G=\mathrm{d}E-\mathrm{d}(TS)-\mathrm{d}(\mathbf{J}\cdot \mathbf{x})=-S\mathrm{d}T-\mathbf{x}\cdot \mathrm{d}\mathbf{J}.
\tag{24}
$$

Similarly, we have

$$
S=-\left( \frac{ \partial G }{ \partial T } \right)_{\mathbf{J}},
\tag{25}
$$
$$
x_{i}=-\left( \frac{ \partial G }{ \partial J_{i} } \right)_{T,J_{j\neq i}}.
\tag{26}
$$

In particular, for an ideal gas, they reduce to

$$
\mathrm{d}G=-S\mathrm{d}T+V\mathrm{d}P
\tag{27}
$$
$$
S=-\left( \frac{ \partial G }{ \partial T } \right)_{P}
\tag{28}
$$
$$
V=\left( \frac{ \partial G }{ \partial P } \right)_{T}
\tag{29}
$$

So far, we have implicitly assumed that the number of particles in the system is constant. However, in chemical reactions, or in phase equilibrium, the number of particles in a given component may change. The change in the number of particles contributes to changes in the internal energy, which is expressed as **[[Chemical Work|chemical work]]**

$$
\mathrm{\bar{d}}W_{N}=\boldsymbol{\mu}\cdot \mathrm{d}\mathbf{N},
\tag{30}
$$

in which $\mathbf{N}=\left( N_{1},N_{2},\dots \right)$ lists the numbers of particles of the different species, and $\boldsymbol{\mu}=\left( \mu_{1},\mu_{2},\dots \right)$ denotes the corresponding chemical potentials. Each **[[Chemical Potential|chemical potential]]** $\mu_{i}$ represents the energetic cost of adding one particle of species $i$ to the system under the specified thermodynamic conditions.

For a system approaching chemical equilibrium while in contact with heat and particle reservoirs at fixed temperature $T$ and fixed chemical potentials $\boldsymbol{\mu}$, and in the absence of mechanical external work, the conditions are $\delta T=0$, $\delta\boldsymbol{\mu}=0$, $\mathrm{\bar{d}} W=0$, and $\mathrm{\bar{d}}W_{N}=\boldsymbol{\mu}\cdot \delta\mathbf{N}$. From Clausius theorem, the heat intake of the system at a constant temperature $T$ satisfies $\mathrm{\bar{d}}Q\leq T\delta S$. Therefore, the internal energy

$$
\delta E=\mathrm{\bar{d}}W_{N}+\mathrm{\bar{d}}Q\leq\boldsymbol{\mu}\cdot \delta\mathbf{N}+T\delta S.
\tag{31}
$$

Hence the appropriate state function is the **[[Grand Potential|grand potential]]** defined as

$$
\mathcal{G}=E-TS-\boldsymbol{\mu}\cdot \mathbf{N}
\tag{32}
$$

since

$$
\delta \mathcal{G}=\delta E-T\delta S-S\delta T-\boldsymbol{\mu}\cdot \delta\mathbf{N}-\mathbf{N}\cdot \delta\boldsymbol{\mu}=\delta E-T\delta S-\boldsymbol{\mu}\cdot \delta \mathbf{N}\leq 0.
\tag{33}
$$

Variations of the grand potential satisfy

$$
\mathrm{d}\mathcal{G}=\mathrm{d}E-T\mathrm{d}S-S\mathrm{d}T-\boldsymbol{\mu}\cdot \mathrm{d}\mathbf{N}-\mathbf{N}\cdot \mathrm{d}\boldsymbol{\mu}=-S\mathrm{d}T+\mathbf{J}\cdot \mathrm{d}\mathbf{x}-\mathbf{N}\cdot\mathrm{d}\boldsymbol{\mu}.
\tag{34}
$$

It is worth emphasizing that for a system that can exchange particles with its surroundings, the differential forms of internal energy, enthalpy, Helmholtz free energy, and Gibbs free energy are

$$
\mathrm{d}E=T\mathrm{d}S+\mathbf{J}\cdot \mathrm{d}\mathbf{x}+\boldsymbol{\mu}\cdot \mathrm{d} \mathbf{N},
\tag{35}
$$
$$
\mathrm{d}H=T\mathrm{d}S-\mathbf{x}\cdot \mathrm{d}\mathbf{J}+\boldsymbol{\mu}\cdot \mathrm{d} \mathbf{N},
\tag{36}
$$
$$
\mathrm{d}F=-S\mathrm{d}T+\mathbf{J}\cdot \mathrm{d}\mathbf{x}+\boldsymbol{\mu}\cdot \mathrm{d} \mathbf{N},
\tag{37}
$$
$$
\mathrm{d}G=-S\mathrm{d}T-\mathbf{x}\cdot \mathrm{d}\mathbf{J}+\boldsymbol{\mu}\cdot \mathrm{d} \mathbf{N}.
\tag{38}
$$

In thermodynamics, the appropriate state function is chosen according to the constraints imposed by the surroundings. For a simple compressible system, which satisfies $\mathbf{J}=-P$ and $\mathbf{x}=V$, with constant volume and number of particles, the internal energy $E(S,V,\mathbf{N})$ is the natural potential when $S$, $V$, and $\mathbf{N}$ are specified. If the system is in thermal contact with a heat reservoir, the temperature $T$ rather than the entropy $S$ is controlled, and the Helmholtz free energy $F(T,V,\mathbf{N})$ becomes the appropriate potential. If the external pressure $-P$ is fixed instead of the volume $V$, the enthalpy $H(S,P,\mathbf{N})$ is natural. If both temperature $T$ and pressure $-P$ are fixed, the Gibbs free energy $G(T,P,\mathbf{N})$ is the appropriate potential. When the system is also in contact with a particle reservoir, the particle numbers $\mathbf{N}$ are replaced by their conjugate chemical potential $\boldsymbol{\mu}$.

The role of a **[[Legendre Transformation|Legendre transformation]]** is to rewrite the state function in a form adapted to the constraints imposed on the system. In this way, the direction of spontaneous processes and the equilibrium condition can be determined directly from the decrease or minimization of the corresponding thermodynamic potential.
