# 📑 Script Config

{% hint style="info" %}
How to structure your Nousigi Kaitun config file.

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

For complete examples of valid and invalid structures, see the [Formatting Examples](examples.md) page.


# Formatting Examples

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
-- arg
["Misc"] = {
    ["Ignore Secret"] = {
        ["La Vacca Saturno Saturnita"] = {
            "All",
        },
    },
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
-- arg
["Misc"] = {
    ["Ignore Secret"] = {
        "La Vacca Saturno Saturnita" -- missing comma (,) at the end
        ["All"], -- bad syntax
    },
},
```
{% endhint %}
