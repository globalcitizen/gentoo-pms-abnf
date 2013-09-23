Unofficial ABNF for the Gentoo Package Management Standard (PMS)
================================================================

Proof of concept!

Requirement
-----------
Maintaining any complex system means managing change over time.
One of the best class of tools for this purpose is the package
manager included in various systems. In Gentoo Linux's case,
this is called `portage`. Unfortunately, when integrating the
`portage` tool with other systems (such as automated build
systems), it became apparent to me that there was actually no
machine parseable specification to validate so central a unit
of the entire Gentoo system as package names and versions.
Since the developers-that-be decided this was not a problem
(and pointed to a non-machine parseable English language
technical document being developed for Gentoo as the *Package
Management Standard*, or PMS), I decided that the only thing
for it was to attempt to translate such in to a formal spec
myself. This repository represents the as yet partial result.

Goal
----
The idea is to generate useful code from the specifications
such that other platforms and systems can easily validate and
verify what is 'supposed' to be happening without having to
read a human-language technical document.

So far, we can generate regular expressions for a given entity
as well as generate test cases.

We also need to generate IETF standard ABNF, which will fix
the remaining bugs in the regex generation.  This is only
a question of converting strings to hex-encoded entities.

Ideally, we might get some acceptance of this 
approach (coupled with versioned releases) so that others
(package manager maintainers, systems integrators, etc.) can 
draw from a single formal specification ... removing an
entire class of potential bugs in every single package
related tool.


Dependencies
------------

 * `perl` and `ruby` are required for running some tests
 * A C compiler and `make` are required to compile the `abnfgen`
   utility that is used to validate the ABNF grammar.
