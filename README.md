# Roblox Player Noclip Script

A server-side script that allows all players to pass through each other while maintaining collision with terrain, walls, and other objects.

## 🎮 Features

- ✅ Players can walk through each other (noclip between players)
- ✅ Players still collide with terrain, walls, and objects
- ✅ Automatic setup for all players (existing and new)
- ✅ Handles respawning automatically
- ✅ Works with accessories and tools
- ✅ Server-authoritative (no exploits possible)
- ✅ Visible to all players (not client-side only)

## 📦 Installation

1. Open your Roblox Studio project
2. Navigate to **ServerScriptService** in the Explorer window
3. Create a new **Script** (not LocalScript)
4. Copy and paste the code from `PlayerNoclipScript.lua`
5. Save and test!

## 🚀 Usage

The script works automatically once placed in ServerScriptService. No additional configuration needed!

### Testing

1. Click **Play** → **Local Server**
2. Set **Number of Players** to 2 or more
3. Click **Start**
4. Try walking through other players - they should pass through!
5. Try colliding with walls/terrain - collision should work normally

## 🔧 How It Works

The script uses Roblox's PhysicsService to create custom collision groups:

1. Creates a collision group called "Players"
2. Sets Players group to NOT collide with other Players
3. Sets Players group to collide with Default group (terrain, walls, objects)
4. Automatically assigns all player character parts to the Players group

## 📋 Requirements

- Roblox Studio
- Server-side script execution
- Must be placed in **ServerScriptService**

## ⚙️ Configuration

No configuration required! The script works out of the box.

If you need to modify collision behavior, edit these constants:

```lua
local PLAYER_COLLISION_GROUP = "Players"
local DEFAULT_COLLISION_GROUP = "Default"
```

## 🐛 Troubleshooting

| Issue | Solution |
|-------|----------|
| Script doesn't work | Ensure it's in **ServerScriptService** as a **Script** (not LocalScript) |
| Players still collide | Check Output window for error messages |
| Warnings appear | Character may load too quickly, script will retry setup automatically |

## 📝 Notes

- This is a **server-side** script, preventing client-side exploits
- All players will see the noclip effect
- Compatible with all Roblox character types
- Works with R6 and R15 rigs

## 📄 License

MIT License - Feel free to use in your projects!

## 👤 Author

**ItoRenz00**

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

## ⭐ Support

If this script helped you, please consider giving it a star on GitHub!

---

**Version:** 1.0.0  
**Last Updated:** November 2025
