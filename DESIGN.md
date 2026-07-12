# DESIGN.md — e.feito social

> Design system extraído diretamente dos arquivos de marca e componentes desta pasta (logos, ícones, fontes e telas de referência). Trate todos os valores abaixo como obrigatórios — não substitua por padrões genéricos.

**Produto:** plataforma de gestão de investimento social e leis de incentivo (cultura, esporte, ICMS, IRPJ, fundos da criança/idoso, PcD, reciclagem etc.) para empresas e organizações do terceiro setor.
**Personalidade:** institucional, confiável e "arrumadinha", mas com um acento humano e caloroso — nunca corporativa fria nem infantilizada.

---

## Color Tokens

### Marca (logo)

| Nome | Hex | Uso |
|---|---|---|
| `brand-green` | `#189478` | Cor oficial da wordmark/monograma do logo. Use apenas em aplicações de marca (logo, capas, materiais institucionais). |
| `brand-navy` | `#123956` | Tinta alternativa do logo para fundos claros/impressão. |
| `brand-coral` | `#EA573D` | Variante secundária do logo, uso pontual em campanhas/materiais de marca. |
| `brand-cream` | `#E9E1C4` | Variante suave do logo para fundos escuros com baixo contraste desejado. |

### Interface (UI)

| Nome | Hex | Uso |
|---|---|---|
| `primary` | `#009377` | Cor de ação primária: botões preenchidos, links, ícones ativos, estado ativo/hover da sidebar, sublinhado de tab ativa. Nunca decorativa. |
| `primary-hover` | `#39AC9A` | Hover/estado claro de elementos primários e realces secundários. |
| `primary-pressed` | `#189478` | Estado pressed de botões e elementos primários. |
| `ink-900` | `#0D1430` | Fundo da sidebar e superfícies escuras principais. |
| `ink-700` | `#133957` | Superfície escura secundária / texto sobre fundos claros quando `ink-900` for pesado demais. |
| `danger` | `#CD2525` | Ações destrutivas (excluir, limpar filtros), erros e validação negativa. Nunca use para ênfase comum. |
| `warning` | `#D8A722` | Estado "em andamento"/atenção em steppers e indicadores de progresso. |
| `text-strong` | `#2D2D2D` | Texto de maior ênfase sobre fundo claro (títulos, valores). |
| `text-muted` | `#767676` | Texto secundário, labels, placeholders. |
| `text-disabled` | `#A5A5A5` | Texto e ícones desabilitados. |
| `border` | `#E5E5EA` | Bordas e divisores padrão. |
| `border-strong` | `#D1D1D6` | Bordas de inputs e componentes interativos. |
| `surface` | `#FFFFFF` | Fundo padrão de páginas e cards. |
| `surface-subtle` | `#F2F2F2` | Fundo de inputs, pills de status e áreas de apoio. |
| `surface-canvas` | `#FDFDFD` | Fundo geral de telas (levemente off-white). |

### Paleta de categorias (ícones de leis/temas)

Usada **exclusivamente** para diferenciar categorias/tags (ex.: tipos de lei de incentivo) — nunca para ações de UI ou estados de sistema.

| Nome | Hex |
|---|---|
| `cat-purple` | `#9747FF` |
| `cat-violet` | `#8A48B9` |
| `cat-blue` | `#0077B7` |
| `cat-cyan` | `#14ACDB` |
| `cat-indigo` | `#5477D0` |
| `cat-coral` | `#EB6158` |
| `cat-green` | `#72D77C` |
| `cat-pink` | `#F177FC` |
| `cat-navy` | `#184A94` |
| `cat-yellow` | `#FBCB50` |
| `cat-gold` | `#D8A722` |
| `cat-orange` | `#F77C30` |

### Estados de status (pills)

| Status | Cor do indicador |
|---|---|
| Rascunho | `#2D2D2D` (preto/cinza-escuro) |
| Ativa | `#4FBB51` (verde) |
| Finalizada | `#5477D0` (azul) |

**Contraste:** todo texto sobre `ink-900`/`ink-700` deve ser branco ou `surface-canvas`. Texto sobre `primary` deve ser branco. Nunca usar `text-muted` sobre fundos escuros.

---

## Typography

**Fonte de interface:** `Montserrat` (arquivos `Montserrat-*.ttf` e `Montserrat-VariableFont_wght.ttf` nesta pasta, pesos de Thin/100 a Black/900, com itálicos correspondentes). Use a variable font quando o ambiente suportar; caso contrário, os pesos estáticos.

**Fonte de marca/display:** `Plateia Bold` (`Plateia Bold.ttf`) — reservada para o wordmark do logo e headlines de grande destaque em materiais institucionais/campanhas. Não usar em textos de interface (botões, tabelas, formulários).

**Fonte decorativa:** `String Beads Regular` (`String Beads Regular.ttf`) — uso pontual e opcional em contextos ilustrativos/lúdicos (ex.: certificados, posts sociais). Nunca em UI funcional ou blocos de texto longos.

| Estilo | Fonte | Tamanho | Peso | Line-height |
|---|---|---|---|---|
| H1 | Montserrat | 32px | Bold (700) | 1.2 |
| H2 | Montserrat | 24px | Bold (700) | 1.25 |
| H3 / Título de card | Montserrat | 18–20px | SemiBold (600) | 1.3 |
| Body | Montserrat | 15–16px | Regular (400) | 1.5 |
| Label / Botão | Montserrat | 15–16px | Bold (700) | 1 |
| Caption / Helper | Montserrat | 13px | Regular (400) | 1.4 |
| Overline (categorias de menu: "GESTÃO", "COMUNICAÇÃO") | Montserrat | 12px | SemiBold (600), letter-spacing +0.04em, uppercase | 1.2 |
| Saudação/destaque sidebar ("Olá, Nome!") | Montserrat | 16px | Bold Italic | 1.3 |

---

## Spacing

Grid base de **4px**, com escala em múltiplos de 4/8, derivada das dimensões reais dos componentes (altura de botão/input = 39–43px, cards com padding generoso):

| Token | Valor |
|---|---|
| `space-1` | 4px |
| `space-2` | 8px |
| `space-3` | 12px |
| `space-4` | 16px |
| `space-5` | 20px |
| `space-6` | 24px |
| `space-8` | 32px |
| `space-10` | 40px |

- Padding horizontal interno de botões/inputs: `space-5` (20px).
- Padding vertical interno de botões/inputs: `space-2`–`space-3` (altura final ~39–43px).
- Gap entre itens de lista (sidebar, dropdown, filtros): `space-4` a `space-6`.
- Padding de cards/tabelas: `space-5`–`space-6`.
- Gap entre seções da sidebar: `space-8`.

---

## Layout

- **Sidebar fixa à esquerda**, fundo `ink-900`, com dois modos: expandida (ícone + label) e recolhida (apenas ícone, mesma largura de toggle). Alterna via botão no topo.
- Itens de navegação agrupados por seção com overline em `text-muted`/verde claro (GESTÃO, COMUNICAÇÃO, PESQUISA). Item ativo/hover recebe fundo `primary` em pill arredondada (`radius-md`), texto branco em negrito.
- **Área de conteúdo** em `surface-canvas`, com breadcrumb no topo (`text-muted` → item atual em `text-strong` bold), título H1, subtítulo em `body`/`text-muted`.
- **Blocos de filtro** sempre acima da tabela/listagem: busca com ícone à direita + dropdowns em linha + ações utilitárias (visualização de colunas, limpar filtros em `danger` outline).
- **Tabelas/cards de dados**: container `surface` com `radius-md` (12px), header com labels `text-muted` bold, linhas separadas por `border`, ação primária de adicionar como botão outline `primary` alinhado à coluna.
- Radius de moldura/frame externo (containers grandes de tela): 4–5px — não usar em componentes internos.
- Componentes interativos (botão, input, select, pill) são sempre **totalmente arredondados** (`radius-pill`, raio = metade da altura).

---

## Components

**Border-radius**
- `radius-pill`: altura/2 (botões, inputs, selects, status pills, tags) — ex. 39px altura → 19.5px de raio.
- `radius-md`: 12px (cards, tabelas, containers).
- `radius-sm`: 4–5px (molduras externas/artboards).

**Botões** (ver `Botões.svg`)
- Primário: fundo `primary`, texto branco bold, `radius-pill`.
- Secundário/outline: borda `primary` 1.5–2px, texto `primary`, fundo transparente.
- Destrutivo: fundo ou outline `danger`, texto branco (preenchido) ou `danger` (outline).
- Desabilitado: fundo/borda em cinza `text-disabled`/`border-strong`, texto `text-disabled` — nunca usar `primary` ou `danger` dessaturados manualmente.
- Ghost/texto: sem fundo nem borda, apenas texto colorido (`primary` ou `danger`), usado em ações terciárias.
- Ícone sempre à esquerda do label, 20–24px.

**Inputs, selects e filtros** (ver `Filtros.svg`)
- Fundo `surface-subtle` (busca) ou `surface` com borda `border-strong` (selects), `radius-pill`, ícone (lupa/chevron) à direita, placeholder em `text-muted`.

**Status pills** (ver `Status de Campanha.svg`)
- Fundo `surface-subtle`, `radius-pill`, dot colorido de 12px à esquerda + label bold `text-muted` + chevron.

**Tabs/Sub-categoria** (ver `Tab Navigation.svg`, `Tab Item.svg`)
- Inativa: `text-muted` regular. Ativa: `primary` bold + barra inferior `primary` (3–4px). Badge contador: pill `primary` (ativo) ou cinza (inativo) com número branco/`text-muted`.

**Stepper/Barra de progresso** (ver `Barra de progresso.svg`, `Etapas.svg`)
- Segmentos em pill, preenchidos `primary`, pendentes `border-strong`, etapa em edição com outline `warning`.

**Breadcrumb/lista de etapas em fundo escuro** (ver `Breadcrumb Item.svg`)
- Fundo cinza-escuro/`ink-700`, borda esquerda 2–3px + texto bold em `primary-hover` (`#39AC9A`) para o item ativo; itens inativos em branco 70% de opacidade.

**Tabela** (ver `Table 3 Columns _ Example.svg`, `Frame Contatos.svg`)
- Header bold `text-muted`, linhas com `border`, célula de ação com botão outline `primary` pill.

**Tags de categoria com ícone** (ver `Recursos Dropdown.svg`, `Component 2.svg`)
- Linha com borda `border`, `radius-pill`, ícone colorido (paleta de categorias) + label bold `ink-900` + chevron `text-muted`.

**Ícones** (ver `Ícones.svg`)
- Set de linha, stroke ~2px, 24px de área. Estado padrão `primary`, destrutivo `danger`, desabilitado `text-disabled`/outline cinza claro.

**Sombras:** não há uso de sombra pesada nos componentes de referência — preferir bordas (`border`) e blocos de cor sólidos a `box-shadow`. Se necessário elevar um elemento (modal, dropdown aberto), usar sombra muito sutil: `0 4px 12px rgba(13,20,48,0.08)`.

---

## Motion

Não há especificações de animação nos arquivos de origem (são exports estáticos). Até haver referência oficial, seguir como padrão conservador e institucional:

- `duration-fast`: 120ms — hover de botões, toggles.
- `duration-base`: 200ms — abrir/fechar dropdown, troca de tab, expandir/recolher sidebar.
- `duration-slow`: 300ms — transições de página/modal.
- Easing padrão: `ease-out` (entradas), `ease-in` (saídas). Evitar easings "bouncy"/elásticos — não combina com o tom institucional da marca.

---

## Voice & Content

- Tom: direto, acolhedor e profissional — fala com gestores de projetos sociais e equipes de compliance/fiscal, então precisão importa (nomes de leis, siglas como IRPJ/ICMS/PcD devem ser exatos).
- Pronomes: trate o usuário diretamente ("Olá, Nome!", "Faça a gestão de..."), evite jargão de marketing.
- CTAs claros e específicos ao objeto: "Adicionar Novo Contato", "Adicionar Doc", "Limpar filtros" — nunca genéricos como "Enviar" ou "OK" quando o contexto permitir ser específico.
- Vocabulário a evitar: superlativos vazios ("incrível", "revolucionário", "mágico"), jargão corporativo genérico, emojis em UI funcional (a marca já tem ícones próprios para isso).
- Português do Brasil, formal-neutro (nem "você" excessivamente informal, nem "senhor(a)" formal demais).

---

## Brand

- **Wordmark principal:** `EF-1122_Logo_Prancheta 1.png` (navy, `#123956`) — versão institucional/documental padrão.
- **Wordmark cor primária:** `EF-1122_Logo-02.png` (verde `#189478`) — uso em produto/digital sobre fundo claro.
- **Wordmark sobre fundo escuro:** `EF-1122_Logo-09.png` (branco) — usada no topo da sidebar (`ink-900`).
- **Monograma "e/a"** (ícone isolado, sem o restante da wordmark): `EF-1122_Logo-20.png` (verde) — para favicons, avatares, espaços muito reduzidos.
- **Lockup empilhado/vertical**: `EF-1122_Logo-14.png` (verde) — para formatos quadrados/estreitos.
- Variantes adicionais de cor (coral `#EA573D`, creme `#E9E1C4`, preto, branco) disponíveis nos demais `EF-1122_Logo-*.png` desta pasta — usar coral/creme apenas em materiais de campanha, não na interface do produto.
- **Área de proteção:** manter espaço livre ao redor do logo equivalente à altura do "e" inicial da wordmark. Não aproximar outros elementos gráficos ou texto dentro dessa margem.
- **Tamanho mínimo:** não reduzir a wordmark horizontal abaixo de ~120px de largura em tela (a inscrição "social" perde legibilidade abaixo disso); nesses casos, usar o monograma "e/a" isolado.
- **Não fazer:**
  - Não recolorir o logo fora das variantes fornecidas (verde, navy, coral, creme, branco, preto).
  - Não aplicar o logo colorido sobre fundos de baixo contraste (ex. verde sobre `primary`, navy sobre `ink-900`) — nesses casos usar a versão branca.
  - Não distorcer, rotacionar ou adicionar sombra/contorno ao logo.
  - Não separar o ícone "e/a" do restante da wordmark ao usar a versão completa (só usar o monograma isolado quando explicitamente necessário por espaço).

---

## Anti-patterns

Proibido:
- Gradientes de qualquer tipo (a marca é 100% cor sólida).
- Emojis como ícone em botões/CTAs — usar sempre o set de ícones de linha da marca (`Ícones.svg`).
- Cantos retos em botões, inputs, pills e tags — sempre `radius-pill`.
- Usar a paleta de categorias (`cat-*`) para estados de sistema, ações primárias ou botões — essa paleta é só para identificação de tags/categorias.
- Usar `danger` (`#CD2525`) para qualquer coisa que não seja destrutivo/erro.
- Sombras pesadas/drop-shadow genérico de UI kit (ex. `box-shadow: 0 10px 30px rgba(0,0,0,0.3)`).
- Easing elástico/bounce em transições.
- Misturar `Plateia Bold` ou `String Beads Regular` em texto de interface — são fontes de marca/decorativas, não de produto.
- Texto em caixa alta fora dos overlines de menu (12px, letter-spacing definido) — não usar uppercase para ênfase geral.

---

## Assets de referência nesta pasta

| Tipo | Arquivos |
|---|---|
| Logos | `EF-1122_Logo-02.png` … `EF-1122_Logo-30.png`, `EF-1122_Logo_Prancheta 1.png` |
| Fontes | `Montserrat-*.ttf`, `Montserrat-VariableFont_wght.ttf`, `Montserrat-Italic-VariableFont_wght.ttf`, `Plateia Bold.ttf`, `String Beads Regular.ttf` |
| Componentes (SVG) | `Botões.svg`, `Ícones.svg`, `Barra de progresso.svg`, `Status de Campanha.svg`, `Etapas.svg`, `Filtros.svg`, `Breadcrumb Item.svg`, `Sidebar.svg`, `Sidebar Item.svg`, `Tab Navigation.svg`, `Tab Item.svg`, `Recursos Dropdown.svg`, `Component 2.svg`, `Table 3 Columns _ Example.svg`, `Frame Contatos.svg` |

Ao gerar qualquer tela ou componente novo, siga estritamente os tokens acima. Quando um caso não estiver coberto aqui, use o componente existente mais próximo (`Frame Contatos.svg` é a referência mais completa de tela real) como base de proporção, espaçamento e hierarquia.
