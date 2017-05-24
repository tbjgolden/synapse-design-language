# Synapses (Design Language)

> Synapses are the _'bridge'_ between the heart (design) and the head (programming).

-----

**DISCLAIMER:**

This is somewhat opinionated, and primarily related to web development and design.

Feel free to fork this and take and leave whatever fits your team best.

-----

### Fundamentally, **this design language aims to:**

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
   actually do.
3) Flexible widths are **not** a complicated thing to communicate.
4) Some parts of design can and **should be** subjective decisions.
5) Some parts of design **should not be** subjective decisions.

### ...and how to fix them:

1) Four different simple unit types, easier than pixels for both design and development.
2) The pen is still mighty even now.
3) You can define 99% of flexible widths with 4 values.
4) Address which ones are.
5) Address which ones aren't.

-----

## Atomic Design Philosophy (aka Component Design)

The Atomic Design Philosophy is the ideology of breaking the interface into
progressively smaller components.

Developers, think React components, Angular components or Object-Oriented style
programming.

Designers, think Sketch symbols, Illustrator symbols/groups, or duplicating
Photoshop layers.

**DRY. Don't repeat yourself.** Componentized designs equals quicker designing and
quicker programming and a more consistent result.

## Breakpoints

Breakpoints are practically always necessary in some form. 'Hamburger' menu icons
are practical on smaller device widths and impractical on larger device widths.

It follows that at least one breakpoint will be needed but often 2 or 3 are **needed**.

Many websites have more than that; but the aim of the design should be to share the
design logic between breakpoints where necessary.

It means less code for developers to write, meaning faster results and less bugs and
technical debt.

**_This means avoiding fixed units EXCEPT when the size would never be affected by the
screen's size._**

## Units: (remainder, grow, ratio, fixed)

A **remainder** unit is one which just fills the remaining space. It has no 
associated number with it. It can be seen as having no 'unit'.

A **grow** unit is one that linearly grow with the screen. A searchbar may want a
minimum width and a maximum width, with the width dependent on the screen's width.

A **ratio** unit is used to group equal dimensions. It can also be used to say that one
size is always a certain percentage bigger than another. Every ratio needs at least
either a fixed unit or a remainder unit.

A **fixed** unit is a constant - px, rem, em, etc. Its size is fixed (i.e. independent
of the screen size).

[DIAGRAM]

## When should design 'come from the heart'?
## The Design Process
## The Development Process
