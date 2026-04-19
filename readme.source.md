```aura width=860 height=300 link="https://github.com/jonvikboi"
<div style={{
  width: '100%', height: '100%', background: '#020205',
  display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center',
  fontFamily: 'Inter, system-ui, sans-serif', position: 'relative', 
  overflow: 'hidden', borderRadius: 24, border: '1px solid rgba(255,255,255,0.1)'
}}>

  {/* CSS Animations */}
  <style>{`
    @keyframes orbit {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }
    @keyframes pulse {
      0%, 100% { opacity: 0.4; transform: scale(1); }
      50% { opacity: 0.8; transform: scale(1.1); }
    }
    #nebula-bg { animation: orbit 20s linear infinite; transform-origin: center; }
    #core-glow { animation: pulse 8s ease-in-out infinite; }
  `}</style>

  {/* Background Nebula Effect */}
  <svg width="860" height="300" style={{ position: 'absolute', top: 0, left: 0, zIndex: 0 }}>
    <defs>
      <radialGradient id="nebula1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(120, 50, 255, 0.4)" />
        <stop offset="100%" stopColor="rgba(120, 50, 255, 0)" />
      </radialGradient>
      <radialGradient id="nebula2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0, 200, 255, 0.3)" />
        <stop offset="100%" stopColor="rgba(0, 200, 255, 0)" />
      </radialGradient>
    </defs>
    <g id="nebula-bg">
       <circle cx="200" cy="150" r="300" fill="url(#nebula1)" />
       <circle cx="660" cy="150" r="250" fill="url(#nebula2)" />
    </g>
    <circle id="core-glow" cx="430" cy="150" r="100" fill="white" fillOpacity="0.05" />
  </svg>

  {/* Content Layer */}
  <div style={{
    zIndex: 10, display: 'flex', flexDirection: 'column', alignItems: 'center',
    padding: '32px', textAlign: 'center'
  }}>
    <div style={{
      fontSize: 48, fontWeight: 900, color: '#fff', 
      background: 'linear-gradient(to bottom, #fff, #aaa)',
      WebkitBackgroundClip: 'text', WebkitTextFillColor: 'transparent',
      letterSpacing: '-2px', marginBottom: 8
    }}>
      Building Tomorrow
    </div>
    
    <div style={{ fontSize: 18, color: 'rgba(255,255,255,0.6)', maxWidth: 500, lineHeight: 1.6 }}>
      Full-stack Engineer exploring the intersection of <span style={{ color: '#8844ff', fontWeight: 600 }}>Web3</span> and <span style={{ color: '#00ccff', fontWeight: 600 }}>AI Agents</span>.
    </div>

    {/* Dynamic Tags */}
    <div style={{ display: 'flex', gap: 12, marginTop: 24 }}>
      {['Next.js', 'TypeScript', 'Rust', 'GenAI'].map((tag) => (
        <div key={tag} style={{
          background: 'rgba(255,255,255,0.05)', border: '1px solid rgba(255,255,255,0.1)',
          padding: '6px 16px', borderRadius: 100, color: '#eee', fontSize: 13, fontWeight: 500
        }}>
          {tag}
        </div>
      ))}
    </div>
  </div>
</div>
