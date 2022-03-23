Game : https://www.roblox.com/games/6284583030

	Codded by : Keathunsar : https://github.com/dady172172/Roblox-Cheats
	Gui made by : https://v3rmillion.net/member.php?action=profile&uid=507120
	Go vouch release thread : https://v3rmillion.net/showthread.php?tid=1040650
	]]--
	local library = loadstring(game:HttpGet('https://raw.githubusercontent.com/bloodball/-back-ups-for-libs/main/wall%20v3'))()
	kVars = {}
	kVars.windowName = "Pet Simulator X GUI" -- Window Name here
	local w = library:CreateWindow(kVars.windowName) -- Creates the window
	local b = w:CreateFolder("Collect") -- Creates the folder(U will put here your buttons,etc)
	local t = w:CreateFolder("Teleport")
	local z = w:CreateFolder("Extra")
	

	b:Toggle("Orbs",function(bool)
	    kVars.varOrbs = bool
	    if bool then collectOrbs() end
	end)
	

	function collectOrbs()
	    spawn(function()
	        while kVars.varOrbs do
	            wait()
	            for i,v in pairs(game:GetService("Workspace")["__THINGS"].Orbs:GetChildren()) do
	                v.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
	                if kVars.varOrbs == false then return end
	            end
	        end
	    end)
	end
	

	b:Toggle("Loot Bags",function(bool)
	    kVars.varLootBags = bool
	    if bool then collectLootBags() end
	end)

