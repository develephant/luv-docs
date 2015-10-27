!!! note "Usage"
    Async handles allow the user to “wakeup” the event loop and get a callback called from another thread.

## new_async

```lua
uv.new_async( callback )
```

Initialize the handle. A NULL callback is allowed.

__Parameters__

Name|Details
----|-------
callback|A callback function.

__Examples__

```lua
local async_handle = uv.new_async(function()
  -- Doing some work...
end )
```

---

## async_send

```lua
uv.async_send( async_handle )
```

Wakeup the event loop and call the async handle’s callback.

__Parameters__

Name|Details
----|-------
async_handle|Reference to an async handle.

__Examples__

```lua
uv.async_send( async_handle )
```

---

### See also

The following API functionality applies to all __handles__:

[handles](../handles)
