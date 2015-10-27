## is_active

```lua
uv.is_active( uv_handle )
```

Returns non-zero if the handle is active, zero if it’s inactive.

__Parameters__

Name|Details
----|-------
uv_handle|A handle to check.

__Examples__

none

---

## is_closing

```lua
uv.is_closing( uv_handle )
```

Returns non-zero if the handle is closing or closed, zero otherwise.

__Parameters__

Name|Details
----|-------
uv_handle|A handle to check.

__Examples__

none

---

## close

```lua
uv.close( uv_handle, callback )
```

Request handle to be closed. callback will be called asynchronously after this call. This MUST be called on each handle before memory is released.

__Parameters__

Name|Details
----|-------
uv_handle|A handle to close.
callback|The callback to trigger after close.

__Examples__

none

---

## ref

```lua
uv.ref( uv_handle )
```

Reference the given handle. References are idempotent, that is, if a handle is already referenced calling this function again will have no effect.

__Parameters__

Name|Details
----|-------
uv_handle|A handle to ref.

__Examples__

none

---

## unref

```lua
uv.unref( uv_handle )
```

Un-reference the given handle. References are idempotent, that is, if a handle is not referenced calling this function again will have no effect.

__Parameters__

Name|Details
----|-------
uv_handle|A handle to unref.

__Examples__

none

---

## has_ref

```lua
uv.has_ref( uv_handle )
```

Returns non-zero if the handle referenced, zero otherwise.

__Parameters__

Name|Details
----|-------
uv_handle|A handle to check.

__Examples__

none

---

## send_buffer_size

```lua
uv.send_buffer_size( uv_handle, buffer_size )
```

Gets or sets the size of the send buffer that the operating system uses for the socket.

!!! note ""
    If value == 0, it will return the current send buffer size, otherwise it will use value to set the new send buffer size.

    This function works for TCP, pipe and UDP handles on Unix and for TCP and UDP handles on Windows.

__Parameters__

Name|Details
----|-------
uv_handle|A handle to get or set.
buffer_size|A number to indicate the buffer size.

__Examples__

none

---

## recv_buffer_size

```lua
uv.recv_buffer_size( uv_handle, buffer_size )
```

Gets or sets the size of the receive buffer that the operating system uses for the socket.

!!! note ""
    If value == 0, it will return the current receive buffer size, otherwise it will use value to set the new receive buffer size.

    This function works for TCP, pipe and UDP handles on Unix and for TCP and UDP handles on Windows.

__Parameters__

Name|Details
----|-------
uv_handle|A handle to check.
buffer_size|A number to indicate the buffer size.

__Examples__

none

---

## fileno

```lua
uv.fileno( uv_handle )
```

Gets the platform dependent file descriptor equivalent.

__Parameters__

Name|Details
----|-------
uv_handle|A handle to check.

__Examples__

none
