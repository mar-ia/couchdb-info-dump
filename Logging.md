#Loging

Logging is now done to stderr by default.
There is a lot of error messages before setup is finished, this is expected so
just ignore them.

##Warnings

	warning: write quorum (2) failed for updated:mydatabase

An internal race for the update to `_global_changes`, the global changes
database. Nothing to worry about, just ignore it. (An internal `409` because of
a race between the write and the anti-entropy system.)
