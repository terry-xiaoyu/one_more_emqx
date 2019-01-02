# one_more_emqx

A shell script for creating a new emqx node for an existing one.

It simply copies the existing emqx directory to new one and then changes the `port` configs in it.

Usage:

```shell
➜  cd _rel
➜  ls
emqx one_more_emqx.sh
➜  ./one_more_emqx.sh emqx2
creating emqx2 ...
using increment factor: 836
.
.
.
.
processing config file: emqx2/etc/plugins/emqx_management.conf
inc port for management.listener.http
-- from: 8080
-- to: 8916
inc port for management.listener.https
-- from:
-- to: 836
.
processing config file: emqx2/etc/plugins/emqx_dashboard.conf
inc port for dashboard.listener.http
-- from: 18083
-- to: 18919
inc port for dashboard.listener.https
-- from:
-- to: 836
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
processing config file: emqx2/etc/emqx.conf
inc port for node.dist_listen_min
-- from: 6369
-- to: 7205
inc port for dist_listen_max
-- from: 6369
-- to: 7205
inc port for tcp_server_port
-- from: 5369
-- to: 6205
inc port for tcp_client_port
-- from: 5369
-- to: 6205
inc port for listener.tcp.external
-- from: 0.0.0.0:1883
-- to: 0.0.0.0:2719
inc port for listener.tcp.internal
-- from: 127.0.0.1:11883
-- to: 127.0.0.1:12719
inc port for listener.ssl.external
-- from: 8883
-- to: 9719
inc port for listener.ws.external
-- from: 8083
-- to: 8919
inc port for listener.wss.external
-- from: 8084
-- to: 8920
inc port for listener.tcp.internal
-- from: 127.0.0.1:12719
-- to: 127.0.0.1:13555
.
```

