---
title: Fast mottakspris
description: Denne artikkelen beskriver hvordan du kan konfigurere og bruke faste mottakspriser i Microsoft Dynamics 365 Supply Chain Management.
author: raprofit
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 2630952f395d1a18202698b4d73b67ef4b760194
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907587"
---
# <a name="fixed-receipt-price"></a>Fast mottakspris

[!include [banner](../includes/banner.md)]

**Fast mottakspris** er et alternativ som du kan velge for en varemodellgruppe når du bruker en annen lagermodell enn *Standard kost* eller *Glidende avveid gjennomsnitt*. I tidlige versjoner av Microsoft Dynamics AX het dette alternativet **Standardkostn**. Det ble gitt nytt navn til **Fast mottakspris** da den nye lagermodellen for standard kostpris ble innført i Dynamics AX 2012. Denne artikkelen beskriver hvordan du kan konfigurere og bruke faste mottakspriser i Dynamics 365 Supply Chain Management.

## <a name="about-fixed-receipt-prices"></a>Om faste mottakspriser

Når du merker av for **Fast mottakspris** på siden **Varemodellgruppe** for en vare, bruker systemet mottaksprisen som en standardkostnad for lagermottaket. Hvis innkjøpsprisen og standard varekostpris som er konfigurert for et produkt avviker, posteres differansen til kontoen **Fortjeneste på fast mottakspris** eller **Tap på fast mottakspris** og motposteres til kontoen **Motkonto for fast mottakspris** som du angir på siden **Lagerposteringsprofil**.

Siden alternativet **Fast mottakspris** brukes sammen med ulike lagermodeller (for eksempel først-inn-først-ut (FIFO); sist inn, først ut (LIFO) og avveid gjennomsnitt), vil prosessen for *lagerlukking og justering* fremdeles opprette utligninger og justeringer i henhold til lagerprinsippet du velger på siden **Varemodellgruppe**. Justeringer gjøres imidlertid bare i avganger fra lageret.

Du har for eksempel konfigurert et produkt med en varemodellgruppe der **Lagermodell**-feltet er satt til *FIFO*, og alternativet **Fast mottakspris** er valgt. Når du mottar lagerbeholdning via en bestilling, blir lagerverdien satt til verdien av varens standard kostpris ved produktmottak. Når du fakturerer bestillingen, og hvis fakturaprisen er forskjellig, posterer systemet standard kostpris på det frigitte produktet til lagerkontoen. Den posterer differansen til kontoen for fortjeneste eller tap ved fast mottakspris. Når du senere selger eller forbruker produktet, bruker systemet det glidende gjennomsnittet for varen på det tidspunktet da salgsordrefakturaen ble postert (med mindre du bruker merking).

Når du kjører *lagerlukkings- og justeringsprosessen* oppretter systemet en utligning med det første mottaket mot den første avgangen. Differansen mellom mottaksprisen som ble brukt på mottaket, og det glidende gjennomsnittet som ble brukt på avgangen, posteres i et nytt bilag.

## <a name="enable-fixed-receipt-prices"></a>Aktivere faste mottakspriser

Følg denne fremgangsmåten for å aktivere faste mottakspriser for en vare.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Varemodellgrupper**.
2. Opprett en ny varemodellgruppe, eller velg en eksisterende modellgruppe.
3. I **Etterkalkuleringsmetode og kostnadsføring**-hurtigkategorien merker du av for **Fast mottakspris**.

    > [!NOTE]
    > Du kan ikke merke av for **Fast mottakspris** hvis **Lagermodell**-felteter satt til *Standardkost* eller *Glidende gjennomsnitt*.

4. Lukk siden.

Når du har aktivert alternativet **Fast mottakspris**, må du oppdatere lagerposteringsprofilen ved å følge disse trinnene.

1. Gå til **Lagerstyring \> Oppsett \> Postering \> Postering**.
1. Velg **Fortjeneste på fast mottakspris** i kolonnen **Velg** i kategorien **Bestilling**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.
1. Angi den nye raden, slik at den gjelder varemodellgruppen som du aktiverte fast mottaksprissetting for, og angi hovedkontoen som skal brukes til å registrere fast mottaksprisfortjeneste for bestillinger. Konfigurere andre innstillinger etter behov.
1. Velg **Tap på fast mottakspris** i kolonnen **Velg**. Legg til en ny rad som gjelder varemodellgruppen som du aktiverte fast mottaksprissetting for, og angi hovedkontoen som skal brukes til å registrere fast mottakspristap for bestillinger. Konfigurere andre innstillinger etter behov.
1. Velg **Motkonto for fast mottakspris** i kolonnen **Velg**. Legg til en ny rad som gjelder varemodellgruppen som du aktiverte fast mottaksprissetting for, og angi hovedkontoen som skal brukes til å registrere fast mottaksprisforskyvinger for bestillinger. Konfigurere andre innstillinger etter behov.
1. Velg **Fortjeneste på fast mottakspris** i kolonnen **Velg** i kategorien **Lager**. Legg til en ny rad som gjelder varemodellgruppen som du aktiverte fast mottaksprissetting for, og angi hovedkontoen som skal brukes til å registrere fast mottaksprisfortjeneste for lager. Konfigurere andre innstillinger etter behov.
1. Velg **Tap på fast mottakspris** i kolonnen **Velg**. Legg til en ny rad som gjelder varemodellgruppen som du aktiverte fast mottaksprissetting for, og angi hovedkontoen som skal brukes til å registrere fast mottakspristap for lager. Konfigurere andre innstillinger etter behov.

> [!NOTE]
> Vi anbefaler vanligvis at feltene **Fortjeneste på fast mottakspris** og **Tap på fast mottakspris** bruker den samme hovedkontoen for både bestillinger og lager.

> [!IMPORTANT]
> Når du endrer verdien i **Pris**-feltet i hurtigkategorien **Behandle kostnader** på siden **Frigitte produkter**, revaluerer ikke systemet automatisk lageret som er tilgjengelig. Som en manuell løsningn kan du åpne siden **Lukking og justering** og velge **Justering \> Beholdning** i handlingsruten. Deretter velger du varene som er tilgjengelige, og justerer dem til gjeldende pris. En klar fordel ved å bruke lagermodellen med standard kostpris, er at det fører til at systemet automatisk revaluerer lagerbeholdningen.
