# merchant-discovery
Ligthning Network Merchant Discovery Protocol. *Protocole pour la découverte automatique de relations commerciales via le réseau Lightning de Bitcoin.*

C'est en français parce que c'est d'même. *Cry harder*, comme qu'y disaient.

L'objet de cette spécification est un ensemble de formats de données permettant la découverte de fournisseurs et de clients à partir des noeuds LN respectifs desdits acteurs économiques. L'esprit du présent document est d'utiliser au maximum les technologies et standards libres existants. Leur simple agencement est donc ici proposé afin de permettre la négotiaction et l'exécution automatiques de contrats commerciaux de gré à gré dans une justice économique décentralisée.

Afin de simplifier, comme [Umbrel](https://getumbrel.com/), [Raspibolt](https://raspibolt.org/) ou [Raspiblitz](https://raspiblitz.org). [Éclair](https://github.com/ACINQ/eclair), [Core Lightning](https://github.com/ElementsProject/lightning) ou [LND](https://github.com/lightningnetwork/lnd). [Liste de projets autour du Lightning Network](https://github.com/bcongdon/awesome-lightning-network).

[Schema.org](https://schema.org) et [JSON-LD](https://json-ld.org)

https://schema.org/BusinessFunction
https://schema.org/Offer
https://schema.org/OfferForPurchase
https://schema.org/Demand
https://schema.org/Order
https://schema.org/OrderItem
https://schema.org/Invoice
https://schema.org/Rating
https://schema.org/EndorsementRating
https://schema.org/Person
https://schema.org/Organization
https://schema.org/DiscoverAction
https://schema.org/MoneyTransfer
https://schema.org/APIReference

S'inspirant probablement de l'[interface de programmation d'avant-boutique par Shopify en GraphQL](https://shopify.dev/api/storefront), probablement en utilisant aussi [gRPC](https://grpc.io) puisque nous souhaitons l'automatisation des interactions commerciales (machine à machine) et pas seulement la construction d'interfaces graphiques (humain à machine).

Idéalement, d'incorporer éventuellement le protocole gRPC dans les messages "onion" de LN directement : 

https://github.com/lightning/bolts/blob/60550f989b56ce5009821449980d9bca7e63cb74/01-messaging.md
https://github.com/lightning/bolts/blob/60550f989b56ce5009821449980d9bca7e63cb74/04-onion-routing.md
https://github.com/lightning/bolts/blob/60550f989b56ce5009821449980d9bca7e63cb74/12-offer-encoding.md




## [Infrastructure à clé publiques (PKI)](https://fr.wikipedia.org/wiki/Infrastructure_%C3%A0_cl%C3%A9s_publiques)

https://github.com/cert-manager/cert-manager
https://github.com/malikzh/NCANode
https://github.com/xipki/xipki
https://github.com/cloudflare/cfssl
https://github.com/dogtagpki/pki
https://github.com/Keyfactor/ejbca-ce
https://github.com/openxpki/openxpki
https://github.com/square/subzero
https://github.com/Nitrokey
https://github.com/solokeys
https://github.com/trussed-dev

## Java

https://github.com/apache/any23
https://github.com/jsonld-java/jsonld-java
https://github.com/filip26/titanium-json-ld
https://github.com/io-informatics/jackson-jsonld
https://github.com/google/schemaorg-java
https://github.com/kropp/jsonld-metadata


## Kubernetes

https://medium.com/@Judezhu87/running-bitcoind-node-on-kubernetes-1d833212b1a
https://tigran.tech/scaling-bitcoin-node-with-kubernetes/
https://github.com/coderiseio/bitcoin-core-kubernetes