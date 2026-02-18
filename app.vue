<template>
  <div class="app">
    <NuxtRouteAnnouncer />
    <header class="site-header">
      <div class="container header-inner">
        <NuxtLink to="/" class="logo">
          <span class="logo-mark">DigitAL RicH</span>
          <span class="logo-tech">Technologies</span>
        </NuxtLink>
        <nav class="nav" aria-label="Main">
          <NuxtLink to="/">Home</NuxtLink>
          <NuxtLink to="/features">Features</NuxtLink>
          <NuxtLink to="/pricing">Pricing</NuxtLink>
          <NuxtLink to="/about-us">About Us</NuxtLink>
          <NuxtLink to="/contact">Contact</NuxtLink>
        </nav>
      </div>
      <div class="header-accent" />
    </header>
    <main class="main">
      <NuxtPage />
    </main>
    <footer class="site-footer">
      <div class="container">
        <p>© Digital Rich Technologies. Venue Genius.</p>
      </div>
    </footer>
  </div>
</template>

<style>
/* DRT brand: blue–teal gradients, purple, geometric feel */
:root {
  --drt-bg: #fff;
  --drt-text: #1a1a1a;
  --drt-text-muted: #555;
  --drt-accent-blue: #1e3a5f;
  --drt-accent-teal: #0d9488;
  --drt-purple: #5b21b6;
  --drt-purple-dark: #3b0764;
  --drt-gradient: linear-gradient(90deg, var(--drt-accent-blue) 0%, var(--drt-accent-teal) 100%);
  --drt-gradient-hero: linear-gradient(135deg, #e0e7ff 0%, #fce7f3 50%, #e0e7ff 100%);
  --font-sans: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}

* { box-sizing: border-box; }
body { margin: 0; font-family: var(--font-sans); color: var(--drt-text); background: var(--drt-bg); line-height: 1.6; }

.app { min-height: 100vh; display: flex; flex-direction: column; }
.main { flex: 1; }

.container { width: 100%; max-width: 960px; margin: 0 auto; padding: 0 1.25rem; }

.site-header {
  background: var(--drt-bg);
  border-bottom: 1px solid #e5e7eb;
  position: relative;
}
.header-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 1rem;
  padding: 1rem 1.25rem;
}
.logo {
  text-decoration: none;
  color: var(--drt-text);
  font-weight: 600;
  font-size: 1.05rem;
}
.logo-mark { color: var(--drt-purple); }
.logo-tech { font-size: 0.9em; opacity: 0.9; }

.nav {
  display: flex;
  gap: 1.5rem;
  flex-wrap: wrap;
}
.nav a {
  color: var(--drt-text-muted);
  text-decoration: none;
  font-size: 0.95rem;
  font-weight: 500;
}
.nav a:hover,
.nav a.router-link-active {
  color: var(--drt-purple);
}

.header-accent {
  height: 4px;
  background: var(--drt-gradient);
  width: 100%;
}

.site-footer {
  padding: 1.5rem 0;
  text-align: center;
  font-size: 0.875rem;
  color: var(--drt-text-muted);
  border-top: 1px solid #e5e7eb;
}
.site-footer p { margin: 0; }
</style>
