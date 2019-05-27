---
title: Beholdningslukking
description: Som en del av prosessen for å utligne avgangstransaksjoner med mottakstransaksjoner, kan du også velge å få økonomimodulen oppdatert for å gjenspeile justeringene som er gjort.
author: AndersGirke
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventClosing
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 61973
ms.assetid: c210c882-6849-4704-b78c-a777dd6cfdb6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a705853ea27d117c99a00893b862348bbac0b9b0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560789"
---
# <a name="inventory-close"></a>Beholdningslukking

[!include [banner](../includes/banner.md)]

Som en del av prosessen for å utligne avgangstransaksjoner med mottakstransaksjoner, kan du også velge å få økonomimodulen oppdatert for å gjenspeile justeringene som er gjort.

Lagerlukkingsprosessen i utligner avgangstransaksjoner mot tilgangstransaksjoner på grunnlag av lagervurderingsmetoden som er valgt i varens varemodellgruppe. Som del av utligningsprosessen kan du angi at økonomimodulen skal oppdateres, slik at den gjenspeiler justeringene som er gjort. Før lagerlukkingen eller omberegningen er kjørt, vil imidlertid avgangstransaksjoner posteres med det løpende gjennomsnittet for kostpris som er beregnet. 

Etter lagerlukkingen kan du ikke lenger postere i perioder som kommer før den angitte lagerlukkingsdatoen, med mindre du tilbakefører en fullført lagerlukkingsprosess. For eksempel kan kjører lagerlukking for perioden som slutter på den 31, du bokføre transaksjoner som har en dato som er tidligere enn 31 januar. 

Varer på lager tilordnes til én av to beholdningstyper: vare eller tjeneste. Lagerlukkingen utfører de samme funksjonene for begge typer. For servicevarer vil lagerlukkingen imidlertid fremdeles utligne avganger til mottak. 

Hvor ofte lagerlukkingsprosessen kjøres, varierer etter firma. Transaksjonsvolumet bør imidlertid bidra til å bestemme hvor ofte du vil kjøre lagerlukking. Som regel kjører de fleste firma lagerlukking som en del av månedsavslutnings- og avstemmingsprosedyren.

## <a name="inventory-recalculation-and-the-general-ledger"></a>Lageromberegning og økonomimodulen
Hvis du må gjøre justeringer i beholdning og i økonomimodulen i løpet av måneden eller en annen lagerperiode, kan du kjøre en lageromberegning i stedet for en lagerlukking. En lageromberegning justerer lagertransaksjoner, men utligner dem ikke. 

Under lageromberegning justeres lagerbeholdningen og lagertransaksjoner, og lageromberegninger og lagerlukkinger kjøres. Disse oppgavene virker inn på enhver finanskonto som er koblet til den opprinnelige lagertransaksjonen. 

**Eksempel** 

Når du oppretter en bestilling fra en salgsordre, oppdateres finanskontoene som ble brukt for den opprinnelige salgsordren. Selv om finanskontoene for varegruppen som er tilknyttet varen, ble endret etter at salgsordren ble postert, og en lageromberegning opprettet et justeringsbeløp, vil justeringsbeløpet likevel bli postert til de opprinnelige finanskontoene, ikke de nye finanskontoene som er tilordnet varen. De justerte beløpene ikke er postert til de nye finanskontoene som er tilordnet til varen. 

Når oppdateringen er fullført, kan du gå gjennom finansbilaget som posteres på grunn av en av disse oppgavene.

1.  På siden **Lukking og justering** i kategorien **Oversikt** velger du oppdateringen som skal gås gjennom.
2.  Klikk **detaljer**, og velg deretter **Bilag**.

## <a name="effects-of-the-inventory-close-process-on-the-general-ledger"></a>Virkningen av lagerlukkingsprosessen i økonomimodulen
Flere av oppgavene du kan utføre på siden **Lukking og justering**, fører til oppdateringer i økonomimodulen. Økonomimodilen oppdateres for eksempel når du foretar beholdningsjusteringer på lager, foretar lagertransaksjonsjusteringer, kjøre en lageromberegning og kjører en lagerlukking. 

Finanskontoene som oppdateres på grunn av disse oppgavene, er koblet til den opprinnelige lagertransaksjonen. Hvis en salgsordre utlignes til en bestilling, vil for eksempel finanskontoene som ble brukt til den opprinnelige salgsordren, bli justert. Dette gjelder selv om finanskontoene for varegruppen som er tilordnet til dette elementet, er endret siden salgsordren ble postert. Når lagerlukking oppretter et utligningsbeløp, er utligningsbeløpet fremdeles postert på de opprinnelige finanskontoene, og ikke på de nye finanskontoene som er tilordnet til varen. Økonomimodulen kan også bli oppdatert hvis du reverserer en lagerlukking. 

**Merknader:**

-   Lagerlukking er ikke obligatorisk hvis du bruker vurderingmetoden standardkost.
-   Før du kjører lukkingsprosedyren kan du vise en liste over varer som ikke kan utlignes under oppdateringen.
-   Vi anbefaler at du kjører lagerlukkingen utenfor vanlig arbeidstid for å sørge for en mer jevn fordeling av datamaskinressurser

## <a name="the-inventory-close-log"></a> Loggen for lagerlukking
Når lagerlukkingsprosessen er fullført, kan det hende at en melding i meldingssentret rapporterer at kostprisen for en vare er feil fordi en transaksjon ikke kan utlignes helt. 

Før denne meldingen blir vist, rapporterer systemet varenummeret og transaksjonen det gjelder. Meldingen forteller deg at kostnadsbeløpet som er brukt for denne transaksjonen, ikke ble oppdatert på grunn av lagerlukkingen. Denne meldingen vises når en transaksjon av avgangstypen ikke kan utlignes. 

Under lagerlukkingsprosessen kontrollerer systemet hver finansdimensjon for å se om det finnes flere avganger enn mottak opptil den angitte avslutningsdatoen. Denne typen ubalansen kan oppstå når en lagertransaksjon fra en bestilling ikke er fullstendig postert økonomisk, fordi leverandørfakturaen ikke er mottatt, eller fordi stykklistekomponenter som er inkludert i en produksjon på et høyere nivå, ikke er økonomisk postert. (Delproduksjonen er ikke kostnadsberegnet.) I dette tilfellet vil ikke den etterfølgende lukkingen justere alle avganger til riktig kostpris, fordi det ikke finnes tilstrekkelig mottaksinformasjon. 

For hver kjøring av lukkingsprosedyren vil systemet angi om en logg med advarsler er lagret og kan vises. 

Hvis du får mange advarsler i meldingen, anbefaler vi at du gjør følgende:

-   Oppdaterer mottak økonomisk.
-   Fremskyver avslutningsdatoen
-   Gjennomgår forretningsprosedyrene på nytt.

I enkelte tilfeller kan du kanskje ikke kan gjøre noe med advarslene. Når merking for eksempel brukes, og den merkede bestillingen har en finansdato som er etter avslutningsdatoen, kan ikke avslutningsdatoen endres.

## <a name="reversing-a-completed-inventory-close"></a>Tilbakeføre en fullført lagerlukking
Noen ganger kan du bli nødt til å tilbakeføre en fullført lagerlukking for å sette utligninger tilbake til statusen de hadde før justeringer ble utført. Når du tilbakefører en fullført lagerlukking, blir lageret åpnet på nytt for å muliggjøre postering i perioden som lagerlukkingen dekker. Relaterte endringer kan også foretas i økonomimodulen. Når du er ferdig med å gjøre justeringer, kan du kjøre lagerlukking på nytt for perioden du arbeider med. 

**Obs!** Bare den siste lagerperioden som ble lukket, kan åpnes på nytt. For å tilbakeføre en tidligere lagerlukking må du tilbakeføre hver etterfølgende lagerlukking én om gangen og begynne med den siste lukkingen.



