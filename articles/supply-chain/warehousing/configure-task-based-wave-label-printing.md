---
title: Planlegge bølgeetikettutskrift under bølge
description: Dette emnet beskriver hvordan du definerer og bruker funksjonaliteten for oppgavebasert bølgeetikettutskrift.
author: MSFTGarm
ms.date: 06/09/2021
ms.topic: article
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-obaranov
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 4883f8a548645436e17b933d87d4ee6330570d48
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777871"
---
# <a name="schedule-wave-label-printing-during-wave"></a>Planlegge bølgeetikettutskrift under bølge

[!include [banner](../../includes/banner.md)]

Bruk funksjonen *Oppgavebasert bølgeetikettutskrift* som en del av bølgeetikettutskriften for å forbedre effektiviteten og for at systemet skal opprette bølgeetiketter og arbeide i separate oppgaver.

Prosessen med å konfigurere utskrift av bølgeetiketter er kompleks og er avhengig av nøyaktig konfigurasjon og hoveddata. Det er ikke så vanlig at genereringen av bølgeetikettposter mislykkes, og når den gjør det, rulles hele bølgebehandlingen tilbake. Ved hjelp av funksjonen for *Oppgavebasert bølgeetikettutskrift* slipper du å opprette arbeid og arbeidslinjer på nytt hver gang en bølgeetikett skrives ut feil.

Når du bruker funksjonen *Oppgavebasert bølgeetikettutskrift*, oppretter systemet først arbeid og arbeidslinjer. Deretter opprettes og skrives det ut bølgeetiketter. Til slutt, hvis bølgeetikettene er opprettet riktig, frigis arbeidet og bølgen for plukking.

## <a name="turn-on-the-task-based-wave-label-printing-feature-in-feature-management"></a>Slå på funksjonen for Oppgavebasert bølgeetikettutskrift i funksjonsbehandling

Hvis du vil bruke funksjonene som beskrives i dette emnet, må de være aktivert på systemet. Bruk arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere funksjonene i følgende rekkefølge:

1. *Bølgeetikettutskrift* – Denne funksjonen er nødvendig for å aktivere bølgeprosessmetoden for utskrift av bølgeetiketter.
1. *Organisasjonsomfattende arbeidsblokkering* – Denne funksjonen kreves for både manuell og automatisk konfigurasjon av planlagt arbeidsopprettelse. (Per Supply Chain Management versjon 10.0.21 er denne funksjonen obligatorisk, så den er aktivert som standard, og kan ikke deaktiveres igjen.)
1. *Oppgavebasert bølgeetikettutskrift* – Denne funksjonen kreves for å dele opp utskrift av bølgeetiketter til et separat transaksjonsområde.

## <a name="manually-enable-the-new-wave-step-method"></a>Aktivere den nye bølgetrinnmetoden manuelt

Du må først opprette den nye bølgetrinnmetoden og aktivere den for parallell, asynkron oppgavebehandling.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgebehandlingsmetoder**.
1. Velg **Generer metoder på nytt** i handlingsruten. Legg merke til at *waveLabelPrinting* legges til i listen over bølgeprosessmetoder som du kan bruke i forsendelsesbølgemaler.
1. Velg posten der feltet **Metodenavn** er satt til *waveLabelPrinting*, og velg deretter **Oppgavekonfigurasjon** i handlingsruten.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Lager** – Velg lageret du vil bruke til behandling av planlegging av arbeidsopprettelse. (Hvis du bruker demodata til testing, kan du velge lager *24*.)
    - **Maksimalt antall satsvise oppgaver** – Angi et maksimalt antall satsvise oppgaver. I de fleste tilfeller bør verdien være fra *8* til og med *16*. Vi anbefaler imidlertid at du eksperimenterer for å finne optimal innstillingen for scenariene.
    - **Satsvis gruppe for bølgebehandling** – Velg en dedikert satsvis gruppe for bølgebehandling for å optimalisere behandlingen av den satsvise køen.

Du kan nå oppdatere en eksisterende bølgemal, slik at den bruker bølgebehandlingsmetoden *Bølgeetikettutskrift*. Du kan også opprette en ny bølgemal som bruker den.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.
1. I handlingsruten velger du **Rediger**.
1. Velg bølgemalen du vil oppdatere, i listeruten. (Hvis du bruker demodata til testing, kan du velge *24 Standardforsendelse*.)
1. I hurtigfanen **Metoder** i kolonnen **Gjenværende metoder** velger du raden der feltet **Navn** er satt til *waveLabelPrinting*.
1. Velg **legg til** (pil høyre-knapp) for å flytte den valgte raden til kolonnen **Valgte metoder**.
1. I feltet **Bølgetrinnkode** angir du en bølgetrinnkode som skal brukes til å koble bølgemalen til en bølgeetikettmal.

## <a name="set-wave-task-processing-threshold-data"></a>Angi terskeldata for behandling av bølgeoppgave

Systemet oppretter standard terskeldata for behandling av bølgeoppgave første gang en bølgeprosess kjører ved hjelp av oppgavebasert behandling. Disse dataene brukes til å styre om bølgebehandling skal kjøre asynkront og være oppgavebasert, slik at den kan behandle og opprette bølgeetiketter parallelt.

Standarddataene bruker først en terskelverdi på *1* for det minste antallet arbeids-IDer (`MinimumWorkThresholdForLabelPrinting`). Når systemet behandler en bølge som har mer enn én arbeids-ID, vil det derfor bruke oppgavebasert behandling av bølgeetiketter i en separat transaksjon. Du kan sette inn eller oppdatere disse dataene manuelt i `WHSWaveTaskProcessingThresholdParameters`-tabellen i testmiljøene. Hvis du vil endre denne innstillingen i et produksjonsmiljø, må du kontakte Microsoft Kundestøtte for å be om oppdateringen.

## <a name="changes-to-the-wave-processing-logic-when-task-based-wave-label-printing-is-used"></a>Endringer i bølgebehandlingslogikken når oppgavebasert bølgeetikettutskrift brukes

Hvis behandling av bølgeetiketter overskrider behandlingsterskelen for bølgeoppgave, startes oppgavebasert behandling. I den neste bølgebehandlingen som passer til bølgemalen, vil utskrift av bølgeetiketter kjøres i en frittstående *ttsbegin*/*ttscommit*-transaksjon rett etter at arbeidet er opprettet. Hvis arbeidsfrigivelse (opphevelse av blokkering) konfigureres på bølgemalen til å kjøres automatisk, skjer den bare etter at utskrift av bølgeetiketter er fullført.

Hvis generering av bølgeetiketter mislykkes (for eksempel hvis konvertering av arbeidsantallet til bølgeetikettantallet mislykkes og feilen oppstår), mislykkes bare den aktuelle transaksjonen. Arbeidet som ble opprettet tidligere, blir frosset. Følg denne fremgangsmåten for å rette feil og skrive ut bølgeetikettene.

1. Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Velg den relevante bølgen i rutenettet.
1. I handlingsruten, i fanen **Bølge** i **Skriv ut**-gruppen, velger du **Bølgeetiketter**.
1. Følg instruksjonene på skjermen for å sende etikettene til utskrift.
1. I **Bølge**-fanen i handlingsruten i **Bølge**-gruppen, velger du **Frigi** for å frigi arbeid for den valgte bølgen manuelt.

## <a name="additional-resources"></a>Tilleggsressurser

- [Bølgeetikettutskrift](configure-wave-label-printing.md)
- [Planlegge oppretting av arbeidstid under bølge](configure-wave-schedule-work-creation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
