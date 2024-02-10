TFTP Server for Networking Labs
================================

A simple TFTP server for networking labs. It is based on the
[pghalliday-docker/tftp][pghalliday-docker/tftp] project.

The server is configured for read-only access.

[pghalliday-docker/tftp]: https://github.com/pghalliday-docker/tftp

Basic Usage
-----------

Start the server:

```sh
docker compose up --detach
```

Stop the server:

```sh
docker compose down
```

Testing
-------

Start TFTP client:

```sh
tftp 127.0.0.1
```

Download the `hello.txt` file to the `/tmp` directory and stop the client:

```
mode binary
get hello.txt /tmp/hello.txt
quit
```

Check:

```sh
cat /tmp/hello.txt
```

The expected output:

```
Hello, World!
```
