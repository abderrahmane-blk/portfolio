# Portfolio

Software projects I've built over the past five years, most of them in the last three. This repo is an index: every folder has its own README with the problem, the stack, the design decisions, and screenshots or terminal recordings where they help.

I hold a master's degree in networking and distributed systems.

**What this is not:** my portfolio website (I haven't built that yet), and not everything I've ever made. It's the subset I'm confident in and allowed to show.

## How these were built

Some were written without AI. Some were written with AI doing the typing while I supervised, reviewed and steered it. I'd rather say that up front than let you guess.

---

## Projects

### Nedjmou Hotel — rental & reservation manager _(in production)_

`Flutter` · local database

A business owner rents apartments and needed to run his reservations from one place. Confirmed bookings marked in pen, tentative ones in pencil, no overlapping confirmed stays, per-night pricing, customer notes, three languages (Arabic / French / English), one-click sharing of house photos and locations to Telegram, Snapchat, Messenger, and a large statistics page covering occupancy, money, guests and errands.

He asked for a fixed set of apartments; I made it dynamic. He asked for a chart of free/occupied; it shows free, occupied, occupied-and-confirmed, and by how many overlapping customers at any date.

It's in production and he uses it.

I also loaded the database with 10+ years of data — more than he'd fill in 30 — and measured it: no unbounded reads (one sanctioned `SELECT * FROM houses`), no N+1, slowest single query 33 ms, a full browsing session at 161 queries / ~1.5 s of database time.

→ [README with screenshots](https://./nedjmou_hotel)

### DALTI (دالتي) — queue & reservation platform

`C# (.NET Core)` · `PostgreSQL` · `Redis` · `SignalR` · `Flutter` · `Svelte`

Real-time reservation and queue management for medical clinics and public institutions. High-concurrency backend, real-time updates, and three clients (for the mvp version , but will be more): Flutter desktop for businesses, Flutter mobile and Svelte web for end users.

**Status:** postponed for now — not for a technical reason — and meant to be picked up again later. The architecture and the confidential parts won't be published here.


### Mini blockchain network

`Python` · `FastAPI` · `Electron`

A bitcoin-inspired network built from scratch. Every node is a separate process with its own port and its own copy of the chain. They find each other, broadcast transactions, mine, and vote on which block gets committed — all over HTTP. Multi-receiver transactions, merkle root, proof of work, and a majority vote that settles the case of two miners finding a block for the same slot.

The source code isn't in the repo. I'm happy to walk through the code and the design on a call.

→ [README with the full run, node by node](https://./mini-blockchain-network)


### Vigenère cipher & modular exponentiation

`Python`

A CLI with two halves: modular exponentiation using Fermat's little theorem, and Vigenère ciphering/deciphering built on top of it. The README explains why `base ** exponent % n` isn't an option and what happens if you try it in Python.

→ [README](https://./vigenere-modular-math)



### Desktop media downloader

`Python` · `PySide6` · `yt_dlp`

A desktop app for downloading YouTube videos and entire playlists at a chosen quality — up to 4320p, or audio only. Paste a link, pick quality and folder (both rememberable), download.

I built it because I had limited internet in the dorm and every free option I found either charged or capped the resolution at the paid tier. It worked fine through those years.

Heads-up: it's an old project, so `yt_dlp` has likely moved on and it needs a small fix to run today.

→ [README with screenshots](https://./desktop-media-downloader)


## Also in here, not documented yet

- **Wumpus** — a small 2D game in Python. An early attempt at writing a game.
    
- **AI web playground** — a Flask site wrapping the AI APIs that existed at the time: text-to-image, text generation streamed letter by letter, and a few more.
    

## Layout

One folder per project, each with its own `README.md` covering the problem, the stack and the design decisions. The two above are still being written.