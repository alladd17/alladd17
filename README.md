-- Define the function to highlight a player
local function highlightPlayer(player)
    local character = player.Character
    if character then
        local highlight = Instance.new("BoxHandleAdornment")
        highlight.Size = character:GetExtentsSize() * 1.2
        highlight.AlwaysOnTop = true
        highlight.ZIndex = 10
        highlight.Color3 = Color3.new(0, 1, 0) -- You can change the color to your preference
        highlight.Transparency = 0.5
        highlight.Adornee = character
        highlight.Parent = character
    end
end

-- Loop through all players in the game and highlight them
for _, player in pairs(game.Players:GetPlayers()) do
    highlightPlayer(player)
end

