---
title: Frigi produktstrukturer
description: Dette emnet beskriver hvordan du kan frigir produktstrukturer i tillegg til å frigi produkter sammen med de tekniske versjonene. På denne måten kan du sikre at teknisk relevante produktdata enkelt kan brukes på nytt i ulike juridiske enheter.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductReleaseSiteBulkEdit, EngChgProductReleaseSendListPage, EngChgProductReleaseSendDetails,EngChgProductReleaseSelection,EngChgProductReleaseReceiveListPage, EngChgProductReleaseReceiveDetails, EngChgProductReleasePreviewPane, EngChgProductReleasePolicy, EngChgProductReleasePart, EngChgProductReleaseNote
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 68f091cca9c3c2baa03813553127ee41abe6d522
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434863"
---
# <a name="release-product-structures"></a>Frigi produktstrukturer

[!include [banner](../includes/banner.md)]

Hvis du vil sikre at teknisk relevante produktdata enkelt kan brukes på nytt i ulike juridiske enheter, kan du frigi fullstendige produktstrukturer i tillegg til å frigi produkter sammen med de tekniske versjonene. Du kan derfor frigi stykklistestrukturer med flere nivåer sammen med den overordnede i én enkelt frigivelseshandling. I dette tilfellet frigis også stykklisten og produktene på lavere nivå.

Tekniske produkter opprettes og vedlikeholdes av det tekniske firmaet på en slik måte at de oppfyller kravene til kvalitet mens de utformes. Hvert driftsfirma som produserer et produkt, trenger samme produkt og underliggende stykkliste. Avhengig av produksjonsanlegget kan ruten opprettes lokalt. I dette tilfellet frigir du ikke en rute sammen med produktet. For juridiske enheter som vil selge produktene, men som ikke produserer dem, er det ikke sikkert at stykklisten kreves.

For at prosessen skal bli mer effektiv, kan alle teknisk relevante data frigis til andre driftsfirmaer samtidig. Disse dataene inkluderer produktstrukturen. Under frigivelsesprosessen kan du velge hvilken del av produktdataene som skal frigis.

Hvis du vil ha mer informasjon om tekniske firmaer og driftsfirmaer, kan du se [Tekniske firmaer og dataeierskapsregler](engineering-org-data-ownership-rules.md) .

Vær oppmerksom på at du kan frigi både standardprodukter og tekniske produkter sammen med produktstrukturen. I løpet av denne prosessen vil hele produktstrukturen bli frigitt, også stykklisten og ruten fra firmaet som produktene frigis i.

Hvis du vil ha et eksempel på hvordan du frigir et produkt, kan du se [Frigi et teknisk produkt i et lokalt firma](engineering-scenarios.md#release)

## <a name="released-data-for-a-product-when-the-release-product-structure-is-used"></a>Frigitte data for et produkt når den frigitte produktstrukturen brukes

Følgende data er inkludert i frigivelsen av tekniske produkter:

- **Produktdata** – Det opprettes et nytt frigitt produkt.
- **Tekniske versjonsdata** – Den tekniske versjonen og dataene blir opprettet eller oppdatert. Vær oppmerksom på at hvis du frigir den samme tekniske versjonen til et driftsfirma, vil de tekniske dataene bli overskrevet.
- **Tekniske attributter** – De tekniske attributtene og deres verdier opprettes eller oppdateres.
- **Teknisk stykkliste** – Den tekniske stykklisten og tilhørende linjer kan opprettes eller oppdateres. Hvis du vil ha mer informasjon om dataeierskap, kan du se [Produkteiere](product-owner.md).
- **Tekniske ruter** – De tekniske rutene og deres operasjoner kan opprettes eller oppdateres. Hvis du vil ha mer informasjon om dataeierskap, kan du se [Produkteiere](product-owner.md).
- **Tekniske dokumenter** – De tekniske dokumentene som er koblet til den tekniske versjonen, opprettes eller oppdateres.

Når du aktiverer behandling av teknisk endring på systemet, er den frigitte produktstrukturen tilgjengelig. I tillegg vil standardprodukter inkludere stykklister og ruter når de frigis.

## <a name="product-acceptance"></a>Produktgodkjenning

**Produktgodkjenning** er en nøkkelparameter som påvirker frigivelsesprosessen. Du kan angi denne parameteren for hvert firma ved å gå til **Behandling av teknikk endring \> Oppsett \> Parametere for behandling av teknisk endring**. Hvis du vil ha mer informasjon, kan du se [Parametere for behandling av teknisk endring](engineering-parameters.md).

### <a name="automatic-product-acceptance"></a>Automatisk produktgodkjenning

Hver frigivelse av tekniske produkter starter når noen fra det tekniske firmaet velger et produkt å frigi. Når parameteren **Produktgodkjenning** er satt til *Automatisk*, bestemmer brukeren ved det tekniske firmaet hvilke produktdata som skal frigis til driftsfirmaene automatisk. Produktet frigis automatisk til firmaene som er valgt i frigivelsesveiviseren.

### <a name="manual-product-acceptance"></a>Manuell produktgodkjenning

Hver frigivelse av tekniske produkter starter når noen fra det tekniske firmaet velger et produkt å frigi. Når parameteren **Produktgodkjenning** er satt til *Manuell*, bestemmer brukeren ved det tekniske firmaet hvilke produktdata som skal frigis til driftsfirmaene. En bruker fra hvert driftsfirma ser deretter gjennom produktdataene og bestemmer om den skal godta frigivelsen. Brukeren ved driftsfirmaet kan angi følgende alternativer når dataene mottas:

- Hvis produktene (oppdateringene) ikke er relevante for driftsfirmaet, kan brukeren velge ikke å godta frogivelsen.
- Brukeren kan endre varemalen for nye produkter.
- Brukeren kan velge om produktet skal frigis sammen med stykklister eller ruter, og om de skal frigis som godkjent og aktive.
- Brukeren kan endre de gyldighetsdatoene for produktene.

Hvis du vil ha et eksempel på hvordan du kan godtar et produkt, kan du se [Se gjennom og godta produktet før du frigir det i det lokale firmaet](engineering-scenarios.md#accept).

> [!NOTE]
> For standardprodukter kan du frigi fra en hvilken som helst juridisk enhet til en hvilken som helst annen juridisk enhet. For tekniske produkter er den eneste juridiske enheten du kan frigi fra, det tekniske firmaet.

## <a name="release-policies"></a>Frigivelsespolicyer

Ikke alle driftsfirmaer trenger de samme produktdataene. Vanligvis vil driftsfirmaer som produserer tekniske produkter, kreve en stykkliste, mens driftsfirmaet som bare selger tekniske produkter, ikke krever en stykkliste. Du kan bruke frigivelsespolicyer til å fastsette parameterne som brukes til frigivelsen av produkter.

For tekniske produkter tilordnes frigivelsespolicyen i kategorien for teknisk produkt, og feltet er obligatorisk. For standardprodukter tilordnes policyen til det delte produktet, og feltet er valgfritt.

Hvis du vil ha mer informasjon om kategorier for teknisk produkt, kan du se [Utviklingsversjoner og utviklingsproduktkategorier](engineering-versions-product-category.md).

Under frigivelsesprosessen kan du påvirke innstillingene.

## <a name="create-and-manage-product-release-policies"></a>Opprett og behandle policyer for produktfrigjøring

Hvis du vil arbeide med produktfrigivelsespolicyer, går du til **Behandling av teknisk endring \> Oppsett \> Produktfrigivelsespolicyer**. Følg deretter ett av disse trinnene.

- Hvis du vil opprette en ny policy, velger du **Nytt** i handlingsruten, og deretter angir du feltene som beskrevet i følgende underavsnitt.
- Hvis du vil redigere en eksisterende policy, velger du det i listeruten, velger **Rediger** i handlingsruten og angir deretter feltene som beskrevet i følgende underavsnitt.
- Hvis du vil slette en eksisterende policy, velger du den i listeruten, velger **Rediger** i handlingsruten og kontrollerer deretter at alternativet **Aktiv** er satt til **Nei** i hurtigfanen *Generelt*. Velg deretter **Slett** i handlingsruten.

### <a name="header"></a>Hode

Angi følgende felter i toppteksten til en produktfrigivelsespolicy.

| Felt | beskrivelse |
|---|---|
| Navn | Angi et navn for policyen. |
| beskrivelse | Angi en beskrivelse av policyen. |

### <a name="general-fasttab"></a>Hurtigfanen Generelt

Angi følgende felter på hurtigfanen **Generelt** til en produktfrigivelsespolicy.

| Felt | beskrivelse |
|---|---|
| Produkttype | Velg om policyen gjelder for produkter av typen *Vare* eller *Tjeneste*. Du kan ikke endre denne innstillingen etter at du har lagret posten. |
| Bruk maler | Velg ett av følgende alternativer for å angi om og hvordan produktfrigivelsesmaler skal brukes når policyen brukes:<ul><li>**Alltid** – Et malfrigitt produkt alltid må brukes for frigivelser. Hvis du velger dette alternativet, bruker du **Alle produkt**-hurtigfanen til å angi malen som skal brukes for hvert firma du frigir til. Hvis du ikke angir en mal for hvert firma som er oppført i hurtigfanen **Alle produkter**, vil du få en feilmelding når du prøver å lagre policyen.</li><li>**Valgfritt** – Hvis et malfrigitt produkt er angitt for et firma som er oppført i hurtigfanen **Alle produkter**, vil denne malen bli brukt når du frigir til dette firmaet. Hvis ikke vil ingen mal bli brukt. Hvis du velger dette alternativet, kan du lagre policyen uten å tilordne maler til alle firmaer. (Ingen advarsel vil bli vist.)</li><li>**Aldri** – Ingen malfrigitte produkter blir brukt for noen firmaer som du frigir til, selv om en mal er angitt for firmaer som er oppført i hurtigfanen **Alle produkter**. Malkolonnene vil ikke være tilgjengelige.</li></ul> |
| Aktive | Bruk dette alternativet til å opprettholde frigivelsespolicyene. Angi til *Ja* for alle frigivelsespolicyene du bruker. Angi til *Nei* for å merke en frigivelsespolicy som inaktiv når den ikke brukes. Legg merke til at du ikke kan deaktivere en frigivelsespolicy som er tilordnet til en kategori for teknisk produkt, og du kan bare slette inaktive frigivelsespolicyer. |

### <a name="all-products-fasttab"></a>Hurtigfanen Alle produkter

I hurtigfanen **Alle produkter** legger du til en rad for hvert driftsfirma du vil bruke denne policyen til å frigi til. Bruk knappene i hurtigfanen **Alle produkter** til å legge til og fjerne rader etter behov. For hver rad du legger til, angir du følgende felter:

> [!NOTE]
> Innstillingene i hurtigfanen **Alle produkter** gjelder både tekniske produkter og standardprodukter.

| Felt | beskrivelse |
|---|---|
| Firmakonto-ID | Velg firmaet som raden gjelder for. Parameterne på raden blir brukt når produkter frigis til dette firmaet. |
| Malfrigitt produkt | Legg til en mal for produktet. |
| Kopier stykklistegodkjenning | Merk av i denne avmerkingsboksen for å kopiere statusen for stykklistegodkjenning til mottaksfirmaet. |
| Kopier stykklisteaktivering | Merk av i denne avmerkingsboksen for å kopiere statusen for stykklisteaktivering til mottaksfirmaet. |
| Kopier rutegodkjenning | Merk av i denne avmerkingsboksen for å kopiere statusen for rutegodkjenning til mottaksfirmaet.|
| Kopier ruteaktivering | Merk av i denne avmerkingsboksen for å kopiere statusen for ruteaktivering til mottaksfirmaet. |

### <a name="option-parameters-for-engineering-products-fasttab"></a>Hurtigfanen Alternativparametere for tekniske produkter

Hver gang du legger til en rad i hurtigfanen **Alle produkter**, opprettes det også en rad som har en samsvarende **firmakonto-ID**-verdi, i hurtigfanen **Alternativparametere for tekniske produkter**. Hvis du fjerner en rad fra hurtigfanen **Alle produkter**, fjernes også raden som har en samsvarende **firmakonto-ID**-verdi, i hurtigfanen **Alternativparametere for tekniske produkter**.

For hver rad som vises i hurtigfanen **Alternativparametere for tekniske produkter**, angir du følgende felter:

> [!NOTE]
> Innstillingene i hurtigfanen **Alternativparametere for tekniske produkter** gjelder bare tekniske produkter.

| Felt | beskrivelse |
|---|---|
| Malstykkliste | Når et produkt som har en stykkliste, blir frigitt, blir linjene i den angitte malstykklisten lagt til. Dette feltet er nyttig for å legge til lokale komponenter, for eksempel pakking eller instruksjoner på det lokale språket. |
| Malrute | Når et produkt som har en rute, blir frigitt, blir linjene i den angitte malen lagt til. |
| Kopier gyldighet | Velg om gyldighetsdatoer skal kopieres fra det tekniske firmaet til driftsfirmaet når du frigir produkter. |
| Legg til automatisk i frigivelsesforslag | Merk av i denne avmerkingsboksen for produkter som automatisk skal frigis på ordre om teknisk endring. På denne måten kan produkter som tilhører kategorier for teknisk produkt som bruker denne frigivelsespolicyen, automatisk frigis til driftsfirmaer der dette alternativet er definert. (Hvis du vil ha mer informasjon, kan du se [Behandle endringer i tekniske produkter](engineering-change-management.md).)

### <a name="review-each-product-when-you-release-it"></a>Gå gjennom hvert produkt når du frigir det

Når tekniske produkter som har stykklister eller ruter frigis, blir parameterne satt til standardverdier som angitt i frigivelsespolicyen. Som en bruker kan du påvirke denne virkemåten på frigivelsessiden når du bruker den frigitte produktstrukturen.

Hvis du vil frigi tekniske produkter, velger du produktene som skal frigis på siden **Frigitte produkter**, og deretter velger **Frigi produktstruktur** for å åpne frigivelsesveiviseren. Siden **Velg tekniske produkter som skal frigis** viser produktene. Velg et enkelt produkt, og velg deretter **Frigivelsesdetaljer** for å se gjennom frigivelsesdetaljene for produktet.

På siden **Frigivelsesdetaljer** kan du endre verdien for feltene **Mottak stykkliste**, **Kopier stykklistegodkjenning**, **Kopier stykklisteaktivering**, **Motta stykkliste**, **Kopier rutegodkjenning** og **Kopiere ruteaktivering**. I send/hent-scenarioet kan du endre verdien for de samme feltene på mottakssiden, forutsatt at stykklisten og ruten frigis.

## <a name="product-owners-and-product-releases"></a>Produkteiere og produktfrigivelser

Siden produkteiere vet hvilke juridiske enheter som trenger produktene, kan et produkt bare frigis av medlemmene i produkteiergruppen for produktet. Andre brukere kan ikke frigi produkter de ikke eier.

Denne virkemåten gjelder bare når et produkt velges direkte for frigivelse. Produkter som er del av en annen produktstruktur via en stykkliste, *kan* frigis av brukere som ikke er eiere, når de frigir det overordnede produktet, forutsatt at de eier det overordnede produktet.

Produkt X er for eksempel tilordnet til produkteiergruppen *Designkabinetter*. Produkt X er også en del av stykklisten for produkt Y, som er tilordnet til produkteiergruppen *Designhøyttalere*. Hvis en bruker fra produkteiergruppen *Designhøyttalere* frigir produkt Y og stykklisten, blir produkt X frigitt sammen med produkt Y.

Hvis du vil ha mer informasjon, kan du se [Produkteiere](product-owner.md).
