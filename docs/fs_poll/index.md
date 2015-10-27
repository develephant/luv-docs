## new_fs_poll

```lua
uv.new_fs_poll()
```

Initialize the handle.

__Parameters__

none

__Examples__

```lua
local fs_poll_handle = uv.new_fs_poll()
```

---

## fs_poll_start

```lua
uv.fs_poll_start( fs_poll_handle, callback, filepath, interval )
```

Check the file at path for changes every interval milliseconds.

__Parameters__

Name|Details
----|-------
fs_poll_handle|The fs poll handle.
callback|The callback function.
filepath|The filepath to poll.
interval|Amount in milliseconds.

!!! note "Tip"
    For maximum portability, use multi-second intervals. Sub-second intervals will not detect all changes on many file systems.

__Examples__

```lua
local function cb()
  print( 'polled' )
end

uv.fs_poll_start( fs_poll_handle, cb, '/some/filepath', 2000 ) --every 2 secs
```

---

## fs_poll_stop

```lua
uv.fs_poll_stop( fs_poll_handle )
```

Stop the handle, the callback will no longer be called.

__Parameters__

Name|Details
----|-------
fs_poll_handle|The fs poll handle.


__Examples__

```lua
uv.fs_poll_stop( fs_poll_handle )
```

---

## fs_poll_getpath

```lua
uv.fs_poll_getpath( fs_poll_handle )
```

Get the path being monitored by the handle.

__Parameters__

Name|Details
----|-------
fs_poll_handle|The fs poll handle.


__Examples__

```lua
local polling_path = uv.fs_poll_getpath( fs_poll_handle )
```

---

### See also

The following API functionality applies to all __handles__:

[handles](../handles)
