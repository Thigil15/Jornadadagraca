# 🤝 Contribuindo para Jornada da Graça

Obrigado por considerar contribuir para o projeto Jornada da Graça! Este documento fornece diretrizes para contribuir com o projeto.

## 📋 Índice

- [Código de Conduta](#código-de-conduta)
- [Como Posso Contribuir?](#como-posso-contribuir)
- [Processo de Desenvolvimento](#processo-de-desenvolvimento)
- [Guia de Estilo](#guia-de-estilo)
- [Reportando Bugs](#reportando-bugs)
- [Sugerindo Melhorias](#sugerindo-melhorias)

## 📜 Código de Conduta

Este projeto segue nosso [Código de Conduta](CODE_OF_CONDUCT.md). Ao participar, espera-se que você mantenha este código. Por favor, reporte comportamentos inaceitáveis.

## 🎯 Como Posso Contribuir?

### 1. Reportar Bugs

Se você encontrar um bug, por favor:

1. Verifique se o bug já foi reportado nas [Issues](https://github.com/Thigil15/Jornadadagraca/issues)
2. Se não encontrar, crie uma nova issue incluindo:
   - Título claro e descritivo
   - Descrição detalhada do problema
   - Passos para reproduzir o comportamento
   - Comportamento esperado vs. comportamento atual
   - Screenshots (se aplicável)
   - Navegador e versão

### 2. Sugerir Melhorias

Sugestões são bem-vindas! Para sugerir uma melhoria:

1. Verifique se a sugestão já existe nas Issues
2. Crie uma nova issue com a tag `enhancement`
3. Descreva detalhadamente:
   - O problema que a melhoria resolve
   - Como você imagina que funcionaria
   - Por que isso seria útil para o projeto

### 3. Contribuir com Código

#### Tipos de Contribuições Aceitas

- 🐛 Correção de bugs
- ✨ Novas funcionalidades (discuta antes via issue)
- 📝 Melhorias na documentação
- 🎨 Melhorias de UI/UX
- ♿ Melhorias de acessibilidade
- 🌐 Traduções e internacionalização
- 🔒 Melhorias de segurança
- ⚡ Otimizações de performance
- 📖 Novos versículos bíblicos

## 🔄 Processo de Desenvolvimento

### 1. Fork e Clone

```bash
# Fork o repositório através do GitHub
# Clone seu fork
git clone https://github.com/SEU-USUARIO/Jornadadagraca.git
cd Jornadadagraca
```

### 2. Crie uma Branch

```bash
# Crie uma branch descritiva
git checkout -b feature/nova-funcionalidade
# ou
git checkout -b fix/correcao-bug
```

### 3. Faça suas Mudanças

- Mantenha as mudanças focadas e específicas
- Siga o guia de estilo do projeto
- Teste suas mudanças em diferentes navegadores
- Teste em dispositivos móveis

### 4. Commit

```bash
# Adicione suas mudanças
git add .

# Faça commit com mensagem descritiva
git commit -m "feat: adiciona nova funcionalidade X"
# ou
git commit -m "fix: corrige problema Y"
```

#### Convenção de Mensagens de Commit

Usamos commits semânticos:

- `feat:` - Nova funcionalidade
- `fix:` - Correção de bug
- `docs:` - Mudanças na documentação
- `style:` - Formatação, ponto e vírgula faltando, etc
- `refactor:` - Refatoração de código
- `test:` - Adição de testes
- `chore:` - Tarefas de manutenção

### 5. Push e Pull Request

```bash
# Push para seu fork
git push origin feature/nova-funcionalidade
```

Abra um Pull Request:
1. Vá para o repositório original no GitHub
2. Clique em "Pull Request"
3. Selecione sua branch
4. Preencha o template de PR:
   - Título claro
   - Descrição detalhada das mudanças
   - Screenshots (se aplicável)
   - Issues relacionadas (#numero)

## 📏 Guia de Estilo

### HTML

- Use HTML5 semântico
- Mantenha indentação consistente (4 espaços)
- Adicione `alt` em todas as imagens
- Use atributos `aria-label` para acessibilidade

### CSS

- Use classes do Tailwind CSS quando possível
- CSS customizado apenas quando necessário
- Mantenha nomes de classes descritivos
- Adicione comentários para seções complexas

### JavaScript

- Use ES6+ (const/let, arrow functions, etc.)
- Mantenha funções pequenas e focadas
- Adicione comentários para lógica complexa
- Use nomes de variáveis descritivos em português
- Sempre adicione tratamento de erros

### Acessibilidade

- Teste com leitores de tela
- Mantenha contraste adequado (WCAG AA)
- Suporte navegação por teclado
- Use ARIA labels apropriadamente

### Performance

- Otimize imagens antes de adicionar
- Minimize JavaScript customizado
- Use lazy loading quando apropriado
- Teste em dispositivos de baixo desempenho

## 🐛 Reportando Bugs

### Antes de Reportar

- Atualize para a versão mais recente
- Verifique se o bug já foi reportado
- Teste em diferentes navegadores

### Template de Bug Report

```markdown
**Descrição do Bug**
Uma descrição clara e concisa do bug.

**Passos para Reproduzir**
1. Vá para '...'
2. Clique em '....'
3. Role até '....'
4. Veja o erro

**Comportamento Esperado**
O que deveria acontecer.

**Comportamento Atual**
O que está acontecendo.

**Screenshots**
Se aplicável, adicione screenshots.

**Ambiente:**
 - Dispositivo: [ex: iPhone 12, Desktop]
 - OS: [ex: iOS 14, Windows 10]
 - Navegador: [ex: Chrome 95, Safari 14]
 - Versão: [ex: 1.0]

**Contexto Adicional**
Qualquer outra informação sobre o problema.
```

## 💡 Sugerindo Melhorias

### Template de Feature Request

```markdown
**Sua sugestão está relacionada a um problema?**
Uma descrição clara do problema. Ex: Fico frustrado quando [...]

**Descreva a solução que você gostaria**
Uma descrição clara do que você quer que aconteça.

**Descreva alternativas que você considerou**
Uma descrição de soluções ou funcionalidades alternativas.

**Contexto adicional**
Adicione qualquer outro contexto ou screenshots sobre a feature.
```

## 🔍 Revisão de Código

Quando revisar Pull Requests:

- Seja respeitoso e construtivo
- Foque no código, não na pessoa
- Explique o "porquê" das suas sugestões
- Aprove mudanças que melhoram o projeto
- Sugira melhorias quando apropriado

## 📚 Áreas que Precisam de Ajuda

- 📖 Expandir base de versículos bíblicos
- 🌐 Traduções para outros idiomas
- ♿ Melhorias de acessibilidade
- 📱 Testes em diferentes dispositivos
- 🔒 Melhorias de segurança
- 📝 Documentação
- 🎨 Melhorias de design

## 🙏 Agradecimentos

Agradecemos muito sua contribuição! Cada melhoria ajuda a levar a mensagem de esperança e graça para mais pessoas.

## 📞 Dúvidas?

Se tiver dúvidas sobre como contribuir:

1. Verifique a [documentação](README.md)
2. Abra uma issue com a tag `question`
3. Entre em contato através dos canais disponíveis

---

**Que sua contribuição abençoe muitas vidas! 🙏✨**
