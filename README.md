# Overwatch 2 Colorbot (Unibot-based)

Hey everyone. This is a little project I'm working on, built on top of [Unibot](https://github.com/vike256/Unibot) by vike256. The idea is to have a pre-configured base for Overwatch 2, so you don't have to spend hours tweaking color values and FOV from scratch.

## What is this?

It's a colorbot. It doesn't touch the game's memory. It just reads the screen, finds enemy outlines by color, and moves the mouse toward them. That's it.

I set it up to aim at the **magenta** outline, since that's the color I found easiest to work with in OW2. I also made the aim smooth and chest-level, so it doesn't look like one of those blatant aimbots that locks onto the head.

## Current Config

The `config.ini` already has the values I use. If you want to change anything, just edit it and hit F1.

- `aim_smoothing_factor = 0.75`
- `speed = 0.7`
- `aim_height = 0.3`
- `lower_color = 140, 240, 200`
- `aim_fov_x = 96`, `aim_fov_y = 96`
- `aim_keys = 0x02` (right mouse button)

The triggerbot is off (`trigger_delay = 9999`). I don't like the idea of letting the bot shoot on its own. I prefer to click.

## Known Issues (Still Working On It)

I'm not gonna pretend everything is perfect. Some stuff is still buggy:

- **Aiming at names:** sometimes Unibot gets confused and aims at the player's name instead of the body. The fix I found was to disable name display in the game.
- **Resolution:** this config is calibrated for **1440x1080**. If you use a different resolution, you'll need to change `resolution_x` and `resolution_y`.
- **False positives:** if there's any magenta effect on screen, the bot can get lost. Increasing the saturation on `lower_color` helps.
- **Stability:** depends on the map and character skins. It's not always perfect.

## How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/your-username/overwatch2-colorbot.git

2. Install dependencies:

       pip install -r requirements.txt

3. Configure the game:

- Turn on Color Blind mode and pick Magenta for Enemy UI.

- Disable enemy names (if you can).

- Set the game to Borderless Windowed.

4. Run it:

       cd src
       python main.py

5. Enjoy :D

Hit F2 to toggle the aimbot and hold right mouse button to use it.

## Warning

This is at your own risk. It's a cheat, it violates the game's terms, and it can get you permanently banned, including your hardware. I'm not responsible for anything. Use a secondary account and don't cry my dm pls
