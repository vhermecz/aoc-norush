# aoc-norush

[![Chrome Web Store Version](https://img.shields.io/chrome-web-store/v/kappjecebnaijcnggpalchijopjjiogp?style=for-the-badge)](https://chromewebstore.google.com/detail/aoc-norush-extension/kappjecebnaijcnggpalchijopjjiogp)
[![Mozilla Add-on Version](https://img.shields.io/amo/v/aoc-norush-extension?style=for-the-badge)](https://addons.mozilla.org/en-US/firefox/addon/aoc-norush-extension/)
![Static Badge](https://img.shields.io/badge/-TBD-red?label=Safari%20Extension&style=for-the-badge)
[![PayPal donate button](https://img.shields.io/badge/paypal-donate-yellow.svg?style=for-the-badge)](https://www.paypal.com/donate/?business=XVU35R3EPXQK2&no_recurring=0&currency_code=USD)

Share opening times with your friends, so you can have a good night's sleep, and still compete.

NOTE: For historical data, install on all Browsers used to solve challenges to harvest those times. See the [privacy policy](PRIVACY.md) about data collected, and how it is used.

## How to use it?

1. Install the browser extension
2. Open a private leaderboard
3. Click on [Ordering] and select the new [NoRush Score] option
4. Hover over the * z Δ o ✔ # icons and day nums in the table header for more details

## How does it look like?

After you select the new [NoRush Score] ordering, the score table is enhanced with a few new options:

![Enhanced dashboard](.resources/demo.png?raw=true "Enhanced dashboard")

## What are the features?

Enhances the rankings with:
- Order/score by:
  - part completion times, delta time
  - norush completion times, opening time (the users who installed this plugin)
- Order by score globally, or by the above times on a daily basis
- See the above time metrics for each user
- Two grid modes:
  - Completion mode: this is the traditional black/silver/gold star grid view
  - Rank mode: display ranking for each part: 1, 2, 3, ..., y, z  #base36

## How does it work?

Your browser captures page visitation info in its history. The extension scans this for the AoC challenge urls and uploads the earliest (first) times to its backend.

When you open a private leaderboard, the backend provides the opening times for all members with the extension installed.

NoRush score is calculated based on the time it took for you to solve the task from when you first opened its description.

NOTE: Opetimes are cached for 5 minutes. Even if you force reload the page. So the backend can chill. You should also ;)

NOTE: The official AoC API data (part completion times) is cached for 15 minutes (See the [API] link at the top of a private dashboard on why)

## Browser support

- Firefox: Click badge at the top
- Chrome: Click badge at the top
- Opera: Install from the Chrome Web Store
- Brave: Install from the Chrome Web Store

## FAQ

- It does not work: Currently the extension only activates, if you navigate to a Private Leaderboard, click on [Ordering] and select [NoRush Score]. If it is still not updating the view according to the screenshot, congrats, you found a bug. I might automatically see it in Sentry and fix it, but feel free to open an Issue about it.
- Where is the source, dude?: I am planning to open up the source code of both the browser extension and the backend, but probably only in January due to EOY deliverables ate up all my free and personal time :(

## Affiliation Disclaimer

Please be aware that "Advent of Code" and "AoC" are properties of Eric Wastl.
This initiative is not an "official" project and is neither endorsed nor affiliated with Advent of Code or its creator/owner in any manner, either directly or indirectly.
For further information about the Advent of Code project, you can visit [this link](https://adventofcode.com/2023/about).

**If you enjoy playing Advent of Code, you might want to [think about making a donation to support it](https://adventofcode.com/support)!**

## Donation

I have spent ~150 hours to date aka 1 man-month on bringing this idea to reality.

If you find it useful, consider a small donation to support this effort.

But only do so if you already [donated to AoC](https://adventofcode.com/support). AoC first, NoRush second. Thank you!

[![PayPal donate button](https://img.shields.io/badge/paypal-donate-yellow.svg?style=for-the-badge)](https://www.paypal.com/donate/?business=XVU35R3EPXQK2&no_recurring=0&currency_code=USD)
