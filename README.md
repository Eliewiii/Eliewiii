# Hi there, I'm Elie MEDIONI 👋

### Scientific Software Developer & Multidisciplinary Research Engineer

I stand at the intersection of **Applied Physics**, **Engineering**, and **High-Performance Computing**. My background spans a vast spectrum—from **Mechanical** and **Civil Engineering** to **CFD** and **Environmental Physics**.

For the past several years, I have not just applied numerical methods, but **architected the software ecosystems** required to solve them. I am now leveraging this deep domain expertise to build the next generation of high-performance urban simulation tools.

---

### 🏆 Engineering the Software Stack (Python Ecosystem)
*During my PhD, I architected a modular co-simulation framework to bridge the gap between CAD geometry and physical engines.*

**[BUA (Building Urban Analysis)](https://github.com/Eliewiii/BUA)**
* **The Platform:** A comprehensive ETL (Extract, Transform, Load) framework for urban geometry, bridging the gap between raw GIS/CAD data and physical simulation tools.
* **Real-World Application:** Developed as part of a research initiative with the **Israeli Ministry of Energy** to model **BIPV (Building Integrated Photovoltaics)** potential at the district scale.
* **Smart Boundary Conditions:** Implements geometric algorithms to automatically detect relevant boundary conditions for LWR and shading, utilizing an **equivalent view-factor configuration** to optimize simulation scope without compromising accuracy.
* **Integration:** Features automated Level-of-Detail (LOD) simplification and deep integration with **Ladybug Tools (LBT)**.

**[EP_LWR_coupled_simulation](https://github.com/Eliewiii/EP_LWR_coupled_simulation)**
* **The Middleware:** A co-simulation engine that synchronizes multiple independent **EnergyPlus** instances in real-time.
* **The Engineering:** Customized the EnergyPlus Python API to enable dynamic data exchange (surface temperatures) at every time-step using **virtual equivalent surfaces** to represent the urban context.
* **Rigorous Accuracy:** These virtual surfaces are designed to be **mathematically equivalent** to the complex geometry, ensuring **no loss in physical accuracy** while drastically reducing computational overhead.
* **Physics:** Solves the longwave radiative exchange between buildings using the **Radiosity formulation**, effectively turning isolated building models into a coupled urban district simulation.

**[View_Factor_Computation_With_Radiance](https://github.com/Eliewiii/View_Factor_Computation_With_Radiance)**
* **The Engine:** A high-throughput Python wrapper orchestrating the **Radiance** ray-tracing engine to compute View Factors ($F_{ij}$) for complex geometries.
* **Hybrid Optimization:** Drastically lowers computational load by using **geometric optimization** to filter significant interactions and substituting expensive ray-tracing with **analytical VF solutions** for equivalent configurations.
* **System Design:** Automates the generation of Radiance scene files (`.rad`) and manages parallel execution of ray-tracing subprocesses.

### 🔗 The Integrated Ecosystem
*From Raw Geometry to Physics-Aware Simulation*

Together, these packages function as a **seamless, fully automated pipeline**. They bridge the gap between static building model files and dynamic, **LWR-aware energy consumption analysis**.

By chaining the geometric optimization of **BUA** and **VF** with the **EP_LWR** middleware, the system achieves **acceptable computation times** even for complex scenes involving a few target buildings surrounded by **100+ simulated buildings** in the boundary conditions. This architecture makes advanced Longwave Radiation integration feasible for **real-world applications**, fitting natively into standard simulation workflows by leveraging and enhancing the industry-standard **EnergyPlus** engine without altering standard input/output structures.

---

### 🔄 Engineering Philosophy & Evolution
*From Academic Scripting to Production-Grade Software*

While my roots are in computational physics, I have **rigorously adopted industry-standard software engineering practices** to bridge the gap between research prototypes and maintainable industrial tools.

* **Best Practices:** I enforce strict **OOP architectures**, **Type Hinting**, and **Unit Testing** (pytest) across my recent Python packages (LWR, VF) to ensure reliability and maintainability.
* **DevOps Mindset:** I utilize **Git** for version control.
* **Current Development:** I am now expanding this engineering rigor into low-level systems programming, actively training in **Modern C++** and **HPC** to optimize memory management and parallelism.

---

### 🛠️ Technical Proficiency & Tools

**Core Competencies (Mastery / Production Level)**
* **Scientific Languages:** **Python** (Advanced Scientific Stack: NumPy, SciPy).
* **Python Parallelization:** Advanced Multiprocessing implementing **Shared Memory** architectures and **Synchronization Barriers** for real-time coupled simulations
* **Domain Physics:** Urban Thermodynamics, Radiative Transfer, Numerical Methods, Fluid Dynamics.
* **Software Engineering:** **Git**, Unit Testing, OOP Architecture.
* **Tools:** LaTeX.

**Functional Proficiency (Intermediate / Daily Driver)**
* **Languages:** **Modern C++** (C++17 STL), **FORTRAN** (Legacy Code Analysis & Solvers).

* **Systems:** **Linux** (Daily driving Arch/EndeavourOS), Bash Scripting.
* **Design:** **Grasshopper** & **Rhino** (Parametric Design).

**Active Learning Path (Training & Improving)**
* **Parallel Computing:** **OpenMP** (Shared Memory), **MPI** (Basic Distributed Memory).
* **GPU Computing:** Porting CPU algorithms to **HIP/CUDA** architectures.
* **Systems Architecture:** Advanced **Docker** containerization and orchestration for HPC workflows.

---

### 🏛️ Educational Background & Specialized Tools

  *  Specialized in **Finite Volume Methods**. Developed high-efficiency fluid solvers from scratch using **FORTRAN**, **OpenMP**, and **MPI** for parallel execution on HPC clusters.
  * Extensive use of **MATLAB** and **Python** for finite element analysis, continuous media mechanics, and algorithm prototyping.
  * Experience with a wide range of industry-standard simulation and visualization software, including **Ansys Fluent**, **Gmsh**, and **ParaView**, acquired through diverse academic projects.
  * Deep expertise in urban thermodynamics, radiative transfer, and building energy modeling.
  * Advanced scripting in **Grasshopper** (Intermediate) and **Rhino** for parametric design.


---

### 🚀 The HPC Roadmap: Refactoring for Scale
*I am currently refactoring these "Research Codes" into "Production HPC Systems" to handle city-scale simulations.*

* **⚡ Porting LWR to C++ & MPI:**
    * *The Logic:* The current Python co-simulation is limited by the Global Interpreter Lock (GIL). I am rewriting the solver in **Modern C++ (C++17)** using **MPI** to distribute the coupled buildings across compute nodes.
* **🎮 VF on GPU (HIP/CUDA):**
    * *The Logic:* Replacing the external Radiance process with a custom **GPU-native ray-casting engine** (using **HIP** for AMD hardware) to remove I/O bottlenecks and achieve real-time geometric analysis.
* **🐳 DevOps & Reproducibility:**
    * Building **Docker** containers to standardize the complex dependencies (EnergyPlus binaries, Radiance paths, Python libraries) into a single reproducible environment.

---

---

### 🎓 Degrees & Certifications

* **Ph.D. in Energy & Building Physics** | Technion - Israel Institute of Technology (2025)
* **M.Sc. in Computational Fluid Dynamics** | Université Paris-Saclay (2020)
* **M.Sc. in Computational Mechanics** | ENS Paris-Saclay (2020)
* **HPC & OpenACC Training** | IDRIS (Institute for Development and Resources in Intensive Scientific Computing).

---

### 📫 Connect with me
[![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/elie-medioni/)
