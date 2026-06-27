luadec v2.1 r80 by viruscamp
based on http://luadec.luaforge.net and https://github.com/sztupy/luadec51
http://code.google.com/p/luadec
viruscamp+luadec@gmail.com

If luadec.exe crashed, try luadec_memwatch.exe, and please send me the lua source or binary and memwatch.log.

Fixes and Improvements:
1. compelete table support
2. improved loop support
3. more clear disassembled results
4. read lua source files directly
5. options to decompile only specific nested function
6. process lua script with 255 or more functions
7. more stable and less memory leaks
8. can process consecutive 255 or more variable assignments

Usage:
1. decompile lua binary file:
	luadec abc.luac
2. decompile lua source file for testing and comparing:
	luadec abc.lua
3. disassemble lua source or binary
	luadec -dis abc.lua
4. -pn print nested functions structure, could be used by -nf
	luadec -pn test.lua
	0
	 1 
	  1_1
	 2
5. -nf decompile only specific nested function
	luadec -nf 1 test.lua 
6. -nf -dn decompile specific function without sub functions
	luadec -dn -nf 1 test.lua


Know Bugs:
1. "local a,b = ..., ..." should be "local a,b=..."
2. "local ,a" should be "local a"
3. complex if..else may produce "do return end" ,that possibly means "else".
4. complex logic expression will produce a wrong result
5. performs badly on stripped lua binary files. use -s arg to test.


ChunkSpy.lua
based on chunkspy.luaforge.net

Improvements:
1. more clear disassembled results
2. read lua source files directly