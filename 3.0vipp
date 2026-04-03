--// 🔥 JAVI MOD GOD FIX (ANTI TODO + LOGO FORZADO)

local url = "https://raw.githubusercontent.com/ApelsinkaFr/ApelHub/refs/heads/main/ApelHub"
local LOGO_ID = "rbxassetid://133147697560132"

-- 🔥 CARGAR SCRIPT
local script = game:HttpGet(url)

-- 🔥 CAMBIAR NOMBRE
script = script:gsub("ApelHub", "JAVI MOD")
script = script:gsub("Apel Hub", "JAVI MOD")

loadstring(script)()

-- 🔥 DETECTOR ULTRA (LOGO + KEY SYSTEM + MENU)
task.spawn(function()
    while true do
        task.wait(0.2)

        for _,v in pairs(game.CoreGui:GetDescendants()) do

            -- 🟢 CAMBIAR TEXTOS
            if v:IsA("TextLabel") or v:IsA("TextButton") then
                if v.Text then
                    local t = string.lower(v.Text)

                    if string.find(t, "apel") or string.find(t, "hub") then
                        v.Text = v.Text
                            :gsub("Apel Hub", "JAVI MOD")
                            :gsub("ApelHub", "JAVI MOD")
                    end
                end
            end

            -- 🟢 CAMBIO BRUTO DE IMÁGENES (ESTE ES EL TRUCO)
            if v:IsA("ImageLabel") or v:IsA("ImageButton") then
                if v.Image and v.Image ~= "" then
                    
                    -- 💀 FORZAR CAMBIO SI ES CUALQUIER LOGO SOSPECHOSO
                    if string.find(string.lower(v.Image), "apel") 
                    or string.find(string.lower(v.Name), "logo")
                    or string.find(string.lower(v.Name), "icon")
                    or v.AbsoluteSize.X < 150 then
                        
                        v.Image = LOGO_ID
                    end

                end
            end

        end
    end
end)

-- 🔥 BLOQUEAR QUE LO CAMBIEN DE NUEVO
task.spawn(function()
    while true do
        task.wait(0.5)

        for _,v in pairs(game.CoreGui:GetDescendants()) do
            if v:IsA("ImageLabel") or v:IsA("ImageButton") then
                
                if v.Image ~= LOGO_ID then
                    if v.AbsoluteSize.X < 150 then
                        v.Image = LOGO_ID
                    end
                end

            end
        end
    end
end)

-- 🔥 HACER REDONDO
task.spawn(function()
    task.wait(1)

    for _,v in pairs(game.CoreGui:GetDescendants()) do
        if v:IsA("ImageLabel") and not v:FindFirstChild("UICorner") then
            local c = Instance.new("UICorner")
            c.CornerRadius = UDim.new(1,0)
            c.Parent = v
        end
    end
end)
