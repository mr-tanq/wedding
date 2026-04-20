import React, { useState, useEffect, useMemo, useRef } from "react";
import {
  Clock, MapPin, Users, Brain, Camera, Heart, Music,
  ChevronRight, Search, Check, X, Trophy, Upload,
  Send, ThumbsUp, Sparkles, Wine, Flame, Disc3,
  Radio, Star, Gift, Quote, Home
} from "lucide-react";

// ============================================================
// KOSTAS & CHARA — WEDDING NIGHT APP
// ============================================================

// ---------- CONFIG ----------
const WEDDING_DATE = new Date(); // demo: "now" so timeline feels live
WEDDING_DATE.setHours(18, 0, 0, 0);

const TIMELINE = [
  { time: "18:00", label: "Arrival",             icon: Gift,   note: "Welcome drinks & first hugs" },
  { time: "19:00", label: "Ceremony",            icon: Heart,  note: "The vows. The moment." },
  { time: "20:00", label: "Dinner",              icon: Wine,   note: "A long, slow feast" },
  { time: "21:30", label: "Speeches",            icon: Quote,  note: "Tears guaranteed" },
  { time: "22:00", label: "Cake",                icon: Sparkles, note: "Sugar before chaos" },
  { time: "22:30", label: "Greek Traditional",   icon: Radio,  note: "Circle up. Feet up." },
  { time: "23:00", label: "Party Starts",        icon: Disc3,  note: "The floor opens" },
  { time: "00:00", label: "80s / 90s / Trance",  icon: Music,  note: "Nostalgia hour" },
  { time: "01:00", label: "Main Dancefloor",     icon: Flame,  note: "Peak madness" },
  { time: "02:00", label: "Metal Block",         icon: Flame,  note: "Hair down. Horns up." },
  { time: "03:00", label: "Survivors Only",      icon: Star,   note: "You made it." },
];

const TABLES = [
  { n: 1,  name: "The Inner Circle",              tag: "Family",     desc: "Parents, siblings, the originals.", people: ["Maria", "Giannis", "Eleni", "Nikos", "Sofia", "Dimitris"] },
  { n: 2,  name: "The Godparents",                tag: "Family",     desc: "Koumbari & co.", people: ["Anna", "Panagiotis", "Katerina", "Yannis"] },
  { n: 3,  name: "The Dutch Survivors",           tag: "Friends",    desc: "They flew in. They stayed too long.", people: ["Sem", "Lotte", "Bram", "Fenna", "Thijs"] },
  { n: 4,  name: "Chara's Oldest Friends",        tag: "Friends",    desc: "They've seen every phase.", people: ["Despina", "Vasiliki", "Marina", "Ioanna"] },
  { n: 5,  name: "The Metalheads",                tag: "Friends",    desc: "Table will be loudest after 02:00.", people: ["Andreas", "Stelios", "Kostis", "Petros", "Manos"] },
  { n: 6,  name: "Work Friends — Kostas",         tag: "Colleagues", desc: "Office legends.", people: ["George", "Elena", "Thanos", "Irini"] },
  { n: 7,  name: "Work Friends — Chara",          tag: "Colleagues", desc: "Lunch-break philosophers.", people: ["Alex", "Natalia", "Pavlos", "Chrysa"] },
  { n: 8,  name: "Family Chaos Department",       tag: "Family",     desc: "Cousins of cousins. Unclear lineage.", people: ["Takis", "Voula", "Spyros", "Aggeliki", "Babis"] },
  { n: 9,  name: "University Years",              tag: "Friends",    desc: "Athens. 3AM gyros. Finals.", people: ["Christos", "Myrto", "Lefteris", "Zoe"] },
  { n: 10, name: "Neighbors & Legends",           tag: "Family",     desc: "They raised the village with them.", people: ["Kyria Rita", "Kyrios Vangelis", "Toula"] },
  { n: 11, name: "Stay Until 5AM Club",           tag: "Friends",    desc: "You know who you are.", people: ["Lazaros", "Anastasia", "Fotis", "Dora", "Mike"] },
  { n: 12, name: "The Newcomers",                 tag: "Friends",    desc: "New but chosen.", people: ["Raoul", "Sarah", "Julien", "Inês"] },
];

const QUIZ = [
  { q: "Where did Kostas and Chara first meet?",          opts: ["A concert in Athens", "A mutual friend's party", "Dating app", "University library"], a: 1 },
  { q: "Who said 'I love you' first?",                     opts: ["Kostas", "Chara", "At the same time", "Nobody remembers"], a: 0 },
  { q: "Kostas's favorite drink?",                         opts: ["Old Fashioned", "Mythos beer", "Tsipouro", "Negroni"], a: 2 },
  { q: "Their song?",                                      opts: ["A Greek classic", "A trance anthem", "Something metal", "Depeche Mode"], a: 3 },
  { q: "Who is more stubborn?",                            opts: ["Kostas", "Chara", "Equally", "Neither"], a: 1 },
  { q: "Who takes longer to get ready?",                   opts: ["Kostas", "Chara", "Same", "Depends on the event"], a: 0 },
  { q: "Who is more likely to get drunk first tonight?",   opts: ["Kostas", "Chara", "Both at the same time", "Neither, they're pacing"], a: 0 },
  { q: "Their favorite trip together?",                    opts: ["Iceland", "Japan", "Santorini", "Road trip in Italy"], a: 1 },
  { q: "First movie they watched together?",               opts: ["Pulp Fiction", "Before Sunrise", "The Matrix", "A horror film"], a: 1 },
  { q: "Who proposed?",                                    opts: ["Kostas", "Chara", "Simultaneously", "It was gradual"], a: 0 },
];

const MUSIC_BLOCKS = [
  {
    id: "greek",    name: "Greek Traditional", time: "22:30", color: "#C9A24B",
    songs: [
      { t: "Zorba — Theodorakis",        v: 24 },
      { t: "Ximeroni — Glykeria",        v: 18 },
      { t: "Fraoules Stomati — Marinella", v: 12 },
      { t: "Ta Deilina — Dalaras",       v: 9  },
    ],
  },
  {
    id: "retro",    name: "80s / 90s / Trance", time: "00:00", color: "#D4AF37",
    songs: [
      { t: "Sandstorm — Darude",         v: 42 },
      { t: "Children — Robert Miles",    v: 38 },
      { t: "Blue — Eiffel 65",           v: 29 },
      { t: "Around the World — ATC",     v: 21 },
      { t: "What Is Love — Haddaway",    v: 19 },
    ],
  },
  {
    id: "party",    name: "Party Classics",    time: "01:00", color: "#E6C15A",
    songs: [
      { t: "Mr. Brightside — The Killers",   v: 51 },
      { t: "Don't Stop Me Now — Queen",      v: 48 },
      { t: "September — Earth Wind & Fire",  v: 33 },
      { t: "Everybody — Backstreet Boys",    v: 27 },
    ],
  },
  {
    id: "metal",    name: "Metal Block",       time: "02:00", color: "#B8862E",
    songs: [
      { t: "Master of Puppets — Metallica",  v: 37 },
      { t: "Painkiller — Judas Priest",      v: 22 },
      { t: "Chop Suey! — System of a Down",  v: 29 },
      { t: "Raining Blood — Slayer",         v: 14 },
      { t: "Rosanna — Rotting Christ",       v: 11 },
    ],
  },
  {
    id: "late",     name: "Late-Night Chaos",  time: "03:00", color: "#A67729",
    songs: [
      { t: "Strobe — Deadmau5",              v: 26 },
      { t: "Teardrop — Massive Attack",      v: 18 },
      { t: "One More Time — Daft Punk",      v: 44 },
    ],
  },
];

// ---------- UTILITIES ----------
const pad = (n) => String(n).padStart(2, "0");

function useNow(tickMs = 1000) {
  const [now, setNow] = useState(new Date());
  useEffect(() => {
    const t = setInterval(() => setNow(new Date()), tickMs);
    return () => clearInterval(t);
  }, [tickMs]);
  return now;
}

function timeStrToDate(str, baseDate) {
  const [h, m] = str.split(":").map(Number);
  const d = new Date(baseDate);
  if (h < 12) d.setDate(d.getDate() + 1); // after midnight = next day
  d.setHours(h, m, 0, 0);
  return d;
}

function formatCountdown(ms) {
  if (ms <= 0) return "now";
  const s = Math.floor(ms / 1000);
  const h = Math.floor(s / 3600);
  const m = Math.floor((s % 3600) / 60);
  const sec = s % 60;
  if (h > 0) return `${h}h ${pad(m)}m`;
  if (m > 0) return `${m}m ${pad(sec)}s`;
  return `${sec}s`;
}

// ---------- STYLE PRIMITIVES ----------
const FONTS = `
  @import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&family=Inter:wght@300;400;500;600&display=swap');
`;

const css = `
  ${FONTS}
  :root {
    --bg: #08070a;
    --bg-soft: #0f0d12;
    --ink: #f5ecd7;
    --ink-dim: #a89978;
    --gold: #d4af37;
    --gold-soft: #c9a24b;
    --gold-deep: #8a6a1e;
    --line: rgba(212, 175, 55, 0.15);
    --glass: rgba(255, 250, 235, 0.035);
    --glass-strong: rgba(255, 250, 235, 0.06);
  }
  * { box-sizing: border-box; }
  html, body, #root { background: var(--bg); }
  body {
    margin: 0;
    font-family: 'Inter', -apple-system, sans-serif;
    color: var(--ink);
    -webkit-font-smoothing: antialiased;
  }
  .serif { font-family: 'Cormorant Garamond', 'Times New Roman', serif; font-weight: 400; letter-spacing: 0.01em; }
  .sans  { font-family: 'Inter', sans-serif; }
  .gold  { color: var(--gold); }

  .app-bg {
    min-height: 100vh;
    background:
      radial-gradient(1200px 600px at 50% -10%, rgba(212,175,55,0.12), transparent 60%),
      radial-gradient(800px 400px at 80% 110%, rgba(212,175,55,0.06), transparent 60%),
      var(--bg);
    position: relative;
    overflow-x: hidden;
  }
  .app-bg::before {
    content: "";
    position: fixed; inset: 0; pointer-events: none;
    background-image: url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='180' height='180'><filter id='n'><feTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='2' stitchTiles='stitch'/><feColorMatrix values='0 0 0 0 0.85  0 0 0 0 0.75  0 0 0 0 0.45  0 0 0 0.08 0'/></filter><rect width='100%' height='100%' filter='url(%23n)'/></svg>");
    opacity: 0.35;
    mix-blend-mode: overlay;
    z-index: 0;
  }

  .glass {
    background: var(--glass);
    backdrop-filter: blur(14px) saturate(130%);
    -webkit-backdrop-filter: blur(14px) saturate(130%);
    border: 1px solid var(--line);
    border-radius: 18px;
  }
  .glass-strong {
    background: var(--glass-strong);
    backdrop-filter: blur(18px) saturate(140%);
    border: 1px solid rgba(212, 175, 55, 0.22);
    border-radius: 20px;
  }

  .hairline { height: 1px; background: linear-gradient(90deg, transparent, rgba(212,175,55,0.45), transparent); }

  .btn-gold {
    background: linear-gradient(180deg, #e6c15a 0%, #c9a24b 60%, #a67729 100%);
    color: #0a0908;
    font-weight: 600;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    font-size: 12px;
    padding: 14px 20px;
    border-radius: 999px;
    border: none;
    cursor: pointer;
    box-shadow: 0 8px 24px -8px rgba(212,175,55,0.5), inset 0 1px 0 rgba(255,255,255,0.4);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }
  .btn-gold:hover { transform: translateY(-1px); box-shadow: 0 12px 32px -8px rgba(212,175,55,0.6), inset 0 1px 0 rgba(255,255,255,0.4); }
  .btn-gold:active { transform: translateY(0); }
  .btn-ghost {
    background: transparent;
    color: var(--gold);
    border: 1px solid rgba(212,175,55,0.35);
    padding: 12px 18px;
    border-radius: 999px;
    font-size: 12px;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    cursor: pointer;
    transition: all 0.2s ease;
  }
  .btn-ghost:hover { background: rgba(212,175,55,0.08); border-color: var(--gold); }

  .tab-bar {
    position: fixed; bottom: 0; left: 0; right: 0;
    background: rgba(8, 7, 10, 0.85);
    backdrop-filter: blur(20px) saturate(140%);
    -webkit-backdrop-filter: blur(20px) saturate(140%);
    border-top: 1px solid var(--line);
    z-index: 50;
    padding: 8px 6px calc(8px + env(safe-area-inset-bottom));
  }
  .tab-row { display: grid; grid-template-columns: repeat(6, 1fr); max-width: 520px; margin: 0 auto; }
  .tab {
    display: flex; flex-direction: column; align-items: center; gap: 3px;
    padding: 8px 4px; color: var(--ink-dim); cursor: pointer;
    font-size: 9px; letter-spacing: 0.05em; text-transform: uppercase;
    transition: color 0.2s;
    background: none; border: none;
  }
  .tab.active { color: var(--gold); }
  .tab.active .tab-dot { opacity: 1; }
  .tab-dot { width: 4px; height: 4px; border-radius: 50%; background: var(--gold); opacity: 0; transition: opacity 0.2s; }

  .screen { max-width: 520px; margin: 0 auto; padding: 24px 20px 100px; position: relative; z-index: 1; }

  .eyebrow { font-size: 10px; letter-spacing: 0.3em; text-transform: uppercase; color: var(--gold-soft); }
  .h-display { font-family: 'Cormorant Garamond', serif; font-weight: 300; font-size: 44px; line-height: 1.05; letter-spacing: -0.01em; color: var(--ink); }
  .h-display .amp { font-style: italic; color: var(--gold); font-weight: 400; padding: 0 4px; }

  .shimmer {
    background: linear-gradient(90deg, transparent, rgba(212,175,55,0.18), transparent);
    background-size: 200% 100%;
    animation: shim 2.4s linear infinite;
  }
  @keyframes shim { 0% { background-position: 200% 0 } 100% { background-position: -200% 0 } }

  .reveal { opacity: 0; transform: translateY(8px); animation: reveal 0.6s ease forwards; }
  @keyframes reveal { to { opacity: 1; transform: none; } }

  .pulse-dot { width: 8px; height: 8px; border-radius: 50%; background: var(--gold); box-shadow: 0 0 0 0 rgba(212,175,55,0.6); animation: pulse 2s infinite; }
  @keyframes pulse {
    0% { box-shadow: 0 0 0 0 rgba(212,175,55,0.6); }
    70% { box-shadow: 0 0 0 10px rgba(212,175,55,0); }
    100% { box-shadow: 0 0 0 0 rgba(212,175,55,0); }
  }

  input, textarea, select {
    background: rgba(255,250,235,0.04);
    border: 1px solid var(--line);
    color: var(--ink);
    padding: 14px 16px;
    border-radius: 12px;
    font-family: 'Inter', sans-serif;
    font-size: 14px;
    width: 100%;
    outline: none;
    transition: border-color 0.2s;
  }
  input:focus, textarea:focus, select:focus { border-color: var(--gold-soft); }
  input::placeholder, textarea::placeholder { color: var(--ink-dim); }

  .chip {
    display: inline-flex; align-items: center; gap: 6px;
    padding: 6px 12px; border-radius: 999px;
    background: rgba(212,175,55,0.08);
    border: 1px solid rgba(212,175,55,0.2);
    color: var(--gold);
    font-size: 10px; letter-spacing: 0.1em; text-transform: uppercase;
  }

  .progress-rail { height: 3px; background: rgba(212,175,55,0.12); border-radius: 999px; overflow: hidden; }
  .progress-fill { height: 100%; background: linear-gradient(90deg, var(--gold-deep), var(--gold), var(--gold-soft)); border-radius: 999px; }

  @media (max-width: 380px) {
    .h-display { font-size: 36px; }
    .tab { font-size: 8px; }
  }
`;

// ============================================================
// ROOT
// ============================================================
export default function WeddingApp() {
  const [tab, setTab] = useState("timeline");
  const tabs = [
    { id: "timeline", label: "Night",   icon: Clock },
    { id: "table",    label: "Table",   icon: MapPin },
    { id: "quiz",     label: "Quiz",    icon: Brain },
    { id: "photos",   label: "Photos",  icon: Camera },
    { id: "messages", label: "Wishes",  icon: Heart },
    { id: "music",    label: "Music",   icon: Music },
  ];

  return (
    <>
      <style>{css}</style>
      <div className="app-bg">
        <Header />
        <main className="screen">
          {tab === "timeline" && <TimelineScreen />}
          {tab === "table"    && <TableScreen />}
          {tab === "quiz"     && <QuizScreen />}
          {tab === "photos"   && <PhotosScreen />}
          {tab === "messages" && <MessagesScreen />}
          {tab === "music"    && <MusicScreen />}
        </main>
        <nav className="tab-bar">
          <div className="tab-row">
            {tabs.map((t) => {
              const Icon = t.icon;
              const active = tab === t.id;
              return (
                <button key={t.id} className={`tab ${active ? "active" : ""}`} onClick={() => setTab(t.id)}>
                  <Icon size={18} strokeWidth={1.5} />
                  <span>{t.label}</span>
                  <span className="tab-dot" />
                </button>
              );
            })}
          </div>
        </nav>
      </div>
    </>
  );
}

// ============================================================
// HEADER
// ============================================================
function Header() {
  return (
    <header style={{ position: "relative", zIndex: 1, paddingTop: 32, paddingBottom: 8 }}>
      <div style={{ maxWidth: 520, margin: "0 auto", padding: "0 20px", textAlign: "center" }}>
        <div className="eyebrow" style={{ marginBottom: 12 }}>A Wedding Night</div>
        <div style={{ display: "flex", alignItems: "center", justifyContent: "center", gap: 10, marginBottom: 8 }}>
          <div style={{ height: 1, width: 40, background: "rgba(212,175,55,0.4)" }} />
          <Sparkles size={12} className="gold" />
          <div style={{ height: 1, width: 40, background: "rgba(212,175,55,0.4)" }} />
        </div>
        <h1 className="h-display">
          Kostas <span className="amp">&</span> Chara
        </h1>
      </div>
    </header>
  );
}

// ============================================================
// 1. TIMELINE
// ============================================================
function TimelineScreen() {
  const now = useNow(1000);

  const events = useMemo(() => {
    return TIMELINE.map((e) => ({ ...e, date: timeStrToDate(e.time, WEDDING_DATE) }));
  }, []);

  const { currentIdx, nextIdx, progress } = useMemo(() => {
    let cur = -1;
    for (let i = 0; i < events.length; i++) {
      if (now >= events[i].date) cur = i;
    }
    const next = cur + 1 < events.length ? cur + 1 : -1;
    let prog = 0;
    if (cur >= 0 && next >= 0) {
      const span = events[next].date - events[cur].date;
      const elapsed = now - events[cur].date;
      prog = Math.min(1, Math.max(0, elapsed / span));
    } else if (cur >= 0) prog = 1;
    return { currentIdx: cur, nextIdx: next, progress: prog };
  }, [now, events]);

  const nextEvent = nextIdx >= 0 ? events[nextIdx] : null;
  const countdown = nextEvent ? formatCountdown(nextEvent.date - now) : "—";
  const overallProgress = currentIdx >= 0 ? (currentIdx + progress) / events.length : 0;

  const liveMsg = nextEvent ? `${nextEvent.label} in ${countdown}` : "The night has ended. Thank you for being here.";

  return (
    <div className="reveal">
      <div className="chip" style={{ marginBottom: 14 }}>
        <span className="pulse-dot" /> Live
      </div>

      <div className="glass-strong" style={{ padding: 24, marginBottom: 20 }}>
        <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", marginBottom: 18 }}>
          <div>
            <div className="eyebrow" style={{ marginBottom: 6 }}>Next</div>
            <div className="serif" style={{ fontSize: 28, lineHeight: 1.1 }}>
              {nextEvent ? nextEvent.label : "Encore"}
            </div>
          </div>
          <div style={{ textAlign: "right" }}>
            <div className="eyebrow" style={{ marginBottom: 6 }}>In</div>
            <div className="gold serif" style={{ fontSize: 26, lineHeight: 1 }}>{countdown}</div>
          </div>
        </div>
        <div className="progress-rail">
          <div className="progress-fill shimmer" style={{ width: `${overallProgress * 100}%`, transition: "width 1s linear" }} />
        </div>
        <div style={{ display: "flex", justifyContent: "space-between", marginTop: 10, fontSize: 11, color: "var(--ink-dim)", letterSpacing: "0.08em" }}>
          <span>{events[0].time}</span>
          <span style={{ color: "var(--gold)" }}>{liveMsg}</span>
          <span>{events[events.length - 1].time}</span>
        </div>
      </div>

      <div style={{ position: "relative", paddingLeft: 4 }}>
        {events.map((e, i) => {
          const isCurrent = i === currentIdx;
          const isPast = i < currentIdx;
          const Icon = e.icon;
          return (
            <div key={e.time} style={{ position: "relative", display: "flex", gap: 16, paddingBottom: 22 }}>
              {/* rail */}
              {i < events.length - 1 && (
                <div style={{
                  position: "absolute", left: 19, top: 40, bottom: 0, width: 1,
                  background: isPast ? "rgba(212,175,55,0.5)" : "rgba(212,175,55,0.12)",
                }} />
              )}
              {/* node */}
              <div style={{
                width: 40, height: 40, borderRadius: "50%", flexShrink: 0,
                display: "flex", alignItems: "center", justifyContent: "center",
                background: isCurrent ? "linear-gradient(180deg, #e6c15a, #a67729)" : isPast ? "rgba(212,175,55,0.15)" : "rgba(255,250,235,0.04)",
                border: isCurrent ? "none" : `1px solid ${isPast ? "rgba(212,175,55,0.4)" : "var(--line)"}`,
                color: isCurrent ? "#0a0908" : isPast ? "var(--gold)" : "var(--ink-dim)",
                boxShadow: isCurrent ? "0 0 24px rgba(212,175,55,0.4)" : "none",
                position: "relative", zIndex: 1,
              }}>
                <Icon size={17} strokeWidth={isCurrent ? 2 : 1.5} />
              </div>
              {/* content */}
              <div style={{ flex: 1, paddingTop: 2 }}>
                <div style={{ display: "flex", alignItems: "baseline", gap: 12, marginBottom: 2 }}>
                  <span className="serif gold" style={{ fontSize: 18, fontVariantNumeric: "tabular-nums" }}>{e.time}</span>
                  {isCurrent && <span className="chip" style={{ padding: "2px 8px", fontSize: 9 }}>You are here</span>}
                </div>
                <div className="serif" style={{ fontSize: 21, color: isPast ? "var(--ink-dim)" : "var(--ink)", marginBottom: 2, textDecoration: isPast ? "line-through" : "none", textDecorationColor: "rgba(212,175,55,0.3)" }}>
                  {e.label}
                </div>
                <div style={{ fontSize: 12, color: "var(--ink-dim)", letterSpacing: "0.02em" }}>{e.note}</div>
              </div>
            </div>
          );
        })}
      </div>
    </div>
  );
}

// ============================================================
// 2. FIND YOUR TABLE
// ============================================================
function TableScreen() {
  const [query, setQuery] = useState("");
  const [selected, setSelected] = useState(null);

  const matches = useMemo(() => {
    if (!query.trim()) return [];
    const q = query.trim().toLowerCase();
    const results = [];
    TABLES.forEach((t) => {
      t.people.forEach((p) => {
        if (p.toLowerCase().includes(q)) results.push({ table: t, person: p });
      });
    });
    return results.slice(0, 8);
  }, [query]);

  return (
    <div className="reveal">
      <div className="eyebrow" style={{ marginBottom: 8 }}>Seating</div>
      <h2 className="h-display" style={{ fontSize: 36, marginBottom: 18 }}>Find your table</h2>

      <div style={{ position: "relative", marginBottom: 16 }}>
        <Search size={16} style={{ position: "absolute", left: 16, top: 16, color: "var(--ink-dim)" }} />
        <input
          value={query}
          onChange={(e) => { setQuery(e.target.value); setSelected(null); }}
          placeholder="Type your name…"
          style={{ paddingLeft: 44 }}
        />
      </div>

      {!selected && matches.length > 0 && (
        <div className="glass" style={{ padding: 6, marginBottom: 16 }}>
          {matches.map((m, i) => (
            <button key={i}
              onClick={() => { setSelected(m); setQuery(m.person); }}
              style={{
                width: "100%", textAlign: "left", padding: "12px 14px",
                background: "transparent", border: "none", color: "var(--ink)",
                display: "flex", justifyContent: "space-between", alignItems: "center",
                cursor: "pointer", borderRadius: 10, fontSize: 14,
              }}
              onMouseEnter={(e) => e.currentTarget.style.background = "rgba(212,175,55,0.06)"}
              onMouseLeave={(e) => e.currentTarget.style.background = "transparent"}
            >
              <span>{m.person}</span>
              <span style={{ color: "var(--gold)", fontSize: 12, letterSpacing: "0.1em" }}>TABLE {m.table.n} →</span>
            </button>
          ))}
        </div>
      )}

      {selected && <TableCard match={selected} />}

      {!selected && !query && (
        <>
          <div className="eyebrow" style={{ margin: "28px 0 12px" }}>All Tables</div>
          <VenueMap tables={TABLES} onSelect={(t) => setSelected({ table: t, person: null })} />
          <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 10, marginTop: 16 }}>
            {TABLES.map((t) => (
              <button key={t.n}
                onClick={() => setSelected({ table: t, person: null })}
                className="glass"
                style={{ padding: 14, textAlign: "left", cursor: "pointer", color: "var(--ink)" }}>
                <div className="gold serif" style={{ fontSize: 20, lineHeight: 1 }}>0{t.n}</div>
                <div className="serif" style={{ fontSize: 15, marginTop: 4, lineHeight: 1.15 }}>{t.name}</div>
                <div style={{ fontSize: 10, color: "var(--ink-dim)", letterSpacing: "0.08em", textTransform: "uppercase", marginTop: 4 }}>{t.people.length} seats</div>
              </button>
            ))}
          </div>
        </>
      )}
    </div>
  );
}

function TableCard({ match }) {
  const { table, person } = match;
  return (
    <div className="glass-strong reveal" style={{ padding: 24, marginBottom: 16 }}>
      {person && (
        <div style={{ marginBottom: 16 }}>
          <div className="eyebrow" style={{ marginBottom: 4 }}>Hello</div>
          <div className="serif" style={{ fontSize: 24 }}>{person}</div>
        </div>
      )}
      <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", marginBottom: 12 }}>
        <div>
          <div className="eyebrow" style={{ marginBottom: 4 }}>Your Table</div>
          <div className="serif" style={{ fontSize: 30, lineHeight: 1 }}>{table.name}</div>
        </div>
        <div className="serif gold" style={{ fontSize: 48, lineHeight: 0.9 }}>0{table.n}</div>
      </div>
      <div className="hairline" style={{ margin: "14px 0" }} />
      <div style={{ fontSize: 13, color: "var(--ink-dim)", fontStyle: "italic", marginBottom: 16 }}>
        "{table.desc}"
      </div>

      <div className="eyebrow" style={{ marginBottom: 10 }}>Seated with you</div>
      <div style={{ display: "flex", flexWrap: "wrap", gap: 8, marginBottom: 18 }}>
        {table.people.map((p) => {
          const isYou = p === person;
          const initials = p.split(" ").map(x => x[0]).join("").slice(0, 2);
          return (
            <div key={p} style={{
              display: "flex", alignItems: "center", gap: 8,
              padding: "6px 12px 6px 6px",
              background: isYou ? "rgba(212,175,55,0.12)" : "rgba(255,250,235,0.03)",
              border: `1px solid ${isYou ? "rgba(212,175,55,0.4)" : "var(--line)"}`,
              borderRadius: 999,
            }}>
              <div style={{
                width: 26, height: 26, borderRadius: "50%",
                background: isYou ? "linear-gradient(135deg, #e6c15a, #8a6a1e)" : "rgba(212,175,55,0.15)",
                color: isYou ? "#0a0908" : "var(--gold)",
                display: "flex", alignItems: "center", justifyContent: "center",
                fontSize: 10, fontWeight: 600, letterSpacing: "0.05em",
              }}>{initials}</div>
              <span style={{ fontSize: 12, color: isYou ? "var(--gold)" : "var(--ink)" }}>{p}{isYou ? " (you)" : ""}</span>
            </div>
          );
        })}
      </div>

      <VenueMap tables={TABLES} highlight={table.n} />
    </div>
  );
}

function VenueMap({ tables, highlight, onSelect }) {
  // mini venue layout — abstract positions
  const positions = {
    1: { x: 50, y: 22 },   2: { x: 75, y: 22 },
    3: { x: 25, y: 35 },   4: { x: 50, y: 42 },  5: { x: 75, y: 42 },
    6: { x: 25, y: 55 },   7: { x: 50, y: 62 },  8: { x: 75, y: 62 },
    9: { x: 25, y: 75 },  10: { x: 50, y: 82 }, 11: { x: 75, y: 82 },
   12: { x: 50, y: 92 },
  };

  return (
    <div style={{
      position: "relative", width: "100%", aspectRatio: "1 / 1.1",
      background: "radial-gradient(ellipse at top, rgba(212,175,55,0.08), transparent 60%), rgba(255,250,235,0.02)",
      border: "1px solid var(--line)", borderRadius: 16, overflow: "hidden",
    }}>
      {/* stage / dancefloor */}
      <div style={{
        position: "absolute", left: "35%", right: "35%", top: 12, height: 18,
        border: "1px solid rgba(212,175,55,0.4)", borderRadius: 4,
        display: "flex", alignItems: "center", justifyContent: "center",
        fontSize: 8, letterSpacing: "0.3em", color: "var(--gold)", textTransform: "uppercase",
      }}>Stage</div>
      <div style={{
        position: "absolute", left: "30%", right: "30%", bottom: 12, top: "auto", height: 40,
        border: "1px dashed rgba(212,175,55,0.3)", borderRadius: 8,
        display: "flex", alignItems: "center", justifyContent: "center",
        fontSize: 8, letterSpacing: "0.3em", color: "var(--ink-dim)", textTransform: "uppercase",
      }}>Dancefloor</div>

      {tables.map((t) => {
        const p = positions[t.n] || { x: 50, y: 50 };
        const isHi = t.n === highlight;
        return (
          <button key={t.n}
            onClick={() => onSelect && onSelect(t)}
            style={{
              position: "absolute", left: `${p.x}%`, top: `${p.y}%`,
              transform: "translate(-50%, -50%)",
              width: 26, height: 26, borderRadius: "50%",
              background: isHi ? "linear-gradient(135deg, #e6c15a, #8a6a1e)" : "rgba(8,7,10,0.8)",
              border: `1px solid ${isHi ? "var(--gold)" : "rgba(212,175,55,0.3)"}`,
              color: isHi ? "#0a0908" : "var(--gold)",
              fontSize: 10, fontWeight: 600,
              cursor: onSelect ? "pointer" : "default",
              boxShadow: isHi ? "0 0 20px rgba(212,175,55,0.6)" : "none",
              fontVariantNumeric: "tabular-nums",
            }}>
            {t.n}
          </button>
        );
      })}
    </div>
  );
}

// ============================================================
// 3. QUIZ
// ============================================================
function QuizScreen() {
  const [idx, setIdx] = useState(0);
  const [answers, setAnswers] = useState([]);
  const [locked, setLocked] = useState(false);
  const [selected, setSelected] = useState(null);
  const [startTime, setStartTime] = useState(Date.now());

  const leaderboard = [
    { name: "Sem",       score: 92 },
    { name: "Despina",   score: 88 },
    { name: "Andreas",   score: 84 },
    { name: "Marina",    score: 79 },
    { name: "You",       score: answers.reduce((s, a) => s + a.points, 0), isYou: true },
  ].sort((a, b) => b.score - a.score);

  useEffect(() => { setStartTime(Date.now()); }, [idx]);

  if (idx >= QUIZ.length) {
    return <QuizDone answers={answers} leaderboard={leaderboard} onRestart={() => { setIdx(0); setAnswers([]); setSelected(null); setLocked(false); }} />;
  }

  const q = QUIZ[idx];

  const pick = (opt) => {
    if (locked) return;
    const elapsed = (Date.now() - startTime) / 1000;
    const correct = opt === q.a;
    const base = correct ? 100 : 0;
    const speed = correct ? Math.max(0, Math.floor(50 - elapsed * 5)) : 0;
    const points = base + speed;
    setSelected(opt);
    setLocked(true);
    setTimeout(() => {
      setAnswers((a) => [...a, { q: q.q, correct, points }]);
      setSelected(null);
      setLocked(false);
      setIdx((i) => i + 1);
    }, 1100);
  };

  return (
    <div className="reveal">
      <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 18 }}>
        <div className="eyebrow">Round {idx + 1} / {QUIZ.length}</div>
        <div className="chip" style={{ padding: "4px 10px" }}>
          <Trophy size={10} /> {answers.reduce((s, a) => s + a.points, 0)} pts
        </div>
      </div>

      <div className="progress-rail" style={{ marginBottom: 24 }}>
        <div className="progress-fill" style={{ width: `${(idx / QUIZ.length) * 100}%`, transition: "width 0.4s" }} />
      </div>

      <div className="h-display" style={{ fontSize: 28, marginBottom: 28, lineHeight: 1.15 }}>{q.q}</div>

      <div style={{ display: "flex", flexDirection: "column", gap: 10 }}>
        {q.opts.map((opt, i) => {
          const isSel = selected === i;
          const isCorrect = locked && i === q.a;
          const isWrong = locked && isSel && i !== q.a;
          return (
            <button key={i} disabled={locked} onClick={() => pick(i)}
              className="glass"
              style={{
                padding: "16px 18px", textAlign: "left", cursor: locked ? "default" : "pointer",
                color: "var(--ink)", display: "flex", justifyContent: "space-between", alignItems: "center",
                borderColor: isCorrect ? "rgba(148, 200, 120, 0.6)" : isWrong ? "rgba(220, 100, 100, 0.5)" : "var(--line)",
                background: isCorrect ? "rgba(148, 200, 120, 0.1)" : isWrong ? "rgba(220, 100, 100, 0.08)" : "var(--glass)",
                transition: "all 0.3s",
              }}>
              <span className="serif" style={{ fontSize: 17 }}>{opt}</span>
              {isCorrect && <Check size={18} style={{ color: "#94c878" }} />}
              {isWrong && <X size={18} style={{ color: "#dc6464" }} />}
            </button>
          );
        })}
      </div>

      <div className="hairline" style={{ margin: "32px 0 18px" }} />
      <div className="eyebrow" style={{ marginBottom: 12 }}>Live Leaderboard</div>
      <div style={{ display: "flex", flexDirection: "column", gap: 4 }}>
        {leaderboard.slice(0, 5).map((p, i) => (
          <div key={p.name} style={{
            display: "flex", justifyContent: "space-between", alignItems: "center",
            padding: "10px 14px", borderRadius: 10,
            background: p.isYou ? "rgba(212,175,55,0.08)" : "transparent",
            border: p.isYou ? "1px solid rgba(212,175,55,0.25)" : "1px solid transparent",
          }}>
            <div style={{ display: "flex", alignItems: "center", gap: 12 }}>
              <span className="serif gold" style={{ fontSize: 15, width: 18 }}>{i + 1}</span>
              <span style={{ fontSize: 14, color: p.isYou ? "var(--gold)" : "var(--ink)" }}>{p.name}{p.isYou ? " (you)" : ""}</span>
            </div>
            <span className="serif" style={{ fontSize: 15, fontVariantNumeric: "tabular-nums" }}>{p.score}</span>
          </div>
        ))}
      </div>
    </div>
  );
}

function QuizDone({ answers, leaderboard, onRestart }) {
  const total = answers.reduce((s, a) => s + a.points, 0);
  const correctCount = answers.filter((a) => a.correct).length;
  return (
    <div className="reveal">
      <div className="glass-strong" style={{ padding: 28, textAlign: "center", marginBottom: 20 }}>
        <Trophy size={40} className="gold" style={{ marginBottom: 14 }} strokeWidth={1} />
        <div className="eyebrow" style={{ marginBottom: 8 }}>Round Complete</div>
        <div className="h-display" style={{ fontSize: 48, marginBottom: 6 }}>{total}</div>
        <div style={{ color: "var(--ink-dim)", fontSize: 13 }}>{correctCount} of {answers.length} correct</div>
        <button className="btn-gold" style={{ marginTop: 22 }} onClick={onRestart}>Play Again</button>
      </div>

      <div className="eyebrow" style={{ marginBottom: 12 }}>Leaderboard</div>
      {leaderboard.map((p, i) => (
        <div key={p.name} className="glass" style={{ display: "flex", justifyContent: "space-between", alignItems: "center", padding: "14px 18px", marginBottom: 6, background: p.isYou ? "rgba(212,175,55,0.08)" : "var(--glass)" }}>
          <div style={{ display: "flex", alignItems: "center", gap: 14 }}>
            <span className="serif gold" style={{ fontSize: 18 }}>{i + 1}</span>
            <span className="serif" style={{ fontSize: 17, color: p.isYou ? "var(--gold)" : "var(--ink)" }}>{p.name}</span>
          </div>
          <span className="serif" style={{ fontSize: 18, fontVariantNumeric: "tabular-nums" }}>{p.score}</span>
        </div>
      ))}
    </div>
  );
}

// ============================================================
// 4. PHOTOS
// ============================================================
function PhotosScreen() {
  const CATS = ["All", "Ceremony", "Food", "Dancefloor", "Funny", "Behind", "Couple"];
  const [cat, setCat] = useState("All");
  const [photos, setPhotos] = useState(seedPhotos());
  const fileRef = useRef(null);

  const filtered = cat === "All" ? photos : photos.filter((p) => p.cat === cat);

  const upload = (e) => {
    const files = Array.from(e.target.files || []);
    files.forEach((f) => {
      const url = URL.createObjectURL(f);
      setPhotos((list) => [{
        id: Date.now() + Math.random(), url, cat: "Funny", author: "You", likes: 0, liked: false
      }, ...list]);
    });
  };

  const toggleLike = (id) => {
    setPhotos((list) => list.map((p) => p.id === id ? { ...p, liked: !p.liked, likes: p.likes + (p.liked ? -1 : 1) } : p));
  };

  return (
    <div className="reveal">
      <div className="eyebrow" style={{ marginBottom: 8 }}>Disposable Camera</div>
      <h2 className="h-display" style={{ fontSize: 36, marginBottom: 6 }}>The Photo Wall</h2>
      <div style={{ color: "var(--ink-dim)", fontSize: 13, marginBottom: 20, fontStyle: "italic" }}>
        Every hidden moment the official camera missed.
      </div>

      <div style={{ display: "flex", gap: 10, marginBottom: 18 }}>
        <button className="btn-gold" style={{ flex: 1 }} onClick={() => fileRef.current?.click()}>
          <Upload size={14} style={{ verticalAlign: "-2px", marginRight: 8 }} />Upload
        </button>
        <button className="btn-ghost" onClick={() => fileRef.current?.click()}>
          <Camera size={14} style={{ verticalAlign: "-2px" }} />
        </button>
        <input ref={fileRef} type="file" accept="image/*" multiple onChange={upload} style={{ display: "none" }} />
      </div>

      <div style={{ display: "flex", gap: 8, overflowX: "auto", paddingBottom: 12, marginBottom: 12, marginLeft: -20, marginRight: -20, paddingLeft: 20, paddingRight: 20, scrollbarWidth: "none" }}>
        {CATS.map((c) => (
          <button key={c} onClick={() => setCat(c)} style={{
            flexShrink: 0, padding: "8px 14px", borderRadius: 999,
            background: cat === c ? "var(--gold)" : "transparent",
            color: cat === c ? "#0a0908" : "var(--ink-dim)",
            border: `1px solid ${cat === c ? "var(--gold)" : "var(--line)"}`,
            fontSize: 11, letterSpacing: "0.1em", textTransform: "uppercase", cursor: "pointer",
            fontWeight: cat === c ? 600 : 400,
          }}>{c}</button>
        ))}
      </div>

      <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 10 }}>
        {filtered.map((p) => (
          <div key={p.id} style={{ position: "relative", borderRadius: 14, overflow: "hidden", aspectRatio: "3 / 4", background: p.url.startsWith("blob") ? "#222" : p.url }}>
            {p.url.startsWith("blob") && <img src={p.url} alt="" style={{ width: "100%", height: "100%", objectFit: "cover" }} />}
            <div style={{
              position: "absolute", inset: 0,
              background: "linear-gradient(180deg, transparent 55%, rgba(0,0,0,0.85))",
            }} />
            <div style={{ position: "absolute", top: 8, left: 8 }}>
              <span className="chip" style={{ padding: "3px 8px", fontSize: 9, background: "rgba(0,0,0,0.4)" }}>{p.cat}</span>
            </div>
            <div style={{ position: "absolute", bottom: 8, left: 10, right: 10, display: "flex", justifyContent: "space-between", alignItems: "flex-end" }}>
              <span style={{ fontSize: 11, color: "rgba(255,255,255,0.8)" }}>@{p.author}</span>
              <button onClick={() => toggleLike(p.id)} style={{
                background: "rgba(0,0,0,0.4)", backdropFilter: "blur(8px)", border: "1px solid rgba(255,255,255,0.15)",
                borderRadius: 999, padding: "4px 10px", color: p.liked ? "var(--gold)" : "white",
                fontSize: 11, display: "flex", alignItems: "center", gap: 5, cursor: "pointer",
              }}>
                <Heart size={11} fill={p.liked ? "var(--gold)" : "none"} />{p.likes}
              </button>
            </div>
          </div>
        ))}
      </div>

      <div className="glass" style={{ padding: 16, marginTop: 20, textAlign: "center" }}>
        <div className="eyebrow" style={{ marginBottom: 6 }}>Photo of the Night</div>
        <div style={{ fontSize: 12, color: "var(--ink-dim)" }}>Voting opens at 02:00. Like your favorites now.</div>
      </div>
    </div>
  );
}

function seedPhotos() {
  // Abstract CSS gradient "photos" so it works with no network
  const palette = [
    "linear-gradient(135deg, #2a1810 0%, #8a5a2e 50%, #d4af37 100%)",
    "linear-gradient(160deg, #1a0f1f 0%, #5a2a5e 60%, #d4af37 100%)",
    "linear-gradient(200deg, #0f1a1a 0%, #2e5a5a 50%, #e6c15a 100%)",
    "linear-gradient(45deg, #1f1a0f 0%, #8a6a2e 70%, #f5ecd7 100%)",
    "linear-gradient(315deg, #1a0f0f 0%, #5a1a1a 50%, #c9a24b 100%)",
    "linear-gradient(135deg, #0a0a1a 0%, #2a2a5a 60%, #d4af37 100%)",
    "linear-gradient(180deg, #1a1008 0%, #5a3a1a 50%, #e6c15a 100%)",
    "linear-gradient(225deg, #1f0a1a 0%, #5a1a4e 60%, #d4af37 100%)",
  ];
  const cats = ["Ceremony", "Food", "Dancefloor", "Funny", "Behind", "Couple"];
  const authors = ["Sem", "Despina", "Andreas", "Marina", "Lotte", "Petros", "Sofia"];
  return Array.from({ length: 8 }, (_, i) => ({
    id: i + 1,
    url: palette[i],
    cat: cats[i % cats.length],
    author: authors[i % authors.length],
    likes: Math.floor(Math.random() * 40) + 3,
    liked: false,
  }));
}

// ============================================================
// 5. MESSAGES
// ============================================================
function MessagesScreen() {
  const [messages, setMessages] = useState([
    { id: 1, name: "Sem & Lotte", type: "Wish",   text: "May your life together be as beautiful and chaotic as your dancefloor will be tonight. We love you both." },
    { id: 2, name: "Despina",     type: "Story",  text: "I remember the exact moment Chara told me about Kostas. Her eyes did that thing. I knew." },
    { id: 3, name: "Andreas",     type: "Joke",   text: "Kostas, remember: the first 10 years are the hardest. Someone told me that on year 11." },
    { id: 4, name: "Mom",         type: "Memory", text: "My little girl. I watched you grow up dreaming of this day. And he was worth the wait." },
  ]);
  const [name, setName] = useState("");
  const [type, setType] = useState("Wish");
  const [text, setText] = useState("");
  const TYPES = ["Wish", "Story", "Advice", "Joke", "Memory"];

  const submit = () => {
    if (!name.trim() || !text.trim()) return;
    setMessages((m) => [{ id: Date.now(), name, type, text }, ...m]);
    setName(""); setText("");
  };

  return (
    <div className="reveal">
      <div className="eyebrow" style={{ marginBottom: 8 }}>For the Couple</div>
      <h2 className="h-display" style={{ fontSize: 36, marginBottom: 18 }}>Leave a <span className="amp">wish</span></h2>

      <div className="glass-strong" style={{ padding: 18, marginBottom: 24 }}>
        <input value={name} onChange={(e) => setName(e.target.value)} placeholder="Your name" style={{ marginBottom: 10 }} />
        <div style={{ display: "flex", gap: 6, marginBottom: 10, flexWrap: "wrap" }}>
          {TYPES.map((t) => (
            <button key={t} onClick={() => setType(t)} style={{
              padding: "6px 12px", borderRadius: 999, fontSize: 10, letterSpacing: "0.1em", textTransform: "uppercase",
              background: type === t ? "var(--gold)" : "transparent",
              color: type === t ? "#0a0908" : "var(--ink-dim)",
              border: `1px solid ${type === t ? "var(--gold)" : "var(--line)"}`,
              cursor: "pointer", fontWeight: type === t ? 600 : 400,
            }}>{t}</button>
          ))}
        </div>
        <textarea value={text} onChange={(e) => setText(e.target.value)} placeholder="Write something beautiful, funny, or honest…" rows={4} style={{ resize: "none", marginBottom: 12 }} />
        <button className="btn-gold" onClick={submit} style={{ width: "100%" }}>
          <Send size={12} style={{ verticalAlign: "-1px", marginRight: 8 }} />Send to Kostas & Chara
        </button>
      </div>

      <div className="eyebrow" style={{ marginBottom: 14 }}>The Wall · {messages.length}</div>
      <div style={{ display: "flex", flexDirection: "column", gap: 12 }}>
        {messages.map((m, i) => (
          <article key={m.id} className="glass" style={{ padding: 20, animationDelay: `${i * 60}ms` }}>
            <div style={{ display: "flex", justifyContent: "space-between", alignItems: "baseline", marginBottom: 10 }}>
              <div className="serif gold" style={{ fontSize: 19 }}>{m.name}</div>
              <span style={{ fontSize: 9, letterSpacing: "0.2em", textTransform: "uppercase", color: "var(--ink-dim)" }}>{m.type}</span>
            </div>
            <Quote size={14} className="gold" style={{ opacity: 0.5, marginBottom: 6 }} />
            <div className="serif" style={{ fontSize: 17, lineHeight: 1.5, fontStyle: "italic", color: "var(--ink)" }}>
              {m.text}
            </div>
          </article>
        ))}
      </div>
    </div>
  );
}

// ============================================================
// 6. MUSIC VOTING
// ============================================================
function MusicScreen() {
  const [blocks, setBlocks] = useState(MUSIC_BLOCKS);
  const [activeBlock, setActiveBlock] = useState(blocks[1].id);
  const [voted, setVoted] = useState({});
  const [suggestion, setSuggestion] = useState("");

  const block = blocks.find((b) => b.id === activeBlock);
  const sorted = [...block.songs].sort((a, b) => b.v - a.v);

  const vote = (title) => {
    const key = `${activeBlock}:${title}`;
    if (voted[key]) return;
    setVoted((v) => ({ ...v, [key]: true }));
    setBlocks((bs) => bs.map((b) => b.id !== activeBlock ? b : {
      ...b, songs: b.songs.map((s) => s.t === title ? { ...s, v: s.v + 1 } : s)
    }));
  };

  const suggest = () => {
    if (!suggestion.trim()) return;
    setBlocks((bs) => bs.map((b) => b.id !== activeBlock ? b : {
      ...b, songs: [...b.songs, { t: suggestion.trim(), v: 1, suggested: true }]
    }));
    setSuggestion("");
  };

  return (
    <div className="reveal">
      <div className="eyebrow" style={{ marginBottom: 8 }}>DJ Vote</div>
      <h2 className="h-display" style={{ fontSize: 36, marginBottom: 6 }}>Shape the <span className="amp">night</span></h2>
      <div style={{ color: "var(--ink-dim)", fontSize: 13, marginBottom: 20, fontStyle: "italic" }}>
        Top 3 in each block get played. Cast wisely.
      </div>

      <div style={{ display: "flex", gap: 8, overflowX: "auto", paddingBottom: 12, marginBottom: 18, marginLeft: -20, marginRight: -20, paddingLeft: 20, paddingRight: 20, scrollbarWidth: "none" }}>
        {blocks.map((b) => {
          const active = b.id === activeBlock;
          return (
            <button key={b.id} onClick={() => setActiveBlock(b.id)} style={{
              flexShrink: 0, padding: "10px 16px", borderRadius: 12,
              background: active ? "rgba(212,175,55,0.1)" : "transparent",
              border: `1px solid ${active ? b.color : "var(--line)"}`,
              cursor: "pointer", textAlign: "left", minWidth: 140,
            }}>
              <div style={{ fontSize: 9, letterSpacing: "0.2em", color: active ? b.color : "var(--ink-dim)", textTransform: "uppercase", marginBottom: 2 }}>{b.time}</div>
              <div className="serif" style={{ fontSize: 14, color: active ? "var(--ink)" : "var(--ink-dim)" }}>{b.name}</div>
            </button>
          );
        })}
      </div>

      <div className="glass-strong" style={{ padding: 20, marginBottom: 16 }}>
        <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 16 }}>
          <div>
            <div className="eyebrow" style={{ marginBottom: 2 }}>{block.time} · Now Voting</div>
            <div className="serif" style={{ fontSize: 22, color: block.color }}>{block.name}</div>
          </div>
          <Disc3 size={28} style={{ color: block.color, animation: "shim 8s linear infinite" }} strokeWidth={1} />
        </div>

        <div style={{ display: "flex", flexDirection: "column", gap: 8 }}>
          {sorted.map((s, i) => {
            const key = `${activeBlock}:${s.t}`;
            const hasVoted = voted[key];
            const max = sorted[0].v;
            const pct = (s.v / max) * 100;
            const isTop3 = i < 3;
            return (
              <div key={s.t} style={{ position: "relative", padding: "12px 14px", borderRadius: 10, overflow: "hidden", background: "rgba(255,250,235,0.03)", border: `1px solid ${isTop3 ? "rgba(212,175,55,0.25)" : "var(--line)"}` }}>
                <div style={{
                  position: "absolute", left: 0, top: 0, bottom: 0, width: `${pct}%`,
                  background: `linear-gradient(90deg, ${block.color}22, ${block.color}08)`,
                  transition: "width 0.5s",
                }} />
                <div style={{ position: "relative", display: "flex", justifyContent: "space-between", alignItems: "center" }}>
                  <div style={{ display: "flex", alignItems: "center", gap: 12, flex: 1, minWidth: 0 }}>
                    <span className="serif" style={{ fontSize: 14, color: isTop3 ? block.color : "var(--ink-dim)", width: 20 }}>{String(i + 1).padStart(2, "0")}</span>
                    <span className="serif" style={{ fontSize: 15, color: "var(--ink)", overflow: "hidden", textOverflow: "ellipsis", whiteSpace: "nowrap" }}>
                      {s.t}
                      {s.suggested && <span style={{ fontSize: 9, color: "var(--ink-dim)", marginLeft: 8, letterSpacing: "0.1em", textTransform: "uppercase" }}>· new</span>}
                    </span>
                  </div>
                  <button onClick={() => vote(s.t)} disabled={hasVoted} style={{
                    background: hasVoted ? "rgba(212,175,55,0.15)" : "transparent",
                    border: `1px solid ${hasVoted ? block.color : "var(--line)"}`,
                    color: hasVoted ? block.color : "var(--ink)",
                    padding: "5px 10px", borderRadius: 999, cursor: hasVoted ? "default" : "pointer",
                    fontSize: 11, display: "flex", alignItems: "center", gap: 5, fontVariantNumeric: "tabular-nums",
                  }}>
                    <ThumbsUp size={10} fill={hasVoted ? block.color : "none"} />{s.v}
                  </button>
                </div>
              </div>
            );
          })}
        </div>
      </div>

      <div className="glass" style={{ padding: 16 }}>
        <div className="eyebrow" style={{ marginBottom: 10 }}>Suggest a song for this block</div>
        <div style={{ display: "flex", gap: 8 }}>
          <input value={suggestion} onChange={(e) => setSuggestion(e.target.value)} placeholder="Artist — Song" style={{ flex: 1 }} />
          <button className="btn-gold" onClick={suggest} style={{ padding: "0 18px" }}>Add</button>
        </div>
        <div style={{ fontSize: 10, color: "var(--ink-dim)", marginTop: 10, letterSpacing: "0.05em", fontStyle: "italic" }}>
          DJ approves additions. Songs must match the block's mood.
        </div>
      </div>
    </div>
  );
}
