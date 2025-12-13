# Webhook

Use the `Webhook` table to mirror key events into external services (Discord, Slack, etc.).

## Url

Set the webhook endpoint the script should post to. Leave empty to disable notifications entirely.

Make sure the service you target accepts standard JSON payloads, usually Discord.

```lua
["Url"] = "",
```

## Ignore Notify

Skip notifications for specific animals and mutation types.

```lua
["Ignore Notify"] = {
    ["La Vacca Saturno Saturnita"] = {
        "Normal",
        "Gold",
        "All",
    },
},
```

* `"La Vacca Saturno Saturnita"` is the animal name.
* Mutation filters can be `Normal`, `Gold`, `Diamond`, `Rainbow`, etc. Add only the variants you want to suppress. Use `"All"` to cover every mutation.
