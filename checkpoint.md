# Checkpoint

Quiz the developer on code that was just written or changed, to make sure they understand it.

## Steps

1. **Get the diff.** Run `git diff HEAD` to see unstaged changes. If empty, try `git diff HEAD~1 HEAD` to see the last commit. If still empty, tell the user there's nothing to checkpoint and stop.

2. **Identify what changed.** Read the diff and identify the most meaningful changes: new functions, logic changes, new imports, schema changes, etc. Note the filenames involved.

3. **Generate 3 questions** based specifically on the diff — nothing generic. Use a mix:
   - One **multiple choice**: 4 options, one correct
   - One **true/false**: a clear statement about the code
   - One **open-ended**: requires the developer to explain something in their own words

4. **Ask the multiple choice question** using the AskUserQuestion tool. Use the question text as the question, and the 4 options as the choices. After they answer, tell them whether they were right and briefly why.

5. **Ask the true/false question** using the AskUserQuestion tool with two options: "True" and "False". After they answer, tell them whether they were right and briefly why.

6. **Ask the open-ended question** as a regular message. Read their response and evaluate whether they genuinely understood — be encouraging but honest. If they missed something important, explain it clearly.

7. **Show the final score**: e.g. "2/3 — solid understanding" or "1/3 — let's recap what happened here" followed by a brief summary of the key things to take away from the diff.

## Rules

- Questions must be specific to the actual diff, not generic programming trivia.
- Keep questions concise. No preamble.
- For MC and T/F, give feedback immediately after each answer before moving on.
- The open-ended question should require the developer to reason, not just recall a fact.
