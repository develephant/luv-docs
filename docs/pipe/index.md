!!! note "Purpose"
    Pipe handles provide an abstraction over local domain sockets on Unix and named pipes on Windows.

## new_pipe

```lua
uv.new_pipe()
```

Initialize the handle.

__Parameters__

none

__Examples__

```lua
local pipe_handle = uv.new_pipe()
```

---

## pipe_open

```lua
uv.pipe_open( fd_or_handle )
```

Open an existing file descriptor or HANDLE as a pipe.

__Parameters__

Name|Details
----|-------
fd_or_handle|The handle of file descriptor.

__Examples__

```lua
uv.pipe_open( fd_or_handle )
```

---

## pipe_bind

```lua
uv.pipe_bind( pipe_handle, filepath )
```

Bind the pipe to a file path (Unix) or a name (Windows).

__Parameters__

Name|Details
----|-------
pipe_handle|The handle to the pipe.
filepath|A file to bind to the pipe.

__Examples__

```lua
uv.pipe_bind( pipe_handle, '/home/somefile' )
```

---

## pipe_connect

```lua
uv.pipe_connect( connect_req, pipe_handle, name, connect_cb )
```

Connect to the Unix domain socket or the named pipe.

__Parameters__

Name|Details
----|-------
connect_req|The connection request.
pipe_handle|The handle to the pipe.
name|Name of the pipe.
connect_cb|The callback to fire on connection.

__Examples__

none

---

## pipe_getsockname

```lua
uv.pipe_getsockname( pipe_handle )
```

Get the name of the Unix domain socket or the named pipe.

__Parameters__

Name|Details
----|-------
pipe_handle|The handle to the pipe.

__Examples__

```lua
local sock_name = uv.pipe_getsockname( pipe_handle )
```

---

## pipe_getpeername

```lua
uv.pipe_getpeername( pipe_handle )
```

Get the name of the Unix domain socket or the named pipe to which the handle is connected.

__Parameters__

none

__Examples__

```lua
local peer_name = uv.pipe_getpeername( pipe_handle )
```

---

## pipe_pending_instances

```lua
uv.pipe_pending_instances( pipe_handle, count )
```

Set the number of pending pipe instance handles when the pipe server is waiting for connections.

!!! warning "This setting applies to Windows only."
    
__Parameters__

Name|Details
----|-------
pipe_handle|The handle to the pipe.
count|The pending pipe instance amount.

__Examples__

```lua
uv.pipe_pending_instances( pipe_handle, 4 )
```

---

## pipe_pending_count

```lua
uv.pipe_pending_count( pipe_handle )
```

Pipe pending count.

__Parameters__

Name|Details
----|-------
pipe_handle|The handle to the pipe.

__Examples__

```lua
local amount = uv.pipe_pending_count( pipe_handle )
```

---

## pipe_pending_type

```lua
uv.pipe_pending_type( pipe_handle )
```

Used to receive handles over IPC pipes.

__Parameters__

Name|Details
----|-------
pipe_handle|The handle to the pipe.

__Examples__

```lua
local handle_type = uv.pipe_pending_type( pipe_handle )
```

---

### See also

The following API functionality applies to all __handles__ and __streams__:

[handles](../handles)
[streams](../streams)
