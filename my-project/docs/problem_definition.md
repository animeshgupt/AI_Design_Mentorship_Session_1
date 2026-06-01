# Problem Definition — Jazz Saxophone Learning System

---

## problem_statement

I need a personal practice coaching system that tells me what to work on each day, tracks what I'm avoiding or lagging behind on, and surfaces relevant videos or exercises to keep my learning fresh and progressing — so I stop defaulting to comfortable material and start making intentional progress on jazz saxophone.

## knowledge_domain

Jazz saxophone — covering technique, music theory, repertoire, improvisation, and ear training. Learning is guided by a mix of a teacher's plan, practice books, and YouTube videos.

---

## current_state

**current_engagement:**
Practicing 4–5 times per week (goal: every day). Weekday sessions are scheduled; weekend sessions are flexible (30–40 min minimum, flexible timing). Learning material spans practice books, a teacher's plan, and YouTube videos — but these are not integrated.

**existing_tools:**
- Practice books
- Teacher's plan (external, session-based)
- YouTube videos (ad hoc, no structured playlist)
- No dedicated tracking or progress tool currently

**current_trigger:**
Fixed schedule on weekdays. No clear trigger on weekends — relies on motivation.

**frequency:**
4–5x per week. Target is daily.

**friction_points:**
- Decision fatigue: unclear what to prioritize each session
- Avoidance: defaults to comfortable material rather than what needs work
- No visibility into progress or what's being neglected
- No system connecting the different sources (books, teacher, YouTube)
- Weekend sessions lack a trigger or structure

---

## desired_state

**success_criteria:**
- System tells me what to practice each day based on what needs attention
- Clear view of what I'm lagging behind on and what I've been avoiding
- Relevant YouTube video surfaced when stuck on a technique
- Fresh content introduced regularly (new exercises, revisited past material)
- Progress visible over time

**expected_impact:**
More intentional practice sessions. Less time deciding what to do, more time actually playing. Consistent daily practice habit. Tangible sense of improvement.

**return_loop_vision:**
Open the system before practice → get today's focus areas → practice → log what I did → system updates what needs attention next. Occasionally: system surfaces something new or flags a pattern ("you haven't touched chord tones in 10 days").

**constraints:**
- Willing to log practice sessions (brief, not burdensome)
- Open to using Notion as the interface
- YouTube playlists can be linked/integrated
- Starting from scratch — no existing system to migrate
- Weekend sessions need flexibility (time and duration)
- Weekday sessions are fixed and can be more structured

---

## assumptions_analysis

**Initial Assumptions Identified:**
1. The system can accurately judge what you're lagging behind on
2. You will consistently log after every session
3. YouTube is a reliable source for surfacing the right content at the right moment

**Validated Constraints:**
- Logging must be minimal: tap-to-select practiced items + check-off plan + 1–5 self-rating
- Weekend sessions need flexible timing and duration
- Starting from scratch — no existing data to import

**Flexible Assumptions:**
- "Lagging behind" can start as self-assessed goals; audio analysis (when sessions are recorded) added later as an enhancement
- YouTube curation starts from trusted channels you already follow, expands with suggestions over time
- Self-rating drives recommendations initially; can be calibrated over time

**Beliefs to Test:**
- That daily logging will actually stick even when kept minimal
- That self-rating is accurate enough to drive meaningful recommendations
- That the system can surface the right video at the right moment (not just any video from a trusted channel)

---

## solution_hypotheses

**Hypothesis 1 — The Organized Library (Level 1: AI as Assistant)**
- **What AI does autonomously:** Tags and organizes practice logs, displays frequency and ratings per topic, maintains a YouTube video library tagged by technique
- **Human touchpoints:** Manual logging after every session, decides what to practice each day by reading the dashboard
- **Interaction pattern:** Open Notion dashboard before session → read data → decide → practice → log
- **Scope boundaries:** Does: organizes and displays. Doesn't: recommend, plan, or suggest
- **Verdict:** Not far enough — visibility without direction doesn't solve decision fatigue

**Hypothesis 2 — The Daily Coach (Level 2: AI as Collaborator)**
- **What AI does autonomously:** Generates a daily practice plan based on logs, ratings, and goals; flags neglected areas; surfaces relevant YouTube videos
- **Human touchpoints:** Reviews and adjusts the generated plan, checks off items during practice, rates session after
- **Interaction pattern:** System drafts plan → you approve/adjust → practice → check off → rate → system updates
- **Scope boundaries:** Does: plan generation, neglect detection, video surfacing. Doesn't: send proactive notifications or act without being opened
- **Verdict:** Feels right — removes decision fatigue while keeping you in control

**Hypothesis 3 — The Autonomous Practice Agent (Level 3: AI as Agent)**
- **What AI does autonomously:** Tracks logs and detects patterns autonomously, queues session plans proactively, sends practice notifications, surfaces new videos/exercises when plateau detected, self-adjusts based on progress
- **Human touchpoints:** Sets goals once, handles exceptions and overrides, reviews flagged patterns
- **Interaction pattern:** Set goals → system runs → notification arrives → practice → log → system adapts
- **Scope boundaries:** Does: proactive planning, pattern detection, autonomous adjustment. Doesn't: override your goals or change practice frequency without input
- **Verdict:** Exciting — the aspirational end state to build toward

---

## selected_solution

**chosen_hypothesis:** Hypothesis 2 — The Daily Coach (Level 2), with Hypothesis 3 as the explicit evolution target

**solution_logic:** "If we implement the Daily Coach, it will produce more intentional practice which builds great momentum — because the system forces engagement with things I'm avoiding or unaware of, removing the decision fatigue that causes me to default to comfortable material."

**autonomous_capabilities:**
- Generate a daily practice plan based on logs, self-ratings, and personal goals
- Detect neglected topics (not practiced in X days) and low-rated areas
- Surface a relevant YouTube video from trusted channels when a technique is flagged
- Occasionally introduce a new exercise or revisit past material to keep sessions fresh
- Track progress over time and display trends per topic

**human_touchpoints:**
- Review and adjust the AI-generated daily plan before practice
- Check off items during or after the session
- Rate performance per item (1–5) after practice
- Set and update personal goals (e.g., "ii-V-I in all 12 keys by end of month")
- Override or skip suggestions when needed

**interaction_pattern:**
Open Notion → see today's plan → adjust if needed → practice → check off items → rate session → system updates for tomorrow

**success_metrics:**
- Practice frequency increases to daily (from 4–5x/week)
- Reduction in time spent deciding what to practice (target: under 2 minutes)
- Neglected topics surface within 3–5 days of being avoided
- Self-ratings on previously low-scored items improve over 4 weeks
- Feels less repetitive — new material or videos introduced regularly

**scope_boundaries:**
- Does: daily plan generation, neglect detection, video surfacing, progress tracking
- Does not: send proactive notifications (that's Hypothesis 3), analyze audio automatically, connect to teacher's plan automatically
- Human always approves the plan before practicing

## process_requirements

**process_inputs:**
- Daily practice log (what was practiced, check-offs, 1–5 ratings)
- Personal goals (set by user, updated as needed)
- YouTube channel list (trusted seed channels)
- Practice topic taxonomy (scales, chord tones, repertoire, technique, ear training, etc.)

**process_outputs:**
- Daily practice plan (prioritized list of focus areas with suggested time)
- Progress dashboard (frequency, ratings, trends per topic)
- Surfaced YouTube video (when relevant to current focus)
- Neglect alerts (topics not touched in too long)

---

## experiment_design

**core_assumption:** AI can generate a genuinely useful daily practice plan from a simple log — correctly identifying what needs attention (low ratings) and what's being neglected (not practiced recently).

**test_approach:** Provide a week of real practice log data to Claude or ChatGPT via a prompt. Evaluate whether the generated plan feels actionable and correctly prioritizes low-rated and neglected items.

**mock_data_examples:**
- Major scale patterns — practiced 3x this week, rated 3/5
- New scale memorization (numbered notes) — practiced 2x this week, rated 2/5 (still shaky)
- Song transcription (few bars) — practiced 1x this week, rated 3/5
- Jazz standard duet/transcription — practiced 2x this week, rated 4/5
- Jazz improv video exercise — practiced 1x this week, rated 3/5, not touched in 4 days

**test_scenarios:**
1. Standard case: does the plan correctly prioritize new scale memorization (lowest rating)?
2. Neglect detection: does the plan flag the improv exercise (4 days without practice)?
3. Balance: does the plan include variety, not just the lowest-rated item?
4. Edge case: what happens if everything is rated the same — does it fall back to neglect-based prioritization?

**success_criteria:**
- Plan surfaces new scale memorization and improv exercise as priorities
- Output feels like something I would actually follow, not generic advice
- Suggested session fits within 30–40 minutes

**learning_goals:**
- Understand how much context AI needs to generate a useful plan
- Identify where AI gets it wrong (too generic, wrong priorities, ignores neglect)
- Determine minimum log format needed for reliable recommendations
