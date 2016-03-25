# PKI Examples

Examples of creating and using your own public key infrastructure between node and Go services.

## Usage

## Generating certs

Make sure your `$DOCKER_HOST` is running locally (cert generation requires writing to a local volume carina can't reach).

```
./gencerts.sh
```

## Using the certs

### Raw TCP Server

You'll be running two processes, a server and a client. In one terminal:

```
source sourcery.sh
node raw-tcp/server.js
```

In another terminal:

```
source sourcery.sh
node raw-tcp/cli.js
```

### HTTPS Server

```
source sourcery.sh
node https/server.js
```

In another terminal:

```
source sourcery.sh
node https/cli.js
```
