# Full-Stack AI Coding Assessment — 120 Minutes

## Goal

Build and deploy a small, secure, authenticated web application. This exercise is designed to show how you work as a front-end developer with back-end knowledge and how you use AI tools to accelerate your work responsibly.

You may use any AI assistant, framework, library, UI kit, authentication provider, database, hosting provider, or public API. We assess your decisions and implementation, not the number of tools you use.

## Timebox

**120 minutes total**, including setup, implementation, testing, documentation, pushing code, and deployment.

Please start your screen recording before creating the branch. If you cannot finish every stretch goal, submit the best working version and clearly document what remains.

## Challenge: Secure Personal Discovery Dashboard

Create an application where a signed-in user can search a public, pre-built API and save items they want to revisit.

Examples of suitable APIs include GitHub repositories, recipes, books, movies, countries, jobs, or weather locations. Choose one that lets you deliver a useful, understandable experience quickly. Do not build the external data source yourself.

### Required user flow

1. A user can sign up or sign in using a real authentication solution.
2. Unauthenticated visitors cannot access the dashboard or another user's saved data.
3. An authenticated user can search the selected external API and view useful results.
4. An authenticated user can save an item and see their own saved items after refresh or a new session.
5. The user can remove a saved item and sign out.

### Required technical behavior

- Use an external pre-built API through your application. Prefer a server-side/API route/BFF layer rather than placing private API credentials in browser code.
- Create at least one back-end endpoint or server-side action that validates input, calls or coordinates a service, and returns an appropriate response.
- Persist saved items in a database or managed data store. Data access must be scoped to the authenticated user on the server/database, not merely filtered in the browser.
- Provide sensible loading, empty, and error states.
- Make the primary flow usable on both desktop and mobile widths.

## Security Expectations

Security is part of the assessment. Demonstrate pragmatic safeguards appropriate for a two-hour build:

- Use a reputable authentication solution; do not implement password handling from scratch.
- Protect dashboard routes and enforce ownership of saved items at the API/database layer (for example, server-side authorization or row-level security).
- Validate and constrain API input on the server. Return safe, useful errors; do not expose stack traces or credentials.
- Do not commit secrets, API keys, tokens, `.env` files, or service-role credentials. Use environment variables and include an `.env.example` containing only variable names/placeholders where needed.
- Do not render API/user-provided content as raw HTML. Avoid unsafe HTML rendering unless you explain sanitization.
- Avoid treating a client-side route check as your only access control.

If your selected public API needs no key, state that clearly in the README.

## AI Usage Requirements

AI is expected for this exercise. You may use ChatGPT, Codex, Claude, Cursor, Copilot, Gemini, or another tool.

Use AI deliberately and retain evidence of your workflow. Your submission must include `AI_USAGE.md` with:

- AI tool(s) used and what each was used for.
- Three or more meaningful prompts/requests (or concise summaries if sharing verbatim would expose sensitive information).
- What you accepted, changed, or rejected from the AI output, and why.
- At least one example of how you verified AI-generated code (test, manual check, documentation check, or security review).

Also provide access to the relevant AI conversation(s): a share link, exported transcript, or screenshots. Redact credentials, tokens, personal information, and proprietary data before sharing. We are interested in your reasoning and validation, not a perfect prompt history.

## Git and Deployment Requirements

1. **Do not commit directly to `main` (or `master`).**
2. Create a new branch named `assessment/<your-name>` (for example, `assessment/jane-doe`).
3. Make your commits on that branch and push it to the repository.
4. Deploy the application from that branch to a publicly accessible preview/live URL (for example, Vercel, Netlify, Cloudflare Pages, Render, or an equivalent platform).
5. Do not merge the branch into `main`.

Use clear, focused commit messages. At minimum, create more than one commit if time permits; the Git history should make the work understandable.

## Repository Documentation

Update this `README.md` in your branch with:

- A one-paragraph description and screenshots/GIF if useful.
- Stack and service choices.
- Local setup instructions, including required environment variable names.
- How authentication and per-user authorization are enforced.
- The external API used and how it is accessed.
- Test/verification steps and any known limitations or unfinished work.
- The deployed URL.

Your repository must run from the documented instructions. Never include real secret values in documentation.

## Submission

> Submit within 120 minutes of starting the recording.

Send all of the following:

- Repository URL and the exact `assessment/<your-name>` branch URL.
- Deployed application URL.
- Screen-recording URL showing the work session from branch creation through deployment/submission.
- AI chat/transcript/share link(s), or a link to the exported/redacted evidence in the repository.
- A short note describing anything incomplete and how you would complete it next.

The application may be public for review. If using a provider requires test accounts, include safe reviewer instructions without publishing passwords or secrets.

Note: Create a private repository in your own GitHub account and invite debug-solution as a collaborator before beginning. Create your work on assessment/<your-name>. Do not add any other collaborators or change the repository visibility.

## Evaluation Criteria

| Area | What we evaluate |
| --- | --- |
| **Effective AI use (25%)** | Clear, purposeful prompts; sound judgment over AI suggestions; iterative verification; awareness of security and correctness. AI output is not accepted blindly. |
| **Front-end engineering (30%)** | Clear component structure, responsive and usable UI, state handling, loading/error/empty states, accessibility basics, and safe browser-side behavior. |
| **Git and delivery (15%)** | Correct branch workflow, understandable commits, clean repository, useful documentation, and a working deployment. No direct commits to `main`. |
| **Back-end engineering (30%)** | Correct authentication and authorization, protected per-user persistence, API design/validation, secure secret handling, and robust integration with the external API. |

### What matters most

A smaller, complete, secure flow is stronger than a feature-heavy demo with broken authorization or undocumented setup. We will consider the time limit: explain trade-offs, shortcuts, and known risks in the README rather than hiding them.

## Optional Enhancements

Only attempt these after the required flow works:

- Debounced search, pagination, or caching.
- Automated tests.
- Accessibility improvements beyond the basics.
- Rate limiting, request cancellation, or graceful third-party API fallback.
- A thoughtful UI polish or a small feature that meaningfully improves the chosen use case.

Good luck — build something focused, trustworthy, and easy to review.
