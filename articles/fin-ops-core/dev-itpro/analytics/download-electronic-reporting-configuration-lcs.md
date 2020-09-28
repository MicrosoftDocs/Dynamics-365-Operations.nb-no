---
title: Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services
description: Dette emnet forklarer hvordan du laster ned konfigurasjoner for elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8a18427114bddb7c72024a8d96d33f3fbf8dbe17
ms.sourcegitcommit: 9857d5cbdc0ab2fc9db049ac5ad118fc2b29bedc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/14/2020
ms.locfileid: "3810625"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Laste ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du laster ned den nyeste versjonen av [Konfigurasjoner for elektronisk rapportering (ER)](general-electronic-reporting.md#Configuration) fra [Delt aktivabibliotek](../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).

1. Logg på programmet med én av følgende roller:

    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

2. Gå til **Organisasjonsstyring** &gt; **Arbeidsområder** &gt; **Elektronisk rapportering**.
3. I delen **Konfigurasjonsleverandører** velger du **Microsoft**-flisen.
4. På **Microsoft**-flisen velger du **Repositorier**.

    [![Microsoft-flis på siden Lokaliseringskonfigurasjon](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. På **Konfigurasjonsrepositorier**-siden i rutenettet velger du det eksisterende repositoriet for **LCS**-typen. Hvis dette repositoriet ikke vises i rutenettet, gjør du følgende:

    1. Velg **Legg til** for å legge til et repositorium.
    2. Velg **LCS** som type repositorium.
    3. Velg **Opprett repositorium**.
    4. Hvis du blir spurt om godkjenning, følger du instruksjonene på skjermen.
    5. Angi et navn og en beskrivelse for repositoriet.
    6. Velg **OK** for å bekrefte den nye repositoriumoppføringen.
    7. I rutenettet velger du det nye repositoriet i **LCS**-typen.

6. Velg **Åpne** for å vise listen over ER-konfigurasjoner for det valgte repositoriet.

    [![Konfigurasjonsrepositorier-side](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > Hvis du har problemer med å få tilgang til LCS-repositoriet for å laste ned konfigurasjoner fra det delte aktivabiblioteket i LCS, kan i stedet du laste ned konfigurasjoner fra [Globalt repositorium](er-download-configurations-global-repo.md).

7. Velg den obligatoriske ER-konfigurasjonen i konfigurasjonstreet i den venstre ruten.
8. I **Versjoner**-hurtigkategorien velger du den nødvendige versjonen av den valgte ER-konfigurasjonen.
9. Velg **Importer** for å laste ned den valgte versjonen fra LCS til den gjeldende forekomsten.

    > [!NOTE]
    > **Importer**-knappen er ikke tilgjengelig for ER-konfigurasjonsversjoner som allerede finnes i den gjeldende forekomsten.

    [![Konfigurasjonsrepositorium-side](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> Avhengig av ER-innstillingene valideres konfigurasjonene når de er importert. Du kan få beskjed om eventuelle problemer som oppdages. Du må løse disse problemene før du kan bruke den importerte konfigurasjonsversjonen. Hvis du vil ha mer informasjon, se listen over relaterte emner for dette emnet.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten](er-download-configurations-global-repo.md)
