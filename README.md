# 🙏 Jornada da Graça - Recomeço com Cristo

[![GitHub](https://img.shields.io/github/license/Thigil15/Jornadadagraca)](LICENSE)
[![GitHub last commit](https://img.shields.io/github/last-commit/Thigil15/Jornadadagraca)](https://github.com/Thigil15/Jornadadagraca/commits)

Uma Single Page Application (SPA) interativa que apresenta a mensagem cristã sobre graça, perdão e recomeço de forma moderna e envolvente, otimizada para dispositivos móveis.

## 📖 Sobre o Projeto

O projeto "Jornada da Graça" nasceu da necessidade de transformar um panfleto evangelístico tradicional em uma experiência digital imersiva. O objetivo é capturar a atenção do usuário (geralmente através de um QR Code) e guiá-lo por uma jornada de reflexão pessoal sobre fé e transformação.

A aplicação foi construída como uma narrativa visual, onde cada seção se baseia na anterior, utilizando técnicas de UI/UX e animações para manter o usuário engajado e focado na mensagem.

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

## 🚀 Tecnologias Utilizadas

- **HTML5**: Estrutura semântica do conteúdo
- **CSS3**: 
  - Tailwind CSS para estilização rápida e responsividade
  - CSS customizado para animações (@keyframes) e efeitos visuais avançados
- **JavaScript (ES6+)**:
  - Vanilla JS puro para máxima performance
  - Intersection Observer API para animações no scroll
  - LocalStorage para persistência de dados
  - SessionStorage para autenticação
- **PWA (Progressive Web App)**:
  - Service Worker para cache offline
  - Manifest.json para instalação no dispositivo

## 📁 Estrutura do Projeto

```
Jornadadagraca/
├── index.html              # Página principal da aplicação
├── admin.html              # Página de redirecionamento para admin
├── manifest.json           # Configuração PWA
├── service-worker.js       # Service worker para PWA
├── .gitignore             # Arquivos ignorados pelo Git
├── README.md              # Este arquivo
├── CONTATOS.md            # Informações de contato
│
├── data/                  # Dados da aplicação
│   ├── admin-credentials.json    # Credenciais de administrador
│   ├── comentarios.json          # Testemunhos aprovados
│   └── versiculos.json           # Base de versículos bíblicos
│
├── src/                   # Código fonte
│   └── admin/            # Painel administrativo
│       ├── login.html    # Página de login
│       └── admin.html    # Painel de administração
│
└── docs/                  # Documentação adicional (opcional)
```

## 🔧 Como Utilizar

### Instalação Local

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/Thigil15/Jornadadagraca.git
   cd Jornadadagraca
   ```

2. **Abra o arquivo principal**:
   - Abra `index.html` em qualquer navegador moderno
   - Não há necessidade de build ou instalação de dependências

### Acesso Online

Acesse diretamente através do GitHub Pages:
```
https://thigil15.github.io/Jornadadagraca/
```

## 🔐 Painel de Administração

### Acesso ao Admin

1. Acesse `admin.html` ou navegue para `src/admin/login.html`
2. Use as credenciais de administrador configuradas em `data/admin-credentials.json`
3. Por padrão:
   - **Email**: thiago.dias@hc.fm.usp.br
   - **Senha**: Jesus1508@

### Funcionalidades do Admin

#### Gerenciamento de Testemunhos
- Visualize todos os testemunhos enviados
- Aprove ou reprove comentários para exibição pública
- Exclua comentários inadequados
- Exporte todos os testemunhos em JSON

#### Gerenciamento de Contatos
- Visualize solicitações de contato
- Veja detalhes (nome, email, telefone, necessidade)
- Exporte contatos em JSON para CRM

#### Gerenciamento de Versículos
- Adicione novos versículos bíblicos
- Edite versículos existentes
- Exclua versículos
- Importe/exporte listas de versículos em JSON

### Segurança

- ⚠️ **IMPORTANTE**: As credenciais estão armazenadas em JSON simples. Para produção, considere:
  - Mover credenciais para backend seguro
  - Implementar hash de senhas (bcrypt)
  - Adicionar HTTPS obrigatório
  - Implementar rate limiting
  - Adicionar autenticação de dois fatores

## 🎨 Paleta de Cores

- **Principal**: `#B38B6D` (Serene Dawn)
- **Secundária**: `#a17c60`
- **Background**: Gradiente entre `#FDFBF8`, `#F8F6F2`, `#EAE3D9`
- **Texto**: `#4A4A4A` e `#3A3A3A`

## 📱 Progressive Web App (PWA)

A aplicação pode ser instalada como um app nativo:

1. Abra o site no navegador móvel
2. Toque em "Adicionar à tela inicial"
3. O app ficará disponível como um ícone no seu dispositivo

Funciona offline após a primeira visita!

## 🌐 Deployment

### GitHub Pages

1. Faça push das alterações para o branch `main`
2. Vá em Settings → Pages
3. Selecione o branch `main` como source
4. O site estará disponível em `https://[seu-usuario].github.io/Jornadadagraca/`

### Netlify

1. Conecte seu repositório GitHub ao Netlify
2. Configure:
   - Build command: (deixe vazio)
   - Publish directory: `/`
3. Deploy automático a cada push

## 🤝 Contribuindo

Contribuições são bem-vindas! Para contribuir:

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/NovaFuncionalidade`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova funcionalidade'`)
4. Push para a branch (`git push origin feature/NovaFuncionalidade`)
5. Abra um Pull Request

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

## 👥 Autor

- **Thiago Dias** - [GitHub](https://github.com/Thigil15)

## 🙏 Agradecimentos

- Comunidade cristã pela inspiração
- Todos que compartilham sua fé através desta plataforma
- Colaboradores e contribuidores do projeto

---

**Que esta jornada toque corações e transforme vidas! 🙏✨**
