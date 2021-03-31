---
title: Dele ER-konfigurasjoner i RCS/det globale repositoriet med eksterne organisasjoner
description: Dette emnet forklarer hvordan du deler konfigurasjoner for elektronisk rapportering (ER) i Microsoft RCS (Regulatory Configuration Services) eller det globale repositoriet direkte med eksterne organisasjoner.
author: JaneA07
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: e7ec24ddc532ee3b87108d076d5103538be903be
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218836"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a>Dele konfigurasjoner for elektronisk rapportering (ER) i RCS(Regulatory Configuration Services) eller det globale repositoriet med eksterne organisasjoner

[!include [banner](../includes/banner.md)]

Du kan bruke Microsoft Regulatory Configuration Services (RCS) til å dele konfigurasjoner for elektronisk rapportering (ER) og deretter publisere dem til eksterne organisasjoner.

Følgende fremgangsmåter forklarer hvordan en RCS-bruker kan dele en versjon av en ER-konfigurasjon som er konfigurert i en RCS-forekomst, med en ekstern organisasjon. Før du kan fullføre de prosedyrene, må du gjøre følgende:

- Åpne en RCS-forekomst.
- Opprette en aktiv konfigurasjonsleverandør. Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
- Opprett og last opp en ny versjon av en ER-konfigurasjon. Hvis du vil ha mer informasjon, kan du se [Opprette og laste opp en ny versjon av en konfigurasjon for elektronisk rapportering (ER)](rcs-global-repo-upload.md).

Du må også kontrollere at det er klargjort et RCS-miljø for firmaet ditt.

1. I en Finance and Operations-app går du til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. Hvis et RCS-miljø ikke er klargjort for firmaet ditt, velger du **Regulatory Services – Ekstern konfigurasjon**, og deretter følger du instruksjonene for å klargjøre en.

Hvis et RCS-miljø allerede er klargjort for ditt firma, bruker du URL-adressen for siden til å få tilgang til den ved å velge alternativet for pålogging.

## <a name="verify-the-configuration-that-you-want-to-share"></a>Kontrollere konfigurasjonen du vil dele

Følg denne fremgangsmåten for å kontrollere at konfigurasjonen du vil dele, allerede er lastet opp til det globale repositoriet.

1. I arbeidsområdet **Elektronisk rapportering** velger du **Repositorier** for konfigurasjonsleverandøren.

    ![Konfigurasjonsleverandører](media/1_RCS_Repo_for_config_provider.JPG)

2. Velg **Globalt repositorium** \> **Åpne**.
3. Søk etter konfigurasjonen du vil dele. Du kan bruke filtreringsfeltet til å begrense søket. Hvis du ikke finner konfigurasjonen i det globale repositoriet, følger du fremgangsmåten under [Opprette og laste opp en ny versjon av en konfigurasjon for elektronisk rapportering (ER)](rcs-global-repo-upload.md).

## <a name="share-er-configurations-with-external-organizations"></a>Dele ER-konfigurasjoner med eksterne organisasjoner

Når en konfigurasjon er opprettet under konfigurasjonsleverandøren, kan du dele den direkte med eksterne organisasjoner ved hjelp av hurtigkategorien **Delt med** på siden **Globalt konfigurasjonsrepositorium**.

1. I arbeidsområdet **Elektronisk rapportering** velger du **Repositorier** for konfigurasjonsleverandøren.
2. Velg **Globalt repositorium** \> **Åpne**. 
3. Velg konfigurasjonen du vil dele.
4. I hurtigkategorien **Delt med** velger du **Organisasjon**.

    ![Delt med hurtigkategori](media/1_RCS_Repo_for_Share_with_org.JPG)

5. I dialogboksen angir du domenenavnet for den eksterne organisasjonen, og deretter velger du **OK**.

    ![Dele konfigurasjonsversjon med dialogboksen Ekstern organisasjon](media/1_RCS_Repo_for_Share_with_form.JPG)

Konfigurasjonen deles med den eksterne organisasjonen, og er tilgjengelig for den organisasjonen i det globale repositoriet. Derfra kan den importeres til organisasjonens forekomst av RCS eller i forekomstene av Finance and Operations-apper.

6. Hvis du vil oppheve deling av en konfigurasjon som tidligere er delt med en ekstern organisasjon, velger du konfigurasjonen og klikker **Opphev deling**, og deretter velger du **OK**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]