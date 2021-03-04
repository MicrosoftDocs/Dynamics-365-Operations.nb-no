---
title: Fordele feedbasert ordreoppretting for detaljhandelstransaksjoner
description: Dette emnet beskriver den fordelte, feedbaserte ordreopprettingen for butikktransaksjoner i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1f864fd6e3aa62cabd039922ed55ad5f7714f0ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991362"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Fordele feedbasert ordreoppretting for detaljhandelstransaksjoner

[!include [banner](includes/banner.md)]

I Dynamics 365 Retail versjon 10.0.4 og tidligere er postering av utdrag en operasjon på slutten av dagen, og alle transaksjoner posteres i bøkene på slutten av dagen. Store transaksjoner må deretter behandles i et begrenset tidsvindu, noe som noen ganger kan føre til belastning og låsing og feil i utdragsposteringen. Forhandlere kan heller ikke føre inntekter og betalinger i sine bøker gjennom hele dagen.

Med fordeling av feedbasert ordreoppretting, som ble innført i Retail versjon 10.0.5, behandles transaksjoner gjennom hele dagen, og bare finansavstemmingen for betalingsmidler og andre kassastyringstransaksjoner behandles på slutten av dagen. Denne funksjonen deler belastningen med å opprette salgsordrer, fakturaer og betalinger gjennom hele dagen, noe som gir bedre ytelse og muligheten til å føre inntekter og betalinger i de andre bøkene i nærheten av sanntid. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Bruke fordeling av feedbasert postering
  
1. Hvis du vil aktivere fordelingsfeedbasert postering av detaljhandelstransaksjoner, aktiverer du funksjonen **Detaljhandelsoppgaver – fordelingsfeed** ved hjelp av Funksjonsbehandling.

    > [!IMPORTANT]
    > Før du aktiverer funksjonen må du sørge for at ingen utdrag venter på å bli postert.

2. Gjeldende utdragsdokument blir delt inn i to typer: transaksjonsutdrag og regnskapsoppgjør.

      - Transaksjonsoppgaven vil plukke opp alle uposterte og godkjente transaksjoner, og opprette salgsordrer, salgsfakturaer, betalings- og rabattjournaler og transaksjoner for inntekter/utgifter med det intervallet du konfigurerer. Du bør konfigurere denne prosessen til å kjøre med høy frekvens, slik at dokumenter opprettes når transaksjonene lastes opp til Headquarters via P-jobben. Med transaksjonsutdraget som allerede oppretter salgsordrer og salgsfakturaer, er det ikke noe reelt behov for å konfigurere den satsvise jobben **Poster lager**. Du kan imidlertid fortsatt bruke den til å oppfylle bestemte forretningskrav som du kanskje har.  
      
     - Regnskapsoppgjøret er utformet til å opprettes på slutten av dagen, og støtter bare avsluttingsmetoden **Skift**. Dette utdraget vil være begrenset til økonomisk avstemming, og vil bare opprette journaler for de ulike beholdningsbeløpene mellom telt beløp og transaksjonsbeløp for de forskjellige anleggsmidlene, sammen med journaler for andre kontantstyringstransaksjoner.   

3. Hvis du vil beregne transaksjonsutdraget, går du til **Retail og Commerce > IT for Retail og Commerce > Salgsstedspostering > Beregn transaksjonsutdrag satsvis**. Hvis du vil postere transaksjonsutdragene satsvis, går du til **Retail og Commerce > IT for Retail og Commerce > Salgsstedspostering > Poster transaksjonsutdrag satsvis**.

4. Hvis du vil beregne regnskapsoppgjøret, går du til **Retail og Commerce > IT for Retail og Commerce > Salgsstedspostering > Beregn regnskapsoppgjør satsvis**. Hvis du vil postere regnskapsoppgjøret satsvis, går du til **Retail og Commerce > IT for Retail og Commerce > Salgsstedspostering > Poster regnskapsoppgjør satsvis**.

> [!NOTE]
> Menyelementene **Retail og Commerce > IT for Retail og Commerce > Salgsstedspostering > Beregn utdrag satsvis** og **Retail og Commerce > IT for Retail og Commerce > Salgsstedspostering > Poster utdrag satsvis** blir fjernet med denne nye funksjonen.

Du kan også opprette typer transaksjons- og regnskapsoppgjør manuelt. Gå til **Retail og Commerce > Kanaler > Butikker** og klikk **Utdrag**. Klikk **Ny**, og velg deretter typen utdrag du vil opprette. Felt på siden **Utdrag** og handlinger under **Utdragsgruppe** på siden viser relevante data og handlinger basert på den valgte utdragstypen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]