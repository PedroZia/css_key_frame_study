# CSS Animation Study Lab

Repositório de estudo de **animações CSS puras** — zero JavaScript. Cada técnica é demonstrada com código funcional e exemplo visual.

## Como usar

1. Abra `index.html` no navegador
2. Navegue pelas 12 abas principais (radio hack CSS-only)
3. Para técnicas avançadas, clique na aba **"Técnicas Modernas →"** (aba 13) que lista as 10 páginas standalone

Não precisa de build, package manager ou servidor. É puro HTML + CSS.

## Estrutura

```
.
├── index.html              # Página principal com 13 abas (12 originais + hub de links)
├── style.css               # CSS base + 12 abas originais
├── nav.css                 # CSS de navegação entre páginas
├── README.md
└── pages/                  # Páginas standalone (uma por técnica avançada)
    ├── 13-starting-style.html
    ├── 14-offset-path.html
    ├── 15-css-vars.html
    ├── 16-color-mix.html
    ├── 17-has.html
    ├── 18-linear-easing.html
    ├── 19-container-queries.html
    ├── 20-scroll-snap.html
    ├── 21-backdrop-filter.html
    └── 22-css-art.html
```

## Índice de técnicas

### Aba Principal (em `index.html`)

| # | Tópico | O que cobre |
|---|--------|-------------|
| 1 | **Transições** | property, duration, timing, delay, multiple, shorthand |
| 2 | **Keyframes** | fade, bounce, spin, pulse, slide, steps |
| 3 | **Transform 2D** | translate, rotate, scale, skew, origin, combined, **matrix** |
| 4 | **Transform 3D** | perspective, rotateX/Y/Z, translateZ, card flip, preserve-3d |
| 5 | **Hover Effects** | glow, border draw, magnetic shift, reveal, text slide, ripple |
| 6 | **Loading** | spinner, dots, progress bar, skeleton, orbital, wave |
| 7 | **Micro-interações** | toggle, button ripple, focus ring, input underline, like, badge |
| 8 | **Scroll CSS** | progress, reveal, parallax, rotate, scale, color shift (animation-timeline) |
| 9 | **Easing** | keywords, cubic-bezier, steps, visual curves, comparison |
| 10 | **Stagger** | fade, slide up, scale, rotate, grid, hover cascade |
| 11 | **Page Transitions** | crossfade, slide H/V, zoom, flip, wipe |
| 12 | **Avançado** | @property, counter, conic, clip-path morph, filter, view transitions, color, text gradient, SVG stroke |
| 13 | **Técnicas Modernas** | Hub de links para as 10 páginas standalone |

### Páginas Standalone (em `pages/`)

| # | Técnica | Browser Support | Destaque |
|---|---------|-----------------|----------|
| 13 | `@starting-style` + `transition-behavior: allow-discrete` | Chrome 117+ | Anima `display: none → block` em transitions |
| 14 | `offset-path` | Chrome 55+ | Movimento ao longo de path SVG |
| 15 | CSS Variables em `@keyframes` | Chrome 85+ | `var()` em keyframes via `@property` |
| 16 | `color-mix()` animado | Chrome 111+ | Interpolação dinâmica de cores |
| 17 | `:has()` parent selectors | Chrome 105+ | Estilizar elementos baseado em filhos |
| 18 | `linear()` easing function | Chrome 113+ | Nova curva de easing com múltiplos stops |
| 19 | Container Queries animadas | Chrome 105+ | Animações responsivas ao container (`cqi`/`cqw`) |
| 20 | `scroll-snap` + animations | Chrome 105+ | Carrossel sem JS com snap + `animation-timeline` |
| 21 | `backdrop-filter` + glassmorphism | Chrome 76+ | Efeitos de vidro fosco animado |
| 22 | CSS Art Gallery | Todos | Animações decorativas puras para inspiração |

## Recursos por técnica

Cada página inclui:
- Demonstração visual interativa
- Código CSS pronto para copiar
- Explicação da sintaxe
- Notas de browser support
- `@supports` fallback quando aplicável

## Recursos globais

- **Dark mode** com tokens semânticos (`var(--accent)`, `var(--bg-primary)`, etc.)
- **Mobile-first** com media queries em 768px e 480px
- **Acessibilidade**: `aria-roles`, `aria-controls`, `aria-labelledby`, `sr-only` para inputs escondidos
- **`prefers-reduced-motion`**: animações desabilitam para usuários sensíveis a movimento
- **Fallback para browsers sem `animation-timeline`**: animações alternativas em `@supports`
- **Sem dependências**: zero JavaScript, zero build, zero framework

## Compatibilidade

| Recurso | Chrome | Firefox | Safari | Edge |
|---------|--------|---------|--------|------|
| Transitions/animations básicas | ✅ 1+ | ✅ 1+ | ✅ 1+ | ✅ 12+ |
| `@property` | 85+ | 128+ | 16.4+ | 85+ |
| `animation-timeline` | 115+ | ❌ | ❌ | 115+ |
| `@starting-style` | 117+ | 129+ | 17.5+ | 117+ |
| `offset-path` | 55+ | 72+ | 16+ | 79+ |
| `color-mix()` | 111+ | 113+ | 16.2+ | 111+ |
| `:has()` | 105+ | 121+ | 15.4+ | 105+ |
| `linear()` easing | 113+ | 112+ | 17.2+ | 113+ |
| Container queries | 105+ | 110+ | 16+ | 105+ |
| `backdrop-filter` | 76+ | 103+ | 9+ | 17+ |
| `@scope` | 118+ | 128+ | 17+ | 118+ |

Recomendado: **Chrome 120+** ou **Edge 120+** para suporte completo.

## Como contribuir

1. Adicione novos cards em uma aba existente
2. Crie uma nova página standalone em `pages/` seguindo o padrão das outras
3. Mantenha o foco: **CSS puro, zero JavaScript**

## Conceitos estudados

- **Transitions**: `transition-property`, `transition-duration`, `transition-timing-function`, `transition-delay`
- **Animations**: `@keyframes`, `animation-name`, `animation-duration`, `animation-fill-mode`, `animation-direction`
- **Transforms 2D/3D**: `translate`, `rotate`, `scale`, `skew`, `matrix`, `perspective`, `preserve-3d`
- **Properties modernas**: `@property` (Houdini), `color-mix()`, `linear()`, container queries
- **Selectors avançados**: `:has()`, `:focus-within`, `:placeholder-shown`, `:user-invalid`
- **Layout responsivo**: `@container`, `cqi`/`cqw`/`cqb` units, `container-type`
- **Motion path**: `offset-path`, `offset-distance`, `offset-rotate`
- **Effects**: `backdrop-filter`, `filter`, `clip-path`, `mask`
- **Scroll-driven**: `animation-timeline: scroll()` / `view()`, `animation-range`
- **Discrete transitions**: `transition-behavior: allow-discrete`, `@starting-style`

## Referências

- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations)
- [CSS Tricks: A Complete Guide to CSS Animations](https://css-tricks.com/css-animation-features-you-didnt-know-existed/)
- [web.dev: New CSS features](https://web.dev/css/)
- [CSS Houdini Spec](https://developer.mozilla.org/en-US/docs/Web/API/CSS_Custom_Properties_API)

---

MIT License — feito para estudo e referência.
