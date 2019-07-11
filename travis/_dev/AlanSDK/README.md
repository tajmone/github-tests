# Binaries Folder

This folder contains some Windows executable files (32 bit) required for the automation of this project and for running integrity tests.

# Alan SDK

Executable binaries from [Alan SDK v3.0beta6]:

- `alan.exe` — Alan CLI compiler (2018-05-26).
- `arun.exe` — Alan CLI interpreter (2018-07-14).
- [`COPYING`][COPYING] — Artistic License 2.0.

This project relies on the [latest Alan SDK release] for building its assets — i.e. the latest beta version, until Alan 3 reaches the first stable release.
We won't be using [development snapshots] for the project.

To ensure that the project is always built using the correct/same SDK version on all machines, we added the Alan binaries to the repository itself, to avoid potential conflicts with other versions of the Alan SDK present on the system `%PATH%` of end users' local machines.

Although version controlling executable files is generally deemed as bad practice, in this case it's justified — after all, these small executables are smaller than the average PDF document you'll find in many repositories, and it's not rare to find repositories that include pre-compiled object files or DLLs.
Alan beta releases are not so frequent, so chances are that inclusion of these binaries will never bloat up the project.


<!-----------------------------------------------------------------------------
                               REFERENCE LINKS
------------------------------------------------------------------------------>

[development snapshots]: https://www.alanif.se/download-alan-v3/development-snapshots/development-snapshots "Go to the development snapshots page on Alan website"
[latest Alan SDK release]: https://www.alanif.se/download-alan-v3/latest-releases "Go to the Alan SDK download page on Alan website"

[Alan SDK v3.0beta6]: https://www.alanif.se/download-v3/official-releases/development-kits/development-kits-3-0beta6

<!-- project files -->

[COPYING]: ./COPYING "Read the ALAN Artistic License 2.0"

<!-- EOF -->
