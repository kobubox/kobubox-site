<!--
Styling notes for the whole page:
- Overall vibe: soft, cozy, “squishmallow” energy.
- Use rounded corners, generous padding, soft pastel background.
- Headings: Fredoka or similar rounded font.
- Body text: Inter or Nunito.
- Accent colours: soft blues, mint greens, warm yellows.
-->

# KobuBox

<!-- HERO SECTION
- Layout: two columns on desktop:
  - Left: text (logo, headline, subheadline, CTA buttons).
  - Right: illustration of Kobu (squishy mascot) + device sketch.
- Background: very light pastel.
-->

## Scan a card. Start an adventure.

KobuBox is a little, squishy-friendly device that lets kids play stories and music by scanning printed cards — **no glowing screen, no locked-in ecosystem, just magic powered by the media you already own**.

It’s designed to feel more like a favourite toy than a gadget.

**KobuBox is:**

- Screen-lite and kid-friendly  
- Built around printable cards (QR/barcodes)  
- Designed to work with Sonos / Home Assistant / your existing subscriptions  
- A project you can tinker with, extend, and truly own  

**Status:** Early prototype.  
**Goal:** A cozy, hackable, screen-lite storyteller for families.

[Follow on GitHub](#follow) · [Get project updates](#follow)

---

<!-- SECTION: What is KobuBox?
- Simple, clear explanation.
- Use an icon row style: toy/device icon, card icon, house/smart-home icon.
-->

## What is KobuBox?

KobuBox is a **physical controller for kids** that lives somewhere between a toy, a story box, and a smart home remote.

At its core:

- A small box powered by an ESP32  
- A barcode/QR scanner on the front  
- A tiny e-paper display for calm feedback  
- A few buttons for lights and scenes  
- Wi-Fi connection to your home network and Home Assistant  

Kids **scan a card**. KobuBox **tells your smart home** what to do:

- Start an audiobook on a Sonos speaker  
- Play a favourite Spotify playlist  
- Trigger a bedtime scene with lights dimmed and a story playing  
- Kick off a morning routine with music and lights  

Everything happens locally. No cloud subscription. No lock-in.

---

<!-- SECTION: Why another kids audio device?
- Compare gently to Yoto/Tonies without naming if you prefer; here we can be explicit.
- Tone: empathetic parent, not ranty.
-->

## Why build another kids audio box?

There are already popular kids’ audio devices out there — Yoto, Tonies, and friends.  
They’re charming, but they come with trade-offs:

- ❌ Closed ecosystems and proprietary cards  
- ❌ Extra content purchases on top of subscriptions you already pay for  
- ❌ Cloud dependencies and opaque firmware  
- ❌ Hard or impossible to repair, modify, or extend  

KobuBox is a different bet:

- ✅ **Use what you already pay for**  
  - Audible, Spotify, Sonos favourites, local media, Home Assistant scenes…  
- ✅ **Printable cards, not expensive plastic**  
  - Print at home, decorate with the kids, replace easily.  
- ✅ **Open and hackable**  
  - Hardware and firmware are built to be inspected, modified, and repaired.  
- ✅ **Local-first and privacy-friendly**  
  - Designed to live happily inside your home network, not in someone else’s cloud.  

It’s a project for families who like the idea of a kid-friendly audio box,  
but **don’t** like being nudged into a content store forever.

---

<!-- SECTION: The Kobu character / squishmallow-style mascot
- Introduce the mascot as part of the narrative.
-->

## Meet Kobu 🫧

Kobu is the little squishy spirit of the box — think of a soft, round “squishmallow-style” buddy who lives inside your stories.

In the world of KobuBox:

- Kobu peeks over the top of the box in the logo  
- Kobu appears on cards, stickers, and the website  
- Kobu is curious, calm, and loves helping start new adventures  

As the project evolves, Kobu could:

- Show simple expressions on the e-paper display  
- Animate in little web illustrations  
- Become a character in printable story cards made by the community  

The idea is that **KobuBox isn’t just hardware — it’s a friendly companion** that kids recognise and trust.

---

<!-- SECTION: How it works (simple)
- Use a 3-step illustration style.
-->

## How KobuBox works (V1)

**1. Scan a card**  
You print a card with a QR code or barcode and a cute drawing.  
Kids scan it with the front-facing scanner module.

**2. KobuBox sends a message**  
The ESP32 firmware reads the code and sends a request to Home Assistant (or another local service) with the ID.

**3. Your home does the magic**  
Home Assistant maps that ID to:

- a Sonos media_player + media URL (Spotify, local file, audiobook, etc.), or  
- a scene (bedtime lights, cozy corner, reading nook), or  
- any other automation you dream up.

Meanwhile, the e-paper display can show:

- title of the story  
- a small icon or Kobu face  
- basic status (“Playing…”, “Paused”, “Next card?”)

---

<!-- SECTION: Vision / Dream
- High level “BHAG” vision but in friendly website language.
-->

## The dream for KobuBox

KobuBox started as a small hack project — but the long-term dream looks like this:

- 🃏 **Printable card packs**  
  - Bedtime stories, favourite albums, chore cards, routine cards, learning cards.  
  - Kids decorate them, parents map them to media.  

- 🧸 **A cozy, toy-like object**  
  - Soft curves, friendly face, sits happily on a shelf or nightstand.  
  - Feels more like a plush companion than a gadget.  

- 🔌 **Built from standard parts**  
  - ESP32, scanners, e-paper displays, buttons.  
  - Repairable and modifiable without a secret “official” repair program.  

- 🧩 **A platform, not a product trap**  
  - Open firmware and hardware docs.  
  - Community-made card sets, enclosures, forks.  
  - Variants with RFID, NFC, or built-in speakers.  

- 🕊 **No ads, no tracking, no dark patterns**  
  - Just a little box that plays stories and music, quietly doing its job.  

---

<!-- SECTION: Current prototype
- Simple, honest status update.
- Later you can embed real photos; for now it’s copy.
-->

## Where the project is today

Right now, KobuBox is in the **early prototyping** phase:

- ✅ ESP32 dev board up and running in Rust  
- ✅ Wi-Fi + simple HTTP server prototype  
- ✅ Basic LED + button control  
- 🔧 Integrating the GM65 barcode/QR scanner  
- 🔧 Bringing up the Waveshare 2.13" e-paper display  
- 🔧 First Home Assistant integration experiments (Sonos + scenes)  
- 🧠 Industrial design sketches & early thoughts on a cozy, “squishmallow-ish” enclosure  

This is still very much a work-in-progress laboratory project — but the foundations are coming together.

As things firm up, this site will show:

- Build logs  
- Wiring diagrams  
- 3D print files  
- Firmware releases  
- Example Home Assistant configs  

---

<!-- SECTION: Values / Philosophy
- Short and punchy.
-->

## What KobuBox stands for

KobuBox is guided by a handful of simple principles:

- **Kids deserve magic without addiction loops.**  
  Stories, music, and imagination — not infinite scrolling and autoplay feeds.

- **Families should own their devices.**  
  If it sits in your kid’s room, it shouldn’t depend on someone else’s cloud or business model.

- **Hardware should be repairable and hackable.**  
  If it breaks, you should have a fair chance of fixing it.  
  If you have ideas, you should be able to tinker.

- **Use the media you already pay for.**  
  Audible, Spotify, local files, etc. — no extra content store required.

- **Calm tech over loud tech.**  
  A tiny e-paper display and soft lights are enough.  
  The “wow” comes from stories, not animations.

---

<!-- SECTION: Roadmap
- Three columns: Now / Next / Future.
-->

## Roadmap

<!-- Styling: use a 3-column grid on larger screens. -->

### Now (Prototype)

- ESP32 firmware in Rust  
- Scanner + e-paper driver integration  
- Basic card → action mapping  
- Simple Sonos / Home Assistant demo  
- Early 3D-printed enclosure experiments

### Next (Maker-ready)

- First “KobuBox starter build” guide  
- Stable firmware + config examples  
- Card template generator (print-at-home)  
- Refinements to case design & kid-proofing  
- Documentation for hacking and extending

### Later (Big dream)

- Polished kits for makers & educators  
- Variants (battery-powered, built-in speaker, RFID/NFC version)  
- Community library of card sets and lesson ideas  
- Robust presence in the open hardware / Home Assistant ecosystem  

---

<!-- SECTION: Follow / community
- Invite people to star the repo, join an email list, or just lurk.
-->

## Follow the project <a id="follow"></a>

KobuBox is just getting started.  
If you’d like to watch it grow (or maybe build your own one day):

- ⭐ **Star or watch the project on GitHub**  
  - `github.com/kobubox` (exact link to be added)  

- 📬 **Join the mailing list / updates**  
  - (Put your preferred method here: newsletter, blog RSS, etc.)

- 💬 **Say hello / share ideas**  
  - (Link to your preferred contact: email, Mastodon, etc.)

Whether you’re a parent, maker, educator, or just someone who likes cozy open hardware, you’re very welcome here.

---

<!-- FOOTER
- Minimal, soft.
-->

KobuBox is an open, experimental project.  
Made with curiosity, coffee, and stories after bedtime. 🌙
