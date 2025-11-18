* Module 02 — Plan Builder (Options → Days)** 
Purpose
Transform the candidate Options (activities, restaurants, events) into structured Days that respect traveler inputs, constraints, and realistic pacing.

Inputs
Dates: trip start/end, daily time windows (default 09:00–21:00).

Location: city/region, lodging coordinates or neighborhood.

Budget: per-day and total trip target; strict or flexible mode.

Traveler preferences: themes (culture, food, nature), pace, dietary needs, accessibility, family/solo.

Transport mode: walk, public transit, car, ride-share.

Options list (from Module 01): activities with attributes (name, type, location, duration, cost range, opening hours, weather sensitivity, booking requirements, tags).

Day-Building Logic
For each day:

Morning (09:00–12:00)

Pick activity near lodging.

Must fit opening hours and allow 15–30 min buffer for transit.

Midday (12:00–15:00)

Include lunch (restaurant or food market) respecting dietary preferences and budget.

Optional short activity nearby; transit ≤25 min.

Afternoon (15:00–18:00)

Select activity with a different theme than earlier slots.

Must fit remaining time and opening hours.

Evening (18:00–21:00)

Restaurant aligned with budget and dietary needs.

Optional event if booking feasible and weather suitable.

Constraints enforced:

Buffers: 15–30 min between activities; 60 min for meals.

Travel guardrails: transit capped per hop (≤30 min walking equivalent).

Budget guardrails: daily total must stay within target (±10% if flexible).

Max 3–4 activities per day to avoid overpacking.

Robustness / Replacement Strategy
Weather fallback: swap outdoor activities for indoor/mixed options.

Missing data: if cost or hours unknown, prefer alternatives with known data; otherwise mark tentative.

Budget stress: replace with free/low-cost options or shorten paid durations.

Accessibility/family mode: filter out unsuitable activities (long walks, late-night events).

Unavailable activity: suggest alternative nearby or mark slot as “free time.”

Outputs
Each Day Plan includes:

Ordered list of activities with: name, type, start/end time, location, travel details, duration, cost estimate, notes (weather, booking, accessibility).

Daily summary: total estimated cost vs. budget, total travel time, themes covered, contingency notes.

Flags: tentative items, bookings required, budget deviations.


