---
title: Grovplanlegging
description: Dette emnet gir informasjon om grovplanlegging. Du kan bruke grovplanlegging for å få et generelt estimat over produksjonsprosessen over tid.
author: ChristianRytt
manager: tfehr
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 198073
ms.assetid: 12c28b11-80aa-4668-b15b-724cb24890bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e95374e0aebca825f589f13eda389d6612737181
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434474"
---
# <a name="operations-scheduling"></a>Grovplanlegging

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om grovplanlegging. Du kan bruke grovplanlegging for å få et generelt estimat over produksjonsprosessen over tid.

Du kan planlegge produksjonen på operasjonsnivået og jobbnivået. I motsetning til finplanlegging, deler grovplanlegging ikke operasjonene for produksjonsruten inn i jobber. Hvis du vil ha flere detaljer i planleggingen, for eksempel informasjon om gjeldende kapasitet, kan du kjøre finplanlegging etter at du kjører grovplanlegging. Du kan også velge bare å kjøre finplanlegging. Finplanlegging brukes vanligvis til å planlegge enkeltjobber på shop floor i en umiddelbar eller kortsiktig tidsramme.

## <a name="components-of-operations-scheduling"></a>Komponenter i grovplanlegging
Hovedkomponentene i grovplanlegging er planleggingsretningen, ressurskapasiteten og materialoptimalisering. Når du bruker grovplanlegging, kan du oppnå følgende mål:

-   Styre planleggingsmetoden ved planlegging forover eller bakover fra en dato.
-   Optimalisere bruken av ressurser ved å planlegge produksjoner på grunnlag av ressurskapasitet. Denne fremgangsmåten kan også fastslå når alternative ressurser skal brukes.
-   Optimalisere bruken av materialer ved å planlegge produksjoner på grunnlag av tilgjengeligheten av de nødvendige materialene.
-   Planlegge og synkronisere referanseproduksjoner. Datoene for referanseproduksjoner justeres når produksjonsordreplanen endres.

Du må estimere kostnaden til en produksjonsordre før du kan kjøre grovplanlegging. Hvis du ikke har kjørt et estimat, kjøres det automatisk før grovplanlegging startes. En grovplanlegging inneholder følgende informasjon:

-   Produktet som er planlagt for produksjon
-   Konfigurasjonen av produktet
-   Antallet som er involvert i produksjonen
-   Datoene når produksjonen starter og slutter
-   Kapasitetsreservasjoner for ressursene som utfører produksjonsaktivitetene

Oppstillingstiden, prosesstiden og kjøretiden angis for operasjoner i produksjonen. Når du har kjørt grovplanlegging, er statusen for produksjonsordren **Planlagt**, og alle operasjoner planlegges i rekkefølgen som er angitt av produksjonsruten. Det tas imidlertid bare hensyn til varigheten til operasjonen. Start- og sluttidspunkt planlegges ikke.

## <a name="scheduling-direction-and-date"></a>Planleggingsretning og dato
Planleggingsretningen er grunnleggende for planleggingsprosessen. Produksjon kan planlegges fremover eller bakover fra en hvilken som helst dato, avhengig av tidspunkt for behov og planlegging.

-   **Fremover fra planleggingsdatoen**– Du kan planlegge at produksjonen skal starte så tidlig som mulig. Produksjonen kan startes i dag, i morgen eller en hvilken som helst dato i fremtiden. Produksjonen planlegges fremover i tid til den tidligst mulige sluttdatoen.
-   **Bakover fra planleggingsdatoen**– Du kan planlegge at produksjonen skal starte så sent som mulig. Planlegging bakover er basert på datoen da produksjonen må være fullført. Tidsplanen teller bakover fra denne datoen til den seneste mulige datoen som produksjonen kan startes og fremdeles fullføres i tide.

## <a name="resource-scheduling"></a>Ressursplanlegging
Når du utfører grovplanlegging, planlegges hver operasjon i produksjonsruten for ressursen som er angitt for operasjonen. I tillegg angis varigheten av hver operasjon på produksjonsruten. Hvis en ressursgruppe er angitt for en operasjon, reserverer planleggingen kapasitet for gruppen. I motsetning til finplanlegging, velger ikke grovplanlegging de bestemte ressursene i gruppen. Hvis du arbeider med begrenset kapasitet, avhenger tidsplanen av tilgjengeligheten av ressursene som kreves for å fullføre produksjonen. Grovplanlegging følger operasjonssekvensen som er angitt for produksjonsruten. Planleggingen reserverer kapasitet i ressursgrupper, basert på operasjonstidene som er definert i produksjonsruten. Summen av tilgjengelig kapasitet for ressursene som er involvert, bestemmer kapasiteten for ressursgruppen. Kapasitetsreserveringer som allerede finnes for ressursene, regnes som utilgjengelig kapasitet. Hvis det ikke er nok tilgjengelig kapasitet for produksjonen, kan produksjonsordrer bli forsinket eller stoppet. Du kan også angi effektiviteten du forventer fra ressursene som er involvert i produksjonen. Du angir effektiviteten som en prosent på ressursen. Effektivitetsprosenten justerer produksjonen for ressursen. Denne justeringen påvirker tiden som er reservert for ressursen. Leveringstider for operasjoner som bruker ressursen, blir også justert i henhold til dette.

## <a name="operations-scheduling-and-master-planning"></a>Grovplanlegging og hovedplanlegging
Operasjonsplanen driver også hovedplanleggingen og fastsetter beregningen for materialbehov. Grovplanlegging tar hensyn til følgende informasjon:

-   **Restanseproduksjoner** - Produkter som er planlagt, frigitt eller startet
-   **Materialtilgjengelighet** - Lager, underordnet produksjon, underleverandører og leverandører
-   **Tilgjengelig kapasitet** – Ressurser som kreves for produksjon

> [!NOTE]
> Hvis du bruker flertrådet hovedplanlegging og grovplanlegging, tas det ikke hensyn til begrenset kapasitet. 

## <a name="cancellations"></a>Annulleringer
Når du kjører grovplanlegging, kan du avbryte bestemte deler av ruten. Disse delene inkluderer køtid, oppstillingstid, prosesstid, overlappingstid og transporttider.

## <a name="finite-materials"></a>Begrensede materialer
Hvis du arbeider med begrenset materiale, avhenger planlegging også av tilgjengeligheten av materialene som kreves for produksjonen. Hvis det ikke er nok tilgjengelige komponenter for produksjonen, kan produksjonen forsinkes. Du kan basere planleggingen på bruk av materialer ved å angi materialene som må være tilgjengelige for produksjon. Når du optimaliserer både ressurskapasitet og tilgjengeligheten av materialer, beregnes produksjonen i henhold til disse begrensningene. En produksjonsordre kan ikke planlegges å starte før kapasitet og materialer er tilgjengelige samtidig og i nødvendige mengder.

<a name="additional-resources"></a>Tilleggsressurser
--------

[Alternativer for grovplanlegging](operation-scheduling-options.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]