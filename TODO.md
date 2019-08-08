Current functionality:
- mk_call performs unsafe command substitution
- xclip (and its 'selection') is hardcoded outside option-default
- signald supports needs an upstream fix for "unsubscribe" to not ACK msgs
  to Signal server anymore (assuming we're the only client for this user).
  Otherwise (more robust): find a way to determine where we left off and
  resume showing messages from that point.
- add (and store?) contacts (and manage groups) not known to signal-cli profile
  (easy with signald, since it allows manipulation of remote contacts)
  in order to send messages to and reply to messages from new contacts
- receive messages from signal-cli via DBUS instead of parsing its stdout?
- use some DBUS integration into python instead of relying on external tool
  in order to send files with ',' inside their filenames
- implement help pop-up

New functionality:
- support other transports (e.g. via spectrum.io)?
