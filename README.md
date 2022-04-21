# labstatus

A script to easily find a free lab machine to use, and more generally to check the status of many remote machines.

## Usage

For information on how to use the command, see `./labstatus -h`.

Note that `labstatus` uses `ssh` under the hood - the given hostnames must be accessable via `ssh` using public-key authentication.

To set a default list of clients, put `alias labstatus=labstatus -f ~/myfavclients.txt` in your `.bashrc` (or shell of choice!).

### Examples

```bash
$ ./labstatus -f hosts.txt

pc5-001-l unreachable
pc8-001-l free
pc8-002-l free
pc8-003-l free
pc8-004-l unreachable
pc8-005-l unreachable
....
```

---

List all free clients:

```bash
$ ./labstatus -Ff hosts.txt

pc8-001-l
pc8-002-l
pc8-003-l
```
