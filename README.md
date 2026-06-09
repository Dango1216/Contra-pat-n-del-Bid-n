<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Contra Tapón - CGS SAS</title>
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@400;600;700;800;900&family=Barlow:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }
 
  body {
    font-family: 'Barlow', sans-serif;
    background: #0a0a0a;
    color: #fff;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 0;
  }
 
  .poster {
    width: 794px;
    min-height: 1123px;
    background: #f5f0e8;
    color: #1a1a1a;
    position: relative;
    overflow: hidden;
    display: flex;
    flex-direction: column;
  }
 
  /* Header strip */
  .header {
    background: #1a2e1a;
    padding: 18px 32px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 16px;
  }
 
  .org-block {
    display: flex;
    flex-direction: column;
  }
 
  .org-name {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 11px;
    font-weight: 600;
    color: #7ab87a;
    letter-spacing: 2px;
    text-transform: uppercase;
  }
 
  .dept-name {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 13px;
    font-weight: 700;
    color: #e0e0e0;
    letter-spacing: 1px;
    text-transform: uppercase;
  }
 
  .header-badge {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 10px;
    font-weight: 700;
    color: #1a2e1a;
    background: #7ab87a;
    padding: 5px 12px;
    letter-spacing: 1.5px;
    text-transform: uppercase;
  }
 
  /* Hero section */
  .hero {
    background: #1a2e1a;
    padding: 36px 40px 28px;
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 8px;
  }
 
  .hero::after {
    content: '';
    position: absolute;
    bottom: -28px;
    left: 0;
    right: 0;
    height: 28px;
    background: #1a2e1a;
    clip-path: polygon(0 0, 100% 0, 100% 0%, 0 100%);
    z-index: 2;
  }
 
  .hero-tag {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 11px;
    font-weight: 700;
    color: #7ab87a;
    letter-spacing: 3px;
    text-transform: uppercase;
    border-left: 3px solid #7ab87a;
    padding-left: 10px;
  }
 
  .hero-title {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 58px;
    font-weight: 900;
    color: #fff;
    line-height: 0.92;
    text-transform: uppercase;
    letter-spacing: -1px;
  }
 
  .hero-title span {
    color: #7ab87a;
  }
 
  .hero-sub {
    font-size: 14px;
    font-weight: 400;
    color: #a0b8a0;
    margin-top: 4px;
    line-height: 1.5;
    max-width: 480px;
  }
 
  /* Incident banner */
  .incident-band {
    background: #c8401a;
    margin-top: 28px;
    padding: 12px 40px;
    display: flex;
    align-items: center;
    gap: 14px;
  }
 
  .incident-band svg {
    flex-shrink: 0;
  }
 
  .incident-text {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 13px;
    font-weight: 600;
    color: #fff;
    letter-spacing: 0.5px;
    line-height: 1.4;
  }
 
  .incident-text strong {
    color: #ffd4c2;
    font-weight: 800;
    font-size: 14px;
  }
 
  /* Body content */
  .body-content {
    padding: 36px 40px 0;
    display: flex;
    flex-direction: column;
    gap: 28px;
    flex: 1;
  }
 
  /* Visual diagram */
  .diagram-row {
    display: flex;
    gap: 24px;
    align-items: stretch;
  }
 
  .drum-visual {
    flex-shrink: 0;
    width: 200px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background: #1a2e1a;
    border-radius: 8px;
    padding: 20px 16px;
    gap: 6px;
  }
 
  .drum-visual-title {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 12px;
    font-weight: 700;
    color: #7ab87a;
    letter-spacing: 2px;
    text-transform: uppercase;
    text-align: center;
  }
 
  .compare-panels {
    flex: 1;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }
 
  .compare-card {
    border-radius: 8px;
    padding: 20px 18px;
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
 
  .compare-card.wrong {
    background: #fdf0ec;
    border: 2px solid #e07050;
  }
 
  .compare-card.right {
    background: #eef5ee;
    border: 2px solid #4a9e4a;
  }
 
  .compare-card-label {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 11px;
    font-weight: 800;
    letter-spacing: 2.5px;
    text-transform: uppercase;
    display: flex;
    align-items: center;
    gap: 6px;
  }
 
  .compare-card.wrong .compare-card-label { color: #c8401a; }
  .compare-card.right .compare-card-label { color: #2d7e2d; }
 
  .compare-card-head {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 20px;
    font-weight: 800;
    color: #1a1a1a;
    line-height: 1.1;
  }
 
  .compare-card-body {
    font-size: 12.5px;
    color: #444;
    line-height: 1.5;
  }
 
  /* Risk chain */
  .section-title {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 16px;
    font-weight: 800;
    color: #1a2e1a;
    text-transform: uppercase;
    letter-spacing: 2px;
    border-left: 4px solid #4a9e4a;
    padding-left: 10px;
    margin-bottom: 2px;
  }
 
  .risk-row {
    display: flex;
    gap: 8px;
    align-items: stretch;
  }
 
  .risk-chip {
    flex: 1;
    background: #1a2e1a;
    border-radius: 6px;
    padding: 14px 12px;
    display: flex;
    flex-direction: column;
    gap: 6px;
    position: relative;
  }
 
  .risk-chip-icon {
    font-size: 22px;
    line-height: 1;
  }
 
  .risk-chip-title {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 13px;
    font-weight: 700;
    color: #7ab87a;
    text-transform: uppercase;
    letter-spacing: 1px;
  }
 
  .risk-chip-body {
    font-size: 11.5px;
    color: #b8ceb8;
    line-height: 1.4;
  }
 
  .risk-arrow {
    display: flex;
    align-items: center;
    color: #c8401a;
    font-size: 18px;
    font-weight: 900;
    flex-shrink: 0;
    padding-top: 8px;
  }
 
  /* Key rule */
  .key-rule {
    background: #1a2e1a;
    border-radius: 8px;
    padding: 22px 28px;
    display: flex;
    align-items: center;
    gap: 20px;
    border-left: 6px solid #7ab87a;
  }
 
  .key-rule-icon {
    font-size: 38px;
    flex-shrink: 0;
  }
 
  .key-rule-text {
    display: flex;
    flex-direction: column;
    gap: 3px;
  }
 
  .key-rule-label {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 10px;
    font-weight: 700;
    color: #7ab87a;
    letter-spacing: 2.5px;
    text-transform: uppercase;
  }
 
  .key-rule-main {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 28px;
    font-weight: 900;
    color: #fff;
    line-height: 1.05;
    text-transform: uppercase;
  }
 
  .key-rule-main span {
    color: #7ab87a;
  }
 
  .key-rule-sub {
    font-size: 12px;
    color: #9ab89a;
    line-height: 1.4;
    margin-top: 2px;
  }
 
  /* Steps */
  .steps-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
  }
 
  .step-card {
    background: #fff;
    border-radius: 8px;
    padding: 16px 12px;
    display: flex;
    flex-direction: column;
    gap: 8px;
    border: 1px solid #d0d8d0;
  }
 
  .step-num {
    width: 28px;
    height: 28px;
    background: #1a2e1a;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 15px;
    font-weight: 800;
    color: #7ab87a;
    flex-shrink: 0;
  }
 
  .step-title {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 13px;
    font-weight: 700;
    color: #1a2e1a;
    text-transform: uppercase;
    line-height: 1.2;
  }
 
  .step-body {
    font-size: 11px;
    color: #555;
    line-height: 1.4;
  }
 
  /* Footer */
  .footer {
    background: #1a2e1a;
    padding: 14px 40px;
    margin-top: 24px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
 
  .footer-left {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 10px;
    font-weight: 600;
    color: #7ab87a;
    letter-spacing: 2px;
    text-transform: uppercase;
  }
 
  .footer-right {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 10px;
    color: #6a8a6a;
    letter-spacing: 1px;
  }
 
  /* Decorative diagonal strip */
  .deco-strip {
    position: absolute;
    top: 0;
    right: 0;
    width: 6px;
    height: 100%;
    background: repeating-linear-gradient(
      180deg,
      #7ab87a 0px,
      #7ab87a 12px,
      #1a2e1a 12px,
      #1a2e1a 24px
    );
  }
</style>
</head>
<body>
<div class="poster">
  <div class="deco-strip"></div>
 
  <!-- Header -->
  <div class="header">
    <div class="org-block">
      <span class="org-name">Centro de Gestión Sostenible SAS ESP</span>
      <span class="dept-name">Gestión QSHE · Seguridad y Salud en el Trabajo</span>
    </div>
    <div class="header-badge">Comunicación SST</div>
  </div>
 
  <!-- Hero -->
  <div class="hero">
    <div class="hero-tag">Gestión de riesgo químico · OCS</div>
    <div class="hero-title">CONTRA<br><span>TAPÓN</span><br>SALVAVIDAS</div>
    <div class="hero-sub">
      El contra tapón en bidones y recipientes con sustancias químicas líquidas
      no es opcional — es la barrera que previene exposiciones graves.
    </div>
  </div>
 
  <!-- Incident band -->
  <div class="incident-band">
    <svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="#fff" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
      <path d="M10.29 3.86L1.82 18a2 2 0 001.71 3h16.94a2 2 0 001.71-3L13.71 3.86a2 2 0 00-3.42 0z"/>
      <line x1="12" y1="9" x2="12" y2="13"/><line x1="12" y1="17" x2="12.01" y2="17"/>
    </svg>
    <div class="incident-text">
      <strong>Evento real · 12/05/2026 · 10:30 AM</strong> — Durante el pesaje de un galón de sustancia química líquida,
      una gota salpicó la frente y el párpado del ojo derecho de un operario, causando ardor y enrojecimiento.
      La ausencia del contra tapón durante la manipulación facilitó la proyección.
    </div>
  </div>
 
  <!-- Body -->
  <div class="body-content">
 
    <!-- Compare panels -->
    <div>
      <div class="section-title">¿Qué marca la diferencia?</div>
      <br>
      <div class="diagram-row">
        <!-- SVG drum -->
        <div class="drum-visual">
          <div class="drum-visual-title">Recipiente con sustancia química</div>
          <!-- SVG drum illustration -->
          <svg width="140" height="160" viewBox="0 0 140 160">
            <!-- drum body -->
            <rect x="30" y="40" width="80" height="95" rx="8" fill="#2d4a2d" stroke="#7ab87a" stroke-width="1.5"/>
            <!-- drum top ellipse -->
            <ellipse cx="70" cy="40" rx="40" ry="10" fill="#3a5c3a" stroke="#7ab87a" stroke-width="1.5"/>
            <!-- drum label area -->
            <rect x="40" y="65" width="60" height="45" rx="4" fill="#1a2e1a" stroke="#5a8a5a" stroke-width="1"/>
            <text x="70" y="84" text-anchor="middle" font-family="Barlow Condensed, sans-serif" font-weight="700" font-size="9" fill="#7ab87a" letter-spacing="1">SUSTANCIA</text>
            <text x="70" y="96" text-anchor="middle" font-family="Barlow Condensed, sans-serif" font-weight="700" font-size="9" fill="#7ab87a" letter-spacing="1">QUÍMICA</text>
            <text x="70" y="108" text-anchor="middle" font-family="Barlow Condensed, sans-serif" font-size="8" fill="#5a8a5a">Líquida</text>
            <!-- ribbing lines on drum -->
            <line x1="30" y1="65" x2="110" y2="65" stroke="#5a8a5a" stroke-width="0.8"/>
            <line x1="30" y1="112" x2="110" y2="112" stroke="#5a8a5a" stroke-width="0.8"/>
            <!-- plug hole -->
            <ellipse cx="70" cy="40" rx="8" ry="2.5" fill="#c8401a" stroke="#e87050" stroke-width="1.5"/>
            <text x="70" y="30" text-anchor="middle" font-family="Barlow Condensed, sans-serif" font-weight="800" font-size="9" fill="#e87050">BOCA</text>
            <!-- down arrow to plug -->
            <line x1="70" y1="33" x2="70" y2="37" stroke="#e87050" stroke-width="1.5" marker-end="url(#a)"/>
            <defs>
              <marker id="a" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="5" markerHeight="5" orient="auto">
                <path d="M2 1L8 5L2 9" fill="none" stroke="#e87050" stroke-width="1.5" stroke-linecap="round"/>
              </marker>
            </defs>
            <!-- bottom -->
            <ellipse cx="70" cy="135" rx="40" ry="10" fill="#3a5c3a" stroke="#7ab87a" stroke-width="1.5"/>
          </svg>
          <div style="font-size:10px; color:#7ab87a; text-align:center; letter-spacing:1px; font-family:'Barlow Condensed',sans-serif; font-weight:600; text-transform:uppercase; margin-top:4px;">Punto crítico: la boca</div>
        </div>
 
        <!-- Compare cards -->
        <div class="compare-panels">
          <div class="compare-card wrong">
            <div class="compare-card-label">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round"><circle cx="12" cy="12" r="10"/><line x1="15" y1="9" x2="9" y2="15"/><line x1="9" y1="9" x2="15" y2="15"/></svg>
              Sin contra tapón
            </div>
            <div class="compare-card-head">Riesgo<br>elevado</div>
            <div class="compare-card-body">
              Derrames y salpicaduras al inclinar o mover el recipiente. Vapores concentrados escapan libremente. Un solo movimiento brusco puede generar exposición ocular o dérmica.
            </div>
          </div>
          <div class="compare-card right">
            <div class="compare-card-label">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round"><circle cx="12" cy="12" r="10"/><polyline points="9 12 11 14 15 10"/></svg>
              Con contra tapón
            </div>
            <div class="compare-card-head">Control<br>efectivo</div>
            <div class="compare-card-body">
              Sello hermético que bloquea el escape de líquido y vapores. Absorbe presión interna. Protege durante el transporte, pesaje y almacenamiento temporal del recipiente.
            </div>
          </div>
        </div>
      </div>
    </div>
 
    <!-- Risk chain -->
    <div>
      <div class="section-title">Cadena de riesgo sin contra tapón</div>
      <br>
      <div class="risk-row">
        <div class="risk-chip">
          <div class="risk-chip-icon">🔄</div>
          <div class="risk-chip-title">Movimiento</div>
          <div class="risk-chip-body">Inclinar, levantar o depositar el recipiente en la báscula</div>
        </div>
        <div class="risk-arrow">→</div>
        <div class="risk-chip">
          <div class="risk-chip-icon">💧</div>
          <div class="risk-chip-title">Salpicadura</div>
          <div class="risk-chip-body">Gota o chorro de sustancia química líquida sale por la boca</div>
        </div>
        <div class="risk-arrow">→</div>
        <div class="risk-chip">
          <div class="risk-chip-icon">👁️</div>
          <div class="risk-chip-title">Contacto</div>
          <div class="risk-chip-body">Proyección a ojos, cara o manos sin cobertura adecuada</div>
        </div>
        <div class="risk-arrow">→</div>
        <div class="risk-chip" style="background:#6a2020;">
          <div class="risk-chip-icon">🚨</div>
          <div class="risk-chip-title" style="color:#f08080;">Lesión</div>
          <div class="risk-chip-body" style="color:#c89090;">Ardor, enrojecimiento, irritación química — potencialmente grave</div>
        </div>
      </div>
    </div>
 
    <!-- Key rule -->
    <div class="key-rule">
      <div class="key-rule-icon">🔒</div>
      <div class="key-rule-text">
        <div class="key-rule-label">Regla de oro · Manejo seguro</div>
        <div class="key-rule-main">Contra tapón<br><span>siempre colocado</span></div>
        <div class="key-rule-sub">
          Antes, durante y después de cada operación con el recipiente. Verificar el sello antes de mover el bidón.
          Si el contra tapón está ausente o dañado, <strong style="color:#c8c8a0;">detén la operación y repórtalo</strong>.
        </div>
      </div>
    </div>
 
    <!-- 4 steps -->
    <div>
      <div class="section-title">Protocolo operativo · 4 pasos</div>
      <br>
      <div class="steps-grid">
        <div class="step-card">
          <div class="step-num">1</div>
          <div class="step-title">Inspección<br>previa</div>
          <div class="step-body">Verificar que el contra tapón esté instalado y en buen estado antes de manipular el recipiente.</div>
        </div>
        <div class="step-card">
          <div class="step-num">2</div>
          <div class="step-title">Apertura<br>controlada</div>
          <div class="step-body">Retirar el contra tapón solo en el momento exacto del vertido. EPP completo puesto.</div>
        </div>
        <div class="step-card">
          <div class="step-num">3</div>
          <div class="step-title">Cierre<br>inmediato</div>
          <div class="step-body">Reinstalar el contra tapón una vez finalizado el vertido o la medición. No dejar el recipiente abierto.</div>
        </div>
        <div class="step-card">
          <div class="step-num">4</div>
          <div class="step-title">Reporte<br>de falla</div>
          <div class="step-body">Si detectas un contra tapón dañado o ausente, reportarlo al supervisor antes de continuar.</div>
        </div>
      </div>
    </div>
 
  </div>
 
  <!-- Footer -->
  <div class="footer">
    <div class="footer-left">CGS SAS ESP · Gestión QSHE · Comunicación SST 2026</div>
    <div class="footer-right">Programa de Riesgo Químico · FR-CD-23 · OCS</div>
  </div>
</div>
</body>
</html>
 


