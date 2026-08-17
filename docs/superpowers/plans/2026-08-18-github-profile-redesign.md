# GitHub Profile README Redesign Plan — Card-Based Terminal Dashboard

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Recreate the reference.png design — a dark-themed, card-based terminal dashboard with colored borders, progress bars, pixel art, and animations.

**Architecture:** Use HTML tables for multi-column grid layout, box-drawing characters for card borders, Unicode block characters for progress bars, emoji for colored accents, and external SVGs for animations. All within GitHub Markdown constraints (no CSS, no JavaScript).

**Tech Stack:** GitHub Markdown, HTML (table, details, img, picture, a, b, i, code, pre, br, p, div), external SVG animations (readme-typing-svg, Platane/snk), Unicode box-drawing characters, Unicode block elements.

**Spec:** reference.png (visual specification — card-based terminal dashboard)

## GitHub Markdown Constraints

- No `style` attributes (stripped by GitHub)
- No JavaScript (stripped)
- No CSS classes
- Allowed HTML: p, br, details, summary, img, picture, a, b, i, code, pre, kbd, sub, sup, hr, table, tr, td, th, thead, tbody, div (align), p (align)
- External images: SVG, PNG, GIF via img src
- Animations: only via external SVG services (readme-typing-svg, Platane/snk)

## Color Mapping (Reference → GitHub Approximation)

| Reference Color | Emoji | Unicode Block | Usage |
|----------------|-------|---------------|-------|
| Green (#00ff00) | 🟢 | `█` (green-tinted via context) | Borders, progress bars, accents |
| Purple (#a855f7) | 🟣 | `█` | Borders, accents |
| Cyan (#06b6d4) | 🔵 | `█` | Borders, accents |
| Pink (#ec4899) | 🔴 | `█` | Borders, accents |
| Yellow (#eab308) | 🟡 | `█` | Progress bars, accents |
| Dark background | — | — | GitHub default dark theme |

**Note:** GitHub doesn't support colored text or backgrounds via markdown. Colors are approximated via emoji and contextual positioning.

---

## Task 1: Create Grid Layout Structure

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: Reference image layout.
- Produces: HTML table structure for 3-column responsive grid.

- [ ] **Step 1: Design table structure**

Create HTML table with 3 columns for desktop. Each cell will contain a card.

```html
<table>
  <tr>
    <td>Hero card</td>
    <td>Pac-Man card</td>
    <td></td>
  </tr>
  <tr>
    <td>System diagnostics</td>
    <td>GitHub contribution</td>
    <td>Now building</td>
  </tr>
  <tr>
    <td>Inventory</td>
    <td>Achievements</td>
    <td>Terminal chat</td>
  </tr>
</table>
```

- [ ] **Step 2: Add table styling via GitHub-compatible attributes**

Use `cellpadding`, `cellspacing`, `border` attributes for basic spacing.

- [ ] **Step 3: Test table rendering**

Verify table renders correctly on GitHub (3 columns, proper spacing).

---

## Task 2: Implement Hero Card

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: Reference image hero section.
- Produces: Hero card with terminal window, name, tagline, loading bar, avatar.

- [ ] **Step 1: Create card border with box-drawing characters**

```
┌─[ yash@github:~ ]────────────────────────────────────┐
│                                                       │
│  Hello, I'm                                           │
│  **Yashpreet Singh_**                                 │
│  full-stack + AI + software builder                   │
│                                                       │
│  loading personality.exe                              │
│  ████████████████████░░░░░░ 100%                      │
│                                                       │
│  [ > enter ]                                          │
│                                                       │
└───────────────────────────────────────────────────────┘
```

- [ ] **Step 2: Add avatar image (anime character)**

Use external image URL for anime avatar. Since we don't have one, use a placeholder or pixel art.

Actually, I need to find a suitable avatar image. Let me check if there's a GitHub avatar or use a pixel art generator.

For now, plan to use the user's GitHub avatar: `https://avatars.githubusercontent.com/u/157383808?v=4`

- [ ] **Step 3: Add loading bar animation**

Use readme-typing-svg for the loading bar animation, or static Unicode blocks.

- [ ] **Step 4: Add "enter" button styling**

Use `[ > enter ]` as clickable text (though not truly interactive).

---

## Task 3: Implement Pac-Man Card

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: Reference image pac-man section.
- Produces: Pac-Man card with ASCII art and mission text.

- [ ] **Step 1: Create card border**

```
┌─[ game.pacman ]───────────────────────────────────────┐
│                                                       │
│  🟡 ● ● ● ● ● ● 👻 👻 👻 👻                         │
│                                                       │
│  > mission: eat bugs, ship features, repeat           │
│                                                       │
└───────────────────────────────────────────────────────┘
```

- [ ] **Step 2: Add Pac-Man ASCII art**

Use Unicode characters: 🟡 for Pac-Man, ● for dots, 👻 for ghosts.

- [ ] **Step 3: Add mission text**

Plain text below the ASCII art.

---

## Task 4: Implement System Diagnostics Card

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: Reference image diagnostics section.
- Produces: Diagnostics card with colored bar charts.

- [ ] **Step 1: Create card border**

```
┌─[ system.diagnostics ]────────────────────────────────┐
│                                                       │
│  🧠 CPU .............. overthinking     ████████░░    │
│  💾 RAM .............. somehow full     ██████████    │
│  ☕ COFFEE ........... required         ███████░░░    │
│  🐛 BUGS ............. multiplying      ██████░░░░    │
│  🌙 SLEEP ............ not found        ██░░░░░░░░    │
│  </> CODE QUALITY .... compiling...     █████████░    │
│                                                       │
│  > status: probably fine.                             │
│                                                       │
└───────────────────────────────────────────────────────┘
```

- [ ] **Step 2: Add colored progress bars**

Use Unicode blocks: `█` for filled, `░` for empty.

- [ ] **Step 3: Add emoji icons for each metric**

🧠 CPU, 💾 RAM, ☕ COFFEE, 🐛 BUGS, 🌙 SLEEP, </> CODE QUALITY.

---

## Task 5: Implement GitHub Contribution Card

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: Reference image contribution section.
- Produces: Contribution card with snake animation.

- [ ] **Step 1: Create card border**

```
┌─[ github.contribution ]───────────────────────────────┐
│                                                       │
│  Contribution Snake 2 🐍                              │
│                                                       │
│  [animated snake SVG]                                 │
│                                                       │
│  > survived another year of touching grass            │
│  🏆 achievement unlocked                             │
│                                                       │
└───────────────────────────────────────────────────────┘
```

- [ ] **Step 2: Embed Platane/snk snake animation**

Use existing verified URL: `https://raw.githubusercontent.com/Platane/snk/output/github-contribution-grid-snake.svg`

- [ ] **Step 3: Add achievement text**

"> survived another year of touching grass" and "🏆 achievement unlocked".

---

## Task 6: Implement Now Building Card

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: Reference image now building section.
- Produces: Now building card with list and obsession level.

- [ ] **Step 1: Create card border**

```
┌─[ now.building ]──────────────────────────────────────┐
│                                                       │
│  Currently Building                                   │
│                                                       │
│  🧪 AI tools that actually help                       │
│  🎨 Better developer experiences                      │
│  ⚙️ Backend systems that scale                        │
│  🔮 Whatever I get obsessed with next                 │
│                                                       │
│  obsession level: ████████████████████░░░░ 87%        │
│                                                       │
└───────────────────────────────────────────────────────┘
```

- [ ] **Step 2: Add building list with emoji icons**

Use 🧪, 🎨, ⚙️, 🔮 for each item.

- [ ] **Step 3: Add obsession level progress bar**

Use Unicode blocks for 87% progress.

---

## Task 7: Implement Inventory Card

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: Reference image inventory section.
- Produces: Inventory card with items and status.

- [ ] **Step 1: Create card border**

```
┌─[ inventory ]─────────────────────────────────────────┐
│                                                       │
│  Developer Inventory 🎒                               │
│                                                       │
│  ⌨️ Mechanical Keyboard                    [✓]        │
│  💻 VS Code                                [✓]        │
│  🔧 Git                                    [✓]        │
│  💡 17 Unfinished Ideas                    [✓]        │
│  📚 Stack Overflow Tab                     [✓]        │
│  ☕ Coffee                                 [✓]        │
│  😴 Sleep                                  [?]        │
│  🕐 Free Time                              [?]        │
│                                                       │
└───────────────────────────────────────────────────────┘
```

- [ ] **Step 2: Add inventory items with emoji**

Use ⌨️, 💻, 🔧, 💡, 📚, ☕, 😴, 🕐.

- [ ] **Step 3: Add status indicators**

[✓] for owned, [?] for uncertain.

---

## Task 8: Implement Achievements Card

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: Reference image achievements section.
- Produces: Achievements card with XP system.

- [ ] **Step 1: Create card border**

```
┌─[ achievements ]──────────────────────────────────────┐
│                                                       │
│  Achievements 🏆                                      │
│                                                       │
│  ┌─────────────────────────────────────────────┐      │
│  │ 🏅 It Works™                                │      │
│  │ Ran the code without error (once)    +10 XP │      │
│  └─────────────────────────────────────────────┘      │
│                                                       │
│  ┌─────────────────────────────────────────────┐      │
│  │ 🗑️ Deleted node_modules                     │      │
│  │ The universal solution               +25 XP │      │
│  └─────────────────────────────────────────────┘      │
│                                                       │
│  ┌─────────────────────────────────────────────┐      │
│  │ 📖 Read The Docs                            │      │
│  │ Impossible achievement                +50 XP │      │
│  └─────────────────────────────────────────────┘      │
│                                                       │
│  Total XP: 9999+                                      │
│                                                       │
└───────────────────────────────────────────────────────┘
```

- [ ] **Step 2: Create achievement cards**

Use nested box-drawing characters for inner cards.

- [ ] **Step 3: Add XP values**

"+10 XP", "+25 XP", "+50 XP".

- [ ] **Step 4: Add total XP**

"Total XP: 9999+".

---

## Task 9: Implement Terminal Chat Card

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: Reference image terminal chat section.
- Produces: Terminal chat card with dialogue and pixel art.

- [ ] **Step 1: Create card border**

```
┌─[ terminal.chat ]─────────────────────────────────────┐
│                                                       │
│  $ who are you?                                       │
│  > just a developer who thinks in code and            │
│    ships in caffeine.                                 │
│                                                       │
│  $ can you fix this bug?                              │
│  > yes.                                               │
│                                                       │
│  $ how?                                               │
│  > magic. ✨                                          │
│                                                       │
│  $ ok fair.                                           │
│                                                       │
└───────────────────────────────────────────────────────┘
```

- [ ] **Step 2: Add pixel art computer**

Use ASCII art for a cute computer character.

- [ ] **Step 3: Add dialogue**

Terminal-style Q&A.

---

## Task 10: Implement Secret.exe Card

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: Reference image secret section.
- Produces: Secret card with hidden content.

- [ ] **Step 1: Create card border**

```
┌─[ secret.exe ]────────────────────────────────────────┐
│                                                       │
│  🔒 You found the secret area!                        │
│  Achievement unlocked: README Archaeologist 🏛️        │
│  Come back later, more secrets loading...             │
│                                                       │
│  👾 🛸 ⭐ 🪐                                          │
│                                                       │
└───────────────────────────────────────────────────────┘
```

- [ ] **Step 2: Add pixel art aliens/planets**

Use emoji: 👾 (alien), 🛸 (UFO), ⭐ (star), 🪐 (planet).

- [ ] **Step 3: Add achievement text**

"README Archaeologist 🏛️".

---

## Task 11: Implement Connect Footer

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: Reference image connect section.
- Produces: Footer with social links.

- [ ] **Step 1: Create footer section**

```
┌─[ connect ]───────────────────────────────────────────┐
│                                                       │
│  Let's build something cool together.                 │
│                                                       │
│  [ GitHub ]  [ LinkedIn ]  [ Email ]  [ Portfolio ]   │
│                                                       │
└───────────────────────────────────────────────────────┘
```

- [ ] **Step 2: Add social links**

Use existing verified URLs.

- [ ] **Step 3: Style as buttons**

Use `[ text ]` format for button appearance.

---

## Task 12: Add Animations

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: Verified external SVG services.
- Produces: Animated elements in README.

- [ ] **Step 1: Add boot typing animation**

Use readme-typing-svg for the hero section loading bar.

- [ ] **Step 2: Add snake animation**

Use Platane/snk for contribution card.

- [ ] **Step 3: Add diagnostics typing animation**

Use readme-typing-svg for system diagnostics output.

- [ ] **Step 4: Verify all animations work**

Test each external URL.

---

## Task 13: Final Review and Verification

**Files:**
- Modify: `README.md` (if changes needed)

**Interfaces:**
- Consumes: Complete README.
- Produces: Final verified README.

- [ ] **Step 1: Verify all cards present**

Check all 10 cards are implemented.

- [ ] **Step 2: Verify animations work**

Test all external SVG URLs.

- [ ] **Step 3: Verify responsive layout**

Check table renders properly.

- [ ] **Step 4: Verify professional info minimal**

Name, tagline, projects, links present.

- [ ] **Step 5: Verify easter eggs present**

Secret.exe card and any details blocks.

- [ ] **Step 6: Run git diff for user review**

Show changes without committing.

---

## Self-Review Checklist

1. **Reference coverage:** Does the plan address all sections in reference.png?
2. **GitHub constraints:** Are all technical limitations acknowledged?
3. **Animation feasibility:** Are animations limited to verified external services?
4. **Color approximation:** Are colors approximated via emoji/blocks?
5. **Layout feasibility:** Is the table-based grid layout possible on GitHub?

**Note:** This plan acknowledges that GitHub markdown has significant limitations (no CSS, no JavaScript). The implementation will approximate the reference design using available tools (box-drawing characters, Unicode blocks, emoji, external SVGs). Some visual elements (colored borders, gradient progress bars, pixel art) will be simplified.