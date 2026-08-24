
Tags: [[CODING]] [[THE ODIN PROJECT]]

---
# All types of 'console' features in Chrome.

1. Find code which modifies an element

- Find the element you want to look the code for in the Elements tab on the DevTools (F12)
- Right-click and go to 'Break on...'
- Select 'attribute modifications'

2 Regular
`console.log(<string>)`
Prints out <string> to the console.

3. Interpolated
   `console.log('Hello I am a %s string', <string>)`

- Behaves like the printf() function of the C language.
- '<string>' appears in place of %s

4. Styled

- `console.log('%c some text...', <css-string>)`
- It lets us style the first argument using css with '%c'
- <css-string> : `'background-color:red; border:5px solid black; box-shadow:brown;'`

5. Warning
   `console.warn(<string>)`

- Prints out <string> to the console with a yellow ! icon before it.

6. Error
   `console.error(<string>)`

- Prints out <string> to the console with a red X icon before it.

7. Testing
   `console.assert(<condition>, <string>)`

- If <condition> is false, <string> will be output to the console.
- eg:
  - `console.assert('2 > 3', 'This statement is wrong');` // 'This statement is wrong'
  - `console.assert('2 === 2', 'This statement is wrong');` // -no-output-

8. Clearing
   `console.clear();`
   Clears the console.

9. Viewing DOM elements (1)
   `console.log(<element>)`
   Prints out the <element> to the console along with its attributes and content.

10. Viewing DOM elements (2)
    `console.dir(<element>)`
    Prints out a drop-down list of properties and methods in <element>.

11. Groups
    `console.group(<string>)`
    `console.groupEnd(<string>)`
    Prints out a drop-down which groups a set of console.logs together. <string> must be the same to start and end the drop-down list.

`console.groupCollapsed(<string>)` 
By default, the drop-down will be printed out uncollapsed, use the method above than console.group to change this behaviour.

12. Counting
    `console.count(<string>)`
    Appends the number of times <string> has been printed out.

13. Timing
    `console.time(<string>)`
    `console.timeEnd(<string>)`
    Prints out how much time passed between time and timeEnd. <string> must be the same.

14. Table
    console.table(<array of objects>)
    Prints out a table of the objects' properties and values.

---

- Function v/s method
- Invoking or Calling a function. (what is Hoisting?)
- if You leave the parameter black i.e () , will it be taken as a truthy value ?
- Anonymous functions & Arrow functions, How to write these functions, when to use them, etc.
- SCOPE : explain it in as much detail as possible, with lots of examples... it's imporant and I don't know shit!




[[THE ODIN PROJECT]]
[[CODING]]
