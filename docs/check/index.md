!!! note "Purpose"
    Check handles will run the given callback once per loop iteration, right after polling for i/o.

## new_check

```lua
uv.new_check()
```

Initialize the handle.

__Parameters__

none

__Examples__

```lua
local check_handle = uv.new_check()
```

---

## check_start

```lua
uv.check_start( check_handle, callback )
```

Start the handle with the given callback.

__Parameters__

none

__Examples__

```lua
uv.check_start( check_handle, function()
  print( 'checking...' )
end )
```

---

## check_stop

```lua
uv.check_stop( check_handle )
```

Stop the handle, the callback will no longer be called.

__Parameters__

none

__Examples__

```lua
uv.check_stop( check_handle )
```

---

### See also

The following API functionality applies to all __handles__:

[handles](../handles)
