# Script Config

The default Steal a Brainrot config:

```lua
getgenv().Config = {
    ["Gameplay"] = {
        ["Server Type"] = "Private",
        -- Private Server config
        ["Collect Cash Cap"] = "10B",
        -- Public Server config
        ["Max Auctioning Multiplier"] = 10,
        ["Lock Base Extra Time"] = 5,
    },
    ["Misc"] = {
        ["Kick if Ping above"] = 750,
        ["Kick if FPS below"] = 5,
        ["Max Rebirth"] = 0,
        ["Rare Animal Generation"] = "10M",
        ["Only keep Secret if Cash Cap"] = true,
        ["Ignore Secret"] = {},
        ["Auto Fuse"] = {
            ["Enable"] = false,
            ["Fuse Animal"] = {},
        },
        ["Buy Lucky Block"] = {},
        ["Open Lucky Block"] = {},
        ["Rare Lucky Block"] = {
            "Secret Lucky Block",
        },
    },
    ["Performance"] = {
        ["FPS Cap"] = 10,
        ["Black Screen"] = true,
    },
    ["Webhook"] = {
        ["Url"] = "",
        ["Ignore Notify"] = {},
    },
}
```

Use these defaults as a base before applying your own overrides and deployment keys.
