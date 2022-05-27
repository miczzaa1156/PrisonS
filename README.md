local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/GreenDeno/Venyx-UI-Library/main/source.lua"))()
local venyx = library.new("PEPLE | Prison Only", 5013109572)
 
 
local page = venyx:addPage("main", 5012544693)
local section1 = page:addSection("section1")
local section2 = page:addSection("Section 2")
local theme = venyx:addPage("Theme", 5012544693)
local colors = theme:addSection("Colors")
 
 
section1:addButton("M4A1", function()
    game.Workspace.Prison_ITEMS.giver["M4A1"].ITEMPICKUP.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
end)
section1:addButton("AK-47", function()
    game.Workspace.Prison_ITEMS.giver["AK-47"].ITEMPICKUP.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
end)
section1:addButton("M9", function()
    game.Workspace.Prison_ITEMS.giver["M9"].ITEMPICKUP.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
end)
section1:addButton("Remington 870", function()
    game.Workspace.Prison_ITEMS.giver["Remington 870"].ITEMPICKUP.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
end)
section1:addButton("Riot Shield", function()
    game.Workspace.Prison_ITEMS.giver["Riot Shield"].ITEMPICKUP.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
end)
section1:addButton("nil", function()
    game.Workspace.Prison_ITEMS.giver["nil"].ITEMPICKUP.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
end)
section1:addButton("Crude Knife", function()
    game.Workspace.Prison_ITEMS.single["Crude Knife"].ITEMPICKUP.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
end)
section1:addButton("Hammer", function()
    game.Workspace.Prison_ITEMS.single["Hammer"].ITEMPICKUP.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
end)
section1:addButton("Knife M9", function()
    game.Workspace.Prison_ITEMS.single["M9"].ITEMPICKUP.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
end)
section2:addButton("Car Spawner1", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-191.606247, 51.6749382, 1880.09424, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)
section2:addButton("Car Spawner2", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-525.94751, 51.6751022, 1774.19812, 0.782586694, 0, 0.622541666, 0, 1, 0, -0.622541666, 0, 0.782586694)
end)
section2:addButton("WalkSpeed", function()
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 100
end)
section2:addButton("Jumpower", function(value)
    loadstring(game:HttpGet(('https://raw.githubusercontent.com/miczzaa1156/Jum/main/README.md'),true))()
end)

section2:addButton("ESP", function(value)
    loadstring(game:HttpGet("https://raw.githubusercontent.com/miczzaa1156/ESP/main/README.md"))();
end)
section2:addButton("infiniteYield FE v5.5", function(value)
    loadstring(game:HttpGet(('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'),true))()
end)    

section2:addKeybind("Toggle Keybind", Enum.KeyCode.One, function()
print("Activated Keybind")
venyx:toggle()
end, function()
print("Changed Keybind")
end) 
 
local themes = {
Background = Color3.fromRGB(24, 24, 24),
Glow = Color3.fromRGB(0, 0, 0),
Accent = Color3.fromRGB(10, 10, 10),
LightContrast = Color3.fromRGB(20, 20, 20),
DarkContrast = Color3.fromRGB(14, 14, 14),  
TextColor = Color3.fromRGB(255, 255, 255)
}
 
 
for theme, color in pairs(themes) do -- all in one theme changer, i know, im cool
colors:addColorPicker(theme, color, function(color3)
venyx:setTheme(theme, color3)
end)
end
 
-- load
venyx:SelectPage(venyx.pages[1], true)
 
 
 
 
 
spawn(function()
   game:GetService("RunService").RenderStepped:Connect(function()
    pcall(function()
        if _G.FastAttack then
            local Combat = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework)
            local Cemara = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework.CameraShaker)
            Cemara.CameraShakeInstance.CameraShakeState = {FadingIn = 3, FadingOut = 2, Sustained = 0, Inactive = 1}
            Combat.activeController.timeToNextAttack = 0
            Combat.activeController.hitboxMagnitude = 120
            Combat.activeController.increment = 3
        end
    end)
end) 
end)
 
 
spawn(function()
   game:GetService("RunService").RenderStepped:Connect(function()
    pcall(function()
        if _G.FastAttack then
            game:GetService'VirtualUser':CaptureController()
            game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
        end
    end)
end) 
end)
