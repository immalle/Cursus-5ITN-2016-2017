bron: http://javascriptplayground.com/blog/2015/09/es6-arrays/ 

    ray = [1,2,3,4]
[1, 2, 3, 4]
    ray.find(2)
Uncaught TypeError: 2 is not a function(…)
    ray.find((x) => x > 2)
3
    ray.findIndex((x) => x > 2)
2
    ray = 10, 20, 30, 40, 50]
Uncaught SyntaxError: Unexpected token ]
    ray = [10, 20, 30, 40, 50]
[10, 20, 30, 40, 50]
    ray.find((x) => x > 2)
10
    ray.findIndex((x) => x > 2)
0
    ray.findIndex((x) => x > 20)
2
    // RETURNS first found element!
undefined
    ray.entries()
ArrayIterator {}__proto__: Array Iterator
    ray.entries().next()
Object {value: Array[2], done: false}done: falsevalue: Array[2]0: 01: 10length: 2__proto__: Array[0]__proto__: Object
    ray.entries().next()
Object {value: Array[2], done: false}done: falsevalue: Array[2]0: 01: 10length: 2__proto__: Array[0]__proto__: Object
    ray.entries().next()
Object {value: Array[2], done: false}done: falsevalue: Array[2]__proto__: Object
    // Een ezel stoot zich geen 3x aan dezelfde steen.
undefined
    var iter = ray.entries()
undefined
    iter.next()
Object {value: Array[2], done: false}done: falsevalue: Array[2]0: 01: 10length: 2__proto__: Array[0]__proto__: Object
    iter.next()
Object {value: Array[2], done: false}done: falsevalue: Array[2]0: 11: 20length: 2__proto__: Array[0]__proto__: Object
    iter.next()
Object {value: Array[2], done: false}done: falsevalue: Array[2]0: 21: 30length: 2__proto__: Array[0]__proto__: Object
    [...entries]
Uncaught ReferenceError: entries is not defined(…)
    console.log([...entries])
Uncaught ReferenceError: entries is not defined(…)
    console.log([...iter])
[Array[2], Array[2]]
undefined
    [...iter]
[]
    console.log([...iter])
[]length: 0__proto__: Array[0]concat: concat()constructor: Array()copyWithin: copyWithin()entries: entries()every: every()fill: fill()filter: filter()find: find()findIndex: findIndex()forEach: forEach()includes: includes()indexOf: indexOf()join: join()keys: keys()lastIndexOf: lastIndexOf()length: 0map: map()pop: pop()push: push()reduce: reduce()reduceRight: reduceRight()reverse: reverse()shift: shift()slice: slice()some: some()sort: sort()splice: splice()toLocaleString: toLocaleString()toString: toString()unshift: unshift()Symbol(Symbol.iterator): values()Symbol(Symbol.unscopables): Object__proto__: Object__defineGetter__: __defineGetter__()__defineSetter__: __defineSetter__()__lookupGetter__: __lookupGetter__()__lookupSetter__: __lookupSetter__()constructor: Object()hasOwnProperty: hasOwnProperty()isPrototypeOf: isPrototypeOf()propertyIsEnumerable: propertyIsEnumerable()toLocaleString: toLocaleString()toString: toString()valueOf: valueOf()get __proto__: __proto__()set __proto__: __proto__()
undefined
    let x = 2
undefined
    x
2
    var y = 3
undefined
    y = 2
2
    x == y
true
    let set = new Set([100,200,300])
undefined
    set
Set {100, 200, 300}size: (...)__proto__: Set[[Entries]]: Array[3]0: 1001: 2002: 300length: 3
    ray = Array.from(set)
[100, 200, 300]
    Array.from([10,20,30,40], (x) => x + 2)
[12, 22, 32, 42]
    Array.from({length: 4}, (val, key) => key)
[0, 1, 2, 3]
    Array.from({length: 4}, (val, key) => val+2)
[NaN, NaN, NaN, NaN]
    Array.from({length: 4}, (val, key) => val)
[undefined, undefined, undefined, undefined]
    Array.from({length: 4}, (val, key) => val.length*key)
Uncaught TypeError: Cannot read property 'length' of undefined(…)
    Array.from({bla:8}, (val, key) => 'a')
[]
    Array.from({length:8}, (val, key) => 'a')
["a", "a", "a", "a", "a", "a", "a", "a"]
