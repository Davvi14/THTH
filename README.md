-- Script para ativar habilidades automaticamente

local jogador = game.Players.LocalPlayer
local personagem = jogador.Character

if personagem then
  local humanoid = personagem:FindFirstChild("Humanoid")
  if humanoid then
    -- Função para ativar a habilidade 1 (substitua "Habilidade1" pelo nome real)
    local function ativarHabilidade1()
      -- Lógica para ativar a habilidade 1
      print("Habilidade 1 ativada automaticamente!")
      -- Insira aqui o código para ativar a habilidade 1
    end

    -- Função para ativar a habilidade 2 (substitua "Habilidade2" pelo nome real)
    local function ativarHabilidade2()
      -- Lógica para ativar a habilidade 2
      print("Habilidade 2 ativada automaticamente!")
      -- Insira aqui o código para ativar a habilidade 2
    end

    -- Evento para detectar quando as habilidades carregam (adapte conforme necessário)
    personagem.ChildAdded:Connect(function(objeto)
      if objeto.Name == "Habilidade1" then
        ativarHabilidade1()
      elseif objeto.Name == "Habilidade2" then
        ativarHabilidade2()
      end
    end)
  end
end
