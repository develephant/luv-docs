## new_idle

```lua
uv.new_idle()
```

Initialize the handle.

__Parameters__

none

__Examples__

```lua
local idle_handle = uv.new_idle()
```

---

## idle_start

```lua
uv.idle_start( idle_handle, callback )
```

Start the handle with the given callback.

__Parameters__

Name|Details
----|-------
idle_handle|The idle handle.
callback|A callback function.

__Examples__

```lua
uv.idle_start( idle_handle, function()
  print( 'idlin' )
end )
```

---

## idle_stop

```lua
uv.idle_stop( idle_handle )
```

Stop the handle, the callback will no longer be called.

__Parameters__

Name|Details
----|-------
idle_handle|The idle handle.
callback|A callback function.

__Examples__

```lua
uv.idle_stop( idle_handle )
```

---

### See also

The following API functionality also applies:

[handles](../handles)
