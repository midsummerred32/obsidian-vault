<%*
// Parses the week from the file title (e.g., 2026-W48); falls back to current date if untitled
const baseDate = moment(tp.file.title, "YYYY-[W]WW", true).isValid() 
  ? moment(tp.file.title, "YYYY-[W]WW") 
  : moment();
const monday = baseDate.clone().startOf('isoWeek');
-%>
---
type: weekly-note
week: <% monday.format("YYYY-[W]WW") %>
start_date: <% monday.format("YYYY-MM-DD") %>
end_date: <% monday.clone().add(6, 'days').format("YYYY-MM-DD") %>
tags:
  - periodic/weekly
---

# Week <% monday.format("WW") %> — <% monday.format("MMM D") %> to <% monday.clone().add(6, 'days').format("MMM D, YYYY") %>

<< [[<% monday.clone().subtract(7, 'days').format("YYYY-[W]WW") %>|Last Week]] | [[<% monday.clone().add(7, 'days').format("YYYY-[W]WW") %>|Next Week]] >>

---

## 🎯 Top Priorities & Goals
- [ ] 
- [ ] 
- [ ] 

## 📅 Week at a Glance
- **Monday (<% monday.format("MM/DD") %>):** 
- **Tuesday (<% monday.clone().add(1, 'days').format("MM/DD") %>):** 
- **Wednesday (<% monday.clone().add(2, 'days').format("MM/DD") %>):** 
- **Thursday (<% monday.clone().add(3, 'days').format("MM/DD") %>):** 
- **Friday (<% monday.clone().add(4, 'days').format("MM/DD") %>):** 
- **Saturday (<% monday.clone().add(5, 'days').format("MM/DD") %>):** 
- **Sunday (<% monday.clone().add(6, 'days').format("MM/DD") %>):** 

---

## 💪 Workout Schedule

| Day       | Date | Exercise | Done |
| --------- | ---- | -------- | ---- |
| Monday    | <% monday.format("MM/DD") %> | | [ ] |
| Tuesday   | <% monday.clone().add(1, 'days').format("MM/DD") %> | | [ ] |
| Wednesday | <% monday.clone().add(2, 'days').format("MM/DD") %> | | [ ] |
| Thursday  | <% monday.clone().add(3, 'days').format("MM/DD") %> | | [ ] |
| Friday    | <% monday.clone().add(4, 'days').format("MM/DD") %> | | [ ] |
| Saturday  | <% monday.clone().add(5, 'days').format("MM/DD") %> | | [ ] |
| Sunday    | <% monday.clone().add(6, 'days').format("MM/DD") %> | | [ ] |

> [!success] Requirements
> - [ ] Full Body Strength (1/2)
> - [ ] Full Body Strength (2/2)
> - [ ] Cardio
> - [ ] HIIT
> - [ ] Flexibility

---

## 📋 Weekly Backlog & Tasks
### Academic / Work
- [ ] 

### Personal / Home
- [ ] 

---

## 🔄 Weekly Review
> [!note]- End-of-Week Reflection
> **Wins & Highlights:**
> - 
> 
> **What could have gone better?**
> - 
> 
> **Carry over to next week:**
> -