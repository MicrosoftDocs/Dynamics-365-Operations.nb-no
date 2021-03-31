---
title: Feilstyring
description: Dette emnet beskriver feilstyring i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 43f996921ccac0b3c85ecea2460cb9e4614f8c04
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226815"
---
# <a name="fault-management"></a>Feilstyring

[!include [banner](../../includes/banner.md)]

 

I Aktivastyring kan du bruke feilutformingen til å definere feilsymptomer, feilområder og feiltyper på anleggsmiddeltyper. På denne måten kan du styre feil som oppdages i aktiva. I tillegg kan feilårsaker og forslag til reparasjon av feil registreres i en arbeidsordre.

Prosessen for feilregistrering og -styring består av disse trinnene.

1. Opprett en liste over feilsymptomer, feilområder og feiltyper som kan oppstå på anleggsmiddeltypene.
2. I feilutformingen definerer du symptomer, feilområder og feiltyper.

Her er noen eksempler som kan hjelpe deg med å forstå forskjellen mellom feilsymptomer, feilområder og feiltyper.

**Feilsymptomer:**

- Ubalanserte spenninger
- Kortslutning
- Støy
- Lekkasje
- Vibrasjoner

**Feilområder:**

- Elektrisk
- Mekanisk
- Hydraulisk
- Pneumatisk

**Feiltyper:**

- Feil i vikling av hovedstator
- Defekt diode
- Skitne viklinger
- Defekt generator
- Defekt sensor

## <a name="create-fault-symptoms"></a>Opprette feilsymptomer

Følg denne fremgangsmåten for å opprette en liste over symptomer som kan brukes i feilutformingen.

1. Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feilsymptomer**.
2. Velg **Ny** for å opprette en oppføring.
3. Skriv inn et navn på feilsymptomet i **Feilsymptom**-feltet.
4. Angi en beskrivelse i **Beskrivelse**-feltet.
5. Velg **Lagre**.

## <a name="create-fault-areas"></a>Opprette feilområder

Følg denne fremgangsmåten for å opprette en liste over områder eller steder som kan brukes i feilutformingen.

1. Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feilområder**.
2. Velg **Ny** for å opprette en oppføring.
3. Skriv inn et navn på feilområdet i **Feilområde**-feltet.
4. Angi en beskrivelse i **Beskrivelse**-feltet.
5. Velg **Lagre**.

## <a name="create-fault-types"></a>Opprette feiltyper

Følg denne fremgangsmåten for å opprette en liste over feiltyper som kan brukes i feilutformingen.

1. Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feiltyper**.
2. Velg **Ny** for å opprette en oppføring.
3. I **Feiltype**-feltet angir du et navn på feiltypen.
4. Angi en beskrivelse i **Beskrivelse**-feltet.
5. Velg **Lagre**.

## <a name="set-up-the-fault-designer"></a>Definere feilutformingen

I feilutformingen definerer du feildata for anleggsmiddeltyper.

1. Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feilutforming**.
2. I venstre rute velger du anleggsmiddeltypen du vil definere en feilpost for.
3. I hurtigfanen **Feil** velger du **Legg til linje**, og deretter velger du et feilsymptom i **Feilsymptom**-feltet.
4. I hurtigfanen **Feilområde** velger du **Legg til linje**, og deretter velger du et feilområde i **Feilområde**-feltet.
5. I hurtigfanen **Feiltype** velger du **Legg til linje**, og deretter velger du en feiltype i **Feiltype**-feltet.
6. Hvis du raskt vil opprette kombinasjoner av alle eksisterende feilsymptomer, områder og typer for den valgte anleggsmiddeltypen, velger du **Opprett feilkombinasjoner**. Denne funksjonen er nyttig hvis du har lagt til mange feilsymptomer, områder og typer. Det er enklere å slette linjene for kombinasjoner som ikke er relevante for anleggsmiddeltypen, enn å opprette nye linjer manuelt.

    > [!NOTE]
    > Hvis du vil kopiere oppsettet av feilsymptomer, områder og typer fra én anleggsmiddeltype til den valgte anleggsmiddeltypen, velger du **Kopier fra anleggsmiddeltype**.

7. Velg **Lagre** for å lagre endringene.

![Siden Feilutforming](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a>Opprette feilårsaker

Følg denne fremgangsmåten for å opprette en liste over kjente feilårsaker som kan legges til i en arbeidsordre eller en melding.

1. Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feilårsaker**.
2. Velg **Ny** for å opprette en oppføring.
3. I **Feilårsak**-feltet angir du et navn på feilårsaken.
4. Angi en beskrivelse i **Beskrivelse**-feltet.
5. Velg **Lagre**.

## <a name="create-fault-remedies"></a>Opprette feilløsninger

Følg denne fremgangsmåten for å opprette en liste over forslag til løsning og reparasjon som kan legges til i en arbeidsordre eller en melding.

1. Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feilløsninger**.
2. Velg **Ny** for å opprette en oppføring.
3. Skriv inn et navn på feilløsningen i **Feilløsning**-feltet.
4. Angi en beskrivelse i **Beskrivelse**-feltet.
5. Velg **Lagre**.

> [!NOTE]
> Du kan endre navnene på feilsymptomer, områder, typer, årsaker og løsninger etter behov. Navneendringene gjenspeiles automatisk i relaterte feilregistreringer.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]