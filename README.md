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

## Installing with Rojo

* Download the `Packaged.zip` file from the [releases page](https://github.com/ChipioIndustries/rodux/releases).
* Unzip the file into the desired location in your project.

## Installing with Roblox

* Download the `rbxm` model file from the [releases page](https://github.com/ChipioIndustries/rodux/releases).
* Drag the model into Roblox Studio to add it to the game.
