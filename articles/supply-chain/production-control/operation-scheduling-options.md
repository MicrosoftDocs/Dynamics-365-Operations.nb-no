---
title: Alternativer for grovplanlegging
description: "Dette emnet beskriver alternativene for grovplanlegging. Du kan bruke grovplanlegging for å få et generelt estimat over produksjonsprosessen over tid."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 198123
ms.assetid: d680d7be-da64-4132-89fe-ad2fa59afb77
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 56eeb2b56261dc3e576192c0ede405996d82b2b7
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="operations-scheduling-options"></a>Alternativer for grovplanlegging

[!INCLUDE [banner](../includes/banner.md)]

Dette emnet beskriver alternativene for grovplanlegging. Du kan bruke grovplanlegging for å få et generelt estimat over produksjonsprosessen over tid.

Grovplanlegging beregner følgende informasjon for en produksjonsordre:

-   Start- og sluttdatoene er angitt for produksjonsordren og hver operasjon.
-   Ressurser er tildelt til operasjoner.

Flere innstillingene bestemmer hvordan produksjonsplaner beregnes. Du definerer disse innstillingene på siden **Grovplanlegging**. Følgende informasjon beskriver alternativer for planlegging.

## <a name="operations-scheduling"></a>Grovplanlegging
### <a name="scheduling-direction"></a>Planleggingsretning

Planleggingsretningen er grunnleggende for planleggingsprosessen. Produksjon kan planlegges fremover eller bakover fra en hvilken som helst dato, avhengig av tidspunkt for behov og planlegging.

-   **Planlegging fremover**– du kan planlegge at produksjonen skal starte så tidlig som mulig. Produksjonen kan startes i dag, i morgen eller fra en hvilken som helst dato i fremtiden. Produksjonen planlegges for start den tidligste mulige datoen, og planlegges fremover i tid til den tidligste mulige sluttdatoen.
-   **Planlegging bakover**– du kan planlegge at produksjonen skal starte så sent som mulig. Tidsplanen baseres på datoen da produksjonen må være fullført, og teller bakover til den seneste mulige datoen da produksjonen kan startes uten at fristen som er satt som mål, overskrides.

Følgende alternativer er tilgjengelige:

-   **Fremover fra i dag** – Planlegg fremover fra gjeldende dato. (Den gjeldende datoen er systemdatoen.)
-   **Fremover fra planlagt start** – Planlegg fremover fra en tidligere startdato. Hvis ingen planlegging finnes fra før, settes planleggingsretning fra gjeldende dato.
-   **Fremover fra planleggingsdato** - Planlegg fremover fra datoen som er angitt i **Planleggingsdato**-feltet. Hvis du ikke angir en planleggingsdato, settes planleggingsretning fra gjeldende dato.
-   **Bakover fra leveringsdato** - Planlegg bakover fra leveringsdatoen angitt for produksjonsordren. Hvis du velger dette alternativet, men det ikke er angitt en leveringsdato, settes leveringsdatoen til den gjeldende datoen.
-   **Bakover fra planlagt slutt** - Planlegg bakover fra en sluttdato som er beregnet tidligere. Hvis ingen planlegging finnes fra før, settes sluttdatoen til gjeldende dato.
-   **Bakover fra planleggingsdato** - Planlegg bakover fra datoen som er angitt i **Planleggingsdato**-feltet. Hvis du ikke angir en planleggingsdato, brukes gjeldende dato. Bakover fra planleggingsdato blir beregnet for produksjonsordren siste gang et behov ble beregnet. Hvis ingen dato er angitt for produksjonsordren, brukes gjeldende systemdato.
-   **Bakover fra termindatoen** - Planlegging bakover fra termindatoen som er ble beregnet for produksjonsordren forrige gang et behov ble beregnet. Hvis ingen termindato er angitt for produksjonsordren, brukes gjeldende systemdato.
-   **Som ved siste planlegging** - I forbindelse med grovplanlegging og finplanlegging blir valgte planleggingsretning og -dato lagret. Du kan derfor velge dette alternativet for senere planlegging. Hvis det ikke finnes tidligere planlegging av produksjonsordren, er planleggingen bakover fra gjeldende systemdato.
-   **Forover fra i morgen** - Planlegging forover fra gjeldende dato pluss én dag.
-   **Fremover fra forrige jobb** - Dette alternativet er bare relevant ved finplanlegging. Hvis du velger denne planleggingsretningen for grovplanlegging, vil produksjonsordren bli planlagt fremover fra gjeldende dato. Finplanlegging er basert på en bestemt jobb, og alle andre jobber for produksjonen blir planlagt i henhold til den jobben.
-   **Bakover fra forrige jobb** - Dette alternativet er bare relevant ved finplanlegging. Hvis du velger denne planleggingsretningen for grovplanlegging, vil planlagte bestillinger bli planlagt bakover fra gjeldende dato. Finplanlegging er basert på en bestemt jobb, og alle andre jobber for produksjonen blir planlagt i henhold til den jobben.

### <a name="scheduling-date"></a>Planleggingsdato

Denne datoen brukes for planleggingsretningene **Fremover fra planleggingsdato** og **Bakover fra planleggingsdato**. Planleggingen foretas deretter bakover eller fremover fra denne datoen. Hvis du vil ha mer informasjon, se Planleggingsretning i forrige avsnitt.

### <a name="recalculate-bom-levels"></a>Beregn stykklistenivåer på nytt

Når du velger **Beregn stykklistenivåer på nytt**, beregnes de valgte stykklistenivåene på nytt for å garantere riktig planleggingssekvens.

## <a name="limitations"></a>Begrensninger
### <a name="finite-capacity"></a>Begrenset kapasitet

Planleggingen er avhengig av at ressursene som kreves for å fullføre produksjonen, er tilgjengelige. Hvis kapasiteten er for liten, kan produksjonsordrene forsinkes ellers stoppe helt. Hvis det brukes begrenset kapasitet i driftsplanleggingen, tas det hensyn til eksisterende kapasitetsreserveringer som gjøres på ressursene, og denne kapasiteten vises som utilgjengelig. Produksjonsordren planlegges på grunnlag av tilgjengeligheten for ressursen som kreves. Grovplanlegging bruker den angitte operasjonssekvensen til å bestemme operasjonsrekkefølgen i produksjonsruten. Grovplanlegging reserverer kapasitet i ressursgrupper, basert på operasjonstidene som er definert i produksjonsruten. Ressursgruppenes kapasitet er summen av tilgjengelig kapasitet for alle ressursene i ressursgruppene.

### <a name="finite-material"></a>Begrenset materiale

Planleggingen er også avhengig av at materialene som kreves i produksjonen, er tilgjengelig. Ikke nok komponenttilgjengelighet kan også forårsake forsinkelser i produksjonen. Planlegging kan også baseres på bruk av materialer. Bare angi materialene som må være tilgjengelige for produksjon, i stedet for materialene som ikke er viktige. Denne typen planlegging kalles planlegging med begrenset materiale. Når du angir begrenset materiale, planlegges produksjonen basert på om materialer er tilgjengelige. **Merk:** Hvis optimalisering skjer på både kapasitet og materialer, beregnes produksjonen slik at det tas hensyn til begge begrensningene. Det tas hensyn til tilgjengeligheten av kapasitet og materialer, og produksjonsordreoperasjoner kan ikke planlegges å starte før kapasitet og materialer er tilgjengelige samtidig og i nødvendige mengder. Merk av i denne avmerkingsboksen for å angi at materialene skal vurderes begrenset under planlegging. Hvis materialene er begrenset, vil materialdekningen for denne tidsperioden vurderes. Med andre ord tar planleggingen hensyn til de fremtidige datoene som beregnes for varene. Planlegging reserverer råvarer og bryter ned gjeldende produksjon. Hvis planlegging skjer flere ganger, vil bare første planlegging kjøre en nedbryting og foreta reserveringer. Hvis du foretar endringer i produksjonsstykklisten eller ruten, vil neste planlegging kjøre en nedbryting. Nedbrytingen forutsetter at materialene behøves samme dag. Fordi produksjonen ikke blir planlagt samtidig som behovsnedbrytningen, blir gjeldende dato beste estimat for når varene vil bli tilgjengelige. Nedbrytingen kontrollerer deretter når varene er tilgjengelige. Hvis varene er tilgjengelige, er det mulig å oppfylle produksjonsbehovet. Hvis varene ikke er tilgjengelige innen gjeldende dato, blir det generert en planlagt bestilling og det blir valgt en motkonto for planlagte ordre. Hvis automatisk autorisasjon er definert for den planlagte bestillingen, vil den planlagte bestillingen automatisk bli autorisert for innkjøp eller produksjon. Produksjonsstatusen endres automatisk til statusen angitt i **Ønsket produksjonsstatus**-feltet i dialogboksen **Dekningsgrupper**. Hvis det ikke er merket av i avmerkingsboksen, var råmaterialene tilgjengelige hele tiden. Derfor tar ikke planlegging i betraktning om materialene er tilgjengelige på tidspunktet for behovet.

### <a name="finite-property"></a>Begrenset egenskap

Merk av i denne boksen hvis finplanlegging skal omfatte egenskapskrav.

### <a name="keep-production-unit"></a>Behold produksjonsenhet

Velg om planleggingsmotoren skal planlegge ressurser som allerede er angitt i produksjonsenheten.

### <a name="keep-warehouse-from-resource"></a>Behold lager fra ressurs

Velg om planleggingsmotoren skal planlegge bare ressursene som er knyttet til innleveringslageret som er angitt på ressursen.

## <a name="references"></a>Referanser
### <a name="schedule-references"></a>Planreferanser

Når referanser avhenger av produksjonsordrer, er de også kjent som underproduksjoner. Underproduksjoner kan planlegges som en del av planleggingen av en produksjonsordre. Velg denne avmerkingsboksen hvis planleggingen av underproduksjoner skal baseres på planleggingen av hovedproduksjonen. I forbindelse med hovedproduksjon planlegges overliggende produksjon fremover og underliggende produksjoner bakover. Du kan vise produksjonsordrereferanser i feltet **Referansenivå** på siden **Produksjonsordrer**.

### <a name="synchronize-references"></a>Synkroniser referanser

Du kan synkronisere referanser med produksjonsordren. Hvis dette alternativet velges, flyttes datoene for underproduksjonene og justeres når det gjøres endringer i produksjonsordreplanen. Hvis en produksjonsordre har én eller flere underproduksjoner, kan det hende at du vil planlegge underproduksjonene sammen med hovedproduksjonen. I så fall kan ikke hovedproduksjonen startes før de tilknyttede underproduksjonene er fullført. Velg derfor denne avmerkingsboksen hvis planleggingen av underproduksjoner skal baseres på start- og sluttidspunkt for den valgte produksjonen. Du kan bare merke av i denne avmerkingsboksen hvis det også er merket av for**Planreferanser**.

## <a name="cancellation"></a>Annullering
### <a name="cancel-queue-time"></a>Avbryt køtid

Merk av i denne boksen for å utelate køtid i planleggingen.

### <a name="cancel-setup"></a>Avbryt oppsett

Merk av i denne boksen for å utelate oppstillingstid i planleggingen.

### <a name="cancel-process"></a>Avbryt prosess

Merk av i denne boksen for å utelate operasjonstid i planleggingen.

### <a name="cancel-overlap"></a>Avbryt overlapping

Merk av i denne boksen for å utelate overlappingstid i planleggingen.

### <a name="cancel-transport"></a>Avbryt transport

Merk av i denne boksen for å utelate transittid i planleggingen.

## <a name="set-default"></a>Angi standard
Du kan lagre de gjeldende verdiene som standardverdier. Det finnes to alternativer:

-   Angi som min standard
-   Angi som standard for alle


<a name="see-also"></a>Se også
--------

[Grovplanlegging](operations-scheduling.md)




