# cmaban

Cmaban is a minimalist dialect of Lojban.
Cmaban's primary design goal is to be simple.
Its secondary design goal is to be understandable to speakers of other dialects.

## Entities and roles

All languages are made up of _sentences_.
Every sentence involves one or more _entities_.
For example, consider the English sentence "Jane eats the apple because she's hungry".
The entities are:

- Jane
- the apple
- the fact that Jane is hungry

Each entity has a _role_ in the sentence.
In this case, the roles are, respectively:

- Jane: the eater
- the apple: the thing being eaten
- the fact that Jane is hungry: the reason

Observe that there are two kinds of sentence parts:

1. words that describe _entities_. In the example sentence, we have:
   - "Jane"
   - "the apple"
   - "she's hungry"
2. words that describe the _role_ of each entity. In the example sentence, we have:
   - "eats" - Describes the role of "Jane" (the eater) and "the apple" (the thing being eaten).
   - "because" - Describes the role of "I'm hungry" (the reason).

We will call phrases like "Jane" and "the apple" _entity phrases_.
We will call phrases like "eats" and "because" _role phrases_.

## My first Cmaban sentence

Let's translate our sentence to Cmaban:

```plaintext
fa la .djein. fe lo plise ku citka ki du la .djein. xagji
```

The entities phrases are:

- `la .jdein.` - Jane
- `lo plise ku` - the apple
- `du la .djein. xagji` - the fact that Jane is hungry

The role phrases are:

- `fa` - Assigns the "eater" role
- `fe` - Assigns the "thing being eaten" role
- `citka` - We'll explain this later
- `ki` - Assigns the "reason" role

Altogether:

```plaintext
fa       la .djein. fe       lo plise ku
[eater:] [Jane]     [eaten:] [apple]

citka
[explained later]

ki        du             la .djein.     xagji
[reason:] [the fact that Jane        is hungry]
```

## What is `citka`?
