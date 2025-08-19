# Travelgram - Perfil de Viagens

## Descrição
Projeto de estudo aplicando conceitos fundamentais de CSS moderno: **container**, **flexbox** e **variáveis CSS**. O Travelgram é uma página de perfil de viagens que demonstra boas práticas de layout responsivo e organização de código CSS.

![Image](https://github.com/user-attachments/assets/e1f6cbb3-152b-4ac0-9b0e-056549f2c7c3)

## Conceitos Aplicados

### 1. **Container (Contêiner)**
O projeto utiliza o conceito de container para centralizar e limitar a largura do conteúdo:

```css
.container {
    padding-inline: 32px;
    max-width: 1280px;
    margin-inline: auto;
}
```

**Características:**
- **Largura máxima**: `max-width: 1280px` para limitar o conteúdo em telas grandes
- **Centralização**: `margin-inline: auto` para centralizar o container
- **Padding lateral**: `padding-inline: 32px` para espaçamento interno consistente
- **Aplicação**: Utilizado em `nav`, `header`, `main` e `footer`

### 2. **Flexbox**
Implementação extensiva do Flexbox para layouts flexíveis e responsivos:

#### **Navegação (nav.css)**
```css
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

nav ul {
    display: flex;
    align-items: center;
    gap: 24px;
}
```

#### **Header (header.css)**
```css
header .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

#profile {
    display: flex;
    align-items: center;
    gap: 32px;
}

#info {
    display: flex;
    flex-direction: column;
    gap: 16px;
}
```

#### **Main (main.css)**
```css
main {
    display: flex;
    flex-wrap: wrap;
    gap: 24px;
}
```

#### **Footer (footer.css)**
```css
footer {
    display: flex;
    gap: 24px;
}

footer span:nth-child(1) {
   margin-right: auto;
}
```

**Propriedades Flexbox utilizadas:**
- `display: flex` - Ativa o flexbox
- `justify-content` - Alinhamento horizontal (space-between, center)
- `align-items` - Alinhamento vertical (center)
- `flex-direction` - Direção dos itens (column)
- `flex-wrap` - Quebra de linha (wrap)
- `gap` - Espaçamento entre itens
- `margin-right: auto` - Empurra elementos para a direita

### 3. **Variáveis CSS (Custom Properties)**
Sistema robusto de variáveis para manter consistência no design:

```css
:root {
    /* Cores */
    --brand-color: #EF5F4C;
    --surface-color: #F5F5F5;
    --text-color-primary: #313131;
    --text-color-secondary: #6C6C6C;
    
    /* Tipografia */
    --font-family: "Poppins", sans-serif;
    --text-lg: bold 32px/125% var(--font-family);
    --text: 16px/1.5 var(--font-family);
    --text-md: 14px/170% var(--font-family);
    --text-sm: 12px/170% var(--font-family);
}
```

**Vantagens das variáveis:**
- **Consistência**: Mesmas cores e tipografias em todo o projeto
- **Manutenibilidade**: Alterações centralizadas
- **Reutilização**: Aplicação em múltiplos elementos
- **Organização**: Separação clara entre cores, tipografia e espaçamentos

## Estrutura do Projeto

```
Perfil de viagem/
├── assets/
│   ├── icon/          # Ícones SVG
│   ├── images/        # Imagens das viagens
│   ├── logo.svg       # Logo do projeto
│   └── profile-pic.jpg # Foto de perfil
├── styles/
│   ├── global.css     # Variáveis e estilos globais
│   ├── nav.css        # Estilos da navegação
│   ├── header.css     # Estilos do cabeçalho
│   ├── main.css       # Estilos do conteúdo principal
│   └── footer.css     # Estilos do rodapé
└── index.html         # Estrutura HTML
```

## Características do Design

- **Grid de imagens** flexível usando flexbox
- **Navegação horizontal** com espaçamento consistente
- **Perfil de usuário** com informações organizadas
- **Tipografia hierárquica** usando variáveis CSS
- **Paleta de cores** consistente e acessível

## Como Executar

1. Clone o repositório
2. Abra o arquivo `index.html` em um navegador
3. Ou use um servidor local para desenvolvimento

## Aprendizados

Este projeto demonstra:
- **Organização de código CSS** em módulos
- **Uso eficiente do Flexbox** para layouts complexos
- **Implementação de variáveis CSS** para design systems
- **Estrutura semântica HTML** com CSS modular
- **Responsividade** através de containers e flexbox

## Próximos Passos

- Implementar media queries para responsividade mobile
- Adicionar animações CSS
- Implementar dark mode usando variáveis CSS
- Adicionar interatividade com JavaScript
