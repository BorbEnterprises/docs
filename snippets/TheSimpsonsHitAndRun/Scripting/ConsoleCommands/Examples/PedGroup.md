{{ tabs }}
{{ tab MFK }}
```js
// Example from missions/level01/leveli.mfk
CreatePedGroup(0);
	AddPed("male6", 2);
	AddPed("girl4", 1);
	AddPed("fem4", 2);
	AddPed("boy3", 2);
ClosePedGroup();
```
{{ endtab }}
{{ tab Lua }}
```lua
-- Example from missions/level01/leveli.mfk
Game.CreatePedGroup(0)
	Game.AddPed("male6", 2)
	Game.AddPed("girl4", 1)
	Game.AddPed("fem4", 2)
	Game.AddPed("boy3", 2)
Game.ClosePedGroup()
```
{{ endtab }}
{{ endtabs }}