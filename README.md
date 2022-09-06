local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("KaiYang Hub", "DarkTheme")
local Tab = Window:NewTab("Main")
local Section = Tab:NewSection("Auto Play")
Section:NewButton("Auto Rebirth", "ButtonInfo", function()
while true do
    wait()
local args = {
    [1] = 500
}

game:GetService("ReplicatedStorage").Events.Rebirth:FireServer(unpack(args))
end
end)
Section:NewButton("Auto click", "ButtonInfo", function()
while true do
    wait()
game:GetService("ReplicatedStorage").Events.Tap:FireServer()
end
end)
