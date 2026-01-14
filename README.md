# 📘 Task Manager App

Yksinkertainen **Jetpack Compose** ‑pohjainen tehtäväsovellus.  
Sovelluksessa voit lisätä tehtäviä, merkitä niitä tehdyiksi, suodattaa ja järjestää listaa sekä palauttaa alkuperäisen näkymän.

---

## Features

### ✔️ Add Task
- Lisää uusi tehtävä tekstikentän kautta.
- Sovellus antaa automaattisesti **uniikin ID:n**.

### ✔️ Toggle Done / Undo
- Jokaisella tehtävällä on nappi:
  - **Undone** → merkitsee tehtävän tehdyksi  
  - **Done** → palauttaa tehtävän ei‑tehdyksi
  - Eli napit näyttää myös tehtävän tilan.
- Emoji näyttää tilan:
  - ❌ = ei tehty  
  - ✔️ = tehty

### ✔️ Sort by Due Date
- Järjestää tehtävät eräpäivän mukaan.
- Painamalla uudestaan palautuu alkuperäinen järjestys.

### ✔️ Show Only Done Tasks
- Näyttää vain tehtävät, joiden `done == true`.
- Painamalla uudestaan palautuu koko lista.

### ✔️ Smart State Logic
Sovellus käyttää kolmea tilaa:

- `backUpList` → sisältää **kaikki tehtävät**, aina ajan tasalla  
- `taskList` → näkyvä lista (suodatettu, järjestetty tai alkuperäinen)  
- `activeFilter` → `"sort"`, `"done"` tai `null`  

Tämä varmistaa, että:
- toggle toimii myös suodatetussa näkymässä  
- muutokset eivät katoa  
- näkymä ei vaihdu väärään listaan  

---

## 📂 Project Structure

