Some handy scripts we've written for Nagios, at Etsy:


check_graphite_data:
    Alert on data, based on number from Graphite.
Usage:
    check_graphite_data <options>
Options:
    -c <num> --crit=<num>       Critical threshold
    -w <num> --warn=<num>       Warning threshold
    -u <url> --url=<url>        Graphite graph URL
    -r                          Reverse - Alert when the value is UNDER warn/crit instead of OVER
    -s <secs> --seconds=<secs>  Average over the last N seconds of data
    --d1 <url> --d2 <url>       Diff the latest values between two graphs
    -W --holt-winters           Perform a Holt-Winters check
    -U --critupper              Upper Holt-Winters band breach causes a crit,
                                    - breaching lower band causes a warn
    -L --critlower              Lower Holt-Winters band breach causes a crit,
                                    - breaching upper band causes a warn
    (If -W, but neither -U nor -L are given, we will always warn)
    --scale=<multiplier>        scale, eg 8 to treat bytes as bits
    --scale-invert=<divisor>    scale, eg 1073741824 to treat bytes as GiB
                                    - --scale{-invert} lets you give thresholds in sane units
