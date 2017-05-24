# Synapses (Design Language)

> Synapses serve as the communication between the heart (design) and the head (development).

Shared standardized design language which designers can create and developers can
understand.

-----

```
**DISCLAIMER:**

This is somewhat opinionated, and primarily related to web development and design.

Feel free to fork this and take and leave whatever fits your team best.
```

**Contents:**

> A\. [Why?](#why)
> > 1\. [Aims](#the-synapses-design-language-aims-to)  
> > 2\. [Common misunderstandings](#some-things-designers-and-developers-dont-always-realize-about-each-others-jobs)   
> > 3\. [How they can be resolved](#and-how-to-fix-them)
> 
> B\. [How?](#how)
> > 4\. [Breakpoints](#breakpoints)  
> > 5\. [Synapses Units](#synapses-units)  
> > **6\. [Synapses Design Language Specification](#synapses-design-language-specification)**  
> > 7\. [The Design Process with Synapses](#the-design-process-with-synapses)  
> > 8\. [The Development Process with Synapses](#the-development-process-with-synapses)  

-----

## Why?

### The **Synapses Design Language aims to:**

* **eradicate ambiguous designs** (i.e. prevent misinterpretation of a design)
* **improve the end product**
* **reduce the number of design drawings** per component
* make the process of **turning designs into code easier**
* **reduce technical debt**
* **reduce the back and forth** between design and development
* generally make design and development much **more efficient and fun**

### Some things designers and developers don't always realize about each others jobs...

1) Pixels values **aren't always helpful** for developers.
2) Few, if any, software products aimed at improving the design development process
   actually do for modern applications.
3) Flexible widths are **not** a complicated thing to communicate.
4) Some parts of design can and **should be** subjective decisions.
5) Some parts of design **should not be** subjective decisions.

### ...and how to fix them:

1) Four different simple unit types, easier than pixels for both design and development.
2) A simple visual communication language.
3) You can define 99% of flexible widths with 4 values.
4) Address which ones are.
5) Address which ones aren't.

-----

## How?

### Breakpoints

Breakpoints are practically always necessary in some form. 'Hamburger' menu icons
are practical on smaller device widths and impractical on larger device widths.

It follows that at least one breakpoint will be needed but often 2 or 3 are **needed**.

**However**, the aim of the design should be to share the design logic between
breakpoints where necessary. A new breakpoint doesn't always need every part of the
interface to change. This is often where display bugs and technical debt comes from.

**Additionally**, 'atoms' (the bottom layer of components) should change as little as
possible between breakpoints. It defeats much of the point of using them otherwise.

**_This means avoiding fixed units EXCEPT when the size would never be affected by the
screen's size._**

### Synapses Units

A **remainder** unit is one which just fills the remaining space. It has no 
associated number with it. It can be seen as having no 'unit'.

A **grow** unit is one that linearly grow with the screen. A searchbar may want a
minimum width and a maximum width, with the width dependent on the screen's width.

A **ratio** unit is used to group equal dimensions. It can also be used to say that one
size is always a certain percentage bigger than another. Every ratio needs at least
either a fixed unit or a remainder unit.

A **fixed** unit is a constant - px, rem, em, etc. Its size is fixed (i.e. independent
of the screen size).

![](http://i.imgur.com/YdHX7wq.jpg)

In this diagram:

* **black represents fixed** units (in px)
* **purple represents ratios**
* **orange represents a grow table**
* **remainders are invisible** (they're there if nothing else is)

### **Synapses Design Language Specification**

### The Design Process with Synapses

#### Component Design Philosophy

e.g. the **[Atomic Design Philosophy](http://atomicdesign.bradfrost.com/chapter-2/)**

The Component Design Philosophy is the ideology of breaking the interface into
progressively **smaller components**. In design this means **greater continuity**.
In development this means **less development time** and reduced time to make small but
widespread changes.

**Developers**, _think React components_, Angular components or reuse-heavy functional
style programming for the front-end.

**Designers**, _think Sketch symbols_, Illustrator symbols/groups, or duplicating
Photoshop layers.

**_DRY. Don't repeat yourself._** Componentized designs equals quicker designing,
quicker development and a more consistent result.

#### Mockups and/or Synapses Wireframes

#### Tools

### The Development Process with Synapses

#### What each unit means
