
• Voici les fichiers que j'ai uploadés
- Extraction "brute" de tous les détails : AllMoviesDetailsRaw.csv (460k lignes env. pour mémoire uniquement)
- Extraction nettoyée des les films avec trop de missing values : AllMoviesDetailsCleaned.csv (330k lignes, je propose que ce soit notre référence comme "univers de tous les film faits")
- Extraction du casting sur notre univers : AllMoviesCastingRaw.csv
- Extraction details & casting + mes notes sur mes films :MyMoviesDetailsCastingRaw.csv (2k lignes, je propose que ce soit notre référence comme "liste de mes films vus")
- 2 notebooks python exemple de data exploration : AllMoviesDataExploration.ipynb & MyMoviesDataExploration.ipynb
- Notre programme cible pour l'objectif N°1 : Clustering My Movies.ipynb

OBJECTIFS
- 1. clustering de mes films => extension à tous les films
- 2. prediction de la note
- 3. NPL, extraction de features avancées (compréhension du résumé, caractérisation avancée du réalisateur ou de l'oeuvre, etc.)

DIFFICULTE
- choix de l'algo : a priori K means (il existe K Modes)
- choix de la distance : a priori euclidienne (il existe Jaccard distance)
- travail sur les features : numérisation, normalisation, missing fields & outliers

CHOIX FEATURES & IMPORTANCE
- nb d'acteurs (***)
- imdb_rating (**)
- tmdb_rating (**)
- personal_rating (***)
- original_language (***)
- nb of votes (**) =>correlation entre imdb_rating & tmdb_rating & nb vote => Pater ?
- release_date (***) => traité comme une var continue
- runtime (**)
- production country (**) nb of countries (*)
- production compagnies, nb de films produits par la boite => A CALCULER stef
- genre (***)
- nb d'acteurs, etc.
- caractérisation du réalisateur cf après

Caractérisation du réalisateur
- Scoring fidélité (***) vs acteurs & equipe => A CALCULER stef
- gender (*)
- temps moyen pour faire un film (**) défaulté à deux ans => A CALCULER pater
- nb de films faits (*)
A voir : cumul du nb de votes, nationalité réalisateur, mots communs dans la description du réalisateur
