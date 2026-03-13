---
name: speed-optimization
description: >
  Performance and Core Web Vitals expertise. Activates when discussing
  page speed, CWV, LCP, INP, CLS, TTFB, performance optimization,
  image optimization, or site speed issues.
---

# Core Web Vitals & Speed Audit Framework

## Performance Baseline
- LCP (target <2.5s), INP (target <200ms), CLS (target <0.1)
- TTFB (target <800ms), FCP (target <1.8s)
- Total page weight (target <3MB), requests (target <50)

## Bottleneck Analysis
- Images: format, compression, lazy loading, srcset, dimensions
- JavaScript: render-blocking, unused JS, large bundles, main thread
- CSS: render-blocking, unused CSS, critical CSS
- Fonts: FOUT/FOIT, too many files, no preload, no font-display:swap
- Third-party scripts: analytics, chat, social, ads — impact?
- Server: slow TTFB, no CDN, no caching, shared hosting
- DOM: excessive elements (target <1500)
- Layout shifts: images without dimensions, dynamic injection

## Per-Issue Fix Format
Issue → Impact (which CWV, estimated improvement) → Fix steps →
Effort (Quick/Medium/Complex) → Priority → Expected improvement
