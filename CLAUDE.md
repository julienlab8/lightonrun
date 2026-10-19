# LIGHT ON RUN · Madine**

Site statique (HTML/CSS/JS, pas de build) du LIGHT ON RUN Madine, organisé par LIGHT ON.
Aperçu local : `python3 -m http.server 8080` à la racine, puis http://localhost:8080.

## Conventions

- Les épreuves s'appellent uniquement **10 KM\*** et **Semi-Marathon\*\*** (21,1 km) (majuscules + étoiles). Pas de noms inventés.
- Les étoiles indiquent le niveau du format : plus il y en a, plus le format est long. L'événement porte le nombre d'étoiles de son plus grand format : « Madine\*\* », « MADINE\*\* 2027 ».
- Ordre d'affichage : du plus petit au plus grand (10 → Semi). Seulement deux formats : pas de "grand format" façon trail, pas de notion d'« ultra » à surveiller (distance max 21,1 km).
- L'organisateur est **LIGHT ON** (pas « LIGHT ON RUN »).
- Date de l'édition 2027 : **jeudi 6 mai 2027**, Lac de Madine. 2027 est la **6e édition** (précédentes en 2022, 2023, 2024, 2025, 2026 - voir resultats.html) : ne jamais écrire « 1re édition » nulle part sur le site (erreur corrigée le 19/10/2026 dans llms.txt).
- Tarif **10 KM\*** : **19 € fixe, sans évolution** (confirmé 19/10/2026, remplace l'ancien barème 18 €→19 €→20 €). Le **Semi-Marathon\*\*** est également à **24 € fixe, sans évolution** (confirmé 19/10/2026 par Julien, remplace l'ancien barème croissant 23 €→24 €→25 € selon date d'inscription ; les deux formats sont désormais harmonisés en tarif unique).
- Clôture des inscriptions : **lundi 3 mai 2027, 20h00**.
- Horaires 2027 (validés par Magali le 19/10/2026) : départ du **Semi-Marathon\*\* à 9h00**, du **10 KM\* à 11h00** (deux heures d'écart). Retrait des dossards : mercredi 5 mai **17h-19h** ; jeudi 6 mai **7h00-8h45** (semi) et **7h00-10h45** (10 km). Remise des récompenses le jeudi à **12h15**.
- Parcours : le Semi-Marathon\*\* fait le **tour complet du lac**, le 10 KM\* alterne **rive et forêt** (il ne fait pas le tour du lac). Tout est à plat (« plat » / « à plat » OK), mais **jamais « bitume » ni « goudronné »** : il y a des chemins et de la forêt. Mention « Bon à savoir : le parcours n'est pas entièrement goudronné » (`.cmp-note`) sur Courses et Événement.
- Ouverture des inscriptions : **mardi 20 octobre 2026, 20h00**. Lien d'inscription njuko 2027 : `https://in.njuko.com/light-on-run-madine-2027?currentPage=select-competition` (branché le 16/10/2026, reçu de Julien avant l'ouverture officielle). Ne jamais citer la marque « njuko » sur le site RUN (aucune occurrence visible du mot dans le contenu, uniquement dans les `href`/JSON-LD). Tous les CTA « S'inscrire »/« Register »/« Anmelden » pointent désormais vers ce lien (nouvel onglet) ; les liens de nav simplement intitulés « Inscriptions »/« Registration »/« Anmeldung » restent en ancre locale vers `infos.html#inscriptions`. Le message de date d'ouverture (mardi 20 octobre 2026, 20h00) reste affiché tant que les inscriptions ne sont pas effectivement ouvertes - à retirer après le 20/10.
- Le village de l'événement s'appelle **Village LIGHT ON**.
- Espaces du Village pour RUN : **LIGHT ON Shop** (boutique) et remise des récompenses. Pas de LIGHT ON Kids ni de LIGHT OFF pour le moment : Magali doit vérifier avec Julien (19/10/2026), ne pas les ajouter sans son retour.
- Partenaires : mur de partenaires nommés activé (confirmé 18/10/2026, override de la précédente politique « pas de mur »), répliquant exactement le pattern TRAIL - ticker `.h-partners` en page d'accueil + section `.partner-tier` sur `communaute.html#partenaires`. Tiers : institutionnel (Lac de Madine), majeur (N2A Expertises), partenaires officiels (Crédit Mutuel, Europe 2), fournisseurs officiels (Apirun, Activa). Le CTA générique « Devenir partenaire » (mailto, ancre `#partenaire` singulier) reste en place en parallèle, inchangé.
- Contact : hello@lightontri.com est volontaire (seule adresse pour le moment).
- Réseaux : Instagram **@lighton_run**, Facebook, YouTube @lightontri, LinkedIn light-on-events. Hashtag officiel : **#LightOnRun** (un seul, sans année).
- Le menu et le pied de page sont dupliqués dans chaque page HTML : toute modification doit être répétée sur toutes les pages.

## DA LIGHT ON (pas encore de charte complète)

- Couleurs : noir `#232323`, orange `#ED5F3E`, blanc `#FFFFFF`. La DA est sombre : le clair n'en fait pas partie.
- Titres : Lemon Milk, bold ou regular selon l'usage, **jamais d'italique**. Textes : Roboto normal, certains mots forts en gras.
- Logos : toujours préférer les versions bicolores (noir/blanc + orange). Le picto (crochets + éclair) est un élément fort de la marque.
- Fichiers source : `~/Documents/Documents/MAZE Planner/LIGHT ON/2 - Light On/DA/` (SVG, PNG, AI).
- Pas de crédit vidéaste à afficher pour les vidéos.

## Direction visuelle du site

- Style « éditorial sombre » : angles droits, pas de cartes arrondies ni de halos, pas d'animations de fondu au défilement. Blocs séparés par des filets avec un trait orange d'accent.
- Signatures de marque (à utiliser avec parcimonie) : crochets du picto (`.brk`, `.brk-in`), coupe en biais dans l'angle de l'éclair (`.cut`, une fois par page), éclair dans les boutons S'inscrire (`.btn-go`).
- Le double menu (barre d'accès rapide + menu principal) est à conserver tel quel.
- Mettre en orange un mot clé des grands titres avec `<em>` (jamais d'italique).
- Témoignages : uniquement de vrais retours de coureurs issus du Google Sheet officiel, cités mot pour mot, avec prénom + initiale et distance (`.v-lead`, `.v-card`, `.q-inline`). Ne garder que les avis réellement positifs. Jamais un avis qui pourrait dénigrer l'événement (ex. « un peu boueux », retiré le 19/10/2026). Avis 2026 utilisés (liste de Magali du 19/10/2026) : accueil, Courses (3 par distance), Événement (L'esprit LIGHT ON), Communauté (bénévoles), Infos. Non utilisés volontairement : Baptiste V. (météo), Cédric D. (arrivée simultanée des deux courses, plus vrai avec les horaires 2027), Dorian H. (maillot/photos inclus, à confirmer pour 2027).
- Photos : **jamais deux fois la même photo sur le site**, sauf le pied de page (`.cta-slim`, coureuse bras levés), l'image du menu et la galerie de `medias.html`. Couleur des dossards : **noir = Semi-Marathon\*\***, **orange = 10 KM\***. Une photo illustrant une distance doit montrer le bon dossard.
- En-têtes où le texte passerait sur des visages : variante `.ph-stack` (photo en bandeau, texte dessous), utilisée sur Événement, Courses, Infos, Communauté et Résultats.
- Photos sources : `~/Documents/Documents/MAZE Planner/LIGHT ON/3 - LIGHT ON RUN/Site Web/Sélection photos site web Run/`. Noms de fichiers descriptifs (ce que montre la photo), textes alternatifs descriptifs en FR/EN/DE.
- Chaque page doit proposer un bouton S'inscrire bien visible ; un seul bouton plein par groupe de boutons.
- Vidéos : hébergées nativement (`<video controls>` dans `.media-frame`), pas d'embed YouTube/tiers sur les pages de contenu courant (médias officiels Drive).
- Les styles de la refonte sont à la fin de `assets/css/site.css` ; changer le `?v=` des liens CSS/JS après chaque modification (convention actuelle : `site.css?v=20271019f`).

## Ton rédactionnel LIGHT ON

LIGHT ON crée des événements sportifs outdoor : triathlon, trail, running.

**Ton** : dynamique, sportif, direct et complice, avec une vraie personnalité, sans en faire trop. On s'adresse aux participants comme à une communauté qui partage le goût du sport, de l'effort et du plaisir.

**Principe clé** : du challenge, oui, mais jamais dans un registre guerrier ou ultra-performance. On peut se dépasser sans se prendre trop au sérieux. L'effort, le plaisir, l'expérience et la convivialité vont ensemble.

**Style** :
- court et efficace : phrases simples, rythme naturel, pas de longs discours ;
- complice : clin d'œil, jeu de mots, pointe d'humour légère ;
- moderne et spontané, pas un texte publicitaire d'agence ;
- sportif mais accessible : on parle aux compétiteurs comme à ceux qui viennent se challenger ou simplement profiter ;
- enthousiaste sans être cucul : pas de grandes envolées émotionnelles, de phrases inspirantes convenues ni de vocabulaire lyrique ;
- concret : le terrain, les sensations, les distances, le lieu, le moment vécu.

Sur le site web : garder cette personnalité, un cran plus sobre que sur Instagram. Clair, identifiable, vivant, sans blabla. Pas d'emojis.

**À éviter** : « une aventure humaine inoubliable », « dépassez vos limites », « vibrez au rythme de… », « une expérience unique », « prêts à relever le défi ? », « passionnés de sport », et tout vocabulaire marketing interchangeable. Pas d'accumulation d'adjectifs ni de superlatifs (« exceptionnel », « incroyable », « incontournable ») : le contenu doit donner envie par lui-même.

**Référence** : « LIGHT ON — Le goût de l'effort, grandeur nature. »

**Aussi** : pas de tirets longs (— ou –), uniquement « - ». Pas le mot « fête ». Remplacer les promesses (« organisation soignée », « ravitaillements généreux ») par des preuves concrètes : paysage, lac, bénévoles, ravitos, retours de coureurs. Chaque grande section doit contenir au moins une phrase impossible à copier sur le site d'une autre course sur route.

**Test avant chaque texte** : cette phrase pourrait-elle appartenir à n'importe quelle course outdoor ? Si oui, la retravailler. Une bonne phrase LIGHT ON pourrait être dite à voix haute par quelqu'un de l'équipe. Entre plusieurs formulations, choisir la plus courte, la plus naturelle et la moins publicitaire.

Ne jamais modifier les informations pratiques (horaires, distances, ravitaillements, barrières horaires, tarifs) sans validation, et ne jamais inventer de donnée absente des sources officielles (site lightonrun.com, page foulées de Madine, règlement PDF 2027, Drive photos/vidéos/logos, Google Sheet d'avis). Signaler toute incohérence plutôt que de la combler par une hypothèse.

## Géographie (à vérifier avant publication)

- Village LIGHT ON au Lac de Madine, départ à **Nonsard-Lamarche (55210, Meuse)**, entre **Verdun et Toul**, dans le **Parc naturel régional de Lorraine**.
- Coordonnées GPS du départ (Maison de Madine, Nonsard-Lamarche) : **48.928, 5.7544** - confirmées le 16/10/2026 via le lien Google Maps fourni par Julien, mises à jour dans le JSON-LD (FR/EN/DE) et l'affichage `.geo` (anciennes valeurs 48.93/5.73 approximatives et imprécises).

## SEO

- Chaque page a un `<title>`, une meta description, une canonical absolue (`https://www.lightonrun.com/...`) et un Open Graph complet : à créer pour toute nouvelle page, et l'ajouter à `sitemap.xml`.
- Le sur-titre de chaque page fait partie du H1 (`<h1><span class="eyebrow page-kicker">…</span> …</h1>`).
- Données structurées JSON-LD : événement 2027 + organisation sur l'accueil, FAQ sur Infos. Les mettre à jour si une date, un horaire, un tarif ou le lieu change. Jamais d'avis/étoiles à partir des témoignages.
- Photos : fichiers au nom descriptif, versions WebP dans `assets/img/webp/` (`nom-640.webp`, `nom-1280.webp`, `nom-1920.webp`, générées avec Pillow/libwebp, qualité 74) via `<picture>`, avec `width`/`height`. Toute nouvelle photo suit ce schéma. **Ne pas utiliser l'AVIF de macOS (ImageIO)** : Chrome l'affiche en gris uni.
- Liens vers l'accueil : `/` (chemins absolus partout sur ce site, y compris `404.html`).
- Vidéos : natives, pas de JS tiers (`.media-frame` + `<video controls>`), fichiers servis depuis `assets/video/` (sources officielles Drive uniquement).

## À vérifier / signaler avant mise en ligne

1. ~~Photos~~ - fait (19/10/2026) : toutes les photos renommées d'après ce qu'elles montrent (plus de `hero-*.jpg`), 14 nouvelles photos tirées du dossier « Sélection photos site web Run », plus aucun doublon hors pied de page, menu et galerie. Écartées : LightOnTriMadine19.09.26-819 (épreuve TRI) et les deux visuels « Rectangles Njuko ». Toujours vérifier le dossard avant publication. « Retour sur 2026 » (accueil) : 5 photos de l'édition 2026 envoyées par Magali le 19/10/2026. Photos écartées de cet envoi : celles signées « Manon.C Photographe » (filigrane), le podium sur fond LIGHT ON TRI et la coureuse sur chemin boueux.
2. ~~**Coordonnées GPS** du départ (48.93, 5.73 dans le JSON-LD de `index.html`) à confirmer auprès d'une source officielle~~ - fait (16/10/2026) : confirmées à 48.928, 5.7544 (Maison de Madine) via lien Google Maps de Julien, mises à jour FR/EN/DE (JSON-LD + affichage `.geo`).
3. ~~**Lien d'inscription njuko 2027**~~ - fait (16/10/2026) : lien reçu de Julien et branché sur tous les CTA « S'inscrire »/« Register »/« Anmelden » (`https://in.njuko.com/light-on-run-madine-2027?currentPage=select-competition`, nouvel onglet). Le message de date d'ouverture (mardi 20 octobre 2026, 20h00) reste affiché jusqu'à l'ouverture effective - à retirer après le 20/10.
4. **`maquette-langues.html`** : fichier de mockup orphelin, contient l'ancien numéro de téléphone TRAIL (`03 74 47 56 52`) - qui est désormais, par coïncidence, identique au nouveau numéro RUN (changé le 15/10/2026). Toujours hors scope du site live (fichier non lié), à supprimer si jamais confirmé inutile.
5. ~~**Fichiers TRAIL orphelins** (`assets/gpx/*.gpx`, résultats 17 et 37 km en PDF et JS)~~ - fait : supprimés dans le commit de rebranding (a336666). `assets/js/resultats-table.js` est réutilisé pour les résultats RUN 2022-2026.
6. ~~`assets/partners/*.png/svg` : anciens logos sponsors TRAIL, à vérifier/supprimer puisque RUN n'affiche pas de mur de partenaires nommés.~~ - fait (18/10/2026) : assets réutilisés tels quels (N2A, Crédit Mutuel, Europe 2, Apirun, Activa - identiques à TRAIL, dont les variantes `white/` nécessaires au ticker) ; seul `pierre-percee.png` supprimé (non pertinent pour RUN) et `lac-madine.png` + `white/lac-madine.png` ajoutés (recadrés depuis une capture Drive, aucun logo officiel autonome disponible).
7. Validité de l'URL d'action du formulaire newsletter Brevo pour la liste RUN (réutilisée depuis TRAIL, jamais revérifiée indépendamment).
8. ~~`sitemap.xml` ne liste actuellement que les pages FR (pas d'alternates hreflang `/en/`, `/de/`)~~ - fait : alternates hreflang fr/en/de ajoutés dans `sitemap.xml` pour les 9 pages FR.
9. ~~`/en/` et `/de/` sont encore des copies non adaptées du site TRAIL~~ - fait : `/en/` et `/de/` réécrits pour RUN Madine ; `assets/search-index-en.json`/`search-index-de.json` régénérés via `tools/build_md.py`.
10. ~~**Lien Facebook non confirmé**~~ - fait (16/10/2026) : confirmé par Julien, `facebook.com/lightonrun` est la bonne page. Toutes les pages FR/EN/DE y pointent déjà de façon cohérente.
