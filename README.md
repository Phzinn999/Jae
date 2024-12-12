-- Interface do Script
local ScreenGui = Instance.new("ScreenGui")
local MinimizeButton = Instance.new("TextButton")
local ScrollingFrame = Instance.new("ScrollingFrame")
local Title = Instance.new("TextLabel")
local ESPButton = Instance.new("TextButton")

-- Propriedades da Interface
ScreenGui.Parent = game.CoreGui

MinimizeButton.Parent = ScreenGui
MinimizeButton.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
MinimizeButton.Position = UDim2.new(0.05, 0, 0.05, 0)
MinimizeButton.Size = UDim2.new(0, 50, 0, 50)
MinimizeButton.Font = Enum.Font.SourceSans
MinimizeButton.Text = "ph"
MinimizeButton.TextColor3 = Color3.fromRGB(255, 255, 255)
MinimizeButton.TextSize = 24

ScrollingFrame.Parent = ScreenGui
ScrollingFrame.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
ScrollingFrame.Position = UDim2.new(0.1, 0, 0.1, 0)
ScrollingFrame.Size = UDim2.new(0, 300, 0, 400)
ScrollingFrame.CanvasSize = UDim2.new(0, 0, 1.5, 0) -- Ajuste o valor conforme necessário
ScrollingFrame.ScrollBarThickness = 10
ScrollingFrame.Visible = true

Title.Parent = ScrollingFrame
Title.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
Title.Size = UDim2.new(1, 0, 0, 50)
Title.Font = Enum.Font.SourceSans
Title.Text = "Script Menu"
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.TextSize = 24

ESPButton.Parent = ScrollingFrame
ESPButton.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
ESPButton.Position = UDim2.new(0, 0, 0.2, 0)
ESPButton.Size = UDim2.new(1, 0, 0, 50)
ESPButton.Font = Enum.Font.SourceSans
ESPButton.Text = "ESP"
ESPButton.TextColor3 = Color3.fromRGB(255, 255, 255)
ESPButton.TextSize = 20

-- Função para habilitar recursos Premium
local function enablePremiumFeatures()
    ScrollingFrame.Visible = true
    ESPButton.Visible = true
    -- Adicionando acesso às casas
    local casas = {"Casa da Maria J.", "Casa do Cirilo", "Casa da Valéria", "Casa do Paulo"}
    for _, casa in ipairs(casas) do
        local CasaButton = Instance.new("TextButton")
        CasaButton.Parent = ScrollingFrame
        CasaButton.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
        CasaButton.Size = UDim2.new(1, 0, 0, 50)
        CasaButton.Font = Enum.Font.SourceSans
        CasaButton.Text = casa
        CasaButton.TextColor3 = Color3.fromRGB(255, 255, 255)
        CasaButton.TextSize = 20
    end
    -- Adicionando acesso aos itens
    local itens = {"Interfone", "Skate", "Estilingue", "Giz Arco-íris"}
    for _, item in ipairs(itens) do
        local ItemButton = Instance.new("TextButton")
        ItemButton.Parent = ScrollingFrame
        ItemButton.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
        ItemButton.Size = UDim2.new(1, 0, 0, 50)
        ItemButton.Font = Enum.Font.SourceSans
        ItemButton.Text = item
        ItemButton.TextColor3 = Color3.fromRGB(255, 255, 255)
        ItemButton.TextSize = 20
    end
end

-- Exemplo de uso
enablePremiumFeatures()
