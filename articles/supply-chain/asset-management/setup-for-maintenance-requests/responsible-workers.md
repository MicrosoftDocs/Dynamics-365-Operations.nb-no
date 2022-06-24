---
title: Ansvarlige vedlikeholdspersoner
description: Denne artikkelen forklarer hvordan du definerer ansvarlige vedlikeholdspersoner i Aktivastyring.
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9535be3161253e88083b5add7ac55c12364aa383
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875599"
---
# <a name="responsible-maintenance-workers"></a>Ansvarlige vedlikeholdspersoner

[!include [banner](../../includes/banner.md)]

 

Ansvarlige vedlikeholdspersoner kan være relatert til aktivatyper, aktiva, arbeidssteder, kategorier for vedlikeholdsjobbtype, vedlikeholdsjobbtyper, varianter av vedlikeholdsjobbtype og fag. De kan brukes på arbeidsordrer og meldinger for å angi en preferanse om vedlikeholdspersonene som skal være ansvarlig for en arbeidsordre. (Disse vedlikeholdspersonene er imidlertid ikke nødvendigvis de samme arbeiderne som er planlagt å utføre arbeidsordren.) Bruk av denne funksjonen er valgfritt. Den kan for eksempel brukes til å velge ansvarlige arbeidere eller arbeidergrupper for bestemte arbeidstyper eller arbeidsområder.

Under et livsløp for en arbeidsordre eller et livsløp for en melding kan ansvarlige vedlikeholdspersoner endres eller oppdateres. Denne endringen eller oppdateringen kan for eksempel være knyttet til en endring i livssyklustilstanden for meldinger eller livssyklustilstanden for arbeidsordren.

Oppsettet på siden **Ansvarlige vedlikeholdspersoner** brukes *ikke* under planlegging av arbeidsordre.

> [!NOTE]
> I Aktivastyring kan du også definere *foretrukne* vedlikeholdspersoner som kan tildeles arbeidsordrer under planlegging av arbeidsordrer.

Før du kan definere ansvarlige vedlikeholdspersoner, må du definere arbeidere og vedlikeholdspersongrupper som skal være tilgjengelige for valg. (Hvis du vil ha informasjon om hvordan du definerer arbeidere og grupper med vedlikeholdspersoner, kan du se [Vedlikeholdspersoner og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md).)

## <a name="set-up-responsible-maintenance-workers"></a>Definer ansvarlige vedlikeholdspersoner

1. Velg **Aktivastyring** \> **Oppsett** \> **Arbeidere** \> **Ansvarlige vedlikeholdspersoner**.
2. Velg **Ny** for å opprette en oppføring.
3. Opprett først en standard ansvarlig vedlikeholdsperson eller et gruppeoppsett for ansvarlig vedlikeholdsperson, der du angir bare feltet **Ansvarlig vedlikeholdspersongruppe** og/eller feltet **Ansvarlig arbeider**. La de resterende feltene stå tomme. Dette standardoppsettet vil bli brukt ved arbeidsordreplanlegging hvis ingen annen, mer spesifikk kombinasjon samsvarer med innholdet i arbeidsordren.

    > [!NOTE]
    > Under opprettelsen av en melding, når en ansvarlig vedlikeholdsperson eller ansvarlig vedlikeholdspersongruppe er gjort tilgjengelig for valg på siden **Alle meldinger**, går Aktivastyring gjennom alle ansvarlige vedlikeholdspersonposter for å se etter et mulig samsvar. Den kontrollerer alltid den mest spesifikke kombinasjonen først. Med andre ord ser Aktivastyring først etter et treff i **Fag**-feltet. Hvis det ikke blir funnet noe treff, kontrolleres det for et treff i feltet **Variant av vedlikeholdsjobbtype**. Hvis det ikke blir funnet noe treff, kontrolleres det for et treff i **Vedlikeholdsjobbtype**-feltet, og så videre. Som du kan se i oppsettet av siden, betyr dette at, for å finne den mest spesifikke kombinasjonen, kontrollerer Aktivastyring hver post fra høyre til venstre for et treff (først **Fag**, deretter **Variant av vedlikeholdsjobbtype**, deretter **Vedlikeholdsjobbtype**, deretter **Kategori av vedlikeholdsjobbtype**, deretter **Arbeidssted**, deretter **Aktiva** og til slutt **Aktivatype**). Hvis det ikke blir funnet noen treff, brukes standardoppføringen, der det ikke er noen valg i disse sju feltene.

Illustrasjonen nedenfor viser et eksempel på siden **Ansarlige vedlikeholdspersoner**.

![Siden Ansvarlige vedlikeholdspersoner.](media/08-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]