<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Web Summit Rio 2026 — Relatório Wati</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;0,9..40,600;0,9..40,700;0,9..40,800;1,9..40,400&display=swap" rel="stylesheet">
<style>
  :root {
    --green: #00E785;
    --green-dark: #00c96f;
    --dark: #0A0A0A;
    --dark-2: #111111;
    --dark-3: #1A1A1A;
    --dark-4: #222222;
    --white: #FFFFFF;
    --off-white: #F8F8F8;
    --light-green: #CAFDE8;
    --light-green-2: #e8fdf4;
    --light-blue: #E3F5FF;
    --light-purple: #FDECFF;
    --light-yellow: #FFF6DA;
    --gray: #666666;
    --gray-2: #999999;
    --gray-light: #EBEBEB;
    --font: 'DM Sans', sans-serif;
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    font-family: var(--font);
    background: var(--dark);
    color: var(--white);
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }

  .page { min-height: 100vh; position: relative; overflow: hidden; }
  .page-inner { max-width: 1100px; margin: 0 auto; padding: 80px 60px; }

  /* COVER */
  .cover { background: var(--dark); display: flex; flex-direction: column; justify-content: center; }
  .cover::before {
    content: ''; position: absolute; top: -200px; right: -200px;
    width: 700px; height: 700px;
    background: radial-gradient(circle, rgba(0,231,133,0.12) 0%, transparent 70%);
    border-radius: 50%; pointer-events: none;
  }
  .cover::after {
    content: ''; position: absolute; bottom: -100px; left: -100px;
    width: 500px; height: 500px;
    background: radial-gradient(circle, rgba(0,231,133,0.06) 0%, transparent 70%);
    border-radius: 50%; pointer-events: none;
  }
  .cover-logo { font-size: 22px; font-weight: 800; color: var(--green); letter-spacing: -0.02em; margin-bottom: 80px; }
  .cover-eyebrow { font-size: 13px; font-weight: 600; letter-spacing: 0.14em; text-transform: uppercase; color: var(--green); margin-bottom: 28px; }
  .cover-title { font-size: clamp(48px, 6vw, 80px); font-weight: 800; line-height: 1.05; letter-spacing: -0.03em; color: var(--white); max-width: 780px; margin-bottom: 24px; }
  .cover-title span { color: var(--green); }
  .cover-subtitle { font-size: 18px; font-weight: 400; color: var(--gray-2); max-width: 560px; line-height: 1.65; margin-bottom: 60px; }
  .cover-meta { display: flex; gap: 40px; align-items: center; flex-wrap: wrap; }
  .cover-meta-item { font-size: 13px; color: var(--gray); }
  .cover-meta-item strong { color: var(--white); font-weight: 600; }
  .cover-divider { width: 1px; height: 20px; background: rgba(255,255,255,0.1); }
  .cover-stripe { position: absolute; bottom: 0; left: 0; right: 0; height: 4px; background: linear-gradient(90deg, var(--green) 0%, transparent 60%); }

  /* INTRO */
  .intro { background: var(--white); color: var(--dark); }
  .intro-label { font-size: 11px; font-weight: 700; letter-spacing: 0.14em; text-transform: uppercase; color: var(--green-dark); margin-bottom: 16px; }
  .intro-headline { font-size: clamp(34px, 4vw, 52px); font-weight: 800; line-height: 1.1; letter-spacing: -0.03em; color: var(--dark); max-width: 640px; margin-bottom: 40px; }
  .intro-headline span { color: var(--green-dark); }
  .stats-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 24px; margin-bottom: 64px; }
  .stat-card { background: var(--dark); border-radius: 16px; padding: 32px 28px; position: relative; overflow: hidden; }
  .stat-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px; background: var(--green); }
  .stat-number { font-size: 44px; font-weight: 800; letter-spacing: -0.04em; color: var(--green); line-height: 1; margin-bottom: 8px; }
  .stat-label { font-size: 13px; font-weight: 500; color: var(--gray-2); line-height: 1.4; }
  .intro-body { display: grid; grid-template-columns: 1fr 1fr; gap: 60px; align-items: start; }
  .intro-text p { font-size: 17px; color: #444; line-height: 1.75; margin-bottom: 20px; }
  .intro-text p strong { color: var(--dark); }
  .thesis-box { background: var(--dark); border-radius: 20px; padding: 40px; position: relative; overflow: hidden; }
  .thesis-box::before { content: ''; position: absolute; top: -60px; right: -60px; width: 200px; height: 200px; background: radial-gradient(circle, rgba(0,231,133,0.15) 0%, transparent 70%); border-radius: 50%; }
  .thesis-label { font-size: 11px; font-weight: 700; letter-spacing: 0.12em; text-transform: uppercase; color: var(--green); margin-bottom: 16px; }
  .thesis-text { font-size: 20px; font-weight: 700; color: var(--white); line-height: 1.45; letter-spacing: -0.02em; }
  .thesis-sub { margin-top: 16px; font-size: 14px; color: var(--gray-2); line-height: 1.65; }

  /* DAY DIVIDER */
  .divider-page { background: var(--dark); display: flex; align-items: center; justify-content: center; text-align: center; position: relative; }
  .divider-page::before { content: ''; position: absolute; inset: 0; background: radial-gradient(ellipse at 50% 40%, rgba(0,231,133,0.08) 0%, transparent 65%); pointer-events: none; }
  .divider-inner { position: relative; z-index: 1; padding: 60px; }
  .divider-day-label { font-size: 12px; font-weight: 700; letter-spacing: 0.18em; text-transform: uppercase; color: var(--green); margin-bottom: 32px; }
  .divider-title { font-size: clamp(36px, 5vw, 64px); font-weight: 800; letter-spacing: -0.04em; line-height: 1.1; color: var(--white); max-width: 700px; margin: 0 auto 20px; }
  .divider-title em { font-style: normal; color: var(--green); }
  .divider-date { font-size: 14px; color: var(--gray); margin-top: 16px; }

  /* CONTENT PAGE */
  .content-page { background: var(--white); color: var(--dark); padding: 100px 0; }
  .content-page .page-inner { display: grid; grid-template-columns: 1fr; gap: 64px; }
  .section-eyebrow { font-size: 11px; font-weight: 700; letter-spacing: 0.14em; text-transform: uppercase; color: var(--green-dark); margin-bottom: 14px; }
  .section-title { font-size: clamp(28px, 3.5vw, 44px); font-weight: 800; letter-spacing: -0.03em; line-height: 1.15; color: var(--dark); margin-bottom: 20px; }
  .section-body { font-size: 17px; color: #444; line-height: 1.75; max-width: 720px; }
  .trends-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px; }
  .trend-card { border-radius: 16px; padding: 32px; position: relative; overflow: hidden; }
  .trend-card.green { background: var(--light-green-2); }
  .trend-card.blue { background: var(--light-blue); }
  .trend-card.purple { background: var(--light-purple); }
  .trend-card.yellow { background: var(--light-yellow); }
  .trend-card.dark { background: var(--dark); color: var(--white); }
  .trend-number { font-size: 12px; font-weight: 700; letter-spacing: 0.1em; text-transform: uppercase; color: var(--green-dark); margin-bottom: 16px; }
  .trend-card.dark .trend-number { color: var(--green); }
  .trend-title { font-size: 20px; font-weight: 700; line-height: 1.3; letter-spacing: -0.02em; color: var(--dark); margin-bottom: 12px; }
  .trend-card.dark .trend-title { color: var(--white); }
  .trend-body { font-size: 14px; line-height: 1.7; color: #555; }
  .trend-card.dark .trend-body { color: var(--gray-2); }
  .implications-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
  .implication-item { display: flex; gap: 16px; align-items: flex-start; padding: 24px; background: var(--off-white); border-radius: 12px; }
  .implication-dot { width: 8px; height: 8px; border-radius: 50%; background: var(--green); flex-shrink: 0; margin-top: 6px; }
  .implication-text { font-size: 15px; line-height: 1.6; color: #444; }
  .implication-text strong { color: var(--dark); }

  /* QUOTE PAGE */
  .quote-page { background: var(--dark-3); display: flex; align-items: center; min-height: 60vh; position: relative; overflow: hidden; }
  .quote-page::before { content: ''; position: absolute; top: -100px; right: -100px; width: 500px; height: 500px; background: radial-gradient(circle, rgba(0,231,133,0.07) 0%, transparent 65%); border-radius: 50%; }
  .quote-inner { max-width: 900px; margin: 0 auto; padding: 80px 60px; position: relative; z-index: 1; }
  .quote-mark { font-size: 120px; line-height: 0.6; color: var(--green); opacity: 0.3; font-family: Georgia, serif; margin-bottom: 16px; display: block; }
  .quote-text { font-size: clamp(22px, 3vw, 36px); font-weight: 700; line-height: 1.35; letter-spacing: -0.02em; color: var(--white); margin-bottom: 32px; }
  .quote-source { font-size: 14px; color: var(--gray-2); }
  .quote-source strong { color: var(--green); }

  /* KEY TAKEAWAYS */
  .takeaways-page { background: var(--dark); color: var(--white); }
  .takeaways-page .page-inner { padding-top: 100px; padding-bottom: 100px; }
  .takeaway-list { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-top: 48px; }
  .takeaway-item { display: flex; gap: 20px; align-items: flex-start; padding: 28px; background: var(--dark-3); border-radius: 16px; }
  .takeaway-num { font-size: 32px; font-weight: 800; color: var(--green); line-height: 1; opacity: 0.5; flex-shrink: 0; letter-spacing: -0.04em; }
  .takeaway-content { flex: 1; }
  .takeaway-title { font-size: 17px; font-weight: 700; color: var(--white); margin-bottom: 6px; letter-spacing: -0.01em; }
  .takeaway-body { font-size: 14px; color: var(--gray-2); line-height: 1.6; }

  /* THESIS CONCLUSION */
  .thesis-page { background: var(--dark); display: flex; align-items: center; justify-content: center; text-align: center; position: relative; overflow: hidden; min-height: 100vh; }
  .thesis-page::before { content: ''; position: absolute; inset: 0; background: radial-gradient(ellipse at 50% 45%, rgba(0,231,133,0.12) 0%, transparent 60%); }
  .thesis-inner { position: relative; z-index: 1; max-width: 800px; padding: 80px 60px; }
  .thesis-eyebrow { font-size: 11px; font-weight: 700; letter-spacing: 0.16em; text-transform: uppercase; color: var(--green); margin-bottom: 24px; }
  .thesis-headline { font-size: clamp(36px, 5.5vw, 70px); font-weight: 800; letter-spacing: -0.04em; line-height: 1.05; color: var(--white); margin-bottom: 28px; }
  .thesis-headline em { font-style: normal; color: var(--green); }
  .thesis-proof { font-size: 17px; color: var(--gray-2); line-height: 1.7; max-width: 600px; margin: 0 auto 28px; }
  .proof-pills { display: flex; flex-wrap: wrap; gap: 10px; justify-content: center; margin-top: 40px; }
  .proof-pill { background: rgba(0,231,133,0.1); border: 1px solid rgba(0,231,133,0.25); color: var(--green); font-size: 13px; font-weight: 600; padding: 8px 18px; border-radius: 100px; }

  /* CTA */
  .cta-page { background: var(--dark); position: relative; overflow: hidden; display: flex; align-items: center; }
  .cta-page::before { content: ''; position: absolute; top: -200px; right: -200px; width: 700px; height: 700px; background: radial-gradient(circle, rgba(0,231,133,0.1) 0%, transparent 65%); border-radius: 50%; }
  .cta-inner { position: relative; z-index: 1; max-width: 1100px; margin: 0 auto; padding: 80px 60px; }
  .cta-grid { display: grid; grid-template-columns: 1fr auto; gap: 80px; align-items: center; }
  .cta-logo { font-size: 24px; font-weight: 800; color: var(--green); letter-spacing: -0.02em; margin-bottom: 40px; }
  .cta-eyebrow { font-size: 11px; font-weight: 700; letter-spacing: 0.14em; text-transform: uppercase; color: var(--green); margin-bottom: 20px; }
  .cta-headline { font-size: clamp(32px, 4vw, 54px); font-weight: 800; letter-spacing: -0.03em; line-height: 1.1; color: var(--white); margin-bottom: 20px; }
  .cta-body { font-size: 17px; color: var(--gray-2); line-height: 1.7; max-width: 520px; margin-bottom: 40px; }
  .cta-btn { display: inline-block; background: var(--green); color: var(--dark); font-size: 15px; font-weight: 700; padding: 16px 36px; border-radius: 100px; text-decoration: none; letter-spacing: -0.01em; }
  .cta-meta { margin-top: 48px; font-size: 13px; color: var(--gray); }
  .cta-meta a { color: var(--gray-2); text-decoration: none; }
  .qr-placeholder { width: 140px; height: 140px; border: 2px solid rgba(255,255,255,0.1); border-radius: 12px; display: flex; align-items: center; justify-content: center; flex-direction: column; gap: 8px; }
  .qr-caption { font-size: 11px; color: var(--gray); text-align: center; line-height: 1.4; }

  @media print {
    .page { page-break-after: always; }
    body { background: white; }
  }
  @media (max-width: 900px) {
    .page-inner { padding: 60px 30px; }
    .stats-grid { grid-template-columns: repeat(2, 1fr); }
    .trends-grid { grid-template-columns: 1fr; }
    .intro-body, .cta-grid, .implications-grid, .takeaway-list { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<!-- CAPA -->
<section class="page cover">
  <div class="page-inner">
    <div class="cover-logo">wati</div>
    <div class="cover-eyebrow">Relatório Pós Web Summit Rio · Junho de 2026</div>
    <h1 class="cover-title">
      O Futuro da IA,<br>das <span>Conversas</span><br>e do Crescimento
    </h1>
    <p class="cover-subtitle">
      As tendências mais importantes, os insights e as oportunidades estratégicas do maior evento de tecnologia da América Latina - curado para líderes de negócio.
    </p>
    <div class="cover-meta">
      <span class="cover-meta-item"><strong>Web Summit Rio 2026</strong></span>
      <span class="cover-divider"></span>
      <span class="cover-meta-item">8 a 11 de Junho de 2026</span>
      <span class="cover-divider"></span>
      <span class="cover-meta-item">Rio de Janeiro, Brasil</span>
      <span class="cover-divider"></span>
      <span class="cover-meta-item"><strong>Relatório dos 4 Dias</strong></span>
    </div>
  </div>
  <div class="cover-stripe"></div>
</section>

<!-- INTRODUÇÃO -->
<section class="page intro">
  <div class="page-inner">
    <div class="intro-label">Contexto</div>
    <h2 class="intro-headline">O maior evento de tech<br>da América Latina<br><span>fez história.</span></h2>

    <div class="stats-grid">
      <div class="stat-card">
        <div class="stat-number">40K+</div>
        <div class="stat-label">Participantes de 100+ países</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">1.572</div>
        <div class="stat-label">Startups — novo recorde histórico</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">688</div>
        <div class="stat-label">Investidores presentes e ativos no evento</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">100+</div>
        <div class="stat-label">Países representados</div>
      </div>
    </div>

    <div class="intro-body">
      <div class="intro-text">
        <p>Foram quatro dias de conversas entre fundadores, investidores, líderes de governo e executivos globais de tecnologia no maior evento de tecnologia da América Latina. E a mensagem que ficou foi: <strong>a era da experimentação com IA acabou.</strong></p>
        <p>O que veio no lugar? Responsabilidade, resultados e uma pergunta nova: como usar a tecnologia para construir um negócio onde cada ponto de contato com o cliente - da aquisição ao suporte e à retenção - flui por meio de uma conversa?</p>
        <p>Este relatório captura as tendências mais importantes, as melhores citações e as implicações estratégicas de cada dia. Projetado para líderes que precisam de clareza, não de volume.</p>
      </div>
      <div class="thesis-box">
        <div class="thesis-label">A tese central</div>
        <div class="thesis-text">"A Conversa É o Negócio."</div>
        <div class="thesis-sub">
          Uma tendência emergiu no Web Summit Rio 2026 e apontou para a conclusão: as empresas que vão ganhar são aquelas que tratam conversas — e não campanhas, funis ou landing pages — como sua principal infraestrutura comercial.
        </div>
      </div>
    </div>
  </div>
</section>

<!-- DIA 1 — DIVISOR -->
<section class="page divider-page">
  <div class="divider-inner">
    <div class="divider-day-label">Dia 1 · 8 de Junho de 2026</div>
    <h2 class="divider-title">O Fim da Era do<br><em>Hype de IA</em></h2>
    <p class="divider-date">A IA deixa de ser promessa e vira responsabilidade</p>
  </div>
</section>

<!-- DIA 1 — CONTEÚDO -->
<section class="page content-page">
  <div class="page-inner">
    <div>
      <div class="section-eyebrow">Resumo Executivo — Dia 1</div>
      <h2 class="section-title">A IA parou de ser promessa.<br>Virou pergunta.</h2>
      <p class="section-body">O primeiro dia do Web Summit Rio 2026 definiu o tom de tudo que veio depois. A pergunta que dominou cada painel e cada pitch: <strong>você consegue provar que funciona?</strong> O ciclo de hype da IA terminou. O que o substitui é um mercado exigente e pragmático que espera resultados mensuráveis — não potencial.</p>
      <p class="section-body" style="margin-top:16px;">Os mercados Brasil e LATAM não eram apenas o cenário dessa conversa. Eram os protagonistas. Com 160 milhões de usuários de internet e penetração de WhatsApp acima de 90%, a região está posicionada como um dos mercados mais importantes do mundo para IA conversacional em escala.</p>
    </div>

    <div>
      <div class="section-eyebrow">Principais Tendências</div>
      <div class="trends-grid">
        <div class="trend-card green">
          <div class="trend-number">Tendência 01</div>
          <div class="trend-title">O ROI de IA se torna métrica que importa muito</div>
          <div class="trend-body">As pessoas pararam de perguntar 'o que a IA pode fazer?' e começaram a perguntar 'o que a IA entregou?' As empresas precisam mostrar estudos de caso, dados de coorte e resultados de negócio — não somente de narrativas de tecnologia.</div>
        </div>
        <div class="trend-card blue">
          <div class="trend-number">Tendência 02</div>
          <div class="trend-title">O Gap de Orquestração surge como grande bloqueio</div>
          <div class="trend-body">As empresas têm ferramentas de IA mas não têm estratégia de IA. A distância entre experimentar com IA e implantá-la como um sistema de negócio é onde a maioria das organizações está travada — e esse gap está aumentando.</div>
        </div>
        <div class="trend-card dark">
          <div class="trend-number">Tendência 03</div>
          <div class="trend-title">WhatsApp vira sistema operacional dos negócios</div>
          <div class="trend-body">Cada vertical — varejo, fintech, saúde, governo — está convergindo para o WhatsApp como interface principal de conversas com o cliente. Não como um aplicativo de mensagens. Como infraestrutura para os resultados do negócio.</div>
        </div>
      </div>
    </div>

    <div>
      <div class="section-eyebrow">O que isso significa para o seu negócio</div>
      <div class="implications-grid">
        <div class="implication-item">
          <div class="implication-dot"></div>
          <div class="implication-text"><strong>Substitua sua demo de IA por um caso de negócio.</strong> Os compradores na LATAM agora exigem prova antes de assinar. Sua narrativa comercial precisa colocar resultados mensuráveis na frente.</div>
        </div>
        <div class="implication-item">
          <div class="implication-dot"></div>
          <div class="implication-text"><strong>Construa uma estratégia de IA, não um stack de IA.</strong> As empresas que estão saindo na frente não são as que têm mais ferramentas — são as que conectaram IA aos seus processos comerciais centrais.</div>
        </div>
        <div class="implication-item">
          <div class="implication-dot"></div>
          <div class="implication-text"><strong>Se você não está no WhatsApp, você é invisível.</strong> No Brasil, as conversas acontecem no WhatsApp. Vendas, suporte, onboarding, retenção — tudo está lá. Sua concorrência também está.</div>
        </div>
        <div class="implication-item">
          <div class="implication-dot"></div>
          <div class="implication-text"><strong>A LATAM está em evidência no mercado global de IA.</strong> O que funciona aqui — em escala, com PMEs sensíveis a preço, no WhatsApp — pode definir o próximo playbook para mercados emergentes no mundo todo.</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- DIA 2 — DIVISOR -->
<section class="page divider-page">
  <div class="divider-inner">
    <div class="divider-day-label">Dia 2 · 9 de Junho de 2026</div>
    <h2 class="divider-title">Quando <em>Infraestrutura</em><br>Vira Vantagem</h2>
    <p class="divider-date">As empresas que ganham dominam a camada de integração</p>
  </div>
</section>

<!-- DIA 2 — CONTEÚDO -->
<section class="page content-page">
  <div class="page-inner">
    <div>
      <div class="section-eyebrow">Resumo Executivo — Dia 2</div>
      <h2 class="section-title">O Muro do Legado é real.<br>A maioria das empresas<br>acabou de bater nele.</h2>
      <p class="section-body">O Dia 2 trouxe um diagnóstico que o mercado estava evitando. Analistas e desenvolvedores deram nome ao problema dominante: o <strong>Muro do Legado</strong> — a fricção técnica e organizacional que impede as empresas de conectar ferramentas modernas de IA aos sistemas onde seu negócio real acontece. CRMs, ERPs, bancos de dados legados, arquiteturas de uma década atrás.</p>
      <p class="section-body" style="margin-top:16px;">As empresas que resolveram esse problema não foram as que tinham os melhores modelos, mas as que tinham a camada de integração mais limpa. Simplicidade e confiança — em dados, em compliance, em infraestrutura — é vantagem competitiva.</p>
    </div>

    <div>
      <div class="section-eyebrow">Principais Tendências</div>
      <div class="trends-grid">
        <div class="trend-card purple">
          <div class="trend-number">Tendência 01</div>
          <div class="trend-title">O Muro do Legado bloqueia a adoção de IA nas empresas</div>
          <div class="trend-body">A maioria das grandes empresas tem 7 a 12 sistemas desconectados. Agentes de IA não conseguem trabalhar com dados em silos. As empresas que estão vencendo na IA são as que resolveram a arquitetura de dados primeiro — não as que compraram o melhor modelo.</div>
        </div>
        <div class="trend-card green">
          <div class="trend-number">Tendência 02</div>
          <div class="trend-title">Agentes de IA precisam de orquestração, não só de implantação</div>
          <div class="trend-body">Ter um agente de IA já é o mínimo esperado. Orquestrar múltiplos agentes ao longo de uma jornada do cliente — sem quebrar a experiência — é a vantagem competitiva real. A maioria das empresas ainda não consegue fazer isso.</div>
        </div>
        <div class="trend-card dark">
          <div class="trend-number">Tendência 03</div>
          <div class="trend-title">Confiança vira infraestrutura de negócio</div>
          <div class="trend-body">Conformidade com LGPD e soberania de dados migraram de checkboxes jurídicos para requisitos de compra. Compradores enterprise estão filtrando fornecedores por sinais de confiança antes de avaliar funcionalidades.</div>
        </div>
      </div>
    </div>

    <div>
      <div class="section-eyebrow">O que isso significa para o seu negócio</div>
      <div class="implications-grid">
        <div class="implication-item">
          <div class="implication-dot"></div>
          <div class="implication-text"><strong>Audite sua camada de integração antes do seu roadmap de IA.</strong> Se seus dados estão fragmentados, cada investimento em IA está sobre uma base quebrada.</div>
        </div>
        <div class="implication-item">
          <div class="implication-dot"></div>
          <div class="implication-text"><strong>Projete para orquestração, não para soluções pontuais.</strong> Os vencedores não estão implantando chatbots isolados — estão construindo sistemas de conversação conectados que atravessam todo o ciclo de vida do cliente.</div>
        </div>
        <div class="implication-item">
          <div class="implication-dot"></div>
          <div class="implication-text"><strong>Torne seu compliance visível.</strong> A LGPD não é mais um centro de custo. Documente suas práticas de dados e use-as como ativos comerciais com prospects enterprise.</div>
        </div>
        <div class="implication-item">
          <div class="implication-dot"></div>
          <div class="implication-text"><strong>A camada de integração é o produto.</strong> Para empresas de tech B2B na LATAM, a pergunta não é 'o que sua IA faz?' — é 'no que sua IA consegue se conectar?'</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- DIA 2 — CITAÇÃO -->
<section class="quote-page">
  <div class="quote-inner">
    <span class="quote-mark">"</span>
    <p class="quote-text">Empresas que tratam IA como uma funcionalidade vão perder para aquelas que a tratam como seu modelo operacional. A vantagem sustentável com IA só existe quando a inteligência está no centro da estratégia de negócio — não sobreposta aos processos existentes.</p>
    <div class="quote-source"><strong>Silvio Meira</strong> · CESAR — Centro de Estudos e Sistemas Avançados do Recife · AI Summit, Web Summit Rio 2026</div>
  </div>
</section>

<!-- DIA 3 — DIVISOR -->
<section class="page divider-page">
  <div class="divider-inner">
    <div class="divider-day-label">Dia 3 · 10 de Junho de 2026</div>
    <h2 class="divider-title">Autenticidade, <em>Voz</em><br>e o Novo Contrato<br>de Marca</h2>
    <p class="divider-date">A verdade humana supera o polimento da IA. Sempre.</p>
  </div>
</section>

<!-- DIA 3 — CONTEÚDO -->
<section class="page content-page">
  <div class="page-inner">
    <div>
      <div class="section-eyebrow">Resumo Executivo — Dia 3</div>
      <h2 class="section-title">Num mundo de conteúdo<br>infinito gerado por IA,<br>a verdade vence.</h2>
      <p class="section-body">O Dia 3 trouxe um sinal contraintuitivo: à medida que o conteúdo gerado por IA inunda todos os canais, as marcas que estão saindo na frente são as que lideram com autenticidade radical. Uma conversa com a atriz e criadora Deborah Secco capturou o espírito do dia — "A verdade é o grande trunfo da internet hoje."</p>
      <p class="section-body" style="margin-top:16px;">O AI Summit revelou outra grande mudança: a voz está se tornando a camada de interação dominante para IA. Empresas estão construindo sistemas de voz em tempo real para mercados como o Brasil — onde mensagens de voz no WhatsApp já são o formato de comunicação preferido de milhões de pessoas. No mesmo dia, o governo brasileiro formalizou sua arquitetura de nuvem soberana, tornando a conformidade com LGPD um requisito inegociável para compras enterprise.</p>
    </div>

    <div>
      <div class="section-eyebrow">Principais Tendências</div>
      <div class="trends-grid">
        <div class="trend-card yellow">
          <div class="trend-number">Tendência 01</div>
          <div class="trend-title">Autenticidade vira a única estratégia de marca que escala</div>
          <div class="trend-body">À medida que o conteúdo gerado por IA se torna indistinguível do conteúdo humano, as audiências estão desenvolvendo um sexto sentido para a verdade. As marcas que ganham atenção são as que lideram com histórias reais de clientes e voz humana genuína — não com copy polido gerado por máquina.</div>
        </div>
        <div class="trend-card green">
          <div class="trend-number">Tendência 02</div>
          <div class="trend-title">A IA de voz chega — em tempo real, contextual, construída para a LATAM</div>
          <div class="trend-body">Empresas estão desenvolvendo interfaces de voz específicas para os mercados que falam português e espanhol. A voz está substituindo as telas como camada primária de interação com IA — especialmente relevante no Brasil, onde áudios no WhatsApp já dominam a comunicação cotidiana.</div>
        </div>
        <div class="trend-card dark">
          <div class="trend-number">Tendência 03</div>
          <div class="trend-title">Nuvem soberana vira filtro de compra para enterprise</div>
          <div class="trend-body">O Serpro formalizou a arquitetura da Nuvem de Governo brasileira. Conformidade com LGPD é agora um requisito obrigatório — não um diferencial — para qualquer contrato enterprise ou de setor público.</div>
        </div>
      </div>
    </div>

    <div>
      <div class="section-eyebrow">O que isso significa para o seu negócio</div>
      <div class="implications-grid">
        <div class="implication-item">
          <div class="implication-dot"></div>
          <div class="implication-text"><strong>Lidere com histórias de clientes, não com conteúdo gerado por IA.</strong> Seu ativo de marketing mais poderoso em 2026 é um cliente real descrevendo um resultado real. Construa seu motor de conteúdo em torno de provas.</div>
        </div>
        <div class="implication-item">
          <div class="implication-dot"></div>
          <div class="implication-text"><strong>Comece a planejar para voz agora.</strong> As mensagens de voz no WhatsApp já são o formato de comunicação dominante para milhões de usuários brasileiros. Seu roadmap de produto precisa de uma camada de voz.</div>
        </div>
        <div class="implication-item">
          <div class="implication-dot"></div>
          <div class="implication-text"><strong>Documente sua posição de compliance.</strong> Se você não consegue responder 'onde ficam meus dados?' em um RFP, você vai perder contratos enterprise a partir do segundo semestre de 2026.</div>
        </div>
        <div class="implication-item">
          <div class="implication-dot"></div>
          <div class="implication-text"><strong>Humano + IA é a única estratégia de conteúdo que escala.</strong> A tecnologia cuida da camada operacional. A autenticidade constrói o relacionamento. Os dois juntos — é isso que separa as empresas que crescem das que só escalam.</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- DIA 3 — CITAÇÃO -->
<section class="quote-page">
  <div class="quote-inner">
    <span class="quote-mark">"</span>
    <p class="quote-text">A verdade é o grande trunfo da internet hoje.</p>
    <div class="quote-source"><strong>Deborah Secco</strong> · Atriz e Criadora Digital · Web Summit Rio 2026</div>
  </div>
</section>

<!-- DIA 4 — DIVISOR -->
<section class="page divider-page">
  <div class="divider-inner">
    <div class="divider-day-label">Dia 4 · 11 de Junho de 2026</div>
    <h2 class="divider-title">Soberania Digital<br>Vira <em>Política de Estado</em></h2>
    <p class="divider-date">As regras do jogo estão sendo escritas agora</p>
  </div>
</section>

<!-- DIA 4 — CONTEÚDO -->
<section class="page content-page">
  <div class="page-inner">
    <div>
      <div class="section-eyebrow">Resumo Executivo — Dia 4</div>
      <h2 class="section-title">O Brasil acaba de se tornar<br>o 5º parceiro digital<br>da União Europeia.</h2>
      <p class="section-body">No último dia de Web Summit Rio, Henna Virkkunen, Vice-Presidente da Comissão Europeia para Soberania Tecnológica, anunciou que o Brasil se tornaria o quinto parceiro digital da Europa — ao lado de Japão, Canadá, Singapura e Coreia do Sul. Um acordo formal foi assinado no dia seguinte em São Paulo, cobrindo governança de dados, inteligência artificial, infraestrutura digital e conectividade.</p>
      <p class="section-body" style="margin-top:16px;">No mesmo dia, o Secretário de Governo Digital apresentou a Nuvem de Governo — uma infraestrutura de nuvem nacional que atenderá mais de 250 órgãos públicos. A mensagem foi: dados críticos permanecem sob jurisdição brasileira. Para empresas de tecnologia operando no Brasil, isso não é política futura. É a nova realidade comercial.</p>
    </div>

    <div>
      <div class="section-eyebrow">Principais Tendências</div>
      <div class="trends-grid">
        <div class="trend-card blue">
          <div class="trend-number">Tendência 01</div>
          <div class="trend-title">O Brasil entra no clube da diplomacia digital global</div>
          <div class="trend-body">A parceria UE-Brasil sinaliza que o Brasil não é mais um mercado periférico. É uma âncora estratégica para a economia digital global — com frameworks de governança, política de IA e padrões de infraestrutura sendo definidos agora.</div>
        </div>
        <div class="trend-card green">
          <div class="trend-number">Tendência 02</div>
          <div class="trend-title">Nuvem de Governo redefine as compras enterprise</div>
          <div class="trend-body">A Nuvem de Governo brasileira cobrirá mais de 250 órgãos do SISP. Três dimensões de soberania — de dados, operacional e tecnológica — agora estão embutidas nas compras do setor público. O setor privado vem logo atrás.</div>
        </div>
        <div class="trend-card dark">
          <div class="trend-number">Tendência 03</div>
          <div class="trend-title">Digitalização das PMEs acelera</div>
          <div class="trend-body">Empresas como Olist, Omie, iugu e Appmax confirmaram o que a Wati já sabe: o mercado de PMEs do Brasil está sendo estruturalmente transformado. Política pública e capital privado estão empurrando na mesma direção — agora.</div>
        </div>
      </div>
    </div>

    <div>
      <div class="section-eyebrow">O que isso significa para o seu negócio</div>
      <div class="implications-grid">
        <div class="implication-item">
          <div class="implication-dot"></div>
          <div class="implication-text"><strong>Compliance virou vantagem comercial.</strong> Empresas com postura LGPD-first ganham contratos enterprise e governamentais. Não se trata mais de evitar multas — trata-se de fechar negócios.</div>
        </div>
        <div class="implication-item">
          <div class="implication-dot"></div>
          <div class="implication-text"><strong>O corredor UE-Brasil está aberto.</strong> Empresas europeias entrando no Brasil e empresas brasileiras expandindo para a Ibéria têm agora um novo framework regulatório para operar — e dentro do qual competir.</div>
        </div>
        <div class="implication-item">
          <div class="implication-dot"></div>
          <div class="implication-text"><strong>A aceleração das PMEs é estrutural.</strong> O momento de construir participação de mercado no segmento de PMEs do Brasil é agora. O incentivo da política pública e do investimento privado está criando uma janela de crescimento de uma década.</div>
        </div>
        <div class="implication-item">
          <div class="implication-dot"></div>
          <div class="implication-text"><strong>Posicione-se como parceiro local, não como fornecedor global.</strong> A conversa sobre soberania abre espaço para empresas que conseguem demonstrar compromisso local, compliance local e entendimento local do mercado.</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- DIA 4 — CITAÇÃO (Virkkunen falou em inglês) -->
<section class="quote-page">
  <div class="quote-inner">
    <span class="quote-mark">"</span>
    <p class="quote-text">80 percent of our technologies are coming from outside of Europe. We don't want to be dependent only on third countries, only on USA companies. There are 160 million Internet users in Brazil — very big opportunities for both of us.</p>
    <div class="quote-source"><strong>Henna Virkkunen</strong> · Vice-Presidente, Comissão Europeia para Soberania Tecnológica · Web Summit Rio 2026</div>
  </div>
</section>

<!-- PRINCIPAIS APRENDIZADOS -->
<section class="page takeaways-page">
  <div class="page-inner">
    <div class="section-eyebrow" style="color: var(--green);">Quatro dias. Uma conclusão.</div>
    <h2 class="section-title" style="color: var(--white); max-width: 600px;">O que o Web Summit Rio 2026 provou sobre o futuro dos negócios</h2>

    <div class="takeaway-list">
      <div class="takeaway-item">
        <div class="takeaway-num">01</div>
        <div class="takeaway-content">
          <div class="takeaway-title">A IA migrou de experimentação para responsabilidade.</div>
          <div class="takeaway-body">O mercado agora exige ROI mensurável. Narrativas de tecnologia não fecham contratos. Resultados de negócio, sim.</div>
        </div>
      </div>
      <div class="takeaway-item">
        <div class="takeaway-num">02</div>
        <div class="takeaway-content">
          <div class="takeaway-title">A camada de orquestração é o verdadeiro diferencial competitivo.</div>
          <div class="takeaway-body">Ter ferramentas de IA é o mínimo. Conectá-las em uma experiência coerente para o cliente — em todos os canais — é onde os vencedores são construídos.</div>
        </div>
      </div>
      <div class="takeaway-item">
        <div class="takeaway-num">03</div>
        <div class="takeaway-content">
          <div class="takeaway-title">Confiança agora é infraestrutura.</div>
          <div class="takeaway-body">Soberania de dados, conformidade com LGPD e transparência migraram de requisitos jurídicos para vantagens comerciais. Compradores filtram por confiança antes de avaliar funcionalidades.</div>
        </div>
      </div>
      <div class="takeaway-item">
        <div class="takeaway-num">04</div>
        <div class="takeaway-content">
          <div class="takeaway-title">Autenticidade é a única estratégia de marca que escala.</div>
          <div class="takeaway-body">Num mundo inundado de conteúdo gerado por IA, a verdade humana — clientes reais, resultados reais, vozes reais — é o único conteúdo que conquista atenção sustentada.</div>
        </div>
      </div>
      <div class="takeaway-item">
        <div class="takeaway-num">05</div>
        <div class="takeaway-content">
          <div class="takeaway-title">A IA de voz chega ao mainstream mais rápido do que se esperava.</div>
          <div class="takeaway-body">No Brasil, onde os áudios no WhatsApp já dominam a comunicação, a migração de texto para voz na IA não é uma tendência futura. É um requisito de produto iminente.</div>
        </div>
      </div>
      <div class="takeaway-item">
        <div class="takeaway-num">06</div>
        <div class="takeaway-content">
          <div class="takeaway-title">O Brasil é âncora estratégica, não mercado emergente.</div>
          <div class="takeaway-body">A parceria digital UE-Brasil, a Nuvem de Governo, a aceleração das PMEs — o Brasil está sendo posicionado como um nó global de governança de IA e comércio digital.</div>
        </div>
      </div>
      <div class="takeaway-item">
        <div class="takeaway-num">07</div>
        <div class="takeaway-content">
          <div class="takeaway-title">O WhatsApp é o sistema operacional dos negócios na LATAM.</div>
          <div class="takeaway-body">Cada tendência, cada vertical, cada caso de uso apontou para aqui. O comércio conversacional via WhatsApp não é uma estratégia de canal. É infraestrutura de negócio.</div>
        </div>
      </div>
      <div class="takeaway-item">
        <div class="takeaway-num">08</div>
        <div class="takeaway-content">
          <div class="takeaway-title">A janela para PMEs está aberta.</div>
          <div class="takeaway-body">Política pública e investimento privado estão acelerando a digitalização das PMEs simultaneamente. As empresas que constroem participação de mercado agora estão construindo posições duradouras.</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CONCLUSÃO DA TESE -->
<section class="page thesis-page">
  <div class="thesis-inner">
    <div class="thesis-eyebrow">Web Summit Rio 2026 — A Conclusão</div>
    <h2 class="thesis-headline">A Conversa<br><em>É</em> o Negócio.</h2>
    <p class="thesis-proof">
      Quatro dias. Centenas de palestrantes. Milhares de conversas entre os líderes de tecnologia, investidores e construtores mais importantes do mundo. E uma verdade emergiu de forma consistente, em cada trilha, cada tendência, cada anúncio: <strong style="color: var(--white);">o negócio acontece por meio de conversas.</strong>
    </p>
    <p class="thesis-proof">
      Não por campanhas. Não por funis. Não por landing pages. Por conversas — personalizadas, em tempo real, contextuais, automatizadas em escala e impulsionadas por IA. As empresas que vão definir a próxima década do comércio na LATAM são as que entendem isso primeiro e constroem isso agora.
    </p>
    <div class="proof-pills">
      <span class="proof-pill">Responsabilidade de IA</span>
      <span class="proof-pill">WhatsApp como infraestrutura</span>
      <span class="proof-pill">Agentes de IA orquestrados</span>
      <span class="proof-pill">Voz autêntica do cliente</span>
      <span class="proof-pill">Comércio conversacional</span>
      <span class="proof-pill">Soberania digital</span>
      <span class="proof-pill">Aceleração das PMEs</span>
      <span class="proof-pill">IA de voz</span>
    </div>
  </div>
</section>

<!-- CTA FINAL -->
<section class="page cta-page">
  <div class="cta-inner">
    <div class="cta-grid">
      <div>
        <div class="cta-logo">wati</div>
        <div class="cta-eyebrow">Pronto para o próximo passo?</div>
        <h2 class="cta-headline">Pronto para transformar<br>conversas em crescimento?</h2>
        <p class="cta-body">
          Se a sua empresa está explorando como IA, WhatsApp e experiências conversacionais podem impulsionar aquisição, retenção e engajamento com clientes — adoraríamos mostrar o que é possível.
        </p>
        <a href="https://www.wati.io/book-a-demo/" class="cta-btn">Agende uma Demo →</a>
        <div class="cta-meta">
          <p>Wati · Plataforma de IA Conversacional para Negócios</p>
          <p><a href="https://www.wati.io">wati.io</a> · WhatsApp API · Agentes de IA · Astra</p>
        </div>
      </div>
      <div style="display: flex; flex-direction: column; align-items: center; gap: 16px;">
        <div class="qr-placeholder">
          <svg width="80" height="80" viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg">
            <rect x="2" y="2" width="28" height="28" rx="3" stroke="white" stroke-width="2"/>
            <rect x="8" y="8" width="16" height="16" fill="white"/>
            <rect x="50" y="2" width="28" height="28" rx="3" stroke="white" stroke-width="2"/>
            <rect x="56" y="8" width="16" height="16" fill="white"/>
            <rect x="2" y="50" width="28" height="28" rx="3" stroke="white" stroke-width="2"/>
            <rect x="8" y="56" width="16" height="16" fill="white"/>
            <rect x="38" y="38" width="6" height="6" fill="white"/>
            <rect x="50" y="38" width="6" height="6" fill="white"/>
            <rect x="62" y="38" width="6" height="6" fill="white"/>
            <rect x="38" y="50" width="6" height="6" fill="white"/>
            <rect x="50" y="50" width="6" height="6" fill="white"/>
            <rect x="62" y="62" width="6" height="6" fill="white"/>
            <rect x="74" y="50" width="6" height="6" fill="white"/>
            <rect x="74" y="62" width="6" height="6" fill="white"/>
          </svg>
        </div>
        <div class="qr-caption">Escaneie para agendar<br>uma demo com a Wati</div>
        <div style="margin-top: 24px; padding: 20px; background: var(--dark-3); border-radius: 12px; max-width: 200px; text-align: center;">
          <div style="font-size: 11px; color: var(--gray); margin-bottom: 8px; letter-spacing: 0.1em; text-transform: uppercase;">Disponível em</div>
          <div style="font-size: 13px; font-weight: 600; color: var(--gray-2);">WhatsApp API</div>
          <div style="font-size: 13px; font-weight: 600; color: var(--gray-2);">Agentes de IA · Astra</div>
          <div style="font-size: 13px; font-weight: 600; color: var(--gray-2);">Inbox Multiagente</div>
        </div>
      </div>
    </div>
  </div>
  <div class="cover-stripe"></div>
</section>

</body>
</html>
