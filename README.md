# 📊 Dashboard Responsivo com SASS

Dashboard moderno e totalmente responsivo construído para demonstrar domínio avançado de **SASS/SCSS** e arquitetura CSS escalável.

<img width="1916" height="825" alt="image" src="https://github.com/user-attachments/assets/885a11c9-75a1-4752-954f-538b0a44bbb6" />


## 🚀 Demonstração

- **Desktop:** Layout completo com sidebar fixa, 4 cards de métricas e tabela de transações
- **Mobile:** Cards empilhados e menu hamburger
- **Tablet:** Layout intermediário com 2 colunas de cards

| Desktop | Mobile |
|---------|--------|
| <img width="1916" height="825" alt="image" src="https://github.com/user-attachments/assets/885a11c9-75a1-4752-954f-538b0a44bbb6" /> | <img width="753" height="831" alt="image" src="https://github.com/user-attachments/assets/18fac941-2abe-4e51-8aec-957a31b6e79d" />
 |

## 💡 Sobre o Projeto

Este projeto foi desenvolvido como estudo aprofundado de **SASS/SCSS**, aplicando conceitos avançados e padrões utilizados no mercado de trabalho. O foco principal foi criar uma arquitetura CSS escalável, reutilizável e de fácil manutenção.

## 🎯 Funcionalidades

- ✅ **Design System completo** com tokens de cores, espaçamentos e tipografia
- ✅ **Grid responsivo** que adapta de 1 → 2 → 4 colunas
- ✅ **Sidebar responsiva** (escondida no mobile, fixa no desktop)
- ✅ **Cards de métricas** com cores e ícones diferenciados
- ✅ **Tabela de transações**
- ✅ **Badges de status** coloridos (Pago, Pendente, Cancelado)
- ✅ **Hamburger menu** no mobile
- ✅ **Hover effects** em links, tabelas e cards
- ✅ **Mobile-first** approach

## 🛠️ Tecnologias

- **SASS/SCSS** - Pré-processador CSS
- **Arquitetura 7-1 Pattern** - Organização de arquivos
- **BEM Methodology** - Nomenclatura de classes
- **Mobile-First** - Abordagem responsiva
- **CSS Grid & Flexbox** - Layout moderno

## 📂 Estrutura do Projeto

```
dashboard-sass/
├── abstracts/
│   ├── _tokens.scss          # Design tokens (cores, espaçamentos, fontes)
│   ├── _functions.scss       # Funções auxiliares (color, spacing, font-size)
│   ├── _mixins.scss          # Mixins reutilizáveis (flex, grid, respond-to)
│   └── _breakpoints.scss     # Breakpoints responsivos
│
├── components/
│   ├── _sidebar.scss         # Navegação lateral
│   ├── _header.scss          # Cabeçalho
│   ├── _metric-card.scss     # Cards de métricas
│   └── _table.scss           # Tabela de transações
│
├── layout/
│   └── _grid.scss            # Grid principal e containers
│
├── utilities/
│   └── _spacing.scss         # Classes utilitárias (mt-, pt-)
│
├── reset.css                 # Modern CSS Reset
├── style.scss                # Arquivo principal (importa tudo)
└── index.html                # HTML estrutural
```

## 🎨 Conceitos SASS Aplicados

### **1. Design Tokens (Maps)**
```scss
$colors: (
  primary: #6366f1,
  success: #10b981,
  warning: #f59e0b,
  danger: #ef4444,
  // ...
);

$spacing: (
  xs: 0.25rem,
  sm: 0.5rem,
  md: 1rem,
  // ...
);
```

### **2. Funções Auxiliares**
```scss
@function color($name) {
  @return map.get($colors, $name);
}

// Uso:
background-color: color(primary);
```

### **3. Mixins Responsivos**
```scss
@mixin grid-responsive($mobile: 1, $tablet: 2, $desktop: 4, $gap: 1rem) {
  display: grid;
  grid-template-columns: repeat($mobile, 1fr);
  gap: $gap;
  
  @include respond-to(md) {
    grid-template-columns: repeat($tablet, 1fr);
  }
  
  @include respond-to(lg) {
    grid-template-columns: repeat($desktop, 1fr);
  }
}
```

### **4. Utilities com @each**
```scss
@each $name, $size in $spacing {
  .mt-#{$name} { margin-top: $size; }
  .mb-#{$name} { margin-bottom: $size; }
  // ...
}
```

### **5. BEM Naming**
```scss
.metric-card {
  &__title { }
  &__value { }
  &--revenue { }  // Modificador
}
```

## 🎓 Aprendizados

Durante o desenvolvimento deste projeto, dominei:

- Arquitetura SASS escalável (7-1 Pattern)
- Design tokens e sistemas de design
- Funções e mixins reutilizáveis
- Loops e automação (@each, @if)
- Grid responsivo com múltiplos breakpoints
- BEM methodology
- Mobile-first approach
- Organização de código para trabalho em equipe

## 🚀 Como Executar

```bash
# 1. Clone o repositório
git clone https://github.com/AlysoonFelipeeDev/dashboard-sass.git

# 2. Entre na pasta
cd dashboard-sass

# 3. Instale as dependências (se usar npm)
npm install

# 4. Compile o SASS
sass --watch style.scss:style.css

# 5. Abra o index.html no navegador
```

## 📱 Responsividade

### Breakpoints utilizados:
- **Mobile:** < 768px (1 coluna)
- **Tablet:** ≥ 768px (2 colunas)
- **Desktop:** ≥ 1024px (4 colunas, sidebar fixa)

<img width="812" height="744" alt="image" src="https://github.com/user-attachments/assets/e0dbbbc2-af9e-4691-8c0c-7ae854f81e21" />


## 📝 Licença

Este projeto está sob a licença MIT.

## 👤 Autor

**Alyson Felipe**

- GitHub: [@AlysoonFelipeeDev](https://github.com/AlysoonFelipeeDev)
- LinkedIn: [Seu LinkedIn](https://www.linkedin.com/in/alysonozorio/)

---

⭐ Se este projeto te ajudou, deixe uma estrela!
