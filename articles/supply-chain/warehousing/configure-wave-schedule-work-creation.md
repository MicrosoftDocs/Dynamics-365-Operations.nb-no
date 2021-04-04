---
title: Planlegge arbeidsopprettelse under bølge
description: Dette emnet beskriver hvordan du definerer og bruker bølgebehandlingsmetoden for planlegging av arbeidsopprettelse.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 36a450f78695f617056875f8d236fe46bc66aaaf
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501228"
---
# <a name="schedule-work-creation-during-wave"></a>Planlegge arbeidsopprettelse under bølge

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bruk funksjonen *Planlegg arbeidsopprettelse* som en del av bølgeprosessen for å øke bølgebehandlingsgjennomstrømming, ved å få systemet til å opprette arbeid ved hjelp av parallell behandling.

Når funksjonaliteten er aktivert, blir planlagt arbeid opprettet automatisk, som systemet til slutt behandler for å opprette faktisk arbeid. Hvis antall bølgelastlinjer når en forhåndsbestemt terskel, oppretter systemet faktisk arbeid raskere ved å bruke parallell, asynkron behandling.

## <a name="enable-the-schedule-work-creation-feature"></a>Aktivere funksjonen Planlegg arbeidsopprettelse

### <a name="enable-the-feature-in-feature-management"></a>Aktivere funksjonen i funksjonsbehandling

Før du kan bruke funksjonen *Planlegg arbeidsopprettelse*, må den være aktivert i systemet. Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Planlegg arbeidsopprettelse*

> [!NOTE]
> Funksjonen *Organisasjonsomfattende arbeidsblokkering* må være aktivert før du kan aktivere *Planlegg arbeidsopprettelse*.

### <a name="manually-enable-batch-processing-of-waves"></a>Aktivere satsvis behandling av bølger manuelt

For å kunne dra nytte av en parallell, asynkron metode for opprettelse av lagerarbeid må bølgeprosessen kjøre satsvis. Slik konfigurerer du dette:

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.

1. Angi *Ja* for **Behandle bølger satsvis** i **Generelt**-fanen. Du kan eventuelt også velge en dedikert **Satsvis gruppe for bølgebehandling** for å unngå at behandlingen av den satsvise køen kjører samtidig som andre prosesser.

1. Angi **Vent på lås (ms)**, som brukes når systemet behandler flere bølger samtidig. Det anbefales en verdi på *60000* for de fleste større bølgeprosessene.

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>Aktivere den nye bølgetrinnmetoden for eksisterende bølgemaler manuelt

Begynn med å opprette den nye bølgetrinnmetoden og aktivere den for parallell, asynkron oppgavebehandling.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgebehandlingsmetoder**.

1. Velg  **Generer metoder på nytt** og legg merke til at metoden *WHSScheduleWorkCreaveStepMethod* er lagt til i listen over bølgeprosessmetoder du kan bruke i forsendelsesbølgemalene.

1. Velg posten med **Metodenavn** *WHSScheduleWorkCreationWaveStepMethod*, og velg **Oppgavekonfigurasjon**.

1. Du kan legge til en ny rad i rutenettet ved å velg **Ny** i handlingsruten og bruke følgende innstillinger:

    - **Lager** – Velg lageret du vil bruke til behandling av planlegging av arbeidsopprettelse.

    - **Maksimalt antall satsvise oppgaver** – Angi et maksimalt antall satsvise oppgaver. Denne verdien skal i de fleste tilfeller være i området 8–16, men vi anbefaler at du eksperimenterer med den optimale innstillingen basert på scenarioene dine.

    - **Satsvis gruppe for bølgebehandling** – Velg en dedikert satsvis gruppe for bølgebehandling for å optimalisere behandlingen av den satsvise køen.

Du er nå klar til å oppdatere en eksisterende bølgemal (eller opprette en ny) for å bruke bølgebehandlingsmetoden *Planlegg arbeidsopprettelse*.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.

1. Velg **Rediger** i handlingsruten.

1. I listeruten velger du bølgemalen du vil oppdatere (hvis du tester ved hjelp av demonstrasjonsdata, kan du bruke *24 Standardforsendelse*).

1. Utvid hurtigfanen **Metoder**, og velg raden der **Navn** er *Planlegg arbeidsopprettelse* i rutenettet **Gjenstående metoder**.

1. Velg pilen som peker mot kolonnen **Valgte metoder** for å flytte den valgte raden til denne kolonnen. (Du kan bare ha én valgt metode om gangen som bruker enten *WHSScheduleWorkCreationWaveStepMethod* eller *createWork*, slik at den eksisterende raden der **Metodenavn** er *createWork*, flyttes automatisk til rutenettet **Gjenstående metoder**.)

## <a name="set-wave-task-processing-threshold-data"></a>Angi terskeldata for behandling av bølgeoppgave

Systemet oppretter standard terskeldata for behandling av bølgeoppgave første gang en bølgeprosess kjører ved hjelp av oppgavebasert behandling. Dataene brukes til å styre når bølgebehandling skal kjøre asynkront og være oppgavebasert, som gjør det mulig å behandle og opprette arbeid parallelt.

Standarddataene bruker først en terskelverdi på 15 for det minste antallet lastlinjer (MINIMUMWAVELOADLINES). Dette betyr at når systemet behandler en bølge med flere enn 15 lastlinjer, bruker det asynkron oppgavebehandling. Du kan sette inn / oppdatere disse dataene manuelt i tabellen **WHSWaveTaskProcessingThresholdParameters** i testmiljøet, men hvis du må endre denne innstillingen i et produksjonsmiljø, må du kontakte Microsoft Kundestøtte for å be om oppdateringen.

## <a name="work-with-the-feature"></a>Arbeide med funksjonen

Når funksjonen *Planlegg arbeidsopprettelse* er aktivert, oppretter bølgebehandling planlagt arbeid, som til slutt blir brukt av den nye prosessen for arbeidsopprettelse. Under arbeidsopprettelse blir arbeidet blokkert ved hjelp av funksjonen *Organisasjonsomfattende arbeidsblokkering*.

Følgende flytdiagram viser hvordan planlagt arbeid blir opprettet under bølgebehandling.

![Planlegg arbeidsoppretting](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Planlagt arbeid

Siden **Detaljer om planlagt arbeid** (**Lagerstyring \> Arbeid \> Detaljer om planlagt arbeid**) viser informasjon om det planlagte arbeidet, som opprinnelig ble opprettet under bølgebehandling. Følgende verdier for **Prosesstatus** er tilgjengelige:

- **Satt i kø** – Det planlagte arbeidet venter på å bli brukt til å opprette arbeid.
- **Fullført** – Det planlagte arbeidet har blitt brukt til å opprette arbeid.
- **Mislykket** – Bølgebehandlingen har mislyktes. Merk at det planlagte arbeidet kan være i tilstanden **Mislykket** med eller uten tilknyttet faktisk arbeid. Når den faktiske prosessen for arbeidsopprettelse mislykkes, forblir statusen for faktisk arbeid *Avbrutt*.

### <a name="batch-job-for-the-work-creation-process"></a>Satsvis jobb for prosessen for arbeidsopprettelse

Hvis du vil vise de satsvise jobbene for bølgebehandling, velger du **Satsvise jobber** i handlingsruten på **Alle bølger**-siden.

Her kan du vise alle detaljene om den satsvise oppgaven for hver ID for satsvis jobb.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]