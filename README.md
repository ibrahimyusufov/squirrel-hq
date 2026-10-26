# Squirrel HQ

A team hub web app for **FRC Team 2930, the Sonic Squirrels** (Snohomish, WA).

Meeting times and announcements on our team kept getting buried in group chats. Squirrel HQ puts the schedule, announcements and team info in one place for mentors, leads and students.

Built by Ibrahim Yusufov for the 2026 Congressional App Challenge (WA-01).

## Features

- **Schedule and RSVP:** every meeting, deadline and competition in one list. Members RSVP so leads know who's coming.
- **Meeting check-in:** on meeting day, members tap "I'm here." The app saves the time and shows how many people checked in. Nobody can check in for someone else.
- **Announcements:** urgent posts are flagged, and unread ones are marked until you've seen them.
- **Team chat:** channels for each subteam.
- **Ask Acorn:** an AI assistant that knows the team schedule, announcements and handbook, plus general FRC knowledge.
- **FRC news:** stories from Chief Delphi, The Blue Alliance and FIRST, shared by leads.
- **Robot CAD viewer:** spin the robot around in 3D, from an Onshape export (STL, OBJ or GLB).
- **Kickoff countdown** to the 2027 season.
- **Acorn Rush:** a small mini-game with a team leaderboard.
- **Accounts and roles:** mentors, leads and squirrels. Permissions are checked on the server, not just hidden in the app.

## How it's built

- One file: `squirrel-hq.html` (HTML, CSS and JavaScript, no framework)
- [three.js](https://threejs.org/) r128 for the 3D robot viewer
- Hosted as a Claude artifact on claude.ai, which provides sign-in, the shared database, file storage and the AI assistant

Because the app relies on claude.ai for accounts and data, opening the file directly in a browser shows the layout with team features offline.

## AI use

I used Claude (Anthropic) to build the first prototype and visual design from my feature ideas, fill in team information, shrink our Onshape CAD export for the viewer, and make the cover image.

What I did myself: came up with the idea and features, chose the team branding, tested it with our real team schedule and announcements, and coded the **meeting check-in** feature (`myCheckins`, `checkinCount`, `isToday`, `checkIn`, and the check-in button in `eventRow`), including finding and fixing its bugs.

## What's next

- Move off Claude onto its own backend so anyone can use it without a Claude account
- Native iOS and Android app with real push notifications
- Pull team results automatically from The Blue Alliance API
- Plug in our scouting app and add an hours tracker

*Have Fun! Build Fun! Be Fun!*
