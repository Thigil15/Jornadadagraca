# 🔐 Admin - Painel de Administração

Este diretório contém todos os arquivos relacionados ao painel administrativo do site Jornada da Graça.

## 📁 Arquivos

- **`login.html`** - Página de login para acesso ao painel administrativo (credenciais embutidas)
- **`admin.html`** - Dashboard principal do painel administrativo
- **`admin-credentials.json.example`** - Arquivo de exemplo (não mais usado, mantido para referência)

## 🚀 Configuração Inicial

As credenciais de acesso estão embutidas diretamente no código do arquivo `login.html`.

### Credenciais Padrão

- **Email**: `admin@jornadadagraca.com`
- **Senha**: `JornadaDaGraca2024!`

### Como Alterar as Credenciais

1. Abra o arquivo `Admin/login.html`
2. Localize a seção de credenciais no código JavaScript (linha ~126)
3. Altere o email e/ou senha conforme necessário:

```javascript
const credentials = [
    {
        "email": "seu-novo-email@exemplo.com",
        "password": "SUA_NOVA_SENHA_FORTE"
    }
];
```

⚠️ **IMPORTANTE**: Use uma senha forte e mantenha suas credenciais em segurança!

## 🌐 Acesso ao Painel

Após configurar as credenciais, você pode acessar o painel de duas formas:

1. **Via redirect**: Acesse `/admin.html` - será redirecionado automaticamente para o login
2. **Diretamente**: Acesse `/Admin/login.html` - vai direto para a página de login

## 🔒 Segurança

⚠️ **ATENÇÃO CRÍTICA DE SEGURANÇA**: 
- As credenciais estão **VISÍVEIS** no código-fonte do arquivo `login.html`
- Qualquer pessoa que acessar o site pode ver as credenciais usando "Ver código-fonte" ou DevTools do navegador
- Esta é uma solução **apenas para ambiente de desenvolvimento/testes** ou sites internos
- **NÃO USE EM PRODUÇÃO** com credenciais reais sem implementar autenticação server-side

### Detalhes Técnicos
- ✅ As credenciais estão embutidas no código JavaScript do arquivo `login.html`
- ✅ As credenciais são verificadas apenas no lado do cliente (client-side)
- ⚠️ Para uso em produção, **IMPLEMENTE** autenticação server-side
- ⚠️ Sempre use HTTPS em produção para proteger as credenciais
- ⚠️ Mude as credenciais padrão para algo seguro antes de usar
- ⚠️ Qualquer pessoa com acesso ao site pode ver as credenciais no código-fonte

## 📊 Funcionalidades do Painel

### 💬 Gerenciamento de Testemunhos
- Visualizar todos os testemunhos enviados
- Aprovar ou reprovar testemunhos
- Excluir testemunhos
- Exportar testemunhos em JSON

### 📞 Gerenciamento de Contatos
- Visualizar solicitações de contato
- Ver detalhes completos (nome, email, telefone, necessidade)
- Excluir contatos processados
- Exportar contatos em JSON

### 📖 Gerenciamento de Versículos
- Adicionar novos versículos
- Editar versículos existentes
- Excluir versículos
- Importar versículos em lote (JSON)
- Exportar todos os versículos (JSON)

## 🛠️ Estrutura de Dados

### Formato de Credenciais

```json
[
  {
    "email": "usuario@exemplo.com",
    "password": "senha_forte_aqui"
  }
]
```

### Formato de Versículos

O painel carrega versículos do arquivo `../data/versiculos.json`:

```json
[
  {
    "id": 1,
    "text": "Texto do versículo",
    "reference": "Livro X:Y",
    "message": "Mensagem reflexiva sobre o versículo"
  }
]
```

## 🔄 Sessão e Logout

- A sessão dura **24 horas** após o login
- Use o botão "Sair" para fazer logout manualmente
- A sessão expira automaticamente ao fechar o navegador
- Logout automático ocorre após 24 horas de inatividade

## 📝 Notas de Desenvolvimento

### Caminhos Relativos

Todos os arquivos admin usam caminhos relativos:
- **login.html** usa credenciais embutidas no código JavaScript
- **admin.html** carrega dados de `../data/versiculos.json`
- Links para o site principal usam `../index.html`

### Armazenamento de Dados

- **Testemunhos e Contatos**: Armazenados em `localStorage`
- **Versículos**: Carregados de `../data/versiculos.json` com cache em `localStorage`
- **Sessão**: Gerenciada via `sessionStorage`

## 🤝 Suporte

Para problemas ou dúvidas:
- 📖 Consulte a [documentação principal](../README.md)
- 🐛 [Reportar bugs](https://github.com/Thigil15/Jornadadagraca/issues)
- 💬 Entre em contato através do GitHub

---

**Feito com ❤️ para a Jornada da Graça**
