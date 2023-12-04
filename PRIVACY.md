# Privacy Policy

Vajk Hermecz ("Me", "Myself", and "I") built AoC NoRush (the "app"). This service is provided by myself and is intended for use as is.

This Privacy Policy explains the types of data the app collects and how it processes and protects that data in connection with the service offered.

The collected information is required for the service to work.

## Information collection and use

When installing the browser extension you grant it access to the following information:

- First opening times of AoC daily challenges and your user ID:
  - This is persisted in the backend service.
  - This is shared with other AoC users using this service and having access to the same private leaderboards.
- Your AoC session ID:
  - Your session ID is used to authenticate that you are an AoC user, and to retrieve your ID and private leaderboard memberships
  - How is this done: The backend calls the `/leaderboard/private` endpoint and extracts your user ID and the list of private leaderboards you are a member of.
  - Why is this done: To ensure that you are not impersonating another user. To ensure that no others can access your data than users who are on the same private leaderboards with you.
  - Security
    - The session ID is NOT persisted in its RAW form anywhere.
    - On the first request:
      - User ID and private leaderboard membership is retrieved from the AoC backend
      - SHA-256 hash of your session ID is persisted in the backend's database
    - On subseqent requests: The SHA-256 hash of the session ID is used to authenticate your user

## Sharing of data with 3rd party services

The app's backend is hosted on [AWS](http://aws.amazon.com/console/). No user data is persisted besides the databased used to serve API requests.

Data is only shared with other AoC users having access to the same private leaderboard.

For the purpose of error tracking, error stacks are shared with [Sentry](https://sentry.io/) ([Privacy notice](https://sentry.io/privacy/)).

## Security

Data between the browser extension and the backend is sent over HTTPS.

AWS's infrastructure is used to protect the backend.

GitHub's Dependabot keeps the backend code up to date and free of known vulnerabilities.

## Consent

By using the browser extension, you hereby consent to this Privacy Policy and agree to its Terms and Conditions.

## Changes to this privacy policy

I may occasionally update this Privacy Policy to reflect company and customer feedback. If there are any updates, I'll inform you by initiating a pull request on this repository, which will remain open for a minimum of 14 days, providing an opportunity for you to express any objections. These updates become effective immediately upon their integration into the main branch. I encourages you to periodically review this Privacy Policy to be informed of how we protecting your information.

## Contact

If you have any questions or suggestions regarding this privacy policy, do not hesitate to [contact me](https://github.com/vhermecz/aoc-norush).
