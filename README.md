<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vaishnavi G | Portfolio Presentation</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts: Inter & JetBrains Mono -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        mono: ['JetBrains Mono', 'monospace'],
                    },
                    colors: {
                        darkBg: '#0b0f19',
                        cardBg: 'rgba(17, 24, 39, 0.7)',
                        accentCyan: '#06b6d4',
                        accentPurple: '#a855f7',
                        accentGreen: '#10b981',
                    },
                    animation: {
                        'pulse-slow': 'pulse 4s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                        'glow': 'glow 2.5s ease-in-out infinite alternate',
                    },
                    keyframes: {
                        glow: {
                            '0%': { boxShadow: '0 0 5px rgba(6, 182, 212, 0.3), 0 0 20px rgba(6, 182, 212, 0.1)' },
                            '100%': { boxShadow: '0 0 15px rgba(168, 85, 247, 0.5), 0 0 30px rgba(168, 85, 247, 0.2)' },
                        }
                    }
                }
            }
        }
    </script>

    <style>
        body {
            background-color: #0b0f19;
            color: #f3f4f6;
            overflow-x: hidden;
        }

        .bg-grid-pattern {
            background-size: 36px 36px;
            background-image: 
                linear-gradient(to right, rgba(255, 255, 255, 0.03) 1px, transparent 1px),
                linear-gradient(to bottom, rgba(255, 255, 255, 0.03) 1px, transparent 1px);
        }

        .glass-panel {
            background: rgba(15, 23, 42, 0.7);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }

        .glass-card {
            background: rgba(30, 41, 59, 0.45);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.06);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .glass-card:hover {
            border-color: rgba(6, 182, 212, 0.4);
            transform: translateY(-3px);
            box-shadow: 0 12px 28px -8px rgba(6, 182, 212, 0.25);
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 7px;
            height: 7px;
        }
        ::-webkit-scrollbar-track {
            background: #0b0f19;
        }
        ::-webkit-scrollbar-thumb {
            background: #1e293b;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #06b6d4;
        }

        /* Active Tab Indicator */
        .tab-btn.active {
            color: #38bdf8;
            background: rgba(56, 189, 248, 0.12);
            border-color: rgba(56, 189, 248, 0.35);
        }
    </style>
</head>
<body class="font-sans min-h-screen flex flex-col justify-between selection:bg-cyan-500 selection:text-white bg-grid-pattern relative">

    <!-- Glowing Background Orbs -->
    <div class="fixed top-1/4 left-10 w-96 h-96 bg-cyan-500/10 rounded-full blur-3xl pointer-events-none animate-pulse-slow"></div>
    <div class="fixed bottom-1/4 right-10 w-96 h-96 bg-purple-500/10 rounded-full blur-3xl pointer-events-none animate-pulse-slow" style="animation-delay: 2s;"></div>

    <!-- Header Section -->
    <header class="w-full max-w-6xl mx-auto px-4 pt-6 pb-2 relative z-10">
        <div class="flex flex-col md:flex-row items-center justify-between gap-6 glass-panel p-6 rounded-2xl shadow-2xl">
            <!-- Profile Info -->
            <div class="flex items-center gap-5">
                <div class="relative">
                    <div class="w-20 h-20 rounded-2xl bg-gradient-to-br from-cyan-400 via-indigo-500 to-purple-500 p-[2px] shadow-lg animate-glow">
                        <div class="w-full h-full bg-slate-900 rounded-[14px] flex items-center justify-center overflow-hidden">
                            <span class="text-3xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-purple-400">VG</span>
                        </div>
                    </div>
                    <span class="absolute -bottom-1 -right-1 flex h-4 w-4">
                      <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>
                      <span class="relative inline-flex rounded-full h-4 w-4 bg-emerald-500 border-2 border-slate-900"></span>
                    </span>
                </div>

                <div>
                    <div class="flex items-center gap-3 flex-wrap">
                        <h1 class="text-3xl font-bold tracking-tight text-white">Vaishnavi G</h1>
                        <span class="inline-flex items-center gap-1.5 px-3 py-1 rounded-full text-xs font-mono bg-cyan-500/10 text-cyan-400 border border-cyan-500/20">
                            @Vaish09-VAISH
                        </span>
                    </div>
                    <p class="text-slate-400 text-sm mt-1 font-mono">Full Stack Aspirant | Open Source Developer</p>
                </div>
            </div>

            <!-- Header Action Links -->
            <div class="flex items-center gap-3">
                <a href="https://github.com/Vaish09-VAISH" target="_blank" rel="noopener" class="glass-card px-4 py-2.5 rounded-xl text-slate-300 hover:text-white flex items-center gap-2 text-sm font-medium transition-all">
                    <i class="fa-brands fa-github text-lg"></i>
                    <span>GitHub Profile</span>
                </a>
                <button onclick="switchTab('projects')" class="px-5 py-2.5 rounded-xl bg-gradient-to-r from-cyan-500 to-blue-600 hover:from-cyan-400 hover:to-blue-500 text-white font-medium text-sm shadow-lg shadow-cyan-500/20 transition-all flex items-center gap-2">
                    <i class="fa-solid fa-folder-open"></i>
                    <span>View 11 Repos</span>
                </button>
            </div>
        </div>
    </header>

    <!-- Navigation Bar -->
    <main class="w-full max-w-6xl mx-auto px-4 py-4 flex-grow relative z-10 flex flex-col">
        
        <nav class="flex items-center justify-start md:justify-center gap-2 overflow-x-auto pb-2 mb-6" id="tabNav">
            <button onclick="switchTab('about')" id="btn-about" class="tab-btn active border border-transparent px-5 py-2 rounded-xl text-slate-400 font-medium text-sm flex items-center gap-2.5 transition-all whitespace-nowrap">
                <i class="fa-solid fa-user-astronaut text-cyan-400"></i> About & Bio
            </button>
            <button onclick="switchTab('projects')" id="btn-projects" class="tab-btn border border-transparent px-5 py-2 rounded-xl text-slate-400 font-medium text-sm flex items-center gap-2.5 transition-all whitespace-nowrap">
                <i class="fa-solid fa-code-fork text-blue-400"></i> Repositories (11)
            </button>
            <button onclick="switchTab('skills')" id="btn-skills" class="tab-btn border border-transparent px-5 py-2 rounded-xl text-slate-400 font-medium text-sm flex items-center gap-2.5 transition-all whitespace-nowrap">
                <i class="fa-solid fa-layer-group text-purple-400"></i> Tech Stack
            </button>
            <button onclick="switchTab('stats')" id="btn-stats" class="tab-btn border border-transparent px-5 py-2 rounded-xl text-slate-400 font-medium text-sm flex items-center gap-2.5 transition-all whitespace-nowrap">
                <i class="fa-solid fa-chart-line text-emerald-400"></i> GitHub Stats
            </button>
        </nav>

        <!-- Carousel Slider Track -->
        <div class="relative w-full overflow-hidden rounded-2xl glass-panel p-6 md:p-8 flex-grow">
            
            <div id="sliderTrack" class="flex transition-transform duration-500 ease-in-out w-full" style="transform: translateX(0%);">
                
                <!-- SLIDE 1: ABOUT & BIO -->
                <div class="w-full flex-shrink-0 min-w-full space-y-6">
                    <div class="border-b border-slate-800 pb-4 flex justify-between items-center">
                        <h2 class="text-2xl font-bold text-white flex items-center gap-3">
                            <span class="w-8 h-8 rounded-lg bg-cyan-500/20 text-cyan-400 flex items-center justify-center text-sm"><i class="fa-solid fa-wave-square"></i></span>
                            👋 About Me
                        </h2>
                        <span class="text-xs font-mono text-cyan-400 bg-cyan-500/10 px-3 py-1 rounded-full border border-cyan-500/20">Slide 1 / 4</span>
                    </div>

                    <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
                        <div class="lg:col-span-2 glass-card p-6 rounded-xl space-y-4">
                            <h3 class="text-lg font-semibold text-cyan-300 flex items-center gap-2">
                                <i class="fa-solid fa-sparkles"></i> Hello & Welcome!
                            </h3>
                            <p class="text-slate-300 leading-relaxed">
                                Hello! I'm <strong class="text-white">Vaishnavi G</strong>, a passionate developer who enjoys learning new technologies, building software projects, and improving problem-solving skills.
                            </p>
                            <p class="text-slate-300 leading-relaxed">
                                I work across full-stack applications with TypeScript, JavaScript, Python, and C, while actively maintaining and forking collaborative open-source web solutions on GitHub under <code class="text-cyan-400 font-mono">Vaish09-VAISH</code>.
                            </p>

                            <div class="pt-4 grid grid-cols-2 sm:grid-cols-3 gap-4">
                                <div class="bg-slate-900/60 p-3.5 rounded-lg border border-slate-800">
                                    <div class="text-xs font-mono text-slate-400">HANDLE</div>
                                    <div class="text-sm font-semibold text-cyan-400 font-mono mt-0.5">Vaish09-VAISH</div>
                                </div>
                                <div class="bg-slate-900/60 p-3.5 rounded-lg border border-slate-800">
                                    <div class="text-xs font-mono text-slate-400">FOCUS</div>
                                    <div class="text-sm font-semibold text-white mt-0.5">Full Stack & Backend</div>
                                </div>
                                <div class="bg-slate-900/60 p-3.5 rounded-lg border border-slate-800">
                                    <div class="text-xs font-mono text-slate-400">CONTRIBUTIONS</div>
                                    <div class="text-sm font-semibold text-emerald-400 font-mono mt-0.5">19 Contributions</div>
                                </div>
                            </div>
                        </div>

                        <!-- Philosophy Card -->
                        <div class="glass-card p-6 rounded-xl flex flex-col justify-between relative overflow-hidden bg-gradient-to-br from-cyan-900/20 to-purple-900/20">
                            <div>
                                <span class="text-xs font-mono text-purple-400 uppercase tracking-widest">Motto & Vision</span>
                                <h3 class="text-xl font-bold text-white mt-2">Personal Philosophy</h3>
                                <div class="my-6 space-y-3 font-mono">
                                    <div class="flex items-center gap-3 text-cyan-400">
                                        <i class="fa-solid fa-graduation-cap"></i>
                                        <span class="text-lg font-bold">Learn</span>
                                    </div>
                                    <div class="flex items-center gap-3 text-indigo-400">
                                        <i class="fa-solid fa-code"></i>
                                        <span class="text-lg font-bold">Build</span>
                                    </div>
                                    <div class="flex items-center gap-3 text-purple-400">
                                        <i class="fa-solid fa-rocket"></i>
                                        <span class="text-lg font-bold">Apply</span>
                                    </div>
                                </div>
                            </div>
                            <div class="pt-4 border-t border-slate-800 text-xs text-slate-400 font-mono">
                                ⭐ <span class="text-slate-300">Learn, build, apply....</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- SLIDE 2: REAL REPOSITORIES & PROJECTS -->
                <div class="w-full flex-shrink-0 min-w-full space-y-6">
                    <div class="border-b border-slate-800 pb-4 flex flex-col sm:flex-row justify-between items-start sm:items-center gap-3">
                        <div>
                            <h2 class="text-2xl font-bold text-white flex items-center gap-3">
                                <span class="w-8 h-8 rounded-lg bg-blue-500/20 text-blue-400 flex items-center justify-center text-sm"><i class="fa-solid fa-folder-tree"></i></span>
                                Public Repositories (11)
                            </h2>
                        </div>
                        <div class="flex items-center gap-3 w-full sm:w-auto">
                            <input type="text" id="repoSearch" onkeyup="filterRepos()" placeholder="Search repos..." class="bg-slate-900/90 border border-slate-800 text-xs text-slate-200 rounded-lg px-3 py-1.5 focus:outline-none focus:border-cyan-500 w-full sm:w-48">
                            <span class="text-xs font-mono text-blue-400 bg-blue-500/10 px-3 py-1 rounded-full border border-blue-500/20 whitespace-nowrap">Slide 2 / 4</span>
                        </div>
                    </div>

                    <!-- Repository Cards Grid -->
                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 max-h-[460px] overflow-y-auto pr-2" id="reposGrid">
                        
                        <!-- 1. ivc-workshop-demo -->
                        <div class="glass-card p-4 rounded-xl flex flex-col justify-between repo-item" data-name="ivc-workshop-demo">
                            <div>
                                <div class="flex items-center justify-between gap-2">
                                    <h4 class="font-bold text-cyan-400 font-mono text-sm truncate">ivc-workshop-demo</h4>
                                    <span class="text-[10px] font-mono px-2 py-0.5 rounded bg-slate-800 text-slate-400 border border-slate-700">Public</span>
                                </div>
                                <p class="text-xs text-slate-400 mt-2 line-clamp-2">Git & GitHub Workshop Hands-on Demonstration repository.</p>
                                <div class="text-[11px] font-mono text-slate-500 mt-2">
                                    <i class="fa-solid fa-code-fork text-slate-400"></i> Forked from <span class="text-slate-400">srinivas2s/...</span>
                                </div>
                            </div>
                            <div class="pt-4 mt-2 border-t border-slate-800/60 flex items-center justify-between text-xs">
                                <span class="flex items-center gap-1.5 text-blue-400 font-mono text-[11px]"><i class="fa-solid fa-circle text-[8px]"></i> Shell/Git</span>
                                <a href="https://github.com/Vaish09-VAISH/ivc-workshop-demo" target="_blank" class="hover:text-cyan-400 text-slate-400 transition-colors flex items-center gap-1">
                                    <span>View</span> <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                                </a>
                            </div>
                        </div>

                        <!-- 2. linkloom -->
                        <div class="glass-card p-4 rounded-xl flex flex-col justify-between repo-item" data-name="linkloom">
                            <div>
                                <div class="flex items-center justify-between gap-2">
                                    <h4 class="font-bold text-cyan-400 font-mono text-sm truncate">linkloom</h4>
                                    <span class="text-[10px] font-mono px-2 py-0.5 rounded bg-slate-800 text-slate-400 border border-slate-700">Public</span>
                                </div>
                                <p class="text-xs text-slate-400 mt-2 line-clamp-2">Modern web project built with strongly-typed structure.</p>
                            </div>
                            <div class="pt-4 mt-2 border-t border-slate-800/60 flex items-center justify-between text-xs">
                                <span class="flex items-center gap-1.5 text-blue-400 font-mono text-[11px]"><i class="fa-solid fa-circle text-[8px] text-blue-500"></i> TypeScript</span>
                                <a href="https://github.com/Vaish09-VAISH/linkloom" target="_blank" class="hover:text-cyan-400 text-slate-400 transition-colors flex items-center gap-1">
                                    <span>View</span> <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                                </a>
                            </div>
                        </div>

                        <!-- 3. LinkLoomproject -->
                        <div class="glass-card p-4 rounded-xl flex flex-col justify-between repo-item" data-name="linkloomproject">
                            <div>
                                <div class="flex items-center justify-between gap-2">
                                    <h4 class="font-bold text-cyan-400 font-mono text-sm truncate">LinkLoomproject</h4>
                                    <span class="text-[10px] font-mono px-2 py-0.5 rounded bg-slate-800 text-slate-400 border border-slate-700">Public</span>
                                </div>
                                <p class="text-xs text-slate-400 mt-2 line-clamp-2">Front-end styling & layout showcase for LinkLoom UI components.</p>
                            </div>
                            <div class="pt-4 mt-2 border-t border-slate-800/60 flex items-center justify-between text-xs">
                                <span class="flex items-center gap-1.5 text-purple-400 font-mono text-[11px]"><i class="fa-solid fa-circle text-[8px] text-purple-500"></i> CSS</span>
                                <a href="https://github.com/Vaish09-VAISH/LinkLoomproject" target="_blank" class="hover:text-cyan-400 text-slate-400 transition-colors flex items-center gap-1">
                                    <span>View</span> <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                                </a>
                            </div>
                        </div>

                        <!-- 4. artician-loom -->
                        <div class="glass-card p-4 rounded-xl flex flex-col justify-between repo-item" data-name="artician-loom">
                            <div>
                                <div class="flex items-center justify-between gap-2">
                                    <h4 class="font-bold text-cyan-400 font-mono text-sm truncate">artician-loom</h4>
                                    <span class="text-[10px] font-mono px-2 py-0.5 rounded bg-slate-800 text-slate-400 border border-slate-700">Public</span>
                                </div>
                                <p class="text-xs text-slate-400 mt-2 line-clamp-2">Artisan & creative platform codebase developed with TypeScript.</p>
                            </div>
                            <div class="pt-4 mt-2 border-t border-slate-800/60 flex items-center justify-between text-xs">
                                <span class="flex items-center gap-1.5 text-blue-400 font-mono text-[11px]"><i class="fa-solid fa-circle text-[8px] text-blue-500"></i> TypeScript</span>
                                <a href="https://github.com/Vaish09-VAISH/artician-loom" target="_blank" class="hover:text-cyan-400 text-slate-400 transition-colors flex items-center gap-1">
                                    <span>View</span> <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                                </a>
                            </div>
                        </div>

                        <!-- 5. Marketplace-frontend -->
                        <div class="glass-card p-4 rounded-xl flex flex-col justify-between repo-item" data-name="marketplace-frontend">
                            <div>
                                <div class="flex items-center justify-between gap-2">
                                    <h4 class="font-bold text-cyan-400 font-mono text-sm truncate">Marketplace-frontend</h4>
                                    <span class="text-[10px] font-mono px-2 py-0.5 rounded bg-slate-800 text-slate-400 border border-slate-700">Public</span>
                                </div>
                                <p class="text-xs text-slate-400 mt-2 line-clamp-2">Full-stack e-commerce marketplace front-end user interface.</p>
                                <div class="text-[11px] font-mono text-slate-500 mt-2">
                                    <i class="fa-solid fa-code-fork text-slate-400"></i> Forked from <span class="text-slate-400">SwarnaNagaraju/...</span>
                                </div>
                            </div>
                            <div class="pt-4 mt-2 border-t border-slate-800/60 flex items-center justify-between text-xs">
                                <span class="flex items-center gap-1.5 text-yellow-400 font-mono text-[11px]"><i class="fa-solid fa-circle text-[8px] text-yellow-400"></i> JavaScript</span>
                                <a href="https://github.com/Vaish09-VAISH/Marketplace-frontend" target="_blank" class="hover:text-cyan-400 text-slate-400 transition-colors flex items-center gap-1">
                                    <span>View</span> <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                                </a>
                            </div>
                        </div>

                        <!-- 6. Marketplace-backend -->
                        <div class="glass-card p-4 rounded-xl flex flex-col justify-between repo-item" data-name="marketplace-backend">
                            <div>
                                <div class="flex items-center justify-between gap-2">
                                    <h4 class="font-bold text-cyan-400 font-mono text-sm truncate">Marketplace-backend</h4>
                                    <span class="text-[10px] font-mono px-2 py-0.5 rounded bg-slate-800 text-slate-400 border border-slate-700">Public</span>
                                </div>
                                <p class="text-xs text-slate-400 mt-2 line-clamp-2">Server APIs and database integrations for marketplace app.</p>
                            </div>
                            <div class="pt-4 mt-2 border-t border-slate-800/60 flex items-center justify-between text-xs">
                                <span class="flex items-center gap-1.5 text-emerald-400 font-mono text-[11px]"><i class="fa-solid fa-circle text-[8px] text-emerald-400"></i> Node / Backend</span>
                                <a href="https://github.com/Vaish09-VAISH/Marketplace-backend" target="_blank" class="hover:text-cyan-400 text-slate-400 transition-colors flex items-center gap-1">
                                    <span>View</span> <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                                </a>
                            </div>
                        </div>

                        <!-- 7. Vaish09-VAISH -->
                        <div class="glass-card p-4 rounded-xl flex flex-col justify-between repo-item" data-name="vaish09-vaish">
                            <div>
                                <div class="flex items-center justify-between gap-2">
                                    <h4 class="font-bold text-cyan-400 font-mono text-sm truncate">Vaish09-VAISH</h4>
                                    <span class="text-[10px] font-mono px-2 py-0.5 rounded bg-cyan-500/10 text-cyan-400 border border-cyan-500/30">Profile README</span>
                                </div>
                                <p class="text-xs text-slate-400 mt-2 line-clamp-2">Special repository used to generate personal GitHub profile README.</p>
                            </div>
                            <div class="pt-4 mt-2 border-t border-slate-800/60 flex items-center justify-between text-xs">
                                <span class="flex items-center gap-1.5 text-slate-400 font-mono text-[11px]"><i class="fa-solid fa-circle text-[8px] text-slate-400"></i> Markdown</span>
                                <a href="https://github.com/Vaish09-VAISH/Vaish09-VAISH" target="_blank" class="hover:text-cyan-400 text-slate-400 transition-colors flex items-center gap-1">
                                    <span>View</span> <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                                </a>
                            </div>
                        </div>

                        <!-- 8. articianhub -->
                        <div class="glass-card p-4 rounded-xl flex flex-col justify-between repo-item" data-name="articianhub">
                            <div>
                                <div class="flex items-center justify-between gap-2">
                                    <h4 class="font-bold text-cyan-400 font-mono text-sm truncate">articianhub</h4>
                                    <span class="text-[10px] font-mono px-2 py-0.5 rounded bg-slate-800 text-slate-400 border border-slate-700">Public</span>
                                </div>
                                <p class="text-xs text-slate-400 mt-2 line-clamp-2">Central hub for artisan projects & community resources.</p>
                            </div>
                            <div class="pt-4 mt-2 border-t border-slate-800/60 flex items-center justify-between text-xs">
                                <span class="flex items-center gap-1.5 text-cyan-400 font-mono text-[11px]"><i class="fa-solid fa-circle text-[8px] text-cyan-400"></i> Full Stack</span>
                                <a href="https://github.com/Vaish09-VAISH/articianhub" target="_blank" class="hover:text-cyan-400 text-slate-400 transition-colors flex items-center gap-1">
                                    <span>View</span> <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                                </a>
                            </div>
                        </div>

                        <!-- 9. my_days -->
                        <div class="glass-card p-4 rounded-xl flex flex-col justify-between repo-item" data-name="my_days">
                            <div>
                                <div class="flex items-center justify-between gap-2">
                                    <h4 class="font-bold text-cyan-400 font-mono text-sm truncate">my_days</h4>
                                    <span class="text-[10px] font-mono px-2 py-0.5 rounded bg-slate-800 text-slate-400 border border-slate-700">Public</span>
                                </div>
                                <p class="text-xs text-slate-400 mt-2 line-clamp-2">Daily activity tracking & personal planning web application.</p>
                            </div>
                            <div class="pt-4 mt-2 border-t border-slate-800/60 flex items-center justify-between text-xs">
                                <span class="flex items-center gap-1.5 text-indigo-400 font-mono text-[11px]"><i class="fa-solid fa-circle text-[8px] text-indigo-400"></i> JavaScript</span>
                                <a href="https://github.com/Vaish09-VAISH/my_days" target="_blank" class="hover:text-cyan-400 text-slate-400 transition-colors flex items-center gap-1">
                                    <span>View</span> <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                                </a>
                            </div>
                        </div>

                        <!-- 10. care -->
                        <div class="glass-card p-4 rounded-xl flex flex-col justify-between repo-item" data-name="care">
                            <div>
                                <div class="flex items-center justify-between gap-2">
                                    <h4 class="font-bold text-cyan-400 font-mono text-sm truncate">care</h4>
                                    <span class="text-[10px] font-mono px-2 py-0.5 rounded bg-slate-800 text-slate-400 border border-slate-700">Public</span>
                                </div>
                                <p class="text-xs text-slate-400 mt-2 line-clamp-2">Healthcare / community assistance application module.</p>
                            </div>
                            <div class="pt-4 mt-2 border-t border-slate-800/60 flex items-center justify-between text-xs">
                                <span class="flex items-center gap-1.5 text-emerald-400 font-mono text-[11px]"><i class="fa-solid fa-circle text-[8px] text-emerald-400"></i> Python</span>
                                <a href="https://github.com/Vaish09-VAISH/care" target="_blank" class="hover:text-cyan-400 text-slate-400 transition-colors flex items-center gap-1">
                                    <span>View</span> <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                                </a>
                            </div>
                        </div>

                        <!-- 11. action & new_day -->
                        <div class="glass-card p-4 rounded-xl flex flex-col justify-between repo-item" data-name="action new_day">
                            <div>
                                <div class="flex items-center justify-between gap-2">
                                    <h4 class="font-bold text-cyan-400 font-mono text-sm truncate">action / new_day</h4>
                                    <span class="text-[10px] font-mono px-2 py-0.5 rounded bg-slate-800 text-slate-400 border border-slate-700">Public Repos</span>
                                </div>
                                <p class="text-xs text-slate-400 mt-2 line-clamp-2">Workflow utility scripts, automations & daily experiment repos.</p>
                            </div>
                            <div class="pt-4 mt-2 border-t border-slate-800/60 flex items-center justify-between text-xs">
                                <span class="flex items-center gap-1.5 text-amber-400 font-mono text-[11px]"><i class="fa-solid fa-circle text-[8px] text-amber-400"></i> C / Scripting</span>
                                <a href="https://github.com/Vaish09-VAISH/action" target="_blank" class="hover:text-cyan-400 text-slate-400 transition-colors flex items-center gap-1">
                                    <span>View</span> <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                                </a>
                            </div>
                        </div>

                    </div>
                </div>

                <!-- SLIDE 3: SKILLS & TECH STACK -->
                <div class="w-full flex-shrink-0 min-w-full space-y-6">
                    <div class="border-b border-slate-800 pb-4 flex justify-between items-center">
                        <h2 class="text-2xl font-bold text-white flex items-center gap-3">
                            <span class="w-8 h-8 rounded-lg bg-purple-500/20 text-purple-400 flex items-center justify-center text-sm"><i class="fa-solid fa-code"></i></span>
                            Skills & Technologies
                        </h2>
                        <span class="text-xs font-mono text-purple-400 bg-purple-500/10 px-3 py-1 rounded-full border border-purple-500/20">Slide 3 / 4</span>
                    </div>

                    <!-- Tech Stack Grids -->
                    <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 gap-4">
                        <!-- Python -->
                        <div class="glass-card p-5 rounded-xl flex flex-col items-center text-center group">
                            <div class="w-14 h-14 rounded-xl bg-slate-800/80 p-2.5 mb-2 flex items-center justify-center group-hover:scale-110 transition-transform">
                                <img src="https://skillicons.dev/icons?i=python" alt="Python" class="w-full h-full object-contain">
                            </div>
                            <h4 class="font-bold text-white text-sm">Python</h4>
                            <span class="text-[11px] text-slate-400 font-mono mt-1">Logic & Algorithms</span>
                        </div>

                        <!-- C Language -->
                        <div class="glass-card p-5 rounded-xl flex flex-col items-center text-center group">
                            <div class="w-14 h-14 rounded-xl bg-slate-800/80 p-2.5 mb-2 flex items-center justify-center group-hover:scale-110 transition-transform">
                                <img src="https://skillicons.dev/icons?i=c" alt="C Language" class="w-full h-full object-contain">
                            </div>
                            <h4 class="font-bold text-white text-sm">C Language</h4>
                            <span class="text-[11px] text-slate-400 font-mono mt-1">Systems Programming</span>
                        </div>

                        <!-- TypeScript -->
                        <div class="glass-card p-5 rounded-xl flex flex-col items-center text-center group">
                            <div class="w-14 h-14 rounded-xl bg-slate-800/80 p-2.5 mb-2 flex items-center justify-center group-hover:scale-110 transition-transform">
                                <img src="https://skillicons.dev/icons?i=ts" alt="TypeScript" class="w-full h-full object-contain">
                            </div>
                            <h4 class="font-bold text-white text-sm">TypeScript</h4>
                            <span class="text-[11px] text-slate-400 font-mono mt-1">Type-Safe Frontend</span>
                        </div>

                        <!-- JavaScript -->
                        <div class="glass-card p-5 rounded-xl flex flex-col items-center text-center group">
                            <div class="w-14 h-14 rounded-xl bg-slate-800/80 p-2.5 mb-2 flex items-center justify-center group-hover:scale-110 transition-transform">
                                <img src="https://skillicons.dev/icons?i=js" alt="JavaScript" class="w-full h-full object-contain">
                            </div>
                            <h4 class="font-bold text-white text-sm">JavaScript</h4>
                            <span class="text-[11px] text-slate-400 font-mono mt-1">Dynamic Web Apps</span>
                        </div>

                        <!-- Git -->
                        <div class="glass-card p-5 rounded-xl flex flex-col items-center text-center group">
                            <div class="w-14 h-14 rounded-xl bg-slate-800/80 p-2.5 mb-2 flex items-center justify-center group-hover:scale-110 transition-transform">
                                <img src="https://skillicons.dev/icons?i=git" alt="Git" class="w-full h-full object-contain">
                            </div>
                            <h4 class="font-bold text-white text-sm">Git</h4>
                            <span class="text-[11px] text-slate-400 font-mono mt-1">Version Control</span>
                        </div>

                        <!-- GitHub -->
                        <div class="glass-card p-5 rounded-xl flex flex-col items-center text-center group">
                            <div class="w-14 h-14 rounded-xl bg-slate-800/80 p-2.5 mb-2 flex items-center justify-center group-hover:scale-110 transition-transform">
                                <img src="https://skillicons.dev/icons?i=github" alt="GitHub" class="w-full h-full object-contain">
                            </div>
                            <h4 class="font-bold text-white text-sm">GitHub</h4>
                            <span class="text-[11px] text-slate-400 font-mono mt-1">Workshops & Repos</span>
                        </div>

                        <!-- Supabase -->
                        <div class="glass-card p-5 rounded-xl flex flex-col items-center text-center group">
                            <div class="w-14 h-14 rounded-xl bg-slate-800/80 p-2.5 mb-2 flex items-center justify-center group-hover:scale-110 transition-transform">
                                <img src="https://skillicons.dev/icons?i=supabase" alt="Supabase" class="w-full h-full object-contain">
                            </div>
                            <h4 class="font-bold text-white text-sm">Supabase</h4>
                            <span class="text-[11px] text-slate-400 font-mono mt-1">Database & Auth</span>
                        </div>

                        <!-- VS Code -->
                        <div class="glass-card p-5 rounded-xl flex flex-col items-center text-center group">
                            <div class="w-14 h-14 rounded-xl bg-slate-800/80 p-2.5 mb-2 flex items-center justify-center group-hover:scale-110 transition-transform">
                                <img src="https://skillicons.dev/icons?i=vscode" alt="VS Code" class="w-full h-full object-contain">
                            </div>
                            <h4 class="font-bold text-white text-sm">VS Code</h4>
                            <span class="text-[11px] text-slate-400 font-mono mt-1">Development IDE</span>
                        </div>
                    </div>
                </div>

                <!-- SLIDE 4: GITHUB STATS & REAL CONTRIBUTION ACTIVITY -->
                <div class="w-full flex-shrink-0 min-w-full space-y-6">
                    <div class="border-b border-slate-800 pb-4 flex justify-between items-center">
                        <h2 class="text-2xl font-bold text-white flex items-center gap-3">
                            <span class="w-8 h-8 rounded-lg bg-emerald-500/20 text-emerald-400 flex items-center justify-center text-sm"><i class="fa-brands fa-github"></i></span>
                            GitHub Activity & Real Stats
                        </h2>
                        <span class="text-xs font-mono text-emerald-400 bg-emerald-500/10 px-3 py-1 rounded-full border border-emerald-500/20">Slide 4 / 4</span>
                    </div>

                    <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
                        <!-- GitHub Stats Widget -->
                        <div class="glass-card p-6 rounded-xl flex flex-col justify-between space-y-4">
                            <div class="flex items-center justify-between">
                                <div class="flex items-center gap-3">
                                    <i class="fa-brands fa-github text-3xl text-cyan-400"></i>
                                    <div>
                                        <h3 class="font-bold text-white">Vaish09-VAISH</h3>
                                        <p class="text-xs font-mono text-slate-400">11 Repositories Created & Forked</p>
                                    </div>
                                </div>
                                <span class="px-2.5 py-1 rounded-full text-xs font-mono bg-emerald-500/10 text-emerald-400 border border-emerald-500/20">
                                    2026 Activity Active
                                </span>
                            </div>

                            <!-- GitHub Stats SVG -->
                            <div class="w-full flex justify-center py-2">
                                <img src="https://github-readme-stats.vercel.app/api?username=Vaish09-VAISH&show_icons=true&theme=dark&bg_color=0f172a&title_color=38bdf8&icon_color=c084fc&text_color=94a3b8" 
                                     alt="Vaish09-VAISH GitHub Stats" 
                                     class="w-full rounded-lg border border-slate-800 object-cover"
                                     onerror="this.onerror=null; this.src='https://placehold.co/600x200/0f172a/38bdf8?text=Vaish09-VAISH+GitHub+Stats';" />
                            </div>
                        </div>

                        <!-- Real Contribution Grid Replica (19 contributions in 2026) -->
                        <div class="glass-card p-6 rounded-xl flex flex-col justify-between space-y-4">
                            <div>
                                <div class="flex justify-between items-center">
                                    <h3 class="font-bold text-white flex items-center gap-2">
                                        <i class="fa-solid fa-calendar-check text-emerald-400"></i> 19 Contributions in 2026
                                    </h3>
                                    <span class="text-xs font-mono px-2.5 py-1 rounded bg-blue-600 text-white font-bold">2026</span>
                                </div>
                                <p class="text-xs text-slate-400 mt-1">Exact calendar contribution breakdown matching your profile</p>
                            </div>

                            <!-- Heatmap Matrix matching your screenshot (May-Oct green activity dots) -->
                            <div class="bg-slate-900/80 p-4 rounded-xl border border-slate-800 space-y-2">
                                <div class="flex justify-between text-[10px] font-mono text-slate-400 px-1">
                                    <span>Nov</span><span>Jan</span><span>Mar</span><span>May</span><span>Jul</span><span>Sep</span><span>Oct</span>
                                </div>
                                
                                <div class="grid grid-cols-16 gap-1.5 py-2" id="githubRealHeatmap">
                                    <!-- Dynamic real blocks rendered via JS -->
                                </div>

                                <div class="flex items-center justify-between text-[10px] text-slate-400 font-mono pt-1">
                                    <span>Learn how contributions count</span>
                                    <div class="flex items-center gap-1">
                                        <span class="text-[10px] mr-1">Less</span>
                                        <span class="w-2.5 h-2.5 rounded-sm bg-slate-800"></span>
                                        <span class="w-2.5 h-2.5 rounded-sm bg-emerald-900"></span>
                                        <span class="w-2.5 h-2.5 rounded-sm bg-emerald-600"></span>
                                        <span class="w-2.5 h-2.5 rounded-sm bg-emerald-400"></span>
                                        <span class="text-[10px] ml-1">More</span>
                                    </div>
                                </div>
                            </div>

                            <a href="https://github.com/Vaish09-VAISH" target="_blank" class="w-full py-2.5 rounded-xl bg-slate-800 hover:bg-slate-700 text-slate-200 text-xs font-mono flex items-center justify-center gap-2 transition-all">
                                <i class="fa-brands fa-github"></i> Open Vaish09-VAISH on GitHub
                            </a>
                        </div>
                    </div>
                </div>

            </div>
        </div>

        <!-- Slide Navigation Controls -->
        <div class="flex items-center justify-between mt-6">
            <button onclick="prevTab()" class="glass-card px-5 py-2.5 rounded-xl text-slate-300 hover:text-white flex items-center gap-2 text-sm font-medium transition-all">
                <i class="fa-solid fa-arrow-left"></i> Previous
            </button>
            <div class="flex gap-2" id="dotsContainer">
                <span class="w-2.5 h-2.5 rounded-full bg-cyan-400 cursor-pointer" onclick="switchTab('about')"></span>
                <span class="w-2.5 h-2.5 rounded-full bg-slate-700 cursor-pointer" onclick="switchTab('projects')"></span>
                <span class="w-2.5 h-2.5 rounded-full bg-slate-700 cursor-pointer" onclick="switchTab('skills')"></span>
                <span class="w-2.5 h-2.5 rounded-full bg-slate-700 cursor-pointer" onclick="switchTab('stats')"></span>
            </div>
            <button onclick="nextTab()" class="glass-card px-5 py-2.5 rounded-xl text-slate-300 hover:text-white flex items-center gap-2 text-sm font-medium transition-all">
                Next <i class="fa-solid fa-arrow-right"></i>
            </button>
        </div>
    </main>

    <!-- Footer -->
    <footer class="w-full max-w-6xl mx-auto px-4 py-6 mt-6 border-t border-slate-800/60 relative z-10 flex flex-col sm:flex-row items-center justify-between gap-4 text-xs text-slate-400 font-mono">
        <div>
            <span>© 2026 Vaishnavi G (Vaish09-VAISH). All rights reserved.</span>
        </div>
        <div class="flex items-center gap-4">
            <a href="https://github.com/Vaish09-VAISH" target="_blank" class="hover:text-cyan-400 transition-colors flex items-center gap-1">
                <i class="fa-brands fa-github"></i> Vaish09-VAISH
            </a>
        </div>
    </footer>

    <!-- Interactive Scripts -->
    <script>
        const tabs = ['about', 'projects', 'skills', 'stats'];
        let currentIndex = 0;

        function switchTab(tabId) {
            const index = tabs.indexOf(tabId);
            if (index === -1) return;
            
            currentIndex = index;
            const sliderTrack = document.getElementById('sliderTrack');
            sliderTrack.style.transform = `translateX(-${currentIndex * 100}%)`;

            // Update active buttons
            tabs.forEach(t => {
                const btn = document.getElementById(`btn-${t}`);
                if (t === tabId) {
                    btn.classList.add('active');
                } else {
                    btn.classList.remove('active');
                }
            });

            // Update indicators
            const dots = document.getElementById('dotsContainer').children;
            for (let i = 0; i < dots.length; i++) {
                if (i === currentIndex) {
                    dots[i].className = 'w-2.5 h-2.5 rounded-full bg-cyan-400 cursor-pointer';
                } else {
                    dots[i].className = 'w-2.5 h-2.5 rounded-full bg-slate-700 cursor-pointer';
                }
            }
        }

        function nextTab() {
            currentIndex = (currentIndex + 1) % tabs.length;
            switchTab(tabs[currentIndex]);
        }

        function prevTab() {
            currentIndex = (currentIndex - 1 + tabs.length) % tabs.length;
            switchTab(tabs[currentIndex]);
        }

        // Repository search filter
        function filterRepos() {
            const query = document.getElementById('repoSearch').value.toLowerCase();
            const items = document.querySelectorAll('.repo-item');
            items.forEach(item => {
                const name = item.getAttribute('data-name');
                if (name.includes(query)) {
                    item.style.display = 'flex';
                } else {
                    item.style.display = 'none';
                }
            });
        }

        // Render matching 2026 contributions heatmap based on your screenshot
        function renderRealHeatmap() {
            const grid = document.getElementById('githubRealHeatmap');
            if (!grid) return;
            
            const totalCells = 48; // 3x16 matrix representation
            // Indices with real commit activity as per your screenshot (May, Jun, Jul, Sep, Oct)
            const activeIndices = {
                18: 'bg-emerald-500',
                22: 'bg-emerald-400',
                25: 'bg-emerald-500',
                28: 'bg-emerald-600',
                30: 'bg-emerald-400',
                34: 'bg-emerald-500',
                39: 'bg-emerald-800',
                42: 'bg-emerald-400'
            };

            for (let i = 0; i < totalCells; i++) {
                const cell = document.createElement('div');
                const activeColor = activeIndices[i] || 'bg-slate-800';
                cell.className = `w-3 h-3 rounded-sm ${activeColor} transition-transform hover:scale-125`;
                grid.appendChild(cell);
            }
        }

        // Touch & Swipe gestures
        let touchStartX = 0;
        let touchEndX = 0;

        document.addEventListener('touchstart', e => {
            touchStartX = e.changedTouches[0].screenX;
        }, false);

        document.addEventListener('touchend', e => {
            touchEndX = e.changedTouches[0].screenX;
            if (touchEndX < touchStartX - 50) nextTab();
            if (touchEndX > touchStartX + 50) prevTab();
        }, false);

        window.onload = function() {
            renderRealHeatmap();
        };
    </script>
</body>
</html>
