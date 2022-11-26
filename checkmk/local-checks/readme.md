## local-checks

### cmk_cifsmounts

Script ermittelt anhand "/proc/mounts" cifs-mounts und prüft mit ls ob auf die entsprechenden mountpoints zugegriffen werden kann.
Im Script wird das Kommando timeout verwendet um ein hängen z.B. bei nicht Erreichbarkeit zu verhindern.
D.h. timeout muss auf dem System ggf. vorher installiert werden.

Script muss im local Verzeichnis des checkmk -Agents ausführbar abgelegt werden.
Z.B. in /usr/lib/check_mk_agent/local/

P.S. Eine Version mit "stat -f" statt ls war bei Netzausfall nicht zu gebrauchen.
