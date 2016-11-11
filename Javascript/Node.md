- Use https://nodejs.org/api/fs.html

	> const fs = require('fs')
	undefined

import the fs module

	> fs.readdirSync()
	TypeError: path must be a string or Buffer
	    at TypeError (native)
	    at Object.fs.readdirSync (fs.js:951:18)
	    at repl:1:4
	    at sigintHandlersWrap (vm.js:22:35)
	    at sigintHandlersWrap (vm.js:96:12)
	    at ContextifyScript.Script.runInThisContext (vm.js:21:12)
	    at REPLServer.defaultEval (repl.js:313:29)
	    at bound (domain.js:280:14)
	    at REPLServer.runBound [as eval] (domain.js:293:12)
	    at REPLServer.<anonymous> (repl.js:513:10)

readdirSync expects a string-parameter

	> fs.readdirSync(".")
	[ '.git',
	  'Begrippenlijst',
	  'CSharp',
	  'Cmd.md',
	  'Excel',
	  'NodjesFiles.md',
	  'README.md',
	  'javascript-1' ]

Returns something that looks like an array of directory-entries (files and directories)

	> readFile=fs.readfileSync
	undefined
	> readFile("javascript-1")
	TypeError: readFile is not a function
	    at repl:1:1
	    at sigintHandlersWrap (vm.js:22:35)
	    at sigintHandlersWrap (vm.js:96:12)
	    at ContextifyScript.Script.runInThisContext (vm.js:21:12)
	    at REPLServer.defaultEval (repl.js:313:29)
	    at bound (domain.js:280:14)
	    at REPLServer.runBound [as eval] (domain.js:293:12)
	    at REPLServer.<anonymous> (repl.js:513:10)
	    at emitOne (events.js:101:20)
	    at REPLServer.emit (events.js:188:7)
	> fs.readfileSync("javascript-1")
	TypeError: fs.readfileSync is not a function
	    at repl:1:4
	    at sigintHandlersWrap (vm.js:22:35)
	    at sigintHandlersWrap (vm.js:96:12)
	    at ContextifyScript.Script.runInThisContext (vm.js:21:12)
	    at REPLServer.defaultEval (repl.js:313:29)
	    at bound (domain.js:280:14)
	    at REPLServer.runBound [as eval] (domain.js:293:12)
	    at REPLServer.<anonymous> (repl.js:513:10)
	    at emitOne (events.js:101:20)
	    at REPLServer.emit (events.js:188:7)

Made some typos. (`readFileSync` with camelCase).
	
	> readFile=fs.readFileSync
	[Function]

An alias for the function in the global environment, as a shortcut, to not use the `fs`-module.
This is handy for live interpretation of javascript code because it results in less typing and clearer code (?).

> Is it really such a good idea to make an alias for a function?
> After all, is `fs.readFileSync(".")` that much harder to type then `readFile(".")`.
> In stead, it reminds us that this is a *synchronous* operation, which, opposite to *asynchronous* operations,
> pauses the flow of the program and waits until the reading of the file is finished before executing the
> code on the next line!
>
> Well, it's probably indeed not such a good idea. But we do it anyway!
> We want to show you it is indeed possible, and in fact **very easy** to *copy* a function, a few lines
> of code execution. Just like it is obviously also very easy to copy variables, as in
```
var a = 3;
var b = a;
a = 5;
// What is b? 
// HINTS: 
// - assignment operator!
// - the top-down flow of this code-block (it's a *sequence*!)
```

Use the function (alias): 

	> readFile("javascript-1")
	<Buffer 76 61 72 20 61 20 3d 20 74 72 75 65 3b 0a 75 6e 64 65 66 69 6e 65 64 0a 76 61 72 20 62 20 3d 20 66 61 6c 73 65 3b 0a 75 6e 64 65 66 69 6e 65 64 0a 61 ... >

Apparently `fs.readFileSync('javascript-1')` returns a `Buffer` and also shows the first bytes (HEX numbers)...


# Buffers

Create buffers:

	> var b = Buffer.alloc(10)
	undefined
	> b
	<Buffer 00 00 00 00 00 00 00 00 00 00>
	> var b2 = Buffer.alloc(10, 2)
	undefined
	> b2
	<Buffer 02 02 02 02 02 02 02 02 02 02>
	> var ray = Buffer.from([1,2,3,4,5])
	undefined
	> ray
	<Buffer 01 02 03 04 05>
	> var tekst = Buffer.from("hello!")
	undefined
	> tekst
	<Buffer 68 65 6c 6c 6f 21>
	> var tekst = Buffer.from("hello!", 'utf-8')
	undefined
	> tekst
	<Buffer 68 65 6c 6c 6f 21>
	> // TODO: use utf-8 or utf-16 character
	undefined

Convert buffers:

	> tekst.toString()
	'hello!'

Convert a freshly created buffer to a string (which is a bit stupid to do,
actually, unless perhaps if you want to control the exact encoding like
'utf-8'.

	> var tekst = Buffer.from("hello!", 'utf-8').toString()
	undefined
	> tekst
	'hello!'


Put file contents into a buffer:

	> readFile=fs.readFileSync("javascript-1"
	... );
	<Buffer 76 61 72 20 61 20 3d 20 74 72 75 65 3b 0a 75 6e 64 65 66 69 6e 65 64 0a 76 61 72 20 62 20 3d 20 66 61 6c 73 65 3b 0a 75 6e 64 65 66 69 6e 65 64 0a 61 ... >

Put file contents into a buffer and convert it to a string, and assign it to a variable:

	> readFile=fs.readFileSync("javascript-1").toString()
	'var a = true;\nundefined\nvar b = false;\nundefined\na && a\ntrue\na && b\nfalse\na || b\ntrue\na\ntrue\nb\nfalse\na || b\ntrue\n!a\nfalse\n!b\ntrue\n3 +2\n5\n2 > 2\nfalse\n2 > 3\nfalse\n3 < 2\nfalse\nif(a) console.log("haha")\nhaha\nundefined\nif(b) console.log("hihi")\nundefined\n'

`readFile` is now not a function anymore. We could joke that `read` in
`readFile` is now past tense, because its meaning has changed, and consequently
its type has also changed!

In Dutch: 
1. `readFile` = leesFile (imperatief! werkwoord! actie!)
2. `readFile` = gelezenFile (data-opslag, log van wat uitgevoerd is, verleden tijd, voltooid deelwoord)


	> readFile
	'var a = true;\nundefined\nvar b = false;\nundefined\na && a\ntrue\na && b\nfalse\na || b\ntrue\na\ntrue\nb\nfalse\na || b\ntrue\n!a\nfalse\n!b\ntrue\n3 +2\n5\n2 > 2\nfalse\n2 > 3\nfalse\n3 < 2\nfalse\nif(a) console.log("haha")\nhaha\nundefined\nif(b) console.log("hihi")\nundefined\n'
	>



> readFile
'var a = true;\nundefined\nvar b = false;\nundefined\na && a\ntrue\na && b\nfalse\na || b\ntrue\na\ntrue\nb\nfalse\na || b\ntrue\n!a\nfalse\n!b\ntrue\n3 +2\n5\n2 > 2\nfalse\n2 > 3\nfalse\n3 < 2\nfalse\nif(a) console.log("haha")\nhaha\nundefined\nif(b) console.log("hihi")\nundefined\n'
> readFile.Split('\n')
TypeError: readFile.Split is not a function
    at repl:1:10
    at sigintHandlersWrap (vm.js:22:35)
    at sigintHandlersWrap (vm.js:96:12)
    at ContextifyScript.Script.runInThisContext (vm.js:21:12)
    at REPLServer.defaultEval (repl.js:313:29)
    at bound (domain.js:280:14)
    at REPLServer.runBound [as eval] (domain.js:293:12)
    at REPLServer.<anonymous> (repl.js:513:10)
    at emitOne (events.js:101:20)
    at REPLServer.emit (events.js:188:7)
> readFile.split('\n')
[ 'var a = true;',
  'undefined',
  'var b = false;',
  'undefined',
  'a && a',
  'true',
  'a && b',
  'false',
  'a || b',
  'true',
  'a',
  'true',
  'b',
  'false',
  'a || b',
  'true',
  '!a',
  'false',
  '!b',
  'true',
  '3 +2',
  '5',
  '2 > 2',
  'false',
  '2 > 3',
  'false',
  '3 < 2',
  'false',
  'if(a) console.log("haha")',
  'haha',
  'undefined',
  'if(b) console.log("hihi")',
  'undefined',
  '' ]
> readFile
'var a = true;\nundefined\nvar b = false;\nundefined\na && a\ntrue\na && b\nfalse\na || b\ntrue\na\ntrue\nb\nfalse\na || b\ntrue\n!a\nfalse\n!b\ntrue\n3 +2\n5\n2 > 2\nfalse\n2 > 3\nfalse\n3 < 2\nfalse\nif(a) console.log("haha")\nhaha\nundefined\nif(b) console.log("hihi")\nundefined\n'
> readFile.split('\n').filter(function(element, index, array) { return (index % 2 === 1) });
[ 'undefined',
  'undefined',
  'true',
  'false',
  'true',
  'true',
  'false',
  'true',
  'false',
  'true',
  '5',
  'false',
  'false',
  'false',
  'haha',
  'if(b) console.log("hihi")',
  '' ]
> readFile.split('\n').filter(function(element, index, array) { return (index % 2 === 0) });
[ 'var a = true;',
  'var b = false;',
  'a && a',
  'a && b',
  'a || b',
  'a',
  'b',
  'a || b',
  '!a',
  '!b',
  '3 +2',
  '2 > 2',
  '2 > 3',
  '3 < 2',
  'if(a) console.log("haha")',
  'undefined',
  'undefined' ]
> // LAST 3 are not good
undefined
> // DOC: Google "javascript show uneven indices of array"
undefined
> // LINK: http://stackoverflow.com/questions/7243355/how-do-i-extract-even-elements-of-an-array


## Coffeescript?

http://stackoverflow.com/questions/8119941/split-an-array-into-two-arrays-based-on-odd-even-position

## Typescript?


