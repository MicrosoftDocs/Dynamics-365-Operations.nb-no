---
title: Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services
description: Dette emnet forklarer hvordan du laster ned elektronisk rapportering (ER) konfigurasjoner fra Microsoft Dynamics Lifecycle tjenester (LCS).
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 9dca5dec846670da25926826f59d7bce0fa0dcea
ms.lasthandoff: 03/31/2017


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services

Dette emnet forklarer hvordan du laster ned elektronisk rapportering (ER) konfigurasjoner fra Microsoft Dynamics Lifecycle tjenester (LCS).

Denne opplæringen leder deg gjennom prosessen med å laste ned nyeste versjon av konfigurasjoner for elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).

1.  Logg på Dynamics 365 for Operations med én av følgende roller:
    -   Utvikler av elektronisk rapportering
    -   Funksjonell konsulent for elektronisk rapportering
    -   Systemansvarlig

2.  Gå til **organisasjonsadministrasjon**&gt;**elektronisk rapportering**.
3.  I delen **Konfigurasjonsleverandører** velger du **Microsoft**-flisen.
4.  I **Microsoft**-flisen klikker du **Repositorier**. [![Update-er-from-LCS-for-MS-Open-MS-repositories-List](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  På **Konfigurasjonsrepositorier**-siden i rutenettet velger du det eksisterende repositoriet for **LCS**-typen. Hvis dette repositoriet ikke vises i rutenettet, gjør du følgende:
    1.  Klikk **Legg til** for å legge til et nytt repositorium.
    2.  Velg **LCS** som type repositorium.
    3.  Klikk **Opprett repositorium**.
    4.  Angi et navn og en beskrivelse for repositoriet.
    5.  Klikk **OK** for å bekrefte den nye repositoriumoppføringen.
    6.  I rutenettet velger du det nye repositoriet i **LCS**-typen.

6.  Klikk **Åpne** for å vise listen over ER-konfigurasjoner for det valgte repositoriet. [![Update-er-from-LCS-for-MS-make-LCS-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  Velg ER-konfigurasjonen du må ha, i konfigurasjonstreet i den venstre ruten.
8.  I **Versjoner**-hurtigkategorien velger du den nødvendige versjonen av den valgte ER-konfigurasjonen.
9.  Klikk **Importer** for å laste ned den valgte versjonen fra LCS til den gjeldende forekomsten av Dynamics 365 for Operations. **Merk:** **Importer**-knappen er ikke tilgjengelig for ER-konfigurasjonsversjoner som allerede finnes i den gjeldende forekomsten av Dynamics 365 for Operations. [![Update-er-from-LCS-for-MS-Download-Configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Merk:** Avhengig av ER-innstillingene valideres konfigurasjonene når de er importert. Du kan få beskjed om eventuelle problemer som oppdages. Du må løse disse problemene før du kan bruke den importerte konfigurasjonsversjonen. Hvis du vil ha mer informasjon, kan du se listen over relaterte artikler for dette emnet.

<a name="see-also"></a>Se også
--------

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)


