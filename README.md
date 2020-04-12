# fake_rsync
A wrapper around rsync which uses sshfs to by pass garbage messages sent by the server.

Copyright (C) 2020 by Nicolás Hermosilla

fake_rsync comes with ABSOLUTELY NO WARRANTY.  This is free software, and
you are welcome to redistribute it under certain conditions.  See the GNU
General Public Licence for details.

fake_rsync is a wrapper around rsync, which uses sshfs to mount remote
locations. This way it allows you to bypass any error caused by protocol
incompatibilities, misconfigured login messages on a server and many others.

```sh
Usage: fake_rsync [OPTIONS]... [USER@]HOST:SRC [DEST]
  or   fake_rsync [OPTIONS]... SRC [USER@]HOST:DEST
```
Please note it currently does not support using several SRC arguments. Neither
does it support any other communication protocol asides from remote shell. It
does, however, support the usage of all rsync options.
