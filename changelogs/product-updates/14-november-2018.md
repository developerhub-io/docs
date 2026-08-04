---
title: '14 November 2018'
date: '2018-11-14 10:28:53'
published: true
---

- {% badge text="New" type="success" /%} **Lua and C#**: Added support for Lua and C# languages in code-blocks.

{% code %}
```lua
-- defines a factorial function
function fact (n)
if n == 0 then
return 1
else
return n \* fact(n-1)
end
end

print("enter a number:")
a = io.read("_number") -- read a number
print(fact(a))
```

```csharp
int Factorial(int i)
{
if (i <= 1)
return 1;
return i _ Factorial(i - 1);
}
```
{% /code %}

- {% badge text="Bug Fix" type="error" /%} **Code text**: Long text in code could have broken the page layout.
