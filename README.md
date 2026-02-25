<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>MEEDEXE — Creative Developer</title>

    <script src="https://cdn.tailwindcss.com"></script>
    <meta name="description" content="MEEDEXE — Creative Developer | Digital Architect | Code with Purpose" />

    <style>
      :root { color-scheme: dark; }
      html, body { height: 100%; scroll-behavior: smooth; }
      body { overflow-x: hidden; font-family: 'Inter', system-ui, -apple-system, sans-serif; }

      .bg-grid {
        background-image: radial-gradient(circle at 1px 1px, rgba(255,255,255,.05) 1px, transparent 0);
        background-size: 32px 32px;
      }
      .glass {
        background: rgba(255,255,255,0.03);
        backdrop-filter: blur(16px);
        -webkit-backdrop-filter: blur(16px);
        border: 1px solid rgba(255,255,255,0.08);
      }
      .shadow-glow {
        box-shadow: 0 0 0 1px rgba(59,130,246,.1), 0 20px 50px rgba(0,0,0,.5);
      }

      .bg-vignette {
        background: 
          radial-gradient(1200px 700px at 15% 10%, rgba(59,130,246,.15), transparent 60%),
          radial-gradient(900px 600px at 85% 30%, rgba(34,211,238,.12), transparent 60%),
          linear-gradient(180deg, #020617 0%, #0f172a 100%);
      }

      .blob {
        position: absolute;
        border-radius: 9999px;
        filter: blur(80px);
        opacity: 0.6;
        animation: floaty 20s ease-in-out infinite;
        will-change: transform;
      }
      .blob.b1 { width: 500px; height: 500px; left: -10%; top: -10%; background: rgba(59,130,246,0.2); }
      .blob.b2 { width: 400px; height: 400px; right: -5%; top: 20%; background: rgba(34,211,238,0.15); animation-delay: -5s; }

      @keyframes floaty {
        0%, 100% { transform: translate(0,0) scale(1); }
        33% { transform: translate(30px, -50px) scale(1.1); }
        66% { transform: translate(-20px, 20px) scale(0.9); }
      }

      /* Fixed ASCII Styling */
      .ascii-container {
        font-family: 'Courier New', Courier, monospace;
        font-weight: 900;
        line-height: 1.1;
        display: inline-block;
        background: linear-gradient(to right, #60a5fa, #22d3ee, #818cf8);
        -webkit-background-clip: text;
        background-clip: text;
        color: transparent;
        filter: drop-shadow(0 0 15px rgba(59,130,246,0.3));
        font-size: clamp(0.5rem, 1.8vw, 1.2rem);
        text-align: left;
      }

      .reveal { opacity: 0; transform: translateY(20px); transition: all 0.8s cubic-bezier(0.22, 1, 0.36, 1); }
      .reveal.is-visible { opacity: 1; transform: translateY(0); }

      .nav-link { position: relative; transition: color 0.3s; }
      .nav-link::after {
        content: '';
        position: absolute;
        width: 0; height: 1px; bottom: -2px; left: 0;
        background: #3b82f6; transition: width 0.3s;
      }
      .nav-link:hover::after { width: 100%; }

      /* Custom Scrollbar */
      ::-webkit-scrollbar { width: 8px; }
      ::-webkit-scrollbar-track { background: #020617; }
      ::-webkit-scrollbar-thumb { background: #1e293b; border-radius: 10px; }
      ::-webkit-scrollbar-thumb:hover { background: #334155; }
    </style>
  </head>

  <body class="bg-slate-950 text-slate-100 selection:bg-blue-500/30">
    <div class="fixed inset-0 -z-10 bg-vignette">
      <div class="absolute inset-0 bg-grid"></div>
      <div class="blob b1"></div>
      <div class="blob b2"></div>
    </div>

    <header class="sticky top-0 z-50 border-b border-white/5 bg-slate-950/80 backdrop-blur-xl">
      <nav class="mx-auto flex max-w-6xl items-center justify-between px-6 py-4">
        <a href="#top" class="group flex items-center gap-3">
          <div class="relative h-10 w-10 overflow-hidden rounded-xl ring-1 ring-white/20 transition-transform group-hover:scale-110">
            <img src="https://i.ibb.co/JwytwC47/92868863.jpg" alt="Logo" class="h-full w-full object-cover" />
          </div>
          <span class="text-lg font-bold tracking-tighter">MEEDEXE</span>
        </a>
        <div class="flex items-center gap-6">
          <a href="#work" class="nav-link text-sm font-medium text-slate-400 hover:text-white">Projects</a>
          <a href="#contact" class="rounded-full bg-blue-600 px-5 py-2 text-sm font-semibold text-white transition-all hover:bg-blue-500 hover:shadow-[0_0_20px_rgba(59,130,246,0.4)]">Hire Me</a>
        </div>
      </nav>
    </header>

    <main id="top" class="mx-auto max-w-6xl px-6">
      <section class="flex min-h-[80vh] flex-col justify-center py-20">
        <div class="grid items-center gap-16 lg:grid-cols-2">
          <div class="reveal">
            <div class="inline-flex items-center gap-2 rounded-full border border-blue-500/20 bg-blue-500/10 px-4 py-1.5 text-xs font-medium text-blue-300">
              <span class="relative flex h-2 w-2">
                <span class="absolute inline-flex h-full w-full animate-ping rounded-full bg-emerald-400 opacity-75"></span>
                <span class="relative inline-flex h-2 w-2 rounded-full bg-emerald-500"></span>
              </span>
              Available for new projects
            </div>

            <div class="mt-8 mb-6">
              <pre class="ascii-container">
███╗   ███╗███████╗███████╗██████╗ ███████╗██╗  ██╗███████╗
████╗ ████║██╔════╝██╔════╝██╔══██╗██╔════╝╚██╗██╔╝██╔════╝
██╔████╔██║█████╗  █████╗  ██║  ██║█████╗   ╚███╔╝ █████╗  
██║╚██╔╝██║██╔══╝  ██╔══╝  ██║  ██║██╔══╝   ██╔██╗ ██╔══╝  
██║ ╚═╝ ██║███████╗███████╗██████╔╝███████╗██╔╝ ██╗███████╗
╚═╝     ╚═╝╚══════╝╚══════╝╚═════╝ ╚══════╝╚═╝  ╚═╝╚══════╝</pre>
            </div>

            <h1 class="text-4xl font-bold tracking-tight text-white sm:text-6xl">
              Digital Architect <br/>
              <span class="text-slate-400">& Creative Developer.</span>
            </h1>
            
            <p class="mt-6 max-w-lg text-lg leading-relaxed text-slate-400">
              Transforming complex problems into elegant digital solutions. Based in 
              <span class="text-blue-400">Chefchaouen, Morocco</span>, working globally.
            </p>

            <div class="mt-10 flex flex-wrap gap-4">
              <button id="copyEmailBtn" class="group flex items-center gap-2 rounded-xl border border-white/10 bg-white/5 px-6 py-3 font-semibold transition-all hover:bg-white/10">
                <span>mkbarrri@gmail.com</span>
                <svg class="h-4 w-4 text-slate-500 transition-colors group-hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"></path></svg>
              </button>
              <a href="https://github.com/MEEDEXE" target="_blank" class="rounded-xl bg-slate-100 px-6 py-3 font-semibold text-slate-900 transition-all hover:bg-white">GitHub Profile</a>
            </div>
          </div>

          <div class="tilt-scene reveal">
            <div class="glass shadow-glow relative rounded-[2.5rem] p-8 transition-transform" data-tilt>
              <div class="flex items-center justify-between">
                <div class="h-12 w-12 rounded-full bg-gradient-to-tr from-blue-500 to-cyan-400 p-0.5">
                  <img src="92868863.jpeg" class="h-full w-full rounded-full object-cover border-2 border-slate-900" alt="Avatar">
                </div>
                <div class="text-right">
                  <div class="text-xs uppercase tracking-widest text-slate-500">Member Since</div>
                  <div class="font-mono text-sm">2021.08.14</div>
                </div>
              </div>

              <div class="mt-12">
                <div class="text-xs uppercase tracking-widest text-slate-500">Principal Stack</div>
                <div class="mt-4 flex flex-wrap gap-2">
                  <span class="rounded-lg bg-blue-500/10 px-3 py-1 text-sm font-medium text-blue-400 ring-1 ring-inset ring-blue-500/20">React / Next.js</span>
                  <span class="rounded-lg bg-cyan-500/10 px-3 py-1 text-sm font-medium text-cyan-400 ring-1 ring-inset ring-cyan-500/20">Tailwind CSS</span>
                  <span class="rounded-lg bg-indigo-500/10 px-3 py-1 text-sm font-medium text-indigo-400 ring-1 ring-inset ring-indigo-500/20">Node.js</span>
                </div>
              </div>

              <div class="mt-8 rounded-2xl bg-black/40 p-4 border border-white/5">
                <div class="flex items-center justify-between text-sm">
                  <span class="text-slate-400">Project Completion</span>
                  <span class="text-emerald-400">100%</span>
                </div>
                <div class="mt-2 h-1.5 w-full rounded-full bg-slate-800">
                  <div class="h-full w-full rounded-full bg-gradient-to-r from-blue-500 to-emerald-400"></div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section id="work" class="py-20">
        <div class="reveal mb-12 flex items-end justify-between">
          <div>
            <h2 class="text-3xl font-bold">Selected Work</h2>
            <p class="mt-2 text-slate-400">Featured projects and client collaborations.</p>
          </div>
        </div>

        <div class="grid gap-6 md:grid-cols-2">
          <a href="https://triana.ma/" target="_blank" class="group reveal glass relative overflow-hidden rounded-3xl p-8 transition-all hover:-translate-y-2 hover:bg-white/[0.05]">
            <div class="relative z-10">
              <span class="text-xs font-bold uppercase tracking-widest text-blue-400">Hospitality</span>
              <h3 class="mt-2 text-2xl font-bold">Triana Restaurant</h3>
              <p class="mt-4 text-slate-400">High-performance multilingual platform with custom reservation flow and SEO optimization.</p>
            </div>
            <div class="mt-8 flex gap-3">
              <span class="text-xs font-medium text-slate-500">UI/UX</span>
              <span class="text-xs font-medium text-slate-500">•</span>
              <span class="text-xs font-medium text-slate-500">Frontend</span>
            </div>
          </a>

          <a href="https://bachirzairi.com/" target="_blank" class="group reveal glass relative overflow-hidden rounded-3xl p-8 transition-all hover:-translate-y-2 hover:bg-white/[0.05]">
            <div class="relative z-10">
              <span class="text-xs font-bold uppercase tracking-widest text-purple-400">Personal Brand</span>
              <h3 class="mt-2 text-2xl font-bold">Bachir Zairi</h3>
              <p class="mt-4 text-slate-400">A minimal, focus-driven identity site designed to highlight professional achievements and conversion.</p>
            </div>
            <div class="mt-8 flex gap-3">
              <span class="text-xs font-medium text-slate-500">Branding</span>
              <span class="text-xs font-medium text-slate-500">•</span>
              <span class="text-xs font-medium text-slate-500">Performance</span>
            </div>
          </a>
        </div>
      </section>

      <footer id="contact" class="py-20 border-t border-white/5">
        <div class="reveal text-center">
          <h2 class="text-4xl font-bold">Let's build something great.</h2>
          <p class="mt-4 text-slate-400">Currently accepting new projects for 2026.</p>
          
          <div class="mt-10 flex justify-center gap-8">
             <a href="https://github.com/MEEDEXE" class="text-slate-400 transition-colors hover:text-white">GitHub</a>
             <a href="mailto:mkbarrri@gmail.com" class="text-slate-400 transition-colors hover:text-white">Email</a>
          </div>

          <p class="mt-16 text-sm text-slate-600">
            &copy; <span id="year"></span> MEEDEXE. All rights reserved. <br/>
            Designed for the future.
          </p>
        </div>
      </footer>
    </main>

    <script>
      // Scroll Reveal
      const observerOptions = { threshold: 0.1 };
      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add('is-visible');
          }
        });
      }, observerOptions);

      document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

      // Tilt Effect
      document.querySelectorAll('[data-tilt]').forEach(card => {
        card.addEventListener('mousemove', e => {
          const rect = card.getBoundingClientRect();
          const x = e.clientX - rect.left;
          const y = e.clientY - rect.top;
          
          const centerX = rect.width / 2;
          const centerY = rect.height / 2;
          
          const rotateX = (y - centerY) / 10;
          const rotateY = (centerX - x) / 10;
          
          card.style.transform = `perspective(1000px) rotateX(${rotateX}deg) rotateY(${rotateY}deg)`;
        });
        
        card.addEventListener('mouseleave', () => {
          card.style.transform = `perspective(1000px) rotateX(0deg) rotateY(0deg)`;
        });
      });

      // Copy Email
      document.getElementById('copyEmailBtn').addEventListener('click', () => {
        navigator.clipboard.writeText('mkbarrri@gmail.com');
        const btn = document.getElementById('copyEmailBtn');
        const originalText = btn.innerHTML;
        btn.innerHTML = '<span>Copied to clipboard!</span>';
        setTimeout(() => { btn.innerHTML = originalText; }, 2000);
      });

      document.getElementById('year').textContent = new Date().getFullYear();
    </script>
  </body>
</html>
