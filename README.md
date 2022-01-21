# V1PER Documentation page

**[!] Any sort of resources used in this are all made by me.**


**[!] This has had a lot of work, dedication and investigation, this is NOT finished. This is the beta release, for my time I have been away, I’ve been working on this. Expect it soon.**

V1PER is a module created for developers, to make things much easier- Including built-in datastore systems, banning systems, admin, pre-done code, and much more!

## Datastores
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

## Admin

_(This is just a placeholder for when it comes out)_

## Banning System

_(This is just a placeholder for when it comes out)_

## Pre-done code

_(This is just a placeholder for when it comes out)_
