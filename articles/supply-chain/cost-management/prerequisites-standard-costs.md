---
title: Oversikt over forutsetninger for standardkostnader
description: Denne artikkelen beskiver de grunnleggende trinnene for bruk av standard kostpris.
author: JennySong-SH
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c36ebe0957cff85fff6af1d979503f9e6e60d28
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066738"
---
# <a name="prerequisites-for-standard-costs-overview"></a>Oversikt over forutsetninger for standardkostnader

[!include [banner](../includes/banner.md)]

Denne artikkelen beskiver de grunnleggende trinnene for bruk av standard kostpris. Fremgangsmåten avhenger av firmaets opererasjoner. Fremgangsmåten er for eksempel forskjellig for et firmaet uten egenproduksjon, et produksjonsmiljø som ikke bruker ruting og et produksjonsmiljø som bruker ruting. 

Følg denne fremgangsmåten for å definere standard kostpris.

**1. Opprett en varemodellgruppe for standard kostpris.**

Bruk **Varemodellgrupper**-siden for å opprette en ny gruppe for standard kostpriser, og tilordne en lagermodell med **standardkost**. Identifikatoren for varemodellgruppen bør ha mening, for eksempel **Std.kost**. Merk av for å angi at gruppen skal tillate økonomisk negativt lager, og at det skal postere fysisk lager og økonomisk lager. Denne standardkostgruppen vil tilordnes til varer.

**2. Definer finanskontoer som er relatert til avvik i standard kostpris.** 

Bruk **Kontoplan**-siden for å definere finanskontoer som er relatert til avvik i standard kostpris. Disse finanskontoene må være definert før de kan tilordnes på **Postering**-siden. Finanskontoene kan gjenspeile varegrupper og kostgrupper.

**3. Tilordne finanskontoer til vareposteringer som er relatert til avvik i standard kostpris.** 

Bruk **Postering**-siden til å tilordne finanskontoer som er relatert til avvik i standard kostpris. Du kan angi en finanskonto for en variant etter vare (eller varegruppe) og kostgruppe (eller kostgruppetype), eller du kan angi at finanskontoen gjelder for alle varer og kostgrupper. Disse alternativene tilsvarer kostrelasjoner for tabeller, grupper og alle. 

Før du definerer vareposteringsreglene, bruker du siden **Transaksjonskombinasjoner** til å aktivere kostrelasjoner (for tabeller, grupper og alle).

**4. Definer lagerparameterne som er relatert til standard kostpris.** 

-  Bruk fanen **Lagerregnskap** på siden **Oppsett for regnskapspolicyer for beholdning > Parametere** til å definere to kostkontrollparametere som er relatert til standard kostpris.

    -  I **Oppdeling av kostnader**-feltet velger du **Ingen** eller **Underfinans**. Hvis du velger **Underfinans**, er kostnadsoppdelingen en *aktiv* kostnadsoppdeling. Aktiv kostnadsoppdeling er kritisk for beregning, opprettholding og visning av kostgruppesegmentering gjennom en produktstruktur på flere nivåer for varer med standard kostpris. Når kostnadsoppdelingen er aktiv, kan du rapportere og analysere lagerbeholdningen, varer i arbeid (VIA) og kostnader for solgte varer per kostgruppe på ett enkelt nivå, over flere nivåer eller totalt. Når kostnadsoppdelingen er aktiv, hvis du aktiverer en produsert vares kostnad, lagres kostgruppesegmenteringen i varens kostprispost. 

    -  Hvis du velger **Ingen**, vil ikke kostgruppesegmentering bli opprettholdt for standardkostvarer. Med andre ord blir en produsert vares standardkost beregnet og opprettholdt som et enkelt beløp, uten kostgruppesegmentering. Kostbidragene for produserte komponenter vil bli aggregert til ett enkeltbeløp.

-  I **Avvik for standard**-feltet velger du **Summert** eller **Per kostgruppe**. Hvis du velger **Per kostgruppe**, kan du identifisere avvik i innkjøpspris og produksjonsavvik etter kostgruppe. Du kan også identifisere de fire typene produksjonsavvik: avvik i partistørrelse, antall, pris og erstatning. Hvis du valgte **Summert**, kan du ikke identifisere avvik etter kostgruppe, og du kan ikke identifisere de fire typene produksjonsavvik. Du kan bare vise en oppsummering av produksjonsavviket.

-  Policyen om avvik for standard kostpris fungerer uavhengig av policyen for kostnadsoppdeling. Det vil si at hvis du velger **Ingen** policy for kostnadsoppdeling samt avvik per kostgruppe, vil produksjonsavvik etter kostgruppe fremdeles vil bli fanget opp.

**5. Opprett kostnadsberegningsversjoner for standard kostpris.** 

Bruk siden **Oppsett av etterkalkuleringsversjon** til å opprette én eller flere kostnadsberegningsversjoner for standard kostpris. Hver kostnadsberegningsversjon må være definert med en kostnadsberegningstype for **Standard kostpris** og må tillate innhold som omfatter kostnadsdata.

**6. Klargjør en eksisterende kunde for bruk av standard kostpris.** 

Kunder som vil endre sine eksisterende varer til en lagermodell med standard kostpris, må bruke siden **Standard kostnadskonvertering**.


## <a name="related-articles"></a>Relaterte artikler

[Oversikt over konvertering av standardkostnad](standard-cost-conversion-overview.md)

### <a name="blogs"></a>Blogger

#### <a name="community-blogs"></a>Fellesskapsblogger

- [Konfigurere standardkostnader for direkte materialer i Finance and Operations](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [Standard direkte arbeidskostnader i Finance and Operations](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
