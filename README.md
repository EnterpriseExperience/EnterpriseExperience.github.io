# Flames Hub | Documentation

## Introduction

Welcome to the official Flames Hub documentation page, empowering success.

---

## Examples

### Introduction | Flames Hub API

```lua
-- Setup --
local Flames_API = loadstring(game:HttpGet('https://raw.githubusercontent.com/EnterpriseExperience/MicUpSource/refs/heads/main/Flame_Hubs_API.lua'))()
```

```lua
-- Get your Character --
local Character = Flames_API.Character
```

```lua
-- Get your Head --
local Head = Flames_API.Head
```

```lua
-- Get your HumanoidRootPart --
local HumanoidRootPart = Flames_API.HumanoidRootPart
```

```lua
-- Get your PlayerGui --
local PlayerGui = Flames_API.PlayerGui
```

```lua
-- Works on ANY executor --
-- Prints the current executor (just the Name of the executor, doesn't include the version) --
local Executor_Name = Flames_API.ExecutorName()

print(Executor_Name)
```

```lua
-- Services --
-- Utilizes and protects services via 'cloneref' (if supported) --
local Players = Flames_API.Service("Players")
local ReplicatedStorage = Flames_API.Service("ReplicatedStorage")
local Workspace = Flames_API.Service("Workspace")
local ReplicatedFirst = Flames_API.Service("ReplicatedFirst")
local VoiceChatInternal = Flames_API.Service("VoiceChatInternal")
local VoiceChatService = Flames_API.Service("VoiceChatService")
local StarterGui = Flames_API.Service("StarterGui")
-- etc --
```

```lua
-- Grabbing 'Vehicle' Model's (if you're sitting in one) --
local Vehicle = Flames_API.Vehicle()

if Vehicle then
    print(Vehicle)
end
```

```lua
-- Targetting other players --
-- Supports shortened Usernames/DisplayNames --
-- Supports DisplayNames --
-- Supports Usernames --
local Target = Flames_API.FindPlayer("Roblox")

if Target and Target.Character then
    print(Target.Name)
end
```

```lua
-- Seat Part (if you're sitting down in a Model)
local Current_SeatPart = Flames_API.SeatPart

print(Current_SeatPart)
```

```lua
-- Defining LocalPlayer --
local LocalPlayer = Flames_API.LocalPlayer

print(LocalPlayer.Name)
```

```lua
-- Randomizing Strings (Credits: Infinite Yield) --
local Randomized_String = Flames_API.RandomString("hello?")

print(Randomized_String)
```

```lua
-- Set WalkSpeed --
function Change_WS(New_Speed)
    Flames_API.WalkSpeed = New_Speed
end

Change_WS(60)
```

```lua
-- Set JumpPower/JumpHeight (supports both) --
function Change_JP(New_JP)
    Flames_API.JumpPower(New_JP)
end

Change_JP(100)
```

```lua
-- Teleport to any player --
local Target = Flames_API.FindPlayer("Roblox")
function Teleport_To_Player(Player)
    Flames_API.GoTo(Player)
end

if Target and Target.Character then
    Teleport_To_Player(Target)
end
```

```lua
-- Bypass WalkSpeed (getconnections only!) --
local Get_Connections = getconnections or get_signal_cons

if not Get_Connections then return warn("Your executor does not support 'getconnections'!") end

if Get_Connections then
    Flames_API.BypassWalkSpeed()
end
```

```lua
-- Bypass JumpPower (getconnections only!) --
-- Bypasses JumpPower AND JumpHeight --
local Get_Connections = getconnections or get_signal_cons

if not Get_Connections then return warn("Your executor does not support 'getconnections'!") end

if Get_Connections then
    Flames_API.BypassJumpPower()
end
```
