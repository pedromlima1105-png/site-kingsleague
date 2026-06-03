# 📋 CONTENT.MD — Guia Completo do Site PatchKingsleague

> **Arquivo de referência para vibecoding.** Use este documento como base para qualquer alteração no site.
> Última atualização: 02/06/2026

---

## 🏗️ ESTRUTURA DO PROJETO

```
site-kingsleague/
├── index.html              ← Arquivo único (HTML + CSS + JS inline)
├── vercel.json             ← Configuração de deploy (site estático)
├── .gitignore              ← Ignora .mp4, .zip, .rar, .7z
├── README.md
├── content.md              ← ESTE ARQUIVO (guia de referência)
└── public/                 ← Todas as imagens e mídias
    ├── capa.png            ← Logo/capa usada no navbar e hero
    ├── Bola.png            ← Bola oficial Kings League
    ├── Chuteiras 1.png     ← Chuteiras Nike (Mercurial Vapor 16)
    ├── Chuteiras 2.png     ← Chuteiras Adidas F50 Elite
    ├── Chuteiras 3.png     ← Seleção de chuteiras
    ├── Chuteiras 4.png     ← Replay com chuteira e bola
    ├── Menu Abertura.png   ← Tela de abertura do patch
    ├── Menu Principal.png  ← Menu principal do jogo com patch
    ├── Nike.png            ← Catálogo Nike no jogo
    ├── Adidas.png          ← Catálogo Adidas no jogo
    ├── Umbro.png           ← Catálogo Umbro no jogo
    ├── Técnicos.mp4        ← Vídeo dos técnicos (NÃO vai pro GitHub)
    ├── Times.mp4           ← Vídeo dos times (NÃO vai pro GitHub)
    ├── Entrada Completa.mp4 ← Vídeo entrada (NÃO vai pro GitHub)
    └── uniformes/          ← Catálogo de uniformes por seleção
        ├── BRAZIL/         (3 imagens)
        ├── CAPIM/          (4 imagens)
        ├── DENDELE/        (4 imagens)
        ├── DESIMPAIN/      (3 imagens)
        ├── DIBRADOS/       (4 imagens)
        ├── FLUXO/          (4 imagens)
        ├── FUNKBOL/        (3 imagens)
        ├── FURIA/          (4 imagens)
        ├── G3X/            (4 imagens)
        ├── LOUD/           (4 imagens)
        └── NYVELADOS/      (3 imagens)
```

---

## 🎨 IDENTIDADE VISUAL

### Paleta de Cores
| Variável CSS       | Valor             | Uso                              |
|--------------------|--------------------|----------------------------------|
| `--bg`             | `#080808`          | Fundo principal (preto)          |
| `--bg2`            | `#0d0d0d`          | Fundo seções alternadas          |
| `--bg3`            | `#111111`          | Fundo modais e sidebar           |
| `--yellow`         | `#FFD600`          | Cor principal (amarelo ouro)     |
| `--yellow2`        | `#F0C800`          | Amarelo secundário               |
| `--yellow-dim`     | `#b89a00`          | Amarelo mais escuro              |
| `--white`          | `#f5f5f0`          | Texto principal                  |
| `--gray`           | `#888880`          | Texto secundário/descrições      |
| `--border`         | `rgba(255,214,0,0.2)` | Bordas com tom amarelo       |
| `--glass`          | `rgba(255,255,255,0.03)` | Fundo de cards (glassmorphism) |

### Fontes
| Variável           | Fonte              | Uso                              |
|--------------------|--------------------|----------------------------------|
| `--font-display`   | **Orbitron**        | Títulos, botões, preços, badges  |
| `--font-body`      | **Sora**            | Texto corrido, descrições, links |

### Efeitos Visuais
- **Glow amarelo** em destaques: `var(--glow-yellow)`
- **Grid animado** no hero (linhas amarelas se movendo)
- **Scanlines** sobrepostas no hero (estilo retro/gaming)
- **Hover com elevação** em todos os cards (`translateY(-6px)`)
- **Scroll reveal** (elementos surgem ao entrar na viewport)
- **Glitch effect** no título "KINGS LEAGUE"
- **Floating animation** na imagem do hero (subindo e descendo)

---

## 📐 SEÇÕES DO SITE (na ordem que aparecem)

### 1. NAVBAR (fixo no topo)
- **Logo**: imagem `public/capa.png` + texto "PATCH**KINGSLEAGUE**"
- **Links**: Início | Diferenciais | Uniformes | Campeonatos | Planos
- **Carrinho**: botão com badge de quantidade
- **Hamburger**: aparece em telas ≤ 900px
- **Comportamento**: fica transparente, ganha fundo escuro ao rolar

### 2. HERO (`#inicio`)
- **Badge**: "⚡ Patches ao vivo — Kings League e mais"
- **Título**: `KINGS LEAGUE` (com efeito glitch) + `PATCH` (gradiente amarelo)
- **Descrição**: "Enquanto os jogos oficiais ficam para trás, o Kings League Patch acompanha cada split em tempo real. Elencos atualizados, uniformes oficiais, escudos, faces realistas e toda a identidade da Kings League dentro do seu jogo."
- **Botões**: "Ver Planos" (amarelo) + "Como Funciona" (outline)
- **Estatísticas**: 4+ Ligas | 500+ Jogadores | 100% Em dia
- **Imagem lateral**: `public/capa.png` em círculo flutuante (some em mobile)

### 3. GALERIA HERO (`#galeria-hero`)
- **Título**: "⚽ Veja o Patch em Ação"
- **Imagens**: Bola + Chuteiras 1-4 em grade
- **Cada imagem é clicável** (abre lightbox)

### 4. DIFERENCIAIS (`#diferenciais`)
- **Tag**: "Por que PatchKingsleague?"
- **Título**: "Nós jogamos no **outro nível**"
- **Sub**: "A gente não espera o patch oficial. A PatchKingsleague já tá na frente."
- **4 Cards**:
  1. ⚡ **Atualização em Tempo Real** — "Toda mudança nos campeonatos reflete nos seus arquivos. Transferência, uniforme novo, contratação — a gente tá de olho 24/7."
  2. 🏆 **Ligas Incluídas no Patch** — "Kings League Brazil, Kings League World Cup, Kings League World Cup Nations, Kings League Spain. Todas completas e Atualizadas."
  3. 🎮 **Compatível Apenas com PC** — "Adquira o jogo sem mesmo ter o Pes 2021, Ele vem incluído no Patch. 100% funcional no Windows."
  4. 🔒 **Suporte e Comunidade VIP** — "Planos Pro e King têm suporte prioritário, acesso a novidades antes de todo mundo e uma comunidade exclusiva no Discord."
- **Botão**: "Ver mais sobre o Patch" → abre modal com todas as 10 imagens da public

### 5. UNIFORMES — CATÁLOGO (`#uniformes`)
- **Tag**: "Catálogo Completo"
- **Título**: "Uniformes por **Seleção**"
- **Sistema de abas** com 11 seleções:
  - 🇧🇷 Brazil (3 uniformes)
  - 🌿 Capim (4 uniformes)
  - ⚡ Dendele (4 uniformes)
  - 🎭 Desimpain (3 uniformes)
  - 🎯 Dibrados (4 uniformes)
  - 🌊 Fluxo (4 uniformes)
  - 🎵 Funkbol (3 uniformes)
  - 🔥 Furia (4 uniformes)
  - 🎮 G3X (4 uniformes)
  - 📢 Loud (4 uniformes)
  - ⚖️ Nyvelados (3 uniformes)
- **Cada imagem clicável** abre lightbox com navegação por setas

### 6. TÉCNICOS (`#tecnicos`)
- **Tag**: "Conteúdo Exclusivo"
- **Título**: "Técnicos no **Patch**"
- **Player de vídeo**: `public/Técnicos.mp4`
- ⚠️ **NOTA**: Vídeos .mp4 NÃO sobem pro GitHub (limite 100MB). Para funcionar na Vercel, os vídeos precisam ser hospedados externamente ou via LFS.

### 7. CAMPEONATOS (`#campeonatos`)
- **Tag**: "Cobertura Total"
- **Título**: "Campeonatos **suportados**"
- **6 Cards**:
  1. 👑 Kings League — **Atualizado** (bolinha pulsante)
  2. 🌎 Kings World Cup — **Atualizado**
  3. 🌍 Kings World Cup Nations — **Atualizado**
  4. 🇧🇷 Kings League Brazil — **Atualizado**
  5. 🇪🇸 Kings League Spain — **Atualizado**
  6. 🚀 Novas Ligas — "Sempre chegando" (sem bolinha)

### 8. PLANOS (`#planos`)
- **Tag**: "Escolha seu plano"
- **Título**: "Jogue no **próximo nível**"
- **3 Cards**:

| Plano     | Preço        | Período       | Destaque? | Features                                                     |
|-----------|-------------|---------------|-----------|--------------------------------------------------------------|
| **Starter** | R$ 34,90    | por mês       | Não       | Atualização da competição atual, Todas as Ligas, Comunidade base, Suporte via WhatsApp |
| **Pro**     | R$ 69,90    | a cada 6 meses| **SIM** (🔥 Mais Popular) | 6 meses ilimitados, Suporte prioritário, Conteúdos antecipados, Todas as ligas, Canal exclusivo Discord |
| **King**    | R$ 149,90   | por ano       | Não       | Suporte especial + instalação remota, Versões beta, Cargo especial Discord, Prioridade máxima, Enquetes de conteúdo |

- Cada plano tem botão "Adicionar ao Carrinho"

### 9. FAQ (`#faq`)
- **Tag**: "Dúvidas Frequentes"
- **Título**: "Tá na cabeça? **A gente responde.**"
- **4 perguntas** (accordion):
  1. **Como recebo os arquivos após a compra?** → "Enviamos um Link para você acessar e baixar seu patch. A gente também te explica como instalar passo a passo via WhatsApp."
  2. **Com que frequência os patches são atualizados?** → Semanais durante competição, mensais fora de temporada. Pro e King recebem antes.
  3. **Funciona em PS4, PS5 e PC?** → Apenas PC (Windows). Consoles não suportam modificação de arquivos internos.
  4. **Posso trocar de plano depois?** → Sim, upgrade com desconto proporcional. Sem contrato, sem multa.

### 10. FOOTER
- **Logo + Tagline**: "Enquanto o jogo oficial dorme, a gente tá atualizando. Sem parar."
- **Redes Sociais**: Instagram, YouTube, Discord, WhatsApp
- **Navegação**: links para todas as seções
- **Planos**: listagem com preços
- **Contato**: WhatsApp +55 12 99189-1100, Instagram, YouTube, Discord
- **Rodapé**: "© 2025 PatchKingsleague" + "⚽ Atualizando o jogo desde 2025"

---

## 🔗 LINKS E CONTATOS

### WhatsApp
- **Número**: +55 12 99189-1100
- **Link direto**: `https://wa.me/5512991891100`
- **Usado em**: botão flutuante, footer, checkout do carrinho

### Redes Sociais
| Rede       | URL                                                                                          |
|------------|----------------------------------------------------------------------------------------------|
| Discord    | `https://discord.gg/kDCFTKNGpt`                                                             |
| Instagram  | `https://www.instagram.com/kingsleaguepatch_oficial?igsh=MWFiMHJrMTYycHFvOQ%3D%3D&utm_source=qr` |
| YouTube    | `https://youtube.com/@patchkingsleagueoficial?si=iNEZK0QbBr1P_IiV`                          |

### GitHub
- **Repositório**: `https://github.com/pedromlima1105-png/site-kingsleague`
- **Branch**: `main`
- **Deploy**: Vercel (automático via GitHub)

---

## 🛒 SISTEMA DE CARRINHO

### Funcionamento
1. Usuário clica "Adicionar ao Carrinho" em qualquer plano
2. Sidebar abre mostrando item adicionado com preço
3. Pode adicionar múltiplos planos
4. Botão "Finalizar via WhatsApp" gera mensagem automática:
   ```
   Olá! 👋 Vim pelo site da *PatchKingsleague* e quero finalizar meu pedido:
   
   • Plano Pro (Semestral) — R$ 69,90
   
   💰 *Total: R$ 69,90*
   
   Pode me passar as instruções de pagamento? 🚀
   ```
5. Redireciona para WhatsApp com a mensagem pronta

### Dados dos Planos (no JS)
```javascript
const PLANS = {
  starter: { name: 'Plano Starter', period: 'Mensal',    price: 34.90,  emoji: '⚡' },
  pro:     { name: 'Plano Pro',     period: 'Semestral', price: 69.90,  emoji: '🔥' },
  elite:   { name: 'Plano King',    period: 'Anual',     price: 149.90, emoji: '👑' },
};
```

---

## 🖥️ MODAIS E OVERLAYS

| Modal                | Trigger                        | Conteúdo                                     |
|----------------------|--------------------------------|----------------------------------------------|
| **Carrinho (sidebar)** | Botão "Carrinho" no navbar   | Lista de itens, total, botão WhatsApp        |
| **Como Funciona**    | Botão "Como Funciona" no hero  | 4 passos ilustrados                          |
| **Galeria Patch**    | Botão "Ver mais" no Diferenciais | Grid com 10 imagens da public             |
| **Lightbox**         | Clique em qualquer imagem      | Imagem em tela cheia + setas de navegação    |

---

## 📱 RESPONSIVIDADE

| Breakpoint    | Mudanças                                                  |
|---------------|-----------------------------------------------------------|
| ≤ 900px       | Navbar links viram hamburger, hero image some, planos 1 coluna |
| ≤ 600px       | Padding reduzido, campeonatos 2 colunas, galeria 2 colunas    |

---

## ⚙️ DEPLOY E GIT

### Git
- **Executável**: `C:\Users\Pedro\AppData\Local\GitHubDesktop\app-3.5.11\resources\app\git\cmd\git.exe`
- **Alias para comandos**: `$git = "caminho_acima"; & $git [comando]`
- **IMPORTANTE**: Usar `;` entre comandos no PowerShell, NÃO `&&`

### .gitignore
```
*.mp4
*.zip
*.rar
*.7z
Thumbs.db
.DS_Store
desktop.ini
public/UNIFORMES-20260531T143832Z-3-001/
```

### Vercel
- Deploy automático ao push no `main`
- Configuração em `vercel.json` (site estático)
- Arquivos de `public/` são servidos diretamente

---

## 🚨 AVISOS IMPORTANTES

1. **Arquivos .mp4 NÃO vão pro GitHub** — limite de 100MB. Se precisar de vídeo no site, hospedar externamente (YouTube embed, Cloudinary, etc.)
2. **Imagem `capa.png`** — usa `<img>` com `onerror` fallback caso não carregue
3. **Nomes de arquivos com espaço** — funcionam no HTML, mas no git precisam de aspas (`"Chuteiras 1.png"`)
4. **Branch orphan** — o histórico foi recriado limpo. Sempre usar `--force` se precisar reescrever
5. **Tudo em um arquivo** — CSS e JS estão inline no `index.html`. Não há arquivos separados de estilo ou script
