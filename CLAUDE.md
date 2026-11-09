# EL POP · context del projecte

Joc educatiu i accessible per al navegador (HTML5 + JavaScript, sense instal·lació), fet per a un centre educatiu. Tot el joc és un sol fitxer: `index.html` (CSS, dibuix en canvas, música i efectes amb Web Audio, sense dependències ni imatges externes; només fonts de Google Fonts).

Publicat amb GitHub Pages des de la branca `main`, carpeta arrel: https://mgatellcat.github.io/el-pop/

## Per a qui és

- Alumnat amb dificultats motrius i/o visuals. El repositori és públic: **no hi posis mai noms ni dades personals de l'alumnat**.
- Primer destinatari: un noi que juga amb PC, amb tecles o commutadors. Li encanta xocar la mà, d'aquí el «XOCA LA POTA!».

## Formes d'accés (prioritat actual)

1. **Tecles** (configurables pel docent).
2. **Pantalla tàctil**: tocar un carril hi porta el pop; tocar el carril on ja és llança tinta.
3. **Mirada**: el centre té **Tobii eye tracker** amb **TD Control** i **Grid 3**, que fan servir la mirada com a ratolí. En el mode MIRADA, el pop va al carril on hi ha el punter quan s'omple un rellotge de fixació. El temps d'espera el programa el docent (per defecte 0,7 s). Amb mirada, els carrils es marquen més i la tinta i la super tinta són automàtiques. Si TD Control fa clic per fixació, també funciona.
4. **Commutadors**: també s'utilitzen al centre, però de moment no són prioritat. El mode «un sol botó» ja existeix.

## Regles de disseny (no les trenquis)

- Interfície i textos en **català i en majúscules (lletra pal)**.
- **Mai cal prémer dues tecles alhora.** Sense pressió de temps; velocitat per defecte lenta.
- **Sense Game Over frustrant**: quan s'acaben les vides surt «NO PASSA RES! TORNEM-HI!». Si passa al boss, es torna a començar davant del boss.
- Cada pantalla acaba amb un boss de patrons lents i clars, que avisen abans d'atacar i sempre deixen almenys un carril lliure.
- En passar la pantalla, el pop diu «XOCA LA POTA!» / «GIVE ME FIVE!» i fa l'animació de xocar el tentacle.
- Dificultat: Fàcil (2 tecles, tinta automàtica), Normal (3 tecles), Pro (4 tecles, amb super tinta manual).

## Estils visuals (el jugador els tria al menú)

- **A · Escull de caramel**: kawaii de dia.
- **B · Escull neó**: anime d'acció de nit.
- **C · Baixa visió**: fons llis i fosc; perles grogues i rodones; perills vermells i punxeguts amb vora blanca; objectes un 30% més grans; lletra Atkinson Hyperlegible; avisos de so; sense tremolors ni flaixos.

Hi ha quatre pops per triar: Pipa, Brau, Lila i Nauti. Encara no està decidit quin estil i quin pop seran els definitius.

## Estat i pendents

- Fet: pantalla 1 (escull) amb el boss Cranc Rei i el poder de la tinta; opcions del docent; estils A, B i C; mode mirada; control tàctil.
- Pendent: pantalles 2-5 (bosc d'algues: bombolla escut; coves: imant de perles; vaixell enfonsat: tentacles dobles; abisme: mode Kraken).
- Idees pendents de decidir: opció de mida dels objectes i de color del fons per a l'estil C; alternativa al vermell per a daltonisme; control amb el cap amb la càmera web.

## Com treballar-hi

- Edita `index.html` directament. Els ajustos es guarden a `localStorage` (`elpop-settings`, `elpop-sel`), així que la pàgina ha de funcionar bé encara que no n'hi hagi.
- Per provar-lo, obre `index.html` amb Playwright (Chromium) i comprova que no hi ha errors a la consola. Per anar directament al boss, fes servir el botó «PROVAR EL BOSS».
