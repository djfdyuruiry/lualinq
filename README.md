lualinq
=======

Lightweight library which allows functional querying and transformation of lua arrays and objects.

The syntax is very similar to the C# linq or Java 8 streams libraries, which are similar in syntax to SQL. It’s released with a BSD 3 clause license.

----

## Install

There is a [LuaRocks](https://luarocks.org/) package for this library: https://luarocks.org/modules/djfdyuruiry/lualinq

To install, install luarocks, and then run:

```bash
luarocks install lualinq
```

## Usage

```lua
local lualinq = require "lualinq"
local from = lualinq.from

local count = from({1,2,3,4,5}).
  where(function(v) return v > 2; end).
  count()

-- prints '3'
print(count)
```

Full documentation on all available functions can be found [here](https://github.com/xanathar/lualinq/blob/master/docs/LuaLinq.pdf)

----

I forked this library to add Lua 5.3 support and update the luarocks module I maintain for this library. Originally authored by [xanathar](https://github.com/xanathar)

Credit goes to [buckle2000](https://github.com/buckle2000) for cleaning up the the original version of lualinq, see their work [here](https://github.com/djfdyuruiry/lualinq)

See [the original repo](https://github.com/xanathar/lualinq) for more info
