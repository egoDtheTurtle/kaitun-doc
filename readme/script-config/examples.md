# Formatting Examples

## 📑 Script Config

{% hint style="info" %}
How to structure your config file.

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
Finish every entry with a comma (`,`) to avoid syntax errors.
{% endhint %}

## Formatting Examples

Use these samples to compare your configuration against known good and bad patterns.

{% hint style="success" %}
**Valid structure**

```lua
-- bool
["Performance"] = {
    ["Black Screen"] = true,
},

-- string
["Gameplay"] = {
    ["Server Type"] = "Private",
},

-- number
["Performance"] = {
    ["FPS Cap"] = 10,
},

-- arg
["Misc"] = {
    ["Ignore Secret"] = {
        ["La Vacca Saturno Saturnita"] = {
            "All",
        },
    },
},
["Buy Lucky Block"] = {
    "Secret Lucky Block",
},
```
{% endhint %}

{% hint style="danger" %}
**Common mistakes**

```lua
-- bool
["Performance"] = {
    ["Black Screen"] = true -- missing comma (,) at the end
},

-- string
["Gameplay"] = {
    ["Server Type"] = Private, -- a string must be inside " or '
},

-- number
["Performance"] = {
    ["FPS Cap"] = "10" -- a number shouldn't be inside " or '
},

-- arg
["Misc"] = {
    ["Ignore Secret"] = {
        "La Vacca Saturno Saturnita" -- missing comma (,) at the end
        ["All"], -- bad syntax
    },
},
["Misc"] = {
    ["Ignore Secret"] = {
        "La Vacca Saturno Saturnita", -- missing mutation type
    },
},
["Buy Lucky Block"] = "Secret Lucky Block" -- arg type must be inside {}
["Buy Lucky Block"] = {
    Secret Lucky Block, -- string must be inside " or '
}
```
{% endhint %}
