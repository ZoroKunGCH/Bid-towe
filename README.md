_G.Hom = 150
TweeSpeed = 350
TP = function(Point)
local LocalPlayer = game.Players.LocalPlayer 
	repeat wait()
		TweenPlay = (Point.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
		if LocalPlayer.Character.Humanoid.Sit == true then 
			LocalPlayer.Character.Humanoid.Sit = false 
		end
		pcall(function() 
			tot = game:GetService("TweenService"):Create(LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(TweenPlay/TweeSpeed, Enum.EasingStyle.Linear),{CFrame = Point})
		end)
		tot:Play()
		if TweenPlay <= _G.Hom then
			tot:Cancel()
			LocalPlayer.Character.HumanoidRootPart.CFrame = Point
		end
		if _G.StopTween == true then
			tot:Cancel()
			_G.Clip = false
		end
		if not game:GetService("Workspace"):FindFirstChild("Part") then
			local Part = Instance.new("Part")
                Part.Name = "Part"
                Part.Parent = game.Workspace
                Part.Anchored = true
                Part.Transparency = 1
                Part.Size = Vector3.new(40, 0.5, 40)
            elseif game:GetService("Workspace"):FindFirstChild("Part") then
                game.Workspace["Part"].CFrame = CFrame.new(LocalPlayer.Character.HumanoidRootPart.CFrame.X,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y - 3.92,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
			else
           	 game:GetService("Workspace"):FindFirstChild("Part"):Destroy()
        	end
	until TweenPlay <= _G.Hom
end

function _G.StopTween(target)
    if not TP then
       _G.StopTween = true
       wait()
             TP(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
       wait()
        if game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
           game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
        end
        _G.StopTween = false
        _G.Clip = false
    end
end

function TPPlayer(Pos)
	repeat wait()
		Distance = (Pos.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
		if game.Players.LocalPlayer.Character.Humanoid.Sit == true then game.Players.LocalPlayer.Character.Humanoid.Sit = false end
		pcall(function() tween = game:GetService("TweenService"):Create(game.Players.LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(Distance/200, Enum.EasingStyle.Linear),{CFrame = Pos}) end)
		tween:Play()
		if Distance <= 350 then
			tween:Cancel()
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
		end
		if Distance >= 1200 then
			tween:Cancel()
			game.Players.LocalPlayer.Character.Head:Destroy()
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
			wait(1)
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
		end
		if _G.StopTween == true then
			tween:Cancel()
			_G.Clip = false
		end
	until Distance <= 3000
end
-- tween 1
_G.Hom = 150
TweeSpeed = 350
topos = function(Point)
local LocalPlayer = game.Players.LocalPlayer 
	repeat wait()
		TweenPlay = (Point.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
		if LocalPlayer.Character.Humanoid.Sit == true then 
			LocalPlayer.Character.Humanoid.Sit = false 
		end
		pcall(function() 
			tot = game:GetService("TweenService"):Create(LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(TweenPlay/TweeSpeed, Enum.EasingStyle.Linear),{CFrame = Point})
		end)
		tot:Play()
		if TweenPlay <= _G.Hom then
			tot:Cancel()
			LocalPlayer.Character.HumanoidRootPart.CFrame = Point
		end
		if _G.StopTween == true then
			tot:Cancel()
			_G.Clip = false
		end
		if not game:GetService("Workspace"):FindFirstChild("Part") then
			local Part = Instance.new("Part")
                Part.Name = "Part"
                Part.Parent = game.Workspace
                Part.Anchored = true
                Part.Transparency = 1
                Part.Size = Vector3.new(40, 0.5, 40)
            elseif game:GetService("Workspace"):FindFirstChild("Part") then
                game.Workspace["Part"].CFrame = CFrame.new(LocalPlayer.Character.HumanoidRootPart.CFrame.X,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y - 3.92,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
			else
           	 game:GetService("Workspace"):FindFirstChild("Part"):Destroy()
        	end
	until TweenPlay <= _G.Hom
end

function _G.StopTween(target)
    if not topos then
       _G.StopTween = true
       wait()
             topos(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
       wait()
        if game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
           game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
        end
        _G.StopTween = false
        _G.Clip = false
    end
end

function TPPlayer(Pos)
	repeat wait()
		Distance = (Pos.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
		if game.Players.LocalPlayer.Character.Humanoid.Sit == true then game.Players.LocalPlayer.Character.Humanoid.Sit = false end
		pcall(function() tween = game:GetService("TweenService"):Create(game.Players.LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(Distance/200, Enum.EasingStyle.Linear),{CFrame = Pos}) end)
		tween:Play()
		if Distance <= 350 then
			tween:Cancel()
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
		end
		if Distance >= 1200 then
			tween:Cancel()
			game.Players.LocalPlayer.Character.Head:Destroy()
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
			wait(1)
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
		end
		if _G.StopTween == true then
			tween:Cancel()
			_G.Clip = false
		end
	until Distance <= 3000
end

local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/bloodball/-back-ups-for-libs/main/lime"))()

local w = Library:Window("Karuma hub") 
  
 w:Button("นั่งเรือก่อนกดเปิดออโต้รันหาเกาะลับ", function(v)
 end) 
 
 w:Button("หยุดการ ทวีน รอ การวาป",function()
  topos(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
  _G.Clip = false
TP(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
_G.Clip = false
  end)
 
 w:Toggle("ฟามปลา",function(v)
Farm = v
while Farm do wait()
game:GetService("VirtualInputManager"):SendKeyEvent(true,"E",false,game)
end
 end)

w:Toggle("ออโต้หาเกาะลับ [ย้ายเชิฟ]",function(value)
  _G.MirageHop = value
if game:GetService("Workspace").Map:FindFirstChild("MysticIsland") then
                           topos(game:GetService("Workspace").Map:FindFirstChild("MysticIsland").HumanoidRootPart.CFrame * CFrame.new(0,500,-100))
                    else
if _G.MirageHop then
hop()
end
end
  end)
  
w:Toggle("วาปไปหาเกียร์",function(value)
  TP(game:GetService("Workspace").Map.MysticIsland:FindFirstChildOfClass("MeshPart").CFrame)
  
end)

 w:Button("วาปไปที่ทำเผ่า",function(v)
 
 end)
 
 w:Button("วาปไปห้องทำเผ่าวี",function()
  Game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(28286.35546875, 14895.3017578125, 102.62469482421875)
    end)
    
w:Button("เทเลพอร์ตไปที่คันโยกดึง",function()
  topos(CFrame.new(28575.181640625, 14936.6279296875, 72.31636810302734))
end)

w:Button("เทเลพอร์ตไปยัง Ancient One (ต้องอยู่ใน Temple of Time!) กดที่นี่เพื่อวาป",function()
  topos(CFrame.new(28981.552734375, 14888.4267578125, -120.245849609375))
end) 
