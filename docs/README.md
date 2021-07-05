
{! ../README.md !}

## Bitcoin Entropy

Statistical Thermodynamic Entropy $S$ is defined by the total number of potential (micro-)states of a system, $\Omega$ times Boltzmann's constant.

$$
S = k_B ln(\Omega)
$$

$$
k_B = 1.38064852 × 10-23 [m^2kg/s^2K]
$$

In proof of work, miners look for any number (the Nonce) that generates a hash with a specific number of leading 0s. The difficutlty is given by

$$
\Omega = D * 2^{48}/ \alpha_c
$$

$$
\alpha_c = 65535 = 0XFFFF
$$


We can think of each guess as a microstrostate of the system, and the number of such possible microstates is given by the current mining difficulty. As a result, we can define Bitcoin Entropy $S_{BTC}$

$$
S_{BTC}(D) = k_B ln(D 2^{48} / \alpha_c) = k_B ln(D) + const
$$

However, Bitcoin's difficulty is not constant, but adjusts every 2 weeks. The change in difficulty, $\Delta D$ results in a change in Entropy $\Delta S_{BTC}$. Taking the derivative $S_{BTC}(D)$ with respective to difficulty drops the above constant, yielding

$$
\Delta S_{BTC}(\Delta D) = k_B \Delta D/D ...
$$

## Bitcoin Enthalpy

Enthalpy $H$ is given by the internal energy $E$ and the environmental pressure $PV$
$$
H = E + PV 
$$

In most chemical reactions we would be interested in just the change in enthalpy, and approximatations may be made about the environment (constant pressure, work done is due to changes in volume only)

$$
\Delta H = q + w + P \Delta V = q + -P\Delta V + P \Delta V = q
$$

Heat $q$ energy that flows due to a difference in temperature. q is negative if heat is being released by the system. Heat always flows spontaneously from high temperature to low temperature. When temperature and pressure are constant: $q= \Delta H$ the change in enthalpy.

Enthalpy of a chemical reaction measured in $\pm kJ/mol$

However Bitcoin mining incentivizes all forms of energy production. Just as there are many chemical processes that may absorb heat from an environment there are many physical processes that may result in mining. Stranded natural gas, geothermal, hydroelectric, wind, and solar have all been used as sources of energy production. Each of these has varying degrees of efficiency, but we can assume such efficiencies are constant relative to the 2-week period of difficulty adjustment. So we may consider such sources "upstream" of the mining operation and only consider the energy able to be leveraged in hash rate.


Recall

* Exothermic - releases energy into the environment
* Endothermic - absorbs energy from the environment
* $H$ -Enthalpy is the internal energy of a system
* $\Delta H$ Change in enthalpy of a system


In Bitcoin, we are interested in the total energy put and released from bitcoin mining, which is proporational to the current hash rate times the efficiency of the mining process.

!!! note
    The hashrate itself is not directly measureable, but is proporational to difficulty.

As the bitcoin network grows, we have seen more and more energy being absorbed by bitcoin mining, so the system is clearly endothermic over long time scales. When the hashrate reduces, however, the energy available to mining may be reallocated elsewhere.


In Thermite, if the reactants have more energy than the surrounding system, then one might expect a sponanteous reaction to occur. However, there are chemical reactions like Ice packs that occur sponanteous and pull energy from the environment. To understand whether a system is set up for spontaneous reaction, we need to take into account Entropy as well as Enthalpy. 



## Gibbs Free Energy

The Gibbs Free Energy relates Enthalpy, $\Delta H$, Temperature $T$ and Entropy $\Delta S$ to determine the energy available to work.

$$
\Delta G = \Delta H - T \Delta S
$$

This is the energy available to do work in a physical propcess. It determines whether a system is spontaneous or non-spontaneous reaction


placeholder |$\Delta H < 0$ | $\Delta H > 0$ 
-------------- | ------------ | ------------
$\Delta S > 0$   | Spontaneous  | Spontaneous at High Temperature
$\Delta S < 0$  | Spontaneous at Low Temperature | Not Spontaneous



What about in between?

$$
0 = \Delta H - T \Delta S
$$

$$
\Delta H = T \Delta S
$$

What does this tell us about Bitcoin's difficulty adjustment?






