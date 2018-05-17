# Lunch and Learns Site

[![build status](https://gitlab.itsshared.net/engineering-community/lunch-and-learn/badges/master/build.svg)](https://gitlab.itsshared.net/engineering-community/lunch-and-learn/commits/master)

A site, built using Middleman, to provide information on upcoming, and past, Lunch and Learn sessions.

https://engineering-community.pages.itsshared.net/lunch-and-learn/

Currently under active development.

## Continuous Deployment

The site is rebuilt, via Gitlab CI, each time a push to `master` is made. This ensures the most recent version of the site is always published and available.

### Scheduled Rebuild

The site is rebuilt, each night, so that sessions move into the appropriate upcoming/today/previous sections of the site.

## Session Data

All session data is kept in `data/sessions.yml`, which is used to generate the frontend. Whenever the site is rebuilt, the sessions will be shown in the appropriate section (upcoming/today/previous).

*Important:* the sessions should be added in date order, otherwise they will appear out of order in the upcoming/previous tables.

Each session object should following this format:

```
- title: "Subject of the session"
    presenter: "Who is talking"
    date: "20180123"
    time:
      start: "13:00"
      end: "14:00"
    location: "Where it is taking place"
```

# Contributing

If you would like to contribute to the project, or simply add a lunch and learn session, you should make your changes on a feature branch (`feature/my-branch-name`). Once ready, create a merge request targetting the `develop` branch. Once approved, the approver will merge the changes and push to `master` as appropriate.
