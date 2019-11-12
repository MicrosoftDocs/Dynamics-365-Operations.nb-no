---
title: Stykklister for aktiva
description: Dette emnet beskriver stykklister for aktiva i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 02686c97a19fa86c3ea93d7c400067f0855b5c4d
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571490"
---
# <a name="asset-boms"></a>Stykklister for aktiva

[!include [banner](../../includes/banner.md)]

 

Dette emnet beskriver stykklister for aktiva i Aktivastyring. Siden **Stykklister for aktiva** viser en liste over alle varer (reservedeler og andre varer) som brukes på et aktivum i løpet av hele levetiden. Når du oppretter et nytt aktivum, bør du vurdere å definere en stykkliste for aktiva som en del av installasjonsprosedyren. På denne måten kan du spore vareloggen for aktivaet fra opprettelsesdatoen.

Når du har fullført en vedlikeholdsjobb, og vareforbruket er registrert på en arbeidsordre, kan du spore forbruk av reservedeler og andre varer som brukes på aktivumet. Med denne funksjonen kan du beholde en fullstendig vareforbrukspost for alle ressursene dine. Du kan for eksempel bruke posten til å overvåke om en bestemt reservedel ofte erstattes, eller til å holde rede på reservedelene eller andre elementer som for øyeblikket brukes på et anleggsmiddel.

> [!NOTE]
> På en Arbeidsordre kan vareforbruk inkludere både reservedeler og andre tilleggsvarer, for eksempel smøremidler, bolter og pakninger.

En STYKKLISTE for aktiva kan oppdateres automatisk basert på oppsettet i Asset Management. Hvis en livsløpstilstand for arbeidsordre er opprettet for å håndtere fullførte arbeidsordrer, og hvis alternativet **Oppdater stykkliste for aktiva** er satt til **Ja** på siden **Livsløpstilstander for arbeidsordre**, oppdateres alle varer som brukes i arbeidsordren, automatisk på siden **Stykkliste for aktiva** når arbeidsordren oppdateres til denne livsløpstilstanden. 


Du kan også oppdatere en stykkliste for aktiva manuelt ved å opprette nye varelinjer på siden **Stykkliste for aktiva**.

På siden **Stykkliste for aktiva** kan du spore historikk for reservedeler for aktiva etter at vareforbruk er registrert på en arbeidsordre. Hvis du vil bruke denne funksjonaliteten, må du velge varegruppene som skal brukes til reservedelsregistrering på siden **Varegrupper for reservedeler**.

Hvis du vil bruke funksjonaliteten for stykkliste for aktiva, må du først definere de nødvendige varegruppene for reservedeler. Hvis du vil at stykklisten for aktiva skal oppdateres automatisk når en arbeidsordre er fullført, kan du definere en livsløpstilstand for arbeidsordre for å håndtere denne oppdateringen. 


## <a name="set-up-spare-parts-item-groups"></a>Definere varegrupper for reservedeler

Oppsettet av reservedelsloggen er basert på varegrupper som er opprettet i modulen **Lagerstyring**. I Aktivastyring definerer du varegrupper slik at du kan spore historikk for reservedeler for varene i de valgte varegruppene.

1. Velg **Aktivastyring** \> **Oppsett** \> **Aktivum** \> **Varegrupper for reservedeler**.
2. Velg **Ny** for å definere en varegruppe.
3. Velg gruppen i **Varegruppe**-feltet. Navnet på gruppen angis automatisk i **Navn**-feltet.

## <a name="view-and-update-asset-boms"></a>Vis og oppdater stykklister for aktiva

Når du bokfører vareforbruk på en arbeidsordre, kan du vise det registrerte vareforbruket på siden **Stykkliste for aktiva**.

1. Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Aktive aktiva**. Velg aktivumet i listen, og velg **Stykkliste for aktiva**.

    > [!NOTE]
    > Hvis du vil vise alle vareforbruksregistreringer på alle aktiva, velger du **Aktivastyring** \> **Forespørsler** \> **Aktiva** \> **Stykkliste for aktiva**.

2. Velg **Oppdater stykkliste for aktiva**. Du kan legge til aktiva, aktivatyper og ressurser i oppdateringen etter behov ved å velge **Velg.** Velg **OK** for å starte oppdateringen. Du kan også definere oppdateringsfunksjonen som en satsvis jobb.
3. Hvis du vil se mer informasjon som er knyttet til varene, kan du legge til lagerdimensjoner. Velg **Beholdning** \> **Dimensjonsvisning**, og merk deretter av i boksene for dimensjonene du vil se. Hvis du vil beholde dette oppsettet for alle aktiva på siden **Stykkliste for aktiva**, setter du **Lagre oppsett** til **Ja**.
4. Hvis du vil ha en oversikt over hvor i Aktivastyring varen på den valgte linjen brukes, i forhold til aktiva, jobbtype standarder, reservedeler og arbeidsordrer, velger du **Vare der brukt**. 
5. Hvis du bare vil se aktive varelinjer, velger du **Vis** \> **Gjeldende**. Hvis du vil se alle varelinjer, inkludert linjer der utløpsdatoen er tidligere enn gjeldende dato, velger du **Vis** \> **Alle**.

> [!NOTE]
> Når du har fullført en arbeidsordre, og hvis noen varer eller reservedeler som er relatert til det relaterte aktivumet er utløpt eller har blitt erstattet av andre varer eller reservedeler, anbefaler vi at du oppdaterer stykklisten for aktiva tilsvarende.

## <a name="create-a-new-item-line-in-an-asset-bom"></a>Opprette en ny varelinje i en stykkliste for aktiva

Du kan opprette varelinjer manuelt for aktiva.

1. Velg **Ny** på siden **Stykkliste for aktiva**.
2. Velg aktivaet du vil legge til en varelinje for, i **Aktivum**-feltet.
3. Angi et sekvensielt linjenummer i feltet **Linjenummer**.
4. I **Gyldig**-feltet angir du en startdato for varen.
5. Hvis varen utløper, angir du en sluttdato i **Utløp**-feltet.
6. Velg varen i **Varenummer**-feltet. Navnet angis automatisk i **Produktnavn**-feltet.
7. Angi antallet som brukes, i **Antall**-feltet. **Enhet**-feltet oppdateres automatisk.
