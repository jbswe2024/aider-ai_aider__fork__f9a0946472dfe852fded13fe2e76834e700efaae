---
parent: More info
nav_order: 500
---

# Analytics

Aider can collect anonymous analytics to help
improve aider's ability to work with LLMs, edit code and complete user requests.

## Opt-in, anonymous, no personal info

Analytics are only collected if you agree and opt-in. 
Aider respects your privacy and never collects your code, chat messages, keys or
personal info.

Aider collects information on:

- which LLMs are used and with how many tokens,
- which of aider's edit formats are used,
- how often features and commands are used,
- information about exceptions and errors,
- etc

These analytics are associated with an anonymous,
randomly generated UUID4 user identifier.

This information helps improve aider by identifying which models, edit formats,
features and commands are most used.
It also helps uncover bugs that users are experiencing, so that they can be fixed
in upcoming releases.

## Enabling & disabling analytics

You can opt out of analytics forever by running this command one time:

```
aider --analytics-disable
```

To enable analytics for a single session, you can run aider with `--analytics`.
This will *not* have any effect if you have permanently disabled analytics with the previous command.

The first time, you will need to agree to opt-in.

```
aider --analytics

Aider respects your privacy and never collects your code, prompts, chats, keys or any personal
info.
For more info: https://aider.chat/docs/more/analytics.html
Allow collection of anonymous analytics to help improve aider? (Y)es/(N)o [Yes]:
```

If you've added `analytics: true` to your 
[yaml config file](/docs/config/aider_conf.html), 
you can disable analytics for a single session, you can run:

```
aider --no-analytics
```

## Details about data being collected

### Sample analytics data

To get a better sense of what type of data is collected, you can review some
[sample analytics logs](https://github.com/aider-ai/aider/blob/main/aider/website/assets/sample-analytics.jsonl).
These are the last 1,000 analytics events from the author's
personal use of aider, updated regularly.


### Analytics code

Since aider is open source, all the places where aider collects analytics
are visible in the source code.
They can be viewed using 
[GitHub search](https://github.com/search?q=repo%3Aaider-ai%2Faider+%22.event%28%22&type=code).


### Logging and inspecting analytics

You can get a full log of the analytics that aider is collecting,
in case you would like to audit or inspect this data.

```
aider --analytics-log filename.jsonl
```

If you want to just log analytics without reporting them, you can do:

```
aider --analytics-log filename.jsonl --no-analytics
```


## Reporting issues

If you have concerns about any of the analytics that aider is collecting
or our data practices
please contact us by opening a
[GitHub Issue](https://github.com/paul-gauthier/aider/issues).

## Privacy policy

Please see aider's
[privacy policy](/docs/legal/privacy.html)
for more details.

