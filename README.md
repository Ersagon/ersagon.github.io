<!DOCTYPE html>
<html lang="en" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Academic & Research Portfolio</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts: Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        darkBg: '#0b0f19',
                        cardBg: '#131c2e',
                        cardHover: '#1a2642',
                        borderSubtle: '#1e293b',
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        /* Smooth transitions for in-page view switching */
        .view-section {
            animation: fadeIn 0.3s ease-in-out forwards;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(8px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="bg-darkBg text-slate-100 min-h-screen font-sans antialiased selection:bg-cyan-500 selection:text-darkBg p-4 sm:p-6 lg:p-10">

    <div class="max-w-4xl mx-auto space-y-6">

        <!-- ================= TOP PROFILE HEADER (Persistent) ================= -->
        <header class="bg-cardBg border border-borderSubtle rounded-2xl p-6 sm:p-8 flex flex-col sm:flex-row items-center gap-6 shadow-2xl relative overflow-hidden">
            <!-- Decorative accent glow -->
            <div class="absolute -top-24 -right-24 w-48 h-48 bg-cyan-500/10 rounded-full blur-3xl pointer-events-none"></div>

            <!-- Profile Picture Placeholder -->
            <div class="relative shrink-0">
                <div class="w-32 h-32 sm:w-36 sm:h-36 rounded-2xl overflow-hidden border-2 border-cyan-500/40 shadow-xl bg-slate-800 flex items-center justify-center">
                    <!-- Placeholder image with fallback -->
                    <img src="https://placehold.co/400x400/0f172a/38bdf8?text=Your+Photo" 
                         alt="Profile Avatar" 
                         class="w-full h-full object-cover"
                         onerror="this.src='https://placehold.co/400x400/0f172a/38bdf8?text=Avatar'">
                </div>
                <span class="absolute bottom-2 right-2 w-4 h-4 bg-emerald-500 border-2 border-cardBg rounded-full" title="Active researcher"></span>
            </div>

            <!-- Biography & Details -->
            <div class="flex-1 text-center sm:text-left space-y-3">
                <div class="flex flex-wrap items-center justify-center sm:justify-start gap-2">
                    <h1 class="text-2xl sm:text-3xl font-bold tracking-tight text-white">Your Name</h1>
                    <span class="bg-cyan-500/10 text-cyan-400 text-xs font-semibold px-3 py-1 rounded-full border border-cyan-500/20">3rd-Year Economics</span>
                </div>
                <p class="text-slate-400 text-sm sm:text-base leading-relaxed">
                    Undergraduate economics researcher exploring heterodox economic theory, post-autistic economic critique, and systemic institutional analysis. Bridging rigorous quantitative inquiry with philosophical critiques of modern tech and corporate culture.
                </p>
                <div class="flex flex-wrap justify-center sm:justify-start gap-4 pt-1 text-xs text-slate-400">
                    <span class="flex items-center gap-1.5"><i class="fa-solid fa-graduation-cap text-cyan-400"></i> Academic Aspirant</span>
                    <span class="flex items-center gap-1.5"><i class="fa-solid fa-code text-emerald-400"></i> Systems & Data</span>
                    <span class="flex items-center gap-1.5"><i class="fa-solid fa-pen-nib text-rose-400"></i> Cultural Critic</span>
                </div>
            </div>
        </header>


        <!-- ================= MAIN DYNAMIC CONTENT CONTAINER ================= -->
        <main id="app-container">

            <!-- HOME VIEW: Pinned Projects & 4 Grid Boxes -->
            <div id="view-home" class="view-section space-y-6">

                <!-- Pinned Projects / Top Hit Section -->
                <div class="bg-gradient-to-r from-cyan-950/40 via-cardBg to-slate-900/50 border border-cyan-500/30 rounded-2xl p-6 sm:p-7 shadow-xl relative overflow-hidden">
                    <div class="absolute top-0 right-0 bg-cyan-500/10 text-cyan-400 text-xs font-bold px-3 py-1 rounded-bl-xl border-l border-b border-cyan-500/20">
                        <i class="fa-solid fa-thumbtack mr-1"></i> Featured Research
                    </div>
                    <span class="text-xs uppercase tracking-wider text-cyan-400 font-semibold">Top Hitter</span>
                    <h2 class="text-xl sm:text-2xl font-bold text-white mt-1 mb-2">A Critical Evaluation of Post-Autistic Economics</h2>
                    <p class="text-slate-300 text-sm sm:text-base mb-4 leading-relaxed">
                        An exhaustive working paper analyzing neoclassical assumptions, mathematical isolation, and the necessity of real-world behavioral and institutional grounding in economic science.
                    </p>
                    <div class="flex flex-wrap items-center gap-3">
                        <button onclick="switchView('research')" class="bg-cyan-500 hover:bg-cyan-400 text-slate-950 font-semibold px-4 py-2 rounded-xl text-sm transition-all shadow-lg shadow-cyan-500/20 flex items-center gap-2">
                            <i class="fa-solid fa-file-lines"></i> Read Research Paper
                        </button>
                        <button onclick="switchView('videos')" class="bg-slate-800 hover:bg-slate-700 text-slate-200 border border-slate-700 font-medium px-4 py-2 rounded-xl text-sm transition-all flex items-center gap-2">
                            <i class="fa-solid fa-play text-rose-400"></i> Watch Video Context
                        </button>
                    </div>
                </div>

                <!-- 4 Interactive Grid Boxes -->
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    
                    <!-- Box 1: Research Papers & Articles -->
                    <div onclick="switchView('research')" class="group bg-cardBg hover:bg-cardHover border border-borderSubtle hover:border-cyan-500/50 p-6 rounded-2xl cursor-pointer transition-all duration-300 shadow-lg relative overflow-hidden">
                        <div class="absolute -right-6 -bottom-6 w-24 h-24 bg-cyan-500/5 rounded-full blur-xl group-hover:bg-cyan-500/10 transition-all"></div>
                        <div class="w-12 h-12 rounded-xl bg-cyan-500/10 text-cyan-400 flex items-center justify-center text-xl mb-4 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-book-open"></i>
                        </div>
                        <h3 class="text-lg font-bold text-white group-hover:text-cyan-400 transition-colors flex items-center justify-between">
                            Research Papers & Articles 
                            <i class="fa-solid fa-arrow-right text-xs opacity-0 group-hover:opacity-100 transition-opacity text-cyan-400"></i>
                        </h3>
                        <p class="text-slate-400 text-sm mt-1">Explore structured economic working papers, article critiques, and academic thought.</p>
                    </div>

                    <!-- Box 2: Projects -->
                    <div onclick="switchView('projects')" class="group bg-cardBg hover:bg-cardHover border border-borderSubtle hover:border-emerald-500/50 p-6 rounded-2xl cursor-pointer transition-all duration-300 shadow-lg relative overflow-hidden">
                        <div class="absolute -right-6 -bottom-6 w-24 h-24 bg-emerald-500/5 rounded-full blur-xl group-hover:bg-emerald-500/10 transition-all"></div>
                        <div class="w-12 h-12 rounded-xl bg-emerald-500/10 text-emerald-400 flex items-center justify-center text-xl mb-4 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-code-branch"></i>
                        </div>
                        <h3 class="text-lg font-bold text-white group-hover:text-emerald-400 transition-colors flex items-center justify-between">
                            Projects & Repositories 
                            <i class="fa-solid fa-arrow-right text-xs opacity-0 group-hover:opacity-100 transition-opacity text-emerald-400"></i>
                        </h3>
                        <p class="text-slate-400 text-sm mt-1">Data simulations, economic toolkits, and code experiments hosted on GitHub.</p>
                    </div>

                    <!-- Box 3: Videos & Essays -->
                    <div onclick="switchView('videos')" class="group bg-cardBg hover:bg-cardHover border border-borderSubtle hover:border-rose-500/50 p-6 rounded-2xl cursor-pointer transition-all duration-300 shadow-lg relative overflow-hidden">
                        <div class="absolute -right-6 -bottom-6 w-24 h-24 bg-rose-500/5 rounded-full blur-xl group-hover:bg-rose-500/10 transition-all"></div>
                        <div class="w-12 h-12 rounded-xl bg-rose-500/10 text-rose-400 flex items-center justify-center text-xl mb-4 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-video"></i>
                        </div>
                        <h3 class="text-lg font-bold text-white group-hover:text-rose-400 transition-colors flex items-center justify-between">
                            Videos & Cultural Essays 
                            <i class="fa-solid fa-arrow-right text-xs opacity-0 group-hover:opacity-100 transition-opacity text-rose-400"></i>
                        </h3>
                        <p class="text-slate-400 text-sm mt-1">Video previews, cultural critiques on LinkedIn NPCs, AI futures, and Brian Griffin syndromic intellect.</p>
                    </div>

                    <!-- Box 4: Message + Connections -->
                    <div onclick="switchView('contact')" class="group bg-cardBg hover:bg-cardHover border border-borderSubtle hover:border-amber-500/50 p-6 rounded-2xl cursor-pointer transition-all duration-300 shadow-lg relative overflow-hidden">
                        <div class="absolute -right-6 -bottom-6 w-24 h-24 bg-amber-500/5 rounded-full blur-xl group-hover:bg-amber-500/10 transition-all"></div>
                        <div class="w-12 h-12 rounded-xl bg-amber-500/10 text-amber-400 flex items-center justify-center text-xl mb-4 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-paper-plane"></i>
                        </div>
                        <h3 class="text-lg font-bold text-white group-hover:text-amber-400 transition-colors flex items-center justify-between">
                            Message + Connections 
                            <i class="fa-solid fa-arrow-right text-xs opacity-0 group-hover:opacity-100 transition-opacity text-amber-400"></i>
                        </h3>
                        <p class="text-slate-400 text-sm mt-1">Send a direct inquiry message or connect via LinkedIn, GitHub, and professional networks.</p>
                    </div>

                </div>
            </div>


            <!-- RESEARCH SUB-PAGE VIEW (In-page switcher) -->
            <div id="view-research" class="view-section hidden space-y-6">
                <div class="flex items-center justify-between border-b border-borderSubtle pb-4">
                    <button onclick="switchView('home')" class="text-slate-400 hover:text-white bg-slate-800/60 hover:bg-slate-800 px-4 py-2 rounded-xl text-sm font-medium transition-all flex items-center gap-2 border border-slate-700">
                        <i class="fa-solid fa-arrow-left"></i> Back to Overview
                    </button>
                    <span class="text-xs uppercase tracking-widest text-cyan-400 font-semibold">Research Archive</span>
                </div>

                <div class="space-y-4">
                    <!-- Research Item 1 -->
                    <div class="bg-cardBg border border-borderSubtle p-6 rounded-2xl space-y-3">
                        <div class="flex flex-wrap items-center justify-between gap-2">
                            <h3 class="text-lg font-bold text-white">A Critical Evaluation of Post-Autistic Economics</h3>
                            <span class="bg-cyan-500/10 text-cyan-400 text-xs px-2.5 py-1 rounded-md border border-cyan-500/20">Working Paper (2026)</span>
                        </div>
                        <p class="text-slate-300 text-sm leading-relaxed">
                            An examination of the 2000 movement started by French economics students. Analyzes why orthodox math-driven models fail to capture ecological limits, behavioral realities, and systemic wealth distribution.
                        </p>
                        <div class="flex items-center gap-3 pt-2">
                            <a href="https://zenodo.org" target="_blank" class="bg-cyan-500/20 hover:bg-cyan-500/30 text-cyan-300 text-xs font-semibold px-3.5 py-2 rounded-xl border border-cyan-500/30 transition-all flex items-center gap-2">
                                <i class="fa-solid fa-file-pdf"></i> Read PDF Preview
                            </a>
                            <span class="text-xs text-slate-50 colspan-2">DOI: 10.5281/zenodo.placeholder</span>
                        </div>
                    </div>

                    <!-- Research Item 2 -->
                    <div class="bg-cardBg border border-borderSubtle p-6 rounded-2xl space-y-3">
                        <div class="flex flex-wrap items-center justify-between gap-2">
                            <h3 class="text-lg font-bold text-white">Neoclassical Assumptions & Algorithmic Labor Markets</h3>
                            <span class="bg-slate-800 text-slate-300 text-xs px-2.5 py-1 rounded-md border border-slate-700">Article Essay</span>
                        </div>
                        <p class="text-slate-300 text-sm leading-relaxed">
                            Discussion piece on how corporate performativity on platforms like LinkedIn mirrors the abstract, frictionless consumer models taught in undergraduate microeconomics textbooks.
                        </p>
                        <div class="pt-2">
                            <a href="#contact" onclick="switchView('contact')" class="text-xs text-cyan-400 hover:underline font-medium">Request full draft via message &rarr;</a>
                        </div>
                    </div>
                </div>
            </div>


            <!-- PROJECTS SUB-PAGE VIEW (In-page switcher) -->
            <div id="view-projects" class="view-section hidden space-y-6">
                <div class="flex items-center justify-between border-b border-borderSubtle pb-4">
                    <button onclick="switchView('home')" class="text-slate-400 hover:text-white bg-slate-800/60 hover:bg-slate-800 px-4 py-2 rounded-xl text-sm font-medium transition-all flex items-center gap-2 border border-slate-700">
                        <i class="fa-solid fa-arrow-left"></i> Back to Overview
                    </button>
                    <span class="text-xs uppercase tracking-widest text-emerald-400 font-semibold">GitHub & Code Projects</span>
                </div>

                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <!-- Project 1 -->
                    <div class="bg-cardBg border border-borderSubtle p-6 rounded-2xl flex flex-col justify-between space-y-4">
                        <div class="space-y-2">
                            <div class="flex items-center justify-between">
                                <h4 class="font-bold text-white text-base">Economic-Data-Scraper</h4>
                                <i class="fa-brands fa-github text-slate-400 text-lg"></i>
                            </div>
                            <p class="text-slate-400 text-sm">Python script to pull macroeconomic indicators and visualize confidence metrics against labor indices.</p>
                        </div>
                        <div class="flex items-center justify-between pt-2 border-t border-slate-800">
                            <span class="text-xs bg-slate-800 text-emerald-400 px-2 py-0.5 rounded font-mono">Python / Pandas</span>
                            <a href="https://github.com" target="_blank" class="text-xs text-cyan-400 hover:underline font-medium">View Repo &rarr;</a>
                        </div>
                    </div>

                    <!-- Project 2 -->
                    <div class="bg-cardBg border border-borderSubtle p-6 rounded-2xl flex flex-col justify-between space-y-4">
                        <div class="space-y-2">
                            <div class="flex items-center justify-between">
                                <h4 class="font-bold text-white text-base">Heterodox-Model-Sandbox</h4>
                                <i class="fa-brands fa-github text-slate-400 text-lg"></i>
                            </div>
                            <p class="text-slate-400 text-sm">Interactive web simulation comparing equilibrium models vs agent-based complexity models.</p>
                        </div>
                        <div class="flex items-center justify-between pt-2 border-t border-slate-800">
                            <span class="text-xs bg-slate-800 text-emerald-400 px-2 py-0.5 rounded font-mono">JavaScript / D3</span>
                            <a href="https://github.com" target="_blank" class="text-xs text-cyan-400 hover:underline font-medium">View Repo &rarr;</a>
                        </div>
                    </div>
                </div>
            </div>


            <!-- VIDEOS SUB-PAGE VIEW (In-page switcher) -->
            <div id="view-videos" class="view-section hidden space-y-6">
                <div class="flex items-center justify-between border-b border-borderSubtle pb-4">
                    <button onclick="switchView('home')" class="text-slate-400 hover:text-white bg-slate-800/60 hover:bg-slate-800 px-4 py-2 rounded-xl text-sm font-medium transition-all flex items-center gap-2 border border-slate-700">
                        <i class="fa-solid fa-arrow-left"></i> Back to Overview
                    </button>
                    <span class="text-xs uppercase tracking-widest text-rose-400 font-semibold">Video Essays & Context</span>
                </div>

                <div class="space-y-6">
                    <!-- Main Featured Video Card -->
                    <div class="bg-cardBg border border-borderSubtle rounded-2xl p-6 space-y-4">
                        <div class="aspect-video w-full bg-slate-900 rounded-xl overflow-hidden relative border border-slate-800 flex items-center justify-center group">
                            <!-- Embedded placeholder or video preview -->
                            <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 via-slate-950/20 to-transparent flex flex-col items-center justify-center p-6 text-center">
                                <div class="w-16 h-16 rounded-full bg-rose-500 text-white flex items-center justify-center text-xl shadow-lg group-hover:scale-110 transition-transform cursor-pointer">
                                    <i class="fa-solid fa-play ml-1"></i>
                                </div>
                                <span class="text-sm font-medium text-slate-200 mt-3">Preview: Post-Autistic Economics & The LinkedIn NPC Phenomenon</span>
                            </div>
                            <img src="https://placehold.co/800x450/0f172a/cbd5e1?text=Video+Essay+Preview" alt="Video thumbnail" class="w-full h-full object-cover opacity-60">
                        </div>
                        <div class="space-y-2">
                            <h3 class="text-lg font-bold text-white">Why LinkedIn is Full of NPCs & What That Means for Young Economists</h3>
                            <p class="text-slate-300 text-sm leading-relaxed">
                                A personal video breakdown exploring performative leadership culture, the Brian Griffin pseud-intellectual trap, and how outcasts will navigate professional identity over the next 20 years of AI integration.
                            </p>
                        </div>
                    </div>
                </div>
            </div>


            <!-- MESSAGE & CONNECTIONS SUB-PAGE VIEW (In-page switcher) -->
            <div id="view-contact" class="view-section hidden space-y-6">
                <div class="flex items-center justify-between border-b border-borderSubtle pb-4">
                    <button onclick="switchView('home')" class="text-slate-400 hover:text-white bg-slate-800/60 hover:bg-slate-800 px-4 py-2 rounded-xl text-sm font-medium transition-all flex items-center gap-2 border border-slate-700">
                        <i class="fa-solid fa-arrow-left"></i> Back to Overview
                    </button>
                    <span class="text-xs uppercase tracking-widest text-amber-400 font-semibold">Contact & Links</span>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <!-- Message Form (2 columns) -->
                    <div class="md:col-span-2 bg-cardBg border border-borderSubtle p-6 rounded-2xl space-y-4">
                        <h3 class="text-lg font-bold text-white">Send a Direct Inquiry</h3>
                        <p class="text-slate-400 text-sm">Have feedback on a research paper, want to discuss Master's opportunities, or talk heterodox economics? Send a message directly to my inbox.</p>
                        
                        <form id="contact-form" onsubmit="handleFormSubmit(event)" class="space-y-4 pt-2">
                            <div>
                                <label class="block text-xs font-medium text-slate-300 mb-1">Your Name</label>
                                <input type="text" required class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-2.5 text-sm text-slate-100 focus:outline-none focus:border-amber-500 transition-colors" placeholder="Jane Doe">
                            </div>
                            <div>
                                <label class="block text-xs font-medium text-slate-300 mb-1">Your Email</label>
                                <input type="email" required class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-2.5 text-sm text-slate-100 focus:outline-none focus:border-amber-500 transition-colors" placeholder="jane@example.com">
                            </div>
                            <div>
                                <label class="block text-xs font-medium text-slate-300 mb-1">Message</label>
                                <textarea rows="4" required class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-2.5 text-sm text-slate-100 focus:outline-none focus:border-amber-500 transition-colors" placeholder="Hello, I read your paper on post-autistic economics..."></textarea>
                            </div>
                            <button type="submit" class="w-full bg-amber-500 hover:bg-amber-400 text-slate-950 font-semibold py-2.5 rounded-xl text-sm transition-all shadow-lg shadow-amber-500/20">
                                Send Message
                            </button>
                        </form>
                        <!-- Success Notification Box (Replaces alert) -->
                        <div id="form-success-msg" class="hidden bg-emerald-500/10 border border-emerald-500/30 text-emerald-400 p-3 rounded-xl text-sm text-center">
                            <i class="fa-solid fa-circle-check mr-1"></i> Message sent successfully! I will get back to you soon.
                        </div>
                    </div>

                    <!-- Connections / Social Links (1 column) -->
                    <div class="bg-cardBg border border-borderSubtle p-6 rounded-2xl space-y-4 flex flex-col justify-between">
                        <div class="space-y-3">
                            <h3 class="text-lg font-bold text-white">Connections</h3>
                            <p class="text-slate-400 text-sm">Find my professional profiles and academic archives across the web.</p>
                            
                            <div class="space-y-2 pt-2">
                                <a href="https://linkedin.com" target="_blank" class="flex items-center gap-3 bg-slate-900 hover:bg-slate-800/80 border border-slate-800 p-3 rounded-xl text-slate-200 text-sm transition-all group">
                                    <i class="fa-brands fa-linkedin text-cyan-400 text-lg w-6"></i>
                                    <span class="group-hover:text-cyan-400 transition-colors">LinkedIn Profile</span>
                                </a>
                                <a href="https://github.com" target="_blank" class="flex items-center gap-3 bg-slate-900 hover:bg-slate-800/80 border border-slate-800 p-3 rounded-xl text-slate-200 text-sm transition-all group">
                                    <i class="fa-brands fa-github text-emerald-400 text-lg w-6"></i>
                                    <span class="group-hover:text-emerald-400 transition-colors">GitHub Repos</span>
                                </a>
                                <a href="https://youtube.com" target="_blank" class="flex items-center gap-3 bg-slate-900 hover:bg-slate-800/80 border border-slate-800 p-3 rounded-xl text-slate-200 text-sm transition-all group">
                                    <i class="fa-brands fa-youtube text-rose-400 text-lg w-6"></i>
                                    <span class="group-hover:text-rose-400 transition-colors">YouTube Channel</span>
                                </a>
                            </div>
                        </div>

                        <div class="pt-4 border-t border-slate-800 text-xs text-slate-500 text-center">
                            Static academic hub & portfolio
                        </div>
                    </div>
                </div>
            </div>

        </main>

        <!-- Footer -->
        <footer class="text-center text-xs text-slate-500 pt-4 pb-8">
            &copy; 2026 • Built for independent economic research and scholarship portfolio.
        </div>

    </div>

    <!-- JavaScript for View Switching & Form Submission -->
    <script>
        function switchView(viewName) {
            // Hide all view sections
            const views = ['home', 'research', 'projects', 'videos', 'contact'];
            views.forEach(v => {
                const el = document.getElementById('view-' + v);
                if (el) {
                    el.classList.add('hidden');
                }
            });

            // Show selected view section
            const target = document.getElementById('view-' + viewName);
            if (target) {
                target.classList.remove('hidden');
                window.scrollTo({ top: 0, behavior: 'smooth' });
            }
        }

        function handleFormSubmit(event) {
            event.preventDefault();
            const form = document.getElementById('contact-form');
            const successMsg = document.getElementById('form-success-msg');
            
            form.reset();
            successMsg.classList.remove('hidden');
            
            setTimeout(() => {
                successMsg.classList.add('hidden');
            }, 5000);
        }
    </script>
</body>
</html>
