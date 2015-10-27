## new_async

```lua
uv.new_async( cb )
```

Initialize the handle. A NULL callback is allowed.

__Parameters__

Name|Details
----|-------
callback|A callback function.

__Examples__

none

## async_send

```lua
uv.async_send(async_ref)
```

Wakeup the event loop and call the async handle’s callback.

__Parameters__

Name|Details
----|-------
async_ref|Reference to an async handle.

__Examples__

none

### See also

[handles](../handles)
