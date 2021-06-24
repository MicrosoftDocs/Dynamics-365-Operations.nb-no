---
title: Instrumentbord for bruksstyring
description: Dette emnet forklarer hvordan du bruker instrumentbordet for bruksstyring til å overvåke bruken av tjenesten for elektronisk fakturering og opprettholder samsvar med forskriftene.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130512"
---
# <a name="usage-management-dashboard"></a>Instrumentbord for bruksstyring

[!include [banner](../includes/banner.md)]

Instrumentbordet **Bruksstyring** hjelper deg å overvåke bruken av tjenesten for elektronisk fakturering, slik at organisasjonen kan opprettholde samsvar med forskriftene når det gjelder månedlig bruk. Forskriftssamsvar fastsettes ved å beregne innsendingsvolumet og sammenligne det med det tilegnede innsendingsvolumet for å finne eventuelle avvik mellom tilegnet og brukt volum.

Instrumentbordet har følgende indikatorer:

- Én kostnadsindikator du kan bruke til å overvåke forbruk for å sikre at det er i tråd med lisensen:

    - Bruk per måned (eksport)

- Tre driftsindikatorer du kan bruke til å spore bruk av tjenesten for elektronisk fakturering til administrasjonsformål:

    - Bruk etter funksjon
    - Bruk etter miljø
    - Bruk per måned (import)

## <a name="measurement-scope"></a>Målingsomfang

- Måleenhet: 

    Instrumentbordet **Bruksstyring** teller forretningsdokumentene som sendes inn, og importerte elektroniske fakturaer.

- Organisasjon: 

    Opptellingen summeres etter leier-ID-en for organisasjonen, uansett antall forekomster av Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management, eller antall juridiske enheter der tjenesten for elektronisk fakturering er aktivert.


## <a name="indicator-usage-per-month-export"></a>Indikator: Bruk per måned (eksport)

Denne indikatoren gir detaljer om de elektroniske fakturaene som organisasjonen utsteder i løpet av en definert periode.

### <a name="scope"></a>Område
- Antall forretningsdokumenter som sendes fra Finance og Supply Chain Management til tjenesten for elektronisk fakturering, uansett hvor mange linjer disse forretningsdokumentene inneholder.
- Antall innsendte forretningsdokumenter som er behandlet av tjenesten for elektronisk fakturering. Et dokument regnes som behandlet når handlingsflyten som er definert i funksjonskonfigurasjonen, er fullført.

> [!NOTE]
> Når en elektronisk faktura sendes til en ekstern nettjeneste, er opptellingen uavhengig av resultatene av nettjenestebehandling (godtatt, avvist eller skjemavalideringsfeil). Hvis nettjenesten mottok og svarte på forespørselen fra tjenesten for elektronisk fakturering, regnes innsendingen som en gyldig telling.

- **Unntak:** Forretningsdokumenter telles ikke hvis de sendes inn på nytt fra Finance og Supply Chain Management til tjenesten for elektronisk fakturering, for eksempel i scenarioer der det kreves en ny sending av samme forretningsdokument for å endre statusen for den elektroniske fakturaen. Utstedelse av en elektronisk faktura for Brasil (regnskapsdokument) telles for eksempel som gyldig, men annulleringsforespørselen for den telles ikke.


### <a name="calculation"></a>Beregning

Beregningen av saldoen utføres som følger:

Saldo = Gratis + Kjøpt – Brukt

Der:

- Gratis:
  
    Et gratis volum med forretningsdokumenter kunden kan sende inn per måned. Det omfatter en pakke med 100 forretningsdokumenter som kan sendes inn til tjenesten for elektronisk fakturering. Gratisvolumet er ikke kumulativt, og eventuell gjenstående saldo rulles ikke over til neste periode.
  
- Kjøpt:
  
    En pakke med 1000 forretningsdokumenter som kan sendes inn til tjenesten for elektronisk fakturering. Denne pakken må anskaffes for organisasjonen hver måned. Det kjøpte volumet er ikke kumulativt, og eventuell gjenstående saldo rulles ikke over til neste periode.
  
- Brukt: 

    Opptellingen av forretningsdokumentinnsendinger til tjenesten for elektronisk fakturering i henhold til definerte kriterier.
   
> [!IMPORTANT]
> Hvis organisasjonen har tenkt å overskride det månedlige volumet på 100 gratis innsendinger, kjøper du det høyeste volumet for å sikre at du opptrer i tråd med Microsofts lisenspolicy for tjenesten for elektronisk fakturering.
>
> Det kjøpte volumet må for tiden angis manuelt i henhold til anskaffelsesdatoen som flere pakker med 1000 innsendinger.

## <a name="indicator-usage-by-feature"></a>Indikator: Bruk etter funksjon

Denne indikatoren viser bruken av funksjoner for elektronisk fakturering til utstedelse av elektroniske fakturaer i løpet av en definert periode.

- Beregning:
  
    Brukt = antall ganger hver funksjon for elektronisk fakturering ble brukt under innsendingen av forretningsdokumenter til tjenesten for elektronisk fakturering.

## <a name="indicator-usage-by-environment"></a>Indikator: Bruk etter miljø

Denne indikatoren viser bruken av tjenestemiljøer for elektronisk fakturering i løpet av en definert periode.

- Beregning:
    
    Brukt = antall ganger hvert tjenestemiljø for elektronisk fakturering ble brukt under innsendingen av forretningsdokumenter til tjenesten for elektronisk fakturering.

## <a name="indicator-usage-per-month-import"></a>Indikator: Bruk per måned (import)

Denne indikatoren viser volumet av elektroniske fakturaer som er importert av tjenesten for elektronisk fakturering til Finance og Supply Chain Management i en definert periode.

- Område:

    Elektroniske fakturaer som importeres til Finance og Supply Chain Management, uansett hvor mange linjer de elektroniske fakturaene inneholder.

- Beregning:

    Mottatt = opptellingen av importerte elektroniske fakturaer til Finance og Supply Chain Management.

## <a name="functions"></a>Funksjoner
### <a name="purchase"></a>Kjøp

Velg **Kjøp** for å registrere beløpet for de anskaffede innsendingene manuelt, i fanen **Bruk per måned (eksport)**.

Velg **Ny** for en gitt dato, og angi antallet **Pakker** som er anskaffet på denne datoen.

**Antall** beregnes som følger:

Antall = Pakker * 1,000

Beregnet **Antall** gjenspeiles i **Kjøpt** fra indikatoren **Bruk per måned (eksport)**.

### <a name="update"></a>Oppdatering

Velg **Oppdater** i handlingsruten for å oppdatere beregningen og dataene som vises på siden og i diagrammet.

### <a name="reset-history-data"></a>Tilbakestill historikkdata

Velg **Tilbakestill loggdata** i handlingsruten for å oppdatere databasen som indikatorene skal beregnes fra.




> [!NOTE]
> Instrumentbordet **Bruksstyring** viser ikke pengebeløp. Det viser i stedet bare volumet av telte innsendinger og importerte dokumenter.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
