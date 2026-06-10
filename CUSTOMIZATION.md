# 🎨 CUSTOMIZATION.md - How to Customize Global Defense Command

## Quick Start Customization

### 1. Open the HTML File
Open `global-defense-command.html` in any text editor (VS Code, Notepad++, Sublime, etc.)

### 2. Find & Replace
Use Find & Replace (Ctrl+H or Cmd+H) to quickly customize:

| Find | Replace With |
|------|---|
| `TECHFEST 2025` | Your Event Name |
| `AXIOM-7` | User Name |
| `NIT Trichy` | User Campus |
| `CSE '25` | User Department & Year |

---

## 🎯 Major Customizations

### Change Event Name
**Location:** Multiple places throughout the file

**Find:**
```html
TECHFEST 2025
TechFest 2025
TechFest 2025
```

**Replace with:**
```html
YOUR EVENT NAME
Your Event Name
Your Event Name
```

**Locations to update:**
1. Topbar: "LIVE TECHFEST 2025"
2. Sidebar footer: "TECHFEST 2025 · ZONAL NODE: SOUTH"
3. Live ticker items
4. Mission descriptions
5. Marketplace descriptions
6. Notifications

---

### Customize Agent Profile

#### Update Agent Card (Sidebar)
```html
<!-- Find this section -->
<div class="agent-card">
  <div class="agent-avatar">🎖️</div>
  <div class="agent-name">AXIOM-7</div>
  <div class="agent-rank">CAPTAIN · TIER III OPERATIVE</div>
  <div style="display:flex;gap:6px;margin-bottom:6px">
    <span class="tag">NIT Trichy</span>
    <span class="tag">CSE '25</span>
  </div>
  <div class="xp-bar-wrap"><div class="xp-bar"></div></div>
  <div class="xp-label"><span>XP 6,840</span><span>→ 10,000</span></div>
  <div class="coin-row">
    <span class="coin-icon">◈</span>
    <span class="coin-val">2,450</span>
    <span class="coin-label">Defense Coins</span>
  </div>
</div>

<!-- Replace with your data -->
<div class="agent-card">
  <div class="agent-avatar">YOUR EMOJI</div>
  <div class="agent-name">YOUR NAME</div>
  <div class="agent-rank">YOUR RANK · YOUR TIER</div>
  <div style="display:flex;gap:6px;margin-bottom:6px">
    <span class="tag">YOUR COLLEGE</span>
    <span class="tag">YOUR DEPT YEAR</span>
  </div>
  <div class="xp-bar-wrap"><div class="xp-bar" style="width:YOUR%"></div></div>
  <div class="xp-label"><span>XP YOUR</span><span>→ YOUR</span></div>
  <div class="coin-row">
    <span class="coin-icon">◈</span>
    <span class="coin-val">YOUR COINS</span>
    <span class="coin-label">Your Currency Name</span>
  </div>
</div>
```

#### Update Stat Cards
```html
<!-- Dashboard stat cards - update these values -->
<div class="stat-card blue">
  <div class="stat-icon">🎯</div>
  <div class="stat-val">18</div>          <!-- Change this number -->
  <div class="stat-label">Missions Done</div>
  <div class="stat-delta">↑ +3 this week</div>
</div>
```

---

### Customize Missions

#### Add New Mission
```html
<div class="mission-card urgent">
  <div class="mission-head">
    <div class="mission-name">YOUR MISSION NAME</div>
    <div class="mission-badge urgent">URGENT</div>  <!-- urgent|active-m|complete|pending -->
  </div>
  <div class="mission-desc">Your mission description goes here.</div>
  <div class="mission-meta">
    <div class="mission-meta-item mission-coin">◈ 800</div>  <!-- Coins -->
    <div class="mission-meta-item mission-xp">⚡ 500 XP</div> <!-- XP -->
    <div class="mission-meta-item">⏱ 48h left</div>  <!-- Deadline -->
  </div>
  <div class="prog-wrap"><div class="prog-fill" style="width:64%;background:var(--danger)"></div></div>
  <div style="font-family:var(--font-hud);font-size:9px;color:var(--text3);margin-top:4px">32/50 PROGRESS</div>
</div>
```

#### Update Existing Mission
```html
<!-- Find -->
<div class="mission-name">OPERATION NEXUS</div>
<div class="mission-desc">Register 50 students for TechFest 2025...</div>
<div class="mission-meta-item mission-coin">◈ 800</div>
<div class="mission-meta-item mission-xp">⚡ 500 XP</div>

<!-- Replace with -->
<div class="mission-name">YOUR MISSION NAME</div>
<div class="mission-desc">Your mission description here...</div>
<div class="mission-meta-item mission-coin">◈ YOUR COINS</div>
<div class="mission-meta-item mission-xp">⚡ YOUR XP</div>
```

#### Mission Status Badge Classes
```html
<div class="mission-badge urgent">URGENT</div>       <!-- Red - Deadline soon -->
<div class="mission-badge active-m">IN PROGRESS</div> <!-- Blue - Currently doing -->
<div class="mission-badge complete">COMPLETE</div>   <!-- Green - Finished -->
<div class="mission-badge pending">AVAILABLE</div>   <!-- Amber - Ready to accept -->
```

---

### Customize Leaderboard Data

#### Update Top Agents
```html
<!-- Find this section and update -->
<div class="lb-row">
  <div class="lb-rank r1">1</div>
  <div class="lb-avatar">🦅</div>
  <div class="lb-info">
    <div class="lb-name">Aryan Shah</div>
    <div class="lb-college">IIT Bombay</div>
  </div>
  <div style="flex:1"></div>
  <div class="lb-bar-wrap"><div class="lb-bar" style="width:100%"></div></div>
  <div class="lb-score" style="min-width:54px;text-align:right">14,220</div>
</div>

<!-- Update with -->
<div class="lb-row">
  <div class="lb-rank r1">1</div>
  <div class="lb-avatar">TOP EMOJI</div>
  <div class="lb-info">
    <div class="lb-name">Top Agent Name</div>
    <div class="lb-college">Top Agent College</div>
  </div>
  <div style="flex:1"></div>
  <div class="lb-bar-wrap"><div class="lb-bar" style="width:100%"></div></div>
  <div class="lb-score" style="min-width:54px;text-align:right">15,000</div>
</div>
```

#### Rank Styling
```html
<div class="lb-rank r1">1</div>  <!-- Gold (#ffd700) -->
<div class="lb-rank r2">2</div>  <!-- Silver (#c0c0c0) -->
<div class="lb-rank r3">3</div>  <!-- Bronze (#cd7f32) -->
<div class="lb-rank rn">4+</div> <!-- Normal color -->
```

---

### Customize Marketplace Items

#### Update Reward Item
```html
<!-- Find a marketplace card -->
<div class="market-card">
  <div class="market-icon">📜</div>
  <div class="market-name">Participation Cert</div>
  <div class="market-desc">Official TechFest 2025 Ambassador Certificate</div>
  <div class="market-price">◈ 200</div>
</div>

<!-- Replace with your reward -->
<div class="market-card">
  <div class="market-icon">YOUR EMOJI</div>
  <div class="market-name">Your Reward Name</div>
  <div class="market-desc">Description of what they get</div>
  <div class="market-price">◈ COIN_AMOUNT</div>
</div>
```

#### Available Marketplace Items Template
The marketplace currently has 6 items. Each one is in a `market-card` div. You can:
- Change the emoji icon
- Update the name
- Write new description
- Modify the coin price

---

### Customize Badges & Achievements

#### Update Badge Name & Icon
```html
<!-- Find -->
<div class="badge-card">
  <div class="badge-icon">🎯</div>
  <div class="badge-name">First Strike</div>
  <div class="badge-pts">+100 XP</div>
</div>

<!-- Replace with -->
<div class="badge-card">
  <div class="badge-icon">YOUR EMOJI</div>
  <div class="badge-name">YOUR BADGE NAME</div>
  <div class="badge-pts">+YOUR XP</div>
</div>
```

#### Lock a Badge
```html
<!-- Unlocked -->
<div class="badge-card">...</div>

<!-- Locked (grayscale & transparent) -->
<div class="badge-card locked">...</div>
```

---

### Customize Notifications

#### Add a New Notification
```html
<div class="notif-item">
  <div class="notif-dot-wrap">
    <div class="notif-dot ALERT_TYPE"></div>  <!-- info|warn|success|alert -->
  </div>
  <div>
    <div class="notif-text">Your notification message here</div>
    <div class="notif-time">When this happened · CATEGORY</div>
  </div>
</div>
```

#### Notification Types
```html
<div class="notif-dot info"></div>      <!-- Blue - Information -->
<div class="notif-dot warn"></div>      <!-- Amber - Warning -->
<div class="notif-dot success"></div>   <!-- Green - Success -->
<div class="notif-dot alert"></div>     <!-- Red - Alert -->
```

---

## 🎨 Color Customization

### Change Color Scheme

#### Locate Color Variables
At the very top of the `<style>` section, find:
```css
:root {
  --neon: #00d4ff;
  --neon2: #7b2fff;
  --neon3: #00ff9d;
  --amber: #ffb347;
  --danger: #ff4757;
  --bg0: #020c1b;
  --bg1: #041428;
  --bg2: #071e38;
  --bg3: #0a2444;
  --glass: rgba(0,212,255,0.05);
  /* ... more colors ... */
}
```

#### Change Primary Color (Neon Blue)
```css
:root {
  --neon: #FF00FF;  /* Change from cyan to magenta */
}
```
This changes all cyan accents to magenta throughout the app.

#### Change Background Color (Dark)
```css
:root {
  --bg0: #000000;   /* Pure black instead of dark blue */
  --bg1: #1a1a1a;   /* Darker panels */
}
```

#### Complete Color Scheme Swap
```css
:root {
  /* Purple/Orange Cyberpunk */
  --neon: #FF006E;        /* Hot pink */
  --neon2: #8338EC;       /* Purple */
  --neon3: #FFBE0B;       /* Yellow */
  --amber: #FB5607;       /* Orange */
  --danger: #D62828;      /* Red */
}
```

#### Color Reference
- **--neon**: Primary accent (usually buttons, borders)
- **--neon2**: Secondary accent (badges, secondary info)
- **--neon3**: Tertiary accent (success, highlights)
- **--amber**: Currency, rewards
- **--danger**: Urgent, alerts, errors
- **--bg0-3**: Background layers (light to dark)

---

### Common Color Schemes

#### Dark Purple (Elegant)
```css
--neon: #9D4EDD;      /* Purple */
--neon2: #5A189A;     /* Dark purple */
--neon3: #E0AAFF;     /* Light purple */
--amber: #E8C1C5;     /* Mauve */
```

#### Neon Green (Matrix)
```css
--neon: #00FF00;      /* Bright green */
--neon2: #00CC00;     /* Dark green */
--neon3: #00FFFF;     /* Cyan */
--amber: #FFFF00;     /* Yellow */
```

#### Red/Orange (Fire)
```css
--neon: #FF0000;      /* Red */
--neon2: #FF6600;     /* Orange */
--neon3: #FFFF00;     /* Yellow */
--amber: #FFD700;     /* Gold */
```

---

## 📝 Text & Content Customization

### Change Event-Specific Text

#### Header Title
```html
<!-- Find -->
<span class="page-title" id="page-title">Command Center</span>

<!-- Pages are listed in pages object, update as needed -->
```

#### Sidebar Footer
```html
<div class="sidebar-footer">
  <span class="status-dot"></span>SYSTEM ONLINE · SESSION SECURE<br>
  <span style="margin-top:4px;display:block">TECHFEST 2025 · ZONAL NODE: SOUTH</span>
</div>

<!-- Change to -->
<div class="sidebar-footer">
  <span class="status-dot"></span>YOUR STATUS TEXT<br>
  <span style="margin-top:4px;display:block">YOUR EVENT · YOUR REGION</span>
</div>
```

#### Live Ticker Items
```html
<!-- Find the ticker section -->
<div class="ticker">
  <span class="ticker-item">🏆 <span class="ticker-up">Rahul K</span> completed...</span>
  <!-- Update these items -->
</div>
```

---

## 🔧 Advanced Customization

### Add New Sections

#### Add a New Navigation Item
```html
<!-- In sidebar nav-section, add -->
<div class="nav-item" onclick="nav('newsection')">
  <span class="nav-icon">📌</span>
  New Section Name
</div>

<!-- Then add a new page -->
<div class="page" id="page-newsection">
  <div class="panel">
    <div class="panel-head">
      <span class="panel-icon">📌</span>
      <span class="panel-title">New Section</span>
    </div>
    <div class="panel-body">
      <!-- Your content here -->
    </div>
  </div>
</div>

<!-- Update pages object in JavaScript -->
const pages = {
  // ... existing pages ...
  newsection: 'New Section Name',
};
```

### Modify Animations

#### Disable Scanline Effect
```css
/* Find and remove or comment out */
body::before {
  display: none;  /* Add this to disable */
}
```

#### Change Ticker Speed
```css
.ticker {
  animation: ticker-scroll 30s linear infinite;
                          ^^
                      Change this number (seconds)
}

/* Faster = smaller number */
/* Slower = larger number */
```

#### Disable Glow Effects
```css
/* Find and remove box-shadow properties */
.logo-icon {
  /* Remove this line */
  box-shadow: 0 0 12px rgba(0,212,255,0.3);
}
```

---

### Modify Fonts

#### Change Font Family
```css
:root {
  --font-hud: 'Your Font', monospace;      /* Data/technical text */
  --font-ui: 'Your Font', sans-serif;      /* UI elements */
  --font-head: 'Your Font', monospace;     /* Headers */
}
```

#### Fallback to System Fonts (Offline)
```css
:root {
  --font-hud: 'Courier New', monospace;
  --font-ui: 'Segoe UI', sans-serif;
  --font-head: 'Arial', sans-serif;
}
```

---

## 🎯 Data Customization Examples

### Update a Complete Agent Profile

```html
<!-- BEFORE -->
<div class="agent-card">
  <div class="agent-avatar">🎖️</div>
  <div class="agent-name">AXIOM-7</div>
  <div class="agent-rank">CAPTAIN · TIER III OPERATIVE</div>
  <div style="display:flex;gap:6px;margin-bottom:6px">
    <span class="tag">NIT Trichy</span>
    <span class="tag">CSE '25</span>
  </div>
  <div class="xp-bar-wrap"><div class="xp-bar" style="width:68%"></div></div>
  <div class="xp-label"><span>XP 6,840</span><span>→ 10,000</span></div>
  <div class="coin-row">
    <span class="coin-icon">◈</span>
    <span class="coin-val">2,450</span>
    <span class="coin-label">Defense Coins</span>
  </div>
</div>

<!-- AFTER (Your Custom Data) -->
<div class="agent-card">
  <div class="agent-avatar">🌟</div>
  <div class="agent-name">PHOENIX-13</div>
  <div class="agent-rank">SERGEANT · TIER II OPERATIVE</div>
  <div style="display:flex;gap:6px;margin-bottom:6px">
    <span class="tag">MIT</span>
    <span class="tag">ENG '26</span>
  </div>
  <div class="xp-bar-wrap"><div class="xp-bar" style="width:45%"></div></div>
  <div class="xp-label"><span>XP 4,500</span><span>→ 10,000</span></div>
  <div class="coin-row">
    <span class="coin-icon">◈</span>
    <span class="coin-val">1,800</span>
    <span class="coin-label">Defense Coins</span>
  </div>
</div>
```

---

## ✅ Customization Checklist

- [ ] Change event name everywhere
- [ ] Update agent profile (name, rank, campus)
- [ ] Update stat card values
- [ ] Customize missions (names, descriptions, rewards)
- [ ] Update top leaderboard agents
- [ ] Modify marketplace rewards
- [ ] Customize badges
- [ ] Update notifications
- [ ] Change color scheme (optional)
- [ ] Update fonts (optional)
- [ ] Test all navigation links
- [ ] Check mobile responsiveness
- [ ] Verify all text displays correctly

---

## 🚀 Tips & Tricks

### Quick Test Changes
1. Make a small change
2. Save the file
3. Refresh browser (F5 or Ctrl+R)
4. See results immediately

### Keep Backup
```bash
# Before making changes, create a backup
cp global-defense-command.html global-defense-command-backup.html
```

### Use Find & Replace Carefully
- Always use "Find All" first to see all matches
- Replace one section at a time
- Verify results after replacing

### Test Across Devices
- Desktop (1920px+)
- Tablet (768px - 1920px)
- Mobile (320px - 768px)

### Common Mistakes to Avoid
- ❌ Breaking HTML tags when editing
- ❌ Changing CSS variable names
- ❌ Removing closing tags
- ❌ Editing JavaScript function names
- ✅ Keep file structure intact
- ✅ Test thoroughly after changes

---

**Happy customizing! Your Global Defense Command platform is now ready for your event.** 🚀
