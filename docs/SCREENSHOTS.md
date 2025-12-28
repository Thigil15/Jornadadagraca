# 📸 Guia Visual do Projeto

Este documento descreve as principais telas e funcionalidades visuais da aplicação Jornada da Graça.

## 🖼️ Screenshots Recomendados

Para documentação completa, recomendamos capturar screenshots das seguintes seções:

### 📱 Página Principal (index.html)

#### 1. Hero Section - Desktop
**Localização**: Seção `#inicio`
**Capture**:
- Título animado completo
- Botão "Iniciar Jornada"
- Seta animada de scroll
- Fundo com gradiente

**Dimensões sugeridas**: 1920x1080

#### 2. Hero Section - Mobile
**Localização**: Seção `#inicio`
**Capture**: Mesma seção em dispositivo móvel
**Dimensões sugeridas**: 375x667 (iPhone SE)

#### 3. Seção "Reconhece algum destes pesos?"
**Localização**: Seção `#dilema`
**Capture**:
- 3 cards interativos
- Efeito tilt 3D (se possível capturar)
- Estado normal e estado "faded" após click

#### 4. Versículo do Dia
**Localização**: Seção `#versiculo`
**Capture**:
- Card do versículo com fundo suave
- Texto, referência e mensagem

#### 5. Galeria de Benefícios
**Localização**: Seção `#beneficios`
**Capture**:
- Grid de 4 cards
- Um card expandido mostrando conteúdo
- Ícones animados

#### 6. Seção "O Caminho"
**Localização**: Seção `#caminho`
**Capture**:
- 3 círculos numerados
- Passos: Reconheça, Creia, Receba

#### 7. Testemunhos
**Localização**: Seção `#testemunhos`
**Capture**:
- Grid de testemunhos aprovados
- Sistema de estrelas (rating)
- Botão para inserir testemunho

#### 8. Formulário de Testemunho
**Localização**: Seção `#testemunhos` (formulário aberto)
**Capture**:
- Formulário completo
- Campos de nome, localização, texto
- Sistema de rating interativo

#### 9. Compartilhamento Social
**Localização**: Seção `#compartilhar`
**Capture**:
- Botões de redes sociais
- Icons coloridos
- Layout responsivo

#### 10. Formulário de Contato
**Localização**: Seção `#acompanhamento`
**Capture**:
- Fluxo de consentimento
- Formulário expandido
- Select de necessidades

#### 11. Oração com Typewriter
**Localização**: Seção `#convite`
**Capture**:
- Botão "Estou pronto"
- Texto da oração com efeito typewriter
- Estado antes e durante a animação

#### 12. Navegação Lateral (Desktop)
**Capture**:
- Menu de navegação lateral fixo
- Indicadores de seção ativa
- Estados hover

#### 13. Back to Top Button
**Capture**:
- Botão "Voltar ao topo"
- Aparência em scroll

### 🔐 Painel Administrativo

#### 14. Login Admin
**Localização**: `src/admin/login.html`
**Capture**:
- Formulário de login
- Campos de email e senha
- Botão de login

#### 15. Dashboard Admin
**Localização**: `src/admin/admin.html`
**Capture**: Overview completo do painel

#### 16. Gestão de Testemunhos
**Localização**: Tab "Testemunhos" no admin
**Capture**:
- Lista de testemunhos pendentes
- Botões: Aprovar, Reprovar, Excluir
- Estatísticas (Total, Aprovados, Pendentes)

#### 17. Gestão de Contatos
**Localização**: Tab "Contatos" no admin
**Capture**:
- Lista de solicitações de contato
- Detalhes completos
- Botão de exportar JSON

#### 18. Gestão de Versículos
**Localização**: Tab "Versículos" no admin
**Capture**:
- Lista de versículos cadastrados
- Formulário de adicionar/editar
- Botões de importar/exportar

### 📱 PWA e Mobile

#### 19. Instalação PWA - Android
**Capture**:
- Prompt de instalação no Chrome Android
- Ícone na tela inicial após instalação
- App aberto em modo standalone

#### 20. Instalação PWA - iOS
**Capture**:
- Menu "Adicionar à Tela de Início" no Safari
- Ícone na tela inicial
- App aberto

#### 21. Modo Offline
**Capture**:
- Aplicação funcionando sem conexão
- Service Worker ativo (DevTools)

### 🎨 Estados e Animações

#### 22. Animações de Scroll
**Capture** (GIF ou vídeo recomendado):
- Elementos com fade-in ao entrar na viewport
- Transições suaves

#### 23. Cards com Tilt 3D
**Capture** (GIF ou vídeo recomendado):
- Efeito de inclinação 3D nos cards de "pesos"
- Movimento do mouse

#### 24. Efeito Typewriter
**Capture** (GIF ou vídeo recomendado):
- Oração sendo "digitada" character por character
- Cursor piscando

## 📐 Especificações para Screenshots

### Ferramentas Recomendadas

- **Desktop**: 
  - Chrome DevTools (F12) → Device Toolbar
  - Firefox Screenshot Tool (Shift+F2 → screenshot)
  - Awesome Screenshot (extensão)

- **Mobile**:
  - Dispositivos reais
  - Emuladores (Android Studio, Xcode Simulator)

### Dimensões Padrão

| Dispositivo | Resolução | Uso |
|------------|-----------|-----|
| Desktop HD | 1920x1080 | Screenshots principais |
| Desktop FHD | 2560x1440 | Screenshots de alta qualidade |
| Laptop | 1440x900 | Screenshots alternativos |
| iPhone SE | 375x667 | Mobile portrait |
| iPhone 12 Pro | 390x844 | Mobile moderno |
| iPad Pro | 1024x1366 | Tablet portrait |
| Android Phone | 360x640 | Mobile padrão |

### Formato

- **Imagens estáticas**: PNG (melhor qualidade)
- **Animações**: GIF ou MP4
- **Compressão**: Use TinyPNG ou similar antes de commit

### Organização

Salve screenshots em:
```
docs/
└── images/
    ├── desktop/
    │   ├── 01-hero-section.png
    │   ├── 02-dilema-cards.png
    │   └── ...
    ├── mobile/
    │   ├── 01-hero-mobile.png
    │   ├── 02-dilema-mobile.png
    │   └── ...
    ├── admin/
    │   ├── 01-login.png
    │   ├── 02-dashboard.png
    │   └── ...
    ├── pwa/
    │   ├── 01-install-android.png
    │   ├── 02-install-ios.png
    │   └── ...
    └── animations/
        ├── tilt-3d.gif
        ├── typewriter.gif
        └── scroll-animations.gif
```

## 🎬 Vídeos Recomendados

Para demonstração completa da experiência:

### 1. Tour Completo do Site (2-3 minutos)
- Scroll completo do início ao fim
- Interações com todos os elementos
- Submissão de formulários
- Narração opcional explicando cada seção

### 2. Demo do Admin Panel (1-2 minutos)
- Login
- Navegação pelas tabs
- Aprovação de testemunho
- Adição de versículo
- Exportação de dados

### 3. Instalação PWA (30-60 segundos)
- Processo completo de instalação
- Android e iOS
- Demonstração offline

## 📝 Como Usar Screenshots na Documentação

Após capturar os screenshots, adicione ao README.md:

```markdown
## 🖼️ Screenshots

### Página Principal

<div align="center">
  <img src="docs/images/desktop/01-hero-section.png" alt="Hero Section" width="800">
  <p><em>Seção inicial com título animado</em></p>
</div>

### Mobile

<div align="center">
  <img src="docs/images/mobile/01-hero-mobile.png" alt="Mobile Hero" width="375">
  <p><em>Experiência mobile-first</em></p>
</div>

### Admin Panel

<div align="center">
  <img src="docs/images/admin/02-dashboard.png" alt="Dashboard Admin" width="800">
  <p><em>Painel administrativo</em></p>
</div>
```

## 🎨 Dicas para Screenshots de Qualidade

1. **Limpe o ambiente**:
   - Feche abas desnecessárias
   - Use modo de navegação anônima
   - Desative extensões que aparecem na UI

2. **Dados de exemplo**:
   - Use dados realistas mas não sensíveis
   - Preencha formulários com exemplos apropriados
   - Testemunhos devem ser fictícios mas autênticos

3. **Consistência**:
   - Mesmo navegador para todas as capturas
   - Mesmo zoom level (100%)
   - Mesma resolução quando possível

4. **Clareza**:
   - Certifique-se de que textos são legíveis
   - Evite imagens muito comprimidas
   - Capture em alta resolução, depois redimensione

5. **Contexto**:
   - Inclua suficiente contexto ao redor do elemento
   - Mostre navegação quando relevante
   - Capture estados importantes (hover, ativo, etc.)

## ✅ Checklist de Screenshots

Use esta checklist para garantir cobertura completa:

**Página Principal:**
- [ ] Hero section (desktop)
- [ ] Hero section (mobile)
- [ ] Cards de "pesos"
- [ ] Versículo do dia
- [ ] Galeria de benefícios
- [ ] Seção "O Caminho"
- [ ] Testemunhos
- [ ] Formulário de testemunho
- [ ] Compartilhamento social
- [ ] Formulário de contato
- [ ] Oração com typewriter
- [ ] Navegação lateral
- [ ] Back to top button

**Admin:**
- [ ] Login
- [ ] Dashboard
- [ ] Gestão de testemunhos
- [ ] Gestão de contatos
- [ ] Gestão de versículos

**PWA:**
- [ ] Instalação Android
- [ ] Instalação iOS
- [ ] Modo offline

**Animações:**
- [ ] Tilt 3D cards
- [ ] Typewriter effect
- [ ] Scroll animations

---

**Nota**: Screenshots não são obrigatórios mas melhoram significativamente a documentação! 📸✨
