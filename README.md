# Mining-Pro
local Back = 1
local success, down = turtle.inspectDown()
  local depth = 0
  for x = 1,8 do
  turtle.dig()
  turtle.forward()
  Back = Back + 1
  end  
for x = 1,5 do
  while down.name ~= "minecraft:bedrock" do
    turtle.digDown()
    turtle.down()
    sucess,down = turtle.inspectDown()  
    depth = depth + 1
    Back = Back + 1
  end  
  for x = 1,depth do
    turtle.up()
    depth = depth -1
  end
  turtle.dig()
  turtle.forward()
  sucess,down = turtle.inspectDown()
end
for x = 1, Back do
  turtle.back()
end
local function PutAway()
  for inventory = 1,16 do
    turtle.select(inventory)
    turtle.dropDown()
  end
end
PutAway()
