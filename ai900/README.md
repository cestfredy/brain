# AI 900
C'est ici que je vais déposer toutes mes notes pour la préparation de la certification : https://learn.microsoft.com/en-us/credentials/certifications/azure-ai-fundamentals/

## IA génerative et agents
L'ia gen c'est une branche de l'IA qui permet aux applications logicielles de générer du nouveaux contenu;
Les modeles savant comment les mots se raproche les uns des autres. C'est justement ça qui leur permet de générer une séquence pertinente de texte?


Aujourd'hui on a des LLMs et des SLMs. La differences se base sur le volume de données et le nombre de variables dans le modèle. 

- LLM : puissant et généralise bien mais peut etre plus couteux a entrainer et a utiliser
- SLM : bon pour des domaines spécifique ou quand la nécéssité d'un petit model qui sera déployé sur des applications locals et les agents sur des appareils

les cas d'usage les plus courants de l'ia générative :
- création d'agents IA qui peuvent faciliter l'access a l'information et automatisation des taches
- creation de documents, contenus de maniere générale
- traduction automatisé de texte entre langue
- résumé ou explication de documents complexes


## Texte et langage naturel
NLP(natural language processing) c'est la base sur laquel les LLMs sont crées.
les cas d'usage les plus courant des technos de NLP :
- analyse de document, transcription d'appels et réunions
- analyse de publication de média, avis sur les produits ou des articles pour évaluer les sentiments et les opinions.
- implementation de chatbots qui peuvent répondre aux questions frequements posées
- orchestrer des dialogues conversationnels prévisibles qui ne necessitent pas la cimplexite de l'ia gen


## Discours
Pour les fonctionnalites vocal dans les applications et agents IA.
La reconnaissance vocal c'est la capacité de l'ia a entendre et a interpreter la parole.

signal audio --- texte
texte --- signal audible

les cas d'usages les plus courants :
- les agents IA qui comprennent les entrées parlées, effectuent des tâches et répondent avec des résultats parlés
- transcription automatisée d'appels/réunions
- automatisation des description audio/video/texte
- traduction vocale entre langue
- classification d'audio

## Vision par ordinateur
C'est le domaine de l'ia qui traite de l'analyse de de l'entrée visuelle (images, videos, flux caméras en direct)

Les cas d'usage les plus répandu de la VO :
- surveillance de vidéo securité
- authentification par reconnaissance faciale
- recherche visuelle
- Agent ia capable de voir
- sous-titrage automatique

## Extraction d'information
L'une des technologie les plus populaire ici est l'OCR (Optical Caracter Recognition) pour l'extraction d'insight dans une images.

ces cas d'usages sont les suivant :
- traitement automatique de formulaire ou d'autres documents dans un process metier
- numerisation de donées provenant de formulaires papiers
- indexation de documents pour la recherche
- identification des points clé a partir de transcription ou de l'enregistrement de reunion

## IA responsable
LEs principes pour une IA responsable :
- impartialité : les données sont sur lesquels sont entrainés nos IA sont sélectionné par des humains un biais inconscient peut donc etre introduit de part la selection discriminatoire que les données eux meme. les Ingénieur Ia doivent dont s'assurer de minimiser les préjugé dans les données d'entrainement et d'assurer l'équité durant la phase de test

- fiabilité et sécurité : l'ia etant basé sur des modeles probabiliste il n'est donc pas infaible nos applications doivent toujours tenir compte de ce risque

- confidentialité et sécurité : les donées utilisés lors de l'entrainement doivent etre gardés en tout sécurité et les modeles résultant ne doivent pas etre utilisé pour révéler des informations sensible a caractere personnel sur les personnes ou organisations privées

- Inclusivité : on doit s'asssurer que nos solution d'IA n'excluent pas certainent personnes, le combat ici est de faire bénéfiecer tout le monde des avantages qu'offre l'ia

- transparence : l'utilisateur doit etre au courant de comment le systeme fonctionne et des limitations potentiel qui peut se presenter

- responsablité :  les personnes et organisations qui developent et distribuent des solutions d'ia sont responsable de leurs actions


## Exercice
Ici l'idée était de comprendre et tester un agent IA.
Plus spécifiquement [Ask Andrew](https://microsoftlearning.github.io/mslearn-ai-concepts/Instructions/exercises/01-explore-agent.html) ;)

### Compréhension de l'architecture

Comment Ask Andrew marche ?

Le processus peut être découpé en 6 étapes :

1. l'utilisateur soumet sa question (un prompt)
2. L'application extrait les mots clés du prompt et utilise ces mots clés pour intérroger une base de connaissance.

Pour cette app, la base de connaissance est le fichier [index.json](https://microsoftlearning.github.io/ai-apps/ask-andrew/index.json), chargé localement dans notre navigateur. Plus scalable, les angents prêt pour la production ont une base de connaissance encore plus fournie et compréhensible.
3. La requete retourne un texte de connaissance stoké pour fournir un contexte qui peut aider pour répondre a la quuestion posée
4. l'agent soumet un message au llm.
le messages est constitué de :
- Prompt System : contient les instructions sur comment le model doit formater sa réponse
- Les infos de contexte : ceux retournées par la requette
- la question de départ
5. Le LLm génere une réponse a la question en utilisant tout le contexte fournis
6. l'agent répond au chat avec la réponse


Cette architecture reflecte exactement comment plusieurs agents IA en production sont conçus. C'est basé sur un pattern général appelé RAG Retrieval Augmented Generation.