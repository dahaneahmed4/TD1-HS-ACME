<!DOCTYPE html>
<!-- removed duplicate <html> -->
<head>
  <meta charset="UTF-8">
  <title>TD N°1 - Entraînement Électrique MCC - Analyse Détaillée</title>
  <style>
    @page {
      size: A4;
      margin: 1.5cm;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Times New Roman', serif;
      line-height: 1.6;
      color: #000;
      background: white;
      padding: 20px;
      max-width: 210mm;
      margin: 0 auto;
    }

    .header {
      text-align: center;
      border-bottom: 3px solid #000;
      padding-bottom: 15px;
      margin-bottom: 25px;
    }

    .header h1 {
      font-size: 22px;
      margin: 8px 0;
      text-transform: uppercase;
    }

    .header .subtitle {
      font-size: 13px;
      font-style: italic;
      margin-top: 8px;
    }

    h2 {
      font-size: 18px;
      margin-top: 25px;
      margin-bottom: 12px;
      border-bottom: 2px solid #000;
      padding-bottom: 5px;
    }

    h3 {
      font-size: 15px;
      margin-top: 18px;
      margin-bottom: 10px;
      font-weight: bold;
    }

    h4 {
      font-size: 13px;
      margin-top: 12px;
      margin-bottom: 8px;
      font-weight: bold;
      font-style: italic;
    }

    p {
      text-align: justify;
      margin: 10px 0;
      font-size: 11pt;
    }

    .info-box, .note, .warning, .key-point {
      border: 1px solid #000;
      padding: 12px;
      margin: 15px 0;
      page-break-inside: avoid;
    }

    .info-box {
      background: #f0f0f0;
    }

    .note {
      background: #f5f5f5;
      border-left: 4px solid #000;
    }

    .warning {
      background: #fff;
      border: 2px solid #000;
    }

    .key-point {
      background: #f9f9f9;
      border-left: 5px solid #000;
      font-weight: 500;
    }

    .equation {
      background: #fafafa;
      border: 1px solid #666;
      padding: 12px;
      margin: 12px 0;
      font-family: 'Courier New', monospace;
      font-size: 11pt;
      text-align: center;
      page-break-inside: avoid;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      margin: 15px 0;
      page-break-inside: avoid;
      font-size: 10pt;
    }

    th {
      background: #e0e0e0;
      border: 1px solid #000;
      padding: 8px;
      text-align: left;
      font-weight: bold;
    }

    td {
      border: 1px solid #000;
      padding: 8px;
    }

    tr:nth-child(even) {
      background: #f5f5f5;
    }

    ul, ol {
      margin: 12px 0;
      padding-left: 25px;
    }

    li {
      margin: 6px 0;
      font-size: 11pt;
    }

    strong {
      font-weight: bold;
    }

    .formula-box {
      border: 2px solid #000;
      padding: 15px;
      margin: 15px 0;
      background: #fafafa;
      page-break-inside: avoid;
    }

    .formula-box h4 {
      margin-top: 0;
      text-decoration: underline;
    }

    .conclusion-box {
      border: 3px double #000;
      padding: 20px;
      margin: 20px 0;
      background: #f9f9f9;
    }

    .conclusion-box h3 {
      margin-top: 0;
      text-align: center;
      text-decoration: underline;
    }

    .footer {
      margin-top: 30px;
      padding-top: 15px;
      border-top: 2px solid #000;
      text-align: center;
      font-size: 10pt;
    }

    .page-break {
      page-break-after: always;
    }

    h2, h3, h4 {
      page-break-after: avoid;
    }

    @media print {
      body {
        padding: 0;
      }
    }
  </style>



  <meta charset="UTF-8">
  <title>TD N°1 - Exercice 02 - Machine Asynchrone - Analyse Détaillée</title>
  <style>
    @page {
      size: A4;
      margin: 1.5cm;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Times New Roman', serif;
      line-height: 1.6;
      color: #000;
      background: white;
      padding: 20px;
      max-width: 210mm;
      margin: 0 auto;
    }

    .header {
      text-align: center;
      border-bottom: 3px solid #000;
      padding-bottom: 15px;
      margin-bottom: 25px;
    }

    .header h1 {
      font-size: 22px;
      margin: 8px 0;
      text-transform: uppercase;
    }

    .header .subtitle {
      font-size: 13px;
      font-style: italic;
      margin-top: 8px;
    }

    h2 {
      font-size: 18px;
      margin-top: 25px;
      margin-bottom: 12px;
      border-bottom: 2px solid #000;
      padding-bottom: 5px;
    }

    h3 {
      font-size: 15px;
      margin-top: 18px;
      margin-bottom: 10px;
      font-weight: bold;
    }

    h4 {
      font-size: 13px;
      margin-top: 12px;
      margin-bottom: 8px;
      font-weight: bold;
      font-style: italic;
    }

    p {
      text-align: justify;
      margin: 10px 0;
      font-size: 11pt;
    }

    .info-box, .note, .warning, .key-point {
      border: 1px solid #000;
      padding: 12px;
      margin: 15px 0;
      page-break-inside: avoid;
    }

    .info-box {
      background: #f0f0f0;
    }

    .note {
      background: #f5f5f5;
      border-left: 4px solid #000;
    }

    .warning {
      background: #fff;
      border: 2px solid #000;
    }

    .key-point {
      background: #f9f9f9;
      border-left: 5px solid #000;
      font-weight: 500;
    }

    .equation {
      background: #fafafa;
      border: 1px solid #666;
      padding: 12px;
      margin: 12px 0;
      font-family: 'Courier New', monospace;
      font-size: 11pt;
      text-align: center;
      page-break-inside: avoid;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      margin: 15px 0;
      page-break-inside: avoid;
      font-size: 10pt;
    }

    th {
      background: #e0e0e0;
      border: 1px solid #000;
      padding: 8px;
      text-align: left;
      font-weight: bold;
    }

    td {
      border: 1px solid #000;
      padding: 8px;
    }

    tr:nth-child(even) {
      background: #f5f5f5;
    }

    ul, ol {
      margin: 12px 0;
      padding-left: 25px;
    }

    li {
      margin: 6px 0;
      font-size: 11pt;
    }

    strong {
      font-weight: bold;
    }

    .formula-box {
      border: 2px solid #000;
      padding: 15px;
      margin: 15px 0;
      background: #fafafa;
      page-break-inside: avoid;
    }

    .formula-box h4 {
      margin-top: 0;
      text-decoration: underline;
    }

    .conclusion-box {
      border: 3px double #000;
      padding: 20px;
      margin: 20px 0;
      background: #f9f9f9;
    }

    .conclusion-box h3 {
      margin-top: 0;
      text-align: center;
      text-decoration: underline;
    }

    .footer {
      margin-top: 30px;
      padding-top: 15px;
      border-top: 2px solid #000;
      text-align: center;
      font-size: 10pt;
    }

    .page-break {
      page-break-after: always;
    }

    h2, h3, h4 {
      page-break-after: avoid;
    }

    .circuit-diagram {
      border: 2px solid #000;
      padding: 20px;
      margin: 20px 0;
      text-align: center;
      background: #fafafa;
    }

    @media print {
      body {
        padding: 0;
      }
    }
  </style>



<body>
  <div class="header">
    <h1>ANALYSE APPROFONDIE ET DÉTAILLÉE</h1>
    <h1>TD N°1 - ENTRAÎNEMENT ÉLECTRIQUE À VITESSE VARIABLE</h1>
    <h1>EXERCICE 01 - MACHINE À COURANT CONTINU</h1>
    <div class="subtitle">Master 1 : Commande Électrique | Année Universitaire 2025/2026</div>
    <div class="subtitle">Matière : Techniques de la Commande Électrique</div>
  </div>

  <div class="info-box">
    <strong>Objectifs pédagogiques de l'Exercice 01 :</strong><br>
    • Maîtriser le fonctionnement de la MCC dans les 4 quadrants mécaniques<br>
    • Analyser les régimes transitoires (accélération, freinage) et permanents<br>
    • Déterminer les paramètres caractéristiques de la machine par essais<br>
    • Comprendre les bilans énergétiques et le dimensionnement des convertisseurs<br>
    • Calculer les couples et courants dans chaque phase du cycle de fonctionnement
  </div>

  <h2>I. CONTEXTE INDUSTRIEL ET PROBLÉMATIQUE</h2>

  <p>L'exercice traite d'un entraînement électrique à base de machine à courant continu (MCC) à excitation indépendante constante, associé à un convertisseur permettant le fonctionnement dans les 4 quadrants mécaniques. Ce type de système est largement utilisé dans l'industrie pour des applications nécessitant un contrôle précis de la vitesse et du couple avec possibilité de freinage électrique récupératif.</p>

  <h3>1.1 Applications Industrielles Typiques</h3>

  <p>Les machines à courant continu à excitation indépendante sont particulièrement adaptées aux applications suivantes :</p>

  <ul>
    <li><strong>Laminoirs et Trains de Laminage :</strong> Nécessitant un couple constant élevé et un contrôle précis de la vitesse pour garantir l'épaisseur du produit laminé.</li>
    
    <li><strong>Machines-Outils à Commande Numérique :</strong> Tours, fraiseuses, centres d'usinage où la précision du positionnement et la stabilité de vitesse sont critiques.</li>
    
    <li><strong>Systèmes de Levage et Manutention :</strong> Ascenseurs, grues, ponts roulants où le freinage électrique est essentiel pour la sécurité. Le freinage permet de récupérer jusqu'à 30-40% de l'énergie.</li>
    
    <li><strong>Enrouleurs et Dérouleurs :</strong> Industries papetières, textiles, sidérurgiques nécessitant un contrôle de tension constant.</li>
    
    <li><strong>Traction Ferroviaire :</strong> Métros, tramways où la récupération d'énergie au freinage peut atteindre 25-35% de la consommation totale.</li>
  </ul>

  <div class="key-point">
    <strong>Fonctionnement 4 Quadrants - Concept Fondamental :</strong><br><br>
    Le fonctionnement dans les 4 quadrants permet à la machine de travailler en moteur et en génératrice dans les deux sens de rotation :<br><br>
    
    <strong>• Quadrant I (Moteur direct) :</strong> Couple > 0, Vitesse > 0. Fonctionnement moteur normal dans le sens direct.<br><br>
    
    <strong>• Quadrant II (Freinage générateur direct) :</strong> Couple < 0, Vitesse > 0. La machine freine et renvoie de l'énergie au réseau.<br><br>
    
    <strong>• Quadrant III (Moteur inverse) :</strong> Couple < 0, Vitesse < 0. Fonctionnement moteur en sens inverse.<br><br>
    
    <strong>• Quadrant IV (Freinage générateur inverse) :</strong> Couple > 0, Vitesse < 0. Freinage en sens inverse avec récupération d'énergie.
  </div>

  <h3>1.2 Caractéristiques de la Machine Étudiée</h3>

  <ul>
    <li><strong>Type :</strong> Machine à courant continu à excitation indépendante constante</li>
    <li><strong>Vitesse nominale :</strong> N = 3000 tr/min (soit 314 rad/s)</li>
    <li><strong>Tension nominale d'induit :</strong> U ≈ 278 V</li>
    <li><strong>Résistance d'induit totale :</strong> Ra = 3 Ω (incluant l'inductance de lissage)</li>
    <li><strong>Puissance estimée :</strong> 4-5 kW</li>
    <li><strong>Hypothèses :</strong> Réaction d'induit négligée, couple de pertes constant</li>
  </ul>

  <div class="note">
    <strong>Rôle de l'Inductance de Lissage :</strong><br><br>
    L'inductance de lissage placée en série avec l'induit réduit les ondulations de courant (qui pourraient atteindre 20-30% sans elle), protège le convertisseur en limitant les di/dt, et améliore la régularité du couple.
  </div>

  <h3>1.3 Cycle de Fonctionnement Imposé</h3>

  <div class="formula-box">
    <h4>Description du Cycle Complet :</h4>
    
    <strong>Phase 1 - Accélération (0 ≤ t ≤ 1s) :</strong><br>
    • Départ à l'arrêt : N₀ = 0 tr/min<br>
    • Arrivée à vitesse : N₁ = 3000 tr/min<br>
    • Durée : Δt = 1 seconde<br>
    • Mode : Moteur en accélération (Quadrant I)<br><br>
    
    <strong>Phase 2 - Régime Permanent (1s ≤ t ≤ 2s) :</strong><br>
    • Vitesse constante : N = 3000 tr/min<br>
    • Durée : Δt = 1 seconde<br>
    • Mode : Moteur en régime établi (Quadrant I)<br><br>
    
    <strong>Phase 3 - Freinage (2s ≤ t ≤ 3s) :</strong><br>
    • Départ à vitesse : N₂ = 3000 tr/min<br>
    • Arrivée à l'arrêt : N₃ = 0 tr/min<br>
    • Durée : Δt = 1 seconde<br>
    • Mode : Freinage générateur (Quadrant II)
  </div>

  <div class="page-break"></div>

  <h2>II. ÉQUATIONS FONDAMENTALES DE LA MCC (Question 1)</h2>

  <h3>2.1 Équation Électrique du Circuit d'Induit</h3>

  <p>Le circuit d'induit est modélisé par une résistance Ra, une inductance La et une FEM E. L'équation de maille en régime transitoire :</p>

  <div class="equation">
    U = E + Ra × Ia + La × (dIa/dt)
  </div>

  <p>En régime permanent, dIa/dt = 0, donc :</p>

  <div class="equation">
    U = E + Ra × Ia
  </div>

  <p>On peut réarranger pour obtenir le courant :</p>

  <div class="equation">
    Ia = (U - E) / Ra = (U - Kf × Ω) / Ra
  </div>

  <div class="key-point">
    <strong>Interprétation Physique Fondamentale :</strong><br><br>
    La FEM E joue le rôle de régulateur naturel du courant. Plus la machine tourne vite, plus E augmente, ce qui réduit (U - E) et donc limite le courant. C'est un mécanisme d'autorégulation intrinsèque.<br><br>
    
    <strong>Cas critique au démarrage :</strong> Quand Ω = 0 → E = 0 → Ia = U / Ra = 278 / 3 ≈ 93 A. Cette valeur est environ 6 fois le courant nominal ! Sans limitation, ce courant causerait la destruction des balais, l'échauffement des enroulements, et des chocs mécaniques.
  </div>

  <h3>2.2 Équation de la Force Contre-Électromotrice</h3>

  <p>La FEM résulte du déplacement des conducteurs dans le champ magnétique. Pour une machine à excitation constante :</p>

  <div class="equation">
    E = Kf × Ω
  </div>

  <p>La constante Kf caractérise la machine et dépend du nombre de conducteurs, du nombre de paires de pôles, et du flux d'excitation maintenu constant.</p>

  <div class="note">
    <strong>Dualité électromécanique :</strong><br>
    La même constante Kf apparaît dans E = Kf × Ω (génération de tension) et Cem = Kf × Ia (production de couple). Cette dualité découle de la conservation de l'énergie : Pem = E × Ia = Cem × Ω.
  </div>

  <h3>2.3 Équation du Couple Électromagnétique</h3>

  <p>Le couple électromagnétique pour une excitation constante :</p>

  <div class="equation">
    Cem = Kf × Ia
  </div>

  <p>Cette relation linéaire simple constitue l'un des avantages majeurs de la MCC :</p>

  <ul>
    <li>Contrôle direct du couple via le courant</li>
    <li>Réponse dynamique rapide (10-50 ms)</li>
    <li>Linéarité sur toute la plage de fonctionnement</li>
    <li>Bidirectionnalité naturelle (courant négatif = couple négatif)</li>
  </ul>

  <h3>2.4 Équation Fondamentale de la Dynamique</h3>

  <p>L'équation mécanique traduit l'équilibre dynamique :</p>

  <div class="equation">
    Cem = Cr + Cp + Jt × (dΩ/dt)
  </div>

  <p>Où :</p>
  <ul>
    <li><strong>Cem :</strong> Couple électromagnétique développé (N.m)</li>
    <li><strong>Cr :</strong> Couple résistant de la charge (N.m)</li>
    <li><strong>Cp :</strong> Couple de pertes mécaniques internes (N.m)</li>
    <li><strong>Jt :</strong> Moment d'inertie total (kg.m²)</li>
    <li><strong>dΩ/dt :</strong> Accélération angulaire (rad/s²)</li>
  </ul>

  <div class="formula-box">
    <h4>Cas Particuliers :</h4>
    
    <strong>1. Régime Permanent :</strong> dΩ/dt = 0 → Cem = Cr + Cp<br><br>
    
    <strong>2. Accélération :</strong> dΩ/dt > 0 → Cem > Cr + Cp<br>
    Couple d'accélération : Ca = Cem - Cr - Cp = Jt × (dΩ/dt)<br><br>
    
    <strong>3. Freinage :</strong> dΩ/dt < 0 → Cem < Cr + Cp (ou Cem négatif)<br>
    La machine fonctionne en génératrice.
  </div>

  <div class="page-break"></div>

  <h2>III. DÉTERMINATION DE LA CONSTANTE Kf (Question 2)</h2>

  <h3>3.1 Principe de l'Essai à Vide</h3>

  <p>L'essai à vide permet de déterminer Kf et le couple de pertes Cp. À vide, la machine ne fournit aucune puissance utile, donc tout le couple électromagnétique sert à compenser les pertes internes.</p>

  <div class="note">
    <strong>Conditions de l'Essai 1 :</strong><br>
    • Vitesse : N = 3000 tr/min<br>
    • Tension : U = 278 V<br>
    • Courant : Ia = 1,05 A<br>
    • Configuration : Machine désaccouplée (à vide)
  </div>

  <h3>3.2 Calculs Détaillés</h3>

  <h4>Étape 1 : Conversion de la vitesse</h4>

  <div class="equation">
    Ω = 2π × N / 60 = 2π × 3000 / 60 = 314,16 rad/s ≈ 314 rad/s
  </div>

  <h4>Étape 2 : Calcul de la FEM</h4>

  <div class="equation">
    E = U - Ra × Ia = 278 - 3 × 1,05 = 274,85 V
  </div>

  <p>La FEM représente 98,87% de la tension appliquée, confirmant l'excellent rendement électrique à vide.</p>

  <h4>Étape 3 : Calcul de Kf</h4>

  <div class="equation">
    Kf = E / Ω = 274,85 / 314,16 = 0,875 V/(rad/s)
  </div>

  <div class="key-point">
    <strong>RÉSULTAT FONDAMENTAL :</strong><br><br>
    Kf = 0,875 V/(rad/s) = 0,875 N.m/A<br><br>
    
    <strong>Double signification :</strong><br>
    1. Constante de FEM : À chaque rad/s, la machine génère 0,875 V<br>
    2. Constante de couple : Pour chaque ampère, la machine développe 0,875 N.m
  </div>

  <h3>3.3 Calcul du Couple de Pertes</h3>

  <p>À vide, tout le couple électromagnétique compense les pertes :</p>

  <div class="equation">
    Cp = Cem(à vide) = Kf × Ia(à vide) = 0,875 × 1,05 = 0,92 N.m
  </div>

  <p>Puissance de pertes correspondante :</p>

  <div class="equation">
    Pp = Cp × Ω = 0,92 × 314 = 289 W
  </div>

  <div class="page-break"></div>

  <h2>IV. RÉGIME PERMANENT ET COUPLE RÉSISTANT (Question 3)</h2>

  <h3>4.1 Point de Fonctionnement Nominal</h3>

  <div class="note">
    <strong>Conditions de l'Essai 4 :</strong><br>
    • Vitesse : N = 3000 tr/min → Ω = 314 rad/s<br>
    • Courant : Ia = 16 A<br>
    • Configuration : Machine couplée à sa charge
  </div>

  <h3>4.2 Calcul du Couple Électromagnétique</h3>

  <div class="equation">
    Cem = Kf × Ia = 0,875 × 16 = 14,00 N.m
  </div>

  <h3>4.3 Équilibre en Régime Permanent</h3>

  <p>En régime permanent, dΩ/dt = 0, donc :</p>

  <div class="equation">
    Cem = Cr + Cp = 14 N.m
  </div>

  <p>Le couple électromagnétique compense exactement les couples résistants (charge + pertes).</p>

  <h2>V. MOMENT D'INERTIE (Question 4)</h2>

  <h3>5.1 Principe de l'Essai Dynamique</h3>

  <p>L'essai 2 réalise une accélération à courant constant permettant de calculer Jt.</p>

  <div class="note">
    <strong>Conditions de l'Essai 2 :</strong><br>
    • Courant constant : Ia = 25 A<br>
    • Durée : Δt = 1 seconde<br>
    • Vitesse initiale : N₀ = 0 tr/min<br>
    • Vitesse finale : N₁ = 1140 tr/min
  </div>

  <h3>5.2 Calculs</h3>

  <p>Couple électromagnétique :</p>

  <div class="equation">
    Cem = Kf × Ia = 0,875 × 25 = 21,875 N.m
  </div>

  <p>Vitesse finale en rad/s :</p>

  <div class="equation">
    Ωm = 2π × 1140 / 60 = 119,38 rad/s
  </div>

  <p>Accélération angulaire :</p>

  <div class="equation">
    α = ΔΩ / Δt = 119,38 / 1 = 119,38 rad/s²
  </div>

  <p>Application de l'équation de la dynamique :</p>

  <div class="equation">
    Jt = (Cem - Cr - Cp) / α = (21,875 - 14) / 119,38 = 0,066 kg.m²
  </div>

  <div class="key-point">
    <strong>RÉSULTAT :</strong> Jt = 0,066 kg.m²<br><br>
    Ce moment d'inertie représente la résistance de l'ensemble aux variations de vitesse. Il se compose de l'inertie du moteur (≈0,015 kg.m²) et de la charge (≈0,05 kg.m²).
  </div>

  <h3>5.3 Énergie Cinétique Stockée</h3>

  <p>À 314 rad/s :</p>

  <div class="equation">
    Ec = ½ × Jt × Ω² = 0,5 × 0,066 × 314² = 3254 J ≈ 3,25 kJ
  </div>

  <div class="page-break"></div>

  <h2>VI. PUISSANCE UTILE ET COUPLE UTILE (Question 5)</h2>

  <h3>6.1 Distinction entre les Couples</h3>

  <table>
    <tr>
      <th>Type</th>
      <th>Symbole</th>
      <th>Définition</th>
      <th>Calcul</th>
    </tr>
    <tr>
      <td>Électromagnétique</td>
      <td>Cem</td>
      <td>Couple développé par interaction électromagnétique</td>
      <td>Kf × Ia</td>
    </tr>
    <tr>
      <td>Pertes</td>
      <td>Cp</td>
      <td>Couple pour vaincre frottements</td>
      <td>Essai à vide</td>
    </tr>
    <tr>
      <td>Utile</td>
      <td>Cu</td>
      <td>Couple disponible sur l'arbre</td>
      <td>Cem - Cp</td>
    </tr>
  </table>

  <h3>6.2 Calcul du Couple Utile</h3>

  <p>En régime permanent avec Cem = 14 N.m et Cp = 0,92 N.m :</p>

  <div class="equation">
    Cu = Cem - Cp = 14 - 0,92 = 13,08 N.m
  </div>

  <p>Le rendement mécanique vaut :</p>

  <div class="equation">
    ηméca = Cu / Cem = 13,08 / 14 = 93,43%
  </div>

  <h3>6.3 Calcul de la Puissance Utile</h3>

  <div class="equation">
    Pu = Cu × Ω = 13,08 × 314 = 4107 W ≈ 4,11 kW
  </div>

  <h3>6.4 Bilan de Puissance</h3>

  <div class="formula-box">
    <h4>Flux de Puissance (Régime Permanent) :</h4>
    
    <strong>1. Puissance absorbée :</strong> Pa = U × Ia ≈ 4,45 kW<br>
    <strong>2. Pertes Joule :</strong> PJ = Ra × Ia² = 768 W (17%)<br>
    <strong>3. Puissance électromagnétique :</strong> Pem ≈ 4,4 kW<br>
    <strong>4. Pertes mécaniques :</strong> Pp = 289 W (6,5%)<br>
    <strong>5. Puissance utile :</strong> Pu = 4,11 kW
  </div>

  <p>Rendement global :</p>

  <div class="equation">
    η = Pu / Pa ≈ 92%
  </div>

  <div class="page-break"></div>

  <h2>VII. ANALYSE DU CYCLE COMPLET (Questions 6 et 7)</h2>

  <h3>7.1 Données du Cycle</h3>

  <div class="formula-box">
    <h4>Paramètres utilisés :</h4>
    • Kf = 0,875 V/(rad/s)<br>
    • Cr = 13,08 N.m<br>
    • Cp = 0,92 N.m<br>
    • Jt = 0,066 kg.m²<br>
    • Ω = 314 rad/s (3000 tr/min)
  </div>

  <h3>7.2 Phase 1 - Accélération (0 ≤ t ≤ 1s)</h3>

  <p>Couple électromagnétique nécessaire (selon solution) :</p>

  <div class="equation">
    Cem = 24,36 N.m
  </div>

  <p>Courant d'induit requis :</p>

  <div class="equation">
    Ia = Cem / Kf = 24,36 / 0,875 = 27,84 A
  </div>

  <div class="key-point">
    <strong>Analyse :</strong><br>
    • Courant = 174% du nominal<br>
    • Répartition : 54% pour la charge, 3% pour les pertes, 43% pour accélérer l'inertie<br>
    • Pertes Joule élevées : 2,3 kW pendant l'accélération
  </div>

  <h3>7.3 Phase 2 - Régime Permanent (1s ≤ t ≤ 2s)</h3>

  <p>En régime permanent :</p>

  <div class="equation">
    Cem = Cr + Cp = 14,00 N.m<br>
    Ia = 16,00 A
  </div>

  <p>Mode le plus économique, pertes Joule = 0,77 kW (réduction de 67%).</p>

  <h3>7.4 Phase 3 - Freinage (2s ≤ t ≤ 3s)</h3>

  <p>Couple de freinage (machine en génératrice) :</p>

  <div class="equation">
    Cem = -6,73 N.m<br>
    Ia = -7,69 A (courant négatif)
  </div>

  <div class="key-point">
    <strong>Freinage Électrique :</strong><br>
    • La machine fonctionne en génératrice (Quadrant II)<br>
    • Conversion de l'énergie cinétique (≈470 J) en énergie électrique<br>
    • Récupération de 30-40% de l'énergie<br>
    • Pas d'usure mécanique (contrairement aux freins à friction)<br>
    • Nécessite un convertisseur réversible (pont en H)
  </div>

  <h3>7.5 Synthèse du Cycle</h3>

  <table>
    <tr>
      <th>Phase</th>
      <th>Durée</th>
      <th>Vitesse</th>
      <th>Couple (N.m)</th>
      <th>Courant (A)</th>
      <th>Mode</th>
    </tr>
    <tr>
      <td>Accélération</td>
      <td>0 → 1s</td>
      <td>0 → 3000 tr/min</td>
      <td>24,36</td>
      <td>27,84</td>
      <td>Moteur (Q1)</td>
    </tr>
    <tr>
      <td>Régime permanent</td>
      <td>1s → 2s</td>
      <td>3000 tr/min</td>
      <td>14,00</td>
      <td>16,00</td>
      <td>Moteur (Q1)</td>
    </tr>
    <tr>
      <td>Freinage</td>
      <td>2s → 3s</td>
      <td>3000 → 0 tr/min</td>
      <td>-6,73</td>
      <td>-7,69</td>
      <td>Générateur (Q2)</td>
    </tr>
  </table>

  <h3>7.6 Tracé des Courbes</h3>

  <div class="formula-box">
    <h4>Description des Courbes Cem(t) et Ω(t) :</h4>
    
    <strong>Courbe de Vitesse Ω(t) :</strong><br>
    • 0 ≤ t < 1s : Rampe linéaire de 0 à 314 rad/s<br>
    • 1s ≤ t < 2s : Plateau à 314 rad/s<br>
    • 2s ≤ t ≤ 3s : Rampe linéaire de 314 à 0 rad/s<br>
    • t > 3s : Vitesse nulle (maintenue par frein mécanique)<br><br>
    
    <strong>Courbe de Couple Cem(t) :</strong><br>
    • 0 ≤ t < 1s : Palier à +24,36 N.m<br>
    • 1s ≤ t < 2s : Palier à +14,00 N.m<br>
    • 2s ≤ t ≤ 3s : Palier à -6,73 N.m<br>
    • t > 3s : Couple nul<br><br>
    
    <strong>Observations :</strong><br>
    • Les transitions sont instantanées (échelons) car la constante de temps électrique (≈20 ms) est négligeable devant la durée des phases (1 s)<br>
    • Le couple d'accélération est supérieur au couple de maintien<br>
    • Le couple de freinage est négatif (fonctionnement générateur)<br>
    • Dissymétrie accélération/freinage due aux couples résistants
  </div>

  <div class="page-break"></div>

  <h2>VIII. COMPLÉMENTS D'ANALYSE</h2>

  <h3>8.1 Bilan Énergétique Global du Cycle</h3>

  <p>Analysons l'énergie consommée et récupérée pendant le cycle complet de 3 secondes :</p>

  <h4>Phase d'Accélération (1 seconde) :</h4>

  <ul>
    <li><strong>Énergie cinétique stockée :</strong> Ec = ½ × 0,066 × (119,38)² ≈ 470 J</li>
    <li><strong>Énergie pour vaincre les résistances :</strong> (Cr + Cp) × Ωmoy × t = 14 × 59,69 × 1 ≈ 836 J</li>
    <li><strong>Pertes Joule :</strong> 3 × (27,84)² × 1 ≈ 2326 J</li>
    <li><strong>Énergie totale consommée :</strong> ≈ 3632 J</li>
  </ul>

  <h4>Phase de Régime Permanent (1 seconde) :</h4>

  <ul>
    <li><strong>Énergie utile transmise :</strong> 13,08 × 314 × 1 = 4107 J</li>
    <li><strong>Pertes mécaniques :</strong> 0,92 × 314 × 1 = 289 J</li>
    <li><strong>Pertes Joule :</strong> 3 × (16)² × 1 = 768 J</li>
    <li><strong>Énergie totale consommée :</strong> ≈ 5164 J</li>
  </ul>

  <h4>Phase de Freinage (1 seconde) :</h4>

  <ul>
    <li><strong>Énergie cinétique récupérée :</strong> ≈ 470 J</li>
    <li><strong>Énergie de la charge en descente :</strong> 13,08 × 157 × 1 ≈ 2054 J</li>
    <li><strong>Pertes mécaniques :</strong> 0,92 × 157 × 1 ≈ 144 J</li>
    <li><strong>Pertes Joule :</strong> 3 × (7,69)² × 1 ≈ 177 J</li>
    <li><strong>Énergie électrique récupérée :</strong> ≈ 2200 J</li>
  </ul>

  <div class="key-point">
    <strong>Bilan Énergétique du Cycle Complet :</strong><br><br>
    • Énergie consommée (phases 1 et 2) : 3632 + 5164 = 8796 J<br>
    • Énergie récupérée (phase 3) : 2200 J<br>
    • Énergie nette consommée : 8796 - 2200 = 6596 J<br>
    • Taux de récupération : 2200/8796 = 25%<br><br>
    
    <strong>Sans freinage électrique :</strong> L'énergie de freinage serait entièrement dissipée en chaleur dans un frein mécanique, portant la consommation totale à 8796 J. Le freinage électrique permet donc une économie d'énergie de 25% sur ce cycle.
  </div>

  <h3>8.2 Dimensionnement du Convertisseur</h3>

  <p>Le convertisseur statique doit être dimensionné pour les conditions les plus sévères du cycle :</p>

  <h4>Courant Maximal :</h4>

  <ul>
    <li><strong>Courant nominal continu :</strong> In = 16 A</li>
    <li><strong>Courant de pointe en accélération :</strong> Imax = 27,84 A (174% de In)</li>
    <li><strong>Durée de la surcharge :</strong> 1 seconde (acceptable thermiquement)</li>
    <li><strong>Dimensionnement recommandé :</strong> Convertisseur de 20-25 A continu, 30-35 A en pointe</li>
  </ul>

  <h4>Tension :</h4>

  <ul>
    <li><strong>Tension nominale :</strong> 278 V</li>
    <li><strong>Marge pour l'accélération :</strong> +15-20% → 320-335 V</li>
    <li><strong>Bus DC recommandé :</strong> 400 V (standard industriel)</li>
  </ul>

  <h4>Puissance :</h4>

  <ul>
    <li><strong>Puissance nominale :</strong> 278 × 16 ≈ 4,5 kW</li>
    <li><strong>Puissance de pointe :</strong> 322 × 27,84 ≈ 9 kW</li>
    <li><strong>Convertisseur recommandé :</strong> 5-7 kW continu, 10 kW en pointe</li>
  </ul>

  <h4>Capacité de Freinage :</h4>

  <ul>
    <li><strong>Énergie à dissiper/récupérer :</strong> 2200 J en 1 seconde = 2,2 kW</li>
    <li><strong>Solutions possibles :</strong>
      <ul>
        <li>Résistance de freinage de 3 kW (solution économique)</li>
        <li>Récupération sur le réseau via pont réversible (solution optimale énergétiquement)</li>
        <li>Stockage dans super-condensateurs (solution pour cycles répétitifs)</li>
      </ul>
    </li>
  </ul>

  <h3>8.3 Comparaison avec d'Autres Technologies</h3>

  <table>
    <tr>
      <th>Critère</th>
      <th>MCC Excitation Indép.</th>
      <th>MAS + Variateur</th>
      <th>MSAP + Variateur</th>
    </tr>
    <tr>
      <td>Contrôle du couple</td>
      <td>Excellent (linéaire)</td>
      <td>Bon</td>
      <td>Excellent</td>
    </tr>
    <tr>
      <td>Rendement</td>
      <td>85-92%</td>
      <td>88-93%</td>
      <td>92-96%</td>
    </tr>
    <tr>
      <td>Maintenance</td>
      <td>Élevée (balais)</td>
      <td>Faible</td>
      <td>Très faible</td>
    </tr>
    <tr>
      <td>Coût système</td>
      <td>Moyen</td>
      <td>Faible</td>
      <td>Élevé</td>
    </tr>
    <tr>
      <td>Dynamique</td>
      <td>Excellente</td>
      <td>Bonne</td>
      <td>Excellente</td>
    </tr>
    <tr>
      <td>Freinage régénératif</td>
      <td>Excellent</td>
      <td>Bon</td>
      <td>Excellent</td>
    </tr>
    <tr>
      <td>Durée de vie</td>
      <td>Moyenne (balais)</td>
      <td>Longue</td>
      <td>Très longue</td>
    </tr>
  </table>

  <div class="note">
    <strong>Évolution Technologique :</strong><br><br>
    La MCC à excitation indépendante, bien que performante, est progressivement remplacée dans les nouvelles installations par :<br>
    • Les machines asynchrones avec variateurs de fréquence (solution économique pour 80% des applications)<br>
    • Les machines synchrones à aimants permanents (MSAP) avec variateurs vectoriels (hautes performances)<br><br>
    
    Cependant, la MCC reste irremplaçable pour :<br>
    • Les installations existantes (parc important)<br>
    • La formation (compréhension simple des principes)<br>
    • Certaines applications spécifiques (très forte puissance, traction ferroviaire historique)
  </div>

  <h3>8.4 Stratégies de Régulation</h3>

  <p>Pour optimiser les performances de l'entraînement, plusieurs boucles de régulation peuvent être mises en œuvre :</p>

  <h4>Régulation en Cascade (Architecture Classique) :</h4>

  <ul>
    <li><strong>Boucle interne de courant :</strong> Très rapide (≈1-5 ms), limite le courant, protège le convertisseur et la machine</li>
    <li><strong>Boucle intermédiaire de vitesse :</strong> Moyenne (≈50-200 ms), maintient la vitesse de consigne</li>
    <li><strong>Boucle externe de position :</strong> Lente (≈500 ms), assure le positionnement précis (si nécessaire)</li>
  </ul>

  <h4>Types de Régulateurs :</h4>

  <ul>
    <li><strong>PI (Proportionnel-Intégral) :</strong> Standard pour vitesse et courant, élimine l'erreur statique</li>
    <li><strong>PID :</strong> Pour position, améliore la dynamique mais sensible au bruit</li>
    <li><strong>Régulateurs adaptatifs :</strong> Pour compenser les variations de charge ou d'inertie</li>
  </ul>

  <h4>Lois de Commande Avancées :</h4>

  <ul>
    <li><strong>Limitation de rampe :</strong> Évite les à-coups mécaniques en limitant dΩ/dt</li>
    <li><strong>Feedforward de charge :</strong> Anticipe les variations de Cr pour améliorer la réponse</li>
    <li><strong>Anti-windup :</strong> Empêche la saturation de l'intégrateur en limitation de courant</li>
    <li><strong>Gestion des transitions :</strong> Passages doux entre modes moteur et générateur</li>
  </ul>

  <div class="page-break"></div>

  <h3>8.5 Aspects Pratiques et Sécurité</h3>

  <h4>Protections Nécessaires :</h4>

  <ul>
    <li><strong>Surintensité :</strong> Détection et limitation à 150-200% de In</li>
    <li><strong>Survitesse :</strong> Détection au-delà de 110% de Nn, arrêt d'urgence</li>
    <li><strong>Thermique moteur :</strong> Sonde PTC ou calcul du modèle thermique</li>
    <li><strong>Perte d'excitation :</strong> Surveillance du courant d'excitation (critique pour MCC)</li>
    <li><strong>Court-circuit :</strong> Protection rapide des semiconducteurs</li>
    <li><strong>Surtension bus DC :</strong> Limitation à 120% de la tension nominale</li>
  </ul>

  <h4>Maintenance Préventive :</h4>

  <table>
    <tr>
      <th>Élément</th>
      <th>Fréquence</th>
      <th>Action</th>
    </tr>
    <tr>
      <td>Balais</td>
      <td>500-2000 h</td>
      <td>Inspection visuelle, remplacement si usure > 50%</td>
    </tr>
    <tr>
      <td>Collecteur</td>
      <td>1000-3000 h</td>
      <td>Nettoyage, vérification planéité, rodage si nécessaire</td>
    </tr>
    <tr>
      <td>Roulements</td>
      <td>5000-10000 h</td>
      <td>Graissage, contrôle vibratoire, remplacement</td>
    </tr>
    <tr>
      <td>Isolation</td>
      <td>Annuel</td>
      <td>Mesure résistance d'isolement (> 1 MΩ)</td>
    </tr>
    <tr>
      <td>Convertisseur</td>
      <td>Annuel</td>
      <td>Dépoussiérage, test ventilateurs, contrôle connexions</td>
    </tr>
  </table>

  <h4>Pannes Courantes et Diagnostic :</h4>

  <ul>
    <li><strong>Étincelles excessives au collecteur :</strong> Balais usés, collecteur sale, surcharge, réglage calage balais</li>
    <li><strong>Vibrations anormales :</strong> Déséquilibre rotor, roulements usés, fixation desserrée</li>
    <li><strong>Échauffement excessif :</strong> Surcharge prolongée, ventilation insuffisante, court-circuit spires</li>
    <li><strong>Perte de couple :</strong> Chute de tension d'excitation, problème convertisseur, usure balais</li>
    <li><strong>Instabilité de vitesse :</strong> Réglage régulateur, problème capteur, ondulations convertisseur</li>
  </ul>

  <div class="page-break"></div>

  <div class="conclusion-box">
    <h3>CONCLUSION GÉNÉRALE DE L'EXERCICE</h3>
    
    <p>Cet exercice complet sur la machine à courant continu à excitation indépendante a permis d'approfondir de nombreux aspects essentiels des entraînements électriques à vitesse variable. Les principaux enseignements sont :</p>
    
    <h4>1. Méthodologie de Caractérisation :</h4>
    
    <p>Par des essais judicieusement choisis (à vide, en charge, dynamique), nous avons déterminé l'ensemble des paramètres de la machine : Kf = 0,875 V/(rad/s), Cp = 0,92 N.m, Jt = 0,066 kg.m². Cette approche expérimentale systématique est applicable à toute machine électrique et constitue une compétence fondamentale de l'ingénieur en électrotechnique.</p>
    
    <h4>2. Maîtrise des Régimes de Fonctionnement :</h4>
    
    <p>L'analyse détaillée du cycle complet (accélération, régime permanent, freinage) a révélé la nécessité d'adapter dynamiquement le couple et le courant à chaque phase. Cette flexibilité, obtenue par un contrôle en boucle fermée du convertisseur, est l'atout majeur des entraînements modernes face aux solutions mécaniques traditionnelles.</p>
    
    <h4>3. Importance de l'Inertie :</h4>
    
    <p>Le moment d'inertie Jt = 0,066 kg.m² influence directement les performances dynamiques et le dimensionnement du convertisseur. Dans les applications réelles, la réduction ou l'optimisation de l'inertie peut apporter des gains significatifs en efficacité énergétique et en productivité (cycles plus rapides).</p>
    
    <h4>4. Efficacité Énergétique et Freinage Régénératif :</h4>
    
    <p>Le freinage électrique permet de récupérer environ 25% de l'énergie consommée sur ce cycle. Pour des applications avec des cycles répétitifs (ascenseurs, métros, machines-outils), cette récupération peut représenter des économies substantielles sur la consommation annuelle totale.</p>
    
    <h4>5. Bilans Énergétiques et Rendement :</h4>
    
    <p>Le rendement global d'environ 92% en régime nominal est satisfaisant, mais les pertes Joule augmentent fortement en transitoire (2,3 kW vs 0,77 kW). Cela souligne l'importance de limiter la durée et la fréquence des phases d'accélération/freinage pour optimiser l'efficacité.</p>
    
    <h4>6. Conception et Dimensionnement :</h4>
    
    <p>L'analyse a montré que le convertisseur doit être dimensionné pour les conditions de pointe (27,84 A, 9 kW) et non pour le régime nominal (16 A, 4,5 kW). C'est un principe général du dimensionnement des entraînements : toujours considérer les transitoires et les cas extrêmes.</p>
    
    <h4>7. Fonctionnement 4 Quadrants :</h4>
    
    <p>La capacité à fonctionner en moteur et en générateur dans les deux sens de rotation offre une flexibilité totale pour les applications industrielles modernes. Cependant, cela nécessite un convertisseur réversible (pont en H) plus complexe et coûteux qu'un simple hacheur unidirectionnel.</p>
    
    <h4>8. Limites et Perspectives :</h4>
    
    <p>Malgré ses excellentes performances en contrôle de couple et sa simplicité conceptuelle, la MCC présente des inconvénients (maintenance du collecteur, étincelles, rendement limité) qui expliquent son remplacement progressif par des solutions sans balais (MAS + variateur, MSAP) dans les installations neuves. Néanmoins, elle reste un outil pédagogique précieux car elle illustre de manière directe et intuitive les principes fondamentaux de la conversion électromécanique.</p>
    
    <h4>Applications Pratiques Directes :</h4>
    
    <p>Les connaissances acquises dans cet exercice s'appliquent directement à :</p>
    <ul>
      <li>La sélection et le dimensionnement d'entraînements pour applications industrielles</li>
      <li>Le réglage et l'optimisation de régulateurs de vitesse et de courant</li>
      <li>Le diagnostic de pannes et la maintenance prédictive</li>
      <li>L'estimation des consommations énergétiques et des économies potentielles</li>
      <li>La conception de profils de mouvement optimaux (compromis temps/énergie)</li>
    </ul>
    
    <h4>Compétences Développées :</h4>
    
    <ul>
      <li>Analyse systémique d'un entraînement électromécanique</li>
      <li>Exploitation judicieuse des essais expérimentaux</li>
      <li>Bilans énergétiques et thermiques</li>
      <li>Dimensionnement de convertisseurs statiques</li>
      <li>Compréhension des couplages électromécaniques</li>
      <li>Démarche méthodique de résolution de problèmes complexes</li>
    </ul>
    
    <p><strong>En conclusion,</strong> cet exercice illustre parfaitement l'appr
  <div class="header">
    <h1>ANALYSE APPROFONDIE ET DÉTAILLÉE</h1>
    <h1>TD N°1 - ENTRAÎNEMENT ÉLECTRIQUE À VITESSE VARIABLE</h1>
    <h1>EXERCICE 02 - MACHINE ASYNCHRONE (MAS)</h1>
    <div class="subtitle">Master 1 : Commande Électrique | Année Universitaire 2025/2026</div>
    <div class="subtitle">Matière : Techniques de la Commande Électrique</div>
  </div>

  <div class="info-box">
    <strong>Objectifs pédagogiques de l'Exercice 02 :</strong><br>
    • Comprendre le modèle mathématique de la MAS en régime permanent dans le repère (d,q)<br>
    • Établir le schéma équivalent monophasé de la machine asynchrone<br>
    • Analyser la relation entre tension, fréquence et couple<br>
    • Calculer le couple maximum et comprendre ses conditions d'obtention<br>
    • Maîtriser les principes de la commande scalaire V/f constant<br>
    • Comprendre l'influence du glissement sur les performances de la machine
  </div>

  <h2>I. CONTEXTE ET IMPORTANCE DE LA MACHINE ASYNCHRONE</h2>

  <h3>1.1 Prédominance de la MAS dans l'Industrie</h3>

  <p>La machine asynchrone (MAS) représente aujourd'hui environ 85-90% des moteurs électriques utilisés dans l'industrie mondiale. Cette prédominance s'explique par ses nombreux avantages par rapport aux autres types de machines électriques :</p>

  <ul>
    <li><strong>Robustesse exceptionnelle :</strong> Construction simple sans collecteur ni balais, résistance aux environnements difficiles (poussière, humidité, températures extrêmes)</li>
    
    <li><strong>Faible coût de fabrication :</strong> Rotor à cage d'écureuil particulièrement économique (barres d'aluminium ou de cuivre coulées), pas d'aimants permanents coûteux</li>
    
    <li><strong>Maintenance minimale :</strong> Pas de pièces d'usure (balais, collecteur), durée de vie typique de 20-30 ans avec maintenance réduite au graissage des roulements</li>
    
    <li><strong>Fiabilité élevée :</strong> Taux de panne très faible (< 2% par an), disponibilité supérieure à 98% dans les applications industrielles</li>
    
    <li><strong>Large gamme de puissance :</strong> De quelques watts (ventilateurs) à plusieurs mégawatts (compresseurs, pompes industrielles, propulsion navale)</li>
    
    <li><strong>Normalisation mondiale :</strong> Standards CEI, NEMA permettant l'interchangeabilité et la disponibilité universelle</li>
  </ul>

  <h3>1.2 Applications Typiques de la MAS</h3>

  <p>La machine asynchrone équipe la majorité des entraînements industriels modernes :</p>

  <ul>
    <li><strong>Pompes et Ventilateurs :</strong> 40-50% des applications MAS, fonctionnement en charge quadratique (C ∝ Ω²)</li>
    <li><strong>Compresseurs :</strong> Industriels, frigorifiques, climatisation, fonctionnement à couple constant ou variable</li>
    <li><strong>Convoyeurs et Manutention :</strong> Bandes transporteuses, ascenseurs, grues, couple constant</li>
    <li><strong>Machines-Outils :</strong> Tours, fraiseuses, perceuses avec variateurs de fréquence</li>
    <li><strong>Traction Électrique :</strong> Trains, métros, tramways modernes avec onduleurs de tension</li>
    <li><strong>Électroménager :</strong> Lave-linge, lave-vaisselle, réfrigérateurs (moteurs à cage simple)</li>
  </ul>

  <div class="key-point">
    <strong>Évolution Technologique - Commande Scalaire vs Vectorielle :</strong><br><br>
    
    <strong>Commande Scalaire (V/f constant) :</strong><br>
    • Principe simple : maintien du rapport tension/fréquence constant<br>
    • Contrôle de la vitesse sans capteur<br>
    • Précision modérée (±1-2% de glissement)<br>
    • Coût réduit<br>
    • Applications : pompes, ventilateurs, convoyeurs simples (70% du marché)<br><br>
    
    <strong>Commande Vectorielle (à flux orienté) :</strong><br>
    • Contrôle découplé du flux et du couple<br>
    • Performances dynamiques comparables à la MCC<br>
    • Précision élevée (±0,01%)<br>
    • Coût plus élevé<br>
    • Applications : machines-outils, robotique, traction (30% du marché)<br><br>
    
    <strong>Cet exercice se concentre sur la commande scalaire</strong>, qui reste la plus utilisée pour sa simplicité et son excellent rapport performances/coût.
  </div>

  <h3>1.3 Principe de Fonctionnement de la MAS</h3>

  <p>Le fonctionnement de la machine asynchrone repose sur trois principes physiques fondamentaux :</p>

  <h4>1. Création du Champ Tournant Statorique</h4>

  <p>Le stator triphasé alimenté par des tensions sinusoïdales déphasées de 120° crée un champ magnétique tournant à la vitesse de synchronisme :</p>

  <div class="equation">
    Ωs = ωs / p = 2π × fs / p
  </div>

  <p>Où :</p>
  <ul>
    <li><strong>Ωs :</strong> Vitesse angulaire de synchronisme (rad/s)</li>
    <li><strong>ωs :</strong> Pulsation statorique (rad/s)</li>
    <li><strong>fs :</strong> Fréquence d'alimentation (Hz)</li>
    <li><strong>p :</strong> Nombre de paires de pôles</li>
  </ul>

  <h4>2. Induction de Courants Rotoriques</h4>

  <p>Le champ tournant coupe les conducteurs du rotor. Puisque le rotor tourne à une vitesse Ω différente de Ωs, il y a une variation relative de flux induisant des fem et des courants rotoriques selon la loi de Faraday-Lenz. La fréquence rotorique est :</p>

  <div class="equation">
    fr = g × fs où g = (Ωs - Ω) / Ωs
  </div>

  <p>Le <strong>glissement g</strong> représente l'écart relatif entre la vitesse du champ et celle du rotor. C'est le paramètre fondamental de fonctionnement de la MAS.</p>

  <h4>3. Production du Couple Électromagnétique</h4>

  <p>L'interaction entre le champ tournant statorique et les courants rotoriques induits produit un couple électromagnétique (loi de Laplace) qui tend à entraîner le rotor dans le sens du champ tournant.</p>

  <div class="note">
    <strong>Caractéristique Fondamentale de la MAS :</strong><br><br>
    La machine asynchrone ne peut jamais atteindre la vitesse de synchronisme en fonctionnement moteur. Si Ω = Ωs, alors g = 0, donc fr = 0, et aucun courant n'est induit dans le rotor, donc aucun couple n'est produit. <br><br>
    
    Le rotor doit nécessairement "glisser" par rapport au champ tournant pour qu'un couple soit développé. En fonctionnement nominal, le glissement est typiquement de 2-5% (g = 0,02 à 0,05).
  </div>

  <div class="page-break"></div>

  <h2>II. MODÈLE MATHÉMATIQUE DE LA MAS EN RÉGIME PERMANENT</h2>

  <h3>2.1 Présentation du Modèle dans le Repère (d,q)</h3>

  <p>Le modèle de la machine asynchrone en régime permanent sinusoïdal utilise la représentation complexe des grandeurs électriques. Les tensions, courants et flux sont représentés par des vecteurs complexes (ou phaseurs) dans le plan complexe (d,q) :</p>

  <div class="equation">
    Vs = Vds + j×Vqs<br>
    Is = Ids + j×Iqs<br>
    Ir = Idr + j×Iqr
  </div>

  <p>Cette représentation transforme les équations différentielles temporelles en équations algébriques complexes, grandement simplifiant l'analyse en régime permanent.</p>

  <h3>2.2 Équations du Modèle Complet</h3>

  <p>Le modèle complet de la MAS en régime permanent est donné par les équations suivantes :</p>

  <div class="formula-box">
    <h4>Équations Électriques Statoriques :</h4>
    
    <strong>Circuit statorique :</strong><br>
    Vs = Rs×Is + j×ωs×Ls×Is + j×ωs×Lm×Ir
    <br><br>
    
    Avec :<br>
    • Vs : Tension statorique complexe (V)<br>
    • Rs : Résistance d'une phase statorique (Ω)<br>
    • Is : Courant statorique complexe (A)<br>
    • Ls : Inductance totale statorique = Lσs + Lm (H)<br>
    • Lσs : Inductance de fuite statorique (H)<br>
    • Lm : Inductance magnétisante mutuelle (H)<br>
    • ωs : Pulsation statorique = 2π×fs (rad/s)
  </div>

  <div class="formula-box">
    <h4>Équations Électriques Rotoriques :</h4>
    
    <strong>Circuit rotorique (ramené au stator) :</strong><br>
    0 = R'r×I'r + j×g×ωs×L'r×I'r + j×g×ωs×Lm×Is
    <br><br>
    
    Ou réarrangé :<br>
    Vs×(Lm/Ls) = (R'r/g)×I'r + j×ωs×Lσ×I'r
    <br><br>
    
    Avec :<br>
    • R'r : Résistance rotorique ramenée au stator (Ω)<br>
    • I'r : Courant rotorique ramené au stator (A)<br>
    • L'r : Inductance totale rotorique = Lσr + Lm (H)<br>
    • g : Glissement = (Ωs - Ω) / Ωs<br>
    • Lσ : Inductance de fuite totale = Lσs + Lσr (H)
  </div>

  <div class="formula-box">
    <h4>Relation entre Courants :</h4>
    
    Le courant statorique se décompose en deux composantes :<br><br>
    
    Is = I'r + Im
    <br><br>
    
    Où :<br>
    • I'r : Courant rotorique ramené au stator (crée le couple)<br>
    • Im : Courant magnétisant (crée le flux mutuel)<br><br>
    
    Avec : Im = (Lm/Ls) × Is
  </div>

  <h3>2.3 Notion de Grandeurs Ramenées au Stator</h3>

  <p>Les grandeurs rotoriques (tension, courant, résistance, inductance) sont "ramenées au stator" par une transformation équivalente au rapport de transformation d'un transformateur. Cette opération permet de travailler avec un schéma équivalent monophasé simple où stator et rotor sont directement couplés magnétiquement.</p>

  <div class="equation">
    Rapport de transformation : m = Ns / Nr<br><br>
    
    Grandeurs ramenées :<br>
    V'r = m × Vr<br>
    I'r = Ir / m<br>
    R'r = m² × Rr<br>
    L'r = m² × Lr
  </div>

  <div class="key-point">
    <strong>Signification Physique du Glissement :</strong><br><br>
    
    Le glissement g caractérise entièrement le point de fonctionnement de la MAS :<br><br>
    
    <strong>• g = 1 :</strong> Rotor à l'arrêt (Ω = 0), démarrage<br>
    - Fréquence rotorique = fs (maximale)<br>
    - Courants rotoriques maximaux<br>
    - Couple de démarrage Cd<br><br>
    
    <strong>• 0 < g < gmax :</strong> Fonctionnement moteur normal<br>
    - g nominal ≈ 0,02 à 0,05 (2-5%)<br>
    - Zone stable de la caractéristique C(g)<br><br>
    
    <strong>• g = gmax :</strong> Point de couple maximum<br>
    - gmax ≈ 0,1 à 0,3 selon la machine<br>
    - Couple de décrochage Cmax<br><br>
    
    <strong>• g < 0 :</strong> Fonctionnement générateur<br>
    - Ω > Ωs (survitesse)<br>
    - La machine restitue de la puissance au réseau<br><br>
    
    <strong>• g > 1 :</strong> Fonctionnement en freinage hypersynchrone<br>
    - Rotation en sens inverse du champ tournant
  </div>

  <div class="page-break"></div>

  <h2>III. SCHÉMA ÉQUIVALENT MONOPHASÉ (Question a)</h2>

  <h3>3.1 Dérivation du Schéma Équivalent</h3>

  <p>À partir des équations du modèle en régime permanent, on peut établir un schéma électrique équivalent monophasé par phase de la machine asynchrone. Ce schéma est analogue à celui d'un transformateur avec un enroulement secondaire particulier.</p>

  <h4>Étape 1 : Équation statorique</h4>

  <p>L'équation statorique peut s'écrire :</p>

  <div class="equation">
    Vs = Rs×Is + j×ωs×Lσs×Is + j×ωs×Lm×(Is + I'r)
  </div>

  <p>Cette équation se traduit par :</p>
  <ul>
    <li>Une résistance Rs (pertes Joule stator)</li>
    <li>Une réactance de fuite Xσs = ωs×Lσs</li>
    <li>Une branche magnétisante en parallèle (réactance Xm = ωs×Lm)</li>
  </ul>

  <h4>Étape 2 : Équation rotorique</h4>

  <p>L'équation rotorique ramenée au stator s'écrit :</p>

  <div class="equation">
    0 = (R'r/g)×I'r + j×ωs×Lσr×I'r - j×ωs×Lm×Is
  </div>

  <p>On peut décomposer R'r/g en deux parties :</p>

  <div class="equation">
    R'r/g = R'r + R'r×(1-g)/g
  </div>

  <p>Où :</p>
  <ul>
    <li><strong>R'r :</strong> Représente les pertes Joule rotoriques</li>
    <li><strong>R'r×(1-g)/g :</strong> Représente la puissance mécanique convertie</li>
  </ul>

  <h3>3.2 Schéma Équivalent Complet</h3>

  <div class="circuit-diagram">
    <h4>Schéma Équivalent Monophasé de la MAS</h4>
    <pre style="font-family: monospace; font-size: 10pt; text-align: left; display: inline-block;">
    
    Rs       Xσs=ωs×Lσs              Xσr=ωs×Lσr      R'r/g
   ┌───┐    ┌────┐              ┌────┐    ┌───┐
   │   │    │    │              │    │    │   │
Vs ○───┴────┴────●──────────────┴────┴────┴───○
   │             │                              │
   │             │      Xm=ωs×Lm                │
   │             │      ┌────┐                  │
   │             └──────┤    ├──────────────────┘
   │                    └────┘
   │                                             
   └─────────────────────────────────────────────┘
   
   Légende :
   • Vs : Tension simple statorique
   • Rs : Résistance statorique
   • Xσs : Réactance de fuite statorique
   • Xm : Réactance magnétisante
   • Xσr : Réactance de fuite rotorique (ramenée)
   • R'r/g : Résistance rotorique totale (ramenée)
    </pre>
  </div>

  <h3>3.3 Interprétation des Éléments du Schéma</h3>

  <table>
    <tr>
      <th>Élément</th>
      <th>Symbole</th>
      <th>Signification Physique</th>
      <th>Valeur Typique</th>
    </tr>
    <tr>
      <td>Résistance statorique</td>
      <td>Rs</td>
      <td>Pertes Joule dans les enroulements stator</td>
      <td>1-5% de Zn</td>
    </tr>
    <tr>
      <td>Réactance fuite stator</td>
      <td>Xσs</td>
      <td>Flux de fuite ne traversant pas l'entrefer</td>
      <td>5-10% de Zn</td>
    </tr>
    <tr>
      <td>Réactance magnétisante</td>
      <td>Xm</td>
      <td>Flux principal traversant l'entrefer</td>
      <td>100-300% de Zn</td>
    </tr>
    <tr>
      <td>Réactance fuite rotor</td>
      <td>Xσr</td>
      <td>Flux de fuite rotorique (ramené au stator)</td>
      <td>5-10% de Zn</td>
    </tr>
    <tr>
      <td>Résistance rotorique</td>
      <td>R'r</td>
      <td>Pertes Joule dans les barres du rotor</td>
      <td>2-8% de Zn</td>
    </tr>
    <tr>
      <td>Résistance mécanique</td>
      <td>R'r×(1-g)/g</td>
      <td>Puissance mécanique transmise à la charge</td>
      <td>Variable avec g</td>
    </tr>
  </table>

  <p><em>Note : Zn = Vn/In est l'impédance nominale de la machine</em></p>

  <h3>3.4 Analogie avec le Transformateur</h3>

  <p>Le schéma équivalent de la MAS ressemble fortement à celui d'un transformateur, avec quelques différences essentielles :</p>

  <table>
    <tr>
      <th>Aspect</th>
      <th>Transformateur</th>
      <th>Machine Asynchrone</th>
    </tr>
    <tr>
      <td>Couplage magnétique</td>
      <td>Fixe et parfait (k ≈ 1)</td>
      <td>Par entrefer (k ≈ 0,9-0,95)</td>
    </tr>
    <tr>
      <td>Fréquence secondaire</td>
      <td>Égale au primaire (f1 = f2)</td>
      <td>Dépend du glissement (fr = g×fs)</td>
    </tr>
    <tr>
      <td>Résistance secondaire</td>
      <td>Fixe (R2)</td>
      <td>Variable avec la vitesse (R'r/g)</td>
    </tr>
    <tr>
      <td>Puissance secondaire</td>
      <td>Électrique (charge électrique)</td>
      <td>Mécanique (charge mécanique)</td>
    </tr>
    <tr>
      <td>Point de fonctionnement</td>
      <td>Déterminé par la charge</td>
      <td>Déterminé par Cr et Ωs</td>
    </tr>
  </table>

  <div class="key-point">
    <strong>Importance du Schéma Équivalent :</strong><br><br>
    
    Le schéma équivalent monophasé permet de :<br><br>
    
    <strong>1. Calculer les performances :</strong><br>
    • Courants statorique et rotorique<br>
    • Couple électromagnétique<br>
    • Rendement et facteur de puissance<br>
    • Pertes par effet Joule et pertes fer<br><br>
    
    <strong>2. Analyser le fonctionnement :</strong><br>
    • Caractéristique couple-vitesse C(Ω)<br>
    • Influence des paramètres (Rs, R'r, Lσ)<br>
    • Comportement au démarrage et en surcharge<br><br>
    
    <strong>3. Dimensionner la commande :</strong><br>
    • Choix du variateur de fréquence<br>
    • Calcul des courants de démarrage<br>
    • Stratégie de commande scalaire V/f
  </div>

  <div class="page-break"></div>

  <h2>IV. COUPLE ÉLECTROMAGNÉTIQUE DE LA MAS</h2>

  <h3>4.1 Expression Générale du Couple</h3>

  <p>Le couple électromagnétique de la machine asynchrone s'exprime à partir de la puissance électromagnétique transmise au rotor :</p>

  <div class="equation">
    Ce = Pe / Ωs
  </div>

  <p>Où :</p>
  <ul>
    <li><strong>Pe :</strong> Puissance électromagnétique transmise au rotor (W)</li>
    <li><strong>Ωs :</strong> Vitesse angulaire de synchronisme (rad/s)</li>
  </ul>

  <p>La puissance électromagnétique correspond aux pertes dans la résistance fictive R'r×(1-g)/g du schéma équivalent :</p>

  <div class="equation">
    Pe = 3 × R'r × (1-g)/g × |I'r|²
  </div>

  <p>D'où l'expression du couple :</p>

  <div class="equation">
    Ce = 3 × R'r × |I'r|² / (g × ωs)
  </div>

  <p>Ou encore, en utilisant Ωs = ωs/p (p = nombre de paires de pôles) :</p>

  <div class="equation">
    Ce = 3p × R'r × |I'r|² / (g × ωs)
  </div>

  <h3>4.2 Expression du Courant Rotorique</h3>
<p>À partir du schéma équivalent avec Rs négligée (Rs → 0), le circuit se simplifie considérablement. Le courant rotorique devient :</p>

  <div class="equation">
    I'r = Vs / [R'r/g + j×ωs×Lσ]
  </div>

  <p>Où Lσ = Lσs + Lσr est l'inductance de fuite totale (on suppose Xm >> Xσ, donc le courant magnétisant est négligeable devant I'r).</p>

  <p>Le module du courant rotorique est :</p>

  <div class="equation">
    |I'r| = Vs / √[(R'r/g)² + (ωs×Lσ)²]
  </div>

  <h3>4.3 Expression Complète du Couple</h3>

  <p>En substituant l'expression de |I'r|² dans celle du couple :</p>

  <div class="equation">
    Ce = 3p × R'r × Vs² / {g × ωs × [(R'r/g)² + (ωs×Lσ)²]}
  </div>

  <p>Développons le dénominateur :</p>

  <div class="equation">
    Ce = 3p × R'r × Vs² / {g × ωs × [R'r²/g² + (ωs×Lσ)²]}
  </div>

  <p>Multiplions numérateur et dénominateur par g² :</p>

  <div class="equation">
    Ce = 3p × g × R'r × Vs² / {ωs × [R'r² + g²×(ωs×Lσ)²]}
  </div>

  <div class="formula-box">
    <h4>Expression Finale du Couple (avec Rs → 0) :</h4>
    
    <strong>Forme 1 (en fonction de g) :</strong><br>
    Ce = [3p × Vs² / ωs] × [g × R'r / (R'r² + g²×(ωs×Lσ)²)]
    <br><br>
    
    <strong>Forme 2 (notation alternative) :</strong><br>
    Ce = [3p × Vs² / ωs] × [g × R'r / (R'r² + g²×ωs²×Lσ²)]
    <br><br>
    
    Cette expression montre que le couple dépend de :<br>
    • La tension d'alimentation Vs (proportionnel à Vs²)<br>
    • La fréquence d'alimentation ωs (inversement proportionnel)<br>
    • Le glissement g (relation non linéaire)<br>
    • Les paramètres de la machine (R'r, Lσ, p)
  </div>

  <div class="note">
    <strong>Observations Importantes :</strong><br><br>
    
    <strong>1. Dépendance en Vs²/ωs :</strong><br>
    Le couple est proportionnel au carré de la tension et inversement proportionnel à la fréquence. Cela justifie la loi de commande V/f = constante pour maintenir le couple disponible constant à toutes les vitesses.<br><br>
    
    <strong>2. Influence du glissement :</strong><br>
    La relation entre couple et glissement est non linéaire. Pour les faibles glissements (g petit, fonctionnement normal), le couple est approximativement proportionnel à g. Pour les forts glissements (démarrage, surcharge), la relation devient plus complexe.<br><br>
    
    <strong>3. Pertes négligées :</strong><br>
    L'hypothèse Rs → 0 simplifie les calculs mais introduit une légère erreur, surtout à basse fréquence où Rs devient significative par rapport aux réactances. Les variateurs modernes compensent cet effet.
  </div>

  <div class="page-break"></div>

  <h2>V. CALCUL DU COUPLE MAXIMUM (Question b)</h2>

  <h3>5.1 Recherche du Glissement Optimal</h3>

  <p>Le couple maximum (ou couple de décrochage) correspond à un point particulier de la caractéristique C(g). Pour le trouver, on cherche le glissement qui annule la dérivée du couple par rapport au glissement :</p>

  <div class="equation">
    dCe/dg = 0
  </div>

  <p>Reprenons l'expression du couple avec Rs → 0 :</p>

  <div class="equation">
    Ce = K × [g × R'r / (R'r² + g²×ωs²×Lσ²)]
  </div>

  <p>Où K = 3p × Vs² / ωs est une constante.</p>

  <p>Posons X = ωs × Lσ (réactance de fuite totale). L'expression devient :</p>

  <div class="equation">
    Ce = K × [g × R'r / (R'r² + g²×X²)]
  </div>

  <h4>Calcul de la Dérivée</h4>

  <p>Appliquons la règle de dérivation d'un quotient u/v : (u/v)' = (u'v - uv')/v²</p>

  <p>Avec :</p>
  <ul>
    <li>u = g × R'r  →  u' = R'r</li>
    <li>v = R'r² + g²×X²  →  v' = 2g×X²</li>
  </ul>

  <div class="equation">
    dCe/dg = K × [R'r×(R'r² + g²×X²) - g×R'r×2g×X²] / (R'r² + g²×X²)²
  </div>

  <p>Simplifions le numérateur :</p>

  <div class="equation">
    Numérateur = R'r×R'r² + R'r×g²×X² - 2g²×R'r×X²<br>
    = R'r³ + R'r×g²×X² - 2g²×R'r×X²<br>
    = R'r³ - g²×R'r×X²<br>
    = R'r × (R'r² - g²×X²)
  </div>

  <p>Pour que dCe/dg = 0, il faut que le numérateur soit nul :</p>

  <div class="equation">
    R'r² - g²×X² = 0<br>
    R'r² = g²×X²<br>
    R'r = g × X  (on prend la solution positive)
  </div>

  <p>D'où le glissement optimal :</p>

  <div class="equation">
    gmax = R'r / X = R'r / (ωs × Lσ)
  </div>

  <div class="key-point">
    <strong>RÉSULTAT FONDAMENTAL - Condition de Couple Maximum :</strong><br><br>
    
    <strong>gmax = R'r / (ωs × Lσ)</strong><br><br>
    
    Le couple maximum est atteint lorsque la résistance rotorique ramenée au stator égale la réactance de fuite totale à la pulsation de glissement :<br><br>
    
    R'r = gmax × ωs × Lσ<br><br>
    
    <strong>Interprétation physique :</strong><br>
    Cette condition correspond à l'adaptation d'impédance du circuit rotorique. C'est le compromis optimal entre :<br>
    • Un glissement suffisant pour induire des courants rotoriques importants<br>
    • Un glissement pas trop élevé qui limiterait l'efficacité de la conversion<br><br>
    
    <strong>Valeurs typiques :</strong><br>
    • Machines standard : gmax = 0,15 à 0,25 (15-25%)<br>
    • Machines à couple élevé : gmax = 0,20 à 0,35<br>
    • Machines à faible glissement : gmax = 0,10 à 0,15
  </div>

  <h3>5.2 Calcul de l'Expression du Couple Maximum</h3>

  <p>Substituons gmax dans l'expression du couple :</p>

  <div class="equation">
    Cemax = K × [gmax × R'r / (R'r² + g²max×X²)]
  </div>

  <p>Avec gmax = R'r / X, on a :</p>

  <div class="equation">
    g²max = R'r² / X²<br>
    g²max × X² = R'r²
  </div>

  <p>Donc le dénominateur devient :</p>

  <div class="equation">
    R'r² + g²max×X² = R'r² + R'r² = 2×R'r²
  </div>

  <p>Et le numérateur :</p>

  <div class="equation">
    gmax × R'r = (R'r/X) × R'r = R'r²/X
  </div>

  <p>D'où :</p>

  <div class="equation">
    Cemax = K × (R'r²/X) / (2×R'r²)<br>
    Cemax = K / (2X)<br>
    Cemax = [3p × Vs² / ωs] / (2 × ωs × Lσ)
  </div>

  <div class="formula-box">
    <h4>EXPRESSION FINALE DU COUPLE MAXIMUM :</h4>
    
    <strong>Forme 1 (avec ωs) :</strong><br>
    Cemax = 3p × Vs² / (2 × ωs² × Lσ)
    <br><br>
    
    <strong>Forme 2 (avec Ωs) :</strong><br>
    Cemax = 3 × Vs² / (2 × ωs × Lσ)  (car ωs = p × Ωs)
    <br><br>
    
    <strong>Forme 3 (avec Nσ = ωs × Lσ, réactance de fuite) :</strong><br>
    Cemax = 3p × Vs² / (2 × ωs × Nσ)
    <br><br>
    
    Cette expression est identique à celle de la solution du TD, où Nσ représente la réactance de fuite totale à la pulsation statorique.
  </div>

  <h3>5.3 Propriétés Remarquables du Couple Maximum</h3>

  <div class="key-point">
    <strong>Caractéristiques Importantes de Cemax :</strong><br><br>
    
    <strong>1. Indépendance de R'r :</strong><br>
    Le couple maximum ne dépend PAS de la résistance rotorique ! Seule la position du maximum (gmax) en dépend. Deux machines avec R'r différents auront le même Cemax mais à des glissements différents.<br><br>
    
    <strong>2. Proportionnel à Vs² :</strong><br>
    Cemax ∝ Vs². Si on double la tension, le couple maximum quadruple. C'est crucial pour le démarrage sous tension réduite.<br><br>
    
    <strong>3. Inversement proportionnel à ωs² :</strong><br>
    Cemax ∝ 1/ωs². Si on double la fréquence sans changer Vs, le couple maximum est divisé par 4. D'où la nécessité de maintenir Vs/fs constant.<br><br>
    
    <strong>4. Inversement proportionnel à Lσ :</strong><br>
    Cemax ∝ 1/Lσ. Les machines à faible inductance de fuite (meilleur couplage magnétique) ont un couple maximum plus élevé.<br><br>
    
    <strong>5. Conservation avec V/f constant :</strong><br>
    Si Vs/ωs = constante, alors Cemax reste constant à toutes les fréquences. C'est le principe de base de la commande scalaire !
  </div>

  <h3>5.4 Rapport Cemax / Cn (Facteur de Surcouple)</h3>

  <p>Le rapport entre le couple maximum et le couple nominal caractérise la capacité de surcharge de la machine :</p>

  <div class="equation">
    k = Cemax / Cn
  </div>

  <table>
    <tr>
      <th>Type de Machine</th>
      <th>Rapport k</th>
      <th>Application Typique</th>
    </tr>
    <tr>
      <td>MAS standard cage simple</td>
      <td>2,0 - 2,5</td>
      <td>Pompes, ventilateurs</td>
    </tr>
    <tr>
      <td>MAS haute performance</td>
      <td>2,5 - 3,0</td>
      <td>Machines-outils, levage</td>
    </tr>
    <tr>
      <td>MAS à double cage</td>
      <td>2,2 - 2,8</td>
      <td>Compresseurs, convoyeurs</td>
    </tr>
    <tr>
      <td>MAS à encoches profondes</td>
      <td>2,3 - 2,9</td>
      <td>Démarrages fréquents</td>
    </tr>
  </table>

  <p>Un facteur k élevé (k > 2,5) indique une bonne réserve de couple permettant à la machine de supporter des surcharges temporaires sans décrocher.</p>

  <div class="page-break"></div>

  <h2>VI. COMMANDE SCALAIRE V/f CONSTANT</h2>

  <h3>6.1 Principe de la Commande Scalaire</h3>

  <p>La commande scalaire (ou commande en V/f) est la stratégie de contrôle la plus simple et la plus répandue pour les variateurs de vitesse à base de MAS. Son principe repose sur le maintien du rapport tension/fréquence constant pour préserver le flux magnétique et donc le couple disponible.</p>

  <h4>Justification Théorique</h4>

  <p>Le flux magnétique dans l'entrefer est approximativement proportionnel à :</p>

  <div class="equation">
    Φ ≈ Vs / (ωs × Lm) ≈ Vs / ωs  (si Lm >> Lσ)
  </div>

  <p>Pour maintenir Φ constant (donc un couple disponible constant), il faut :</p>

  <div class="equation">
    Vs / ωs = constante  ou  Vs / fs = constante
  </div>

  <h3>6.2 Loi de Commande V/f</h3>

  <div class="formula-box">
    <h4>Loi de Commande Scalaire Standard :</h4>
    
    <strong>Zone de flux constant (f ≤ fn) :</strong><br>
    Vs / fs = Vn / fn = constante<br>
    Vs = (Vn / fn) × fs<br><br>
    
    Dans cette zone :<br>
    • Le flux reste constant : Φ = Φn<br>
    • Le couple maximum reste constant : Cemax = Cemax,n<br>
    • La vitesse est proportionnelle à la fréquence : Ω ≈ Ωs<br><br>
    
    <strong>Zone de défluxage (f > fn) :</strong><br>
    Vs = Vn (tension limitée à la valeur nominale)<br>
    Φ diminue avec 1/fs<br>
    Cemax diminue avec 1/fs²<br>
    Puissance approximativement constante (P ≈ Pn)
  </div>

  <h3>6.3 Compensation de Rs à Basse Fréquence</h3>

  <p>À basse fréquence (f < 10-15 Hz), la chute de tension dans Rs devient significative par rapport à la tension totale. Sans compensation, le flux diminue et le couple chute dangereusement.</p>

  <div class="equation">
    Vs,corrigée = (Vn/fn) × fs + Rs × Is,estimé
  </div>

  <p>Cette compensation, appelée "boost de tension" ou "compensation I×R", est essentielle pour :</p>
  <ul>
    <li>Maintenir le couple à basse vitesse</li>
    <li>Assurer un démarrage en charge</li>
    <li>Éviter le décrochage en montée en charge lente</li>
  </ul>

  <h3>6.4 Limitations de la Commande Scalaire</h3>

  <table>
    <tr>
      <th>Limitation</th>
      <th>Origine</th>
      <th>Conséquence Pratique</th>
    </tr>
    <tr>
      <td>Précision de vitesse</td>
      <td>Glissement variable avec la charge</td>
      <td>Variation ±1-2% de la vitesse</td>
    </tr>
    <tr>
      <td>Dynamique limitée</td>
      <td>Pas de contrôle direct du couple</td>
      <td>Temps de réponse lent (>100 ms)</td>
    </tr>
    <tr>
      <td>Couple à basse vitesse</td>
      <td>Effet de Rs non parfaitement compensé</td>
      <td>Couple réduit de 20-30% à f < 5 Hz</td>
    </tr>
    <tr>
      <td>Fonctionnement générateur</td>
      <td>Pas de régulation du freinage</td>
      <td>Nécessite résistance de freinage</td>
    </tr>
    <tr>
      <td>Variations paramétriques</td>
      <td>R'r varie avec la température</td>
      <td>Glissement variable (±50% sur R'r)</td>
    </tr>
  </table>

  <div class="note">
    <strong>Quand Utiliser la Commande Scalaire ?</strong><br><br>
    
    <strong>Applications Adaptées (70% des cas) :</strong><br>
    • Pompes et ventilateurs (charge quadratique)<br>
    • Convoyeurs légers à vitesse constante<br>
    • Applications ne nécessitant pas de précision de vitesse<br>
    • Coût d'installation prioritaire<br>
    • Pas de variations brutales de charge<br><br>
    
    <strong>Applications Nécessitant une Commande Vectorielle :</strong><br>
    • Machines-outils (précision de positionnement)<br>
    • Robotique (dynamique rapide)<br>
    • Levage (contrôle de couple précis)<br>
    • Traction (performances au démarrage)<br>
    • Enrouleurs (contrôle de tension)
  </div>

  <div class="page-break"></div>

  <h2>VII. CARACTÉRISTIQUE COUPLE-VITESSE</h2>

  <h3>7.1 Allure Générale de la Caractéristique</h3>

  <p>La caractéristique couple-vitesse C(Ω) ou C(g) de la MAS présente une forme caractéristique avec plusieurs zones distinctes :</p>

  <div class="formula-box">
    <h4>Zones de Fonctionnement :</h4>
    
    <strong>Zone 1 - Démarrage (g = 1, Ω = 0) :</strong><br>
    • Couple de démarrage Cd = 0,5 à 2,5 × Cn (selon le type de rotor)<br>
    • Courant de démarrage Id = 5 à 8 × In (très élevé !)<br>
    • Fonctionnement instable si Cd < Cr<br><br>
    
    <strong>Zone 2 - Accélération (1 > g > gmax) :</strong><br>
    • Couple croissant avec la vitesse<br>
    • Zone stable : dC/dg < 0<br>
    • Courant décroissant avec la vitesse<br><br>
    
    <strong>Zone 3 - Couple Maximum (g = gmax) :</strong><br>
    • Point de décrochage : C = Cemax = 2 à 3 × Cn<br>
    • Si Cr > Cemax, la machine décroche (arrêt)<br>
    • Limite de surcharge admissible<br><br>
    
    <strong>Zone 4 - Fonctionnement Nominal (gmax > g > 0) :</strong><br>
    • Zone de fonctionnement normal<br>
    • Couple approximativement linéaire : C ≈ K × g<br>
    • Point nominal : gn = 0,02 à 0,05, C = Cn<br>
    • Zone stable : auto-régulation naturelle<br><br>
    
    <strong>Zone 5 - Fonctionnement Générateur (g < 0) :</strong><br>
    • Vitesse supérieure au synchronisme : Ω > Ωs<br>
    • Machine entraînée par la charge<br>
    • Renvoi d'énergie au réseau<br>
    • Applications : éoliennes, descentes en charge
  </div>

  <h3>7.2 Équation de la Caractéristique</h3>

  <p>En combinant la relation du couple avec l'équilibre mécanique, on peut tracer C en fonction de Ω :</p>

  <div class="equation">
    g = (Ωs - Ω) / Ωs  →  Ω = Ωs × (1 - g)
  </div>

  <p>La caractéristique C(Ω) se déduit de C(g) par ce changement de variable.</p>

  <h3>7.3 Influence des Paramètres</h3>

  <table>
    <tr>
      <th>Paramètre</th>
      <th>Augmentation de...</th>
      <th>Effet sur Cd</th>
      <th>Effet sur Cemax</th>
      <th>Effet sur gmax</th>
    </tr>
    <tr>
      <td>R'r</td>
      <td>Résistance rotorique</td>
      <td>↑ Augmente</td>
      <td>= Constant</td>
      <td>↑ Augmente</td>
    </tr>
    <tr>
      <td>Lσ</td>
      <td>Inductance de fuite</td>
      <td>↓ Diminue</td>
      <td>↓ Diminue</td>
      <td>↓ Diminue</td>
    </tr>
    <tr>
      <td>Vs</td>
      <td>Tension statorique</td>
      <td>↑↑ Augmente (∝ Vs²)</td>
      <td>↑↑ Augmente (∝ Vs²)</td>
      <td>= Constant</td>
    </tr>
    <tr>
      <td>fs</td>
      <td>Fréquence</td>
      <td>↓ Diminue</td>
      <td>↓ Diminue</td>
      <td>↑ Augmente</td>
    </tr>
  </table>

  <h3>7.4 Types de Rotors et Leurs Caractéristiques</h3>

  <div class="formula-box">
    <h4>Comparaison des Technologies de Rotor :</h4>
    
    <strong>1. Rotor à Cage Simple (Standard) :</strong><br>
    • R'r faible → gmax faible (10-15%)<br>
    • Cd faible (0,5-1,5 × Cn)<br>
    • Cemax élevé (2,0-2,5 × Cn)<br>
    • Rendement excellent (> 90%)<br>
    • Applications : pompes, ventilateurs, charge légère<br><br>
    
    <strong>2. Rotor à Double Cage :</strong><br>
    • Cage externe haute résistance (démarrage)<br>
    • Cage interne basse résistance (régime nominal)<br>
    • Cd élevé (1,5-2,5 × Cn)<br>
    • Compromis entre Cd et rendement<br>
    • Applications : compresseurs, convoyeurs, charge lourde<br><br>
    
    <strong>3. Rotor à Encoches Profondes :</strong><br>
    • Effet de peau variable avec la fréquence rotorique<br>
    • R'r élevée au démarrage, faible en nominal<br>
    • Cd moyen (1,2-2,0 × Cn)<br>
    • Bon compromis coût/performances<br>
    • Applications : démarrages fréquents<br><br>
    
    <strong>4. Rotor Bobiné (rare aujourd'hui) :</strong><br>
    • Résistances externes ajustables<br>
    • Cd très élevé (jusqu'à 3 × Cn)<br>
    • Contrôle du couple de démarrage<br>
    • Coût et maintenance élevés<br>
    • Remplacé par les variateurs électroniques
  </div>

  <div class="page-break"></div>

  <h2>VIII. APPLICATIONS PRATIQUES ET DIMENSIONNEMENT</h2>

  <h3>8.1 Sélection d'une MAS pour une Application</h3>

  <p>Le choix d'une machine asynchrone nécessite de considérer plusieurs critères :</p>

  <h4>Critères de Base :</h4>

  <ul>
    <li><strong>Puissance nominale :</strong> Pn ≥ 1,15 × Pcharge (marge de sécurité 15%)</li>
    <li><strong>Vitesse nominale :</strong> Fonction du nombre de pôles et de la fréquence du réseau</li>
    <li><strong>Couple de démarrage :</strong> Cd > Cr,démarrage (avec marge de 20-30%)</li>
    <li><strong>Facteur de service :</strong> FS = 1,0 (continu) à 1,15 (intermittent)</li>
    <li><strong>Classe d'isolation :</strong> F (155°C) ou H (180°C) selon l'environnement</li>
  </ul>

  <h4>Critères Environnementaux :</h4>

  <ul>
    <li><strong>Indice de protection :</strong> IP54 (standard), IP55 (extérieur), IP56 (humide)</li>
    <li><strong>Classe de température :</strong> Selon température ambiante (-20°C à +60°C)</li>
    <li><strong>Altitude :</strong> Déclassement si > 1000 m (1% par 100 m)</li>
    <li><strong>Atmosphère :</strong> Version antidéflagrante si nécessaire (Ex, ATEX)</li>
  </ul>

  <h3>8.2 Dimensionnement d'un Variateur de Fréquence</h3>

  <p>Pour piloter une MAS en vitesse variable, le variateur doit être correctement dimensionné :</p>

  <table>
    <tr>
      <th>Paramètre</th>
      <th>Règle de Dimensionnement</th>
      <th>Exemple (MAS 7,5 kW)</th>
    </tr>
    <tr>
      <td>Puissance variateur</td>
      <td>Pvariateur ≥ 1,1 × Pmoteur</td>
      <td>≥ 8,25 kW → Variateur 10 kW</td>
    </tr>
    <tr>
      <td>Courant nominal</td>
      <td>Ivariateur ≥ 1,1 × Imoteur</td>
      <td>In,moteur = 15 A → Variateur 17 A</td>
    </tr>
    <tr>
      <td>Courant de surcharge</td>
      <td>1,5 × In pendant 60 s</td>
      <td>Imax = 22,5 A / 60 s</td>
    </tr>
    <tr>
      <td>Tension d'alimentation</td>
      <td>±10% de la tension réseau</td>
      <td>400 V ±10% → 360-440 V</td>
    </tr>
    <tr>
      <td>Fréquence de sortie</td>
      <td>0 à fmax (50-400 Hz)</td>
      <td>0-100 Hz (vitesse variable 1:20)</td>
    </tr>
    <tr>
      <td>Résistance de freinage</td>
      <td>Si freinage fréquent : Pfrein ≥ 0,3 × Pn</td>
      <td>≥ 2,25 kW</td>
    </tr>
  </table>
<div class="footer">
    <p><strong>Document préparé pour le Master 1 - Commande Électrique</strong></p>
    <p>Département d'Électrotechnique - Année Universitaire 2025/2026</p>
    <p style="margin-top: 12px; font-style: italic;">
      Ce document constitue une analyse approfondie et détaillée du TD N°1 sur les entraînements électriques à vitesse variable. Il couvre l'ensemble des aspects théoriques, pratiques et applicatifs nécessaires à une compréhension complète et professionnelle du sujet.
    </p>
    <p style="margin-top: 10px; font-weight: bold;">
      Created By : DAHANE AHMED LAMINE & RAMZI MAMOU
    </p>
  </div>
 
 
</body>
</html>

