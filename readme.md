# Principles of Writing Consistent, Flavored BEM Notation

The following document outlines a reasonable style guide for flavored BEM
notation. These guidelines strongly encourage the use of existing, common,
sensible patterns. They should be adapted as needed to create your own
style guide.

This is a living document and new ideas are always welcome. Please contribute.
Really.


## Preface

In order to get the most out of this style guide, it’s important to be
familiarized with [BEM](//bem.info/),
[Idiomatic CSS](//github.com/imbatta/idiomatic-css) and
[Idiomatic HTML](//github.com/imbatta/idiomatic-html).


## Table of Contents

1. [General Principles](#general-principles)
2. [Brief Introduction](#brief-introduction)
3. [Naming](#naming)
4. [Afterword](#afterword)

[Acknowledgements](#acknowledgements) & [License](#license).


<a name="general-principles"></a>
## 1. General Principles

<blockquote>
“Part of being a good steward to a successful project is realizing that writing
code for yourself is a bad idea. If thousands of people are using your code,
then write your code for maximum clarity, not your personal preference of how
to get clever within the spec.”
<br />
— <b>Idan Gazit</b>.
</blockquote>

<blockquote>
“Arguments over style are pointless. There should be a style guide, and you
should follow it.”
<br />
— <b>Rebecca Murphey</b>.
</blockquote>

<blockquote>
“The only programming project with no disagreement whatsoever on code
formatting is the one you work on alone.”
<br />
— <b>Jeff Atwood</b>.
</blockquote>

* You are not a human code compiler/compressor, so don’t try to be one.
* All code in any code-base should look like a single person typed it, no
  matter how many people contributed.
* Strictly enforce the agreed upon style.
* If in doubt when deciding upon a style, use existing, common patterns.


<a name="brief-introduction"></a>
## 2. Brief Introduction

__BEM__ is an acronym of _Block, Element, Modifier_. BEM is a
methodology developed at [Yandex](//www.yandex.ru/).

* __Block:__ an independent entity, a “building block” of an application. A
  block can be either simple or compound —containing other blocks.
* __Element:__ a part of a block that performs a certain function. Elements are
  context-dependent, they only make sense in the context of the block they
  belong to.
* __Modifier:__ a property of a block or an element that alters its look
  or behavior.

An extensive coverage about this methodology can be found in
[BEM’s website](//bem.info/).


<a name="naming"></a>
## 3. Naming

1. Always use lowercase to define class names.
2. If a standard HTML element already exist, use it as the class name
  —e.g. `img` rather than `image`.
3. If needed, a prefix could be used. It should be placed before the
  block or element name and separated by a hyphen.
4. In presence of compound names, words should be separated using a hyphen.
5. A block name only could be preceded by a prefix.
6. An element name if combined with a block name should be separated by a
  double underscore.
7. A block or element combined with a modifier should be separated by a
  double hyphen.

Example:

```css
.prefix-block {} /* A prefixed block. */
.block {} /* A unprefixed block. */
.block__element {} /* A block and an element combined. */
.block__element--modifier {} /* A block, an element and a modifier combined. */
.block--modifier {} /* A block and a modifier combined. */
```

Although BEM’s original methodology advices not to use descendant selectors,
shouldn’t cause much harm if used wisely —usually relying in the child
combinator AKA immediate child selector.

Don’t get clever, name in a sensible way. And always remember:

<blockquote>
“A class name should be as short as possible but as long as necessary.”
<br />
— <b>Jens Meiert</b>.
</blockquote>


<a name="afterword"></a>
## 4. Afterword

It doesn’t actually matter which code style is used in a code-base. What
really does matter is that everyone on the team sticks with those conventions
and uses them consistently.

So, if you’re editing code, take a closer look and determine its style. If
spaces are being used for indentation, use spaces; if single quotes are being
used for any given purpose, use single quotes too. Bottom line, do what is
being done. Period.

The whole point of having a style guide is to have a common vocabulary, so
people can concentrate on what you’re saying rather than on how you’re saying
it. If code you add to a file looks drastically different from the existing
code around it, it throws readers out of their rhythm when they go to read it.
Avoid this. __Be consistent__.


<a name="acknowledgements"></a>
## Acknowledgements

Inspired on [BEM](//bem.info/),
[Idiomatic CSS](//github.com/necolas/idiomatic-css),
[Idiomatic JavaScript](//github.com/rwldrn/idiomatic.js),
[Google HTML/CSS Style Guide](//google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml) &
many others.


<a name="license"></a>
## License

_Principles of Writing Consistent, Flavored BEM Notation_ is licensed under
[Creative Commons](//creativecommons.org/licenses/by/3.0/).
This applies to all documents in this repository.