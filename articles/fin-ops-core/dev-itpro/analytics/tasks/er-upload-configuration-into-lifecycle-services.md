---
title: Laste opp en konfigurasjon til Lifecycle Services
description: Dette emnet forklarer hvordan du oppretter en ny konfigurasjon for elektronisk rapportering (ER) og laster den opp til Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92fc6d7a8b2508c9a1f7b56ca8115adbd6ae00ea
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092547"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a>Laste opp en konfigurasjon til Lifecycle Services

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny [konfigurasjon for elektronisk rapportering (ER)](../general-electronic-reporting.md#Configuration) og laste den opp til [aktivabiblioteket på prosjektnivå](../../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).

I dette eksemplet skal du opprette en konfigurasjon og laste den opp til LCS for et eksempelfirma med navnet Litware, Inc. Denne fremgangsmåten kan fullføres i alle firmaer ettersom ER-konfigurasjoner deles mellom alle firmaer. For å fullføre disse trinnene må du først fullføre trinnene i [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). Tilgang til LCS er også nødvendig.

1. Logg på programmet med én av følgende roller:

    - Utvikler av elektronisk rapportering
    - Systemansvarlig

2. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
3. Velg **Litware, Inc.** og merk som **Aktiv**.
4. Velg **Konfigurasjoner**.

<a name="accessconditions"></a>
> [!NOTE]
> Kontroller at den gjeldende Dynamics 365 Finance-brukeren er medlem av LCS-prosjektet som inneholder [aktivabiblioteket](../../lifecycle-services/asset-library.md#asset-library-support) som brukes til å importere ER-konfigurasjoner.
>
> Du kan ikke få tilgang til et LCS-prosjekt fra et ER-repositorium som representerer et annet domene enn domenet som brukes i Finance. Hvis du prøver, vises det en tom liste over LCS-prosjekter, og du kan ikke importere ER-konfigurasjonene fra aktivabiblioteket på prosjektnivå i LCS. Hvis du vil ha tilgang til aktivabiblioteker på prosjektnivå fra et ER-repositorium som brukes til å importere ER-konfigurasjoner, logger du på Finance-modulen ved hjelp av legitimasjonen til en bruker som tilhører leieren (domenet) som gjeldende Finance-forekomst er klargjort for.

## <a name="create-a-new-data-model-configuration"></a>Opprett en ny datamodellkonfigurasjon

1. Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.
2. På siden **Konfigurasjoner** velger du **Opprett konfigurasjon** for å åpne dialogboksen med rullegardinliste.

    I dette eksemplet skal du opprette en konfigurasjon som inneholder en eksempeldatamodell for elektroniske dokumenter. Denne datamodellkonfigurasjonen lastes inn i LCS senere.

3. I feltet **Navn** angir du **Eksempelmodellkonfigurasjon**.
4. I feltet **Beskrivelse** angir du **Eksempelmodellkonfigurasjon**.
5. Velg **Opprett konfigurasjon**.
6. Velg **Modellutforming**.
7. Velg **Ny**.
8. I **Navn**-feltet angir du **Inngangspunkt**.
9. Velg **Legg til**.
10. Velg **Lagre**.
11. Lukk siden.
12. Velg **Endre status**.
13. Velg **Fullfør**.
14. Velg **OK**.
15. Lukk siden.

## <a name="register-a-new-repository"></a>Registrere et nytt repositorium

1. Gå til **Organisasjonsstyring \> Arbeidsområder \> Elektronisk rapportering**.

2. I delen **Konfigurasjonsleverandører** velger du **Litware, Inc.**-flisen.

3. På **Litware, Inc.**-flisen velger du **Repositorier**.

    Nå kan du åpne listen over repositorier for konfigurasjonsleverandøren Litware, Inc.

4. Velg **Legg til** for å åpne dialogboksen med rullegardinliste.

    Du kan nå legge til et nytt repositorium.

5. I feltet **Konfigurasjonsrepositorium** velger du **LCS**.
6. Velg **Opprett repositorium**.
7. Angi eller velg en verdi i feltet **Prosjekt**.

    I dette eksemplet velger du det ønskede LCS-prosjektet. Du må ha [tilgang](#accessconditions) til prosjektet.

8. Velg **OK**.

    Fullfør en ny oppføring i repositoriet.

9. Merk den valgte raden i listen.

    I dette eksemplet velger du repositoriumposten i **LCS**.

    Vær oppmerksom på at et registrert repositorium er merket med gjeldende leverandør. Det er med andre ord bare konfigurasjoner som eies av denne leverandøren, som kan plasseres i repositoriet og som derfor lastes opp til det valgte LCS-prosjektet.

10. Velg **Åpne**.

    Du åpner repositoriet for å vise listen over ER-konfigurasjoner. Hvis det valgte prosjektet ennå ikke er brukt for deling av ER-konfigurasjoner, vil listen være tom.

11. Lukk siden.
12. Lukk siden.

## <a name="upload-a-configuration-into-lcs"></a>Laste opp en konfigurasjon til LCS

1. Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.
2. På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Eksempelmodellkonfigurasjon**.

    Du må velge en opprettet konfigurasjon som allerede er fullført.

3. Finn og velg ønsket post i listen.

    For dette eksemplet velger du versjonen av den valgte konfigurasjonen som har statusen **Fullført**.

4. Velg **Endre status**.
5. Velg **Del**.

    Statusen for konfigurasjonen endres fra **Fullført** til **Delt** når konfigurasjonen er publisert i LCS.

6. Velg **OK**.
7. Finn og velg ønsket post i listen.

    For dette eksemplet velger du konfigurasjonsversjonen som har statusen **Delt**.

    Vær oppmerksom på at statusen for den valgte versjonen ble endret fra **Fullført** til **Delt**.

8. Lukk siden.
9. Velg **Repositorier**.

    Nå kan du åpne listen over repositorier for konfigurasjonsleverandøren Litware, Inc.

10. Velg **Åpne**.

    I dette eksemplet velger du repositoriet **LCS** og åpner det.

    Vær oppmerksom på at den valgte konfigurasjonen vises som et anleggsmiddel for det valgte LCS-prosjektet.

11. Åpne LCS ved å gå til <https://lcs.dynamics.com>.
12. Åpne et prosjekt som ble brukt tidligere til registrering av repositorium.
13. Åpne aktivabiblioteket for prosjektet.
14. Velg aktivatypen **GER-konfigurasjon**.

    ER-konfigurasjonen du lastet opp, bør nå vises.

    Vær oppmerksom på at den opplastede LCS-konfigurasjonen kan importeres til en annen forekomst hvis leverandører har tilgang til dette LCS-prosjektet.
