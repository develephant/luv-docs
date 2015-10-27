!!! note "Purpose"
    The purpose of poll handles is to enable integrating external libraries that rely on the event loop to signal it about the socket status changes, like c-ares or libssh2. ___Using poll for any other purpose is not recommended.___

## new_poll

```lua
uv.new_poll( fd )
```

Initialize the handle using a file descriptor.

__Parameters__

none

__Examples__

```lua
local poll_handle = uv.new_poll( file_descriptor )
```

---

## socket_poll

```lua
uv.socket_poll( socket )
```

Initialize the handle using a socket descriptor.

__Parameters__

none

__Examples__

```lua
local poll_handle = uv.socket_poll( socket )
```

---

## poll_start

```lua
uv.poll_start( poll_handle, events, callback )
```

Initialize the handle using a socket descriptor.

__Parameters__

none

__Examples__

```lua
uv.poll_start( poll_handle, events, function() {
  print('polling started')
} )
```

---

## poll_stop

```lua
uv.poll_stop( poll_handle )
```

Stop polling the file descriptor, the callback will no longer be called.

__Parameters__

none

__Examples__

```lua
uv.poll_stop( poll_handle )
```

---

### See also

The following API functionality applies to all __handles__:

[handles](../handles)
