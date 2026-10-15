# LIGHT ON RUN · Madine**

Site statique (HTML/CSS/JS, pas de build) du LIGHT ON RUN Madine, organisé par LIGHT ON.
Aperçu local : `python3 -m http.server 8080` à la racine, puis http://localhost:8080.

## Conventions

- Les épreuves s'appellent uniquement **10 KM\*** et **Semi-Marathon\*\*** (21,1 km) (majuscules + étoiles). Pas de noms inventés.
- Les étoiles indiquent le niveau du format : plus il y en a, plus le format est long. L'événement porte le nombre d'étoiles de son plus grand format : « Madine\*\* », « MADINE\*\* 2027 ».
- Ordre d'affichage : du plus petit au plus grand (10 → Semi). Seulement deux formats : pas de "grand format" façon trail, pas de notion d'« ultra » à surveiller (distance max 21,1 km).
- L'organisateur est **LIGHT ON** (pas « LIGHT ON RUN »).
- Date de l'édition 2027 : **jeudi 6 mai 2027**, Lac de Madine.
- Clôture des inscriptions : **lundi 3 mai 2027, 20h00**.
- Ouverture des inscriptions : **mardi 20 octobre 2026, 20h00**. Lien d'inscription njuko 2027 : **pas encore disponible**. Ne jamais citer la marque « njuko » sur le site RUN. Tant que le lien n'existe pas, tous les CTA « S'inscrire » renvoient vers `/infos.html#inscriptions`, avec un message indiquant la date d'ouverture (mardi 20 octobre 2026, 20h00) plutôt qu'un vague « arrive bientôt ». Mettre à jour dès réception du vrai lien le 20 octobre (ou après), et retirer les mentions de date d'ouverture une fois les inscriptions effectivement ouvertes.
- Le village de l'événement s'appelle **Village LIGHT ON**.
- Espaces du Village pour RUN : **LIGHT ON Shop** (boutique) uniquement. Pas de LIGHT ON Kids, pas de LIGHT OFF sur cette épreuve (confirmé, ne pas réintroduire sans validation).
- Partenaires : pas de mur de logos sponsors nommés sur le site RUN. CTA générique « Devenir partenaire » (mailto) uniquement.
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
- Témoignages : uniquement de vrais retours de coureurs issus du Google Sheet officiel, cités mot pour mot, avec prénom + initiale et distance (`.v-lead`, `.v-card`, `.q-inline`). Ne garder que les avis réellement positifs.
- Chaque page doit proposer un bouton S'inscrire bien visible ; un seul bouton plein par groupe de boutons.
- Vidéos : hébergées nativement (`<video controls>` dans `.media-frame`), pas d'embed YouTube/tiers sur les pages de contenu courant (médias officiels Drive).
- Les styles de la refonte sont à la fin de `assets/css/site.css` ; changer le `?v=` des liens CSS/JS après chaque modification (convention actuelle : `?v=20271006b`).

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
- Coordonnées GPS déjà présentes dans le JSON-LD de `index.html` (48.93, 5.73) mais **non vérifiées indépendamment auprès d'une source officielle** (règlement PDF, Drive, ou Julien). À confirmer avant publication plutôt qu'à prendre pour acquises.

## SEO

- Chaque page a un `<title>`, une meta description, une canonical absolue (`https://www.lightonrun.com/...`) et un Open Graph complet : à créer pour toute nouvelle page, et l'ajouter à `sitemap.xml`.
- Le sur-titre de chaque page fait partie du H1 (`<h1><span class="eyebrow page-kicker">…</span> …</h1>`).
- Données structurées JSON-LD : événement 2027 + organisation sur l'accueil, FAQ sur Infos. Les mettre à jour si une date, un horaire, un tarif ou le lieu change. Jamais d'avis/étoiles à partir des témoignages.
- Photos : fichiers au nom descriptif, versions WebP dans `assets/img/webp/` (`nom-640.webp`, `nom-1280.webp`, `nom-1920.webp`, générées avec Pillow/libwebp, qualité 74) via `<picture>`, avec `width`/`height`. Toute nouvelle photo suit ce schéma. **Ne pas utiliser l'AVIF de macOS (ImageIO)** : Chrome l'affiche en gris uni.
- Liens vers l'accueil : `/` (chemins absolus partout sur ce site, y compris `404.html`).
- Vidéos : natives, pas de JS tiers (`.media-frame` + `<video controls>`), fichiers servis depuis `assets/video/` (sources officielles Drive uniquement).

## À vérifier / signaler avant mise en ligne

1. ~~**Photo hero de `resultats.html`** (`groupe-finishers-medailles-madine.jpg`) : un dossard visible semble indiquer « 37 KM »~~ - fait : photo remplacée (15/10/2026) par une sélection du dossier Drive officiel `LIGHT ON RUN Madine - Photos`. 14 photos au total remplacées sur le site (voir liste ci-dessous). Une photo du même dossier (nommée `LightOnTriMadine19.09.26-819.jpg`) a été écartée après vérification du dossard (« RUN - 7 KM », épreuve LIGHT ON TRI et non RUN Madine) - à garder en tête si d'autres photos de ce dossier Drive sont réutilisées un jour : toujours vérifier le texte du dossard avant publication.
   - Photos remplacées : `depart-arche-light-on-madine.jpg`, `village-arche-arrivee-madine.jpg`, `groupe-finishers-medailles-madine.jpg`, `ligne-arrivee-madine-matin.jpg`, `selfie-bord-lac-madine.jpg`, `coureurs-sentier-bord-lac-madine.jpg`, `peloton-depart-foulees-madine.jpg`, `arrivee-sourires-coureuses-madine.jpg`, `hero-courses.jpg`, `hero-actualites.jpg`, `hero-evenement.jpg`, `hero-infos.jpg`, `hero-communaute.jpg`, `hero-medias.jpg`.
   - Non remplacées faute de photo correspondante dans ce dossier Drive (aucune photo de bénévole, ravitaillement ou podium dans la sélection) : `arrivee-duo-coureurs-madine.jpg`, `benevole-encouragements-coureur-madine.jpg`, `ravitaillement-benevoles-madine.jpg`, `podium-femmes-light-on-run-madine.jpg`.
2. **Coordonnées GPS** du départ (48.93, 5.73 dans le JSON-LD de `index.html`) à confirmer auprès d'une source officielle - non revérifiées indépendamment.
3. **Lien d'inscription njuko 2027** : ouverture annoncée pour le **mardi 20 octobre 2026, 20h00** (le site l'indique désormais à la place du vague « arrive bientôt »). À brancher dès réception du vrai lien, sur tous les CTA actuellement en placeholder (`/infos.html#inscriptions`), et retirer les mentions de date d'ouverture une fois les inscriptions ouvertes.
4. **`maquette-langues.html`** : fichier de mockup orphelin, contient encore l'ancien numéro de téléphone TRAIL (`03 74 47 56 52`). Hors scope du site live, à supprimer ou corriger si jamais réutilisé.
5. **Fichiers TRAIL orphelins** à supprimer une fois confirmé non réutilisés : `assets/gpx/*.gpx`, `assets/docs/resultats-17km-2026.pdf`, `assets/docs/resultats-37km-2026.pdf`, `assets/js/resultats-17km-2026.js`, `assets/js/resultats-37km-2026.js`. Sort de `assets/js/resultats-table.js` à trancher (probablement réutilisable en 2027, actuellement inutilisé).
6. `assets/partners/*.png/svg` : anciens logos sponsors TRAIL, à vérifier/supprimer puisque RUN n'affiche pas de mur de partenaires nommés.
7. Validité de l'URL d'action du formulaire newsletter Brevo pour la liste RUN (réutilisée depuis TRAIL, jamais revérifiée indépendamment).
8. ~~`sitemap.xml` ne liste actuellement que les pages FR (pas d'alternates hreflang `/en/`, `/de/`)~~ - fait : alternates hreflang fr/en/de ajoutés dans `sitemap.xml` pour les 9 pages FR.
9. ~~`/en/` et `/de/` sont encore des copies non adaptées du site TRAIL~~ - fait : `/en/` et `/de/` réécrits pour RUN Madine ; `assets/search-index-en.json`/`search-index-de.json` régénérés via `tools/build_md.py`.
10. **Lien Facebook non confirmé** : toutes les pages FR pointent maintenant vers `facebook.com/lightonrun` (vanity URL cohérente avec `@lighton_run` sur Instagram), mais 4 pages (`resultats.html`, `actualites.html`, `mentions-legales.html`, `404.html`) pointaient initialement vers `facebook.com/profile.php?id=61581806080267` - standardisé sur la majorité (7 pages) sans confirmation officielle. À vérifier avec Julien avant publication : lequel des deux est la vraie page Facebook LIGHT ON RUN ?
