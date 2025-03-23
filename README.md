Projet : DApp de Vote

Auteurs
Nour El Houda EL BOUZ
Inès ZAHEM

Description
Ce projet consiste en une application décentralisée (DApp) de vote basée sur la blockchain Ethereum. Le smart contract permet à une organisation de gérer un processus de vote transparent et sécurisé. Les votants, préalablement inscrits sur une liste blanche, peuvent proposer des idées et voter pour leurs propositions préférées. Le gagnant est déterminé à la majorité simple.

Fonctionnalités
Inscription des votants : L'administrateur peut ajouter des votants à la liste blanche.

Enregistrement des propositions : Les votants inscrits peuvent soumettre des propositions pendant la session d'enregistrement.

Session de vote : Les votants peuvent voter pour leurs propositions préférées.

Comptabilisation des votes : L'administrateur peut clôturer la session de vote et déterminer la proposition gagnante.

Transparence : Tous les votes sont visibles par les participants.

Technologies utilisées
Smart Contract : Solidity (compilateur latest)

Framework : Truffle

Bibliothèque : OpenZeppelin (Ownable)

Frontend : React.js (ou autre framework Web3)

Test : Mocha/Chai

Déploiement : Ganache (local), Ethereum Testnet (Ropsten, Rinkeby, etc.)

Installation
Prérequis
Node.js (version 16.x ou supérieure)

Truffle (npm install -g truffle)

Ganache (pour tester localement)

MetaMask (pour interagir avec la DApp)

Processus de vote
Inscription des votants : L'administrateur ajoute les adresses Ethereum des votants à la liste blanche.

Enregistrement des propositions : Les votants inscrits soumettent leurs propositions.

Session de vote : Les votants votent pour leurs propositions préférées.

Comptabilisation des votes : L'administrateur clôture la session de vote et détermine le gagnant.

Consultation des résultats : Tout le monde peut consulter la proposition gagnante.

Exemple d'interaction avec Truffle Console
bash
Copy
truffle console --network <nom_du_réseau>
> const instance = await Voting.deployed()
> await instance.addVoter(<adresse_votant>)
> await instance.startProposalsRegistration()
> await instance.submitProposal("Description de la proposition")
> await instance.endProposalsRegistration()
> await instance.startVotingSession()
> await instance.vote(<proposalId>)
> await instance.endVotingSession()
> await instance.tallyVotes()
> const winner = await instance.winningProposalId()
> console.log(winner)
Tests
Pour exécuter les tests unitaires :

bash
Copy
truffle test
Fonctionnalités supplémentaires (DWYW)
Vote pondéré : Les votants peuvent avoir un poids de vote différent en fonction de leur rôle dans l'organisation.

Vote anonyme : Utilisation de techniques cryptographiques pour garantir la confidentialité des votes tout en maintenant la transparence.

Commentaires Natspec
Le code du smart contract est documenté en utilisant le format Natspec pour une meilleure compréhension et maintenabilité. Exemple :

solidity
Copy
/// @title Voting Contract
/// @author Nour
/// @notice Ce contrat gère un processus de vote décentralisé.
Démonstration
Vidéo de démo : [Lien vers la vidéo YouTube ou autre plateforme]

Déploiement public : [Lien vers Heroku, Vercel, GitHub Pages, etc.]


