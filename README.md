js-continuedfraction
====================

Continued fraction calculator for the web

Usage
-----

Enter a decimal or a math expression on the left.  The
continued fraction coefficients will appear on the right
and a pretty-printed list of convergents as well as a
pretty-printed continued fraction will appear 
(courtesy of MathJax).

Alternatively, you may enter a comma-separated list
on the right and the decimal approximation along with
all convergents will appear on the left.


API
---

Including `js-continuedfraction.js` will add the `ContinuedFraction`
object to global scope.  You can create continued fractions with

	frac = new ContinuedFraction(<decimal>);
	frac = new ContinuedFraction(<list of ints>);


There are also several utility functions supplied

  * `ContinuedFraction.evaluateMath` evaluates a string expression
as math (including powers with ^ (like `2^3`) and constants like
`pi`, `phi`, and `e`.
  * `ContinuedFraction.MathFunctions` the object containing all math
functions available to `evaluateMath`.
  * `ContinuedFraction.inputbox` utility to create linked and
dynamically updating continued fraction views in either
decimal or continued fraction coefficient list views.


*Usage of `ContinuedFraction.inputbox`*

Arguments: object with properties

	decimalInput: the `<input/>` where you type a decimal number
	continuedFractionInput: the `<input/>` where you type a cf comma separated list
	updateCallback: the function to be called whenever the cf is changed
	createInputs: bool specifying if you'd like `<input/>` to be created for you

Returns: object with properties

	fraction: the ContinuedFraction object
	decimalInput: the `<input/>` for decimals or `null`
	continuedFractionInput: the `<input/>` for cf or `null`
	inputs: the parent element of the inputs or `null`
 

