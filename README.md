# cmaban

Cmaban is a minimalist dialect of Lojban.
Cmaban's primary design goal is to be simple.
Its secondary design goal is to be understandable to speakers of other dialects.

## Entities and tags

Let's translate "Jane runs to the market" into Cmaban:

```plaintext
fa la .djein. bajra seka'a lo zarci ku
```

Below is the (roughly) corresponding English translation of each part:

```plaintext
fa        la .djein. bajra
[runner:] [Jane]     [relation (explained later)]

seka'a         lo zarci ku
[destination:] [market]
```

Every Cmaban sentence consists of _entities_ and _tags_.
Entities are the "things"--people, places, circumstances, etc.
Tags describe the relationship between the entities.
A tag describes the role of the entity that comes after it in the sentence.

In the above example, the entities are:

- `la .djein.` - Jane
- `lo zarci ku` - the market

The tags are:

- `fa` - Assigns the "runner" role.
- `seka'a` - Assigns the "destination" role.

You should now understand every part of the given Cmaban sentence,
except the word `bajra`.
`bajra` is a _relation_.
We will explain relations in a future section.

## Another example

Let's translate "The bird flies to the nest" into Cmaban:

```plaintext
fa lo cipni ku vofli seka'a lo zdani ku
```

Once again, we'll break this down:

```plaintext
fa       lo cipni ku vofli
[flier:] [bird]      [relation (explained later)]

seka'a         lo zdani ku
[destination:] [nest]
```

In the above example, the entities are:

- `lo cipni ku` - the bird
- `lo zdani ku` - the nest

The tags are:

- `fa` - Assigns the "flier" role.
- `seka'a` - Assigns the "destination" role.

You should now understand every part of the given Cmaban sentence,
except the relation `vofli`.
We will explain relations in the next section.

## Relations

You may have noticed that the tag `fa` assigned different roles
in each of the two examples.
In the first example, it assigned the "runner" role.
In the second example, it assigned the "flier" role.

This is because `fa` assigns roles based on the current sentence's _relation_.

### Recall example 1:

```plaintext
fa        la .djein. bajra
[runner:] [Jane]     [relation]

seka'a         lo zarci ku
[destination:] [market]
```

The relation is `bajra`.
The definition of `bajra` is

```plaintext
x1 runs on surface x2 using limbs x3 with gait x4.
```

`fa` assigns the role of the current relation's `x1`.
For `bajra`, the `x1` is the thing that runs, so `fa` assigns the role of "runner".

### Recall example 2:

```plaintext
fa       lo cipni ku vofli
[flier:] [bird]      [relation]

seka'a         lo zdani ku
[destination:] [nest]
```

The relation is `vofli`.
The definition of `vofli` is:

```plaintext
x1 flies using propulsion means x2.
```

Since the `x1` of `vofli` is the thing that flies, `fa` assigns
the role of "flier".

### What about `x2`, `x3`, etc?

You can use `fe`, `fi`, `fo`, and `fu` to
assign the roles of `x2`, `x3`, `x4`, and `x5`, respectively.

For example, let's say "The dog runs on the street using its hind legs".
Translation:

```plaintext
fa lo gerku ku fe lo klaji ku fi lo rixtu'e ku bajra
```

Let's break this down:

```plaintext
fa        lo gerku ku
[runner:] [dog]

fe          lo klaji ku
[surface:] [street]

fi       lo rixtu'e ku bajra
[limbs:] [hind legs]        [relation]
```

Recall that the definition of `bajra` is

```plaintext
x1 runs on surface x2 using limbs x3 with gait x4.
```

Thus:

- `fa` assigns the "runner" role
- `fe` assigns the "surface" role
- `fi` assigns the "limbs" role.
