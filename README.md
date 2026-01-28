# KauanFlix - App Android IPTV Player

<div align="center">
  <h3>📱 Player IPTV moderno e completo para Android</h3>
  <p>Desenvolvido com Kotlin, Jetpack Compose e ExoPlayer</p>
</div>

## 🎯 Características

### ✨ Interface Moderna
- **Jetpack Compose**: UI declarativa e moderna
- **Material Design 3**: Componentes atualizados
- **Animações fluidas**: Transições suaves entre telas
- **Dark Mode**: Interface escura profissional
- **Gradientes neon**: Design vibrante (ciano, roxo, rosa)

### 📺 Funcionalidades
- ✅ **TV ao Vivo**: Streaming de canais em tempo real
- ✅ **Filmes VOD**: Catálogo completo de filmes
- ✅ **Séries**: Navegação por temporadas e episódios
- ✅ **Busca em tempo real**: Pesquisa rápida e eficiente
- ✅ **Categorias**: Filtros por categoria
- ✅ **Histórico**: Continue de onde parou
- ✅ **ExoPlayer**: Reprodução profissional de vídeo

### 🔐 Segurança e Persistência
- **DataStore**: Armazenamento seguro de credenciais
- **Autenticação Xtream Codes**: Login com servidor, usuário e senha
- **Cache inteligente**: Reduz chamadas desnecessárias à API
- **Sessão persistente**: Login automático

## 🏗️ Arquitetura

```
┌─────────────────────────────────────────────────┐
│                  UI Layer                       │
│  (Jetpack Compose Screens + Material Design 3)  │
├─────────────────────────────────────────────────┤
│               ViewModel Layer                   │
│     (LoginViewModel, MainViewModel)             │
├─────────────────────────────────────────────────┤
│              Repository Layer                   │
│           (XtreamRepository)                    │
├─────────────────────────────────────────────────┤
│               Data Sources                      │
│  (XtreamApi + PreferencesManager)               │
└─────────────────────────────────────────────────┘
```

### Padrões Utilizados
- **MVVM**: Model-View-ViewModel
- **Repository Pattern**: Abstração de fontes de dados
- **StateFlow**: Gerenciamento reativo de estado
- **Dependency Injection**: Manual (fácil migração para Hilt)

## 📋 Requisitos

- **Android Studio**: Hedgehog (2023.1.1) ou superior
- **Gradle**: 8.1+
- **Min SDK**: 24 (Android 7.0)
- **Target SDK**: 34 (Android 14)
- **Kotlin**: 1.9.20
- **Compose**: 1.5.4

## 🚀 Instalação

### 1. Clone o repositório
```bash
git clone https://github.com/seu-usuario/kauanflix-android.git
cd kauanflix-android
```

### 2. Abra no Android Studio
- File → Open → Selecione a pasta do projeto
- Aguarde o Gradle Sync

### 3. Configure um emulador ou dispositivo
- AVD Manager → Create Virtual Device
- Ou conecte um dispositivo físico via USB

### 4. Execute o app
- Clique em "Run" (▶️) ou pressione Shift+F10

## 📱 Estrutura do Projeto

```
app/
├── src/main/
│   ├── java/com/kauan/flix/
│   │   ├── data/
│   │   │   ├── api/           # Retrofit API interface
│   │   │   ├── model/         # Data classes (modelos)
│   │   │   ├── repository/    # Repository pattern
│   │   │   └── preferences/   # DataStore manager
│   │   ├── ui/
│   │   │   ├── screen/        # Composable screens
│   │   │   ├── theme/         # Tema, cores, tipografia
│   │   │   └── viewmodel/     # ViewModels
│   │   ├── MainActivity.kt    # Activity principal
│   │   ├── PlayerActivity.kt  # Activity do player
│   │   └── KauanFlixApp.kt    # Application class
│   ├── AndroidManifest.xml
│   └── res/
│       ├── values/
│       │   ├── strings.xml
│       │   └── themes.xml
│       └── xml/
│           ├── backup_rules.xml
│           └── data_extraction_rules.xml
└── build.gradle
```

## 🎨 Design System

### Cores Principais
```kotlin
PrimaryCyan   = #00D9FF  // Azul ciano neon
PrimaryPurple = #8B5CF6  // Roxo vibrante
PrimaryPink   = #FF006E  // Rosa intenso
PrimaryOrange = #FF6B35  // Laranja quente
```

### Backgrounds
```kotlin
BackgroundDark    = #0A0E1A  // Fundo principal
BackgroundCard    = #1A1F35  // Cards e elementos
BackgroundSidebar = #141829  // Sidebar
```

### Gradientes
- **Live TV**: Ciano → Azul
- **Filmes**: Laranja → Rosa
- **Séries**: Roxo → Rosa Claro

## 🔧 Configuração

### Credenciais Xtream
O app requer:
1. **URL do Servidor**: `http://seu-servidor.com:8080`
2. **Usuário**: Seu username
3. **Senha**: Sua senha

### ExoPlayer
Configurado com:
- HLS support
- Controles nativos
- Auto-play
- Modo fullscreen
- Controles automáticos (timeout: 5s)

## 📦 Dependências Principais

```gradle
// Jetpack Compose
implementation "androidx.compose.ui:ui:1.5.4"
implementation "androidx.compose.material3:material3:1.1.2"

// Navigation
implementation "androidx.navigation:navigation-compose:2.7.5"

// ExoPlayer
implementation "androidx.media3:media3-exoplayer:1.2.0"
implementation "androidx.media3:media3-ui:1.2.0"

// Networking
implementation "com.squareup.retrofit2:retrofit:2.9.0"
implementation "com.squareup.retrofit2:converter-gson:2.9.0"

// Image Loading
implementation "io.coil-kt:coil-compose:2.5.0"

// DataStore
implementation "androidx.datastore:datastore-preferences:1.0.0"
```

## 🎬 Funcionalidades Detalhadas

### TV ao Vivo
- Lista todos os canais disponíveis
- Ícones dos canais
- Reprodução instantânea com ExoPlayer
- Suporte a M3U8/HLS
- Filtro por categorias

### Filmes
- Grid de posters
- Informações do filme (quando disponível)
- Reprodução direta
- Suporte a múltiplos formatos (MP4, MKV, etc.)

### Séries
- Navegação por temporadas
- Seleção de episódios
- Informações detalhadas
- Capas e sinopses
- Progresso de visualização

### Histórico
- Últimos 50 itens assistidos
- Continue de onde parou
- Barra de progresso visual
- Informações de episódio (séries)
- Opção de limpar histórico

## 🛡️ Segurança

- ✅ Credenciais armazenadas com DataStore (encrypted)
- ✅ HTTPS quando disponível
- ✅ Validação de entrada
- ✅ Timeout de conexão configurado
- ✅ Tratamento de erros robusto

## 🐛 Solução de Problemas

### Erro de compilação
```bash
./gradlew clean
./gradlew build
```

### Erro de sincronização Gradle
- File → Invalidate Caches → Invalidate and Restart

### Vídeo não carrega
- Verifique a URL do servidor
- Confirme as credenciais
- Teste a conexão de rede
- Verifique se o formato é suportado

### App trava ao abrir
- Limpe dados do app
- Reinstale
- Verifique logs no Logcat

## 📱 Screenshots

*(Adicione screenshots do app aqui)*

## 🔄 Roadmap

- [ ] Suporte a legendas
- [ ] Download offline
- [ ] Favoritos
- [ ] Chromecast
- [ ] Modo PiP (Picture-in-Picture)
- [ ] Tema claro
- [ ] Múltiplos perfis
- [ ] Controle parental

## 📄 Licença

Este projeto é fornecido como está, sem garantias.

## 👨‍💻 Desenvolvimento

### Tecnologias
- Kotlin 1.9.20
- Jetpack Compose 1.5.4
- Material Design 3
- ExoPlayer 1.2.0
- Retrofit 2.9.0
- Coil 2.5.0
- DataStore 1.0.0

### Requisitos de Build
- JDK 17
- Android Gradle Plugin 8.1.2
- Gradle 8.1

## 🆘 Suporte

Para problemas ou dúvidas:
1. Verifique a documentação
2. Consulte os issues no GitHub
3. Abra um novo issue descrevendo o problema

## 🙏 Agradecimentos

- Anthropic (Claude) - Assistência no desenvolvimento
- Android Team - Jetpack Compose
- Google - ExoPlayer
- Comunidade Open Source

---

**Desenvolvido com ❤️ usando Kotlin e Jetpack Compose**
