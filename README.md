<div align="center">

<a href="https://portfolio-orcin-nine-x51rqo3inw.vercel.app">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/banner-light.svg">
  <img src="assets/banner.svg" alt="João Tabosa, Full Stack Developer. Construo aplicações web do banco de dados à interface." width="100%">
</picture>
</a>

<br>

[![Portfólio](https://img.shields.io/badge/Portf%C3%B3lio-7F5AF5?style=for-the-badge&logo=googlechrome&logoColor=white)](https://portfolio-orcin-nine-x51rqo3inw.vercel.app) [![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/joãotabosa3599) [![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/j_pedro32k) [![E-mail](https://img.shields.io/badge/E--mail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:joao.tabosa3599@gmail.com)

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

![Status](https://img.shields.io/badge/Projeto_pessoal-reposit%C3%B3rio_privado-12161E?style=for-the-badge&labelColor=0D1017) &nbsp; ![Universos](https://img.shields.io/badge/Dois_universos-Constela_e_%C3%93rion-ED83B2?style=for-the-badge&labelColor=0D1017) &nbsp; ![Testes](https://img.shields.io/badge/293_testes-Vitest-6E9F18?style=for-the-badge&labelColor=0D1017)

</div>

**Constela & Órion** é uma plataforma de estudos gamificada em pixel art. Agenda
semanal com arrastar e soltar, edital com o progresso de cada assunto, quizzes
com explicação, simulados no tempo da prova e flashcards com repetição espaçada
(FSRS). São dois universos trocáveis, cada um com mascote, paleta e céu animado
próprios, a abelhinha Constela e o Ori, o axolote. Tudo funciona sem internet e
sincroniza com a conta quando ela existe. XP e conquistas premiam a constância
sem punir o dia perdido.

> [!NOTE]
> Projeto pessoal, por isso o repositório é privado e o app ainda não está
> publicado. O GIF abaixo é o app real, com dados de demonstração.

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
  <sub><b>Next.js · TypeScript · Tailwind</b></sub><br>
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
  <sub><b>React · Vite · JavaScript</b></sub><br>
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
  <sub><b>React · TypeScript · Tailwind · Framer Motion</b></sub><br>
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
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

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

![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

</td>
</tr>
</table>

<details>
<summary><b>Também trabalho com</b></summary>

<br>

Java e C, da graduação em Engenharia da Computação. Estruturas de dados,
processamento de texto e um sistema de gestão de funcionários estão nos
repositórios públicos.

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)

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
