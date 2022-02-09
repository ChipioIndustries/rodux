# Rodux

This is a fork of [Roblox/rodux](https://github.com/Roblox/rodux) that introduces multiple quality-of-life improvements.

## getValueChangedSignal

The `Store:getValueChangedSignal(string path)` function returns a signal that fires when that specific value changes.

```lua
store:getValueChangedSignal("playerData.ChipioIndustries"):connect(function(newValue, oldValue)
	print("My player data changed from ", oldValue, "to", newValue)
end)
```

If the value being listened to is a table, replacing the table will fire the signal even if the table contents don't change.

## Installing with Wally

* Add this line to your `wally.toml` file under `[dependencies]`:

	```toml
	Rodux = "chipioindustries/rodux@3.0.2"
	```

* Then run `wally install` to install the package.
* 