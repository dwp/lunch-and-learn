# Lunch and Learns Site

[![build status](https://gitlab.itsshared.net/software-engineering-community/lunch-and-learn-site/badges/master/build.svg)](https://gitlab.itsshared.net/software-engineering-community/lunch-and-learn-site/commits/master)

A site, built using Middleman, to provide information on upcoming, and past, Lunch and Learn sessions.

https://software-engineering-community.pages.itsshared.net/lunch-and-learn-site/

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
