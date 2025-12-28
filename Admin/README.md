# 🔐 Admin - Painel de Administração

Este diretório contém todos os arquivos relacionados ao painel administrativo do site Jornada da Graça.

## 📁 Arquivos

- **`login.html`** - Página de login para acesso ao painel administrativo
- **`admin.html`** - Dashboard principal do painel administrativo
- **`admin-credentials.json.example`** - Template de credenciais (use como exemplo)
- **`admin-credentials.json`** - Arquivo de credenciais (não versionado no git)

## 🚀 Configuração Inicial

Antes de usar o painel administrativo pela primeira vez, você precisa configurar suas credenciais:

### 1. Copie o arquivo de exemplo

```bash
cp Admin/admin-credentials.json.example Admin/admin-credentials.json
```

### 2. Edite o arquivo com suas credenciais

Abra o arquivo `Admin/admin-credentials.json` e altere o email e a senha:

```json
[
  {
    "email": "seu-email@exemplo.com",
    "password": "ALTERE_ESTA_SENHA_PARA_UMA_SENHA_FORTE"
  }
]
```

⚠️ **IMPORTANTE**: Use uma senha forte e mantenha suas credenciais em segurança!

## 🌐 Acesso ao Painel

Após configurar as credenciais, você pode acessar o painel de duas formas:

1. **Via redirect**: Acesse `/admin.html` - será redirecionado automaticamente para o login
2. **Diretamente**: Acesse `/Admin/login.html` - vai direto para a página de login

## 🔒 Segurança

- ✅ O arquivo `admin-credentials.json` está no `.gitignore` e **não será commitado**
- ✅ As credenciais são verificadas apenas no lado do cliente (client-side)
- ⚠️ Para uso em produção, considere implementar autenticação server-side
- ⚠️ Sempre use HTTPS em produção para proteger as credenciais

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
- **login.html** carrega credenciais de `./admin-credentials.json`
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
