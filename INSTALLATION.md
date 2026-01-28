# 📱 Guia de Instalação e Compilação - KauanFlix Android

## 🎯 Opções de Instalação

Você tem 3 opções para usar o KauanFlix:

### Opção 1: Instalar APK Compilado (Mais Fácil)
### Opção 2: Compilar no Android Studio
### Opção 3: Compilar via Linha de Comando

---

## 📦 OPÇÃO 1: Instalar APK Compilado

### Pré-requisitos
- Smartphone ou tablet Android 7.0+ (API 24+)
- ~50MB de espaço livre

### Passo a Passo

1. **Baixe o APK**
   - Faça o download do arquivo `KauanFlix.apk`

2. **Habilite instalação de fontes desconhecidas**
   - Vá em: Configurações → Segurança
   - Ative: "Fontes desconhecidas" ou "Instalar apps desconhecidos"

3. **Instale o APK**
   - Abra o arquivo APK baixado
   - Clique em "Instalar"
   - Aguarde a instalação

4. **Abra o app**
   - Encontre o ícone "KauanFlix" no menu de apps
   - Toque para abrir

5. **Faça login**
   - URL do Servidor: `http://seu-servidor.com:8080`
   - Usuário: seu username
   - Senha: sua senha
   - Clique em "ENTRAR"

---

## 🛠️ OPÇÃO 2: Compilar no Android Studio

### Pré-requisitos

#### Software Necessário
- **Android Studio**: Hedgehog (2023.1.1) ou superior
  - Download: https://developer.android.com/studio
- **JDK 17**: Incluído no Android Studio
- **Espaço em disco**: ~10GB

#### Conhecimentos Recomendados
- Básico de Android development
- Familiaridade com Gradle

### Passo a Passo Detalhado

#### 1. Instalar Android Studio

**Windows:**
```bash
# Baixe o instalador em:
# https://developer.android.com/studio
# Execute o instalador e siga as instruções
```

**macOS:**
```bash
# Baixe o .dmg em:
# https://developer.android.com/studio
# Arraste para Applications
```

**Linux:**
```bash
# Baixe o .tar.gz
wget https://redirector.gvt1.com/edgedl/android/studio/ide-zips/2023.1.1.26/android-studio-2023.1.1.26-linux.tar.gz

# Extraia
tar -xvzf android-studio-*-linux.tar.gz

# Execute
cd android-studio/bin
./studio.sh
```

#### 2. Preparar o Projeto

```bash
# Opção A: Clone o repositório (se estiver no GitHub)
git clone https://github.com/seu-usuario/kauanflix-android.git
cd kauanflix-android

# Opção B: Ou apenas descompacte o ZIP
unzip kauanflix-android.zip
cd kauanflix-android
```

#### 3. Abrir no Android Studio

1. Abra o Android Studio
2. Clique em "Open" ou "File → Open"
3. Navegue até a pasta `kauanflix-android`
4. Clique em "OK"

#### 4. Aguardar o Gradle Sync

O Android Studio irá automaticamente:
- Baixar dependências (~500MB na primeira vez)
- Configurar o projeto
- Indexar arquivos

**Tempo estimado**: 5-10 minutos (primeira vez)

#### 5. Configurar Emulador ou Dispositivo

**Opção A: Usar Emulador**
1. Tools → Device Manager
2. Create Device
3. Selecione: Pixel 6 (ou similar)
4. Selecione System Image: API 34 (Android 14)
5. Clique em "Finish"

**Opção B: Usar Dispositivo Real**
1. Conecte o smartphone via USB
2. No smartphone:
   - Configurações → Sobre o telefone
   - Toque 7x em "Número da compilação"
   - Volte → Opções do desenvolvedor
   - Ative "Depuração USB"
3. No Android Studio, o dispositivo aparecerá no topo

#### 6. Compilar e Executar

**Método Visual:**
1. Clique no botão ▶️ "Run" no topo
2. Aguarde a compilação
3. O app abrirá automaticamente

**Tempo de compilação**: 2-5 minutos (primeira vez)

**Atalhos:**
- Run: `Shift + F10`
- Debug: `Shift + F9`

#### 7. Gerar APK para Instalação

**Debug APK (para testes):**
```
Build → Build Bundle(s) / APK(s) → Build APK(s)
```
APK estará em: `app/build/outputs/apk/debug/app-debug.apk`

**Release APK (para produção):**
```
Build → Build Bundle(s) / APK(s) → Build APK(s)
```
APK estará em: `app/build/outputs/apk/release/app-release.apk`

---

## ⌨️ OPÇÃO 3: Compilar via Linha de Comando

### Pré-requisitos
- JDK 17
- Android SDK
- Gradle (incluído no projeto)

### Linux/macOS

```bash
# 1. Navegar até o projeto
cd kauanflix-android

# 2. Dar permissão ao gradlew
chmod +x gradlew

# 3. Compilar
./gradlew assembleDebug

# 4. APK estará em:
# app/build/outputs/apk/debug/app-debug.apk

# Para versão release:
./gradlew assembleRelease
```

### Windows

```cmd
REM 1. Navegar até o projeto
cd kauanflix-android

REM 2. Compilar
gradlew.bat assembleDebug

REM 3. APK estará em:
REM app\build\outputs\apk\debug\app-debug.apk

REM Para versão release:
gradlew.bat assembleRelease
```

### Comandos Úteis

```bash
# Limpar build
./gradlew clean

# Compilar e instalar no dispositivo conectado
./gradlew installDebug

# Rodar testes
./gradlew test

# Verificar dependências
./gradlew dependencies

# Listar tarefas disponíveis
./gradlew tasks
```

---

## 📱 Instalando o APK Gerado

### Via Android Studio
1. Com dispositivo conectado:
   ```
   Run → Run 'app'
   ```

### Via ADB (Android Debug Bridge)

```bash
# Instalar
adb install app/build/outputs/apk/debug/app-debug.apk

# Desinstalar
adb uninstall com.kauan.flix

# Verificar dispositivos conectados
adb devices
```

### Via Arquivo

1. Copie o APK para o smartphone
2. Abra o gerenciador de arquivos
3. Toque no APK
4. Clique em "Instalar"

---

## 🐛 Solução de Problemas Comuns

### Erro: "Gradle sync failed"

```bash
# Solução 1: Limpar cache
./gradlew clean

# Solução 2: Invalidar cache do Android Studio
File → Invalidate Caches → Invalidate and Restart
```

### Erro: "SDK not found"

1. Abra SDK Manager: Tools → SDK Manager
2. Instale:
   - Android SDK Platform 34
   - Android SDK Build-Tools 34
   - Android Emulator

### Erro: "Dependency resolution failed"

```bash
# Verifique conexão com internet
# Execute:
./gradlew --refresh-dependencies
```

### Erro: "Device not found"

**Emulador:**
- Verifique se está rodando
- Tools → Device Manager → ▶️

**Dispositivo Real:**
- Verifique se USB debugging está ativo
- Execute: `adb devices`
- Deve aparecer algo como: `0123456789ABCDEF device`

### App trava ao abrir

```bash
# Ver logs
adb logcat | grep KauanFlix

# Ou no Android Studio:
# View → Tool Windows → Logcat
```

---

## ⚙️ Configurações Avançadas

### Assinar APK (Para Release)

1. **Criar Keystore:**
```bash
keytool -genkey -v -keystore kauanflix.keystore -alias kauanflix -keyalg RSA -keysize 2048 -validity 10000
```

2. **Configurar no build.gradle:**
```gradle
android {
    signingConfigs {
        release {
            storeFile file("kauanflix.keystore")
            storePassword "sua_senha"
            keyAlias "kauanflix"
            keyPassword "sua_senha"
        }
    }
    buildTypes {
        release {
            signingConfig signingConfigs.release
        }
    }
}
```

3. **Compilar:**
```bash
./gradlew assembleRelease
```

### Otimizar APK

```gradle
android {
    buildTypes {
        release {
            minifyEnabled true
            shrinkResources true
            proguardFiles getDefaultProguardFile('proguard-android-optimize.txt')
        }
    }
}
```

---

## 📊 Verificar Compilação

### Informações do APK

```bash
# Tamanho
ls -lh app/build/outputs/apk/debug/app-debug.apk

# Conteúdo
aapt dump badging app/build/outputs/apk/debug/app-debug.apk
```

### Métricas Esperadas
- **Tamanho do APK**: ~15-25 MB
- **Tempo de compilação**: 2-5 min (primeira vez)
- **Tempo de instalação**: 10-30 seg
- **RAM necessária**: ~100-200 MB

---

## 📞 Suporte

Se encontrar problemas:

1. **Verifique os logs**
   - Android Studio → Logcat
   - Ou: `adb logcat`

2. **Limpe o projeto**
   ```bash
   ./gradlew clean
   rm -rf .gradle/
   rm -rf build/
   ```

3. **Reinstale dependências**
   ```bash
   ./gradlew --refresh-dependencies
   ```

4. **Abra um issue**
   - Descreva o erro
   - Inclua logs
   - Especifique versão do Android

---

## ✅ Checklist de Instalação

- [ ] Android Studio instalado
- [ ] JDK 17 configurado
- [ ] Projeto aberto no Android Studio
- [ ] Gradle sync completado
- [ ] Emulador ou dispositivo configurado
- [ ] App compilado com sucesso
- [ ] APK gerado
- [ ] App instalado e rodando

---

**Pronto! Seu KauanFlix está instalado e funcionando! 🎉**
