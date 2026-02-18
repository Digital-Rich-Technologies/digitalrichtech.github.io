<template>
  <div class="page-pricing">
    <!-- Tiers -->
    <section class="pricing-intro">
      <div class="container">
        <h1>Venue Genius pricing</h1>
        <p class="lead">Pricing by team size. Pre-launch—contact us and we’ll find the right fit.</p>
      </div>
    </section>

    <section class="plans-section">
      <div class="container container--wide">
        <div class="plan-grid">
          <PricingPlanCard
            v-for="plan in tierPlans"
            :key="plan.name"
            :name="plan.name"
            :price="plan.price"
            :period="plan.period"
            :features="plan.features"
            :cta-text="plan.ctaText"
            :cta-href="plan.ctaHref"
            :recommended="plan.recommended"
          />
        </div>
      </div>
    </section>

    <!-- Add-ons (separate from tiers) -->
    <section id="add-ons" class="addons-section">
      <div class="container container--wide">
        <h2 class="section-title">Add-ons</h2>
        <p class="addons-intro">Optional add-ons available with any tier. Pricing on request.</p>
        <div class="addons-grid">
          <PricingAddonCard
            v-for="addon in addons"
            :key="addon.name"
            :name="addon.name"
            :description="addon.description"
            :cta-text="addon.ctaText"
            :cta-href="addon.ctaHref"
          />
        </div>
      </div>
    </section>

    <!-- Questions & Answers -->
    <section class="faq-section">
      <div class="container container--wide">
        <h2 class="faq-title">Questions &amp; Answers</h2>
        <div class="faq-list">
          <details
            v-for="(item, i) in faqItems"
            :key="i"
            class="faq-item"
          >
            <summary class="faq-item__question">{{ item.question }}</summary>
            <div class="faq-item__answer">
              <p>{{ item.answer }}</p>
            </div>
          </details>
        </div>
      </div>
    </section>

    <section class="pricing-cta">
      <div class="container">
        <h2 class="pricing-cta__headline">Get started with Venue Genius</h2>
        <p>Need a custom quote or have questions? <NuxtLink to="/contact">Contact us</NuxtLink>.</p>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
const tierPlans = [
  {
    name: 'Small Tier',
    price: '1 – 10',
    period: ' staff',
    features: [
      'For small teams and single venues',
      'Real-time coordination',
      'Coordinator dashboard',
      'Pre-launch: pricing on request'
    ],
    ctaText: 'Contact us',
    ctaHref: '/contact',
    recommended: false
  },
  {
    name: 'Medium Tier',
    price: '10 – 100',
    period: ' staff',
    features: [
      'For growing teams and multi-venue',
      'Everything in Small Tier',
      'Higher capacity and reporting',
      'Pre-launch: pricing on request'
    ],
    ctaText: 'Contact us',
    ctaHref: '/contact',
    recommended: false
  },
  {
    name: 'Large Tier',
    price: '100+',
    period: ' staff',
    features: [
      'For large operations and enterprises',
      'Everything in Medium Tier',
      'Dedicated support and custom needs',
      'Pre-launch: pricing on request'
    ],
    ctaText: 'Contact us',
    ctaHref: '/contact',
    recommended: false
  }
]

const addons = [
  {
    name: 'Walkie Talkie Functionality',
    description: 'Voice push-to-talk style communication so staff can coordinate hands-free during events.',
    ctaText: 'Contact us',
    ctaHref: '/contact'
  },
  {
    name: 'Location Aware Check-ins',
    description: 'Staff check in from the floor with location context so coordinators see who’s where in real time.',
    ctaText: 'Contact us',
    ctaHref: '/contact'
  },
  {
    name: 'AI Event Summaries',
    description: 'Automated summaries and insights after events so you can review what happened and improve next time.',
    ctaText: 'Contact us',
    ctaHref: '/contact'
  }
]

const faqItems = [
  {
    question: 'What is the right plan for me?',
    answer: 'Add your answer here. Consider team size (1–10 = Small, 10–100 = Medium, 100+ = Large) and which add-ons you need.'
  },
  {
    question: 'What are my payment options?',
    answer: 'Add your answer here. Pre-launch we’ll work with you on payment terms.'
  },
  {
    question: 'How do add-ons work with my tier?',
    answer: 'Add-ons (Walkie Talkie, Location Check-ins, AI Summaries) are optional and can be added to any tier. Contact us for pricing.'
  },
  {
    question: 'Where can I ask more questions?',
    answer: 'Reach out via our Contact page—we’re happy to walk you through options and demo Venue Genius.'
  }
]
</script>

<style scoped>
.page-pricing { padding-bottom: 3rem; }
.pricing-intro {
  padding: 2rem 0 1rem;
  text-align: center;
}
.pricing-intro h1 { margin: 0 0 0.5rem; font-size: 1.75rem; }
.pricing-intro .lead {
  margin: 0;
  color: var(--drt-text-muted);
  max-width: 40ch;
  margin-left: auto;
  margin-right: auto;
}

.container--wide { max-width: 960px; }

.plans-section { padding: 1rem 0 2rem; }
.plan-grid {
  display: grid;
  gap: 1.25rem;
  grid-template-columns: repeat(3, 1fr);
}
@media (max-width: 768px) {
  .plan-grid { grid-template-columns: 1fr; }
}

.addons-section {
  padding: 2rem 0;
  border-top: 1px solid #e5e7eb;
  background: #fafafa;
}
.section-title {
  margin: 0 0 0.25rem;
  font-size: 1.25rem;
  font-weight: 600;
}
.addons-intro {
  margin: 0 0 1rem;
  font-size: 0.95rem;
  color: var(--drt-text-muted);
}
.addons-grid {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
}

.faq-section {
  padding: 2.5rem 0;
  border-top: 1px solid #e5e7eb;
}
.faq-title {
  margin: 0 0 1rem;
  font-size: 1.25rem;
  font-weight: 600;
}
.faq-list { max-width: 640px; }
.faq-item {
  border: 1px solid #e5e7eb;
  border-radius: 6px;
  margin-bottom: 0.5rem;
  background: #fff;
}
.faq-item__question {
  padding: 0.75rem 1rem;
  font-weight: 500;
  cursor: pointer;
  list-style: none;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 0.5rem;
}
.faq-item__question::-webkit-details-marker { display: none; }
.faq-item__question::after {
  content: '';
  width: 0;
  height: 0;
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: 6px solid var(--drt-text-muted);
  flex-shrink: 0;
  transition: transform 0.2s;
}
.faq-item[open] .faq-item__question::after {
  transform: rotate(180deg);
}
.faq-item__answer {
  padding: 0 1rem 1rem;
  border-top: 1px solid #e5e7eb;
}
.faq-item__answer p {
  margin: 0.75rem 0 0;
  font-size: 0.95rem;
  color: var(--drt-text-muted);
  line-height: 1.5;
}

.pricing-cta {
  padding: 2rem 0;
  text-align: center;
  border-top: 1px solid #e5e7eb;
  background: #fafafa;
}
.pricing-cta__headline {
  margin: 0 0 0.5rem;
  font-size: 1.35rem;
  font-weight: 600;
}
.pricing-cta a { color: var(--drt-purple); font-weight: 500; }
</style>
