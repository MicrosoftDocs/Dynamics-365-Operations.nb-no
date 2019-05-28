---
title: Opprette en innkjøpsreturordre
description: Denne fremgangsmåten viser hvordan du oppretter en innkjøpsreturordre ved hjelp av Kreditnota-handlingen, for å kopiere linjer fra et leverandørfakturadokument til en ny bestilling.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchCopying, InventMarking, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e080252006d889e2f27db2bccb7b541f3ee4cf9e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547497"
---
# <a name="create-a-purchase-return-order"></a>Opprette en innkjøpsreturordre

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en innkjøpsreturordre ved hjelp av Kreditnota-handlingen, for å kopiere linjer fra et leverandørfakturadokument til en ny bestilling. Den viser også hvordan du bekrefter ordren og behandler leveringen av varene tilbake til leverandøren. Eksemplet som vises i denne fremgangsmåten, kan brukes i demonstrasjonsdatafirmaet USMF. Denne oppgaven utføres vanligvis av en innkjøpsagent.


## <a name="create-a-new-purchase-return-order"></a>Opprette en ny innkjøpsreturordre
1. Gå til Innkjøp og leverandører > Bestillinger > Alle bestillinger.
    * Det første trinnet er å opprette en ny bestilling som skal brukes som en bestillingsretur.  
2. Klikk Ny.
3. Angi US-102 i Leverandørkonto-feltet.
4. Klikk OK.
5. Klikk Kjøp i handlingsruten.
6. Klikk Kreditnota.
    * Dette er siden der du kan kopiere fra eksisterende leverandørfaktura til returordren. Dette er den samme siden som brukes for andre kopieringshandlinger. Siden vi har åpnet den fra Kreditnota-handlingen, er imidlertid siden konfigurert til å støtte oppretting av en returordre som utligner leverandørfakturaer.  
7. Utvid seksjonen Parametere.
    * Alternativet Snu fortegn velges automatisk og kan ikke endres. Dette sikrer at fortegnet endres for antallene, og at ordrelinjer som er lagt til, utlignes mot leverandørfakturaen.  
    * Alternativet Kopier gebyrer velges automatisk og kan ikke endres. Dette betyr at gebyrer fra leverandørfakturaen legges til innkjøpsreturordren for utligning mot det opprinnelige gebyret. Det er mulig å endre gebyrene i ordrehodet og -linjene senere.  
    * Alternativet Kopier presist velges automatisk og kan ikke endres. Dette sikrer at det opprettes en nøyaktig kopi av verdiene i alle feltene i leverandørfakturahodet og -linjene. Dette betyr at det opprettes en innkjøpsreturordre med verdiene som oppfyller alle vilkårene som brukes med leverandørfakturadokumentet.  
    * Alternativet Slett innkjøpslinjer sletter alle bestillingslinjene som allerede finnes på bestillingen, før du legger til de nye linjene. I dette eksemplet har vi ennå ikke har lagt til linjer i innkjøpsreturordren, slik at det ikke vil ha noen innvirkning. Vær forsiktig når du bruker dette alternativet, siden dette sletter alle eksisterende linjer uten advarsel.  
    * Alternativet Kopier ordrehode velges automatisk og kan ikke endres. Dette sikrer at informasjon kopieres fra leverandørfakturaen og brukes i hodet på innkjøpsreturordren. Dette er nyttig fordi det bidrar til å sikre at innkjøpsreturordren utligner fakturaen ved å bruke samme vilkår.  
8. Skjul Parametere-delen.
9. Vis Fakturaer-delen.
    * Siden er åpnet fra Kreditnota-handlingen, så det eneste tilgjengelige alternativet er å kopiere informasjon fra leverandørfakturaer. Denne kategorien viser alle tilgjengelige fakturaer for leverandørkontoen som er angitt på innkjøpsreturordren som du opprettet tidligere.   Fakturaene identifiseres av fakturabilaget eller bestillings-ID-ene.  
10. Finn leverandørfakturaen identifisert av fakturanummer AP-0006, og uthev linjen ved å klikke et felt på linjen.
11. Velg linjen ved å klikke i avmerkingsboksen for linjen. 
    * Legg merke til at linjene som er tilgjengelige i leverandørfakturaen, velges automatisk sammen med ordren. Denne bestemte leverandørfakturaen har to ordrelinjer. I dette eksemplet returnerer vi deler av antallet fra den andre linjen.  
12. Merk den andre linjen (den med varen M0006) ved å klikke et felt på linjen.
13. I Antall-feltet endrer du antallet til 10. Dette er antallet som returneres til leverandøren. 
14. Merk den første linjen (den med varen M0005) ved å klikke et felt på linjen.
15. Fjern merket for linjen.
    * Bare linjene som du har valgt, kopieres til bestillingen.  
16. Skjul Fakturaer-delen.
17. Vis delen Valgte linjer eller topptekst som skal kopieres.
    * Denne visningen viser et sammendrag av alle dokumenter og linjer som du har valgt å kopiere til bestillingen.  
18. Skjul delen Valgte linjer eller topptekst som skal kopieres.
19. Klikk OK.
    * Linjen som du valgte, er nå kopiert til din innkjøpsreturordre. Antall-feltet viser -10.   
20. Klikk Lager.
21. Klikk Merking.
    * Ordrelinjen som ble opprettet, merkes mot lagertransaksjonen fra leverandørfakturaen. Dette sikrer at beholdningen som returneres til leverandøren, er lik beholdningen som ble mottatt fra dem tidligere. Det finnes situasjoner der merking ikke utføres, for eksempel hvis beholdningen allerede er merket som Forbrukt, eller hvis produktet er et som ikke bruker merking.  
22. Klikk OK.

## <a name="confirm-and-record-the-shipment-of-goods"></a>Bekrefte og registrere levering av varer
1. Klikk Bekreft.
2. Klikk Motta i handlingsruten.
3. Klikk Produktkvittering.
    * Denne siden brukes til å registrere produktkvittering for bestillinger og også behandle arbeid retur av varer til leverandøren. Ordrelinjer med et negativt antall betyr at varer skal returneres til leverandøren, og dokumentet som kan genereres fra denne siden, kan brukes som følgeseddel for denne bruken.   
    * I Antall-feltet velger du Bestilt antall i dette eksemplet.   Dette sikrer at forsendelsen behandles for hele det bestilte antallet som ordrelinjene ble opprettet med.   
4. Skriv inn en verdi i feltet Produktkvittering.
    * Dette feltet brukes til å angi en referanse som skal brukes som bilag for produktkvitteringsjournalen.  
5. Klikk OK.
    * Varene er nå registrert som mottatt som sendt i innkjøpsreturordren, og en produktkvitteringsjournal er opprettet. Du kan bruke handlingen Produktmottak for å vise journaler som er opprettet med bestillingen, og se hva som er mottatt eller returnert, og når.  

