# site-monitor

Uptime alarms for sites West Product Development looks after. Each workflow in
`.github/workflows/` checks a public web address on a schedule. When a site
stops answering, the run fails and GitHub emails Brian.

This repository is public because GitHub Actions minutes are free for public
repositories. Nothing in it is secret: only public URLs and the checks run
against them.

| Workflow | Checks | How often |
|---|---|---|
| `spaamfaa-members.yml` | members.spaamfaa.org sign-in and home pages | every 30 minutes |
| `keepalive.yml` | stops GitHub switching the schedules off after 60 quiet days | 1st of each month |

To add another site, copy `spaamfaa-members.yml`, change the URLs and the text
the page must contain, and push.
