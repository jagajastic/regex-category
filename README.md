# Regex-category
Regular Expression symbol and meaning categorization

# TABLE 

####  Regular expression literal characters

<table border="1">

<tbody>

<tr>

<th>

Character

</th>

<th>

Matches

</th>

</tr>

<tr>

<td>

Alphanumeric character

</td>

<td>

Itself

</td>

</tr>

<tr>

<td>

<tt class="literal">\0</tt>

</td>

<td>

The NUL character <tt class="literal">(\u0000</tt>)

</td>

</tr>

<tr>

<td>

<tt class="literal">\t</tt>

</td>

<td>

Tab <tt class="literal">(\u0009</tt>)

</td>

</tr>

<tr>

<td>

<tt class="literal">\n</tt>

</td>

<td>

Newline (<tt class="literal">\u000A</tt>)

</td>

</tr>

<tr>

<td>

<tt class="literal">\v</tt>

</td>

<td>

Vertical tab (<tt class="literal">\u000B</tt>)

</td>

</tr>

<tr>

<td>

<tt class="literal">\f</tt>

</td>

<td>

Form feed (<tt class="literal">\u000C</tt>)

</td>

</tr>

<tr>

<td>

<tt class="literal">\r</tt>

</td>

<td>

Carriage return (<tt class="literal">\u000D</tt>)

</td>

</tr>

<tr>

<td>

<tt class="literal">\x</tt>_<tt><tt>nn</tt></tt>_

</td>

<td>

The Latin character specified by the hexadecimal number _<tt><tt>nn</tt></tt>_; for example, <tt class="literal">\x0A</tt> is the same as <tt class="literal">\n</tt>

</td>

</tr>

<tr>

<td>

<tt class="literal">\u</tt>_<tt><tt>xxxx</tt></tt>_

</td>

<td>

The Unicode character specified by the hexadecimal number _<tt><tt>xxxx</tt></tt>_; for example, <tt class="literal">\u0009</tt> is the same as <tt class="literal">\t</tt>

</td>

</tr>

<tr>

<td>

<tt class="literal">\c</tt>_<tt><tt>X</tt></tt>_

</td>

<td>

The control character <tt class="literal">^</tt>_<tt><tt>X</tt></tt>_; for example, <tt class="literal">\cJ</tt> is equivalent to the newline character <tt class="literal">\n</tt>

</td>

</tr>

</tbody>

</table>

####  Regular expression character classes

<table border="1">

<tbody>

<tr>

<th>

Character

</th>

<th>

Matches

</th>

</tr>

<tr>

<td>

<tt class="literal">[...]</tt>

</td>

<td>

Any one character between the brackets.

</td>

</tr>

<tr>

<td>

<tt class="literal">[^...]</tt>

</td>

<td>

Any one character not between the brackets.

</td>

</tr>

<tr>

<td>

<tt class="literal">.</tt><a name="IXT-10-57406"></a>

<a name="IXT-10-57406"></a></td>

<td>

Any character except newline or another Unicode line terminator.

</td>

</tr>

<tr>

<td>

<tt class="literal">\w</tt><a name="IXT-10-57407"></a>

<a name="IXT-10-57407"></a></td>

<td>

Any ASCII word character. Equivalent to <tt class="literal">[a-zA-Z0-9_]</tt>.

</td>

</tr>

<tr>

<td>

<tt class="literal">\W</tt><a name="IXT-10-57408"></a>

<a name="IXT-10-57408"></a></td>

<td>

Any character that is not an ASCII word character. Equivalent to <tt class="literal">[^a-zA-Z0-9_]</tt>.

</td>

</tr>

<tr>

<td>

<tt class="literal">\s</tt>

</td>

<td>

Any Unicode whitespace character.

</td>

</tr>

<tr>

<td>

<tt class="literal">\S</tt><a name="IXT-10-57409"></a>

<a name="IXT-10-57409"></a></td>

<td>

Any character that is not Unicode whitespace. Note that <tt class="literal">\w</tt> and <tt class="literal">\S</tt> are not the same thing.

</td>

</tr>

<tr>

<td>

<tt class="literal">\d</tt>

</td>

<td>

<a name="IXT-10-57410"></a><a name="IXT-10-57411">Any ASCII digit. Equivalent to <tt class="literal">[0-9]</tt>.</a>

<a name="IXT-10-57411"></a></td>

</tr>

<tr>

<td>

<tt class="literal">\D</tt><a name="IXT-10-57412"></a>

<a name="IXT-10-57412"></a></td>

<td>

Any character other than an ASCII digit. Equivalent to <tt class="literal">[^0-9]</tt>.

</td>

</tr>

<tr>

<td>

<tt class="literal">[\b]</tt><a name="IXT-10-57413"></a>

<a name="IXT-10-57413"></a></td>

<td>

A literal backspace (special case).

</td>

</tr>

</tbody>

</table>

####  Regular expression repetition characters

<table border="1">

<tbody>

<tr>

<th>

Character

</th>

<th>

Meaning

</th>

</tr>

<tr>

<td>

<tt class="literal">{</tt>_<tt><tt>n</tt></tt>_<tt><tt><tt class="literal">,</tt>_m_</tt></tt><tt class="literal">}</tt>

</td>

<td>

<a name="IXT-10-57419">Match the previous item at least _<tt><tt>n</tt></tt>_ times but no more than _<tt><tt>m</tt></tt>_ times.</a>

<a name="IXT-10-57419"></a></td>

</tr>

<tr>

<td>

<tt class="literal">{</tt>_<tt><tt>n</tt></tt>_<tt class="literal">,}</tt>

</td>

<td>

Match the previous item _<tt><tt>n</tt></tt>_ or more times.

</td>

</tr>

<tr>

<td>

<tt class="literal">{</tt>_<tt><tt>n</tt></tt>_<tt class="literal">}</tt>

</td>

<td>

Match exactly _<tt><tt>n</tt></tt>_ occurrences of the previous item.

</td>

</tr>

<tr>

<td>

<tt class="literal">?</tt>

</td>

<td>

<a name="IXT-10-57420"></a><a name="IXT-10-57421">Match zero or one occurrences of the previous item. That is, the previous item is optional. Equivalent to <tt class="literal">{0,1}</tt>.</a>

<a name="IXT-10-57421"></a></td>

</tr>

<tr>

<td>

<tt class="literal">+</tt>

</td>

<td>

<a name="IXT-10-57422">Match one or more occurrences of the previous item. Equivalent to <tt class="literal">{1,}</tt>.</a>

<a name="IXT-10-57422"></a></td>

</tr>

<tr>

<td>

<tt class="literal">*</tt>

</td>

<td>

<a name="IXT-10-57423">Match zero or more occurrences of the previous item. Equivalent to <tt class="literal">{0,}</tt>.</a>

<a name="IXT-10-57423"></a></td>

</tr>

</tbody>

</table>

####  Regular expression alternation, grouping, and reference characters

<table border="1">

<tbody>

<tr>

<th>

Character

</th>

<th>

Meaning

</th>

</tr>

<tr>

<td>

<tt class="literal">|</tt>

</td>

<td>

<a name="IXT-10-57437">Alternation. Match either the subexpressions to the left or the subexpression to the right.</a>

<a name="IXT-10-57437"></a></td>

</tr>

<tr>

<td>

<tt class="literal">(...)</tt>

</td>

<td>

<a name="IXT-10-57438">Grouping. Group items into a single unit that can be used with <tt class="literal">*</tt>, <tt class="literal">+</tt>, <tt class="literal">?</tt>, <tt class="literal">|</tt>, and so on. Also remember the characters that match this group for use with later references.</a>

<a name="IXT-10-57438"></a></td>

</tr>

<tr>

<td>

<tt class="literal">(?:...)</tt>

</td>

<td>

Grouping only. Group items into a single unit, but do not remember the characters that match this group.

</td>

</tr>

<tr>

<td>

<tt class="literal">\</tt>_<tt><tt>n</tt></tt>_

</td>

<td>

<a name="IXT-10-57439">Match the same characters that were matched when group number _<tt><tt>n</tt></tt>_ was first matched. Groups are subexpressions within (possibly nested) parentheses. Group numbers are assigned by counting left parentheses from left to right. Groups formed with <tt class="literal">(?:</tt> are not numbered.</a>

<a name="IXT-10-57439"></a></td>

</tr>

</tbody>

</table>

####  Regular expression anchor characters

<table border="1">

<tbody>

<tr>

<th>

Character

</th>

<th>

Meaning

</th>

</tr>

<tr>

<td>

<tt class="literal">^</tt><a name="IXT-10-57453"></a>

<a name="IXT-10-57453"></a></td>

<td>

<a name="IXT-10-57454"></a><a name="IXT-10-57455">Match the beginning of the string and, in multiline searches, the beginning of a line.</a>

<a name="IXT-10-57455"></a></td>

</tr>

<tr>

<td>

<tt class="literal">$</tt><a name="IXT-10-57456"></a>

<a name="IXT-10-57456"></a></td>

<td>

Match the end of the string and, in multiline searches, the end of a line.

</td>

</tr>

<tr>

<td>

<tt class="literal">\b</tt><a name="IXT-10-57457"></a>

<a name="IXT-10-57457"></a></td>

<td>

Match a word boundary. That is, match the position between a <tt class="literal">\w</tt> character and a <tt class="literal">\W</tt> character or between a <tt class="literal">\w</tt> character and the beginning or end of a string. (Note, however, that <tt class="literal">[\b]</tt> matches backspace.)

</td>

</tr>

<tr>

<td>

<tt class="literal">\B</tt><a name="IXT-10-57458"></a><a name="IXT-10-57459"></a>

<a name="IXT-10-57459"></a></td>

<td>

Match a position that is not a word boundary.

</td>

</tr>

<tr>

<td>

<tt class="literal">(?=</tt>_<tt><tt>p</tt></tt>_<tt class="literal">)</tt>

</td>

<td>

A <a name="IXT-10-57460"></a><a name="IXT-10-57461">positive look-ahead assertion. Require that the following characters match the pattern _<tt><tt>p</tt></tt>_, but do not include those characters in the match.</a>

<a name="IXT-10-57461"></a></td>

</tr>

<tr>

<td>

<tt class="literal">(?!</tt><a name="IXT-10-57462">_<tt><tt>p</tt></tt>_<tt class="literal">)</tt></a>

<a name="IXT-10-57462"></a></td>

<td>

A negative look-ahead assertion. Require that the following characters do not match the pattern _<tt><tt>p</tt></tt>_.

</td>

</tr>

</tbody>

</table>

####  Regular expression flags

<table border="1">

<tbody>

<tr>

<th>

Character

</th>

<th>

Meaning

</th>

</tr>

<tr>

<td>

<tt class="literal">i</tt>

</td>

<td>

Perform case-insensitive matching.

</td>

</tr>

<tr>

<td>

<tt class="literal">g</tt>

</td>

<td>

Perform a global match. That is, find all matches rather than stopping after the first match.

</td>

</tr>

<tr>

<td>

<tt class="literal">m</tt>

</td>

<td>

Multiline mode. <tt class="literal">^</tt> matches beginning of line or beginning of string, and <tt class="literal">$</tt> matches end of line or end of string.

</td>

</tr>

</tbody>

</table>

###  Perl RegExp Features Not Supported in JavaScript

<a name="jscript4-CHP-10-SECT-1.7"></a><a name="IXT-10-57472">We've said that ECMAScript v3 specifies a relatively complete subset of the regular expression facilities from Perl 5\. Advanced Perl features that are not supported by ECMAScript include the following:</a>

<a name="IXT-10-57472">*   The s (single-line mode) and x (extended syntax) flags

    *   The \a, \e, \l, \u, \L, \U, \E, \Q, \A, \Z, \z, and \G escape sequences

    *   The (?<= positive look-behind anchor and the (?<! negative look-behind anchor

    </a>
*   <a name="IXT-10-57472"></a>

    <a name="IXT-10-57472">The (?# comment and the other</a> <a name="IXTR3-107"></a><a name="IXTR3-108">extended (? syntaxes</a>

    <a name="IXTR3-108"></a>
