# Hop Server

### \[Main] Server Hop

The main of Hop Server, will Hop Server for anything that require to Hop Server (find Items/Bosses/etc).

```lua
["[Main] Server Hop"] = <bool>
```

### \[Farm] Server Hop if Player nearby

Like it's name, will Hop Server whenever a Player nearby you.

```lua
["[Farm] Server Hop if Player nearby"] = <bool>
```

### \[Sea 3 Quest] Server Hop for 1M+ Blox Fruit

When you reached level 1,500 and don't have 1M+ value Blox Fruit, will Hop Server looking for a Blox Fruit that have 1M+ value to get to Sea 3.

```lua
["[Sea 3 Quest] Server Hop for 1M+ Blox Fruit"] = <bool>
```

### Delay

The seconds wait before Hop Server.\
If this higher than `120` It will do [Farm method after maxed](uncategory.md#farm-method-after-maxed), otherwise it will standing still.\
If you have large quantity of account running in same device/internet I recommended that you should put this above `300` or disable Hop Server entirely.\
Maximum amount of the delay is `7200` (2 hours).

```lua
["Delay"] = <number>
```
