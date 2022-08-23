---
title: Definere og kjøre behandling for å kalle et enkelt ER-format for å generere en Excel-rapport
description: Denne artikkelen inneholder et eksempel som viser hvordan du definerer og bruker elektroniske meldinger.
author: AdamTrukawka
ms.date: 07/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.custom: ''
ms.search.form: ''
ms.openlocfilehash: 6090c45a98b672f718f89fc1d2e1c060498bb8a0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279344"
---
# <a name="set-up-and-run-processing-to-call-a-simple-exporting-er-format-to-generate-an-excel-report"></a>Definere og kjøre behandling for å kalle et enkelt ER-format for å generere en Excel-rapport

[!include [banner](../includes/banner.md)]

Når du har opprettet ER-formatet, tilordnet det til datakilder og fullført det, kan du kjøre det fra arbeidsområdet **Elektronisk rapportering**. Etter at en rapport genereres, kan du lagre den lokalt.

For å kontrollere følgende aspekter av rapporteringsprosessen, må du definere behandling av elektroniske meldinger:

- Logginformasjon om hvem som genererte rapporten.
- Logginformasjon om når rapporten ble generert.
- Lagre rapportene som er generert for tidligere perioder.

Følgende eksempel viser hvordan du kan definere elektroniske meldinger for å generere en rapport som er basert på et ER-eksportformat for Microsoft Excel. Hvis du vil følge dette eksemplet, må ER Excel-eksportformatet allerede være opprettet, tilordnet datakilder og fullført. I tillegg må en nummerserie allerede være definert for elektroniske meldinger.

Når du bygger behandling, er det nyttig hvis du først definerer behandlingshandlingene og -statuser som skal opprettes. Illustrasjonen nedenfor viser hvordan behandlingen ser ut i dette eksemplet.

![Oppsett for behandling](media/processing-scheme.png)

## <a name="create-message-statuses"></a>Opprette meldingsstatuser

1. Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Meldingsstatuser**.
2. Opprett følgende meldingsstatuser:

    - Nytt
    - Forberedt
    - Generert

    ![Meldingsstatuser](media/message-statuses.png)

3. På linjen for **Ny**-status merker du av for **Tillat sletting** for å la brukere slette meldinger som har denne statusen.

## <a name="create-additional-fields"></a>Opprette tilleggsfelt

1. Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Tilleggsfelt**.
2. Legge til et ekstra felt og tilhørende verdier.
3. Sett alternativet **Brukerredigering** til **Ja**, slik at brukere kan redigere feltet.

![Tilleggsfelt](media/additional-fields.png)

## <a name="create-message-processing-actions"></a>Opprette meldingsbehandlingshandlinger

I dette eksemplet oppretter du følgende meldingsbehandlingshandlinger:

- **Opprett melding**
- **Oppdater til Klargjort**
- **Generer rapport**
- **Oppdater til innledende status** (valgfritt)

Følg trinnene nedenfor for å opprette handlingene.

1. Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Handlinger for meldingsbehandling**.
2. Opprett en handling som heter **Opprett melding**. På hurtigfanen **Generelt** i feltet **Handlingstype** velger du **Opprett melding**.
3. Opprett en handling som heter **Oppdater til Klargjort**, og angi følgende felt:

    - På hurtigfanen **Generelt** i feltet **Handlingstype** velger du **Behandling av bruker på meldingsnivå**.
    - I hurtigfanen **Opprinnelige statuser**, i feltet **Meldingsstatus**, velger du **Ny**.
    - I hurtigfanen **Resultatstatuser**, i feltet **Meldingsstatus**, velger du **Klargjort**. I feltet **Svartype** angir du **Ble kjørt**.

4. Opprett en handling som heter **Generer rapport**, og angi følgende felt:

    - På hurtigfanen **Generelt** i feltet **Handlingstype** velger du **Eksport av elektronisk rapportering**. I feltet **Formattilordning** velger du ER-eksportformatet. Alternativene er **Excel**, **XML**, **JSON**, **Tekst** og **Annet**.
    - I hurtigfanen **Opprinnelige statuser**, i feltet **Meldingsstatus**, velger du **Klargjort**.
    - I hurtigfanen **Resultatstatuser**, i feltet **Meldingsstatus**, velger du **Generert**. I feltet **Svartype** angir du **Ble kjørt**.

    ![Generer rapporthandling](media/generate-report-action.png)

5. Valgfritt: Hvis du vil la brukerne generere en rapport flere ganger, kan du opprette en handling kalt **Oppdater til innledende status** og angi følgende felt:

    - På hurtigfanen **Generelt** i feltet **Handlingstype** velger du **Behandling av bruker på meldingsnivå**.
    - I hurtigfanen **Opprinnelige statuser**, i feltet **Meldingsstatus**, velger du **Generert**.
    - I **Resultatstatuser**-hurtigkategorien legger du til en egen linje for hver av de to meldingsstatusene (**Klargjort** og **Ny**). For begge linjene angir du feltet **Svartype** til **Ble kjørt**.

## <a name="electronic-message-processing"></a>Behandling av elektronisk melding

I dette eksemplet må alle handlingene settes opp slik at de kjører separat. Det antas at brukeren vil initialisere alle handlinger.

1. Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Behandling av elektronisk melding**.
2. Legg til en post for din behandling, og legg til alle tidligere definerte handlinger og et ekstra felt.
3. Valgfritt: På hurtigfanen **Sikkerhetsroller** definerer du sikkerhetsroller for behandlingen din for å begrense tilgangen til bestemt rapportering.
4. Gå til **Mva** \> **Forespørsler og rapporter** \> **Elektroniske meldinger** \> **Elektroniske meldinger**.
5. Velg **Ny** for å opprette en melding. Nå kan du legge til datoer og en beskrivelse. Du kan også oppdatere verdien i tilleggsfeltet etter behov.

    ![Opprette en elektronisk melding](media/create-electronic-message.png)

    Rutenettet i hurtigfanen **Handlingslogg** fylles automatisk ut med en logg over alle handlinger som utføres på meldingen.

    Du kan nå slette eller oppdatere meldingsstatusen. 

6. Hvis du vil oppdatere meldingsstatus, velger du **Oppdater status**. I feltet **Ny status** velger du **Klargjort**, og deretter velger du **OK**.

    ![Oppdatere meldingsstatusen](media/update-status.png)

    Status for meldingen oppdateres til **Klargjort**.

7. Generer rapporten ved å velge **Generer rapport**.

    Rapporten genereres, og meldingsstatusen og -loggen oppdateres.

8. Hvis du vil vise den genererte rapporten, velger du **Vedlegg**-knappen (bindersikonet) i øvre høyre hjørne på siden.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
