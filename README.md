# Grant Assistant

An open-source workspace for managing grant applications, maintaining a centralized company knowledge base, and generating grant-specific responses with AI.

## Why this exists

Most grant applications require the same information to be rewritten repeatedly for different funders.

Grant Assistant separates:

* **Company knowledge** (facts that rarely change)
* **Grant-specific context** (the RFP, priorities, and requirements)
* **Application responses** (adaptive content and custom questions)

This allows teams to maintain a single source of truth while tailoring applications to each grant opportunity.

---

## Features

### Centralized Knowledge Base

Store reusable company information such as:

* Technology overview
* Team information
* Funding history
* Traction and milestones
* IP and patents

These fields become the factual foundation for all generated content.

### Grant Workspaces

Create a dedicated workspace for each grant opportunity.

Each workspace includes:

* Grant description
* Notes
* Adaptive fields
* Grant-specific questions
* Custom word limits

### Adaptive Content Generation

Generate grant-specific versions of reusable narratives such as:

* Problem statement
* Mission statement
* Funding use
* Impact narrative

The system rewrites content to align with the priorities of the selected grant while preserving factual accuracy.

### Grant-Specific Questions

Add custom application questions for each grant.

Examples:

* What is your commercialization strategy?
* Describe the expected societal impact.
* How will funding accelerate development?

Generate draft answers and refine them over time.

### Feedback-Aware Regeneration

Provide feedback on generated content such as:

> Make this less technical.

> Focus more on patient outcomes.

> Reduce jargon and improve clarity.

The feedback is incorporated into subsequent generations, allowing iterative improvement rather than starting from scratch.

### Word Limits

Apply field-specific and question-specific word limits to keep responses aligned with application requirements.

---

## Tech Stack

| Layer    | Technology                           |
| -------- | ------------------------------------ |
| Frontend | React (CDN, no build step)           |
| Backend  | Node.js + Express                    |
| Database | node-json-db                         |
| AI       | OpenAI API                           |
| Hosting  | Render, Railway, or any Node.js host |

---

## Getting Started

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd grant-assistant
```

### 2. Install dependencies

```bash
npm install
```

### 3. Create environment variables

Create a `.env` file:

```env
OPENAI_API_KEY=your_api_key_here
OPENAI_MODEL=gpt-5.4-mini
```

### 4. Start the application

```bash
npm start
```

The application will be available at:

```text
http://localhost:3000
```

---

## Project Structure

```text
server.js
public/
  index.html
package.json
db.json
```

### Key Files

* `server.js` — API routes, persistence, and AI integration
* `public/index.html` — frontend application
* `db.json` — local JSON database

---

## Notes

AI-generated content should always be reviewed before submission.

Grant Assistant is designed to improve drafting efficiency, not replace human review or domain expertise.

---

## License

MIT
