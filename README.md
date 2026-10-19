# Andy Fantasy GM

A private, non-commercial decision-support project for my own Yahoo Fantasy Basketball teams. This public repository contains only the project description for API access review.

## Intended users and purpose

The intended user base is one person: myself, managing my own teams across five Yahoo Fantasy Basketball leagues in which I participate. The project is not a public fantasy platform, subscription service, or commercial product.

The goal is to receive a daily, league-specific roster and streaming brief in my private Discord channel. Each league is analyzed using its own scoring categories or points rules, roster positions, and relevant league settings.

## Requested Yahoo Fantasy data

Read-only access is requested for:

- Discovery of my leagues and teams for the current basketball season.
- League settings, scoring categories and modifiers, roster positions, lineup rules, waiver rules, and playoff settings where available.
- My roster and the other participating teams' rosters within those leagues.
- Free-agent and waiver availability.
- Current matchups, category totals, or fantasy points.
- Available player statistics and injury/status fields.
- Recent completed league transactions.

These data support explainable recommendations such as whether to hold a player, consider a free-agent replacement, or avoid a roster move when the evidence is insufficient.

## Planned operation

A Python program will run daily on GitHub Actions, with a backup attempt if needed. It will send an overview and individual league briefs through a Discord webhook to my private channel. My personal computer will not need to remain on.

The program will not automatically add or drop players, change lineups, submit waiver bids, or propose or accept trades. All fantasy roster decisions remain manual. Only Yahoo Fantasy read access is required.

## Privacy and data handling

OAuth credentials, refresh tokens, Discord webhook URLs, private league snapshots, and implementation code will be kept in private storage or a separate private repository. This public information repository will not contain them.

The tool is for my own analysis and will not publicly redistribute raw league or player data. Requests will use caching, bounded pagination, and retry/backoff controls.

## Development status

The initial implementation and offline tests have been prepared. Yahoo account authorization, verification against my actual leagues, and cloud delivery remain pending API access approval and setup. This project is not affiliated with or endorsed by Yahoo.

## Attribution

Reports using Yahoo Fantasy data will include: [Fantasy data provided by Yahoo Fantasy](https://basketball.fantasysports.yahoo.com/). Any additional access, usage, retention, or branding requirements communicated during review will be followed.
