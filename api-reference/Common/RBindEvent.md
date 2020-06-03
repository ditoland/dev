# **RBindEvent**

| **유저가 작성한 Lua 함수를 연결, 특정 상황에 연결된 함수를 호출해 주는 객체에요.** |
## **함수**

| **bool Connect(LuaScriptFunction Function)** |
| :--- |
| **작성한 Lua 함수를 해당 이벤트에 연결하는 함수** |
## **샘플**

```lua
local function EnterPlayer (Player)
	Logger:Log(“Hello”)
end

-- Game.OnEnterPlayer가 RBindEvent을 리턴
Game.OnEnterPlayer:Connect(EnterPlayer)	 
```