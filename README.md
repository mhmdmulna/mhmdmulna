```aura width=800 height=260
<div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center', width: '100%', height: '100%', background: '#06060a', borderRadius: 20, padding: 30, fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden', border: '1px solid rgba(91,33,182,0.25)' }}>
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
        <stop offset="0%" stopColor="rgba(91,33,182,0.7)" />
        <stop offset="60%" stopColor="rgba(91,33,182,0.2)" />
        <stop offset="100%" stopColor="rgba(91,33,182,0)" />
      </radialGradient>
      <radialGradient id="hg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(6,182,212,0.6)" />
        <stop offset="60%" stopColor="rgba(6,182,212,0.15)" />
        <stop offset="100%" stopColor="rgba(6,182,212,0)" />
      </radialGradient>
      <radialGradient id="hg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(56,189,248,0.55)" />
        <stop offset="100%" stopColor="rgba(56,189,248,0)" />
      </radialGradient>
      <radialGradient id="hg4" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(168,85,247,0.5)" />
        <stop offset="100%" stopColor="rgba(168,85,247,0)" />
      </radialGradient>
      <radialGradient id="hg5" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(249,115,22,0.5)" />
        <stop offset="100%" stopColor="rgba(249,115,22,0)" />
      </radialGradient>
      <radialGradient id="hg6" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(79,70,229,0.5)" />
        <stop offset="100%" stopColor="rgba(79,70,229,0)" />
      </radialGradient>
      <radialGradient id="hg7" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(20,184,166,0.4)" />
        <stop offset="100%" stopColor="rgba(20,184,166,0)" />
      </radialGradient>
      <radialGradient id="hg8" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(236,72,153,0.45)" />
        <stop offset="100%" stopColor="rgba(236,72,153,0)" />
      </radialGradient>
      <linearGradient id="hg-scan" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stopColor="rgba(56,189,248,0)" />
        <stop offset="40%" stopColor="rgba(56,189,248,0.15)" />
        <stop offset="50%" stopColor="rgba(56,189,248,0.4)" />
        <stop offset="60%" stopColor="rgba(56,189,248,0.15)" />
        <stop offset="100%" stopColor="rgba(56,189,248,0)" />
      </linearGradient>
      <linearGradient id="hg-hline" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stopColor="rgba(91,33,182,0)" />
        <stop offset="15%" stopColor="rgba(79,70,229,0.25)" />
        <stop offset="50%" stopColor="rgba(56,189,248,0.5)" />
        <stop offset="85%" stopColor="rgba(249,115,22,0.25)" />
        <stop offset="100%" stopColor="rgba(249,115,22,0)" />
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
    <circle id="hdr-ring1" cx="400" cy="110" r="80" fill="none" stroke="rgba(99,102,241,0.2)" strokeWidth="1" />
    <circle id="hdr-ring2" cx="400" cy="110" r="120" fill="none" stroke="rgba(56,189,248,0.12)" strokeWidth="1" />
    <rect id="hdr-scan1" x="0" y="90" width="200" height="1" fill="url(#hg-scan)" />
    <rect id="hdr-scan2" x="0" y="135" width="160" height="1" fill="url(#hg-scan)" />
    <path id="hdr-path1" d="M 50 240 Q 200 200 400 230 Q 600 260 750 220" fill="none" stroke="rgba(91,33,182,0.25)" strokeWidth="1" strokeDasharray="250 250" strokeLinecap="round" />
    <path id="hdr-path2" d="M 50 20 Q 200 50 400 25 Q 600 0 750 40" fill="none" stroke="rgba(56,189,248,0.15)" strokeWidth="1" strokeDasharray="200 200" strokeLinecap="round" />
    <circle id="hdr-dot1" cx="120" cy="45" r="2" fill="rgba(56,189,248,0.8)" />
    <circle id="hdr-dot2" cx="680" cy="55" r="1.5" fill="rgba(168,85,247,0.7)" />
    <circle id="hdr-dot3" cx="300" cy="200" r="2" fill="rgba(249,115,22,0.6)" />
    <circle id="hdr-dot4" cx="550" cy="30" r="1.5" fill="rgba(45,212,191,0.7)" />
    <circle id="hdr-dot5" cx="150" cy="180" r="2" fill="rgba(99,102,241,0.8)" />
    <circle id="hdr-dot6" cx="650" cy="190" r="1.5" fill="rgba(251,146,60,0.6)" />
    <circle id="hdr-dot7" cx="450" cy="240" r="2" fill="rgba(192,132,252,0.7)" />
    <circle id="hdr-dot8" cx="250" cy="25" r="1.5" fill="rgba(56,189,248,0.8)" />
    <rect id="hdr-hline1" x="80" y="148" width="640" height="1" fill="url(#hg-hline)" rx="1" />
    <rect id="hdr-hline2" x="150" y="152" width="500" height="1" fill="url(#hg-hline)" rx="1" />
    <rect id="hdr-hline3" x="250" y="156" width="300" height="1" fill="url(#hg-hline)" rx="1" />
  </svg>
  <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', zIndex: 10, gap: 4 }}>
    <span style={{ fontSize: 64, fontWeight: 900, background: 'linear-gradient(135deg, #ffffff 0%, #a5b4fc 30%, #38bdf8 65%, #fb923c 100%)', backgroundClip: 'text', WebkitBackgroundClip: 'text', color: 'transparent', letterSpacing: 10 }}>ACE</span>
    <span style={{ fontSize: 14, color: '#818cf8', fontWeight: 500, letterSpacing: 4, textTransform: 'uppercase', marginTop: 2 }}>Abhishek Anand</span>
    <span style={{ fontSize: 12, color: '#94a3b8', fontWeight: 300, letterSpacing: 1.5, marginTop: 6 }}>Low-level Systems Programmer | Performance Engineering | Bare-metal</span>
  </div>
  <div style={{ display: 'flex', gap: 8, marginTop: 22, zIndex: 10 }}>
    <span style={{ padding: '5px 16px', background: 'rgba(8,6,14,0.7)', color: '#38bdf8', borderRadius: 14, fontSize: 12, fontWeight: 600, border: '1px solid rgba(56,189,248,0.25)', letterSpacing: 1 }}>OSDEV</span>
    <span style={{ padding: '5px 16px', background: 'rgba(8,6,14,0.7)', color: '#a5b4fc', borderRadius: 14, fontSize: 12, fontWeight: 600, border: '1px solid rgba(165,180,252,0.25)', letterSpacing: 1 }}>Performance</span>
    <span style={{ padding: '5px 16px', background: 'rgba(8,6,14,0.7)', color: '#fb923c', borderRadius: 14, fontSize: 12, fontWeight: 600, border: '1px solid rgba(251,146,60,0.25)', letterSpacing: 1 }}>x86/ARM</span>
    <span style={{ padding: '5px 16px', background: 'rgba(8,6,14,0.7)', color: '#34d399', borderRadius: 14, fontSize: 12, fontWeight: 600, border: '1px solid rgba(52,211,153,0.25)', letterSpacing: 1 }}>open source</span>
  </div>
</div>
```

```aura width=800 height=190
<div style={{ display: 'flex', width: '100%', height: '100%', gap: 14, fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden', background: '#06060a', borderRadius: 18, padding: 20, border: '1px solid rgba(91,33,182,0.2)' }}>
  <style>
    {`
      @keyframes about-drift-r { 0%, 100% { transform: translate(0, 0); opacity: 0.75; } 50% { transform: translate(35px, -18px); opacity: 1.1; } }
      @keyframes about-drift-l { 0%, 100% { transform: translate(0, 0); opacity: 0.65; } 50% { transform: translate(-30px, 16px); opacity: 1; } }
      @keyframes about-pulse { 0%, 100% { transform: scale(1); opacity: 0.7; } 50% { transform: scale(1.2); opacity: 0.45; } }
      @keyframes about-scan { 0% { transform: translate(-900px, 0); opacity: 0; } 10% { opacity: 0.8; } 90% { opacity: 0.8; } 100% { transform: translate(900px, 0); opacity: 0; } }
      @keyframes about-bar { 0%, 100% { opacity: 0.3; transform: scale(1, 0.8); } 50% { opacity: 0.9; transform: scale(1, 1); } }
      #about-g1 { animation: about-drift-r 7.5s ease-in-out infinite; }
      #about-g2 { animation: about-drift-l 6.5s ease-in-out infinite 0.2s; }
      #about-g3 { animation: about-pulse 5.5s ease-in-out infinite 0.4s; }
      #about-g4 { animation: about-drift-r 8.5s ease-in-out infinite 0.3s; }
      #about-scan1 { animation: about-scan 5s linear infinite 1s; }
      #about-bar1 { animation: about-bar 2.5s ease-in-out infinite; }
      #about-bar2 { animation: about-bar 3s ease-in-out infinite 0.5s; }
    `}
  </style>
  <svg width="800" height="190" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="abg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(6,182,212,0.55)" />
        <stop offset="100%" stopColor="rgba(6,182,212,0)" />
      </radialGradient>
      <radialGradient id="abg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(91,33,182,0.5)" />
        <stop offset="100%" stopColor="rgba(91,33,182,0)" />
      </radialGradient>
      <radialGradient id="abg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(249,115,22,0.4)" />
        <stop offset="100%" stopColor="rgba(249,115,22,0)" />
      </radialGradient>
      <radialGradient id="abg4" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(20,184,166,0.35)" />
        <stop offset="100%" stopColor="rgba(20,184,166,0)" />
      </radialGradient>
      <linearGradient id="ab-scan" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stopColor="rgba(56,189,248,0)" />
        <stop offset="45%" stopColor="rgba(56,189,248,0.12)" />
        <stop offset="50%" stopColor="rgba(56,189,248,0.3)" />
        <stop offset="55%" stopColor="rgba(56,189,248,0.12)" />
        <stop offset="100%" stopColor="rgba(56,189,248,0)" />
      </linearGradient>
    </defs>
    <ellipse id="about-g1" cx="80" cy="95" rx="170" ry="110" fill="url(#abg1)" />
    <ellipse id="about-g2" cx="720" cy="85" rx="150" ry="100" fill="url(#abg2)" />
    <ellipse id="about-g3" cx="400" cy="160" rx="130" ry="90" fill="url(#abg3)" />
    <ellipse id="about-g4" cx="560" cy="30" rx="110" ry="75" fill="url(#abg4)" />
    <rect id="about-scan1" x="0" y="95" width="180" height="1" fill="url(#ab-scan)" />
    <rect id="about-bar1" x="18" y="30" width="2" height="130" rx="1" fill="rgba(56,189,248,0.3)" />
    <rect id="about-bar2" x="782" y="30" width="2" height="130" rx="1" fill="rgba(165,180,252,0.3)" />
  </svg>
  <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: 'rgba(10,8,18,0.7)', borderRadius: 14, padding: 22, border: '1px solid rgba(79,70,229,0.2)', zIndex: 10, justifyContent: 'center' }}>
    <span style={{ fontSize: 10, color: '#38bdf8', textTransform: 'uppercase', letterSpacing: 3, marginBottom: 10, fontWeight: 600 }}>Profile</span>
    <span style={{ fontSize: 15, fontWeight: 700, color: '#ffffff', marginBottom: 6 }}>Systems Programmer</span>
    <span style={{ fontSize: 12, color: 'rgba(203,213,225,0.8)', lineHeight: 1.5 }}>Specializing in C, C++ and x86/ARM Assembly for hardware-near optimization.</span>
  </div>
  <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: 'rgba(10,8,18,0.7)', borderRadius: 14, padding: 22, border: '1px solid rgba(79,70,229,0.2)', zIndex: 10, justifyContent: 'center' }}>
    <span style={{ fontSize: 10, color: '#a5b4fc', textTransform: 'uppercase', letterSpacing: 3, marginBottom: 10, fontWeight: 600 }}>Experience</span>
    <div style={{ display: 'flex', flexDirection: 'column', gap: 7 }}>
      <div style={{ display: 'flex', alignItems: 'center', gap: 10 }}>
        <span style={{ width: 8, height: 8, borderRadius: 4, background: 'linear-gradient(135deg, #38bdf8, #0284c7)', boxShadow: '0 0 6px rgba(56,189,248,0.5)' }}></span>
        <span style={{ fontSize: 13, color: '#e2e8f0', fontWeight: 500 }}>System engineer at Matiks</span>
      </div>
      <div style={{ display: 'flex', alignItems: 'center', gap: 10 }}>
        <span style={{ width: 8, height: 8, borderRadius: 4, background: 'linear-gradient(135deg, #a5b4fc, #6366f1)', boxShadow: '0 0 6px rgba(165,180,252,0.5)' }}></span>
        <span style={{ fontSize: 13, color: '#e2e8f0', fontWeight: 500 }}>dotlottie performance patch</span>
      </div>
      <div style={{ display: 'flex', alignItems: 'center', gap: 10 }}>
        <span style={{ width: 8, height: 8, borderRadius: 4, background: 'linear-gradient(135deg, #fb923c, #ea580c)', boxShadow: '0 0 6px rgba(251,146,60,0.5)' }}></span>
        <span style={{ fontSize: 13, color: '#e2e8f0', fontWeight: 500 }}>JSI native module creation</span>
      </div>
    </div>
  </div>
</div>
```

```aura width=800 height=70
<div style={{ display: 'flex', gap: 10, padding: '14px 22px', width: '100%', height: '100%', background: '#06060a', borderRadius: 30, alignItems: 'center', justifyContent: 'center', fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden', border: '1px solid rgba(91,33,182,0.2)' }}>
  <style>
    {`
      @keyframes ts-drift-r { 0%, 100% { transform: translate(0, 0); opacity: 0.75; } 50% { transform: translate(30px, -10px); opacity: 1.1; } }
      @keyframes ts-drift-l { 0%, 100% { transform: translate(0, 0); opacity: 0.7; } 50% { transform: translate(-25px, 12px); opacity: 1; } }
      @keyframes ts-pulse { 0%, 100% { transform: scale(1); opacity: 0.75; } 50% { transform: scale(1.2); opacity: 0.5; } }
      @keyframes ts-scan { 0% { transform: translate(-900px, 0); } 100% { transform: translate(900px, 0); } }
      #ts-g1 { animation: ts-drift-r 7.5s ease-in-out infinite; }
      #ts-g2 { animation: ts-drift-l 8.3s ease-in-out infinite 0.2s; }
      #ts-g3 { animation: ts-pulse 5.8s ease-in-out infinite 0.4s; }
      #ts-g4 { animation: ts-drift-r 6.7s ease-in-out infinite 0.1s; }
      #ts-g5 { animation: ts-drift-l 9.2s ease-in-out infinite 0.3s; }
      #ts-scan1 { animation: ts-scan 3.5s linear infinite; }
    `}
  </style>
  <svg width="800" height="70" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="tg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(91,33,182,0.55)" />
        <stop offset="100%" stopColor="rgba(91,33,182,0)" />
      </radialGradient>
      <radialGradient id="tg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(2,132,199,0.5)" />
        <stop offset="100%" stopColor="rgba(2,132,199,0)" />
      </radialGradient>
      <radialGradient id="tg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(249,115,22,0.4)" />
        <stop offset="100%" stopColor="rgba(249,115,22,0)" />
      </radialGradient>
      <radialGradient id="tg4" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(20,184,166,0.4)" />
        <stop offset="100%" stopColor="rgba(20,184,166,0)" />
      </radialGradient>
      <radialGradient id="tg5" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(168,85,247,0.35)" />
        <stop offset="100%" stopColor="rgba(168,85,247,0)" />
      </radialGradient>
      <linearGradient id="ts-scg" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stopColor="rgba(56,189,248,0)" />
        <stop offset="40%" stopColor="rgba(56,189,248,0.15)" />
        <stop offset="50%" stopColor="rgba(165,180,252,0.35)" />
        <stop offset="60%" stopColor="rgba(56,189,248,0.15)" />
        <stop offset="100%" stopColor="rgba(56,189,248,0)" />
      </linearGradient>
    </defs>
    <ellipse id="ts-g1" cx="500" cy="80" rx="150" ry="70" fill="url(#tg1)" />
    <ellipse id="ts-g2" cx="300" cy="75" rx="130" ry="65" fill="url(#tg2)" />
    <ellipse id="ts-g3" cx="650" cy="60" rx="100" ry="55" fill="url(#tg3)" />
    <ellipse id="ts-g4" cx="150" cy="70" rx="110" ry="60" fill="url(#tg4)" />
    <ellipse id="ts-g5" cx="400" cy="85" rx="90" ry="50" fill="url(#tg5)" />
    <rect id="ts-scan1" x="0" y="34" width="140" height="1" fill="url(#ts-scg)" />
  </svg>
  <span style={{ padding: '5px 16px', background: 'rgba(8,6,14,0.7)', color: '#38bdf8', borderRadius: 16, fontSize: 13, fontWeight: 700, border: '1px solid rgba(79,70,229,0.25)', zIndex: 10 }}>C</span>
  <span style={{ padding: '5px 16px', background: 'rgba(8,6,14,0.7)', color: '#38bdf8', borderRadius: 16, fontSize: 13, fontWeight: 700, border: '1px solid rgba(79,70,229,0.25)', zIndex: 10 }}>C++</span>
  <span style={{ padding: '5px 16px', background: 'rgba(8,6,14,0.7)', color: '#a5b4fc', borderRadius: 16, fontSize: 13, fontWeight: 700, border: '1px solid rgba(79,70,229,0.25)', zIndex: 10 }}>x86 ASM</span>
  <span style={{ padding: '5px 16px', background: 'rgba(8,6,14,0.7)', color: '#34d399', borderRadius: 16, fontSize: 13, fontWeight: 700, border: '1px solid rgba(79,70,229,0.25)', zIndex: 10 }}>Python</span>
  <span style={{ padding: '5px 16px', background: 'rgba(8,6,14,0.7)', color: '#fbbf24', borderRadius: 16, fontSize: 13, fontWeight: 700, border: '1px solid rgba(79,70,229,0.25)', zIndex: 10 }}>JavaScript</span>
  <span style={{ padding: '5px 16px', background: 'rgba(8,6,14,0.7)', color: '#fb923c', borderRadius: 16, fontSize: 13, fontWeight: 700, border: '1px solid rgba(79,70,229,0.25)', zIndex: 10 }}>Rust</span>
  <span style={{ padding: '5px 16px', background: 'rgba(8,6,14,0.7)', color: '#c084fc', borderRadius: 16, fontSize: 13, fontWeight: 700, border: '1px solid rgba(79,70,229,0.25)', zIndex: 10 }}>GLSL</span>
  <span style={{ padding: '5px 16px', background: 'rgba(8,6,14,0.7)', color: '#2dd4bf', borderRadius: 16, fontSize: 13, fontWeight: 700, border: '1px solid rgba(79,70,229,0.25)', zIndex: 10 }}>OpenGL</span>
</div>
```

```aura width=800 height=100
<div style={{ display: 'flex', width: '100%', height: '100%', gap: 12, fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden', background: '#06060a', borderRadius: 16, padding: 18, border: '1px solid rgba(91,33,182,0.2)', alignItems: 'center', justifyContent: 'center' }}>
  <style>
    {`
      @keyframes stat-drift-r { 0%, 100% { transform: translate(0, 0); opacity: 0.7; } 50% { transform: translate(25px, -12px); opacity: 1; } }
      @keyframes stat-scan { 0% { transform: translate(-900px, 0); } 100% { transform: translate(900px, 0); } }
      #stat-g1 { animation: stat-drift-r 7s ease-in-out infinite; }
      #stat-scan1 { animation: stat-scan 4s linear infinite; }
    `}
  </style>
  <svg width="800" height="100" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="stg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(91,33,182,0.5)" />
        <stop offset="100%" stopColor="rgba(91,33,182,0)" />
      </radialGradient>
      <linearGradient id="st-scg" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stopColor="rgba(56,189,248,0)" />
        <stop offset="45%" stopColor="rgba(56,189,248,0.12)" />
        <stop offset="50%" stopColor="rgba(165,180,252,0.3)" />
        <stop offset="55%" stopColor="rgba(56,189,248,0.12)" />
        <stop offset="100%" stopColor="rgba(56,189,248,0)" />
      </linearGradient>
    </defs>
    <ellipse id="stat-g1" cx="400" cy="50" rx="250" ry="60" fill="url(#stg1)" />
    <rect id="stat-scan1" x="0" y="50" width="160" height="1" fill="url(#st-scg)" />
  </svg>
  <div style={{ display: 'flex', gap: 30, alignItems: 'center', zIndex: 10 }}>
    <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', gap: 4 }}>
      <span style={{ fontSize: 24, fontWeight: 800, color: '#ffffff' }}>{github?.stats?.totalStars ?? 0}</span>
      <span style={{ fontSize: 10, color: '#fbbf24', textTransform: 'uppercase', letterSpacing: 2, fontWeight: 600 }}>Stars</span>
    </div>
    <span style={{ width: 1, height: 40, background: 'rgba(79,70,229,0.25)' }}></span>
    <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', gap: 4 }}>
      <span style={{ fontSize: 24, fontWeight: 800, color: '#ffffff' }}>{github?.stats?.totalForks ?? 0}</span>
      <span style={{ fontSize: 10, color: '#a5b4fc', textTransform: 'uppercase', letterSpacing: 2, fontWeight: 600 }}>Forks</span>
    </div>
    <span style={{ width: 1, height: 40, background: 'rgba(79,70,229,0.25)' }}></span>
    <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', gap: 4 }}>
      <span style={{ fontSize: 24, fontWeight: 800, color: '#ffffff' }}>{github?.stats?.totalRepos ?? 0}</span>
      <span style={{ fontSize: 10, color: '#2dd4bf', textTransform: 'uppercase', letterSpacing: 2, fontWeight: 600 }}>Repos</span>
    </div>
    <span style={{ width: 1, height: 40, background: 'rgba(79,70,229,0.25)' }}></span>
    <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', gap: 4 }}>
      <span style={{ fontSize: 24, fontWeight: 800, color: '#ffffff' }}>{github?.stats?.totalCommits ?? 0}</span>
      <span style={{ fontSize: 10, color: '#38bdf8', textTransform: 'uppercase', letterSpacing: 2, fontWeight: 600 }}>Commits</span>
    </div>
  </div>
</div>
```

```aura width=800 height=180
<div style={{ display: 'flex', flexDirection: 'column', width: '100%', height: '100%', fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden', background: '#06060a', borderRadius: 16, padding: 24, border: '1px solid rgba(91,33,182,0.2)' }}>
  <style>
    {`
      @keyframes lang-drift-r { 0%, 100% { transform: translate(0, 0); opacity: 0.6; } 50% { transform: translate(30px, -15px); opacity: 1; } }
      @keyframes lang-drift-l { 0%, 100% { transform: translate(0, 0); opacity: 0.55; } 50% { transform: translate(-25px, 12px); opacity: 0.9; } }
      #lang-g1 { animation: lang-drift-r 8s ease-in-out infinite; }
      #lang-g2 { animation: lang-drift-l 7s ease-in-out infinite 0.3s; }
    `}
  </style>
  <svg width="800" height="180" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="lng1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(79,70,229,0.4)" />
        <stop offset="100%" stopColor="rgba(79,70,229,0)" />
      </radialGradient>
      <radialGradient id="lng2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(6,182,212,0.35)" />
        <stop offset="100%" stopColor="rgba(6,182,212,0)" />
      </radialGradient>
    </defs>
    <ellipse id="lang-g1" cx="650" cy="90" rx="180" ry="100" fill="url(#lng1)" />
    <ellipse id="lang-g2" cx="150" cy="100" rx="160" ry="90" fill="url(#lng2)" />
  </svg>
  <span style={{ fontSize: 10, color: '#38bdf8', textTransform: 'uppercase', letterSpacing: 3, marginBottom: 16, fontWeight: 600, zIndex: 10 }}>Most Used Languages</span>
  <div style={{ display: 'flex', width: '100%', height: 6, borderRadius: 3, overflow: 'hidden', marginBottom: 16, zIndex: 10, background: 'rgba(255,255,255,0.05)' }}>
    {(github?.languages ?? []).map((lang, i) => (
      <div key={i} style={{ width: `${lang.percentage}%`, height: '100%', background: lang.color }} />
    ))}
  </div>
  <div style={{ display: 'flex', flexWrap: 'wrap', gap: 14, zIndex: 10 }}>
    {(github?.languages ?? []).map((lang, i) => (
      <div key={i} style={{ display: 'flex', alignItems: 'center', gap: 6, minWidth: 120 }}>
        <span style={{ width: 10, height: 10, borderRadius: 5, background: lang.color, boxShadow: `0 0 6px ${lang.color}40` }}></span>
        <span style={{ fontSize: 13, color: '#e2e8f0', fontWeight: 500 }}>{lang.name}</span>
        <span style={{ fontSize: 11, color: '#64748b', fontWeight: 400 }}>{lang.percentage}%</span>
      </div>
    ))}
  </div>
</div>
```
![Contribution Calendar](./.github/assets/contribution-calendar.svg "Contribution Calendar")

```aura width=800 height=185 link="https://github.com/acedmicabhishek"
<div style={{ display: 'flex', width: '100%', height: '100%', gap: 12, fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden', background: '#06060a', borderRadius: 16, padding: 18, border: '1px solid rgba(91,33,182,0.2)' }}>
  <style>
    {`
      @keyframes proj-drift-r { 0%, 100% { transform: translate(0, 0); opacity: 0.7; } 50% { transform: translate(30px, -15px); opacity: 1.05; } }
      @keyframes proj-drift-l { 0%, 100% { transform: translate(0, 0); opacity: 0.6; } 50% { transform: translate(-26px, 14px); opacity: 1; } }
      @keyframes proj-pulse { 0%, 100% { transform: scale(1); opacity: 0.65; } 50% { transform: scale(1.18); opacity: 0.4; } }
      @keyframes proj-draw { 0% { stroke-dashoffset: 100; } 100% { stroke-dashoffset: 0; } }
      @keyframes proj-draw2 { 0% { stroke-dashoffset: 80; } 100% { stroke-dashoffset: 0; } }
      @keyframes proj-glow-dot { 0%, 100% { opacity: 0.3; } 50% { opacity: 1; } }
      #proj-g1 { animation: proj-drift-r 7s ease-in-out infinite; }
      #proj-g2 { animation: proj-drift-l 8.5s ease-in-out infinite 0.3s; }
      #proj-g3 { animation: proj-pulse 6s ease-in-out infinite 0.5s; }
      #proj-g4 { animation: proj-drift-r 9s ease-in-out infinite 0.2s; }
      #proj-corner1 { animation: proj-draw 2s ease-in-out infinite; }
      #proj-corner2 { animation: proj-draw2 2.5s ease-in-out infinite 0.5s; }
      #proj-corner3 { animation: proj-draw 3s ease-in-out infinite 1s; }
      #proj-d1 { animation: proj-glow-dot 2s ease-in-out infinite; }
      #proj-d2 { animation: proj-glow-dot 2.5s ease-in-out infinite 0.8s; }
      #proj-d3 { animation: proj-glow-dot 3s ease-in-out infinite 1.6s; }
    `}
  </style>
  <svg width="800" height="185" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="pg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(79,70,229,0.5)" />
        <stop offset="100%" stopColor="rgba(79,70,229,0)" />
      </radialGradient>
      <radialGradient id="pg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(6,182,212,0.45)" />
        <stop offset="100%" stopColor="rgba(6,182,212,0)" />
      </radialGradient>
      <radialGradient id="pg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(249,115,22,0.4)" />
        <stop offset="100%" stopColor="rgba(249,115,22,0)" />
      </radialGradient>
      <radialGradient id="pg4" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(2,132,199,0.4)" />
        <stop offset="100%" stopColor="rgba(2,132,199,0)" />
      </radialGradient>
    </defs>
    <ellipse id="proj-g1" cx="180" cy="90" rx="170" ry="100" fill="url(#pg1)" />
    <ellipse id="proj-g2" cx="620" cy="110" rx="150" ry="90" fill="url(#pg2)" />
    <ellipse id="proj-g3" cx="400" cy="155" rx="110" ry="75" fill="url(#pg3)" />
    <ellipse id="proj-g4" cx="80" cy="50" rx="130" ry="80" fill="url(#pg4)" />
    <path id="proj-corner1" d="M 30 25 L 30 15 L 40 15" fill="none" stroke="rgba(56,189,248,0.5)" strokeWidth="1.5" strokeDasharray="50 50" strokeLinecap="round" />
    <path id="proj-corner2" d="M 770 25 L 770 15 L 760 15" fill="none" stroke="rgba(165,180,252,0.5)" strokeWidth="1.5" strokeDasharray="40 40" strokeLinecap="round" />
    <path id="proj-corner3" d="M 30 165 L 30 175 L 40 175" fill="none" stroke="rgba(249,115,22,0.4)" strokeWidth="1.5" strokeDasharray="50 50" strokeLinecap="round" />
    <circle id="proj-d1" cx="34" cy="15" r="2" fill="rgba(56,189,248,0.8)" />
    <circle id="proj-d2" cx="766" cy="15" r="2" fill="rgba(165,180,252,0.8)" />
    <circle id="proj-d3" cx="34" cy="175" r="2" fill="rgba(249,115,22,0.7)" />
  </svg>
  <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: 'rgba(10,8,18,0.7)', borderRadius: 14, padding: 18, border: '1px solid rgba(56,189,248,0.15)', zIndex: 10, justifyContent: 'center' }}>
    <span style={{ fontSize: 17, fontWeight: 800, color: '#ffffff', marginBottom: 4 }}>BrainDance OS</span>
    <span style={{ fontSize: 11, color: '#38bdf8', marginBottom: 6, fontWeight: 600, letterSpacing: 0.5 }}>Custom Operating System</span>
    <span style={{ fontSize: 11, color: 'rgba(203,213,225,0.75)', lineHeight: 1.4, marginBottom: 10 }}>Ring-0 hybrid OS with bootloader, protected mode kernel, VFS, custom shell, BDFS filesystem, and syscall interface</span>
    <div style={{ display: 'flex', gap: 5 }}>
      <span style={{ padding: '2px 10px', background: 'rgba(56,189,248,0.08)', color: '#38bdf8', borderRadius: 8, fontSize: 10, fontWeight: 600, border: '1px solid rgba(56,189,248,0.2)' }}>C</span>
      <span style={{ padding: '2px 10px', background: 'rgba(165,180,252,0.08)', color: '#a5b4fc', borderRadius: 8, fontSize: 10, fontWeight: 600, border: '1px solid rgba(165,180,252,0.2)' }}>x86 ASM</span>
      <span style={{ padding: '2px 10px', background: 'rgba(52,211,153,0.08)', color: '#34d399', borderRadius: 8, fontSize: 10, fontWeight: 600, border: '1px solid rgba(52,211,153,0.2)' }}>NASM</span>
    </div>
  </div>
  <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: 'rgba(10,8,18,0.7)', borderRadius: 14, padding: 18, border: '1px solid rgba(165,180,252,0.15)', zIndex: 10, justifyContent: 'center' }}>
    <span style={{ fontSize: 17, fontWeight: 800, color: '#ffffff', marginBottom: 4 }}>CAT</span>
    <span style={{ fontSize: 11, color: '#a5b4fc', marginBottom: 6, fontWeight: 600, letterSpacing: 0.5 }}>LLVM-Based Compiler</span>
    <span style={{ fontSize: 11, color: 'rgba(203,213,225,0.75)', lineHeight: 1.4, marginBottom: 10 }}>Compiler frontend and IR generator for a statically-typed language, type inference, modular x86/ARM backends</span>
    <div style={{ display: 'flex', gap: 5 }}>
      <span style={{ padding: '2px 10px', background: 'rgba(56,189,248,0.08)', color: '#38bdf8', borderRadius: 8, fontSize: 10, fontWeight: 600, border: '1px solid rgba(56,189,248,0.2)' }}>C++</span>
      <span style={{ padding: '2px 10px', background: 'rgba(165,180,252,0.08)', color: '#a5b4fc', borderRadius: 8, fontSize: 10, fontWeight: 600, border: '1px solid rgba(165,180,252,0.2)' }}>LLVM</span>
    </div>
  </div>
  <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: 'rgba(10,8,18,0.7)', borderRadius: 14, padding: 18, border: '1px solid rgba(251,146,60,0.15)', zIndex: 10, justifyContent: 'center' }}>
    <span style={{ fontSize: 17, fontWeight: 800, color: '#ffffff', marginBottom: 4 }}>Calcium 3D</span>
    <span style={{ fontSize: 11, color: '#fb923c', marginBottom: 6, fontWeight: 600, letterSpacing: 0.5 }}>Game Engine</span>
    <span style={{ fontSize: 11, color: 'rgba(203,213,225,0.75)', lineHeight: 1.4, marginBottom: 10 }}>Powerful and lightweight game engine with Forced optimization</span>
    <div style={{ display: 'flex', gap: 5 }}>
      <span style={{ padding: '2px 10px', background: 'rgba(56,189,248,0.08)', color: '#38bdf8', borderRadius: 8, fontSize: 10, fontWeight: 600, border: '1px solid rgba(56,189,248,0.2)' }}>C++</span>
      <span style={{ padding: '2px 10px', background: 'rgba(45,212,191,0.08)', color: '#2dd4bf', borderRadius: 8, fontSize: 10, fontWeight: 600, border: '1px solid rgba(45,212,191,0.2)' }}>OpenGL</span>
      <span style={{ padding: '2px 10px', background: 'rgba(251,146,60,0.08)', color: '#fb923c', borderRadius: 8, fontSize: 10, fontWeight: 600, border: '1px solid rgba(251,146,60,0.2)' }}>GLSL</span>
    </div>
  </div>
</div>
```
