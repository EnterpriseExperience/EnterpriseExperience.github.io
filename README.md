# Flames Hub | Documentation

## Introduction

Welcome to the official Flames Hub documentation page, enjoy our BETA API!

---

## © | Flames Hub API | ©

### Loadstring | Setup (required).
```lua
-- Setup --
local Flames_API = loadstring(game:HttpGet('https://raw.githubusercontent.com/EnterpriseExperience/MicUpSource/refs/heads/main/Flame_Hubs_API.lua'))()
```

### Character initialization.
```lua
local Character = Flames_API.Character
```

### Head.
```lua
local Head = Flames_API.Head

if Head then
    print(Head.Name)
end
```

### HumanoidRootPart.
```lua
local HumanoidRootPart = Flames_API.HumanoidRootPart

if HumanoidRootPart then
    print(HumanoidRootPart.Name)
end
```

### PlayerGui.
```lua
local PlayerGui = Flames_API.PlayerGui

if PlayerGui then
    print(PlayerGui.Name)
end
```

### Executor Name.
```lua
-- Works on ANY executor. --
-- Prints just the Name of the executor, doesn't include the version or other details. --
local Executor_Name = Flames_API.ExecutorName()

print(Executor_Name)
```

### Services.
```lua
-- CAN protect services via 'cloneref' (if supported) --
-- EXAMPLES: --
local Players = Flames_API.Service("Players")
local ReplicatedStorage = Flames_API.Service("ReplicatedStorage")
local Workspace = Flames_API.Service("Workspace")
local ReplicatedFirst = Flames_API.Service("ReplicatedFirst")
local VoiceChatInternal = Flames_API.Service("VoiceChatInternal")
local VoiceChatService = Flames_API.Service("VoiceChatService")
local StarterGui = Flames_API.Service("StarterGui")
-- etc/add other services. --
```

### Vehicles.
```lua
-- Only works if you are currently in a vehicle! --
local Vehicle = Flames_API.Vehicle()

if Vehicle then
    print(Vehicle)
end
```

### Target player(s) functionality.
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

### SeatPart.
```lua
local Current_SeatPart = Flames_API.SeatPart

print(Current_SeatPart)
```

### Defining LocalPlayer.
```lua
local LocalPlayer = Flames_API.LocalPlayer

print(LocalPlayer.Name)
```

### Random string generation.
```lua
local Randomized_String = Flames_API.RandomString("hello?") -- String input

print(Randomized_String)
```

### WalkSpeed changer.
```lua
-- Set WalkSpeed --
function Change_WS(New_Speed)
    Flames_API.WalkSpeed = New_Speed
end

Change_WS(60)
```

### JumpPower/JumpHeight changer.
```lua
-- Set JumpPower/JumpHeight (supports both) --
function Change_JP(New_JP)
    Flames_API.JumpPower(New_JP)
end

Change_JP(100)
```

### Teleport/GoTo to other players.
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

### WalkSpeed Anti-Cheat Bypass (getconnections only!)
```lua
local Get_Connections = getconnections or get_signal_cons

if not Get_Connections then return warn("Your executor does not support 'getconnections'!") end

if Get_Connections then
    Flames_API.BypassWalkSpeed()
end
```

### JumpPower Anti-Cheat Bypass (getconnections only!)
```lua
-- Bypasses JumpPower AND JumpHeight --
local Get_Connections = getconnections or get_signal_cons

if not Get_Connections then return warn("Your executor does not support 'getconnections'!") end

if Get_Connections then
    Flames_API.BypassJumpPower()
end
```
