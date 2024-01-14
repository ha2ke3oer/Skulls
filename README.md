Local Spawner = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()


-- Create entity
local entityTable = Spawner.createEntity({
    CustomName = "the skull.", -- Custom name of your entity
    Model = "https://github.com/tonyBflako/vynixusdoors/blob/main/fatality.rbxm?raw=true", -- Can be GitHub file or rbxassetid
    Speed = 30000, -- Percentage, 100 = default Rush speed
    DelayTime = 5, -- Time before starting cycles (seconds)
    HeightOffset = 0,
    CanKill = true,
    KillRange = 500,
    BackwardsMovement = true,
    BreakLights = true,
    FlickerLights = {
        true, -- Enabled/Disabled
        100000, -- Time (seconds)
    },
    Cycles = {
        Min = 5,
        Max = 10,
        WaitTime = 3,
    },
    CamShake = {
        true, -- Enabled/Disabled
        {5555, 133124, 0, 1.5}, -- Shake values (don't change if you don't know)
        60, -- Shake start distance (from Entity to you)
    },
    Jumpscare = {
        true, -- Enabled/Disabled
        {
            Image1 = "rbxassetid://0", -- Image1 url
            Image2 = "rbxassetid://0", -- Image2 url
            Shake = true,
            Sound1 = {
                7817626386, -- SoundId
                { Volume = 5 }, -- Sound properties
            },
            Sound2 = {
                0, -- SoundId
                { Volume = 0.5 }, -- Sound properties
            },
            Flashing = {
                false, -- Enabled/Disabled
                Color3.fromRGB(255, 255, 255), -- Color
            },
            Tease = {
                true, -- Enabled/Disabled
                Min = 50,
                Max = 50,
            },
        },
    },
    CustomDialog = {"You can", "put your", "custom death", "message here."}, -- Custom death message
})

Spawner.runEntity(entityTable)
