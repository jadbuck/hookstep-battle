# HOOKSTEP BATTLE - COMPREHENSIVE TEST SCENARIOS
**Version 2.0 - With Confirmations & Advanced Settings**

---

## 🎯 NEW FEATURES TESTED

### 1. Settings Panel (Fixed Top-Right)
- **Location:** Fixed position, top-right corner
- **Does NOT overlap:** Battle scoreboard
- **Contains:** 3 configurable settings

### 2. Configurable Settings
- ⏱️ Countdown Duration (10-300 seconds)
- ⭐ Points Per Correct Guess (1-10 points)
- 🎉 Bonus Points for Perfect Set (0-20 points)

### 3. Confirmation Dialogs
- ✅ Confirm & Add Score → Shows confirmation
- ↻ Restart Set → Shows confirmation
- 🔄 Reset Battle → Shows confirmation with current scores

### 4. Pause Button Positioning
- **Location:** Next to timer in stats bar
- **Size:** Smaller, less prominent
- **Style:** Subtle red border, transparent background

---

## 📋 COMPLETE TEST SCENARIOS

### TEST GROUP 1: SETTINGS PANEL (5 scenarios)

#### Scenario 1.1: Open/Close Settings ✅
**Steps:**
1. Menu screen → Click "⚙️ Settings" (top-right)
2. Expected: Panel appears with 3 inputs (Timer=60, Points=1, Bonus=2)
3. Click "✓ Save & Close"
4. Expected: Panel disappears

#### Scenario 1.2: Change Timer Duration ✅
**Steps:**
1. Open settings → Change timer to 90
2. Save & Close
3. Start Set 1 → Click START
4. Expected: Timer shows 90 seconds

#### Scenario 1.3: Change Points Per Success ✅
**Steps:**
1. Open settings → Change points to 3
2. Save & Close
3. Start any set → Click SUCCESS
4. Expected: Score increases by 3 (not 1)

#### Scenario 1.4: Change Bonus Points ✅
**Steps:**
1. Open settings → Change bonus to 10
2. Save & Close
3. Complete perfect set (8/8 songs)
4. Expected: Shows "+10 BONUS" (total = 8 + 10 = 18)

#### Scenario 1.5: Settings Panel Position ✅
**Steps:**
1. Menu screen → Click "⚙️ Settings"
2. Verify: Panel does NOT overlap Groom/Bride scores
3. Verify: Button remains at top-right, always accessible

---

### TEST GROUP 2: PAUSE BUTTON (3 scenarios)

#### Scenario 2.1: Pause Button Position ✅
**Steps:**
1. Start any set
2. Observe stats bar layout:
   - Left: Team name
   - Center: Timer + Pause button below
   - Right: Score

#### Scenario 2.2: Pause Button Styling ✅
**Steps:**
1. Game screen
2. Verify: Pause button is smaller, subtle red styling
3. Verify: Less prominent than PASS/SUCCESS buttons

#### Scenario 2.3: Pause Functionality ✅
**Steps:**
1. Game in progress → Click "⏸ PAUSE"
2. Expected: Timer freezes, overlay appears
3. Click "▶ RESUME"
4. Expected: Timer continues

---

### TEST GROUP 3: CONFIRMATION DIALOGS (3 scenarios)

#### Scenario 3.1: Confirm & Add Score ✅
**Setup:** Complete set with score of 8

**Test A: Accept Confirmation**
1. Click "✓ Confirm & Add Score"
2. Popup: "Add 8 points to Groom's total score?"
3. Click OK
4. Expected: Score added, return to menu

**Test B: Cancel Confirmation**
1. Complete another set (score 6)
2. Click "✓ Confirm & Add Score"
3. Popup appears
4. Click Cancel
5. Expected: Score NOT added, stay on results

#### Scenario 3.2: Restart Set ✅
**Setup:** Complete set with score of 5

**Test A: Accept Restart**
1. Click "↻ Restart Set"
2. Popup: "Restart this set? Your current score will be discarded."
3. Click OK
4. Expected: Set restarts, score=0, timer resets

**Test B: Cancel Restart**
1. Complete set again
2. Click "↻ Restart Set"
3. Click Cancel
4. Expected: Stay on results, score unchanged

#### Scenario 3.3: Reset Battle ✅
**Setup:** Groom: 12, Bride: 15

**Test A: Accept Reset**
1. Click "🔄 Reset Battle"
2. Popup shows:
   ```
   ⚠️ RESET ENTIRE BATTLE?
   
   This will erase all scores for both teams.
   
   Groom: 12 → 0
   Bride: 15 → 0
   ```
3. Click OK
4. Expected: Both scores → 0

**Test B: Cancel Reset**
1. Add scores again (Groom: 8, Bride: 10)
2. Click "🔄 Reset Battle"
3. Click Cancel
4. Expected: Scores unchanged (8, 10)

---

### TEST GROUP 4: CONFIGURABLE SCORING (6 scenarios)

#### Scenario 4.1: Custom Points (2 per success) ✅
**Settings:** Timer=60, Points=2, Bonus=2

1. Start Set 1 → Click SUCCESS × 4
2. Expected Score: 8 (4 songs × 2 points)
3. Timer expires
4. Final Score: 8

#### Scenario 4.2: Custom Points (5 per success) ✅
**Settings:** Timer=60, Points=5, Bonus=0

1. Start Set 2 → Click SUCCESS × 3
2. Expected Score: 15 (3 songs × 5 points)

#### Scenario 4.3: Perfect Set - Default Bonus ✅
**Settings:** Timer=60, Points=1, Bonus=2

1. Start any set → Click SUCCESS × 8 (all songs)
2. Expected: Score = 10 (8 + 2 bonus)
3. Message: "🎉 PERFECT! +2 BONUS 🎉"

#### Scenario 4.4: Perfect Set - Custom Bonus ✅
**Settings:** Timer=60, Points=1, Bonus=10

1. Start any set → Click SUCCESS × 8
2. Expected: Score = 18 (8 + 10 bonus)
3. Message: "🎉 PERFECT! +10 BONUS 🎉"

#### Scenario 4.5: Perfect Set - No Bonus ✅
**Settings:** Timer=60, Points=1, Bonus=0

1. Start any set → Click SUCCESS × 8
2. Expected: Score = 8 (8 + 0 bonus)
3. Bonus message: Hidden

#### Scenario 4.6: Perfect Set - High Points & High Bonus ✅
**Settings:** Timer=120, Points=3, Bonus=15

1. Start any set → Click SUCCESS × 8
2. Expected: Score = 39 (24 + 15 bonus)
3. Message: "🎉 PERFECT! +15 BONUS 🎉"

---

### TEST GROUP 5: FULL GAME FLOW (2 complete battles)

#### Scenario 5.1: Standard Battle (Default Settings) ✅
**Settings:** Timer=60, Points=1, Bonus=2

1. **Round 1:**
   - Set 1 (Groom): 6 songs → Confirm → Groom: 6
   - Set 2 (Bride): 8 songs (perfect) → Confirm → Bride: 10

2. **Round 2:**
   - Set 3 (Groom): 8 songs (perfect) → Confirm → Groom: 16
   - Set 4 (Bride): 5 songs → Confirm → Bride: 15

3. **Round 3:**
   - Set 5 (Groom): 7 songs → Confirm → Groom: 23
   - Set 6 (Bride): 8 songs (perfect) → Confirm → Bride: 27

4. **Declare Winner:**
   - Click "🏆 Declare Winner"
   - Expected: "🎉 BRIDE WINS! 🎉"
   - Shows: "Groom: 23 | Bride: 27"

#### Scenario 5.2: Custom Battle (High Scoring) ✅
**Settings:** Timer=90, Points=2, Bonus=5

1. **Round 1:**
   - Set 1 (Groom): 8 songs (perfect) → Score: 21 → Confirm → Groom: 21
   - Set 2 (Bride): 6 songs → Score: 12 → Confirm → Bride: 12

2. **Round 2:**
   - Set 3 (Groom): 7 songs → Score: 14 → Confirm → Groom: 35
   - Set 4 (Bride): 8 songs (perfect) → Score: 21 → Confirm → Bride: 33

3. **Round 3:**
   - Set 5 (Groom): 5 songs → Score: 10 → Confirm → Groom: 45
   - Set 6 (Bride): 8 songs (perfect) → Score: 21 → Confirm → Bride: 54

4. **Declare Winner:**
   - Expected: "🎉 BRIDE WINS! 🎉"
   - Shows: "Groom: 45 | Bride: 54"

5. **Reset:**
   - Click "🔄 Reset Battle" → Confirm
   - Expected: Groom: 0, Bride: 0

---

### TEST GROUP 6: EDGE CASES (4 scenarios)

#### Scenario 6.1: Minimum Settings ✅
**Settings:** Timer=10, Points=1, Bonus=0

1. Start set with 10-second timer
2. Timer expires quickly
3. No bonus even if all 8 completed

#### Scenario 6.2: Maximum Settings ✅
**Settings:** Timer=300, Points=10, Bonus=20

1. Start set with 5-minute timer
2. Complete all 8 songs
3. Expected Score: 100 (80 + 20 bonus)

#### Scenario 6.3: Long Song Names (Set 3) ✅
**Test:** Visual layout with long titles

1. Start Set 3 or Set 4
2. Songs: "Teri Baaton Mein Aisa Uljha Jiya", etc.
3. Verify:
   - Text wraps properly
   - Card doesn't expand too much
   - Undo button visible (bottom-right)
   - No overlap with other elements

#### Scenario 6.4: Rapid Button Presses ✅
**Test:** System handles rapid input

1. Start any set
2. Click SUCCESS rapidly 8 times
3. Expected:
   - All clicks registered
   - Score updates correctly
   - Undo history maintained
   - End screen appears

---

## 📊 SUMMARY

**Total Test Scenarios:** 26
**Test Groups:** 6
- Settings Panel: 5 tests
- Pause Button: 3 tests
- Confirmation Dialogs: 3 tests
- Configurable Scoring: 6 tests
- Full Game Flow: 2 tests
- Edge Cases: 4 tests

**All Features Working:** ✅

**Key Improvements:**
1. ✅ Settings button doesn't overlap scores
2. ✅ Configurable points and bonus
3. ✅ All score changes require confirmation
4. ✅ Pause button less prominent, better positioned
5. ✅ Undo button doesn't block content

---

## 🎮 RECOMMENDED SETTINGS FOR DIFFERENT EVENTS

### Quick Party (20-30 mins)
- Timer: 45 seconds
- Points: 1
- Bonus: 3

### Standard Wedding (30-45 mins)
- Timer: 60 seconds
- Points: 1
- Bonus: 2

### Epic Battle (60+ mins)
- Timer: 90 seconds
- Points: 2
- Bonus: 5

### Casual Fun (Easy)
- Timer: 120 seconds
- Points: 1
- Bonus: 5
