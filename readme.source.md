
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
      #glow-red-1 { animation: float-crimson 10s ease-in-out infinite; }
      #glow-red-2 { animation: float-primary 12s ease-in-out infinite reverse; }
    `}</style>

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

```aura width=860 height=440 link="https://github.com/jonvikboi"
<div style={{
  width: '100%', height: '100%', background: 'rgba(10, 0, 5, 1)',
  display: 'flex', flexDirection: 'column', padding: '40px 48px',
  fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden',
  borderRadius: 24, border: '1px solid rgba(244, 12, 63, 0.15)'
}}>

  {/* Header Section */}
  <div style={{ display: 'flex', flexDirection: 'column', gap: 32 }}>
    
    {/* Web Dev Stack */}
    <div style={{ display: 'flex', flexDirection: 'column', gap: 16 }}>
      <div style={{ 
        fontSize: 13, fontWeight: 800, color: 'rgba(244, 12, 63, 0.8)', 
        letterSpacing: '3px', textTransform: 'uppercase' 
      }}>
        Web Development
      </div>
      <div style={{ display: 'flex', flexWrap: 'wrap', gap: 12 }}>
        {[
          { name: 'HTML5', slug: 'html5' },
          { name: 'CSS3', slug: 'css3' },
          { name: 'JavaScript', slug: 'javascript' },
          { name: 'TypeScript', slug: 'typescript' },
          { name: 'Tailwind', slug: 'tailwindcss' },
          { name: 'React', slug: 'react' },
          { name: 'Next.js', slug: 'nextdotjs' }
        ].map(tech => (
          <div key={tech.name} style={{
            width: 168, height: 46, borderRadius: 10,
            background: 'rgba(49, 1, 8, 1)', 
            border: '2px solid rgba(110, 4, 25, 1)',
            display: 'flex', alignItems: 'center', padding: '0 14px', gap: 12,
            boxShadow: '0 4px 12px rgba(0,0,0,0.4)',
            backgroundImage: 'linear-gradient(to right, rgba(255,255,255,0.05) 0%, rgba(49,1,8,1) 12%, rgba(110,4,25,0.4) 50%, rgba(244,12,63,0.3) 65%, rgba(49,1,8,1) 85%, rgba(110,4,25,1) 100%)'
          }}>
            <img src={'https://cdn.simpleicons.org/' + tech.slug + '/white'} width={22} height={22} />
            <span style={{ fontSize: 13, fontWeight: 600, color: '#fff', letterSpacing: '0.2px' }}>{tech.name}</span>
          </div>
        ))}
      </div>
    </div>

    {/* Coding Stack */}
    <div style={{ display: 'flex', flexDirection: 'column', gap: 16 }}>
      <div style={{ 
        fontSize: 13, fontWeight: 800, color: 'rgba(244, 12, 63, 0.8)', 
        letterSpacing: '3px', textTransform: 'uppercase' 
      }}>
        Coding languages
      </div>
      <div style={{ display: 'flex', flexWrap: 'wrap', gap: 12 }}>
        {[
          { name: 'Python', slug: 'python' },
          { name: 'C', slug: 'c' },
          { name: 'C++', slug: 'cplusplus' },
          { name: 'Java', slug: 'openjdk' },
          { name: 'Shell', slug: 'gnubash' }
        ].map(tech => (
          <div key={tech.name} style={{
            width: 168, height: 46, borderRadius: 10,
            background: 'rgba(49, 1, 8, 1)', 
            border: '2px solid rgba(110, 4, 25, 1)',
            display: 'flex', alignItems: 'center', padding: '0 14px', gap: 12,
            boxShadow: '0 4px 12px rgba(0,0,0,0.4)',
            backgroundImage: 'linear-gradient(to right, rgba(255,255,255,0.05) 0%, rgba(49,1,8,1) 12%, rgba(110,4,25,0.4) 50%, rgba(244,12,63,0.3) 65%, rgba(49,1,8,1) 85%, rgba(110,4,25,1) 100%)'
          }}>
            <img src={'https://cdn.simpleicons.org/' + tech.slug + '/white'} width={22} height={22} />
            <span style={{ fontSize: 13, fontWeight: 600, color: '#fff', letterSpacing: '0.2px' }}>{tech.name}</span>
          </div>
        ))}
      </div>
    </div>

  </div>

  <div style={{
    position: 'absolute', top: -100, right: -100, width: 300, height: 300,
    background: 'rgba(244, 12, 63, 0.12)', filter: 'blur(80px)', borderRadius: '100%'
  }} />
  <div style={{
    position: 'absolute', bottom: -100, left: -100, width: 300, height: 300,
    background: 'rgba(110, 4, 25, 0.15)', filter: 'blur(80px)', borderRadius: '100%'
  }} />
</div>
```
