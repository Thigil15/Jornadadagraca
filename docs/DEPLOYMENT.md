# 🚀 Guia de Deployment

Este guia explica como fazer o deploy da aplicação Jornada da Graça em diferentes plataformas.

## 📋 Pré-requisitos

A aplicação é uma SPA (Single Page Application) estática que não requer:
- ❌ Node.js ou npm
- ❌ Build steps ou compilation
- ❌ Servidor backend
- ❌ Banco de dados

Você precisa apenas de:
- ✅ Um servidor web capaz de servir arquivos HTML estáticos
- ✅ Suporte a HTTPS (recomendado para PWA)

## 🌐 GitHub Pages (Recomendado)

### Configuração Inicial

1. **Prepare o Repositório**
   ```bash
   # Certifique-se de que todos os arquivos estão commitados
   git add .
   git commit -m "Prepare para deploy"
   git push origin main
   ```

2. **Configure GitHub Pages**
   - Vá para Settings do repositório
   - Navegue até "Pages"
   - Em "Source", selecione:
     - Branch: `main`
     - Folder: `/ (root)`
   - Clique em "Save"

3. **Aguarde o Deploy**
   - O GitHub Pages levará alguns minutos para fazer o deploy
   - A URL será: `https://[seu-usuario].github.io/Jornadadagraca/`

4. **Configure Custom Domain (Opcional)**
   - Em GitHub Pages settings, adicione seu domínio customizado
   - Atualize os registros DNS do seu domínio:
     ```
     CNAME: www -> [seu-usuario].github.io
     A Records:
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```

### Atualizações Automáticas

Cada push para o branch `main` automaticamente aciona um novo deploy:

```bash
# Faça suas mudanças
git add .
git commit -m "Atualização do conteúdo"
git push origin main
# Deploy automático acontece em ~2 minutos
```

## 📦 Netlify

### Deploy via Git

1. **Conecte ao Netlify**
   - Acesse [netlify.com](https://netlify.com)
   - Clique em "Add new site" → "Import an existing project"
   - Conecte sua conta GitHub
   - Selecione o repositório Jornadadagraca

2. **Configure Build Settings**
   ```
   Build command: (deixe vazio)
   Publish directory: /
   ```

3. **Deploy**
   - Clique em "Deploy site"
   - Netlify gerará uma URL: `https://random-name.netlify.app`

4. **Custom Domain (Opcional)**
   - Vá em "Domain settings"
   - Adicione seu domínio customizado
   - Siga as instruções para configurar DNS

### Deploy Contínuo

- Todo push para o branch principal aciona deploy automático
- Preview deployments para Pull Requests
- Rollback fácil para versões anteriores

### Variáveis de Ambiente (se necessário)

```
# Em Netlify → Site settings → Environment variables
SITE_URL=https://seu-dominio.com
```

## ☁️ Vercel

### Deploy via CLI

1. **Instale Vercel CLI**
   ```bash
   npm install -g vercel
   ```

2. **Deploy**
   ```bash
   cd Jornadadagraca
   vercel
   ```

3. **Siga o prompt:**
   - Set up and deploy: Yes
   - Project name: jornadadagraca
   - Directory: ./
   - Build command: (deixe vazio)
   - Output directory: (deixe vazio)

### Deploy via Git

1. Acesse [vercel.com](https://vercel.com)
2. "Add New" → "Project"
3. Import seu repositório GitHub
4. Configure:
   ```
   Framework Preset: Other
   Build Command: (deixe vazio)
   Output Directory: (deixe vazio)
   Install Command: (deixe vazio)
   ```
5. Deploy

## 🗄️ Cloudflare Pages

1. **Configure Cloudflare Pages**
   - Acesse [pages.cloudflare.com](https://pages.cloudflare.com)
   - "Create a project"
   - Conecte repositório GitHub

2. **Build Settings**
   ```
   Production branch: main
   Build command: (none)
   Build output directory: /
   ```

3. **Deploy**
   - Deploy automático após configuração
   - URL: `https://jornadadagraca.pages.dev`

## 🐳 Docker (Opcional)

Para ambientes que requerem containerização:

### Dockerfile

```dockerfile
FROM nginx:alpine
COPY . /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```

### Build e Run

```bash
# Build
docker build -t jornadadagraca .

# Run
docker run -d -p 8080:80 jornadadagraca

# Acesse em http://localhost:8080
```

## 🖥️ Servidor Tradicional (Apache/Nginx)

### Apache

1. **Upload via FTP/SFTP**
   ```
   Faça upload de todos os arquivos para: /var/www/html/
   ```

2. **Configure .htaccess** (se necessário)
   ```apache
   # Force HTTPS
   RewriteEngine On
   RewriteCond %{HTTPS} off
   RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
   
   # Enable compression
   <IfModule mod_deflate.c>
     AddOutputFilterByType DEFLATE text/html text/plain text/xml text/css text/javascript application/javascript
   </IfModule>
   ```

### Nginx

1. **Configure nginx.conf**
   ```nginx
   server {
       listen 80;
       server_name seu-dominio.com;
       root /var/www/jornadadagraca;
       index index.html;
       
       location / {
           try_files $uri $uri/ /index.html;
       }
       
       # Enable gzip compression
       gzip on;
       gzip_types text/plain text/css application/json application/javascript text/xml application/xml;
   }
   ```

2. **Upload Files**
   ```bash
   scp -r * user@server:/var/www/jornadadagraca/
   ```

3. **Restart Nginx**
   ```bash
   sudo systemctl restart nginx
   ```

## 🔒 Configuração HTTPS

### Let's Encrypt (Gratuito)

```bash
# Instale certbot
sudo apt-get install certbot python3-certbot-nginx

# Obtenha certificado
sudo certbot --nginx -d seu-dominio.com -d www.seu-dominio.com

# Renovação automática já está configurada
```

## ✅ Checklist Pós-Deploy

Após fazer o deploy, verifique:

- [ ] Site está acessível via HTTPS
- [ ] Service Worker está registrado (Console do navegador)
- [ ] PWA pode ser instalado em dispositivos móveis
- [ ] Todos os links funcionam corretamente
- [ ] Formulários enviam dados corretamente
- [ ] Versículos do dia carregam corretamente
- [ ] Sistema de testemunhos funciona
- [ ] Admin panel é acessível
- [ ] Botões de compartilhamento funcionam
- [ ] Design responsivo em mobile/tablet/desktop
- [ ] Performance score (Lighthouse) > 90

## 🔧 Troubleshooting

### Problema: PWA não instala

**Solução:**
- Verifique se o site está em HTTPS
- Confirme que `manifest.json` está acessível
- Verifique que `service-worker.js` está registrado
- Teste em modo de navegação anônima

### Problema: Service Worker não atualiza

**Solução:**
```javascript
// Limpe o cache do service worker
if ('serviceWorker' in navigator) {
  navigator.serviceWorker.getRegistrations().then(registrations => {
    registrations.forEach(registration => registration.unregister());
  });
}
```

### Problema: Links quebrados após deploy

**Solução:**
- Verifique caminhos absolutos vs relativos
- Configure base URL corretamente no `manifest.json`
- Use caminhos relativos quando possível

## 📊 Monitoramento

### Google Analytics (Opcional)

Adicione antes do `</head>` em `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Performance Monitoring

Use [Google Lighthouse](https://developers.google.com/web/tools/lighthouse) para:
- Performance
- Accessibility
- Best Practices
- SEO
- PWA

## 🔄 CI/CD Automation

### GitHub Actions (Exemplo)

Crie `.github/workflows/deploy.yml`:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./
```

## 📞 Suporte

Se encontrar problemas durante o deploy:

1. Verifique a [documentação oficial](README.md)
2. Consulte as [Issues do GitHub](https://github.com/Thigil15/Jornadadagraca/issues)
3. Abra uma nova issue com:
   - Plataforma de deploy
   - Mensagens de erro
   - Passos que você seguiu

---

**Que seu deploy seja bem-sucedido e alcance muitos corações! 🙏✨**
