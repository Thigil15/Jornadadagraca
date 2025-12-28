# Data Directory

Este diretório contém os arquivos de dados da aplicação.

## Arquivos

### admin-credentials.json (NÃO VERSIONADO)

**⚠️ IMPORTANTE**: Este arquivo contém as credenciais de administrador e **NÃO deve ser commitado** no repositório.

#### Configuração Inicial

1. Copie o arquivo template:
   ```bash
   cp admin-credentials.json.example admin-credentials.json
   ```

2. Edite o arquivo `admin-credentials.json` com suas credenciais:
   ```json
   [
     {
       "email": "seu-email@exemplo.com",
       "password": "SuaSenhaSegura123!"
     }
   ]
   ```

3. **Segurança**:
   - Use uma senha forte e única
   - Não compartilhe suas credenciais
   - O arquivo já está no `.gitignore` e não será commitado
   - Mantenha o arquivo seguro em seu ambiente local

### comentarios.json

Contém os testemunhos aprovados que são exibidos no site.

### versiculos.json

Contém a base de versículos bíblicos que são exibidos diariamente no site.

## Notas de Segurança

- ⚠️ O arquivo `admin-credentials.json` está listado no `.gitignore`
- ✅ Sempre use o template `.example` como referência
- ✅ Configure credenciais fortes antes do primeiro uso
- ✅ Não exponha credenciais em documentação ou código
