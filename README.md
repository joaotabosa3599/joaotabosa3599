<div align="center">

<a href="https://portfolio-orcin-nine-x51rqo3inw.vercel.app">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/banner-light.svg">
  <img src="assets/banner.svg" alt="João Tabosa, Full Stack Developer. Construo aplicações web do banco de dados à interface." width="100%">
</picture>
</a>

<br>

[![Portfólio](https://img.shields.io/badge/Portf%C3%B3lio-7F5AF5?style=for-the-badge&logo=googlechrome&logoColor=white)](https://portfolio-orcin-nine-x51rqo3inw.vercel.app) [![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/joaotabosa/) [![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/j_pedro32k) [![E-mail](https://img.shields.io/badge/E--mail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:joao.tabosa3599@gmail.com)

</div>

<br>

## Projetos

<a href="https://liquid-journal-trading-app.vercel.app">
  <img src="assets/debrief.svg" alt="Debrief, diário de trading com análise de performance. Opere com dados, evolua com evidências." width="100%">
</a>

<div align="center">

[![Abrir o app](https://img.shields.io/badge/Abrir_o_app-2563EB?style=for-the-badge&logo=vercel&logoColor=white)](https://liquid-journal-trading-app.vercel.app) &nbsp; ![Status](https://img.shields.io/badge/Produto_comercial-reposit%C3%B3rio_privado-12161E?style=for-the-badge&labelColor=0D1017) &nbsp; ![Beta](https://img.shields.io/badge/Gr%C3%A1tis_em_beta-sem_cart%C3%A3o-22C55E?style=for-the-badge&labelColor=0D1017)

</div>

**Debrief** é um SaaS onde traders registram cada operação com o contexto que justificou
a entrada e descobrem, nos próprios números, o que funciona no seu operacional.
Contas em BRL, USD e EUR com cotação ao vivo, calculadora de resultado com câmbio
embutido, prints e notas em cada trade, tags por estratégia, calendário de PNL,
feedback de IA sobre o histórico, exportação em PDF e notificações push.

**Stack**

![Next.js 16](https://img.shields.io/badge/Next.js_16-000000?style=flat-square&logo=nextdotjs&logoColor=white) ![React 19](https://img.shields.io/badge/React_19-149ECA?style=flat-square&logo=react&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Tailwind CSS 4](https://img.shields.io/badge/Tailwind_CSS_4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) ![shadcn/ui](https://img.shields.io/badge/shadcn%2Fui-000000?style=flat-square&logo=shadcnui&logoColor=white) ![ECharts](https://img.shields.io/badge/ECharts-AA344D?style=flat-square&logo=apacheecharts&logoColor=white) ![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white) ![GSAP](https://img.shields.io/badge/GSAP-88CE02?style=flat-square&logo=greensock&logoColor=white) ![Framer Motion](https://img.shields.io/badge/Framer_Motion-0055FF?style=flat-square&logo=framer&logoColor=white) ![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![Claude API](https://img.shields.io/badge/Claude_API-D97757?style=flat-square&logo=anthropic&logoColor=white) ![Web Push](https://img.shields.io/badge/Web_Push-5A0FC8?style=flat-square&logo=pwa&logoColor=white) ![jsPDF](https://img.shields.io/badge/jsPDF-E5484D?style=flat-square) ![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)

**Destaques técnicos**

- **Trades monitorados ao vivo:** um `pg_cron` roda a cada minuto, confere as velas
  de 1 minuto e, se o preço tocou o stop ou o alvo, fecha a operação no nível,
  calcula o resultado na moeda da conta e avisa por push.
- **Sem service role no job:** a rotina lê e grava por funções do banco travadas
  por um segredo, e o resto do app vive sob Row Level Security.
- **Cena 3D no topo da página inicial**, com React Three Fiber e o scroll
  coreografado em GSAP.
- **Português e inglês**, com rotas por idioma e troca de idioma no app.
- **Calendário econômico do TradingView** (FOMC, CPI, NFP) dentro do dashboard e
  exportação da conta em PDF e CSV.

> [!NOTE]
> Produto comercial em desenvolvimento, por isso o repositório é privado.
> O app está no ar e aberto para uso. Antes se chamava Liquid Journal.

<details open>
<summary><b>Registro de um trade, do ativo ao PNL</b> · GIF de 27s</summary>

<br>

<img src="assets/debrief-demo.gif" alt="Demonstração: no dashboard do Debrief, um trade em XAUUSD é importado pelo buscador de ativos, a calculadora estima o PNL em dólar, o print do gráfico e as notas são anexados, e ao salvar os indicadores e a curva de patrimônio se atualizam." width="100%">

<p align="center"><sub>Buscar o ativo · informar entrada e saída · a calculadora fecha o PNL na moeda da conta · anexar o print e as notas · salvar e ver o dashboard se atualizar</sub></p>

</details>

<details>
<summary><b>Como ele é montado</b></summary>

<br>

```mermaid
%%{init: {"theme": "base", "themeVariables": {
  "fontFamily": "-apple-system, Segoe UI, Helvetica, Arial, sans-serif",
  "primaryColor": "#12161e", "primaryTextColor": "#f3f4f6", "primaryBorderColor": "#273040",
  "lineColor": "#2563eb", "edgeLabelBackground": "#0d1017", "clusterBkg": "#0d1017"
}}}%%
flowchart LR
    U([Trader]) --> APP["Next.js App Router<br/>React · Tailwind · ECharts"]
    APP --> SA["Server Actions<br/>e Route Handlers"]
    SA --> AUTH["Supabase Auth<br/>e-mail e Google"]
    SA --> DB[("PostgreSQL<br/>Row Level Security")]
    SA --> ST["Supabase Storage<br/>prints dos trades"]
    SA --> FX["API de câmbio<br/>BRL, USD, EUR"]
    SA --> AI["Claude API<br/>feedback de performance"]
    SA --> PUSH["Web Push<br/>notificações"]

    classDef user fill:#12161e,stroke:#9ca3af,color:#f3f4f6
    classDef app fill:#2563eb,stroke:#60a5fa,color:#fff
    classDef data fill:#14532d,stroke:#22c55e,color:#fff
    classDef ext fill:#1a1f29,stroke:#64748b,color:#f3f4f6
    class U user
    class APP,SA app
    class DB,AUTH,ST data
    class FX,AI,PUSH ext
```

Cada trader só enxerga as próprias operações, e isso é garantido no banco
por Row Level Security — não por uma checagem na aplicação que alguém possa
esquecer de escrever.

</details>

<br>

<img src="assets/constela-orion.svg" alt="Constela & Órion, plataforma de estudos gamificada em pixel art. Estudar vira jogo. Cada dia, uma estrela." width="100%">

<div align="center">

![Abrir o app em breve](https://img.shields.io/badge/Abrir_o_app-em_breve-4B5563?style=for-the-badge&logo=vercel&logoColor=white&labelColor=0D1017) &nbsp; ![Status](https://img.shields.io/badge/Projeto_pessoal-reposit%C3%B3rio_privado-12161E?style=for-the-badge&labelColor=0D1017) &nbsp; ![Universos](https://img.shields.io/badge/Dois_universos-Constela_e_%C3%93rion-ED83B2?style=for-the-badge&labelColor=0D1017) &nbsp; ![Testes](https://img.shields.io/badge/293_testes-Vitest-6E9F18?style=for-the-badge&labelColor=0D1017)

</div>

**Constela & Órion** é uma plataforma de estudos gamificada em pixel art. Agenda
semanal com arrastar e soltar, edital com o progresso de cada assunto, quizzes
com explicação, simulados no tempo da prova e flashcards com repetição espaçada
(FSRS). São dois universos trocáveis, cada um com mascote, paleta e céu animado
próprios, a abelhinha Constela e o Ori, o axolote. Tudo funciona sem internet e
sincroniza com a conta quando ela existe. XP e conquistas premiam a constância
sem punir o dia perdido.

**Stack**

![Next.js 16](https://img.shields.io/badge/Next.js_16-000000?style=flat-square&logo=nextdotjs&logoColor=white) ![React 19](https://img.shields.io/badge/React_19-149ECA?style=flat-square&logo=react&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Tailwind CSS 4](https://img.shields.io/badge/Tailwind_CSS_4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) ![Zustand](https://img.shields.io/badge/Zustand-453F39?style=flat-square) ![IndexedDB](https://img.shields.io/badge/IndexedDB-F59E0B?style=flat-square) ![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![FSRS-6](https://img.shields.io/badge/FSRS--6-ED83B2?style=flat-square) ![Canvas 2D](https://img.shields.io/badge/Canvas_2D-E34F26?style=flat-square&logo=html5&logoColor=white) ![Web Audio](https://img.shields.io/badge/Web_Audio-5B9BFF?style=flat-square) ![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white) ![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)

**Destaques técnicos**

- **Local-first:** cada tela lê e grava no aparelho (Zustand e IndexedDB) e
  funciona offline; com conta, um motor próprio sincroniza com o Supabase em
  segundo plano, sem nunca misturar dados de contas diferentes.
- **Motor de partículas em Canvas 2D**, um por universo: pétalas, estrelas
  cadentes, vagalumes e constelações que se desenham, pausado fora da tela e
  parado com movimento reduzido.
- **Intro de jogo** em game loop, com hit-stop e efeitos sonoros sintetizados na
  hora em Web Audio, sem arquivos de áudio.
- **Temas trocados por CSS**, sem piscar na hidratação, e o mascote "repinta" o
  site a partir de onde está com a View Transitions API.
- **JavaScript enxuto:** sem bibliotecas de animação nem de gráfico, com Supabase,
  formulários e abas secundárias sob demanda (35% a 61% menos JS por tela).

> [!NOTE]
> Ainda não publicado: o app ganha domínio próprio em breve. O repositório é
> privado por ser um projeto pessoal, e o GIF abaixo é o app real, com dados de
> demonstração.

<details open>
<summary><b>Da abertura ao estudo, nos dois universos</b> · GIF de 26s</summary>

<br>

<img src="assets/constela-orion-demo.gif" alt="Demonstração: a intro do Constela & Órion, com a abelhinha e o axolote dando um toca aqui; a Constela é escolhida e prepara o app; a página inicial abre com uma constelação se desenhando no céu; no Meu Cantinho, uma sessão é concluída e rende XP e conquistas; nas Configurações, o Ori assume o controle e repinta o site no universo Órion." width="100%">

<p align="center"><sub>Intro com o toca aqui · escolher o parceiro, que prepara o app · o céu da página inicial · concluir uma sessão e ganhar XP · o Ori assume o controle e repinta tudo</sub></p>

</details>

<details>
<summary><b>Como ele é montado</b></summary>

<br>

```mermaid
%%{init: {"theme": "base", "themeVariables": {
  "fontFamily": "-apple-system, Segoe UI, Helvetica, Arial, sans-serif",
  "primaryColor": "#16121d", "primaryTextColor": "#f3f4f6", "primaryBorderColor": "#2b2e36",
  "lineColor": "#ed83b2", "edgeLabelBackground": "#0d1017", "clusterBkg": "#0d1017"
}}}%%
flowchart LR
    U([Estudante]) --> APP["Next.js 16 App Router<br/>React 19 · Tailwind 4 · Canvas 2D"]
    APP --> LOCAL[("Stores locais<br/>Zustand · IndexedDB")]
    LOCAL <-->|"com conta"| SYNC["Motor de sincronização<br/>documento por área"]
    SYNC --> SB[("Supabase<br/>Auth · Postgres com RLS")]
    APP --> FSRS["FSRS-6<br/>repetição espaçada"]
    APP --> RH["Route Handlers"]
    RH --> AI["Gemini<br/>feedback e cartões"]
    RH --> WEB["Busca na web<br/>bot de questões"]

    classDef user fill:#16121d,stroke:#9ca3af,color:#f3f4f6
    classDef app fill:#ed83b2,stroke:#f9a8d4,color:#1a1020
    classDef data fill:#24427a,stroke:#5b9bff,color:#fff
    classDef ext fill:#1a1f29,stroke:#64748b,color:#f3f4f6
    class U user
    class APP,RH app
    class LOCAL,SYNC,SB data
    class FSRS,AI,WEB ext
```

Local-first: cada tela lê e grava no próprio aparelho e funciona sem internet.
Com conta, a sincronização roda em segundo plano, e o Row Level Security garante
que cada pessoa só enxerga os próprios dados. Quem não tem conta nem baixa o
Supabase, e o JavaScript inicial de cada tela fica entre 210 e 275 KB.

</details>

<br>

<table>
<tr>
<td width="33.33%" valign="top">
<a href="https://cinesol-cinema.vercel.app">
  <img src="assets/cinesol.svg" alt="CineSol, reserva de cinema" width="100%">
</a>
<p align="center">
  <img src="https://img.shields.io/badge/Next.js_16-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js 16">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Tailwind_CSS_4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS 4">
  <img src="https://img.shields.io/badge/React_Hook_Form-EC5990?style=flat-square&logo=reacthookform&logoColor=white" alt="React Hook Form">
  <img src="https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white" alt="Zod">
  <img src="https://img.shields.io/badge/Framer_Motion-0055FF?style=flat-square&logo=framer&logoColor=white" alt="Framer Motion">
</p>
<ul>
  <li><sub>Escolha de poltronas e combos da bomboniere</sub></li>
  <li><sub>Checkout com cartão ou Pix e recibo por download ou e-mail</sub></li>
  <li><sub>Cadastro e login validados com Zod e programa de pontos</sub></li>
  <li><sub>Desafio em dupla do processo seletivo da Loading Jr.</sub></li>
</ul>
<p align="center">
  <a href="https://cinesol-cinema.vercel.app"><b>Ver demo</b></a>
  &nbsp;·&nbsp;
  <a href="https://github.com/joaotabosa3599/cinesol-cinema">código</a>
</p>
</td>
<td width="33.33%" valign="top">
<a href="https://anabijus-ecommerce.vercel.app">
  <img src="assets/anabijus.svg" alt="Anabijus, e-commerce de joias" width="100%">
</a>
<p align="center">
  <img src="https://img.shields.io/badge/React_19-149ECA?style=flat-square&logo=react&logoColor=white" alt="React 19">
  <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white" alt="Vite">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=white" alt="JavaScript">
  <img src="https://img.shields.io/badge/React_Router_7-CA4245?style=flat-square&logo=reactrouter&logoColor=white" alt="React Router 7">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/Font_Awesome-528DD7?style=flat-square&logo=fontawesome&logoColor=white" alt="Font Awesome">
</p>
<ul>
  <li><sub>Rotas protegidas que devolvem você à página de origem após o login</sub></li>
  <li><sub>Carrinho persistente com total em tempo real e histórico de pedidos</sub></li>
  <li><sub>Busca global por nome ou categoria, layout mobile-first</sub></li>
  <li><sub>Catálogo em JSON trocável por uma API real sem mexer nas telas</sub></li>
</ul>
<p align="center">
  <a href="https://anabijus-ecommerce.vercel.app"><b>Ver demo</b></a>
  &nbsp;·&nbsp;
  <a href="https://github.com/joaotabosa3599/anabijus-ecommerce">código</a>
</p>
</td>
<td width="33.33%" valign="top">
<a href="https://portfolio-orcin-nine-x51rqo3inw.vercel.app">
  <img src="assets/portfolio.svg" alt="Portfólio, site pessoal" width="100%">
</a>
<p align="center">
  <img src="https://img.shields.io/badge/React_19-149ECA?style=flat-square&logo=react&logoColor=white" alt="React 19">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white" alt="Vite">
  <img src="https://img.shields.io/badge/Tailwind_CSS_4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS 4">
  <img src="https://img.shields.io/badge/GSAP-88CE02?style=flat-square&logo=greensock&logoColor=white" alt="GSAP">
  <img src="https://img.shields.io/badge/Framer_Motion-0055FF?style=flat-square&logo=framer&logoColor=white" alt="Framer Motion">
  <img src="https://img.shields.io/badge/Lenis-4B5563?style=flat-square" alt="Lenis">
</p>
<ul>
  <li><sub>Cena 3D em CSS (sem WebGL) no topo, que se abre com o ponteiro</sub></li>
  <li><sub>Abertura com câmera orbitando, pulável e desligada com movimento reduzido</sub></li>
  <li><sub>Estudos de caso gerados a partir de dados</sub></li>
  <li><sub>Imagens AVIF e WebP responsivas e fontes auto-hospedadas</sub></li>
</ul>
<p align="center">
  <a href="https://portfolio-orcin-nine-x51rqo3inw.vercel.app"><b>Ver site</b></a>
  &nbsp;·&nbsp;
  <a href="https://github.com/joaotabosa3599/portfolio">código</a>
</p>
</td>
</tr>
</table>

<br>

## Stack

<table align="center">
<tr>
<td align="center" valign="top" width="25%">

**Interface**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-149ECA?style=flat-square&logo=react&logoColor=white)<br>
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

</td>
<td align="center" valign="top" width="25%">

**Servidor e dados**

![Node.js](https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)<br>
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)

</td>
<td align="center" valign="top" width="25%">

**Mobile**

![Capacitor](https://img.shields.io/badge/Capacitor-119EFF?style=flat-square&logo=capacitor&logoColor=white)

</td>
<td align="center" valign="top" width="25%">

**Testes e deploy**

![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white) ![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

</td>
</tr>
</table>

<details>
<summary><b>Também trabalho com</b></summary>

<br>

Java e C, da graduação em Engenharia da Computação. Estruturas de dados,
processamento de texto e um sistema de gestão de funcionários estão nos
repositórios públicos.

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)

</details>

<br>

## Estudando agora

Quero desenhar de onde o dado vem, não só consumi-lo.

<table>
<tr>
<td align="center" width="33.33%">🧭<br><b>Arquitetura de API REST</b></td>
<td align="center" width="33.33%">🗂️<br><b>Modelagem relacional</b></td>
<td align="center" width="33.33%">🔐<br><b>Row Level Security no Postgres</b></td>
</tr>
</table>

<br>

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com/?user=joaotabosa3599&hide_border=true&border_radius=16&background=15171C&stroke=2B2E36&ring=7F5AF5&fire=5EEAD4&currStreakNum=F5F5F5&sideNums=F5F5F5&currStreakLabel=A48BFB&sideLabels=9A9CA3&dates=64666D&date_format=j%20M%5B%20Y%5D">
  <source media="(prefers-color-scheme: light)" srcset="https://streak-stats.demolab.com/?user=joaotabosa3599&hide_border=true&border_radius=16&background=FFFFFF&stroke=E5E7EB&ring=7F5AF5&fire=0891B2&currStreakNum=111318&sideNums=111318&currStreakLabel=7F5AF5&sideLabels=64666D&dates=9A9CA3&date_format=j%20M%5B%20Y%5D">
  <img src="https://streak-stats.demolab.com/?user=joaotabosa3599&hide_border=true&border_radius=16&background=15171C&stroke=2B2E36&ring=7F5AF5&fire=5EEAD4&currStreakNum=F5F5F5&sideNums=F5F5F5&currStreakLabel=A48BFB&sideLabels=9A9CA3&dates=64666D&date_format=j%20M%5B%20Y%5D" alt="Sequência de contribuições de João Tabosa no GitHub">
</picture>

</div>
