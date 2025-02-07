cmake_minimum_required(VERSION 3.6)
project(linux_0_12)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ")

set(SOURCE_FILES
    boot/bootsect.S
    boot/head.s
    boot/setup.S
    fs/bitmap.c
    fs/block_dev.c
    fs/buffer.c
    fs/char_dev.c
    fs/exec.c
    fs/fcntl.c
    fs/file_dev.c
    fs/file_table.c
    fs/inode.c
    fs/ioctl.c
    fs/Makefile
    fs/namei.c
    fs/open.c
    fs/pipe.c
    fs/read_write.c
    fs/select.c
    fs/stat.c
    fs/super.c
    fs/truncate.c
    include/asm/io.h
    include/asm/memory.h
    include/asm/segment.h
    include/asm/system.h
    include/linux/config.h
    include/linux/fdreg.h
    include/linux/fs.h
    include/linux/hdreg.h
    include/linux/head.h
    include/linux/kernel.h
    include/linux/math_emu.h
    include/linux/mm.h
    include/linux/sched.h
    include/linux/sys.h
    include/linux/tty.h
    include/sys/param.h
    include/sys/resource.h
    include/sys/stat.h
    include/sys/time.h
    include/sys/times.h
    include/sys/types.h
    include/sys/utsname.h
    include/sys/wait.h
    include/a.out.h
    include/const.h
    include/ctype.h
    include/errno.h
    include/fcntl.h
    include/signal.h
    include/stdarg.h
    include/stddef.h
    include/string.h
    include/termios.h
    include/time.h
    include/unistd.h
    include/utime.h
    init/main.c
    init/main.s
    kernel/blk_drv/blk.h
    kernel/blk_drv/floppy.c
    kernel/blk_drv/hd.c
    kernel/blk_drv/ll_rw_blk.c
    kernel/blk_drv/Makefile
    kernel/blk_drv/ramdisk.c
    kernel/chr_drv/console.c
    kernel/chr_drv/keyboard.S
    kernel/chr_drv/Makefile
    kernel/chr_drv/pty.c
    kernel/chr_drv/rs_io.s
    kernel/chr_drv/serial.c
    kernel/chr_drv/tty_io.c
    kernel/chr_drv/tty_ioctl.c
    kernel/math/add.c
    kernel/math/compare.c
    kernel/math/convert.c
    kernel/math/div.c
    kernel/math/ea.c
    kernel/math/error.c
    kernel/math/get_put.c
    kernel/math/Makefile
    kernel/math/math_emulate.c
    kernel/math/mul.c
    kernel/asm.s
    kernel/exit.c
    kernel/fork.c
    kernel/Makefile
    kernel/mktime.c
    kernel/panic.c
    kernel/printk.c
    kernel/sched.c
    kernel/signal.c
    kernel/sys.c
    kernel/sys_call.s
    kernel/traps.c
    kernel/vsprintf.c
    lib/_exit.c
    lib/close.c
    lib/ctype.c
    lib/dup.c
    lib/errno.c
    lib/execve.c
    lib/Makefile
    lib/malloc.c
    lib/open.c
    lib/setsid.c
    lib/string.c
    lib/wait.c
    lib/write.c
    mm/Makefile
    mm/memory.c
    mm/page.s
    mm/swap.c
    tools/build.c
    Makefile
    README.md)

include_directories(include)
include_directories(include/asm)
include_directories(include/linux)
include_directories(include/sys)

add_executable(linux_0_12 ${SOURCE_FILES})