# gitlab-team-dashboard

Gitlab dashboard for team activity tracking

Two tabs:

- opened MRs, assigned MRs, and assigned issues per user
- assigned issues for the whole team per (active, sorted by ascending due date) milestone

## Setup

```
$ npm i
$ cp cfg.json.dist cfg.json
```

Then edit `cfg.json` to suit your needs:

- `baseUrl`: domain name of your Gitlab instance (without a trailing slash)
- `token`: Gitlab token - you need to get one from your user account
- `usernames`: names of users you want to fetch data for
- `projectIds`: by default, only group milestones are fetched; enable project milestones individually here
- `labelsToExclude`: a regex to exclude issues bearing matching labels (leave blank to disable)

## Develop

```
$ npm start
```

Then browse `http://localhost:8080`.

## Build

### Local

```
$ npm run local
```

Then browse `file:///path/to/gitlab-team-dashboard/dist/index.html`.

### Production

```
$ npm run build
```

Then use your HTTP server of choice.
