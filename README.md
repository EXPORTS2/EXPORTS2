local function Invite()
  local req = syn.request or http_request or request or http.request or nil
  if req ~= nil then
    for port=6463, 6472, 1 do
      local inv = "http://127.0.0.1:"..tostring(port).."/rpc?v=1"
      local http = game:GetService("HttpService")
      local t = {cmd = "INVITE_BROWSER", args = {["code"] = "Export HUB"}, nonce = string.lower(http:GenerateGUID(false))}
      local post = http:JSONEncode(t)
      req({Url = inv, Method = "POST", Body = post, Headers = {["Content-Type"] = "application/json", ["Origin"] = "https://discord.com"}})
    end
  end
end

local discordinv = "https://discord.gg/WFDfZKekzW"
local d
local f = pcall(function()
    d = game:HttpGet("https://raw.githubusercontent.com/Forgxtten/Phantom-Hub/main/Supported%20Games/"..game.PlaceId..".lua")
end)
if f == true then
    loadstring(d)()
else
    game.Players.LocalPlayer:Kick("Game Not Supported Or Patched Join Discord Server For The Updates! Invite link Is Copied To Clipboard. "..discordinv)
    Invite()
    setclipboard(discordinv)
endlocal function Invite()
  local req = syn.request or http_request or request or http.request or nil
  if req ~= nil then
    for port=6463, 6472, 1 do
      local inv = "http://127.0.0.1:"..tostring(port).."/rpc?v=1"
      local http = game:GetService("HttpService")
      local t = {cmd = "INVITE_BROWSER", args = {["code"] = "phantomhub"}, nonce = string.lower(http:GenerateGUID(false))}
      local post = http:JSONEncode(t)
      req({Url = inv, Method = "POST", Body = post, Headers = {["Content-Type"] = "application/json", ["Origin"] = "https://discord.com"}})
    end
  end
end

local discordinv = "https://discord.gg/WFDfZKekzW"
local d
local f = pcall(function()
    d = game:HttpGet("https://raw.githubusercontent.com/Forgxtten/Phantom-Hub/main/Supported%20Games/"..game.PlaceId..".lua")
end)
if f == true then
    loadstring(d)()
else
    game.Players.LocalPlayer:Kick("Game Not Supported Or Patched Join Discord Server For The Updates! Invite link Is Copied To Clipboard. "..discordinv)
    Invite()
    setclipboard(discordinv)
end
