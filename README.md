### Date Suite
For ~~decades~~decennia I'v been bothered by the assbackwards order that the date and time, or time and date, are written, no natter the culture that may order some of the date rationally.  At best, named dates were medially sorted—the American assinheadbackwards time locations on _Back to the Future_ not quite and always felt awkward.  The decennium earlier ISO 2014 in 1976 made dates shorten, but only numerically and professionally—I may recall stamped documents (library slips?) where the month was short named but in serial capitals like a fake dumb acroným in the ISO order but kids aren't made to reason about their cultural mores so the best ways don't become popular.  
I found the limited date and time customization of the Mac menu bar, Windows task bar, and file dates lame.  In the 20-00s I would rewrite/rearrange the PHP date format variables (tokens?) and separators on message boards I used to make sense.  One of the formats had  coloned numeric date, space, short weekday name, space, and dotted time.  The later used spaced short month named date instead which, with the short weekday name in the middle, was easiest to read and understand by this culture that mainly uses named months and weekdays.  
These applets rearrange Date() (now) so that the timestamp units shorten.
* Four-digit year, space, short month name, space, two-digit month, space, short weekday name, two-digit hour, colon, two-digit minute, colon, two-digit second, space, Z, offset sign, two-digit hour offset, two-digit minute offset, colon, short time zone.
  * The short time zone is made from the first three initials of the OS's civil time zone to be compact.  In four-word time zones this leaves out T for Time.
    * Thus time zones with the same offset and first three initials aren't unique in country-crowded longitudes.  See the Wikipedia list of what initialisms may stand for: [List of time zone abbreviations](https://en.wikipedia.org/wiki/List_of_time_zone_abbreviations).
* Date Sort puts your run timestamp on your clipboard.
* Date Preempt substitutes your clipboard with your paste timestamp.
  * Preempt is a pun of print, both verbs.
    * Preempt is not a valid verb in languages descended from this root, as this culture takes deverbal adjectives as verbs.
  * Regular copying is broken until the window is reloaded.
* Sign Preempt substitutes your MediaWiki ~~~~ signature with a nondisplayed ~~~~ signature, your ~~~ signature, and your paste timestamp.
  * The standard signature timestamp stays in the source to comply with bot duties.
  * Regular copying is broken until the window is reloaded.
 
### Installation
Make a bookmark/favorite with this code as the address:
##### Date Sort
```javascript:(()=>{let[D,M,d,y,t,O,L,S,T]=Date().toString().split(' ');navigator.clipboard.writeText(`${[y,M,d,D,t,'Z'+O.slice(3)+':'+L[1]+S[0]+T[0]].join(' ')}`)})()```
##### Date Preempt
```javascript:(()=>{onpaste=e=>{e.preventDefault();let[D,M,d,y,t,O,L,S,T]=Date().toString().split(' ');document.execCommand('insertText',true,[y,M,d,D,t,'Z'+O.slice(3)+':'+L[1]+S[0]+T[0]].join(' '))}})()```
##### Sign Preempt
```javascript:(()=>{onpaste=e=>{e.preventDefault();let[D,M,d,y,t,O,L,S,T]=Date().toString().split(' ');document.execCommand('insertText',true,' <s style=display:none>~~~~</s>~~~ '+[y,M,d,D,t,'Z'+O.slice(3)+':'+L[1]+S[0]+T[0]].join(' ')+'<!--GitHub/alysdexia/Date_Suite#Sign_Preempt-->')}})()```

### Preview
##### Date Preempt
If you had pasted at the Banda Aceh earthquake that shortend Earth's day by 7 μs: ```2004 Dec 26 Sun 07:58:53 Z+700:WIT```.
##### Sign Preempt
Pasting on a talk page, or wherever: ```<s style=display:none>~~~~</s>~~~ 2004 Dec 26 Sun 07:58:53 Z+700:WIT<!--GitHub/alysdexia/Date_Suite#Sign_Preempt-->```

### Development
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split
  * I didn't know about destructuring until months later so the comma operated array variables on the leftern split expression was a lucky try!  Also the MDN destructuring site is too long.
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice
* I only involved Google AI when needan the paste to use this code instead of whatever was on the clipboard.  This was mostly a bad time so I'll leave the log out.  Whenever Google AI has to speculate about new unwritten applications, the code is wrong more than 90% of the time.  When trying to restore the clipboard after a overridden paste, that gave me 23 snippets in a row that didn't work, often with repeat fake means.  If you know of a way that preventDefault() can be turned off, please tell me so that we don't need to reload the window after pasting.  When seeing whether a paste without preventDefault() could be redirected to void or null so that onpaste could write the timestamp on the next paste, that Google AI gave me 14 snippets in a row to paste to a real hidden layered div or something that didn't work.

### Other must-use applets
* [Type Sample](https://www.typewolf.com/type-sample), [Wayback](https://web.archive.org/web/20201203064635/https://www.typesample.com/) on Typewolf, names and previews fonts
* [Validate This Page](https://validator.w3.org/nu/about.html) on W3C, tests HTML
* My others, the simpler of which I found buried in [Wikipedia "Bookmarklet" history](https://en.wikipedia.org/w/index.php?title=Bookmarklet&action=history) deleted after decades and simplified:
  * [Text Count](https://github.com/alysdexia/Text_Count), counts pages, lines, words, numbers, digits, figures in selection
  * lastModified, says webpage date: ```javascript:alert(Date(document.lastModified))```
  * designMode, turns webpage into text editor: ```javascript:document.designMode='on'```
  * [Hue Shift](https://gighub.com/alysdexia/Hue_Shift), tints webpage colored elements 24 hues like +hue/-hue but better

### Must-see applets
* [clone slowly](https://www.squarefree.com/bookmarklets/testbrowsers.html#clone_slowly) on Jesse's Bookmarklets Site, simulates 1962–1976 dialup loading speed
* "[More Must-Have Bookmarklets Than You Can Swing a Browser At](https://lorelle.wordpress.com/2005/10/13/more-must-have-bookmarklets-than-you-can-swing-a-browser-at/)" on Lorelle on WordPress, list of lists of lists of lists of and lists of lists of bookmarklets, one of the sites deleted from Wikipedia

alysdexia
