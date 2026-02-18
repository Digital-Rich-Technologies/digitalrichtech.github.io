<template>
  <section class="customer-partners" aria-labelledby="partners-heading">
    <div class="container">
      <h2 id="partners-heading" class="visually-hidden">DRT Partners &amp; brand</h2>
      <div class="partners-layout">
        <div class="partners-visual">
          <img
            src="/images/drt-partners.png"
            alt="DRT Partners: Newlab, Taylor'd Garden, Bamboo Detroit, Techtown Detroit, Eleven11 Event Studio, The Norwood, Garden Theater, Opulence Gallery, The Eastern. The market is ready to use our technology."
            width="800"
            height="450"
            class="partners-image"
          />
        </div>
        <div class="partners-message">
          <p class="partners-label">DRT Partners</p>
          <p class="partners-tagline">The market is ready to use our technology.</p>
        </div>
      </div>
      <div class="brand-visual">
        <img
          src="/images/drt-investor-deck.png"
          alt="Digital Rich Technologies — Seamless operations for memorable events. Investor Deck, Winter 2025."
          width="800"
          height="450"
          class="brand-image"
        />
      </div>
    </div>
  </section>
</template>

<style scoped>
.customer-partners {
  padding: 3rem 0;
  background: #fff;
  border-top: 1px solid #e5e7eb;
}

.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}

.partners-layout {
  display: grid;
  gap: 1.5rem;
  margin-bottom: 2rem;
}
@media (min-width: 720px) {
  .partners-layout {
    grid-template-columns: 1fr minmax(240px, 320px);
    align-items: center;
  }
}

.partners-visual {
  border-radius: 8px;
  overflow: hidden;
  background: #f8fafc;
}
.partners-image {
  width: 100%;
  height: auto;
  display: block;
  object-fit: contain;
}

.partners-message {
  background: var(--drt-purple-dark, #3b0764);
  color: #fff;
  padding: 1.5rem;
  border-radius: 8px;
  min-height: 120px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.partners-label {
  margin: 0 0 0.5rem;
  font-size: 0.9rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  opacity: 0.9;
}
.partners-tagline {
  margin: 0;
  font-size: clamp(1rem, 2vw, 1.2rem);
  font-weight: 700;
  line-height: 1.3;
  text-transform: uppercase;
}

.brand-visual {
  border-radius: 8px;
  overflow: hidden;
  background: #f8fafc;
  max-width: 720px;
  margin: 0 auto;
}
.brand-image {
  width: 100%;
  height: auto;
  display: block;
  object-fit: contain;
}
</style>
