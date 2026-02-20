<section class="relative h-screen w-full overflow-hidden bg-[oklch(0.596_0.145_163.225)] selection:bg-[oklch(0.905_0.093_164.15)] selection:text-[oklch(0.262_0.051_172.552)]">
    <!-- Abstract Background Recreation -->
    <div class="absolute inset-0 z-0 pointer-events-none overflow-hidden">
        <!-- Base gradient using brand emerald tones -->
        <div class="absolute inset-0 bg-gradient-to-br from-[oklch(0.596_0.145_163.225)] via-[oklch(0.508_0.118_165.612)] to-[oklch(0.432_0.095_166.913)]"></div>
        
        <!-- Light streaks/blobs using lighter emerald tones for dappled light effect -->
        <div class="bg-blur-shape bg-[oklch(0.845_0.143_164.978)] w-[150%] h-[40%] -top-[10%] -left-[20%] animate-fade-in delay-0"></div>
        <div class="bg-blur-shape bg-[oklch(0.765_0.177_163.223)] w-[120%] h-[30%] top-[30%] -right-[20%] animate-fade-in delay-100"></div>
        <div class="bg-blur-shape bg-[oklch(0.845_0.143_164.978)] w-[100%] h-[40%] bottom-[10%] left-[10%] animate-fade-in delay-200"></div>
        <div class="bg-blur-shape bg-[oklch(0.765_0.177_163.223)] w-[80%] h-[50%] -bottom-[20%] -right-[10%] animate-fade-in delay-300"></div>
        
        <!-- Noise texture overlay for grain -->
        <div class="absolute inset-0 opacity-[0.03]" style="background-image: url('data:image/svg+xml,%3Csvg viewBox=%220 0 200 200%22 xmlns=%22http://www.w3.org/2000/svg%22%3E%3Cfilter id=%22noiseFilter%22%3E%3CfeTurbulence type=%22fractalNoise%22 baseFrequency=%220.65%22 numOctaves=%223%22 stitchTiles=%22stitch%22/%3E%3C/filter%3E%3Crect width=%22100%25%22 height=%22100%25%22 filter=%22url(%23noiseFilter)%22/%3E%3C/svg%3E');"></div>
    </div>

    <!-- Main Hero Content -->
    <main class="relative z-10 flex flex-col items-center justify-center h-full w-full px-4 text-center">
        
        <!-- Headline -->
        <h1 class="text-balance font-serif text-[oklch(0.985_0_0)] leading-[0.9] md:leading-[0.85] tracking-tight">
            <!-- Line 1: Italic -->
            <span class="block text-[13vw] sm:text-[12vw] md:text-[8rem] lg:text-[10rem] xl:text-[11rem] italic font-light animate-fade-in-up delay-200">
                Approachable
            </span>
            <!-- Line 2: Regular -->
            <span class="block text-[13vw] sm:text-[12vw] md:text-[8rem] lg:text-[10rem] xl:text-[11rem] font-normal mt-2 md:mt-4 animate-fade-in-up delay-300">
                Intelligence
            </span>
        </h1>

        <!-- Subheadline -->
        <p class="mt-8 md:mt-12 text-pretty font-sans text-lg md:text-2xl text-[oklch(0.985_0_0)] max-w-2xl opacity-90 animate-fade-in-up delay-500 font-light tracking-wide">
            $20M+ in proven savings through vetted provider networks and elite dealership technology.
        </p>

    </main>

    <!-- Bottom Left: Accessibility Toggle -->
    <div class="absolute bottom-6 left-6 md:bottom-8 md:left-8 z-20 animate-fade-in delay-700">
        <button class="bg-[oklch(0.985_0_0)] rounded-full p-1 pr-4 flex items-center gap-3 border border-[oklch(0.922_0_0)] hover:border-[oklch(0.87_0_0)] transition-all group">
            <span class="bg-[oklch(0.922_0_0)] group-hover:bg-[oklch(0.87_0_0)] transition-colors rounded-full px-3 py-1.5 text-[10px] md:text-xs font-sans uppercase tracking-widest text-[oklch(0.439_0_0)] font-medium">
                Off
            </span>
            <span class="text-[10px] md:text-xs font-sans text-[oklch(0.439_0_0)] tracking-wider">
                Accessibility Mode
            </span>
        </button>
    </div>
</section>

<style>
    .text-balance { text-wrap: balance; }
    .text-pretty { text-wrap: pretty; }

    /* Animation keyframes */
    @keyframes fadeInUp {
        from {
            opacity: 0;
            transform: translateY(30px);
            filter: blur(4px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
            filter: blur(0);
        }
    }

    @keyframes fadeIn {
        from { opacity: 0; }
        to { opacity: 1; }
    }

    /* Animation Classes */
    .animate-fade-in-up {
        opacity: 0;
        animation: fadeInUp 0.8s cubic-bezier(0.22, 0.61, 0.36, 1) forwards;
    }

    .animate-fade-in {
        opacity: 0;
        animation: fadeIn 0.8s cubic-bezier(0.22, 0.61, 0.36, 1) forwards;
    }

    /* Staggered Delays */
    .delay-0 { animation-delay: 0ms; }
    .delay-200 { animation-delay: 200ms; }
    .delay-300 { animation-delay: 300ms; }
    .delay-500 { animation-delay: 500ms; }
    .delay-700 { animation-delay: 700ms; }

    /* Custom Background Styles to match the abstract blur */
    .bg-blur-shape {
        position: absolute;
        border-radius: 50%;
        filter: blur(80px);
        opacity: 0.6;
        transform: rotate(-45deg);
    }

    @media (prefers-reduced-motion: reduce) {
        .animate-fade-in-up, .animate-fade-in {
            animation: none;
            opacity: 1;
            transform: none;
            filter: none;
        }
    }
</style>
