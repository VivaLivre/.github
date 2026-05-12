# 💙 VivaLivre — Acessibilidade e Dignidade em suas mãos

<p align="center">
  <img src="img/icon_app.png" width="150" alt="VivaLivre Logo">
</p>

<p align="center">
  <strong>Devolvendo autonomia, segurança e qualidade de vida para quem tem pressa.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter">
  <img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="Go">
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/PostGIS-336791?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostGIS">
  <img src="https://img.shields.io/badge/BLoC-blueviolet?style=for-the-badge&logo=flutter&logoColor=white" alt="BLoC">
</p>

---

## 🎯 Visão e Missão

### Visão
Criar um ecossistema tecnológico que devolva autonomia, segurança e qualidade de vida para pessoas que vivem com **Doenças Inflamatórias Intestinais (DII)**, como Doença de Crohn e Retocolite Ulcerativa.

### Missão
Fornecer ferramentas digitais que permitam aos utilizadores:
- 🚨 Localizar rapidamente banheiros adaptados em situações de emergência
- 📊 Registar e acompanhar sintomas e padrões de saúde
- 🗺️ Contribuir para um mapa colaborativo de recursos acessíveis
- 🪪 Validar-se como portador de DII em locais públicos
- 📈 Compartilhar dados de saúde com profissionais médicos

---

## 🚀 Sobre o Projeto

**VivaLivre** é uma solução full-stack desenvolvida para resolver um problema real de mobilidade urbana e saúde: a dificuldade de encontrar banheiros acessíveis e pontos de suporte em tempo real para pessoas com DII.

Utilizando geolocalização avançada com **PostGIS** e processamento de dados espaciais, o app oferece uma interface intuitiva para que utilizadores possam:
- Localizar banheiros adaptados próximos em um toque
- Avaliar e comentar sobre pontos de apoio
- Registar sintomas e padrões de saúde
- Manter um histórico digital para consultas médicas
- Contribuir para um mapa colaborativo comunitário

**Garantindo autonomia e conforto no dia a dia.**

## 🛠️ Arquitetura Técnica

Diferente de soluções convencionais, o VivaLivre foi construído com uma arquitetura independente, escalável e desacoplada:

### Stack Tecnológico

```
┌─────────────────────────────────────────────────────────────┐
│                    VIVALIVRE ECOSYSTEM                      │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ┌──────────────────┐         ┌──────────────────────┐    │
│  │   MOBILE APP     │         │   BACKEND API        │    │
│  │   (Flutter)      │◄───────►│   (Go + Gin)         │    │
│  │                  │  REST   │                      │    │
│  │  • BLoC Pattern  │  JSON   │  • JWT Auth          │    │
│  │  • Geolocation   │         │  • PostGIS Queries   │    │
│  │  • Health Diary  │         │  • CRUD Operations   │    │
│  │  • Digital Card  │         │  • Data Validation   │    │
│  └──────────────────┘         └──────────────────────┘    │
│                                         │                  │
│                                         │ SQL              │
│                                         ▼                  │
│                              ┌──────────────────────┐     │
│                              │   DATABASE           │     │
│                              │   PostgreSQL + PostGIS│    │
│                              │                      │     │
│                              │  • Users             │     │
│                              │  • Health Entries    │     │
│                              │  • Bathrooms (Geo)   │     │
│                              │  • Ratings           │     │
│                              └──────────────────────┘     │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Componentes Principais

| Camada | Tecnologia | Responsabilidade |
|---|---|---|
| **Frontend Mobile** | Flutter 3.x + Dart 3.x | Interface nativa iOS/Android, BLoC state management |
| **Backend API** | Go 1.21+ + Gin Gonic | API REST, autenticação JWT, lógica de negócio |
| **Banco de Dados** | PostgreSQL 14+ | Dados relacionais, ACID compliance |
| **Geolocalização** | PostGIS | Queries geoespaciais, radius search, proximity |
| **Autenticação** | JWT + Bcrypt | Tokens seguros, hashing de senhas |
| **Comunicação** | HTTP/REST + JSON | Protocolo padrão, sem dependências proprietárias |

### Princípios Arquiteturais

- ✅ **Desacoplamento**: Frontend e Backend independentes
- ✅ **Escalabilidade**: Arquitetura preparada para crescimento
- ✅ **Segurança**: Autenticação proprietária, dados criptografados
- ✅ **Performance**: Go para alta concorrência, Flutter para UX fluida
- ✅ **Soberania de Dados**: Infraestrutura própria, sem dependências de terceiros
- ✅ **Clean Architecture**: Separação clara de responsabilidades

---

## 📂 Repositórios Principais

| Projeto | Descrição | Stack | Status |
| :--- | :--- | :--- | :--- |
| [**vivalivre-app**](https://github.com/VivaLivre/vivalivre-app) | Aplicativo mobile nativo com geolocalização, diário de saúde e mapa colaborativo. | Flutter/Dart + BLoC | ✅ Ativo |
| [**vivalivre-backend**](https://github.com/VivaLivre/vivalivre-backend) | API REST robusta com autenticação JWT, PostGIS e CRUD de dados. | Go + Gin Gonic + PostgreSQL | ✅ Ativo |
| [**.github**](https://github.com/VivaLivre/.github) | Documentação central, visão do projeto e recursos compartilhados. | Markdown | ✅ Ativo |

### Como Começar

**Para Desenvolvedores:**
1. Clone [vivalivre-app](https://github.com/VivaLivre/vivalivre-app) — Siga o README para setup local
2. Clone [vivalivre-backend](https://github.com/VivaLivre/vivalivre-backend) — Configure PostgreSQL e PostGIS
3. Leia [AGENTS.md](https://github.com/VivaLivre/vivalivre-app/blob/develop/AGENTS.md) — Entenda os papéis e workflows

**Para Contribuidores:**
- Faça um fork de qualquer repositório
- Crie uma branch a partir de `develop`: `git checkout -b feat/sua-feature`
- Siga os padrões de código e commits semânticos
- Abra um Pull Request para revisão

---

## ✨ Funcionalidades Principais

### 🚨 Botão de Emergência
Localiza o banheiro mais próximo e bem avaliado em um toque, com integração de rotas e navegação GPS.

### 🗺️ Mapa Colaborativo
- Busca de banheiros adaptados via geolocalização avançada (PostGIS)
- Filtros por tipo de adaptação e avaliação
- Contribuição comunitária: adicionar novos banheiros
- Atualização de informações em tempo real

### 🩺 Diário de Saúde
- Registo diário de sintomas e evacuações
- Rastreamento de humor e bem-estar
- Histórico completo com timestamps
- Sincronização automática com backend

### 🪪 Cartão Digital DII
- Validação visual rápida para uso em filas
- Acesso a banheiros preferenciais
- Informações médicas essenciais
- Sem necessidade de documento físico

### 📊 Relatórios e Análises
- Exportação de histórico em PDF
- Gráficos de padrões de sintomas
- Relatórios para profissionais de saúde
- Análise de tendências ao longo do tempo

---

## 🔄 Fluxo de Desenvolvimento

```
Feature Request
    ↓
Design & Planning (@Architect)
    ↓
Backend Implementation (@Backend)
    ↓
Frontend Implementation (@Coder)
    ↓
Testing & QA (@TestEngineer)
    ↓
Code Review (@Reviewer)
    ↓
Merge to develop
    ↓
Release & Deploy (@DevOps)
```

Veja [AGENTS.md](https://github.com/VivaLivre/vivalivre-app/blob/develop/AGENTS.md) para detalhes completos sobre papéis e responsabilidades.

---

## 📊 Estatísticas do Projeto

- **Linguagens**: Flutter/Dart, Go, SQL
- **Padrões**: Clean Architecture, BLoC, REST API
- **Banco de Dados**: PostgreSQL com PostGIS
- **Autenticação**: JWT proprietário
- **Testes**: Unitários, Widget, Integração
- **CI/CD**: GitHub Actions

---

## 🤝 Como Contribuir

Contribuições são muito bem-vindas! Siga os passos:

1. **Faça um fork** do repositório desejado
2. **Crie uma branch** a partir de `develop`:
   ```bash
   git checkout develop
   git pull origin develop
   git checkout -b feat/sua-feature
   ```

3. **Faça suas alterações** seguindo os padrões do projeto
4. **Commit com mensagens semânticas**:
   ```bash
   git commit -m "feat(health): add symptom tracking"
   git commit -m "fix(auth): handle token expiration"
   ```

5. **Envie para seu fork**:
   ```bash
   git push origin feat/sua-feature
   ```

6. **Abra um Pull Request** para `develop`

### Padrões de Contribuição

- ✅ Código limpo e bem documentado
- ✅ Testes unitários (cobertura ≥ 70%)
- ✅ Commits semânticos (feat:, fix:, refactor:, docs:)
- ✅ Sem hard-coded strings ou secrets
- ✅ Responsivo e acessível (mobile)
- ✅ Dark mode suportado

---

## 📚 Documentação

- **[vivalivre-app README](https://github.com/VivaLivre/vivalivre-app/blob/develop/README.md)** — Guia do aplicativo mobile
- **[vivalivre-backend README](https://github.com/VivaLivre/vivalivre-backend/blob/develop/README.md)** — Guia da API REST
- **[AGENTS.md](https://github.com/VivaLivre/vivalivre-app/blob/develop/AGENTS.md)** — Definição de papéis e workflows
- **[CONTRIBUTING.md](https://github.com/VivaLivre/vivalivre-app/blob/develop/CONTRIBUTING.md)** — Guia de contribuição

---

## 👨‍💻 Desenvolvedor Principal

Este ecossistema foi idealizado e desenvolvido por **Gabriel José de Souza**.

- 🎓 Estudante de Análise e Desenvolvimento de Sistemas (USCS)
- 🛠️ Experiência técnica em Eletrônica (ETEC) e Qualidade (White Belt 5s)
- 🎯 Foco em tornar-se um Desenvolvedor Full-Stack focado em soluções que impactam vidas
- 💙 Comprometido com a comunidade DII brasileira

<p align="left">
  <a href="https://www.linkedin.com/in/gjds/">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <a href="https://github.com/gabrieljose2004">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
  </a>
</p>

---

## 📞 Suporte e Comunidade

- **Issues**: Abra uma issue em qualquer repositório
- **Discussões**: Participe das discussões no GitHub
- **Email**: [contato@vivalivre.com](mailto:contato@vivalivre.com)

---

## 📄 Licença

Todos os repositórios VivaLivre estão sob a licença **MIT**. Veja o arquivo LICENSE em cada repositório para detalhes.

---

<p align="center">
  <strong>Feito com 💙 para a comunidade DII brasileira</strong>
</p>

<p align="center">
  <i>"Toda pessoa com DII merece viver com liberdade e dignidade."</i>
</p>

<p align="center">
  <a href="#-vivalivre--acessibilidade-e-dignidade-em-suas-mãos">⬆ Voltar ao topo</a>
</p>
