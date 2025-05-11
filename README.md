<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Script Roblox</title>
  <style>
    body {
      background-color: #1e1e1e;
      color: #ffffff;
      font-family: monospace;
      padding: 20px;
    }
    textarea {
      width: 100%;
      height: 400px;
      background-color: #2e2e2e;
      color: #00ff90;
      padding: 10px;
      border: none;
      resize: vertical;
      font-size: 12px;
    }
    button {
      margin-top: 10px;
      padding: 10px 20px;
      background-color: #00aa88;
      color: white;
      border: none;
      cursor: pointer;
      font-size: 14px;
    }
    button:hover {
      background-color: #007766;
    }
  </style>
</head>
<body>
  <h1>Script para Roblox:</h1>
  <textarea id="script" readonly>
pcall(function() game.CoreGui["&hubGUI"]:Destroy() end)local g=Instance.new("ScreenGui",game.CoreGui)g.Name="&hubGUI"g.ResetOnSpawn=false
local o=Instance.new("TextButton",g)o.Size=UDim2.new(0,50,0,50)o.Position=UDim2.new(0,20,0,20)o.Text="&"o.BackgroundColor3=Color3.fromRGB(30,30,30)o.TextColor3=Color3.new(1,1,1)o.BorderSizePixel=0;o.ZIndex=10
spawn(function()while true do for i=0,1,0.01 do task.wait(0.02)o.Position=UDim2.new(0,20+math.cos(i*6.28)*10,0,20+math.sin(i*6.28)*10)end end end)
local m=Instance.new("Frame",g)m.Size=UDim2.new(0,280,0,480)m.Position=UDim2.new(0.5,-140,0.5,-240)m.BackgroundColor3=Color3.fromRGB(30,30,30)m.Visible=false
m.Active=true m.Draggable=true m.BorderSizePixel=0
local function notify(t)local l=Instance.new("TextLabel",g)l.Size=UDim2.new(0,220,0,30)l.Position=UDim2.new(0.5,-110,0.1,0)l.Text=t;l.TextScaled=true
l.BackgroundTransparency=0.3;l.BackgroundColor3=Color3.fromRGB(40,40,40)l.TextColor3=Color3.new(1,1,1)l.BorderSizePixel=0;game:GetService("Debris"):AddItem(l,2)end
-- (demais linhas ocultadas por brevidade; você pode colar o resto do script aqui)
  </textarea>
  <button onclick="copiar()">Copiar</button>

  <script>
    function copiar() {
      const textarea = document.getElementById("script");
      textarea.select();
      document.execCommand("copy");
      alert("Script copiado!");
    }
  </script>
</body>
</html>