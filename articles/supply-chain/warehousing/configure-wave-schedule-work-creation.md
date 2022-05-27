---
title: Planlegge arbeidsopprettelse under bølge
description: Dette emnet beskriver hvordan du definerer og bruker bølgebehandlingsmetoden for planlegging av arbeidsopprettelse.
author: Mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c955e7275c0bdc12dc206dde1d7e390f16270148
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691138"
---
# <a name="schedule-work-creation-during-wave"></a>Planlegge arbeidsopprettelse under bølge

[!include [banner](../../includes/banner.md)]

Bruk funksjonen *Planlegg arbeidsopprettelse* som en del av bølgeprosessen for å øke bølgebehandlingsgjennomstrømming, ved å få systemet til å opprette arbeid ved hjelp av parallell behandling.

Når funksjonaliteten er aktivert, blir planlagt arbeid opprettet automatisk, som systemet til slutt behandler for å opprette faktisk arbeid. Hvis antall bølgelastlinjer når en forhåndsbestemt terskel, oppretter systemet faktisk arbeid raskere ved å bruke parallell, asynkron behandling.

## <a name="turn-on-the-scheduled-work-creation-features-in-feature-management"></a>Slå på funksjonene for planlagte arbeidsopprettelse i funksjonsadministrasjon

Hvis du vil bruke funksjonene som beskrives i dette emnet, må de være aktivert på systemet. Bruk arbeidsområdet [Funksjonsadministrering](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktiverer du følgende funksjoner i følgende rekkefølge:

1. **Organisasjonsomfattende arbeidsblokkering** – Kreves for både manuell og automatisk konfigurasjon av planlagt arbeidsopprettelse. (Per Supply Chain Management versjon 10.0.21 er denne funksjonen obligatorisk, så den er aktivert som standard, og kan ikke deaktiveres igjen.)
1. **Planlegg arbeidsopprettelse** – Kreves for både manuell og automatisk konfigurasjon av planlagt arbeidsopprettelse.
1. **Organisasjonsomfattende "Planlegg arbeidsopprettelse"-bølgemetode** – Kreves for både manuell og automatisk konfigurasjon av planlagt arbeidsopprettelse. Du trenger ikke denne funksjonen hvis du bare vil bruke manuell konfigurasjon.

<a name="Auto-enable-schedule-work-creation"></a>

## <a name="automatically-configure-scheduled-work-creation"></a>Konfigurer planlagt arbeidsopprettelse automatisk

Hvis du aktiverer funksjonen *Organisasjonsomfattende "Planlegg arbeidsopprettelse"-bølgemetode*, skjer følgende automatisk på systemet:

- Bølgemetoden *Planlegg arbeidsopprettelse* (`WHSScheduleWorkCreationWaveStepMethod`) legges til og konfigureres til å kjøre parallelt på tvers av alle juridiske enheter.
- Bølgemaler fra alle juridiske enheter der **Bølgemaltype** er angitt til *Forsendelse* og **Malstatus** er angitt til *Gyldig*, vil få *Opprett arbeid*-metoden erstattet av metoden *Planlegg arbeidsopprettelse*. Bølgemaler fra juridiske enheter der metoden *Opprett arbeid* kan gjentas, vil imidlertid ikke bli endret.
- Oppgavekonfigurasjoner for metoden *Planlegg arbeidsopprettelse* opprettes for alle lagre fra alle juridiske enheter der **Bruk lagerstyringsprosesser** er aktivert. Dette betyr at metoden *Planlegg arbeidsopprettelse* nå vil bli kjørt parallelt som standard. Eksisterende lagre der du endrer **Bruk lagerstyringsprosesser** fra *Nei* til *Ja*, vil også kjøre denne denne metoden parallelt som standard.
- Alle juridiske enheter behandler bølger satsvis, og **Vent på lås (ms)** blir satt til en standardverdi på *60 000* ms hvis den tidligere var satt til *0* ms.
- Alle de nye bølgemalene du oppretter, vil ha bølgemetoden *Planlegg arbeidsopprettelse* i stedet for *Opprett arbeid*-metoden.

De eksisterende konfigurasjonene for oppgave- og bølgebehandling vil også bli beholdt for alle juridiske enheter som allerede er konfigurert til å behandle bølger i partier, og for alle lagre som allerede er konfigurert til å bruke metoden *Planlegg arbeidsopprettelse* parallelt.

Om nødvendig kan du manuelt tilbakestille noen av eller alle innstillingene som ble gjort automatisk da du aktiverte funksjonen *Organisasjonsomfattende "Planlegg arbeidsopprettelse"-bølgemetode* ved å gjøre følgende:

- For bølgemaler går du til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**. Erstatt metoden *Planlegg arbeidsopprettelse* med *Opprett arbeid*.
- For lagerparametere går du til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**. På **Bølgebehandling**-fanen bruker du de foretrukne verdiene for **Behandle bølger satsvis** og **Vent på lås (ms)**.
- For bølgemetodene går du til **Lagerstyring \> Oppsett \> Bølger \> Bølgebehandlingsmetoder**. Velg `WHSScheduleWorkCreationWaveStepMethod`, og velg **Oppgavekonfigurasjon** i handlingsruten. Endre eller slett antall satsvise oppgaver og den tilordnede bølgegruppen for hvert oppførte lager etter behov.

## <a name="manually-configure-scheduled-work-creation"></a>Konfigurer planlagt arbeidsopprettelse manuelt

Hvis du ikke aktiverte [funksjonen *Organisasjonsomfattende "Planlegg arbeidsopprettelse"-bølgemetode*](#Auto-enable-schedule-work-creation), kan du bruke fremgangsmåtene i denne delen for å konfigurere planlagt arbeidsopprettelse manuelt etter behov.

### <a name="manually-enable-batch-processing-of-waves"></a>Aktivere satsvis behandling av bølger manuelt

For å kunne dra nytte av en parallell, asynkron metode for opprettelse av lagerarbeid må bølgeprosessen kjøre satsvis. Slik konfigurerer du dette:

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.
1. Angi *Ja* for **Behandle bølger satsvis** i **Generelt**-fanen. Du kan eventuelt også velge en dedikert **Satsvis gruppe for bølgebehandling** for å unngå at behandlingen av den satsvise køen kjører samtidig som andre prosesser.
1. Angi **Vent på lås (ms)**, som brukes når systemet behandler flere bølger samtidig. Det anbefales en verdi på *60000* for de fleste større bølgeprosessene.

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>Aktivere den nye bølgetrinnmetoden for eksisterende bølgemaler manuelt

Begynn med å opprette den nye bølgetrinnmetoden og aktivere den for parallell, asynkron oppgavebehandling.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgebehandlingsmetoder**.
1. Velg **Generer metoder på nytt** og legg merke til at metoden *WHSScheduleWorkCreationWaveStepMethod* er lagt til i listen over bølgeprosessmetoder du kan bruke i forsendelsesbølgemalene.
1. Velg posten med **Metodenavn** *WHSScheduleWorkCreationWaveStepMethod*, og velg **Oppgavekonfigurasjon**.
1. Du kan legge til en ny rad i rutenettet ved å velg **Ny** i handlingsruten og bruke følgende innstillinger:

    - **Lager** – Velg lageret du vil bruke til behandling av planlegging av arbeidsopprettelse.
    - **Maksimalt antall satsvise oppgaver** – Angi et maksimalt antall satsvise oppgaver. Denne verdien skal i de fleste tilfeller være i området 8–16, men vi anbefaler at du eksperimenterer med den optimale innstillingen basert på scenarioene dine.
    - **Satsvis gruppe for bølgebehandling** – Velg en dedikert satsvis gruppe for bølgebehandling for å optimalisere behandlingen av den satsvise køen.

Du er nå klar til å oppdatere en eksisterende bølgemal (eller opprette en ny) for å bruke bølgebehandlingsmetoden *Planlegg arbeidsopprettelse*.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.
1. Velg **Rediger** i handlingsruten.
1. I listeruten velger du bølgemalen du vil oppdatere (hvis du tester ved hjelp av demonstrasjonsdata, kan du bruke *24 Standardforsendelse*).
1. Utvid hurtigfanen **Metoder**, og velg raden der **Navn** er *Planlegg arbeidsopprettelse* i rutenettet **Gjenstående metoder**.
1. Velg pilen som peker mot kolonnen **Valgte metoder** for å flytte den valgte raden til denne kolonnen. (Du kan bare ha én valgt metode om gangen som bruker enten `WHSScheduleWorkCreationWaveStepMethod` eller `createWork`, slik at den eksisterende raden der **Metodenavn** er `createWork`, flyttes automatisk til rutenettet **Gjenstående metoder**.)

## <a name="set-wave-task-processing-threshold-data"></a>Angi terskeldata for behandling av bølgeoppgave

Systemet oppretter standard terskeldata for behandling av bølgeoppgave første gang en bølgeprosess kjører ved hjelp av oppgavebasert behandling. Dataene brukes til å styre når bølgebehandling skal kjøre asynkront og være oppgavebasert, som gjør det mulig å behandle og opprette arbeid parallelt.

Standarddataene bruker først en terskelverdi på 15 for det minste antallet lastlinjer (`MINIMUMWAVELOADLINES`). Dette betyr at når systemet behandler en bølge med flere enn 15 lastlinjer, bruker det asynkron oppgavebehandling. Du kan sette inn / oppdatere disse dataene manuelt i `WHSWaveTaskProcessingThresholdParameters`-tabellen i testmiljøene. Hvis du må endre denne innstillingen i et produksjonsmiljø, må du kontakte Microsoft Kundestøtte for å be om oppdateringen.

## <a name="work-with-the-scheduled-work-creation"></a>Arbeide med opprettingen av planlagt arbeid

Hvis du vil ha mer informasjon om hvordan du arbeider med planlagt arbeidsopprettelse, kan du se [Bølgeoppretting og -behandling](wave-processing.md). 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
