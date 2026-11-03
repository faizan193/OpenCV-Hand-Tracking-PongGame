# OpenCV_Projects 
OpenCV projects like Face Recognition, Item Detection, Hand Tracking, Human Detection and more.
<br/>

## Setup

Use Python 3.12 and install the project dependencies from the project folder:

```powershell
py -3.12 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

In VS Code, select `.venv` with **Python: Select Interpreter**. To start the Pong hand-tracking demo from the project folder:

```powershell
python .\HandTracking\PongGame\PongGame.py
```

To browse and launch the available demos from a menu, run:

```powershell
python .\main.py
```

Choose a demo by its number, then close it to return to the menu. Run demos one at a time; many use the same webcam or other system resources.

### FM BALL GAME controls

Start `HandTracking\PongGame\PongGame.py`. The game opens at its main menu and does not begin a match until you click **START GAME**. Choose a game mode and difficulty first; pressing Enter does not start a match. The menu uses aligned, equal-size buttons, and the result screen offers **PLAY AGAIN** and **MAIN MENU**. **Settings** opens a separate page for audio, camera, preview, hand-sensitivity, contrast, calibration, ball-skin, **TOTAL GAME TIME**, and **CONTROLS**. The Controls page lets you choose Hand Controller, Mouse Control, or Keyboard Control, then return to Settings with **BACK TO SETTINGS**. Set hours, minutes, and seconds on the time page; the selected duration applies to every mode and is saved between runs. The in-game timer pauses and resumes with the match. From a match, **BACK TO GAME** resumes play. The arena background is drawn by the game and does not rely on a stock image. The **How to Play** screen shows the control guide and identifies each side, and **High Scores** displays local summary tiles and per-mode match records.

During a match, the scoreboard labels the computer's right-hand paddle **COMPUTER** in VS COMPUTER and TIME ATTACK modes. In two-player mode it shows **PLAYER 2**; in practice mode the right-side wall is labeled **WALL**. Each player's score is shown in a card aligned with their side of the court.

During a match, select Hand Controller, Mouse Control, or Keyboard Control in Settings > Controls. Hand Control uses webcam hand motion; Mouse Control follows the mouse pointer or scroll wheel; Keyboard Control uses W/S for Player 1 and I/K for Player 2. The round **X** button in the top-right closes the game.

The Pong window supports these keyboard controls:

- `1`: play against the computer; `2`: two-player hand tracking; `3`: practice; `4`: time attack.
- `E`, `M`, or `H`: set the computer difficulty to easy, medium, or hard.
- `[` and `]`: decrease or increase the points needed to win.
- In Keyboard Control, `W`/`S` moves Player 1's paddle and `I`/`K` moves Player 2's paddle.
- In Mouse Control, move the mouse over the court or scroll the wheel; in two-player mode, use the left or right half for the corresponding paddle.
- Click the **PAUSE** and **RESUME** buttons or press `P` to pause/resume; `R` restarts; `Esc` returns to the main menu. Press `Esc` again from the main menu to quit.
- `C`: switch camera; `V`: show/hide the camera preview; `B`: calibrate hand range for five seconds; `,`/`.`: decrease/increase hand sensitivity; `G`: toggle high-contrast display.

The Settings gear also adjusts music and sound-effect volume, camera, camera preview, hand sensitivity, contrast, and starts hand calibration. Game mode, difficulty, point target, total game time, selected control method, volume, camera, calibration, preview, and accessibility preferences are saved in the current user's local application-data folder; match results and high scores are stored separately there. Neither is saved to the installation directory.

Ball movement is scaled to elapsed time, with long frame stalls capped, and hand positions are smoothed to reduce jitter. If no camera is available, the game displays a warning and can be played with the mouse or keyboard. Hand tracking runs locally using the bundled MediaPipe model.

Face-recognition demos need the additional `face-recognition` package. Install it with `python -m pip install -r requirements-face-recognition.txt`. On Windows, its `dlib` dependency may need extra build tools if no compatible wheel is available.

The camera demos need a working camera. For network-camera demos, enter the complete stream URL when prompted.

## Download the latest revision
```
# Download using this code:

git clone https://github.com/muki01/OpenCV_Projects.git
```

## :scroll: Changelog
OpenCV_Projects gets updates with new features, improvements, and bugfixes.
Be sure to check out the [changelog here]().

## Check out all the photos below
