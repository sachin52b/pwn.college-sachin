# An-epic-filesystem-quest:

Find a hidden layered flag by tracking a series of text-based clues spread across the filesystem. Use ls/ls -a to uncover directory
contents (dotfiles included), and cat to display clue files. Follow clue instrunction — trapped  means don't cd (read as full path),
hidden means a dotfile (use ls -a), and delayed means you have to cd prior to the file being readable.

## My solve
**Flag:** `pwn.college{gmMqugWnH3hIrO-UAp8rk0UWmON.QX5IDO0wiN5gjNzEzW}`

### Thought process/Procedure
Treated filesystem like a treasure hunt: read clues carefully, used directory listings to find desired files, and used proper way 
to access each clue based on its instruction. When a clue cautioned against directory changing I read the target by absolute path 
like by directly using cat and path as the argument and if it declared a file to be hidden I listed with -a(ls-a) to show . files 
and when a clue called for stepping into a directory I changed into that directory and read the last file. The focus was on reading
the clue language well and applying ls/ls -a and cat well in order to reach the flag.




```bash
~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
NUGGET  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin     challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat NUGGET
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/arch/mips/include/asm/mach-dec

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ cat /opt/linux/linux-5.4/arch/mips/include/asm/mach-dec
cat: /opt/linux/linux-5.4/arch/mips/include/asm/mach-dec: Is a directory
hacker@commands~an-epic-filesystem-quest:/$ ls /opt/linux/linux-5.4/arch/mips/include/asm/mach-dec
TRACE-TRAPPED  cpu-feature-overrides.h  mc146818rtc.h
hacker@commands~an-epic-filesystem-quest:/$ cat ls /opt/linux/linux-5.4/arch/mips/include/asm/mach-dec/TRACE-TRAPPED
cat: ls: No such file or directory
Yahaha, you found me!
The next clue is in: /usr/local/lib/python3.8/dist-packages/cle/backends/elf/relocation/__pycache__
hacker@commands~an-epic-filesystem-quest:/$ ls /usr/local/lib/python3.8/dist-packages/cle/backends/elf/relocation/__pycache__
INFO                     arm64.cpython-38.pyc         elfreloc.cpython-38.pyc  mips64.cpython-38.pyc  sparc.cpython-38.pyc
__init__.cpython-38.pyc  arm_cortex_m.cpython-38.pyc  generic.cpython-38.pyc   pcc64.cpython-38.pyc
amd64.cpython-38.pyc     armel.cpython-38.pyc         i386.cpython-38.pyc      ppc.cpython-38.pyc
arm.cpython-38.pyc       armhf.cpython-38.pyc         mips.cpython-38.pyc      s390x.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/local/lib/python3.8/dist-packages/cle/backends/elf/relocation/__pycache__/INFO
Congratulations, you found the clue!
The next clue is in: /usr/share/locale/az

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ ls /usr/share/locale/az
BLUEPRINT-TRAPPED  LC_MESSAGES
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/share/locale/az/BLUEPRINT-TRAPPED
Tubular find!
The next clue is in: /usr/share/racket/pkgs/web-server-lib/web-server/private

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/share/locale/az/LC_MESSAGES
cat: /usr/share/locale/az/LC_MESSAGES: Is a directory
hacker@commands~an-epic-filesystem-quest:/$ ls -a /usr/share/racket/pkgs/web-server-lib/web-server/private
.                connection-manager.rkt                 launch.rkt                            url-param.rkt
..               define-closure.rkt                     mime-types.rkt                        util.rkt
.WHISPER         dispatch-server-sig.rkt                mod-map.rkt                           web-server-structs.rkt
cache-table.rkt  dispatch-server-unit.rkt               raw-dispatch-server-connect-unit.rkt  xexpr.rkt
compiled         dispatch-server-with-connect-unit.rkt  servlet.rkt
configure.rkt    gzip.rkt                               timer.rkt
hacker@commands~an-epic-filesystem-quest:/$ cat ls -a /usr/share/racket/pkgs/web-server-lib/web-server/private/.WHISPER
cat: invalid option -- 'a'
Try 'cat --help' for more information.
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/share/racket/pkgs/web-server-lib/web-server/private/.WHISPER
Tubular find!
The next clue is in: /usr/lib/x86_64-linux-gnu/perl-base/Carp
hacker@commands~an-epic-filesystem-quest:/$ ls /usr/lib/x86_64-linux-gnu/perl-base/Carp
GIST  Heavy.pm
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/lib/x86_64-linux-gnu/perl-base/Carp/GIST
Congratulations, you found the clue!
The next clue is in: /usr/lib/python3/dist-packages/jedi/third_party/typeshed/third_party/2and3/dateutil
hacker@commands~an-epic-filesystem-quest:/$ ls  /usr/lib/python3/dist-packages/jedi/third_party/typeshed/third_party/2and3/dateutil
POINTER  __init__.pyi  _common.pyi  parser.pyi  relativedelta.pyi  rrule.pyi  tz  utils.pyi
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/lib/python3/dist-packages/jedi/third_party/typeshed/third_party/2and3/dateutil/POINTER
Yahaha, you found me!
The next clue is in: /usr/include/sepol

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ ls /usr/include/sepol
CLUE-TRAPPED      context.h         handle.h            ibpkeys.h        kernel_to_conf.h  nodes.h        ports.h        users.h
boolean_record.h  context_record.h  ibendport_record.h  iface_record.h   module.h          policydb       roles.h
booleans.h        debug.h           ibendports.h        interfaces.h     module_to_cil.h   policydb.h     sepol.h
cil               errcodes.h        ibpkey_record.h     kernel_to_cil.h  node_record.h     port_record.h  user_record.h
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/include/sepol/CLUE-TRAPPED
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/drivers/net/can/m_can

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /opt/linux/linux-5.4/drivers/net/can/m_can
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/net/can/m_can$ ls
Kconfig  Makefile  SPOILER  m_can.c  m_can.h  m_can_platform.c  tcan4x5x.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/net/can/m_can$ cat SPOILER
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{gmMqugWnH3hIrO-UAp8rk0UWmON.QX5IDO0wiN5gjNzEzW}```
