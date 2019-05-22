# iptell
Static site generator to check if machines are online, show current machine state and show their IPs (Local and Global)

Next stage of development is to have a graph of mem usage, cpu usage and disk usage.
A global config system also needs to be developed - which will be soon.

### !!! This will probably end up in my dotfiles !!!


## Scripts
- `iptell` is a script that can be run by a cron job on a LOCAL machine, which will create an html partial and scp it to a host
- `listip` is a script that can be run by a cron job on a HOST machine, which merges the partial files together
- `usagelog` is a script which WILL be used to log machine stats in the background for graphs (TODO)

Currently the scripts are *very poorly organised* and *lots of things are hardcoded* but this will change soon.
