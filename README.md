<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>OArt - Creative Community</title>

  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;600;700&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet" />

  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            serif: ['"Playfair Display"', 'serif'],
            sans: ['"Plus Jakarta Sans"', 'sans-serif']
          },
          colors: {
            oart: {
              bg: '#F3ECF8',
              surface: '#EAE1F4',
              card: '#FFFFFF',
              purple: '#2D1548',
              accent: '#6B38AC',
              lightPurple: '#DDD2EC'
            }
          }
        }
      }
    };
  </script>

  <style>
    .no-scrollbar::-webkit-scrollbar { display: none; }
    .no-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }
    body {
      background-color: #F3ECF8;
      font-family: 'Plus Jakarta Sans', sans-serif;
      color: #2D1548;
    }
  </style>
</head>
<body class="min-h-screen flex flex-col">

  <header class="bg-[#F3ECF8]/90 backdrop-blur-md sticky top-0 z-50 border-b border-purple-100/50">
    <div class="max-w-7xl mx-auto px-6 py-3 flex items-center justify-between gap-4">
      <div class="flex items-center gap-8">
        <button onclick="showPage('home')" class="font-serif text-3xl font-bold text-oart-purple tracking-tight hover:opacity-90 transition-opacity">
          OArt
        </button>

        <nav class="hidden md:flex items-center gap-6 font-medium text-sm">
          <button onclick="showPage('home')" class="nav-link flex items-center gap-2 py-1 text-oart-purple border-b-2 border-oart-purple font-semibold" data-page="home">
            <i class="fa-solid fa-house text-xs"></i> Home
          </button>
          <button onclick="showPage('explore')" class="nav-link flex items-center gap-2 py-1 text-slate-600 hover:text-oart-purple border-b-2 border-transparent transition-all" data-page="explore">
            <i class="fa-solid fa-globe text-xs"></i> Explore
          </button>
          <button onclick="showPage('about')" class="nav-link flex items-center gap-2 py-1 text-slate-600 hover:text-oart-purple border-b-2 border-transparent transition-all" data-page="about">
            About Us
          </button>
          <button onclick="showPage('profile')" class="nav-link flex items-center gap-2 py-1 text-slate-600 hover:text-oart-purple border-b-2 border-transparent transition-all" data-page="profile">
            <i class="fa-regular fa-user text-xs"></i> Profile
          </button>
          <button onclick="showPage('faq')" class="nav-link flex items-center gap-2 py-1 text-slate-600 hover:text-oart-purple border-b-2 border-transparent transition-all" data-page="faq">
            FAQ
          </button>
          <button onclick="showPage('guide')" class="nav-link flex items-center gap-2 py-1 text-slate-600 hover:text-oart-purple border-b-2 border-transparent transition-all" data-page="guide">
            User guide
          </button>
        </nav>
      </div>

      <div class="relative w-full max-w-xs">
        <i class="fa-solid fa-magnifying-glass absolute left-3.5 top-1/2 -translate-y-1/2 text-slate-400 text-xs"></i>
        <input
          type="text"
          placeholder="Search artwork..."
          class="w-full bg-white/80 focus:bg-white transition-all rounded-full py-2 pl-9 pr-4 text-xs text-slate-800 placeholder-slate-400 outline-none border border-slate-200/80 shadow-sm focus:ring-2 focus:ring-purple-300"
        />
      </div>
    </div>

    <div class="md:hidden flex items-center justify-between px-4 py-2 border-t border-purple-100 overflow-x-auto text-xs font-medium space-x-4 no-scrollbar">
      <button onclick="showPage('home')" class="mobile-nav-btn whitespace-nowrap text-oart-purple font-semibold" data-page="home">Home</button>
      <button onclick="showPage('explore')" class="mobile-nav-btn whitespace-nowrap text-slate-600" data-page="explore">Explore</button>
      <button onclick="showPage('about')" class="mobile-nav-btn whitespace-nowrap text-slate-600" data-page="about">About Us</button>
      <button onclick="showPage('profile')" class="mobile-nav-btn whitespace-nowrap text-slate-600" data-page="profile">Profile</button>
      <button onclick="showPage('faq')" class="mobile-nav-btn whitespace-nowrap text-slate-600" data-page="faq">FAQ</button>
      <button onclick="showPage('guide')" class="mobile-nav-btn whitespace-nowrap text-slate-600" data-page="guide">User guide</button>
    </div>
  </header>

  <main class="flex-1 max-w-7xl w-full mx-auto px-4 sm:px-6 py-6">
    <section id="page-home" class="page-content space-y-8">
      <div class="flex gap-4 overflow-x-auto no-scrollbar rounded-2xl">
        <div class="w-full md:w-[85%] shrink-0 h-52 sm:h-64 md:h-72 rounded-2xl overflow-hidden shadow-sm relative">
          <img src="https://images.unsplash.com/photo-1541701494587-cb58502866ab?auto=format&fit=crop&w=1400&q=80" alt="Abstract Paint" class="w-full h-full object-cover">
        </div>
        <div class="hidden md:block w-[15%] shrink-0 h-72 rounded-2xl overflow-hidden shadow-sm">
          <img src="https://images.unsplash.com/photo-1579783902614-a3fb3927b675?auto=format&fit=crop&w=600&q=80" alt="Creative Art Detail" class="w-full h-full object-cover">
        </div>
      </div>

      <div class="pt-2">
        <h1 class="text-2xl sm:text-3xl md:text-4xl font-bold text-oart-purple tracking-tight">
          OArt Community - Arts, Ideas, Connections
        </h1>
      </div>

      <div class="grid grid-cols-1 sm:grid-cols-2 gap-6 max-w-2xl">
        <div class="flex items-center gap-4 bg-white/40 p-3 rounded-2xl border border-white/60">
          <img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=200&q=80" alt="Artist" class="w-16 h-16 rounded-full object-cover border-2 border-white shadow-sm">
          <div>
            <h3 class="font-bold text-base text-oart-purple">Artist</h3>
            <p class="text-xs text-slate-600">Artist</p>
          </div>
        </div>

        <div class="flex items-center gap-4 bg-white/40 p-3 rounded-2xl border border-white/60">
          <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?auto=format&fit=crop&w=200&q=80" alt="Leona" class="w-16 h-16 rounded-full object-cover border-2 border-white shadow-sm">
          <div>
            <h3 class="font-bold text-base text-oart-purple">Leona</h3>
            <p class="text-xs text-slate-600">Profile</p>
          </div>
        </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-6 pt-2">
        <div class="space-y-3">
          <h2 class="font-bold text-base text-oart-purple">Open Collaboration Project Feed</h2>
          <div class="bg-white rounded-2xl p-3 shadow-sm border border-purple-100 flex flex-col sm:flex-row gap-4">
            <img src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?auto=format&fit=crop&w=500&q=80" alt="Collaboration" class="w-full sm:w-44 h-32 rounded-xl object-cover">
            <div class="flex flex-col justify-between py-1 space-y-2">
              <div>
                <h3 class="font-bold text-sm text-oart-purple">Project: Global Mural</h3>
                <p class="text-xs text-slate-700 mt-1 leading-snug">
                  A massive collaborative mural visible for your digital art and ideas.
                </p>
              </div>
              <p class="text-[11px] text-slate-500 leading-snug">
                Artists worldwide welcome all styles and stages. Add your piece to the wall.
              </p>
            </div>
          </div>
        </div>

        <div class="space-y-3">
          <h2 class="font-bold text-base text-oart-purple">Open Collaboration Project Feed</h2>
          <div class="bg-white rounded-2xl p-3 shadow-sm border border-purple-100 flex flex-col sm:flex-row gap-4">
            <img src="https://images.unsplash.com/photo-1579783900882-c0d3dad7b119?auto=format&fit=crop&w=500&q=80" alt="Abstract Collaboration" class="w-full sm:w-44 h-32 rounded-xl object-cover">
            <div class="flex flex-col justify-between py-1 space-y-2">
              <div>
                <h3 class="font-bold text-sm text-oart-purple">Project: Global Mural</h3>
                <p class="text-xs text-slate-700 mt-1 leading-snug">
                  A massive collaborative mural project for your digital art and ideas.
                </p>
              </div>
              <p class="text-[11px] text-slate-500 leading-snug">
                Artists worldwide unite to co-create art, share ideas, and inspire. Weekly meetings starting this week.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="page-explore" class="page-content hidden space-y-8 py-10">
      <div class="text-center space-y-3 max-w-xl mx-auto">
        <span class="text-xs font-semibold uppercase tracking-wider text-purple-600 bg-purple-100 px-3 py-1 rounded-full">Explore</span>
        <h1 class="text-3xl sm:text-4xl font-bold text-oart-purple">Discover creators and their work</h1>
        <p class="text-slate-600 text-sm">Browse galleries, explore original concepts, and find collaborators across disciplines.</p>
      </div>

      <div class="bg-white/60 border border-white/80 rounded-3xl p-12 text-center max-w-md mx-auto shadow-sm space-y-4">
        <div class="w-16 h-16 bg-purple-100 text-oart-accent rounded-full flex items-center justify-center mx-auto text-2xl">
          <i class="fa-solid fa-compass"></i>
        </div>
        <h2 class="text-2xl font-bold text-oart-purple tracking-widest uppercase">Coming Soon</h2>
        <p class="text-xs text-slate-600">We are currently curating new creator showcases and open collaborative canvases.</p>
      </div>
    </section>

    <section id="page-about" class="page-content hidden space-y-10 py-4">
      <div class="w-full h-44 sm:h-52 rounded-2xl overflow-hidden shadow-sm">
        <img src="https://images.unsplash.com/photo-1541701494587-cb58502866ab?auto=format&fit=crop&w=1400&q=80" alt="About OArt Banner" class="w-full h-full object-cover">
      </div>

      <div class="space-y-2">
        <h1 class="text-3xl font-bold text-oart-purple">About OArt</h1>
        <p class="text-lg text-purple-900 font-medium">Arts, Ideas, Connections</p>
        <p class="text-sm text-slate-700 max-w-3xl leading-relaxed">
          OArt brings creative people together through art and ideas. Open collaboration projects give the community a shared place to create.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div class="bg-white/70 backdrop-blur-sm p-6 rounded-2xl border border-white shadow-sm space-y-2">
          <h3 class="font-bold text-base text-oart-purple">Our community</h3>
          <p class="text-xs text-slate-600 leading-relaxed">A place for artists to meet through their work and share original creative visions.</p>
        </div>
        <div class="bg-white/70 backdrop-blur-sm p-6 rounded-2xl border border-white shadow-sm space-y-2">
          <h3 class="font-bold text-base text-oart-purple">Create together</h3>
          <p class="text-xs text-slate-600 leading-relaxed">Share digital art, vocal work, graphics, soundscapes and whatever else you imagine.</p>
        </div>
        <div class="bg-white/70 backdrop-blur-sm p-6 rounded-2xl border border-white shadow-sm space-y-2">
          <h3 class="font-bold text-base text-oart-purple">Creativity in many forms</h3>
          <p class="text-xs text-slate-600 leading-relaxed">A community built entirely around original human work and open collaboration.</p>
        </div>
      </div>

      <div class="bg-oart-purple text-white p-6 sm:p-8 rounded-2xl flex flex-col sm:flex-row items-center justify-between gap-4">
        <div>
          <h3 class="font-bold text-lg">Join our team</h3>
          <p class="text-xs text-purple-200 mt-1">Interested in helping build OArt? Tell us about your skills and ideas.</p>
        </div>
        <button onclick="showPage('faq')" class="bg-white text-oart-purple text-xs font-semibold px-5 py-2.5 rounded-xl hover:bg-purple-50 transition-colors shrink-0">
          Contact Support
        </button>
      </div>
    </section>

    <section id="page-profile" class="page-content hidden space-y-8 py-4">
      <div class="bg-white/70 backdrop-blur-sm border border-white/80 rounded-3xl p-6 sm:p-8 flex flex-col sm:flex-row items-center gap-6">
        <img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=300&q=80" alt="Profile Picture" class="w-24 h-24 rounded-full object-cover border-4 border-white shadow-md">
        <div class="text-center sm:text-left space-y-1">
          <h1 class="text-2xl font-bold text-oart-purple">Artist Profile</h1>
          <p class="text-xs font-medium text-purple-700 bg-purple-100 px-2.5 py-0.5 rounded-full inline-block">Digital Artist & Illustrative Concept Creator</p>
          <p class="text-xs text-slate-600 pt-2 max-w-lg">
            Welcome to my OArt workspace! Exploring human-created digital paintings, mixed media, and open mural projects.
          </p>
        </div>
      </div>

      <div class="space-y-4">
        <h2 class="text-lg font-bold text-oart-purple">Shared Portfolio</h2>
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
          <div class="bg-white rounded-2xl overflow-hidden shadow-sm border border-purple-100">
            <img src="https://images.unsplash.com/photo-1579783902614-a3fb3927b675?auto=format&fit=crop&w=600&q=80" class="w-full h-48 object-cover">
            <div class="p-3"><h3 class="font-semibold text-xs text-oart-purple">Canvas Abstract I</h3></div>
          </div>
          <div class="bg-white rounded-2xl overflow-hidden shadow-sm border border-purple-100">
            <img src="https://images.unsplash.com/photo-1541701494587-cb58502866ab?auto=format&fit=crop&w=600&q=80" class="w-full h-48 object-cover">
            <div class="p-3"><h3 class="font-semibold text-xs text-oart-purple">Fluid Vibrance</h3></div>
          </div>
          <div class="bg-white rounded-2xl overflow-hidden shadow-sm border border-purple-100">
            <img src="https://images.unsplash.com/photo-1513364776144-60967b0f800f?auto=format&fit=crop&w=600&q=80" class="w-full h-48 object-cover">
            <div class="p-3"><h3 class="font-semibold text-xs text-oart-purple">Color Studies</h3></div>
          </div>
        </div>
      </div>
    </section>

    <section id="page-faq" class="page-content hidden space-y-8 py-4">
      <div class="text-center space-y-2 max-w-xl mx-auto">
        <h1 class="text-3xl font-bold text-oart-purple">Frequently asked questions</h1>
        <p class="text-xs text-slate-600">Connecting with creators and sharing original work</p>
      </div>

      <div class="max-w-3xl mx-auto space-y-4">
        <div class="bg-white rounded-2xl p-5 shadow-sm border border-purple-100 space-y-2">
          <h3 class="font-bold text-sm text-oart-purple">How can I connect with other creators?</h3>
          <p class="text-xs text-slate-600 leading-relaxed">
            Explore artwork to find people with shared interests and connect through creative projects.
          </p>
        </div>

        <div class="bg-white rounded-2xl p-5 shadow-sm border border-purple-100 space-y-2">
          <h3 class="font-bold text-sm text-oart-purple">What should I share with the community?</h3>
          <p class="text-xs text-slate-600 leading-relaxed">
            Share your own creative work, introduce your interests, and invite others to collaborate.
          </p>
        </div>

        <div class="bg-white rounded-2xl p-5 shadow-sm border border-purple-100 space-y-2">
          <h3 class="font-bold text-sm text-oart-purple">How can I build positive connections?</h3>
          <p class="text-xs text-slate-600 leading-relaxed">
            Be respectful, give constructive feedback, and ask permission before sharing someone else's work.
          </p>
        </div>

        <div class="bg-amber-50/80 border border-amber-200 rounded-2xl p-5 space-y-2">
          <div class="flex items-center gap-2 text-amber-800 font-bold text-sm">
            <i class="fa-solid fa-triangle-exclamation"></i>
            <h3>Can I post AI-generated content?</h3>
          </div>
          <p class="text-xs text-amber-900 leading-relaxed font-medium">
            <strong>No.</strong> OArt does not allow content generated wholly or partly by AI, including text, images, audio, and video. Unsure about a tool? Ask support before posting.
          </p>
        </div>
      </div>
    </section>

    <section id="page-guide" class="page-content hidden space-y-8 py-4">
      <div class="space-y-1">
        <h1 class="text-3xl font-bold text-oart-purple">OArt user guide</h1>
        <p class="text-xs text-slate-600 font-medium">Getting started with the creative community</p>
      </div>

      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-4">
        <div class="bg-white p-5 rounded-2xl shadow-sm border border-purple-100 flex flex-col justify-between space-y-4">
          <div class="space-y-2">
            <span class="w-7 h-7 bg-purple-100 text-oart-purple rounded-full flex items-center justify-center font-bold text-xs">1</span>
            <h3 class="font-bold text-xs text-oart-purple">Explore the community</h3>
          </div>
          <p class="text-xs text-slate-600 leading-relaxed">Browse artwork and projects on Home.</p>
        </div>

        <div class="bg-white p-5 rounded-2xl shadow-sm border border-purple-100 flex flex-col justify-between space-y-4">
          <div class="space-y-2">
            <span class="w-7 h-7 bg-purple-100 text-oart-purple rounded-full flex items-center justify-center font-bold text-xs">2</span>
            <h3 class="font-bold text-xs text-oart-purple">Share your original work</h3>
          </div>
          <p class="text-xs text-slate-600 leading-relaxed">Introduce your interests and show your own creations.</p>
        </div>

        <div class="bg-white p-5 rounded-2xl shadow-sm border border-purple-100 flex flex-col justify-between space-y-4">
          <div class="space-y-2">
            <span class="w-7 h-7 bg-purple-100 text-oart-purple rounded-full flex items-center justify-center font-bold text-xs">3</span>
            <h3 class="font-bold text-xs text-oart-purple">Connect and collaborate</h3>
          </div>
          <p class="text-xs text-slate-600 leading-relaxed">Find a project that matches your creative interests.</p>
        </div>

        <div class="bg-white p-5 rounded-2xl shadow-sm border border-purple-100 flex flex-col justify-between space-y-4">
          <div class="space-y-2">
            <span class="w-7 h-7 bg-purple-100 text-oart-purple rounded-full flex items-center justify-center font-bold text-xs">4</span>
            <h3 class="font-bold text-xs text-oart-purple">Keep conversations constructive</h3>
          </div>
          <p class="text-xs text-slate-600 leading-relaxed">Give useful feedback. Ask permission before resharing.</p>
        </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-6 pt-2">
        <div class="bg-white/70 p-6 rounded-2xl border border-white shadow-sm space-y-2">
          <h3 class="font-bold text-sm text-oart-purple">Before you share</h3>
          <p class="text-xs text-slate-600 leading-relaxed">
            Share human-created work only. OArt does not allow content generated wholly or partly by AI.
          </p>
        </div>

        <div class="bg-white/70 p-6 rounded-2xl border border-white shadow-sm space-y-2">
          <h3 class="font-bold text-sm text-oart-purple">Need help?</h3>
          <p class="text-xs text-slate-600 leading-relaxed">
            Read the FAQ or ask support before you post.
          </p>
        </div>
      </div>
    </section>
  </main>

  <footer class="bg-[#EAE1F4] border-t border-purple-200/60 mt-auto py-6">
    <div class="max-w-7xl mx-auto px-6 flex flex-col sm:flex-row items-center justify-between gap-4 text-xs text-slate-600">
      <div class="flex items-center gap-6">
        <button onclick="showPage('home')" class="font-serif text-xl font-bold text-oart-purple">OArt</button>
        <span>Arts, Ideas, Connections</span>
      </div>
      <div>
        Contact support: <a href="mailto:oart.support@mail.com" class="text-oart-purple font-medium hover:underline">oart.support@mail.com</a>
      </div>
    </div>
  </footer>

  <script>
    function showPage(pageId) {
      document.querySelectorAll('.page-content').forEach(page => {
        page.classList.add('hidden');
      });

      const activePage = document.getElementById(`page-${pageId}`);
      if (activePage) activePage.classList.remove('hidden');

      document.querySelectorAll('.nav-link').forEach(btn => {
        btn.classList.remove('text-oart-purple', 'border-oart-purple', 'font-semibold');
        btn.classList.add('text-slate-600', 'border-transparent');
      });

      document.querySelectorAll('.mobile-nav-btn').forEach(btn => {
        btn.classList.remove('text-oart-purple', 'font-semibold');
        btn.classList.add('text-slate-600');
      });

      const activeNavBtns = document.querySelectorAll(`[data-page="${pageId}"]`);
      activeNavBtns.forEach(btn => {
        btn.classList.add('text-oart-purple', 'border-oart-purple', 'font-semibold');
        btn.classList.remove('text-slate-600', 'border-transparent');
      });

      window.scrollTo({ top: 0, behavior: 'smooth' });
    }
  </script>
</body>
</html>
