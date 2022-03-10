---
title: Forutsetninger for standard kostnadskonvertering
description: Dette emnet beskriver oppgaver som må utføres før du kjører en standard kostnadskonvertering.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 50891
ms.assetid: 73af66cf-c924-45be-837a-a648dbd05a31
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2eefb305f12996eb8fe1b72715f7e8e2509c551ff1e6abb3656221a8dbc76461
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734313"
---
# <a name="prerequisites-for-a-standard-cost-conversion"></a>Forutsetninger for standard kostnadskonvertering

[!include [banner](../includes/banner.md)]

Dette emnet beskriver oppgaver som må utføres før du kjører en standard kostnadskonvertering. 

Før du kjører en standard kostnadskonvertering, gjør du følgende:

1.  Definer en **varemodellgruppe** for standard kostpris. Bruk Varemodellgrupper-siden til å opprette en varemodellgruppe som bruker lagermodellen med standard kostpris. Når du definerer en standard kostnadskonvertering, tilordner du denne varemodellgruppen til varene som konverteres.
2.  Tilordne en **kostgruppe** til hver vare.
    -   Kostgruppen som tilordnes til en innkjøpt vare, kan fungere som grunnlag for tilordning av finanskontoer som er knyttet til standard kostpris. Dette kan omfatte tilordning av finanskontoer for innkjøpsprisavvik. I et produksjonsmiljø gir kostgruppen som er tilordnet innkjøpte komponenter også kostnadssegmentering i de beregnede kostnadene for en produsert vare.
    -   Kostgruppen som er tilordnet en produsert vare, kan fungerer som utgangspunkt for tilordning av finanskontoer som er knyttet til standardkostnader, som tilordning av finanskontoer for avvik i produksjon.

3.  Tilordne et **standard ordreantall** til en produsert vare når den har konstantkostnader. Standard ordreantall for en produsert vare fungerer som en regnskapspartistørrelse for amortisering eller proporsjonal fordeling av konstante kostnader. Disse kan omfatte oppstillingstid i ruteoperasjoner eller en konstant komponentmengde i en stykkliste.
4.  Tilordne **økonomikontoer** som er knyttet til standard kostpris, særlig revalueringsavvik. Bruk **Postering**-siden (**Lagerstyring** &gt; **Oppsett**) til å tilordne økonomikontoer som er relatert til standard kostpris. For standard kostnadskonverteringsprosessen må du som et minimum, tilordne kontoen for revalueringsavvik for alle varer og kostgrupper. Bruk **Kontoplan**-siden for å definere økonomikontoene som trengs for standard kostpris. Bruk siden **Transaksjonskombinasjoner** til å aktivere kostrelasjoner (for tabeller, grupper og alle) før du definerer vareposteringsreglene.
5.  Definer lagerparameterne som er relatert til standard kostpris. Bruk fanen **Nummerserier** på siden **Parametere for beholdnings- og lagerstyring** for å tilordne en nummerserie til revalueringsbilag. Det genereres et revalueringsbilag når standardkostnadskonverteringen oppretter en endring av varens lagerverdi. Bruk siden **Parametere for beholdnings- og lagerstyring** for å definere kostkontrollparametere (i fanen **Lagerregnskap**) for å definere to parametere som er relatert til standard kostpris.
    -   Bruk feltet **Oppdeling av kostnader** til å velge Nei eller Underfinans. Valget Underfinans betegnes som aktiv kostnadsoppdeling. Aktiv kostnadsoppdeling er svært viktig for beregning, opprettholding og visning av kostgruppesegmentering gjennom en produktstruktur på flere nivåer for varer med standard kostpris. Når kostnadsoppdelingen er aktiv, kan du rapportere og analysere følgende i formatet enkelt nivå, flere nivåer eller totalt:
        1.  Beholdning
        2.  Varer i arbeid (VIA)
        3.  Solgte varers kost (vareforbruk) per kostnadsgruppe

        Aktiv kostnadsoppdeling betyr at hvis du aktiverer prisen for en produsert vare, lagres resultatet i kostgruppesegmenteringen i varens kostprispost. Hvis du ikke legger inn en verdi i feltet **Oppdeling av kostnader**, blir ikke kostgruppesegmenteringen opprettholdt for varer med standard kostpris. Det vil si at standard kostpris for en produsert vare vil bli beregnet og opprettholdt som et enkeltbeløp uten kostgruppesegmentering, og kostbidragene for produserte komponenter vil bli aggregert inn i dette enkeltbeløpet.
    -   Bruk feltet **Avvik for standard** til å velge summert eller per kostgruppe. Valget av per kostgruppe gjør at du kan identifisere avvik i innkjøpspris og produksjonsavvik etter kostgruppe. Dette gir også mulighet til å identifisere de fire typene produksjonsavvik (avvik i partistørrelse, antall, pris og erstatning). Hvis du valgte summert, kan du ikke identifisere avvik etter kostgruppe, og du kan ikke identifisere de fire typene produksjonsavvik. Du kan bare vise en oppsummering av produksjonsavviket. Policyen om avvik for standard kostpris er uavhengig av policyen for kostnadsoppdeling. Det vil si at hvis du velger ingen policy for kostnadsoppdeling samt avvik per kostgruppe, vil produksjonsavvik etter kostgruppe fremdeles vil bli fanget opp.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]