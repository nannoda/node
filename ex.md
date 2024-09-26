sudo ./configure --ninja -C --debug

sudo make -j12 BUILDTYPE=Debug



cd ./out && gdb ./Debug/node

(gdb) break uv_thread_create
(gdb) break pthread_create

Breakpoint 2 at 0x1669090
(gdb) run ../mytest.mk/src/index.js

https://github.com/nodejs/node-code-ide-configs/blob/main/vscode.md