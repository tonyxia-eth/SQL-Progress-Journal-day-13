# SQL-Progress-Journal-day-13

# ⚾ CS50 Moneyball SQL Review – Day 13: JOIN Mastery and Debugging

## ✅ Session Overview

Today was all about **pushing deeper into SQL JOINs**, debugging errors, and building true confidence in multi-table querying.

Even with a busy schedule, I made time for consistent practice and tackled 5 structured quizzes that tested my ability to:

- SELECT across multiple tables
- JOIN correctly using primary and foreign keys
- Filter results with WHERE
- Use ORDER BY properly for sorting
- Debug syntax errors in real-time
- Explore table structures smartly using `.schema`
- Think carefully about columns vs. tables

---

## 🧠 Key Skills Strengthened

- Clean JOIN syntax: `JOIN ... ON table1.id = table2.foreign_id`
- WHERE conditions chaining with `AND`
- ORDER BY specific columns ascending/descending
- Using `.schema` to find correct column names (e.g., `birth_year` instead of guessing)
- Debugging JOIN mistakes like wrong IDs or missing quotes
- Staying calm and fixing issues logically, not guessing

---

## 🛠️ Commands Practiced Today

```bash
sqlite3 moneyball.db
.tables
.schema players
.schema performances

SELECT players.first_name, players.last_name, performances.HR FROM players JOIN performances ON players.id = performances.player_id WHERE performances.year = 2000 AND performances.HR >= 40 ORDER BY players.last_name;

SELECT players.first_name, players.last_name, performances.HR FROM players JOIN performances ON players.id = performances.player_id WHERE players.birth_state = 'CA' AND performances.year = 2001 AND performances.HR >= 30 ORDER BY performances.HR DESC;

SELECT players.first_name, players.last_name, performances.RBI FROM players JOIN performances ON players.id = performances.player_id WHERE players.birth_country = 'USA' AND performances.RBI >= 100 AND performances.year = 1999 ORDER BY performances.RBI DESC LIMIT 5;

SELECT players.first_name, players.last_name, performances.SB FROM players JOIN performances ON players.id = performances.player_id WHERE players.birth_year = 1972 AND performances.year = 2001 AND performances.SB > 20 ORDER BY performances.SB DESC LIMIT 5;


🌱 Reflections
Today was about growth through persistence:
I made mistakes — wrong JOINs, wrong columns, typos — but I debugged every time by thinking through .schema and checking the database structure instead of guessing.

Every single correction made me stronger.

By the end of the session, I was able to solve tricky JOIN challenges on the first or second try — something that felt overwhelming only a few days ago.
