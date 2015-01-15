msys-jlog-tools
===============

Miscellaneous tools for JLog (journalled log) files

See [https://labs.omniti.com/labs/jlog] for a description of JLogs.

jlogcat
-------

This is like the cat command, but on a jlog. E.g.:

```jlogcat /var/log/ecelerity/foo.jlog```

For a jlog containing JSON records, you can use --no-escape and pipe
the output into [jq](https://stedolan.github.io/jq/) for pretty-printing:

```jlogcat /var/log/ecelerity/event_hydrant.rt --no-escape | jq .```

See `jlogcat --help` for more details.

jlogtail
--------

This is like the tail command, but on a jlog. E.g.: follow the jlog
to show new entries:

```jlogtail -f /var/log/ecelerity/foo.jlog```

jlogtail supports the --no-escape option, like jlogcat.

See `jlogtail --help` for more details.

jlog-trim-subscribers
---------------------

See script for more details.
