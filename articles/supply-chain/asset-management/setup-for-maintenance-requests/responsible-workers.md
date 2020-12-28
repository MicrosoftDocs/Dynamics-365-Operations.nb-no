---
title: Ansvarlige vedlikeholdsarbeidere
description: Dette emnet forklarer hvordan du ansvarlige vedlikeholdspersoner i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 113ee2b45c569c7dae3609f1027e31c4e5e5c54a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434518"
---
# <a name="responsible-maintenance-workers"></a>Ansvarlige vedlikeholdsarbeidere

[!include [banner](../../includes/banner.md)]

 

Ansvarlige vedlikeholdsarbeidere kan være relatert til aktivatyper, aktiva, arbeidssteder, kategorier for vedlikeholdsjobbtype, vedlikeholdsjobbtyper, varianter av vedlikeholdsjobbtype og fag. De kan brukes på arbeidsordrer og vedlikeholdsanmodninger for å angi en preferanse om vedlikeholdsarbeiderne som skal være ansvarlig for en arbeidsordre. (Disse vedlikeholdsarbeiderne er imidlertid ikke nødvendigvis de samme arbeiderne som er planlagt å utføre arbeidsordren.) Bruk av denne funksjonen er valgfritt. Den kan for eksempel brukes til å velge ansvarlige arbeidere eller arbeidergrupper for bestemte arbeidstyper eller arbeidsområder.

Under et livsløp for en arbeidsordre eller et livsløp for en vedlikeholdsanmodning kan ansvarlige vedlikeholdsarbeidere endres eller oppdateres. Denne endringen eller oppdateringen kan for eksempel være knyttet til en endring i livsløpstilstanden for vedlikeholdsanmodninger eller livsløpstilstanden for arbeidsordren.

Oppsettet på siden **Ansvarlige vedlikeholdsarbeidere** brukes *ikke* under planlegging av arbeidsordre.

> [!NOTE]
> I Aktivastyring kan du også definere *foretrukne* vedlikeholdsarbeidere som kan tildeles arbeidsordrer under planlegging av arbeidsordrer.

Før du kan definere ansvarlige vedlikeholdsarbeidere, må du definere arbeidere og vedlikeholdsarbeidergrupper som skal være tilgjengelige for valg. (Hvis du vil ha informasjon om hvordan du definerer arbeidere og grupper med vedlikeholdspersoner, kan du se [Vedlikeholdspersoner og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md).)

## <a name="set-up-responsible-maintenance-workers"></a>Definer ansvarlige vedlikeholdspersoner

1. Velg **Aktivastyring** \> **Oppsett** \> **Arbeidere** \> **Ansvarlige vedlikeholdsarbeidere**.
2. Velg **Ny** for å opprette en oppføring.
3. Opprett først en standard ansvarlig vedlikeholdsarbeider eller et gruppeoppsett for ansvarlig vedlikeholdsarbeider, der du angir bare feltet **Ansvarlig vedlikeholdspersongruppe** og/eller feltet **Ansvarlig arbeider**. La de resterende feltene stå tomme. Dette standardoppsettet vil bli brukt ved arbeidsordreplanlegging hvis ingen annen, mer spesifikk kombinasjon samsvarer med innholdet i arbeidsordren.

    > [!NOTE]
    > Under opprettelsen av en vedlikeholdsanmodning, når en ansvarlig vedlikeholdsarbeider eller ansvarlig vedlikeholdsarbeidergruppe er gjort tilgjengelig for valg på siden **Alle vedlikeholdsanmodninger**, går Aktivastyring gjennom alle ansvarlige vedlikeholdsarbeiderposter for å se etter et mulig samsvar. Den kontrollerer alltid den mest spesifikke kombinasjonen først. Med andre ord ser Aktivastyring først etter et treff i **Fag**-feltet. Hvis det ikke blir funnet noe treff, kontrolleres det for et treff i feltet **Variant av vedlikeholdsjobbtype**. Hvis det ikke blir funnet noe treff, kontrolleres det for et treff i **Vedlikeholdsjobbtype**-feltet, og så videre. Som du kan se i oppsettet av siden, betyr dette at, for å finne den mest spesifikke kombinasjonen, kontrollerer Aktivastyring hver post fra høyre til venstre for et treff (først **Fag**, deretter **Variant av vedlikeholdsjobbtype**, deretter **Vedlikeholdsjobbtype**, deretter **Kategori av vedlikeholdsjobbtype**, deretter **Arbeidssted**, deretter **Aktiva** og til slutt **Aktivatype**). Hvis det ikke blir funnet noen treff, brukes standardoppføringen, der det ikke er noen valg i disse sju feltene.

Illustrasjonen nedenfor viser et eksempel på siden **Ansarlige vedlikeholdsarbeidere**.

![Siden Ansvarlige vedlikeholdsarbeidere](media/08-setup-for-requests.png)
