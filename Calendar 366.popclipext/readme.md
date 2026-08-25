# Calendar 366 for PopClip

Turns selected text into an event or a task in [Calendar 366](https://calendar366.com).

Select some text anywhere on your Mac and click the Calendar 366 button in the
PopClip bar. Two entries open up:

| Entry | Action |
|---|---|
| New Event | Create an **event** from the selection |
| New Task | Create a **task** from the selection |

The entry is created straight away — no window opens, no confirmation is needed.

“New Event” only shows up when the selection contains something that looks like a
date or a time: a clock time, a numeric date, a weekday, or a word such as “today”
or “tomorrow”. An event without a date would have nothing to be filed under, so the
entry stays out of the way. “New Task” is always available — a task without a due
date simply lands in your list.

## Requirements

Calendar 366 for Mac must be installed and unlocked. The extension hands the text
to the app through its `cal366://` URL scheme.

## Natural language

The selected text is not just used as the title. Calendar 366 reads dates, times
and a few shorthand tokens out of it — the same syntax the title field inside the
app understands. Everything in front of the first recognised token becomes the title.

| You select | You get |
|---|---|
| `Lunch with Anna tomorrow 12:30` | Event tomorrow at 12:30 |
| `Dentist next monday 9am -45` | Event lasting 45 minutes |
| `Team sync friday 10:00 -a15m -r1w` | Weekly event with an alert 15 minutes before |
| `Call the landlord !!` | Task with medium priority |
| `Groceries /Home` | Task in the list whose name starts with “Home” |

### Tokens

| Token | Meaning |
|---|---|
| `/Name` | Target calendar (events) or list (tasks). Matches the first visible one whose name starts with `Name`. |
| `-30` | Duration in minutes. Events only, needs a space in front of it. |
| `-a30m`, `-a2h`, `-a1d` | Alert 30 minutes / 2 hours / 1 day before. Events only, can be used more than once. |
| `-r1d`, `-r2w`, `-r1m`, `-r1y` | Repeats every 1 day / 2 weeks / 1 month / 1 year. |
| `!`, `!!`, `!!!` | Low, medium or high priority. |

A web address in the selection is attached as a link, a phone number is put into
the notes. Anything left over after the date is taken as the location.

## Note

A selection consisting of a single word cannot be interpreted and opens an empty
editor instead — select at least two words.

## Credits

By Vincent Miethe — [calendar366.com](https://calendar366.com)
