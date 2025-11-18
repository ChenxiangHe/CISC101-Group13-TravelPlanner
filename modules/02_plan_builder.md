<!-- Change Log
v2 (2025-11-18): 
- Clarified activity selection rules and variety expectations.
- Connected metadata (duration, cost, distance) to user constraints.
- Added fallback logic for unknown lodging and bad weather.
- Introduced daily duration caps and backup activity guidance.
-->

Module 2 — Plan Builder (Options → Days)

Goal: Build realistic daily activity plans from a candidate list while respecting user constraints.

### Step 1 — Create a structured candidate list
For each time-of-day slot (Morning, Midday, Afternoon, Evening), generate **3–5 candidate activities**.  
Each activity must include:
- type (e.g., museum, cafe, park, landmark)
- estimated duration  
- cost range  
- distance or travel time from prior activity / lodging  
- indoor/outdoor flag  
- notes (e.g., seasonal closure, booking required)

**Variety expectations**:
- Afternoon must differ in theme from Morning (culture → nature, indoor → outdoor, etc.).
- Avoid repeating the same type across consecutive days unless user preferences allow it.

### Step 2 — Integrate user constraints
Filter or reorder candidates using:
- **Budget:** match cost range to budget style.  
- **Pace:** relaxed = fewer/shorter activities; fast = denser schedule.  
- **Mobility:** avoid long walks; prefer short-distance transit options.  
- **Dietary needs:** ensure restaurant options meet restrictions.

### Step 3 — Fallback rules
If lodging location is missing:
- default to central district or major transit hub.

If bad weather:
- include at least **one indoor candidate per slot**.

### Step 4 — Build each day (simple loop)
for each day:
- pick Morning activity (near lodging or fallback area)
- pick Midday activity (close by)
- pick Afternoon activity (different theme)
- pick Evening restaurant or optional event

### Step 5 — Feasibility guidance
- Keep total daily duration within **8–10 hours**.
- Ensure transitions are realistic (travel time + distance).
- Add **one backup activity** per day when possible.
