# Projeto: Huddle Landing Page

Esse projeto é uma página inicial do **Huddle**, e mesmo sendo visualmente simples, me ensinou bastante sobre detalhes finos do CSS, como sombras, bordas e comportamento de ícones. 😁💜

---

## 💡 Desafios encontrados e como resolvi

Durante esse projeto, enfrentei alguns desafios que me ensinaram bastante sobre comportamento de elementos no CSS:

### 1. Linha fantasma embaixo dos ícones

Apareceu uma linha esquisita embaixo dos ícones Font Awesome. No começo, tentei resolver colocando `text-decoration: none;` direto na tag `<i>`, mas não funcionava.  
Depois percebi que o problema estava no link (`<a>`) que envolve o ícone.  
💡 **Solução**: apliquei `text-decoration: none;` no seletor da âncora (`a`), e aí funcionou certinho!

```css
.social a {
  text-decoration: none;
}
```

---

### 2. Hover não aplicava na borda

Eu queria mudar a cor da borda no `:hover`, tipo assim:

```css
:hover {
  color: var(--cor-do-button);
  border: 1px solid var(--cor-do-botton);
}
```

Mas o hover só mudava a cor do ícone e não da borda. Tentei de várias formas, até que percebi que a borda estava sendo aplicada no lugar errado.  
💡 **Solução**: movi a borda para dentro do seletor do `<i>` (ícone), e o hover passou a funcionar como eu queria.

```css
.social a i {
  border: 1px solid #fff;
  border-radius: 50%;
}

.social a:hover .fa-brands {
  color: var(--cor-do-botton);
  border: 1px solid var(--cor-do-botton);
}
```

---

### 3. Encontrar o valor ideal do box-shadow

Outro desafio que superei foi encontrar o valor ideal para o `box-shadow`. Eu testei várias combinações até chegar numa sombra suave que combinasse com o design e não ficasse exagerada nem muito fraca.  

💡 **Solução**: ajustei manualmente os valores até encontrar um equilíbrio legal entre **desfoque**, **espalhamento** e **cor**. Isso me ajudou a entender melhor como cada valor do `box-shadow` influencia o visual final.

```css
box-shadow: 5px 5px 10px rgba(0,0,0,0.2);
```

---
