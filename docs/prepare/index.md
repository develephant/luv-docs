!!! note ""
    Prepare handles will run the given callback once per loop iteration, right before polling for i/o.

## new_prepare

```lua
uv.new_prepare()
```

Initialize the handle.

__Parameters__

none

__Examples__

```lua
local prepare_handle = uv.new_prepare()
```

---

## prepare_start

```lua
uv.prepare_start( prepare_handle, callback )
```

Start the handle with the given callback.

__Parameters__

none

__Examples__

```lua
uv.prepare_start( prepare_handle, function()
  print( 'preparing...')
end )
```

---

## prepare_stop

```lua
uv.prepare_stop( prepare_handle )
```

Stop the handle, the callback will no longer be called.

__Parameters__

none

__Examples__

```lua
uv.prepare_stop( prepare_handle )
```

---

### See also

The following API functionality applies to all __handles__:

[handles](../handles)
