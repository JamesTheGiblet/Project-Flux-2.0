🚀 Project Flux 2.0: The System is the Game

Hackable. Modular. Yours. Every line of code is an invitation.

Welcome to Flux 2.0, the evolution of the Sovereign Engine. Where the first version proved a game could be hackable, Flux 2.0 makes the hacking the game itself. We've moved beyond a single game with a mod panel and have rebuilt the foundation to be a true, community-ready platform for creativity.

This isn't just a game engine; it's a living manifesto for digital sovereignty. We believe software should be transparent, modifiable, and truly owned by its users. Flux 2.0 is the embodiment of that belief. No gatekeepers, no black boxes—just pure creative freedom.
✨ What is Flux 2.0?

Flux 2.0 is a complete architectural and philosophical evolution. We have rebuilt the system on three core pillars:

    A True Modular Ecosystem: The engine (flux-core) is now completely separate from its content (flux-mods). Weapons, enemies, game rules, and player classes are now "Mod Packs"—self-contained folders that the core engine discovers and loads at runtime. This means you can add, remove, or create entire content packages just by managing folders.

    Robust Sandbox Environment: Your creativity should never be punished by a crash. All user-written code is now validated in a secure background Web Worker. This sandbox prevents syntax errors, infinite loops, and other common mistakes from ever freezing the main game. If your code is broken, we tell you why, without interrupting your experience.

    A Complete Modder Workflow: We have built a full suite of tools for a seamless creative process. Save your custom mods to your browser's local storage, build a personal library, delete old versions, and—most importantly—share your creations with anyone, anywhere, using a simple import/export string.

🚀 Getting Started

Getting the Flux 2.0 ecosystem running on your local machine is simple.
1. Clone the Repository

You'll need git installed.

git clone [https://github.com/your-username/project-flux.git](https://github.com/your-username/project-flux.git)
cd project-flux

2. Run a Local Server

The engine is designed to be run from any simple HTTP server. If you have Python 3, this is the easiest way:

# Navigate to the flux-core directory
cd flux-core

# Start the server
python -m http.server 8000

If you have Node.js, you can use npx serve.
3. Open in Browser

Open your web browser and navigate to http://localhost:8000. The Flux 2.0 client will load, discover all available mod packs, and be ready for you to play and create.
🛠️ The Modding Workflow

The mod panel is your creation hub. Here’s how to get started on your first custom mod.

    Select a Mod Type: Choose a section, like 🔫 WEAPON MOD.

    Load a Preset: Use the dropdown to select a base mod, like Shotgun. The code will instantly appear in the editor. This is the best way to learn.

    Hack Away: Modify the code. For example, change the pelletCount from 8 to 20, or change the spread to 1.5 for a ridiculously wide blast.

    Apply Your Changes: Click Apply Weapon. The sandbox will instantly validate your code. If it's safe, the mod will be applied to your ship in real-time. If there's an error, a notification will appear, and the error will be printed to your browser's console.

    Save Your Creation: If you love your new "Super-Spreader 2000", type a name into the "Save as..." input box and click 💾 Save. Your mod is now permanently saved and will appear in the dropdown with a [C] prefix for "Custom".

    Share with the World: Click 📤 Export. The entire code for your mod will be copied to your clipboard as a compressed string. Paste this string in a message to a friend.

    Import a Friend's Mod: Click 📥 Import and paste a string your friend sent you. Their mod will instantly load into your editor, ready to be applied and saved.

📦 Creating Your First Mod Pack

Ready to contribute to the ecosystem? You can create your own collection of mods that the engine will automatically discover.
1. Create Your Pack Folder

Inside the flux-mods/ directory, create a new folder. It must be uniquely named, for example: my-awesome-pack.
2. Create a Manifest

Every mod pack must have a manifest.json file at its root. This file tells the Flux Core engine what mods are inside.

Example flux-mods/my-awesome-pack/manifest.json:

{
    "weapon": {
        "Laser Beam": "laser-beam.js",
        "Charge Cannon": "charge-cannon.js"
    },
    "rule": {
        "Sudden Death Mode": "sudden-death.js"
    }
}

    The top-level keys (weapon, rule) must match the categories defined by the engine.

    The values are the relative paths to your mod files within your pack's folder.

3. Add Your Mod Files

Create the .js files you defined in your manifest. For example, create laser-beam.js inside my-awesome-pack/.

Example flux-mods/my-awesome-pack/laser-beam.js:

function(player, target, engine) {
    // Your awesome laser beam logic here!
    engine.projectiles.push({
        /* ... */
    });
}

4. Run the Game

That's it! The next time you load flux-core/index.html, the mod loader will automatically discover my-awesome-pack, read its manifest, and your "Laser Beam," "Charge Cannon," and "Sudden Death Mode" mods will appear in the appropriate dropdowns, ready to be used.
🔮 The Praximous Vision: The Future of Flux

Our foundation is built. Our systems are robust. The Praximous business plan now calls for the most exciting phase: making the system the game.

Future development will focus on:

    Mods as In-Game Loot: Enemies will drop code fragments that can be combined on the fly.

    The JIT (Just-In-Time) Compiler: A gameplay mechanic where players risk compiling unstable, temporary mods in the heat of battle.

    The Black Market: An in-game hub for browsing and "installing" mods from the community, powered by the import/export string system.

🤝 Contributing

The easiest way to contribute is to create a Mod Pack! Build a cool set of weapons, a new game mode, or a challenging new enemy pack. If you want to contribute to the core engine itself, please open an issue on GitHub to discuss your proposed changes.
📄 License

Project Flux 2.0 is released under the MIT License. For full details, see the LICENSE file.
