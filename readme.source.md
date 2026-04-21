
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
        33% { transform: translate(140px, 50px) scale(1.3); }
        66% { transform: translate(-70px, 100px) scale(0.85); }
      }
      @keyframes mesh-2 {
        0%, 100% { transform: translate(0, 0) scale(1.15); }
        50% { transform: translate(-120px, -80px) scale(0.75); }
      }
      @keyframes mesh-3 {
        0%, 100% { transform: translate(0, 0) opacity: 0.2; }
        50% { transform: translate(100px, -100px) opacity: 0.5; }
      }
      @keyframes glance {
        0% { transform: translateX(-100%) rotate(45deg); }
        100% { transform: translateX(200%) rotate(45deg); }
      }
      #mesh-blob-1 { animation: mesh-1 12s ease-in-out infinite; }
      #mesh-blob-2 { animation: mesh-2 10s ease-in-out infinite reverse; }
      #mesh-blob-3 { animation: mesh-3 8s ease-in-out infinite; }
      .glance-line { animation: glance 8s linear infinite; }
    `}</style>

  <svg width="860" height="200" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="nebula-1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(244, 12, 63, 0.4)" />
        <stop offset="100%" stopColor="rgba(244, 12, 63, 0)" />
      </radialGradient>
      <radialGradient id="nebula-2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(110, 4, 25, 0.6)" />
        <stop offset="100%" stopColor="rgba(110, 4, 25, 0)" />
      </radialGradient>
      <radialGradient id="nebula-3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(229, 11, 59, 0.25)" />
        <stop offset="100%" stopColor="rgba(229, 11, 59, 0)" />
      </radialGradient>
    </defs>
    <circle id="mesh-blob-1" cx="200" cy="100" r="280" fill="url(#nebula-1)" />
    <circle id="mesh-blob-2" cx="660" cy="150" r="230" fill="url(#nebula-2)" />
    <circle id="mesh-blob-3" cx="430" cy="50" r="210" fill="url(#nebula-3)" />
  </svg>

  <div className="glance-line" style={{
    position: 'absolute', top: 0, left: 0, width: '200%', height: '100%',
    background: 'linear-gradient(to right, transparent, rgba(255, 255, 255, 0.03), transparent)',
    zIndex: 1
  }} />

  <div style={{
    position: 'absolute', left: 48, top: 44, width: 112, height: 112,
    borderRadius: 56, background: 'linear-gradient(135deg, rgba(244, 12, 63, 1), rgba(49, 1, 8, 1))',
    display: 'flex', alignItems: 'center', justifyContent: 'center',
    padding: 4, border: '2px solid rgba(244, 12, 63, 0.5)', zIndex: 10
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
          background: 'rgba(244, 12, 63, 0.1)', border: '1px solid rgba(244, 12, 63, 0.4)',
          color: 'rgba(255, 255, 255, 0.85)', textTransform: 'uppercase'
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
    @keyframes orbit-fast {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }
    @keyframes breathe {
      0%, 100% { 
        border-color: rgba(244, 12, 63, 0.3); 
        background: rgba(49, 1, 8, 0.7);
        transform: scale(1);
      }
      50% { 
        border-color: rgba(244, 12, 63, 1); 
        background: rgba(80, 5, 20, 0.9);
        transform: scale(1.05);
        box-shadow: 0 0 15px rgba(244, 12, 63, 0.6);
      }
    }
    .pill-button { animation: breathe 3s infinite ease-in-out; }
    #tech-nebula { animation: orbit-fast 20s linear infinite; transform-origin: center; }
  `}</style>

  <svg width="860" height="380" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="tech-g1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(244, 12, 63, 0.25)" />
        <stop offset="100%" stopColor="rgba(244, 12, 63, 0)" />
      </radialGradient>
      <radialGradient id="tech-g2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(110, 4, 25, 0.4)" />
        <stop offset="100%" stopColor="rgba(110, 4, 25, 0)" />
      </radialGradient>
    </defs>
    <g id="tech-nebula">
      <circle cx="150" cy="190" r="350" fill="url(#tech-g1)" />
      <circle cx="710" cy="220" r="300" fill="url(#tech-g2)" />
    </g>
  </svg>

  <div style={{ display: 'flex', flexDirection: 'column', gap: 40, zIndex: 10 }}>
    
    <div style={{ display: 'flex', flexDirection: 'column', gap: 18 }}>
      <div style={{ 
        fontSize: 12, fontWeight: 900, color: 'rgba(255, 255, 255, 0.5)', 
        letterSpacing: '4px', textTransform: 'uppercase' 
      }}>
        Web Dev Stack
      </div>
      <div style={{ display: 'flex', flexWrap: 'wrap', gap: 12 }}>
        {['HTML', 'CSS', 'JavaScript', 'TypeScript', 'Tailwind CSS', 'React', 'Next.js'].map(tech => (
          <div key={tech} className="pill-button" style={{
            padding: '6px 20px', borderRadius: 100,
            background: 'rgba(49, 1, 8, 0.7)',
            border: '2px solid rgba(244, 12, 63, 0.4)',
            color: 'rgba(255, 255, 255, 1)',
            fontSize: 13, fontWeight: 700, letterSpacing: '0.5px',
            display: 'flex', alignItems: 'center', justifyContent: 'center'
          }}>
            {tech}
          </div>
        ))}
      </div>
    </div>

    <div style={{ display: 'flex', flexDirection: 'column', gap: 18 }}>
      <div style={{ 
        fontSize: 12, fontWeight: 900, color: 'rgba(255, 255, 255, 0.5)', 
        letterSpacing: '4px', textTransform: 'uppercase' 
      }}>
        Programming Languages
      </div>
      <div style={{ display: 'flex', flexWrap: 'wrap', gap: 12 }}>
        {['Python', 'C', 'C++', 'Java', 'Shell'].map(tech => (
          <div key={tech} className="pill-button" style={{
            padding: '6px 20px', borderRadius: 100,
            background: 'rgba(49, 1, 8, 0.7)',
            border: '2px solid rgba(244, 12, 63, 0.4)',
            color: 'rgba(255, 255, 255, 1)',
            fontSize: 13, fontWeight: 700, letterSpacing: '0.5px',
            display: 'flex', alignItems: 'center', justifyContent: 'center'
          }}>
            {tech}
          </div>
        ))}
      </div>
    </div>

  </div>
</div>
```

```aura width=120 height=44 link="https://www.linkedin.com/in/joshuazacharyjose" inline align=center
<SocialMediaButton
  icon="https://raw.githubusercontent.com/jonvikboi/jonvikboi/main/icons/linkedin.svg"
  text="Linkedin"
  backgroundColor="rgba(49, 1, 8, 1)"
  width={120}
  height={44}
  gradientStops={[
    { offset: '0%', color: 'rgba(244, 12, 63, 0.8)' },
    { offset: '30%', color: 'rgba(49, 1, 8, 1)' },
    { offset: '60%', color: 'rgba(229, 11, 59, 0.8)' },
    { offset: '80%', color: 'rgba(49, 1, 8, 1)' },
    { offset: '100%', color: 'rgba(244, 12, 63, 0.5)' },
  ]}
/>
```

```aura width=138 height=44 link="https://x.com/mistah_jzj" inline align=center
<SocialMediaButton
  icon="https://raw.githubusercontent.com/jonvikboi/jonvikboi/main/icons/x.svg"
  text="X.com"
  backgroundColor="rgba(49, 1, 8, 1)"
  width={138}
  height={44}
  gradientStops={[
    { offset: '0%', color: 'rgba(244, 12, 63, 0.8)' },
    { offset: '30%', color: 'rgba(49, 1, 8, 1)' },
    { offset: '60%', color: 'rgba(229, 11, 59, 0.8)' },
    { offset: '80%', color: 'rgba(49, 1, 8, 1)' },
    { offset: '100%', color: 'rgba(244, 12, 63, 0.5)' },
  ]}
/>
```

```aura width=130 height=44 link="https://www.instagram.com/__jooosh__j" inline align=center
<SocialMediaButton
  icon="https://raw.githubusercontent.com/jonvikboi/jonvikboi/main/icons/instagram.svg"
  text="Instagram"
  backgroundColor="rgba(49, 1, 8, 1)"
  width={130}
  height={44}
  gradientStops={[
    { offset: '0%', color: 'rgba(244, 12, 63, 0.8)' },
    { offset: '30%', color: 'rgba(49, 1, 8, 1)' },
    { offset: '60%', color: 'rgba(229, 11, 59, 0.8)' },
    { offset: '80%', color: 'rgba(49, 1, 8, 1)' },
    { offset: '100%', color: 'rgba(244, 12, 63, 0.5)' },
  ]}
/>
```

```aura width=110 height=44 link="mailto:mistahjzj@gmail.com" inline align=center
<SocialMediaButton
  icon="https://raw.githubusercontent.com/jonvikboi/jonvikboi/main/icons/gmail.svg"
  text="Email"
  backgroundColor="rgba(49, 1, 8, 1)"
  width={110}
  height={44}
  gradientStops={[
    { offset: '0%', color: 'rgba(244, 12, 63, 0.8)' },
    { offset: '30%', color: 'rgba(49, 1, 8, 1)' },
    { offset: '60%', color: 'rgba(229, 11, 59, 0.8)' },
    { offset: '80%', color: 'rgba(49, 1, 8, 1)' },
    { offset: '100%', color: 'rgba(244, 12, 63, 0.5)' },
  ]}
/>
```

```aura width=130 height=44 link="https://www.jonvikboi.vercel.app" inline align=center
<SocialMediaButton
  icon="https://raw.githubusercontent.com/jonvikboi/jonvikboi/main/icons/jvb.svg"
  text="Website"
  backgroundColor="rgba(49, 1, 8, 1)"
  width={130}
  height={44}
  gradientStops={[
    { offset: '0%', color: 'rgba(244, 12, 63, 0.8)' },
    { offset: '30%', color: 'rgba(49, 1, 8, 1)' },
    { offset: '60%', color: 'rgba(229, 11, 59, 0.8)' },
    { offset: '80%', color: 'rgba(49, 1, 8, 1)' },
    { offset: '100%', color: 'rgba(244, 12, 63, 0.5)' },
  ]}
/>
```

<p align="center">
<a href="https://www.linkedin.com/in/joshuazacharyjose"><img src="./.github/assets/readme-aura-component-2.svg" width="120" height="44" /></a><a href="https://x.com/mistah_jzj"><img src="./.github/assets/readme-aura-component-3.svg" width="138" height="44" /></a><a href="https://www.instagram.com/__jooosh__j"><img src="./.github/assets/readme-aura-component-4.svg" width="130" height="44" /></a><a href="mailto:mistahjzj@gmail.com"><img src="./.github/assets/readme-aura-component-5.svg" width="110" height="44" /></a><a href="https://www.jonvikboi.vercel.app"><img src="./.github/assets/readme-aura-component-6.svg" width="130" height="44" /></a>
</p>
