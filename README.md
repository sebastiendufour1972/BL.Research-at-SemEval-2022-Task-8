Utilisation des NB pour résoudre les problèmes de similarité d'articles Semeval Task 8 2022

1) Modèles réalisés par langues (base programme Multi-lingues) : 6 modèles
Modèles : anglais - français - allemand - espagnol - arabe - turc
2) les modèles définissent un certain nombre de scores de similarité entre les articles (base Titres + Textes)
- similarité de titres à partrir de sentence transformer
- Résumé de textes par Transformers Hugging face puis score de similarité des résumés par sentence transformer
- Zero shot classification sur la base de catégories presse (Transformers Hugging face) : score de similarité de classification
- sentiment analysis ou tonalité (Transformers Hugginbg face) : score de similarité de classification
- NER recognition : Groupes + Noms / Dates / Locations : Spacy ou Transformers Hugging Face : score de nombre d'entités communes 
- NER Locations : score de localisation globale géographique (library Geopy) : Moyenne et Max
- Termes principaux : Library Pke : scores liés aux termes communs : sélection des 20 ou 40 termes principaux, renforcés par l'utilisation de termes sémantiquement proches (Word2vec et gensim)
=> Certain nombre de notations de similarités entre les 2 articles de presse
3) utilisation de techniques et de régression et d'algorithmes de classification pourfinaliser l'évaluation:
- création d'un dataset de réfernce par langues
- finalisation de la classification
