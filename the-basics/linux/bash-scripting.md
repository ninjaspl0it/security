# Bash-scripting

## Iterate over a file <a id="iterate-over-a-file"></a>

This script will iterate over a file and echo out every single line:

```text
#!/bin/bash

for line in $(cat file.txt);do
    echo $line
done
```

Another way of writing is this:

```text
#!/bin/bash

while read p; do
    echo  $p
done <file.txt
```

## For-loops <a id="for-loops"></a>

```text
#!/bin/bash

for ((i = 0; i < 10; i++)); do
    echo $i
done
```

Another way to write this is by using the program `seq`. Seq is pretty much like `range()` in python. So it can be used like this:

```text
#!/bin/bash

for x in `seq 1 100`; do
    echo $x
done
```

## If statement <a id="if-statement"></a>

`$1` here represent the first argument.

```text

if [ "$1" == "" ]; then
    echo "This happens"
fi
```

## If/Else <a id="ifelse"></a>

```text
#!/bin/bash

if [ "$1" == "" ]; then
    echo "This happens"
else
    echo "Something else happens"
fi
```

## Command line arguments <a id="command-line-arguments"></a>

Command line arguments are represented like this

```text
#!/bin/bash

$1
```

This is the first command line argument.

## Daemonize an execution <a id="daemonize-an-execution"></a>

If you do a ping-sweep with host the command will take about a second to complete. And if you run that against 255 hosts I will take a long time to complete. To avoid this we can just deamonize every execution to make it faster. We use the `&` to daemonize it.

```text
#!/bin/bash

for ip in $(cat ips.txt); do
    ping -c 1 $ip &
done
```

## Use the output of command <a id="use-the-output-of-command"></a>

It has happened to me several times that I want to input the output of a command into a new command, for example:

I search for a file, find three, and take the last line, which is a path. Now I want to cat that path:

```text
#!/bin/bash

locate 646.c | tail -n 1
```

This can be done like this:

```text
#!/bin/bash

cat $(locate 646.c | tail -n 1)
```

### Piping stdout to clipboard 

Useful when you have no GUI available and need to pipe contents or output of commands to the clipboard.

`apt-get install xsel` Now, edit ~/.bash\_aliases

```text
alias copy='xsel -ib'
```

Restart terminal, now pipe anything to clipboard with: `cat file.txt | copy`

