# content
secure user account
# format
- one entry per line for each user listed in /etc/passwd
- all fields are separated by a colon(:) symbol
- line format: username:password:lastchanged:minimum:maximum:warn:inactive:expire
- password format: $id$salt$hashed
- $id represents the algorithm used as follows

|id|algorithm|
|----|----|
|1|MD5|
|2a|Blowfish|
|2y|Blowfish|
|5|SHA-256|
|6|SHA-512|
