# amigaux

amigaux brings Commodore's Amiga UNIX to newer Amiga hardware: new kernels, drivers, firmware, install
media and a package manager. Downloads and install guides are on [amigaux.org](https://amigaux.org);
everything we know about Amiga UNIX is in the [grimoire](https://jusii.github.io/grimoire-amix/).

## Reporting a problem or asking a question

If you don't know where to report something, report it here. Questions, feature requests, install
problems, anything where you are not sure which part is at fault: this is the place, and we pass it
on to the right repository.

- **A bug or an install problem:** [open an issue](https://github.com/jusii/amigaux/issues/new/choose).
- **A question or an idea:** start a [discussion](https://github.com/jusii/amigaux/discussions).
- **A machine or card we don't cover yet:** see [Asking for hardware support](#asking-for-hardware-support).

If you already know where the fault lives, open the issue or pull request in that component's
repository (see below).

A good bug report has:

- the machine: A3000, A4000 or A4000T, or the emulator and its version
- the accelerator and its firmware version, and the SCSI controller if there is one
- the file you installed from, by its name on the Downloads page or in `SHA256SUMS`
  (for example `amigaux-1.0-k1-card.zip`)
- what you did, what you expected, and what happened
- a capture of the console or serial output

## Asking for hardware support

Release 1.0 runs on the machines listed on [amigaux.org/hardware](https://amigaux.org/hardware/): an
A3000, A4000 or A4000T with a Z3660 accelerator, and, so far tested only in an emulator, an A3000 or an
A4000 with a full 68030 card. Release 1.1 is planned to add, among other things, installing onto an
IDE disk in an A4000 with a Z3660, the A4000T's own SCSI and the Z3660's 68030 mode. Anything else,
such as another accelerator, another Amiga model or another disk controller, is a new target.

To ask about yours, [open a hardware support request](https://github.com/jusii/amigaux/issues/new?template=hardware_support.md)
and tell us the hardware. We check whether it is already covered, whether an emulator can model it, and
what a driver would take, and answer on the issue.

## Where things live

| Repository | What belongs there |
|---|---|
| [jusii/amix-installng](https://github.com/jusii/amix-installng) | Install media: boot floppies, install CDs, the SD card, the installer |
| [jusii/amix-packagemanager](https://github.com/jusii/amix-packagemanager) | `apkg` and the package tools |
| [jusii/amix-packages](https://github.com/jusii/amix-packages) | The packages `apkg` installs: broken builds, versions, packages you miss |
| [asokero/amix-040-060-port](https://github.com/asokero/amix-040-060-port) | The kernel on the 68040 and 68060 |
| [jusii/amix-kerntools](https://github.com/jusii/amix-kerntools) | Kernel builds: the build hub that patches your own Amiga UNIX tree |
| [jusii/amix-a4091](https://github.com/jusii/amix-a4091) | The A4091 / A4092 SCSI driver |
| [jusii/amix-z3660scsi](https://github.com/jusii/amix-z3660scsi) | The Z3660 SCSI driver (the SD card disk) |
| [jusii/amix-z3660net](https://github.com/jusii/amix-z3660net) | The Z3660 ethernet driver |
| [jusii/amix-z3660rtg](https://github.com/jusii/amix-z3660rtg) | The Z3660 graphics driver |
| [hmlio/amix-gayle-ide](https://github.com/hmlio/amix-gayle-ide) | The A4000 Gayle IDE driver |
| [jusii/amix-cdfs](https://github.com/jusii/amix-cdfs) | The CD filesystem |
| [jusii/Z3660-amix](https://github.com/jusii/Z3660-amix) | The Z3660 firmware with Amiga UNIX support (1.0 is branch `release-1.0`) |
| [jusii/gcc-cross-amix](https://github.com/jusii/gcc-cross-amix) | The `m68k-cbm-sysv4` cross toolchain |
| [jusii/grimoire-amix](https://github.com/jusii/grimoire-amix) | The documentation |

More drivers and ports by friends of the project are listed on
[amigaux.org/github](https://amigaux.org/github/).

## Release notes

Each release is described on amigaux.org: [what is in 1.0](https://amigaux.org/hardware/#in-1.0),
the [known issues](https://amigaux.org/docs/known-issues/) and the
[downloads](https://amigaux.org/downloads/) with their `SHA256SUMS`.

---

This project and its developers are not affiliated with, endorsed by, or sponsored by Amiga
Corporation. Amiga is a registered trademark of Amiga Corporation.
