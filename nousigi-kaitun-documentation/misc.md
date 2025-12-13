# Misc

The `Misc` table contains protective routines and quality-of-life actions.

## Kick if Ping above

Monitors average network latency over 30 seconds. If the ping stays above the configured value, the script force-kicks the player to avoid mis-buying animals while lagging.

```lua
["Kick if Ping above"] = 750,
```

## Kick if FPS below

Tracks the average frame rate across the last 60 seconds. If it remains below the configured threshold for over 30 seconds, the script kicks the player. Low FPS reduces input accuracy and can trigger bad purchases.

```lua
["Kick if FPS below"] = 5,
```

## Max Rebirth

Sets an upper limit for automated rebirths. When your rebirth count is **equal to or higher** than this value, script stops rebirthing. The script never rebirths if a generation `10m+` animal is active in your base.

* Set to `-1` to disable rebirths entirely.
* Set to `0` to always rebirth up to the current maximum.

```lua
["Max Rebirth"] = 5,
```

In the example above, rebirthing stops after reaching 5 rebirths.

## Rare Animal Generation

Defines the minimum generation-per-second value that marks an animal as **rare**. Rare animals are never sold and stop rebirths while they stay in your base. Accepts shorthand values like `10B`, `100.5M`, or `1.5T`.

```lua
["Rare Animal Generation"] = "10M",
```

## Ignore Secret

Treats the listed secret animals as regular animals. They can be sold if the base is full, and the Black Screen color is unaffected. Configure entries with the animal name and mutation types you want to treat as normal.

```lua
["Ignore Secret"] = {
    ["La Vacca Saturno Saturnita"] = {
        "Normal",
        "Gold",
        "All",
    },
},
```

* `"La Vacca Saturno Saturnita"` is the animal name.
* Mutation values include `Normal`, `Gold`, `Diamond`, `Rainbow`, etc. Use `"All"` to cover every mutation.

## Auto Fuse

Automatically finds the listed secret animal in your base and sends it to the Fuse machine. While getting animals to fuse, if a [Rare Animal Generation](misc.md#rare-animal-generation) spawned, script will cancel the current task and go purchase it.

* `Enable`: toggles the automaton on or off.
* `Fuse Animal`: list of animals that should be fused, with their mutation filters like the [Ignore Secret](misc.md#ignore-secret) config above, will priority fusing the lowest generation animals first.

```lua
["Auto Fuse"] = {
    ["Enable"] = true,
    ["Fuse Animal"] = {
        ["La Vacca Saturno Saturnita"] = {
                "All",
        },
    },
},
```

The `Fuse Animal` can also be `"All"` to make it fuse every animals in your base, but not the [Rare Animal Generation](misc.md#rare-animal-generation). Will fuse the lowest generation animals first.

```lua
["Fuse Animal"] = "All",
```

## Buy Lucky Block

Prioritizes purchasing the listed Lucky Blocks. The script will sell regular animals (never ones that match [Rare Animal Generation](misc.md#rare-animal-generation)) if necessary to free space.

```lua
["Buy Lucky Block"] = {
    "Secret Lucky Block",
},
```

Available names (not 100% real time up-to-dated):

```
"Los Lucky Blocks",
"Taco Lucky Block",
"Admin Lucky Block",
"Secret Lucky Block",
"Brainrot God Lucky Block",
"Mythic Lucky Block",
"Spooky Lucky Block",
```

Set to `"All"` to buy every Lucky Block except Mythic and Brainrot God.

## Open Lucky Block

Opens the Lucky Blocks you list. Names must match exactly what you configured inside [Buy Lucky Block](misc.md#buy-lucky-block) (set the config just like the one above).
