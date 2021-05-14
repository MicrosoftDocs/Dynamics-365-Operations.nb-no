---
title: Utsatt behandling av manuell lagerbevegelse
description: Dette emnet beskriver hvordan du bruker utsatt behandling av manuelle lagerbevegelser i Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 04/27/2021
ms.topic: article
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: Mirzaab
ms.search.validFrom: 2021-04-27
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 54a202b7e6728bc83022851c901d3c5db17510bf
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956769"
---
# <a name="deferred-processing-of-manual-inventory-movement"></a>Utsatt behandling av manuell lagerbevegelse

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du bruker utsatt behandling av manuelle lagerbevegelser i Microsoft Dynamics 365 Supply Chain Management.

Den utsatte behandlingen lar lagerarbeidere fortsette å utføre annet arbeid mens plasseringsoperasjonen behandles i bakgrunnen. Utsatt behandling er nyttig når serveren kan ha tilfeldige eller ikke-planlagte økninger i behandlingstiden, og den økte behandlingstiden kan påvirke brukerens produktivitet. Arbeidstypen *Lagerbevegelse* er nå lagt til i settet med arbeidstyper som denne funksjonen støtter.

Bakgrunnsbehandling oppnås ved å bruke funksjonen [Funksjonen Behandle lagerapphendelser](warehouse-app-events.md).

## <a name="turn-on-this-feature-for-your-system"></a>Aktivere denne funksjonen for systemet

For å gjøre denne funksjonen tilgjengelig aktiverer du følgende funksjoner i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Du må aktivere dem i denne rekkefølgen:

1. Organisasjonsomfattende arbeidsblokkering
1. Behandle lagerapphendelser
1. Utsatte plasseringsoperasjoner
1. Utsatt behandling av manuell lagerbevegelsesoperasjon

## <a name="configure-the-work-processing-policies"></a>Konfigurere policyer for arbeidsbehandling

Hvis du vil bruke utsatt behandling, må du konfigurere og bruke en policy for arbeidsbehandling. [Funksjonen Utsatt behandling av lagerarbeid](deferred-put.md) støtter følgende arbeidstyper: *Salgsordre*, *Utsted overføringsordre* og *Etterfylling*. Funksjonene *Utsatt behandling av manuell lagerbevegelse* legger til en ny arbeidstype: *Lagerbevegelse*.

Følg denne fremgangsmåten for å definere en policy for arbeidsbehandling.

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsbehandlingspolicyer**.
1. Velg en eksisterende policy i listen, eller opprett en ny policy ved å velge **Ny** i handlingsruten. Hodet i hver policy har følgende felt:

    - **Navn på arbeidsbehandlingspolicy** – Navnet på arbeidsbehandlingspolicyen.
    - **Beskrivelse:** – En beskrivelse av arbeidsbehandlingspolicyen.

1. I hurtigkategorien **Behandlingsregler** angir du samlingen av regler som policyen skal gjelde for. Bruk knappene på verktøylinjen for å legge til og fjerne regler etter behov. For hver rad angir du feltene nedenfor:

    - **Arbeidsordretype** – Velg arbeidstypen som policyen gjelder for.
    - **Operasjon** – Velg operasjonen som policyen brukes til å behandle. Hvis du valgte *Lagerbevegelse* i **Arbeidsordretype**-feltet, trenger du ikke å angi dette feltet, fordi både plukkoperasjoner og plasserte operasjoner behandles som en enkelt hendelse.
    - **Arbeidsbehandlingsmetode** – Velg metoden som brukes til å behandle arbeidslinjen. Hvis du velger *Umiddelbar*, ligner virkemåten atferden når ingen arbeidsbehandlingspolicyer brukes til å behandle linjen. Hvis du velger *Utsatt*, bruker systemet utsatt behandling som bruker det satsvise rammeverket.
    - **Terskel for utsatt behandling** – Hvis du setter dette feltet til *0* (null), er det ingen terskel. I dette tilfellet brukes *Utsatt* behandlingsmetode hvis mulig. Hvis den spesifikke terskelberegningen er under terskelen, brukes metoden *Umiddelbar*. Ellers brukes *Utsatt*-metoden hvis mulig. For salgs- og overføringsrelatert arbeid beregnes terskelen som antall tilknyttede kildelastlinjer som behandles for arbeidet. For etterfyllingsarbeid beregnes terskelen som antall arbeidslinjer som etterfylles av arbeidet. Ved å angi en terskel på for eksempel *5* for salg sikrer du at mindre arbeid som har færre enn fem første kildelastlinjer, ikke bruker utsatt behandling, men større arbeide vil bruke den. Terskelen har bare en effekt hvis feltet **Arbeidsbehandlingsmetode** er satt til *Utsatt*.
    - **Satsvis gruppe for utsatt behandling** – Angi den satsvise gruppen som brukes til behandling. Hvis du valgte *Lagerbevegelse* i feltet **Arbeidsordretype**, trenger du ikke å definere dette feltet, fordi den satsvise gruppen er valgt i dialogboksen **Behandle lagerapphendelser**.

## <a name="assign-the-work-creation-policy"></a>Tilordne policyen for arbeidsopprettelse

Hvis du vil ha mer informasjon om hvordan du tilordner en policy for arbeidsopprettelse, kan du se [Utsatt behandling av lagerarbeid](deferred-put.md).

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Konfigurere en satsvis jobb for å behandle lagerapphendelser

Hvis du vil bruke prosessen *Utsatt behandling av manuell lagerbevegelse*, konfigurerer du en planlagt satsvis jobb.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Behandle lagerapphendelser**.
1. I dialogboksen **Behandle lagerapphendelser** i hurtigfanen **Kjør i bakgrunnen** setter du alternativet for **Satsvis behandling** til *Ja*.
1. Velg **Regelmessighet**, og definer en kjøreplan som oppfyller kravene i virksomheten.
1. Velg **OK** i hver dialogboks.

## <a name="inquire-about-the-warehouse-app-events"></a>Spørre om lagerapphendelser

Du kan vise hendelseskøen og hendelsesmeldingene som lagerappen genererer, ved å gå til **Lagerstyring \> Forespørsler og rapporter \> Logger for mobilenheter \> Lagerapphendelser**.

Hendelsesmeldingene for *Lagerbevegelse* vil få statusen *I kø* første gang de opprettes. Denne statusen angir at den satsvise jobben **Behandle lagerapphendelser** henter hendelsesmeldinger og behandler dem. Når statusen oppdateres til *Fullført*, slettes alle relaterte hendelser fra køen.

Alle *Lagerbevegelse*-hendelser samles under én samling per hendelsestype og lager.

Den satsvise jobben behandler lagerapphendelsene i henhold til gjentakelsen som er definert i dialogboksen **Behandle lagerapphendelser**. Så inntil en melding blir behandlet, kan du finne lager-IDen ved å se i **Identifikator**-feltet.

Detaljene i meldingen inneholder detaljene for flyttingen (for eksempel fra- og til-lokasjonene).

Hvis du vil ha mer informasjon, kan du se [Behandling av hendelse for lagerappen](warehouse-app-events.md).

## <a name="configure-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Konfigurere menyen på mobilenheten for å hoppe over den utsatte behandlingspolicyen

Hvis du vil ha mer informasjon om hvordan du konfigurerer mobilenhetsmenyen for å hoppe over den utsatte behandlingspolicyen, kan du se [Utsatt behandling av lagerarbeid](deferred-put.md).

## <a name="impact-on-closed-work-dates"></a>Innvirkning på lukkede arbeidsdatoer

Hvis du vil ha mer informasjon om innvirkningen på lukkede arbeidsdatoer, kan du se [Utsatt behandling av lagerarbeid](deferred-put.md).

## <a name="additional-resources"></a>Tilleggsressurser

- [Utsatt behandling av lagerarbeid](deferred-put.md)
- [Behandling av lagerapphendelse](warehouse-app-events.md)
- [Definere mobilenheter for lagerarbeid](configure-mobile-devices-warehouse.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
