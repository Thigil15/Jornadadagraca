# 🔒 Política de Segurança

## 🎯 Versões Suportadas

| Versão | Suportada          |
| ------ | ------------------ |
| 1.0.x  | :white_check_mark: |
| < 1.0  | :x:                |

## 🐛 Reportando uma Vulnerabilidade

A segurança do projeto Jornada da Graça é levada a sério. Agradecemos seus esforços para divulgar responsavelmente suas descobertas.

### 📧 Como Reportar

Se você descobrir uma vulnerabilidade de segurança, por favor **NÃO** abra uma issue pública. Em vez disso:

1. **Entre em contato via GitHub** - Use a aba "Security" do repositório para reportar vulnerabilidades privadamente
2. **Ou abra uma issue privada** com label "security" (se disponível)
3. **Inclua os seguintes detalhes**:
   - Tipo de vulnerabilidade
   - Localização do código vulnerável (arquivo e linha, se possível)
   - Passos para reproduzir
   - Impacto potencial
   - Qualquer solução ou mitigação que você sugira

3. **Aguarde nossa resposta** dentro de 48 horas
4. **Trabalhe conosco** para verificar e corrigir o problema

### 🏆 Reconhecimento

Contribuidores que reportam vulnerabilidades de segurança responsavelmente serão reconhecidos (se desejarem) em:
- SECURITY.md (este arquivo)
- Release notes da versão com a correção
- README.md na seção de agradecimentos

## 🛡️ Medidas de Segurança Implementadas

### ✅ Proteções Atuais

1. **Client-Side**
   - Validação de formulários
   - Sanitização de inputs
   - Proteção contra XSS básica
   - HTTPS obrigatório para PWA

2. **Admin Panel**
   - Autenticação via SessionStorage
   - Sessão expira em 24 horas
   - Logout manual disponível
   - Auto-logout ao fechar navegador

3. **Dados**
   - LocalStorage para dados não-sensíveis
   - Sem armazenamento de senhas de usuários
   - Consentimento explícito antes de coletar dados

### ⚠️ Limitações Conhecidas

**IMPORTANTE**: Esta é uma aplicação client-side com limitações de segurança:

1. **Credenciais Admin**
   - ⚠️ Armazenadas em arquivo JSON local (não versionado)
   - ❌ Sem hash de senhas (client-side apenas)
   - ❌ Sem criptografia
   - ✅ Arquivo `data/admin-credentials.json` não é commitado (está no .gitignore)
   - ⚠️ **Configure suas próprias credenciais fortes antes do primeiro uso**

2. **Autenticação**
   - ❌ Apenas client-side
   - ❌ Sem validação server-side
   - ❌ Sem rate limiting
   - ❌ Sem 2FA

3. **Armazenamento**
   - ❌ LocalStorage não é criptografado
   - ❌ Dados acessíveis via DevTools
   - ❌ Sem backup automático

4. **APIs**
   - ❌ Sem backend seguro
   - ❌ Sem validação server-side
   - ❌ Tentativa de criar issues no GitHub (pode falhar)

## 🔐 Recomendações de Segurança

### Para Uso Pessoal/Protótipo

A implementação atual é adequada para:
- ✅ Projetos pessoais
- ✅ Protótipos
- ✅ Demonstrações
- ✅ Ambientes de desenvolvimento
- ✅ Sites informativos sem dados sensíveis

### Para Produção com Dados Sensíveis

**NÃO use a implementação atual em produção com dados sensíveis sem melhorias:**

#### 1. Backend Seguro

```javascript
// Implemente API REST
- Node.js/Express ou Python/Flask ou Go
- Validação server-side
- Rate limiting
- CORS configurado
```

#### 2. Autenticação Robusta

```javascript
// Opções recomendadas:
- JWT (JSON Web Tokens)
- OAuth 2.0
- Firebase Authentication
- Auth0
- Passport.js
```

#### 3. Banco de Dados

```javascript
// Use banco de dados real:
- PostgreSQL
- MongoDB
- Firebase Firestore
- Supabase

// Com:
- Conexões criptografadas
- Backups automáticos
- Acesso controlado
```

#### 4. Senhas Seguras

```javascript
// Hash de senhas:
- bcrypt (Node.js)
- Argon2 (recomendado)
- scrypt (Python)

// Nunca armazene senhas em plain text!
```

#### 5. HTTPS Obrigatório

```javascript
// Configure:
- Certificado SSL/TLS (Let's Encrypt)
- HSTS headers
- Secure cookies
- CSP (Content Security Policy)
```

#### 6. Proteção Adicional

```javascript
// Implemente:
- CSRF tokens
- XSS protection headers
- Input sanitization
- SQL injection prevention
- Rate limiting
- Session management seguro
- 2FA (Two-Factor Authentication)
```

## 📚 Recursos de Segurança

### Aprender Mais

- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/)
- [MDN Web Security](https://developer.mozilla.org/en-US/docs/Web/Security)
- [Google Web Fundamentals - Security](https://developers.google.com/web/fundamentals/security)

### Ferramentas de Scan

- [npm audit](https://docs.npmjs.com/cli/v8/commands/npm-audit) (se usar Node.js)
- [OWASP ZAP](https://www.zaproxy.org/)
- [Snyk](https://snyk.io/)
- [GitHub Security](https://github.com/security)

## 🔄 Atualizações de Segurança

### Como Mantemos Segurança

1. **Dependências**
   - Monitoramento de CVEs
   - Atualizações regulares
   - GitHub Dependabot alerts

2. **Code Review**
   - Revisão de PRs com foco em segurança
   - Verificação de inputs
   - Validação de lógica

3. **Testes**
   - Testes de penetração básicos
   - Validação de formulários
   - Verificação de sanitização

## 📊 Histórico de Vulnerabilidades

### 2025

Nenhuma vulnerabilidade reportada até o momento.

## 🙏 Hall da Fama de Segurança

Agradecemos aos seguintes pesquisadores de segurança (lista será atualizada):

*Aguardando primeiras contribuições...*

## 📞 Contato

**Para questões de segurança:**
- 🔒 Use a aba "Security" do GitHub para reportar vulnerabilidades
- 🐛 Ou crie uma issue com label `security` (para questões não sensíveis)

**Para outras questões:**
- 🐛 [Issues do GitHub](https://github.com/Thigil15/Jornadadagraca/issues)
- 📖 [Documentação](docs/)

## ⚖️ Divulgação Responsável

Seguimos os princípios de divulgação responsável:

1. **Confidencialidade**: Mantemos detalhes privados até correção
2. **Colaboração**: Trabalhamos com o reporter para verificar e corrigir
3. **Transparência**: Divulgamos após correção com detalhes apropriados
4. **Reconhecimento**: Creditamos descobridores (se desejarem)

## 🔐 Boas Práticas para Usuários

### Se você usar este projeto:

1. **Configure Credenciais**
   ```bash
   # Copie o template e configure suas credenciais
   cp data/admin-credentials.json.example data/admin-credentials.json
   
   # Edite com suas credenciais fortes
   # Formato:
   [
     {
       "email": "seu@email.com",
       "password": "SuaSenhaForte123!"
     }
   ]
   ```

2. **Use HTTPS**
   - Deploy apenas em sites HTTPS
   - Nunca use em HTTP para produção

3. **Backup Regular**
   - Exporte dados regularmente
   - Mantenha backups seguros
   - Não confie apenas em LocalStorage

4. **Monitore Acesso**
   - Verifique logs de acesso (se disponível)
   - Revise testemunhos e contatos pendentes
   - Exclua dados sensíveis antigos

5. **Atualize Regularmente**
   - Mantenha código atualizado
   - Aplique patches de segurança
   - Siga releases do projeto

## 📝 Notas Legais

- Este projeto é fornecido "como está", sem garantias
- Use por sua própria conta e risco
- Não nos responsabilizamos por uso inadequado
- Leia a [LICENSE](LICENSE) para mais detalhes

---

**A segurança é responsabilidade de todos. Obrigado por ajudar a manter o projeto seguro! 🙏🔒**
