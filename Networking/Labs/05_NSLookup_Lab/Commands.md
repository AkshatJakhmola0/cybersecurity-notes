# NSLookup Lab - Commands Executed

# Basic DNS Lookup
nslookup google.com

# DNS Lookup for Another Domain
nslookup github.com

# Retrieve Mail Exchange (MX) Records
nslookup -type=mx google.com

# Retrieve Name Server (NS) Records
nslookup -type=ns google.com

# Reverse DNS Lookup
nslookup 8.8.8.8

# Interactive Mode
nslookup

server 8.8.8.8

google.com

set type=mx
google.com

set type=ns
google.com

exit
