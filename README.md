# Graduate Attributes Self-Assessment

**Live tool: https://drdukegledhill.github.io/GraduateAttributes/**

A lightweight, single-page web tool for students to self-assess their development across the University of Huddersfield's seven Graduate Attributes. No accounts, no server, no data storage — progress is encoded directly in a bookmarkable URL.

## Graduate Attributes

The seven Graduate Attributes describe the qualities that employers consistently look for in graduates. The tool helps you track your self-assessed development across each one throughout the year.

### 🎯 Self-motivated

**Taking ownership of your work and development without needing external prompting.**

Self-motivation means setting goals for yourself, following through without being chased, and actively seeking new challenges rather than waiting to be told what to do. It shows up in how you manage your time, how proactively you seek feedback, and how much you invest in your own development beyond what is formally required.

In practice: managing your workload effectively, going beyond the minimum because you care about quality, seeking feedback before it is offered, developing skills outside of structured study, following through on commitments without reminders.

*Employers value this because* self-motivated graduates can be trusted to work independently, take initiative, and grow in a role without constant supervision.

---

### 🌐 Commercially aware

**Understanding how organisations operate within their broader environment.**

Commercial awareness means knowing what drives success in an organisation — including markets, competition, regulation, finance, and the needs of different stakeholders. It is the ability to see the bigger picture: understanding why decisions are made, how different parts of a business connect, and what pressures organisations face from outside.

In practice: following industry news and trends relevant to your field, understanding what makes a business financially viable, recognising how decisions in one team affect others, appreciating what customers, employees, and shareholders each need from an organisation.

*Employers value this because* graduates who understand business context make better decisions, communicate more effectively, and can quickly contribute beyond their immediate role.

---

### 💡 Enterprising

**Bringing creativity, initiative, and adaptability to problems and opportunities.**

Being enterprising is not just about starting businesses — it means bringing entrepreneurial energy to whatever you do. It is about spotting opportunities, generating ideas, and adapting your approach when circumstances change or a plan is not working. Enterprising people find ways forward where others see obstacles.

In practice: proposing solutions rather than just identifying problems, approaching challenges with a "how might we?" mindset, pivoting quickly when a plan is not working, experimenting with new approaches, turning a creative idea into a concrete action.

*Employers value this because* organisations need people who can innovate and adapt. An enterprising mindset drives growth, problem-solving, and continuous improvement at every level.

---

### 🏋️ Resilient

**Maintaining drive and focus when things get difficult.**

Resilience is the ability to deal constructively with setbacks, pressure, and uncertainty — and to keep going. It does not mean never struggling; it means being able to recover, learn from difficulty, and sustain your effort over time. Resilient people do not need everything to go smoothly to perform well.

In practice: staying calm under pressure, bouncing back after a disappointing result, learning from failure rather than being defeated by it, persisting when a task is harder than expected, keeping perspective when things go wrong.

*Employers value this because* workplaces are demanding and unpredictable. Resilient graduates sustain their performance, support their teams, and navigate ambiguity without needing excessive reassurance.

---

### 🤝 Effective collaborator

**Working productively with others and building positive relationships.**

Effective collaboration is more than just being easy to work with. It means actively contributing to group success, listening to understand rather than just waiting to speak, managing disagreements constructively, and adapting your communication style to suit different people and contexts.

In practice: taking an active, constructive role in group work, listening carefully and checking your understanding, managing disagreements respectfully and without escalating them, adapting how you communicate to suit different people, celebrating team successes as well as your own.

*Employers value this because* almost all professional work involves collaboration. Graduates who build rapport quickly, navigate team dynamics well, and make the people around them more effective are invaluable.

---

### 🚀 Confident leader

**Stepping up to inspire, guide, and motivate others — whether or not you hold a formal role.**

Leadership is not reserved for managers. A confident leader is someone who can identify what needs doing, bring others along, and make things happen. It means communicating a clear direction, holding yourself and others accountable, encouraging contributions from quieter voices, and owning the outcome of the decisions you make.

In practice: taking responsibility for a group's direction when needed, communicating goals clearly so others feel energised by them, drawing out contributions from everyone in a team, holding yourself accountable when things do not go to plan, making decisions and seeing them through.

*Employers value this because* organisations need people at every level who can create momentum and give teams direction, not just those at the top of an org chart.

---

### 🌍 Globally & socially aware

**Understanding the world beyond your immediate context and welcoming diverse perspectives.**

Global and social awareness means recognising that decisions have implications beyond the immediate — for people, communities, and the environment. It involves being curious about perspectives that differ from your own, understanding how cultural differences shape communication and expectation, and thinking about ethical and sustainability impacts alongside performance.

In practice: seeking out viewpoints that differ from your own, staying curious about global events and how they connect to your field, recognising how cultural differences shape communication and expectation, thinking about sustainability and ethical impact alongside commercial outcomes, being genuinely inclusive and respectful of difference.

*Employers value this because* today's organisations operate across borders and face growing scrutiny over their social and environmental impact. Graduates who are globally and socially aware make better decisions, build more inclusive teams, and contribute to more ethical, sustainable organisations.

---

## How it works

Students visit the page and rate themselves 1–5 on each attribute. The radar/spider chart updates in real time as they answer. On saving, the browser URL updates to encode their scores — they bookmark it and return later for subsequent assessments.

Up to **5 assessments** can be completed across the academic year. Each new assessment adds another layer to the radar chart, making development over time visible at a glance.

Once two assessments are saved, an **Assessment / Progress** tab switcher appears at the top of the page. The Progress tab shows:

- **Score trends** — a line chart tracing each attribute across all completed assessments, with a colour-coded legend
- **Progress so far** — a side-by-side score grid for quick comparison

Switching back to the Assessment tab always presents a clean form for the next round. A **dark/light mode** toggle (☀️/🌙) in the header switches themes, with the preference saved in the browser. A **Reset all data** button in the footer clears the URL and returns the tool to its initial state.

Each attribute card on the assessment page has an **ⓘ button** that opens a popup with a fuller explanation of that attribute — useful for students who want to understand what they are rating themselves on before answering.

### URL format

Each assessment is stored as a 7-digit string (one digit per attribute, 1–5):

```
index.html?v1=3452341
index.html?v1=3452341&v2=4563452
```

No data ever leaves the student's browser.

## Hosting

The tool is designed to be served via **GitHub Pages** from the `/docs` folder.

1. Push this repository to GitHub
2. Go to **Settings → Pages**
3. Set source to **Deploy from branch → `main` → `/docs`**
4. The tool will be available at `https://<username>.github.io/<repo>/`

## Development

The tool is a single self-contained HTML file at `docs/index.html` with no build step or dependencies beyond a CDN-hosted copy of [Chart.js](https://www.chartjs.org/).

To run locally, open `docs/index.html` directly in a browser or serve with any static file server:

```bash
npx serve docs
```

## Licence

[Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](LICENSE)

© Dr Duke Gledhill. Free to use and adapt for non-commercial educational purposes with attribution.
