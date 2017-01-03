---
layout: article
title: "Starting my computer science year: NAND2Tetris and my history with programming (Vlog #93)"
category: vlog
---

I started the free [NAND2Tetris](http://nand2tetris.org/) course on "building a modern computer from first principles", woohoo! (Detailed notes below.) But before that, I took a moment to reflect on my past encounters with programming and computer science in [today's video blog](https://www.youtube.com/watch?v=jb-WvIakDAg).

{% include toc.html %}

<iframe width="1280" height="720" src="https://www.youtube.com/embed/jb-WvIakDAg" frameborder="0" allowfullscreen></iframe>

I also created [a page for my 2016 plans](/2016/) so I'll have all my notes and ideas in one place. Yay, organization! Oh yeah, and I did finally get some sleep! I slept from maybe 8am to 11am, worked on my website and some other stuff, and then spent 2 hours starting NAND2Tetris.

## Starting NAND2Tetris

Right, so [NAND2Tetris](http://nand2tetris.org/) is a free course on "building a modern computer from first principles", and I can't wait to start! I heard about it a few years ago and I've always wanted to give it a try, but I never made the time. Now is the time!

**2:00pm:** First I watched this [intro video about the course](https://www.youtube.com/watch?v=IlPj5Rg1y2w). There's also a [NAND2Tetris Google Tech Talk](https://www.youtube.com/watch?v=IlPj5Rg1y2w) but it's an hour long, so I'll watch that one later. I will note that I loved this phrase from the video description: building a computer from first principles demonstrates "the supreme power of recursive ascent". Reminds me of [*Gödel, Escher, Bach*](http://amzn.to/1SqVRB8)! There's something magical about that idea, that in building a computer from the ground up, you might even get a glimpse into the nature of human consciousness. But that'll be a stretch for my imagination another day, when I'm feeling more flexible. For today, I just want to dive in and start this course!

The [first project](http://nand2tetris.org/01.php) is to build a bunch of logic gates within the hardware simulator. So first I have some reading to do!

## Project 1 reading list

- [Chapter 1 of *The Elements of Computing Systems*](http://nand2tetris.org/chapters/chapter%2001.pdf) (PDF) by Noam Nisan and Shimon Schocken
- [Appendix A: Hardware Description Language (HDL)](http://nand2tetris.org/chapters/appendix%20A.pdf) (PDF)
- [Hardware simulator tutorial](http://nand2tetris.org/tutorials/PDF/Hardware%20Simulator%20Tutorial.pdf) (PDF)
- And for an extra reference: [Hardware Description Language (HDL) Survivor Guide](http://nand2tetris.org/software/HDL%20Survival%20Guide.html) by Mark Armbrust

## Notes on Chapter 1

**2:18pm:** Oh boy, it starts with [Boolean algebra](https://en.wikipedia.org/wiki/Boolean_algebra) right away. Good thing I said I wanted to learn about computer science *and* math this year, because we're diving right into the math!

[Truth tables](https://en.wikipedia.org/wiki/Truth_table) are pretty! They list every possible combinations of input for a given function and the output for each set of inputs.

**2:22pm:** What are [tuples](https://en.wikipedia.org/wiki/Tuple)? Yikes, that's a deep rabbit hole! Lots of different uses in math, programming, linguistics... Yeah, let's not fall in there just yet. Moving on.

**2:25pm:** The Boolean operators are **And**, **Or**, and **Not**. I learned this once a long time ago! I like [these Venn diagram visualizations](http://www.columbia.edu/cu/lweb/help/clio/boolean_operators.html) of how they work. Anyone who searches for anything on the internet would benefit from knowing about Boolean operators! The notation borrowed form arithmetic is going to annoy me though, I just know it!

**2:28pm:** Wow, this book is dense. They just gloss right over the Boolean operators. The course said the only prerequisite was knowledge of a programming language, but they should also say that you better be comfortable with algebraic notation! Hmph. Well, it's a good thing I learned this once before. Otherwise I'd probably feel pretty lost right now.

**2:31pm:** Only in computer science is it OK to use "And" as a verb, haha! They talk about "And-ing" things together.

**2:33pm:** This paragraph on page 9 seems to be trying to prove why every Boolean function can always be expressed with the operators And, Or and Not. I know that's true, but I'm not satisfied with the explanation. So that's a question for later.

**2:39pm:** I like the table on page 10, which shows every possible Boolean function of two variables. So I guess a Boolean function is any combination of Boolean operators and terms (which are either *literals*, which I take to be numbers, or *variables*, which are representated by letters). They say that "the number of Boolean functions that can be defined over *n* binary variables is 2^2^n" -- that's 2 to the power of 2 to the power of *n*. Wow, we're already using nested exponents?! I am not comfortable with this! I guess I understand what it means, but I don't know *why* that statement is true.

**2:33pm:** New piece of trivia: Nor is shorthand for Not-Or, the negation of the result Or-ing two variables. And Xor is short for "exclusive Or". Cool!

I remember a joke about this: Bertrand Russell walks out of the hospital after his wife just gave birth to their child, and someone asks him: "Is it a girl or a boy?" His answer: "Yes." 

**2:51pm:** After reading more about the names of common Boolean functions and wasting a bit of time looking for more logic jokes, I started wondering *why* it's true that the Boolean operations (And, Or, and Not) can all be constructed out of nothing but the Nand function.

But I do understand the implication of this: once you have your Nand working, you can basically build a whole computer out of nothing but a whole bunch of Nand functions! That is downright magical! And I don't think it will ever seem less magical no matter how well I ever understand this stuff! Magical in the same sense that I feel it's magical that the universe exists or that there's any order or pattern to anything at all.

**2:57pm:** I didn't know that a "gate" simply means "a physical device that implements a Boolean function." Good to know! So functions, operators, expressions and all that jazz -- those are just theoretical terms. Gates come into the picture when you start to get your hands dirty.

Gates have a pin for every input and every output. And simple gates "are made from tiny switching devices, called *transistors*, wired in a certain topology designed to effect the overall gate functionality." I wonder what they mean by "topology" in this context. Also, they never said what they meant by "pins"!

**3:03pm:** I like how they explain why computer scientists don't have to worry about the details of implementation, only the theory. That's left to "the physicists and electrical engineers—bless their souls", haha! So they go on to say that primitive gates are [black boxes](https://en.wikipedia.org/wiki/Black_box) as far as computer scientists are concerned; let's not worry about *how* they work, as long as they do work. I both love and hate black boxes.

*Composite gates* are chains of *primitive gates*, and primitive gates are physical implementations of And, Or, and Not. I like this definition: "logic design is the art of interconnecting gates in order to implement more complex functionality, leading to the notion of composite gates." I wonder if there are still any logic designers, or if it's all automated by computers now?

**3:10pm:** I like the drawing on page 12 illustrating two ways to view gates: interface versus implementation. The interface (which is a term I've run across in object-oriented programming) is the black box version, showing only the inputs and outputs. The implementation shows how the thing actually works on the inside, how it's constructed. An interface can often be created through many different implementations, but *the interface is unique*. My new mantra for this afternoon: the interface is unique, the interface is unique. So far this all makes sense and it's a bit familiar to me from that Electrical Engineering 101 class I took some seven years ago.

**3:15pm:** Yay, we finally got to the part about *Hardware Description Language*, or HDL! Haha, HDL makes me think of cholesterol because my dad talks about it a lot. Anyway, so hardware designers test everything out using a computer simulation before actually manufacturing any physical devices. I used some sort of hardware simulation program once before, and I remember liking it! But I only used it through a visual interface, dragging and dropping logic gates onto the screen and drawing connectors between them. It was sort of like a (relatively boring) video game.

But here they say that HDL is a text-based representation for a design, consisting of a *header* section and a *parts* section. The header specifies the name of the chip and its inputs and outputs, and the *parts* section specifies how it's built. Then each of those parts is represented by a *statement* that describes how it fits into the design. Clear documentation (much like an API in the software world) is absolutely necessary.

The example on page 16 is a bit intimidating! Hmm. First a note on this quote: "the output of a Not gate is piped into the input of a subsequent And gate." This made me think of the use of the [pipe character](https://en.wikipedia.org/wiki/Vertical_bar) in command line interfaces (see [this page on the Unix pipeline](https://en.wikipedia.org/wiki/Pipeline_(Unix))), and now it makes so much more sense! (I just learned about that the other day from a friend and hadn't made the connection between the pipe character and an actual *pipeline*. So that's why they call it the pipe character, oh! Duuuuh!)

**3:29pm:** OK, let's get back on track. I got distracted by reading about Unix and Bash. Anyway, looking at this HDL stuff, I can see this is going to take some practice to get comfortable with! It really is like learning a new language! I feel an impulse to stop now because it looks scary. But let's press on.

**3:37pm** A *multipliexer* takes three inputs, one of which tell it which of the other two other inputs it should pass on as its output. A *demultiplixer* does it in reverse. I don't remember why these are useful, though.

**3:40pm:** A *bus* is a multi-bit array, but they don't say what that really means.

**3:42pm** I skimmed over a bunch of these descriptions of chips for now, but it will be a useful reference later.

I like this quote: "Similar to the role of axioms in mathematics, primitive gates provide a set of elementary building blocks from which everything else can be built."

## New concepts and jargon

- [Boolean algebra](https://en.wikipedia.org/wiki/Boolean_algebra)
- [Truth tables](https://en.wikipedia.org/wiki/Truth_table)
- Boolean operators: And, Or, Not
- Expressions
- Functions
- Operators
- Terms
- Literals
- Variables
- Canonical representation
- Gates: primitive and composite
- Pins
- Transistors
- Chips
- Logic design
- Interface versus implementation
- Hardware Description Language (HDL)
- "Recursive ascent"
- Multipliexer (mux)
- Demultiplexer (demux)
- Buses

## Questions

- What is a tuple?
- What does canonical representation actually mean?
- Why is it that the number of Boolean functions using *n* binary variables is exactly 2^2^n?
- Why exactly is it true that every Boolean expression can be expressed with the operators And, Or and Not?
- Why exactly can every Boolean operation be constructed from nothing but the Nand function?
- How do transistors work?
- What are pins in the context of logic gates?
- Are there still people who do logic design, or is it automated by computers?
- What is a bus as a multi-bit array?

## Next steps

My next task is to complete the first project in the course:  implement all the logic gates from Chapter 1, all built from Nand gates! In order to accomplish this, I'll need to assimliate a few different pieces of this puzzle:

- Install the [NAND2Tetris course software suite](http://nand2tetris.org/software.php), which includes a hardware simluator and a bunch of other things.
- Learn how to use the hardware simulator.
- Learn how to write HDL -- read [Appendix A](http://nand2tetris.org/chapters/appendix%20A.pdf) (PDF) sections A1 to A6 
- Complete part 1 to 3 of the [hardware simulator tutorial](http://nand2tetris.org/tutorials/PDF/Hardware%20Simulator%20Tutorial.pdf) (PDF).
- Figure out how to combine Nand gates into several other gates according to the project files at the end of Chapter 1.

I guess I won't be finishing this today, because I already used up my alotted 2 hours of study time (and I'm about to fall asleep)! But I'll pick up where I left off tomorrow.

## Time breakdown

- Video production time: 1 hour 13 min
  - Script writing/preparation: none
  - Filming/setup: 25 min
  - Video editing: 28 min
  - Publishing: 20 min
- Study time: 2 hours