<template>
  <div class="page-about">
    <!-- Banner -->
    <section class="page-banner">
      <div class="page-banner__placeholder" aria-hidden="true">
        <span class="page-banner__label">About Us banner image</span>
        <span class="page-banner__hint">Add image (e.g. 1200×400)</span>
      </div>
    </section>

    <section class="content">
      <div class="container">
        <h1>About Us</h1>
        <p><strong>Digital Rich Technologies</strong> builds Venue Genius—event staff coordination and point of management for teams.</p>

        <!-- Longer blurb about Digital Rich - fill in as needed -->
        <div class="about-blurb">
          <h2>About Digital Rich Technologies</h2>
          <p class="about-blurb__fill">
            Add a longer blurb about Digital Rich Technologies here: company story, mission, why you focus on event tech, who you serve, and how Venue Genius fits. This box is for richer “about the company” copy separate from the team bios below.
          </p>
        </div>

        <h2 id="team">Our Team</h2>
        <div class="team-grid">
          <article class="team-card">
            <h3>Lauren Daniels</h3>
            <p class="role">CEO</p>
            <p class="bio">Lauren brings a strong background in catering, event coordination, and bar staffing, along with experience as an auditor and accountant. She leads Digital Rich Technologies and the vision for Venue Genius.</p>
          </article>
          <article class="team-card">
            <h3>Sharon Doss</h3>
            <p class="role">CTO</p>
            <p class="bio">Sharon is an information technology leader with 25 years of experience in the automotive industry. In her current role at Stellantis she is a Senior Business Process Specialist, providing business process and project management expertise in the Information and Communication Technology (ICT) – MOPAR Vehicle Protection area.</p>
            <p class="bio">Prior to her current role, Sharon has held a variety of roles across various IT disciplines, both regionally and globally, including global SAP process lead and release manager, IT tools and process manager, and manufacturing cost and vehicle invoicing systems manager.</p>
            <p class="bio">She holds a Bachelor of Public Affairs degree from Wayne State University and a Master of Science in Computing and Information Systems from the University of Detroit Mercy School of Business. She has been an active member and volunteer of the Michigan Council of Women in Technology (MCWT) for several years and currently serves on the MCWT Advisory Board.</p>
          </article>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'About Us — Venue Genius',
  meta: [{ name: 'description', content: 'Digital Rich Technologies team: Lauren Daniels (CEO), Sharon Doss (CTO).' }]
})
</script>

<style scoped>
.page-about { padding-bottom: 3rem; }

.page-banner {
  width: 100%;
  margin-bottom: 2rem;
}
.page-banner__placeholder {
  aspect-ratio: 3 / 1;
  min-height: 180px;
  background: #e5e7eb;
  border: 2px dashed #9ca3af;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 0.25rem;
  color: #6b7280;
  font-size: 0.875rem;
}
.page-banner__label { font-weight: 600; color: #4b5563; }
.page-banner__hint { font-size: 0.75rem; opacity: 0.9; }

.content { padding: 0 0 2rem; }
.content h1 { margin: 0 0 1rem; font-size: 1.75rem; }
.content > .container > p:first-of-type { margin: 0 0 1.5rem; color: var(--drt-text-muted); }

.about-blurb {
  padding: 1.5rem;
  background: #f8fafc;
  border: 1px solid #e5e7eb;
  border-radius: 8px;
  margin-bottom: 2rem;
}
.about-blurb h2 {
  margin: 0 0 0.75rem;
  font-size: 1.2rem;
  font-weight: 600;
}
.about-blurb__fill {
  margin: 0;
  font-size: 0.95rem;
  color: var(--drt-text-muted);
  line-height: 1.6;
  font-style: italic;
}

.content h2 { margin: 2rem 0 1rem; font-size: 1.35rem; }
.content h2#team { margin-top: 0; }
.content p { margin: 0 0 0.75rem; color: var(--drt-text-muted); }
.team-grid { display: grid; gap: 1.5rem; margin-top: 1.5rem; }
@media (min-width: 600px) { .team-grid { grid-template-columns: 1fr 1fr; } }
.team-card {
  padding: 1.5rem;
  background: #f8fafc;
  border-radius: 8px;
  border: 1px solid #e5e7eb;
}
.team-card h3 { margin: 0 0 0.25rem; font-size: 1.2rem; }
.team-card .role { margin: 0 0 0.5rem; font-weight: 600; color: var(--drt-purple); font-size: 0.9rem; }
.team-card .bio { margin: 0 0 0.5rem; font-size: 0.95rem; }
.team-card .bio:last-of-type { margin-bottom: 0; }
</style>
