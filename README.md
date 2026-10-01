# MessyMobility · SG Crowd Analysis

An interactive dashboard that finds **where and when a Singapore neighbourhood's crowd
rose sharply above its own normal range** in July 2026, then reads each crowd for **who
came, where they travelled from, and what likely drew them**.

**▶ Live dashboard:** https://brettlim2.github.io/messymobility-sg-crowd-analysis/

## What it shows

- **12 crowd spikes** across the heartland, CBD, an industrial estate and weekends — big
  concert and stadium venues are filtered out to focus on community life.
- For each spike: a **crowd-vs-normal time chart** (that day's hourly crowd against the
  typical same-weekday range), **who came** (behavioural segments and life-stage), **where
  from** (home areas, with origin→event flow lines on the map), how local the crowd is, and
  the share of first-time visitors.
- A **likely cause** for each, labelled by confidence — from *confirmed* (e.g. the
  President's Challenge run at Jurong Lake Gardens) through *likely* recurring draws (pasar
  malams, GetActive! carnivals) down to *unexplained*.
- A **rail-node check** for context, and a plain-language note on how reliable the detector is.

## Method, in brief

Movement is aggregated to ~150 m cells by hour. A spike is a cell whose **share of all
island movement** in that hour rose far above its own same-hour-of-week normal (so busy or
quiet days island-wide don't create false events). Adjacent spiking cells are grouped into a
single event and the window trimmed to the main burst. Crowd make-up and home origin are
drawn from the people whose home area can be placed, then weighted so under-represented
neighbourhoods count fairly.

## Privacy

Figures are **panel devices, not head counts** (the panel represents roughly 1 in 40
residents). Nothing identifies an individual; any figure covering fewer than 5 devices is
hidden. The page is fully self-contained — all data is baked in, there are no trackers and
no external calls beyond web fonts.

---

© MessyMobility. Built as a static, cached snapshot for July 2026.
