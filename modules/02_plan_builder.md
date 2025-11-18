**Module 2 — Plan Builder (Options → Days)**

Create a short list of candidate activities (e.g., museums, landmarks, restaurants, parks) with the inputs of trip_budget and date_range. Each activity includes type, estimated duration, cost range, and distance. Between each activity, calculate travel time and add a 10% time buffer in case of delays. Schedule activities so that travel time is 30 minutes or less. Also, budget time for the following meals: Breakfast in the morning, Lunch in the middle of the day, and Dinner at the end of the day. If an activity is unavailable, provide another option. For each day, calculate day_budget and add up the total trip budget. If the total budget is greater than the input trip_budget, revise the activities so they are cheaper until the total budget is less than the input trip_budget. Estimate the time for each activity, and ensure the daily total time for activities is less than or equal to 6 hours.

Use a simple loop to build days:

for each day:   pick Morning activity (near lodging)    pick Midday activity (after lunch)    pick Afternoon activity (different theme than previous activities)    pick Evening restaurant or optional event
