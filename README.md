local lib = loadstring(game:HttpGet('https://raw.githubusercontent.com/Bail-03r/Roblox/main/%5BLibrary%5D/Emenem.lua'))()

--creating main menu
local main = lib:CreateMain('Shadow Hub')

--creating tabs in menu
local tab1 = main:CreateTab('buy nft)')
local tab3 = main:CreateTab('Scripts')



tab1:AddTextbox("Buy Mommeh", "Type the amount.", function(txt)
	for i = 1,txt do
		wait(0)
		game:GetService("ReplicatedStorage").RemoteEvents.BuyItemCash:FireServer("Mommeh Long Legs")
	end
end)
tab1:AddTextbox("Buy Watermelon", "Type the amount.", function(txt)
	for i = 1,txt do
		wait(0.1)
		game:GetService("ReplicatedStorage").RemoteEvents.BuyItemCash:FireServer("Watermelon")
	end
end)
tab1:AddTextbox("nome do item", "Type the name.", function(txt)
	_G.custombuy = txt
end)
tab1:AddTextbox("Quantidade", "Type the amount.", function(txt)
	for i = 1,txt do
		wait(0.0000000000)
		game:GetService("ReplicatedStorage").RemoteEvents.BuyItemCash:FireServer(_G.custombuy)
	end
end)

tab3:AddTextbox("Speed", "Type the amount. Default is 16.", function(txt)
	_G.Speed = txt
	game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 16
		game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = txt
end)

tab3:CreateButton("Destroy Pads", "Only you see this", function()
	game:GetService("Workspace").Map.GroupReward:Destroy()
	game:GetService("Workspace").Map.CodePad:Destroy()
end)
tab3:CreateButton("Destroy Clothing", "Only you see this", function()
	game:GetService("Workspace").Map.ClothingRack:Destroy()
end)
tab3:CreateButton("Destroy Mystery Box", "Only you see this", function()
	game:GetService("Workspace").Map.WeeklyDrop:Destroy()
end)
tab3:CreateButton("Destroy Bubbles", "Only you see this", function()
	game:GetService("Workspace").Map.Decorations:Destroy()
end)
tab3:CreateButton("Destroy Group Wall", "Only you see this", function()
	game:GetService("Workspace").Map.GroupReward.Field:Destroy()
end)
tab3:CreateButton("Destroy Featured Item", "Only you see this", function()
	game:GetService("Workspace").Map.FeaturedItem:Destroy()
end)


    

