# CS2-Predictive-Outcome-Model-
An automated Python model I built to predict pro Counter-Strike 2 match outcomes. It scrapes its own data, rates every team off how they've actually performed, and runs the whole thing on its own.
The tools I built
The scraper. This is the engine of the whole thing. I built it to pull match results and team stats off HLTV automatically and keep them current as new matches happen, so the model's always working off fresh data and I never touch a spreadsheet by hand. Getting this part reliable was most of the work.
The rating engine. Once the data's in, each team gets a composite rating I built that weighs results by how good the opponent was — beating a top team is worth way more than stomping some bottom-tier squad. That turns a messy pile of match results into one clean number per team that I can actually compare across the field. How I weight it is the part I'm keeping to myself.
The matchup model. For any given match it takes both teams' ratings and turns them into a win probability — my own read on who's actually favored, built from the numbers instead of from rankings or vibes.
The tracker. I built a logging system that locks in every prediction before the match and records what really happened after, so I've got an honest running record of how the model does over time. No going back and cherry-picking a hot week — the number is the number.
How it all fits together
Scrape → rate → predict → log, every day, automatically. The pieces hand off to each other so the whole pipeline runs start to finish without me in the middle of it. That part — getting separate tools to run as one automated system — is what I'm proudest of.
Built with
Python · Google Apps Script · HLTV data · Google Sheets
<img width="1920" height="1080" alt="Counter Strike Model - Google Sheets - Google Chrome 6_9_2026 9_53_38 AM" src="https://github.com/user-attachments/assets/03f5a18a-e089-47f9-b2d9-17582ab7a010" />
