---
title: "4 Division by zero Rant"
outputs: "Reveal"
---

{{< slide background="#555" >}}

## Computers CAN divide by zero they just HATE YOU

---

{{< slide background="#555" >}}

## What they want you to think

"Dividing by zero doesn't make logical sense."

"It's conceptually invalid"

"Division is defined as anti-multiplication. Since

```math
x / 0 = y 
```

cannot be undone with

```math
0 * y = x
```

it technically isn't division."

---

{{< slide background="#555" >}}

## The truth

LOOK AT THIS FUCKING GRAPH THE ANSWER IS SO OBVIOUS

```math
x/0=INFINITY
```

THERE! THE ANSWER! WASN'T THAT HARD WAS IT!

---

{{< slide background="#555" >}}

## Fun computer facts

The IEEE 754 standard for floating point numbers EXPLICITLY LISTS INFINITY AS THE RESULT OF A DIVIDE BY ZERO

Many programming languages follow this standard but specify divide by zero as `undefined behaviour` (meaning you can't rely on it).

Most IMPLEMENTATIONS of programming languages DO RETURN INFINITY but you can't RELY on it because the language itself is too COWED BY THE ESTABLISHMENT!

---

{{< slide background="#555" >}}

## In other news

I'm sick of writing

```code
try{
    return maths();
}catch(exception){
    oh no;
}
```

just because I DARED use one of the FUNDAMENTAL MATHEMATICAL OPERATIONS

---

{{< slide background="#555" >}}

just let me write this instead

```code
    auto result = maths();
    if(result.isNotValid()) oh no;
    return result;
```

or even better

```code
    return maths();
```

---

{{< slide background="#555" >}}

goddamn 8 year olds learn division why the fuck are we CHOOSING to embed a goddamn special case that doesn't need to be there

Computers need to stop SHITTING THE BED just because you DARED divide one number by another number

JUST RETURN INFINITY
