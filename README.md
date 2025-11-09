
wait()
LoudVolume = true
Submerged = false
Music = true
script.Name = "InkPerson" -- or Bendy.
Character = game.Players.LocalPlayer.Character
Head = Character.Head
anim = Character.Humanoid.Animator
b23 = Instance.new("BoolValue",Character)b23.Name = "InkPerson"
rage = false
CV="Blue"
	p = game.Players.LocalPlayer
	char = p.Character
	local txt = Instance.new("BillboardGui", char)
	txt.Adornee = char .Head
	txt.Name = "_status"
	txt.Size = UDim2.new(2, 0, 1.2, 0)
	txt.StudsOffset = Vector3.new(-9, 8, 0)
	local text = Instance.new("TextLabel", txt)
	text.Size = UDim2.new(10, 0, 7, 0)
	text.FontSize = "Size24"
	text.TextScaled = true
	text.TextTransparency = 0
	text.BackgroundTransparency = 1 
	text.TextTransparency = 0
	text.TextStrokeTransparency = 0
	text.Font = "Arcade"
	text.TextStrokeColor3 = Color3.new(0,0,0)

	text.TextColor3 = Color3.new(0,1,0)
	text.Text = ""
	s = Instance.new("Sound",char.Head)
	s.Name = "BendyMusic"
	s.SoundId = "rbxassetid://746781548"
	s.Pitch = 1
	if LoudVolume == true then
	s.Volume = 5
	else
	s.Volume = 1
	end
	s.Looped = true
	wait(0.1)
	s:play()
	ds = Instance.new("ChorusSoundEffect",s)ds.Enabled = false
	ds2 = Instance.new("TremoloSoundEffect",s)ds2.Frequency = 1.25 ds2.Depth = 0.75 ds2.Duty = 1.5 ds2.Enabled = false
	Music = false
p = game.Players.LocalPlayer
char = p.Character
torso = char.Torso
neck = char.Torso.Neck
cos = math.cos
Player=game:GetService("Players").LocalPlayer
Character=Player.Character 
PlayerGui=Player.PlayerGui
Backpack=Player.Backpack 
Torso=Character.Torso 
Head=Character.Head 
Humanoid=Character.Humanoid Humanoid.Name = "Bendy"
LeftArm=Character["Left Arm"]
LeftLeg=Character["Left Leg"] 
RightArm=Character["Right Arm"]
RightLeg=Character["Right Leg"] 
cam=game.Workspace.CurrentCamera
LS=Torso["Left Shoulder"] 
LH=Torso["Left Hip"] 
RS=Torso["Right Shoulder"] 
RH=Torso["Right Hip"] 
Face = Head.face
Neck=Torso.Neck
it=Instance.new
attacktype=1
vt=Vector3.new
cf=CFrame.new
euler=CFrame.fromEulerAnglesXYZ
angles=CFrame.Angles
cloaked=false
necko=cf(0, 1, 0, -1, -0, -0, 0, 0, 1, 0, 1, 0)
necko2=cf(0, -0.5, 0, -1, -0, -0, 0, 0, 1, 0, 1, 0)
LHC0=cf(-1,-1,0,-0,-0,-1,0,1,0,1,0,0)
LHC1=cf(-0.5,1,0,-0,-0,-1,0,1,0,1,0,0)
RHC0=cf(1,-1,0,0,0,1,0,1,0,-1,-0,-0)
RHC1=cf(0.5,1,0,0,0,1,0,1,0,-1,-0,-0)
RootPart=Character.HumanoidRootPart
RootJoint=RootPart.RootJoint
RootCF=euler(-1.57,0,3.14)
attack = false 
bounce=false
cooldown=false
deeznuts=false
attackdebounce = false 
deb=false
equipped=true
hand=false
MMouse=nil
combo=0
mana=0
trispeed=.2
attackmode='none'
local idle=0
local Anim="Idle"
local Effects={}
local gun=false
local shoot=false
player=nil 
mana=0
cam = workspace.CurrentCamera
ZTarget = nil
RocketTarget = nil
local m = Instance.new("Model",Character)
m.Name = "WeaponModel"
Humanoid.MaxHealth = math.huge
Humanoid.Health = Humanoid.MaxHealth
mouse=Player:GetMouse()
--welds 
RW, LW=Instance.new("Weld"), Instance.new("Weld") 
RW.Name="Right Shoulder" LW.Name="Left Shoulder"
LH=Torso["Left Hip"]
RH=Torso["Right Hip"]
TorsoColor=Torso.BrickColor
function NoOutline(Part)
Part.TopSurface,Part.BottomSurface,Part.LeftSurface,Part.RightSurface,Part.FrontSurface,Part.BackSurface = 10,10,10,10,10,10
end
player=Player 
ch=Character
RSH=ch.Torso["Right Shoulder"] 
LSH=ch.Torso["Left Shoulder"] 
--  

	function swait(num)
    if num==0 or num==nil then
    game:service'RunService'.Heartbeat:wait(0)
    else
    for i=0,num do
    game:service'RunService'.Heartbeat:wait(0)
    end
    end
	end
	

local Player = game.Players.localPlayer
local Character = Player.Character
local red = 255
local green = 255
local blue = 255
local mouse = Player:GetMouse()
local m = Instance.new("Model", Character)
m.Name = "WeaponModel"
local Head = Character.Head
local Torso = Character.Torso
local cam = game.Workspace.CurrentCamera
local RootPart = Character.HumanoidRootPart
local RootJoint = RootPart.RootJoint
local equipped = false
local attack = false
local Anim = "Idle"
local idle = 0
local attacktype = 1
local Torsovelocity = (RootPart.Velocity * Vector3.new(1, 0, 1)).magnitude
local velocity = RootPart.Velocity.y
local sine = 0
local change = 1
local charge = 1
local grabbed = false
local cn = CFrame.new
local mr = math.rad
local angles = CFrame.Angles
local ud = UDim2.new
local c3 = Color3.new
local lim = 0
local st = 0
local necko = cn(0, 1, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
local attacktype = 1
local ZTarget, RocketTarget = nil, nil
local euler = CFrame.fromEulerAnglesXYZ
local v = game.Players.localPlayer
local torso = v.Character.Torso
-- Bypass
local trazx = Instance.new("ParticleEmitter")
local soonds = Instance.new("Sound")
-- 
plr = game.Players.LocalPlayer
char = game.Players.LocalPlayer.Character
t = game.Players.LocalPlayer.Character.Torso
h = game.Players.LocalPlayer.Character.Head
ra = game.Players.LocalPlayer.Character["Right Arm"]
la = game.Players.LocalPlayer.Character["Left Arm"]
rl = game.Players.LocalPlayer.Character["Right Leg"]
ll = game.Players.LocalPlayer.Character["Left Leg"]
hrp = Character.HumanoidRootPart
tors = Character.Torso
lleg = Character["Left Leg"]
root = Character.HumanoidRootPart
hed = Character.Head
rleg = Character["Right Leg"]
rarm = Character["Right Arm"]
larm = Character["Left Arm"]
  RSC0 = CFrame.new(1, 0.5, 0, 0, 0, 1, 0, 1, 0, -1, 0, 0)
  RSC1 = CFrame.new(-0.5, 0.5, 0, 0, 0, 1, 0, 1, 0, -1, 0, 0)
  LSC0 = CFrame.new(-1, 0.5, 0, 0, 0, -1, 0, 1, 0, 1, 0, 0)
  LSC1 = CFrame.new(0.5, 0.5, 0, 0, 0, -1, 0, 1, 0, 1, 0, 0)
  RHC0 = CFrame.new(1, -1, 0, 0, 0, 1, 0, 1, 0, -1, 0, 0)
  RHC1 = CFrame.new(0.5, 1, 0, 0, 0, 1, 0, 1, 0, -1, 0, 0)
  LHC0 = CFrame.new(-1, -1, 0, 0, 0, -1, 0, 1, 0, 1, 0, 0)
  LHC1 = CFrame.new(-0.5, 1, 0, 0, 0, -1, 0, 1, 0, 1, 0, 0)
  NC0 = CFrame.new(0, 1, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
  NC1 = CFrame.new(0, -0.5, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
  RJC0 = CFrame.new(0, 0, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
  RJC1 = CFrame.new(0, 0, 0, -1, 0, 0, 0, 0, 1, 0, 1, 0)
  RS = tors:FindFirstChild("Right Shoulder")
  LS = tors:FindFirstChild("Left Shoulder")
  RH = tors:FindFirstChild("Right Hip")
  LH = tors:FindFirstChild("Left Hip")
  RJ = hrp:FindFirstChild("RootJoint")
  N = tors:FindFirstChild("Neck")
  cf = CFrame.new
  ang = CFrame.Angles
  rd = math.rad
  rd2 = math.random
bsize1 = NumberSequenceKeypoint.new(3,3,3)
bsize2 = NumberSequenceKeypoint.new(10,10,10)
local Effects = {}
attack = false
local attacking = false
vt = Vector3.new
bc = BrickColor.new
br = BrickColor.random
it = Instance.new
cf = CFrame.new
euler = CFrame.fromEulerAnglesXYZ
angles = CFrame.Angles
matr = math.random
local colororg = BrickColor.new("Dark indigo") -- set color u like
local meshtype = "Sphere" -- only for specialmesh
mouse = plr:GetMouse()

  function lerpz(joint, prop, cfrmz, alp)
    joint[prop] = joint[prop]:lerp(cfrmz, alp)
  end
  function resetlerp()
    RJ.C0 = RJC0
    RJ.C1 = RJC1
    N.C0 = NC0
    N.C1 = NC1
    RS.C0 = RSC0
    RS.C1 = RSC1
    LS.C0 = LSC0
    LS.C1 = LSC1
    RH.C0 = RHC0
    RH.C1 = RHC1
    LH.C0 = LHC0
	LH.C1 = LHC1
  end
local S = Instance.new("Sound",hrp)S.SoundId = "rbxassetid://718967797" S:Play() S.Volume = 1
char.Head:FindFirstChild("face").Texture = "rbxassetid://258433204"
for i = 1,35,0.5 do
swait()
lerpz(RJ, "C0", RJC0 * cf(0, 0, 0) * ang(rd(-15), rd(0), rd(0)), 0.3)
lerpz(N, "C0", NC0 * cf(0, 0, 0) * ang(rd(-15), rd(0), rd(0)), 0.3)
lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(-35), rd(0), rd(180)), 0.3)
lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(LS, "C0", LSC0 * cf(0, 0, 0) * ang(rd(-35), rd(0), rd(-180)), 0.3)
lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-15), rd(0), rd(-25)), 0.3)
lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(-15), rd(0), rd(25)), 0.3)
lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
end
char.Head:FindFirstChild("face").Texture = ""
char:findFirstChild("Body Colors"):remove()
for i,v in pairs (char:children()) do
if v.ClassName == "Part" then
if v.Name ~= "HumanoidRootPart" then
v.Material = "Sand" v.BrickColor = BrickColor.new("Really black")
local tra = trazx:clone()tra.Parent = v
tra.Texture = "rbxassetid://286708119"
tra.LightEmission = 0
tra.Color = ColorSequence.new(Color3.new(0/255,0/255,0/255))
tra.Rate = 200
tra.Lifetime = NumberRange.new(1)
tra.Size = NumberSequence.new({NumberSequenceKeypoint.new(0,0,0),NumberSequenceKeypoint.new(1,3,0)})
tra.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0,0),NumberSequenceKeypoint.new(0.8,0,0),NumberSequenceKeypoint.new(1,1,0)})
tra.Speed = NumberRange.new(0) tra.VelocitySpread = 360 tra.Name = "Ink" tra.LockedToPart = true
tra.VelocityInheritance = 0.5 tra.ZOffset = 3
if v.Name ~= "Head" then
local M = Instance.new("SpecialMesh",v)M.MeshId = "rbxassetid://9856898" M.TextureId = "rbxassetid://64619306"
M.Scale = Vector3.new(v.Size.X*2,v.Size.Y*2,v.Size.Z*2)
end
end
end
end
char.Head.Transparency = 1
local P = Instance.new("Part",char)P.Size = Vector3.new(2,1,1)P.Anchored = false P.CanCollide = false P.Name = "HeadPart"
local W = Instance.new("Weld",P)W.Part0 = P W.Part1 = char.Head
local HM = Instance.new("SpecialMesh",P)HM.MeshId = "rbxassetid://539723444" HM.TextureId = "rbxassetid://64619306" HM.Scale = Vector3.new(0.97,0.97,0.97)
wait(3)
char.Head:FindFirstChild("face").Texture = ""
if char:findFirstChild("Shirt")~=nil then
char:findFirstChild("Shirt"):remove()
end
if char:findFirstChild("Pants")~=nil then
char:findFirstChild("Pants"):remove()
end
for i,v in pairs (char:children()) do
if v.ClassName == "Accessory" then
v.Handle.Mesh.TextureId = "rbxassetid://64619306"
v.Handle.Material = "Sand"
end
if v.ClassName == "Part" then
if v:findFirstChild("Ink")~=nil then
v:findFirstChild("Ink").Acceleration = Vector3.new(0,-10,0) v:findFirstChild("Ink").LockedToPart = false v:findFirstChild("Ink").ZOffset = 0
v:findFirstChild("Ink").Size = NumberSequence.new({NumberSequenceKeypoint.new(0,0.6,0.025),NumberSequenceKeypoint.new(1,0,0)})
end
end
end
local S2 = soonds:clone() S2.Parent = hrp S2.SoundId = "rbxassetid://137473066" S2:Play() S2.Volume = 1 S2.PlaybackSpeed = 1.75
New = function(Object, Parent, Name, Data)
	local Object = Instance.new(Object)
	for Index, Value in pairs(Data or {}) do
		Object[Index] = Value
	end
	Object.Parent = Parent
	Object.Name = Name
	return Object
end

function InkPuddle(Size,CFramez)
local P4 = Instance.new("Part",game.Workspace)P4.BrickColor = BrickColor.new("Really black")P4.CanCollide = false P4.Name = "Ink"
P4.CFrame = CFramez P4.Anchored = true local M6 = Instance.new("SpecialMesh",P4) M6.MeshId = "rbxassetid://465435723" M6.TextureId = "rbxassetid://64619306"
M6.Scale = Vector3.new(Size/30,0.01,Size/30)game.Debris:AddItem(P4,15)
P4.Size = P4.Size + Vector3.new(0.2,0.2,0.2)
end

function Submerge()
if Submerged == false then
Submerged = true
attack = true
hrp.Anchored = true
Humanoid.WalkSpeed = 150 Humanoid.JumpPower = 250
local P = Instance.new("Part",game.Workspace)P.Transparency = 1 P.Anchored = true P.CanCollide = false P.Size = Vector3.new(0.2,0.2,0.2)
P.CFrame = hrp.CFrame*CFrame.new(0,-2,0)
local tra = trazx:clone()tra.Parent = P
tra.Texture = "rbxassetid://286708119"
tra.LightEmission = 0
tra.Color = ColorSequence.new(Color3.new(0/255,0/255,0/255))
tra.Rate = 400
tra.Lifetime = NumberRange.new(0.5) tra.Acceleration = Vector3.new(0,-125,0)
tra.Size = NumberSequence.new({NumberSequenceKeypoint.new(0,5,0),NumberSequenceKeypoint.new(1,0,0)})
tra.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0,0),NumberSequenceKeypoint.new(0.8,0,0),NumberSequenceKeypoint.new(1,1,0)})
tra.Speed = NumberRange.new(25) tra.VelocitySpread = 360 tra.Name = "Ink" tra.LockedToPart = true
tra.VelocityInheritance = 0.5 tra.ZOffset = 5
local S4 = soonds:clone() S4.Parent = hrp S4.SoundId = "rbxassetid://466869979" S4.Volume = 10 S4:Play() game.Debris:AddItem(S4,5)
for i = 1,1 do
swait()
lerpz(RJ, "C0", RJC0 * cf(0, 0, 5000) * ang(rd(0), rd(0), rd(0)), 1)
end
hrp.Anchored = false
tra.Enabled = false
game.Debris:AddItem(P,2)
InkPuddle(12,hrp.CFrame*CFrame.new(0,-2.5,0))
while Submerged == true do
wait()
end
InkPuddle(24,hrp.CFrame*CFrame.new(0,-2.5,0))
Humanoid.WalkSpeed = 16 Humanoid.JumpPower = 50
attack = false
else
Submerged = false
local P = Instance.new("Part",game.Workspace)P.Transparency = 1 P.Anchored = true P.CanCollide = false P.Size = Vector3.new(0.2,0.2,0.2)
P.CFrame = hrp.CFrame*CFrame.new(0,-2,0)
local tra = trazx:clone()tra.Parent = P
tra.Texture = "rbxassetid://286708119"
tra.LightEmission = 0
tra.Color = ColorSequence.new(Color3.new(0/255,0/255,0/255))
tra.Rate = 400
tra.Lifetime = NumberRange.new(1.5) tra.Acceleration = Vector3.new(0,-150,0)
tra.Size = NumberSequence.new({NumberSequenceKeypoint.new(0,8,0),NumberSequenceKeypoint.new(1,0,0)})
tra.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0,0),NumberSequenceKeypoint.new(0.8,0,0),NumberSequenceKeypoint.new(1,1,0)})
tra.Speed = NumberRange.new(75) tra.VelocitySpread = 360 tra.Name = "Ink" tra.LockedToPart = true
tra.VelocityInheritance = 0.5 tra.ZOffset = 5 
local S4 = soonds:clone() S4.Parent = hrp S4.SoundId = "rbxassetid://130779572" S4.Volume = 10 S4:Play() game.Debris:AddItem(S4,5)
wait(0.25)
hrp.Anchored = false
tra.Enabled = false
game.Debris:AddItem(P,2)
end
end
CarriedPlayah = nil
function PullSubmerge()
if Submerged == false and CarriedPlayah == nil then
local hit = false
for i,v in pairs (game.Workspace:children()) do
if v ~= char and v:findFirstChild("Humanoid")~=nil and v:findFirstChild("HumanoidRootPart")~=nil then
if (v.HumanoidRootPart.Position-hrp.Position).magnitude <= 4 then
if hit == true then return end
InkPuddle(18,hrp.CFrame*CFrame.new(0,-2.5,0))
v.Parent = nil
CarriedPlayah = v
hrp.Anchored = true
Humanoid.WalkSpeed = 150
Submerged = true
attack = true
--
for i,v in pairs (v:children()) do
if v.ClassName == "Part" or v.ClassName == "MeshPart" then
if v.Name ~= "HumanoidRootPart" then
v.Material = "Sand" v.BrickColor = BrickColor.new("Really black")
local tra = trazx:clone()tra.Parent = v
tra.Texture = "rbxassetid://286708119"
tra.LightEmission = 0
tra.Color = ColorSequence.new(Color3.new(0/255,0/255,0/255))
tra.Rate = 200
tra.Lifetime = NumberRange.new(1)
tra.Size = NumberSequence.new({NumberSequenceKeypoint.new(0,0,0),NumberSequenceKeypoint.new(1,2,0)})
tra.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0,0),NumberSequenceKeypoint.new(0.8,0,0),NumberSequenceKeypoint.new(1,1,0)})
tra.Speed = NumberRange.new(0) tra.VelocitySpread = 360 tra.Name = "Ink" tra.LockedToPart = true
tra.VelocityInheritance = 0.5 tra.ZOffset = 3
if v.Name ~= "Head" then
local M = Instance.new("SpecialMesh",v)M.MeshId = "rbxassetid://9856898" M.TextureId = "rbxassetid://64619306"
M.Scale = Vector3.new(v.Size.X*2,v.Size.Y*2,v.Size.Z*2)
end
end
end
end
v.Head:FindFirstChild("face"):remove()
local HM = Instance.new("SpecialMesh",v.Head)HM.MeshId = "rbxassetid://539723444" HM.TextureId = "rbxassetid://64619306"
if v:findFirstChild("Shirt")~=nil then
v:findFirstChild("Shirt"):remove()
end
if v:findFirstChild("Pants")~=nil then
v:findFirstChild("Pants"):remove()
end
for i,v in pairs (v:children()) do
if v.ClassName == "Accessory" then
v.Handle.Mesh.TextureId = "rbxassetid://64619306"
v.Handle.Material = "Sand"
end
if v.ClassName == "Part" or v.ClassName == "MeshPart" then
if v.Name ~= "HumanoidRootPart" then
if v:findFirstChild("Mesh")~= nil then
if v:findFirstChild("Mesh").ClassName == "SpecialMesh" then
v.Mesh.TextureId = "rbxassetid://64619306"
end
end
v.Material = "Sand" v.BrickColor = BrickColor.new("Really black")
v:findFirstChild("Ink").Acceleration = Vector3.new(0,-10,0) v:findFirstChild("Ink").LockedToPart = false v:findFirstChild("Ink").ZOffset = 0
v:findFirstChild("Ink").Size = NumberSequence.new({NumberSequenceKeypoint.new(0,0.2,0.025),NumberSequenceKeypoint.new(1,0,0)})
if v.Name ~= "Head" then
local M = Instance.new("SpecialMesh",v)M.MeshId = "rbxassetid://9856898" M.TextureId = "rbxassetid://64619306"
M.Scale = Vector3.new(v.Size.X*2,v.Size.Y*2,v.Size.Z*2)
end
end
end
end
--
local P = Instance.new("Part",game.Workspace)P.Transparency = 1 P.Anchored = true P.CanCollide = false P.Size = Vector3.new(0.2,0.2,0.2)
P.CFrame = hrp.CFrame*CFrame.new(0,-2,0)
local tra = trazx:clone()tra.Parent = P
tra.Texture = "rbxassetid://286708119"
tra.LightEmission = 0
tra.Color = ColorSequence.new(Color3.new(0/255,0/255,0/255))
tra.Rate = 400
tra.Lifetime = NumberRange.new(0.5) tra.Acceleration = Vector3.new(0,-125,0)
tra.Size = NumberSequence.new({NumberSequenceKeypoint.new(0,5,0),NumberSequenceKeypoint.new(1,0,0)})
tra.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0,0),NumberSequenceKeypoint.new(0.8,0,0),NumberSequenceKeypoint.new(1,1,0)})
tra.Speed = NumberRange.new(25) tra.VelocitySpread = 360 tra.Name = "Ink" tra.LockedToPart = true
tra.VelocityInheritance = 0.5 tra.ZOffset = 5
local S4 = soonds:clone() S4.Parent = hrp S4.SoundId = "rbxassetid://466869979" S4.Volume = 10 S4:Play() game.Debris:AddItem(S4,5)
for i = 1,1 do
lerpz(RJ, "C0", RJC0 * cf(0, 0, 5000) * ang(rd(0), rd(0), rd(0)), 1)
end
hrp.Anchored = false
tra.Enabled = false
game.Debris:AddItem(P,2)
end
end
end
while Submerged == true do
wait()
end
Humanoid.WalkSpeed = 16
attack = false
elseif CarriedPlayah ~= nil then
Submerged = false
InkPuddle(30,hrp.CFrame*CFrame.new(0,-2.5,0))
local P = Instance.new("Part",game.Workspace)P.Transparency = 1 P.Anchored = true P.CanCollide = false P.Size = Vector3.new(0.2,0.2,0.2)
P.CFrame = hrp.CFrame*CFrame.new(0,-2,0)
local tra = trazx:clone()tra.Parent = P
tra.Texture = "rbxassetid://286708119"
tra.LightEmission = 0
tra.Color = ColorSequence.new(Color3.new(0/255,0/255,0/255))
tra.Rate = 400
tra.Lifetime = NumberRange.new(1.5) tra.Acceleration = Vector3.new(0,-150,0)
tra.Size = NumberSequence.new({NumberSequenceKeypoint.new(0,8,0),NumberSequenceKeypoint.new(1,0,0)})
tra.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0,0),NumberSequenceKeypoint.new(0.8,0,0),NumberSequenceKeypoint.new(1,1,0)})
tra.Speed = NumberRange.new(75) tra.VelocitySpread = 360 tra.Name = "Ink" tra.LockedToPart = true
tra.VelocityInheritance = 0.5 tra.ZOffset = 5 
local S4 = soonds:clone() S4.Parent = hrp S4.SoundId = "rbxassetid://130779572" S4.Volume = 10 S4:Play() game.Debris:AddItem(S4,5)
CarriedPlayah.Parent = game.Workspace
CarriedPlayah.HumanoidRootPart.CFrame = hrp.CFrame
CarriedPlayah = nil
wait(0.25)
hrp.Anchored = false
tra.Enabled = false
game.Debris:AddItem(P,2)
end
end

function Whistle()
local Whis = Instance.new("Sound",game.Workspace) Whis.Volume = 2 Whis.SoundId = "rbxassetid://850062880" Whis:Play()
end

local Mosci = true
function Musicz()
if LoudVolume == true then
if Mosci == true then
Mosci = false
for i = 1,10 do
s.Volume = s.Volume - 5/10
wait()
end
else
Mosci = true
for i = 1,10 do
s.Volume = s.Volume + 5/10
wait()
end
end
else
if Mosci == true then
Mosci = false
for i = 1,10 do
s.Volume = s.Volume - 0.1
wait()
end
else
Mosci = true
for i = 1,10 do
s.Volume = s.Volume + 0.1
wait()
end
end	
end
end

moosict = 1
function MusicSwitch()
if moosict == 1 then
moosict = 2
s.SoundId = "rbxassetid://742318689"
elseif moosict == 2 then
moosict = 3
s.SoundId = "rbxassetid://695408779"
elseif moosict == 3 then
moosict = 4
s.SoundId = "rbxassetid://914975605"
elseif moosict == 4 then
moosict = 1
s.SoundId = "rbxassetid://746781548"
end
end
Dance1 = false
Dance2 = false
function DanceOne()
if Dance1 == false then
Dance1 = true attack = true
anim.Parent = nil
local Cane = Instance.new("Part",char)Cane.Size = Vector3.new(4,0.2,0.2)Cane.CanCollide = false Cane.BrickColor = BrickColor.new("Pine Cone")
Cane.Anchored = false Cane.Material = "Wood" 
local CW = Instance.new("Weld",RightArm)CW.Part0 = RightArm CW.Part1 = Cane CW.C0 = CFrame.new(-1.5,-1,0)
while Dance1 == true do
CW.C0 = CFrame.new(-0.5,-1,0)
for i = 1,3 do -- RIGHT
swait()
lerpz(RJ, "C0", RJC0 * cf(-0.5, 0, 0) * ang(rd(0), rd(-5), rd(0)), 0.3)
lerpz(N, "C0", NC0 * cf(0, 0, -0.35) * ang(rd(0), rd(-15), rd(0)), 0.3)
lerpz(RS, "C0", RSC0 * cf(0, -0.2, 0) * ang(rd(-5), rd(-45), rd(25)), 0.3)
lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(LS, "C0", LSC0 * cf(0, 0.2, -1) * ang(rd(75), rd(10), rd(-45)), 0.3)
lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(-50), rd(0), rd(0)), 0.3)
lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(10), rd(0), rd(0)), 0.3)
lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
end
wait(0.3)
CW.C0 = CFrame.new(-1.5,-1,0)
for i = 1,3 do
swait()
lerpz(RJ, "C0", RJC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(N, "C0", NC0 * cf(0, 0, 0.3) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(RS, "C0", RSC0 * cf(0, 0.6, 0) * ang(rd(0), rd(0), rd(45)), 0.3)
lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(LS, "C0", LSC0 * cf(0, 0.6, 0) * ang(rd(0), rd(0), rd(-45)), 0.3)
lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
end
wait(0.1)
CW.C0 = CFrame.new(-0.5,-1,0)
for i = 1,3 do -- LEFT
swait()
lerpz(RJ, "C0", RJC0 * cf(0.5, 0, 0) * ang(rd(0), rd(5), rd(0)), 0.3)
lerpz(N, "C0", NC0 * cf(0, 0, -0.35) * ang(rd(0), rd(15), rd(0)), 0.3)
lerpz(RS, "C0", RSC0 * cf(0, 0.2, -1) * ang(rd(75), rd(-10), rd(45)), 0.3)
lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(LS, "C0", LSC0 * cf(0, -0.2, 0) * ang(rd(-85), rd(-25), rd(-85)), 0.3)
lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(10), rd(0), rd(0)), 0.3)
lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(-50), rd(0), rd(0)), 0.3)
lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
end
wait(0.3)
CW.C0 = CFrame.new(-1.5,-1,0)
for i = 1,3 do
swait()
lerpz(RJ, "C0", RJC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(N, "C0", NC0 * cf(0, 0, 0.3) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(RS, "C0", RSC0 * cf(0, 0.6, 0) * ang(rd(0), rd(0), rd(45)), 0.3)
lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(LS, "C0", LSC0 * cf(0, 0.6, 0) * ang(rd(0), rd(0), rd(-45)), 0.3)
lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.3)
end
wait(0.1)
end
Cane:remove()
anim.Parent = Humanoid
attack = false
else
Dance1 = false
end
end

function DanceTwo()
if Dance2 == false then
Dance2 = true attack = true
anim.Parent = nil
while Dance2 == true do
for i = 1,3 do
swait()
lerpz(RJ, "C0", RJC0 * cf(0, 0, 0.1) * ang(rd(0), rd(0), rd(0)), 0.35)
lerpz(N, "C0", NC0 * cf(0, 0, 0.25) * ang(rd(0), rd(0), rd(0)), 0.35)
lerpz(RS, "C0", RSC0 * cf(0, -0.1, 0) * ang(rd(5), rd(0), rd(0)), 0.35)
lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.35)
lerpz(LS, "C0", LSC0 * cf(0, -0.1, 0) * ang(rd(5), rd(0), rd(0)), 0.35)
lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.35)
lerpz(RH, "C0", RHC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.35)
lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.35)
lerpz(LH, "C0", LHC0 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.35)
lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.35)
end
wait(0.415)
for i = 1,3 do
swait()
lerpz(RJ, "C0", RJC0 * cf(0, 0, -0.5) * ang(rd(0), rd(0), rd(0)), 0.35)
lerpz(N, "C0", NC0 * cf(0.2, 0, -0.2) * ang(rd(0), rd(-20), rd(0)), 0.35)
lerpz(RS, "C0", RSC0 * cf(0, 0.3, 0) * ang(rd(-5), rd(0), rd(0)), 0.35)
lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.35)
lerpz(LS, "C0", LSC0 * cf(0, 0.3, 0) * ang(rd(-5), rd(0), rd(0)), 0.35)
lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.35)
lerpz(RH, "C0", RHC0 * cf(0, 0.35, 0) * ang(rd(-4), rd(0), rd(0)), 0.35)
lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.35)
lerpz(LH, "C0", LHC0 * cf(0, 0.35, 0) * ang(rd(-4), rd(0), rd(0)), 0.35)
lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), 0.35)
end
wait(0.415)
end
anim.Parent = Humanoid
attack = false
else
Dance2 = false
end
end

Smile = false
function BSmile()
if Smile == true then
char.Head:FindFirstChild("face").Texture = "rbxassetid://875244780"
Smile = false
else
Smile = true
char.Head:FindFirstChild("face").Texture = ""
end
end

function BFrown()
if Smile == true then
char.Head:FindFirstChild("face").Texture = "rbxassetid://876092595"
Smile = false
else
Smile = true
char.Head:FindFirstChild("face").Texture = ""
end
end

TimeFreeze = false
function TimeFresh()
if TimeFreeze == false then
TimeFreeze = true
for i,v in pairs (char:children()) do
if v.ClassName == "Accessory" then
for i,v2 in pairs (v:children()) do
if v2.ClassName == "Part" then
v2.Anchored = true
end
end
end
for i,v in pairs (char:children()) do
if v.ClassName == "Part" then
v.Anchored = true
end
end
end
else
TimeFreeze = false
end
end

function InkClone()
char.Archivable = true
local C = char:clone()C.Parent = game.Workspace
C.HumanoidRootPart.CFrame = char.HumanoidRootPart.CFrame
C.HumanoidRootPart.Touched:connect(function(Part)
if Part.Parent ~= char and Part.Name ~= "Handle" and Part.Size.Z <= 150 and Part.Size.X <= 150 and Part.Size.Y <= 150 then
local P = Instance.new("Part",game.Workspace)P.Transparency = 1 P.Anchored = true P.CanCollide = false P.Size = Vector3.new(0.2,0.2,0.2)
P.CFrame = C.HumanoidRootPart.CFrame*CFrame.new(0,-2,0)
local tra = trazx:clone()tra.Parent = P
tra.Texture = "rbxassetid://286708119"
tra.LightEmission = 0
tra.Color = ColorSequence.new(Color3.new(0/255,0/255,0/255))
tra.Rate = 400
tra.Lifetime = NumberRange.new(1.5) tra.Acceleration = Vector3.new(0,-150,0)
tra.Size = NumberSequence.new({NumberSequenceKeypoint.new(0,6,0),NumberSequenceKeypoint.new(1,0,0)})
tra.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,0,0),NumberSequenceKeypoint.new(0.8,0,0),NumberSequenceKeypoint.new(1,1,0)})
tra.Speed = NumberRange.new(45) tra.VelocitySpread = 360 tra.Name = "Ink" tra.LockedToPart = true
tra.VelocityInheritance = 0.5 tra.ZOffset = 5 
local S4 = soonds:clone() S4.Parent = hrp S4.SoundId = "rbxassetid://130779572" S4.Volume = 10 S4:Play() game.Debris:AddItem(S4,5)
InkPuddle(4,C.HumanoidRootPart.CFrame*CFrame.new(0,-2.5,0))
C:remove()
wait(0.1)
tra.Enabled = false game.Debris:AddItem(P,2)
end
end)
char.Archivable = false
end

mouse.KeyDown:connect(function(key)
if key == "z" then
Submerge()
end
if key == "x" then
PullSubmerge()
end
if key == "c" then
InkClone()
end
if key == "b" then
Whistle()
end
if key == "f" then
DanceOne()
end
if key == "g" then
DanceTwo()
end
if key == "j" then
TimeFresh()
end
if key == "l" then
BSmile()
end
if key == ";" then
BFrown()
end
if key == "n" then
MusicSwitch()
end
if key == "m" then
Musicz()
end
end)

  game:GetService("RunService").RenderStepped:connect(function()

	Humanoid.MaxHealth = Humanoid.MaxHealth*2
	Humanoid.Health = Humanoid.MaxHealth*2
	if TimeFreeze == false then
	for i,v in pairs (char:children()) do
	if v.ClassName == "Accessory" then
	for i,v2 in pairs (v:children()) do
	if v2.ClassName == "Part" then
	v2.Anchored = false
	for i,v3 in pairs (v2:children()) do
	if v3.ClassName == "Fire" then
	v3:remove()
	end
	if v3.ClassName == "ParticleEmitter" and v3.Name ~= "Ink" then
	v3:remove()
	end
	end
	end
	end
	end
	end
	for i,v in pairs (char:children()) do
	if v.ClassName == "Part" then
	v.Anchored = false
	end
	end
	end
	if attack == false and Dance1 == false and Dance2 == false then
	    if RootPart.Velocity.y > 1 then
      Anim = "Jump"

    else
      if RootPart.Velocity.y < -1 then
        Anim = "Fall"

      else
        if Torsovelocity < 1 then
          Anim = "Idle"
		local animsped = 1
        sine = sine + 5
        lerpz(RJ, "C0", RJC0 * cf(0, 0, ( 0.1 * cos(sine / 20))) * ang(rd(0), rd(0), rd(0)), animsped)
        lerpz(N, "C0", NC0 * cf(0, 0, -(0.1 * cos(sine / 40))) * ang(rd(4 + 2 * cos(sine / 20)), rd(0), rd(0)), animsped)
        lerpz(RS, "C0", RSC0 * cf(0, 0, 0) * ang(rd(8 * cos(sine / 80)), rd(0), rd(8 * cos(sine / 80))), animsped)
        lerpz(RS, "C1", RSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), animsped)
        lerpz(LS, "C0", LSC0 * cf(0, 0, 0) * ang(rd(8 * cos(sine / 80)), rd(0), rd(8 * cos(sine / 80))), animsped)
        lerpz(LS, "C1", LSC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), animsped)
        lerpz(RH, "C0", RHC0 * cf(0, (0.1 * cos(sine / 40)), 0) * ang(rd(-5), rd(-5), rd(1)), animsped)
        lerpz(RH, "C1", RHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), animsped)
        lerpz(LH, "C0", LHC0 * cf(0, (0.1 * cos(sine / 40)), 0) * ang(rd(-5), rd(5), rd(1)), animsped)
        lerpz(LH, "C1", LHC1 * cf(0, 0, 0) * ang(rd(0), rd(0), rd(0)), animsped)
        else
          if Torsovelocity > 2 then
            Anim = "Walk"

			end
          end
        end
      end
    end
	end)
