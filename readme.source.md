
```aura width=860 height=200 link="https://github.com/jonvikboi"
<div style={{
  width: '100%', height: '100%', background: 'rgba(15, 0, 5, 1)',
  display: 'flex', alignItems: 'center', fontFamily: 'Inter, sans-serif',
  position: 'relative', overflow: 'hidden', borderRadius: 20,
  border: '1px solid rgba(244, 12, 63, 0.2)'
}}>

  <style>{`
      @keyframes float-crimson {
        0%, 100% { transform: translate(0, 0); opacity: 0.6; }
        50% { transform: translate(100px, 20px); opacity: 0.9; }
      }
      @keyframes float-primary {
        0%, 100% { transform: translate(0, 0); opacity: 0.4; }
        50% { transform: translate(-80px, -30px); opacity: 0.7; }
      }
      @keyframes scanline {
        0% { transform: translateY(-100%); }
        100% { transform: translateY(100%); }
      }
      #glow-red-1 { animation: float-crimson 10s ease-in-out infinite; }
      #glow-red-2 { animation: float-primary 12s ease-in-out infinite reverse; }
    `}</style>

  {/* Animated Background Aura */}
  <svg width="860" height="200" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="grad-crimson" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(110, 4, 25, 0.7)" />
        <stop offset="60%" stopColor="rgba(49, 1, 8, 0.3)" />
        <stop offset="100%" stopColor="rgba(49, 1, 8, 0)" />
      </radialGradient>
      <radialGradient id="grad-primary" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(244, 12, 63, 0.4)" />
        <stop offset="70%" stopColor="rgba(229, 11, 59, 0)" />
      </radialGradient>
    </defs>
    <ellipse id="glow-red-1" cx="200" cy="180" rx="300" ry="200" fill="url(#grad-crimson)" />
    <ellipse id="glow-red-2" cx="600" cy="50" rx="250" ry="150" fill="url(#grad-primary)" />
  </svg>

  <div style={{
    position: 'absolute', left: 48, top: 52, width: 96, height: 96,
    borderRadius: 48, background: 'linear-gradient(135deg, rgba(244, 12, 63, 1), rgba(110, 4, 25, 1))',
    display: 'flex', alignItems: 'center', justifyContent: 'center',
    boxShadow: '0 0 30px rgba(244, 12, 63, 0.3)'
  }}>
    <img src={github?.user?.avatarUrl ?? 'https://github.com/jonvikboi.png'} width={88} height={88} style={{ borderRadius: 44 }} />
  </div>

  <div style={{ display:'flex', flexDirection:'column', marginLeft:176, gap:6, zIndex: 10 }}>
    <div style={{ 
      display:'flex', fontSize:42, fontWeight:900, color:'rgba(255,255,255,1)', 
      letterSpacing:'-1.5px', lineHeight:1 
    }}>
      {github?.user?.name || 'jonvikboi'}
    </div>
    <div style={{ 
      display:'flex', fontSize:16, color:'rgba(244, 12, 63, 0.9)', 
      fontWeight:500, letterSpacing:'0.5px' 
    }}>
      {github?.user?.bio || 'Building cutting-edge digital experiences'}
    </div>
    <div style={{ display:'flex', gap:10, marginTop:12 }}>
      {['Creative Developer', 'Problem Solver', 'Open Source'].map((label, i) => (
        <div key={i} style={{
          padding: '4px 14px', borderRadius: 100,
          background: 'rgba(244, 12, 63, 0.1)', border: '1px solid rgba(244, 12, 63, 0.3)',
          color: 'rgba(255, 255, 255, 0.9)', fontSize: 12, fontWeight: 600
        }}>
          {label}
        </div>
      ))}
    </div>
  </div>
</div>
```

```aura width=860 height=260 link="https://github.com/jonvikboi"
<div style={{
  width: '100%', height: '100%', background: 'rgba(10, 0, 5, 1)',
  display: 'flex', flexDirection: 'column', padding: '32px 48px',
  fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden',
  borderRadius: 20, border: '1px solid rgba(244, 12, 63, 0.15)'
}}>

  <style>{`
    @keyframes pulse-border {
      0%, 100% { border-color: rgba(244, 12, 63, 0.2); }
      50% { border-color: rgba(244, 12, 63, 0.5); }
    }
    .tech-card { animation: pulse-border 4s infinite; }
  `}</style>

  <div style={{ display: 'flex', gap: 40, width: '100%', height: '100%' }}>
    
    {/* Web Dev Stack */}
    <div style={{ flex: 1, display: 'flex', flexDirection: 'column', gap: 16 }}>
      <div style={{ 
        fontSize: 14, fontWeight: 800, color: 'rgba(244, 12, 63, 1)', 
        letterSpacing: '2px', textTransform: 'uppercase' 
      }}>
        Web Dev Stack
      </div>
      <div style={{ display: 'flex', flexWrap: 'wrap', gap: 8 }}>
        {['HTML', 'CSS', 'JAVASCRIPT', 'TYPESCRIPT', 'TAILWIND CSS', 'REACT', 'NEXT.JS'].map(tech => (
          <div key={tech} className="tech-card" style={{
            padding: '8px 16px', borderRadius: 12, background: 'rgba(49, 1, 8, 0.5)',
            border: '1px solid rgba(110, 4, 25, 0.4)', color: 'rgba(255, 255, 255, 0.85)',
            fontSize: 12, fontWeight: 600, letterSpacing: '0.5px'
          }}>
            {tech}
          </div>
        ))}
      </div>
    </div>

    {/* Separator Line */}
    <div style={{ width: 1, background: 'linear-gradient(to bottom, transparent, rgba(244, 12, 63, 0.3), transparent)' }} />

    {/* Coding Stack */}
    <div style={{ flex: 1, display: 'flex', flexDirection: 'column', gap: 16 }}>
      <div style={{ 
        fontSize: 14, fontWeight: 800, color: 'rgba(244, 12, 63, 1)', 
        letterSpacing: '2px', textTransform: 'uppercase' 
      }}>
        Coding Stack
      </div>
      <div style={{ display: 'flex', flexWrap: 'wrap', gap: 8 }}>
        {['PYTHON', 'C', 'C++', 'JAVA', 'SHELL'].map(tech => (
          <div key={tech} className="tech-card" style={{
            padding: '8px 16px', borderRadius: 12, background: 'rgba(49, 1, 8, 0.5)',
            border: '1px solid rgba(110, 4, 25, 0.4)', color: 'rgba(255, 255, 255, 0.85)',
            fontSize: 12, fontWeight: 600, letterSpacing: '0.5px'
          }}>
            {tech}
          </div>
        ))}
      </div>
    </div>

  </div>

  {/* Accent Glow */}
  <div style={{
    position: 'absolute', bottom: -50, right: -50, width: 200, height: 200,
    background: 'rgba(110, 4, 25, 0.2)', filter: 'blur(60px)', borderRadius: '100%'
  }} />
</div>
```
