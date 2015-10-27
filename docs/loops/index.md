!!! note "Purpose"
    The event loop is the central part of libuv’s functionality. It takes care of polling for i/o and scheduling callbacks to be run based on different sources of events.

## run

```lua
uv.run( mode )
```

This function runs the event loop. It will act differently depending on the specified mode:

__Modes__

Mode|Details
----|------
"default"|Runs the event loop until there are no more active and referenced handles or requests.
"once"|Poll for i/o once. Note that this function blocks if there are no pending callbacks.
"nowait"|Poll for i/o once but don’t block if there are no pending callbacks.


__Parameters__

Name|Details
----|-------
mode|The loop mode. See __Modes__ above.

__Examples__

```lua
uv.run( "default" )

--OR

uv.run()
```

---

## loop_alive

```lua
uv.loop_alive()
```

Returns non-zero if there are active handles or request in the loop.

__Parameters__

none

__Examples__

```lua
uv.loop_alive()
```

---

## stop

```lua
uv.stop()
```

Stop the event loop, causing __[run](#run)__ to end as soon as possible. This will happen not sooner than the next loop iteration. If this function was called before blocking for i/o, the loop won’t block for i/o on this iteration.

__Parameters__

none

__Examples__

```lua
uv.stop()
```

---


## loop_close

```lua
uv.loop_close()
```

Closes all internal loop resources. This function must only be called once the loop has finished its execution

__Parameters__

none

__Examples__

```lua
uv.loop_close()
```

---

## backend_fd

```lua
uv.backend_fd()
```

Get backend file descriptor. Only kqueue, epoll and event ports are supported.

__Parameters__

none

__Examples__

```lua
local be_fd = uv.backend_fd()
```

---

## backend_timeout

```lua
uv.backend_timeout()
```

Get the poll timeout. The return value is in milliseconds, or -1 for no timeout.

__Parameters__

none

__Examples__

```lua
local be_timeout = uv.backend_timeout()
```

---

## now

```lua
uv.now()
```

Return the current timestamp in milliseconds. The timestamp is cached at the start of the event loop tick.

__Parameters__

none

__Examples__

```lua
local now = uv.now()
```

---

## update_time

```lua
uv.update_time()
```

Update the event loop’s concept of “now”. Libuv caches the current time at the start of the event loop tick in order to reduce the number of time-related system calls.

!!! note "Note"
    You won’t normally need to call this function unless you have callbacks that block the event loop for longer periods of time, where “longer” is somewhat subjective but probably on the order of a millisecond or more.

__Parameters__

none

__Examples__

```lua
uv.update_time()
```

---

## walk

```lua
uv.walk( walk_callback )
```

Walk the list of handles: __walk_callback__ will be executed with the given arg.

__Parameters__

Name|Details
----|-------
walk_callback|The function to be run on each handle.

__Examples__

```lua
uv.walk( walk_callback )
```

---
