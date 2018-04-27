---
title: "Salg og markedsføring"
description: "Du kan bruke salg og markedsføring til å hente, lagre og bruke ulike typer data i salgsflyten. Disse dataene inkluderer det innledende salgsordreinitiativet, fremtidig oppfølgningshandling og påfølgende salg."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 92303
ms.assetid: 65ca9992-bbfa-4224-bf0e-067a25c7e6a4
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: da48a9eef118a7a369343c986e4b67f53266f7e1
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="sales-and-marketing"></a>Salg og markedsføring

[!INCLUDE [banner](../includes/banner.md)]

Du kan bruke salg og markedsføring til å hente, lagre og bruke ulike typer data i salgsflyten. Disse dataene inkluderer det innledende salgsordreinitiativet, fremtidig oppfølgningshandling og påfølgende salg.

<a name="marketing"></a>Markedsføring
---------

Du bruker markedsføringskampanjer og aktiviteter for å finne og bygge relasjoner med potensielle kunder, slik at de første samhandlingene kan utvikles til salgsrelasjoner. Denne arbeidsflyten viser forretningsprosessen for markedsføring. [![Forretningsprosess for markedsføring](./media/marketing01.jpg)](./media/marketing01.jpg)

### <a name="relationships"></a>Relasjoner

I salg og markedsføring kan de første samhandlingene du har med potensielle kunder, oppstå i ulike situasjoner. Du finner for eksempel en potensiell kunde mens du deltar på en varemesse, eller du kan ha et mulig kundeemne med en kunde etter at organisasjonen har kjørt en masseutsendelseskampanje. Det er svært viktig at du forstår flyten for enheten for en part før denne parten blir en kunde. Grafikken nedenfor viser flyten for enhetsrelasjoner når en potensiell kunde blir en faktisk kunde. [![Salg og markedsføring 01](./media/salesandmarketing01.jpg)](./media/salesandmarketing01.jpg)

### <a name="campaigns"></a>Kampanjer

En kampanje er målrettet mot kontakter for prospekter, kundeemner, salgsmuligheter og kunder som er valgt til å delta i kampanjen. I i Microsoft Dynamics 365 for Finance and Operations kan du kan opprette flere typer kampanjer, for eksempel telemarketing, post- og e-post-kampanjer, for maksimere kundepotensialet. Etter hvert som kampanjen går fremover og du får positive svar, kan du starte salgsprosessen med disse mottakerne som har respondert positivt på kampanjen.

## <a name="sales"></a>Salg
Du kan bruke salgsfunksjonaliteten til å opprette tilbud, mersalg og kryssalg til nye og eksisterende kunder, opprette salgsordrer og opprette salgsfakturaer for kunder. Denne arbeidsflyten viser forretningsprosessen for salg. [![Forretningsprosess for salg](./media/sales01.jpg)](./media/sales01.jpg)

### <a name="sales-quotations"></a>Salgstilbud

Du kan opprette salgstilbud for å presentere et tilbud av varer eller tjenester som du vil gi til kunder. En kunde kan be om et tilbud, eller du kan opprette et tilbud som svar på en forespørsel fra en potensiell eller eksisterende kunde. Når kunden godkjenner salgstilbudet, kan du konvertere det til en salgsordre.

### <a name="up-sellcross-sell"></a>Mersalg/kryssalg

Mersalg og kryssalg er teknikker for å selge produkter når en ordre registreres for en kunde. Ved mersalg blir det foreslått et annet produkt i stedet gjeldende produkt. Ved kryssalg blir det foreslått et produkt i tillegg gjeldende produkt. Når du setter opp produktlister, kan du opprette spesifikke regler for å angi når et produkt skal foreslås som et kryssalgs- eller mersalgsprodukt.

### <a name="sales-orders"></a>Salgsordrer

Når du oppretter en ny salgsordre, må du velge hvilken type salgsordre som skal opprettes. Du har fem alternativer. **Obs!** Når du har opprettet en salgsordre, kan en hvilken som helst ordretype, bortsett fra typen **Varekrav** hvis salgsordren har statusen **Levert**.

| Salgsordretype  | Beskrivelse                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Journal           | Bruk denne typen som et utkast for en salgsordre. Denne typen har ingen innvirkning på lagerantall, og genererer ikke varetransaksjoner.                                                                                                                                                                    |
| Abonnement      | Bruk denne typen for regelmessige ordrer. Når ordren faktureres, angis ordrestatusen automatisk til en åpen ordre. Det leverte antallet som ble fakturert, og den gjenstående leveringen oppdateres. Du kan ikke bruke denne salgsordretypen hvis du bruker funksjonen Lagerstyring. |
| Salgsordre       | Bruk denne typen når en kunde har lagt inn eller bekreftet en ordre.                                                                                                                                                                                                                                        |
| Returordre    | Bruk denne typen når en kunde returnerer en vare. Et returvarenummer (autorisasjonsreturnummer) tildeles automatisk.                                                                                                                                                                                            |
| Varebehov | Denne typen opprettes automatisk når du foretar et varesalg gjennom et prosjekt.                                                                                                                                                                                                                       |

### <a name="sales-agreements"></a>Salgsavtaler

En salgsavtale er en kontrakt som forplikter kunden for å kjøpe et produkt i et bestemt antall eller for et bestemt beløp over tid, i bytte mot spesielle priser og rabatter. Prisene og rabattene i salgsavtalen overstyrer priser og rabatter som er angitt i en forretningsavtale. En salgsavtale er gyldig i en definert periode. Den ønskede forsendelsesdatoen som er angitt for et salg på siden **Salgsordre**, skal være innenfor den gyldige perioden. En salgsavtale er som standard på vent. Du kan bare bestille fra en salgsavtale når den er satt til **Gyldig**.

### <a name="backorders"></a>Restordrer

Når du registrerer og validerer ordrer, kan det hende du må administrere restordrer og unntak før salget kan fullføres. Restordrer er enten bestillinger som ennå ikke er levert fra en leverandør eller salgsordrer som ennå ikke er levert til en kunde. Det er viktig at du følger opp restordrer. Hvis produkter for eksempel er forsinket fra en leverandør, må du kanskje endre datoen for levering til en kunde, og deretter informere kunden om forsinkelsen. Du kan vise restordrer etter vare, kunde eller leverandør.

#### <a name="viewing-backorders-by-item"></a>Vise restordrer etter vare

Når du viser restordrer etter vare, kan du følge opp den forventede fremtidige flyten av transaksjoner for en bestemt vare. Du kan for eksempel kontrollere følgende informasjon:

-   Antall salgsordrer som er lagt inn for en vare
-   Om leveringer av varen fra leverandører fremdeles mangler
-   Om flere varer må bestilles, slik at du kan levere alle salgsordrene i tide

Ved å utføre denne kontrollen, kan du svare på forespørsler fra kunder om tidspunktet for levering av varen. Du kan også prioritere restordrer for salg, og eventuelt dele varene på lager mellom ordrene.

#### <a name="viewing-backorders-by-customer"></a>Vise restordrer etter kunde

Når du viser restordre etter kunde, kan du vise statusen til kundens gjenstående ordrer. Dette alternativet er nyttig når du må forholde seg til kunder som venter på varer som har blitt forsinket.

#### <a name="viewing-backorders-by-vendor"></a>Vise restordrer etter leverandør

Når du viser restordrer etter leverandør, kan du følge opp manglende leveringer og visning av forventede leveringsdatoer. Denne kontrollen lar deg prioritere restordrene når produkter ankommer fra leverandører og salgsordrene må plukkes for levering.

### <a name="invoices"></a>Fakturaer

Du kan opprette tre typer fakturaer under salgsprosessen:

-   Kundefaktura
-   Fritekstfaktura
-   Proformafaktura

#### <a name="customer-invoice"></a>Kundefaktura

En kundefaktura er en regning som en organisasjon gir til en kunde i forbindelse med et salg. Du oppretter denne typen kundefaktura basert på en salgsordre som inkluderer et hode og én eller flere linjer for varer eller tjenester. Kundefakturaen fullfører syklusen med salgsordren, følgeseddelen og salgsfakturaen.  

Du kan postere og skrive ut én enkelt kundefaktura basert på en salgsordre eller følgeseddel og dato. Du kan også postere og skrive ut flere kundefakturaer samtidig basert på følgesedler og datoer. Når du posterer én enkelt kundefaktura ved hjelp av salgsordren, oppdateres **Fakturarest**-antallet for hver vare med totalantallet som er fakturert fra den valgte salgsordren.  

Hvis **Fakturarest**-antallet og **Gjenstående levering**-antallet for alle varer på salgsorden er 0 (null), endres statusen for salgsorden til **Fakturert**. Hvis antallet et av feltene ikke er null, endres ikke statusen for salgsordren, og du kan registrere flere fakturaer. Hvis du vil bokføre og skrive ut én eller flere kundefakturaer basert på følgesedlene, må du allerede har bokført minst én følgeseddel for hver salgsordre. Kundefakturaen er basert på følgesedlene og gjenspeiler antallet som vises i dem.  

Du kan opprette en kundefaktura som er basert på følgeseddellinjevarene som er levert til nå, selv om ikke alle varene i en bestemt salgsordre er levert ennå. Du kan for eksempel gjøre dette hvis den juridiske enheten din sender ut én faktura per kunde per måned for å dekke alle forsendelser du sender i løpet av den måneden. Hver følgeseddel representerer en delvis eller komplett forsendelse av varene i salgsordren.  

Når du posterer fakturaen, oppdateres **Fakturarest**-antallet for hver vare med totalantallet som er levert for de valgte følgesedlene. Hvis **Fakturarest**-antallet og **Gjenstående levering**-antallet for alle varer på salgsorden er 0 (null), endres statusen for salgsorden til **Fakturert**. Hvis antallet ikke er null, endres ikke statusen for salgsordren, og du kan registrere flere fakturaer. Lagertransaksjoner oppdateres med fakturanummeret, og statusen på salgsordrelinjen endres til **Fakturert**.

#### <a name="free-text-invoice"></a>Fritekstfaktura

En fritekstfaktura er en faktura som ikke er knyttet til en salgsordre. Den inneholder ordrelinjer som omfatter finanskontoer, fritekstbeskrivelser og et salgsbeløp. Du kan ikke angi et varenummer i denne fakturatypen, og du må skrive inn riktige mva-opplysninger. En hovedkonto for salg er angitt på hver fakturalinje. Kundesaldoen posteres til samlekontoen fra posteringsprofilen som brukes for fritekstfakturaen.

#### <a name="pro-forma-invoice"></a>Proformafaktura

En proformafaktura er en faktura som er klargjort som et estimat av det faktiske fakturabeløpet før fakturaen posteres. Du kan skrive ut en proformafaktura for enten en kundefaktura eller en fritekstfaktura.




