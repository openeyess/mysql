# mysql
A library that makes contact with MySQL via API.

## How to use

```lua
require('mysql')

query(string sql [, table values], function(err, result, fields) callback)
```

## How to implement

Add `builds`, `libs` and `meta.xml` files

## Examples

With values
```lua
require('mysql')

query('SELECT ? + ?', {1, 2}, function(err, result, fields)
  if (err) then return iprint(err) end
  print(result)
end)
```

No values
```lua
require('mysql')

query('SELECT 1 + 2', function(err, result, fields)
  if (err) then return iprint(err) end
  print(result)
end)
```
