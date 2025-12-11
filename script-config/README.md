# 📑 Script Config

{% hint style="info" %}
Here's how script config works.

{% code title="Explanation" %}
```lua
-- ["Config"] = <bool>
["Bool"] = true
["Bool"] = false

-- ["Config"] = <string>
["String"] = "abc"

-- ["Config"] = <number>
["Number"] = 12

-- ["Config"] = <arg>
["Arg"] = {1, 2}
["Arg"] = {"abc", "xyz"}
```
{% endcode %}
{% endhint %}

{% hint style="warning" %}
Make sure the config always have the comma (`,`) at the end of it.
{% endhint %}

{% hint style="success" %}
Good example

```lua
-- bool
["Raid if Maxed Blox Fruit"] = true,
-- string
["Farm method after maxed"] = "Raid Boss Farm - Cake Prince Farm",
-- arg
["Performance"] = {
    ["Hide Map"] = true,
    ["Black Screen"] = true,
    ["Lock FPS"] = 30,
},
["Blox Fruit Sniper"] = {
    "Dough-Dough",
    "Leopard-Leopard",
},
```
{% endhint %}

{% hint style="danger" %}
Bad example

```lua
-- bool
["Raid if Maxed Blox Fruit"] = true -- missing comma (,) at the end
-- string
["Farm method after maxed"] = Raid Boss Farm - Cake Prince Farm, -- a string must inside " or '
-- arg
["Performance"] = {
    ["Hide Map"] = true -- missing comma (,) at the end
    ["Black Screen"] = true -- missing comma (,) at the end
    ["Lock FPS"] = 30,
},
["Blox Fruit Sniper"] = {
    "Dough-Dough", -- missing comma (,) at the end
    Leopard-Leopard, -- a string must inside " or '
},
```
{% endhint %}
