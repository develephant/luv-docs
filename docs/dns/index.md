## getaddrinfo

```lua
uv.getaddrinfo( getaddrinfo_req, callback, node, service, hints )
```

Asynchronous getaddrinfo.

__Parameters__

none

__Examples__

```lua
local function callback()
  print('addr')
end
uv.getaddrinfo( getaddrinfo_req, callback, node, service, hints )
```

---

## getnameinfo

```lua
uv.getnameinfo( getnameinfo_req, callback, addr, flags )
```

Asynchronous getnameinfo.

__Parameters__

none

__Examples__

```lua
local function callback()
  print('name')
end
uv.getnameinfo( getnameinfo_req, callback, addr, flags )
```

---

### See also

The following API functionality applies to all __requests__ and __handles__:

[requests](../requests)
[handles](../handles)
