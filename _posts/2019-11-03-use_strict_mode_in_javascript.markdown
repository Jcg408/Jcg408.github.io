---
layout: post
title:      "Use Strict Mode in JavaScript"
date:       2019-11-04 01:01:35 +0000
permalink:  use_strict_mode_in_javascript
---


Strict Mode is  a feature of JavaScript which was released with ES5. When enabled, strict mode restricts a program to be run in a 'strict' context. Goodbye sloppy code! 

JavaScript will allow bad code practices without throwing an exception or error. This may cause problems later in the development of the program, which means more time spent fixing a problem which could have been identified earlier.

To enable strict mode you can type 'use strict' either at the top of the file to restrict the entire script, or you may add it to a function to be used within that context. That's all you need to do to get these benefits:

1. Strict mode removes silent errors by actually throwing errors.
2. Fixes mistakes which affect optimization which may improve runtime over non-strict mode
3. Restricts certain syntax such as undeclared variables and accidental creation of global variables.
4. Secure code and cleaner code

It is a good habit to have 'use strict' in the script. I use strict mode along with a linter. Sometimes, the brain and fingers are not in agreement so it is appreciated when these errors are caught early.  ESlint, JSlint, JShint and others are 3rd party linters which are suggestive, and may have an option to enable strict mode but they are also suggestive programs which have different opinions on what is accepted syntax. Strict Mode is JavaScript and follows the standards of ECMAscript. It is always available for use in JavaScript.

I must admit, I have not always been consistent on using strict mode. Lately, however, I have had to work with more complex applications and algorithms. I find that adding 'use strict' makes me more aware of correct syntax and better code structure. 

