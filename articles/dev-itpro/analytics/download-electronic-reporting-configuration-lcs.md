---
title: Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services
description: Dette emnet forklarer hvordan du laster ned konfigurasjoner for elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
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
ms.openlocfilehash: 8686d2639a3ab7f2e79944cc5eed51571d463261
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "315757"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Laste ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du laster ned konfigurasjoner for elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).

Denne opplæringen leder deg gjennom prosessen med å laste ned nyeste versjon av konfigurasjoner for elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).

1. Logg på Finance and Operations med én av følgende roller:

    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

2. Gå til **Organisasjonsstyring** &gt; **Elektronisk rapportering**.
3. I delen **Konfigurasjonsleverandører** velger du **Microsoft**-flisen.
4. I **Microsoft**-flisen klikker du **Repositorier**.

    [![oppdatere-er-fra-lcs-for-ms-åpen-ms-repositorier-liste](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. På **Konfigurasjonsrepositorier**-siden i rutenettet velger du det eksisterende repositoriet for **LCS**-typen. Hvis dette repositoriet ikke vises i rutenettet, gjør du følgende:

    1. Klikk **Legg til** for å legge til et nytt repositorium.
    2. Velg **LCS** som type repositorium.
    3. Klikk **Opprett repositorium**.
    4. Hvis du blir bedt om det, følger du autorisasjonsinstruksjonene.
    5. Angi et navn og en beskrivelse for repositoriet.
    6. Klikk **OK** for å bekrefte den nye repositoriumoppføringen.
    7. I rutenettet velger du det nye repositoriet i **LCS**-typen.

6. Klikk **Åpne** for å vise listen over ER-konfigurasjoner for det valgte repositoriet.

    [![Oppdatere-er-fra-LCS-for-MS-merke-LCS-repositorium](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

7. Velg ER-konfigurasjonen du må ha, i konfigurasjonstreet i den venstre ruten.
8. I **Versjoner**-hurtigkategorien velger du den nødvendige versjonen av den valgte ER-konfigurasjonen.
9. Klikk **Importer** for å laste ned den valgte versjonen fra LCS til den gjeldende forekomsten av Finance and Operations.

    > [!NOTE]
    > **Importer**-knappen er ikke tilgjengelig for ER-konfigurasjonsversjoner som allerede finnes i den gjeldende forekomsten av Finance and Operations.

    [![oppdatere-er-fra-lcs-for-ms-nedlasting-konfigurasjon](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> Avhengig av ER-innstillingene valideres konfigurasjonene når de er importert. Du kan få beskjed om eventuelle problemer som oppdages. Du må løse disse problemene før du kan bruke den importerte konfigurasjonsversjonen. Hvis du vil ha mer informasjon, se listen over relaterte artikler for dette emnet.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)
