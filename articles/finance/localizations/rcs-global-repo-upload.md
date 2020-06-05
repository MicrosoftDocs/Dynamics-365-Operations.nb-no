---
title: Opprette ER-konfigurasjoner i RCS og laste dem opp til det globale repositoriet
description: Dette emnet forklarer hvordan du oppretter en konfigurasjon for elektronisk rapportering (ER) i Microsoft RCS (Regulatory Configuration Services) og laster den opp til det globale repositoriet.
author: JaneA07
manager: AnnBe
ms.date: 05/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 0e194a8b777f984412d81e315f92ab4bb8a3b0c9
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371261"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>Opprette ER-konfigurasjoner i Regulatory Configuration Services (RCS) og laste dem opp til det globale repositoriet

[!include [banner](../includes/banner.md)]

Du kan bruke Microsoft Regulatory Configuration Services (RCS) til å utforme konfigurasjoner for elektronisk rapportering (ER) og publisere dem slik at de kan brukes i organisasjonen.

Fremgangsmåtene nedenfor forklarer hvordan en bruker i rollen systemansvarlig eller elektronisk rapportering kan opprette en avledet versjon av en ER-konfigurasjon som er konfigurert i en RCS-forekomst, og deretter laste opp den avledede konfigurasjonen til det globale repositoriet. 

Før du kan fullføre de prosedyrene, må du gjøre følgende:

- Åpne en RCS-forekomst.
- Opprette en aktiv konfigurasjonsleverandør. Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Du må også kontrollere at det er klargjort et RCS-miljø for firmaet ditt.

1. I en Finance and Operations-app går du til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. Hvis et RCS-miljø ikke er klargjort for firmaet ditt, velger du **Regulatory Services – Ekstern konfigurasjon**, og deretter følger du instruksjonene for å klargjøre en.

Hvis et RCS-miljø allerede er klargjort for ditt firma, bruker du URL-adressen for siden til å få tilgang til den ved å velge alternativet for pålogging.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Opprette en avledet versjon av en konfigurasjon i RCS

1. I arbeidsområdet **Elektronisk rapportering** kontrollerer du at du har en aktiv konfigurasjonsleverandør for organisasjonen. 
2. Velg **Rapporteringskonfigurasjoner**.
3. Velg konfigurasjonen du vil avlede en ny versjon fra. Du kan bruke filtreringsfeltet over treet til å begrense søket.
4. Velg **Opprett konfigurasjon** \> **Avled fra navn**.
5. Angi et navn og en beskrivelse, og velg deretter **Opprett konfigurasjon** for å opprette en ny avledet versjon.
6. Velg den nylig avledede konfigurasjonen, legg til en beskrivelse av versjonen, og velg deretter **OK**. Statusen for konfigurasjonen til er endret til **Fullført**.

![Ny konfigurasjonsversjon i RCS](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Når konfigurasjonsstatusen endres, kan du få en valideringsfeilmelding som er knyttet til de tilkoblede appene. Hvis du vil deaktivere valideringen, velger du **Brukerparametere** i kategorien **Konfigurasjoner**, og deretter setter du alternativet **Hopp over validering ved konfigurasjonens statusendring og rebasering** til **Ja** 

## <a name="upload-a-configuration-to-the-global-repository"></a>Laste opp en konfigurasjon til det globale repositoriet

Hvis du vil dele en ny eller avledet konfigurasjon med organisasjonen, kan du laste den opp til det globale repositoriet.

1. Velg den fullførte versjonen av konfigurasjonen, og velg deretter **Last opp til repositorium**.
2. Velg alternativet **Globalt (Microsoft)**, og velg deretter **Last opp**.

    ![Laste opp til alternativer for repositorium](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Velg **Ja** i bekreftelsesboksen. 
4. Oppdater beskrivelsen av versjonen etter behov, og velg deretter **OK**. 

Statusen for konfigurasjonen oppdateres til **Dele**, og konfigurasjonen lastes opp til det globale repositoriet. Derfra kan du arbeide med den på følgende måter:

- Importere den til Dynamics 365-forekomsten. Hvis du vil ha mer informasjon, kan du se [(ER) Importere konfigurasjoner fra RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Hvis du vil dele den med en tredjepart eller en ekstern organisasjon, kan du se [RCS Dele konfigurasjoner for elektronisk rapportering (ER) med eksterne organisasjoner](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)

![Avledet versjon av Intrastat Contoso-konfigurasjon i det globale repositoriet](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Config_upload_GlobalRepo.JPG)
