---
title: Code Structure Overview
date: 2025-03-18
---
this page will most likely be of no help to you

json contains a [rune type](rune_types.md)
somehow routes code to the corresponding class
parses the rest of the data into the class
	gets tag to see what the variable name is
	all the data inside it is added to that variable
		individual code for each datatype!!
		parse code all in one central function? each abstract class accepts json?
		each abstract accepts json
completed rune object is made
someplace needed to store all the runes

mixins dotted around, listen for events, check if any runes of that type exist?
	search for better method of this