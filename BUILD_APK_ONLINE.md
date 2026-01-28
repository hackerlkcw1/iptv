# 🚀 Como Gerar o APK Automaticamente (ONLINE - Sem Instalar Nada!)

## Método GitHub Actions (RECOMENDADO - 100% Automático)

### Passo 1: Criar Conta no GitHub
1. Acesse: https://github.com
2. Clique em "Sign up"
3. Crie sua conta (é grátis!)

### Passo 2: Criar Repositório
1. Faça login no GitHub
2. Clique no **+** no canto superior direito
3. Clique em "New repository"
4. Nome: `kauanflix-android`
5. Deixe como **Public** (ou Private se preferir)
6. Clique em "Create repository"

### Passo 3: Upload do Projeto
1. Na página do repositório, clique em "uploading an existing file"
2. Arraste a pasta `iptv-android-app` inteira
3. Ou clique em "choose your files" e selecione todos os arquivos
4. Aguarde o upload
5. Clique em "Commit changes"

### Passo 4: Ativar GitHub Actions
1. No seu repositório, clique na aba "Actions"
2. GitHub detectará o workflow automaticamente
3. Clique em "I understand my workflows, go ahead and enable them"

### Passo 5: Rodar o Build
1. Clique na aba "Actions" novamente
2. Clique no workflow "Build Android APK"
3. Clique em "Run workflow"
4. Clique no botão verde "Run workflow"

### Passo 6: Aguardar e Baixar
1. Aguarde a compilação (5-10 minutos)
2. Quando ficar verde ✅, clique no workflow
3. Role para baixo até "Artifacts"
4. Clique em "KauanFlix-APK"
5. Baixe o ZIP
6. Extraia o APK
7. **Pronto!** Instale no celular!

---

## Alternativa: Replit (Também Online)

### Passo 1: Criar Conta
1. Acesse: https://replit.com
2. Crie uma conta

### Passo 2: Criar Repl
1. Clique em "+ Create"
2. Escolha "Import from GitHub"
3. Cole a URL do seu repositório GitHub
4. Ou faça upload dos arquivos

### Passo 3: Compilar
1. No terminal do Replit, digite:
```bash
chmod +x gradlew
./gradlew assembleDebug
```
2. Aguarde a compilação
3. O APK estará em: `app/build/outputs/apk/debug/app-debug.apk`

---

## Se Você Preferir Fazer no Android Studio

Eu vi que você já abriu o projeto! Vamos resolver aquele erro:

### Correção Rápida:

1. **Abra**: `settings.gradle`

2. **Encontre**:
```gradle
dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
```

3. **Mude para**:
```gradle
dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.PREFER_SETTINGS)
```

4. **Clique em**: "Sync Now" (notificação azul no topo)

5. **Aguarde** o download das dependências (5-15 min)

6. **Build → Build APK(s)**

7. **Pronto!**

---

## 📱 Precisa de Ajuda Específica?

Me diga qual método você prefere e eu te ajudo passo a passo! 😊

GitHub Actions é o **mais fácil** porque faz tudo automaticamente na nuvem!
