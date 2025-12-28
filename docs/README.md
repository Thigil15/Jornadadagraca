# 📚 Documentação do Projeto

Bem-vindo à documentação completa da **Jornada da Graça**!

## 📖 Índice de Documentação

### 🏠 Documentação Principal

- **[README.md](../README.md)** - Visão geral do projeto, quick start, e guia de uso
- **[LICENSE](../LICENSE)** - Licença MIT do projeto
- **[CONTRIBUTING.md](../CONTRIBUTING.md)** - Como contribuir para o projeto
- **[CODE_OF_CONDUCT.md](../CODE_OF_CONDUCT.md)** - Código de conduta da comunidade
- **[CONTATOS.md](../CONTATOS.md)** - Como acessar e gerenciar contatos

### 🛠️ Documentação Técnica

- **[ARCHITECTURE.md](ARCHITECTURE.md)** - Arquitetura técnica detalhada
  - Stack tecnológico
  - Estrutura de diretórios
  - Fluxo de dados
  - Componentes principais
  - Segurança
  - Performance
  - Acessibilidade
  - State management

- **[DEPLOYMENT.md](DEPLOYMENT.md)** - Guia completo de deployment
  - GitHub Pages
  - Netlify
  - Vercel
  - Cloudflare Pages
  - Docker
  - Servidor tradicional
  - Configuração HTTPS
  - CI/CD

- **[SCREENSHOTS.md](SCREENSHOTS.md)** - Guia para documentação visual
  - Lista de screenshots recomendados
  - Especificações técnicas
  - Ferramentas e dimensões
  - Organização de arquivos
  - Dicas de qualidade

## 🎯 Guias Rápidos

### Para Desenvolvedores

1. **Iniciando**
   ```bash
   git clone https://github.com/Thigil15/Jornadadagraca.git
   cd Jornadadagraca
   # Abra index.html no navegador
   ```

2. **Estrutura Básica**
   - `index.html` - Página principal
   - `src/admin/` - Painel administrativo
   - `data/` - Dados em JSON
   - `docs/` - Esta documentação

3. **Desenvolvimento Local**
   - Não requer build ou instalação
   - Apenas abra index.html em um navegador
   - Use Live Server para hot reload

4. **Contribuindo**
   - Leia [CONTRIBUTING.md](../CONTRIBUTING.md)
   - Siga o [CODE_OF_CONDUCT.md](../CODE_OF_CONDUCT.md)
   - Abra issues e pull requests

### Para Administradores

1. **Acesso Admin**
   - URL: `/src/admin/login.html`
   - Credenciais em `data/admin-credentials.json`
   - Altere as credenciais padrão!

2. **Gerenciamento**
   - Testemunhos: Aprovar/reprovar comentários
   - Contatos: Visualizar solicitações
   - Versículos: CRUD completo

3. **Backup**
   - Exporte dados regularmente
   - Use os botões "Exportar JSON"
   - Salve arquivos em local seguro

### Para Designers

1. **Design System**
   - Paleta: Tons de bege (#B38B6D como principal)
   - Fonte: Inter (300-700)
   - Mobile-first approach
   - Veja detalhes em [ARCHITECTURE.md](ARCHITECTURE.md)

2. **Componentes**
   - Cards interativos
   - Formulários
   - Animações CSS
   - Estados hover/active

### Para Contribuidores de Conteúdo

1. **Adicionar Versículos**
   - Acesse painel admin
   - Adicione novo versículo
   - Inclua: texto, referência, mensagem

2. **Revisar Testemunhos**
   - Verifique testemunhos pendentes
   - Aprove os apropriados
   - Mantenha qualidade do conteúdo

## 🔍 Referência Rápida

### Tecnologias Utilizadas

- HTML5 + CSS3 + JavaScript ES6+
- Tailwind CSS (via CDN)
- PWA (Service Worker + Manifest)
- LocalStorage para persistência
- Vanilla JS (sem frameworks)

### Navegadores Suportados

- ✅ Chrome/Edge (últimas 2 versões)
- ✅ Firefox (últimas 2 versões)
- ✅ Safari (últimas 2 versões)
- ✅ Mobile browsers (iOS Safari, Chrome Android)

### Requisitos do Sistema

- ❌ Não requer Node.js
- ❌ Não requer npm/yarn
- ❌ Não requer build tools
- ✅ Apenas um navegador moderno
- ✅ Servidor web estático (para deploy)

## 📞 Suporte

### Onde Obter Ajuda

1. **Documentação**
   - Leia os arquivos desta pasta
   - Consulte README.md principal
   - Veja exemplos de código

2. **Issues do GitHub**
   - [Reportar Bug](https://github.com/Thigil15/Jornadadagraca/issues/new?labels=bug)
   - [Solicitar Feature](https://github.com/Thigil15/Jornadadagraca/issues/new?labels=enhancement)
   - [Fazer Pergunta](https://github.com/Thigil15/Jornadadagraca/issues/new?labels=question)

3. **Contato Direto**
   - Email: thiago.dias@hc.fm.usp.br
   - GitHub: [@Thigil15](https://github.com/Thigil15)

## 🎓 Recursos de Aprendizado

### Para Aprender Mais

**JavaScript:**
- [MDN Web Docs](https://developer.mozilla.org/pt-BR/)
- [JavaScript.info](https://javascript.info/)

**PWA:**
- [Google PWA Guide](https://web.dev/progressive-web-apps/)
- [PWA Builder](https://www.pwabuilder.com/)

**Web APIs:**
- [Intersection Observer API](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API)
- [Service Worker API](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API)

**Acessibilidade:**
- [WCAG 2.1 Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- [A11Y Project](https://www.a11yproject.com/)

## 🗺️ Roadmap

### Melhorias Planejadas

- [ ] Backend com API REST
- [ ] Banco de dados real
- [ ] Autenticação JWT
- [ ] Sistema de notificações
- [ ] Modo escuro
- [ ] Internacionalização (i18n)
- [ ] Analytics dashboard
- [ ] A/B testing
- [ ] Sistema de busca
- [ ] PWA push notifications

### Como Contribuir para o Roadmap

1. Abra uma issue com label `enhancement`
2. Descreva a feature proposta
3. Participe da discussão
4. Implemente e abra um PR

## 📊 Status do Projeto

- ✅ **Funcional**: Sim, totalmente operacional
- ✅ **Mantido**: Sim, ativamente mantido
- ✅ **Documentado**: Sim, documentação completa
- ✅ **Open Source**: Sim, licença MIT
- ✅ **Produção**: Sim, pronto para uso real

## 🙏 Agradecimentos

Agradecemos a todos que contribuem para tornar este projeto melhor:

- Colaboradores de código
- Revisores de conteúdo
- Testadores
- Documentadores
- Usuários que reportam issues

## 📝 Atualizações da Documentação

Esta documentação é mantida atualizada com o projeto. Se encontrar algo desatualizado:

1. Abra uma issue
2. Ou faça um PR corrigindo
3. Label: `documentation`

## 🔗 Links Úteis

- [Site Demo](https://thigil15.github.io/Jornadadagraca/)
- [Repositório GitHub](https://github.com/Thigil15/Jornadadagraca)
- [Issues](https://github.com/Thigil15/Jornadadagraca/issues)
- [Pull Requests](https://github.com/Thigil15/Jornadadagraca/pulls)

---

**Que esta documentação ajude você a contribuir e fazer a diferença! 🙏✨**

*Última atualização: 2025-01*
