[![Snap Status](https://build.snapcraft.io/badge/ogra1/tinyproxy-snap.svg)](https://build.snapcraft.io/user/ogra1/tinyproxy-snap)

# TinyProxy snap

The proxy runs on port 8080 and only allows connections from localhost by default.

## Configuration

If you want to change the configuartion use the "snap set" command:

### Allow

Comma separated list of IPs and networks that can connect to this tinyproxy instance

Example:

```sudo snap set tinyproxy-ogra allow="127.0.0.1,192.168.0.0/16"```

Allows acess from localhost and all machines on the 192.168.* networks

### Filters

Comma or space separated list of domains or urls to filter

If ```filterurls``` is set to ```off```, use a comma separated list of domain names

Example:

sudo snap set tinyproxy-ogra filters="www.grawert.net,www.ubuntu.com"```

If ```filterurls``` is set to ```on``` use an url list with globbing and pattern matching.

Example:

```sudo snap set tinyproxy-ogra filters="^.*grawert.net/car/,.*ubuntu.com"```

### Filterurls

Either filter by domain names or by urls, if ```filterurls``` is set to ```on``` use url
patterns, else use domain names.

Example:

```sudo snap set tinyproxy-ogra filterurls="on"```

### Port

Port the proxy listens on, defaults to 8080

Example:

```sudo snap set tinyproxy-ogra port="7990"```

### Timeout

Connection timeout in seconds.

Example:

```sudo snap set tinyproxy-ogra timeout="300"```

## Logging

Logs are written to:

/var/snap/tinyproxy/current/tinyproxy.log
