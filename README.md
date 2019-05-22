# iptell
Static site generator to check if machines are online, show current machine state and show their IPs (Local and Global)

This project (rather niftily) shows a graph of mem usage, cpu usage and disk usage.
A global config system also needs to be developed - which will be soon.

Currently the scripts are *very poorly organised* and *lots of things are hardcoded* but this will change soon.

### !!! This will probably end up in my dotfiles !!!

## Scripts
- `iptell` is a script that can be run by a cron job on a LOCAL machine, which will create an html partial and scp it to a host
- `listip` is a script that can be run by a cron job on a HOST machine, which merges the partial files together
- `usagelog` is a script which can be used to log machine stats in the background for graphs (TODO)


## Requirements
[STYLE CSS](http://willmatthews.xyz/css/dark.css)
[DARK CSS](http://willmatthews.xyz/css/style.css)
[MOMENT JS](http://willmatthews.xyz/js/moment.min.js)
[CHART.JS JS](http://willmatthews.xyz/js/Chart.min.js)

## Installation
### Client
- Make the folder `~/.iptell`
- Move all scripts to `~/.iptell`
- Add the scripts to your Crontab (suggestions in the file `crontab`)
    - iptell and usagelog commands if your machine is a CLIENT
- Check settings that files are being scp'd correctly, and paths are correct
### Host
- Do `mkdir -p ./.iptell/ip`
- Move all scripts to `~/.iptell`
- Add the scripts to your Crontab (suggestions in the file `crontab`)
    - listip if your machine is a HOST
- Check settings that files are being moved to correct paths
- Add relevant JS and CSS to your webserver's /css/ and /js/

(this will be automated away soon)
