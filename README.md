# Bayesian analysis of the rotational period and galactic velocity of pulsars

This reporsitory For reference, see [Fragione & Loeb 2023](https://arxiv.org/pdf/2305.08920.pdf).

## Model

The spin at birth can be modeled as the sum of two contributions. The first contribution is the spin that the neutron star may inherit from the rotation of the progenitor star before explosion
\begin{equation}
    \mathbf{S_{\rm b,*}} = \frac{2\pi}{P_{\rm b,*}} \mathbf{\hat{j}}\,,
\end{equation}
where $\mathbf{\hat{j}}$ is the rotation axis and $P_{\rm b,*}$ its period. The second contribution arises from the possible off-center natal kick imparted to the neutron star at formation, as a result of asymmetries associated with the supernova ejecta
\begin{equation}
    \Delta \mathbf{S} = \frac{M_{\rm NS}}{I_{\rm NS}} \mathbf{R}_{\rm kick} \times \mathbf{V}_{\rm kick}\,.
\end{equation}
Here, $M_{\rm NS}$ and $I_{\rm NS}$ are the pulsar mass and moment of inertia, which we fix to $1.4\msun$ and $50\msun\ {\rm km}^2$ \citep[e.g.,][]{WoosleyHeger2002}, respectively, $V_{\rm kick}$ is the velocity kick, and $R_{\rm kick}$ is the location of the kick with respect to the center. Therefore, the total spin of a neutron star at birth is simply
\begin{equation}
    \mathbf{S_0}=\mathbf{S_{\rm b,*}} + \Delta \mathbf{S}\,.
\end{equation}
Regarding its magnitude, it is straightforward to show that
\begin{equation}
    S_0 = \left[\left(S_{\rm b,*}+\Delta S \cos\gamma \right)^2+\left(\Delta S \sin\gamma \right)^2\right]^{1/2}\,,
    \label{eqn:s0}
\end{equation}
where $\gamma$ is the angle between $\mathbf{S_{\rm b,*}}$ and $\Delta \mathbf{S}$, and
\begin{equation}
\Delta S = \frac{M_{\rm NS} R_{\rm kick} V_{\rm TR} \sin\alpha}{I_{\rm NS} \sin\beta}\,.
\end{equation}
Here, $\alpha$ is the angle between $\mathbf{R}_{\rm kick}$ and $\mathbf{V}_{\rm kick}$, and $V_{\rm TR} = V_{\rm kick} \sin\beta$ to correct for the fact the we only measure the 2D transverse velocity of pulsars (in Galactic coordinates), $V_{\rm TR}$, with $\beta$ being the projection angle. Hence, if pulsars receive an off-center kick, there should exist a correlation between their period at birth and the magnitude of the natal kick velocity.

Note that we observe pulsars not right after they are born, rather at some time after their birth. Therefore, we need to account for the fact that pulsars spin down during their lifetime as a result of energy emission through dipole magnetic braking \citep{GoldreichJulian1969,Sturrock1971}. The spin of a neutron star at birth, $P_0=2\pi/S_0$, is related to the its spin, $P$, at some time $\tau$ after birth through
\begin{equation}
    \frac{P^2-P_0^2}{2} = P\dot{P} \tau\,,
    \label{eqn:pp0}
\end{equation}
where $\dot{P}$ is the rate of spin down. From observations we can only directly estimate the characteristic age
\begin{equation}
    \tau_{\rm ch} = \frac{P}{2\dot{P}}\,
\end{equation}
of a pulsar, which represents an upper limit to the pulsar true age. Introducing $\tilde{\tau} = \tau/\tau_{\rm ch}$, which is naturally defined in the range $[0-1]$, Equation~\ref{eqn:pp0} can be recast as
\begin{equation}
    P=\frac{2\pi}{S_0(1-\tilde{\tau})^{1/2}}\,.
    \label{eqn:fit}
\end{equation}
The above equation relates the observed pulsars spin and transverse velocity, and can be used to constrain the parameters of our model. 
