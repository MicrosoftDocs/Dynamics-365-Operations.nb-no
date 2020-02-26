---
title: Fordele feedbasert ordreoppretting for detaljhandelstransaksjoner
description: Dette emnet beskriver den fordelte, feedbaserte ordreopprettingen for detaljhandelstransaksjoner i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3f691017ad06d3416e4ba0e86d7a0bc207aba5bd
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004280"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a>Fordele feedbasert ordreoppretting for detaljhandelstransaksjoner (offentlig forhåndsvisning)

[!include [banner](includes/banner.md)]



I Dynamics 365 Retail versjon 10.0.4 og tidligere er postering av utdrag en operasjon på slutten av dagen, og alle transaksjoner posteres i bøkene på slutten av dagen. Store transaksjoner må deretter behandles i et begrenset tidsvindu, noe som noen ganger kan føre til belastning og låsing og feil i utdragsposteringen. Forhandlere kan heller ikke føre inntekter og betalinger i sine bøker gjennom hele dagen.

Med offentlig forhåndsvisning av fordeling av feedbasert ordreoppretting, som ble innført i Retail versjon 10.0.5, behandles transaksjoner gjennom hele dagen, og bare finansavstemmingen for betalingsmidler og andre kassastyringstransaksjoner behandles på slutten av dagen. Denne funksjonen deler belastningen med å opprette salgsordrer, fakturaer og betalinger gjennom hele dagen, noe som gir bedre ytelse og muligheten til å føre inntekter og betalinger i de andre bøkene i nærheten av sanntid. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Bruke fordeling av feedbasert postering
  
1. Hvis du vil aktivere fordeling av feedbasert postering for transaksjoner, går du til **Systemadministrasjon > Oppsett > Lisenskonfigurasjon** og deaktiverer nøkkelen **Utdrag**.

2. På samme side aktiverer du lisensnøkkelen **Utdrag (fordelingsfeed) – forhåndsvisning**. Når du aktiverer denne nøkkelen, må du kontrollere at det ikke finnes ventende utdrag som venter på å bli postert. 

    > [!Important]
    > Før du aktiverer lisensnøkkelen **Utdrag (fordelingsfeed) – forhåndsvisning**, må du kontrollere at ingen ventende utdrag venter på å bli postert.

3. Gjeldende utdragsdokument blir delt inn i to forskjellige typer: transaksjonsutdrag og regnskapsoppgjør.

      - Transaksjonsoppgaven vil plukke opp alle uposterte og godkjente transaksjoner, og opprette salgsordrer, salgsfakturaer, betalings- og rabattjournaler og transaksjoner for inntekter/utgifter med det intervallet du konfigurerer. Du bør konfigurere denne prosessen til å kjøre med høy frekvens, slik at dokumenter opprettes når transaksjonene lastes opp til Headquarters via P-jobben. Med transaksjonsutdraget som allerede oppretter salgsordrer og salgsfakturaer, er det ikke noe reelt behov for å konfigurere den satsvise jobben **Poster lager**. Du kan imidlertid fortsatt bruke den til å oppfylle bestemte forretningskrav som du kanskje har.  
      
     - Regnskapsoppgjøret er utformet til å opprettes på slutten av dagen, og støtter bare avsluttingsmetoden **Skift**. Dette utdraget vil være begrenset til økonomisk avstemming, og vil bare opprette journaler for de ulike beholdningsbeløpene mellom telt beløp og transaksjonsbeløp for de forskjellige anleggsmidlene, sammen med journaler for andre kontantstyringstransaksjoner.   

4. Hvis du vil beregne transaksjonsutdraget, klikker du **Detaljhandel og handel > IT for Detaljhandel og handel > Salgsstedspostering > Beregn transaksjonsutdrag satsvis**. Hvis du vil postere transaksjonsutdrag satsvis, klikker du **Detaljhandel og handel > IT for Detaljhandel og handel > Salgsstedspostering > Poster transaksjonsutdrag satsvis**.

5. Hvis du vil beregne regnskapsoppgjøret, klikker du **Detaljhandel og handel > IT for Detaljhandel og handel > Salgsstedspostering > Beregn regnskapsoppgjør satsvis**. Hvis du vil postere regnskapsoppgjøret satsvis, klikker du **Detaljhandel og handel > IT for Detaljhandel og handel > Salgsstedspostering > Poster regnskapsoppgjør satsvis**.

> [!NOTE]
> Menyelementene **Detaljhandel og handel > IT for Detaljhandel og handel > Salgsstedspostering > Beregn utdrag satsvis** og **Detaljhandel og handel > IT for Detaljhandel og handel > Salgsstedspostering > Poster utdrag satsvis** blir fjernet med denne nye funksjonen.

Du kan også opprette typer transaksjons- og regnskapsoppgjør manuelt. Gå til **Detaljhandel og handel > Kanaler > Butikker** og klikk **Utdrag**. Klikk **Ny**, og velg deretter typen utdrag du vil opprette. Felt på siden **Utdrag** og handlinger under **Utdragsgruppe** på siden viser relevante data og handlinger basert på den valgte utdragstypen.
