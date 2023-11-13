#!/bin/bash

PARENT="$(ps -o comm= $PPID)"
INTERNALS="$( cd "$( dirname "$( readlink -f "$0" )" )/.." && pwd )"
cd "$INTERNALS"

if [ "$PARENT" == "systemd" ]; then
	for f in rc/*; do
		source $f
	done
else
	echo "command must be run by awesome wm (see README)"
fi
