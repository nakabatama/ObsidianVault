The first law of thermodynamics states that energy is conserved in a thermodynamic process. Heat supplied to a system is used partly to increase the internal energy of the system and partly to do work by the system on its surroundings.

The conservation of energy implies that, for an otherwise adiabatically isolated system, the work required to change its state depends only on the initial and final states, not on the way in which the work is performed or on the intermediate states through which the system passes.

Based on this conclusion, for the thermodynamic system, we can construct another state function, **[[Internal Energy|internal energy]]** $E(\mathrm{X})$, in which $\mathrm{X}$ denotes the state of the system. The internal energy $E(\mathrm{X})$ can be obtained from the amount of the work $W$ needed for an **[[Adiabatic Transformation|adiabatic transformation]]** from an initial state $\mathrm{X_i}$ to a final state $\mathrm{X_f}$, by using

$$
W=E(\mathrm{X_f})-E(\mathrm{X_i}).
\tag1
$$

Once the adiabatic constraint is removed, the amount of work is no longer equal to the change in the internal energy. The difference is defined as the heat intake of the system from its surroundings. The relation can be denoted as

$$
Q=\Delta E-W,
\tag2
$$

in which $\Delta E$ stands for the change of internal energy and $W$ stands for the work done on the system.

For an infinitesimal change, the equation becomes

$$
\mathrm{\bar{d}} Q = \mathrm{d}E-\mathrm{\bar{d}}W.
\tag3
$$

Obviously, the heat $Q$ and the work $W$ are not separately functions of state, because they depend on external factors like the means of applying work. To emphasize this, we use the denotation $\mathrm{\bar{d}}$.  However, the internal energy can be obtained by differentiation as

$$
\mathrm{d} E = \sum_i \partial_i E \mathrm{d} X_i.
\tag4
$$

We now turn to the question of how the work term can be calculated. For quasi-static transformations, this can be done by expressing work in terms of generalized displacements and their conjugate generalized forces.

A **[[Quasi-static Transformation|quasi-static transformation]]** is one that is performed sufficiently slowly so that the system is always in equilibrium. Therefore, at any stage of the transformation, the thermodynamic coordinate of the system exist and can be computed in principle. 

One can typically divide the state variables $(\mathrm{X_1},...)$ into a set of **[[Generalized Displacements|generalized displacements]]** $(x_1,...)$ and a set of **[[Generalized Forces|generalized forces]]** $(J_1,...)$. Thus the work of an infinitesimal transformation can be computed as

$$
\mathrm{\bar{d}}W=\sum_iJ_i\mathrm{d}x_i.
\tag5
$$

The displacements are always extensive quantities, which is proportional to the size of the system, while the forces are always intensive and independent of size.

For the ideal gas, we have $PV\propto T$. By Joule's free expansion experiment, we know that if an ideal gas expands adiabatically from a volume $V_i$ to $V_f$, the initial and final temperature are the same. Because of the adiabaticity, we obtain $Q=0$, and we also obtain $W=0$ from free expansion. As a result, we have $\Delta E=0$. Since the volume of the gas change in the process, but its temperature remains the same, we conclude that internal energy only depends on temperature. Or

$$
E(V,T)=E(T).
\tag6
$$

**[[Response Functions|Response functions]]** are quantities that characterize how a system responds to small changes in external conditions or thermodynamic variables, which can usually be measured by experiment with external probes. They not only make the first law operational, but also connect abstract thermodynamic quantities with experimentally measurable properties.

**[[Heat Capacities|Heat capacities]]** are obtained from the change in temperature upon addition of heat to the system. Since heat is not a function of state, the path by which it is supplied must be specified. We can calculate the heat capacities at constant volume or at constant pressure, and we can get different properties. Their definition and simplification is as follows,

$$
C_V=\left(\frac{\mathrm{\bar{d}}Q}{\mathrm{d}T}\right)_V=\left(\frac{\mathrm{d}E-\mathrm{\bar{d}}W}{\mathrm{d}T}\right)_V=\left(\frac{\mathrm{d}E+P\mathrm{d}V}{\mathrm{d}T}\right)_V=\left(\frac{\partial E}{\partial T}\right)_V,
\tag{7}
$$
$$
C_P=\left(\frac{\mathrm{\bar{d}}Q}{\mathrm{d}T}\right)_P=\left(\frac{\mathrm{d}E-\mathrm{\bar{d}}W}{\mathrm{d}T}\right)_P=\left(\frac{\mathrm{d}E+P\mathrm{d}V}{\mathrm{d}T}\right)_P=\left(\frac{\partial E}{\partial T}\right)_P+P\left(\frac{\partial V}{\partial T}\right)_P.
\tag{8}
$$

Apart from the two heat capacities, other important response functions include the isothermal compressibility, magnetic susceptibility, thermal expansion coefficient, etc. The **[[Isothermal Compressibility|isothermal compressibility]]** is defined as

$$
\kappa_{T}=-\frac{1}{V}\left(\frac{\partial V}{\partial P}\right)_{T},
\tag{9}
$$

which describes the relative change in volume of a system in response to a change in pressure at fixed temperature.

The **[[Magnetic Susceptibility|magnetic susceptibility]]** of a megnet is defined as

$$
\chi_{T}=\frac{1}{V}\left(\frac{\partial M}{\partial B}\right)_{T}.
\tag{10}
$$

The **[[Thermal Expansion Coefficient|thermal expansion coefficient]]** of a gas is given by

$$
\alpha_{T}=\frac{1}{V}\left(\frac{\partial V}{\partial T}\right)_{P},
\tag{11}
$$

which describes the relative change in volume of a system in response to a change in temperature at fixed pressure.

Especially, for an ideal gas, we have $\kappa_{T}=1/P$ , $\alpha_{T}=1/T$, and

$$
C_{P}-C_{V}=\frac{\mathrm{d} E}{\mathrm{d} T}+P\left(\frac{\partial V}{\partial T}\right)_P-\frac{\mathrm{d} E}{\mathrm{d} T}=PV\alpha_{T}=\frac{PV}{T}=Nk_{B}.
\tag{12}
$$
