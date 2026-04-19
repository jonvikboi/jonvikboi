
```aura width=860 height=200 link="https://github.com/jonvikboi"
<div style={{
  width: '100%', height: '100%', background: 'rgba(10, 0, 5, 1)',
  display: 'flex', alignItems: 'center', fontFamily: 'Inter, sans-serif',
  position: 'relative', overflow: 'hidden', borderRadius: 24,
  border: '1px solid rgba(244, 12, 63, 0.25)'
}}>

  <style>{`
      @keyframes mesh-1 {
        0%, 100% { transform: translate(0, 0) scale(1); }
        33% { transform: translate(120px, 40px) scale(1.2); }
        66% { transform: translate(-50px, 80px) scale(0.9); }
      }
      @keyframes mesh-2 {
        0%, 100% { transform: translate(0, 0) scale(1.1); }
        50% { transform: translate(-100px, -60px) scale(0.8); }
      }
      @keyframes mesh-3 {
        0%, 100% { transform: translate(0, 0) opacity: 0.3; }
        50% { transform: translate(80px, -80px) opacity: 0.6; }
      }
      #mesh-blob-1 { animation: mesh-1 15s ease-in-out infinite; }
      #mesh-blob-2 { animation: mesh-2 12s ease-in-out infinite reverse; }
      #mesh-blob-3 { animation: mesh-3 10s ease-in-out infinite; }
    `}</style>

  <svg width="860" height="200" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="nebula-1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(244, 12, 63, 0.35)" />
        <stop offset="100%" stopColor="rgba(244, 12, 63, 0)" />
      </radialGradient>
      <radialGradient id="nebula-2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(110, 4, 25, 0.5)" />
        <stop offset="100%" stopColor="rgba(110, 4, 25, 0)" />
      </radialGradient>
      <radialGradient id="nebula-3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(229, 11, 59, 0.2)" />
        <stop offset="100%" stopColor="rgba(229, 11, 59, 0)" />
      </radialGradient>
    </defs>
    <circle id="mesh-blob-1" cx="200" cy="100" r="250" fill="url(#nebula-1)" />
    <circle id="mesh-blob-2" cx="660" cy="150" r="200" fill="url(#nebula-2)" />
    <circle id="mesh-blob-3" cx="430" cy="50" r="180" fill="url(#nebula-3)" />
  </svg>

  <div style={{
    position: 'absolute', left: 48, top: 44, width: 112, height: 112,
    borderRadius: 56, background: 'linear-gradient(135deg, rgba(244, 12, 63, 1), rgba(49, 1, 8, 1))',
    display: 'flex', alignItems: 'center', justifyContent: 'center',
    padding: 4, border: '2px solid rgba(244, 12, 63, 0.4)'
  }}>
    <img src={github?.user?.avatarUrl ?? 'https://github.com/jonvikboi.png'} width={100} height={100} style={{ borderRadius: 50 }} />
  </div>

  <div style={{ display:'flex', flexDirection:'column', marginLeft:192, gap:4, zIndex: 10 }}>
    <div style={{ 
      display:'flex', fontSize:44, fontWeight:900, color:'rgba(255,255,255,1)', 
      letterSpacing:'-2px', lineHeight:1 
    }}>
      {github?.user?.name || 'jonvikboi'}
    </div>
    <div style={{ 
      display:'flex', fontSize:17, color:'rgba(244, 12, 63, 1)', 
      fontWeight:600, letterSpacing:'0.2px', marginBottom: 6
    }}>
      {github?.user?.bio || 'Architecting Premium Experience'}
    </div>
    <div style={{ display: 'flex', gap: 8 }}>
      {['Next.js Specialist', 'UI/UX Enthusiast', 'Creative Technologist'].map((tag) => (
        <div key={tag} style={{
          padding: '4px 12px', borderRadius: 100, fontSize: 11, fontWeight: 700,
          background: 'rgba(244, 12, 63, 0.08)', border: '1px solid rgba(244, 12, 63, 0.3)',
          color: 'rgba(255, 255, 255, 0.8)', textTransform: 'uppercase'
        }}>{tag}</div>
      ))}
    </div>
  </div>
</div>
```

```aura width=860 height=380 link="https://github.com/jonvikboi"
<div style={{
  width: '100%', height: '100%', background: 'rgba(8, 0, 4, 1)',
  display: 'flex', flexDirection: 'column', padding: '48px',
  fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden',
  borderRadius: 24, border: '1px solid rgba(244, 12, 63, 0.2)'
}}>

  <style>{`
    @keyframes orbit-slow {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }
    @keyframes glow-pulse {
      0%, 100% { border-color: rgba(244, 12, 63, 0.3); box-shadow: 0 0 5px rgba(244, 12, 63, 0.2); }
      50% { border-color: rgba(244, 12, 63, 0.8); box-shadow: 0 0 15px rgba(244, 12, 63, 0.5); }
    }
    .pill-button { animation: glow-pulse 3s infinite ease-in-out; }
    #tech-nebula { animation: orbit-slow 25s linear infinite; transform-origin: center; }
  `}</style>

  <svg width="860" height="380" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="tech-g1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(244, 12, 63, 0.2)" />
        <stop offset="100%" stopColor="rgba(244, 12, 63, 0)" />
      </radialGradient>
      <radialGradient id="tech-g2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(110, 4, 25, 0.3)" />
        <stop offset="100%" stopColor="rgba(110, 4, 25, 0)" />
      </radialGradient>
    </defs>
    <g id="tech-nebula">
      <circle cx="100" cy="190" r="300" fill="url(#tech-g1)" />
      <circle cx="760" cy="190" r="250" fill="url(#tech-g2)" />
    </g>
  </svg>

  <div style={{ display: 'flex', flexDirection: 'column', gap: 40, zIndex: 10 }}>
    
    <div style={{ display: 'flex', flexDirection: 'column', gap: 18 }}>
      <div style={{ 
        fontSize: 12, fontWeight: 900, color: 'rgba(255, 255, 255, 0.4)', 
        letterSpacing: '4px', textTransform: 'uppercase' 
      }}>
        Primary Stack
      </div>
      <div style={{ display: 'flex', flexWrap: 'wrap', gap: 10 }}>
        {['HTML', 'CSS', 'JavaScript', 'TypeScript', 'Tailwind CSS', 'React', 'Next.js'].map(tech => (
          <div key={tech} className="pill-button" style={{
            padding: '6px 20px', borderRadius: 100,
            background: 'rgba(49, 1, 8, 0.7)',
            border: '1px solid rgba(244, 12, 63, 0.4)',
            color: 'rgba(255, 255, 255, 0.9)',
            fontSize: 13, fontWeight: 700, letterSpacing: '0.5px'
          }}>
            {tech}
          </div>
        ))}
      </div>
    </div>

    <div style={{ display: 'flex', flexDirection: 'column', gap: 18 }}>
      <div style={{ 
        fontSize: 12, fontWeight: 900, color: 'rgba(255, 255, 255, 0.4)', 
        letterSpacing: '4px', textTransform: 'uppercase' 
      }}>
        Secondary Stack
      </div>
      <div style={{ display: 'flex', flexWrap: 'wrap', gap: 10 }}>
        {['Python', 'C', 'C++', 'Java', 'Shell'].map(tech => (
          <div key={tech} className="pill-button" style={{
            padding: '6px 20px', borderRadius: 100,
            background: 'rgba(49, 1, 8, 0.7)',
            border: '1px solid rgba(244, 12, 63, 0.4)',
            color: 'rgba(255, 255, 255, 0.9)',
            fontSize: 13, fontWeight: 700, letterSpacing: '0.5px'
          }}>
            {tech}
          </div>
        ))}
      </div>
    </div>

  </div>
</div>
```
