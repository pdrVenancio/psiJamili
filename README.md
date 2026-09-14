# Landing Page — Jamili Naely Ferreira | Psicóloga

Landing page em página única (React + Vite + Tailwind CSS), com navbar fixa,
animações leves ao rolar (framer-motion) e botão flutuante de WhatsApp.

## Stack

- React 19 + Vite
- Tailwind CSS v4
- framer-motion (animações de entrada ao rolar a página)
- react-icons (ícones do WhatsApp, Instagram e e-mail)

## Como executar

Pré-requisito: [Node.js](https://nodejs.org/) 18 ou superior instalado.

```bash
# 1. Entrar na pasta do projeto
cd psi-jamili-landing

# 2. Instalar as dependências
npm install

# 3. Rodar em modo desenvolvimento
npm run dev
```

O terminal vai mostrar um endereço local (geralmente `http://localhost:5173`).
Abra esse endereço no navegador.

### Gerar versão de produção

```bash
npm run build
```

Os arquivos finais (prontos para hospedar em qualquer serviço estático —
Vercel, Netlify, Hostinger etc.) ficam na pasta `dist/`.

Para conferir o resultado do build localmente antes de publicar:

```bash
npm run preview
```

## Onde editar os textos

**Todo o conteúdo textual do site fica em um único arquivo:**

```
src/data/content.json
```

Basta abrir esse arquivo, alterar o texto desejado (nome, textos das seções,
perguntas do FAQ, links de contato etc.) e salvar. A página é atualizada
automaticamente — não é necessário mexer em nenhum componente `.jsx`.

## Onde colocar as imagens

As imagens ficam na pasta `public/images/`. Atualmente há placeholders
(`hero.svg`, `diferencial.svg`, `atendimento.svg`) só para ocupar o espaço
visualmente — substitua os arquivos por fotos reais mantendo o mesmo nome, ou
adicione o arquivo novo e ajuste o caminho no campo `"imagem"` correspondente
dentro de `src/data/content.json`.

## Estrutura do projeto

```
src/
  data/
    content.json        → todos os textos do site (editar aqui)
  components/
    Navbar.jsx           → menu fixo com links âncora
    Hero.jsx              → seção inicial
    Diferencial.jsx       → seção "Qual meu diferencial?"
    Atendimento.jsx       → seção "Como serão nossos encontros?"
    Faq.jsx                → perguntas frequentes (lista simples)
    Contato.jsx            → seção final + rodapé (WhatsApp, Instagram, e-mail)
    WhatsAppButton.jsx     → botão flutuante fixo, sempre visível
    Reveal.jsx              → wrapper de animação (fade + slide ao entrar na tela)
public/
  images/                → imagens do site (placeholders inclusos)
```

## Pendências para o próximo passo

- Substituir as imagens placeholder pelas fotos reais.
- Integração com a API do Instagram para exibir posts (mencionada em
  conversa anterior, ainda não implementada nesta versão).
