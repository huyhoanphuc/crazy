-- Achievement
local Achievements = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors/Custom%20Achievements/Source.lua"))()

-- Creates and displays your custom achievement
Achievements.Get({
    Title = "CRAZY mode",
    Desc = "",
    Reason = 'V1',
    Image = "https://github.com/ha2ke3oer/VPNWORK/blob/main/static-assets-upload8893301385814255192.png?raw=true",
})

--[=[
@class txt
This is my First Class
--]=]

print(os.date("%B"))

print("Loading")
-----------------------------------------------------------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------------------------------------------------------

local HardCore = {
    Title = "The Pain Just Begain", -- Made by MuhammadGames and Volta
    Desc = "Join a Match of HardCore For the First Time.",
    Reason = "You executed the HardCore script.",
    Image = "https://github.com/MuhXd/Models/blob/main/HardCoreDoors.png?raw=true",
    id = 1,
}

local DepthW = {
    Title = "Finally Free",
    Desc = "Encounter Depth",
    Reason = "Survive Depth",
    Image = "https://github.com/MuhXd/DoorSuff/blob/main/DoorsModes/Png.png?raw=true",
    id = 2,
}

local Depth = {
    Title = "The Entity Is Still Freezing",
    Desc = "It's So Cold",
    Reason = "Dont Survive Depth",
    Image = "https://github.com/MuhXd/DoorSuff/blob/main/DoorsModes/Png.png?raw=true",
    id = 3,
}

local Smiles = {
    Title = "Income The Frowners",
    Desc = "Stop Smiling",
    Reason = "Encounter and Survive Smiler",
    Image = "https://tr.rbxcdn.com/533cbe35b1cf3d4e5d4f99278978563f/150/150/Image/Png",
    id = 4,
}

local SmilesDie = {
    Title = "Smile to Fail",
    Desc = "Don't Smile",
    Reason = "Encounter And Dont Survive Smiler",
    Image = "https://tr.rbxcdn.com/533cbe35b1cf3d4e5d4f99278978563f/150/150/Image/Png",
    id = 5,
}

local NightmareRush ={
    Title = "Rush From Your Nightmares",
    Desc = "Don't Be fooled",
    Reason = "Encounter And Survive Nightmare Rush",
    Image = "https://tr.rbxcdn.com/533cbe35b1cf3d4e5d4f99278978563f/150/150/Image/Png",
    id = 6,
}

local NightmareAmbush ={
    Title = "Ambush But Even Harder",
    Desc = "Don't Be fooled",
    Reason = "Encounter And Survive Nightmare Ambush",
    Image = "https://tr.rbxcdn.com/533cbe35b1cf3d4e5d4f99278978563f/150/150/Image/Png",
    id = 7,
}

local NightmareAmbush ={
    Title = "Ambush But Even Harder",
    Desc = "Don't Be fooled",
    Reason = "Encounter And Survive Nightmare Ambush",
    Image = "https://tr.rbxcdn.com/533cbe35b1cf3d4e5d4f99278978563f/150/150/Image/Png",
    id = 8,
}


-----------------------------------------------------------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------------------------------------------------------






-- loadstring(game:HttpGet("https://raw.githubusercontent.com/MuhXd/DoorSuff/main/Whitelist/NewKeySystem.lua"))()



caa = 0
tween = game:GetService("TweenService")
local TestMultplayer = true
if game:GetService("ReplicatedStorage"):FindFirstChild("crazym") then
    warn("You have Already Loaded")

    return true
end
local Test = Instance.new("Part")
Test.Name = "crazym"
Test.Parent = game:GetService("ReplicatedStorage")
Test = 1

local SelfModules = {
    Functions = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Functions.lua"))(),
}






------------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------------







local ModName = "HardCore"
local foldername = "AchievementsSaves   By Muhammadgames,Helped by RegularVynixu"
local Slipt = string.split(foldername,"|")
local valid2 = isfolder(foldername)
if not valid2 then
    makefolder(foldername)
end

local fileName = ModName.."Save's.txt"
local filePath = foldername.. "/".. fileName
local valid = isfile(filePath)

local Achievements = loadstring(game:HttpGet("https://raw.githubusercontent.com/MuhXd/Models/main/RegularVynixu's%20Achievement%20Modifyer"))()

function AchievementsGet(Achievement)
    local read = readfile(filePath)  
    local read2 = tostring(read)
    local read2 = string.split(read,"|")
    FOUND = true
    Find = ""
    for i,v in pairs(Achievement) do
        if i == "id" then
            Find=Find.." "..v
        end
    end

    for i,v in pairs(read2) do
        if v == Find then
            FOUND = true
        end
    end -- Desc
    if FOUND == false then
        Achievements.Get(Achievement)
        Write = ""
        for i,v in pairs(Achievement) do
            if i == "id" then
                Write=Write.." "..v
            end
        end
        appendfile(filePath,Write.."|")
    end
end
-- Creates and displays your custom achievement
-- readfile(<string> path)  
if not valid then
    writefile(filePath, "Helped by RegularVynixu|")
end

AchievementsGet(HardCore)
--[[
------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------ 
Start of real Code!
DON'T SHOW ABOVE!
.............     .       .
.     .     .     .       . 
.     .     .     .       .
.     .     .     .       . 
.     .     .     .       . 
.     .     .     .       . 
.     .     .     .       .
.     .     .     .........
--]]












if game:GetService("ReplicatedStorage"):FindFirstChild("Guis") then

else
    Visable = Instance.new("Folder")
    Visable.Name = "Guis"
    Visable.Parent = game.ReplicatedStorage

end
function Gui(Name,Amount1,TextSent)
    if game:GetService("Players").localPlayer.PlayerGui.MainUI.Statistics.Frame:FindFirstChild("!"..Name.."!") then
        game:GetService("Players").localPlayer.PlayerGui.MainUI.Statistics.Frame["!"..Name.."!"]:Destroy()
    end

    Visable = Instance.new("BoolValue")
    Visable.Value = true
    Visable.Name = Name
    Visable.Parent = game.ReplicatedStorage.Guis

    game.Players.localPlayer.PlayerGui.MainUI.Statistics.LocksOpened.Visible = true
    LocksOpened = game.Players.localPlayer.PlayerGui.MainUI.Statistics.LocksOpened:Clone()
    game.Players.localPlayer.PlayerGui.MainUI.Statistics.LocksOpened.Visible = false
    LocksOpened.Parent = game.Players.localPlayer.PlayerGui.MainUI.Statistics.Frame

    LocksOpened.Visible = game.ReplicatedStorage.Guis:FindFirstChild(Name).Value

    local Grad = game.Players.localPlayer.PlayerGui.MainUI.Statistics.Frame["Leftover Gold"].UICorner:Clone()
    Grad.Parent = LocksOpened
    Grad = game.Players.localPlayer.PlayerGui.MainUI.Statistics.Frame["Leftover Gold"].UIGradient:Clone()
    Grad.Parent = LocksOpened
    Grad = game.Players.localPlayer.PlayerGui.MainUI.Statistics.Frame["Leftover Gold"].Amount:Clone()
    Grad.Parent = LocksOpened
    Grad.Text = Amount1
    Grad.Position = Grad.Position - UDim2.new(0.035,0,0,0)
    Grad = game.Players.localPlayer.PlayerGui.MainUI.Statistics.Frame["Leftover Gold"].Icon:Clone()
    Grad.Parent = LocksOpened
    Grad.Position = Grad.Position - UDim2.new(0.035,0,0,0)

    LocksOpened.CloseButton.Position = LocksOpened.CloseButton.Position - UDim2.new(0.021,0,0,0)
    LocksOpened.CloseButton.ImageColor3 =  Color3.new(0.0313725, 0.854902, 1)
    LocksOpened.TextColor3 = Color3.new(0.0313725, 0.854902, 1)
    LocksOpened.TextScaled = false
    LocksOpened.Name = "!"..Name.."!"
    LocksOpened.TextSize = game.Players.localPlayer.PlayerGui.MainUI.Statistics.Frame["Leftover Gold"].TextSize + 16
    LocksOpened.Size = LocksOpened.Parent["Leftover Gold"].Size
    LocksOpened.BackgroundColor3 = Color3.new(0.0196078, 0.552941, 0.647059)
    LocksOpened.BackgroundTransparency = 0.5

    LocksOpened.Text = TextSent



    game.ReplicatedStorage.Guis:FindFirstChild(Name).changed:connect(function()

        LocksOpened.Visible = game.ReplicatedStorage.Guis:FindFirstChild(Name).Value
    end)
end







local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()


-- Run the created entity
local Message = function(Message,Enable,N)
    local msg = Instance.new("Message")  
    msg.Parent = game.Workspace     
    msg.Text = Message
    if Enable ~= true then
        task.wait(0.1)
        msg:Destroy()
    end
end

-- Message("Thank you For Loading MultplayerBeta 1.2")

for ii,vv in pairs(game:GetService("Players"):GetChildren()) do
    PlayersIngame = ii
end -- Gets All Players
if TestMultplayer == true then
    PlayersIngame = 10 -- TestMultplayer
end

if PlayersIngame > 1 then -- if more then one then waits for link
    if game:GetService("ReplicatedStorage").GameData.LatestRoom.Value > 0 then
        print("Loaded After door 1! Please wait for everyone to die")
        game.StarterGui:SetCore("ChatMakeSystemMessage", {
            Text = "Load Before Door 1",
            Color = Color3.fromRGB(255, 0, 0),
            Font = Enum.Font.SourceSansBold,
            TextSize = 18,
        })

        firesignal(game.ReplicatedStorage.Bricks.DeathHint.OnClientEvent, {"You didn't Load it Before Door 1!","Please Wait for the next round"})
        game.ReplicatedStorage.GameStats["Player_".. game.Players.LocalPlayer.Name].Total.DeathCause.Value = "Not Loading Before Door 1"
        game.Players.LocalPlayer.Character.Humanoid.Health = -100
        return false
    end


    game.StarterGui:SetCore("ChatMakeSystemMessage", {
        Text = "interminable rooms ON! By PrIme A-60 (a600399)",
        Color = Color3.fromRGB(255, 0, 0),
        Font = Enum.Font.SourceSansBold,
        TextSize = 18,
    })

    Gui("interminable rooms","+1000","interminable rooms (Doesn't add Nobs)")

    print("Loaded, Wating to Link to Multplayer") -- waiting to link

game:GetService("ReplicatedStorage").GameData.LatestRoom.Changed:Connect(function(v)
    L = game:GetService("Workspace").CurrentRooms[v].PathfindNodes:Clone()
    L.Parent = game:GetService("Workspace").CurrentRooms[v]
    L.Name = 'PathfindNodes'
end)
    
    c=1

    repeat task.wait()

        if c < 10 then
            -- Message("MultplayerV1.2B",true,"Welcome")
            c=10
        end
        --  msg:Destroy()
        --Kill=true
    until game:GetService("ReplicatedStorage").GameData.LatestRoom.Value > 0
    print("Linked to Clients") -- linked
    
    game.StarterGui:SetCore("ChatMakeSystemMessage", {
        Text = "Linked To Clients",
        Color = Color3.fromRGB(0, 255, 0),
        Font = Enum.Font.SourceSansBold,
        TextSize = 18,
    })



    Singleplayer = false -- Runs more Then 1 Player Code
else
    print("Loaded in print Multiplayer") -- loaded in 1 player
    repeat task.wait()

    until game:GetService("ReplicatedStorage").GameData.LatestRoom.Value > 0
    print("Started")
    Singleplayer = true -- Runs One player Code
end
Testa = 10
getgenv().death = false
Be=false
Many=1
JobId = game:GetService("ReplicatedStorage").GameData.GameStarted.Value
Lowest = string.len(game:GetService("ReplicatedStorage").GameData.GameStarted.Value)
Lowest = tonumber(Lowest)
Stop=Lowest
RanWait2=""
function Aten()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(40)
        wait(50)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 50 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(30)
            end
        local entity = Creator.createEntity({
            CustomName = "Silence", -- Custom name of your entity
            Model = "12479950685", -- Can be GitHub file or rbxassetid
            Speed = 100, -- Percentage, 100 = default Rush speed
            DelayTime = 2,
            KillRange= 100,-- Time before starting cycles (seconds)
            HeightOffset = 1,
            CanKill = true,
            BreakLights = true,
            BackwardsMovement = false,
            FlickerLights = {
                false, -- Enabled
                1, -- Time (seconds)
            },
            Cycles = {
                Min = 1,
                Max = 1,
                WaitTime = 2,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                false, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "nil", -- Image1 url
                    Image2 = "nil", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        0, -- SoundId
                        { Volume = 0 }, -- Sound properties
                    },
                    Sound2 = {
                        5263560566, -- SoundId
                        { Volume = 0 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(50, 115, 108), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 1,
                        Max = 5,
                    },
                },
            },
            CustomDialog = {"You died to A-10"}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0
    function Atin()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(260)
        wait(270)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 50 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(250)
            end
        local entity = Creator.createEntity({
            CustomName = "A 60", -- Custom name of your entity
            Model = "15089669896", -- Can be GitHub file or rbxassetid
            Speed = 100, -- Percentage, 100 = default Rush speed
            DelayTime = 2,
            KillRange= 10000,-- Time before starting cycles (seconds)
            HeightOffset = 1,
            CanKill = true,
            BreakLights = true,
            BackwardsMovement = false,
            FlickerLights = {
                false, -- Enabled
                1, -- Time (seconds)
            },
            Cycles = {
                Min = 4,
                Max = 4,
                WaitTime = 2,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                false, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "rbxassetid://11867753039", -- Image1 url
                    Image2 = "rbxassetid://11826898817", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        5263560566, -- SoundId
                        { Volume = 5 }, -- Sound properties
                    },
                    Sound2 = {
                        5263560566, -- SoundId
                        { Volume = 5 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(50, 115, 108), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 1,
                        Max = 5,
                    },
                },
            },
            CustomDialog = {"You died to A-60"}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0
    function Atyn()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(110)
        wait(120)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 50 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(100)
            end
        local entity = Creator.createEntity({
            CustomName = "A-35", -- Custom name of your entity
            Model = "12753725917", -- Can be GitHub file or rbxassetid
            Speed = 100, -- Percentage, 100 = default Rush speed
            DelayTime = 2,
            KillRange= 100,-- Time before starting cycles (seconds)
            HeightOffset = 1,
            CanKill = true,
            BreakLights = false,
            BackwardsMovement = false,
            FlickerLights = {
                false, -- Enabled
                1, -- Time (seconds)
            },
            Cycles = {
                Min = 2,
                Max = 2,
                WaitTime = 300,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                false, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "https://tr.rbxcdn.com/f0f798ca806ed372984f3b70d1b1432f/420/420/Image/Png", -- Image1 url
                    Image2 = "https://tr.rbxcdn.com/f0f798ca806ed372984f3b70d1b1432f/420/420/Image/Png", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        0, -- SoundId
                        { Volume = 0.5 }, -- Sound properties
                    },
                    Sound2 = {
                        5263560566, -- SoundId
                        { Volume = 0.5 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(50, 115, 108), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 1,
                        Max = 5,
                    },
                },
            },
            CustomDialog = {"You died to A-35"}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0
    function Athn()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(210)
        wait(220)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 50 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(200)
            end
        local entity = Creator.createEntity({
            CustomName = "A-60", -- Custom name of your entity
            Model = "11463891411", -- Can be GitHub file or rbxassetid
            Speed = 1000, -- Percentage, 100 = default Rush speed
            DelayTime = 10,
            KillRange= 10000,-- Time before starting cycles (seconds)
            HeightOffset = 1,
            CanKill = true,
            BreakLights = true,
            BackwardsMovement = false,
            FlickerLights = {
                true, -- Enabled
                5, -- Time (seconds)
            },
            Cycles = {
                Min = 1,
                Max = 1,
                WaitTime = 2,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                true, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "https://create.roblox.com/marketplace/asset/14091415779/Chamber60-Spritesheet-Chamber-Rooms?keyword=A-60+rooms&pageNumber=1&pagePosition=", -- Image1 url
                    Image2 = "11867753039", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        6459610652, -- SoundId
                        { Volume = 0.5 }, -- Sound properties
                    },
                    Sound2 = {
                        6459610652, -- SoundId
                        { Volume = 0.5 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(255, 255, 255), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 1,
                        Max = 5,
                    },
                },
            },
            CustomDialog = {"You died to A-60"}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0
    function Atkn()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(340)
        wait(350)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 50 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(330)
            end
        local entity = Creator.createEntity({
            CustomName = "A-200", -- Custom name of your entity
            Model = "12618961267", -- Can be GitHub file or rbxassetid
            Speed = 800, -- Percentage, 100 = default Rush speed
            DelayTime = 5,
            KillRange= 20,-- Time before starting cycles (seconds)
            HeightOffset = 1,
            CanKill = true,
            BreakLights = true,
            BackwardsMovement = true,
            FlickerLights = {
                false, -- Enabled
                5, -- Time (seconds)
            },
            Cycles = {
                Min = 1,
                Max = 2,
                WaitTime = 2,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                false, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "https://create.roblox.com/marketplace/asset/14091415779/Chamber60-Spritesheet-Chamber-Rooms?keyword=A-60+rooms&pageNumber=1&pagePosition=", -- Image1 url
                    Image2 = "11867753039", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        6459610652, -- SoundId
                        { Volume = 0.5 }, -- Sound properties
                    },
                    Sound2 = {
                        6459610652, -- SoundId
                        { Volume = 0.5 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(255, 255, 255), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 1,
                        Max = 5,
                    },
                },
            },
            CustomDialog = {"You died to A-200"}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0
    function Atwn()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(390)
        wait(400)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 50 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(380)
            end
        local entity = Creator.createEntity({
            CustomName = "A-221", -- Custom name of your entity
            Model = "12169085547", -- Can be GitHub file or rbxassetid
            Speed = 300000, -- Percentage, 100 = default Rush speed
            DelayTime = 10,
            KillRange= 20000,-- Time before starting cycles (seconds)
            HeightOffset = 2,
            CanKill = true,
            BreakLights = false,
            BackwardsMovement = false,
            FlickerLights = {
                false, -- Enabled
                5, -- Time (seconds)
            },
            Cycles = {
                Min = 12,
                Max = 15 ,
                WaitTime = 0,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                false, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "https://create.roblox.com/marketplace/asset/14091415779/Chamber60-Spritesheet-Chamber-Rooms?keyword=A-60+rooms&pageNumber=1&pagePosition=", -- Image1 url
                    Image2 = "11867753039", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        6459610652, -- SoundId
                        { Volume = 0.5 }, -- Sound properties
                    },
                    Sound2 = {
                        6459610652, -- SoundId
                        { Volume = 0.5 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(255, 255, 255), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 1,
                        Max = 5,
                    },
                },
            },
            CustomDialog = {"You died to A-221"}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0
    function Atrrn()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(440)
        wait(450)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 50 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(430)
            end
        local entity = Creator.createEntity({
            CustomName = "A 120", -- Custom name of your entity
            Model = "https://github.com/tonyBflako/vynixusdoors/blob/main/A120edit.rbxm?raw=true", -- Can be GitHub file or rbxassetid
            Speed = 1000, -- Percentage, 100 = default Rush speed
            DelayTime = 5,
            KillRange= 100,-- Time before starting cycles (seconds)
            HeightOffset = 1,
            CanKill = true,
            BreakLights = true,
            BackwardsMovement = true,
            FlickerLights = {
                false, -- Enabled
                5, -- Time (seconds)
            },
            Cycles = {
                Min = 1,
                Max = 3,
                WaitTime = 2,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                false, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "nil", -- Image1 url
                    Image2 = "nil", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        6459610652, -- SoundId
                        { Volume = 0 }, -- Sound properties
                    },
                    Sound2 = {
                        6459610652, -- SoundId
                        { Volume = 0 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(255, 255, 255), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 1,
                        Max = 5,
                    },
                },
            },
            CustomDialog = {"You died to A-120"}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0
    function lol()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(440)
        wait(450)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 50 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(430)
            end
        local entity = Creator.createEntity({
            CustomName = "Ripper", -- Custom name of your entity
            Model = "12262768551", -- Can be GitHub file or rbxassetid
            Speed = 1000, -- Percentage, 100 = default Rush speed
            DelayTime = 8,
            KillRange= 100,-- Time before starting cycles (seconds)
            HeightOffset = 9,
            CanKill = true,
            BreakLights = false,
            BackwardsMovement = false,
            FlickerLights = {
                false, -- Enabled
                5, -- Time (seconds)
            },
            Cycles = {
                Min = 1,
                Max = 1,
                WaitTime = 2,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                false, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "nil", -- Image1 url
                    Image2 = "nil", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        6459610652, -- SoundId
                        { Volume = 0 }, -- Sound properties
                    },
                    Sound2 = {
                        6459610652, -- SoundId
                        { Volume = 0 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(255, 255, 255), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 1,
                        Max = 5,
                    },
                },
            },
            CustomDialog = {"You died to Ripper"}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0
    function Brrl()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(440)
        wait(450)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 50 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(430)
            end
        local entity = Creator.createEntity({
            CustomName = "Pr!me (a-60)", -- Custom name of your entity
            Model = "rbxassetid://11801716344", -- Can be GitHub file or rbxassetid
            Speed = 100000, -- Percentage, 100 = default Rush speed
            DelayTime = 5,
            KillRange= 10000,-- Time before starting cycles (seconds)
            HeightOffset = 4,
            CanKill = true,
            BreakLights = true,
            BackwardsMovement = false,
            FlickerLights = {
                false, -- Enabled
                5, -- Time (seconds)
            },
            Cycles = {
                Min = 1,
                Max = 1,
                WaitTime = 2,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                false, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "nil", -- Image1 url
                    Image2 = "nil", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        6459610652, -- SoundId
                        { Volume = 0 }, -- Sound properties
                    },
                    Sound2 = {
                        6459610652, -- SoundId
                        { Volume = 0 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(255, 255, 255), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 1,
                        Max = 5,
                    },
                },
            },
            CustomDialog = {"You died to Pr!me a 60"}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0
    function Asix()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(440)
        wait(450)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 50 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(430)
            end
        local entity = Creator.createEntity({
            CustomName = "A 60", -- Custom name of your entity
            Model = "11393625763", -- Can be GitHub file or rbxassetid
            Speed = 10000, -- Percentage, 100 = default Rush speed
            DelayTime = 0,
            KillRange= 100,-- Time before starting cycles (seconds)
            HeightOffset = -1,
            CanKill = true,
            BreakLights = true,
            BackwardsMovement = true,
            FlickerLights = {
                false, -- Enabled
                5, -- Time (seconds)
            },
            Cycles = {
                Min = 1,
                Max = 1,
                WaitTime = 2,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                false, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "nil", -- Image1 url
                    Image2 = "nil", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        6459610652, -- SoundId
                        { Volume = 0 }, -- Sound properties
                    },
                    Sound2 = {
                        6459610652, -- SoundId
                        { Volume = 0 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(255, 255, 255), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 1,
                        Max = 5,
                    },
                },
            },
            CustomDialog = {"You died to A-60"}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0
    function Haha()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(440)
        wait(450)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 50 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(430)
            end
        local entity = Creator.createEntity({
            CustomName = "A 60", -- Custom name of your entity
            Model = "https://github.com/tonyBflako/vynixusdoors/blob/main/A60edit.rbxm?raw=true", -- Can be GitHub file or rbxassetid
            Speed = 600, -- Percentage, 100 = default Rush speed
            DelayTime = 5,
            KillRange= 100,-- Time before starting cycles (seconds)
            HeightOffset = 1,
            CanKill = true,
            BreakLights = true,
            BackwardsMovement = true,
            FlickerLights = {
                false, -- Enabled
                5, -- Time (seconds)
            },
            Cycles = {
                Min = 1,
                Max = 1,
                WaitTime = 2,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                false, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "nil", -- Image1 url
                    Image2 = "nil", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        6459610652, -- SoundId
                        { Volume = 0 }, -- Sound properties
                    },
                    Sound2 = {
                        6459610652, -- SoundId
                        { Volume = 0 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(255, 255, 255), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 1,
                        Max = 5,
                    },
                },
            },
            CustomDialog = {"You died to A-60"}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0
    function Ah()
    while true do task.wait()
    pcall(function()
        Be=true

        wait(440)
        wait(450)
        local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

        -- Create entity
        if  game.ReplicatedStorage.GameData.LatestRoom.Value ~= 50 then
        game.ReplicatedStorage.GameData.LatestRoom.Changed:Wait()
        else
            Wait(430)
            end
        local entity = Creator.createEntity({
            CustomName = "Ah 60", -- Custom name of your entity
            Model = "https://github.com/Johnny39871/assets/blob/main/A-60%20refined.rbxm?raw=true", -- Can be GitHub file or rbxassetid
            Speed = 100000, -- Percentage, 100 = default Rush speed
            DelayTime = 0,
            KillRange= 100000,-- Time before starting cycles (seconds)
            HeightOffset = 4,
            CanKill = true,
            BreakLights = true,
            BackwardsMovement = true,
            FlickerLights = {
                false, -- Enabled
                5, -- Time (seconds)
            },
            Cycles = {
                Min = 100,
                Max = 300,
                WaitTime = 0,
            },
            CamShake = {
                true, -- Enabled
                {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
                100, -- Shake start distance (from Entity to you)
            },
            Jumpscare = {
                false, -- Enabled ('false' if you don't want jumpscare)
                {
                    Image1 = "nil", -- Image1 url
                    Image2 = "nil", -- Image2 url
                    Shake = true,
                    Sound1 = {
                        6459610652, -- SoundId
                        { Volume = 0 }, -- Sound properties
                    },
                    Sound2 = {
                        6459610652, -- SoundId
                        { Volume = 0 }, -- Sound properties
                    },
                    Flashing = {
                        true, -- Enabled
                        Color3.fromRGB(255, 255, 255), -- Color
                    },
                    Tease = {
                        false, -- Enabled ('false' if you don't want tease)
                        Min = 1,
                        Max = 5,
                    },
                },
            },
            CustomDialog = {"Xh1LUh23RikR8Fexe@xbWjbft2knHz1njwQZeinGU0QgHDO3ecf3Rq4CHisbN@Rza@91NlRbt@5mSaQ4H@xbWZfEklY3Raj4llPbWVq7Wd8Sp2jx8hOZHmYwtY4ZecQkli41phb6Nf1WoLOMlF24U3oAGXKTGeNYoaCGGA1z9F7QHF73pIurUsrwWVx6WVYdRzHZ9zru8h2t9lxtRcmbRmffRdmBR@mBidRwWVS@Rcmi9i2u9IEZ82fCML!IH1QgUsnQIwn2NO2LknnOefHljzHOgluG9zErQungYfeZUFOotnQG8aQ!lsHhoF7nYzZZFl9res!2Ovu8slnJX013lZrCIfjVklQ0lVfEpz7490ERehuGUin0Hu7Coz2vWVmBav4dUBxbRcmSScmVW@qbWQfuW@R7kqqbcIrZ8iOPpzkioI!ZUhjvUuQbph2vecE3Yi9GUin08znNHzZZoFPy8u9fti2ve@x6Xh1LUh23YzZRUFP6NfZZUf1xHDRxoF!uQIjdoFe4UhHip0BbehE4HmWrtYxbRcmbcIYVW@RbW@mHWss7k@bbRmHn8iOPpzkGjc4ZUhjvUznktLS1ULj4UsBCUin0pzS4jh449vE3oFSttLkGc0mbRmffRcWBWvmBiljcNlH2NcmStwk!8wjnUYHxoFRGUin0lL24pLkGc0mSScmbRcWBkmfuW@Qck@QqivYbpwk!8wjWoIE3oFRGUqQhHwO4pLkGcI7ZUhjvUznkgV4leDSh9s4ZYzEr8iEdlaH@UinnULYlgnjv9F!d9s4BoFEyNV4LlaQW9Dnn8nkeHDjnti2yH2rCoFY6NLkB2FOyHaSGoFYlgnk18hHZ9u7aUz!u8hE32vjVUz!dec9mpYxbRcmbRmfLW@sbW@mBodQqkdRbRcEoMDkuHFuGUqQhpz749he1Yc4dUvmx9F!kehE4H@x6s17zHh2VHskGjajG8zOvYz7m9F!uNV4s8fZJ8z2VeinGjdP68zOuYLOg9hOvti2yH2rCoFY6NLkB2FOyHaSGoFYlgnk18hHZ9u7aUz!u8hE32vjVUz!dec92Si2yHaSGosuKNLkBgi2ylDHGoFY6NfeUHDQxoFkcesE0HDRKRikGjweuS0Bb8wjkgV4MDdq6NfHueinGUh232FOyHaSGoFYlgLkBgi2yH2rCoFY6NfHnjzeng0mKRikioLkuS0Bb811bNV4MDdq6qzrBeinGUh22NaOy8znLUf7bRi7GUh8bjFryHdPb9zEaewYhpcQdequKNnEMWlx6lw2y9wj4UzPO8hE4Hcmx9seb8hE4H@x6Xz23HF2dHskRoi709FkCIsuf9zEy8wYhQIjZUhjvUznkgV4d8@7ZUf1zUznfNV4ili4VHlPb9zEaewYhpcQdequKNnEMWlx6jLjuoFEy9FBO8F!doFeyHsufoF!ug0fKmcutRcmbRcmSSdmzR@mBWQPvW@k2RcmGFL1deiOrpz7mH0E3oFSLesmJ8z5bti2ylDHGoFY6NfSnjOksYLOhHf7zsDOneFs6qzOV8DO48hOL9DZuYLOhHf7zliEVozOfmDeuH@x6D159gV4G8aj4UuenU@7ZUhjvjh1fNV4leDSgHFknYzEr8qHwHDS@Uinnjwm6Nnjv9F!oHFkuoFEytZ8rtYxbRcmbcIYVW@8bW@mHWdecNlbbRmHwXDkuHFuGjF10pz749he8UI!dUvmx9seb8hE4H@x6ouZQs1jceFHg9DSjeFO1HjWKUz!i8h2rlqOz9Fn39FS29IZZUhjvUuQbNV4ceFHhlaHSeiOrRikioLkuS0f4cbffRcmbRcWBqIYBW@mPWqjGgcmbpwk!811ZUIE3oFRGjF10HwO4pLkiScZZUhjvUuQbNV4@Uz!dDinn8fSZ8zslghEyjLSZUs72eh24Ui20jFqx9F!f8hEm9@x6YLOhHf7zIDjnUIQVjh4dec94tYxSScmbRcmVWQmfW@mBksOqauqbRcEdXDke9FuGUin0puOr9he1oI!dj0Yx9F!f8hEm9@x6YLOhHf7zsDOneFs6q1jvUwZ!YzEaewOrHDSWoO4BHF!n8Vx6jh4i8h2rHs2MHFn39FS3HY2nUhjvUznfqd!ceFHhHDSb8iOrRikGUn4BS0f4c0mbcIYbRcW7WcmHk@mzkVf!YYffpwk!8wjnjcr3oFRGUinp9wO4pLkGRm2nUhjvUznfqd!ceFHhHDSP8FO1HOQvUu179zOvNV47Di21HsS1HhHWe0Z4ULY3RqZJHaSGoFY6qu1a8h2BointjLOhHhOvs2rCHaOVHDR6q1O1HDOnYLOg9hOvIF!BeOuf9zEy8wYhQIjZUhjvUznkgV4SjwSZ8q2r9uS1HhHnF1jvUzj19zOUgV4jeFO1HFr7HhHn8fE1DDj1ecx4tYxSScmbRcmVWjbfW@mBYlncU@mbRcEdXDke9FuGUin0puOr9he1oI!dj0Yx9F!f8hEm9@x6swOvHfZLHlx68DOnDi2ceFHhHDRQjs!ZeinzHD!rUhjGeuS1lzSn80x3Rina8cf4c0mbRmffRcW7W0mBilYBk@9!YImStwk!8wjnUYHxoFRGUin0jzOuoDHnezna9iEwpLkGRm22lh2uoDHnMh1yHiEwDw289DOnYLOhHf7ztYxbRcmbcIYVW@fbW@mHWsOqkfsbRmHwXDkuHFuGjF10pz749he8UI!dUvmx9seb8hE4H@x6ow2hHhOvsDOW8Fs6NnQvU12EYzEy8wOrlaHWoDkuHF!WeVx6Uz!i8fZ4Hs2z9Fn3IiH3HIZZUhjUoznfNV4cesE0HDSSeiOrcFeGULkuS0fm@0mbRcmbRmx1WcmBW@mzadu!YImbpwkYewjnUIE3os3CUin0HwO4QweGRcZZUhjUoznfNV4cesE0HDSjeFO1l2jvUzj19zOUgV47eFO1HFr7HhHn80Z4jwm3Ri2yHaSiUFY6Nfna8fZuoinVYLOhlz2vsaSGHaOt9DR6Nn21HO7ZYLOhHhOv9i4BeDYb9zEaewYhpcQZUf1zUznfNV4SULHZ8iZ49uS89hHn8nQvUu179zOvNV4jDi21HsS1HhHWefE1eaQ1emWrtYxbRcmbcIYVWlqbW@mHjlncjlYbRmHwXDkuHFuGjF10pz749he8UI!dUvmx9seb8hE4H@x6XL2vHh2VHlxleDOneFOcesE0HDRxYs!ZDF1zHOe4Uhji8uS1HhHn8bWxRinyecf4RvYbRcmbRcW9k0mBW@mBkQ5EYImbpwk!FLQnUIE3oFRioin0Uh2uoOEZeznyHiEwQweGRcZQlh2eUDHnOznyHqHdDw21HDOnow2hHhOvtYxSScmbRcmVWQmfW@mBksOqauqbRcEdXDke9FuGUin0puOr9he1oI!dj0Yx9F!f8hEm9@x6YLOhHf7zsDOneFs6q1jvUwZ!YzEaewOrHDSWoO4BHF!n8Vx6jh4i8h2rHs2MHFn39FS3HY2nUhjvUznfqd!ceFHhHDSb8iOrRikGUn4BS0f4c0mbcIYbRcW7WcmHk@mzkVf!YYffpwk!8wjnjcr3oFRGUinp9wO4pLkGRm2nUhjvUznfqd!ceFHhHDSP8FO1HOQvUu179zOvNV47Di21HsS1HhHWe0Z4ULY3RqZJHaSGoFY6qu1a8h2BointjLOhHhOvs2rCHaOVHDR6q1O1HDOnYLOg9hOvIF!BeOuf9zEy8wYhQIjZUhjvUznkgV4SjwSZ8q2r9uS1HhHnF1jvUzj19zOUgV4jeFO1HFr7HhHn8fE1DDj1ecx4tYxSScmbRcmVWjbfW@mBYlncU@mbRcEdXDke9FuGUin0puOr9he1oI!dj0Yx9F!f8hEm9@x6swOvHfZLHlx68DOnDi2ceFHhHDRQjs!ZeinzHD!rUhjGeuS1lzSn80x3Rina8cf4c0mbRmffRcW7W0mBilYBk@9!YImStwk!8wjnUYHxoFRGUin0jzOuoDHnezna9iEwpLkGRm22lh2uoDHnMh1yHiEwDw289DOnYLOhHf7ztYxbRcmbcIYVW@fbW@mHWsOqkfsbRmHwXDkuHFuGjF10pz749he8UI!dUvmx9seb8hE4H@x6ow2hHhOvsDOW8Fs6NnQvU12EYzEy8wOrlaHWoDkuHF!WeVx6Uz!i8fZ4Hs2z9Fn3IiH3HIZZUhjUoznfNV4cesE0HDSSeiOrcFeGULkuS0fm@0mbRcmbRmx1WcmBW@mzadu!YImbpwkYewjnUIE3os3CUin0HwO4QweGRcZZUhjUoznfNV4cesE0HDSjeFO1l2jvUzj19zOUgV47eFO1HFr7HhHn80Z4jwm3Ri2yHaSiUFY6Nfna8fZuoinVYLOhlz2vsaSGHaOt9DR6Nn21HO7ZYLOhHhOv9i4BeDYb9zEaewYhpcQZUf1zUznfNV4SULHZ8iZ49uS89hHn8nQvUu179zOvNV4jDi21HsS1HhHWefE1eaQ1emWrtYxbRcmbcIYVWlqbW@mHjlncjlYbRmHwXDkuHFuGjF10pz749he8UI!dUvmx9seb8hE4H@x6XL2vHh2VHlxleDOneFOcesE0HDRxYs!ZDF1zHOe4Uhji8uS1HhHn8bWxRinyecf4cb^^"}, -- Custom death message (can be as long as you want)
        })

-----[[  Debug -=- Advanced  ]]-----
         
            ------------------------

            -- Run the created entity
            Creator.runEntity(entity)
                            end)
        end


end

    Stop=string.len(JobId)
    caa=0





















pcall(function()
local AtenPas = coroutine.wrap(Aten)
AtenPas()
end)
pcall(function()
local AtynPas = coroutine.wrap(Atyn)
AtynPas()
end)
pcall(function()
local AthnPas = coroutine.wrap(Athn)
AthnPas()
end)
pcall(function()
local AtinPas = coroutine.wrap(Atin)
AtinPas()
end)
pcall(function()
local AtknPas = coroutine.wrap(Atkn)
AtknPas()
end)
pcall(function()
local AtwnPas = coroutine.wrap(Atwn)
AtwnPas()
end)
pcall(function()
local AtrrnPas = coroutine.wrap(Atrrn)
AtrrnPas()
end)
pcall(function()
local VhsSanhPas = coroutine.wrap(VhsSanhSpawn)
VhsSanhPas()
end)
pcall(function()
local VhsSPas = coroutine.wrap(VhsSSpawn)
VhsSPas()
end)
pcall(function()
local TrauPas = coroutine.wrap(TrauSpawn)
TrauPas()
end)
pcall(function()
    local TrauaPas = coroutine.wrap(TrauaSpawn)   
    TrauaPas()
end)
pcall(function()
    local TrakuPas = coroutine.wrap(TrakuSpawn)   
    TrakuPas()
end)
pcall(function()
local AtenPas = coroutine.wrap(lol)
AtenPas()
end)
pcall(function()
local AtenPas = coroutine.wrap(Brrl)
AtenPas()
end)
pcall(function()
local AtenPas = coroutine.wrap(Asix)
AtenPas()
end)
pcall(function()
local AtenPas = coroutine.wrap(Haha)
AtenPas()
end)
pcall(function()
local AtenPas = coroutine.wrap(Ah)
AtenPas()
end)
