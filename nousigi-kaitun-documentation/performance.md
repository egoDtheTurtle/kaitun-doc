# Performance

Tune render cost for long farming sessions.

## FPS Cap

Sets the in-game frame limiter. Keeping this low (e.g., `10`) reduces CPU/GPU usage and keeps background sessions stable. Use `0` to leave the frame rate uncapped.

```lua
["FPS Cap"] = 10,
```

## Black Screen

When enabled, forces a black overlay while the script runs. This saves resources and hides rapid camera movement on unattended machines.

```lua
["Black Screen"] = true,
```
