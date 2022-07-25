	local LP = game.Players.LocalPlayer
		for i,v in ipairs(LP.Character:GetDescendants()) do
			if v:IsA("MeshPart") then v.Massless = true
				v.CanCollide = false
				v.CustomPhysicalProperties = PhysicalProperties.new(0, 0, 0, 0, 0)
	
			end
		end
	
		for i,v in ipairs(game.workspace:GetDescendants()) do
			if v:IsA("Seat") then 
				v.Disabled = true
			end
		end
		local x = 40
		local y = 40
		local z = 40
	
	
		local fist = Vector3.new(x,y,z)
	
		LP.Character.RightHand.Size = fist
	
		LP.Character.RightHand.Transparency = 1
		local selectionBox = Instance.new("SelectionBox",LP.Character.RightHand)
		selectionBox.Adornee = LP.Character.RightHand
		selectionBox.Color3 = Color3.new(1, 0, 0)
		selectionBox.Transparency = 0
	
		LP.Character.LeftHand.Size = fist
		LP.Character.BodyEffects.SpecialParts.LeftHand.Size = fist
	
		LP.Character.LeftHand.Transparency = 1
		local selectionBox = Instance.new("SelectionBox",LP.Character.LeftHand)
		selectionBox.Adornee = LP.Character.LeftHand
		selectionBox.Color3 = Color3.new(1, 0, 0)
