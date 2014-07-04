calmcard
========

**not-so-wild wildcard string matching**


Calmcard provides a simple string pattern matching with `*` as the only special character which is a placeholder for
any sequence of characters, unless it is escaped.

## Examples

* `foo*bar` will match "foo123bar"
* `foo\*bar` will match "foo\*bar" but not "foo123bar"

## Installation

Currently, calmcard is built for node.js and available via NPM.

    npm install calmcard

## Usage

```js
    var calmcard = require("calmcard");

    calmcard("foo*bar", "foo123bar"); // -> true
    calmcard("foo*bar", "foobar"); // -> false
```
