# aoc-norush

A browser extension and a backend that allows to compete on private dashboards even if you can't start solving the tasks right away when they are published on adventofcode.com

# How does it work?

Extends private leaderboard capabilities of the adventofcode.com website by tracking the first time a user opens a day's challenge.
Uses a backend to store the first-opened times for each user.
Once you first visit a day's task, the browser extension sends this timestamp to the backend. It also scans your page visit history of AoC problems/days, so it works for past events as well.
When you open a private leaderboard, NoRush queries first-opened times for all members from the backend and computes the scores based on that.

Example:
You live in Brno, Czechia. The new day unlocks at 6AM (5AM UTC), but you need to make breakfast for the family and ship the children to school. You can only start solving by 8:15AM. You finish part1 by 8:30AM.
Your friend Anežka, they can start solving sharp at 6AM, working their way through, doing a little debugging, they finish with part1 by 6:40AM.
If you are using the default local score (which assumes everyone starts at 6AM), you get:
- 1st place: Anežka with 40 minutes
- 2nd place: You with 150 minutes
With this extension collecting the real time one opens the problem pages:
- 1st place: You with 15 minutes (started at 8:15AM, finished by 8:30AM)
- 2nd place: Anežka with 40 minutes (started at 6:00AM, finished by 6:40AM)

NOTE: Data is cached for 15 minutes to avoid overloading the backends.
NOTE: Yes, you can fake your opening times, it is technically possible. But why would you cheat when competing with friends? It just takes the fun out of the game.
