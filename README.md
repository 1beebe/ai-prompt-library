# AI Prompt Library

A deployable, interactive prompt library for B2B teams — built to turn AI adoption intent into daily AI habits.

**[Live demo →](https://1beebe.github.io/ai-prompt-library/)**

---

## What it is

A single-file HTML app containing 50+ copy-paste-ready AI prompts organized by department: Sales, Customer Success, Channel Partner, Implementation, Marketing, HR, Finance, Leadership, and a Thought Partner section for structured thinking.

Features include:
- Filter by team, difficulty level, or category
- Full-text search across all prompts
- One-click copy to clipboard
- Email Connector prompts (for AI tools with productivity suite integrations)
- Works with any AI assistant — ChatGPT, Claude, Gemini, Copilot, or others

## Why it exists

Most AI adoption programs stall at the "here's what AI can do" stage. This tool solves the next step: giving people actual prompts for their actual jobs, so they can get a useful result on day one instead of spending 20 minutes figuring out how to ask.

## How it was built

**Input** — A project brief from stakeholder interviews and business requirements gathering, covering team structure, prompt categories, design specs, and success criteria.

**Build** — The brief went to Claude Code, which generated a single self-contained HTML file through iterative prompting and feedback loops. No front-end framework. No dependencies beyond a CDN icon set.

**Quality check** — Output was reviewed by prompting Claude Code to evaluate the file from the perspective of a CEO, a COO, and a UX reviewer. That surfaced structural changes like reorganizing the Thought Partner section, adding card-level filtering, and fixing anchor links. Manual QA and additional iterations followed.

## Customize it for your org

1. Open `index.html` in a text editor
2. Search for `[Your Company]` and replace with your company name
3. Edit or add prompts in the `PROMPTS` array in the `<script>` section — each prompt follows this shape:

```js
{
  team: "Sales",           // department filter
  title: "Prompt Title",
  category: "Writing",     // Writing | Analysis | Research | Planning | Communication
  difficulty: "Quick Start", // Quick Start | Going Deeper | In-Depth
  prompt: `Your prompt text here. Use [VARIABLES] for things users fill in.`,
  tip: "A short coaching note shown below the prompt.",
  alsoFor: ["Marketing"]   // optional: show card in additional team filters
}
```

3. Save and open in any browser — it's fully self-contained, no server required
4. Deploy anywhere: GitHub Pages, Netlify, your intranet, or just share the HTML file

## Prompt data

The raw prompt data is also available as [`prompts.json`](prompts.json) if you want to build your own UI on top of it.

## License

MIT — free to use, copy, and modify. Please keep the credit intact.

AI-generated outputs produced when using these prompts are not guaranteed to be accurate. Always review before use.

---

Built with Claude Code · Directed by [Ligaya Beebe](https://lbeebe.com) · April 2026
