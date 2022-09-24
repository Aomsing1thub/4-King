if game:GetService("Workspace"):FindFirstChild("B)") then
game:GetService("Workspace")["B)"]:Destroy()
end

Name_GUI = "Duck HUB"
local Ui = game:GetService("CoreGui"):FindFirstChild(Name_GUI)
if Ui then
    Ui:Destroy()
end
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Aomsing1thub/Xenon-GUI/main/README.md", false))()
local CenterHubNo1 = library:CreateWindow(Name_GUI.." 🙂",Enum.KeyCode.RightControl)
local Tab = CenterHubNo1:CreateTab("Auto Farm")
local Sector1 = Tab:CreateSector("Auto Farm","left")

function TP(P)
   local Distance = (P.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
   local Speed = 15
   tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear)
   tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = P})
   tween:Play()
end

function GetPlayer(String)
   local Found = {}
   local strl = String:lower()
       for i,v in pairs(game.Players:GetPlayers()) do
           if v.Name:lower():sub(1, #String) == String:lower() then
               if v.Name ~= game.Players.LocalPlayer.Name then
               table.insert(Found,v.Name)
               end
           end
       end    
   return Found    
end

spawn(function()
        game:GetService("RunService").Heartbeat:Connect(function()
        if _G.GGEZ then
            if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Humanoid") then
                setfflag("HumanoidParallelRemoveNoPhysics", "False")
                setfflag("HumanoidParallelRemoveNoPhysicsNoSimulate2", "False")
                game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
            end
        end
    end)
end)

local savecon = {}

Sector1:AddTextbox("Select",false,function(t)
    _G.Select_Player = GetPlayer(t)[1]
end)

Sector1:AddToggle("Auto Kill",_G.Auto_Kill,function(t)
_G.Auto_Kill = t
if _G.Auto_Kill then
    _G.Noclip = true
else
    _G.Noclip = false
end
---
end)

Sector1:AddToggle("Auto Farm Money",false,function(t)
    _G.Auto_Money = t
    if _G.Auto_Money then
        _G.GGEZ = true
        _G.Noclip = true
    else
        _G.GGEZ = false
        _G.Noclip = false
        tween:Cancel()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,8,0)
    end
end)

Weapon = "Fist"

function Noclip()
for i, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
        if v:IsA("BasePart") and v.CanCollide == true then
            v.CanCollide = false
        end
    end
end

game:GetService("RunService").Stepped:Connect(function()
    if _G.Noclip then
    pcall(function()
        Noclip()
    end)
    end
end)

game:GetService("RunService").Stepped:Connect(function()
if _G.Auto_Kill then
pcall(function()
game.Players[_G.Select_Player].Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,0,-2.5)
game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(Weapon))
game:GetService'VirtualUser':CaptureController()
game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
end)
end
end)

spawn(function()
while wait() do
if _G.Auto_Money then
pcall(function()
Fire_ALL()
wait(1)
end)
end
end
end)

spawn(function()
while wait() do
if _G.Auto_Money then
pcall(function()
_G.Auto_Money1 = true
wait(8)
_G.Auto_Money1 = false
_G.Auto_Money2 = true
wait(8)
_G.Auto_Money1 = false
_G.Auto_Money2 = false
_G.Auto_Money3 = true
wait(8)
_G.Auto_Money1 = false
_G.Auto_Money2 = false
_G.Auto_Money3 = false
_G.Auto_Money4 = true
wait(8)
_G.Auto_Money1 = false
_G.Auto_Money2 = false
_G.Auto_Money3 = false
_G.Auto_Money4 = false
_G.Auto_Money5 = true
wait(8)
_G.Auto_Money1 = false
_G.Auto_Money2 = false
_G.Auto_Money3 = false
_G.Auto_Money4 = false
_G.Auto_Money5 = false
_G.Auto_Money6 = true
wait(8)
_G.Auto_Money1 = false
_G.Auto_Money2 = false
_G.Auto_Money3 = false
_G.Auto_Money4 = false
_G.Auto_Money5 = false
_G.Auto_Money6 = false
_G.Auto_Money7 = true
wait(8)
_G.Auto_Money1 = false
_G.Auto_Money2 = false
_G.Auto_Money3 = false
_G.Auto_Money4 = false
_G.Auto_Money5 = false
_G.Auto_Money6 = false
_G.Auto_Money7 = false
_G.Auto_Money8 = true
wait(8)
_G.Auto_Money1 = false
_G.Auto_Money2 = false
_G.Auto_Money3 = false
_G.Auto_Money4 = false
_G.Auto_Money5 = false
_G.Auto_Money6 = false
_G.Auto_Money7 = false
_G.Auto_Money8 = false
_G.Auto_Money9 = true
end)
end
end
end)

spawn(function()
while wait() do
if _G.Auto_Money then
pcall(function()
if _G.Auto_Money1 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5.059920787811279, 6.042726516723633, 45.41558837890625) * CFrame.new(0,-7,0)
elseif _G.Auto_Money2 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(185.20172119140625, 6.042726516723633, -8.63344955444336) * CFrame.new(0,-7,0)
elseif _G.Auto_Money3 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(391.28363037109375, 6.042646408081055, -12.520451545715332) * CFrame.new(0,-7,0)
elseif _G.Auto_Money4 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(248.52706909179688, 6.04032039642334, -274.5538024902344) * CFrame.new(0,-7,0)
elseif _G.Auto_Money5 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(162.00059509277344, 6.0425333976745605, -209.9502716064453) * CFrame.new(0,-7,0)
elseif _G.Auto_Money6 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(36.20331954956055, 6.042530059814453, -213.32644653320312) * CFrame.new(0,-7,0)
elseif _G.Auto_Money7 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-127.67198181152344, 6.042724609375, -531.7274780273438) * CFrame.new(0,-7,0)
elseif _G.Auto_Money8 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(166.43116760253906, 6.042726993560791, -573.3761596679688) * CFrame.new(0,-7,0)
elseif _G.Auto_Money9 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(182.19052124023438, 6.042085647583008, -399.63323974609375) * CFrame.new(0,-7,0)
end
end)
end
end
end)

game:GetService("RunService").Stepped:Connect(function()
    if _G.Auto_Kill then
    pcall(function()
        Noclip()
    end)
    end
end)

Sector1:AddToggle("Spectate",false,function(t)
    _G.a1 = t
    if _G.a1 then
    else
        workspace.CurrentCamera.CameraSubject = game:GetService("Players").LocalPlayer.Character.Humanoid
    end
end)

spawn(function()
while wait() do
if _G.a1 then
pcall(function()
workspace.CurrentCamera.CameraSubject = game.Players[_G.Select_Player].Character.Humanoid
end)
end
end
end)

Sector1:AddTextbox("Select Protect Player",false,function(t)
    _G.Protect_Player = GetPlayer(t)[1]
end)

Sector1:AddToggle("HITBOX",false,function(t)
    _G.a2 = t
    if _G.a2 then
    else
        for i,v in next, game:GetService('Players'):GetPlayers() do
            if v.Name ~= game:GetService('Players').LocalPlayer.Name then
                if v.Team ~= game:GetService('Players').LocalPlayer.Team then
                v.Character.HumanoidRootPart.Size = Vector3.new(2,2,1)
                v.Character.HumanoidRootPart.Transparency = 1
                end
            end
        end
    end
end)

spawn(function()
        game:GetService("RunService").Heartbeat:Connect(function()
        if _G.Fly then
            if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Humanoid") then
                game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
            end
        end
    end)
end)

spawn(function()
while wait() do
if _G.a2 then
pcall(function()
for i,v in next, game:GetService('Players'):GetPlayers() do
if v.Name ~= game:GetService('Players').LocalPlayer.Name then
    if v.Team ~= game:GetService('Players').LocalPlayer.Team then
        if v.Name ~= _G.Protect_Player then
            if v.Character.Humanoid.Health <= 27 and v.Character.Humanoid.Health >= 1 then
                pcall(function()
                v.Character.HumanoidRootPart.Size = Vector3.new(5,5,5)
                v.Character.HumanoidRootPart.Transparency = 0.7
                v.Character.HumanoidRootPart.BrickColor = BrickColor.new("Hot pink")
                end)
            elseif v.Character.Humanoid.Health <= 0 then
                pcall(function()
                v.Character.HumanoidRootPart.Size = Vector3.new(2,2,1)
                v.Character.HumanoidRootPart.Transparency = 1
                end)
            else
                pcall(function()
                    v.Character.HumanoidRootPart.Size = Vector3.new(_G.Size,_G.Size,_G.Size)
                    v.Character.HumanoidRootPart.Transparency = 0.7
                    v.Character.HumanoidRootPart.Material = "Neon"
                    v.Character.HumanoidRootPart.CanCollide = false
                end)
                if v.Character.Humanoid.Health <= 100 and v.Character.Humanoid.Health >= 81 then
                    pcall(function()
                    v.Character.HumanoidRootPart.BrickColor = BrickColor.new("Lime green")
                    end)
                elseif v.Character.Humanoid.Health <= 80 and v.Character.Humanoid.Health >= 61 then
                    pcall(function()
                    v.Character.HumanoidRootPart.BrickColor = BrickColor.new("New Yeller")
                    end)
                elseif v.Character.Humanoid.Health <= 60 and v.Character.Humanoid.Health >= 51 then
                    pcall(function()
                    v.Character.HumanoidRootPart.BrickColor = BrickColor.new("Bright orange")
                    end)
                elseif v.Character.Humanoid.Health <= 50 and v.Character.Humanoid.Health >= 28 then
                    pcall(function()
                    v.Character.HumanoidRootPart.BrickColor = BrickColor.new("Really red")
                    end)
                end
            end
        else
            v.Character.HumanoidRootPart.Size = Vector3.new(2,2,1)
            v.Character.HumanoidRootPart.Transparency = 1
        end
    else
        v.Character.HumanoidRootPart.Size = Vector3.new(2,2,1)
        v.Character.HumanoidRootPart.Transparency = 1
    end
end
end
end)
end
end
end)

if _G.Size == nil then
_G.Size = 15
end

Sector1:AddSlider("Select Size",0,_G.Size,100,1,function(x)
_G.Size = x
end)

Sector1:AddButton("Random Players",function()
    local Ran = math.random(2,#game:GetService("Players"):GetChildren())
    for i,v in pairs(game:GetService("Players"):GetChildren()) do
        if Ran == i then 
            _G.Select_Player = v.Name
        end
    end
end)

local Sector1 = Tab:CreateSector("Auto Click","left")

function Fire_ALL()
    for i,v in pairs(game:GetService("Workspace"):GetChildren()) do --game:GetService("Workspace").TempMap.Main.Lockers.Locker.Door.LockerPrompt
        if v.Name == "ATM" then
            pcall(function()
            fireproximityprompt(v.ProximityPrompt,1)
            end)
        elseif string.find(v.Name,"กูรู้นะ") then
            pcall(function()
            fireproximityprompt(v.ProximityPrompt,1)
            end)
        elseif string.find(v.Name,"MoneyD") then
            pcall(function()
            fireproximityprompt(v.ProximityPrompt,1)
            end)
        elseif string.find(v.Name,"Money") then
            pcall(function()
            fireproximityprompt(v.ProximityPrompt,1)
            end)
        elseif string.find(v.Name,"Coin") then
            pcall(function()
            fireproximityprompt(v.ProximityPrompt,1)
            end)
        elseif string.find(v.Name,"P2") then
            pcall(function()
            fireproximityprompt(v.ProximityPrompt,1)
            end)
        elseif v.Name == "Ammo Box Rifle" then
            pcall(function()
            fireproximityprompt(v.PromptAttachment.ProximityPrompt,1)
            end)
        elseif v.Name == "amogus" then
            pcall(function()
            fireproximityprompt(v.SafeDoor.ProximityPrompt,20)
            end)
        elseif v.Name == "Door Vault" then
            pcall(function()
            fireproximityprompt(v.Knob.ProximityPrompt,20)
            end)
        end
    end
end

Mouse = game.Players.LocalPlayer:GetMouse()
Mouse.KeyUp:Connect(function(KEY)
    if KEY:lower() == "q" then
        Fire_ALL()
    end
end)

Sector1:AddDropdown("Select Target For Click",{"ATM","Coin","Ammo","Garbage","Door Vault","Vault"},"Select",false,function(t)
    _G.Target = t
end)

Sector1:AddToggle("Auto Click",false,function(t)
_G.Auto_Click = t

spawn(function()
while wait(1) do
if _G.Auto_Click then
pcall(function()
    if _G.Target == "ATM" then -- ATM
        --
        for i,v in pairs(game:GetService("Workspace"):GetChildren()) do --game:GetService("Workspace").TempMap.Main.Lockers.Locker.Door.LockerPrompt
            if v.Name == "ATM" then
                pcall(function()
                fireproximityprompt(v.ProximityPrompt,1)
                end)
            end
        end
        --
    elseif _G.Target == "Coin" then -- Coin
        --
        for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
            if string.find(v.Name,"กูรู้นะ") then
                pcall(function()
                fireproximityprompt(v.ProximityPrompt,1)
                end)
            elseif string.find(v.Name,"MoneyD") then
                pcall(function()
                fireproximityprompt(v.ProximityPrompt,1)
                end)
            elseif string.find(v.Name,"Money") then
                pcall(function()
                fireproximityprompt(v.ProximityPrompt,1)
                end)
            elseif string.find(v.Name,"Coin") then
                pcall(function()
                fireproximityprompt(v.ProximityPrompt,1)
                end)
            end
        end
        --
    elseif _G.Target == "Ammo" then -- Ammo
        --
        for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
            if v.Name == "Ammo Box Rifle" then
                pcall(function()
                fireproximityprompt(v.PromptAttachment.ProximityPrompt,1)
                end)
            end
        end
        --
    elseif _G.Target == "Garbage" then -- Trash
        --
        for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
            if string.find(v.Name,"P2") then
                pcall(function()
                fireproximityprompt(v.ProximityPrompt,1)
                end)
            end
        end
        --
    elseif _G.Target == "Door Vault" then -- Door Vault
        --
        for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
            if v.Name == "Door Vault" then
                pcall(function()
                fireproximityprompt(v.Knob.ProximityPrompt,20)
                end)
            end
        end
        --
    elseif _G.Target == "Vault" then -- Vault
        --
        for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
            if v.Name == "amogus" then
                pcall(function()
                fireproximityprompt(v.SafeDoor.ProximityPrompt,20)
                end)
            end
        end
        --
    end
end)
end
end
end)
end)

Sector1:AddButton("Click",function()
    if _G.Target == "ATM" then -- ATM
        --
        for i,v in pairs(game:GetService("Workspace"):GetChildren()) do --game:GetService("Workspace").TempMap.Main.Lockers.Locker.Door.LockerPrompt
            if v.Name == "ATM" then
                pcall(function()
                fireproximityprompt(v.ProximityPrompt,1)
                end)
            end
        end
        --
    elseif _G.Target == "Coin" then -- Coin
        --
        for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
            if string.find(v.Name,"กูรู้นะ") then
                pcall(function()
                fireproximityprompt(v.ProximityPrompt,1)
                end)
            elseif string.find(v.Name,"MoneyD") then
                pcall(function()
                fireproximityprompt(v.ProximityPrompt,1)
                end)
            elseif string.find(v.Name,"Money") then
                pcall(function()
                fireproximityprompt(v.ProximityPrompt,1)
                end)
            elseif string.find(v.Name,"Coin") then
                pcall(function()
                fireproximityprompt(v.ProximityPrompt,1)
                end)
            end
        end
        --
    elseif _G.Target == "Ammo" then -- Ammo
        --
        for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
            if v.Name == "Ammo Box Rifle" then
                pcall(function()
                fireproximityprompt(v.PromptAttachment.ProximityPrompt,1)
                end)
            end
        end
        --
    elseif _G.Target == "Garbage" then -- Trash
        --
        for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
            if string.find(v.Name,"P2") then
                pcall(function()
                fireproximityprompt(v.ProximityPrompt,1)
                end)
            end
        end
        --
    elseif _G.Target == "Door Vault" then -- Door Vault
        --
        for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
            if v.Name == "Door Vault" then
                pcall(function()
                fireproximityprompt(v.Knob.ProximityPrompt,20)
                end)
            end
        end
        --
    elseif _G.Target == "Vault" then -- Vault
        --
        for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
            if v.Name == "amogus" then
                pcall(function()
                fireproximityprompt(v.SafeDoor.ProximityPrompt,20)
                end)
            end
        end
        --
    end
end)

function GOD()
local player = game.Players.LocalPlayer
if player.Character then
if player.Character:FindFirstChild("Humanoid") then
player.Character.Humanoid.Name = "1"
end
local l = player.Character["1"]:Clone()
l.Parent = player.Character
l.Name = "Humanoid"; wait(0.1)
player.Character["1"]:Destroy()
workspace.CurrentCamera.CameraSubject = player.Character.Humanoid
player.Character.Animate.Disabled = true; wait(0.1)
player.Character.Animate.Disabled = false
end
end

function respawn()
function TurnVisible()
		if IsInvis == false then return end
		invisFix:Disconnect()
		invisDied:Disconnect()
		CF = workspace.CurrentCamera.CFrame
		Character = Character
		local CF_1 = Player.Character.HumanoidRootPart.CFrame
		Character.HumanoidRootPart.CFrame = CF_1
		InvisibleCharacter:Destroy()
		Player.Character = Character
		Character.Parent = workspace
		IsInvis = false
		Player.Character.Animate.Disabled = true
		Player.Character.Animate.Disabled = false
		invisDied = Character:FindFirstChildOfClass'Humanoid'.Died:Connect(function()
			Respawn()
			invisDied:Disconnect()
		end)
		invisRunning = false
end
local plr = game.Players.LocalPlayer
	if invisRunning then TurnVisible() end
	local char = plr.Character
	if char:FindFirstChildOfClass("Humanoid") then char:FindFirstChildOfClass("Humanoid"):ChangeState(15) end
	char:ClearAllChildren()
	local newChar = Instance.new("Model")
	newChar.Parent = workspace
	plr.Character = newChar
	wait()
	plr.Character = char
	newChar:Destroy()
end

spawn(function()
        game:GetService("RunService").Heartbeat:Connect(function()
        if _G.Stand then
            if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Humanoid") then
                game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
            end
        end
    end)
end)

function uneq()
for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
if v:IsA "Tool" then 
    game.Players.LocalPlayer.Character[v.Name].Parent = game.Players.LocalPlayer.Backpack
end
end
end

function TPBring()
game.Players[_G.Select_Player].Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(1.5,0,-2)
end

spawn(function()
    while wait() do
        if _G.Bring then
            TPBring()
        end
    end
end)

spawn(function()
    while wait() do
        if _G.Bring then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = NormalCFrame
        end
    end
end)

local Sector1 = Tab:CreateSector("Character","right")

if _G.Walk == nil then
    _G.Walk = 16
end

Sector1:AddSlider("Select SPEED",12,_G.Walk,21,1,function(x)
_G.Walk = x
end)

Sector1:AddToggle("The Fast",true,function(t)
_G.Walkfast = t
end)

game:GetService("RunService").Stepped:Connect(function()
    if _G.Walkfast then
        pcall(function()
            game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = _G.Walk
        end)
    end
end)

Sector1:AddToggle("Destroy barrier",true,function(t)
_G.GOD = t
end)

game:GetService("RunService").Stepped:Connect(function()
    if _G.GOD then
        pcall(function()
            for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
                if v.Name == "TeamDoor" then
                    v:Destroy()
                end
            end
        end)
    end
end)

Sector1:AddToggle("Noclip",true,function(t)
_G.Noclip = t
end)

Sector1:AddToggle("Auto Save Item",true,function(t)
_G.Auto_Save_Item = t
end)

Sector1:AddToggle("Auto Load Item",true,function(t)
_G.Auto_Load_Item = t
end)

FirstTime = true

Sector1:AddToggle("Infinity Ammo [Press R]",true,function(t)
_G.Infinity_Ammo = t
end)

Sector1:AddToggle("Auto Glab Item",true,function(t)
_G.Auto_Glab_Item = t
end)

Sector1:AddToggle("GOD",false,function(t)
_G.GOG = t
_G.Fly = t
end)

AA = 3.2575
spawn(function()
    pcall(function()
        game:GetService("RunService").Heartbeat:Connect(function()
            if _G.GOG then
                Find_C = game.Players.LocalPlayer.Character:FindFirstChild("Click to TP")
                Find_B = game.Players.LocalPlayer.Backpack:FindFirstChild("Click to TP")
                if not Find_B then
                    if not Find_C then
                        mouse = game.Players.LocalPlayer:GetMouse()
                        tool = Instance.new("Tool")
                        tool.RequiresHandle = false
                        tool.Name = "Click to TP"
                        tool.Activated:connect(function()
                        local pos = mouse.Hit+Vector3.new(0,2.5,0)
                        pos = CFrame.new(pos.X,pos.Y,pos.Z)
                        TP(pos)
                        end)
                        tool.Parent = game.Players.LocalPlayer.Backpack
                    end
                end
            else
                if game:GetService("Workspace"):FindFirstChild("LOL") then
                    game:GetService("Workspace"):FindFirstChild("LOL"):Destroy()
                end
                if Find_C then
                    pcall(function()
                    game.Players.LocalPlayer.Character:FindFirstChild("Click to TP"):Destroy()
                    end)
                    else
                    if Find_B then
                        pcall(function()
                        game.Players.LocalPlayer.Backpack:FindFirstChild("Click to TP"):Destroy()
                        end)
                    end
                end
            end
        end)
    end)
 end)

game:GetService("RunService").Stepped:Connect(function()
    if _G.Auto_Glab_Item then
        pcall(function()
            for i,v in pairs(game:GetService("Workspace"):GetChildren()) do -- GetDescendants
                if v:IsA "Tool" then
                    v.Parent = game.Players.LocalPlayer.Backpack
                end
            end
        end)
    end
end)

spawn(function()
    while wait() do
        if _G.Auto_Save_Item then
            pcall(function()
local Find_Save = game.Players.LocalPlayer:FindFirstChild("Save")
local N = Instance.new("Folder")

if Find_Save then
    else
    N.Parent = game.Players.LocalPlayer
    N.Name = "Save"
end
-- Save
for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do -- GetDescendants
    local Find_Save_Item = game.Players.LocalPlayer.Save:FindFirstChild(v.Name)
    if Find_Save_Item then
    else
        if v.Name ~= "Click to TP" then
        game.Players.LocalPlayer.Backpack[v.Name]:Clone().Parent = game.Players.LocalPlayer.Save
        end
    end
end
wait(.5)
            end)
        end
    end
end)

spawn(function()
    while wait() do
        if _G.Auto_Load_Item then
            pcall(function()

-- Load          
for i,v in pairs (game.Players.LocalPlayer.Save:GetChildren()) do
    local Find_Back = game.Players.LocalPlayer.Backpack:FindFirstChild(v.Name)
    local Find_Chacarater = game.Players.LocalPlayer.Character:FindFirstChild(v.Name)
    if Find_Back then
    else
        if not Find_Chacarater then
        game.Players.LocalPlayer.Save[v.Name]:Clone().Parent = game.Players.LocalPlayer.Backpack
        end
    end
end
wait(.5)
            end)
        end
    end
end)

Sector1:AddButton("Save item",function()
for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do -- GetDescendants
    local Find_Save_Item = game.Players.LocalPlayer.Save:FindFirstChild(v.Name)
    if Find_Save_Item then
    else
        game.Players.LocalPlayer.Backpack[v.Name]:Clone().Parent = game.Players.LocalPlayer.Save
    end
end
end)

Sector1:AddButton("Load Save",function()
for i,v in pairs (game.Players.LocalPlayer.Save:GetChildren()) do
    local Find_Back = game.Players.LocalPlayer.Backpack:FindFirstChild(v.Name)
    local Find_Chacarater = game.Players.LocalPlayer.Character:FindFirstChild(v.Name)
    if Find_Back then
    else
        if not Find_Chacarater then
        game.Players.LocalPlayer.Save[v.Name]:Clone().Parent = game.Players.LocalPlayer.Backpack
        end
    end
end
end)

Sector1:AddButton("Clear Save",function()
for i,v in pairs (game.Players.LocalPlayer.Save:GetChildren()) do
    v:Destroy()
end
end)

Mouse = game.Players.LocalPlayer:GetMouse()
Mouse.KeyUp:Connect(function(KEY)
if _G.Infinity_Ammo then
    if KEY:lower() == "r" then
        for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do 
            if v:IsA "Tool" then 
                v:Destroy()
                repeat wait() until game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(v.Name)
                game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(v.Name))
            end
        end
    end
end
end)

function EquipTool(Trash)
game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(Trash))
end

Sector1:AddButton("Destroy item",function()
    for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do 
        if v:IsA "Tool" then 
            v:Destroy()
        end
    end
end)
