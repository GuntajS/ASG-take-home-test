# Take-Home Test: Vehicle Inspection System

A full-stack vehicle inspection management system using React + TypeScript (frontend) and Express + TypeScript (backend).

**Recommended Time: around 1 - 2 hours** — You may take as long as you need, but please don't overthink it.

---

## Backend Tasks (`/backend`)

### Task 1: Implement `createCheck` Controller

**File:** `src/controllers/checkController.ts`

The `POST /checks` endpoint controller is not implemented. You need to:

1. Validate request body using `validateCheckRequest(req.body)`
2. Return 400 with `ErrorResponse` format if validation fails
3. Call `checkService.createCheck()` if validation passes
4. Return 201 with the created check

**Verify:** Remove `.skip` from the test `"should create check and return 201"` in `api.test.ts`

### Task 2: Fix the bug in service function `createCheck`

**File:** `src/services/checkService.ts`

The `hasIssue` flag is not correctly identifying if one inspection record has issue. Find and fix the bug.

**Verify:** Remove `.skip` from the test `"should set hasIssue to true when any item fails"` in `api.test.ts`

Run `npm test` — all tests should pass.

---

## Frontend Tasks (`/frontend`)

### Task 1: Fix Form Input

**File:** `src/CheckForm.tsx`

Check the form to make sure the fields are accepting valid input. You may change the input type where you find it appropriate.

### Task 2: Add Notes Field

**File:** `src/CheckForm.tsx`

Add a textarea for optional notes:

- Maximum 300 characters
- (Optional) Display character counter (e.g., "45/300")
- Include in API request and reset after submission

### Task 3: Implement Toast Notifications

**File:** `src/CheckForm.tsx`

Show visual feedback using the provided `Toast.tsx` and `useToast.ts`:

- Success toast on successful submission
- Error toast on failure
- (Optional) Show good error message in toast on failure

---

## Questions

Please answer these briefly:

1. **Authentication:** If we need to add authentication to this system, how would you approach it?

   - A: For the current system a JSON Web Token authentication would suffice but if this was a production system I would implement OAuth 2.0 since that is the industry standard

2. **Improvements:** What other improvements would you implement if this were going to production or if you have more time?

    - A: I would firstly implement a database such as MongoDB or PostgreSQL, then I would implement Ci/CD pipelines, and logging system for errors. and maybe an AI agent if the app had more functions (my area of expertise).

3. **Tech Stack Experience:** Do you have experience with PHP, Vue.js, or mobile app development (React Native/Flutter)?

    - A: I do not specifically have experience PHP, Vue.js or mobile app development but I have a strong background in web technologies with Python, Flask Typescript, React TS and JS and Java and axios. 

4. **AI / Tools:** What tools/assistants did you use while working on this assignment (e.g., GitHub Copilot, ChatGPT, etc.)? We appreciate AI usage, we're interested in _how_ you use these tools.

   - A: I used Gemini Pro 3.0 to primarily to verify if my thought process and implementation was correct and used its recommendations to improve my work, but I made the final decision on what should be implemented and how.

5. **Visa Status:** What visa are you currently on?

   - A: I am an Australian Citizen

6. **Languages:** We have users from different backgrounds and industries. What language(s) do you know and what's your proficiency level?

   - A: I proficiently know English, Hindi and Punjabi. I am learning Polish, low proficiency.

> **Tip:** You can write your answers directly in this README.md file below each question.

---

## Submission (How to Submit)

1. Create a **public GitHub repository** for this assignment.
2. Push your code with all changes.
3. **Create at least two pull requests (PRs):** one for backend and one for frontend. You may create more (e.g., each task can be an independent PR). You may merge them into the main branch. We can review and may leave comments on your PRs for feedback.
4. Answer questions above.
5. **Please complete and submit within 3 days** unless otherwise discussed.
6. Send the repository link to **admin@enroute-tech.com**.

---

Good luck!
