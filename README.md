# efficiency

Some of these checks make multiple SSH connections to the target.  It could be more efficient to run one script on the target.  It could also improve efficiency to make sure SSH configuration keeps a master connection open and routes new connections through a socket.

# redundant code

Some checks have redundant code.  Each one checks that a scheduled script returned zero within a recent timeframe.  These could probably be deduplicated into one script, and commands could be defined to call the script with appropriate arguments or variables to specify the log and ret files to check and the expected timeframe.
