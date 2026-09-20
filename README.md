# Hodgkin-Huxley-HH-model
# 🧠 Hodgkin-Huxley Neuron Simulator

An interactive Python-based simulator of the Hodgkin-Huxley (HH) model for studying neuronal action potentials, ion-channel dynamics, and firing-frequency behaviour.

The project numerically solves the Hodgkin-Huxley equations using the Euler method and provides an interactive visualization interface built with Gradio and Plotly.

---

📌 Project Overview

The Hodgkin-Huxley model is a mathematical model that describes how neurons generate electrical impulses through the interaction of voltage-gated sodium and potassium ion channels.

This project implements the model from scratch in Python and allows users to interactively explore:

- Membrane voltage dynamics
- Sodium channel activation and inactivation
- Potassium channel activation
- Sodium and potassium conductances
- Action potential generation
- Repetitive neuronal firing
- Firing frequency as a function of applied current

The simulator provides adjustable parameters and real-time visualization of the model's behavior.

🎯 Objectives

- Implement the Hodgkin-Huxley model computationally using Python.
- Numerically solve the model using the Euler integration method.
- Study the gating variables **m, n, and h**.
- Visualize sodium and potassium channel conductances.
- Investigate action-potential generation under external stimulation.
- Analyze the relationship between applied current and firing frequency.
- Build an interactive interface for exploring neuronal dynamics.

🧬 Hodgkin-Huxley Model

The membrane voltage is governed by the current-balance equation:

$$
C_m\frac{dV}{dt}
=
-g_{Na}(V-E_{Na})
-g_K(V-E_K)
-g_L(V-E_L)
+I_{app}
$$

where:
V = Membrane potential 
C_m = Membrane capacitance 
I_{app} = Applied external current 
g_{Na} = Sodium conductance 
g_K = Potassium conductance 
g_L = Leak conductance 
E_{Na} = Sodium reversal potential 
E_K = Potassium reversal potential 
E_L = Leak reversal potential 

The ion-channel conductances are modeled as:

$$
g_{Na} = \bar{g}_{Na}m^3h
$$

$$
g_K = \bar{g}_Kn^4
$$

The gating variables represent the probability-related dynamics of voltage-dependent channel states:

- **m** → Sodium activation
- **h** → Sodium inactivation
- **n** → Potassium activation

Their dynamics are given by:

$$
\frac{dm}{dt} = \alpha_m(1-m)-\beta_m m
$$

$$
\frac{dh}{dt} = \alpha_h(1-h)-\beta_h h
$$

$$
\frac{dn}{dt} = \alpha_n(1-n)-\beta_n n
$$

---

⚙️ Numerical Method

The differential equations are solved using the **Euler integration method**.

For a variable $x$:

$$
x(t+\Delta t)=x(t)+\Delta t\frac{dx}{dt}
$$

The simulator allows the user to modify the time step through the interactive interface.

Default time step:

```text
0.01 ms
