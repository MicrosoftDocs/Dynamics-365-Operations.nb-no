---
title: Definere og generere informasjon om aldersfordeling for kunde
description: Denne veiledningen vil hjelpe deg med å sette opp en definisjon av aldersfordelingsperioden, aldersfordele kundesaldoer og vise saldoer i den aldersfordelte saldolisten og Innkrevinger-siden.
author: abruer
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 996fb289c32a1819103fd67ffddc940dfd2870fb
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753566"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Definere og generere informasjon om aldersfordeling for kunde

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
