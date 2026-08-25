# Calendar 366 for PopClip

A PopClip extension that turns selected text into an event or a task in [Calendar 366](https://calendar366.com).

## Getting Started

1. Install the extension from its page in the PopClip Extensions directory. PopClip takes care of the download and of future updates.
2. Ensure Calendar 366 is installed on the same Mac.

## Capabilities

* Create an event from the selected text, including date, time and duration
* Create a task from the selected text, with or without a due date
* Choose the target calendar or list by name
* Set priority, alerts and a repeat interval from within the selection
* Attach a web address as a link and a phone number to the notes
* Take whatever follows the date as the location

Both entries sit behind a single Calendar 366 button in the PopClip bar. The entry is created straight away — no window opens, no confirmation is needed. “New Event” only appears when the selection contains something that looks like a date or a time, because an event without one has nothing to be filed under. “New Task” is always available, since a task without a due date simply lands in your list.

## Natural Language

The selected text is not just used as the title. Calendar 366 reads dates, times and a few shorthand tokens out of it — the same syntax the title field inside the app understands. Everything in front of the first recognised token becomes the title.

| You select | You get |
|---|---|
| `Lunch with Anna tomorrow 12:30` | Event tomorrow at 12:30 |
| `Dentist next monday 9am -45` | Event lasting 45 minutes |
| `Team sync friday 10:00 -a15m -r1w` | Weekly event with an alert 15 minutes before |
| `Call the landlord !!` | Task with medium priority |
| `Groceries /Home` | Task in the list whose name starts with “Home” |

| Token | Meaning |
|---|---|
| `/Name` | Target calendar (events) or list (tasks). Matches the first visible one whose name starts with `Name`. |
| `-30` | Duration in minutes. Events only, needs a space in front of it. |
| `-a30m`, `-a2h`, `-a1d` | Alert 30 minutes / 2 hours / 1 day before. Events only, can be used more than once. |
| `-r1d`, `-r2w`, `-r1m`, `-r1y` | Repeats every 1 day / 2 weeks / 1 month / 1 year. |
| `!`, `!!`, `!!!` | Low, medium or high priority. |

A selection consisting of a single word cannot be interpreted and opens an empty editor instead — select at least two words.

## Requirements

* macOS 14.6
* PopClip 2023.9 (build 4225) or later
* Calendar 366 v3.0.0 installed and unlocked on the same Mac

## Data Handling

The extension hands the selected text to Calendar 366 entirely on-device, through the app's `cal366://` URL scheme. The text never leaves your Mac.

## About This Repository

This repository hosts the extension package as published in the PopClip Extensions directory. The source code of the underlying application is maintained privately.

## Links

* Product: https://calendar366.com
* Documentation: https://calendar366.com/help/index.html#ext-popclip
* Privacy Policy: https://calendar366.com/about/privacy/
* Terms of Service: https://calendar366.com/about/legal/
