/**
 * TikTok Expert — Premium Interactions
 * Gradient mesh canvas, particle system, micro-interactions
 */

/* ──────────────────────────────────────────────────────────────
   DOM References
   ────────────────────────────────────────────────────────────── */
const navbar        = document.getElementById('navbar');
const hamburger     = document.getElementById('hamburger');
const navMenu       = document.getElementById('nav-menu');
const pricingToggle = document.getElementById('pricing-toggle');
const backToTop     = document.getElementById('back-to-top');
const heroParticles = document.getElementById('hero-particles');
const gradientCanvas = document.getElementById('gradient-canvas');

/* ──────────────────────────────────────────────────────────────
   AOS Init
   ────────────────────────────────────────────────────────────── */
document.addEventListener('DOMContentLoaded', () => {
  AOS.init({
    duration: 800,
    once: true,
    easing: 'ease-out-expo',
    anchorPlacement: 'top-bottom',
    offset: 60,
  });
});

/* ═══════════════════════════════════════════════════════════════
   Gradient Mesh Canvas
   ═══════════════════════════════════════════════════════════════ */
(function initGradientMesh() {
  if (!gradientCanvas) return;
  const ctx = gradientCanvas.getContext('2d');
  let w, h;

  const resize = () => {
    w = gradientCanvas.width  = window.innerWidth;
    h = gradientCanvas.height = window.innerHeight;
  };
  resize();
  window.addEventListener('resize', resize);

  // Gradient orbs
  const orbs = [
    { x: 0.25, y: 0.20, r: 0.35, color: '102, 126, 234',  dx: 0.00008, dy: 0.00006 },
    { x: 0.70, y: 0.60, r: 0.30, color: '118, 75, 162',   dx: -0.00006, dy: -0.00004 },
    { x: 0.80, y: 0.25, r: 0.25, color: '0, 242, 254',    dx: 0.00005, dy: -0.00007 },
    { x: 0.15, y: 0.70, r: 0.28, color: '155, 89, 182',   dx: -0.00007, dy: 0.00005 },
    { x: 0.50, y: 0.85, r: 0.22, color: '102, 126, 234',  dx: 0.00004, dy: -0.00006 },
  ];

  let time = 0;
  function draw() {
    time += 1;
    ctx.clearRect(0, 0, w, h);

    for (const orb of orbs) {
      const ox = orb.x + Math.sin(time * orb.dx) * 0.05;
      const oy = orb.y + Math.cos(time * orb.dy) * 0.05;
      const px = ox * w;
      const py = oy * h;
      const pr = orb.r * Math.max(w, h);

      const grad = ctx.createRadialGradient(px, py, 0, px, py, pr);
      grad.addColorStop(0, `rgba(${orb.color}, 0.10)`);
      grad.addColorStop(0.4, `rgba(${orb.color}, 0.04)`);
      grad.addColorStop(1, 'rgba(0, 0, 0, 0)');

      ctx.fillStyle = grad;
      ctx.fillRect(0, 0, w, h);
    }

    requestAnimationFrame(draw);
  }

  draw();
})();

/* ═══════════════════════════════════════════════════════════════
   Hero Particle System
   ═══════════════════════════════════════════════════════════════ */
(function initParticles() {
  if (!heroParticles) return;
  const count = 35;

  for (let i = 0; i < count; i++) {
    const particle = document.createElement('div');
    particle.classList.add('particle');
    const size = Math.random() * 3 + 1;
    particle.style.width  = size + 'px';
    particle.style.height = size + 'px';
    particle.style.left = Math.random() * 100 + '%';
    particle.style.animationDuration = (Math.random() * 8 + 6) + 's';
    particle.style.animationDelay = (Math.random() * 8) + 's';
    const colors = ['#667eea', '#764ba2', '#00f2fe', '#f093fb'];
    particle.style.background = colors[Math.floor(Math.random() * colors.length)];
    heroParticles.appendChild(particle);
  }
})();

/* ═══════════════════════════════════════════════════════════════
   Navbar Scroll Effect
   ═══════════════════════════════════════════════════════════════ */
let lastScrollTop = 0;
let scrollTicking = false;

window.addEventListener('scroll', () => {
  if (!scrollTicking) {
    requestAnimationFrame(() => {
      const scrollTop = window.pageYOffset || document.documentElement.scrollTop;

      // Scrolled class
      navbar.classList.toggle('scrolled', scrollTop > 60);

      // Hide on scroll down, show on scroll up
      if (scrollTop > lastScrollTop && scrollTop > 150) {
        navbar.style.transform = 'translateY(-100%)';
      } else {
        navbar.style.transform = 'translateY(0)';
      }

      lastScrollTop = Math.max(0, scrollTop);
      scrollTicking = false;
    });
    scrollTicking = true;
  }
}, { passive: true });

/* ═══════════════════════════════════════════════════════════════
   Mobile Menu
   ═══════════════════════════════════════════════════════════════ */
hamburger.addEventListener('click', () => {
  hamburger.classList.toggle('active');
  navMenu.classList.toggle('active');
  document.body.style.overflow = navMenu.classList.contains('active') ? 'hidden' : '';
});

// Close on link click
document.querySelectorAll('.nav-link').forEach(link => {
  link.addEventListener('click', () => {
    hamburger.classList.remove('active');
    navMenu.classList.remove('active');
    document.body.style.overflow = '';
  });
});

/* ═══════════════════════════════════════════════════════════════
   Active Nav Link
   ═══════════════════════════════════════════════════════════════ */
const sections = document.querySelectorAll('section[id]');
const navLinks = document.querySelectorAll('.nav-link');

function updateActiveNavLink() {
  let current = '';
  sections.forEach(section => {
    if (window.pageYOffset >= section.offsetTop - 150) {
      current = section.getAttribute('id');
    }
  });
  navLinks.forEach(link => {
    link.classList.toggle('active', link.getAttribute('href') === `#${current}`);
  });
}

window.addEventListener('scroll', updateActiveNavLink, { passive: true });

/* ═══════════════════════════════════════════════════════════════
   Smooth Scroll
   ═══════════════════════════════════════════════════════════════ */
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
  anchor.addEventListener('click', function (e) {
    e.preventDefault();
    const target = document.querySelector(this.getAttribute('href'));
    if (target) {
      window.scrollTo({
        top: target.offsetTop - 80,
        behavior: 'smooth',
      });
    }
  });
});

/* ═══════════════════════════════════════════════════════════════
   Pricing Toggle
   ═══════════════════════════════════════════════════════════════ */
if (pricingToggle) {
  pricingToggle.addEventListener('change', function () {
    document.body.classList.toggle('yearly-active', this.checked);
    // Animate numbers
    document.querySelectorAll('.amount:not(.yearly):not(.monthly), .amount.monthly, .amount.yearly').forEach(el => {
      el.style.transform = 'scale(0.85)';
      el.style.opacity = '0.4';
      setTimeout(() => {
        el.style.transform = 'scale(1)';
        el.style.opacity = '1';
      }, 160);
    });
  });
}

/* ═══════════════════════════════════════════════════════════════
   Counter Animation
   ═══════════════════════════════════════════════════════════════ */
function animateCounter(el) {
  const raw = el.getAttribute('data-target') || el.textContent.replace(/[^\d]/g, '');
  const target = parseInt(raw, 10);
  if (isNaN(target)) return;

  const suffix = (el.textContent.match(/[%+h]/) || [''])[0];
  const prefix = el.textContent.startsWith('$') ? '$' : '';
  const duration = 2000;
  const startTime = performance.now();

  function update(now) {
    const progress = Math.min((now - startTime) / duration, 1);
    // Ease out cubic
    const eased = 1 - Math.pow(1 - progress, 3);
    const current = Math.floor(eased * target);

    if (suffix) el.textContent = prefix + current + suffix;
    else if (prefix) el.textContent = prefix + current.toLocaleString();
    else el.textContent = current.toLocaleString();

    if (progress < 1) requestAnimationFrame(update);
  }

  requestAnimationFrame(update);
}

const counterObserver = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      animateCounter(entry.target);
      counterObserver.unobserve(entry.target);
    }
  });
}, { threshold: 0.3 });

document.querySelectorAll('.stat-number, .stats-number').forEach(el => counterObserver.observe(el));

/* ═══════════════════════════════════════════════════════════════
   Mouse-Track Glow on Service Cards
   ═══════════════════════════════════════════════════════════════ */
document.querySelectorAll('.service-card').forEach(card => {
  card.addEventListener('mousemove', (e) => {
    const rect = card.getBoundingClientRect();
    const x = ((e.clientX - rect.left) / rect.width) * 100;
    const y = ((e.clientY - rect.top) / rect.height) * 100;
    card.style.setProperty('--mouse-x', x + '%');
    card.style.setProperty('--mouse-y', y + '%');
  });
});

/* ═══════════════════════════════════════════════════════════════
   FAQ Accordion
   ═══════════════════════════════════════════════════════════════ */
document.querySelectorAll('.faq-question').forEach(btn => {
  btn.addEventListener('click', () => {
    const item = btn.parentElement;
    const isActive = item.classList.contains('active');

    // Close all
    document.querySelectorAll('.faq-item').forEach(el => el.classList.remove('active'));

    // Open clicked (unless it was already open)
    if (!isActive) item.classList.add('active');
  });
});

/* ═══════════════════════════════════════════════════════════════
   Back to Top
   ═══════════════════════════════════════════════════════════════ */
window.addEventListener('scroll', () => {
  backToTop.classList.toggle('visible', window.pageYOffset > 600);
}, { passive: true });

backToTop.addEventListener('click', () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
});

/* ═══════════════════════════════════════════════════════════════
   Parallax Hero
   ═══════════════════════════════════════════════════════════════ */
const heroBg    = document.querySelector('.hero-background');
const heroContent = document.querySelector('.hero-content');

window.addEventListener('scroll', () => {
  const scrollY = window.pageYOffset;
  if (heroBg)    heroBg.style.transform    = `translateY(${scrollY * -0.3}px)`;
  if (heroContent && scrollY < window.innerHeight) {
    heroContent.style.transform = `translateY(${scrollY * -0.1}px)`;
  }
}, { passive: true });

/* ═══════════════════════════════════════════════════════════════
   Loading State for CTA Buttons
   ═══════════════════════════════════════════════════════════════ */
function showLoading(button) {
  const icon = button.querySelector('i');
  const originalClass = icon ? icon.className : '';
  if (icon) icon.className = 'fas fa-spinner fa-spin';
  button.style.pointerEvents = 'none';
  button.style.opacity = '0.7';

  setTimeout(() => {
    if (icon) icon.className = originalClass;
    button.style.pointerEvents = '';
    button.style.opacity = '';
  }, 2000);
}

document.querySelectorAll('.btn-primary, .pricing-btn').forEach(btn => {
  if (btn.href && btn.href.includes('discord')) {
    btn.addEventListener('click', function () { showLoading(this); });
  }
});

/* ═══════════════════════════════════════════════════════════════
   Service Worker (PWA)
   ═══════════════════════════════════════════════════════════════ */
if ('serviceWorker' in navigator) {
  window.addEventListener('load', () => {
    fetch('/sw.js')
      .then(res => { if (res.ok) navigator.serviceWorker.register('/sw.js'); })
      .catch(() => {});
  });
}

/* ═══════════════════════════════════════════════════════════════
   Theme Detection
   ═══════════════════════════════════════════════════════════════ */
const darkQuery = window.matchMedia('(prefers-color-scheme: dark)');
darkQuery.addEventListener('change', e => {
  document.body.classList.toggle('dark-theme', e.matches);
});
document.body.classList.toggle('dark-theme', darkQuery.matches);

/* ═══════════════════════════════════════════════════════════════
   Analytics Stub
   ═══════════════════════════════════════════════════════════════ */
function trackEvent(name, props = {}) {
  if (window.gtag)     window.gtag('event', name, props);
  if (window.analytics) window.analytics.track(name, props);
}

document.querySelectorAll('.btn-primary, .pricing-btn').forEach(btn => {
  btn.addEventListener('click', function () {
    trackEvent('cta_click', {
      text: this.textContent.trim().slice(0, 30),
      section: this.closest('section')?.id || 'unknown',
    });
  });
});

const sectionObserver = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      trackEvent('section_view', { section: entry.target.id });
    }
  });
}, { threshold: 0.4 });

sections.forEach(s => sectionObserver.observe(s));

/* ═══════════════════════════════════════════════════════════════
   Error Handling
   ═══════════════════════════════════════════════════════════════ */
window.addEventListener('error', e => console.error('JS Error:', e.error));
window.addEventListener('unhandledrejection', e => {
  console.error('Unhandled rejection:', e.reason);
  e.preventDefault();
});
