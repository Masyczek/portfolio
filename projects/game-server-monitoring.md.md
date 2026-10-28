---
layout: default
title: Live Game Server Monitoring
description: Self-hosted infrastructure monitoring using Docker, PostgreSQL, Python, and Grafana.
permalink: /servers/
---

<section class="wrap" style="padding-top: 4rem; padding-bottom: 2rem;">
  <p class="hero__eyebrow">Infrastructure &amp; Observability</p>
  <h1>Live Game Server Monitoring</h1>
  <p class="hero__lede">
    A self-hosted monitoring system tracking the operational health
    of four dedicated game servers. The system combines container
    performance metrics, automated backup verification, and live
    visualization in a single dashboard.
  </p>

  <ul class="hero__facts">
    <li>Linux &amp; Docker</li>
    <li>Python &amp; PostgreSQL</li>
    <li>Grafana</li>
    <li>Cloudflare Tunnel</li>
  </ul>
</section>

<section>
  <div class="wrap">
    <div class="section-head">
      <h2>Live operational dashboard</h2>
      <p>
        Live container performance and backup health metrics,
        collected automatically from my home server.
      </p>
    </div>

    <div style="border: 1px solid rgba(128,128,128,.25); border-radius: 12px; overflow: hidden; background: #111827;">
      <iframe
        src="https://grafana.johnmasyczek.com/d/game-servers?orgId=1&amp;kiosk"
        title="Live Game Server Monitoring Dashboard"
        style="display: block; width: 100%; height: 1050px; border: 0;"
        loading="lazy"
        referrerpolicy="strict-origin-when-cross-origin">
      </iframe>
    </div>

    <p style="margin-top: 1rem;">
      <a class="project-card__link"
         href="https://grafana.johnmasyczek.com/d/game-servers?orgId=1&amp;kiosk"
         target="_blank"
         rel="noopener noreferrer">
        Open dashboard in a new tab
      </a>
    </p>
  </div>
</section>

<section style="padding-top: 3rem; padding-bottom: 4rem;">
  <div class="wrap">
    <div class="section-head">
      <h2>System architecture</h2>
      <p>
        Designed for automated collection, operational visibility,
        and controlled public access.
      </p>
    </div>

    <div class="project-list">
      <div class="project-card">
        <h3>Telemetry collection</h3>
        <p>
          Python-based collection services periodically capture
          container CPU, memory, network, health, uptime, and
          restart metrics. Timestamped observations are stored
          in PostgreSQL for historical analysis.
        </p>
      </div>

      <div class="project-card">
        <h3>Backup observability</h3>
        <p>
          Automated backup monitoring records job outcomes,
          snapshot retention, completion times, and scheduled
          execution. The dashboard highlights stale observations,
          missed backups, and unhealthy states.
        </p>
      </div>

      <div class="project-card">
        <h3>Secure public visualization</h3>
        <p>
          A dedicated Grafana instance provides anonymous,
          read-only visualization using restricted PostgreSQL
          views. Cloudflare Tunnel delivers the dashboard over
          HTTPS without exposing the private monitoring interface
          or opening inbound router ports.
        </p>
      </div>
    </div>
  </div>
</section>
