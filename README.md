# 🚀 Certificard - Imersão.Dev Alura (2021)

> **Jornada completa:** Do primeiro "Hello World" até aplicações web interativas com JavaScript, CSS Grid e integração de APIs.

![Imersão Dev](https://www.alura.com.br/assets/img/imersoes/dev-2021/logo-imersao-dev.png)

---

## 📖 Sobre o Projeto

Este repositório documenta minha participação na **Imersão Dev 2021** da [Alura](https://alura.com.br), um bootcamp intensivo de **10 dias** focado em desenvolvimento frontend com **HTML, CSS e JavaScript**.

Durante a imersão, construí **12 projetos progressivos**, evoluindo desde conceitos básicos até aplicações complexas com manipulação de DOM, APIs, lógica de jogos e sistemas de gerenciamento.

---

## 🎯 Objetivos de Aprendizado

✅ Fundamentos de **HTML5 semântico**  
✅ **CSS3** moderno (Flexbox, Grid, animações)  
✅ **JavaScript ES6+** (arrays, objetos, funções, DOM)  
✅ Integração com **APIs externas**  
✅ Lógica de programação aplicada (jogos, conversores, tabelas dinâmicas)  
✅ Design responsivo e **UX/UI básico**  

---

## 🗂️ Estrutura de Projetos

### 🟢 **Projetos Iniciais (Dias 1-3)**

#### 1️⃣ Hello World
**Tema:** Primeiro contato com HTML/CSS/JS  
**Conceitos:** Tags básicas, estilização, `alert()`, `console.log()`  
**[Ver no CodePen](https://codepen.io/Edlucaz/)** | **Melhorias futuras:** Migrar para GitHub Pages

---

#### 2️⃣ Calculadora de Média + Conversor de Temperaturas
**Tema:** Operações matemáticas e interatividade  
**Conceitos:** `prompt()`, operadores aritméticos, funções  
**Tech:** HTML, CSS, JavaScript  
**[Ver no CodePen](https://codepen.io/Edlucaz/pen/wveebNP)** 

**📈 Roadmap para v2.0 (Full-Stack):**
- [ ] Refatorar UI com **Vue 3 + Tailwind CSS**
- [ ] Backend Django REST API para salvar histórico de cálculos
- [ ] Login com Django AllAuth (usuário salva suas conversões)
- [ ] Gráficos de histórico (Chart.js ou Plotly)
- [ ] Deploy: Vercel (frontend) + Railway (backend)

---

#### 3️⃣ Conversor de Moedas v1 & v2
**Tema:** Manipulação de valores monetários  
**Conceitos:** Lógica condicional, formatação de números  
**[Ver v1 no CodePen](https://codepen.io/Edlucaz/pen/GREMvjG)** | **[Ver v2 no CodePen](https://codepen.io/Edlucaz/pen/bGRvJar)**

**📈 Roadmap para v3.0 (Full-Stack):**
- [ ] Integrar API real de cotações (**AwesomeAPI** ou **ExchangeRate-API**)
- [ ] Backend Django: cache de cotações com **Redis** (reduzir requests)
- [ ] Sistema de favoritos (usuário salva pares de moedas)
- [ ] Histórico de conversões com gráfico de tendência (30 dias)
- [ ] PWA (funciona offline com última cotação salva)
- [ ] Deploy: Vercel + Railway

---

### 🟡 **Projetos Intermediários (Dias 4-6)**

#### 4️⃣ Mentalista
**Tema:** Jogo de adivinhação  
**Conceitos:** `Math.random()`, loops, condicionais  
**[Ver no CodePen](https://codepen.io/Edlucaz/pen/ExXbyNM)**

**📈 Roadmap para v2.0 (Full-Stack):**
- [ ] Backend Django: **leaderboard global** (menores tentativas)
- [ ] Sistema de dificuldade (fácil: 1-10, médio: 1-100, hard: 1-1000)
- [ ] Multiplayer: **WebSockets** (2 jogadores competem em tempo real)
- [ ] Modo IA: algoritmo de busca binária (usuário tenta vencer a IA)
- [ ] Achievements e XP (gamificação)
- [ ] Deploy: Vercel + Railway + Redis (leaderboard)

---

#### 5️⃣ Lista de Filmes
**Tema:** Arrays e objetos  
**Conceitos:** CRUD básico, `forEach`, `map`  
**Status:** Código não fornecido (reconstruir)

**📈 Roadmap para v2.0 (Full-Stack):**
- [ ] Integrar **TMDb API** (pôsteres e detalhes reais)
- [ ] Backend Django: sistema de listas personalizadas
- [ ] Usuário pode criar múltiplas listas ("Assistir", "Favoritos", "Abandonei")
- [ ] Sistema de avaliação (1-5 estrelas) + comentários
- [ ] Social: compartilhar listas com amigos
- [ ] Deploy: Vercel + Railway + PostgreSQL

---

#### 6️⃣ WandaFlix ⭐
**Tema:** Catálogo de filmes estilo Netflix  
**Conceitos:** Manipulação de DOM, objetos complexos, layout Grid  
**[Ver no CodePen](https://codepen.io/Edlucaz/pen/jOwzQxM)**

**🔥 Roadmap para WandaFlix 2.0 (Full-Stack):**
- [ ] **Frontend:** Refatorar com **React** ou **Vue 3**
  - Componentes reutilizáveis (MovieCard, CategoryRow, SearchBar)
  - Context API ou Pinia (gerenciamento de estado)
  - React Router / Vue Router (navegação entre páginas)
  - Lazy loading de imagens (performance)

- [ ] **Backend Django REST Framework:**
  ```python
  # models.py
  class Movie(models.Model):
      title = models.CharField(max_length=200)
      poster_url = models.URLField()
      category = models.ForeignKey('Category', on_delete=models.CASCADE)
      release_year = models.IntegerField()
      rating = models.DecimalField(max_digits=3, decimal_places=1)
      
  class Category(models.Model):
      name = models.CharField(max_length=100)  # Drama, Ação, Terror, etc.
  
  class UserList(models.Model):
      user = models.ForeignKey(User, on_delete=models.CASCADE)
      movie = models.ForeignKey(Movie, on_delete=models.CASCADE)
      list_type = models.CharField(max_length=50)  # 'watchlist', 'favorites'
      added_at = models.DateTimeField(auto_now_add=True)
