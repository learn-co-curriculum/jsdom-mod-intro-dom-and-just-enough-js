# Intro DOM And Just Enough JavaScript

## Problem Statement

Once you understand how to write HTML and CSS, an exciting next step is to
learn JavaScript. That's where you are now!

JavaScript was _born_ in the browser. It was made to work with browser content.
JavaScript changes content through an intermediary called the DOM, the Document
Object Model. JavaScript and the DOM have been there, together, since the
beginning. Understanding the DOM manipulation is the _foundation_ of being a
front-end developer.

Because of they're twins, learning about the DOM will require us to write some
JavaScript &mdash; which we don't know yet! And learning all the details of
JavaScript language won't tell us anything about the DOM. It would just tell us
how to write valid JavaScript code. It's a chicken-and-egg situation.

This unit will teach you about the DOM, but we're going to equip you with some
_basic_ JavaScript first. Some of these lines of code you might not fully
understand at first and _that's OK_. We'll cover them _all_ later in more depth
when we discuss (*cue the trumpets*) The JavaScript Programming Language.

We take this approach because it's more fun. It's fun to change text on pages
or to change layout. Also, some of the JavaScript concepts tend to sneak in
along the way and make learning (*cue the trumpets*) The JavaScript Programming
Language easier. It's also the way you learned your native language. You
learned parents, food, "I want" and "No!" etc. before you learned "adjective"
and "noun." We want to teach you the [sight words][sight] of JavaScript.

It's OK to come back here if you get confused or forget something. You might
want to bookmark this page or keep it open in a tab as you move along.

## Objectives

1. List basic JavaScript code bits used when learning about the DOM:
2. Explain that JavaScript Has Things
3. Explain that JavaScript Has Variables
4. Explain that JavaScript Can Compare Things
5. Explain that JavaScript Has Collections
6. Explain that JavaScript Is Object-Oriented
6. Explain that JavaScript Is Has Loops

## List Basic JavaScript Code Bits Used When Learning About The DOM

## Explain that JavaScript Has Things

It might sound a bit weird to say, but there are "Things" in JavaScript. You
might have heard them called "types" if you've programmed before.

One type of Thing is a _Number_ like `2` or `3.14`.

Another type of Thing is an arrangement of characters, called a _String_ like
`"Byron"` or `'Please feed the dog'`. Strings are written inside of `"` **or**
`'`.

## Explain that JavaScript Has Variables

Sometimes you want to hold a `String` or a `Number` under another name.

> **TYPOGRAPHICAL NOTE** The `//=>` means "What JavaScript would return back".

```javascript
3.14 //=> 3.14
var pi = 3.14
pi //=> 3.14
```

JavaScript also lets you say:

```javascript
3.14 //=> 3.14
let pi = 3.14
pi //=> 3.14
```

or

```javascript
3.14 //=> 3.14
const pi = 3.14
pi //=> 3.14
```

When JavaScript first came out it had only `var`. Now it has `let` and `const`
too. We'll cover the differences between these later. They all tell JavaScript,
"Hey this is a name that I'm going to associate with some bit of information."

## Explain that JavaScript Can Compare Things

```javascript
1 < 3  //=> true
3 == 3 //=> true
3 != 4 //=> true
5 > 2  //=> true
```

Be careful here, `=` means "assign to," like we did with `var` just above. For
_comparison_ we use `==` (and, later on, `===`).

We can build on our previous example:

```javascript
3.14 //=> 3.14
const pi = 3.14
pi //=> 3.14
pi == 3.14 //=> true
```

## Explain that JavaScript Has Collections

Sometimes a _variable_ might point to a Thing which actually has multiple
Things inside of it. If you're familiar with programming, these collection
Things are called _arrays_. So technically, `Array` belongs with `String` and
`Number`.

```javascript
slytherins[0] //=> "Salazar Slytherin"
slytherins[1] //=> "Bellatrix Black"
slytherins[2] //=> "Draco Malfoy"
```

In JavaScript, _arrays_ start at `0`. In America, the floor where you walk in
is called the `1` floor (or first floor). In most of Europe and the rest of the
world, the floor where you walk in is called something else. Arrays are like
that, they start at `0`.

We can get one of the _elements_ of a collection by putting `[]` after a
collection's name and putting a number inside of the `[]`. In the example we
get the names of some wizards stored in a collection of wizard-names
(`Strings`).

## Explain that JavaScript is Object-Oriented

When working with the DOM in JavaScript, many of the Things are you meet are
_objects_. _Objects_ are bits of code you can talk to that know _state_ and
_behavior_. _Objects_ should round out our universe of JavaScript Things along
with `Array`s, `String`s, and `Number`s.

When talking to an _object_ you can ask it for a bit of _state_ by using a `.`
and then that _state's_ name. You can trigger _behavior_ by using a `.` and
then the _behavior's_ name followed by `()`. Due to the `.` being the separator
between the object-name and the state or behavior name, we call writing code
this way "dot-notation."

The thing that holds a bit of _state_ is known as a _property_. To ask, say, an
adorable poodle its "`name`" state, you would do it like so:


``` javascript
poodle.name //=> "Byron"
```

If you ask an object for a _property_ it doesn't have, JavaScript says
`undefined`

``` javascript
poodle.favoritePainter //=> undefined
```

When asking an object to _do_ something (a _behavior_),  you use a `.` and a
_behavior-name_ (usually a verb) followed by `()`.

```javascript
poodle.bark() //=> An ear-splitting bark is heard
```

Objects's _behaviors_ have access to all of that object's properties.

```javascript
poodle.introduceYourselfFormally() //=> "Hello, my name is Byron the poodle"
```

In this case the _method_ `introduceYourselfFormally` presumably looks at
`poodle`'s `name` property and writes some text around it. We might imagine
that it's returning `"Hello, my name is " + this.name + " the poodle"`. As it
turns out, that is **entirely valid JavaScript** and it is probably what's
happening!

Finally, _behaviors_ can take _arguments_. _Behaviors_ on objects are called
_methods_.  _Arguments_ change the _method's_ operation.

```javascript
poodle.eat(1) //=> "Byron eats 1 can of food"
poodle.eat(2) //=> "Byron eats 2 cans of food"
```

_Methods_ can take multiple arguments.

```javascript
poodle.eyeEnviously("Shack Burger", "$", 9.57)
// ==> "Byron eyes your Shack Burger enviously, hoping you will drop some, not caring the least that it cost you $9.57."
```

<figure>
  <img src="https://curriculum-content.s3.amazonaws.com/jsdom-mod/jsdom-mod-intro-dom-and-just-enough-js/poodle2.jpg" alt="Picture of IG:@byron_poodle_darling, who would like a snack" width="640" height="480">
  <figcaption><em>I'm more than behavior and state, I'm a burger-eating
machine!</em></figcaption>
</figure>

<br><br>
Here we can imagine JavaScript doing some calculations to turn the `Number`
`9.57` and `String` `$` into the new string `$9.57`. We can also imagine it
using the property of `name` to supply Byron.

A very important object when working with the DOM is called `document`.

## Explain That JavaScript Is Has Loops

Another key concept in most programming languages is the idea of "looping."
Sometimes you don't want to manually type something out multiple times, but you
want to perform some action "for each" element in a collection. That's where
looping comes in.

In this module, we'll be using a very common loop structure that' found in C,
C++, Java, PHP, and many other languages: The `for` loop.

Let's pull together several of the concepts of this document by coding that
"for each" character in the `slytherin` collection (or "`Array`"), we would
like the `harry_potter` object to invoke the `expelliarmus` method on the
wizard or witch who is passed in as an _argument_

```javascript

for (let i = 0; i < slytherins.count; i = i + 1) {
  harry_potter.expelliarmus(slytherins[i]);
}

```

The important thing to take away is the ability to "sight read" that `for`
invokes the idea of doing some repeating action for each element in a
collection. This will be explored further in our JavaScript programming
curriculum.

## Conclusion

In this lesson you've learned the "sight words" of basic JavaScript. You should
be able to reason about what code is doing when it works with the DOM in the
subsequent lessons. Don't forget the power of imagination! By looking at these
bits of code, you can _imagine_ that the code, written by humans just like you
_probably does something like..._. You might be surprised, but professional
developers try not to make their code surprising or "non-intuitive" as much as
possible. Guesses and imagination are a vital part of your toolkit!

[sight]: https://en.wikipedia.org/wiki/Sight_word
