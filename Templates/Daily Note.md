<%*
// Parses YYYY-MM-DD from the filename; falls back to today if untitled
const date = moment(tp.file.title, "YYYY-MM-DD", true).isValid()
  ? moment(tp.file.title, "YYYY-MM-DD")
  : moment();

// Maps each day of the week to your base workout schedule
const schedule = {
  Monday: "Full Body Strength",
  Tuesday: "Active Rest",
  Wednesday: "Volleyball (Cardio)",
  Thursday: "Full Body Strength",
  Friday: "Flexibility",
  Saturday: "Active Rest",
  Sunday: "Volleyball (Cardio)"
};
const dayName = date.format("dddd");
const todayWorkout = schedule[dayName];
-%>
---
type: daily-note
date: <% date.format("YYYY-MM-DD") %>
week: "[[<% date.format("YYYY-[W]WW") %>]]"
quarter: "<% date.format("YYYY-[Q]Q") %>"
year: "<% date.format("YYYY") %>"
workout_type: "<% todayWorkout %>"
workout_done: false
tags:
  - daily-note
---

# <% date.format("dddd, MMMM D, YYYY") %>

<< [[<% date.clone().subtract(1, 'days').format("YYYY-MM-DD") %>|Yesterday]] | [[<% date.format("YYYY-[W]WW") %>|Week <% date.format("WW") %>]] | [[<% date.clone().add(1, 'days').format("YYYY-MM-DD") %>|Tomorrow]] >>

> [!info] Today's Focus
> - **Planned Workout:** <% todayWorkout %>
> - **Top Priority:** 

---

## Interesting Things of the Day

1. 

## Accomplishments and Things to be Grateful For

1. 

## Tasks

- [ ]