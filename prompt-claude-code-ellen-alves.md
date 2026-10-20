# Prompt para o Claude Code — Landing page Ellen Álves (Hipnoterapia / Ansiedade)

> **Como usar:** crie uma pasta para o projeto, coloque dentro dela uma subpasta `fotos/` com `ellen-hero.jpg` (foto principal) e `ellen-sobre.jpg` (foto da seção "Quem vai te atender") e `consultorio.jpg` (foto do consultório). Abra o Claude Code nessa pasta, cole o prompt abaixo e, se possível, anexe os prints das seções da página de referência e a arte da Ellen (para a paleta).

---

## PROMPT (copie daqui para baixo)

Crie uma landing page de uma página só, em **um único arquivo `index.html`**, com todo o CSS dentro de uma tag `<style>` e o pouco JavaScript necessário dentro de uma tag `<script>` no próprio arquivo. Sem React, sem Tailwind, sem build, sem dependências, exceto as fontes do Google Fonts. As imagens ficam na pasta `fotos/`.

### 1. Referência obrigatória

Modele a página a partir de: **https://facaterapia.com.br/andrezagalceron**

Acesse a URL, leia o HTML e o CSS e use a página como molde. Siga a referência apenas na ordem das seções e nos textos. Nos demais pontos abaixo, a identidade visual definida a seguir tem prioridade:
- blocos e seções, na mesma ordem;
- layout de cada seção (colunas, alinhamentos, larguras, espaçamentos, raios de borda, sombras);
- tipografia: **Playfair Display** nos títulos (com o trecho final em *itálico* e cor de destaque) e **Poppins** no corpo, botões, etiquetas e números pequenos. Mesmos tamanhos, pesos e entrelinhas;
- componentes: etiquetas em pílula com bolinha antes do texto e letras maiúsculas espaçadas, botões arredondados (pill), ícones de check em círculo, card flutuante sobre a foto do hero, cards de depoimento, accordion do FAQ.

**Identidade visual própria (não copie o visual da referência).** Use a referência só para a ordem das seções e os textos. O visual deve ser diferente, com o conceito "respiração profunda / hipnose": um hero escuro e profundo, com anéis concêntricos que respiram lentamente atrás da foto em arco.

```
--abismo:     #0F2A33   azul-abismo: header, hero, faixa de números, depoimentos, CTA final, rodapé, card da consulta
--abismo-2:   #163A45   cards sobre o fundo escuro
--mar:        #8CC7BE   vidro-do-mar: destaques e botões sobre o escuro (texto do botão em #0F2A33)
--mar-forte:  #2F6F6A   destaques sobre o claro (itálico dos títulos, etiquetas, marcadores)
--nevoa:      #EEF3F1   fundo claro principal
--branco:     #FFFFFF   seções claras alternadas
--crepusculo: #C9B8E6   toque raro: aspas dos depoimentos e um dos anéis
--texto:      #41565C   parágrafos no claro;  #C5D6D6 parágrafos no escuro
--linha:      #D5E1DE
```

Tipografia (as mesmas fontes da página de referência): **Playfair Display** (500/600, itálico 500/600) nos títulos, nos números, nas citações dos depoimentos e nas perguntas do FAQ; **Poppins** (300/400/500/600) no texto, nos botões, nas etiquetas e no menu. Tamanhos: h1 clamp(2.5rem, 4.6vw, 4.2rem) com peso 600; h2 clamp(2rem, 3.3vw, 2.9rem) com peso 600; texto em 16px.

Layout por seção:
- Header escuro (#0F2A33) com o nome "Ellen *Álves*" à esquerda, links claros e botão em --mar.
- Hero escuro: texto à esquerda em branco, com o itálico em --mar. Foto à direita em formato de arco (border-radius 999px 999px 28px 28px, proporção 4:5,2), contorno fino em --mar a 10px de distância e 4 anéis concêntricos finos atrás, com animação "respirar" de 10s (escala de 0,94 a 1,04) desativada em prefers-reduced-motion. Card flutuante em vidro escuro (blur).
- Números integrados à base do hero, no mesmo fundo escuro, com os números em Playfair Display e cor --mar.
- "Antes de mais nada": fundo névoa, em duas colunas (título à esquerda, parágrafos à direita). A frase "É exatamente lá que a hipnoterapia atua." vira uma citação grande em itálico, com uma barra --mar à esquerda.
- Método: fundo branco; o card "Consulta Exclusiva" fica escuro (--abismo), com "1h a 1h30" grande em branco e anéis decorativos no canto.
- Marcadores das listas: um anel com um ponto no centro (sem ícone de check).
- Como funciona: fundo névoa, lista em duas colunas separada por linhas finas.
- Depoimentos: seção escura, com cards em --abismo-2, citação em Playfair Display 1,12rem e avatar com anel --mar.
- Sobre: fundo branco, com a foto também em arco (sticky no desktop) e as pílulas com fundo névoa.
- FAQ: duas colunas (título à esquerda, perguntas à direita), perguntas em Playfair Display e o "+" dentro de um círculo.
- CTA final: seção escura de ponta a ponta, com os anéis concêntricos atrás do texto centralizado e botão --mar.
- Rodapé escuro e centralizado, com o ícone do Instagram em --mar e sem borda.
- Etiquetas de seção em caixa normal (sem letras maiúsculas espaçadas), com um pequeno anel antes do texto.
- Sem animação de entrada nas seções: o único movimento automático da página são os anéis.

### 2. Regras gerais
- **Não use efeito hover em cards nem em itens que não tenham ação.** Hover só em botões, links e nas perguntas do FAQ.
- Todos os botões de agendamento abrem o WhatsApp em nova aba:
  `https://wa.me/5561991481192?text=Ol%C3%A1.%20Gostaria%20de%20agendar%20uma%20consulta%20de%20hipnoterapia.`
- Instagram: `https://www.instagram.com/ellen_hipnoterapia/`
- Header fixo no topo; rolagem suave para as âncoras compensando a altura do header.
- Animações de entrada sutis (fade + leve deslocamento ao rolar), desativadas com `prefers-reduced-motion`.
- Responsivo em 375px, 768px e 1280px. No celular, o menu vira hambúrguer.
- FAQ: só uma pergunta aberta por vez, ícone "+" que gira ao abrir.
- SEO: `lang="pt-BR"`, title "Consulta de Hipnoterapia | Ellen Álves", meta description e Open Graph com o texto do hero, meta author "Ellen Álves".
- **Não** copie o Pixel do Facebook da página de referência (é da outra profissional).

### 3. Conteúdo, seção por seção

**Header**: links Método (#metodo), Consulta (#consulta), Depoimentos (#depoimentos), Sobre (#sobre) + botão "Agendar minha consulta".

**Hero** (texto novo, promessa voltada para ansiedade):
- Etiqueta: TERAPIA BREVE
- H1: "A ansiedade é uma resposta do seu inconsciente. E ela pode ser *reorganizada.*"
- Subtítulo: "Nem a mente acelerada nem a sensação de aperto no peito são permanentes. Entenda como a hipnoterapia ajuda a reestruturar os gatilhos emocionais e abra espaço para uma vida com mais presença e tranquilidade."
- Botão: "Quero minha consulta de avaliação"
- Selos: "98% saem com clareza sobre a raiz da ansiedade" • "Método humanizado"
- Foto: `fotos/ellen-hero.jpg`, em proporção 4:5 (560 × 700 px no desktop), com a grade do hero em `minmax(0,1fr) minmax(0,560px)` e gap de 64px, para a foto acompanhar a altura do bloco de texto. Abaixo de 1180px, use colunas `1fr .9fr` com gap de 48px; no celular, a foto vai abaixo do texto com até 480px de largura, com card flutuante: "**Clareza sobre a sua ansiedade** / em uma única consulta"

**Faixa de números** (igual à referência): +1000 mulheres atendidas · +1000 consultas realizadas · 98% eficácia comprovada

**Antes de mais nada** (texto reescrito, mesmo objetivo):
- H2: "O que você sente não é *fraqueza, nem frescura.*"
- P1: "Se você já tentou respirar fundo, pensar positivo, fazer terapia, ler tudo sobre ansiedade, e mesmo assim o coração dispara, a mente acelera e o corpo trava nos mesmos momentos, essa consulta é pra você."
- P2: "A ansiedade não é falta de controle. É uma resposta automática que o seu sistema nervoso aprendeu em algum momento da sua história, e que dispara antes mesmo de você conseguir pensar."
- P3: "Por isso, só entender racionalmente não basta: a razão mora na consciência, e a origem da ansiedade está no subconsciente."
- P4: "É exatamente lá que a hipnoterapia atua."
- Botão: "Agendar consulta agora"

**Método** (#metodo, texto reescrito):
- H2: "Pessoas que estão tratando a ansiedade *pela origem.*"
- Parágrafo: "Em vez de apenas aliviar os sintomas, vamos juntas investigar o que alimenta a sua ansiedade e traçar um caminho de saída possível, respeitando a sua história e o seu ritmo. Cada ansiedade tem uma origem própria, e é ela que guia todo o processo."
- Lista com check:
  - Investigação da origem emocional da sua ansiedade
  - Reconhecimento das crenças subconscientes que mantêm o corpo em estado de alerta
  - Compreensão dos gatilhos que disparam crises, medos e preocupação excessiva
  - Avaliação honesta se a hipnoterapia é indicada para o seu momento
  - Definição do processo de ressignificação mais adequado pra você
  - Plano de próximos passos feito sob medida
- Card "CONSULTA EXCLUSIVA": "1h a 1h30" / "de atendimento individual, olho no olho, sobre a origem da sua ansiedade." / Formato: Online e presencial · Resultados: 98% comprovados · Indicado: Ansiedade e equilíbrio emocional · Vagas: Limitadas por mês / botão "Quero minha consulta"

**Como funciona** (#consulta, idêntico à referência):
- H2: "Consulta de Avaliação *em hipnoterapia*"
- Subtítulo: "Tudo o que você precisa pra sair desse ciclo com clareza e um caminho real pela frente."
- 8 itens em 2 colunas: Consulta de 1h a 1h30 · Anamnese aprofundada da sua história · Identificação da origem subconsciente do padrão · Avaliação clínica honesta · Direcionamento com um plano 100% personalizado · Espaço reservado pras suas dúvidas · 98% de eficácia comprovada · Sem fórmula genérica
- Botão: "Agendar minha consulta"

**Local de atendimento** (#local, nova seção logo antes dos Depoimentos, fundo branco):
- Duas colunas: à esquerda, a foto `fotos/consultorio.jpg` (proporção 3:2, canto superior esquerdo bem arredondado, 200px, e os outros com 28px), com uma etiqueta escura sobre a foto: ícone de pino + "Brasília · DF". À direita, o texto.
- Etiqueta: "Local de atendimento"
- H2: "Um espaço pensado para você *desacelerar.*"
- Parágrafo: "Os atendimentos presenciais acontecem em Brasília, num consultório tranquilo, reservado e acolhedor, preparado para que você se sinta à vontade desde o primeiro momento."
- Lista com linhas finas: (pino) **Brasília – DF**: "Endereço em definição. O local exato é informado no agendamento." / (monitor) **Atendimento online**: "Com o mesmo cuidado e sigilo do presencial."
- Botão: "Agendar minha consulta"
- No celular, a foto vai acima do texto.

**Depoimentos** (#depoimentos, mesma estrutura da referência, mantendo a linha "RELATOS ILUSTRATIVOS — CONTEÚDO TEMPORÁRIO"):
- H2: "Pessoas que saíram do ciclo, *de verdade.*"
- Subtítulo: "Veja como essas pessoas encontraram clareza e saíram dos padrões que as prendiam."
- 3 cards, cada um com foto redonda (48px), nome e tema em pílula:
  1. `fotos/rafael.jpg`, **Rafael Vazques** (Sobrecarga emocional): "Eu vivia no automático, dando conta de tudo e de todo mundo, menos de mim. Entendi de onde vinha essa cobrança e comecei a me tratar com mais leveza."
  2. `fotos/leticia.jpg`, **Letícia Ferreira** (Transtorno de ansiedade generalizada): "Passei 5 anos refém da ansiedade e achava que era normal viver no limite o tempo todo. Descobri a raiz emocional disso depois que me consultei com a Ellen e hoje enxergo tudo diferente."
  3. `fotos/olga.jpg`, **Olga Azevedo** (Ansiedade): "A ansiedade tomava conta do meu dia. Depois da consulta com a Ellen, entendi o que estava por trás dela e comecei a recuperar minha paz."
- Botão: "Quero minha consulta de avaliação"

**Quem vai te atender** (#sobre, mesma estrutura, texto novo):
- Foto: `fotos/ellen-sobre.jpg`
- H2: "Sou Ellen Álves, *hipnoterapeuta.*"
- Parágrafos (exatamente estes):
  1. "Sou Ellen Álves, hipnoterapeuta, com atuação especializada em ansiedade, e há mais de 10 anos venho me dedicando ao estudo e à prática de abordagens voltadas ao cuidado integral do ser humano."
  2. "Minha trajetória no universo holístico começou pelo interesse em compreender a relação entre mente, emoções, comportamentos e bem-estar. Ao longo desses anos, aprofundei meus conhecimentos em diferentes práticas integrativas, construindo uma visão cada vez mais ampla e individualizada sobre o cuidado."
  3. "Foi a partir dessa experiência que a hipnoterapia passou a ocupar um lugar central no meu trabalho. A hipnose possibilita um olhar direcionado aos padrões emocionais e comportamentais, permitindo trabalhar questões de forma personalizada, respeitando a história e as necessidades de cada pessoa."
  4. "Hoje, uno minha formação em hipnoterapia à experiência construída ao longo desses anos no campo das práticas holísticas e integrativas. Quando adequado a cada caso, diferentes recursos complementares podem fazer parte da abordagem."
  5. "Meu propósito é oferecer um espaço de acolhimento, escuta, respeito e autoconhecimento, onde cada pessoa possa ser compreendida para além do seu sintoma."
- Pílulas: Hipnoterapeuta Clínica · Atendimento online e presencial · Especialista em ansiedade
- Botão "Quero minha consulta de avaliação" + botão redondo com ícone do Instagram

**FAQ**: exatamente igual à referência (mesmas 6 perguntas e respostas).

**CTA final**: etiqueta "Vagas limitadas por mês", H2 "Quebrar ciclos repetitivos começa quando você finalmente entende *de onde eles vêm.*", parágrafo: "Marque sua Consulta de Avaliação e descubra, com clareza, a raiz do padrão que te mantém presa. Comece hoje." e botão "Agendar minha consulta".

**Rodapé**: botão do Instagram, links Método e Perguntas **centralizados** numa linha, e abaixo, também centralizado: "© 2026 Ellen Álves — Consulta de Avaliação em Hipnoterapia".

### 4. Entrega
Ao terminar, abra o `index.html` num navegador headless (ou descreva como testar), confira desktop e celular e me diga o que ficou pendente.
