# Viper

Discontinued. It has old documentation, and may not be the best to understand;

# V1PER Documentation page

V1PER; https://www.roblox.com/library/8547614595/V1PER-BETA

**[!] Any sort of resources used in this are all made by me.**


**[!] This has had a lot of work, dedication and investigation, this is NOT finished. This is the beta release, for my time I have been away, I’ve been working on this. Expect it soon.**

V1PER is a module created for developers, to make things much easier- Including built-in datastore systems, banning systems, admin, pre-done code, and much more!

# Datastores
_(Note: You need to enable API Services in your game settings to make this work)_

Datastores can be used in leaderstats to save data for players.

We can use the _BuildNewLeaderstats()_ function to be able to create leaderstats, and apply them in the correct format for the datastore functions to work.

```
local V1PER = require(V1PER.Path)

game.Players.PlayerAdded:Connect(function(Player)
  local Data = V1PER.DataStoreResource.BuildNewLeaderstats({
    -- One of these is a single leaderstats
    {
      Name = "Diamonds",
      TypeValue = "Int",
      Default = 200
    }
  }, Player)
  
  V1PER.DataStoreResoruce.LoadData(Player, Data)
end
```

There, now we can load some data, this will also create the leaderstats.
Now, we need to save our data, or else what's the point?

```
local V1PER = require(V1PER.Path)

game.Players.PlayerAdded:Connect(function(Player)
  local Data = V1PER.DataStoreResource.BuildNewLeaderstats({
    -- One of these is a single leaderstats
    {
      Name = "Diamonds",
      TypeValue = "Int",
      Default = 200
    }
  }, Player)
  
  V1PER.DataStoreResoruce.LoadData(Player, Data)
end)

game.Players.PlayerRemoving:Connect(function(Player)
  V1PER.DataStoreResource.SaveData(Player)
end)
```

There, with this we can now save our diamonds, and if we never played, we will have the default ammount; 200

# Admin

_(This is just a placeholder for when it comes out)_

# Banning System

Create a ServerScript in ServerScriptService and add this code;

```
local V1PER = require(V1PER.Path)

game.Players.PlayerAdded:Connect(V1PER.BanningSystem.ConnectPlayerAdded)
```

and you can use this command in the module to add a player to the banning list:

```
local V1PER = require(V1PER.Path)

V1PER.BanningSystem.BanUser(ID, ReasonForBan)
```

# Pre-done code

_(This is just a placeholder for when it comes out)_

[OLD POST](https://devforum.roblox.com/t/v1per-the-developer-toolbox-updated/1628724)

[BETA DOWNLOAD](V1PER-BETA.rbxm)