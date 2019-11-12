---
title: Fordele feedbasert ordreoppretting for detaljhandelstransaksjoner
description: Dette emnet beskriver den fordelte, feedbaserte ordreopprettingen for detaljhandelstransaksjoner i Microsoft Dynamics 365 Retail.
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
ms.openlocfilehash: 80233a73dbffc7380503cf03703758b187824c2a
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622672"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a>Fordele feedbasert ordreoppretting for detaljhandelstransaksjoner (offentlig forhåndsvisning)

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

I Dynamics 365 Retail versjon 10.0.4 og tidligere er postering av detaljhandelsutdrag en operasjon på slutten av dagen, og alle transaksjoner posteres i bøkene på slutten av dagen. Store transaksjoner må deretter behandles i et begrenset tidsvindu, noe som noen ganger kan føre til belastning og låsing og feil i utdragsposteringen. Forhandlere kan heller ikke føre inntekter og betalinger i sine bøker gjennom hele dagen.

Med offentlig forhåndsvisning av fordeling av feedbasert ordreoppretting, som ble innført i Retail versjon 10.0.5, behandles transaksjoner gjennom hele dagen, og bare finansavstemmingen for betalingsmidler og andre kassastyringstransaksjoner behandles på slutten av dagen. Denne funksjonen deler belastningen med å opprette salgsordrer, fakturaer og betalinger gjennom hele dagen, noe som gir bedre ytelse og muligheten til å føre inntekter og betalinger i de andre bøkene i nærheten av sanntid. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Bruke fordeling av feedbasert postering
  
1. Hvis du vil aktivere fordeling av feedbasert postering for detaljhandelstransaksjoner, går du til **Systemadministrasjon > Oppsett > Lisenskonfigurasjon** og deaktiverer nøkkelen **Detaljhandelsutdrag**.

2. På samme side aktiverer du lisensnøkkelen **Detaljhandelsutdrag (fordelingsfeed) – forhåndsvisning**. Når du aktiverer denne nøkkelen, må du kontrollere at det ikke finnes ventende utdrag som venter på å bli postert. 

> [!Important]
> Før du aktiverer lisensnøkkelen **Detaljhandelsutdrag (fordelingsfeed) – forhåndsvisning**, må du kontrollere at ingen ventende utdrag venter på å bli postert.

3. Gjeldende utdragsdokument blir delt inn i to forskjellige typer: transaksjonsutdrag og regnskapsoppgjør.

      - Transaksjonsoppgaven vil plukke opp alle uposterte og godkjente detaljhandelstransaksjoner, og opprette salgsordrer, salgsfakturaer, betalings- og rabattjournaler og transaksjoner for inntekter/utgifter med det intervallet du konfigurerer. Du bør konfigurere denne prosessen til å kjøre med høy frekvens, slik at dokumenter opprettes når detaljhandelstransaksjonene lastes opp til Retail Headquarters via P-jobben. Med transaksjonsutdraget som allerede oppretter salgsordrer og salgsfakturaer, er det ikke noe reelt behov for å konfigurere den satsvise jobben **Poster lager**. Du kan imidlertid fortsatt bruke den til å oppfylle bestemte forretningskrav som du kanskje har.  
      
     - Regnskapsoppgjøret er utformet til å opprettes på slutten av dagen, og støtter bare avsluttingsmetoden **Skift**. Dette utdraget vil være begrenset til økonomisk avstemming, og vil bare opprette journaler for de ulike beholdningsbeløpene mellom telt beløp og transaksjonsbeløp for de forskjellige anleggsmidlene, sammen med journaler for andre kontantstyringstransaksjoner.   

4. Hvis du vil beregne transaksjonsutdraget, klikker du **Detaljhandel > IT for detaljhandel > Salgsstedspostering > Beregn transaksjonsutdrag satsvis**. Hvis du vil postere transaksjonsutdrag satsvis, klikker du **Detaljhandel > IT for detaljhandel > Salgsstedspostering > Poster transaksjonsutdrag satsvis**.

5. Hvis du vil beregne regnskapsoppgjøret, klikker du **Detaljhandel > IT for detaljhandel > Salgsstedspostering > Beregn regnskapsoppgjør satsvis**. Hvis du vil postere regnskapsoppgjør satsvis, klikker du **Detaljhandel > IT for detaljhandel > Salgsstedspostering > Poster regnskapsoppgjør satsvis**.

> [!NOTE]
> Menyelementene **Detaljhandel > IT for detaljhandel > Salgsstedspostering > Beregn utdrag satsvis** og **Detaljhandel > IT for detaljhandel > Salgsstedspostering > Poster utdrag satsvis** blir fjernet med denne nye funksjonen.

Du kan også opprette typer transaksjons- og regnskapsoppgjør manuelt. Gå til **Detaljhandel > Kanaler > Detaljhandelsbutikker** og klikk **Detaljhandelsutdrag**. Klikk **Ny**, og velg deretter typen utdrag du vil opprette. Felt på siden **Detaljhandelsutdrag** og handlinger under **Utdragsgruppe** på siden viser relevante data og handlinger basert på den valgte utdragstypen.
