# 🎬 KauanFlix - Aplicativo Android IPTV

## 📱 Sobre o Projeto

O **KauanFlix** é um aplicativo Android moderno e profissional para reprodução de conteúdo IPTV através da API Xtream Codes. Foi desenvolvido completamente em Kotlin com Jetpack Compose, oferecendo uma experiência de usuário fluida e intuitiva.

### ✨ Destaques

- 📺 **TV ao Vivo**: Assista canais em tempo real
- 🎬 **Filmes**: Catálogo completo de filmes VOD
- 📺 **Séries**: Navegue por temporadas e episódios
- 🎨 **Design Moderno**: Interface com gradientes neon e animações
- 💾 **Histórico**: Continue de onde parou
- 🔐 **Login Automático**: Credenciais salvas com segurança

## 📦 Conteúdo do Pacote

```
KauanFlix-Android/
├── README.md              # Este arquivo
├── INSTALLATION.md        # Guia completo de instalação
├── USER_GUIDE.md         # Manual de uso do app
├── CHANGELOG.md          # Notas de versão
├── build.gradle          # Configuração do projeto
├── settings.gradle       # Configurações Gradle
├── gradle.properties     # Propriedades do Gradle
└── app/
    ├── build.gradle               # Configuração do módulo app
    ├── proguard-rules.pro         # Regras ProGuard
    ├── src/main/
    │   ├── AndroidManifest.xml    # Manifest do app
    │   ├── java/com/kauan/flix/   # Código-fonte Kotlin
    │   │   ├── data/              # Camada de dados
    │   │   │   ├── api/           # Retrofit API
    │   │   │   ├── model/         # Modelos de dados
    │   │   │   ├── repository/    # Repositórios
    │   │   │   └── preferences/   # DataStore
    │   │   ├── ui/                # Interface do usuário
    │   │   │   ├── screen/        # Telas Compose
    │   │   │   ├── theme/         # Tema e cores
    │   │   │   └── viewmodel/     # ViewModels
    │   │   ├── MainActivity.kt    # Activity principal
    │   │   ├── PlayerActivity.kt  # Player de vídeo
    │   │   └── KauanFlixApp.kt    # Application class
    │   └── res/                   # Recursos (strings, themes, XML)
    └── ...
```

## 🚀 Como Começar

### Opção 1: Instalar APK Pronto (Mais Fácil)

Se você recebeu um APK compilado:

1. **Habilite instalação de apps desconhecidos** no Android
2. **Instale o APK** no seu dispositivo
3. **Abra o app** e faça login com suas credenciais Xtream

### Opção 2: Compilar o Projeto

Se você quer compilar o código-fonte:

1. **Leia o arquivo**: `INSTALLATION.md` (guia completo)
2. **Instale**: Android Studio Hedgehog ou superior
3. **Abra o projeto** no Android Studio
4. **Aguarde** o Gradle Sync
5. **Execute** o app (▶️)

## 📖 Documentação

### 📚 Guias Disponíveis

1. **INSTALLATION.md**
   - Como instalar Android Studio
   - Como compilar o projeto
   - Compilação via linha de comando
   - Gerar APK
   - Solução de problemas técnicos

2. **USER_GUIDE.md**
   - Como usar o aplicativo
   - Tutorial de cada funcionalidade
   - Dicas e truques
   - Perguntas frequentes
   - Troubleshooting

3. **CHANGELOG.md**
   - Notas da versão 1.0.0
   - Funcionalidades implementadas
   - Tecnologias utilizadas
   - Roadmap futuro

## 🎯 Funcionalidades Principais

### 🔐 Login e Autenticação
- Formulário de login moderno
- Validação de credenciais
- Mensagens de erro claras
- Login automático (credenciais salvas)
- Logout seguro

### 📺 TV ao Vivo
- Lista de todos os canais
- Ícones dos canais
- Busca em tempo real
- Filtro por categorias
- Player ExoPlayer integrado
- Suporte HLS/M3U8

### 🎬 Filmes
- Grid de posters
- Busca instantânea
- Filtro por categoria
- Reprodução direta
- Informações do filme

### 📺 Séries
- Catálogo completo
- Navegação por temporadas
- Seleção de episódios
- Informações detalhadas
- Capas e metadados

### ⏯️ Histórico
- Continue assistindo
- Até 50 itens salvos
- Barra de progresso
- Salva posição automaticamente
- Opção de limpar

## 💻 Requisitos Técnicos

### Para Usar o App
- Android 7.0+ (API 24+)
- 50MB de espaço livre
- Conexão com internet
- Credenciais Xtream Codes válidas

### Para Compilar
- Android Studio Hedgehog (2023.1.1+)
- JDK 17
- Gradle 8.1+
- ~10GB de espaço em disco

## 🛠️ Tecnologias

### Core
- **Linguagem**: Kotlin 1.9.20
- **Build**: Gradle 8.1
- **Min SDK**: 24 (Android 7.0)
- **Target SDK**: 34 (Android 14)

### Interface
- **Jetpack Compose**: 1.5.4
- **Material Design**: 3
- **Navigation**: Compose 2.7.5

### Networking
- **Retrofit**: 2.9.0
- **OkHttp**: 4.12.0
- **Gson**: 2.10.1

### Media
- **ExoPlayer**: (Media3) 1.2.0
- **Coil**: 2.5.0 (imagens)

### Arquitetura
- **Pattern**: MVVM
- **Storage**: DataStore
- **Async**: Coroutines + Flow

## 🎨 Design

### Paleta de Cores
- **Cyan Neon**: #00D9FF
- **Purple**: #8B5CF6
- **Pink**: #FF006E
- **Orange**: #FF6B35
- **Background**: #0A0E1A

### Características Visuais
- Dark mode por padrão
- Gradientes vibrantes
- Animações suaves
- Cards com elevação
- Ícones modernos

## 📱 Screenshots

_(Adicione screenshots aqui quando disponíveis)_

## ❓ Precisa de Ajuda?

### 🐛 Encontrou um Bug?
1. Verifique se já foi reportado
2. Abra um issue no GitHub
3. Descreva o problema detalhadamente
4. Inclua logs se possível

### 💬 Dúvidas sobre Uso?
- Leia o **USER_GUIDE.md**
- Verifique as FAQs
- Entre em contato com suporte

### 🔧 Problemas Técnicos?
- Consulte **INSTALLATION.md**
- Veja a seção "Troubleshooting"
- Limpe e recompile o projeto

## 🔒 Segurança e Privacidade

- ✅ Credenciais criptografadas localmente
- ✅ Sem coleta de dados pessoais
- ✅ Sem rastreamento de uso
- ✅ Sem anúncios
- ✅ Código-fonte disponível

## 📜 Licença

Este projeto é fornecido como está, sem garantias.

## 🙏 Agradecimentos

- **Anthropic (Claude)** - Assistência no desenvolvimento
- **Android Team** - Jetpack Compose e ExoPlayer
- **Material Design Team** - Design system
- **Open Source Community** - Bibliotecas utilizadas

## 📞 Contato

- **Issues**: GitHub Issues
- **Email**: _(adicionar se houver)_
- **Website**: _(adicionar se houver)_

## 🔄 Versão

**v1.0.0** - Lançamento Inicial (28/01/2025)

Veja **CHANGELOG.md** para detalhes completos.

## 📋 Checklist Rápido

Antes de começar:

- [ ] Tenho credenciais Xtream Codes válidas
- [ ] Li a documentação necessária
- [ ] Instalei as ferramentas (se for compilar)
- [ ] Tenho Android 7.0+ (para usar o app)

Para compilar:
- [ ] Android Studio instalado
- [ ] JDK 17 configurado
- [ ] Projeto importado
- [ ] Gradle sync completo

Para usar:
- [ ] App instalado
- [ ] Login realizado
- [ ] Internet conectada

## 🎓 Próximos Passos

1. **Se você vai USAR o app**:
   - Instale o APK
   - Leia **USER_GUIDE.md**
   - Faça login e aproveite!

2. **Se você vai COMPILAR**:
   - Leia **INSTALLATION.md**
   - Abra no Android Studio
   - Compile e execute

3. **Se você vai CONTRIBUIR**:
   - Fork o repositório
   - Crie uma branch
   - Faça suas alterações
   - Envie um pull request

## 🌟 Features em Destaque

### Destaque 1: Continue Assistindo
O app salva automaticamente onde você parou, permitindo continuar de onde parou em qualquer dispositivo (com mesma conta).

### Destaque 2: Busca Instantânea
A busca funciona em tempo real enquanto você digita, filtrando instantaneamente os resultados.

### Destaque 3: Design Moderno
Interface completamente moderna com Jetpack Compose, seguindo as últimas diretrizes do Material Design 3.

### Destaque 4: Performance
Otimizado para usar poucos recursos, com cache inteligente e carregamento assíncrono.

---

## 📌 Resumo Ultra-Rápido

**O que é?** App IPTV para Android com Xtream Codes

**Como instalar?** 
- Usuário: Instale o APK
- Desenvolvedor: Compile no Android Studio

**Funciona?** Sim! TV ao vivo, filmes e séries

**É grátis?** O app sim, mas você precisa de assinatura IPTV

**Documentação?** 3 guias completos inclusos

---

**Desenvolvido com ❤️ usando Kotlin e Jetpack Compose**

🎬 **Bom entretenimento com KauanFlix!** 🎬
