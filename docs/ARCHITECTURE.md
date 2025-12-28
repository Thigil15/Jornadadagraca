# 🏗️ Arquitetura do Projeto

Este documento descreve a arquitetura técnica da aplicação Jornada da Graça.

## 📋 Visão Geral

Jornada da Graça é uma **Single Page Application (SPA)** progressiva construída com tecnologias web nativas, sem frameworks JavaScript. A aplicação foi projetada para ser leve, rápida e funcionar offline.

### Princípios Arquiteturais

- **Progressive Enhancement**: Funcionalidade básica sem JavaScript, melhorias progressivas com JS
- **Mobile-First**: Design responsivo otimizado para dispositivos móveis
- **Performance**: Carregamento rápido e experiência fluida
- **Offline-First**: PWA com capacidade de funcionar offline
- **Acessibilidade**: WCAG 2.1 AA compliance
- **Simplicidade**: Sem dependências externas de build ou runtime

## 🗂️ Estrutura de Diretórios

```
Jornadadagraca/
├── index.html              # Página principal da aplicação
├── admin.html              # Redirecionador para painel admin
├── manifest.json           # Manifest PWA
├── service-worker.js       # Service Worker para cache offline
├── LICENSE                 # Licença MIT
├── README.md              # Documentação principal
├── CONTRIBUTING.md        # Guia de contribuição
├── CODE_OF_CONDUCT.md     # Código de conduta
├── CONTATOS.md            # Informações sobre contatos
├── .gitignore            # Arquivos ignorados pelo Git
│
├── data/                  # Dados da aplicação
│   ├── admin-credentials.json    # Credenciais admin (JSON simples)
│   ├── comentarios.json          # Base de testemunhos
│   └── versiculos.json           # Base de versículos bíblicos
│
├── src/                   # Código fonte
│   └── admin/            # Painel administrativo
│       ├── login.html    # Página de login
│       └── admin.html    # Dashboard administrativo
│
└── docs/                  # Documentação técnica
    ├── DEPLOYMENT.md     # Guia de deployment
    └── ARCHITECTURE.md   # Este arquivo
```

## 🎨 Stack Tecnológico

### Frontend

| Tecnologia | Versão | Propósito |
|-----------|--------|-----------|
| HTML5 | - | Estrutura semântica |
| CSS3 | - | Estilização e animações |
| Tailwind CSS | 3.x (CDN) | Framework CSS utility-first |
| JavaScript | ES6+ | Lógica e interatividade |
| Vanilla JS | - | Sem frameworks, máxima performance |

### APIs Web Utilizadas

- **Intersection Observer API**: Animações ao scroll
- **LocalStorage API**: Persistência de dados local
- **SessionStorage API**: Gerenciamento de sessão
- **Service Worker API**: Funcionalidade offline (PWA)
- **Fetch API**: Carregamento de dados JSON
- **Clipboard API**: Compartilhamento de conteúdo

### Fontes e Ícones

- **Google Fonts**: Inter (300, 400, 500, 600, 700)
- **Emojis**: Ícones nativos Unicode

## 🔄 Fluxo de Dados

### 1. Dados Estáticos

```
JSON Files (data/) → Fetch API → LocalStorage → DOM Rendering
```

**Arquivos de Dados:**
- `versiculos.json`: Base de versículos bíblicos
- `comentarios.json`: Testemunhos aprovados iniciais
- `admin-credentials.json`: Credenciais de acesso admin

### 2. Dados do Usuário

```
User Input → Form Validation → LocalStorage → Admin Review → Public Display
```

**Fluxos:**

**Testemunhos:**
```
User fills form → Save to localStorage (jornada-comments)
→ Admin reviews → Approve/Reject → Display on frontend
```

**Contatos:**
```
User fills form → Save to localStorage (jornada-contacts)
→ Optional GitHub Issue → Admin review
```

## 🎭 Componentes Principais

### 1. Página Principal (index.html)

**Seções:**

1. **Hero Section** (`#inicio`)
   - Título animado palavra por palavra
   - Animação de entrada fade-in
   - Botão CTA para iniciar jornada

2. **Dilema Section** (`#dilema`)
   - Cards interativos com efeito tilt 3D
   - Click to fade (simboliza descarte de pesos)
   - Intersection Observer para animações

3. **Versículo do Dia** (`#versiculo`)
   - Rotação diária baseada em day-of-year
   - Carregamento de `versiculos.json`
   - Fallback para versículo padrão

4. **Grace Section** (`#graca`)
   - Explicação conceitual da graça
   - Citações bíblicas
   - Background fixed com efeito parallax

5. **Benefits Gallery** (`#beneficios`)
   - Cards expansíveis (acordeão)
   - Transições CSS suaves
   - Icons animados

6. **Caminho** (`#caminho`)
   - Três passos numerados
   - Fade-in progressivo com delays
   - Design responsivo em grid

7. **Testemunhos** (`#testemunhos`)
   - Exibição de comentários aprovados
   - Sistema de rating (estrelas)
   - Formulário de submissão
   - Validação client-side

8. **Recursos** (`#recursos`)
   - Links externos
   - Cards com hover effects
   - Abertura em nova aba

9. **Compartilhamento** (`#compartilhar`)
   - Botões para redes sociais
   - WhatsApp, Facebook, Twitter, Telegram, Instagram, Email
   - Mensagens pré-formatadas

10. **Contato** (`#acompanhamento`)
    - Fluxo de consentimento
    - Formulário condicional
    - Campos dinâmicos

11. **Oração** (`#convite`)
    - Typewriter effect
    - Seleção aleatória de orações
    - Animação character-by-character

### 2. Admin Panel (src/admin/)

**login.html:**
- Autenticação via JSON
- Session storage para token
- Redirecionamento automático

**admin.html:**
- Dashboard com estatísticas
- Gestão de testemunhos (aprovar/reprovar/excluir)
- Gestão de contatos (visualizar/exportar)
- Gestão de versículos (CRUD completo)
- Exportação de dados em JSON
- Logout com limpeza de sessão

## 🔐 Segurança

### Atual (Client-Side)

⚠️ **Limitações de Segurança:**
- Credenciais em JSON plain text
- Autenticação client-side apenas
- Sem criptografia de dados
- Dados em LocalStorage (não criptografado)

**Adequado para:**
- Projetos pessoais
- Protótipos
- Ambientes de desenvolvimento
- Sites informativos

### Recomendações para Produção

Para uso em produção com dados sensíveis:

1. **Backend Seguro**
   ```
   - API REST com autenticação JWT
   - Hash de senhas (bcrypt)
   - Rate limiting
   - CORS configurado
   ```

2. **Banco de Dados**
   ```
   - PostgreSQL ou MongoDB
   - Conexão criptografada
   - Backups automáticos
   ```

3. **HTTPS Obrigatório**
   ```
   - Certificado SSL/TLS
   - HSTS headers
   - Secure cookies
   ```

4. **Melhorias de Autenticação**
   ```
   - OAuth 2.0
   - 2FA (Two-Factor Authentication)
   - Session timeout
   - Token refresh
   ```

## 🚀 Performance

### Otimizações Implementadas

1. **CSS**
   - Tailwind CSS via CDN (cacheable)
   - CSS crítico inline
   - Animações via GPU (transform, opacity)
   - Remoção de animações em `prefers-reduced-motion`

2. **JavaScript**
   - Vanilla JS (sem overhead de frameworks)
   - Event delegation onde possível
   - Lazy loading de conteúdo
   - Debouncing em scroll events

3. **Imagens**
   - SVG emojis (leves)
   - Inline SVG data URIs
   - Sem imagens externas pesadas

4. **Carregamento**
   - HTML estrutural primeiro
   - CSS inline para critical path
   - JS não-blocking
   - Preconnect para Google Fonts

### Service Worker (PWA)

```javascript
// Cache Strategy: Cache First
self.addEventListener('fetch', (event) => {
  event.respondWith(
    caches.match(event.request).then((response) => {
      return response || fetch(event.request);
    })
  );
});
```

**Recursos Cacheados:**
- HTML pages
- CSS/JS files
- Fonts
- Manifest

## ♿ Acessibilidade

### Implementações WCAG 2.1

1. **Estrutura Semântica**
   ```html
   - <header>, <nav>, <main>, <section>, <footer>
   - Headings hierárquicos (h1 → h6)
   - <article> para testemunhos
   ```

2. **ARIA Labels**
   ```html
   - aria-label em buttons e links
   - role="navigation"
   - aria-pressed para estados
   ```

3. **Navegação por Teclado**
   - Todos os elementos interativos são focáveis
   - Skip links para conteúdo principal
   - Ordem de tabulação lógica

4. **Contraste**
   - Ratio mínimo 4.5:1 para texto normal
   - Ratio mínimo 3:1 para texto grande

5. **Screen Readers**
   - Alt text em imagens
   - Labels em form fields
   - Status messages para ações

## 📱 Responsividade

### Breakpoints (Tailwind)

```css
/* Mobile First */
Base: < 640px     /* Mobile */
sm: 640px+        /* Tablet */
md: 768px+        /* Tablet landscape */
lg: 1024px+       /* Desktop */
xl: 1280px+       /* Large desktop */
```

### Design Adaptativo

- **Mobile**: Stack vertical, menu simplificado
- **Tablet**: Grid 2 colunas, navegação lateral
- **Desktop**: Grid 3 colunas, efeitos hover, tilt 3D

## 🎨 Sistema de Design

### Paleta de Cores

```css
/* Primary */
--brand: #B38B6D (Serene Dawn)
--brand-dark: #a17c60

/* Background */
--bg-primary: #FDFBF8
--bg-secondary: #F8F6F2
--bg-accent: #EAE3D9

/* Text */
--text-heading: #3A3A3A
--text-body: #4A4A4A
--text-muted: #6B7280
```

### Tipografia

```css
/* Font Family */
font-family: 'Inter', sans-serif;

/* Scales */
text-xs: 0.75rem
text-sm: 0.875rem
text-base: 1rem
text-lg: 1.125rem
text-xl: 1.25rem
text-2xl: 1.5rem
text-3xl: 1.875rem
text-4xl: 2.25rem
```

### Espaçamento

```css
/* Consistent spacing scale */
p-2: 0.5rem
p-4: 1rem
p-6: 1.5rem
p-8: 2rem
p-12: 3rem
```

## 🔄 State Management

### LocalStorage Schema

```javascript
// Testemunhos
{
  key: 'jornada-comments',
  value: [
    {
      name: string,
      location: string,
      text: string,
      rating: number (1-5),
      approved: boolean,
      dataHora: ISO8601 string
    }
  ]
}

// Contatos
{
  key: 'jornada-contacts',
  value: [
    {
      nome: string,
      email: string,
      telefone: string,
      necessidade: string,
      outrosTexto: string,
      dataHora: ISO8601 string
    }
  ]
}

// Versículos (cache local)
{
  key: 'jornada-verses-local',
  value: [
    {
      text: string,
      reference: string,
      message: string
    }
  ]
}
```

### SessionStorage (Admin)

```javascript
{
  key: 'admin-session',
  value: {
    authenticated: boolean,
    email: string,
    expiry: timestamp
  }
}
```

## 🧪 Testing Strategy

### Manual Testing Checklist

- [ ] Funcionalidade em Chrome, Firefox, Safari, Edge
- [ ] Responsividade em mobile/tablet/desktop
- [ ] PWA instalável
- [ ] Funcionalidade offline
- [ ] Formulários validam corretamente
- [ ] Animações suaves
- [ ] Performance Lighthouse > 90
- [ ] Acessibilidade Lighthouse > 90

### Recomendações para Testes Automatizados

```javascript
// Playwright/Cypress
- E2E tests para fluxos principais
- Form submissions
- Admin authentication
- Data persistence
```

## 📊 Analytics e Monitoramento

### Métricas Recomendadas

1. **User Engagement**
   - Tempo na página
   - Scroll depth
   - Seções visualizadas
   - Taxa de bounce

2. **Conversões**
   - Testemunhos submetidos
   - Contatos enviados
   - Cliques em recursos externos
   - Compartilhamentos sociais

3. **Performance**
   - Page load time
   - Time to interactive
   - Largest Contentful Paint
   - Cumulative Layout Shift

## 🔮 Evolução Futura

### Possíveis Melhorias

1. **Backend**
   - API REST em Node.js/Python/Go
   - Banco de dados real
   - Autenticação JWT

2. **Features**
   - Sistema de busca de versículos
   - Comentários com resposta
   - Notificações push (PWA)
   - Modo escuro

3. **Internacionalização**
   - Suporte multi-idioma
   - Detecção automática de idioma
   - Traduções profissionais

4. **Analytics**
   - Dashboard de métricas
   - Heatmaps
   - A/B testing

## 📞 Suporte Técnico

Para dúvidas sobre a arquitetura:

1. Consulte a [documentação](../README.md)
2. Veja [exemplos de código](../src/)
3. Abra uma [issue](https://github.com/Thigil15/Jornadadagraca/issues)

---

**Arquitetura simples, mas poderosa para alcançar corações! 🙏✨**
