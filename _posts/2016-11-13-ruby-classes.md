---
layout: default
---
  Since I am admittedly somewhat of a masochist, I am going to give my
  vote for favorite mod 1 concept to the one that caused me the most
  confusion: Classes.

  When we were first introduced to the concept in class, I was immediately
  lulled into a false sense of security by the abstract nature of the
  term - it sounded like something straight out of philosophy class.
  I even latched on to the idea of the ruby Class being very similar
  to that of Plato’s idea of [Form](http://plato.stanford.edu/entries/plato-metaphysics/#5):

  > “A Form, then, is what it is in its own right in that it Is its
  > essence, and since the only thing it Is is its essence, each Form
  > is monoeides, ‘of one essence’. In virtue of Being its essence, each
  > Form Is something regardless of whether any particular does or even
  > may participate in it. Thus each Form is separate from every
  > particular instance of it.”

  The phrasing is even similar! Just as a ruby Class defines yet is
  separate from each particular object that it instantiates, the Form
  defines yet it separate from “from every particular instance of it.”
  Yesssss. I enjoyed my liberal-artsy cleverness and mentally stroked my
  nonexistent beard for about 5 min. before realizing that philosophy
  wasn’t really contributing to the technical understanding.

  I needed to know how to actually _use_ a Class. Was it a container?
  A blueprint? A object factory? An object instance factory?
  An organizational tool? A model? All of the above? None of the above?
  Options A, C, and D only? I kept trying on different ways to think about
  it but nothing seemed to fit. I was adding classes to my code because I
  knew that it was a pattern that I needed to follow, but I had no idea
  what it was actually doing other than providing a thematic wrapper
  or container for my methods.

  After one evening of desperation and floundering due to Still-Not-Getting-It, I decided to set aside my current project until I had a
  basic functional understanding of a class. In the course of my googling,
  I eventually came across a YouTube video that promised
  ["A Deep Dive into the Ruby Object Model”](https://www.youtube.com/watch?v=by5fFOBhtPQ).
  While I won’t pretend to have understood even
  half of what was covered in the video, believe me when I say that I
  enjoyed many “lightbulb” moments that evening as I discovered that
  there was actually some underlying structure to how Classes were
  represented internally in Ruby. In particular, knowing that a Class
  (at the C source code level) is made of references to tables containing
  the methods, instance variables, constants, and it’s parent (super)
  class finally forced me to see the Class as a legitimate structural
  object, rather than simply a vague organizational tool.

  Going back to my original ideas about how to use a class,
  I was actually on the right track but was simply missing the
  knowledge that there was an actual (but hidden) structure to support
  all of the ideas I had. Yes, a class is similar to a blueprint for
  constructing models of objects, BUT that metaphor only holds because a
  class holds data in the form of instance variables and constants, holds
  methods to interact with the data, and knows its place in the object
  hierarchy. In other words, the Class can act as a blueprint only because
  it literally holds the necessary pieces for creating or instantiating
  an object.

  Anyways, no doubt my understanding will continue to be refined as
  I continue to grow and learn as a ruby programmer. And I will continue
  to look for any and all available opportunities to
  relate - inappropriately or not - obscure philosophical
  concepts to programming.
