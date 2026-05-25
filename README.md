<div align="center">

<img src="assets/banner.png" alt="Odd Brawlhalla" width="100%" />

<h1>Odd Brawlhalla</h1>

<p><strong>Browse, recolor, and bring your own art to every Brawlhalla legend — right on your desktop.</strong></p>

<p>
  <a href="https://github.com/odd999/Odd-Brawlhalla/releases/latest">
    <img alt="Latest release" src="https://img.shields.io/github/v/release/odd999/Odd-Brawlhalla?style=for-the-badge&color=ff6a00&label=Download" />
  </a>
  <a href="https://github.com/odd999/Odd-Brawlhalla/releases">
    <img alt="Downloads" src="https://img.shields.io/github/downloads/odd999/Odd-Brawlhalla/total?style=for-the-badge&color=00b4d8" />
  </a>
  <img alt="Platform" src="https://img.shields.io/badge/Windows-10%2F11-0078D6?style=for-the-badge&logo=windows&logoColor=white" />
  <img alt="License" src="https://img.shields.io/badge/Free%20to%20use-personal-22c55e?style=for-the-badge" />
</p>

<p>
  <a href="https://github.com/odd999/Odd-Brawlhalla/releases/latest"><b>Download Setup.exe</b></a>
  &nbsp;·&nbsp;
  <a href="#features"><b>Features</b></a>
  &nbsp;·&nbsp;
  <a href="#how-it-works"><b>How it works</b></a>
  &nbsp;·&nbsp;
  <a href="#mod-responsibly"><b>Mod responsibly</b></a>
  &nbsp;·&nbsp;
  <a href="#support-the-project"><b>Support</b></a>
</p>

</div>

---

## What is Odd Brawlhalla?

**Odd Brawlhalla** is a free Windows app that lets you explore the art behind every playable Brawlhalla legend, recolor any costume, replace individual shapes with your own artwork, and export the result as a modded `.swf` you can load into the game.

It reads your installed game directly — no separate dumps, no command-line tinkering — and gives you a clean, two-tier browser to dive from a legend straight into the editor.

> Built by a fan, for fans. Not affiliated with Blue Mammoth Games or Ubisoft.

---

## Screenshots

<table>
  <tr>
    <td align="center" width="50%">
      <img src="assets/screenshot-browser.png" alt="Legend and costume browser" /><br/>
      <sub><b>Two-tier browser</b> — pick a legend, see every costume.</sub>
    </td>
    <td align="center" width="50%">
      <img src="assets/screenshot-editor.png" alt="Costume editor" /><br/>
      <sub><b>Editor</b> — live SVG preview, color schemes, shape replace.</sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%">
      <img src="assets/screenshot-recolor.png" alt="Recolor in progress" /><br/>
      <sub><b>Recolor</b> — apply any of the 75 in-game color schemes.</sub>
    </td>
    <td align="center" width="50%">
      <img src="assets/screenshot-export.png" alt="Export to SWF" /><br/>
      <sub><b>Export</b> — write a clean modded SWF, PNG, or SVG.</sub>
    </td>
  </tr>
</table>

---

## Features

- **Every legend, every costume.** A curated catalog of all 68 playable legends and 764 costumes, including crossovers (Lara Croft, Master Chief, Rayman, Shovel Knight, Po, Hellboy, Finn & Jake, and more).
- **Native SVG preview.** Costumes render as crisp vector art that scales to any zoom level — no blurry pixel previews.
- **Live recoloring.** Switch between any of the 75 official color schemes, or build a custom palette, and see it on the legend instantly.
- **Bring your own art.** Draw or paint a piece in any tool (Photoshop, Krita, Inkscape, Procreate, even MS Paint), import the PNG or SVG, and the app drops your artwork straight into the costume — with full vector round-trip and a clean modified `.swf` on export.
- **Shape-level editing.** Click any body part to select the exact underlying SWF shape; replace it with your own art, recolor it, or hide it — without touching the rest of the costume.
- **Pose-aware compositing.** Silhouette hit-testing lets you click directly on a body part to select the underlying bone and slot.
- **Default-skin-first ordering.** Every legend's grid leads with the canonical costume, so you always know what "stock" looks like.
- **One-click updates.** The app self-updates via [Velopack](https://github.com/velopack/velopack); just hit "Check for updates" or wait for the next launch.
- **Clean Windows installer.** A single `Setup.exe`, no admin rights required, installs to your local profile.

---

## Download and install

1. [Download the latest Setup.exe](https://github.com/odd999/Odd-Brawlhalla/releases/latest)
2. Run the installer (Windows 10 or 11).
3. On first launch, point it at your Brawlhalla install folder (e.g. `C:\Program Files (x86)\Steam\steamapps\common\Brawlhalla`).
4. Browse, recolor, export.

> **A note on SmartScreen.** The v1 builds are unsigned, so Windows may show a *"Windows protected your PC"* dialog the first time you run `Setup.exe`. Click **More info → Run anyway**. Code signing is on the roadmap.

---

## How it works

```
┌──────────────────────┐     ┌─────────────────────┐     ┌──────────────────────┐
│  Legends grid        │ ──▶ │  Costumes grid      │ ──▶ │  Editor              │
│  (68 legends)        │     │  (default first)    │     │  · SVG preview       │
└──────────────────────┘     └─────────────────────┘     │  · Color schemes     │
                                                         │  · Shape replace     │
                                                         │  · Export SWF/PNG/SVG│
                                                         └──────────────────────┘
```

Under the hood, Odd Brawlhalla reads your `Game.swz` and `Init.swz` archives in place (read-only) to discover characters, costumes, bones, and color schemes, then composes a live SVG preview from the game's own vector art. When you export, it writes a fresh `.swf` you can drop next to the original.

The app never modifies `Game.swz` or `Gfx_Hands.swf` — those are off-limits to protect your install and avoid cross-legend palette pollution.

---

## Mod responsibly

Blue Mammoth Games (the studio behind Brawlhalla) allows cosmetic modding as long as the mods don't give a competitive advantage and don't hurt the company's income. You can play with your modded skins — including online — without worrying about EAC bans.

That permission comes with one rule the modding community takes very seriously:

> ### Only mod paid skins. Never mod default (free) skins.

The community calls modding free skins **"default modding"**, and treats it as piracy. Here's why it matters:

- **Blue Mammoth funds Brawlhalla largely through paid-skin purchases.** Skin sales are how a small studio keeps the game free to play.
- **Modding a default skin to look like a paid one breaks that paywall.** It produces the "why buy when I can mod it for free?" mindset — the textbook definition of piracy.
- **If default modding spreads, BMG may pull modding support altogether** and ruin it for everyone, including the legitimate modders who follow the rules.

**What to do instead:** if you want a cooler look for your favorite legend, buy a paid costume first, then mod *that*. You support the devs, you get a cool skin, and you keep the modding scene alive.

> Read the full rationale in the Brawlhalla Modding Community Discord's `#default-modding` channel. The "default skin lock" on the [roadmap](#roadmap) will enforce this rule at the tool level.

---

## Tech and stack

- **.NET 8** and **Avalonia UI** (cross-platform XAML UI toolkit)
- **Velopack** for the Windows installer and auto-update
- Bundled open-source libraries from the Brawlhalla modding community (all MIT) — see [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md)

---

## Roadmap

- [ ] **Default-skin lock** — block modding of default (free) skins at the tool level, so users can't accidentally break Blue Mammoth's paywall. (See [Mod responsibly](#mod-responsibly) for the *why*.)
- [ ] **Authenticode code signing** — eliminate the first-run SmartScreen warning.

Have an idea? [Open an issue.](https://github.com/odd999/Odd-Brawlhalla/issues/new)

---

## Credits

Odd Brawlhalla stands on the shoulders of the Brawlhalla modding community. Particular thanks to:

- **moffel1020** and **AllHailCheese** for the WallyMapEditor, WallyMapSpinzor2, BrawlhallaSwz, SwiffCheese, AbcDisassembler, and WallyAnmSpinzor libraries that decode the SWZ container, the SWF shape data, and the animation format.
- Everyone on **GameBanana** who documented the manual modding workflow long before tools like this one existed.

Brawlhalla © Blue Mammoth Games / Ubisoft. This project is fan-made and unaffiliated.

---

## Support the project

If Odd Brawlhalla saved you time, a small donation goes a long way:

<p>
  <a href="https://www.paypal.com/donate/?business=moalketbi9@gmail.com">
    <img alt="Donate via PayPal" src="https://img.shields.io/badge/PayPal-Donate-0070ba?style=for-the-badge&logo=paypal&logoColor=white" />
  </a>
</p>

---

## License

Odd Brawlhalla is free to use for personal, non-commercial purposes. You can download it, install it, and share the unmodified installer with others — no charge, no signup, no account.

The app itself is closed source. You may not sell it, repackage it, or reverse-engineer it. See [LICENSE](LICENSE) for the full terms.

Odd Brawlhalla bundles several open-source projects from the Brawlhalla modding community, all MIT-licensed. Their copyright notices and the projects they come from are listed in [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md). Each of those components remains under its own MIT license.

<div align="center">
  <sub>Built by <a href="https://github.com/odd999">Odd</a>.</sub>
</div>
