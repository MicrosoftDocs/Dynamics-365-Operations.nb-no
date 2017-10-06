---
title: Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services
description: Dette emnet forklarer hvordan du laster ned konfigurasjoner for elektronisk rapportering (ER) for fra Microsoft Dynamics Lifecycle Services (LCS).
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: be77d76194e9d38589548113cc650599d5af4323
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017

---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services

[!include[banner](../includes/banner.md)]


Dette emnet forklarer hvordan du laster ned konfigurasjoner for elektronisk rapportering (ER) for fra Microsoft Dynamics Lifecycle Services (LCS).

Denne opplæringen leder deg gjennom prosessen med å laste ned nyeste versjon av konfigurasjoner for elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).

1.  Logg på Finance and Operations med én av følgende roller:
    -   Utvikler av elektronisk rapportering
    -   Funksjonell konsulent for elektronisk rapportering
    -   Systemansvarlig

2.  Gå til **Organisasjonsstyring** &gt; **Elektronisk rapportering**.
3.  I delen **Konfigurasjonsleverandører** velger du **Microsoft**-flisen.
4.  I **Microsoft**-flisen klikker du **Repositorier**. [![oppdatere-er-fra-lcs-for-ms-åpen-ms-repositorier-liste](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  På **Konfigurasjonsrepositorier**-siden i rutenettet velger du det eksisterende repositoriet for **LCS**-typen. Hvis dette repositoriet ikke vises i rutenettet, gjør du følgende:
    1.  Klikk **Legg til** for å legge til et nytt repositorium.
    2.  Velg **LCS** som type repositorium.
    3.  Klikk **Opprett repositorium**.
    4. Hvis du blir bedt om det, følger du autorisasjonsinstruksjonene.
    5.  Angi et navn og en beskrivelse for repositoriet.
    6.  Klikk **OK** for å bekrefte den nye repositoriumoppføringen.
    7.  I rutenettet velger du det nye repositoriet i **LCS**-typen.

6.  Klikk **Åpne** for å vise listen over ER-konfigurasjoner for det valgte repositoriet. [![Oppdatere-er-fra-LCS-for-MS-merke-LCS-repositorium](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  Velg ER-konfigurasjonen du må ha, i konfigurasjonstreet i den venstre ruten.
8.  I **Versjoner**-hurtigkategorien velger du den nødvendige versjonen av den valgte ER-konfigurasjonen.
9.  Klikk **Importer** for å laste ned den valgte versjonen fra LCS til den gjeldende forekomsten av Finance and Operations. **Merk:** **Importer**-knappen er ikke tilgjengelig for ER-konfigurasjonsversjoner som allerede finnes i den gjeldende forekomsten av Finance and Operations. [![oppdatere-er-fra-lcs-for-ms-nedlasting-konfigurasjon](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Merk:** Avhengig av ER-innstillingene valideres konfigurasjonene når de er importert. Du kan få beskjed om eventuelle problemer som oppdages. Du må løse disse problemene før du kan bruke den importerte konfigurasjonsversjonen. Hvis du vil ha mer informasjon, se listen over relaterte artikler for dette emnet.

<a name="see-also"></a>Se også
--------

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)



