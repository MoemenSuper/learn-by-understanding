# Understand First Teaching Philosophy

This reference describes a topic-agnostic teaching style for agents, tutors, assistants, and learning systems.

## 1. The Main Problem This Skill Solves

Many explanations move too quickly from words to abstractions:

- "This handles the request."
- "This manages state."
- "This is best practice."
- "This step processes the input."
- "This formula gives the result."

These phrases often hide the part the learner actually needs: what each word means, where it came from, what is happening physically or logically, and what breaks if the step is missing.

The teaching philosophy here is: **understanding comes before flow**.

## 2. The Explanation Ladder

Use this ladder for every important idea.

### 1. Plain Meaning

Start with the learner's natural language.

Example:

`request` lets us take inputs that the user did on our website.

### 2. Precise Meaning

Then add the technical definition.

Example:

In Flask, `request` is an object representing the current HTTP request sent from the browser to the backend route.

### 3. Source

Say where the thing comes from.

Examples:

- imported from a library,
- defined earlier in the same file,
- passed into a function,
- received from a user,
- read from a file,
- calculated by a prior step,
- provided by an external service.

### 4. Mechanism

Say what actually happens.

Avoid saying "processes". Say what changes:

- string becomes number,
- JSON becomes dictionary,
- pressure becomes motion,
- force changes direction,
- rule selects one option,
- external server returns a response.

### 5. Output Or Consequence

Say what comes out.

Examples:

- returns a dictionary,
- stores a number,
- changes the page,
- sends a message,
- moves the body,
- narrows the search,
- produces a decision.

### 6. Why

Explain why this choice exists.

Examples:

- "A dictionary fits because fields have names."
- "A list fits because there are many similar items."
- "A class fits because state and behavior belong together."
- "A check exists because user input is unreliable."
- "A warmup exists because the body is not ready for load yet."

### 7. Failure Mode

Say what goes wrong without it.

Examples:

- crashes with `KeyError`,
- wrong type causes comparison failure,
- secret leaks to users,
- external service timeout stops the flow,
- learner memorizes steps without knowing when to use them,
- physical movement becomes unsafe,
- argument becomes unsupported.

### 8. Tiny Example

Give the smallest possible example.

### 9. Real Example

Connect it to the learner's actual project, task, sport, problem, or goal.

## 3. The Active Learning Loop

Use this loop for durable learning:

1. Teach one small concept.
2. Ask the learner to predict.
3. Ask the learner to attempt.
4. Give hint 1: directional nudge.
5. Give hint 2: specific guidance.
6. Give solution only after attempt or explicit request.
7. Ask "explain it back".
8. Correct the explanation.
9. Record the new learning level if the environment supports learning records.

## 4. Good Explanation Patterns

### Software Example

Bad:

`jsonify` handles the response.

Good:

`jsonify` comes from Flask. It takes a Python dictionary like `{"success": True}` and turns it into a real HTTP JSON response the browser can read. We use it because frontend JavaScript expects JSON. Without it, the browser may receive the wrong response shape or headers.

### General Learning Example

Bad:

Warmups prepare your body.

Good:

A warmup gradually raises body temperature, increases blood flow, and lets joints move through the range they will need. We do it before hard work because cold muscles and stiff joints perform worse. Without it, you may feel slow, tight, or more likely to strain something.

### Math Example

Bad:

Use the formula to solve for x.

Good:

The formula is a shortcut for undoing the operation that was done to `x`. If `x` was multiplied, division reverses it. We use this structure because equations must stay balanced on both sides. If you change only one side, the equality stops being true.

## 5. Questions To Ask While Teaching

Use these questions internally:

- What is the learner probably pretending to understand?
- Which word in this explanation is still undefined?
- Where did this value/tool/rule come from?
- What type or form is it right now?
- What changes after this step?
- Why did we choose this structure instead of another?
- What would break first if this line or step were removed?
- Is this happening locally, externally, physically, socially, or abstractly?
- Can the learner predict the next result?
- Can the learner explain it back without copying my wording?

## 6. Anti-Patterns

Avoid:

- starting with architecture before syntax,
- giving definitions without examples,
- giving examples without saying why,
- saying "best practice" without failure modes,
- skipping imports/sources,
- skipping runtime location,
- teaching the happy path only,
- revealing solutions before effort,
- turning lessons into passive reading,
- using polished language that hides mechanics.

## 7. Minimal Lesson Skeleton

Use this structure:

1. **Goal:** what the learner will be able to do.
2. **Vocabulary:** define each new word.
3. **Literal syntax or step:** decode it.
4. **Why this shape:** data structure, method, or practice.
5. **What can break:** failure modes.
6. **Tiny example:** isolated and clear.
7. **Real example:** learner's actual context.
8. **Prediction:** learner guesses result.
9. **Practice:** learner attempts.
10. **Hints:** progressive.
11. **Solution:** delayed.
12. **Explain it back:** learner recalls.
13. **Takeaway:** one compressed rule.

## 8. Output Standard

The learner should leave with:

- a plain-language explanation,
- a precise explanation,
- one tiny example,
- one real example,
- a reason for the chosen method,
- a known failure mode,
- a recall prompt.

If any of those are missing, the teaching is incomplete.
