# 7:00 Court Clock

A phone-friendly clock for the 7:00 am court release. It shows Hong Kong time (UTC+8), checked against an internet clock, with a countdown to 07:00:00 and a cue for each step of the morning.

**Live page:** https://y-dogic.github.io/court-clock/

## How it keeps time

The page fetches the tiny `tick.txt` file from its own GitHub Pages server and reads the server's `Date` header. That header only has whole seconds, so the page times its requests to land on second boundaries and narrows the clock offset down to roughly the network round trip (usually well under 0.1 s). If it can't reach the server, it falls back to the phone's own clock and says so.

The page never connects to SmartPLAY or any booking system. It's only a clock.

## Using it on an iPhone

1. Open the live page in Safari.
2. Tap **Share → Add to Home Screen**.
3. Check the status chip says **Synced**. If it says **Using iPhone clock**, turn on Settings → General → Date & Time → Set Automatically.

iOS pauses web pages in the background, so the countdown and beeps only run while the page is on screen. Running it on a second device works best.
