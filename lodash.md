#lodash

通过自学[lodash](),对lodash也有了初步的了解。

lodash一个[javascript]()库，也是[Node JS]()的常用模块，一开始是[Underscore.js]()库的一个fork，

主解决的是JavaScript中的数据转换、匹配、 查找，大大简化了我们对数据操作的复杂程度。

###“Array” Methods

####_.intersection([arrays])

#####作用

找到几个数组中共有的元素，并输出。

#####Example

```
_.intersection([1, 2, 3], [5, 2, 1, 4], [2, 1]);  
// → [1, 2]
```

####_.difference(array, [values])

#####作用

在第一个数组元素中删除与第二个数组相同的元素。

#####Example

```
_.difference([1, 2, 3], [5, 2, 10]);  
// → [1, 3]  
```

###_.drop(array, [n=1])

#####作用

输出删除的指定位置元素（默认值为1），如果为0则返回原数组。

#####Example

```
_.drop([1, 2, 3]);  
// → [2, 3]  

_.drop([1, 2, 3], 2);  
// → [3]  

_.drop([1, 2, 3], 5);  
// → []  

_.drop([1, 2, 3], 0);  
// → [1, 2, 3]  
```

###_.dropRightWhile(array, [predicate=*.identity], [thisArg])

#####作用

根据条件(users, 'active')，查找'user'中不满足条件的对象。 根据(users, { 'status': 'away' })，查找'user'中不满足条件的对象。

#####Example

```
_.dropRightWhile([1, 2, 3], function(n) { return n > 1; });  
// → [1]  

var users = [  
  { 'user': 'barney',  'status': 'busy', 'active': false },  
  { 'user': 'fred',    'status': 'busy', 'active': true },  
  { 'user': 'pebbles', 'status': 'away', 'active': true }  
];  

// using the "_.property" callback shorthand  
_.pluck(_.dropRightWhile(users, 'active'), 'user');  
// → ['barney']  

// using the "_.matches" callback shorthand  
_.pluck(_.dropRightWhile(users, { 'status': 'away' }), 'user');  
// → ['barney', 'fred']  
```

####_.zip([arrays])

#####作用

从两个数组的对应位置上取出数据并存放到新的数组中（一个位置一个数组）。

#####Example

```
var zipped = _.zip(['fred', 'barney'], [30, 40], [true, false]);  
// → [['fred', 30, true], ['barney', 40, false]]  

_.unzip(zipped);  
// → [['fred', 'barney'], [30, 40], [true, false]]  
```
