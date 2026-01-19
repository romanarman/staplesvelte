<script lang="ts">
  import FeatureRow from "$lib/FeatureRow.svelte"
  import mascot from "$lib/assets/mascot/mascot.svg";


  const NAVY = "#252640";
  const CREAM = "#FFF9E5";
  const year = new Date().getFullYear();
</script>

<svelte:head>
  <style>
    html { scroll-behavior: smooth; }
  </style>
</svelte:head>

<div
  class="min-h-screen overflow-x-hidden"
  style="
    background-color: {CREAM};
    color: {NAVY};
    font-family: 'Hurme Geometric Sans 3', ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, 'Apple Color Emoji', 'Segoe UI Emoji';
  "
>
  <div id="top"></div>

  <!-- Top Nav -->
  <header style="background-color: {NAVY}; color: {CREAM};">
    <div class="mx-auto flex max-w-6xl items-center justify-between px-5 py-5">
      <a href="#top" class="flex items-center gap-3" aria-label="Staple home">
        <img src="/logo/staple-logo.svg" alt="Staple Bakery" class="h-12 w-auto" />
      </a>

      <nav class="hidden items-center gap-6 text-sm md:flex">
        <a class="opacity-80 hover:opacity-100" href="#about">About</a>
        <a class="opacity-80 hover:opacity-100" href="#ingredients">Ingredients</a>
        <a class="opacity-80 hover:opacity-100" href="#location">Location</a>
        <a class="opacity-80 hover:opacity-100" href="#contact">Contact</a>
      </nav>

      <a
        href="https://instagram.com/staplebakery"
        target="_blank"
        rel="noreferrer"
        class="inline-flex h-9 w-9 items-center justify-center rounded-full border transition hover:opacity-80"
        style="border-color: rgba(255,249,229,0.35);"
        aria-label="Instagram"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="1.5"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="h-5 w-5"
        >
          <rect x="2" y="2" width="20" height="20" rx="5" ry="5" />
          <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z" />
          <line x1="17.5" y1="6.5" x2="17.51" y2="6.5" />
        </svg>
      </a>
    </div>
  </header>

  <main>
    <!-- Hero -->
    <section class="relative">
    <div class="mx-auto grid min-h-[calc(100svh-72px)] items-center gap-10 px-5 py-10 md:grid-cols-12 md:py-16">
        <!-- Left -->
        <div class="md:col-span-6 flex flex-col items-center">
        <div class="flex flex-col items-center md:items-start">
          <p class="text-xs font-medium tracking-[0.22em] opacity-80">
              NEIGHBOURHOOD BAKERY • FOUNDED 2026
          </p>

          <h1 class="mt-6 text-[clamp(4.5rem,8vw,10rem)] font-bold leading-[0.9] tracking-tight text-center md:text-left">
              <span class="block">BREAD</span>
              <span class="block">PASTRY</span>
              <span class="block">COFFEE</span>
          </h1>
        </div>
        </div>

        <!-- Right -->
    <div class="md:col-span-6 flex items-center justify-center md:justify-center overflow-visible">
        <img
            src={mascot}
            alt="Mascot"
            class="block h-auto w-[min(88vw,420px)] sm:w-[520px] md:w-[640px] lg:w-[720px] xl:w-[820px]"
        />
        </div>
    </div>

    <div class="mx-auto max-w-6xl px-5">
        <div class="h-px w-full" style="background-color: rgba(37,38,64,0.14);"></div>
    </div>
    </section>

    <!-- About -->
    <section id="about">
      <div class="mx-auto max-w-6xl px-5 py-14 md:py-20">
        <div class="grid gap-10 md:grid-cols-12">
          <div class="md:col-span-4">
            <p class="text-xs font-medium tracking-[0.22em] opacity-80">ABOUT</p>
            <h2 class="mt-4 text-3xl font-medium tracking-tight">A local bakery, made properly.</h2>
          </div>

          <div class="md:col-span-8">
            <div class="max-w-2xl space-y-8 text-[clamp(1.05rem,1.2vw,1.25rem)] leading-relaxed opacity-90">
              <p>
                Founded in 2026, sitting just off Stapleton Road - a small neighbourhood bakery built around household staples:
                the everyday breads, pastries and drinks that make a home feel like home.
              </p>
              <p>
                Our bread is made in-house using British-milled organic flour. Our pastry is laminated the traditional way
                with high quality French butter. And our drinks are made with freshly-roasted beans from a local roaster.
              </p>
            </div>
          </div>
        </div>
      </div>

      <div class="mx-auto max-w-6xl px-5">
        <div class="h-px w-full" style="background-color: rgba(37,38,64,0.14);"></div>
      </div>
    </section>

    <!-- Ingredients -->
    <section id="ingredients">
      <div class="mx-auto max-w-6xl px-5 py-14 md:py-20">
        <div class="grid gap-10 md:grid-cols-12">
          <div class="md:col-span-5">
            <p class="text-xs font-medium tracking-[0.22em] opacity-80">INGREDIENTS</p>
            <h2 class="mt-4 text-3xl font-medium tracking-tight">Quality you can taste.</h2>
            <p class="mt-4 text-sm leading-relaxed opacity-85">
              We keep it simple: great flour, great butter, great coffee - and a lot of repetition.
            </p>
          </div>

          <div class="md:col-span-7">
            <div class="grid gap-4">
              <FeatureRow
                title="Bread"
                body="Made in-house using British-milled organic flour - slow fermentation for flavour and structure."
              />
              <FeatureRow
                title="Pastry"
                body="Traditional lamination with high-quality French butter and French flour for that clean, crisp flake."
              />
              <FeatureRow
                title="Coffee"
                body="Drinks made with beans from a local roaster - dialled in for maximum flavour."
              />
            </div>
          </div>
        </div>
      </div>

      <div class="mx-auto max-w-6xl px-5">
        <div class="h-px w-full" style="background-color: rgba(37,38,64,0.14);"></div>
      </div>
    </section>

    <!-- Location -->
    <section id="location">
      <div class="mx-auto max-w-6xl px-5 py-14 md:py-20">
        <div class="grid gap-10 md:grid-cols-12">
          <div class="md:col-span-5">
            <p class="text-xs font-medium tracking-[0.22em] opacity-80">LOCATION</p>
            <h2 class="mt-4 text-3xl font-medium tracking-tight">Find Staple.</h2>
            <p class="mt-4 text-sm leading-relaxed opacity-85">
              We’re in Easton, Bristol - come and find us!
            </p>
          </div>

          <div class="md:col-span-7">
            <div class="rounded-3xl border p-6" style="border-color: rgba(37,38,64,0.14);">
              <div class="text-sm font-medium">112 St Marks Road</div>
              <div class="mt-1 text-sm opacity-80">Easton, Bristol, BS5 6JD</div>

              <div class="mt-6 grid gap-3 md:grid-cols-2">
                <a
                  class="inline-flex items-center justify-center gap-2 rounded-2xl border px-4 py-3 text-sm font-medium transition hover:bg-[rgba(37,38,64,0.04)]"
                  style="border-color: rgba(37,38,64,0.22);"
                  href="https://www.google.com/maps/search/?api=1&query=112%20St%20Marks%20Road%2C%20Easton%2C%20Bristol%2C%20BS5%206JD"
                  target="_blank"
                  rel="noreferrer"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="1.7"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    class="h-4 w-4 opacity-80"
                    aria-hidden="true"
                  >
                    <path d="M12 21s7-4.35 7-11a7 7 0 1 0-14 0c0 6.65 7 11 7 11z" />
                    <circle cx="12" cy="10" r="2.5" />
                  </svg>
                  Open in Maps
                </a>

                <a
                  class="inline-flex items-center justify-center gap-2 rounded-2xl px-4 py-3 text-sm font-medium shadow-sm transition hover:shadow"
                  style="background-color: {NAVY}; color: {CREAM};"
                  href="https://waze.com/ul?q=112%20St%20Marks%20Road%20Easton%20Bristol%20BS5%206JD&navigate=yes"
                  target="_blank"
                  rel="noreferrer"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="1.7"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    class="h-4 w-4 opacity-90"
                    aria-hidden="true"
                  >
                    <path d="M7 7h10" />
                    <path d="M7 7v10a3 3 0 0 0 3 3h7" />
                    <circle cx="7" cy="7" r="1.5" />
                    <circle cx="17" cy="20" r="1.5" />
                  </svg>
                  Open in Waze
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="mx-auto max-w-6xl px-5">
        <div class="h-px w-full" style="background-color: rgba(37,38,64,0.14);"></div>
      </div>
    </section>

    <!-- Contact -->
    <section id="contact">
      <div class="mx-auto max-w-6xl px-5 py-14 md:py-20">
        <div class="grid items-start gap-10 md:grid-cols-12">
          <div class="md:col-span-6">
            <p class="text-xs font-medium tracking-[0.22em] opacity-80">CONTACT</p>
            <h2 class="mt-4 text-3xl font-medium tracking-tight">Hello 👋</h2>
            <p class="mt-4 text-sm leading-relaxed opacity-85">
              For enquiries or questions, email us and we’ll get back to you as soon as we can.
            </p>

            <div class="mt-6 flex w-full flex-col items-center gap-3 md:items-start">
              <a
                href="mailto:hello@staplebakery.co.uk"
                class="
                  w-full md:w-auto
                  rounded-2xl
                  px-6 py-4
                  text-sm font-medium
                  text-center
                  shadow-sm transition hover:shadow
                "
                style="background-color: {NAVY}; color: {CREAM};"
              >
                hello@staplebakery.co.uk
              </a>
              <span class="text-xs opacity-70">(tap to email)</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="border-t" style="border-color: rgba(37,38,64,0.12);">
      <div class="mx-auto flex max-w-6xl flex-col gap-4 px-5 py-10 md:flex-row md:items-center md:justify-between">
        <div class="text-sm opacity-85">© {year} Staple Bakery</div>
        <div class="flex flex-wrap items-center gap-x-6 gap-y-2 text-sm">
          <a class="opacity-80 hover:opacity-100" href="#about">About</a>
          <a class="opacity-80 hover:opacity-100" href="#ingredients">Ingredients</a>
          <a class="opacity-80 hover:opacity-100" href="#location">Location</a>
          <a class="opacity-80 hover:opacity-100" href="mailto:hello@staplebakery.co.uk">Email</a>
        </div>
      </div>
    </footer>
  </main>
</div>
