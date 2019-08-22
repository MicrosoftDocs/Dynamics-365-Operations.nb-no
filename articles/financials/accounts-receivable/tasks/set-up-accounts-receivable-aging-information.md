---
title: Definere og generere informasjon om aldersfordeling for kunde
description: Denne veiledningen vil hjelpe deg med å sette opp en definisjon av aldersfordelingsperioden, aldersfordele kundesaldoer og vise saldoer i den aldersfordelte saldolisten og Innkrevinger-siden.
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77b5dd5feb16cc3bd6d64b6520cc47087c5b5224
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834373"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Definere og generere informasjon om aldersfordeling for kunde

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne veiledningen vil hjelpe deg med å sette opp en definisjon av aldersfordelingsperioden, aldersfordele kundesaldoer og vise saldoer i den aldersfordelte saldolisten og Innkrevinger-siden. Denne registreringen bruker demonstrasjonsfirmaet USMF.


## <a name="create-an-aging-period-definition"></a>Opprette definisjon av en aldersfordelingsperiode
1. Gå til **Navigasjonsrute > Moduler > Kreditt og innkreving > Oppsett > Definisjoner av aldersfordelingsperiode**.
2. Klikk på **Ny**.
3. Angi en verdi i feltet **Definisjon av aldersfordelingsperiode**.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Klikk **Legg til nedenfor** for å sette inn en ny aldersfordelingsperiode.
6. Angi beskrivelsen skal vises i rapporter for aldersfordeling, i **Periode**-feltet.
7. Angi et tall i **Enhet**-feltet.
8. Velg et alternativ i **Intervall**-feltet. Finansperiode samsvarer med perioden til finanskalenderen. Dag, uke, måned, kvartal og år definerer størrelsen på intervallet etter datotype. Ubegrenset velger alle transaksjoner som er før eller etter forrige periode, avhengig av om det er den første eller siste perioden.  
9. Velg et alternativ i feltet **Indikator for aldersfordeling**.
10. Velg perioden øverst i rutenettet. Oppdater beskrivelsen for å beskrive den eldste perioden i definisjonen av aldersfordelingsperiode.
11. Angi den nye beskrivelsen for aldersfordelingsperiode i **Periode**-feltet.
12. Lukk siden.

## <a name="age-the-balances"></a>Aldersfordele saldoere
1. Gå til **Kreditt og innkreving > Periodiske oppgaver > Aldersfordel kundesaldoer**.
2. Velg definisjonen av aldersfordelingsperiode som du opprettet, i feltet **Definisjon av aldersfordelingsperiode**.
    + Du kan ha ett aktivt øyeblikksbilde for hver definisjon av aldersfordelingsperiode.  
    + Alle kunder behandles som standard. Du kan bruke dette valget til å beregne en enkelt samlingspulje med kunder.  
    + Velg datoen fra transaksjonen som du vil bruke for aldersfordeling.  
    + Velg en "per"-dato for aldersfordeling. Standarden er i dag, men hvis du endrer dette feltet til Valgt dato, vil du kunne velge den ønskede datoen. For satsvis behandling kan du bruke dagens dato.  
3. Utvid **Firma**-området. Du kan velge firmaene som skal inkluderes i det statiske utvalget. Det gjeldende selskapet er valgt som standard.
4. Klikk **OK** for å behandle øyeblikksbildet. Det vil ta litt tid, så vent til glidebryteren forsvinner og kontroller meldingssentret for en melding.

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>Se på saldoene på listen over aldersfordelte saldoer og på innkrevingssiden
1. Gå til **Kreditt og innkreving > Innkrevinger > Aldersfordelte saldoer**. Listesiden viser saldoene for kunden. Aldersfordelingsikonet viser aldersfordelingsperioden for den eldste transaksjonen.  
2. Velg en kunde med en saldo.
3. Vis faktaboksområdet **Aldersfordeling** for å vise de aldersfordelte saldoene. Definisjonen av aldersfordelingsperiode for faktaboksen hentes fra standarddefinisjonen av aldersfordelingsperiode angitt i parameterne. Du kan endre den ved hjelp av Samle inn-menyen.  

