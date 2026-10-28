# Team Availability Tracker

A single-page prototype for seeing who is free, who is booked and where schedules clash, without a spreadsheet. Built with React and Tailwind, mobile friendly, no login and no backend.

Sample work items are fictional. The team starts with four people and you manage it yourself in the app.

## Run it

Open `index.html` in a browser. It loads React, Tailwind and fonts from public CDNs, so it needs an internet connection.

## What it does

- **Add work in seconds.** Title, team member, start and end dates, work type and status (In-Process, Confirmed, Tentative). Press `N` to open the form.
- **Calendar-first views.** A month calendar, a 14-day availability grid (7 days on phones) and a conflicts list. Select a date or item to see details, assigned people and status.
- **Automatic conflict detection.** The same person on overlapping dates is flagged in the form as you type, on the calendar and in the Conflicts tab.
- **Work types.** Project, Client work, Exhibition, Training, Review, Travel, In office, Medical leave, Vacation, Public holiday, All hands, Special event and Internal. Add your own with **New type**.
- **Singapore public holidays.** 2026 and 2027 from the MOM calendar, including substitute Mondays. They mark the whole team as unavailable.
- **Manage the team.** The **Team** button adds, renames and removes people. Removing someone also removes their calendar items. The team and all changes are saved in your browser.
- **Filters.** Filter by person, status, category (work, leave, in office, team-wide) or conflicts only, and by work type.
- **Calendar links.** Each item has Add to Google Calendar, Outlook and Microsoft 365 links. You can also import an `.ics` file exported from Google Calendar or Outlook, and copy the whole calendar as `.ics` text.

## How conflicts and availability work

- A conflict is one person with two overlapping commitments. Tentative items count.
- Leave and vacation block a person. Public holidays block everyone.
- All hands, special events and In office are shown but never block anyone or cause conflicts.

## Notes

- Data is stored in your browser (`localStorage`). Nothing is sent anywhere.
- Live two-way sync with Google or Microsoft is not included. It needs an account sign-in and a backend.
- Public holiday dates: [MOM 2026](https://www.mom.gov.sg/newsroom/press-releases/2025/0616-public-holidays-for-2026), [MOM 2027](https://mom.gov.sg/newsroom/press-releases/2026/0618-public-holidays-for-2027). The 2026 Hari Raya dates were marked subject to confirmation.
