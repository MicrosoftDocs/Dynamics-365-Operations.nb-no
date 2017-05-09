---
title: "Betalingsmåter i et telefonsenter"
description: "Dette emnet beskriver de ulike betalingsmåtene som du kan bruke i et telefonsenter i Detaljhandel og handel."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 636d83ecc7732a164924352853603588cded0db4
ms.lasthandoff: 03/31/2017


---

# <a name="payment-methods-in-a-call-center"></a>Betalingsmåter i et telefonsenter

[!include[banner](includes/banner.md)]


Dette emnet beskriver de ulike betalingsmåtene som du kan bruke i et telefonsenter i Detaljhandel og handel.

Betalingsmåtene som brukes i andre kanaler i Detaljhandel og handel i Microsoft Dynamics AX, for eksempel kontanter, sjekk, kredittkort og gavekort, kan også brukes i telefonsentre. Når du definerer en betalingsmåte for et telefonsenter, vises den som et av alternativene i **Betalinger**-delen på siden **Salgsordre** for telefonsenterbrukere. Du kan også definere kuponger for å gi kunder rabatter når de bestiller noe i organisasjonens telefonsenter. Kuponger kan være for en fastbeløpsrabatt eller for en prosent av en varepris eller ordretotalen. En beløpsbasert kupong kan for eksempel tilby kundene en rabatt på 75.00 når kunden bruker 750.00 eller mer. Du kan opprette ulike typer kuponger, definere overordnede/underordnede kuponger og kopiere eller annullere en kupong. Bruk alternativene i tabellen nedenfor for å opprette kuponger.

|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Attributt**             | I **Innløsingssats**-feltet angir du den forventede innløsingssatsen for kupongen som en prosent, og deretter velger du om kupongen kan brukes på engangskupong, skal utstedes på nytt automatisk, eller gjelde spesifikt for en kunde.                                                                                                                                                                                                                                                                                                                                                                                       |
| **Gyldig**                 | I feltene **Startdato** og **Sluttdato** angir du datoene for første og siste dag kupongen er gyldig.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Inkluderings-/utelatelsesregler** | I feltene **Kataloger** og **Varer** velger du om eventuelle kataloger eller varer skal inkluderes i eller utelates fra kupongen. Hvis du velger **Inkluder** eller **Utelat**, klikker du **Oppsett**, velger **Inkluder/utelat kataloger** eller **Inkluder/utelat produkter**, og angir informasjon om katalogen eller varen. Hvis du velger **Ingen** i disse feltene, blir alle kataloger eller varer tatt med i kupongen.                                                                                                                                                                                                                          |
| **Diverse**         | Hvis denne kupongen ikke kan brukes sammen med andre rabatter, merker du av for **Eksklusiv**. Deretter velger hvor kupongen kan brukes, i **Opprinnelse** -feltet. Hvis dette er kupongen til en produsent, merker du av for **Produsentkupong**.                                                                                                                                                                                                                                                                                                                                                                |
| **Fremtidig kupong**         | Hvis denne kupongen skal tilknyttes andre kuponger som en overordnet kupong, merker du av for **Overordnet kupong**. Hvis denne kupongen skal tilknyttes som underordnet for en eksisterende kupong, velger du den overordnede kupongen i feltet **ID for overordnet kupong**. Du kan for eksempel opprette en kupong for den kommende vårkatalogen. Alle andre kuponger du oppretter for vårkatalogen, blir underordnede kuponger for kupongen for vårkatalogen. Underordnede kuponger kan inneholde 20 prosent rabatt for nye kundeordrer, 10 prosent rabatt på en nylig utgitt vare eller en rabatt på 95,00 på ordrer på 1 000,00 eller mer. |

Hvis du sender en kredittkortbetaling fra siden **Salgsordre** og får en melding om at kortet ikke ble godkjent, kan du håndtere godkjenning manuelt. Du kan godkjenne, avvise eller sende en kredittkorttransaksjon på nytt ved hjelp av siden **Autorisasjonsadministrasjon**. Du bruker siden Telefonsenterparametere til å konfigurere tilleggsalternativene for betalingsbehandling:

-   Sjekksperrer lar økonomiansatte behandle ordrer som sperret fordi en sjekk ble brukt når betalingsmåte, og sjekken overskrider terskelbeløpet for sjekksperring. Sperring kan frigis manuelt, eller den utløper automatisk ved slutten av perioden som er konfigurert.
-   Du kan angi terskler for refunderinger som utstedes via sjekker eller kredittkort, der overskridelse av tersklene gjør at refunderingene må godkjennes manuelt. Refundering som overskrider terskelbeløpet, legges til i godkjenningskøen. Når du har godkjent refunderingen, kan retursalgsordren faktureres.





