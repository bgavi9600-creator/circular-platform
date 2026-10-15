<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CIRCULAR â€” Design Electronics for Repair, Reuse & Recovery | IMX26-PS07</title>
  <meta name="description" content="A digital platform keeping electronics in active service longer through open repair diagnostics, vetted local workshops, and certified end-of-life recovery. Challenge: IMX26-PS07 â€” CEDA-EPS">

  <!-- Google Fonts: Plus Jakarta Sans & Space Mono -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&family=Space+Mono:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet">

  <style>
/* ==========================================================================
   CIRCULAR â€” Design Electronics for Repair, Reuse & Recovery
   Challenge: IMX26-PS07 â€” CEDA-EPS
   Style System: Editorial Climate-Tech & Clean Product Design
   ========================================================================== */

:root {
  /* Color Palette */
  --bg-warm: #F9F8F4;
  --bg-card: #FFFFFF;
  --bg-subtle: #F2F1EC;
  --bg-muted: #EBEAE3;
  --bg-dark: #0D2416;
  --bg-dark-card: #143321;
  --bg-dark-elevated: #1B402B;

  /* Forest Greens */
  --forest-900: #091910;
  --forest-800: #0E2818;
  --forest-700: #143823;
  --forest-600: #1D4E32;
  --forest-500: #296843;
  --forest-300: #4B916B;
  --forest-100: #D8EADF;

  /* Vivid Lime Accents */
  --lime-500: #C2FA2B;
  --lime-400: #CEFF3E;
  --lime-300: #DCFF70;
  --lime-100: #F3FED6;
  --lime-text: #0E2818;

  /* Charcoal & Neutrals */
  --charcoal-900: #161B18;
  --charcoal-800: #242B27;
  --charcoal-700: #38423D;
  --charcoal-500: #5D6B63;
  --charcoal-400: #7E8D85;
  --charcoal-200: #C8D1CA;
  --charcoal-100: #E4E9E5;

  /* Borders */
  --border-subtle: #E6E5DD;
  --border-card: #DEDCD3;
  --border-focus: #143823;
  --border-lime: #B8F020;
  --border-dark: #1E462E;

  /* Functional Alerts */
  --alert-red-bg: #FEF2F2;
  --alert-red-border: #F87171;
  --alert-red-text: #991B1B;
  --alert-amber-bg: #FFFBEB;
  --alert-amber-border: #FBBF24;
  --alert-amber-text: #92400E;
  --alert-green-bg: #ECFDF5;
  --alert-green-border: #34D399;
  --alert-green-text: #065F46;

  /* Typography */
  --font-sans: 'Plus Jakarta Sans', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  --font-mono: 'Space Mono', 'SF Mono', Consolas, monospace;
  --font-display: 'Plus Jakarta Sans', sans-serif;

  /* Elevation */
  --shadow-xs: 0 1px 2px rgba(13, 36, 22, 0.04);
  --shadow-sm: 0 2px 6px rgba(13, 36, 22, 0.06);
  --shadow-md: 0 6px 18px rgba(13, 36, 22, 0.08);
  --shadow-lg: 0 16px 36px rgba(13, 36, 22, 0.12);
  --shadow-card: 0 3px 0 #D8D7CE;

  /* Radius */
  --radius-sm: 6px;
  --radius-md: 10px;
  --radius-lg: 16px;
  --radius-xl: 24px;
  --radius-full: 9999px;

  /* Transitions */
  --transition-fast: 160ms cubic-bezier(0.2, 0, 0, 1);
  --transition-normal: 240ms cubic-bezier(0.2, 0, 0, 1);
  --transition-bounce: 350ms cubic-bezier(0.34, 1.56, 0.64, 1);
}

/* Base Reset */
*, *::before, *::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  scroll-behavior: smooth;
  font-size: 16px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

body {
  font-family: var(--font-sans);
  background-color: var(--bg-warm);
  color: var(--charcoal-800);
  line-height: 1.6;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  overflow-x: hidden;
}

img, svg {
  display: block;
  max-width: 100%;
}

a {
  color: inherit;
  text-decoration: none;
}

button, input, select, textarea {
  font: inherit;
  color: inherit;
  background: none;
  border: none;
  outline: none;
}

button {
  cursor: pointer;
}

/* Container */
.container {
  width: 100%;
  max-width: 1240px;
  margin: 0 auto;
  padding: 0 1.5rem;
}

.container-narrow {
  width: 100%;
  max-width: 900px;
  margin: 0 auto;
  padding: 0 1.5rem;
}

/* ==========================================================================
   NAVIGATION BAR & CHALLENGE BANNER
   ========================================================================== */

.top-bar {
  background-color: var(--forest-900);
  color: var(--charcoal-200);
  font-size: 0.8125rem;
  padding: 0.45rem 1rem;
  border-bottom: 1px solid var(--border-dark);
}

.top-bar-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.challenge-tag {
  display: inline-flex;
  align-items: center;
  gap: 0.45rem;
  font-family: var(--font-mono);
  font-size: 0.75rem;
  color: var(--lime-400);
  letter-spacing: 0.04em;
  font-weight: 600;
}

.challenge-tag .pulse-dot {
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background-color: var(--lime-400);
  box-shadow: 0 0 8px var(--lime-400);
  animation: pulseDot 2s infinite;
}

@keyframes pulseDot {
  0%, 100% { opacity: 1; transform: scale(1); }
  50% { opacity: 0.4; transform: scale(0.8); }
}

.top-bar-links {
  display: flex;
  align-items: center;
  gap: 1.25rem;
}

.top-bar-links a {
  color: var(--charcoal-200);
  transition: color var(--transition-fast);
}

.top-bar-links a:hover {
  color: #FFFFFF;
}

/* Main Site Header */
.site-header {
  position: sticky;
  top: 0;
  z-index: 90;
  background-color: rgba(249, 248, 244, 0.94);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border-bottom: 1px solid var(--border-subtle);
  transition: box-shadow var(--transition-normal);
}

.site-header.scrolled {
  box-shadow: var(--shadow-sm);
}

.header-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 4.75rem;
  gap: 1.5rem;
}

/* Brand Identity */
.brand-link {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.brand-icon {
  width: 2.5rem;
  height: 2.5rem;
  border-radius: var(--radius-md);
  background: var(--forest-800);
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--lime-400);
  box-shadow: 0 2px 0 var(--forest-900);
  transition: transform var(--transition-fast);
}

.brand-link:hover .brand-icon {
  transform: rotate(-8deg);
}

.brand-meta {
  display: flex;
  flex-direction: column;
}

.brand-title {
  font-size: 1.35rem;
  font-weight: 800;
  letter-spacing: -0.03em;
  color: var(--forest-900);
  line-height: 1.1;
  display: flex;
  align-items: center;
  gap: 0.4rem;
}

.brand-title .badge-beta {
  font-family: var(--font-mono);
  font-size: 0.625rem;
  padding: 0.1rem 0.4rem;
  background-color: var(--lime-400);
  color: var(--forest-900);
  border-radius: var(--radius-sm);
  font-weight: 700;
  letter-spacing: 0.05em;
}

.brand-sub {
  font-size: 0.725rem;
  color: var(--charcoal-500);
  font-weight: 500;
  letter-spacing: 0.02em;
}

/* Primary Nav */
.main-nav {
  display: flex;
  align-items: center;
  gap: 0.4rem;
}

.nav-link {
  padding: 0.5rem 0.85rem;
  font-size: 0.9375rem;
  font-weight: 600;
  color: var(--charcoal-700);
  border-radius: var(--radius-sm);
  transition: all var(--transition-fast);
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
}

.nav-link:hover {
  color: var(--forest-900);
  background-color: var(--bg-subtle);
}

.nav-link.active {
  color: var(--forest-900);
  background-color: var(--forest-100);
}

.header-cta-group {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.mobile-toggle {
  display: none;
  padding: 0.6rem;
  border-radius: var(--radius-sm);
  background-color: var(--bg-subtle);
  border: 1px solid var(--border-subtle);
  color: var(--forest-900);
}

/* Buttons */
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 1.4rem;
  border-radius: var(--radius-md);
  font-size: 0.9375rem;
  font-weight: 700;
  letter-spacing: -0.01em;
  transition: all var(--transition-fast);
  white-space: nowrap;
  user-select: none;
}

.btn-sm {
  padding: 0.45rem 0.85rem;
  font-size: 0.8125rem;
  border-radius: var(--radius-sm);
}

.btn-lg {
  padding: 0.95rem 1.85rem;
  font-size: 1.05rem;
  border-radius: var(--radius-md);
}

.btn-primary {
  background-color: var(--forest-800);
  color: #FFFFFF;
  border: 1px solid var(--forest-900);
  box-shadow: 0 3px 0 var(--forest-900);
}

.btn-primary:hover {
  background-color: var(--forest-700);
  transform: translateY(-1px);
  box-shadow: 0 4px 0 var(--forest-900);
}

.btn-primary:active {
  transform: translateY(2px);
  box-shadow: 0 1px 0 var(--forest-900);
}

.btn-lime {
  background-color: var(--lime-400);
  color: var(--forest-900);
  border: 1px solid #A4DB10;
  box-shadow: 0 3px 0 #92C60B;
}

.btn-lime:hover {
  background-color: var(--lime-300);
  transform: translateY(-1px);
  box-shadow: 0 4px 0 #92C60B;
}

.btn-lime:active {
  transform: translateY(2px);
  box-shadow: 0 1px 0 #92C60B;
}

.btn-secondary {
  background-color: var(--bg-card);
  color: var(--forest-900);
  border: 1px solid var(--border-card);
  box-shadow: 0 2px 0 var(--border-card);
}

.btn-secondary:hover {
  background-color: var(--bg-subtle);
  border-color: var(--charcoal-200);
  transform: translateY(-1px);
}

.btn-secondary:active {
  transform: translateY(1px);
  box-shadow: none;
}

.btn-ghost {
  color: var(--forest-800);
  padding: 0.5rem 0.75rem;
}

.btn-ghost:hover {
  background-color: var(--bg-subtle);
}

/* ==========================================================================
   HERO SECTION
   ========================================================================== */

.hero-section {
  padding: 4.5rem 0 3.5rem;
  position: relative;
  overflow: hidden;
}

.hero-grid {
  display: grid;
  grid-template-columns: 1.15fr 0.85fr;
  gap: 3.5rem;
  align-items: center;
}

.hero-copy {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.hero-pill-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.6rem;
  padding: 0.35rem 0.85rem;
  background-color: var(--bg-subtle);
  border: 1px solid var(--border-card);
  border-radius: var(--radius-full);
  font-size: 0.8125rem;
  font-weight: 600;
  color: var(--forest-800);
  width: fit-content;
}

.hero-pill-badge .indicator-pill {
  background-color: var(--lime-400);
  color: var(--forest-900);
  padding: 0.15rem 0.45rem;
  border-radius: var(--radius-full);
  font-size: 0.6875rem;
  font-weight: 800;
  font-family: var(--font-mono);
}

.hero-headline {
  font-size: clamp(2.35rem, 5vw, 3.65rem);
  font-weight: 800;
  line-height: 1.08;
  letter-spacing: -0.035em;
  color: var(--forest-900);
}

.hero-headline .highlight-lime {
  position: relative;
  display: inline-block;
  color: var(--forest-800);
}

.hero-headline .highlight-lime::after {
  content: '';
  position: absolute;
  left: -2px;
  right: -2px;
  bottom: 6px;
  height: 14px;
  background-color: var(--lime-300);
  z-index: -1;
  border-radius: 4px;
  opacity: 0.85;
}

.hero-subhead {
  font-size: 1.15rem;
  line-height: 1.55;
  color: var(--charcoal-700);
  max-width: 580px;
}

.hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  margin-top: 0.5rem;
}

.hero-trust-bullets {
  display: flex;
  flex-wrap: wrap;
  gap: 1.5rem;
  padding-top: 1rem;
  border-top: 1px solid var(--border-subtle);
  font-size: 0.8125rem;
  color: var(--charcoal-600);
}

.trust-item {
  display: flex;
  align-items: center;
  gap: 0.45rem;
  font-weight: 600;
}

.trust-item svg {
  color: var(--forest-600);
  flex-shrink: 0;
}

/* Hero Interactive Telemetry Card */
.hero-visual-card {
  background-color: var(--forest-900);
  border-radius: var(--radius-xl);
  border: 1px solid var(--border-dark);
  box-shadow: var(--shadow-lg), 0 0 0 1px rgba(255,255,255,0.05) inset;
  color: #FFFFFF;
  padding: 1.75rem;
  position: relative;
  overflow: hidden;
}

.hero-visual-card::before {
  content: '';
  position: absolute;
  top: -100px;
  right: -100px;
  width: 250px;
  height: 250px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(194,250,43,0.18) 0%, rgba(194,250,43,0) 70%);
  pointer-events: none;
}

.telemetry-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-bottom: 1px solid var(--border-dark);
  padding-bottom: 1rem;
  margin-bottom: 1.25rem;
}

.telemetry-status {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-family: var(--font-mono);
  font-size: 0.75rem;
  color: var(--lime-400);
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.telemetry-chip {
  background: rgba(255, 255, 255, 0.08);
  padding: 0.25rem 0.6rem;
  border-radius: var(--radius-sm);
  font-family: var(--font-mono);
  font-size: 0.7rem;
  color: var(--charcoal-200);
}

/* Device Schematic graphic */
.schematic-frame {
  background: var(--bg-dark-card);
  border: 1px dashed rgba(200, 255, 50, 0.25);
  border-radius: var(--radius-md);
  padding: 1.25rem;
  margin-bottom: 1.25rem;
  position: relative;
}

.schematic-svg {
  width: 100%;
  height: auto;
  stroke: var(--lime-400);
}

.schematic-callouts {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.75rem;
  margin-top: 1rem;
}

.callout-node {
  background: rgba(0, 0, 0, 0.35);
  border-left: 3px solid var(--lime-400);
  padding: 0.5rem 0.65rem;
  border-radius: 0 var(--radius-sm) var(--radius-sm) 0;
}

.callout-node.alert {
  border-left-color: #FF6B4A;
}

.callout-title {
  font-family: var(--font-mono);
  font-size: 0.7rem;
  color: var(--charcoal-200);
  text-transform: uppercase;
  letter-spacing: 0.04em;
}

.callout-val {
  font-size: 0.85rem;
  font-weight: 700;
  color: #FFFFFF;
}

.telemetry-metrics-row {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0.75rem;
  margin-top: 1rem;
}

.mini-stat-box {
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: var(--radius-sm);
  padding: 0.65rem;
  text-align: center;
}

.mini-stat-num {
  font-family: var(--font-mono);
  font-size: 1.15rem;
  font-weight: 700;
  color: var(--lime-400);
}

.mini-stat-lbl {
  font-size: 0.6875rem;
  color: var(--charcoal-200);
  margin-top: 0.15rem;
}

/* ==========================================================================
   CIRCULAR JOURNEY: DIAGNOSE -> REPAIR -> REUSE -> RECOVER
   ========================================================================== */

.section-padding {
  padding: 5rem 0;
}

.section-header {
  text-align: center;
  max-width: 740px;
  margin: 0 auto 3.5rem;
}

.section-label {
  display: inline-flex;
  align-items: center;
  gap: 0.45rem;
  font-family: var(--font-mono);
  font-size: 0.75rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: var(--forest-600);
  background-color: var(--forest-100);
  padding: 0.25rem 0.75rem;
  border-radius: var(--radius-full);
  margin-bottom: 0.85rem;
}

.section-title {
  font-size: clamp(1.85rem, 3.5vw, 2.75rem);
  font-weight: 800;
  letter-spacing: -0.03em;
  color: var(--forest-900);
  line-height: 1.15;
  margin-bottom: 1rem;
}

.section-desc {
  font-size: 1.05rem;
  color: var(--charcoal-600);
  line-height: 1.6;
}

/* Journey Flow Nodes */
.journey-timeline {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1.25rem;
  position: relative;
}

.journey-step-card {
  background: var(--bg-card);
  border: 1px solid var(--border-card);
  border-radius: var(--radius-lg);
  padding: 1.75rem 1.4rem;
  display: flex;
  flex-direction: column;
  position: relative;
  box-shadow: var(--shadow-card);
  transition: all var(--transition-normal);
  cursor: pointer;
}

.journey-step-card:hover {
  transform: translateY(-4px);
  border-color: var(--forest-500);
  box-shadow: 0 8px 0 var(--border-card);
}

.journey-step-card.active {
  border-color: var(--forest-800);
  background: #FCFDF9;
  box-shadow: 0 4px 0 var(--forest-800);
}

.step-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 1.25rem;
}

.step-badge {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  font-weight: 800;
  color: var(--forest-800);
  background: var(--bg-subtle);
  border: 1px solid var(--border-subtle);
  padding: 0.2rem 0.5rem;
  border-radius: var(--radius-sm);
}

.step-icon-wrap {
  width: 2.75rem;
  height: 2.75rem;
  border-radius: var(--radius-md);
  background: var(--forest-100);
  color: var(--forest-800);
  display: flex;
  align-items: center;
  justify-content: center;
}

.step-title {
  font-size: 1.2rem;
  font-weight: 800;
  color: var(--forest-900);
  letter-spacing: -0.02em;
  margin-bottom: 0.5rem;
}

.step-hierarchy {
  font-family: var(--font-mono);
  font-size: 0.6875rem;
  font-weight: 700;
  color: var(--forest-600);
  text-transform: uppercase;
  margin-bottom: 0.75rem;
}

.step-text {
  font-size: 0.875rem;
  color: var(--charcoal-600);
  line-height: 1.5;
  margin-bottom: 1rem;
  flex-grow: 1;
}

.step-outcome-pill {
  font-size: 0.75rem;
  font-weight: 700;
  padding: 0.35rem 0.65rem;
  background-color: var(--bg-subtle);
  border-radius: var(--radius-sm);
  color: var(--forest-800);
  display: flex;
  align-items: center;
  gap: 0.4rem;
}

/* ==========================================================================
   PROBLEM VS SOLUTION / WHY CIRCULAR WORKS
   ========================================================================== */

.problem-solution-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
  margin-top: 2rem;
}

.problem-card {
  background: #FFF5F2;
  border: 1px solid #FED7AA;
  border-radius: var(--radius-xl);
  padding: 2.5rem;
  position: relative;
}

.solution-card {
  background: var(--forest-900);
  border: 1px solid var(--border-dark);
  border-radius: var(--radius-xl);
  padding: 2.5rem;
  color: #FFFFFF;
  position: relative;
}

.ps-badge {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  padding: 0.25rem 0.65rem;
  border-radius: var(--radius-sm);
  display: inline-block;
  margin-bottom: 1.25rem;
}

.problem-card .ps-badge {
  background: #FEE2E2;
  color: #B91C1C;
}

.solution-card .ps-badge {
  background: rgba(194, 250, 43, 0.2);
  color: var(--lime-400);
  border: 1px solid rgba(194, 250, 43, 0.4);
}

.ps-title {
  font-size: 1.6rem;
  font-weight: 800;
  letter-spacing: -0.02em;
  line-height: 1.2;
  margin-bottom: 1.25rem;
}

.problem-card .ps-title {
  color: #7C2D12;
}

.solution-card .ps-title {
  color: #FFFFFF;
}

.ps-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.ps-list li {
  display: flex;
  align-items: flex-start;
  gap: 0.75rem;
  font-size: 0.9375rem;
  line-height: 1.5;
}

.problem-card .ps-list li {
  color: #431407;
}

.solution-card .ps-list li {
  color: var(--charcoal-200);
}

.ps-icon-cross {
  color: #DC2626;
  flex-shrink: 0;
  margin-top: 0.15rem;
}

.ps-icon-check {
  color: var(--lime-400);
  flex-shrink: 0;
  margin-top: 0.15rem;
}

/* ==========================================================================
   FEATURED REPAIR EXAMPLES & TRUST SECTION
   ========================================================================== */

.featured-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
}

.featured-card {
  background: var(--bg-card);
  border: 1px solid var(--border-card);
  border-radius: var(--radius-lg);
  overflow: hidden;
  box-shadow: var(--shadow-sm);
  transition: all var(--transition-normal);
  display: flex;
  flex-direction: column;
}

.featured-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-md);
  border-color: var(--forest-500);
}

.featured-visual {
  height: 160px;
  background: var(--bg-subtle);
  border-bottom: 1px solid var(--border-subtle);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1.5rem;
  position: relative;
}

.score-badge-floating {
  position: absolute;
  top: 1rem;
  right: 1rem;
  font-family: var(--font-mono);
  font-size: 0.75rem;
  font-weight: 800;
  background: var(--forest-900);
  color: var(--lime-400);
  padding: 0.25rem 0.55rem;
  border-radius: var(--radius-sm);
}

.featured-body {
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  flex-grow: 1;
}

.featured-device {
  font-size: 1.15rem;
  font-weight: 800;
  color: var(--forest-900);
  margin-bottom: 0.35rem;
}

.featured-tagline {
  font-size: 0.875rem;
  color: var(--charcoal-600);
  margin-bottom: 1.25rem;
  flex-grow: 1;
}

.featured-stats-row {
  display: flex;
  justify-content: space-between;
  border-top: 1px solid var(--border-subtle);
  padding-top: 0.85rem;
  font-size: 0.8125rem;
  color: var(--charcoal-700);
}

.featured-stats-row span strong {
  color: var(--forest-900);
}

/* Trust Principles Grid */
.trust-principles-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
  margin-top: 2rem;
}

.principle-card {
  background: var(--bg-card);
  border: 1px solid var(--border-card);
  border-radius: var(--radius-lg);
  padding: 1.75rem;
}

.principle-icon {
  width: 2.75rem;
  height: 2.75rem;
  border-radius: var(--radius-md);
  background: var(--forest-100);
  color: var(--forest-800);
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1rem;
}

.principle-title {
  font-size: 1.1rem;
  font-weight: 800;
  color: var(--forest-900);
  margin-bottom: 0.5rem;
}

.principle-text {
  font-size: 0.875rem;
  color: var(--charcoal-600);
  line-height: 1.55;
}

/* ==========================================================================
   DEVICE CHECKER: INTERACTIVE CORE DEMO
   ========================================================================== */

.checker-container {
  background: var(--bg-card);
  border: 1px solid var(--border-card);
  border-radius: var(--radius-xl);
  box-shadow: var(--shadow-md);
  overflow: hidden;
  margin-top: 2rem;
}

/* Step Bar */
.checker-steps-bar {
  background: var(--bg-subtle);
  border-bottom: 1px solid var(--border-subtle);
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  position: relative;
}

.step-tab {
  padding: 1.15rem 1rem;
  display: flex;
  align-items: center;
  gap: 0.75rem;
  color: var(--charcoal-500);
  font-size: 0.875rem;
  font-weight: 700;
  border-bottom: 3px solid transparent;
  transition: all var(--transition-fast);
}

.step-tab.active {
  color: var(--forest-900);
  background: #FFFFFF;
  border-bottom-color: var(--forest-800);
}

.step-tab.completed {
  color: var(--forest-700);
}

.step-tab-num {
  width: 1.65rem;
  height: 1.65rem;
  border-radius: 50%;
  background: var(--border-card);
  color: var(--charcoal-700);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: var(--font-mono);
  font-size: 0.75rem;
  font-weight: 700;
}

.step-tab.active .step-tab-num {
  background: var(--forest-800);
  color: #FFFFFF;
}

.step-tab.completed .step-tab-num {
  background: var(--lime-400);
  color: var(--forest-900);
}

.checker-body {
  padding: 2.5rem;
}

.checker-step-pane {
  display: none;
}

.checker-step-pane.active {
  display: block;
  animation: fadeIn 0.3s ease;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(6px); }
  to { opacity: 1; transform: translateY(0); }
}

.pane-heading {
  margin-bottom: 1.75rem;
}

.pane-title {
  font-size: 1.5rem;
  font-weight: 800;
  color: var(--forest-900);
  letter-spacing: -0.02em;
  margin-bottom: 0.4rem;
}

.pane-subtitle {
  font-size: 0.9375rem;
  color: var(--charcoal-600);
}

/* Category Grid */
.category-selection-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 1rem;
}

.category-card-btn {
  background: var(--bg-card);
  border: 2px solid var(--border-card);
  border-radius: var(--radius-lg);
  padding: 1.5rem 1rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.75rem;
  text-align: center;
  transition: all var(--transition-fast);
}

.category-card-btn:hover {
  border-color: var(--forest-600);
  background: var(--bg-subtle);
  transform: translateY(-2px);
}

.category-card-btn.selected {
  border-color: var(--forest-800);
  background: var(--forest-100);
  box-shadow: 0 0 0 2px var(--forest-800);
}

.cat-icon-frame {
  width: 3.25rem;
  height: 3.25rem;
  border-radius: var(--radius-md);
  background: var(--bg-subtle);
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--forest-800);
}

.category-card-btn.selected .cat-icon-frame {
  background: var(--forest-800);
  color: var(--lime-400);
}

.cat-label {
  font-size: 0.9375rem;
  font-weight: 700;
  color: var(--forest-900);
}

/* Model Preset & Search */
.model-input-wrap {
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
}

.quick-models-label {
  font-size: 0.8125rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  color: var(--charcoal-500);
  font-family: var(--font-mono);
}

.model-presets-row {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.model-preset-pill {
  padding: 0.5rem 1rem;
  border-radius: var(--radius-full);
  border: 1px solid var(--border-card);
  background: var(--bg-card);
  font-size: 0.875rem;
  font-weight: 600;
  color: var(--charcoal-700);
  transition: all var(--transition-fast);
}

.model-preset-pill:hover {
  border-color: var(--forest-800);
  color: var(--forest-900);
}

.model-preset-pill.selected {
  background: var(--forest-800);
  color: #FFFFFF;
  border-color: var(--forest-800);
}

.or-divider {
  display: flex;
  align-items: center;
  gap: 1rem;
  color: var(--charcoal-400);
  font-size: 0.8125rem;
  text-transform: uppercase;
  font-family: var(--font-mono);
}

.or-divider::before, .or-divider::after {
  content: '';
  flex: 1;
  height: 1px;
  background: var(--border-subtle);
}

.form-group {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.form-label {
  font-size: 0.875rem;
  font-weight: 700;
  color: var(--forest-900);
}

.form-input, .form-select, .form-textarea {
  width: 100%;
  padding: 0.75rem 1rem;
  border: 1px solid var(--border-card);
  border-radius: var(--radius-md);
  background: #FFFFFF;
  font-size: 0.9375rem;
  color: var(--charcoal-800);
  transition: border-color var(--transition-fast);
}

.form-input:focus, .form-select:focus, .form-textarea:focus {
  border-color: var(--forest-700);
  box-shadow: 0 0 0 3px rgba(20, 56, 35, 0.12);
}

.unknown-model-box {
  background: var(--bg-subtle);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-md);
  padding: 1rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
}

.unknown-model-box p {
  font-size: 0.8125rem;
  color: var(--charcoal-600);
}

/* Issue Selection Grid */
.issue-selection-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
}

.issue-card-btn {
  background: var(--bg-card);
  border: 2px solid var(--border-card);
  border-radius: var(--radius-md);
  padding: 1.25rem;
  display: flex;
  flex-direction: column;
  gap: 0.65rem;
  text-align: left;
  transition: all var(--transition-fast);
}

.issue-card-btn:hover {
  border-color: var(--forest-600);
  background: var(--bg-subtle);
}

.issue-card-btn.selected {
  border-color: var(--forest-800);
  background: var(--forest-100);
  box-shadow: 0 0 0 2px var(--forest-800);
}

.issue-card-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.issue-icon {
  width: 2.25rem;
  height: 2.25rem;
  border-radius: var(--radius-sm);
  background: var(--bg-subtle);
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--forest-800);
}

.issue-card-btn.selected .issue-icon {
  background: var(--forest-800);
  color: var(--lime-400);
}

.issue-title {
  font-size: 1rem;
  font-weight: 700;
  color: var(--forest-900);
}

.issue-symptoms-list {
  font-size: 0.775rem;
  color: var(--charcoal-500);
  display: flex;
  flex-direction: column;
  gap: 0.2rem;
}

/* Context Questions */
.context-questions-wrap {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.question-block {
  background: var(--bg-subtle);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-md);
  padding: 1.25rem;
}

.q-label {
  font-size: 0.9375rem;
  font-weight: 700;
  color: var(--forest-900);
  margin-bottom: 0.75rem;
}

.choice-options-row {
  display: flex;
  flex-wrap: wrap;
  gap: 0.75rem;
}

.choice-pill {
  padding: 0.5rem 1.15rem;
  border-radius: var(--radius-full);
  border: 1px solid var(--border-card);
  background: #FFFFFF;
  font-size: 0.875rem;
  font-weight: 600;
  color: var(--charcoal-700);
  cursor: pointer;
  transition: all var(--transition-fast);
}

.choice-pill:hover {
  border-color: var(--forest-800);
}

.choice-pill.selected {
  background: var(--forest-800);
  color: #FFFFFF;
  border-color: var(--forest-800);
}

.checkbox-custom-item {
  display: flex;
  align-items: center;
  gap: 0.65rem;
  font-size: 0.875rem;
  font-weight: 600;
  color: var(--charcoal-700);
  cursor: pointer;
}

.checkbox-custom-item input[type="checkbox"] {
  width: 1.15rem;
  height: 1.15rem;
  accent-color: var(--forest-800);
  cursor: pointer;
}

/* Wizard Navigation Footer */
.checker-footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 2.25rem;
  padding-top: 1.5rem;
  border-top: 1px solid var(--border-subtle);
}

/* Loading Simulation Screen */
.diagnosis-loading-screen {
  text-align: center;
  padding: 3.5rem 1.5rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.25rem;
}

.loader-spinner {
  width: 3.5rem;
  height: 3.5rem;
  border: 4px solid var(--border-subtle);
  border-top-color: var(--forest-800);
  border-right-color: var(--lime-500);
  border-radius: 50%;
  animation: spin 0.9s cubic-bezier(0.68, -0.55, 0.27, 1.55) infinite;
}

@keyframes spin {
  to { transform: rotate(360deg); }
}

.loading-log {
  font-family: var(--font-mono);
  font-size: 0.8125rem;
  color: var(--forest-600);
  background: var(--bg-subtle);
  padding: 0.4rem 0.85rem;
  border-radius: var(--radius-sm);
  display: inline-block;
}

/* ==========================================================================
   DIAGNOSIS RESULTS CARD (Step 5 Output)
   ========================================================================== */

.diagnosis-result-wrap {
  display: flex;
  flex-direction: column;
  gap: 1.75rem;
}

.result-hero-banner {
  background: var(--forest-900);
  border-radius: var(--radius-lg);
  color: #FFFFFF;
  padding: 2rem;
  position: relative;
  overflow: hidden;
}

.result-hero-banner::after {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  width: 200px;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(194, 250, 43, 0.08));
  pointer-events: none;
}

.result-banner-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 1rem;
  margin-bottom: 1.25rem;
}

.estimate-notice {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  color: var(--lime-400);
  background: rgba(255, 255, 255, 0.08);
  padding: 0.25rem 0.65rem;
  border-radius: var(--radius-sm);
  letter-spacing: 0.04em;
}

.result-device-title {
  font-size: 1.75rem;
  font-weight: 800;
  letter-spacing: -0.02em;
  color: #FFFFFF;
}

.result-summary-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1rem;
  margin-top: 1.5rem;
}

.result-metric-card {
  background: var(--bg-dark-card);
  border: 1px solid var(--border-dark);
  border-radius: var(--radius-md);
  padding: 1rem;
}

.metric-lbl {
  font-family: var(--font-mono);
  font-size: 0.6875rem;
  text-transform: uppercase;
  color: var(--charcoal-200);
  letter-spacing: 0.04em;
  margin-bottom: 0.35rem;
}

.metric-val-main {
  font-size: 1.35rem;
  font-weight: 800;
  color: #FFFFFF;
}

.metric-val-main.lime {
  color: var(--lime-400);
}

.metric-sub {
  font-size: 0.75rem;
  color: var(--charcoal-200);
  margin-top: 0.15rem;
}

/* Safety guidance banner */
.safety-alert-box {
  background: var(--alert-amber-bg);
  border: 2px solid var(--alert-amber-border);
  border-radius: var(--radius-md);
  padding: 1.25rem 1.5rem;
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  color: var(--alert-amber-text);
}

.safety-alert-box.danger {
  background: var(--alert-red-bg);
  border-color: var(--alert-red-border);
  color: var(--alert-red-text);
}

.safety-alert-icon {
  flex-shrink: 0;
  margin-top: 0.15rem;
}

.safety-alert-title {
  font-size: 1rem;
  font-weight: 800;
  margin-bottom: 0.35rem;
}

.safety-alert-text {
  font-size: 0.875rem;
  line-height: 1.5;
}

/* Compare Repair vs Replacement interactive section */
.compare-container {
  background: var(--bg-card);
  border: 1px solid var(--border-card);
  border-radius: var(--radius-lg);
  padding: 1.75rem;
}

.compare-heading {
  font-size: 1.2rem;
  font-weight: 800;
  color: var(--forest-900);
  margin-bottom: 1.25rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.compare-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.5rem;
}

.compare-column {
  border-radius: var(--radius-md);
  padding: 1.5rem;
}

.compare-column.repair {
  background: var(--forest-100);
  border: 1px solid var(--forest-300);
}

.compare-column.replace {
  background: var(--bg-subtle);
  border: 1px solid var(--border-card);
}

.col-tag {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  font-weight: 800;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  margin-bottom: 0.75rem;
}

.compare-column.repair .col-tag {
  color: var(--forest-700);
}

.compare-column.replace .col-tag {
  color: var(--charcoal-600);
}

.col-price {
  font-size: 2rem;
  font-weight: 800;
  color: var(--forest-900);
  line-height: 1.1;
  margin-bottom: 0.25rem;
}

.col-desc {
  font-size: 0.8125rem;
  color: var(--charcoal-600);
  margin-bottom: 1.25rem;
}

.compare-benefits-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 0.65rem;
  font-size: 0.875rem;
}

.compare-benefits-list li {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

/* Parts & Tools Checklist Box */
.parts-tools-panel {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.5rem;
  background: var(--bg-subtle);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-md);
  padding: 1.5rem;
}

.panel-block-title {
  font-size: 0.9375rem;
  font-weight: 800;
  color: var(--forest-900);
  margin-bottom: 0.75rem;
  display: flex;
  align-items: center;
  gap: 0.45rem;
}

.checklist-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 0.45rem;
  font-size: 0.875rem;
}

.checklist-item {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  color: var(--charcoal-700);
}

.checklist-item input[type="checkbox"] {
  accent-color: var(--forest-800);
}

/* Results Action Buttons */
.result-actions-bar {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  padding-top: 1rem;
  border-top: 1px solid var(--border-subtle);
}

/* ==========================================================================
   REPAIR LIBRARY
   ========================================================================== */

.filter-controls-card {
  background: var(--bg-card);
  border: 1px solid var(--border-card);
  border-radius: var(--radius-lg);
  padding: 1.5rem;
  margin-bottom: 2rem;
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
}

.search-input-wrap {
  position: relative;
  width: 100%;
}

.search-input-wrap svg {
  position: absolute;
  left: 1.15rem;
  top: 50%;
  transform: translateY(-50%);
  color: var(--charcoal-400);
}

.search-input-wrap input {
  width: 100%;
  padding: 0.85rem 1rem 0.85rem 2.85rem;
  border: 1px solid var(--border-card);
  border-radius: var(--radius-md);
  background: #FFFFFF;
  font-size: 0.9375rem;
  color: var(--charcoal-800);
}

.search-input-wrap input:focus {
  border-color: var(--forest-800);
  box-shadow: 0 0 0 3px rgba(20, 56, 35, 0.1);
}

.filters-row {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
}

.filter-pills-group {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.filter-pill {
  padding: 0.45rem 0.95rem;
  border-radius: var(--radius-full);
  border: 1px solid var(--border-card);
  background: var(--bg-subtle);
  font-size: 0.8125rem;
  font-weight: 700;
  color: var(--charcoal-600);
  cursor: pointer;
  transition: all var(--transition-fast);
}

.filter-pill:hover {
  background: #FFFFFF;
  color: var(--forest-900);
}

.filter-pill.active {
  background: var(--forest-800);
  color: #FFFFFF;
  border-color: var(--forest-800);
}

.filter-select-wrap {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 0.8125rem;
  font-weight: 700;
  color: var(--charcoal-600);
}

.filter-select {
  padding: 0.45rem 0.85rem;
  border: 1px solid var(--border-card);
  border-radius: var(--radius-sm);
  background: #FFFFFF;
  font-size: 0.8125rem;
  font-weight: 600;
  color: var(--forest-900);
}

/* Guide Cards Grid */
.guides-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
}

.guide-card {
  background: var(--bg-card);
  border: 1px solid var(--border-card);
  border-radius: var(--radius-lg);
  padding: 1.75rem;
  display: flex;
  flex-direction: column;
  box-shadow: var(--shadow-card);
  transition: all var(--transition-normal);
  cursor: pointer;
}

.guide-card:hover {
  transform: translateY(-4px);
  border-color: var(--forest-600);
  box-shadow: 0 8px 0 var(--border-card);
}

.guide-top-meta {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 1rem;
}

.difficulty-badge {
  font-family: var(--font-mono);
  font-size: 0.6875rem;
  font-weight: 800;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  padding: 0.2rem 0.55rem;
  border-radius: var(--radius-sm);
}

.difficulty-badge.Novice {
  background: #DEF7EC;
  color: #03543F;
}

.difficulty-badge.Moderate {
  background: #FEF08A;
  color: #713F12;
}

.difficulty-badge.Advanced {
  background: #FEE2E2;
  color: #991B1B;
}

.guide-time-pill {
  font-size: 0.75rem;
  color: var(--charcoal-500);
  display: flex;
  align-items: center;
  gap: 0.35rem;
}

.guide-title {
  font-size: 1.15rem;
  font-weight: 800;
  color: var(--forest-900);
  letter-spacing: -0.02em;
  line-height: 1.3;
  margin-bottom: 0.5rem;
}

.guide-device-name {
  font-size: 0.8125rem;
  font-weight: 700;
  color: var(--forest-600);
  margin-bottom: 1rem;
}

.guide-tags-row {
  display: flex;
  flex-wrap: wrap;
  gap: 0.4rem;
  margin-bottom: 1.25rem;
}

.guide-tool-tag {
  font-size: 0.725rem;
  background: var(--bg-subtle);
  color: var(--charcoal-600);
  padding: 0.2rem 0.5rem;
  border-radius: var(--radius-sm);
}

.guide-card-footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-top: 1rem;
  border-top: 1px solid var(--border-subtle);
  margin-top: auto;
}

.cost-savings-snippet {
  font-size: 0.75rem;
  color: var(--charcoal-600);
}

.cost-savings-snippet strong {
  color: var(--forest-800);
  font-weight: 800;
}

/* ==========================================================================
   REPAIR NETWORK DIRECTORY
   ========================================================================== */

.directory-layout {
  display: grid;
  grid-template-columns: 1.6fr 1.4fr;
  gap: 2rem;
}

.repairers-list-wrap {
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
}

.repairer-card {
  background: var(--bg-card);
  border: 1px solid var(--border-card);
  border-radius: var(--radius-lg);
  padding: 1.75rem;
  box-shadow: var(--shadow-sm);
  transition: all var(--transition-normal);
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.repairer-card:hover {
  border-color: var(--forest-600);
  box-shadow: var(--shadow-md);
}

.repairer-head {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: 1rem;
}

.repairer-name {
  font-size: 1.2rem;
  font-weight: 800;
  color: var(--forest-900);
  letter-spacing: -0.02em;
}

.repairer-meta-line {
  font-size: 0.8125rem;
  color: var(--charcoal-500);
  display: flex;
  align-items: center;
  gap: 0.75rem;
  margin-top: 0.25rem;
}

.rating-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.25rem;
  font-weight: 700;
  color: #B45309;
}

.repairer-badges-row {
  display: flex;
  flex-wrap: wrap;
  gap: 0.45rem;
}

.rep-badge {
  font-family: var(--font-mono);
  font-size: 0.6875rem;
  font-weight: 700;
  padding: 0.2rem 0.55rem;
  border-radius: var(--radius-sm);
  background: var(--forest-100);
  color: var(--forest-800);
}

.repairer-desc {
  font-size: 0.875rem;
  color: var(--charcoal-600);
  line-height: 1.5;
}

.repairer-pricing-table {
  background: var(--bg-subtle);
  border-radius: var(--radius-sm);
  padding: 0.75rem 1rem;
  font-size: 0.8125rem;
}

.pricing-row {
  display: flex;
  justify-content: space-between;
  padding: 0.25rem 0;
  border-bottom: 1px dashed var(--border-card);
}

.pricing-row:last-child {
  border-bottom: none;
}

.repairer-actions {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  padding-top: 0.75rem;
  border-top: 1px solid var(--border-subtle);
}

/* Simulated Map / Interactive Radar */
.directory-sidebar-card {
  background: var(--forest-900);
  border-radius: var(--radius-xl);
  border: 1px solid var(--border-dark);
  color: #FFFFFF;
  padding: 2rem;
  position: sticky;
  top: 6rem;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.radar-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.radar-title {
  font-size: 1.15rem;
  font-weight: 800;
  color: #FFFFFF;
}

.simulated-map-frame {
  height: 240px;
  background: var(--bg-dark-card);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: var(--radius-md);
  position: relative;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}

.map-grid-pattern {
  position: absolute;
  inset: 0;
  background-image: 
    linear-gradient(rgba(200, 255, 50, 0.08) 1px, transparent 1px),
    linear-gradient(90deg, rgba(200, 255, 50, 0.08) 1px, transparent 1px);
  background-size: 24px 24px;
}

.radar-pin {
  position: absolute;
  width: 14px;
  height: 14px;
  border-radius: 50%;
  background: var(--lime-400);
  box-shadow: 0 0 10px var(--lime-400);
  cursor: pointer;
  transition: transform var(--transition-fast);
}

.radar-pin:hover {
  transform: scale(1.4);
}

.radar-pin::after {
  content: '';
  position: absolute;
  inset: -6px;
  border: 1px solid var(--lime-400);
  border-radius: 50%;
  animation: pulsePin 2s infinite;
}

@keyframes pulsePin {
  0% { transform: scale(0.8); opacity: 1; }
  100% { transform: scale(2.2); opacity: 0; }
}

.radar-stats-box {
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: var(--radius-md);
  padding: 1.25rem;
  font-size: 0.8125rem;
  color: var(--charcoal-200);
  line-height: 1.6;
}

/* ==========================================================================
   GIVE A DEVICE A SECOND LIFE (Pathways, Erasure, Checklist)
   ========================================================================== */

.secondlife-pathways-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1.25rem;
  margin-bottom: 3.5rem;
}

.pathway-card {
  background: var(--bg-card);
  border: 1px solid var(--border-card);
  border-radius: var(--radius-lg);
  padding: 1.75rem 1.4rem;
  display: flex;
  flex-direction: column;
  box-shadow: var(--shadow-card);
  transition: all var(--transition-normal);
}

.pathway-card:hover {
  transform: translateY(-4px);
  border-color: var(--forest-600);
  box-shadow: 0 8px 0 var(--border-card);
}

.pathway-icon {
  width: 2.75rem;
  height: 2.75rem;
  border-radius: var(--radius-md);
  background: var(--forest-100);
  color: var(--forest-800);
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.25rem;
}

.pathway-title {
  font-size: 1.2rem;
  font-weight: 800;
  color: var(--forest-900);
  letter-spacing: -0.02em;
  margin-bottom: 0.35rem;
}

.pathway-tagline {
  font-size: 0.8125rem;
  font-weight: 700;
  color: var(--forest-600);
  margin-bottom: 0.85rem;
}

.pathway-desc {
  font-size: 0.875rem;
  color: var(--charcoal-600);
  line-height: 1.5;
  margin-bottom: 1.25rem;
  flex-grow: 1;
}

.pathway-benefit-box {
  background: var(--bg-subtle);
  border-radius: var(--radius-sm);
  padding: 0.75rem;
  font-size: 0.75rem;
  color: var(--charcoal-700);
}

/* Secure Erasure Tabs Card */
.erasure-card {
  background: var(--bg-card);
  border: 1px solid var(--border-card);
  border-radius: var(--radius-xl);
  overflow: hidden;
  box-shadow: var(--shadow-md);
  margin-bottom: 3.5rem;
}

.erasure-header {
  background: var(--forest-900);
  color: #FFFFFF;
  padding: 2rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 1rem;
}

.os-tab-buttons {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.os-tab-btn {
  padding: 0.5rem 1rem;
  border-radius: var(--radius-full);
  font-size: 0.8125rem;
  font-weight: 700;
  color: var(--charcoal-200);
  background: rgba(255, 255, 255, 0.08);
  transition: all var(--transition-fast);
}

.os-tab-btn:hover {
  background: rgba(255, 255, 255, 0.16);
  color: #FFFFFF;
}

.os-tab-btn.active {
  background: var(--lime-400);
  color: var(--forest-900);
}

.erasure-body {
  padding: 2rem;
}

.steps-ordered-list {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.ordered-step-item {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
}

.step-circle-num {
  width: 2rem;
  height: 2rem;
  border-radius: 50%;
  background: var(--forest-800);
  color: #FFFFFF;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: var(--font-mono);
  font-size: 0.8125rem;
  font-weight: 700;
  flex-shrink: 0;
}

.step-instruction-text {
  font-size: 0.9375rem;
  color: var(--charcoal-700);
  line-height: 1.55;
  padding-top: 0.15rem;
}

/* Handoff Interactive Checklist */
.checklist-card {
  background: var(--bg-card);
  border: 1px solid var(--border-card);
  border-radius: var(--radius-xl);
  padding: 2.25rem;
  box-shadow: var(--shadow-card);
}

.checklist-header-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 1.5rem;
}

.progress-track {
  width: 100%;
  height: 8px;
  background: var(--bg-subtle);
  border-radius: var(--radius-full);
  overflow: hidden;
  margin-bottom: 1.5rem;
}

.progress-fill {
  height: 100%;
  background: var(--lime-500);
  width: 0%;
  transition: width 0.35s ease;
}

.interactive-checklist-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}

.checklist-interactive-item {
  display: flex;
  align-items: flex-start;
  gap: 0.75rem;
  padding: 0.85rem 1rem;
  background: var(--bg-subtle);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-md);
  cursor: pointer;
  transition: all var(--transition-fast);
}

.checklist-interactive-item:hover {
  background: #FFFFFF;
  border-color: var(--forest-600);
}

.checklist-interactive-item.checked {
  background: var(--forest-100);
  border-color: var(--forest-300);
}

.checklist-interactive-item.checked span {
  text-decoration: line-through;
  color: var(--forest-700);
}

/* ==========================================================================
   IMPACT & JUDGE-READY STORYTELLING
   ========================================================================== */

.judge-banner-card {
  background: var(--forest-900);
  border: 2px solid var(--lime-400);
  border-radius: var(--radius-xl);
  padding: 2.5rem;
  color: #FFFFFF;
  margin-bottom: 3.5rem;
  position: relative;
  overflow: hidden;
}

.judge-tag {
  font-family: var(--font-mono);
  font-size: 0.8125rem;
  font-weight: 800;
  color: var(--forest-900);
  background: var(--lime-400);
  padding: 0.3rem 0.75rem;
  border-radius: var(--radius-sm);
  display: inline-block;
  margin-bottom: 1rem;
  letter-spacing: 0.05em;
}

.judge-grid-five-pillars {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 1rem;
  margin-top: 2rem;
}

.pillar-box {
  background: rgba(255, 255, 255, 0.06);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: var(--radius-md);
  padding: 1.15rem;
}

.pillar-name {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  color: var(--lime-400);
  text-transform: uppercase;
  margin-bottom: 0.35rem;
}

.pillar-heading {
  font-size: 1rem;
  font-weight: 700;
  color: #FFFFFF;
  margin-bottom: 0.35rem;
}

.pillar-text {
  font-size: 0.775rem;
  color: var(--charcoal-200);
  line-height: 1.45;
}

/* Interactive Impact Simulator */
.simulator-card {
  background: var(--bg-card);
  border: 1px solid var(--border-card);
  border-radius: var(--radius-xl);
  padding: 2.5rem;
  box-shadow: var(--shadow-card);
  margin-bottom: 3.5rem;
}

.slider-group {
  margin-bottom: 2rem;
}

.slider-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 0.65rem;
}

.slider-label {
  font-weight: 700;
  color: var(--forest-900);
  font-size: 0.9375rem;
}

.slider-value-badge {
  font-family: var(--font-mono);
  font-size: 1.15rem;
  font-weight: 800;
  color: var(--forest-800);
  background: var(--forest-100);
  padding: 0.25rem 0.65rem;
  border-radius: var(--radius-sm);
}

.range-slider {
  width: 100%;
  height: 8px;
  background: var(--border-subtle);
  border-radius: var(--radius-full);
  outline: none;
  -webkit-appearance: none;
  cursor: pointer;
}

.range-slider::-webkit-slider-thumb {
  -webkit-appearance: none;
  width: 24px;
  height: 24px;
  border-radius: 50%;
  background: var(--forest-800);
  border: 3px solid var(--lime-400);
  cursor: pointer;
  box-shadow: var(--shadow-sm);
  transition: transform var(--transition-fast);
}

.range-slider::-webkit-slider-thumb:hover {
  transform: scale(1.15);
}

.simulator-results-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1.25rem;
  padding-top: 1.75rem;
  border-top: 1px solid var(--border-subtle);
}

.sim-metric-card {
  background: var(--bg-subtle);
  border: 1px solid var(--border-card);
  border-radius: var(--radius-md);
  padding: 1.25rem;
  text-align: center;
}

.sim-metric-num {
  font-family: var(--font-mono);
  font-size: 1.85rem;
  font-weight: 800;
  color: var(--forest-900);
  line-height: 1.1;
  margin-bottom: 0.35rem;
}

.sim-metric-label {
  font-size: 0.8125rem;
  color: var(--charcoal-600);
  font-weight: 600;
}

/* Roadmap / Pilot Plan Timeline */
.timeline-list {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.timeline-phase-card {
  background: var(--bg-card);
  border: 1px solid var(--border-card);
  border-left: 5px solid var(--forest-800);
  border-radius: 0 var(--radius-lg) var(--radius-lg) 0;
  padding: 1.75rem;
  box-shadow: var(--shadow-sm);
}

.phase-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 0.5rem;
}

.phase-name {
  font-family: var(--font-mono);
  font-size: 0.8125rem;
  font-weight: 800;
  color: var(--forest-600);
}

.phase-milestone {
  font-size: 1.25rem;
  font-weight: 800;
  color: var(--forest-900);
  margin-bottom: 0.85rem;
}

.phase-bullets {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  font-size: 0.875rem;
  color: var(--charcoal-600);
}

.phase-bullets li {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.phase-bullets li::before {
  content: 'â–¸';
  color: var(--forest-600);
  font-weight: bold;
}

/* ==========================================================================
   MODALS (Guide Viewer, Quote Request, List Repairer)
   ========================================================================== */

.modal-backdrop {
  position: fixed;
  inset: 0;
  background: rgba(13, 36, 22, 0.7);
  backdrop-filter: blur(6px);
  -webkit-backdrop-filter: blur(6px);
  z-index: 999;
  display: none;
  align-items: center;
  justify-content: center;
  padding: 1.5rem;
  opacity: 0;
  transition: opacity 0.25s ease;
}

.modal-backdrop.open {
  display: flex;
  opacity: 1;
}

.modal-window {
  background: var(--bg-card);
  border: 1px solid var(--border-card);
  border-radius: var(--radius-xl);
  width: 100%;
  max-width: 820px;
  max-height: 90vh;
  overflow-y: auto;
  box-shadow: var(--shadow-lg);
  position: relative;
  transform: translateY(20px);
  transition: transform 0.3s cubic-bezier(0.16, 1, 0.3, 1);
}

.modal-backdrop.open .modal-window {
  transform: translateY(0);
}

.modal-header {
  padding: 1.75rem 2rem;
  border-bottom: 1px solid var(--border-subtle);
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: sticky;
  top: 0;
  background: var(--bg-card);
  z-index: 10;
}

.modal-title {
  font-size: 1.35rem;
  font-weight: 800;
  color: var(--forest-900);
}

.modal-close-btn {
  width: 2.25rem;
  height: 2.25rem;
  border-radius: 50%;
  background: var(--bg-subtle);
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--charcoal-600);
  transition: all var(--transition-fast);
}

.modal-close-btn:hover {
  background: var(--charcoal-200);
  color: var(--charcoal-900);
}

.modal-body {
  padding: 2rem;
  display: flex;
  flex-direction: column;
  gap: 1.75rem;
}

/* Toast Notifications */
.toast-container {
  position: fixed;
  bottom: 2rem;
  right: 2rem;
  z-index: 9999;
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
  pointer-events: none;
}

.toast {
  background: var(--forest-900);
  border: 1px solid var(--border-dark);
  color: #FFFFFF;
  padding: 1rem 1.4rem;
  border-radius: var(--radius-md);
  box-shadow: var(--shadow-lg);
  font-size: 0.875rem;
  font-weight: 600;
  display: flex;
  align-items: center;
  gap: 0.75rem;
  transform: translateY(12px);
  opacity: 0;
  transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
  pointer-events: auto;
}

.toast.show {
  transform: translateY(0);
  opacity: 1;
}

.toast.success {
  border-left: 4px solid var(--lime-400);
}

.toast.alert {
  border-left: 4px solid #FF5733;
}

/* ==========================================================================
   FOOTER
   ========================================================================== */

.site-footer {
  background: var(--forest-900);
  color: var(--charcoal-200);
  padding: 4.5rem 0 2.5rem;
  margin-top: auto;
  border-top: 1px solid var(--border-dark);
}

.footer-grid {
  display: grid;
  grid-template-columns: 1.6fr repeat(3, 1fr);
  gap: 3rem;
  margin-bottom: 3.5rem;
}

.footer-brand-col {
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
}

.footer-brand-title {
  font-size: 1.5rem;
  font-weight: 800;
  color: #FFFFFF;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.footer-mission {
  font-size: 0.875rem;
  color: var(--charcoal-200);
  line-height: 1.6;
  max-width: 380px;
}

.footer-nav-col {
  display: flex;
  flex-direction: column;
  gap: 0.85rem;
}

.footer-heading {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  font-weight: 800;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  color: var(--lime-400);
  margin-bottom: 0.25rem;
}

.footer-nav-col a {
  font-size: 0.875rem;
  color: var(--charcoal-200);
  transition: color var(--transition-fast);
}

.footer-nav-col a:hover {
  color: #FFFFFF;
}

.footer-bottom {
  border-top: 1px solid var(--border-dark);
  padding-top: 2rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 1rem;
  font-size: 0.8125rem;
  color: var(--charcoal-400);
}

.challenge-attribution {
  font-family: var(--font-mono);
  color: var(--lime-400);
  font-size: 0.75rem;
}

/* ==========================================================================
   RESPONSIVE DESIGN (TABLETS & MOBILE)
   ========================================================================== */

@media (max-width: 1024px) {
  .hero-grid {
    grid-template-columns: 1fr;
    gap: 2.5rem;
  }
  .journey-timeline {
    grid-template-columns: 1fr 1fr;
  }
  .featured-grid {
    grid-template-columns: 1fr 1fr;
  }
  .guides-grid {
    grid-template-columns: 1fr 1fr;
  }
  .directory-layout {
    grid-template-columns: 1fr;
  }
  .secondlife-pathways-grid {
    grid-template-columns: 1fr 1fr;
  }
  .judge-grid-five-pillars {
    grid-template-columns: 1fr 1fr;
  }
  .simulator-results-grid {
    grid-template-columns: 1fr 1fr;
  }
  .footer-grid {
    grid-template-columns: 1fr 1fr;
  }
}

@media (max-width: 768px) {
  .top-bar {
    display: none;
  }
  .main-nav, .header-cta-group {
    display: none;
  }
  .mobile-toggle {
    display: block;
  }
  .mobile-menu-drawer {
    position: fixed;
    top: 4.75rem;
    left: 0;
    right: 0;
    bottom: 0;
    background: var(--bg-warm);
    z-index: 85;
    padding: 1.5rem;
    display: none;
    flex-direction: column;
    gap: 1rem;
    overflow-y: auto;
  }
  .mobile-menu-drawer.open {
    display: flex;
  }
  .mobile-menu-drawer .nav-link {
    font-size: 1.15rem;
    padding: 0.85rem 1rem;
    border-bottom: 1px solid var(--border-subtle);
  }
  .category-selection-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  .issue-selection-grid {
    grid-template-columns: 1fr;
  }
  .checker-steps-bar {
    grid-template-columns: 1fr;
  }
  .result-summary-grid {
    grid-template-columns: 1fr 1fr;
  }
  .compare-grid {
    grid-template-columns: 1fr;
  }
  .parts-tools-panel {
    grid-template-columns: 1fr;
  }
  .interactive-checklist-grid {
    grid-template-columns: 1fr;
  }
  .problem-solution-grid {
    grid-template-columns: 1fr;
  }
  .featured-grid, .guides-grid {
    grid-template-columns: 1fr;
  }
  .secondlife-pathways-grid {
    grid-template-columns: 1fr;
  }
  .trust-principles-grid {
    grid-template-columns: 1fr;
  }
  .footer-grid {
    grid-template-columns: 1fr;
  }
}

</style>
</head>
<body>

  <!-- ==========================================================================
       TOP STATUS BAR â€” HACKATHON CHALLENGE BRIEF
       ========================================================================== -->
  <aside class="top-bar">
    <div class="container top-bar-inner">
      <div class="challenge-tag">
        <span class="pulse-dot"></span>
        <span>HACKATHON CHALLENGE: IMX26-PS07 â€” CEDA-EPS</span>
        <span style="opacity:0.6;">|</span>
        <span>DESIGN ELECTRONICS FOR REPAIR, REUSE & RECOVERY</span>
      </div>
      <div class="top-bar-links">
        <a href="#impact" class="route-trigger" data-route="impact">Judges Brief & Pilot Roadmap</a>
        <span style="opacity:0.3;">â€¢</span>
        <a href="#checker" class="route-trigger" data-route="checker">Launch Core Demo</a>
        <span style="opacity:0.3;">â€¢</span>
        <span style="font-family:var(--font-mono); font-size:0.75rem; color:var(--lime-400);">PROTOTYPE V1.0</span>
      </div>
    </div>
  </aside>

  <!-- ==========================================================================
       PRIMARY HEADER & NAVIGATION
       ========================================================================== -->
  <header class="site-header">
    <div class="container header-inner">
      <a href="#home" class="brand-link route-trigger" data-route="home">
        <div class="brand-icon">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
            <path d="M21 12a9 9 0 0 0-9-9 9.75 9.75 0 0 0-6.74 2.74L3 8"/>
            <path d="M3 3v5h5"/>
            <path d="M3 12a9 9 0 0 0 9 9 9.75 9.75 0 0 0 6.74-2.74L21 16"/>
            <path d="M21 21v-5h-5"/>
          </svg>
        </div>
        <div class="brand-meta">
          <div class="brand-title">
            CIRCULAR
            <span class="badge-beta">DEMO</span>
          </div>
          <div class="brand-sub">Electronics Life Extension Platform</div>
        </div>
      </a>

      <nav class="main-nav" aria-label="Main Navigation">
        <a href="#home" class="nav-link active" data-route="home">Overview</a>
        <a href="#checker" class="nav-link" data-route="checker">Device Checker</a>
        <a href="#guides" class="nav-link" data-route="guides">Repair Library</a>
        <a href="#network" class="nav-link" data-route="network">Repair Network</a>
        <a href="#second-life" class="nav-link" data-route="second-life">Second Life</a>
        <a href="#impact" class="nav-link" data-route="impact">Impact & Deck</a>
      </nav>

      <div class="header-cta-group">
        <a href="#checker" class="btn btn-lime btn-sm route-trigger" data-route="checker">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
            <circle cx="12" cy="12" r="10"/><path d="m10 15 5-3-5-3v6Z"/>
          </svg>
          Check My Device
        </a>
        <button type="button" class="mobile-toggle" id="mobileMenuToggle" aria-label="Toggle mobile menu">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
            <line x1="4" y1="6" x2="20" y2="6"/><line x1="4" y1="12" x2="20" y2="12"/><line x1="4" y1="18" x2="20" y2="18"/>
          </svg>
        </button>
      </div>
    </div>
  </header>

  <!-- Mobile Drawer Menu -->
  <div class="mobile-menu-drawer" id="mobileMenuDrawer">
    <a href="#home" class="nav-link route-trigger" data-route="home">Overview</a>
    <a href="#checker" class="nav-link route-trigger" data-route="checker">Device Checker (Core Demo)</a>
    <a href="#guides" class="nav-link route-trigger" data-route="guides">Repair Library</a>
    <a href="#network" class="nav-link route-trigger" data-route="network">Repair Network</a>
    <a href="#second-life" class="nav-link route-trigger" data-route="second-life">Give a Device a Second Life</a>
    <a href="#impact" class="nav-link route-trigger" data-route="impact">Impact & Judge Deck</a>
    <div style="margin-top:1rem; padding-top:1rem; border-top:1px solid var(--border-subtle);">
      <a href="#checker" class="btn btn-lime route-trigger" style="width:100%;" data-route="checker">Check My Device</a>
    </div>
  </div>

  <main>
    <!-- ==========================================================================
         1. HERO SECTION (HOME)
         ========================================================================== -->
    <section id="home" class="hero-section">
      <div class="container hero-grid">
        <div class="hero-copy">
          <div class="hero-pill-badge">
            <span class="indicator-pill">CIRCULAR v1.0</span>
            <span>Right-to-Repair & Circular Economy Platform</span>
          </div>

          <h1 class="hero-headline">
            The best device is the one you <span class="highlight-lime">donâ€™t have to replace.</span>
          </h1>

          <p class="hero-subhead">
            Keep electronics in active service longer through transparent repair diagnostics, open parts guidance, verified local technicians, and certified end-of-life recovery.
          </p>

          <div class="hero-actions">
            <a href="#checker" class="btn btn-lime btn-lg route-trigger" data-route="checker">
              Check My Device
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
            </a>
            <a href="#circular-journey" class="btn btn-secondary btn-lg">
              Explore How It Works
            </a>
          </div>

          <div class="hero-trust-bullets">
            <div class="trust-item">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
              <span>Zero referral markups</span>
            </div>
            <div class="trust-item">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
              <span>Open repairability rubric</span>
            </div>
            <div class="trust-item">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
              <span>R2v3 / e-Stewards certified recovery</span>
            </div>
          </div>
        </div>

        <!-- Telemetry Diagnostic Schematic Visual Card -->
        <div class="hero-visual-card">
          <div class="telemetry-header">
            <div class="telemetry-status">
              <span class="pulse-dot"></span>
              <span>LIVE DIAGNOSTIC TELEMETRY</span>
            </div>
            <span class="telemetry-chip">MODEL: OPEN-HARDWARE-TREE</span>
          </div>

          <!-- Device schematic graphic (SVG Exploded View) -->
          <div class="schematic-frame">
            <svg class="schematic-svg" viewBox="0 0 420 190" fill="none" xmlns="http://www.w3.org/2000/svg">
              <!-- Exploded Phone Layers -->
              <rect x="25" y="25" width="100" height="140" rx="10" stroke="rgba(255,255,255,0.4)" stroke-width="1.5" stroke-dasharray="3 3"/>
              <text x="32" y="42" fill="rgba(255,255,255,0.6)" font-family="monospace" font-size="9">OLED LAYER [6.1"]</text>
              <line x1="125" y1="95" x2="160" y2="95" stroke="var(--lime-400)" stroke-width="1.5"/>
              <circle cx="160" cy="95" r="3" fill="var(--lime-400)"/>

              <!-- Battery Module -->
              <rect x="170" y="35" width="105" height="120" rx="6" fill="rgba(194, 250, 43, 0.12)" stroke="var(--lime-400)" stroke-width="2"/>
              <text x="180" y="55" fill="var(--lime-400)" font-family="monospace" font-size="9" font-weight="bold">LI-ION CELL [3227mAh]</text>
              <text x="180" y="70" fill="rgba(255,255,255,0.7)" font-family="monospace" font-size="8">Pull-Tab Adhesive: 2x</text>
              <text x="180" y="85" fill="rgba(255,255,255,0.7)" font-family="monospace" font-size="8">Health Index: 76% (Replace)</text>
              <rect x="180" y="100" width="85" height="6" rx="3" fill="rgba(255,255,255,0.2)"/>
              <rect x="180" y="100" width="62" height="6" rx="3" fill="var(--lime-400)"/>

              <!-- Motherboard & Sub-board -->
              <rect x="290" y="25" width="105" height="140" rx="8" fill="rgba(255,255,255,0.04)" stroke="rgba(255,255,255,0.3)" stroke-width="1.5"/>
              <text x="300" y="42" fill="rgba(255,255,255,0.6)" font-family="monospace" font-size="9">CHASSIS & LOGIC</text>
              <rect x="305" y="55" width="28" height="28" rx="4" stroke="rgba(200,255,50,0.6)" stroke-width="1.2"/>
              <text x="310" y="72" fill="var(--lime-400)" font-family="monospace" font-size="8">SoC</text>
              <rect x="305" y="125" width="45" height="18" rx="2" stroke="rgba(255,255,255,0.5)" stroke-width="1"/>
              <text x="310" y="138" fill="rgba(255,255,255,0.7)" font-family="monospace" font-size="7">USB-C PORT</text>
            </svg>

            <div class="schematic-callouts">
              <div class="callout-node">
                <div class="callout-title">REPAIRABILITY SCORE</div>
                <div class="callout-val">7.8 / 10 (Modular Sub-board)</div>
              </div>
              <div class="callout-node alert">
                <div class="callout-title">THERMAL LIFECYCLE</div>
                <div class="callout-val">Replace Battery (35 min DIY)</div>
              </div>
            </div>
          </div>

          <div class="telemetry-metrics-row">
            <div class="mini-stat-box">
              <div class="mini-stat-num">62.0 Mt</div>
              <div class="mini-stat-lbl">Annual Global E-Waste</div>
            </div>
            <div class="mini-stat-box">
              <div class="mini-stat-num">82%</div>
              <div class="mini-stat-lbl">Premature Discard Rate</div>
            </div>
            <div class="mini-stat-box">
              <div class="mini-stat-num">71.4%</div>
              <div class="mini-stat-lbl">Repairable Potential</div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ==========================================================================
         THE CIRCULAR JOURNEY: DIAGNOSE -> REPAIR -> REUSE -> RECOVER
         ========================================================================== -->
    <section id="circular-journey" class="section-padding" style="background-color: var(--bg-subtle);">
      <div class="container">
        <div class="section-header">
          <div class="section-label">THE CIRCULAR HIERARCHY</div>
          <h2 class="section-title">A clear path from broken to restored</h2>
          <p class="section-desc">
            Electronics should never follow a linear "take-make-waste" pipeline. CIRCULAR guides each device through an energy-first hierarchy where life extension is prioritized before material recovery.
          </p>
        </div>

        <div class="journey-timeline">
          <!-- Step 1: Diagnose -->
          <div class="journey-step-card active" onclick="document.querySelector('[data-route=checker]').click()">
            <div class="step-header">
              <span class="step-badge">STAGE 01</span>
              <div class="step-icon-wrap">
                <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>
              </div>
            </div>
            <div class="step-hierarchy">ASSESS FIRST</div>
            <div class="step-title">Diagnose</div>
            <p class="step-text">
              Interactive multi-step assessment of symptoms, hardware age, and battery health to estimate fault root-cause and repairability.
            </p>
            <div class="step-outcome-pill">
              <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
              <span>Repairability score + parts checklist</span>
            </div>
          </div>

          <!-- Step 2: Repair -->
          <div class="journey-step-card" onclick="document.querySelector('[data-route=guides]').click()">
            <div class="step-header">
              <span class="step-badge">STAGE 02</span>
              <div class="step-icon-wrap">
                <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M14.7 6.3a1 1 0 0 0 0 1.4l1.6 1.6a1 1 0 0 0 1.4 0l3.77-3.77a6 6 0 0 1-7.94 7.94l-6.91 6.91a2.12 2.12 0 0 1-3-3l6.91-6.91a6 6 0 0 1 7.94-7.94l-3.76 3.76z"/></svg>
              </div>
            </div>
            <div class="step-hierarchy">EXTEND USEFUL LIFE</div>
            <div class="step-title">Repair</div>
            <p class="step-text">
              Choose between transparent community DIY guides or vetted independent technicians who honor Right-to-Repair principles.
            </p>
            <div class="step-outcome-pill">
              <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
              <span>Saves ~80% embodied carbon</span>
            </div>
          </div>

          <!-- Step 3: Reuse -->
          <div class="journey-step-card" onclick="document.querySelector('[data-route=second-life]').click()">
            <div class="step-header">
              <span class="step-badge">STAGE 03</span>
              <div class="step-icon-wrap">
                <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M17 1l4 4-4 4"/><path d="M3 11V9a4 4 0 0 1 4-4h14"/><path d="M7 23l-4-4 4-4"/><path d="M21 13v2a4 4 0 0 1-4 4H3"/></svg>
              </div>
            </div>
            <div class="step-hierarchy">RE-CIRCULATE HARDWARE</div>
            <div class="step-title">Reuse & Repurpose</div>
            <p class="step-text">
              Securely wipe data using hardware cryptographic standards, then donate to digital inclusion programs or upcycle into utility nodes.
            </p>
            <div class="step-outcome-pill">
              <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
              <span>Zero-waste handoff checklist</span>
            </div>
          </div>

          <!-- Step 4: Recover -->
          <div class="journey-step-card" onclick="document.querySelector('[data-route=second-life]').click()">
            <div class="step-header">
              <span class="step-badge">STAGE 04</span>
              <div class="step-icon-wrap">
                <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M7 19H4.815a1.83 1.83 0 0 1-1.57-.881 1.785 1.785 0 0 1-.004-1.784L7.196 9.5"/><path d="M11 19h8.2a1.8 1.8 0 0 0 1.57-2.665L16.8 9.5"/><path d="m9 5 3-3 3 3"/></svg>
              </div>
            </div>
            <div class="step-hierarchy">RESPONSIBLE END-OF-LIFE</div>
            <div class="step-title">Recover</div>
            <p class="step-text">
              When hardware is non-repairable, route through R2v3 / e-Stewards certified recyclers to smelt and recover critical raw minerals safely.
            </p>
            <div class="step-outcome-pill">
              <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>
              <span>Gold, Cobalt & Copper closed loops</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ==========================================================================
         THE PROBLEM VS CIRCULAR'S SYSTEMIC ARCHITECTURE
         ========================================================================== -->
    <section class="section-padding">
      <div class="container">
        <div class="section-header">
          <div class="section-label">SYSTEMIC ANALYSIS</div>
          <h2 class="section-title">Why electronics fail prematurely</h2>
          <p class="section-desc">
            The electronics industry generates over 62 million metric tonnes of e-waste every year. The barrier to longevity is rarely physicsâ€”it is information asymmetry, locked parts, and repair intimidation.
          </p>
        </div>

        <div class="problem-solution-grid">
          <div class="problem-card">
            <span class="ps-badge">CURRENT LINEAR PARADIGM</span>
            <div class="ps-title">Planned Obsolescence & Fragmented Support</div>
            <ul class="ps-list">
              <li>
                <span class="ps-icon-cross">âœ•</span>
                <span><strong>Cryptographic parts serialization:</strong> Swapping a genuine camera or battery triggers software error banners or disables features.</span>
              </li>
              <li>
                <span class="ps-icon-cross">âœ•</span>
                <span><strong>Repair intimidation:</strong> Users assume a dead battery or loose charging port means the entire $1,000 device must be replaced.</span>
              </li>
              <li>
                <span class="ps-icon-cross">âœ•</span>
                <span><strong>Unregulated recycling claims:</strong> E-waste shipped overseas to informal dumpsites where acid baths cause toxic bioaccumulation.</span>
              </li>
              <li>
                <span class="ps-icon-cross">âœ•</span>
                <span><strong>Fear of data leakage:</strong> Millions of functional phones rot in drawers because owners don't know how to sanitize storage securely.</span>
              </li>
            </ul>
          </div>

          <div class="solution-card">
            <span class="ps-badge">THE CIRCULAR DIGITAL PLATFORM</span>
            <div class="ps-title">Open Diagnostics & Transparent Longevity</div>
            <ul class="ps-list">
              <li>
                <span class="ps-icon-check">âœ“</span>
                <span><strong>Open Repairability Scoring:</strong> Objective assessment of adhesive strength, modular sub-assemblies, and schematic availability.</span>
              </li>
              <li>
                <span class="ps-icon-check">âœ“</span>
                <span><strong>Bifurcated Pathways (DIY vs Pro):</strong> Clear triage that empowers novice DIYers while connecting complex micro-soldering to local shops.</span>
              </li>
              <li>
                <span class="ps-icon-check">âœ“</span>
                <span><strong>Audited Second Life Protocols:</strong> Cryptographic wipe procedures (NIST 800-88 compliant) and vetted donation partner routing.</span>
              </li>
              <li>
                <span class="ps-icon-check">âœ“</span>
                <span><strong>True Cost & LCA Transparency:</strong> Shows exact dollars and embodied carbon saved by repairing rather than replacing.</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- ==========================================================================
         SAMPLE IMPACT COHORT PANEL (HONEST DEMO DATA)
         ========================================================================== -->
    <section class="section-padding" style="background-color: var(--forest-900); color: #FFFFFF;">
      <div class="container">
        <div style="display:flex; justify-content:space-between; align-items:flex-end; flex-wrap:wrap; gap:1.5rem; margin-bottom:3rem;">
          <div>
            <div style="font-family:var(--font-mono); font-size:0.75rem; color:var(--lime-400); font-weight:800; text-transform:uppercase; letter-spacing:0.05em; margin-bottom:0.5rem;">
              SIMULATED PILOT COHORT METRICS
            </div>
            <h2 style="font-size:clamp(1.85rem, 3.5vw, 2.5rem); font-weight:800; letter-spacing:-0.03em; color:#FFFFFF;">
              Measurable outcomes from 3,420 assessed devices
            </h2>
            <p style="color:var(--charcoal-200); font-size:0.95rem; max-width:620px; margin-top:0.5rem;">
              Illustrative model simulating a 6-month university campus and municipal community pilot based on EPA WEEE and Fraunhofer Life Cycle Assessment (LCA) benchmarks.
            </p>
          </div>
          <div style="background:rgba(255,255,255,0.08); padding:0.6rem 1rem; border-radius:var(--radius-md); font-family:var(--font-mono); font-size:0.75rem; color:var(--lime-300);">
            NOTE: Illustrative Demo Data for Hackathon Evaluation
          </div>
        </div>

        <div style="display:grid; grid-template-columns:repeat(4, 1fr); gap:1.25rem;">
          <div style="background:var(--bg-dark-card); border:1px solid var(--border-dark); border-radius:var(--radius-lg); padding:1.75rem;">
            <div style="font-family:var(--font-mono); font-size:0.75rem; color:var(--charcoal-200); text-transform:uppercase; margin-bottom:0.5rem;">Diverted from Landfill</div>
            <div style="font-size:2.4rem; font-weight:800; color:var(--lime-400); font-family:var(--font-mono); line-height:1;">71.4%</div>
            <div style="font-size:0.8125rem; color:var(--charcoal-200); margin-top:0.5rem;">2,442 units repaired or re-homed</div>
          </div>

          <div style="background:var(--bg-dark-card); border:1px solid var(--border-dark); border-radius:var(--radius-lg); padding:1.75rem;">
            <div style="font-family:var(--font-mono); font-size:0.75rem; color:var(--charcoal-200); text-transform:uppercase; margin-bottom:0.5rem;">Embodied COâ‚‚e Avoided</div>
            <div style="font-size:2.4rem; font-weight:800; color:#FFFFFF; font-family:var(--font-mono); line-height:1;">194 t</div>
            <div style="font-size:0.8125rem; color:var(--charcoal-200); margin-top:0.5rem;">Equivalent to ~42 gas cars off road 1 yr</div>
          </div>

          <div style="background:var(--bg-dark-card); border:1px solid var(--border-dark); border-radius:var(--radius-lg); padding:1.75rem;">
            <div style="font-family:var(--font-mono); font-size:0.75rem; color:var(--charcoal-200); text-transform:uppercase; margin-bottom:0.5rem;">Critical Minerals Kept</div>
            <div style="font-size:2.4rem; font-weight:800; color:#FFFFFF; font-family:var(--font-mono); line-height:1;">83 kg</div>
            <div style="font-size:0.8125rem; color:var(--charcoal-200); margin-top:0.5rem;">Cobalt, Lithium & Precious Gold</div>
          </div>

          <div style="background:var(--bg-dark-card); border:1px solid var(--border-dark); border-radius:var(--radius-lg); padding:1.75rem;">
            <div style="font-family:var(--font-mono); font-size:0.75rem; color:var(--charcoal-200); text-transform:uppercase; margin-bottom:0.5rem;">Community Wealth Retained</div>
            <div style="font-size:2.4rem; font-weight:800; color:var(--lime-400); font-family:var(--font-mono); line-height:1;">$684k</div>
            <div style="font-size:0.8125rem; color:var(--charcoal-200); margin-top:0.5rem;">Kept in local pockets vs retail hardware</div>
          </div>
        </div>
      </div>
    </section>

    <!-- ==========================================================================
         FEATURED REPAIR STORIES / EXEMPLAR HARDWARE
         ========================================================================== -->
    <section class="section-padding">
      <div class="container">
        <div class="section-header">
          <div class="section-label">HARDWARE ARCHITECTURE</div>
          <h2 class="section-title">Exemplars in repairable design</h2>
          <p class="section-desc">
            Repairability is an intentional engineering choice. See how modularity directly influences the lifespan of popular consumer hardware.
          </p>
        </div>

        <div class="featured-grid">
          <!-- Card 1: Fairphone 4 -->
          <div class="featured-card">
            <div class="featured-visual">
              <span class="score-badge-floating">10 / 10 REPAIR SCORE</span>
              <svg width="120" height="90" viewBox="0 0 140 100" fill="none" stroke="var(--forest-800)" stroke-width="2">
                <rect x="25" y="10" width="90" height="80" rx="8" stroke-dasharray="2 2"/>
                <rect x="40" y="25" width="60" height="50" rx="4" fill="var(--lime-100)" stroke="var(--forest-800)"/>
                <text x="45" y="52" font-family="monospace" font-size="8" fill="var(--forest-900)">MODULAR CORE</text>
              </svg>
            </div>
            <div class="featured-body">
              <div class="featured-device">Fairphone 4</div>
              <div class="featured-tagline">
                Zero glue assembly with modular spare parts swappable using a single Phillips #00 screwdriver.
              </div>
              <div class="featured-stats-row">
                <span>DIY Battery Swap: <strong>3 mins</strong></span>
                <span>Spare Parts: <strong>100% Available</strong></span>
              </div>
            </div>
          </div>

          <!-- Card 2: ThinkPad T480 -->
          <div class="featured-card">
            <div class="featured-visual">
              <span class="score-badge-floating">9.2 / 10 REPAIR SCORE</span>
              <svg width="120" height="90" viewBox="0 0 140 100" fill="none" stroke="var(--forest-800)" stroke-width="2">
                <path d="M15 70h110v5a3 3 0 0 1-3 3H18a3 3 0 0 1-3-3v-5z"/>
                <rect x="25" y="15" width="90" height="55" rx="3"/>
                <line x1="50" y1="40" x2="90" y2="40" stroke="var(--lime-500)" stroke-width="2"/>
              </svg>
            </div>
            <div class="featured-body">
              <div class="featured-device">ThinkPad T480</div>
              <div class="featured-tagline">
                Dual swappable batteries (Bridge Battery system), dual SO-DIMM RAM slots, and snap-fit display bezel.
              </div>
              <div class="featured-stats-row">
                <span>Screen Swap: <strong>20 mins</strong></span>
                <span>Active Life: <strong>8+ years</strong></span>
              </div>
            </div>
          </div>

          <!-- Card 3: Framework 13 -->
          <div class="featured-card">
            <div class="featured-visual">
              <span class="score-badge-floating">10 / 10 REPAIR SCORE</span>
              <svg width="120" height="90" viewBox="0 0 140 100" fill="none" stroke="var(--forest-800)" stroke-width="2">
                <rect x="20" y="20" width="100" height="60" rx="4"/>
                <rect x="30" y="30" width="20" height="15" rx="2" fill="var(--lime-300)"/>
                <rect x="55" y="30" width="20" height="15" rx="2" fill="var(--lime-300)"/>
                <rect x="80" y="30" width="20" height="15" rx="2" fill="var(--lime-300)"/>
              </svg>
            </div>
            <div class="featured-body">
              <div class="featured-device">Framework Laptop 13</div>
              <div class="featured-tagline">
                Fully modular expansion cards (USB-C, HDMI, MicroSD) and upgradable mainboards with open-source schematics.
              </div>
              <div class="featured-stats-row">
                <span>Port Swap: <strong>Instant plug</strong></span>
                <span>Open Schematics: <strong>Yes</strong></span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ==========================================================================
         TRUST & INTEGRITY SECTION
         ========================================================================== -->
    <section class="section-padding" style="background-color: var(--bg-subtle);">
      <div class="container">
        <div class="section-header">
          <div class="section-label">TRANSPARENCY CHARTER</div>
          <h2 class="section-title">Built on verified recommendations</h2>
          <p class="section-desc">
            CIRCULAR is designed to be an objective utility for hardware owners, not a storefront or lead-generation broker.
          </p>
        </div>

        <div class="trust-principles-grid">
          <div class="principle-card">
            <div class="principle-icon">
              <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><circle cx="12" cy="12" r="10"/><path d="m10 15 5-3-5-3v6Z"/></svg>
            </div>
            <div class="principle-title">Zero Referral Kickbacks</div>
            <p class="principle-text">
              We never take commissions from repair shops or parts sellers. All workshop rankings and diagnostic pathways are strictly based on proximity, credentials, and repairability.
            </p>
          </div>

          <div class="principle-card">
            <div class="principle-icon">
              <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>
            </div>
            <div class="principle-title">Rigorous Lithium Safety</div>
            <p class="principle-text">
              We never downplay battery swelling risks. Users receive explicit discharge protocols, ESD safety guidelines, and emergency containment steps for unstable cells.
            </p>
          </div>

          <div class="principle-card">
            <div class="principle-icon">
              <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"/></svg>
            </div>
            <div class="principle-title">Certified Recovery Only</div>
            <p class="principle-text">
              When a device reaches true end-of-life, recycling pathways are restricted to R2v3 and e-Stewards facilities, preventing hazardous toxic dumping overseas.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- ==========================================================================
         2. DEVICE CHECKER â€” THE CORE DEMO (#checker)
         ========================================================================== -->
    <section id="checker" class="section-padding">
      <div class="container">
        <div class="section-header">
          <div class="section-label">INTERACTIVE CORE DEMO</div>
          <h2 class="section-title">Assess your device in seconds</h2>
          <p class="section-desc">
            Walk through our interactive diagnostic tree to get an honest repairability assessment, estimated parts costs, safety guidance, and tailored circular next steps.
          </p>
        </div>

        <div class="checker-container">
          <!-- Step Indicator Bar -->
          <div class="checker-steps-bar">
            <div class="step-tab active" data-step-num="1">
              <span class="step-tab-num">1</span>
              <span>1. Category</span>
            </div>
            <div class="step-tab" data-step-num="2">
              <span class="step-tab-num">2</span>
              <span>2. Brand & Model</span>
            </div>
            <div class="step-tab" data-step-num="3">
              <span class="step-tab-num">3</span>
              <span>3. Symptom</span>
            </div>
            <div class="step-tab" data-step-num="4">
              <span class="step-tab-num">4</span>
              <span>4. Context</span>
            </div>
          </div>

          <div class="checker-body">
            <!-- Step 1: Category Selection -->
            <div class="checker-step-pane active" id="checkerStep1">
              <div class="pane-heading">
                <div class="pane-title">What type of electronics device are you assessing?</div>
                <div class="pane-subtitle">Select your device form factor to load relevant repairability rubrics.</div>
              </div>
              <div class="category-selection-grid" id="checkerCategoryGrid">
                <!-- Dynamically populated by app.js -->
              </div>
            </div>

            <!-- Step 2: Brand & Model Selection -->
            <div class="checker-step-pane" id="checkerStep2">
              <div class="pane-heading">
                <div class="pane-title">Specify your device brand and model</div>
                <div class="pane-subtitle">Choose a common model preset or type your exact model number.</div>
              </div>

              <div class="model-input-wrap">
                <div>
                  <div class="quick-models-label">Popular Reference Models</div>
                  <div class="model-presets-row" id="modelPresetsRow">
                    <!-- Dynamically populated by app.js -->
                  </div>
                </div>

                <div class="or-divider">OR ENTER CUSTOM MODEL</div>

                <div class="form-group">
                  <label class="form-label" for="customModelInput">Device Model or Series</label>
                  <input type="text" id="customModelInput" class="form-input" placeholder="e.g. Dell XPS 13 9310, iPad Pro 11, Pixel 7">
                </div>

                <div class="unknown-model-box">
                  <div>
                    <strong style="color:var(--forest-900);">Don't know your exact model number?</strong>
                    <p>Check the bottom lid, under Settings > About, or proceed with generic category defaults.</p>
                  </div>
                  <label class="checkbox-custom-item">
                    <input type="checkbox" id="unknownModelCheckbox">
                    <span>Use Assisted Detection</span>
                  </label>
                </div>
              </div>
            </div>

            <!-- Step 3: Issue / Symptom Selection -->
            <div class="checker-step-pane" id="checkerStep3">
              <div class="pane-heading">
                <div class="pane-title">What is the primary symptom or hardware failure?</div>
                <div class="pane-subtitle">Select the most prominent issue observed with your device.</div>
              </div>
              <div class="issue-selection-grid" id="checkerIssueGrid">
                <!-- Dynamically populated by app.js -->
              </div>
            </div>

            <!-- Step 4: Context Questions -->
            <div class="checker-step-pane" id="checkerStep4">
              <div class="pane-heading">
                <div class="pane-title">A few quick context details for diagnostic accuracy</div>
                <div class="pane-subtitle">Hardware age and power states significantly affect the repair vs replacement equation.</div>
              </div>

              <div class="context-questions-wrap">
                <!-- Age Question -->
                <div class="question-block">
                  <div class="q-label">Approximately how old is this device?</div>
                  <div class="choice-options-row">
                    <button type="button" class="choice-pill age-choice-pill" data-age="<1">Less than 1 year</button>
                    <button type="button" class="choice-pill age-choice-pill selected" data-age="1-3">1 to 3 years</button>
                    <button type="button" class="choice-pill age-choice-pill" data-age="3-5">3 to 5 years</button>
                    <button type="button" class="choice-pill age-choice-pill" data-age="5+">5+ years</button>
                  </div>
                </div>

                <!-- Power State Question -->
                <div class="question-block">
                  <div class="q-label">Does the device power on or show signs of life?</div>
                  <div class="choice-options-row">
                    <button type="button" class="choice-pill power-choice-pill selected" data-power="yes">Yes, boots normally</button>
                    <button type="button" class="choice-pill power-choice-pill" data-power="intermittent">Intermittent / Reboots randomly</button>
                    <button type="button" class="choice-pill power-choice-pill" data-power="no">No, completely unresponsive</button>
                  </div>
                </div>

                <!-- Specific Symptoms Checklist -->
                <div class="question-block">
                  <div class="q-label">Select all symptoms currently observed:</div>
                  <div id="symptomsContextList" style="display:grid; grid-template-columns:1fr 1fr; gap:0.65rem;">
                    <!-- Populated dynamically based on selected issue -->
                  </div>
                </div>
              </div>
            </div>

            <!-- Loading Simulation Pane -->
            <div class="checker-step-pane" id="checkerLoadingScreen">
              <div class="diagnosis-loading-screen">
                <div class="loader-spinner"></div>
                <div style="font-size:1.25rem; font-weight:800; color:var(--forest-900);">Synthesizing Diagnostic Assessment...</div>
                <div class="loading-log" id="loadingDynamicLog">Analyzing hardware disassembly complexity...</div>
              </div>
            </div>

            <!-- Step 5: Diagnosis Result Output -->
            <div class="checker-step-pane" id="checkerStep5">
              <div id="diagnosisResultContent">
                <!-- Dynamically rendered by renderDiagnosisResult in app.js -->
              </div>
            </div>

            <!-- Wizard Footer Controls -->
            <div class="checker-footer">
              <button type="button" class="btn btn-secondary" id="checkerBackBtn" style="visibility:hidden;">
                <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="19" y1="12" x2="5" y2="12"/><polyline points="12 19 5 12 12 5"/></svg>
                Back
              </button>
              <div style="display:flex; gap:0.75rem;">
                <button type="button" class="btn btn-ghost" id="checkerRestartBtn">Reset</button>
                <button type="button" class="btn btn-primary" id="checkerNextBtn">
                  Continue
                  <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ==========================================================================
         3. REPAIR LIBRARY (#guides)
         ========================================================================== -->
    <section id="guides" class="section-padding" style="background-color: var(--bg-subtle);">
      <div class="container">
        <div class="section-header">
          <div class="section-label">OPEN KNOWLEDGE BASE</div>
          <h2 class="section-title">Verified repair guides & teardowns</h2>
          <p class="section-desc">
            Explore step-by-step disassembly manuals created with clear safety protocols, required tools checklists, and estimated cost savings.
          </p>
        </div>

        <!-- Filter Controls -->
        <div class="filter-controls-card">
          <div class="search-input-wrap">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>
            <input type="text" id="guideSearchInput" placeholder="Search guides by device (e.g. iPhone 13, ThinkPad, Sony headphones) or tool...">
          </div>

          <div class="filters-row">
            <div class="filter-pills-group">
              <button type="button" class="filter-pill guide-category-pill active" data-cat="all">All Devices</button>
              <button type="button" class="filter-pill guide-category-pill" data-cat="phone">Smartphones</button>
              <button type="button" class="filter-pill guide-category-pill" data-cat="laptop">Laptops</button>
              <button type="button" class="filter-pill guide-category-pill" data-cat="audio">Audio & Wearables</button>
              <button type="button" class="filter-pill guide-category-pill" data-cat="tablet">Tablets</button>
            </div>

            <div class="filter-select-wrap">
              <label for="guideDifficultySelect">Difficulty:</label>
              <select id="guideDifficultySelect" class="filter-select">
                <option value="all">All Levels</option>
                <option value="Novice">Novice (Snap-fit & Screws)</option>
                <option value="Moderate">Moderate (Adhesive & Batteries)</option>
                <option value="Advanced">Advanced (Thermal & Micro-ribbons)</option>
              </select>
            </div>
          </div>
        </div>

        <!-- Guides Grid -->
        <div class="guides-grid" id="repairGuidesGrid">
          <!-- Dynamically populated by app.js -->
        </div>

        <div style="margin-top:2.5rem; text-align:center;">
          <p style="font-size:0.8125rem; color:var(--charcoal-500); font-family:var(--font-mono);">
            * DEMO CONTENT: Guides represent open community instructional standards. Not affiliated with or approved by original equipment manufacturers.
          </p>
        </div>
      </div>
    </section>

    <!-- ==========================================================================
         4. REPAIR NETWORK DIRECTORY (#network)
         ========================================================================== -->
    <section id="network" class="section-padding">
      <div class="container">
        <div class="section-header">
          <div class="section-label">INDEPENDENT REPAIR DIRECTORY</div>
          <h2 class="section-title">Connect with verified local technicians</h2>
          <p class="section-desc">
            Support local repair businesses pledged to transparency, genuine component sourcing, and component-level repair over expensive board replacements.
          </p>
        </div>

        <div class="directory-layout">
          <!-- Left: Search & Repairers List -->
          <div>
            <div class="filter-controls-card" style="margin-bottom:1.5rem;">
              <div class="search-input-wrap">
                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>
                <input type="text" id="repairerSearchInput" placeholder="Filter by workshop name, city (e.g. Brooklyn, Queens), or service...">
              </div>
              <div class="filter-pills-group" style="margin-top:0.5rem;">
                <button type="button" class="filter-pill repairer-spec-pill active" data-spec="all">All Specialties</button>
                <button type="button" class="filter-pill repairer-spec-pill" data-spec="Smartphones">Smartphones</button>
                <button type="button" class="filter-pill repairer-spec-pill" data-spec="Laptops">Laptops</button>
                <button type="button" class="filter-pill repairer-spec-pill" data-spec="Micro-soldering">Micro-soldering</button>
                <button type="button" class="filter-pill repairer-spec-pill" data-spec="Audio">Audio / Hi-Fi</button>
              </div>
            </div>

            <div class="repairers-list-wrap" id="repairersListContainer">
              <!-- Populated by app.js -->
            </div>
          </div>

          <!-- Right: Interactive Radar / Map Sidebar & Onboarding -->
          <div>
            <div class="directory-sidebar-card">
              <div class="radar-header">
                <div class="radar-title">Community Repair Proximity</div>
                <span class="telemetry-chip">DEMO RADIUS: 10 KM</span>
              </div>

              <!-- Simulated Map Frame -->
              <div class="simulated-map-frame">
                <div class="map-grid-pattern"></div>
                <!-- Interactive Pins -->
                <div class="radar-pin" style="top:35%; left:42%;" title="CircuitCraft Labs (1.2 km)"></div>
                <div class="radar-pin" style="top:55%; left:68%;" title="Volt & Solder Precision (3.4 km)"></div>
                <div class="radar-pin" style="top:25%; left:75%;" title="The Fixer's Guild (4.8 km)"></div>
                <div class="radar-pin" style="top:70%; left:30%;" title="Silicon Resurrect Labs (6.1 km)"></div>
                
                <div style="position:absolute; bottom:12px; left:12px; font-family:var(--font-mono); font-size:0.7rem; color:var(--lime-400); background:rgba(0,0,0,0.6); padding:0.2rem 0.5rem; border-radius:4px;">
                  4 ACTIVE VERIFIED BENCHES IN RADIUS
                </div>
              </div>

              <div class="radar-stats-box">
                <strong style="color:#FFFFFF; display:block; margin-bottom:0.25rem;">Why Choose Independent Repair?</strong>
                Authorised depot centers routinely charge $400+ to swap entire motherboards for a simple 50-cent blown diode or loose port pin. Independent shops save electronics at the component level.
              </div>

              <div style="border-top:1px solid rgba(255,255,255,0.1); padding-top:1.25rem;">
                <div style="font-size:0.95rem; font-weight:800; color:#FFFFFF; margin-bottom:0.35rem;">Are you an independent repairer?</div>
                <p style="font-size:0.8125rem; color:var(--charcoal-200); margin-bottom:1rem;">
                  Join the CIRCULAR vetted directory, pledge to Right-to-Repair pricing transparency, and receive qualified hardware repair requests.
                </p>
                <button type="button" class="btn btn-lime" id="btnOpenListShopModal" style="width:100%;">
                  List Your Repair Service
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ==========================================================================
         5. GIVE A DEVICE A SECOND LIFE (#second-life)
         ========================================================================== -->
    <section id="second-life" class="section-padding" style="background-color: var(--bg-subtle);">
      <div class="container">
        <div class="section-header">
          <div class="section-label">RESPONSIBLE TRANSITIONS</div>
          <h2 class="section-title">Give a device a second life</h2>
          <p class="section-desc">
            When you're ready to upgrade or when repair is no longer economical, choose the highest-value circular pathway to prevent hardware from turning into toxic e-waste.
          </p>
        </div>

        <!-- 4 Circular Pathways -->
        <div class="secondlife-pathways-grid">
          <!-- Pathway 1: Donate -->
          <div class="pathway-card">
            <div class="pathway-icon">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"/></svg>
            </div>
            <div class="pathway-title">Donate</div>
            <div class="pathway-tagline">Digital Inclusion Programs</div>
            <p class="pathway-desc">
              Pass working laptops and tablets to students, community centers, and non-profits who bridge the digital divide.
            </p>
            <div class="pathway-benefit-box">
              <strong>Requirement:</strong> Boots to OS, battery holds &gt;60 mins charge, activation locks disabled.
            </div>
          </div>

          <!-- Pathway 2: Refurbish / Upcycle -->
          <div class="pathway-card">
            <div class="pathway-icon">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M14.7 6.3a1 1 0 0 0 0 1.4l1.6 1.6a1 1 0 0 0 1.4 0l3.77-3.77a6 6 0 0 1-7.94 7.94l-6.91 6.91a2.12 2.12 0 0 1-3-3l6.91-6.91a6 6 0 0 1 7.94-7.94l-3.76 3.76z"/></svg>
            </div>
            <div class="pathway-title">Refurbish & Upcycle</div>
            <div class="pathway-tagline">Repurpose Into Utility Nodes</div>
            <p class="pathway-desc">
              Transform sluggish smartphones into smart-home dashboards or convert old laptops into low-power home servers (Pi-hole, media vault).
            </p>
            <div class="pathway-benefit-box">
              <strong>Advantage:</strong> Zero transit emissions, infinite utility from depreciated chips.
            </div>
          </div>

          <!-- Pathway 3: Resale -->
          <div class="pathway-card">
            <div class="pathway-icon">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="12" y1="1" x2="12" y2="23"/><path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"/></svg>
            </div>
            <div class="pathway-title">Fair P2P Resale</div>
            <div class="pathway-tagline">Honest Secondary Market</div>
            <p class="pathway-desc">
              Sell directly to secondary market buyers with honest battery health and scratch disclosures, displacing demand for new hardware.
            </p>
            <div class="pathway-benefit-box">
              <strong>Advantage:</strong> Recovers liquid cash while extending device service life.
            </div>
          </div>

          <!-- Pathway 4: Certified Recovery -->
          <div class="pathway-card">
            <div class="pathway-icon">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M7 19H4.815a1.83 1.83 0 0 1-1.57-.881 1.785 1.785 0 0 1-.004-1.784L7.196 9.5"/><path d="M11 19h8.2a1.8 1.8 0 0 0 1.57-2.665L16.8 9.5"/><path d="m9 5 3-3 3 3"/></svg>
            </div>
            <div class="pathway-title">Certified Recycling</div>
            <p class="pathway-desc">
              When structural damage is irreparable, route hardware strictly to R2v3 / e-Stewards recyclers to smelt and reclaim gold, cobalt, and copper.
            </p>
            <div class="pathway-benefit-box">
              <strong>Advantage:</strong> Eliminates toxic landfill lithium fires and heavy metal leaching.
            </div>
          </div>
        </div>

        <!-- Secure Erasure Step-by-Step Guide -->
        <div class="erasure-card">
          <div class="erasure-header">
            <div>
              <div style="font-family:var(--font-mono); font-size:0.75rem; color:var(--lime-400); font-weight:800; letter-spacing:0.05em; text-transform:uppercase;">
                DATA PROTECTION PROTOCOL (NIST 800-88)
              </div>
              <div style="font-size:1.4rem; font-weight:800;">Secure Data Sanitization Guide</div>
            </div>
            <div class="os-tab-buttons" id="erasureOsTabs">
              <!-- Populated by app.js -->
            </div>
          </div>
          <div class="erasure-body" id="erasureStepsContainer">
            <!-- Populated by app.js -->
          </div>
        </div>

        <!-- Interactive Pre-Handoff Checklist -->
        <div class="checklist-card">
          <div class="checklist-header-row">
            <div>
              <div style="font-size:1.3rem; font-weight:800; color:var(--forest-900);">Pre-Handoff Checklist</div>
              <div style="font-size:0.875rem; color:var(--charcoal-600);">
                Check off each item to ensure your hardware is safe, clean, and unlinked before reuse or recycling.
              </div>
            </div>
            <div style="font-family:var(--font-mono); font-size:0.875rem; font-weight:800; color:var(--forest-800);" id="handoffProgressText">
              0 of 7 Done (0%)
            </div>
          </div>

          <div class="progress-track">
            <div class="progress-fill" id="handoffProgressFill"></div>
          </div>

          <div class="interactive-checklist-grid" id="handoffChecklistGrid">
            <!-- Populated by app.js -->
          </div>
        </div>
      </div>
    </section>

    <!-- ==========================================================================
         6. ABOUT / IMPACT & JUDGE-FRIENDLY HACKATHON BRIEF (#impact)
         ========================================================================== -->
    <section id="impact" class="section-padding">
      <div class="container">
        <!-- Hackathon Challenge Callout Banner -->
        <div class="judge-banner-card">
          <span class="judge-tag">CHALLENGE: IMX26-PS07 â€” CEDA-EPS</span>
          <h2 style="font-size:clamp(1.85rem, 3.5vw, 2.5rem); font-weight:800; line-height:1.15; letter-spacing:-0.03em;">
            Design Electronics for Repair, Reuse & Recovery
          </h2>
          <p style="color:var(--charcoal-200); font-size:1.05rem; max-width:760px; margin-top:0.75rem; line-height:1.6;">
            CIRCULAR directly tackles the electronics waste crisis by addressing the root cause: lack of accessible diagnostic clarity, proprietary repair locks, and friction in passing functional hardware on.
          </p>

          <div class="judge-grid-five-pillars">
            <div class="pillar-box">
              <div class="pillar-name">01. USEFULNESS</div>
              <div class="pillar-heading">Solves Friction</div>
              <p class="pillar-text">Gives non-technical device owners clear triage within 60 seconds without manufacturer gatekeeping.</p>
            </div>
            <div class="pillar-box">
              <div class="pillar-name">02. FEASIBILITY</div>
              <div class="pillar-heading">Zero Hard Sci-Fi</div>
              <p class="pillar-text">Built on standard web standards, open repair schemas, and existing independent repair infrastructure.</p>
            </div>
            <div class="pillar-box">
              <div class="pillar-name">03. ORIGINALITY</div>
              <div class="pillar-heading">Hierarchy First</div>
              <p class="pillar-text">Prioritizes component-level repair and cryptographic data wiping before material smelting.</p>
            </div>
            <div class="pillar-box">
              <div class="pillar-name">04. IMPACT</div>
              <div class="pillar-heading">Measurable LCA</div>
              <p class="pillar-text">Tracks avoided supply-chain COâ‚‚e, diverted e-waste kg, and retained local community capital.</p>
            </div>
            <div class="pillar-box">
              <div class="pillar-name">05. SCALABILITY</div>
              <div class="pillar-heading">Digital Passport</div>
              <p class="pillar-text">Architected to integrate with upcoming EU Digital Product Passport (DPP) compliance regulations.</p>
            </div>
          </div>
        </div>

        <!-- Interactive Impact Simulator -->
        <div class="simulator-card">
          <div style="display:flex; justify-content:space-between; align-items:flex-start; flex-wrap:wrap; gap:1rem; margin-bottom:2rem;">
            <div>
              <div class="section-label">INTERACTIVE MODEL</div>
              <div style="font-size:1.6rem; font-weight:800; color:var(--forest-900); letter-spacing:-0.02em;">
                Community Impact Simulator
              </div>
              <p style="font-size:0.9375rem; color:var(--charcoal-600); margin-top:0.25rem;">
                Adjust the sliders below to simulate environmental and economic dividends for a campus, district, or municipal deployment.
              </p>
            </div>
            <span class="estimate-notice" style="color:var(--forest-800); background:var(--forest-100);">
              LCA BENCHMARKS: FRAUNHOFER IZM &amp; EPA WEEE
            </span>
          </div>

          <!-- Slider 1: Devices -->
          <div class="slider-group">
            <div class="slider-header">
              <span class="slider-label">Number of community electronics assessed:</span>
              <span class="slider-value-badge" id="simDevicesVal">2,500</span>
            </div>
            <input type="range" class="range-slider" id="simDevicesSlider" min="200" max="25000" step="100" value="2500">
          </div>

          <!-- Slider 2: Lifespan Extension -->
          <div class="slider-group">
            <div class="slider-header">
              <span class="slider-label">Average useful lifespan extended via repair/reuse:</span>
              <span class="slider-value-badge" id="simMonthsVal">18 mo</span>
            </div>
            <input type="range" class="range-slider" id="simMonthsSlider" min="6" max="36" step="3" value="18">
          </div>

          <!-- Reactive Impact Numbers -->
          <div class="simulator-results-grid">
            <div class="sim-metric-card">
              <div class="sim-metric-num" id="simMetricCo2">413 t</div>
              <div class="sim-metric-label">Supply Chain COâ‚‚e Eliminated</div>
            </div>
            <div class="sim-metric-card">
              <div class="sim-metric-num" id="simMetricEwaste">2,125 kg</div>
              <div class="sim-metric-label">E-Waste Diverted From Landfill</div>
            </div>
            <div class="sim-metric-card">
              <div class="sim-metric-num" id="simMetricWealth">$700,000</div>
              <div class="sim-metric-label">Kept in Household Pockets</div>
            </div>
            <div class="sim-metric-card">
              <div class="sim-metric-num" id="simMetricMaterials">85g Au / 38kg Co</div>
              <div class="sim-metric-label">Critical Minerals Preserved</div>
            </div>
          </div>
        </div>

        <!-- Feasibility, Prospective Partners & Pilot Plan -->
        <div style="margin-bottom:3rem;">
          <div class="section-label">ROADMAP &amp; FEASIBILITY</div>
          <h3 style="font-size:1.75rem; font-weight:800; color:var(--forest-900); margin-bottom:1.5rem;">
            Phased implementation roadmap
          </h3>

          <div class="timeline-list">
            <!-- Phase 1 -->
            <div class="timeline-phase-card">
              <div class="phase-top">
                <span class="phase-name">PHASE 01: MONTHS 1 â€“ 3</span>
                <span class="rep-badge">LOCAL PROOF OF CONCEPT</span>
              </div>
              <div class="phase-milestone">Campus &amp; Community Diagnostic Desk</div>
              <ul class="phase-bullets">
                <li>Deploy open diagnostic rubric across top 50 consumer smartphone and laptop models.</li>
                <li>Partner with 5 vetted independent repair shops in a pilot metropolitan zone.</li>
                <li>Establish first physical "Drop &amp; Diagnose" student repair clinic at university makerspaces.</li>
              </ul>
            </div>

            <!-- Phase 2 -->
            <div class="timeline-phase-card">
              <div class="phase-top">
                <span class="phase-name">PHASE 02: MONTHS 4 â€“ 7</span>
                <span class="rep-badge">INTEGRATION &amp; STANDARDS</span>
              </div>
              <div class="phase-milestone">Open Parts Catalog &amp; Recycler APIs</div>
              <ul class="phase-bullets">
                <li>Aggregate verified OEM-grade parts availability (iFixit open parts schemas, Framework catalog).</li>
                <li>Implement digital product passport serial logs for verified repairs and battery swaps.</li>
                <li>Integrate verified e-Stewards / R2v3 recycler drop-off geofence mapping.</li>
              </ul>
            </div>

            <!-- Phase 3 -->
            <div class="timeline-phase-card">
              <div class="phase-top">
                <span class="phase-name">PHASE 03: MONTHS 8 â€“ 12</span>
                <span class="rep-badge">MUNICIPAL EXPANSION</span>
              </div>
              <div class="phase-milestone">Enterprise &amp; Civic Circularity Network</div>
              <ul class="phase-bullets">
                <li>Corporate device lifecycle dashboard for universities and local enterprise fleets.</li>
                <li>Issue tamper-proof verified environmental impact audit receipts for corporate ESG compliance.</li>
                <li>Public API for municipal sanitation departments to divert electronics ahead of incinerators.</li>
              </ul>
            </div>
          </div>
        </div>

        <!-- Prospective Partners & Honest Collaboration Note -->
        <div style="background:var(--bg-subtle); border:1px solid var(--border-card); border-radius:var(--radius-lg); padding:2rem;">
          <div style="font-size:1.15rem; font-weight:800; color:var(--forest-900); margin-bottom:0.5rem;">
            Prospective Ecosystem Partners &amp; Integration Targets
          </div>
          <p style="font-size:0.875rem; color:var(--charcoal-600); line-height:1.6; margin-bottom:1.25rem;">
            To maintain full integrity for hackathon judges, the following organizations are recognized as <strong>prospective integration candidates</strong> aligned with our architectural standards, not formal endorsements:
          </p>
          <div style="display:grid; grid-template-columns:repeat(4, 1fr); gap:1rem;">
            <div style="background:#FFFFFF; padding:1rem; border-radius:var(--radius-md); border:1px solid var(--border-subtle);">
              <div style="font-weight:800; font-size:0.95rem; color:var(--forest-900);">Repair.org Coalition</div>
              <div style="font-size:0.75rem; color:var(--charcoal-500); margin-top:0.25rem;">Policy &amp; Right to Repair legal standards alignment</div>
            </div>
            <div style="background:#FFFFFF; padding:1rem; border-radius:var(--radius-md); border:1px solid var(--border-subtle);">
              <div style="font-weight:800; font-size:0.95rem; color:var(--forest-900);">iFixit Open Data API</div>
              <div style="font-size:0.75rem; color:var(--charcoal-500); margin-top:0.25rem;">Teardown schema and tool compatibility taxonomies</div>
            </div>
            <div style="background:#FFFFFF; padding:1rem; border-radius:var(--radius-md); border:1px solid var(--border-subtle);">
              <div style="font-weight:800; font-size:0.95rem; color:var(--forest-900);">e-Stewards / R2v3</div>
              <div style="font-size:0.75rem; color:var(--charcoal-500); margin-top:0.25rem;">Audited ethical end-of-life recycling verification</div>
            </div>
            <div style="background:#FFFFFF; padding:1rem; border-radius:var(--radius-md); border:1px solid var(--border-subtle);">
              <div style="font-weight:800; font-size:0.95rem; color:var(--forest-900);">Repair CafÃ© Int'l</div>
              <div style="font-size:0.75rem; color:var(--charcoal-500); margin-top:0.25rem;">Grassroots community volunteer workshop networks</div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>

  <!-- ==========================================================================
       MODALS
       ========================================================================== -->

  <!-- 1. Detailed Repair Guide Viewer Modal -->
  <div class="modal-backdrop" id="guideModal" role="dialog" aria-modal="true">
    <div class="modal-window">
      <div class="modal-header">
        <div class="modal-title" id="guideModalTitle">Repair Manual</div>
        <button type="button" class="modal-close-btn" aria-label="Close modal">âœ•</button>
      </div>
      <div class="modal-body" id="guideModalBody">
        <!-- Dynamically rendered by app.js -->
      </div>
    </div>
  </div>

  <!-- 2. Request Diagnostic / Quote Modal -->
  <div class="modal-backdrop" id="quoteModal" role="dialog" aria-modal="true">
    <div class="modal-window" style="max-width:560px;">
      <div class="modal-header">
        <div class="modal-title">Request Diagnostic Quote</div>
        <button type="button" class="modal-close-btn" aria-label="Close modal">âœ•</button>
      </div>
      <div class="modal-body">
        <p style="font-size:0.875rem; color:var(--charcoal-600);">
          Sending preliminary diagnostic telemetry to <strong id="quoteShopName" style="color:var(--forest-900);">Workshop</strong>.
        </p>

        <form id="quoteRequestForm" style="display:flex; flex-direction:column; gap:1rem;">
          <div class="form-group">
            <label class="form-label" for="quoteDeviceField">Device Model</label>
            <input type="text" id="quoteDeviceField" class="form-input" readonly>
          </div>
          <div class="form-group">
            <label class="form-label" for="quoteIssueField">Observed Symptom</label>
            <input type="text" id="quoteIssueField" class="form-input" readonly>
          </div>
          <div class="form-group">
            <label class="form-label" for="quoteUserName">Your Name *</label>
            <input type="text" id="quoteUserName" class="form-input" placeholder="e.g. Alex Morgan" required>
          </div>
          <div class="form-group">
            <label class="form-label" for="quoteUserEmail">Email Address *</label>
            <input type="email" id="quoteUserEmail" class="form-input" placeholder="alex@example.com" required>
          </div>
          <div class="form-group">
            <label class="form-label" for="quoteNotes">Optional Diagnostic Notes</label>
            <textarea id="quoteNotes" class="form-textarea" rows="3" placeholder="Any dropped history, error codes, or urgency..."></textarea>
          </div>

          <div style="display:flex; justify-content:flex-end; gap:0.75rem; margin-top:0.5rem;">
            <button type="button" class="btn btn-secondary modal-close-btn">Cancel</button>
            <button type="submit" class="btn btn-lime">Send Diagnostic Inquiry</button>
          </div>
        </form>
      </div>
    </div>
  </div>

  <!-- 3. List Repair Service Modal -->
  <div class="modal-backdrop" id="listShopModal" role="dialog" aria-modal="true">
    <div class="modal-window" style="max-width:620px;">
      <div class="modal-header">
        <div class="modal-title">List Your Independent Repair Service</div>
        <button type="button" class="modal-close-btn" aria-label="Close modal">âœ•</button>
      </div>
      <div class="modal-body">
        <p style="font-size:0.875rem; color:var(--charcoal-600);">
          Join our directory by pledging adherence to transparent repair pricing, component-level troubleshooting, and customer data privacy.
        </p>

        <form id="listShopForm" style="display:flex; flex-direction:column; gap:1.15rem;">
          <div class="form-group">
            <label class="form-label" for="listShopName">Workshop / Business Name *</label>
            <input type="text" id="listShopName" class="form-input" placeholder="e.g. Precision Silicon Labs" required>
          </div>

          <div style="display:grid; grid-template-columns:1fr 1fr; gap:1rem;">
            <div class="form-group">
              <label class="form-label" for="listShopEmail">Business Contact Email *</label>
              <input type="email" id="listShopEmail" class="form-input" placeholder="service@lab.com" required>
            </div>
            <div class="form-group">
              <label class="form-label" for="listShopPhone">Phone Number</label>
              <input type="tel" id="listShopPhone" class="form-input" placeholder="+1 (555) 000-0000">
            </div>
          </div>

          <div class="form-group">
            <label class="form-label" for="listShopAddress">Physical Address / City *</label>
            <input type="text" id="listShopAddress" class="form-input" placeholder="e.g. 142 Greenpoint Ave, Brooklyn, NY" required>
          </div>

          <div class="form-group">
            <label class="form-label">Primary Specialties</label>
            <div style="display:grid; grid-template-columns:1fr 1fr; gap:0.5rem; font-size:0.875rem;">
              <label class="checkbox-custom-item"><input type="checkbox" checked> Smartphones / Screen Swaps</label>
              <label class="checkbox-custom-item"><input type="checkbox" checked> Micro-soldering / Logic Board</label>
              <label class="checkbox-custom-item"><input type="checkbox" checked> Laptops &amp; MacBooks</label>
              <label class="checkbox-custom-item"><input type="checkbox"> Vintage Audio / Hi-Fi</label>
            </div>
          </div>

          <div class="unknown-model-box">
            <label class="checkbox-custom-item" style="font-size:0.8125rem;">
              <input type="checkbox" required checked>
              <span>We pledge to respect Right-to-Repair pricing transparency and safe hazardous battery disposal.</span>
            </label>
          </div>

          <div style="display:flex; justify-content:flex-end; gap:0.75rem;">
            <button type="button" class="btn btn-secondary modal-close-btn">Cancel</button>
            <button type="submit" class="btn btn-primary">Submit Application</button>
          </div>
        </form>
      </div>
    </div>
  </div>

  <!-- ==========================================================================
       SITE FOOTER
       ========================================================================== -->
  <footer class="site-footer">
    <div class="container footer-grid">
      <div class="footer-brand-col">
        <div class="footer-brand-title">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
            <path d="M21 12a9 9 0 0 0-9-9 9.75 9.75 0 0 0-6.74 2.74L3 8"/>
            <path d="M3 3v5h5"/>
            <path d="M3 12a9 9 0 0 0 9 9 9.75 9.75 0 0 0 6.74-2.74L21 16"/>
            <path d="M21 21v-5h-5"/>
          </svg>
          CIRCULAR
        </div>
        <p class="footer-mission">
          Empowering individuals and communities to keep electronics in active service longer. Built for the CEDA-EPS hackathon challenge on sustainable product lifecycles.
        </p>
        <div style="font-family:var(--font-mono); font-size:0.75rem; color:var(--lime-400);">
          Challenge: IMX26-PS07 â€” CEDA-EPS
        </div>
      </div>

      <div class="footer-nav-col">
        <div class="footer-heading">Platform</div>
        <a href="#checker" class="route-trigger" data-route="checker">Device Checker</a>
        <a href="#guides" class="route-trigger" data-route="guides">Repair Library</a>
        <a href="#network" class="route-trigger" data-route="network">Repair Network</a>
        <a href="#second-life" class="route-trigger" data-route="second-life">Second Life Pathways</a>
      </div>

      <div class="footer-nav-col">
        <div class="footer-heading">Ecosystem</div>
        <a href="#circular-journey">Circular Journey</a>
        <a href="#second-life">Data Sanitization</a>
        <a href="#second-life">Handoff Checklist</a>
        <a href="#impact">Impact Simulator</a>
      </div>

      <div class="footer-nav-col">
        <div class="footer-heading">Hackathon &amp; Standards</div>
        <a href="#impact" class="route-trigger" data-route="impact">Judges Brief</a>
        <a href="#impact" class="route-trigger" data-route="impact">LCA Benchmarks</a>
        <a href="#impact" class="route-trigger" data-route="impact">Pilot Roadmap</a>
        <a href="#impact" class="route-trigger" data-route="impact">Prospective Partners</a>
      </div>
    </div>

    <div class="container footer-bottom">
      <div>
        &copy; 2026 CIRCULAR. Open-source prototype for Challenge IMX26-PS07.
      </div>
      <div class="challenge-attribution">
        Challenge: IMX26-PS07 â€” CEDA-EPS | Design Electronics for Repair, Reuse &amp; Recovery
      </div>
    </div>
  </footer>

  <!-- Application Scripts -->
  <script>
/**
 * CIRCULAR â€” Platform Dataset
 * Challenge: IMX26-PS07 â€” CEDA-EPS
 * 
 * Transparent, realistic demo dataset representing repair guides,
 * device taxonomy, independent repairers, life-cycle assessment (LCA) benchmarks,
 * and circular economy metrics.
 * 
 * NOTE: All figures, guide details, and repair listings are clearly labeled
 * as illustrative demo data for the hackathon prototype.
 */

const CIRCULAR_DATA = {
  challenge: {
    id: "IMX26-PS07",
    track: "CEDA-EPS",
    title: "Design Electronics for Repair, Reuse & Recovery",
    theme: "Circular Electronics Digital Platform"
  },

  deviceCategories: [
    {
      id: "phone",
      name: "Smartphone",
      icon: "smartphone",
      embodiedCo2Kg: 65,
      avgWeightKg: 0.19,
      preciousMetals: { goldMg: 34, silverMg: 350, cobaltG: 12, lithiumG: 3.2 },
      popularModels: [
        { brand: "Apple", model: "iPhone 13", repairabilityScore: 6.5, releaseYear: 2021 },
        { brand: "Apple", model: "iPhone 12", repairabilityScore: 6.0, releaseYear: 2020 },
        { brand: "Samsung", model: "Galaxy S22", repairabilityScore: 5.5, releaseYear: 2022 },
        { brand: "Google", model: "Pixel 7", repairabilityScore: 7.0, releaseYear: 2022 },
        { brand: "Fairphone", model: "Fairphone 4", repairabilityScore: 10.0, releaseYear: 2021 },
        { brand: "Motorola", model: "Moto G Power", repairabilityScore: 7.0, releaseYear: 2021 }
      ]
    },
    {
      id: "laptop",
      name: "Laptop",
      icon: "laptop",
      embodiedCo2Kg: 280,
      avgWeightKg: 1.8,
      preciousMetals: { goldMg: 220, silverMg: 1100, cobaltG: 45, lithiumG: 14.5 },
      popularModels: [
        { brand: "Lenovo", model: "ThinkPad T480", repairabilityScore: 9.2, releaseYear: 2018 },
        { brand: "Apple", model: "MacBook Air M1", repairabilityScore: 4.8, releaseYear: 2020 },
        { brand: "Dell", model: "XPS 13 (9310)", repairabilityScore: 6.0, releaseYear: 2021 },
        { brand: "Framework", model: "Framework Laptop 13", repairabilityScore: 10.0, releaseYear: 2022 },
        { brand: "HP", model: "EliteBook 840 G7", repairabilityScore: 8.5, releaseYear: 2020 }
      ]
    },
    {
      id: "tablet",
      name: "Tablet",
      icon: "tablet",
      embodiedCo2Kg: 120,
      avgWeightKg: 0.48,
      preciousMetals: { goldMg: 85, silverMg: 420, cobaltG: 22, lithiumG: 6.8 },
      popularModels: [
        { brand: "Apple", model: "iPad Air 4", repairabilityScore: 3.8, releaseYear: 2020 },
        { brand: "Samsung", model: "Galaxy Tab S8", repairabilityScore: 5.2, releaseYear: 2022 },
        { brand: "Microsoft", model: "Surface Pro 8", repairabilityScore: 4.5, releaseYear: 2021 }
      ]
    },
    {
      id: "audio",
      name: "Audio & Wearables",
      icon: "headphones",
      embodiedCo2Kg: 35,
      avgWeightKg: 0.25,
      preciousMetals: { goldMg: 15, silverMg: 120, cobaltG: 6, lithiumG: 1.5 },
      popularModels: [
        { brand: "Sony", model: "WH-1000XM4", repairabilityScore: 7.2, releaseYear: 2020 },
        { brand: "Bose", model: "QuietComfort 45", repairabilityScore: 7.8, releaseYear: 2021 },
        { brand: "Apple", model: "AirPods Pro (1st Gen)", repairabilityScore: 1.2, releaseYear: 2019 }
      ]
    },
    {
      id: "console",
      name: "Gaming & Other",
      icon: "gamepad-2",
      embodiedCo2Kg: 190,
      avgWeightKg: 2.5,
      preciousMetals: { goldMg: 150, silverMg: 850, cobaltG: 18, lithiumG: 5.0 },
      popularModels: [
        { brand: "Nintendo", model: "Switch OLED", repairabilityScore: 7.0, releaseYear: 2021 },
        { brand: "Valve", model: "Steam Deck", repairabilityScore: 8.8, releaseYear: 2022 },
        { brand: "Sony", model: "PlayStation 5", repairabilityScore: 6.8, releaseYear: 2020 }
      ]
    }
  ],

  issueTaxonomy: [
    {
      id: "battery",
      label: "Battery Degraded or Swollen",
      icon: "battery-warning",
      urgency: "High if swollen, Moderate if low health",
      hasSafetyRisk: true,
      typicalSymptoms: ["Losing charge rapidly", "Sudden shutdown at 20%", "Screen lifting due to swollen cell", "Device hot while charging"]
    },
    {
      id: "screen",
      label: "Cracked or Unresponsive Screen",
      icon: "smartphone-charging",
      urgency: "Moderate to High",
      hasSafetyRisk: false,
      typicalSymptoms: ["Glass spiderweb cracks", "Black ink spots on OLED/LCD", "Touch input ghosting or unresponsive", "Flickering lines"]
    },
    {
      id: "charging",
      label: "Charging Port Loose or Not Powering",
      icon: "plug-zap",
      urgency: "Moderate",
      hasSafetyRisk: false,
      typicalSymptoms: ["Cable must be held at an angle", "Port clogged with lint", "Slow charging warning", "No charging LED indicator"]
    },
    {
      id: "performance",
      label: "Thermal Throttling & Sluggish Performance",
      icon: "gauge",
      urgency: "Low",
      hasSafetyRisk: false,
      typicalSymptoms: ["Fan screaming constantly", "Severe stutter during simple tasks", "Device chassis uncomfortably hot", "Storage full warning"]
    },
    {
      id: "liquid",
      label: "Liquid or Moisture Exposure",
      icon: "droplet",
      urgency: "Critical / Immediate",
      hasSafetyRisk: true,
      typicalSymptoms: ["Dropped in water", "Sticky keys or buttons", "Intermittent power", "Red moisture indicator sticker"]
    },
    {
      id: "board",
      label: "Won't Turn On / Logic Board Issue",
      icon: "cpu",
      urgency: "High",
      hasSafetyRisk: false,
      typicalSymptoms: ["No response to power button", "No lights, chime, or vibration", "Short circuit smell", "Black screen despite fan spinning"]
    }
  ],

  repairGuides: [
    {
      id: "guide-iphone-battery",
      title: "iPhone 13: Battery Replacement & Water Seal Renewal",
      category: "phone",
      device: "Apple iPhone 13",
      issueType: "battery",
      difficulty: "Moderate",
      timeEstimate: "35 â€“ 50 min",
      repairabilityScore: 6.5,
      costRangeDemo: "$28 â€“ $42",
      oemReplacementCost: "$89 â€“ $99 (Apple Authorized)",
      savingsEstimate: "~$55",
      safetyNote: "CRITICAL: Swollen lithium batteries are fire hazards. Never use metal tools to pry lithium pouches. Discharge battery below 25% before beginning.",
      requiredTools: [
        "P2 Pentalobe Screwdriver (0.8mm)",
        "Tri-point Y000 Screwdriver",
        "Suction handle or iSclack",
        "Plastic opening picks / Spudger",
        "Heat pad or iOpener (80Â°C / 176Â°F)",
        "Pre-cut waterproof display adhesive"
      ],
      requiredParts: [
        "Replacement 3,227 mAh Li-ion battery (compatible OEM-grade)",
        "Battery stretch-release adhesive pull-tabs",
        "Screen perimeter gasket seal"
      ],
      steps: [
        {
          num: 1,
          title: "Power Off & Discharge",
          detail: "Turn off the phone completely. Ensure battery level is below 25% to minimize thermal runaway hazard if accidentally punctured.",
          tip: "Work on a clean, ESD-safe silicone mat in a well-ventilated space."
        },
        {
          num: 2,
          title: "Remove Pentalobe Screws & Apply Soft Heat",
          detail: "Remove the two 3.5mm P2 screws on either side of the Lightning connector. Apply moderate heat (75Â°C) to the lower front edge for 2 minutes to soften the water-resistant adhesive.",
          tip: "Do not exceed 85Â°C to avoid damaging the OLED panel."
        },
        {
          num: 3,
          title: "Lift Display Assembly & Prop at 90Â°",
          detail: "Place suction cup on bottom left edge. Pull gently to create a hairline gap, insert plastic pick, and slide along bottom and left edges. Lift from right to left like a book cover. Do not pull past 90 degrees.",
          tip: "Cables run along the left edge. Keep angle restricted to prevent ribbon tears."
        },
        {
          num: 4,
          title: "Disconnect Battery Connector First",
          detail: "Remove the three Y000 screws securing the connector bracket. Gently pry up the battery connector using a plastic spudger. ALWAYS disconnect the battery before uncoupling screen cables.",
          tip: "Never use metal tweezers on live battery terminals."
        },
        {
          num: 5,
          title: "Extract Stretch-Release Adhesive Tabs",
          detail: "Gently peel the exposed tips of the pull tabs at the bottom and top of the battery. Pull horizontally at a low angle with slow, steady tension without jerking.",
          tip: "If a tab snaps, apply a few drops of 99% isopropyl alcohol around the edge and wait 2 minutes."
        },
        {
          num: 6,
          title: "Install New Battery & Replace Water Seal",
          detail: "Place new adhesive strips, position new battery, reconnect terminals to verify boot. Apply new perimeter water gasket, reassemble screws, and press firmly for 30 seconds.",
          tip: "Recalibrate new battery: charge to 100% and keep charging for at least 2 extra hours, then run down to zero once."
        }
      ]
    },
    {
      id: "guide-thinkpad-screen",
      title: "ThinkPad T480: 1080p IPS Display & Bezel Replacement",
      category: "laptop",
      device: "Lenovo ThinkPad T480 / T490",
      issueType: "screen",
      difficulty: "Novice",
      timeEstimate: "20 â€“ 30 min",
      repairabilityScore: 9.2,
      costRangeDemo: "$45 â€“ $65",
      oemReplacementCost: "$180 â€“ $240 (Lenovo Depot)",
      savingsEstimate: "~$140",
      safetyNote: "Ensure internal and external batteries are disabled in BIOS before opening bezel.",
      requiredTools: [
        "Phillips #00 Screwdriver",
        "Flat plastic spudger / Guitar pick",
        "Double-sided bezel tape (3mm)"
      ],
      requiredParts: [
        "14-inch Full HD (1920x1080) 30-pin eDP IPS Panel (e.g., Innolux N140HCG or AUO B140HAN)"
      ],
      steps: [
        {
          num: 1,
          title: "Disable Internal Battery in BIOS & Remove External Pack",
          detail: "Eject the removable rear battery pack. Boot into ThinkPad BIOS (Enter -> F1), navigate to Config -> Power -> 'Disable Built-in Battery'. The machine will automatically shut down.",
          tip: "This cuts power from the motherboard 30-pin eDP rail, eliminating backlight fuse blowouts."
        },
        {
          num: 2,
          title: "Pry Off the Display Bezel",
          detail: "Starting at the top inside edge between the screen and plastic frame, gently insert a plastic pick to unclip the retention hooks. Work around all four sides.",
          tip: "Take care near the web camera and dual microphone array at the top center."
        },
        {
          num: 3,
          title: "Remove 4 Mounting Screws & Drop Panel",
          detail: "Remove the four small Phillips #00 screws located at each corner bracket. Gently fold the screen down onto the keyboard deck face-first.",
          tip: "Place a soft microfiber cloth over the keyboard to prevent key scratching."
        },
        {
          num: 4,
          title: "Unlatch 30-Pin eDP Video Connector",
          detail: "Lift the clear adhesive tape holding the 30-pin connector. Flip the tiny metal bail wire latch upwards, then gently slide the cable connector straight back.",
          tip: "Do not pull vertically on the cable."
        },
        {
          num: 5,
          title: "Attach Replacement Panel & Snap Bezel",
          detail: "Slide the connector into the new panel, flip down the metal bail, re-tape. Power on temporarily to verify display output and brightness keys before reinstalling bezel clips.",
          tip: "Plugging in the AC adapter will automatically reactivate the internal battery."
        }
      ]
    },
    {
      id: "guide-sony-headphones",
      title: "Sony WH-1000XM4: Swivel Hinge & Lithium Battery Renewal",
      category: "audio",
      device: "Sony WH-1000XM4",
      issueType: "battery",
      difficulty: "Moderate",
      timeEstimate: "30 â€“ 45 min",
      repairabilityScore: 7.2,
      costRangeDemo: "$19 â€“ $29",
      oemReplacementCost: "$120 â€“ $150 (Sony Out-of-Warranty)",
      savingsEstimate: "~$95",
      safetyNote: "Touch sensor ribbon cable on the right ear cup is delicate. Pry ear cushions with plastic tools only.",
      requiredTools: [
        "Phillips #0 Screwdriver",
        "Plastic pry tool",
        "Tweezers",
        "Double-sided acoustic seal ring"
      ],
      requiredParts: [
        "Replacement 1000mAh 3.7V 3-wire Li-Polymer battery (Model: 721535 / SP 73)"
      ],
      steps: [
        {
          num: 1,
          title: "Unclip the Right Ear Cushion",
          detail: "Locate the 6 plastic clips securing the synthetic leather cushion. Twist and slide a spudger around the perimeter to release each clip without tearing foam.",
          tip: "Store the foam acoustic dampener ring carefully; it affects active noise cancellation performance."
        },
        {
          num: 2,
          title: "Remove Screws from Driver Baffle",
          detail: "Unscrew the three Phillips screws holding the speaker driver plate to the outer housing. Tilt the driver plate back gently.",
          tip: "Watch the thin red and black wires connected to the microphone capsules."
        },
        {
          num: 3,
          title: "Unplug JST Battery Connector",
          detail: "Locate the miniature 3-pin battery connector on the audio PCB. Use plastic tweezers to slide the connector straight out from the socket.",
          tip: "Never pull directly on the colored wires."
        },
        {
          num: 4,
          title: "Swap Battery & Secure with Cushion Foam",
          detail: "Pry out the old pouch battery from its adhesive nest. Drop in the new battery, connect the plug, reinstall the baffle screws, and snap the ear cushion into place.",
          tip: "Perform a quick Bluetooth pair check before snapping the final cushion clips."
        }
      ]
    },
    {
      id: "guide-macbook-thermal",
      title: "MacBook Air M1: Trackpad Replacement & Thermal Re-paste",
      category: "laptop",
      device: "Apple MacBook Air M1 (2020)",
      issueType: "performance",
      difficulty: "Advanced",
      timeEstimate: "45 â€“ 60 min",
      repairabilityScore: 4.8,
      costRangeDemo: "$34 â€“ $52",
      oemReplacementCost: "$229+ (Apple Store Trackpad/Topcase)",
      savingsEstimate: "~$180",
      safetyNote: "Touch ID sensor is paired to the M1 Secure Enclave. Only the trackpad should be swapped; do not damage the power button cable.",
      requiredTools: [
        "P5 Pentalobe Screwdriver",
        "Torx T3 & T5 Screwdrivers",
        "Plastic spudger",
        "Thermal Grizzly or high-grade thermal pad"
      ],
      requiredParts: [
        "Replacement Force Touch Trackpad assembly (A2337)",
        "Precision trackpad shim washers"
      ],
      steps: [
        {
          num: 1,
          title: "Remove Bottom Case P5 Screws",
          detail: "Remove 10 Pentalobe P5 screws. Use a suction cup near the rear hinge vent to pop the hidden aluminum clips, then slide the plate forward.",
          tip: "Keep track of screw lengths: rear screws are longer than front edge screws."
        },
        {
          num: 2,
          title: "Disconnect Battery Isolation Terminal",
          detail: "Peel back the battery connector cover. Unscrew the large T5 battery power screw and flip up the small battery data cable clip.",
          tip: "Confirm all power lights and indicators are dead before proceeding."
        },
        {
          num: 3,
          title: "Detach Trackpad Cable & Mounting Screws",
          detail: "Disconnect the trackpad ribbon cable from the motherboard. Remove the six Torx T5 screws securing the trackpad brackets to the unibody shell.",
          tip: "Retain the tiny silver shims under each screw mount to maintain perfect click depth."
        },
        {
          num: 4,
          title: "Align New Trackpad & Reassemble",
          detail: "Set the replacement trackpad into the recess, align spacing evenly with 0.2mm gap all around, snug the screws, and reconnect cables.",
          tip: "Test click feel before fully re-torquing the lower cover."
        }
      ]
    },
    {
      id: "guide-galaxy-usb",
      title: "Galaxy S22: USB-C Daughterboard & Mic Replacement",
      category: "phone",
      device: "Samsung Galaxy S22",
      issueType: "charging",
      difficulty: "Moderate",
      timeEstimate: "30 â€“ 40 min",
      repairabilityScore: 5.5,
      costRangeDemo: "$18 â€“ $30",
      oemReplacementCost: "$110 â€“ $140 (Authorized Center)",
      savingsEstimate: "~$85",
      safetyNote: "Glass back cover is brittle. Apply consistent, gentle heat (80Â°C) to loosen perimeter glue.",
      requiredTools: [
        "Phillips #00 Screwdriver",
        "Heat gun or hot air plate",
        "Plastic pry card",
        "B-7000 or pre-cut adhesive back tape"
      ],
      requiredParts: [
        "OEM Samsung Galaxy S22 Sub-board (Charging Port + Mic + SIM reader PCB)"
      ],
      steps: [
        {
          num: 1,
          title: "Heat and Remove Rear Glass Panel",
          detail: "Heat edges to 80Â°C for 3 minutes. Insert razor-thin plastic pick in lower seam, cutting through adhesive bead while keeping pick shallow.",
          tip: "Camera island glass is welded to rear panelâ€”lift gently around lens rims."
        },
        {
          num: 2,
          title: "Unscrew Lower Speaker Enclosure",
          detail: "Remove the 6 black Phillips screws holding the loudspeaker module at the bottom. Lift module to expose the sub-board.",
          tip: "Clean any dust accumulation from the speaker mesh chamber."
        },
        {
          num: 3,
          title: "Disconnect Main Interconnect & Antenna Coaxial Cables",
          detail: "Use plastic spudger to pop off the primary ribbon cables and two micro-coaxial RF antenna lines.",
          tip: "Do not bend the coaxial cables past 90 degrees."
        },
        {
          num: 4,
          title: "Swap Sub-board & Reseal",
          detail: "Unscrew single retaining screw, lever out old port PCB, seat new board, reconnect antennas with audible snap, test charging with USB multimeter, and apply fresh back seal.",
          tip: "Verify fast charging protocol triggers on screen before final glue curing."
        }
      ]
    }
  ],

  repairers: [
    {
      id: "rep-1",
      name: "CircuitCraft Community Labs",
      rating: 4.9,
      reviewCount: 142,
      distanceKm: "1.2 km away",
      address: "142 Greenpoint Ave, Brooklyn, NY (Simulated Demo)",
      verified: true,
      badges: ["Right-to-Repair Pledge", "Certified Independent", "Zero-Waste Shop"],
      specialties: ["Smartphones", "Micro-soldering", "MacBooks", "Audio"],
      turnaround: "Same-day screen/battery; 48h board repair",
      diagnosticFee: "Free diagnostic with repair ($20 stand-alone)",
      samplePricing: [
        { service: "Battery Replacement (Labor)", cost: "$35 â€“ $45" },
        { service: "Screen Replacement (Labor)", cost: "$40 â€“ $55" },
        { service: "Logic Board Ultrasonic Cleaning", cost: "$50" }
      ],
      contact: "hello@circuitcraft-demo.org",
      phone: "+1 (555) 234-7890",
      description: "Community-first repair cooperative offering transparent component-level repairs, schematic transparency, and monthly open DIY workshops."
    },
    {
      id: "rep-2",
      name: "Volt & Solder Precision Tech",
      rating: 4.8,
      reviewCount: 98,
      distanceKm: "3.4 km away",
      address: "88 Industrial Way, Queens, NY (Simulated Demo)",
      verified: true,
      badges: ["Certified Independent", "ESD Compliant"],
      specialties: ["Laptops", "Thermal Upgrades", "Data Recovery", "Port Soldering"],
      turnaround: "24 â€“ 48 hours typical",
      diagnosticFee: "Free preliminary visual inspection",
      samplePricing: [
        { service: "DC Jack / USB-C Port Re-soldering", cost: "$65 â€“ $85" },
        { service: "Thermal Paste & Deep Clean", cost: "$40" },
        { service: "Display Assembly Replacement", cost: "$50 â€“ $70" }
      ],
      contact: "service@voltsolder-demo.com",
      phone: "+1 (555) 345-8901",
      description: "Dedicated micro-electronics workshop equipped with stereo microscopes, hot-air rework stations, and authentic OEM-grade parts."
    },
    {
      id: "rep-3",
      name: "The Fixer's Guild & Repair CafÃ©",
      rating: 4.95,
      reviewCount: 215,
      distanceKm: "4.8 km away",
      address: "310 Hudson St, New York, NY (Simulated Demo)",
      verified: true,
      badges: ["Community Repair Cafe", "Right-to-Repair Pledge", "Non-Profit Partner"],
      specialties: ["Vintage Audio", "Home Electronics", "Smartphones", "Mentorship"],
      turnaround: "Every Saturday Walk-In or 3-5 days dropped off",
      diagnosticFee: "Donation-based (<script src="data.js"></script>â€“$15 suggested)",
      samplePricing: [
        { service: "Guided DIY Co-Repair (with technician coach)", cost: "Pay-what-you-can" },
        { service: "Headphone Cable / Jack Re-wiring", cost: "$20 â€“ $30" },
        { service: "Battery Swaps (All types)", cost: "$30 + part cost" }
      ],
      contact: "team@fixersguild-demo.org",
      phone: "+1 (555) 456-9012",
      description: "Hybrid volunteer repair cafÃ© and community lab teaching electronics autonomy and advocating against planned obsolescence."
    },
    {
      id: "rep-4",
      name: "Silicon Resurrect Labs",
      rating: 4.7,
      reviewCount: 64,
      distanceKm: "6.1 km away",
      address: "12 Pine St, Jersey City, NJ (Simulated Demo)",
      verified: true,
      badges: ["Refurbishment Certified", "e-Stewards Ally"],
      specialties: ["Gaming Consoles", "GPU Refurbishment", "Water Damage Remediation"],
      turnaround: "48 â€“ 72 hours",
      diagnosticFee: "$25 (Credited toward repair)",
      samplePricing: [
        { service: "HDMI Port Replacement (PS5 / Xbox)", cost: "$79 â€“ $95" },
        { service: "Liquid Damage Corrosion Bath", cost: "$65" },
        { service: "Joy-Con Hall-Effect Stick Upgrade", cost: "$35" }
      ],
      contact: "bench@siliconresurrect-demo.com",
      phone: "+1 (555) 567-0123",
      description: "Specialists in saving hardware other shops declare unfixable. Dedicated to rescuing gaming hardware and high-performance silicon."
    }
  ],

  secondLifePathways: [
    {
      id: "donate",
      title: "Donate for Digital Inclusion",
      tagline: "Empower students, seniors, and community centers",
      idealFor: "Working devices up to 7 years old with functional screens and batteries.",
      criteria: [
        "Device powers on and holds charge for at least 60 minutes",
        "Screen is readable without dangerous glass shards",
        "Operating system can browse modern web and install security updates",
        "All user accounts and Activation Locks are completely removed"
      ],
      whatHappens: "Partner non-profits clean, load educational software or lightweight Linux, and distribute to individuals lacking digital access.",
      carbonBenefit: "Saves ~85% of embodied carbon compared to manufacturing a new budget tablet/laptop."
    },
    {
      id: "refurbish",
      title: "Refurbish & Upcycle at Home",
      tagline: "Repurpose old hardware into smart home or utility devices",
      idealFor: "Slow or cosmetically damaged devices with working processors.",
      criteria: [
        "Can stay plugged into power",
        "WiFi or Bluetooth connection functions normally"
      ],
      ideas: [
        "Old Android Phone -> Dedicated Home Assistant dash or security IP camera (via open apps)",
        "Old Laptop -> Home media server, Plex host, or Pi-hole ad-blocking gateway",
        "Old Tablet -> Digital photo frame, recipe display, or bedside white-noise generator"
      ],
      whatHappens: "Zero transportation emissions, zero manufacturing impact, maximum practical utility."
    },
    {
      id: "sell",
      title: "Responsible Peer-to-Peer Resale",
      tagline: "Fair value recovery with full disclosure",
      idealFor: "Valuable devices under 4 years old that you simply no longer need.",
      criteria: [
        "Provide honest disclosure of battery health percentage",
        "List any cosmetic scuffs or replaced components",
        "Include original charger if possible to reduce cable waste"
      ],
      whatHappens: "Directly displaces demand for new retail units while putting money back into your pocket.",
      carbonBenefit: "Every secondary market transaction delays primary mining cycles."
    },
    {
      id: "recycle",
      title: "Certified Material Recovery (Recycling)",
      tagline: "Recover precious elements when repair or reuse is impossible",
      idealFor: "Crushed, corroded, or structurally dead devices beyond safe repair.",
      criteria: [
        "Device does not power on, board has structural breaks, or repair cost exceeds new price by 2x+",
        "Must be routed through R2v3 or e-Stewards certified facilities",
        "Never dump in household garbage (causes landfill lithium fires)"
      ],
      whatHappens: "Batteries are safely disassembled; circuit boards are smelted in closed-loop systems to recover gold, copper, palladium, and rare earths.",
      carbonBenefit: "Recycling gold from e-waste produces 80% fewer greenhouse emissions than primary ore mining."
    }
  ],

  secureEraseGuides: [
    {
      os: "iOS & iPadOS",
      name: "Apple iPhone & iPad",
      steps: [
        "Connect to Wi-Fi and complete an iCloud Backup (Settings -> [Your Name] -> iCloud -> iCloud Backup -> Back Up Now).",
        "Sign out of Apple ID / iCloud to disable 'Find My' Activation Lock (Settings -> [Your Name] -> Sign Out).",
        "Go to Settings -> General -> Transfer or Reset iPhone -> Erase All Content and Settings.",
        "Enter passcode if prompted. Apple's secure hardware encryption instantly obliterates the cryptographic keys, rendering storage irrecoverable.",
        "Verify: On reboot, the device should display the multi-language 'Hello' welcome screen."
      ]
    },
    {
      os: "Android",
      name: "Google Android (Samsung, Pixel, etc.)",
      steps: [
        "Back up photos and data to Google Drive or an external USB-C drive.",
        "CRITICAL: Remove Google Account first (Settings -> Passwords & Accounts -> Tap account -> Remove Account). This disables Factory Reset Protection (FRP) so the next owner can use it.",
        "Disable screen lock PIN/Pattern.",
        "Go to Settings -> System -> Reset Options -> Erase all data (factory reset).",
        "For modern Android devices (Android 10+), AES-256 hardware encryption is active by default; deleting the keys makes data unrecoverable."
      ]
    },
    {
      os: "Windows",
      name: "Windows 10 / 11 PC & Laptops",
      steps: [
        "Backup critical folders to an external hard drive or OneDrive.",
        "Go to Settings -> System -> Recovery -> Reset this PC -> Click 'Reset PC'.",
        "Choose 'Remove everything' (Do NOT choose 'Keep my files').",
        "Select 'Cloud download' or 'Local reinstall'.",
        "Under Additional Settings, click 'Change settings' and turn ON 'Clean data? Yes (Clean the drive)'. This writes zeros/random data over sectors so file recovery tools cannot salvage fragments.",
        "De-register the machine from your Microsoft Account Devices list at account.microsoft.com/devices."
      ]
    },
    {
      os: "macOS",
      name: "Apple Mac (Apple Silicon & Intel)",
      steps: [
        "Back up with Time Machine to an external drive.",
        "Sign out of iCloud (System Settings -> [Your Name] -> Sign Out).",
        "Unpair Bluetooth devices if selling locally.",
        "On Apple Silicon (M1/M2/M3) or T2 Intel Macs: Open System Settings -> General -> Transfer or Reset -> 'Erase All Content and Settings'. Follow the Erase Assistant.",
        "On older Intel Macs: Restart and hold Command + R to enter macOS Recovery -> Disk Utility -> Erase 'Macintosh HD' (APFS format) -> Reinstall macOS."
      ]
    }
  ],

  handoffChecklist: [
    { id: "c1", label: "Perform full cloud or physical drive backup of photos and documents", category: "Data" },
    { id: "c2", label: "Log out of primary accounts (Apple ID, Google, Microsoft, Steam)", category: "Accounts" },
    { id: "c3", label: "Disable anti-theft locks (Find My, Android FRP, BIOS passwords)", category: "Accounts" },
    { id: "c4", label: "Perform cryptographic factory reset and verify Hello/Setup screen", category: "Data" },
    { id: "c5", label: "Remove physical SIM card and MicroSD memory card", category: "Hardware" },
    { id: "c6", label: "Disinfect chassis with 70% isopropyl alcohol and a lint-free cloth", category: "Physical" },
    { id: "c7", label: "Bundle compatible power adapter, cable, or adapters if available", category: "Accessories" }
  ],

  impactBenchmarks: {
    // LCA references derived from Fraunhofer IZM, Fairphone LCA reports, and EPA WEEE data
    co2PerPhoneKg: 65,
    co2PerLaptopKg: 280,
    co2PerTabletKg: 120,
    ewasteWeightAvgKg: 0.85, // weighted average mixed electronics
    annualEwasteGlobalMillionTonnes: 62.0, // Global E-waste Monitor
    prematureDiscardRatePercent: 82, // devices replaced while still repairable/functional
    preciousMetalsPer1000Phones: {
      goldGrams: 34,
      silverGrams: 350,
      copperKg: 15,
      cobaltKg: 12
    }
  },

  pilotPlan: [
    {
      phase: "Phase 1: Foundation (Months 1â€“3)",
      milestone: "Community Repair Pilot",
      deliverables: [
        "Launch open repairability assessment rubric across top 50 consumer electronics models.",
        "Partner with 5 independent repair workshops in a pilot metropolitan area.",
        "Establish first physical 'CIRCULAR Drop & Diagnose' desk at a university makerspace."
      ]
    },
    {
      phase: "Phase 2: Network & Parts (Months 4â€“7)",
      milestone: "Open Parts Transparency API",
      deliverables: [
        "Aggregate verified independent parts vendors (iFixit, MobileSentrix, Framework open catalog).",
        "Launch Digital Product Passport (DPP) readiness preview with serialized repair logging.",
        "Integrate verified e-Stewards / R2 certified recycler drop-off locator."
      ]
    },
    {
      phase: "Phase 3: Circular Scaling (Months 8â€“12)",
      milestone: "Enterprise & Municipal Circularity",
      deliverables: [
        "Expand corporate device lifecycle tracker for universities and local businesses.",
        "Introduce verifiable impact audit certificates for repaired and diverted devices.",
        "Public API for municipal waste management authorities to divert electronics prior to incinerators."
      ]
    }
  ]
};

</script>
  <script>
/**
 * CIRCULAR â€” Digital Platform Application Logic
 * Challenge: IMX26-PS07 â€” CEDA-EPS
 * 
 * Interactive logic for:
 * - Multi-step Device Checker with real-time diagnostic synthesis
 * - Repair Library with multi-attribute filtering & interactive step-by-step guide viewer
 * - Vetted Repairer Network directory with quote request and service listing modals
 * - Second Life secure erasure OS tabs and interactive pre-handoff checklist
 * - Live Impact Simulator with dynamic LCA calculations
 * - Hackathon Judge storytelling & pilot roadmap
 */

(function () {
  'use strict';

  // --- STATE STORE ---
  const state = {
    currentRoute: 'home',
    checker: {
      step: 1,
      category: 'phone',
      model: '',
      isModelUnknown: false,
      issue: 'battery',
      age: '1-3',
      powersOn: 'yes',
      symptoms: []
    },
    library: {
      searchQuery: '',
      categoryFilter: 'all',
      difficultyFilter: 'all',
      timeFilter: 'all'
    },
    network: {
      searchQuery: '',
      specialtyFilter: 'all'
    },
    secondLife: {
      activeOs: 'iOS & iPadOS',
      checkedItems: new Set(['c1'])
    },
    impact: {
      devicesCount: 2500,
      lifespanMonths: 18
    },
    activeGuide: null
  };

  // --- DOM READY INIT ---
  document.addEventListener('DOMContentLoaded', () => {
    initNavigation();
    initDeviceChecker();
    initRepairLibrary();
    initRepairNetwork();
    initSecondLife();
    initImpactSimulator();
    initModals();
    handleRouteFromHash();
  });

  // ==========================================================================
  // NAVIGATION & ROUTING
  // ==========================================================================

  function initNavigation() {
    const navLinks = document.querySelectorAll('.nav-link, .route-trigger');
    const mobileToggle = document.getElementById('mobileMenuToggle');
    const mobileDrawer = document.getElementById('mobileMenuDrawer');

    navLinks.forEach(link => {
      link.addEventListener('click', (e) => {
        const route = link.getAttribute('data-route') || link.getAttribute('href')?.replace('#', '');
        if (route && document.getElementById(route)) {
          e.preventDefault();
          navigateTo(route);
          if (mobileDrawer) mobileDrawer.classList.remove('open');
        }
      });
    });

    if (mobileToggle && mobileDrawer) {
      mobileToggle.addEventListener('click', () => {
        mobileDrawer.classList.toggle('open');
      });
    }

    window.addEventListener('hashchange', handleRouteFromHash);

    // Header shadow on scroll
    window.addEventListener('scroll', () => {
      const header = document.querySelector('.site-header');
      if (header) {
        if (window.scrollY > 20) {
          header.classList.add('scrolled');
        } else {
          header.classList.remove('scrolled');
        }
      }
    });
  }

  function handleRouteFromHash() {
    const hash = window.location.hash.replace('#', '');
    if (hash && document.getElementById(hash)) {
      navigateTo(hash, false);
    } else {
      navigateTo('home', false);
    }
  }

  function navigateTo(routeId, updateHash = true) {
    state.currentRoute = routeId;

    // Update nav links active state
    document.querySelectorAll('.nav-link').forEach(link => {
      if (link.getAttribute('data-route') === routeId) {
        link.classList.add('active');
      } else {
        link.classList.remove('active');
      }
    });

    // Scroll to section smoothly
    const targetEl = document.getElementById(routeId);
    if (targetEl) {
      const headerOffset = 80;
      const elementPosition = targetEl.getBoundingClientRect().top;
      const offsetPosition = elementPosition + window.pageYOffset - headerOffset;

      window.scrollTo({
        top: offsetPosition,
        behavior: 'smooth'
      });
    }

    if (updateHash && window.location.hash !== `#${routeId}`) {
      history.pushState(null, null, `#${routeId}`);
    }
  }

  // ==========================================================================
  // DEVICE CHECKER (CORE DEMO FLOW)
  // ==========================================================================

  function initDeviceChecker() {
    renderCategorySelection();
    renderModelPresets();
    renderIssueSelection();
    setupCheckerControls();
  }

  function renderCategorySelection() {
    const container = document.getElementById('checkerCategoryGrid');
    if (!container) return;

    container.innerHTML = CIRCULAR_DATA.deviceCategories.map(cat => `
      <button type="button" class="category-card-btn ${state.checker.category === cat.id ? 'selected' : ''}" data-category="${cat.id}">
        <div class="cat-icon-frame">
          ${getCategorySvgIcon(cat.id)}
        </div>
        <div class="cat-label">${cat.name}</div>
      </button>
    `).join('');

    container.querySelectorAll('.category-card-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        container.querySelectorAll('.category-card-btn').forEach(b => b.classList.remove('selected'));
        btn.classList.add('selected');
        state.checker.category = btn.getAttribute('data-category');
        renderModelPresets();
      });
    });
  }

  function renderModelPresets() {
    const presetsContainer = document.getElementById('modelPresetsRow');
    const modelInput = document.getElementById('customModelInput');
    const unknownCheckbox = document.getElementById('unknownModelCheckbox');

    if (!presetsContainer) return;

    const currentCatObj = CIRCULAR_DATA.deviceCategories.find(c => c.id === state.checker.category) || CIRCULAR_DATA.deviceCategories[0];
    const models = currentCatObj.popularModels || [];

    presetsContainer.innerHTML = models.map(m => `
      <button type="button" class="model-preset-pill ${state.checker.model === `${m.brand} ${m.model}` ? 'selected' : ''}" data-model="${m.brand} ${m.model}">
        ${m.brand} ${m.model}
      </button>
    `).join('');

    presetsContainer.querySelectorAll('.model-preset-pill').forEach(pill => {
      pill.addEventListener('click', () => {
        presetsContainer.querySelectorAll('.model-preset-pill').forEach(p => p.classList.remove('selected'));
        pill.classList.add('selected');
        state.checker.model = pill.getAttribute('data-model');
        if (modelInput) modelInput.value = state.checker.model;
        if (unknownCheckbox) unknownCheckbox.checked = false;
        state.checker.isModelUnknown = false;
      });
    });

    if (modelInput) {
      modelInput.addEventListener('input', (e) => {
        state.checker.model = e.target.value;
        presetsContainer.querySelectorAll('.model-preset-pill').forEach(p => p.classList.remove('selected'));
        if (unknownCheckbox) unknownCheckbox.checked = false;
        state.checker.isModelUnknown = false;
      });
    }

    if (unknownCheckbox) {
      unknownCheckbox.addEventListener('change', (e) => {
        state.checker.isModelUnknown = e.target.checked;
        if (e.target.checked) {
          state.checker.model = `Generic ${currentCatObj.name} (Assisted Detection)`;
          if (modelInput) modelInput.value = '';
          presetsContainer.querySelectorAll('.model-preset-pill').forEach(p => p.classList.remove('selected'));
        }
      });
    }
  }

  function renderIssueSelection() {
    const container = document.getElementById('checkerIssueGrid');
    if (!container) return;

    container.innerHTML = CIRCULAR_DATA.issueTaxonomy.map(issue => `
      <button type="button" class="issue-card-btn ${state.checker.issue === issue.id ? 'selected' : ''}" data-issue="${issue.id}">
        <div class="issue-card-header">
          <div class="issue-icon">${getIssueSvgIcon(issue.id)}</div>
          ${issue.hasSafetyRisk ? '<span class="rep-badge" style="background:#FEE2E2;color:#991B1B;">Safety Precaution</span>' : ''}
        </div>
        <div class="issue-title">${issue.label}</div>
        <div class="issue-symptoms-list">
          ${issue.typicalSymptoms.slice(0, 2).map(s => `<span>â€¢ ${s}</span>`).join('')}
        </div>
      </button>
    `).join('');

    container.querySelectorAll('.issue-card-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        container.querySelectorAll('.issue-card-btn').forEach(b => b.classList.remove('selected'));
        btn.classList.add('selected');
        state.checker.issue = btn.getAttribute('data-issue');
        updateSymptomChecklistForIssue();
      });
    });
  }

  function updateSymptomChecklistForIssue() {
    const checklistContainer = document.getElementById('symptomsContextList');
    if (!checklistContainer) return;

    const issueObj = CIRCULAR_DATA.issueTaxonomy.find(i => i.id === state.checker.issue) || CIRCULAR_DATA.issueTaxonomy[0];
    checklistContainer.innerHTML = issueObj.typicalSymptoms.map((symptom, idx) => `
      <label class="checkbox-custom-item">
        <input type="checkbox" name="symptom" value="${symptom}" ${idx === 0 ? 'checked' : ''}>
        <span>${symptom}</span>
      </label>
    `).join('');
  }

  function setupCheckerControls() {
    const btnNext = document.getElementById('checkerNextBtn');
    const btnBack = document.getElementById('checkerBackBtn');
    const btnRestart = document.getElementById('checkerRestartBtn');

    // Age pill selection
    document.querySelectorAll('.age-choice-pill').forEach(pill => {
      pill.addEventListener('click', () => {
        document.querySelectorAll('.age-choice-pill').forEach(p => p.classList.remove('selected'));
        pill.classList.add('selected');
        state.checker.age = pill.getAttribute('data-age');
      });
    });

    // Powers-on pill selection
    document.querySelectorAll('.power-choice-pill').forEach(pill => {
      pill.addEventListener('click', () => {
        document.querySelectorAll('.power-choice-pill').forEach(p => p.classList.remove('selected'));
        pill.classList.add('selected');
        state.checker.powersOn = pill.getAttribute('data-power');
      });
    });

    if (btnNext) {
      btnNext.addEventListener('click', () => {
        if (state.checker.step < 4) {
          // Validation for step 2: model
          if (state.checker.step === 2 && !state.checker.model && !state.checker.isModelUnknown) {
            const currentCat = CIRCULAR_DATA.deviceCategories.find(c => c.id === state.checker.category);
            state.checker.model = currentCat ? `${currentCat.name} (General)` : "Standard Electronics Model";
          }
          goToCheckerStep(state.checker.step + 1);
        } else if (state.checker.step === 4) {
          // Run diagnosis simulation
          runDiagnosisSimulation();
        }
      });
    }

    if (btnBack) {
      btnBack.addEventListener('click', () => {
        if (state.checker.step > 1) {
          goToCheckerStep(state.checker.step - 1);
        }
      });
    }

    if (btnRestart) {
      btnRestart.addEventListener('click', resetChecker);
    }
  }

  function goToCheckerStep(stepNumber) {
    state.checker.step = stepNumber;

    // Update tab bar
    document.querySelectorAll('.step-tab').forEach(tab => {
      const tabNum = parseInt(tab.getAttribute('data-step-num'), 10);
      tab.classList.remove('active', 'completed');
      if (tabNum === stepNumber) {
        tab.classList.add('active');
      } else if (tabNum < stepNumber) {
        tab.classList.add('completed');
      }
    });

    // Switch panes
    document.querySelectorAll('.checker-step-pane').forEach(pane => {
      pane.classList.remove('active');
    });

    const activePane = document.getElementById(`checkerStep${stepNumber}`);
    if (activePane) activePane.classList.add('active');

    // Update button states
    const btnBack = document.getElementById('checkerBackBtn');
    const btnNext = document.getElementById('checkerNextBtn');

    if (btnBack) {
      btnBack.style.visibility = stepNumber === 1 ? 'hidden' : 'visible';
    }

    if (btnNext) {
      if (stepNumber === 4) {
        btnNext.innerHTML = 'Synthesize Diagnosis & Report <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M5 12h14M12 5l7 7-7 7"/></svg>';
        btnNext.className = 'btn btn-lime';
      } else {
        btnNext.innerHTML = 'Continue <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M5 12h14M12 5l7 7-7 7"/></svg>';
        btnNext.className = 'btn btn-primary';
      }
    }

    if (stepNumber === 4) {
      updateSymptomChecklistForIssue();
    }
  }

  function runDiagnosisSimulation() {
    // Show loading pane
    document.querySelectorAll('.checker-step-pane').forEach(p => p.classList.remove('active'));
    const loadingPane = document.getElementById('checkerLoadingScreen');
    if (loadingPane) loadingPane.classList.add('active');

    const footer = document.querySelector('.checker-footer');
    if (footer) footer.style.display = 'none';

    const logMessages = [
      "Analyzing hardware disassembly complexity...",
      "Querying open parts availability & authorized telemetry...",
      "Evaluating safety hazard threshold (Lithium / HV)...",
      "Calculating embodied carbon & comparative savings...",
      "Generating tailored circular recommendation..."
    ];

    const logEl = document.getElementById('loadingDynamicLog');
    let logIdx = 0;

    const interval = setInterval(() => {
      if (logEl && logIdx < logMessages.length) {
        logEl.textContent = logMessages[logIdx];
        logIdx++;
      }
    }, 450);

    setTimeout(() => {
      clearInterval(interval);
      if (loadingPane) loadingPane.classList.remove('active');
      renderDiagnosisResult();
      const resultPane = document.getElementById('checkerStep5');
      if (resultPane) resultPane.classList.add('active');
    }, 2400);
  }

  function renderDiagnosisResult() {
    const container = document.getElementById('diagnosisResultContent');
    if (!container) return;

    const catObj = CIRCULAR_DATA.deviceCategories.find(c => c.id === state.checker.category) || CIRCULAR_DATA.deviceCategories[0];
    const issueObj = CIRCULAR_DATA.issueTaxonomy.find(i => i.id === state.checker.issue) || CIRCULAR_DATA.issueTaxonomy[0];
    const deviceName = state.checker.model || `${catObj.name} (Assisted Detection)`;

    // Calculate simulated repairability score
    let baseScore = 7.0;
    if (catObj.id === 'phone') baseScore = 6.8;
    if (catObj.id === 'laptop') baseScore = 8.2;
    if (catObj.id === 'tablet') baseScore = 4.5;
    if (catObj.id === 'audio') baseScore = 7.4;
    if (state.checker.issue === 'board') baseScore -= 1.8;
    if (state.checker.issue === 'battery') baseScore += 0.5;
    if (state.checker.powersOn === 'no') baseScore -= 1.2;

    const finalScore = Math.max(2.5, Math.min(9.8, baseScore)).toFixed(1);

    // Decision Logic for Recommended Next Step
    let recommendedStep = "DIY Guide Recommended";
    let stepBadgeColor = "var(--lime-400)";
    let recommendedAction = "view-guide";

    if (state.checker.issue === 'board' || state.checker.powersOn === 'no' || state.checker.issue === 'liquid') {
      recommendedStep = "Professional Repairer Recommended (Micro-soldering/Depot)";
      stepBadgeColor = "#FEF08A";
      recommendedAction = "find-repairer";
    } else if (state.checker.age === '5+' && state.checker.powersOn === 'no') {
      recommendedStep = "Responsible Material Recovery (Recycle / Harvesting)";
      stepBadgeColor = "#D8EADF";
      recommendedAction = "second-life";
    }

    // Savings Calculation
    const estNewCost = catObj.id === 'laptop' ? 950 : (catObj.id === 'phone' ? 799 : 320);
    const estDiyCost = state.checker.issue === 'battery' ? 35 : (state.checker.issue === 'screen' ? 75 : 25);
    const estProCost = estDiyCost + 45;
    const co2Saved = catObj.embodiedCo2Kg;

    // Safety Alert Box content
    let safetyBannerHtml = '';
    if (state.checker.issue === 'battery') {
      safetyBannerHtml = `
        <div class="safety-alert-box danger">
          <div class="safety-alert-icon">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="m21.73 18-8-14a2 2 0 0 0-3.48 0l-8 14A2 2 0 0 0 4 21h16a2 2 0 0 0 1.73-3Z"/><line x1="12" y1="9" x2="12" y2="13"/><line x1="12" y1="17" x2="12.01" y2="17"/></svg>
          </div>
          <div>
            <div class="safety-alert-title">LITHIUM-ION SAFETY PROTOCOL REQUIRED</div>
            <div class="safety-alert-text">
              If your device display is bulging or the chassis is separating, your battery may be swollen. 
              <strong>Do NOT puncture, crush, or apply heat above 85Â°C.</strong> Discharge to below 25% charge before attempting service or transport.
            </div>
          </div>
        </div>
      `;
    } else if (state.checker.issue === 'liquid') {
      safetyBannerHtml = `
        <div class="safety-alert-box danger">
          <div class="safety-alert-icon">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M12 2v20M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"/></svg>
          </div>
          <div>
            <div class="safety-alert-title">ACTIVE CORROSION RISK (DO NOT CHARGE)</div>
            <div class="safety-alert-text">
              Plugging a moisture-exposed device into power causes rapid electrochemical galvanic corrosion on motherboard traces. Keep the device unpowered and consult an ultrasonic cleaning specialist immediately.
            </div>
          </div>
        </div>
      `;
    } else {
      safetyBannerHtml = `
        <div class="safety-alert-box">
          <div class="safety-alert-icon">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><circle cx="12" cy="12" r="10"/><line x1="12" y1="8" x2="12" y2="12"/><line x1="12" y1="16" x2="12.01" y2="16"/></svg>
          </div>
          <div>
            <div class="safety-alert-title">PRE-REPAIR ESD SAFETY ADVISORY</div>
            <div class="safety-alert-text">
              Always disconnect internal battery connections before touching display ribbons or memory slots to prevent blowing motherboard backlight fuses.
            </div>
          </div>
        </div>
      `;
    }

    container.innerHTML = `
      <div class="diagnosis-result-wrap">
        <!-- Hero Result Card -->
        <div class="result-hero-banner">
          <div class="result-banner-top">
            <span class="estimate-notice">PRELIMINARY ASSESSMENT â€¢ ILLUSTRATIVE DEMO ESTIMATE</span>
            <span class="rep-badge" style="background:${stepBadgeColor}; color:var(--forest-900); font-weight:800;">
              ${recommendedStep}
            </span>
          </div>
          <div class="result-device-title">${deviceName}</div>
          <div style="color:var(--charcoal-200); font-size:0.95rem; margin-top:0.35rem;">
            Primary Symptom Identified: <strong>${issueObj.label}</strong> (Reported Age: ${state.checker.age} years)
          </div>

          <div class="result-summary-grid">
            <div class="result-metric-card">
              <div class="metric-lbl">Repairability Index</div>
              <div class="metric-val-main lime">${finalScore} / 10</div>
              <div class="metric-sub">Open Rubric Metric</div>
            </div>
            <div class="result-metric-card">
              <div class="metric-lbl">Est. DIY Parts</div>
              <div class="metric-val-main">${estDiyCost} â€“ ${estDiyCost + 20}</div>
              <div class="metric-sub">Demo market average</div>
            </div>
            <div class="result-metric-card">
              <div class="metric-lbl">Est. Pro Labor</div>
              <div class="metric-val-main">${estProCost} â€“ ${estProCost + 25}</div>
              <div class="metric-sub">Independent shop</div>
            </div>
            <div class="result-metric-card">
              <div class="metric-lbl">Avoided COâ‚‚e</div>
              <div class="metric-val-main lime">~${co2Saved} kg</div>
              <div class="metric-sub">Embodied carbon</div>
            </div>
          </div>
        </div>

        <!-- Safety Banner -->
        ${safetyBannerHtml}

        <!-- Compare Repair vs Replacement -->
        <div class="compare-container">
          <div class="compare-heading">
            <span>Direct Comparison: Repair vs Buying Replacement</span>
            <span style="font-size:0.8125rem; font-family:var(--font-mono); color:var(--forest-600); font-weight:700;">CIRCULAR IMPACT BENEFIT</span>
          </div>
          <div class="compare-grid">
            <div class="compare-column repair">
              <div class="col-tag">Option A: Repair & Keep Device</div>
              <div class="col-price">${estDiyCost} â€“ ${estProCost}</div>
              <div class="col-desc">Complete functional restoration with new battery/display</div>
              <ul class="compare-benefits-list">
                <li><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" color="#16A34A"><polyline points="20 6 9 17 4 12"/></svg> Keeps ~${estNewCost - estProCost} in your wallet</li>
                <li><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" color="#16A34A"><polyline points="20 6 9 17 4 12"/></svg> Zero data migration downtime</li>
                <li><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" color="#16A34A"><polyline points="20 6 9 17 4 12"/></svg> Eliminates ${co2Saved} kg of supply-chain COâ‚‚e</li>
                <li><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" color="#16A34A"><polyline points="20 6 9 17 4 12"/></svg> Preserves rare earths & prevents landfilling</li>
              </ul>
            </div>

            <div class="compare-column replace">
              <div class="col-tag">Option B: Buy New Replacement</div>
              <div class="col-price">${estNewCost}+</div>
              <div class="col-desc">Retail purchasing cycle for brand-new device</div>
              <ul class="compare-benefits-list">
                <li><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" color="#DC2626"><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg> High financial expenditure</li>
                <li><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" color="#DC2626"><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg> Old unit often sits in drawer or gets discarded</li>
                <li><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" color="#DC2626"><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg> Triggers additional 100+ kg mining footprint</li>
                <li><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" color="#DC2626"><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg> Account setup & backup restoration overhead</li>
              </ul>
            </div>
          </div>
        </div>

        <!-- Parts & Tools Checklist -->
        <div class="parts-tools-panel">
          <div>
            <div class="panel-block-title">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M14.7 6.3a1 1 0 0 0 0 1.4l1.6 1.6a1 1 0 0 0 1.4 0l3.77-3.77a6 6 0 0 1-7.94 7.94l-6.91 6.91a2.12 2.12 0 0 1-3-3l6.91-6.91a6 6 0 0 1 7.94-7.94l-3.76 3.76z"/></svg>
              Essential Tools Checklist
            </div>
            <ul class="checklist-list">
              <li class="checklist-item"><input type="checkbox" checked> Precision Driver Set (Phillips #00, Torx T5 / Pentalobe)</li>
              <li class="checklist-item"><input type="checkbox" checked> Anti-static Plastic Spudger / Guitar Picks</li>
              <li class="checklist-item"><input type="checkbox"> Suction Display Handle / iSclack</li>
              <li class="checklist-item"><input type="checkbox"> Low-temperature Heat Pad or Hairdryer (75Â°C)</li>
            </ul>
          </div>
          <div>
            <div class="panel-block-title">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><rect width="18" height="18" x="3" y="3" rx="2"/><path d="M7 7h.01M17 7h.01M7 17h.01M17 17h.01"/></svg>
              Suggested Replacement Parts
            </div>
            <ul class="checklist-list">
              <li class="checklist-item"><input type="checkbox" checked> OEM-grade ${issueObj.label.split(' ')[0]} Replacement Assembly</li>
              <li class="checklist-item"><input type="checkbox" checked> Pre-cut perimeter water-resistant gasket adhesive</li>
              <li class="checklist-item"><input type="checkbox"> Stretch-release battery pull-tabs</li>
            </ul>
          </div>
        </div>

        <!-- Action Buttons -->
        <div class="result-actions-bar">
          <div style="display:flex; gap:0.75rem; flex-wrap:wrap;">
            <button type="button" class="btn btn-lime" id="resultJumpGuideBtn">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z"/><path d="M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z"/></svg>
              Open Step-by-Step DIY Guide
            </button>
            <button type="button" class="btn btn-secondary" id="resultJumpNetworkBtn">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z"/><circle cx="12" cy="10" r="3"/></svg>
              Find Local Repair Shop
            </button>
          </div>
          <div style="display:flex; gap:0.75rem;">
            <button type="button" class="btn btn-ghost" id="resultExportBtn">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>
              Export Assessment Summary
            </button>
            <button type="button" class="btn btn-secondary" id="resultStartOverBtn">Start Over</button>
          </div>
        </div>
      </div>
    `;

    // Wire Result Buttons
    document.getElementById('resultJumpGuideBtn')?.addEventListener('click', () => {
      // Find matching guide or first guide
      const matchingGuide = CIRCULAR_DATA.repairGuides.find(g => g.category === state.checker.category) || CIRCULAR_DATA.repairGuides[0];
      navigateTo('guides');
      openGuideModal(matchingGuide.id);
    });

    document.getElementById('resultJumpNetworkBtn')?.addEventListener('click', () => {
      navigateTo('network');
      showToast('Filtered nearby vetted repair shops based on your diagnosis.', 'success');
    });

    document.getElementById('resultExportBtn')?.addEventListener('click', () => {
      exportDiagnosisSummary(deviceName, finalScore, issueObj.label, co2Saved);
    });

    document.getElementById('resultStartOverBtn')?.addEventListener('click', resetChecker);
  }

  function exportDiagnosisSummary(device, score, issue, co2) {
    const summaryText = `CIRCULAR ASSESSMENT SUMMARY\n----------------------------------\nChallenge: IMX26-PS07 â€” CEDA-EPS\nDevice: ${device}\nIssue: ${issue}\nRepairability Score: ${score}/10\nEmbodied CO2e Saved: ~${co2} kg\nAssessment Timestamp: ${new Date().toLocaleDateString()}\nStatus: Verified Prototype Assessment`;
    
    // Copy to clipboard & notify
    navigator.clipboard?.writeText(summaryText).then(() => {
      showToast('Diagnosis assessment copied to clipboard! Ready to share with your repair technician.', 'success');
    }).catch(() => {
      showToast(`Diagnosis for ${device} generated successfully!`, 'success');
    });
  }

  function resetChecker() {
    state.checker.step = 1;
    const footer = document.querySelector('.checker-footer');
    if (footer) footer.style.display = 'flex';
    goToCheckerStep(1);
  }

  // ==========================================================================
  // REPAIR LIBRARY
  // ==========================================================================

  function initRepairLibrary() {
    renderRepairGuides();

    const searchInput = document.getElementById('guideSearchInput');
    const difficultySelect = document.getElementById('guideDifficultySelect');
    const categoryPills = document.querySelectorAll('.guide-category-pill');

    if (searchInput) {
      searchInput.addEventListener('input', (e) => {
        state.library.searchQuery = e.target.value.toLowerCase();
        renderRepairGuides();
      });
    }

    if (difficultySelect) {
      difficultySelect.addEventListener('change', (e) => {
        state.library.difficultyFilter = e.target.value;
        renderRepairGuides();
      });
    }

    categoryPills.forEach(pill => {
      pill.addEventListener('click', () => {
        categoryPills.forEach(p => p.classList.remove('active'));
        pill.classList.add('active');
        state.library.categoryFilter = pill.getAttribute('data-cat');
        renderRepairGuides();
      });
    });
  }

  function renderRepairGuides() {
    const container = document.getElementById('repairGuidesGrid');
    if (!container) return;

    const filtered = CIRCULAR_DATA.repairGuides.filter(guide => {
      const matchSearch = guide.title.toLowerCase().includes(state.library.searchQuery) ||
                          guide.device.toLowerCase().includes(state.library.searchQuery) ||
                          guide.requiredTools.some(t => t.toLowerCase().includes(state.library.searchQuery));
      
      const matchCat = state.library.categoryFilter === 'all' || guide.category === state.library.categoryFilter;
      const matchDiff = state.library.difficultyFilter === 'all' || guide.difficulty.toLowerCase() === state.library.difficultyFilter.toLowerCase();

      return matchSearch && matchCat && matchDiff;
    });

    if (filtered.length === 0) {
      container.innerHTML = `
        <div style="grid-column: 1 / -1; text-align:center; padding:3rem; background:var(--bg-card); border-radius:var(--radius-lg); border:1px dashed var(--border-card);">
          <div style="color:var(--forest-600); margin-bottom:0.75rem;">
            <svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" style="margin:0 auto;"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>
          </div>
          <div style="font-weight:800; font-size:1.15rem; color:var(--forest-900);">No matching repair guides found</div>
          <p style="color:var(--charcoal-600); font-size:0.875rem; margin-top:0.25rem;">Try adjusting your search terms or clearing your difficulty filter.</p>
        </div>
      `;
      return;
    }

    container.innerHTML = filtered.map(guide => `
      <div class="guide-card" data-guide-id="${guide.id}">
        <div class="guide-top-meta">
          <span class="difficulty-badge ${guide.difficulty}">${guide.difficulty}</span>
          <div class="guide-time-pill">
            <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
            ${guide.timeEstimate}
          </div>
        </div>

        <div class="guide-device-name">${guide.device}</div>
        <div class="guide-title">${guide.title}</div>

        <div class="guide-tags-row">
          ${guide.requiredTools.slice(0, 3).map(tool => `<span class="guide-tool-tag">${tool.split('(')[0]}</span>`).join('')}
          ${guide.requiredTools.length > 3 ? `<span class="guide-tool-tag">+${guide.requiredTools.length - 3} more</span>` : ''}
        </div>

        <div class="guide-card-footer">
          <div class="cost-savings-snippet">
            Parts: <strong>${guide.costRangeDemo}</strong> (Saves ${guide.savingsEstimate})
          </div>
          <button type="button" class="btn btn-sm btn-secondary view-guide-btn" data-guide-id="${guide.id}">
            View Guide
          </button>
        </div>
      </div>
    `).join('');

    container.querySelectorAll('.guide-card, .view-guide-btn').forEach(el => {
      el.addEventListener('click', (e) => {
        const guideId = el.getAttribute('data-guide-id');
        if (guideId) openGuideModal(guideId);
      });
    });
  }

  function openGuideModal(guideId) {
    const guide = CIRCULAR_DATA.repairGuides.find(g => g.id === guideId);
    if (!guide) return;

    state.activeGuide = guide;
    const modal = document.getElementById('guideModal');
    const titleEl = document.getElementById('guideModalTitle');
    const bodyEl = document.getElementById('guideModalBody');

    if (!modal || !titleEl || !bodyEl) return;

    titleEl.textContent = guide.title;

    bodyEl.innerHTML = `
      <div style="display:flex; justify-content:space-between; flex-wrap:wrap; gap:1rem; padding-bottom:1rem; border-bottom:1px solid var(--border-subtle);">
        <div>
          <div style="font-size:0.8125rem; font-family:var(--font-mono); color:var(--forest-600); font-weight:700;">DEMONSTRATION GUIDE â€¢ INFORMATIONAL USE ONLY</div>
          <div style="font-size:1.15rem; font-weight:800; color:var(--forest-900);">${guide.device}</div>
        </div>
        <div style="display:flex; gap:0.5rem; align-items:center;">
          <span class="difficulty-badge ${guide.difficulty}">${guide.difficulty}</span>
          <span class="rep-badge">Est. Time: ${guide.timeEstimate}</span>
          <span class="rep-badge" style="background:var(--lime-400); color:var(--forest-900);">Score: ${guide.repairabilityScore}/10</span>
        </div>
      </div>

      <!-- Safety Alert Box -->
      <div class="safety-alert-box danger">
        <div class="safety-alert-icon">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="m21.73 18-8-14a2 2 0 0 0-3.48 0l-8 14A2 2 0 0 0 4 21h16a2 2 0 0 0 1.73-3Z"/><line x1="12" y1="9" x2="12" y2="13"/><line x1="12" y1="17" x2="12.01" y2="17"/></svg>
        </div>
        <div>
          <div class="safety-alert-title">SAFETY FIRST: MANDATORY PRECAUTION</div>
          <div class="safety-alert-text">${guide.safetyNote}</div>
        </div>
      </div>

      <!-- Parts & Tools Checklist -->
      <div class="parts-tools-panel">
        <div>
          <div class="panel-block-title">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M14.7 6.3a1 1 0 0 0 0 1.4l1.6 1.6a1 1 0 0 0 1.4 0l3.77-3.77a6 6 0 0 1-7.94 7.94l-6.91 6.91a2.12 2.12 0 0 1-3-3l6.91-6.91a6 6 0 0 1 7.94-7.94l-3.76 3.76z"/></svg>
            Required Tools
          </div>
          <ul class="checklist-list">
            ${guide.requiredTools.map(t => `<li class="checklist-item"><input type="checkbox"> <span>${t}</span></li>`).join('')}
          </ul>
        </div>
        <div>
          <div class="panel-block-title">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><rect width="18" height="18" x="3" y="3" rx="2"/><path d="M7 7h.01M17 7h.01M7 17h.01M17 17h.01"/></svg>
            Replacement Parts (${guide.costRangeDemo})
          </div>
          <ul class="checklist-list">
            ${guide.requiredParts.map(p => `<li class="checklist-item"><input type="checkbox"> <span>${p}</span></li>`).join('')}
          </ul>
        </div>
      </div>

      <!-- Step by Step Instructions -->
      <div>
        <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:1.25rem;">
          <div style="font-size:1.15rem; font-weight:800; color:var(--forest-900);">Step-by-Step Instructions</div>
          <div style="font-size:0.8125rem; font-family:var(--font-mono); color:var(--forest-600);" id="guideStepCounter">0 of ${guide.steps.length} Steps Completed</div>
        </div>

        <div style="display:flex; flex-direction:column; gap:1.25rem;">
          ${guide.steps.map(step => `
            <div style="background:var(--bg-subtle); border:1px solid var(--border-subtle); border-radius:var(--radius-md); padding:1.25rem;">
              <div style="display:flex; align-items:center; justify-content:space-between; margin-bottom:0.65rem;">
                <div style="display:flex; align-items:center; gap:0.65rem;">
                  <span class="step-circle-num">${step.num}</span>
                  <span style="font-size:1.05rem; font-weight:800; color:var(--forest-900);">${step.title}</span>
                </div>
                <label style="display:flex; align-items:center; gap:0.4rem; font-size:0.8125rem; font-weight:700; cursor:pointer;">
                  <input type="checkbox" class="guide-step-cb" data-step="${step.num}">
                  <span>Complete</span>
                </label>
              </div>
              <p style="font-size:0.9375rem; color:var(--charcoal-700); line-height:1.55; margin-left:2.65rem;">
                ${step.detail}
              </p>
              ${step.tip ? `
                <div style="margin-top:0.75rem; margin-left:2.65rem; background:rgba(200,255,50,0.15); border-left:3px solid var(--forest-800); padding:0.5rem 0.75rem; border-radius:0 var(--radius-sm) var(--radius-sm) 0; font-size:0.8125rem; color:var(--forest-900);">
                  <strong>Technician Tip:</strong> ${step.tip}
                </div>
              ` : ''}
            </div>
          `).join('')}
        </div>
      </div>

      <div style="display:flex; justify-content:space-between; align-items:center; padding-top:1.25rem; border-top:1px solid var(--border-subtle);">
        <span style="font-size:0.775rem; color:var(--charcoal-500);">Disclaimer: Informational community content. Always take appropriate ESD and eye safety precautions.</span>
        <button type="button" class="btn btn-secondary modal-close-btn-inline">Close Guide</button>
      </div>
    `;

    // Interactive step tracker
    const stepBoxes = bodyEl.querySelectorAll('.guide-step-cb');
    const counterEl = document.getElementById('guideStepCounter');
    stepBoxes.forEach(cb => {
      cb.addEventListener('change', () => {
        const completedCount = bodyEl.querySelectorAll('.guide-step-cb:checked').length;
        if (counterEl) counterEl.textContent = `${completedCount} of ${guide.steps.length} Steps Completed`;
        if (completedCount === guide.steps.length) {
          showToast(`All ${guide.steps.length} steps completed! Congratulations on repairing your hardware!`, 'success');
        }
      });
    });

    bodyEl.querySelector('.modal-close-btn-inline')?.addEventListener('click', closeModal);

    openModal('guideModal');
  }

  // ==========================================================================
  // REPAIR NETWORK DIRECTORY
  // ==========================================================================

  function initRepairNetwork() {
    renderRepairersList();

    const searchInput = document.getElementById('repairerSearchInput');
    const specialtyPills = document.querySelectorAll('.repairer-spec-pill');
    const btnListShop = document.getElementById('btnOpenListShopModal');

    if (searchInput) {
      searchInput.addEventListener('input', (e) => {
        state.network.searchQuery = e.target.value.toLowerCase();
        renderRepairersList();
      });
    }

    specialtyPills.forEach(pill => {
      pill.addEventListener('click', () => {
        specialtyPills.forEach(p => p.classList.remove('active'));
        pill.classList.add('active');
        state.network.specialtyFilter = pill.getAttribute('data-spec');
        renderRepairersList();
      });
    });

    if (btnListShop) {
      btnListShop.addEventListener('click', () => {
        openModal('listShopModal');
      });
    }

    initListShopForm();
    initQuoteRequestForm();
  }

  function renderRepairersList() {
    const container = document.getElementById('repairersListContainer');
    if (!container) return;

    const filtered = CIRCULAR_DATA.repairers.filter(rep => {
      const matchSearch = rep.name.toLowerCase().includes(state.network.searchQuery) ||
                          rep.address.toLowerCase().includes(state.network.searchQuery) ||
                          rep.specialties.some(s => s.toLowerCase().includes(state.network.searchQuery));
      
      const matchSpec = state.network.specialtyFilter === 'all' || 
                        rep.specialties.some(s => s.toLowerCase().includes(state.network.specialtyFilter.toLowerCase()));

      return matchSearch && matchSpec;
    });

    if (filtered.length === 0) {
      container.innerHTML = `
        <div style="text-align:center; padding:3rem; background:var(--bg-card); border-radius:var(--radius-lg); border:1px dashed var(--border-card);">
          <div style="font-weight:800; font-size:1.15rem; color:var(--forest-900);">No repair workshops matched your search</div>
          <p style="color:var(--charcoal-600); font-size:0.875rem; margin-top:0.25rem;">Try clearing your specialty filter or searching for another term.</p>
        </div>
      `;
      return;
    }

    container.innerHTML = filtered.map(rep => `
      <div class="repairer-card">
        <div class="repairer-head">
          <div>
            <div class="repairer-name">${rep.name}</div>
            <div class="repairer-meta-line">
              <span class="rating-badge">â˜… ${rep.rating} (${rep.reviewCount} reviews)</span>
              <span>â€¢</span>
              <span>${rep.distanceKm}</span>
              <span>â€¢</span>
              <span>${rep.address.split(',')[0]}</span>
            </div>
          </div>
          <div class="repairer-badges-row">
            ${rep.badges.map(b => `<span class="rep-badge">${b}</span>`).join('')}
          </div>
        </div>

        <p class="repairer-desc">${rep.description}</p>

        <div class="repairer-pricing-table">
          <div style="font-size:0.75rem; font-weight:800; text-transform:uppercase; color:var(--forest-700); margin-bottom:0.4rem;">
            Transparent Benchmark Pricing (Illustrative)
          </div>
          ${rep.samplePricing.map(p => `
            <div class="pricing-row">
              <span>${p.service}</span>
              <strong>${p.cost}</strong>
            </div>
          `).join('')}
        </div>

        <div class="repairer-actions">
          <div style="font-size:0.8125rem; color:var(--charcoal-600);">
            Turnaround: <strong>${rep.turnaround}</strong>
          </div>
          <div style="display:flex; gap:0.5rem;">
            <button type="button" class="btn btn-sm btn-secondary rep-call-btn" data-phone="${rep.phone}">
              Call
            </button>
            <button type="button" class="btn btn-sm btn-primary rep-quote-btn" data-shop-id="${rep.id}">
              Request Quote
            </button>
          </div>
        </div>
      </div>
    `).join('');

    // Wire buttons
    container.querySelectorAll('.rep-call-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        showToast(`Simulated connection: Calling ${btn.getAttribute('data-phone')}...`, 'success');
      });
    });

    container.querySelectorAll('.rep-quote-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        const shopId = btn.getAttribute('data-shop-id');
        const shop = CIRCULAR_DATA.repairers.find(s => s.id === shopId);
        openQuoteModal(shop);
      });
    });
  }

  function openQuoteModal(shop) {
    if (!shop) return;
    const modal = document.getElementById('quoteModal');
    const shopNameEl = document.getElementById('quoteShopName');
    const deviceField = document.getElementById('quoteDeviceField');
    const issueField = document.getElementById('quoteIssueField');

    if (shopNameEl) shopNameEl.textContent = shop.name;
    if (deviceField) deviceField.value = state.checker.model || "Consumer Electronics Device";
    if (issueField) {
      const issueObj = CIRCULAR_DATA.issueTaxonomy.find(i => i.id === state.checker.issue);
      issueField.value = issueObj ? issueObj.label : "General Hardware Service";
    }

    openModal('quoteModal');
  }

  function initQuoteRequestForm() {
    const form = document.getElementById('quoteRequestForm');
    if (!form) return;

    form.addEventListener('submit', (e) => {
      e.preventDefault();
      const name = document.getElementById('quoteUserName')?.value;
      const email = document.getElementById('quoteUserEmail')?.value;

      if (!name || !email) {
        showToast('Please fill in your name and contact email.', 'alert');
        return;
      }

      closeModal();
      form.reset();
      showToast(`Diagnostic request sent to workshop! A confirmation was sent to ${email}.`, 'success');
    });
  }

  function initListShopForm() {
    const form = document.getElementById('listShopForm');
    if (!form) return;

    form.addEventListener('submit', (e) => {
      e.preventDefault();
      const shopName = document.getElementById('listShopName')?.value;
      const address = document.getElementById('listShopAddress')?.value;

      if (!shopName || !address) {
        showToast('Please complete workshop name and address.', 'alert');
        return;
      }

      closeModal();
      form.reset();
      showToast(`Workshop '${shopName}' submitted for Right-to-Repair credential verification!`, 'success');
    });
  }

  // ==========================================================================
  // GIVE A DEVICE A SECOND LIFE (Pathways, Erasure & Checklist)
  // ==========================================================================

  function initSecondLife() {
    renderSecureErasureTabs();
    renderHandoffChecklist();
  }

  function renderSecureErasureTabs() {
    const tabsContainer = document.getElementById('erasureOsTabs');
    const contentContainer = document.getElementById('erasureStepsContainer');
    if (!tabsContainer || !contentContainer) return;

    tabsContainer.innerHTML = CIRCULAR_DATA.secureEraseGuides.map(guide => `
      <button type="button" class="os-tab-btn ${state.secondLife.activeOs === guide.os ? 'active' : ''}" data-os="${guide.os}">
        ${guide.os}
      </button>
    `).join('');

    function updateContent() {
      const current = CIRCULAR_DATA.secureEraseGuides.find(g => g.os === state.secondLife.activeOs) || CIRCULAR_DATA.secureEraseGuides[0];
      contentContainer.innerHTML = `
        <div style="margin-bottom:1.25rem;">
          <div style="font-size:1.15rem; font-weight:800; color:var(--forest-900);">${current.name} Secure Wipe Procedure</div>
          <div style="font-size:0.875rem; color:var(--charcoal-600); margin-top:0.2rem;">
            Follow these exact steps to destroy encryption keys and protect your identity before passing hardware on.
          </div>
        </div>
        <div class="steps-ordered-list">
          ${current.steps.map((step, idx) => `
            <div class="ordered-step-item">
              <div class="step-circle-num">${idx + 1}</div>
              <div class="step-instruction-text">${step}</div>
            </div>
          `).join('')}
        </div>
      `;
    }

    updateContent();

    tabsContainer.querySelectorAll('.os-tab-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        tabsContainer.querySelectorAll('.os-tab-btn').forEach(b => b.classList.remove('active'));
        btn.classList.add('active');
        state.secondLife.activeOs = btn.getAttribute('data-os');
        updateContent();
      });
    });
  }

  function renderHandoffChecklist() {
    const container = document.getElementById('handoffChecklistGrid');
    const progressFill = document.getElementById('handoffProgressFill');
    const progressText = document.getElementById('handoffProgressText');

    if (!container) return;

    function updateProgress() {
      const total = CIRCULAR_DATA.handoffChecklist.length;
      const count = state.secondLife.checkedItems.size;
      const percent = Math.round((count / total) * 100);

      if (progressFill) progressFill.style.width = `${percent}%`;
      if (progressText) progressText.textContent = `${count} of ${total} Done (${percent}%)`;

      if (percent === 100) {
        showToast('Your device is 100% prepared for secure handoff, reuse, or recycling!', 'success');
      }
    }

    container.innerHTML = CIRCULAR_DATA.handoffChecklist.map(item => {
      const isChecked = state.secondLife.checkedItems.has(item.id);
      return `
        <label class="checklist-interactive-item ${isChecked ? 'checked' : ''}" data-item-id="${item.id}">
          <input type="checkbox" ${isChecked ? 'checked' : ''}>
          <span><strong>[${item.category}]</strong> ${item.label}</span>
        </label>
      `;
    }).join('');

    container.querySelectorAll('.checklist-interactive-item').forEach(label => {
      const cb = label.querySelector('input[type="checkbox"]');
      const id = label.getAttribute('data-item-id');

      label.addEventListener('click', (e) => {
        if (e.target !== cb) {
          cb.checked = !cb.checked;
        }
        if (cb.checked) {
          state.secondLife.checkedItems.add(id);
          label.classList.add('checked');
        } else {
          state.secondLife.checkedItems.delete(id);
          label.classList.remove('checked');
        }
        updateProgress();
      });
    });

    updateProgress();
  }

  // ==========================================================================
  // IMPACT SIMULATOR & LCA BENCHMARKS
  // ==========================================================================

  function initImpactSimulator() {
    const devicesSlider = document.getElementById('simDevicesSlider');
    const monthsSlider = document.getElementById('simMonthsSlider');
    const devicesValBadge = document.getElementById('simDevicesVal');
    const monthsValBadge = document.getElementById('simMonthsVal');

    if (!devicesSlider || !monthsSlider) return;

    function recalculateImpact() {
      const count = parseInt(devicesSlider.value, 10);
      const months = parseInt(monthsSlider.value, 10);

      if (devicesValBadge) devicesValBadge.textContent = count.toLocaleString();
      if (monthsValBadge) monthsValBadge.textContent = `${months} mo`;

      // Formulas derived from Fraunhofer IZM and EPA e-waste benchmarks:
      // Average weighted embodied CO2 per diverted electronics unit: ~110 kg CO2e
      // Lifespan extension factor: scaling factor based on delaying manufacturing cycles
      const extensionFactor = months / 12;
      const co2TotalTonnes = Math.round((count * 110 * extensionFactor) / 1000);
      const ewasteKg = Math.round(count * 0.85); // 0.85kg avg weight
      const moneyKeptInCommunity = Math.round(count * 280); // avg savings vs new purchases
      const goldSavedGrams = Math.round((count * 34) / 1000); // 34mg per unit avg
      const cobaltSavedKg = Math.round((count * 15) / 1000); // 15g per unit avg

      document.getElementById('simMetricCo2').textContent = `${co2TotalTonnes.toLocaleString()} t`;
      document.getElementById('simMetricEwaste').textContent = `${ewasteKg.toLocaleString()} kg`;
      document.getElementById('simMetricWealth').textContent = `${moneyKeptInCommunity.toLocaleString()}`;
      document.getElementById('simMetricMaterials').textContent = `${goldSavedGrams}g Au / ${cobaltSavedKg}kg Co`;
    }

    devicesSlider.addEventListener('input', recalculateImpact);
    monthsSlider.addEventListener('input', recalculateImpact);

    recalculateImpact();
  }

  // ==========================================================================
  // MODALS & TOAST UTILITIES
  // ==========================================================================

  function initModals() {
    // Backdrop click close
    document.querySelectorAll('.modal-backdrop').forEach(modal => {
      modal.addEventListener('click', (e) => {
        if (e.target === modal) closeModal();
      });
    });

    // Close buttons
    document.querySelectorAll('.modal-close-btn').forEach(btn => {
      btn.addEventListener('click', closeModal);
    });

    // Escape key
    window.addEventListener('keydown', (e) => {
      if (e.key === 'Escape') closeModal();
    });
  }

  function openModal(modalId) {
    const modal = document.getElementById(modalId);
    if (modal) {
      modal.classList.add('open');
      document.body.style.overflow = 'hidden';
    }
  }

  function closeModal() {
    document.querySelectorAll('.modal-backdrop').forEach(modal => {
      modal.classList.remove('open');
    });
    document.body.style.overflow = '';
  }

  function showToast(message, type = 'success') {
    let container = document.getElementById('globalToastContainer');
    if (!container) {
      container = document.createElement('div');
      container.id = 'globalToastContainer';
      container.className = 'toast-container';
      document.body.appendChild(container);
    }

    const toast = document.createElement('div');
    toast.className = `toast ${type}`;
    toast.innerHTML = `
      <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
        ${type === 'success' 
          ? '<polyline points="20 6 9 17 4 12"/>' 
          : '<circle cx="12" cy="12" r="10"/><line x1="12" y1="8" x2="12" y2="12"/><line x1="12" y1="16" x2="12.01" y2="16"/>'}
      </svg>
      <span>${message}</span>
    `;

    container.appendChild(toast);

    requestAnimationFrame(() => {
      toast.classList.add('show');
    });

    setTimeout(() => {
      toast.classList.remove('show');
      setTimeout(() => toast.remove(), 350);
    }, 4500);
  }

  // ==========================================================================
  // SVG ICON GENERATORS (Self-contained, high-performance)
  // ==========================================================================

  function getCategorySvgIcon(catId) {
    switch (catId) {
      case 'phone':
        return `<svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect width="14" height="20" x="5" y="2" rx="2" ry="2"/><line x1="12" y1="18" x2="12.01" y2="18"/></svg>`;
      case 'laptop':
        return `<svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M20 16V7a2 2 0 0 0-2-2H6a2 2 0 0 0-2 2v9m16 0H4m16 0 1.28 2.55a1 1 0 0 1-.9 1.45H3.62a1 1 0 0 1-.9-1.45L4 16"/></svg>`;
      case 'tablet':
        return `<svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect width="18" height="18" x="3" y="3" rx="2"/><circle cx="12" cy="18" r="1"/></svg>`;
      case 'audio':
        return `<svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M3 14h3a2 2 0 0 1 2 2v3a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-7a9 9 0 0 1 18 0v7a2 2 0 0 1-2 2h-1a2 2 0 0 1-2-2v-3a2 2 0 0 1 2-2h3"/></svg>`;
      case 'console':
        return `<svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="6" y1="12" x2="10" y2="12"/><line x1="8" y1="10" x2="8" y2="14"/><line x1="15" y1="13" x2="15.01" y2="13"/><line x1="18" y1="11" x2="18.01" y2="11"/><rect width="20" height="12" x="2" y="6" rx="6"/></svg>`;
      default:
        return `<svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect width="18" height="18" x="3" y="3" rx="2"/></svg>`;
    }
  }

  function getIssueSvgIcon(issueId) {
    switch (issueId) {
      case 'battery':
        return `<svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect width="16" height="10" x="2" y="7" rx="2" ry="2"/><line x1="22" y1="11" x2="22" y2="13"/><line x1="7" y1="12" x2="13" y2="12"/></svg>`;
      case 'screen':
        return `<svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect width="14" height="20" x="5" y="2" rx="2" ry="2"/><path d="m9 8 3 4-2 3 5 4"/></svg>`;
      case 'charging':
        return `<svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 2v10"/><path d="m9 9 3 3 3-3"/><rect width="16" height="8" x="4" y="14" rx="2"/></svg>`;
      case 'performance':
        return `<svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="m14 14-4-4"/></svg>`;
      case 'liquid':
        return `<svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 2.69l5.66 5.66a8 8 0 1 1-11.31 0z"/></svg>`;
      case 'board':
        return `<svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect width="16" height="16" x="4" y="4" rx="2"/><rect width="6" height="6" x="9" y="9"/><line x1="9" y1="1" x2="9" y2="4"/><line x1="15" y1="1" x2="15" y2="4"/><line x1="9" y1="20" x2="9" y2="23"/><line x1="15" y1="20" x2="15" y2="23"/></svg>`;
      default:
        return `<svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/></svg>`;
    }
  }

})();

</script>
</body>
</html>

