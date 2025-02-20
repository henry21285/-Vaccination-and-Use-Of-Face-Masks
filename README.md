Mathematical modeling plays a crucial role in public health by helping policymakers integrate evidence, predict disease dynamics, and evaluate intervention strategies. This research examined the combined impact of face masks, quarantine, social distancing, and vaccination in managing infectious respiratory diseases. The basic reproduction number was determined using the next-generation matrix (NGM). Local stability was assessed through the Gershgorin Circle Theorem, while global stability was analyzed using the Quadratic Lyapunov Theorem. Sensitivity analysis was conducted with the normalized forward sensitivity index, and numerical simulations were carried out utilizing Python libraries such as **scipy**, **numpy**, and **matplotlib.pyplot**. Bifurcation analysis was performed based on the Center Manifold Theorem. The results indicated that although these interventions significantly reduced infection rates, they were not sufficient to entirely eradicate disease transmission. This study highlights the necessity of integrating multiple strategies simultaneously to effectively curb infectious disease spread and inform public health policies.
# Mathematical Model for Infectious Disease Transmission

## Population Compartments
The total human population at a given time, \(t\), denoted as \(N(t)\), is divided into eight mutually exclusive sub-populations:

- **Susceptible** \(S(t)\)
- **Vaccinated** \(V(t)\)
- **Exposed** \(E(t)\)
- **Quarantined** \(Q(t)\)
- **Asymptomatic but Infectious** \(A(t)\)
- **Symptomatic but Infectious** \(I(t)\)
- **Isolated (Hospitalized/Specialized Care)** \(J(t)\)
- **Recovered** \(R(t)\)

The total human population is given by:

\[ N(t) = S(t) + V(t) + E(t) + Q(t) + A(t) + I(t) + J(t) + R(t) \]

## Model Flow Chart
The model flow chart illustrating the transitions between compartments is shown below:![FLOWCHART](https://github.com/user-attachments/assets/a7bceccf-8774-40de-bacf-94822864945f)

## Description of Model Dynamics
- The **susceptible** population \(S\) increases at a birth rate \(\Lambda\).
- A fraction of the susceptible individuals are vaccinated at rate \(\alpha\), but vaccination does not provide full immunity. The vaccine efficacy is denoted by \(\theta\) where \(0 \leq \theta \leq 1\).
- Susceptible individuals become infected at a rate determined by the **force of infection** \(\lambda\).
- **Exposed** individuals are quarantined at a rate \(c\), and after a quarantine period \(z\), a fraction \(d\) of those who test positive are isolated, while the rest return to the susceptible population.
- After an incubation period \(g\), a fraction \(f\) of exposed individuals become asymptomatic, while the rest develop symptoms.
- **Asymptomatic** individuals recover at rate \(r_1\), while symptomatic individuals recover at rate \(r_2\).
- Some symptomatic individuals require hospitalization at rate \(\eta\) and later recover at rate \(r_3\).
- Recovered individuals lose immunity at a natural rate \(\delta\).
- A natural mortality rate \(\mu\) applies across all compartments.

---
This model provides insight into the impact of vaccination, quarantine, social distancing, and other control measures on the spread of infectious respiratory diseases.

