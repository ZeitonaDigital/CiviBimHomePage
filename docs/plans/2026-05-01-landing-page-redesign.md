# Landing Page Redesign — Technology for Engineering

> **For Antigravity:** REQUIRED WORKFLOW: Use `.agent/workflows/execute-plan.md` to execute this plan in single-flow mode.

**Goal:** Rewrite the CiviBIM landing page from a BIM-centric page to a broad technology consultancy for AEC companies (plugins, automation, custom software, digital diagnostics), with a light nav/footer and refreshed copy in PT-PT.

**Architecture:** Single HTML file + CSS file + JS file. No framework. All changes are content (copy), structure (HTML sections), and styling (CSS). Logo stays as-is.

**Tech Stack:** HTML5, Vanilla CSS, Vanilla JS

---

### Task 1: Update CSS — Light Nav & Footer

**Files:**
- Modify: `style.css` (nav and footer blocks)

**Step 1: Update nav to light theme**

In `style.css`, change `.nav` background from `rgba(11,32,60,.96)` to `rgba(255,255,255,0.97)` with a bottom shadow. Update `.nav__logo-img` filter to `none` (show original logo colours). Update `.nav__link` colour to `var(--clr-text)`. Update `.nav__hamburger span` to dark colour.

**Step 2: Update footer to light theme**

Add `.footer` rule: `background: var(--clr-white); border-top: 1px solid var(--clr-border);`. Change `.footer__tagline`, `.footer__link`, `.footer__copy` colours to dark text. Change `.footer__logo-img` filter to `none`.

**Step 3: Verify nav scrolled state still works**

`.nav.scrolled` should stay light: `background: rgba(255,255,255,0.99); box-shadow: 0 2px 20px rgba(0,0,0,.08);`

**Step 4: Commit**
```
git add style.css
git commit -m "style: light theme for nav and footer"
```

---

### Task 2: Rewrite Hero Section

**Files:**
- Modify: `index.html` (hero section, lines ~46–138)

**Step 1: New hero headline and sub**

Replace hero content:
- Eyebrow: `Tecnologia para Engenharia`
- H1: `A equipa de TI que a sua empresa de engenharia ainda não tem`
- Sub: `Desenvolvemos plugins, automatizamos processos e criamos software à medida — para que engenheiros e arquitectos se concentrem no que sabem fazer melhor.`
- CTAs: `Falar connosco` (primary) + `Ver os nossos serviços` (ghost, href=#services)

**Step 2: Replace hero visual card**

Replace the IFC model card with a "tech stack" visual showing 4 capability pills/chips: `Plugin Revit`, `Automação`, `API & Integrações`, `Software à Medida` — styled as glowing badges inside a dark card.

**Step 3: Update hero stats**

Change 3 stats to: `Plugins` / `desenvolvidos` · `Automação` / `de processos` · `Software` / `à medida`

**Step 4: Commit**
```
git add index.html
git commit -m "feat: rewrite hero section for tech consultancy positioning"
```

---

### Task 3: Rewrite Problem Section

**Files:**
- Modify: `index.html` (problem section, lines ~141–185)

**Step 1: New headline**

- Section label: `01 — Desafios`
- H2: `Gerir tecnologia em engenharia é complexo sem o parceiro certo`
- Sub: `Pequenas empresas AEC enfrentam os mesmos problemas tecnológicos das grandes — mas sem equipa dedicada para os resolver.`

**Step 2: New 4 problem cards**

1. **Ferramentas que não comunicam** — Software de projecto, orçamento e obra em silos; dados exportados manualmente, erros acumulam-se.
2. **Software subutilizado** — Pagam licenças de ferramentas poderosas mas aproveitam apenas uma fracção do potencial.
3. **Processos manuais que escalam mal** — Tarefas repetitivas feitas à mão travam o crescimento e geram retrabalho constante.
4. **Sem apoio técnico interno** — Quando algo falha ou há uma necessidade nova, não há ninguém internamente para resolver.

**Step 3: Commit**
```
git add index.html
git commit -m "feat: rewrite problem section"
```

---

### Task 4: Rewrite Services Section

**Files:**
- Modify: `index.html` (training section → rename to services, lines ~187–248)

**Step 1: Update section id and label**

Change `id="training"` to `id="services"`. Update nav links accordingly. Label: `02 — Serviços`.

**Step 2: New headline**

H2: `Soluções à medida, independentes de software`
Sub: `Não vendemos licenças nem representamos vendors. Analisamos o vosso contexto e entregamos a solução certa — seja um plugin, uma automação ou uma plataforma completa.`

**Step 3: 4 new service cards (replace training modules)**

1. **Diagnóstico Tecnológico** — Analisamos ferramentas, fluxos e pontos de dor. Entregamos um plano claro com prioridades e ROI estimado. Bullets: Entrevistas com a equipa · Mapeamento de processos · Relatório de prioridades · Plano de acção 2–6 semanas
2. **Plugins & Extensões** — Desenvolvemos plugins para Revit, AutoCAD e outras ferramentas AEC. Automatize fluxos de trabalho directamente nas ferramentas que já usam. Bullets: Revit API / Dynamo · AutoCAD / Civil 3D · Exportações e relatórios custom · Integração com outros sistemas
3. **Automação & Integrações** — Ligamos os vossos sistemas e eliminamos trabalho manual. De Excel a APIs REST, criamos pontes entre ferramentas. Bullets: Scripts de automação · Integrações entre plataformas · Processamento de dados AEC · Relatórios automáticos
4. **Software à Medida** — Quando não existe uma solução no mercado, criamos uma. Aplicações web, ferramentas internas ou portais de projecto adaptados ao vosso negócio. Bullets: Aplicações web · Ferramentas internas · Portais de projecto · Arquitectura e manutenção

**Step 4: Commit**
```
git add index.html
git commit -m "feat: rewrite services section with 4 new offerings"
```

---

### Task 5: Rewrite Process Section

**Files:**
- Modify: `index.html` (process section, lines ~250–294)

**Step 1: Update copy (keep 4-step structure)**

Label: `03 — Como trabalhamos`
H2: `Da conversa à solução`
Sub: `Um processo simples, sem jargão e sem surpresas — do diagnóstico à entrega.`

Steps:
1. **Descoberta** — Percebemos o vosso contexto: ferramentas, processos, equipa e onde surgem as maiores fricções.
2. **Diagnóstico** — Identificamos o problema real (não apenas o sintoma) e definimos a solução mais eficiente.
3. **Proposta** — Apresentamos uma solução clara: âmbito, prazo e custo. Sem letra pequena.
4. **Entrega** — Implementamos, testamos e transferimos o conhecimento. Ficam autónomos.

**Step 2: Commit**
```
git add index.html
git commit -m "feat: rewrite process section"
```

---

### Task 6: Rewrite Outcomes / Why Us Section

**Files:**
- Modify: `index.html` (outcomes section, lines ~296–354)

**Step 1: New headline**

Label: `04 — Porquê nós`
H2: `O vosso departamento de TI externo`
(Remove sub or keep short)

**Step 2: 6 outcome cards**

1. **Sem overhead de equipa interna** — Acesso a competências de software engineering sem salários, seguros ou gestão de RH.
2. **Agnósticos de software** — Não vendemos licenças. Recomendamos e implementamos o que é certo para vós.
3. **Especializados em AEC** — Conhecemos Revit, IFC, CAD, BIM e os processos de engenharia e construção por dentro.
4. **Entregas rápidas** — Projectos com âmbito definido, sem metodologias pesadas. Da proposta à entrega em semanas, não meses.
5. **Custo previsível** — Preço fixo por projecto ou retainer mensal. Sem surpresas.
6. **Know-how que fica** — Documentamos tudo e formamos a equipa. Não criamos dependências.

**Step 3: Commit**
```
git add index.html
git commit -m "feat: rewrite outcomes/why-us section"
```

---

### Task 7: Rewrite Vision Section

**Files:**
- Modify: `index.html` (vision section, lines ~356–394)

**Step 1: New copy**

Label: `05 — Abordagem`
H2: `Tecnologia certa. No momento certo.`
Body: `Não existe uma solução universal. Começamos sempre por perceber o problema — e só depois escolhemos a ferramenta. Às vezes é um plugin de Revit. Outras vezes é uma aplicação web ou uma simples automação em Python. O que importa é que funciona para a vossa equipa.`
Second paragraph: `A CiviBIM existe para ser o parceiro tecnológico que pequenas empresas AEC merecem mas raramente têm acesso. Simples, directo e focado em resultados.`

**Step 2: Update vision nodes**

1. Diagnóstico → *Disponível agora*
2. Desenvolvimento → *Plugins, automação, software*
3. Suporte contínuo → *Retainer ou por projecto*

**Step 3: Commit**
```
git add index.html
git commit -m "feat: rewrite vision/approach section"
```

---

### Task 8: Update Nav Links & CTA Section Copy

**Files:**
- Modify: `index.html` (nav links + CTA section)

**Step 1: Update nav links**

- `#problem` → Desafios
- `#services` → Serviços (was `#training`)
- `#process` → Como trabalhamos
- `#outcomes` → Porquê nós (was Resultados)
- `#cta` → Falar connosco

**Step 2: Update CTA section**

H2: `Conte-nos o vosso desafio`
Sub: `Seja um plugin, uma automação ou uma aplicação — começamos por perceber o que precisam. Sem compromisso, sem jargão.`
Badge: `Vamos trabalhar juntos`
Form disclaimer: stays the same.

**Step 3: Update footer tagline**

Change: `BIM com método, do modelo à decisão.` → `Tecnologia para engenharia. Simples, directo, eficaz.`

**Step 4: Update page title and meta**

Title: `CiviBIM — Tecnologia para Engenharia e Construção`
Description: `A CiviBIM é o parceiro tecnológico ideal para empresas de engenharia, arquitectura e construção. Plugins, automação, integrações e software à medida — sem o custo de uma equipa interna.`

**Step 5: Commit**
```
git add index.html
git commit -m "feat: update nav, CTA, footer and meta for new positioning"
```

---

### Task 9: Final CSS Polish

**Files:**
- Modify: `style.css`

**Step 1: Add light footer styles**

Add rules for `.footer`, `.footer__tagline`, `.footer__link`, `.footer__copy` with dark text on white background.

**Step 2: Ensure nav link active/hover works on light bg**

`.nav__link:hover` should use light blue tint: `background: rgba(4,82,167,.07); color: var(--clr-primary);`

**Step 3: Update `.nav__cta-link` for light nav**

Keep blue button — it will pop well on white nav.

**Step 4: Commit**
```
git add style.css
git commit -m "style: final css polish for light nav and footer"
```
