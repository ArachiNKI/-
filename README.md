# -
скрипт роблокс, который дает команду трем кубам подниматься вверх\вниз с помощью fps
1/ делаем новый проект в Роблоксе.
2/ делаем три куба и даем им имена: 'a' 'b' 'c'
3/ делаем внутри их скрипты:
  --скрипт на куб 'a' - воспроизводит 30 fps
  local a_block = game.Workspace.a --делаем локальную переменую a_block, помещаем в нее наш куб(обьект) под названием "a"
a_block.Anchored = true -- закрепляем его в пространстве
while true do -- Мы сделали бесконечный цикл
	wait(1);
	a_block.Position = a_block.Position + Vector3.new(0,10,0);
	wait(1);
	a_block.Position = a_block.Position - Vector3.new(0,10,0);
end


--скрипт куба 'b' - воспроизводит 60fps
local b_block = game.Workspace.b --делаем локальную переменую a_block, помещаем в нее наш куб(обьект) под названием "a"
b_block.Anchored = true -- закрепляем его в пространстве
while true do -- Мы сделали бесконечный цикл
	for i = 1,10 do
		wait(0.01);
		b_block.Position = b_block.Position + Vector3.new(0,1,0);
		wait(0.01);
		b_block.Position = b_block.Position + Vector3.new(0,1,0);
	end
	for i = 1,10 do
		b_block.Position = b_block.Position - Vector3.new(0,1,0);
		wait(0.01);
		b_block.Position = b_block.Position - Vector3.new(0,1,0);
		wait(0.01)
	end
end



--скрипт куба 'c' - воспроизводит 120 fps
local c_block = game.Workspace.c --делаем локальную переменую a_block, помещаем в нее наш куб(обьект) под названием "a"

c_block.Anchored = true -- закрепляем его в пространстве
while true do -- Мы сделали бесконечный цикл
	for i = 1,10 do
		wait(0.01);
		c_block.Position = c_block.Position + Vector3.new(0,0.3,0);
		wait(0.01);
		c_block.Position = c_block.Position + Vector3.new(0,0.3,0);
	end
	for i = 1,10 do
		c_block.Position = c_block.Position - Vector3.new(0,0.3,0);
		wait(0.01);
		c_block.Position = c_block.Position - Vector3.new(0,0.3,0);
		wait(0.01)
	end
end
