# Real Gas Law Simulator: Ideal vs. Van der Waals

*Overview*

This web application provides an interactive simulator to explore the differences between the behavior of an Ideal Gas (governed by the Ideal Gas Law) and a Real Gas (modeled by the Van der Waals equation of state).

It allows users to input thermodynamic and gas-specific parameters to calculate the resulting pressure and visualize the deviation from ideal behavior using the Compressibility Factor ($Z$).

*Features*

* **Dual Calculation**: Calculates pressure ($P$) using both the Ideal Gas Law and the Van der Waals equation simultaneously.

* **Custom Inputs**: Adjustable parameters for:

* **Moles** ($n$)

* **Temperature** ($T$)

* **Volume** ($V$)

* **Van der Waals constant** $a$ (related to intermolecular attraction)

* **Van der Waals constant** $b$ (related to molecular volume/repulsion)

* **Visualization**: A dynamic plot of the Compressibility Factor ($Z$) vs. Pressure ($P$).

* **Real-time Results**: Displays instant pressure outputs and updates the plot upon calculation.

* **Input Validation**: Checks for physically impossible conditions (e.g., Volume $\le n \cdot b$).

*The Science Behind the Simulation*

**1. Ideal Gas Law**

The simplest equation of state, based on the assumption that gas particles have negligible volume and no intermolecular forces.

$$PV = nRT$$

**2. Van der Waals Equation** (Real Gas)

This equation modifies the Ideal Gas Law to account for the finite size of molecules and the attractive forces between them, using two gas-specific constants, $a$ and $b$.

$$\left(P + a\left(\frac{n}{V}\right)^2\right)(V - nb) = nRT$$

**3. Compressibility Factor** ($Z$)

The primary measure of deviation from ideal behavior is the Compressibility Factor:

$$Z = \frac{PV}{nRT}$$

* **For an Ideal Gas**, $Z$ is always equal to 1.

* **For a Real Gas**:

    * When $Z < 1$, attractive forces (constant $a$) dominate, making the gas more compressible than an ideal gas.

    * When $Z > 1$, repulsive forces (constant $b$) dominate, making the gas less compressible than an ideal gas.

*Technology Stack*

This project is implemented as a single, self-contained HTML file:

* **HTML5**: Structure and content.

* **Tailwind CSS**: Modern, utility-first styling for a responsive, clean interface.

* **JavaScript (Vanilla)**: Core logic for calculations, input handling, and data generation.

* **Chart.js**: Used for generating the interactive and responsive $Z$ vs $P$ line plot.

*How to Use*

**1. Set Parameters**: Enter values for $n, T, V$, and the Van der Waals constants $a$ and $b$ (default values for Oxygen are pre-filled).

**2. Calculate**: Click the "Run Simulation & Plot" button.

**3. Review Results**:

  * The calculated pressures ($P_{ideal}$ and $P_{real}$) will be displayed.

  * The $Z$ vs. $P$ plot will update, showing the real gas isotherm relative to the ideal gas line ($Z=1$).

**4. Explore Deviations**: Adjust the temperature ($T$) or constants ($a$ and $b$) to see how these factors shift the real gas behavior.
