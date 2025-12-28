# 🙏 Jornada da Graça - Recomeço com Cristo

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub last commit](https://img.shields.io/github/last-commit/Thigil15/Jornadadagraca)](https://github.com/Thigil15/Jornadadagraca/commits)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Code of Conduct](https://img.shields.io/badge/Code%20of-Conduct-blue.svg)](CODE_OF_CONDUCT.md)

**Uma experiência web interativa e imersiva que apresenta a mensagem transformadora da graça cristã**

[🌐 Ver Demo](https://thigil15.github.io/Jornadadagraca/) · [📖 Documentação](docs/) · [🐛 Reportar Bug](https://github.com/Thigil15/Jornadadagraca/issues) · [💡 Sugerir Feature](https://github.com/Thigil15/Jornadadagraca/issues)

</div>

---

## 📖 Sobre o Projeto

**Jornada da Graça** é uma Progressive Web App (PWA) que transforma a mensagem tradicional do evangelho em uma experiência digital moderna e interativa. Desenvolvida como uma Single Page Application (SPA), a aplicação guia os visitantes através de uma jornada espiritual estruturada sobre **graça, perdão e recomeço com Cristo**.

### 🎯 Objetivo

Transformar um panfleto evangelístico tradicional em uma experiência digital imersiva que:
- ✨ **Captura a atenção** através de design moderno e animações envolventes
- 🎭 **Conta uma história** progressiva sobre graça e transformação
- 💡 **Engaja o visitante** com elementos interativos significativos
- 📱 **Alcança qualquer pessoa** com acesso mobile-first e PWA
- 🙏 **Facilita decisões** com convites claros e recursos de acompanhamento

### 🌟 Diferenciais

- **Narrativa Visual Estruturada**: Progressão natural do questionamento à ação
- **Design Emocional**: Cada elemento é pensado para tocar o coração
- **Tecnologia Moderna**: PWA, offline-first, instalável como app
- **Zero Dependências**: Vanilla JavaScript, sem frameworks pesados
- **Open Source**: Código aberto para comunidades adaptarem e melhorarem

### 🎨 Filosofia de Design

A aplicação segue princípios de **storytelling visual**, onde:
1. Cada seção constrói sobre a anterior
2. Animações reforçam conceitos espirituais
3. Interações simbolizam transformações reais
4. O design facilita (não distrai) a mensagem

---

## ⚡ Quick Start

### 🌐 Visualização Rápida

**Opção 1 - Acesse Online (Recomendado)**
```
https://thigil15.github.io/Jornadadagraca/
```

**Opção 2 - Execute Localmente**
```bash
# Clone o repositório
git clone https://github.com/Thigil15/Jornadadagraca.git

# Entre no diretório
cd Jornadadagraca

# Abra index.html no seu navegador
# Não requer Node.js, npm, ou build steps!
```

**Opção 3 - Instale como PWA**
- No navegador móvel, toque em "Adicionar à tela inicial"
- Use como um aplicativo nativo
- Funciona offline após primeira visita!

### 🔐 Acesso Administrativo

Para gerenciar testemunhos, contatos e versículos:

**Configuração Inicial:**
```bash
# Copie o template de credenciais e configure suas credenciais
cp data/admin-credentials.json.example data/admin-credentials.json
# Edite o arquivo data/admin-credentials.json com seu editor preferido
```

**Acesso:**
```
URL: /src/admin/login.html (ou /admin.html)

⚠️ IMPORTANTE: As credenciais de acesso (email e senha) estão armazenadas 
no arquivo data/admin-credentials.json. Configure suas próprias credenciais
antes do primeiro acesso e mantenha-as em segurança.

⚠️ SEGURANÇA: O arquivo data/admin-credentials.json não deve ser commitado
no repositório (já está no .gitignore).
```

---

## ✨ Funcionalidades Principais

### Para Visitantes
- **🎯 Jornada Guiada**: Progressão narrativa estruturada (Questionamento → Dilema → Revelação → Benefícios → Ação)
- **💫 Animações de Entrada**: Elementos surgem suavemente conforme o usuário rola a página
- **📝 Título Animado**: Revelação palavra por palavra para impacto visual
- **🎨 Efeito Tilt 3D**: Cartões com inclinação 3D que respondem ao movimento do mouse (desktop)
- **🗑️ Interação Simbólica**: "Descarte" visual dos pesos do passado ao clicar nos cartões
- **🎁 Galeria Interativa**: Cartões expansíveis que revelam os benefícios da graça
- **⌨️ Animação de Máquina de Escrever**: Oração final "digitada" após confirmação do usuário
- **🧭 Navegação de Progresso**: Menu lateral que indica em qual seção o usuário está
- **📱 Design Responsivo**: Mobile-first, otimizado para todos os dispositivos
- **🌈 Fundo Animado**: Gradiente sutil e animado para atmosfera serena
- **💬 Sistema de Testemunhos**: Usuários podem compartilhar suas experiências
- **📞 Formulário de Contato**: Para pedidos de oração, estudos bíblicos e visitas
- **📖 Versículo do Dia**: Rotação diária de versículos bíblicos inspiradores
- **📤 Compartilhamento Social**: Botões para WhatsApp, Facebook, Twitter, Telegram, Instagram e Email

### Para Administradores
- **🔐 Sistema de Login Seguro**: Autenticação baseada em JSON
- **💬 Gerenciamento de Testemunhos**: Aprovar, reprovar ou excluir comentários
- **📞 Gerenciamento de Contatos**: Visualizar e exportar solicitações de contato
- **📖 Gerenciamento de Versículos**: Adicionar, editar, excluir e importar versículos
- **📊 Estatísticas**: Visualização rápida de pendências e totais
- **📥 Exportação de Dados**: Download de comentários, contatos e versículos em JSON
- **🚪 Logout Seguro**: Sessão de 24 horas com renovação automática

## 🚀 Tecnologias e Stack

### Frontend Core

| Tecnologia | Uso | Motivo |
|-----------|-----|--------|
| **HTML5** | Estrutura semântica | Acessibilidade e SEO |
| **CSS3** | Estilização | Animações nativas e performance |
| **Tailwind CSS** | Framework CSS | Desenvolvimento rápido e consistente |
| **Vanilla JavaScript (ES6+)** | Lógica e interatividade | Zero overhead, máxima performance |

### APIs Web Utilizadas

- **Intersection Observer API** - Animações ao scroll de forma performática
- **LocalStorage API** - Persistência de dados do usuário
- **SessionStorage API** - Gerenciamento de sessão administrativa
- **Service Worker API** - Funcionalidade offline (PWA)
- **Fetch API** - Carregamento assíncrono de dados
- **Clipboard API** - Compartilhamento de conteúdo

### Progressive Web App (PWA)

- ✅ **Instalável** - Adicione à tela inicial
- ✅ **Offline-First** - Funciona sem internet após cache
- ✅ **App-Like** - Experiência de aplicativo nativo
- ✅ **Leve** - Menos de 1MB total

### Características Técnicas

- 🚫 **Zero Build Steps** - Sem webpack, babel ou npm
- 🚫 **Zero Dependencies** - Sem node_modules ou frameworks pesados
- ✅ **100% Client-Side** - Deploy em qualquer servidor estático
- ✅ **Mobile-First** - Design responsivo otimizado
- ✅ **SEO Ready** - Meta tags e estrutura semântica
- ✅ **Acessível** - WCAG 2.1 AA compliance

> 💡 **Filosofia**: Simplicidade sem sacrificar funcionalidade. Código limpo, manutenível e eficiente.

---

## 📁 Estrutura do Projeto

```
Jornadadagraca/
├── 📄 index.html              # Página principal da aplicação
├── 📄 admin.html              # Redirecionador para painel admin
├── 📄 manifest.json           # Configuração PWA
├── 📄 service-worker.js       # Service worker para cache offline
├── 📄 LICENSE                 # Licença MIT
├── 📄 README.md              # Documentação principal (este arquivo)
├── 📄 CONTRIBUTING.md        # Guia de contribuição
├── 📄 CODE_OF_CONDUCT.md     # Código de conduta
├── 📄 CONTATOS.md            # Instruções para acessar contatos
├── 📄 .gitignore             # Arquivos ignorados pelo Git
│
├── 📂 data/                  # Dados da aplicação (JSON)
│   ├── admin-credentials.json.example  # Template de credenciais (copie para admin-credentials.json)
│   ├── comentarios.json          # Testemunhos aprovados
│   └── versiculos.json           # Base de versículos bíblicos
│
├── 📂 src/                   # Código fonte
│   └── admin/               # Painel administrativo
│       ├── login.html       # Página de login admin
│       └── admin.html       # Dashboard administrativo
│
└── 📂 docs/                  # Documentação técnica
    ├── DEPLOYMENT.md        # Guia completo de deployment
    └── ARCHITECTURE.md      # Arquitetura técnica detalhada
```

---

## 📖 Como Funciona o Site

### 🎭 Jornada do Visitante

A experiência é estruturada como uma **narrativa progressiva** em 8 seções:

#### 1. 🌅 **Início** - O Questionamento
- Título animado palavra por palavra: _"O que você faria se pudesse recomeçar de novo?"_
- Convite para iniciar a jornada
- Animações de fade-in para criar atmosfera

#### 2. ⛓️ **O Dilema** - Reconhecendo os Pesos
- Cards interativos com **efeito tilt 3D** (desktop)
- Três pesos universais: Falhas, Ansiedade, Vazio
- Click simboliza "descartar" o peso
- Transição visual que prepara para a solução

#### 3. 📖 **Versículo do Dia**
- Rotação automática baseada no dia do ano
- Carregado de `data/versiculos.json`
- Mensagem reflexiva acompanhando cada versículo

#### 4. ✨ **A Graça** - O Conceito Transformador
- Explicação clara e acessível da graça cristã
- Citações bíblicas contextualizadas
- Design que convida à contemplação

#### 5. 🆕 **Nova Criação** - A Promessa
- Conceito de transformação e recomeço
- Versículo central: 2 Coríntios 5:17
- Ponte entre compreensão e aplicação

#### 6. 🚪 **Ele Está à Porta** - O Convite Pessoal
- Apocalipse 3:20 - Jesus aguardando decisão
- Transição da teoria para a prática
- Preparação para os benefícios

#### 7. 🎁 **Benefícios** - Os Dons da Nova Vida
- **Galeria interativa** de 4 cards expansíveis
- Click expande para revelar detalhes
- Benefícios: Perdão, Nova Identidade, Força, Propósito

#### 8. 🛤️ **O Caminho** - Como Responder
- Três passos claros: Reconheça, Creia, Receba
- Design numerado e progressivo
- Guia prático para decisão

#### 9. 💬 **Testemunhos**
- Histórias reais de transformação
- Sistema de rating (5 estrelas)
- Formulário para enviar testemunho próprio

#### 10. 📚 **Recursos**
- Links para Bíblia online
- Música de adoração
- Localizador de igrejas

#### 11. 📤 **Compartilhamento**
- 6 redes sociais integradas
- Mensagens pré-formatadas
- Facilita evangelização digital

#### 12. 🤝 **Acompanhamento**
- Fluxo de consentimento respeitoso
- Formulário de contato condicional
- Opções: Oração, Ajuda, Estudos, Visita

#### 13. 🙏 **Oração Pessoal**
- Botão de decisão consciente
- **Efeito typewriter** para criar momento especial
- Seleção aleatória de 6 orações baseadas em arrependimento, fé e obediência

### 🎨 Interações Especiais

| Elemento | Efeito | Simbolismo |
|----------|--------|------------|
| Cards de "pesos" | Fade ao clicar | Liberação e descarte |
| Cards de benefícios | Expansão suave | Descoberta e revelação |
| Oração typewriter | Digitação lenta | Momento solene e pessoal |
| Navegação lateral | Tracking de scroll | Progresso na jornada |
| Animações de entrada | Fade + translateY | Surgimento de esperança |

---

## 🔐 Painel de Administração

### 🚀 Acesso ao Admin

**URL**: `/admin.html` ou `/src/admin/login.html`

**Configuração de Credenciais**:
```bash
# Antes do primeiro acesso, configure suas credenciais:
cp data/admin-credentials.json.example data/admin-credentials.json

# Edite o arquivo e defina seu email e senha
```

**Formato do arquivo data/admin-credentials.json**:
```json
[
  {
    "email": "seu-email@exemplo.com",
    "password": "SuaSenhaSegura123!"
  }
]
```

⚠️ **IMPORTANTE**: 
- Configure credenciais fortes antes do primeiro uso
- O arquivo data/admin-credentials.json não é versionado (está no .gitignore)
- Mantenha suas credenciais em segurança e não compartilhe

### 📊 Dashboard Administrativo

#### 1️⃣ **Gerenciamento de Testemunhos**

**Recursos:**
- 📋 Visualizar todos os testemunhos (aprovados e pendentes)
- ✅ Aprovar testemunhos para exibição pública
- ❌ Reprovar ou excluir testemunhos inadequados
- 📥 Exportar todos em JSON
- 📊 Estatísticas: Total, Aprovados, Pendentes

**Fluxo:**
```
Visitante envia → Salvo como "pendente" → Admin revisa → Aprova/Reprova → Exibe no site
```

#### 2️⃣ **Gerenciamento de Contatos**

**Recursos:**
- 📋 Visualizar todas as solicitações
- 👤 Ver detalhes completos (nome, email, telefone, necessidade)
- 🗑️ Excluir contatos processados
- 📥 Exportar para JSON (integração com CRM)
- 📊 Contador de solicitações

**Campos Capturados:**
- Nome completo
- Email
- Telefone (com DDD)
- Necessidade: Oração | Ajuda | Estudos Bíblicos | Visita | Outros
- Descrição (se "Outros")
- Data/hora de envio

#### 3️⃣ **Gerenciamento de Versículos**

**Recursos:**
- ➕ Adicionar novos versículos
- ✏️ Editar versículos existentes
- 🗑️ Excluir versículos
- 📥 Importar lote (JSON)
- 📤 Exportar todos (JSON)
- 🔄 Preview de rotação diária

**Estrutura de Versículo:**
```json
{
  "text": "Texto do versículo",
  "reference": "Livro X:Y",
  "message": "Mensagem reflexiva"
}
```

### 🔒 Segurança do Admin

**Implementação Atual (Client-Side):**
- ✅ Autenticação por JSON
- ✅ Sessão de 24 horas (SessionStorage)
- ✅ Logout manual
- ✅ Auto-logout ao fechar navegador

**⚠️ Limitações Conhecidas:**
- Credenciais em plain text
- Sem criptografia
- Apenas client-side
- Dados em LocalStorage

**📚 Para Produção - Veja**: [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md#-segurança)

---
- Adicione novos versículos bíblicos
- Edite versículos existentes
- Exclua versículos
- Importe/exporte listas de versículos em JSON

### 🔒 Segurança do Admin

**Implementação Atual (Client-Side):**
- ✅ Autenticação por JSON
- ✅ Sessão de 24 horas (SessionStorage)
- ✅ Logout manual
- ✅ Auto-logout ao fechar navegador

**⚠️ Limitações Conhecidas:**
- Credenciais em plain text
- Sem criptografia
- Apenas client-side
- Dados em LocalStorage

**📚 Para Produção - Veja**: [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md#-segurança)

---

## 🎨 Design System

### Paleta de Cores

A paleta foi escolhida para transmitir **serenidade, acolhimento e esperança**:

```css
/* Cores Primárias */
--brand-primary: #B38B6D    /* Serene Dawn - Tom quente e acolhedor */
--brand-dark: #a17c60       /* Tom escuro para hover states */

/* Background */
--bg-gradient-start: #FDFBF8  /* Off-white suave */
--bg-gradient-mid: #F8F6F2    /* Bege muito claro */
--bg-gradient-end: #EAE3D9    /* Bege claro */

/* Tipografia */
--text-heading: #3A3A3A     /* Cinza escuro para títulos */
--text-body: #4A4A4A        /* Cinza médio para corpo */
--text-muted: #6B7280       /* Cinza claro para texto secundário */
```

### Tipografia

**Fonte**: [Inter](https://fonts.google.com/specimen/Inter) - Moderna, legível, humanista

```css
Pesos usados: 300 (Light), 400 (Regular), 500 (Medium), 600 (Semibold), 700 (Bold)

Escalas:
- Corpo: 1rem (16px)
- Lead: 1.125rem (18px)
- H3: 1.25rem (20px)
- H2: 1.875rem - 2.25rem (30-36px)
- H1: 2.25rem - 3.75rem (36-60px)
```

### Animações

| Nome | Duração | Uso |
|------|---------|-----|
| `fadeIn` | 0.8s - 1s | Elementos entrando na viewport |
| `titleReveal` | 0.8s | Palavras do título principal |
| `gradientBG` | 20s | Background animado sutil |
| `bounce` | 2s | Seta de scroll |
| `typewriter` | Character-based | Oração final |

---

## 📱 Progressive Web App (PWA)

### 🚀 Funcionalidades PWA

- ✅ **Instalável** - Adicione à tela inicial (Android/iOS)
- ✅ **Offline-First** - Funciona sem internet após cache inicial
- ✅ **App-Like Experience** - Fullscreen, sem barra do navegador
- ✅ **Fast Load** - Service Worker cacheia assets críticos
- ✅ **Auto-Update** - Novo conteúdo sincroniza automaticamente

### 📲 Como Instalar

**Android (Chrome):**
1. Abra o site no Chrome
2. Toque no menu (⋮) → "Adicionar à tela inicial"
3. Confirme a instalação

**iOS (Safari):**
1. Abra o site no Safari
2. Toque no botão de compartilhar (□ com seta)
3. Role e toque em "Adicionar à Tela de Início"
4. Confirme

**Desktop (Chrome/Edge):**
1. Ícone de instalação aparece na barra de endereço
2. Clique em "Instalar"
3. App abre em janela própria

### ⚙️ Configuração do Service Worker

```javascript
// Arquivos cacheados:
- index.html, admin.html
- src/admin/*.html
- manifest.json
- Fontes do Google Fonts
- Tailwind CSS CDN

// Estratégia: Cache-First
// Fallback: Network se cache falha
```

---

## 🚀 Deployment

### 📋 Pré-requisitos

- ✅ Servidor web estático (Apache, Nginx, ou plataforma cloud)
- ✅ HTTPS (obrigatório para PWA e Service Workers)
- ❌ Não requer Node.js, PHP, ou backend
- ❌ Não requer build steps ou compilation

### 🌐 GitHub Pages (Recomendado - Gratuito)

1. **Configure no Repositório**
   ```
   Settings → Pages → Source: main branch (root)
   ```

2. **Acesse**
   ```
   https://[seu-usuario].github.io/Jornadadagraca/
   ```

3. **Deploy Automático**
   - Cada push para `main` = deploy automático em ~2 minutos

### ☁️ Outras Plataformas

| Plataforma | Custo | Deploy | HTTPS | Recomendação |
|-----------|-------|--------|-------|-------------|
| **Netlify** | Gratuito | Automático (Git) | ✅ Sim | ⭐⭐⭐⭐⭐ Excelente |
| **Vercel** | Gratuito | Automático (Git) | ✅ Sim | ⭐⭐⭐⭐⭐ Excelente |
| **Cloudflare Pages** | Gratuito | Automático (Git) | ✅ Sim | ⭐⭐⭐⭐ Muito Bom |
| **Firebase Hosting** | Gratuito | Manual (CLI) | ✅ Sim | ⭐⭐⭐⭐ Muito Bom |

**📚 Guia Completo**: [docs/DEPLOYMENT.md](docs/DEPLOYMENT.md)

---

## 🤝 Contribuindo

Contribuições são **muito bem-vindas**! Este projeto é open source e acreditamos que a comunidade pode torná-lo ainda melhor.

### 🎯 Formas de Contribuir

- 🐛 **Reportar bugs** - Encontrou algo quebrado?
- 💡 **Sugerir features** - Tem ideias de melhorias?
- 📖 **Adicionar versículos** - Expanda a base de versículos
- 🌐 **Traduzir** - Leve a mensagem para outros idiomas
- ♿ **Melhorar acessibilidade** - Torne inclusivo para todos
- 📝 **Documentação** - Ajude outros a entender o projeto
- 🎨 **Design** - Melhore a experiência visual
- 💻 **Código** - Implemente features ou corrija bugs

### 🚀 Como Contribuir

1. **Fork** o repositório
2. **Clone** seu fork
   ```bash
   git clone https://github.com/SEU-USUARIO/Jornadadagraca.git
   ```
3. **Crie uma branch**
   ```bash
   git checkout -b feature/minha-contribuicao
   ```
4. **Faça suas mudanças** e commit
   ```bash
   git commit -m "feat: adiciona nova funcionalidade"
   ```
5. **Push** para seu fork
   ```bash
   git push origin feature/minha-contribuicao
   ```
6. **Abra um Pull Request** no repositório original

### 📚 Leia Mais

- 📖 [Guia Completo de Contribuição](CONTRIBUTING.md)
- 🤝 [Código de Conduta](CODE_OF_CONDUCT.md)
- 🏗️ [Arquitetura do Projeto](docs/ARCHITECTURE.md)

---

## 📄 Licença

Este projeto está licenciado sob a **MIT License** - veja o arquivo [LICENSE](LICENSE) para detalhes.

**Em resumo, você pode:**
- ✅ Usar comercialmente
- ✅ Modificar livremente
- ✅ Distribuir
- ✅ Uso privado

**Com as condições:**
- 📋 Incluir a licença e copyright nos seus projetos
- 🚫 Sem garantia (uso por sua conta e risco)

---

## 👥 Autor e Contato

**Thiago Dias**
- 🐙 GitHub: [@Thigil15](https://github.com/Thigil15)
- 📧 Email: Disponível no perfil do GitHub

### 💬 Suporte e Comunidade

- 🐛 [Reportar Bugs](https://github.com/Thigil15/Jornadadagraca/issues/new?labels=bug)
- 💡 [Solicitar Features](https://github.com/Thigil15/Jornadadagraca/issues/new?labels=enhancement)
- ❓ [Fazer Perguntas](https://github.com/Thigil15/Jornadadagraca/issues/new?labels=question)
- 📖 [Ver Documentação](docs/)
- 📧 Email: Disponível no perfil do GitHub [@Thigil15](https://github.com/Thigil15)

---

## 📚 Documentação Adicional

Este projeto possui documentação completa e profissional:

### 📖 Documentos Principais

- **[📘 README.md](README.md)** - Este documento (visão geral completa)
- **[📜 LICENSE](LICENSE)** - Licença MIT do projeto
- **[🤝 CONTRIBUTING.md](CONTRIBUTING.md)** - Como contribuir
- **[📋 CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)** - Código de conduta
- **[📝 CHANGELOG.md](CHANGELOG.md)** - Histórico de versões
- **[🔒 SECURITY.md](SECURITY.md)** - Política de segurança
- **[📞 CONTATOS.md](CONTATOS.md)** - Gerenciamento de contatos

### 🛠️ Documentação Técnica (docs/)

- **[🏗️ ARCHITECTURE.md](docs/ARCHITECTURE.md)** - Arquitetura técnica detalhada
- **[🚀 DEPLOYMENT.md](docs/DEPLOYMENT.md)** - Guia completo de deployment
- **[📸 SCREENSHOTS.md](docs/SCREENSHOTS.md)** - Guia de documentação visual
- **[📚 docs/README.md](docs/README.md)** - Índice da documentação

### 🎯 Recursos Úteis

- 🌐 [Site Demo](https://thigil15.github.io/Jornadadagraca/)
- 💻 [Repositório GitHub](https://github.com/Thigil15/Jornadadagraca)
- 🐛 [Issues](https://github.com/Thigil15/Jornadadagraca/issues)
- 🔀 [Pull Requests](https://github.com/Thigil15/Jornadadagraca/pulls)

---

## 🙏 Agradecimentos

- **Comunidade cristã** pela inspiração e propósito
- **Todos que compartilham sua fé** através desta plataforma
- **Colaboradores e contribuidores** que melhoram o projeto
- **Usuários e testadores** que reportam bugs e sugerem melhorias
- **Desenvolvedores de open source** cujas ferramentas usamos

### 💝 Agradecimentos Especiais

- **Tailwind CSS** - Framework CSS incrível
- **Google Fonts** - Tipografia Inter linda
- **GitHub** - Hospedagem e ferramentas
- **MDN Web Docs** - Documentação técnica essencial

---

<div align="center">

### 🌟 **Que esta jornada toque corações e transforme vidas!** 🙏✨

**Feito com ❤️ e fé | Open Source sob Licença MIT**

[⬆ Voltar ao Topo](#-jornada-da-graça---recomeço-com-cristo)

</div>
