local WindUI = loadstring(game:HttpGet("https://tree-hub.vercel.app/api/UI/WindUI"))()

local Window = WindUI:CreateWindow({
    Title = "Zylo Hub", -- UI Title
    Author = "By Devs", -- Author & Creator
    Folder = "Zylo Hub", -- Folder name for saving data (And key)
    Size = UDim2.fromOffset(560, 820), -- UI Size
    KeySystem = { -- Creates key system
        Key = "mwj9x0lZQSMORPVe4ALctX", -- key
        Note = "Go to Linkvertise to get ur key", -- Note
        URL = "https://link-center.net/1227251/zylo-hub-key", -- URL To get key (example: Discord)
        SaveKey = true, -- Saves the key in the folder specified above
},
    Transparent = true,-- UI Transparency
    Theme = "Dark", -- UI Theme
    SideBarWidth = 200, -- UI Sidebar Width (number)
    HasOutline = false, -- Adds Oultines to the window
})

local MainTab = Window:Tab({
    Title = "Universal",
    Icon = "house",
})

Window:SelectTab(1)

local Divider = Window:Divider()

MainTab:Section({ 
    Title = "Walk and jump changer",
    TextXAlignment = "Left"
})

local Slider = MainTab:Slider({
    Title = "Walkspeed changer",
    Desc = "Changes speed up to 500",
    Step = 1,
    Value = {
        Min = 5,
        Max = 500,
        Default = 16,
    },
    Callback = function(value)
        game.Workspace[game.Players.LocalPlayer.Name].Humanoid.WalkSpeed = value
    end
})

local Slider = MainTab:Slider({
    Title = "JumpPower Changer",
    Desc = "Changes JumpPower up to 500",
    Step = 1,
    Value = {
        Min = 20,
        Max = 500,
        Default = 50,
    },
    Callback = function(value)
        game.Workspace[game.Players.LocalPlayer.Name].Humanoid.JumpPower = value
    end
})

MainTab:Section({ 
    Title = "Universal Scripts",
    TextXAlignment = "Right"
})

local Button = MainTab:Button({
    Title = "Inf Yield",
    Desc = "Opens Inf Yield",
    Callback = function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
        Dialog:Open()
    end,
})

local Button = MainTab:Button({
    Title = "Fps Booster",
    Desc = "Opens Fps Booster",
    Callback = function()
        loadstring(game:HttpGet("https://pastebin.com/raw/1j5J9c9i"))()
        Dialog:Open()
    end,
})

local Button = MainTab:Button({
    Title = "Brick Admin",
    Desc = "Opens Brick Admin",
    Callback = function()
        loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Brick-Admin-BETA-12105",true))()
        Dialog:Open()
    end,
})

local Button = MainTab:Button({
    Title = "Aimbot Script",
    Desc = "Opens Aimbot Script",
    Callback = function()
        loadstring(game:HttpGet("https://pastebin.com/raw/EMk8B3tC"))()
        Dialog:Open()
    end,
})

local Button = MainTab:Button({
    Title = "Esp Script",
    Desc = "Opens Esp Script",
    Callback = function()
        pcall(function() loadstring(game:HttpGet('https://raw.githubusercontent.com/ic3w0lf22/Unnamed-ESP/master/UnnamedESP.lua'))() end)
        Dialog:Open()
    end,
})

local MainTab = Window:Tab({
    Title = "Fisch",
    Icon = "fish",
})

local Divider = Window:Divider()

local WindowTab = Window:Tab({
    Title = "Window and File Configuration",
    Icon = "settings",
})

WindowTab:Section({ Title = "Keybinds" })

local KeybindClicked = false
local Keybind = WindowTab:Keybind({
    Title = "Keybind Toggle UI",
    Desc = "Keybind Toggle UI Desc",
    Value = "LeftShift",
    CanChange = true,
    Callback = function(k)
        if not KeybindClicked then
            Window:Close()
        else
            Window:Open()
        end
        KeybindClicked = not KeybindClicked
    end
})

