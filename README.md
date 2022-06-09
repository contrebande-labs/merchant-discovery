# merchant-discovery
Ligthning Network Merchant Discovery Protocol. *Protocole de découverte socio-commerciale automatisée via le réseau Lightning de Bitcoin.*

C'est en français parce que c'est d'même. *Cry harder*, comme qu'y disaient.


## TL;DR

3 étapes faciles pour les pressés:

1) Démarrez et maintenez un noeud Bitcoin Lightning Network.
2) Mettez l'URL (Tor/HTTP ou DNS/TCP/IP/HTTP) de votre commerce électronique comme alias pour votre noeud créé à l'étape #1.
3) Chercher parmi les noeuds du réseau Bitcoin Lightning Network ceux qui annoncent des offres et des appels d'offres dans leur alias comme à l'étape #2, et ouvrez des canaux vers les noeuds les marchands qui vous intéressent. Voyez où ça vous mène.

## Comment j'ai appris à ne plus m'en faire et à aimer ma souveraineté

Nous reconnaissons la *maison* comme unité fondamentale de souveraineté, et le commerce comme forme essentielle de diplomatie entre les souverainetés domestiques. Nous redonnons ici à *maison* son sens *à la française*, selon lequel on entend à la fois *territoire*, *habitat* et un *commerce*, le tout sur plusieurs générations. L'objet de cette spécification est un ensemble de formats de données permettant la découverte des maisons entre elles à partir de leurs noeuds LN respectifs. Nous souhaitons utiliser au maximum les technologies et standards libres existants. Un simple agencement de ces technologies est donc ici proposé afin de permettre la négotiaction et l'exécution automatique de contrats commerciaux de gré à gré dans une diplomatie économique décentralisée.

Au minimum, pour être conforme au présent protocole, une maison doit établir et maintenir au moins:

1) deux liens point à point privés radio/fibre/Wireguard/Cjdns/Yggdrasil/etc. vers deux autres maisons;
2) un canal LN vers les noeuds distants de chacune de ces maisons;
3) un répondant permannent au protocole ci-défini accessible via le noeud LN de la maison.

Idéalement, chaque maison est économiquement active sur le réseau LN via son noeud (un agent) et pas seulement un répondant.

Commerce, import/export: Annoncer, offrir et consommer des produits et/ou services en transigeant via le canal LN susmentionné, incluant la litigation.

En ce sens, représentation [JSON-LD](https://json-ld.org) des ontologies [Schema.org](https://schema.org) et en particuler tous les dérivés de l'ontologie [Goodrelations](http://purl.org/goodrelations/) comme [Offer](https://schema.org/Offer) et [Demand](
https://schema.org/Demand).

Une [interface](https://schema.org/APIReference) de commerce électronique doit être exposée par les agents dans le système en s'inspirant probablement de [EDI](https://fr.wikipedia.org/wiki/Échange_de_données_informatisé) et de l'[interface de programmation d'avant-boutique par Shopify en GraphQL](https://shopify.dev/api/storefront), probablement en utilisant aussi [gRPC](https://grpc.io) puisque l'automatisation des interactions commerciales (machine à machine) et pas seulement la construction d'interfaces graphiques (humain à machine) sont visées ici. [OpenBazaar](https://github.com/OpenBazaar/openbazaar-go)


https://www.gs1.org/voc/?show=classes
https://schema.org/WebAPI


Ultimement, Incluant mais ne se limitant pas de , de tourisme, de solidarité, d'immigration et de relève selon les différents modèles de maison possibles : monastère (retraite, hotellerie, noviciat, voeux, règle, fondations), ermitage, commune, territoires, famille nucléaire, actionnariat, compagnonnage, garçonnière, mariages, concubinages, alliances, défense, représentation, litigation, médiation, réputation (stabilité, crédit, solidarité), assurances, etc.


* https://schema.org/DiscoverAction
* https://schema.org/Rating
* https://schema.org/EndorsementRating


## Pourquoi le Lightning Network ?

- Dominance et popularité de Bitcoin
- Secret par défaut
- Entretenir son propre noeud


Afin de simplifier l'accès à la souveraineté computationelle et financière, comme [Umbrel](https://getumbrel.com/), [Raspibolt](https://raspibolt.org/) ou [Raspiblitz](https://raspiblitz.org). [Éclair](https://github.com/ACINQ/eclair), [Core Lightning](https://github.com/ElementsProject/lightning) ou [LND](https://github.com/lightningnetwork/lnd). [Liste de projets autour du Lightning Network](https://github.com/bcongdon/awesome-lightning-network). Mettre un nom de domaine comme nom de de noeud LN.


- Extensibilité du protocole de messagerie


Idéalement, d'incorporer éventuellement le protocole gRPC dans les messages en oignon de LN directement : 
* [BOLT-01 (Messagerie)](https://github.com/lightning/bolts/blob/60550f989b56ce5009821449980d9bca7e63cb74/01-messaging.md)
* [BOLT-04 (Routage en oignon)](https://github.com/lightning/bolts/blob/60550f989b56ce5009821449980d9bca7e63cb74/04-onion-routing.md)
* [BOLT-12 (Protocole transactionnel)](https://github.com/lightning/bolts/blob/60550f989b56ce5009821449980d9bca7e63cb74/12-offer-encoding.md)

https://rusty-lightning.medium.com/onion-messaging-in-depth-d8e384ee4184


## Pourquoi *LN-d'abord* ?

Ligthning est ce que Bitcoin était à ses début: excitant et fraternel. Laissons les maximalistes s'entretuer. Mobilisation infinie autour de l'insécurité des détenteurs et des fournisseurs de services fiduciaires. Pour bâtir une vie, une maison, un commerce, une famille, mieux vaut tout connaître des fondantions sur lequelles on construit, et en particulier sur ses faiblesses. Parce que des faiblesses dans les fondations sont des vulnérabilités pour tout ce qui est au-dessus. Ni Bitcoin, ni LN ne sont pour nous des fins en soi. La fin en soi, c'est ce qu'on bâtit sur ces technologies: c'est à dire, une amélioration de notre qualité de vie par la décentralisation. Et la décentralisation consiste pour nous à remplacer les dépendences que nous avons envers les entités qui nient ou restraignent notre souveraineté d'être, de vivre, de penser, d'agir et de prospérer. Il serait donc futile de se libérer de ces dépendances en créant d'autres dépendances, d'autres servitudes, d'autres assujettissements. Nous ne sommes affiliés, ni ne prêtons allégeance, ni aux programmeurs de Bitcoin, ni aux détenteurs de Bitcoin, ni aux usagers de Bitcoin, ni aux mineurs de Bitcoin, ni aux fournisseurs de services Bitcoin, ni à Bitcoin lui-même. Nous ne tolèrons pas le maximalisme et nous le critiquons comme le maximalisme ne tolère pas ceux qui le critiquent. Et comme c'est le cas pour tous les totalitarismes, dogmatismes, orthodoxies, etc., les maximalistes se condamnent eux-même à l'intégrisme parce qu'ils parlent à travers leur chapeau et qu'ils ne veulent pas s'aventurer dans des débats qu'ils se savent condamner à perdre. Si pour toi être maximaliste veut dire arrêter d'être curieux, critique, innovateur, clairement, ça ne va pas marcher. Aussi donc, autant d'un point de vue technique que théorique, mon analyse des risques centralisateurs que posent les problèmes de la fongibilité, de l'algorithme de forage et de la Turing-incomplétude des contrats Bitcoin demeure valide. On peut ne pas être d'accord, parce qu'on peut avoir d'autres priorités dans la vie (eg. «wen lambo?»). Mais de censurer certains sujets tabous, ce n'est pas un signe d'intelligence. Il n'y aura jamais de désaccord zéro entre nous, mais je nous souhaite de toujours avoir la maturité d'un esprit ouvert.

- Infongibilité et large surface d'attaque publique
- Turing-incomplétude des contrats
- Gaspillage des externalités et centralisation de la frappe

## lngRPC

https://github.com/grpc/grpc/blob/master/doc/server-reflection.md
https://github.com/grpc/grpc/blob/master/doc/server_reflection_tutorial.md
https://github.com/grpc/grpc-java/blob/master/documentation/server-reflection-tutorial.md
https://github.com/grpc/grpc/blob/master/doc/compression.md
https://github.com/grpc/grpc/blob/master/doc/compression_cookbook.md
https://github.com/grpc/grpc/blob/master/doc/http-grpc-status-mapping.md
https://github.com/grpc/grpc/blob/master/doc/statuscodes.md
https://github.com/protocolbuffers/protobuf/blob/main/docs/implementing_proto3_presence.md
https://github.com/protocolbuffers/protobuf/blob/main/docs/field_presence.md
https://github.com/protocolbuffers/protobuf/blob/main/docs/jvm_aot.md
https://developers.google.com/protocol-buffers/docs/proto#options

https://json-ld.org/spec/latest/json-ld/
https://schema.org/docs/jsonldcontext.json

https://github.com/protocolbuffers/protobuf/blob/main/src/google/protobuf/any.proto
https://github.com/protocolbuffers/protobuf/blob/main/src/google/protobuf/api.proto
https://github.com/protocolbuffers/protobuf/blob/main/src/google/protobuf/descriptor.proto
https://github.com/protocolbuffers/protobuf/blob/main/src/google/protobuf/duration.proto
https://github.com/protocolbuffers/protobuf/blob/main/src/google/protobuf/field_mask.proto
https://github.com/protocolbuffers/protobuf/blob/main/src/google/protobuf/source_context.proto
https://github.com/protocolbuffers/protobuf/blob/main/src/google/protobuf/struct.proto
https://github.com/protocolbuffers/protobuf/blob/main/src/google/protobuf/timestamp.proto
https://github.com/protocolbuffers/protobuf/blob/main/src/google/protobuf/type.proto
https://github.com/protocolbuffers/protobuf/blob/main/src/google/protobuf/wrappers.proto
https://github.com/protocolbuffers/protobuf/blob/main/src/google/protobuf/compiler/plugin.proto

https://github.com/grpc-ecosystem/grpc-gateway
https://github.com/ysugimoto/grpc-graphql-gateway
https://github.com/confluentinc/schema-registry
https://github.com/chrusty/protoc-gen-jsonschema
https://github.com/Embedded-AMS/EmbeddedProto
https://github.com/google/gnostic


## Infrastructure à clés publiques (PKI)

* https://github.com/cert-manager/cert-manager
* https://github.com/malikzh/NCANode
* https://github.com/xipki/xipki
* https://github.com/cloudflare/cfssl
* https://github.com/dogtagpki/pki
* https://github.com/Keyfactor/ejbca-ce
* https://github.com/openxpki/openxpki
* https://github.com/square/subzero
* https://github.com/Nitrokey
* https://github.com/solokeys
* https://github.com/trussed-dev

## Implémentations pertinentes

* https://github.com/ACINQ/eclair
* https://github.com/bitcoinj/bitcoinj
* https://github.com/ACINQ/bitcoin-lib
* https://github.com/lightningnetwork/lnd/tree/master/lnrpc
* https://github.com/apache/any23
* https://github.com/jsonld-java/jsonld-java
* https://github.com/filip26/titanium-json-ld
* https://github.com/io-informatics/jackson-jsonld
* https://github.com/google/schemaorg-java
* https://github.com/kropp/jsonld-metadata
* https://ethereum.org/en/developers/docs/programming-languages/java/
* https://github.com/web3j/web3j
* https://github.com/web3j/web3j-evm
* https://github.com/web3j/web3j-unit
* https://github.com/web3j/web3j-quorum
* https://github.com/ConsenSys/quorum
* https://github.com/epirus-io/epirus-cli
* https://github.com/alexbosworth/invoices
* https://github.com/altangent/node-lightning/tree/main/packages/invoice
* https://github.com/puzzle/lightning-beer-tap
* https://github.com/jamaljsr/polar
* https://github.com/LN-Zap/node-lnd-grpc
* https://github.com/ZeusLN/zeus
* https://github.com/shesek/spark-wallet
* https://gitlab.com/bluesky-community1/decentralized-ecosystem/-/blob/master/README.md
* https://protocol.ai/
* https://github.com/OpenBazaar/openbazaar-go
* https://github.com/bisq-network/bisq


## Infrastructure Kubernetes

* https://medium.com/@Judezhu87/running-bitcoind-node-on-kubernetes-1d833212b1a
* https://tigran.tech/scaling-bitcoin-node-with-kubernetes/
* https://github.com/coderiseio/bitcoin-core-kubernetes

# Infrastructure Internet
* https://ispdesign.ui.com/
* https://www.ui.com/uisp/ptp-bridging
* https://ca.store.ui.com/collections/operator-airmax-and-ltu/products/airfiber-5xhd-1
* https://www.pc-canada.com/item/ubiquiti-airfiber-af5u-1-gbit-s-wireless-bridge/af-5u
* https://onionbalance.readthedocs.io/en/latest/v3/tutorial-v3.html
* https://gitlab.torproject.org/tpo/core/torspec/-/blob/main/proposals/265-load-balancing-with-overhead.txt
* https://gitlab.torproject.org/tpo/core/torspec/-/blob/main/proposals/330-authority-contact.md


# Transactions réversibles
* https://acinq.github.io/eclair/#createinvoice

# Taux de change
* https://api.newton.co/dashboard/api/rates/
* https://api.shakepay.com/rates

# Capacité entrante, rebalancement et routage LN
* https://github.com/bitrefill/thor-api-doc
* https://github.com/synonymdev/blocktank-server
* https://coincept.com
* https://github.com/lnd-routing/lnd-routing
* https://amboss.space/magma
* https://github.com/synonymdev/blocktank-client
* https://github.com/lightninglabs/loop
* https://lightningconductor.net/channels
* https://lightningto.me
* https://peernode.net
* https://lnbig.com
* https://lightningnetwork.plus
* https://github.com/ACINQ/eclair/blob/master/docs/TrampolinePayments.md
* https://github.com/ACINQ/eclair/blob/master/docs/CircularRebalancing.md