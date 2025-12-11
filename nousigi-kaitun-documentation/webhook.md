# Webhook Options

Use the `Webhook` table to mirror key events into external services (Discord, Slack, etc.).

## Url

Set the webhook endpoint the script should post to. Leave empty to disable notifications entirely. Make sure the service you target accepts standard JSON payloads.

## Ignore Notify

Skip notifications for specific animals and mutation types.

```lua
["Ignore Notify"] = {
    ["La Vacca Saturno Saturnita"] = {
        "Normal",
        "Gold",
    },
},
```

- `"La Vacca Saturno Saturnita"` is the animal name.
- Mutation filters can be `Normal`, `Gold`, `Diamond`, `Rainbow`, etc. Add only the variants you want to suppress.
