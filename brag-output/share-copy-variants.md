# Share copy variants

## Short (X / Discord)
RoValid has screened 900,000 Roblox usernames. Every free one looks like `2b6b2`.
Free names are not scarce — good ones are. So it watches 3,600 of them and waits.

## Technical (HN / dev Discord)
RoValid checks Roblox username availability in two stages: a bulk endpoint that screens
200 names per request, then a per-name validator for the survivors — because censored and
reserved names have no account behind them and a batch-only checker calls them free.
A GitHub Action runs it every 15 minutes and commits what it finds to a Pages board.

## Deadpan
I built a Roblox username hunter. It has found 185,300 free names.
Not one of them is worth having.
