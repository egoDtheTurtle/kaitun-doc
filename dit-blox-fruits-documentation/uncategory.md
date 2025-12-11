# Uncategory

### Fast Attack Duration/Cooldown

For who keep getting kicked for "Stop trying to lag the server, or you will be banned.", otherwise leave this alone, don't touch.\
Example: you put {2, 5} so it will Fast Attack for 2 seconds then stop and wait 5 seconds before Attack No Cooldown for 2 seconds again.\
So put `{2, 5}` or `{1, 5}` if you got kicked, or completely disable Fast Attack by set to `{0, 0}`.\
**This Fast Attack Duration/Cooldown only applied on mobs higher you 200 levels** otherwise mobs below or same as your level is fine to keep Fast Attacking without getting kick.

```lua
["Fast Attack Duration/Cooldown"] = {<number>, <number>}
```

### Raid if Maxed Blox Fruit

Will go Raid if maxed stored Blox Fruit amount (and you have a Blox Fruit in your Hot bar).

```lua
["Raid if Maxed Blox Fruit"] = <bool>
```

### Farm boss drops while not maxed

While farming for level/items if boss spawned and you dont have their drop it will go kill them.

```lua
["Farm boss drops while not maxed"] = <bool>
```

### Farm Blox Fruit Mastery if maxed

If you ate an Blox Fruit, will farm Blox Fruit's mastery when maxed while [Extra Time](extra-time.md).

```lua
["Farm Blox Fruit Mastery if maxed"] = <bool>
```

### Farm method after maxed

After reached max Level, it will do the thing you set.

```lua
["Farm method after maxed"] = <string>
```

{% code title="Method list" %}
```
"Mob Farm - Level Path"
"Raid Boss Farm - Cake Prince Farm"
"Mob Aura - Haunted Castle"
"Mob Aura - Sea of Treats 4"
```
{% endcode %}

### Extra time Farm until unlock skills

During [Extra Time](extra-time.md).\
`true` Will farm Fighting Styles/Weapons until unlocked all it skill and switch to another.\
`false` Like above but farming until 600 Mastery then switch to another.

```lua
["Extra time Farm until unlock skills"] = <bool>
```

### Auto Race

After complete [Do Action](do-action.md) will do Race v2/v3.\
Put `None` if you want to disable.

```lua
["Auto Race"] = <string>
```

{% code title="Race list" %}
```
"Human"
"Mink"
"Fishman"
```
{% endcode %}
