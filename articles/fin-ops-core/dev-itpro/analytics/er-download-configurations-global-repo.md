---
title: Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten
description: Denne artikkelen forklarer hvordan du laster ned elektroniske rapporteringskonfigurasjoner (ER) fra det globale repositoriet for konfigurasjonstjenesten.
author: NickSelin
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 53007504f1094b69ec6578d382c451a2bf1f9059
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108926"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a>Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du laster ned [elektroniske rapporteringskonfigurasjoner (ER)](general-electronic-reporting.md#Configuration) fra det globale repositoriet for konfigurasjonstjenesten. Hvis du vil ha mer informasjon, kan du se [Microsoft Dynamics 365 Finance – Regulatory Services, konfigurasjonstjeneste](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="open-configurations-repository"></a>Åpne konfigurasjonsrepositoriet

1. Logg på Dynamics 365 Finance-programmet med én av følgende roller:

    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

2. Gå til **Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering**.
3. I delen **Konfigurasjonsleverandører** velger du **Microsoft**-flisen.
3. På **Microsoft**-flisen velger du **Repositorier**.

    ![Arbeidsområdet Elektronisk rapportering.](./media/er-download-configurations-global-repo-er-workspace.png)

4. På **Konfigurasjonsrepositorier**-siden i rutenettet velger du det eksisterende repositoriet for **Global**-typen. Hvis dette repositoriet ikke vises i rutenettet, gjør du følgende:

    1. Velg **Legg til** for å legge til et nytt repositorium.
    2. Velg **Global** som repositoriumstype, og velg deretter **Opprett repositorium**.
    3. Hvis du blir bedt om det, følger du autorisasjonsinstruksjonene.
    4. Skriv inn et navn og en beskrivelse for repositoriet, og velg deretter **OK** for å bekrefte det nye repositoriet.
    5. I rutenettet velger du det nye repositoriet i **Global**-typen.

5. Velg **Åpne** for å vise listen over ER-konfigurasjoner for det valgte repositoriet.

    ![Konfigurasjonsrepositorier-side.](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a>Importere én enkelt konfigurasjon

1. På **Konfigurasjonsrepositorier**-siden går du til konfigurasjonstreet og velger den ønskede ER-konfigurasjonen.
2. I **Versjoner**-hurtigkategorien velger du den nødvendige versjonen av den valgte ER-konfigurasjonen.
3. Velg **Importer** for å laste ned den valgte versjonen fra det globale repositoriet til den gjeldende forekomsten av Finance.

    > [!NOTE]
    > **Importer**-knappen er ikke tilgjengelig for ER-konfigurasjonsversjoner som allerede finnes i den gjeldende Finance-forekomsten.

    ![Side for konfigurasjonsrepositorium, Konfigurasjoner-hurtigfane.](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a>Importere filtrerte konfigurasjoner

1. På **Konfigurasjonsrepositorier**-siden går du til konfigurasjonstreet og utvider **Filter**-hurtigkategorien.
2. I **Koder**-rutenettet legger du til eventuelle koder som kreves.
3. I **Relevans for land-/område**-feltet velger du de aktuelle lands-/områdekodene, og velger **Bruk filter**.

    > [!NOTE]
    > I **Konfigurasjoner**-hurtigkategorien ser du alle konfigurasjonene som oppfyller de angitte utvalgsbetingelsene.

4. I **Konfigurasjoner**-hurtigkategorien velger du **Importer** for å laste ned de filtrerte konfigurasjonene fra det globale repositoriet til den gjeldende forekomsten.
5. I **Konfigurasjoner**-hurtigkategorien velger du **Nullstill filter** for å tømme de angitte utvalgsbetingelsene.

    ![Siden for konfigurasjonsrepositorium, Versjoner-hurtigfane, Importer-knapp.](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> Avhengig av ER-innstillingene valideres konfigurasjonene når de er importert. Du kan få beskjed om eventuelle problemer som oppdages. Du må løse problemene før du kan bruke den importerte konfigurasjonsversjonen. Hvis du vil ha mer informasjon, se listen over relaterte ressurser for denne artikkelen.

> [!NOTE]
> ER-konfigurasjoner kan konfigureres som avhengige av andre konfigurasjoner. Sammen med en valgt konfigurasjon kan derfor også andre konfigurasjoner importeres automatisk. Hvis du vil ha mer informasjon om avhengigheter, se [Definere avhengigheten for ER-konfigurasjoner på andre komponenter](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

