# "The Python & Calculus Bridge" 3-Week Sprint Learning Plan (Enriched Version v2.0)

**Philosophy**: This plan is not just a syllabus, but a learning system designed to maximize feasibility. It introduces concepts like a **Safety Pod, Quantified Milestones, a Learning Community, Templated Work, and Tiered Tasks** to transform an intense solo sprint into a structured experience with support, feedback, and motivation.

---

### **Week 0: Environment & Mindset Safety Pod (Preparatory Phase, ~3-4 hours)**

**Goal**: Clear all technical and psychological hurdles before starting, ensuring a smooth takeoff instead of burning out on the runway.

*   **Part 1: The Fail-Proof Installation Guide (1-2 hours)**
    *   **Task**: Strictly follow our **frame-by-frame screenshot guide for Anaconda installation**.
    *   **Purpose**: To eliminate the frustration that often comes from environment setup issues. A broken environment is a common reason beginners give up.

*   **Part 2: Your First Debugging Drill (1.5 hours)**
    *   **Task**: Open the `Week0_Debugging_Drill.ipynb` notebook. It contains several broken code cells. Your mission is to fix them and make them run. You'll encounter and solve common errors like `NameError`, `SyntaxError`, and `IndentationError`.
    *   **Purpose**: To learn by doing. Instead of just reading about errors, you'll actively solve them, turning red error messages from "scary warnings" into "helpful clues" from the very beginning.

*   **Part 3: Master Your Debugging Superpower: `print()` (0.5 hours)**
    *   **Task**: In the same notebook, learn to use the `print()` function to trace your code's execution flow and see the values of variables at different steps.
    *   **Purpose**: To master the simplest, most universally effective debugging method. This isn't just a function; it's a way to make the invisible processes of your code visible.

---

### **Week 1: Laying the Foundation - From Code to Images (20 hours)**

**Resource**: Download this week's **template notebook `Week1_Template.ipynb`**. It already contains all task titles and code frameworks, allowing you to focus on the core logic.
**Suggested Pacing**: 4-5 sessions of 4-5 hours each.

*   **Part 1: Environment & Basics (8 hours)**
    *   Learn the essentials of Jupyter Notebook and the Python language.

*   **Part 2: Plotting & Functions (12 hours)**
    *   Learn NumPy (`np.linspace`) and Matplotlib (`plt.plot`).
        *   **Mini-Bridge (Why NumPy?)**: Python's standard lists are flexible but slow for math. NumPy provides a powerful `ndarray` object, which is a grid of values, all of the same type. These arrays are stored in a contiguous block of memory, which allows NumPy to perform mathematical operations on the entire array at once (vectorization). This is orders of magnitude faster than looping through a Python list element by element.
    *   Learn Python functions (`def`).
        *   **Mini-Bridge (Why Functions?)**: Functions are the building blocks of larger programs. They allow you to bundle a set of instructions into a reusable block with a name. This practice, known as "abstraction," makes your code more organized, readable, easier to debug, and prevents you from repeating yourself (the DRY principle: Don't Repeat Yourself).
    *   **Practice**: Complete tasks like plotting quadratic and trigonometric functions.

*   **✅ Week 1 Milestone (Quantified Goal)**
    *   **Successfully export a `.png` image containing both `y=x^2` and `y=cos(x)` curves. The image must have a title, legend, and axis labels.**

*   **🚀 Share & Showcase (Learning Community)**
    *   **Task**: Share your milestone screenshot in the study group and briefly explain the toughest error you encountered this week and how you solved it.

*   **🏆 Challenger Task (Optional)**
    *   **Task**: Try plotting a polar coordinate graph, like the function `r = 1 - sin(θ)` (a cardioid). This will require you to learn the `plt.polar()` function.

---

### **Week 2: Deep Dive - Visualizing Calculus Concepts (20 hours)**

**Resource**: Download this week's **template notebook `Week2_Template.ipynb`**.
**Suggested Pacing**: 4-5 sessions of 4-5 hours each.

*   **Part 1: Visualizing Limits (8 hours)**
    *   Learn `for` loops and use code to practice the process of approaching limits for sequences and functions.

*   **Part 2: The Geometric Meaning of Derivatives (12 hours)**
    *   Learn and practice how to calculate the slope of a secant line with code and observe how it approximates the slope of the tangent line.

*   **✅ Week 2 Milestone (Quantified Goal)**
    *   **Design a computational experiment in a Jupyter cell. Your experiment will test the hypothesis that the secant line slope of `f(x)=x^3` at x=2 approaches the true derivative (12) as a second point moves from x=3 towards x=2. Print the slope at each step (e.g., for x=3, 2.5, 2.1, 2.01, 2.001) to demonstrate the convergence.**

*   **🚀 Share & Showcase (Learning Community)**
    *   **Task**: Record a 15-second short GIF (or share your Notebook file) showing how your secant line "rotates" into the tangent line's position.

*   **🏆 Challenger Task (Optional)**
    *   **Task**: Try to use code and graphs to explore and verify **Rolle's Theorem** or the **Mean Value Theorem**. For example, find the point where the derivative is zero within an interval and mark its horizontal tangent on the graph.

---

### **Week 3: Unlocking Superpowers - Symbolic Computation & Intro to Integration (20 hours)**

**Resource**: Download this week's **template notebook `Week3_Template.ipynb`**.
**Suggested Pacing**: 4-5 sessions of 4-5 hours each.

*   **Part 1: Symbolic Computation (10 hours)**
    *   Learn the `SymPy` library. Unlike NumPy which works with numbers, SymPy works with symbols. This allows it to perform exact, algebraic computations like finding derivatives or integrals analytically, just as you would by hand.

*   **Part 2: The Essence of Integration (10 hours)**
    *   Learn the concept of Riemann sums (approximating the area under a curve with rectangles) and visualize them using `plt.bar()`.

*   **✅ Week 3 Milestone (Quantified Goal)**
    *   **1. Use SymPy to successfully calculate the indefinite integral of `sin(x) * exp(x)`.**
    *   **2. Use Matplotlib to successfully plot the right Riemann sum for the function `f(x) = 4 - x^2` on the interval `[0, 2]` with `n=20` rectangles.**

*   **🚀 Share & Showcase (Learning Community)**
    *   **Task**: Share a screenshot of your Riemann sum visualization. Show the results for `n=5` and `n=50` side-by-side in one image to visually compare the difference in precision.

*   **🏆 Challenger Task (Optional)**
    *   **Task**: Explore **Taylor Expansions**. Try using SymPy to calculate the first few terms of the Taylor expansion for `f(x)=sin(x)` at x=0. Then, use Matplotlib to plot the original function and its Taylor approximations (e.g., 1st, 3rd, 5th order) on the same graph to observe how the approximation improves with more terms.

---

### **Final Project: The "Function Investigator" Notebook**

**Your Mission**: Choose one interesting function (e.g., `x * sin(1/x)`, `e^(-x^2) * cos(x)`, or one of your own). Your task is to create a comprehensive "investigation report" in a single Jupyter Notebook.

**Your Report Must Include**:
1.  **Visualization**: A high-quality plot of the function over a relevant interval, with labels and a title.
2.  **Symbolic Analysis**: Use `SymPy` to find its exact first and second derivatives.
3.  **Numeric Analysis**: Visualize the concept of the derivative by plotting the function and a tangent line at a specific point.
4.  **Integration**: Visualize the area under a portion of the curve using a Riemann sum with `n=50` rectangles.
5.  **Special Feature (from a Challenger Task)**: Incorporate the result of at least one challenger task you completed (e.g., show a Taylor expansion, plot in polar coordinates, or verify the Mean Value Theorem).

This project isn't just a summary; it's a capstone piece that proves you can use computational tools to deeply analyze and understand a mathematical object. It will be the best proof of your study and a powerful tool for your future courses.
