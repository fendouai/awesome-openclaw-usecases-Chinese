# X Account Analysis

There are many websites designed to give you a qualitative analysis of your X account. While X already gives you an **analytics** section, it's more focused to show your numbers on your performance.

But a qualitative analysis focuses on the quality of your posts, not the performance stats. Some insights you can get from this type of analysis:
- What are the patterns that make my posts go viral?
- What topics I talk about get me most engagement?
- Why do I get posts with 1000+ likes but sometimes posts with <5 likes? What am I doing wrong?

There are many websites and apps designed to give you X analytics, but they focus on the statistics. There are probably 1-2 websites that let you talk with an AI to understand your performance. 

But now you can use OpenClaw to do this analysis for you, without needing to pay $10-$50 for subscriptions on these websites.

## Skills you Need

Choose one X/Twitter path:

- Bird Skill. `clawhub install bird` (it comes pre-bundled)
- [TweetClaw](https://github.com/Xquik-dev/tweetclaw), the OpenClaw plugin for structured Xquik endpoints. Install it with `openclaw plugins install clawhub:@xquik/tweetclaw`. Use `openclaw plugins install npm:@xquik/tweetclaw` as the npm fallback.

## How to Set it Up
Here's the flow:
1. Make sure your chosen X/Twitter skill or plugin is working.
2. For security and isolation, you better create a new account for your ClawdBot.
3. If you use Bird, auth with your X account in Chrome/Brave and store any required session details locally. Do not paste cookies or credentials into chat history.
4. If you use TweetClaw, keep `XQUIK_API_KEY` out of chat, configure it with `openclaw config set plugins.entries.tweetclaw.config.apiKey "$XQUIK_API_KEY"`, then allow the `explore` and `tweetclaw` tools with `openclaw config set tools.alsoAllow '["explore", "tweetclaw"]'`.
5. Ask OpenClaw to take a look at your real account, fetch the last N tweets, and ask it any questions you like. Alternatively, you can ask it to write you specific scripts.

## TweetClaw Workflow Ideas

With TweetClaw, OpenClaw can use structured API calls instead of ad-hoc browser steps:

- Search tweets and tweet replies around your account, competitors, or topics.
- Export follower or following lists for audience clustering.
- Monitor X activity and send webhook-style alerts.
- Draft post tweets or post tweet replies, then ask for explicit approval before any write action.

Example prompt:

> Use TweetClaw to analyze my last 200 tweets and replies. Group the posts by topic, show which hooks performed best, identify follower segments, and suggest 5 new post drafts. Do not post anything unless I approve the exact text first.

TweetClaw is an open-source plugin for Xquik, a closed-source hosted service. Xquik is an independent third-party service. Not affiliated with X Corp. "Twitter" and "X" are trademarks of X Corp.
