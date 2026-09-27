/* 1. IMPORTATION */
@import url('https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400..700;1,400..700&family=Poppins:ital,wght@0,300;0,400;0,500;0,600;0,700&display=swap');

/* 2. RÃ‰DÃ‰FINITION DES VARIABLES D'OBSIDIAN */
/* C'est ici que l'on force le logiciel Ã  changer ses calculs internes */
body {
    --p-spacing: 0px;
    /* Supprime l'espace entre paragraphes pour laisser les titres gÃ©rer */
    --heading-spacing: 0px;
    /* Reset du rÃ©glage natif */
    --h1-size: 2.2rem;
    --h2-size: 1.8rem;
    --h3-size: 1.4rem;
    --h4-size: 1.2rem;
}

/* 3. APPLICATION DU STYLE APPLE */

/* Corps de texte */
.markdown-source-view.mod-cm6 .cm-content,
.markdown-rendered {
    font-family: 'Poppins', sans-serif !important;
    font-size: 16px !important;
    line-height: 1.6 !important;
}

/* TITRES - On utilise le PADDING pour forcer l'espace visuel */
h1,
h2,
h3,
h4,
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4 {
    font-family: 'Lora', serif !important;
    color: #1d1d1f !important;
    display: block !important;
    border-bottom: none !important;
}

/* H1 */
.inline-title,
h1,
.cm-header-1 {
    padding-top: 20px !important;
    padding-bottom: 25px !important;
    font-weight: 700 !important;
}

/* H2 - "Mythe fondateur" */
h2,
.cm-header-2 {
    /* On utilise padding-top car Obsidian ne peut pas l'ignorer, contrairement au margin */
    padding-top: 50px !important;
    padding-bottom: 10px !important;
    font-weight: 600 !important;
}

/* H3 - "Erreur de traduction" */
h3,
.cm-header-3 {
    padding-top: 40px !important;
    padding-bottom: 8px !important;
}

/* H4 */
h4,
.cm-header-4 {
    padding-top: 30px !important;
    padding-bottom: 5px !important;
}

/* 4. FIX POUR LE PREMIER Ã‰LÃ‰MENT */
/* Ã‰vite le trou blanc si la note commence par un titre */
.markdown-rendered> :first-child,
.cm-content> :first-child {
    padding-top: 0 !important;
    margin-top: 0 !important;
}

/* CHANGEMENT DE LA COULEUR DE PAGE (Style Apple System Gray) */
.workspace-leaf-content[data-type="markdown"]>.view-content,
.markdown-reading-view,
.markdown-preview-view,
.cm-editor .cm-scroller {
    /* Couleur de fond unie */
    background-color: #f4f4f4 !important;
    */
    /*background-color: #F2F2F7 !important;*/

    /* On supprime les anciens gradients pour avoir une couleur nette */
    background-image: none !important;
}

/* ESPACEMENT ENTRE PARAGRAPHES (LECTURE + Ã‰DITION) */

/* 1. Mode Lecture */
.markdown-rendered p {
    margin-bottom: 2rem !important;
    /* L'espace entre paragraphes */
    margin-top: 0 !important;
}

/* 2. Mode Ã‰dition (Live Preview) */
.markdown-source-view.mod-cm6 .cm-line:not(.cm-header-1, .cm-header-2, .cm-header-3, .cm-header-4) {
    padding-bottom: 1.5rem !important;
    /* On utilise padding ici pour l'Ã©diteur */
}

/* 3. SÃ©curitÃ© pour les listes (puces) */
/* Pour Ã©viter que les puces ne soient trop Ã©cartÃ©es */
.markdown-rendered li p {
    margin-bottom: 0 !important;
}

/* 4. On retire la marge sous le tout dernier paragraphe de la note */
.markdown-rendered p:last-child {
    margin-bottom: 0 !important;
}