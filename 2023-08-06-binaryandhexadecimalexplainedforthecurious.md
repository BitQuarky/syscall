---
title: "binary and hexadecimal explained for the curious"
date: 2023-08-06
---
# binary and hexadecimal explained for the curious
	you might have accidentally opened an app with a text editor at some point, 
	maybe thought some file would be in plaintext but wasn't. Either way, you 
	probably saw something you didn't expect or atleast didn't understand- 
	characters that you can't type with your keyboard, 
	atleast not under normal circumstances.
## what is binary or hexadecimal anyways?
	to understand what binary or hexadecimal is your going to have to look inward first,
	not at yourself, but at the numbering system you've *hopefully* grown up with.
	this numbering system, over thousands of years of improvement and use,
	has been gratiously labelled '10-base' (or for non number-philes, '**dec**imal'),
	for the 10 characters that represent how many fish are in the tank,
	or how many friends you have, depending on who you ask. these are:
	(0, 1, 2, 3, 4, 5, 6, 7, 8, 9)
	and although most can count the number of friends they know from real life on their hands,
	the great mathematicians of the past (successors to the developer of the wheel)
	developed less popular means of counting the number of gold coins this loin cloth is worth,
	including base-40, which, you-guessed-it, has 40 characters representing 40 numbers
	(which gave 40 or more people who weren't astrologers headaches).
	and it is because of this that you are getting a headache looking at 1's and 0's right now.

	whether your counting how many AI services or loin cloths there are, your going to run into
	numbers that don't have a place in your base. Luckily, solutions have been around as
	long as these numerical systems have been used in practice. You've probably already counted
	beyond 9, but we need a way to describe how we arrive at 10, mathematically.
	
	essentially every digit after the first is like a remainder, or 'overflow', what you can't describe
	in just a single digit, so you move it over and start again. In the decimal system, you have
	10 possible characters representing ascending amounts of objects. every time you increase the overflow,
	it tells you that this number is equal to 9 + 1 + thefirstdigit. If we overflow twice (20), it tells us
	2(9 + 1) + thefirstdigit, so we can reduce this to a formula- o(base) + x. however, we can overflow
	the overflow digit, in this case, the tens digit, into the so-called hundreds digit.
	in this case, overflowing once tells us 1(9 + 1)^2 + 0(9 + 1) + 0, which can be further simplified:

### count = Dx(base^x) + ... D1(base) + D0

	we can reapply this to other bases to convert numbers or count in bases we're not used to.

	binary is 2-base, so to convert 0110

- count = 0(2^3) + 1(2^2) + 1(2^1) + 0
- count = 0 + 4 + 2 + 0
- count = 6
	 
## ON and OFF, TRUE and FALSE, 1 and 0?
	binary has been around for as long as computers have been reprogrammable
	(something like 70 years)
	and then some
	(something like 200 thanks to Boole),
	possibly even longer, but probably not in circulation since it is a
### 01110000 01100001 01101001 01101110
	or pain, in plain English.
	of course, most of that pain is from language speakers, both since computers don't feel pain,
	and it is actually more convenient for them.

	to understand why, we have to go back to the 19th century (or something like that)
	when Robert Boole created the most basic language that can describe whether or not you left the stove on,
	life, the universe, and everything. This was boolean math, and instead of 0 + 1 you just NOT FALSE.
	more specifically boolean involves taking a fact, 
	determining if it is TRUE or FALSE, 
	and doing something based on this, or a combination of statements.
	since these statements are only ever two values, it allows special operations, 
	NOT possible in regular mathematics, including:
	

 - **Not:** takes either TRUE or FALSE and flips it. If the ball is TRUEly red, then it is definitely NOT NOT red (a double negative)
 - **And:** takes two boolean values (TRUE or FALSE) and return TRUE only if both are TRUE.
 - **Or:** takes two boolean values, and if either one of them is TRUE, output TRUE
 

and we can arrive at other operations by combining these.

## so when do computers come into play?

	around the same time (as far as I'm concerned) Charles Babbage created the first device that computes-
	well- anything at all really. this first device, weighing tons, forged in true, dense copper alloys,
	sporting steampunker-style tubes for carrying punch cards as fast as possible (then), was- a calculator
	that's right, not even the cool kind you can type movie spoilers into! well it is called a computer,
	afterall.. unfortunately, this, and other devices by babbage, were huge, expensive disasters as far
	as his money was concerned, and it was only capable of calculating differences, far from
	the teams of mathematicians solving polynomials that he observed, which inspired this invention.
	fast forward a 130 years (give or take) though, and you will discover that these dreams are realized,
	sporting boolean math, interchangeable parts, capacitors, and transistors! 
	pure silicon, baby!

	since boolean math is simple and it can describe all things, it was a no-brainer to revive for modern
	computers. however, we introduced a few synonyms to true and false along the way. including on and off,
	and the fabled 1 and 0!
	
## why 1 and 0?

	computers, however analog, had existed and been in development (a bit more affordably) since the 1880s, 
	however, it wasn't until WWII that silicon and electricity had been used to- at the very least -speed up
	these expensive projects. As they became more powerful, and more widely used, one thing became clear- 	
	they need to be reprogrammable! for this to work, there would need to be:
	

 - interchangeable parts, which make manufacturing easier, less expensive, and less personal, courtesy of the industrial revolution
 - a measurable unit for memory, which can be worked on by
 - the processor, a part which is responsible for changing basic state, which should be standardized to some extent so that improvements can be made but the re-programmable elements (software) don't have to be rewritten for each new release and maintained independently (in case you don't upgrade to the newest AMD chip)  

this 'unit of memory' became

## the bit

	either 0 or 1, these babies describe everything that is on your screen,
	and this is only the tip of the iceberg!

	because it's hard to describe which letter comes next in just one bit, these units formed the basis
	for further measurements much like inch is to foot. these larger units are:

 - **the byte:** totaling 8 bits, you might have noticed earlier that for each letter in pain, there was one byte!
 - **the [double | quad | double quad, etc]word:** totaling two bytes (discounting modifiers), this unit was introduced for 16-bit computers, and is the basis for every other unit (as one might say, *word*.)

## using the bit

	by stringing bits together into bytes and words, we grow the possible combinations of 0's and 1's 
	exponentially. 8 bit's alone can represent numbers 0 through 255, and new 64-bit systems can
	have numbers as large as 2^64 (16 exobytes, which will be brought up again later). Unfortunately
	1's and 0's are the basic language of everything on your computer, but they aren't our
	basic language, so as computers were developing in the 60s, it became obvious that they
	would become useful to businesses and maybe even for individuals (wink wink), but not without
	'user friendliness'. the first step towards this would be to standardize a conversion from
	numbers to every character you now see on your keyboard, and then some. 
	Since a byte fits conveniently in the smallest and fastest area of memory a cpu can access 
	(that being the registers),
	and the total number of characters fits within that, 
	leg room for extended characters accommodated as well,
	one of the first standards for equating numbers to characters emerged, 'ASCII'.

	since then several others have surfaced, like unicode-[8 | 16], boasting other features,
	such as built in support for emojis, special characters, etc.
	however, ASCII remains one of the most widespread. oddly enough, ASCII places some special
	characters for return and NULL ('nothing') before the actual characters we type in with our keyboard.
	because of this, 1 and 0 are actually in the 40's on the ASCII scale!

	your text editor might have asked whether you wanted to open a file in binary or text mode at some point.
	this is because binary files do not go by ASCII standards- there are only two characters with a size
	equivalent to one bit each, but ASCII assumes there are 256 characters equivalent to 8 bit's each-
	opening in text mode would produce an unreadable mess of special and non-special ascii characters.
	Of course, when working with these binary files, it is practically more unreadable to look at binary.

	enter hexadecimal.

## the need for hexadecimal

	opening the aforementioned binary file may give a third option- hexadecimal view. You might notice
	that the editor has taken some liberties to separate every two digits by a space, maybe even separate
	every two or four sets by a line end.

	hexadecimal, as you might have guessed, is base-16: we take the usual decimal set from 0-9
	and simply represent 10-15 with A-F. All previous rules apply. Hexadecimal numbers are ideal 
	for representing large numbers due to it's high base. Since 64-bit devices have started to appear,
	there is a theoretical memory limit of 16 exobytes (I won't even list it in bytes, but you
	get the idea from it's cooler-than-usual modifier.) when we work with that as 'low-level'
	programmers, we end up having to actually address* and manipulate that, not to mention other
	large numbers. To simplify this, we use the hexadecimal system to represent these numbers.

	There are two particular reasons we use hexadecimal:

- it has total characters up to 2^4, which neatly aligns it with binary. your text editor uses this knowledge to condense every byte of the binary file (8-digits) into just two hex digits. Processor designers picked up on this and gave each instruction (hardware routines) a corresponding 2-digit hex code (so your text editor might go the extra step and look this up to tell you exactly what is in the code. This is effectively [disassembly](https://en.wikipedia.org/wiki/Disassembler)).
- it has a large base, so it can represent large numbers in fewer digits. The next base that would represent larger numbers AND be aligned to binary would be a base-32, which could not be easily represent-able or remember-able (alphanumerical - w, y, x, and z?)

for those curious, other systems have been tried with varying success, including a pretty useless octal (base-8).
 
 footnotes:

*:  see [memory address](https://en.wikipedia.org/wiki/Memory_address)
 
	
	
	
