!!! note "Purpose"
    FS Event handles allow the user to monitor a given path for changes, for example, if the file was renamed or there was a generic change in it. This handle uses the best backend for the job on each platform.

## new_fs_event

```lua
uv.new_fs_event()
```

Initialize the handle.

__Parameters__

none

__Examples__

```lua
local fs_event_handle = uv.new_fs_event()
```

---

## fs_event_start

```lua
uv.fs_event_start( fs_event_handle, callback )
```

Start the handle with the given callback.

__Parameters__

Name|Details
----|-------
fs_event_handle|The fs event handle.
callback|The callback function.

__Examples__

```lua
uv.fs_event_start( fs_event_handle, function()
  print( 'fs event' )
end )
```

---

## fs_event_stop

```lua
uv.fs_event_stop( fs_event_handle )
```

Stop the handle, the callback will no longer be called.

__Parameters__

Name|Details
----|-------
fs_event_handle|The fs event handle.

__Examples__

```lua
uv.fs_event_stop( fs_event_handle )
```

---

## fs_event_getpath

```lua
uv.fs_event_getpath( fs_event_handle )
```

Get the path being monitored by the handle.

__Parameters__

Name|Details
----|-------
fs_event_handle|The idle handle.

__Examples__

```lua
local path = uv.fs_event_getpath( fs_event_handle )
```

---

### See also

The following API functionality applies to all __handles__:

[handles](../handles)
