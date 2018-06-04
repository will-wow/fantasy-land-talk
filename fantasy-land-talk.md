---
title: Fantasy Land
author: Will Ockelmann-Wagner
...

# Fantasy Land

- A set of types for Haskell-like functional data structures in JS
- Some libraries export Fantasy-Land complient structures
- Others can work on Fantasy-Land complinet structures

# Why???

- Same reason as in Haskell
  - lets you write more abstract code

# What's with the name?

- Comes from a GitHub issue on the A-Plus Promises spec
- Someone suggested designing promises as monads
- This was the response:

# domenic commented on Apr 10, 2013

"Yeah this is really not happening. It totally ignores reality in favor of
typed-language fantasy land, making a more awkward and less useful API just
to satisfy some peoples' aesthetic preferences that aren't even applicable
to JavaScript."

https://github.com/promises-aplus/promises-spec/issues/94#issuecomment-16176966

# Which, honestly, is fair

# Things turned out okay 

- Promises stayed at their own weird almost-monad thing
- Brian McKenna announced Fantasy Land later in that GitHub thread

https://github.com/fantasyland/fantasy-land

# Simple example

- Ramda's map and folktale's maybe both implement Fantasy Land
- So this works:

```javascript
const Maybe = require('folktale/maybe');
import * as R from 'ramda';

const upperCase = R.map(R.toUpper);

upperCase(Maybe.Just('Good')); // Maybe.Just("GOOD")
upperCase(Maybe.Noting()); // Maybe.Nothing();

```

# Other functions

- Ramda - supports `ap`, `chain`, `lift`
- Sanctuary - more functions and data structures 
- Folk Tale - popular, lots of data types

