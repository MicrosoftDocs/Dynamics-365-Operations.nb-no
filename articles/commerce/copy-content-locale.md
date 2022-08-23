---
title: Kopiere innhold til en annen nasjonal innstilling
description: Denne artikkelen beskriver hvordan du kopierer eksisterende innhold til en annen nasjonal innstilling innenfor et område i Microsoft Dynamics 365 Commerce-områdebyggeren.
author: josaw1
ms.date: 07/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 6afa871048bde22133ae083b8d56b6e99e49c401
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269268"
---
# <a name="copy-content-to-another-locale"></a>Kopiere innhold til en annen nasjonal innstilling

[!include[banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du kopierer eksisterende innhold til en annen nasjonal innstilling innenfor et område i Microsoft Dynamics 365 Commerce-områdebyggeren.

Når du oppretter innhold i Commerce-områdebyggeren, knyttes det alltid til en ID for nasjonal innstilling, for eksempel "en-us". Du kan kopiere enkeltsider og anleggsmidler til ulike nasjonale innstillinger innenfor det samme e-handelsområdet, ved å bytte mellom de nasjonale språk når du redigerer en innholdsvare og deretter oppretter en ny variant av varen. I noen tilfeller, for eksempel når du starter en helt ny nasjonal innstilling i butikken, er det fornuftig å duplisere alle innholdselementene fra en eksisterende nasjonal innstilling til den nye nasjonale innstillingen. Hvis den nye nasjonale innstillingen har samme basisspråk som én av de eksisterende nasjonale innstillingene, kan du bruke den eksisterende nasjonale innstillingen som kildeinnstillingen for kopieringsoperasjonen av den nasjonale innstillingen. (For eksempel vil de nasjonale språkinnstillingene for "en-us" og "en-au" begge bruke engelsk språk.) På denne måten kan du redusere den nødvendige innsatsen for å lokalisere innholdet i den nye nasjonale innstillingen.

Fremgangsmåtene nedenfor forklarer hvordan du legger til en ny nasjonal innstilling i en eksisterende kanal, kopierer alle innholdselementene fra en eksisterende nasjonal innstilling til en ny nasjonal innstilling og overvåker statusen til en kopieringsoperasjon for nasjonal innstilling.

## <a name="add-a-new-locale"></a>Legg til en ny nasjonal innstilling

Følg denne fremgangsmåten for å legge til en ny nasjonal innstilling i Commerce-områdebygger.

1. Gå til området i områdebyggeren.
1. I venstre navigasjonsrute velger du **Områdeinnstillinger**, og deretter velger du **Kanaler**.
1. Under **Kanal** velger du kanalen der du vil legge til den nye nasjonale innstillingen.
1. Velg **Legg til en nasjonal innstilling** i kanaldialogboksen som vises til høyre.
1. I dialogboksen **Legg til en nasjonal innstilling**, i feltet **Nasjonal innstilling som skal støttes**, velger du en nasjonal innstilling.
1. Bekreft at **Domene**-verdien er riktig.
1. Under **Bane** angir du en unik URL-bane (for **eksempel en-us** eller **english-us**).
1. Velg **OK**.
1. Lukk kanaldialogboksen.
1. Under **Kanal** bekrefter du at den nye nasjonale innstillingen vises ved siden av riktig kanal.
1. Velg **Lagre og publiser**.

> [!NOTE]
> Før den nye nasjonale innstillingen kan konfigureres i områdebyggeren, må den legges til i den tilknyttede nettbutikkanalen i Commerce headquarters.

## <a name="copy-all-content-items-to-a-new-locale"></a>Kopier alle innholdselementer til en ny nasjonal innstilling

Følg denne fremgangsmåten for å kopiere alle innholdselementer til en ny nasjonal innstilling i Commerce-områdebygger.

1. Gå til området i områdebyggeren.
1. I venstre navigasjonsrute velger du **Områdeinnstillinger**, og deretter velger du **Kanaler**.
1. Velg **Opprett kopi av nasjonal innstilling fra** på kommandolinjen.
1. I dialogboksen **Opprett kopi av nasjonal innstilling** som vises til høyre, under **Kildeområde**, bekrefter du at riktig område er valgt.
1. Velg kildekanalen i feltet **Kildekanal**.
1. Velg den samme kildekanalen i feltet **Målkanal**.
1. Velg den nasjonale kildeinnstillingen i feltet **Nasjonal kildeinnstilling**.
1. Velg den nye nasjonale innstillingen i feltet **Målets nasjonale innstilling**.
1. Velg **Kopier nasjonal innstilling**. En varsling bekrefter at kopieringen av den nasjonale innstillingen er startet.

> [!NOTE]
> Du kan også kopiere innhold mellom ulike kanaler.

## <a name="monitor-the-status-of-the-locale-copy"></a>Overvåk statusen til kopien av den nasjonale innstillingen

Følg denne fremgangsmåten hvis du vil overvåke statusen til en kopiering av en nasjonal innstilling.

1. Gå til området i områdebyggeren.
1. I venstre navigasjonsrute velger du **Områdeinnstillinger**, og deretter velger du **Jobber**.
1. Velg jobben du vil overvåke, under **Nåværende jobber**. Jobbdetaljene vises i dialogboksen som vises til høyre.
