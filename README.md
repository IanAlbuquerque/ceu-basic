# Developing a Beginner Friendly Graphic Library for Céu

<--
ACHO QUE NAO PRECISA
## About Céu

Céu is a programming language that targets system-level development of reactive systems.

The language is under development at the LabLua since 2011.

For a little introduction about Céu, please watch the video in our front page:

http://ceu-lang.org/

Céu appeared in "Future Programming" and "Curry-On" workshops:

http://www.future-programming.org/2014/program.html

http://curry-on.org/2015/sessions/structured-synchronous-programming.html
-->

## Brief Explanation

Currently, Céu has a binding for the SDL graphic library called Céu-SDL.

https://github.com/fsantanna/ceu-sdl

<!--
ACHO QUE NAO PRECISA
SDL is a C-based and cross-platform development library that provides access to audio, keyboard, mouse, joystick, and graphics hardware:

http://libsdl.org/
-->

However, even the basic tasks such as drawing a square on the screen requires a considerable amount of code and some computer graphics experience.

The goal of this project is to develop a beginner friendly graphic library in Céu with *Structured Synchronous Reactive Programming* in mind.
<!--It is desired to allow "a 12 year old student" to use the library with ease (NAO SEI SE EH PRA TANTO)--> <!--while not limiting the functionalities of more experienced users (TALVEZ SIM)-->
As an example, a program that traces a line pixel by pixel on every key press would look like as follows:

```
input void KEY;
output (int,int) PIXEL;

var int x = 0;
every KEY do
    emit PIXEL(x,10);
    x = x + 1;
end
```

## Tools

The most important tool that can be used as part of the implementation of the new graphic library is Céu-SDL, the binding of SDL for Céu.

https://github.com/fsantanna/ceu-sdl

This biding empowers the development of SDL applications in Céu with the following extensions:

- Awaiting events in direct/sequential style.
- Parallel lines of execution with
    - safe abortion;
    - deterministic behavior (in contrast with threads).
- Asynchronous loops for heavy computations.
- Seamless integration with standard SDL (e.g., `SDL_RenderFillRect`, `SDL_RenderPresent`, etc).

## Graphic Library References

Below you can find some references of libraries and projects in other languages that can be used as a reference when developing this project:


- `gfx`, a simple graphics library for CSE 20211. This library is meant to be simple and easy to learn, so that beginning CSE students can get right into the interesting parts of programming. The gfx library only requires that the programmer understand how to invoke basic C functions with scalar arguments.

https://www3.nd.edu/~dthain/courses/cse20211/fall2013/gfx/

- PICO-8 is a fantasy console for making, sharing and playing tiny games and other computer programs. When you turn it on, the machine greets you with a shell for typing in Lua commands and provides simple built-in tools for creating your own cartridges

http://www.lexaloffle.com/pico-8.php

## Expected results

It is part of the project the discussion and definition of the formal requisites and interface of the library.

However, it is expected some basic functionalities:

- Drawing pixels and basic primitives with colors on the screen
    - Pixels
    - Lines
    - Rectangles
    - Triangles
    - Circles

- Gathering input
    - From keyboard
    - From mouse

It is also expected a vast documentation of the library, including usage examples.

The library must be built to be used with *Structured Synchronous Reactive Programming* in mind. Specifically, it must work in conjunction with the core functionalities of Céu seamlessly.

The library must also be very simple in its default use. The very basic goal is to have a library that is very natural to learn and use while programming in Céu. The idea is for it to be "easy enough for a 12 y.o student to use".

With that in mind, we do not expect the library to do everything that a advanced programmer might want a graphics library to do.

One important milestone of the project is being able to rewrite programs in Céu that use Céu-SDL using only the graphic library being developed. One of those programs are:

https://github.com/fsantanna/ceu-sdl-storm

Once the basic goal is achieved, it is also possible to expand the functionalities of the library things such as:

 - Transforms
 - Assets, Images, Textures, Text
 - Cameras, Viewports
 - Audio

Overall, a good performance of the library is not essential - specially because the goal is to use it for simple projects. However, having good performance and developing with scalability in mind is a good "extra" goal to consider.

## Prerequisites

We expect the applicants to know *C* well and to develop minimum familiarity with the important tools before the project kicks off.

For this reason, we will ask the applicants to perform two activities *before* 
the application period:

1. Install Céu and Céu-SDL
2. Compile some existing Céu examples
3. Compile some existing Céu-SDL examples
4. Create a repository on *GitHub* and write some simple "Hello World" examples that demonstrates the basic understanding of Céu-SDL.

All those activities should be simple, i.e., nothing more than following tutorials  on the web.

## How to apply

* Get in touch: https://gitter.im/fsantanna/ceu-gsoc-2016
* Follow the official GSoC instructions.
* Follow the LabLua instructions.

## Skill level

Medium

## Mentor

Francisco Sant'Anna

http://www.ceu-lang.org/chico

