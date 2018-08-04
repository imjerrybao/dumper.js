<div align="center">
	<img src="https://i.imgur.com/JgbF61K.png" alt="dd() - Dump information about a variable">
	<br/><br/>
	<a href="https://travis-ci.org/zeeshanu/git-profile">
		<img src="https://img.shields.io/travis/zeeshanu/git-profile/master.svg?style=flat-square" alt="Build Status">
	</a>
	<a href="#">
		<img src="https://img.shields.io/teamcity/coverage/bt428.svg?style=flat-square" alt="TeamCity CodeBetter Coverage">
	</a>
	<a href="https://github.com/zeeshanu/git-profile/releases">
		<img src="https://img.shields.io/github/release/zeeshanu/git-profile.svg?style=flat-square" alt="Latest Version">
	</a>
	<a href="#">
		<img src="https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square" alt="Software License">
	</a>
	<br/><br/>
</div>

> `DD` is a better formatted alternative to JS's `console.log` functions. Dump an object and kill the process in node.js for quick debugging.

## Installation

Compatibility: `dd` requires Node >=6.0.0. It works best with Node >=10.

```bash
npm install --save dd 
# or
yarn add dd
```

## Usage

### Example

Calling `dd` will print the object in your terminal and kill the process.

```js
const dd = require('dd');

const users = [
    { user: 'barney', age: 36, active: true, createdAt: new Date(), getAge: () => this.age },
    { user: 'fred', age: 40, active: false, createdAt: new Date(), getAge: () => this.age },
    { user: 'pebbles', age: 1, active: true, createdAt: new Date(), getAge: () => this.age }
];

dd(users);
```

### Outputs:

![dd1](https://i.imgur.com/8eYdVN0.png)

### Example 

If you want to print multiple objects at once call `dd()` function like this:

```js
const dd = require('dd');

let baz = true;
let foo = ['a', 'b', 'c', 'a', 'b', 'c'];
let bar = [{ x: 1 }, { x: 2 }, { x: 3 }, { x: 1 }];

dd({foo, bar, baz});
```

### Outputs:

![dd2](https://i.imgur.com/XWeoEni.png)

## Test

To execute tests for the library, install the project dependencies once:

```bash
npm install
```

Then, the tests can be executed:

```bash
npm run test
```

## License

Copyright © Zeeshan Ahmed <ziishaned@gmail.com>. Please see [License File](LICENSE.md) for more information.
