# redz Library V4
## Library loadstring
### Antigo (não funcionando):
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/REDzHUB/RedzLibV4/main/Source.lua"))()
```
### Novo:
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/hackedx-prototype/RedzLibV4/main/Source.lua"))()
```

Funções da biblioteca
```lua
Library:SetTheme("Nome do Tema") -- https://raw.githubusercontent.com/REDzHUB/RedzLibV4/main/Themes.lua

Library:SetTransparency(0.1) -- 0, 1

Library:GetThemes() -- void, return = table

Library:GetIcon("Nome do Ícone")

-- ///////// 

Library.info.PlaceName

Library.info.Version
```

## Funções Globais
```lua
Instance:Destroy()

Instance:Visible(false)
```

## Janela
Criar uma Janela
```lua
local Window = redzlib:MakeWindow({
  Title = "REDz HUB : Example",
  SubTitle = "by : redz9999",
  LoadText = "redz Hub",
  Flags = "redz Hub | Example.lua"
})

--[[
  Window:Set("Novo Título ou Imagem")
]]
```

## Notificação
Criar uma Notificação
```lua
local Notify = Library:MakeNotify({
  Title = "Notificação",
  Text = "Isso é uma Notificação",
  Time = 5
})

--[[
  Notify:Wait() -- Esperar para Notificação terminar
]]
```

## Tab
Criar uma Tab
```lua
local Tab = Window:MakeTab({Name = "Tab", Icon = "Home"})

--[[
  Tab:Set("Novo Nome ou Imagem")
]]
```

## Seção
Criar uma Seção
```lua
local Section = Tab:AddSection({"Isso é uma seção"})

--[[
  Section:Set("Seção")
]]
```

## Parágrafo
Criar um Parágrafo
```lua
local Paragraph = Tab:AddParagraph({"Parágrafo", "isso é um Parágrafo"})

--[[
  Paragraph:Set("Novo Texto")
  
  Paragraph:Set("Novo Nome", "Novo Texto")
]]
```

## Rótulo (Texto)
Criar um Rótulo de Texto
```lua
local TextLabel = Tab:AddLabel({"Texto", "Isso é um Rótulo de Texto"})

--[[
  TextLabel:Set("Novo Nome")
]]
```

Criar um Rótulo de Imagem
```lua
local ImageLabel = Tab:AddLabel({"Imagem", "Isso é um Rótulo de Imagem", "rbxassetid://"})

--[[
  ImageLabel:Set("Novo Nome", "Nova Imagem")
]]
```

## Botão
Criar um Botão
```lua
local Button = Tab:AddButton({
  Name = "Botão",
  Callback = function()

  end
})

--[[
  Button:Callback(function()
    
  end)
  
  Button:Set("Novo Nome")
]]
```

## Interruptor (ON/OFF)
Criar um Interruptor
```lua
local Toggle = Tab:AddToggle({
  Name = "Interruptor",
  Default = false,
  Callback = function(Value)

  end
})

--[[
  Toggle:Set(false)
  
  Toggle:Callback(function(Value)
  
  end)
]]
```

## Dropdown
Criar um Dropdown
```lua
local Dropdown = Tab:AddDropdown({
  Name = "Dropdown",
  Options = {"1", "2", "3"}
  Default = {"2"}
  MultSelect = false,
  Callback = function(Value)

  end
})

--[[
  Dropdown:Set({New Options}, Void)
  -- Example : {
    Dropdown:Set({"um", "dois", "tre
três"}, true)
  }
  
  Dropdown:Callback(function(Value)
    
  end)
]]
```

## Slider
Criar um Slider
```lua
local Slider = Tab:AddSlider({
  Name = "Slider",
  MinValue = 1,
  MaxValue = 10,
  Default = 5,
  Increase = 1,
  Callback = function(Value)

  end
})

--[[
  Slider:Set(7)
  
  Slider:Callback(function(Value)
    
  end)
]]
```
## Caixa de Entrada
```lua
local TextBox = Tap:AddTextBox({"Título", "", " < entrada > ",
Callback = function()

end
})
```



## Extra
Adicionar um link de convite de Discord
```lua
Tab:AddDiscordInvite({
  DiscordTitle = "REDz Hub | Community",
  DiscordIcon = "rbxassetid://15298567397",
  DiscordLink = "https://discord.gg/7aR7kNVt4g"
})
```

Criar um botão de minimizar
```lua
Window:AddMinimizeButton({
  Button = {
    -- Propriedades do Botão
    Image = "rbxassetid://15298567397"
  },
  UICorner = {true,
    -- Propriedades da borda
    CornerRadius = UDim.new(0.5, 0)
  },
  UIStroke = {false, {
    -- Propriedades do Stroke
  }}
})
```