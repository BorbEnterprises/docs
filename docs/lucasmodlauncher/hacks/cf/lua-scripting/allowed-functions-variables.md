---
title: Allowed Functions/Variables
description: "This page documents what parts of Lua's stock functionality are available for use in this hack."
authors: ["loren","proddy"]
---

This hack's implementation of Lua is customised and only allows usage of some of Lua's stock functionality:

* _G
* _VERSION
* assert
* collectgarbage
* coroutine.create
* coroutine.isyieldable
	* Added in Version 1.23.10.
* coroutine.resume
* coroutine.running
* coroutine.status
* coroutine.wrap
* coroutine.yield
* debug.debug
* debug.gethook
* debug.getinfo
* debug.getlocal
* debug.getmetatable
* debug.getregistry
* debug.getupvalue
* debug.getuservalue
* debug.sethook
* debug.setlocal
* debug.setmetatable
* debug.setupvalue
* debug.setuservalue
* debug.traceback
* debug.upvaluejoin
* debug.upvalueid
* error
* getmetatable
* ipairs
* math.abs
* math.acos
* math.asin
* math.atan
* math.ceil
* math.cos
* math.deg
* math.exp
* math.floor
* math.fmod
* math.huge
* math.log
* math.max
* math.maxinteger
* math.min
* math.mininteger
* math.modf
* math.pi
* math.rad
* math.sin
* math.sqrt
* math.tan
* math.tointeger
* math.type
* math.ult
* next
* os.clock
* os.date
* os.difftime
* os.exit
* os.setlocale
* os.time
* pairs
* pcall
* print
* rawequal
* rawget
* rawlen
* rawset
* select
* setmetatable
* string.byte
* string.char
* string.dump
* string.find
* string.format
* string.gmatch
* string.gsub
* string.len
* string.lower
* string.match
* string.pack
* string.packsize
* string.rep
* string.reverse
* string.sub
* string.unpack
* string.upper
* table.concat
* table.insert
* table.move
* table.pack
* table.remove
* table.sort
* table.unpack
* tonumber
* tostring
* type
* utf8.char
* utf8.charpattern
* utf8.codepoint
* utf8.codes
* utf8.len
* utf8.offset
* xpcall

The following functions are also supported with a custom implementation:

* dofile
* load
* loadfile
* math.random
* math.randomseed
	* Added in Version 1.23.10.

The following functions were removed in [Version 1.12](/lucasmodlauncher/versions/version_1.12.md#hacks_custom-files_lua-scripting) due to the Lua version being changed from 5.2.3 to 5.3.1:

* math.atan2
* math.cosh
* math.frexp
* math.ldexp
* math.log10
* math.pow
* math.sinh
* math.tanh
* table.maxn

Documentation of these functions and variables can be found in in the [Lua manual](https://www.lua.org/manual/5.3/).
