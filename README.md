# githooks
githookstest

#!/bin/sh

if git diff --cached | grep -E "AKIA[0-9A-Z]+"
then
  echo " Möjlig nyckel hittad i staged filer. Avbryter commit."
  exit 1
fi

exit 0
