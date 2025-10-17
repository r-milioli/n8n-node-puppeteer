# 🚀 Instruções para Deploy no NPM

## ✅ Configurações já aplicadas:
- ✅ Nome do pacote: `n8n-nodes-puppeteer-integration`
- ✅ Autor: Robson Milioli
- ✅ Email: robson.milioli@gmail.com
- ✅ Repositório: https://github.com/r-milioli/n8n-node-puppeteer
- ✅ Dependência `puppeteer-extra-plugin-user-preferences` adicionada

---

## 📦 PASSO 1: Enviar código para o GitHub

### Opção A: Via Git (linha de comando)

**1. Instale o Git primeiro:**
- Baixe: https://git-scm.com/download/win
- Instale e reinicie o terminal

**2. Execute os comandos no PowerShell:**

```powershell
# Vá para o diretório do projeto
cd d:\dev\n8n-nodes-puppeteer

# Inicializar repositório
git init

# Adicionar todos os arquivos
git add .

# Fazer o commit
git commit -m "feat: add user-preferences plugin support"

# Adicionar o repositório remoto
git remote add origin https://github.com/r-milioli/n8n-node-puppeteer.git

# Configurar branch principal
git branch -M main

# Enviar para o GitHub
git push -u origin main
```

### Opção B: Via GitHub Desktop (interface gráfica)

1. Baixe e instale: https://desktop.github.com/
2. Abra o GitHub Desktop e faça login
3. File > Add Local Repository
4. Selecione: `d:\dev\n8n-nodes-puppeteer`
5. Clique em "Publish repository"
6. Confirme e publique

---

## 🌐 PASSO 2: No servidor Debian (onde tem Node.js)

**1. SSH no servidor:**
```bash
ssh usuario@seu-servidor
```

**2. Clone o repositório:**
```bash
cd ~
git clone https://github.com/r-milioli/n8n-node-puppeteer.git
cd n8n-node-puppeteer
```

**3. Instale as dependências:**
```bash
npm install
```

**4. Faça o build:**
```bash
npm run build
```

**5. Faça login no NPM:**
```bash
npm login
# Username: robsonmilioli
# Password: sua-senha-npm
# Email: robson.milioli@gmail.com
```

**6. Publique no NPM:**
```bash
npm publish
```

---

## 🎉 Pronto! Seu pacote está publicado!

### Para instalar no n8n:

**Via Community Nodes:**
1. Settings > Community Nodes
2. Install: `n8n-nodes-puppeteer-integration`

**Via NPM:**
```bash
npm install n8n-nodes-puppeteer-integration
```

---

## 📊 Links úteis:

- **NPM Package:** https://www.npmjs.com/package/n8n-nodes-puppeteer-integration
- **GitHub Repo:** https://github.com/r-milioli/n8n-node-puppeteer
- **Seu perfil NPM:** https://www.npmjs.com/~robsonmilioli

---

## 🔄 Para atualizar o pacote no futuro:

```bash
# 1. Edite a versão no package.json (ex: 1.4.2 → 1.4.3)
# 2. Faça suas alterações
# 3. No servidor:
git pull
npm install
npm run build
npm publish
```

---

## ⚠️ Troubleshooting:

### Erro: "You do not have permission to publish"
```bash
npm login
# Faça login novamente
```

### Erro: "Package name already exists"
```bash
# O nome já foi usado, escolha outro no package.json
```

### Erro: "npm ERR! 402 Payment Required"
```bash
# Você tentou publicar pacote privado (precisa pagar)
# Use: npm publish --access public
```

---

Boa sorte! 🚀

