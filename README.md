# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [ ] The purpose of this game is for the user to guess the secret value.
- [ ] Two bugs were found:
      1. Attempts allowed was not equal to the attempts left.
      2. The hints were wrong.
- [ ] The solution applied to the first bug was that in the code block ' if "attempts" not in st.session_state:
    st.session_state.attempts = 0', st.session_state.attempts was at first set to 1 which is what caused the inconsistency in the number of attempts that the user had, so instead I set it to 0. To continue, for the second bug the solution applied was simply switching the return logic within the check_guess function. So if it said "Go LOWER", it was changed to "Go HIGHER" and vice versa.
## 📸 Demo Walkthrough

Describe your fixed game in numbered steps so a reader can follow along without watching a video:

1. User types in a number in the input field under "Enter your guess:"
2. Once the user has decided on a guess, click Submit guess
3. The game will provide a hint - "Go HIGER" or "Go LOWER"
4. The user uses the hint to continue guessing
5. Repeat steps 3 and 4 until user is correct or user runs out of attempts and click new game to generate a new game

**Screenshot** *(optional)*: <!-- Insert a screenshot of your fixed, winning game here -->

## 🧪 Test Results

```
# Paste your pytest output here, e.g.:
# pytest tests/
# ========================= X passed in 0.XXs =========================
```

## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, describe the Enhanced UI changes here — a screenshot is optional]
