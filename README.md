# Guild Activity Bot

A Discord bot for tracking guild activity and looking up player stats,
built for the Vectius guild Discord server.

**Status: in development.**

## Planned features

- **Guild activity tracking:** a scheduled job makes one request per hour
  to the Hypixel guild endpoint, which returns every member's GEXP history
  in a single response. Daily snapshots are stored in a local database.
- **Weekly leaderboard and inactivity report:** posted to Discord from the
  stored data.
- **!bw <username>:** on-demand Bedwars stats lookup for guild members.
  Requests are only made when a member runs the command, results are cached
  for several hours, and each user has a cooldown.

## How it works

- All Hypixel API requests come from a single backend on a fixed schedule
  or in response to commands.
- The bot runs only in the guild's own Discord server.
- The API key is read from an environment variable (`HYPIXEL_API_KEY`) and
  is never committed to this repository.

## Disclaimer

This project is not affiliated with or endorsed by Hypixel.
