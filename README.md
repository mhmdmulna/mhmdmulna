<div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center', width: '100%', height: '100%', background: '#06060a', borderRadius: 20, padding: 30, fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden', border: '1px solid rgba(110,80,220,0.2)' }}>
  <style>
    {`
      @keyframes hdr-drift-r { 0%, 100% { transform: translate(0, 0); opacity: 0.7; } 50% { transform: translate(45px, -22px); opacity: 1.15; } }
      @keyframes hdr-drift-l { 0%, 100% { transform: translate(0, 0); opacity: 0.6; } 50% { transform: translate(-40px, 20px); opacity: 1.05; } }
      @keyframes hdr-drift-u { 0%, 100% { transform: translate(0, 0); opacity: 0.75; } 50% { transform: translate(30px, -30px); opacity: 1.1; } }
      @keyframes hdr-pulse { 0%, 100% { transform: scale(1); opacity: 0.6; } 50% { transform: scale(1.3); opacity: 0.35; } }
      @keyframes hdr-scan { 0% { transform: translate(-900px, 0); opacity: 0; } 10% { opacity: 1; } 90% { opacity: 1; } 100% { transform: translate(900px, 0); opacity: 0; } }
      @keyframes hdr-ring-pulse { 0%, 100% { transform: scale(0.9); opacity: 0.15; } 50% { transform: scale(1.1); opacity: 0.4; } }
      @keyframes hdr-ring2-pulse { 0%, 100% { transform: scale(1.1); opacity: 0.1; } 50% { transform: scale(0.85); opacity: 0.3; } }
      @keyframes hdr-draw { 0% { stroke-dashoffset: 500; } 100% { stroke-dashoffset: 0; } }
      @keyframes hdr-draw-rev { 0% { stroke-dashoffset: 0; } 100% { stroke-dashoffset: -400; } }
      @keyframes hdr-dot-float { 0%, 100% { transform: translate(0, 0); opacity: 0.4; } 50% { transform: translate(12px, -18px); opacity: 1; } }
      @keyframes hdr-dot-float2 { 0%, 100% { transform: translate(0, 0); opacity: 0.3; } 50% { transform: translate(-15px, 14px); opacity: 0.9; } }
      @keyframes hdr-dot-float3 { 0%, 100% { transform: translate(0, 0); opacity: 0.5; } 50% { transform: translate(8px, 20px); opacity: 0.8; } }
      @keyframes hdr-line-glow { 0%, 100% { opacity: 0.2; } 50% { opacity: 0.7; } }
      #hdr-g1 { animation: hdr-drift-r 6.5s ease-in-out infinite; }
      #hdr-g2 { animation: hdr-drift-l 8.2s ease-in-out infinite 0.4s; }
      #hdr-g3 { animation: hdr-drift-u 7.0s ease-in-out infinite 0.7s; }
      #hdr-g4 { animation: hdr-pulse 5.0s ease-in-out infinite; }
      #hdr-g5 { animation: hdr-drift-r 9.5s ease-in-out infinite 0.2s; }
      #hdr-g6 { animation: hdr-drift-l 6.8s ease-in-out infinite 0.6s; }
      #hdr-g7 { animation: hdr-drift-u 8.0s ease-in-out infinite 0.1s; }
      #hdr-g8 { animation: hdr-pulse 7.5s ease-in-out infinite 0.5s; }
      #hdr-scan1 { animation: hdr-scan 4s linear infinite; }
      #hdr-scan2 { animation: hdr-scan 4.5s linear infinite 2s; }
      #hdr-ring1 { animation: hdr-ring-pulse 4s ease-in-out infinite; }
      #hdr-ring2 { animation: hdr-ring2-pulse 5s ease-in-out infinite 0.5s; }
      #hdr-path1 { animation: hdr-draw 3s ease-in-out infinite; }
      #hdr-path2 { animation: hdr-draw-rev 4s ease-in-out infinite 0.5s; }
      #hdr-dot1 { animation: hdr-dot-float 3.5s ease-in-out infinite; }
      #hdr-dot2 { animation: hdr-dot-float2 4.2s ease-in-out infinite 0.3s; }
      #hdr-dot3 { animation: hdr-dot-float3 3.8s ease-in-out infinite 0.6s; }
      #hdr-dot4 { animation: hdr-dot-float 5s ease-in-out infinite 0.8s; }
      #hdr-dot5 { animation: hdr-dot-float2 4.5s ease-in-out infinite 1s; }
      #hdr-dot6 { animation: hdr-dot-float3 3.2s ease-in-out infinite 0.2s; }
      #hdr-dot7 { animation: hdr-dot-float 4.8s ease-in-out infinite 1.2s; }
      #hdr-dot8 { animation: hdr-dot-float2 3.6s ease-in-out infinite 0.4s; }
      #hdr-hline1 { animation: hdr-line-glow 3s ease-in-out infinite; }
      #hdr-hline2 { animation: hdr-line-glow 4s ease-in-out infinite 1s; }
      #hdr-hline3 { animation: hdr-line-glow 3.5s ease-in-out infinite 2s; }
    `}
  </style>
  <svg width="800" height="260" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="hg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(138,43,226,0.65)" />
        <stop offset="60%" stopColor="rgba(138,43,226,0.15)" />
        <stop offset="100%" stopColor="rgba(138,43,226,0)" />
      </radialGradient>
      <radialGradient id="hg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(20,80,255,0.6)" />
        <stop offset="60%" stopColor="rgba(20,80,255,0.12)" />
        <stop offset="100%" stopColor="rgba(20,80,255,0)" />
      </radialGradient>
      <radialGradient id="hg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,220,240,0.55)" />
        <stop offset="100%" stopColor="rgba(0,220,240,0)" />
      </radialGradient>
      <radialGradient id="hg4" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(220,40,255,0.5)" />
        <stop offset="100%" stopColor="rgba(220,40,255,0)" />
      </radialGradient>
      <radialGradient id="hg5" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(255,40,120,0.45)" />
        <stop offset="100%" stopColor="rgba(255,40,120,0)" />
      </radialGradient>
      <radialGradient id="hg6" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(60,50,255,0.5)" />
        <stop offset="100%" stopColor="rgba(60,50,255,0)" />
      </radialGradient>
      <radialGradient id="hg7" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,200,180,0.4)" />
        <stop offset="100%" stopColor="rgba(0,200,180,0)" />
      </radialGradient>
      <radialGradient id="hg8" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(200,20,200,0.5)" />
        <stop offset="100%" stopColor="rgba(200,20,200,0)" />
      </radialGradient>
      <linearGradient id="hg-scan" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stopColor="rgba(120,200,255,0)" />
        <stop offset="40%" stopColor="rgba(120,200,255,0.15)" />
        <stop offset="50%" stopColor="rgba(120,200,255,0.4)" />
        <stop offset="60%" stopColor="rgba(120,200,255,0.15)" />
        <stop offset="100%" stopColor="rgba(120,200,255,0)" />
      </linearGradient>
      <linearGradient id="hg-hline" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stopColor="rgba(138,43,226,0)" />
        <stop offset="15%" stopColor="rgba(100,60,255,0.25)" />
        <stop offset="50%" stopColor="rgba(80,200,255,0.5)" />
        <stop offset="85%" stopColor="rgba(200,50,255,0.25)" />
        <stop offset="100%" stopColor="rgba(200,50,255,0)" />
      </linearGradient>
    </defs>
    <ellipse id="hdr-g1" cx="80" cy="50" rx="180" ry="120" fill="url(#hg1)" />
    <ellipse id="hdr-g2" cx="720" cy="70" rx="160" ry="110" fill="url(#hg2)" />
    <ellipse id="hdr-g3" cx="400" cy="220" rx="200" ry="120" fill="url(#hg3)" />
    <ellipse id="hdr-g4" cx="220" cy="180" rx="130" ry="90" fill="url(#hg4)" />
    <ellipse id="hdr-g5" cx="620" cy="200" rx="140" ry="95" fill="url(#hg5)" />
    <ellipse id="hdr-g6" cx="30" cy="170" rx="110" ry="80" fill="url(#hg6)" />
    <ellipse id="hdr-g7" cx="770" cy="30" rx="120" ry="85" fill="url(#hg7)" />
    <ellipse id="hdr-g8" cx="350" cy="20" rx="100" ry="70" fill="url(#hg8)" />
    <circle id="hdr-ring1" cx="400" cy="110" r="80" fill="none" stroke="rgba(120,80,255,0.2)" strokeWidth="1" />
    <circle id="hdr-ring2" cx="400" cy="110" r="120" fill="none" stroke="rgba(80,180,255,0.12)" strokeWidth="1" />
    <rect id="hdr-scan1" x="0" y="90" width="200" height="1" fill="url(#hg-scan)" />
    <rect id="hdr-scan2" x="0" y="135" width="160" height="1" fill="url(#hg-scan)" />
    <path id="hdr-path1" d="M 50 240 Q 200 200 400 230 Q 600 260 750 220" fill="none" stroke="rgba(138,43,226,0.2)" strokeWidth="1" strokeDasharray="250 250" strokeLinecap="round" />
    <path id="hdr-path2" d="M 50 20 Q 200 50 400 25 Q 600 0 750 40" fill="none" stroke="rgba(80,200,255,0.15)" strokeWidth="1" strokeDasharray="200 200" strokeLinecap="round" />
    <circle id="hdr-dot1" cx="120" cy="45" r="2" fill="rgba(120,200,255,0.8)" />
    <circle id="hdr-dot2" cx="680" cy="55" r="1.5" fill="rgba(200,120,255,0.7)" />
    <circle id="hdr-dot3" cx="300" cy="200" r="2" fill="rgba(255,120,200,0.6)" />
    <circle id="hdr-dot4" cx="550" cy="30" r="1.5" fill="rgba(120,255,200,0.7)" />
    <circle id="hdr-dot5" cx="150" cy="180" r="2" fill="rgba(100,150,255,0.8)" />
    <circle id="hdr-dot6" cx="650" cy="190" r="1.5" fill="rgba(255,180,120,0.6)" />
    <circle id="hdr-dot7" cx="450" cy="240" r="2" fill="rgba(180,120,255,0.7)" />
    <circle id="hdr-dot8" cx="250" cy="25" r="1.5" fill="rgba(120,220,255,0.8)" />
    <rect id="hdr-hline1" x="80" y="148" width="640" height="1" fill="url(#hg-hline)" rx="1" />
    <rect id="hdr-hline2" x="150" y="152" width="500" height="1" fill="url(#hg-hline)" rx="1" />
    <rect id="hdr-hline3" x="250" y="156" width="300" height="1" fill="url(#hg-hline)" rx="1" />
  </svg>
  <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', zIndex: 10, gap: 4 }}>
    <span style={{ fontSize: 64, fontWeight: 900, background: 'linear-gradient(135deg, #ffffff 0%, #d0c0ff 30%, #7ee7ff 55%, #ff88cc 80%, #ffffff 100%)', backgroundClip: 'text', WebkitBackgroundClip: 'text', color: 'transparent', letterSpacing: 10 }}>ACE</span>
    <span style={{ fontSize: 14, color: '#6a6a8a', fontWeight: 400, letterSpacing: 4, textTransform: 'uppercase', marginTop: 2 }}>Abhishek Anand</span>
    <span style={{ fontSize: 12, color: '#4a4a6a', fontWeight: 300, letterSpacing: 1.5, marginTop: 6 }}>Low-level Systems Programmer | Performance Engineering | Bare-metal</span>
  </div>
  <div style={{ display: 'flex', gap: 8, marginTop: 22, zIndex: 10 }}>
    <span style={{ padding: '5px 16px', background: 'rgba(8,6,14,0.7)', color: '#7ee7ff', borderRadius: 14, fontSize: 12, fontWeight: 600, border: '1px solid rgba(120,200,255,0.2)', letterSpacing: 1 }}>OSDEV</span>
    <span style={{ padding: '5px 16px', background: 'rgba(8,6,14,0.7)', color: '#e8c8ff', borderRadius: 14, fontSize: 12, fontWeight: 600, border: '1px solid rgba(200,120,255,0.2)', letterSpacing: 1 }}>Performance</span>
    <span style={{ padding: '5px 16px', background: 'rgba(8,6,14,0.7)', color: '#ff88cc', borderRadius: 14, fontSize: 12, fontWeight: 600, border: '1px solid rgba(255,100,180,0.2)', letterSpacing: 1 }}>x86/ARM</span>
    <span style={{ padding: '5px 16px', background: 'rgba(8,6,14,0.7)', color: '#9ee79e', borderRadius: 14, fontSize: 12, fontWeight: 600, border: '1px solid rgba(120,220,120,0.2)', letterSpacing: 1 }}>open source</span>
  </div>
</div>

# Muhammad Mulnawarman

**Informatics Student | Developer | Designer**

I am an Informatics student at Telkom University with an interest in **software development, web development, artificial intelligence, and digital design**.

I enjoy turning ideas into practical digital products and continuously learning how technology can be used to solve real-world problems. Beyond coding, I also have an interest in **UI/UX, visual design, and education**.

Currently, I am focusing on strengthening my fundamentals in programming and exploring how development, design, and AI can work together to create meaningful products.

---

## About Me

I'm an Informatics student at **Telkom University** who enjoys exploring the intersection of **technology, design, and problem solving**.

I like building things from ideas — whether it's a web application, a small programming project, or a visual concept. For me, every project is an opportunity to understand something new and improve the way I approach problems.

```javascript
const arman = {
  field: "Informatics",
  building: ["Web Applications", "Digital Products"],
  exploring: ["AI", "Software Development", "UI/UX"],
  tools: ["C++", "Go", "JavaScript", "HTML", "CSS"],
  mindset: "learn → build → improve"
};
```

---

## Projects

I build projects as a way to learn, experiment, and turn ideas into practical solutions.

* **[Project Name]** — Brief description of what the project does and the problem it solves.
* **[Project Name]** — Brief description of the application or system.
* **[Project Name]** — Brief description of the project and its main purpose.

More projects can be found in my repositories.

---

## Tech Stack

**Languages & Web**

C++ · Go · JavaScript · HTML · CSS

**Design**

Figma · Adobe Photoshop · Adobe Illustrator

**Currently Exploring**

Artificial Intelligence · Web Development · Software Engineering

---

## Connect

* **LinkedIn:** [linkedin.com/in/mhmdmulna](https://linkedin.com/in/mhmdmulna)
* **Instagram:** [@mhmdmulna](https://instagram.com/mhmdmulna)
* **Email:** [mhmdmulna14@gmail.com](mailto:mhmdmulna14@gmail.com)

---

> Building, learning, and improving — one project at a time.
