Name_GUI = "Duck HUB"
local Ui = game:GetService("CoreGui"):FindFirstChild(Name_GUI)
if Ui then
    Ui:Destroy()
end
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/naypramx/Ui__Project/Script/XeNonUi", true))()
local CenterHubNo1 = library:CreateWindow("Duck HUB 🙂 ",Enum.KeyCode.RightControl)
local Tab = CenterHubNo1:CreateTab("Auto Farm")

local Sector1 = Tab:CreateSector("Auto Farm","left")

function TP(P)
   local Distance = (P.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
   local Speed = 18
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

Sector1:AddTextbox("Select",false,function(t)
    Select_Player = GetPlayer(t)[1]
end)

Sector1:AddToggle("Auto Kill",false,function(t)
    Auto_Kill = t
    if Auto_Kill then
        _G.Noclip = true
    else
        _G.Noclip = false
    end
end)

Sector1:AddToggle("Auto Farm Money",false,function(t)
    Auto_Money = t
    if Auto_Money then
        _G.GGEZ = true
        _G.Noclip = true
    else
        _G.GGEZ = false
        _G.Noclip = false
        tween:Cancel()
    end
end)

Weapon = "Fist"

function Noclip()
for i, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
        if v:IsA("BasePart") and v.CanCollide == true then
            v.CanCollide = false -- Script ทะลุกำเเพง
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
if Auto_Kill then
pcall(function()
game.Players[Select_Player].Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,0,-2.5)
game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(Weapon))
game:GetService'VirtualUser':CaptureController()
game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
end)
end
end)

spawn(function()
while wait() do
if Auto_Money then
pcall(function()
Fire_ALL()
wait(.5)
end)
end
end
end)

spawn(function()
while wait() do
if Auto_Money then
pcall(function()
Auto_Money1 = true
wait(5)
Auto_Money1 = false
Auto_Money2 = true
wait(5)
Auto_Money1 = false
Auto_Money2 = false
Auto_Money3 = true
wait(5)
Auto_Money1 = false
Auto_Money2 = false
Auto_Money3 = false
Auto_Money4 = true
wait(5)
Auto_Money1 = false
Auto_Money2 = false
Auto_Money3 = false
Auto_Money4 = false
Auto_Money5 = true
wait(5)
Auto_Money1 = false
Auto_Money2 = false
Auto_Money3 = false
Auto_Money4 = false
Auto_Money5 = false
Auto_Money6 = true
wait(5)
Auto_Money1 = false
Auto_Money2 = false
Auto_Money3 = false
Auto_Money4 = false
Auto_Money5 = false
Auto_Money6 = false
Auto_Money7 = true
wait(5)
Auto_Money1 = false
Auto_Money2 = false
Auto_Money3 = false
Auto_Money4 = false
Auto_Money5 = false
Auto_Money6 = false
Auto_Money7 = false
Auto_Money8 = true
wait(5)
Auto_Money1 = false
Auto_Money2 = false
Auto_Money3 = false
Auto_Money4 = false
Auto_Money5 = false
Auto_Money6 = false
Auto_Money7 = false
Auto_Money8 = false
Auto_Money9 = true
end)
end
end
end)

spawn(function()
while wait() do
if Auto_Money then
pcall(function()
if Auto_Money1 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5.059920787811279, 6.042726516723633, 45.41558837890625) * CFrame.new(0,-7,0)
elseif Auto_Money2 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(185.20172119140625, 6.042726516723633, -8.63344955444336) * CFrame.new(0,-7,0)
elseif Auto_Money3 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(391.28363037109375, 6.042646408081055, -12.520451545715332) * CFrame.new(0,-7,0)
elseif Auto_Money4 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(248.52706909179688, 6.04032039642334, -274.5538024902344) * CFrame.new(0,-7,0)
elseif Auto_Money5 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(162.00059509277344, 6.0425333976745605, -209.9502716064453) * CFrame.new(0,-7,0)
elseif Auto_Money6 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(36.20331954956055, 6.042530059814453, -213.32644653320312) * CFrame.new(0,-7,0)
elseif Auto_Money7 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-127.67198181152344, 6.042724609375, -531.7274780273438) * CFrame.new(0,-7,0)
elseif Auto_Money8 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(166.43116760253906, 6.042726993560791, -573.3761596679688) * CFrame.new(0,-7,0)
elseif Auto_Money9 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(182.19052124023438, 6.042085647583008, -399.63323974609375) * CFrame.new(0,-7,0)
end
end)
end
end
end)

game:GetService("RunService").Stepped:Connect(function()
    if Auto_Kill then
    pcall(function()
        Noclip()
    end)
    end
end)

Sector1:AddToggle("Spectate",false,function(t)
    a1 = t
    if a1 then
    else
        workspace.CurrentCamera.CameraSubject = game:GetService("Players").LocalPlayer.Character.Humanoid
    end
end)

spawn(function()
while wait() do
if a1 then
pcall(function()
workspace.CurrentCamera.CameraSubject = game.Players[Select_Player].Character.Humanoid
end)
end
end
end)

Sector1:AddToggle("HITBOX",false,function(t)
    a2 = t
    if a2 then
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
while wait() do
if a2 then
pcall(function()
for i,v in next, game:GetService('Players'):GetPlayers() do
if v.Name ~= game:GetService('Players').LocalPlayer.Name then
    if v.Team ~= game:GetService('Players').LocalPlayer.Team then
        if v.Character.Humanoid.Health <= 0 then
            v.Character.HumanoidRootPart.Size = Vector3.new(2,2,1)
            v.Character.HumanoidRootPart.Transparency = 1
        else
            pcall(function()
            v.Character.HumanoidRootPart.Size = Vector3.new(Size,Size,Size)
            v.Character.HumanoidRootPart.Transparency = 0.7
            v.Character.HumanoidRootPart.BrickColor = BrickColor.new("Really white")
            v.Character.HumanoidRootPart.Material = "Neon"
            v.Character.HumanoidRootPart.CanCollide = false
            end)
        end
    end
end
end
end)
end
end
end)

Sector1:AddSlider("Select Size",0,50,100,1,function(x)
Size = x
end)

Sector1:AddButton("Random Players",function()
    local Ran = math.random(2,#game:GetService("Players"):GetChildren())
    for i,v in pairs(game:GetService("Players"):GetChildren()) do
        if Ran == i then 
            Select_Player = v.Name
        end
    end
end)

local Sector1 = Tab:CreateSector("SECTOR CENTERHUB","left")

Sector1:AddDropdown("Select Target",{"ATM","Coin","Ammo","ALL"},"Select",false,function(t)

end)

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
        end
    end
end

function Fire_ATM()
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do --game:GetService("Workspace").TempMap.Main.Lockers.Locker.Door.LockerPrompt
    if v.Name == "ATM" then
        pcall(function()
        fireproximityprompt(v.ProximityPrompt,1)
        end)
    end
end
end

function Fire_Coin()
    for i,v in pairs(game:GetService("Workspace"):GetChildren()) do -- GetDescendants
        if string.find(v.Name,"กูรู้นะ") then
            pcall(function()
            fireproximityprompt(v.ProximityPrompt,1)
            end)
        end
        if string.find(v.Name,"MoneyD") then
            pcall(function()
            fireproximityprompt(v.ProximityPrompt,1)
            end)
        end
    end
end

function Fire_CoinD()
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do -- GetDescendants
    if string.find(v.Name,"MoneyD") then
        pcall(function()
        fireproximityprompt(v.ProximityPrompt,1)
        end)
    end
end
end

function Fire_Money()
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do -- GetDescendants
    if string.find(v.Name,"Money") then
        pcall(function()
        fireproximityprompt(v.ProximityPrompt,1)
        end)
    end
end
end

function Fire_CoinD()
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do -- GetDescendants
    if string.find(v.Name,"MoneyD") then
        pcall(function()
        fireproximityprompt(v.ProximityPrompt,1)
        end)
    end
end
end

function Fire_CoinS()
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do -- GetDescendants
    if string.find(v.Name,"Coin") then
        pcall(function()
        fireproximityprompt(v.ProximityPrompt,1)
        end)
    end
end
end

function Fire_Bag()
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do -- GetDescendants
    if string.find(v.Name,"P2") then
        pcall(function()
        fireproximityprompt(v.ProximityPrompt,1)
        end)
    end
end
end

function Fire_Ammo()
    for i,v in pairs(game:GetService("Workspace"):GetChildren()) do -- GetDescendants
        if v.Name == "Ammo Box Rifle" then
            pcall(function()
            fireproximityprompt(v.PromptAttachment.ProximityPrompt,1)
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

Sector1:AddToggle("TOGGLE BY CENTERHUB",false,function(t)
    print(t)
end)

Sector1:AddButton("TesT",function()
game.Players[Select_Player].Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,0,-1)
end)

Sector1:AddButton("GOD",function()
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
end)

local Sector1 = Tab:CreateSector("Character","right")

Sector1:AddSlider("Select SPEED",12,0,21,1,function(x)
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
end)
