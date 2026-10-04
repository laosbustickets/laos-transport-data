---
license: cc-by-4.0
pretty_name: Laos Transport Data
language:
- en
tags:
- laos
- transport
- railway
- train-timetable
- border-crossings
- bus-routes
- maps
---

# Laos Transport Data

Open data from [Laos Bus Tickets](https://laosbustickets.com/): border checkpoints, bus,
train and flight routes, the Laos–China Railway timetable and the Laos transport map.
**laosbustickets.com is the original source**; this repository is a copy, synced every day
by a GitHub Action. If the two ever differ, trust the website, and please cite its pages.

| File | What it is | Updated | Canonical page |
|---|---|---|---|
| `laos-train-timetable.json` | Every passenger train on the Laos–China Railway for the next 7 days: stations, arrival and departure times, running days, through trains to Kunming. Read every morning from the official LCR Ticket app of the Laos-China Railway Company. | Daily, 06:00 Laos time | [Laos train timetable](https://laosbustickets.com/train-tickets-laos/#timetable) |
| `routes.json` | Bus, train and flight routes to, from and within Laos: border crossing used, duration, indicative fare, whether it can be booked online. | When routes change | [All routes](https://laosbustickets.com/routes/) |
| `checkpoints.json` | Every checkpoint on the Lao Department of Immigration's register: hours, visa on arrival and eVisa status, coordinates, per-checkpoint verified date. | Weekly check | [Laos border checkpoints](https://laosbustickets.com/laos-border-checkpoints/) |
| `maps/laos-transport-map-<lang>.svg` | The Laos transport map in 7 languages (en, fr, de, es, ja, ko, ru), portrait and `-landscape`. | When routes or crossings change | [Laos transport map](https://laosbustickets.com/laos-transport-map/) |

## The timetable file

- `checkedAt`: when the timetable was last read from the railway's app (UTC). If a daily
  check fails, the previous timetable is kept, so this date tells you how fresh it is.
- `dates`: the days covered (the app sells tickets 7 days ahead).
- `trains[]`: `train` (D88, C95, K11…), `direction`, `from`, `to`, `runsOn` (dates),
  `weekdays`, `weekdaysNotOnSaleYet` (days the app has not opened yet, not days the train
  does not run), and `stops[]` with `station`, `code`, `country`, `arrive`, `depart` and
  `utcOffset` (Laos UTC+7, China UTC+8).

## Licence and citation

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Credit "Laos Bus Tickets
(laosbustickets.com)" and link the canonical page above. For example:
Laos Bus Tickets, "Laos–China Railway timetable", https://laosbustickets.com/train-tickets-laos/.

More about the data and how it is checked: https://laosbustickets.com/sources/#open-data
