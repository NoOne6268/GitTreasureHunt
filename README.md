# 🗺️ Git Treasure Hunt

Welcome adventurer!  
You’re about to go on a journey through **Git history** to uncover a hidden treasure 🎉.  
But beware: the past is full of **wrong turns** and **clues**.  

This activity will teach you how commits work, how to view history, and how to recover from mistakes.  

---

## 🚀 Step 1 — Begin Your Hunt

Clone the repository with only the latest commit:

```bash
git clone --depth=1 <repo-url>
cd git-treasure-hunt
```

Now check the log:

```bash
git log --oneline
```

👉 You should see **one commit only**.
That’s your starting point.

---

## 🕵️ Step 2 — Dig Deeper

The history is hidden. To reveal more commits from the past, you must fetch deeper:

```bash
git fetch --depth=2
git log --oneline
```

Now you’ll see **two commits**.
Read the **latest clue** in the history.

Every time you dig deeper, increase the depth by 1:

```bash
git fetch --depth=3
git log --oneline
```

Then:

```bash
git fetch --depth=4
git log --oneline
```

Keep going: `--depth=5`, `--depth=6`, … until you reach the beginning.

---

## � Step 3 — Follow the Clues

* Some commits are **wrong turns**.
   They may contain junk files.
   Their commit message will tell you how to **get back on track**
   (e.g., run `git checkout <hash>` of the last good commit).

* Other commits are **clues**.
   They’ll guide you further into the past.

* At one point, a clue will ask you to **make your own commit**.
   Do it with:

   ```bash
   echo "I’m part of the treasure hunt!" > mynote.txt
   git add mynote.txt
   git commit -m "My treasure hunt commit"
   ```

   Then check:

   ```bash
   git log --oneline
   ```

   You’ll see your commit added to history 🎉.

---

## 🏆 Step 4 — Claim the Treasure

When you finally reach the **oldest commit** (after fetching with `--depth=9`),
you’ll find the file:

```
treasure.txt
```

Open it to reveal the hidden message:

```
🎉 Congrats! You found the treasure!
```

That’s the end of your hunt 🗡️✨.

---

## 💡 Pro Tips

* Run `git log --oneline` often to see your progress.
* Use `git checkout <commit-hash>` to explore what files existed in each commit.
* Don’t skip straight to the end — the fun is in the journey!
* Wrong commits aren’t failures — they’re lessons in how to recover and move on.

---

Good luck, explorer. The treasure awaits! 🚀

