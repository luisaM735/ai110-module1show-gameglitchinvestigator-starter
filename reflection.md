# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

The first time the game was ran, at first glance everything looked fine. There were some descrepanices. Two bugs were found in the game. First being that the "attempts allowed" on the left side panel and the "attempts left" in the center main field did not match. The second broken logic was the hints that were given when a user guessed a number, being either "go higher" or " go lower", were backwards.


**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
|Attempts |Attempts should be 8 |Attempts was 7 |Console Ouput: none/ |
|Hints |Hints should be "go higher" if guess is lower than secret value, and "go lower" if the guess is higher |The hints are wrong, they're reversed |Console Ouput: none/ |
|New Game |Resets game | Doesn't generate new secret value nor clear the input value for the user to pplay again |Console Ouput: none/ |

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion you did not accept as written (including what the AI suggested, why you rejected or changed it, and how you verified your version). It does not have to be a suggestion that was wrong: over-engineered, out of scope, harder to read, or a poor fit for this codebase all count.

The AI tool used on this project was Claude.
For instance, when dealing with the reversed hint logic, I provided AI with the relevant code block that was affecting the output, along with some context of what it was doing and what I needed. It then suggested that I simply switch the logic, switch the hint "Go Lower" with "Go Higher" and vice versa. Furthermore, the AI did not provide a suggestion that I did not accept.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

I decided if a bug was really fixed by applying the changes to the code, saving it, refreshing the game, and trying out the use case to see if the result was correct or wrong again. For instance, once I applied the suggested AI solution from claude on my code and saved it, I gave the input a lower number than the secret value to see if the game would output the correct value, then I did the same for an input value higher than the secret value and the output was correct. I did not ask AI to help me design any tests.

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit? 

I would explain Streamlit reruns as a way to see changes made to your code almost immediately. Whenever you interact with the app, such as clicking a button, Streamlit reruns the Python script and updates the output on the website. This allows you to see the results of your interactions. Furthermore, session state allows the app to remember information, such as a score or user input, between reruns. It is essentiallt the last state the session was in.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.


One strategy I would would want to reuse in future labs or projects is marking the "crime scene" in my code to tell AI explicitly where the code is wrong and where I need the changes to be made. One thing I would do differently next time is give step by step of what I need it to do instead of just telling AI what I need output to be. Moreover, this project changed the way I think about AI generated code by seeing it as a tool that I guide rather than a tool that already knows.