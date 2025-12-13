# Gameplay

The `Gameplay` table shapes how script behaves in different server environments.

## Server Type

Accepted values: `Public`, `Private.`

### Public

When set to `Public`, script assumes you are in a shared lobby and enables safety routines:

* Repeatedly auctions animals you try to purchase so other players cannot snipe them.
* Frequently taps the lock button on your base.
* Attacks thieves attempting to steal animals from your base.

### Private

When set to `Private`, the script expects you to be inside a private server that you control. If it detects a public server, it will kick you to prevent unintended purchases or resets.



```lua
["Server Type"] = "Private",
```

## Collect Cash Cap (Private)

Controls how much cash is collected inside a private server. The script stops collecting once the cap is reached and parks the character at the animal spawn point to reduce accidental purchases. Accepts shorthand values such as `10B`, `100.5M`, or `1.5T`.

```lua
["Collect Cash Cap"] = "10B",
```

## Max Auctioning Multiplier (Public)

Caps how aggressively the script re-bids during auctions in public servers. The multiplier is applied to the original price. Example: if the base price is `100M` and the multiplier is `10`, the script refuses to buy once the bidding reaches `1B`.

```lua
["Max Auctioning Multiplier"] = 10,
```

## Lock Base Extra Time (Public)

Adds a delay (in seconds) before the script confirms the base lock. This gives other automated steps time to finish before the base is sealed.

```lua
["Lock Base Extra Time"] = 5,
```
