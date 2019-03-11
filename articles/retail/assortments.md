---
title: Sortimentstyring
description: Dette emnet beskriver de grunnleggende begrepene for sortimentstyring i Microsoft Dynamics 365 for Retail, og gir informasjon om implementering av prosjekt.
author: jblucher
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: jeffbl
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Application update 5
ms.openlocfilehash: b4de2a97a19be6d4e52c43180e36baf7adf6a649
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "365046"
---
# <a name="assortment-management"></a>Sortimentstyring

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Oversikt

Microsoft Dynamics 365 for Retail gir *sortimenter* som lar deg administrere produkttilgjengelighet på tvers av kanaler. Sortimenter bestemmer hvilke varer som er tilgjengelige i bestemte butikker og i en bestemt periode.

I Retail er et sortiment en forskjellig en tilordning av én eller flere kanaler (eller grupper av kanaler, når du bruker organisasjonshierarkier) til én eller flere produkter (eller produktgrupper, når du bruker kategorihierarkier).

Den generelle produktsammensetningen av en kanal bestemmes av de publiserte sortimentene som er tilordnet til kanalen. Derfor kan du konfigurere flere aktive sortimenter per kanal.

### <a name="basic-assortment-setup"></a>Grunnleggende oppsett av sortimenter

I eksemplet nedenfor er en unik sortiment konfigurert for hver butikk. I dette tilfellet er bare produkt 1 tilgjengelig i butikk 1, og bare produkt 2 er tilgjengelig i butikk 2.

![Hvert produkt er tilgjengelig i én butikk](./media/Managing-assortments-figure1.png)

Hvis du vil gjøre produkt 2 tilgjengelig i butikk 1, kan du legge produktet til sortiment 1.

![Produkt 2 lagt til i sortiment 1](./media/Managing-assortments-figure2.png)

Du kan også legge butikk 1 til sortiment 2.

![Butikk 1 lagt til i sortiment 2](./media/Managing-assortments-figure3.png)

### <a name="organization-hierarchies"></a>Organisasjonshierarkier

I tilfeller der flere kanaler deler samme produktsortimentene, kan du konfigurere sortimentene ved hjelp av organisasjonshierarkiet for sortimenter i Retail. Når noder fra dette hierarkiet legges til, er alle kanaler i denne noden og de underordnede nodene inkludert.

![Organisasjonshierarki](./media/Managing-assortments-figure4.png)

### <a name="product-categories"></a>Produktkategorier

På samme måte kan du på produkt-siden inkludere produktgrupper ved hjelp av kategorihierarkier for produkter. Du kan konfigurere sortimenter ved å inkludere én eller flere kategorihierarkinoder. I så fall omfatter sortimentet alle produkter i kategorinoden og de underordnede nodene.

![Produktkategorier](./media/Managing-assortments-figure5.png)

### <a name="excluded-products-or-categories"></a>Ekskluderte produkter eller kategorier

I tillegg til å inkludere produkter og kategorier i sortimenter, kan du bruke alternativet Ekskluder til å definere bestemte produkter eller kategorier som skal ekskluderes fra sortimenter. I eksemplet nedenfor vil du ta med alle produkter i en bestemt kategori, med unntak av produkt 2. I så fall trenger du ikke definerer sortimentet produkt etter produkt eller opprette flere kategorinoder. Du kan derimot bare inkluderer kategorien, men utelate produktet.

> [!NOTE]
> Hvis et produkt per definisjon er både inkludert og ekskludert i én eller flere sortimenter, skal produktet alltid regnes som ekskludert.

![Ekskludert produkt](./media/Managing-assortments-figure6.png)

### <a name="global-and-released-products"></a>Globale og frigitte produkter

Sortimenter defineres på et globalt nivå og kan inneholde kanaler fra flere juridiske enheter. Produkter og kategorier som er inkludert i sortimenter er også delt på tvers av juridiske enheter. Et produkt må imidlertid frigis før det faktisk kan selges, bestilles, telles eller mottas i kanalen (for eksempel i utsalgsstedet \[POS\]). Selv om to butikker i ulike juridiske enheter kan dele et sortiment som inneholder de samme produktene, er produktene bare tilgjengelige hvis de er frigitt til de juridiske enhetene.

### <a name="dynamic-and-static-assortments"></a>Dynamiske og statiske sortimenter

Du kan definere sortimenter med bestemte kanaler og produkter eller ved å inkludere organisasjonsenheter og kategorier. Sortimenter, inkludert referanser til disse gruppene, anses som dynamiske sortimenter. Hvis definisjonen til eller innholdet i disse gruppene endres mens sortimentet er aktivt, endres også definisjonen av sortimentet.

Et utvalg er for eksempel opprinnelig definert og publisert slik at den refererer til en kategori av produkter. Hvis flere produkter blir lagt til kategorien senere, inkluderes disse produktene automatisk i definisjonen av det eksisterende sortimentet. Du trenger ikke å legge til produktene til sortimentet manuelt. På samme måte, hvis en organisasjonsenhet er lagt til en annen node, justeres organisasjonsenhetens sortimentet automatisk basert på definisjonen.

### <a name="stopped-products"></a>Produkter som er stoppet

Du kan "stoppe" frigitte produkter for salgsprosessen ved å aktivere en innstilling i innstillingen **Standard ordre**. Denne innstillingen brukes oftest når et produkt er på slutten av levetiden og ikke skal selges i en kanal. Sortimenter godtar denne innstillingen, og produkter som er stoppet vil ikke bli sortert, uansett hvilken sortimentets konfigurasjon.

### <a name="blocked-products"></a>Sperrede produkter

I tillegg til å stoppe salg av et produkt, kan du midlertidig blokkere salg av et produkt. Du kan konfigurere denne innstillingen på kategorien **Retail** til et frigitt produkt. Sperrede produkter blir fremdeles sortert, men du får en melding i POS som sier at produktet ikke kan selges.

### <a name="date-effectivity"></a>Datoeffektivitet

Sortimenter er datoeffektive. Forhandlere kan derfor konfigurere når produkter skal eller ikke skal være tilgjengelig per kanal. Du kan definere og publisere sortimenter på forhånd, og angi start- og sluttdatoer. Produktene blir automatisk tilgjengelige eller ikke tilgjengelige på de angitte datoene.

### <a name="process-assortments-batch-job"></a>Behandle den satsvise jobben for sortimenter.

Sortimenter som er definert i Retail må behandles før de trer i kraft. Behandlingen gjøres av følgende årsaker:

- Sortimentdefinisjoner må være de-normalisert slik at kanaler enklere kan bruke dem. Et produktutvalg for en kanal kan defineres gjennom flere sortimenter som strekker seg over flere datointervaller. Når deler av informasjonen blir beregnet på forhånd på serveren, forbedres kanalens ytelse.
- Produkter og kanaler i sortimentet kan endre utenfor selve sortimentet. Dynamiske sortimenter som inneholder referanser til kategorier eller organisasjonsenheter må behandles med jevne mellomrom, slik at de inkluderer eller ekskluderer poster, basert på deres gjeldende tildeling.

## <a name="implementation-considerations"></a>Informasjon om implementering

Vurder følgende implementeringskrav når du planlegger og behandler sortimenter for detaljhandelimplementering:

- **Datareplikering og størrelsen på databasen** – selv om sortimenter hjelper forretningen med å administrere produkttilgjengelighet, er de også et viktig verktøy for administrasjon av størrelsen på kanaler og frakoblede databaser. Ordentlig administrerte sortimenter reduserer mengden data som må behandles og replikeres til kanaler og frakoblede databaser. De hjelper også med å redusere antall poster som må beholdes. Færre poster i databasene øker ytelsen når du legger varer til en transaksjon, et søk eller når du søker etter produkter.
- **Datoeffektive/utløpende sortimenter** – blant de mest effektive verktøyene for administrasjon av antall produkter i kanalen og frakoblede databaser er datoeffektiviteten i sortimenter. Hvis du beholder åpne (ikke utløpende) sortimenter for sesongbetonte produkter eller produkter som er på slutten av levetiden, vil databasene vokse på ubestemt tid. Du kan bruke forskjellige metoder for å administrere denne situasjonen. Du kan for eksempel vedlikeholde separate sortimenter for sesongbetonte produkter og produkter som alltid er tilgjengelige.
- **Salg og returer utenfor sortimenter** – denne funksjonen hjelper forhandlerne å administrere sortimenter effektiv, ved at de kan begrense antall tilgjengelige produkter til produkter som hører til kjerneutvalget for butikken. Denne funksjonen bidrar også til å håndtere tilfeller der et produkt ved en feiltakelse ble utelatt fra et utvalg, eller der et produkt ble returnert utenfor de effektive datoene for sortimentet.

Hvis produktdataen ikke eksisterer i kanalens database, foretar POS et sanntidsanrop til hovedkontoret for å hente den nødvendige informasjonen, slik at produktet kan solges, returneres eller legges til en kundeordre. Produktinformasjon som hentes på denne måten er bare tilgjengelig i løpet av transaksjonen. Produktet blir ikke lagt til sortimentdefinisjonen. Derfor foretas sanntidsanrop etter behov.
