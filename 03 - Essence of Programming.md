# 03 - Essence of Programming

**Modules**

[01 - Intro](01%20-%20Intro.md)

[02 - Python in Engineering](02%20-%20Python%20in%20Engineering.md)

[03 - Essence of Programming](03%20-%20Essence%20of%20Programming.md)

[04 - The Community](04%20-%20The%20Community.md)

[05 - The Path](05%20-%20The%20Path.md)

# **The Essence of Computer Programming**

Hello and welcome back to video 3 of the Flocode Intro to Python Series. In this video, we're going to delve into some fundamental programming principles. 

I'd like to emphasize that this is not an in-depth exploration of coding or syntax. Instead, we'll take a high-level, fast-paced approach to provide you with an overview of the essential concepts in the beginner Python landscape. This will help you understand how the various components fit together, especially in an engineering context.

Don't worry if you're unable to grasp all the nuances of the syntax during this video, because I do provide some examples just to show you generally how things work. 

The primary goal is to introduce these concepts at a high level, planting the seeds in your mind and familiarizing you with the 50,000-foot view of Python programming. We'll dive deeper into the specifics in subsequent videos, but for now, let's focus on building a solid foundation for your journey into Python.

So let’s jump into it.

---

Finally I will cover some technical content. This is the essence of programming.

Computers are incredibly powerful tools, designed for one thing: solving problems.  As an engineer, you are fundamentally a problem-solver. You take in the complexities of terrain, the laws of physics, the constraints of materials, and you craft solutions – bridges that span valleys, structures that withstand the elements or roads to connect our communities.

A lot of what we discuss in this section will be familiar to you through the context of your current experience with existing tools like Microsoft Excel or Mathcad but these are also important fundamentals that we need to establish, as we relate them to Python.

Just as you wouldn't design a bridge without understanding the physics and mechanics involved, programming demands a new kind of engineering toolkit. Swap statics and dynamics for logic, algorithms, and data – this is how you shape the structure of your solutions. 

Python teaches you a whole new fluency for problem-solving, one where you dissect complex challenges into clear, computationally solvable steps, this leads us to our first core principle and one you’re already well versed in…

## Problem Definition & Decomposition

Just like any successful engineering project, the foundation of effective programming is clearly defining the problem. You wouldn't start pouring concrete before carefully surveying the site or calculating material requirements.  In the same way,  a computer needs precise instructions. It can't understand vague goals; it thrives on clarity and specificity.

Let's take the example of designing a beam to support a load. To a human engineer, that statement  implied a whole process with many steps and variables -  considering applicable codes, material options, beam geometry, and safety factors. A computer can't make those leaps intuitively.  We must reframe the problem in its language: "Given specific material properties, a defined load, a span length, and based on a certain set of sequential logic and algorithms, calculate the minimum required dimensions to satisfy code-mandated stress requirements."

The initial problem seems insurmountable to a computer. That's where decomposition comes in - the programmer's most  powerful tool. It's  the process of breaking down a large, complex problem into smaller, self-contained ones. Could we isolate the calculation of beam span? Can we define the loads separately? What about determining the section modulus needed to resist the bending moment? Each of these sub-problems is far more manageable for a computer to solve. I know this might sound very obvious, because you’re already familiar with this concept but abstracting this type of thinking to a variety of engineering problems can become quite nuanced so that’s why we’re beginning with the basics.

Think of programming like this: you translate the entire solution to your problem into a sequence of precise mathematical and logical operations. When the computer tackles each smaller task individually and combines the results, it effectively solves the complex problem you initially posed. 

I think you get it. 

Sounds so simple when I say it like that, and it certainly can be but usually it’s not!

## **Algorithms**

An algorithm is the heart of any program. It's a recipe that tells the computer exactly how to solve a problem or complete a task.  And just as a great recipe needs the right ingredients, it also needs the correct order of operations to be successful. You don’t put a pizza in the oven without the cheese. 

Think of a familiar engineering task: calculating the stress in an element. This is a simple fundamental formula with a single output:

```python
stress = force / area
```

Formulas directly calculate a single output. 

Algorithms can encompass multiple formulas, logic, and even create new formulas on the fly to adapt to input data.

We can turn this simple formula into an algorithm to make it a little more robust and useful.

For example, we can add a couple of bells and whistles, like a check to ensure the area is a positive value, and give a warning if not, then we add a printed output statement to verify our result.

```python
def calculate_stress(force, area):
    if area <= 0:
        return "Invalid area. Area must be greater than zero."
    return force / area

# Example usage
force = 100  # in Newtons
area = 0.5  # in square meters
stress = calculate_stress(force, area)
print(f"Stress: {stress} Pascals")
```

A formula is rigid. An algorithm can adjust its behavior based on conditions, making it more versatile.

The true power of algorithms comes in their versatility and repeatability.  Imagine needing to calculate bending moments at multiple points along a beam, or needing to modify the design to analyze different loading scenarios. Just as you might update a recipe by altering the quantity of one ingredient, you can change the input values for the algorithm (like the magnitude of the force), and the  computer will execute the same steps to produce a new answer.

Algorithms can manage intricate decision-making processes. Think of optimizing beam design: An algorithm could iterate through standard sizes or geometric configurations, assessing each against stress limits and weight.  If any option fails the check, the algorithm has rules in place to discard it and move on to the next check, by increasing the beam depth, web thickness or some other pre-defined parameter.

Algorithms are the building blocks of computational problem-solving. Once you grasp the idea of translating well-defined engineering problems into these step-by-step recipes, you open a powerful new chapter in your design and analysis capabilities. 

> **Crafting precise algorithms is an art, constantly seeking brevity and utility.**
> 

## **Variables**

Just like a physical toolbox holds your tools, variables are the storage units within your program for the data you need to solve problems. Consider them as customizable containers with the following key aspects:

- **Name:** Choose descriptive names that directly relate to the engineering concept they represent (e.g., 'beamLength', 'steel_grade', 'steel_density'). This makes your code self-documenting and easier to understand for yourself and anyone working with it.
- **Data Type:** Variables hold different types of data:
    - [Numbers](https://docs.python.org/3/library/stdtypes.html#typesnumeric) (for measurements, forces, etc.): Can be **integers** (whole numbers) or **floats** (with decimals)
    - Text (names, labels, ids, attributes): Use [strings](https://docs.python.org/3/library/stdtypes.html#text-sequence-type-str)
    - True/False Values (for logical conditions): Use [booleans](https://docs.python.org/3/library/stdtypes.html#boolean-type-bool)
- **Value:** This is the actual data the variable stores and can be changed throughout your program as calculations progress. This is a feature of a dynamically typed language.

**Why Variables Matter**

- **Flexibility:** Variables allow engineers to easily adjust and experiment with different parameters. Need to analyze multiple beam spans? Simply update the `beamLength` variable and rerun your calculations. Or even better, assign the variable `beamLength` to a list of beams with different lengths or a database of beams and their associated properties.
- **Readability:** Imagine trying to keep track of raw numbers in a complex formula. Well-named variables make your code much easier to understand and debug. We want to focus on the logic and the process, and not getting bogged down in the numerical data. This is the cornerstone of thinking Pythonically.
- **Organization:** Variables bring structure to your calculations. By assigning specific variables to forces, dimensions, material properties, and other relevant parameters, you can create a clear and organized framework for your analyses. This structured approach maintains a clear overview of your computational model and ensures that each component of the project is accounted for and can be easily adjusted as needed.

**Let's Bring This to Life with an Example:**

Say you're calculating the deflection of a simple beam with a load at the center.

The deflection formula is:

$$
\delta = \frac{\text{P} \cdot \text{L}^3}{48 \cdot \text{E} \cdot I}
$$

You might have variables like:

- `beamLength` (number, representing the length of the beam, L)
- `load` (number, representing the applied force, P)
- `youngsModulus` (number, representing the material's stiffness, E)
- `I` (number, moment of inertia, I)
- `deflection` (number, storing the final calculated result, Delta)

**Best Practices:**

- Choose meaningful names that reflect the engineering concepts.
- Be aware of data types and ensure your calculations use them correctly.

```python
# Beam Deflection Calculator, Load at Midspan
beamLength = 10  # meters
load = 100  # kN
youngsModulus = 200e9  # Pascals (for steel, as an example)
I = 4000e-6  # meters^4, example moment of inertia

# Calculate deflection
deflection = ((load * 1000) * beamLength**3) / (48 * youngsModulus * I)

print(f"Deflection: {deflection:.4f} meters")
```

Output:

`Deflection: 0.0026 meters` 

Variables are the fundamental building blocks to construct your algorithms but they are only one piece of the puzzle. How do we logically operate with all of these variables. That’s the next topic.

## **Operators, Logic, and Control**

Operators form the core of how you perform computations in Python. Basic arithmetic operators `(+, -, *, /)` let you work with numerical data for everything from structural analysis to fluid flow calculations. Beyond that, comparison operators `(>, <, ==, etc.)` allow you to test conditions essential for engineering decision-making: Is this load within safety limits?  Does this length exceed a certain value? Python's operators empower you to translate your engineering judgment into code that automates evaluation and actions.

**Logic: Programming Your Engineering Decisions**

Logic operators (and, or, not) allow you to build complex conditions that reflect real-world scenarios. Imagine selecting materials: is it strong enough AND cost-effective? Logic operators let you express these nuanced requirements within your code.  Conditional statements (if, elif, else) then direct your program's actions based on these evaluations. It's like embedding your problem-solving process into the program, guiding how Python should calculate different scenarios or generate design alternatives.

**Control: Shaping How Your Code Executes**

Control flow tools govern the order Python executes instructions.  Looping structures (for, while), let you iterate through calculations for every beam in a frame, or recalculate a model as design parameters change.  This makes repetitive yet crucial engineering tasks far more efficient. The ability to control execution lets you design code that aligns with how you think through engineering problems, automating steps to focus on the results, not the process.

**Arithmetic Operators**

| **Symbol** | **Description** | **Example** |
| --- | --- | --- |
| + | Addition | `x = 5 + 3 # x becomes 8` |
| - | Subtraction | `y = 10 - 2 # y becomes 8` |
| * | Multiplication | `area = length * width` |
| / | Division | `stress = force / area` |
| % | Modulus (remainder after division) | `remainder = 17 % 3 # remainder is 2` |
| // | Floor division (integer quotient) | `quotient = 25 // 6 # quotient is 4` |
| ** | Exponentiation | `volume = 4** 3 # volume is 64` |

**Comparison Operators**

| **Symbol** | **Description** | **Example** |
| --- | --- | --- |
| == | Equal to | `is_equal = (5 == 5) # True` |
| != | Not equal to | `not_equal = (10 != 2) # True` |
| > | Greater than | `x = (8 > 5) # x becomes True` |
| < | Less than | `y = (3 < 10) # y becomes True` |
| >= | Greater than or equal to | `z = (20 >= 20) # z becomes True` |
| <= | Less than or equal to | `a = (6 <= 8) # a becomes True` |

**Logical Operators**

| **Symbol** | **Description** | **Example** |
| --- | --- | --- |
| and | True if both operands are True | `x = (5 > 3) and (10 == 10) # x becomes True` |
| or | True if either operand is True | `y = (4 < 2) or (6 == 6) # y becomes True` |
| not | Inverts the logical value (True/False) | `z = not (10 == 5) # z becomes True` |

**Assignment Operators**

| **Symbol** | **Description** | **Example** |
| --- | --- | --- |
| = | Assigns value | `x = 10` |
| += | Adds and assigns | `x += 5 # same as x = x + 5` |
| -= | Subtracts and assigns | `y -= 2 # same as y = y - 2` |
| *= | Multiplies and assigns | `z *= 3` |
| /= | Divides and assigns | `area /= 2` |

There are more advanced operators but we will cover those when appropriate.

**Notes**

- **Precedence:** Python follows standard mathematical order of operations (PEMDAS/BODMAS: Parentheses, Exponents, Multiplication/Division, Addition/Subtraction).
- **Type Matters:** Operators might behave differently based on the data types of the operands. But this is a topic for another day.

## Closing

This whirlwind tour has covered the essentials. At this point, the concepts might still feel a bit abstract, like drawings without the completed building.

The principles we've discussed will translate directly into the fundamentals of Python code. As we progress through the Flocode Essentials course, these concepts will snap into focus with tangible examples from your engineering experience.

You'll see how to:

- **Automate tedious calculations**
- **Iterate through solutions**
- **Visualize and analyze data**
- **And much more…**

The best part is, as you learn to code, the way you view engineering problems themselves may even begin to shift.  It's a strange experience but it's certainly worth the effort based on my personal experience.

---

**Next:** [04 - The Community](04%20-%20The%20Community.md)