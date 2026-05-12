First-time setup
Grant GPS permission
When you first open LINKS, Safari asks:

"links-golf.github.io" Would Like to Use Your Location

Tap Allow While Using App. If you tap Don't Allow by mistake:
Settings → Privacy & Security → Location Services → Safari → While Using the App
Golfer profile
The opening screen sets up your avatar for the shot animations:

Height — adjust with the slider (5'0" to 7'0")
Dominant hand — Left or Right
Build — Slim / Average / Stocky

Tap Build My Avatar → when done. You can change these any time from the settings gear on the main tracker.
Select a course
Five courses are built in: Augusta National, Pebble Beach, St Andrews (Old Course), TPC Sawgrass, and Torrey Pines South.
To search 40,000+ real courses:

Tap the Live Data toggle (top right of course select screen)
Get a free API key at golfcourseapi.com — it takes 2 minutes
Paste the key and tap Connect & Test
Search any course by name

Using the tracker on the course
Before you tee off
Open LINKS while still at the clubhouse or car park. This gives the GPS chip time to get a solid fix before you reach the first tee. Watch for the GPS indicator to show ±8m or better — that's when you're ready.
Starting a hole

Stand on the tee box
Tap ⛳ Track
Your gold dot appears on the hole map at the tee position
Hit your shot and walk toward the ball

Shot detection
The app watches your GPS position every second. When you stop moving (less than 3 metres of movement over 3+ seconds), a countdown ring appears with options:
OptionWhen to useLog NowYou just hit — tap this immediately, don't waitLet the timer runYou want fully hands-free loggingNot a shotYou stopped to check the yardage, wait for others, look at the scorecard

Tip: Tapping Log Now right after impact is the most reliable workflow. The auto-detection is a backup, not a requirement.

Logging a shot
The shot modal has two selections:
Trajectory — determines the ball flight arc drawn on the map:
TrajectoryBall flightBest forHighSteep, soft landingFull irons, lob wedgeLine DrivePenetrating, lower apexDriver, 3-woodLow PunchKnockdown, runningInto wind, punch from roughBump & RunMostly groundChip, bump from fringe
Club — Driver, 3W, 5W, 3H, 4–9 iron, PW, GW, SW, LW, PT
Tap LOG SHOT — the tracer animates on the map and the shot saves immediately to local storage.
Putting
After your last approach shot, a putt prompt appears. The app suggests a putt count based on your approach distance and club:

Close chip (under 30y ground shot) → suggests 1 putt
Short lofted approach (under 50y) → suggests 1 putt
Greenside regulation → suggests 2 putts
Very long approach (over 120y) → suggests 3 putts

Select your actual putt count, confirm whether you hit the Green in Regulation (GIR), then tap Confirm Putts.
Tap Next Hole → to advance.
Map camera modes
Four views, switchable anytime during tracking:
ModeWhat you're looking atBehindOver-the-shoulder perspective from your ball looking toward the pin. Fairway corridor, bunkers, water, and the green scale with distance and disappear when you've passed them.AerialTop-down view zoomed to your exact window — ball at the bottom, pin at the top. Shows only what's ahead. A bunker 300 yards from the hole won't appear if you're 140 yards out.SideBroadcast TV angle. Shows terrain elevation, full predicted arc, apex height in feet, bunker cross-sections.Full HoleAll shots on this hole simultaneously, with club and distance labels.
Timer settings
Tap Stop while tracking, then adjust at the bottom of the Stop modal:
TimerBest for10sFast players, riding carts30sNormal walking pace (default)60sSlow groups, you want time to think2minYou always tap Log Now manually
Pin drops
Tap 📍 then tap anywhere on the map to place a named pin. Use this to manually mark a landing spot if your GPS dot doesn't quite match where the ball is.
Hole navigation
The hole strip runs across the top of the map. Tap any hole pill to jump — if you have unsaved putts on the current hole, the app prompts you before switching.
Stopping early
Tap Stop → Confirm Stop. If you have shots logged but no putts yet, the putt modal opens automatically so you don't lose the scoring data.

Scorecard
Tap 📊 (bottom right of tracker) at any time:

Live score vs par, color-coded: red eagle/birdie, white par, blue bogey, purple double+
Total putts and GIR count
Running +/− against par
Tap any hole row to expand: shows each shot with club, yardage, and trajectory indicator


Round replay
Open LINKS Replay from your home screen after the round.
Loading a round
The opening screen shows:

Demo Rounds — Augusta National and Pebble Beach 9-hole demos, pre-loaded and ready to play
Simulate a Random Round — generates a plausible randomized 9-hole round with real hole shapes

(Exporting your tracked round into the replay is on the roadmap — for now, the replay uses demo data or simulated rounds.)
Playback controls
ControlFunction▶ / ⏸Play / pause⏮ ⏭Previous / next shot⏪Restart current shot from addressSpeed (tap)Cycle: 0.25× → 0.5× → 1× → 1.5× → 2×Progress barTap to jump, drag to scrubShot stripTap any numbered tile to jump to that shot📋Round summary📷Cycle cameras
Camera modes (replay)
CameraDetailAerialTop-down, viewport follows shot — ball lie at bottom, pin at top. Fairway shape, bunkers, and water use the exact bezier geometry of the hole.BehindPerspective from ball looking toward pin. Bunkers and hazards ahead show distance labels (⚠ 85y). Features behind you are culled.SideLeft edge = ball, right edge = pin. Ghost arc shows full predicted flight. Apex height annotated at peak. Terrain elevation profile from geom data.Full HoleStatic aerial of the entire hole. All shots for this hole drawn simultaneously as colored traces with club labels.
Round summary
Opens automatically after the last shot, or tap 📋 at any time:

Score vs par, total shots, total putts
GIR and FIR counts
Per-hole row with colored shot pills and score (+1, E, −1 etc.)


GPS accuracy tips
For best results:

Open the app at the car park, not the tee — gives the chip 5 minutes to warm up
Hold the phone face-up or in a shirt pocket, not a back pocket (your body absorbs signal)
iPhone 12 and newer: expect ±3–6m on open fairways
Older iPhones or heavy tree cover: ±10–20m is normal

The app is designed for real-world GPS:

Fixes worse than ±25m are automatically filtered out
Stop detection uses a 3-metre movement threshold with a 3-second buffer, which handles normal GPS jitter without false triggers
If a fix is weak, the accuracy indicator shows Weak GPS ±20m — you can keep playing and just tap Log Now manually

If your dot is in the wrong spot:

Use 📍 Pin Drop to manually mark the ball position
The dot will self-correct as GPS improves


Offline play
Once installed via GitHub Pages or Netlify and opened at least once on WiFi, LINKS works with zero signal on the course.
Works completely offline:

GPS tracking (the chip is local to your phone)
Shot logging and scoring
Hole navigation
Scorecard
Round replay with demo rounds

Requires a connection:

Live course search (Golf Course API)
Google Fonts on first load (falls back to system serif/sans gracefully)


Resume after interruption
Every shot you log is written to localStorage immediately. If the app closes unexpectedly — battery dies, Safari crashes, you close the tab — your round is safe.
Next time you open LINKS, a Resume Round prompt appears showing which course, how many shots logged, and which hole you were on. Tap Resume Round to pick up exactly where you left off.
Saved rounds are tied to today's date. Opening the app tomorrow starts fresh with no prompt.

Keep the screen awake
LINKS requests a Screen Wake Lock so the display stays on while tracking. This works on iOS 16.4+ with Safari 16.4+. If your phone still goes to sleep:
Settings → Display & Brightness → Auto-Lock → Never
Set it back to your normal setting after the round.

Troubleshooting
"Waiting for GPS…" won't clear
GPS can take 30–60 seconds for a first fix in poor conditions. If it doesn't resolve:

Make sure Location Services is on: Settings → Privacy & Security → Location Services → ON
Make sure Safari has access: Settings → Privacy & Security → Location Services → Safari → While Using the App
Step outside or away from buildings
Fully close and reopen the app

Shot detected when I didn't hit
The 3-second stop buffer handles most false triggers. If it still fires when you stop to read a yardage book, tap Not a shot — the countdown dismisses and tracking resumes. Increasing the timer to 60s or 2min also reduces false positives.
Shot not detected after I hit
The GPS needs to see you moving between shots. If you're in a cart and don't move far enough between stops, tap Log Now manually — it bypasses detection entirely.
GPS dot is far from where I am
GPS drift of 5–15 metres is normal in tree-lined areas or when the signal is bouncing off buildings. Use 📍 Pin Drop to manually place your position on the map.
App closed mid-round and I lost my data
If you installed via GitHub Pages or Netlify (HTTPS), your shots are in localStorage and the Resume prompt will appear when you reopen. If you're running the file locally (file:// URL), localStorage still works but may behave differently per browser.
Service worker not updating
If you update the files on your server but the app still shows the old version: in Safari on iPhone, go to Settings → Safari → Advanced → Website Data, find the domain, and delete it. Then reload.
The hole map doesn't match the real course layout
The hole shapes (fairway curve, bunker positions, green location) are procedurally generated from each hole's par, yardage, and dogleg direction — they're realistic in proportion but not satellite-accurate. Your real GPS position is always accurate; only the background map is approximate.
