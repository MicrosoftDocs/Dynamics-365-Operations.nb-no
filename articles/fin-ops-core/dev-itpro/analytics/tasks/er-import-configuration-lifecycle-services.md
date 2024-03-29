---
title: Importere en konfigurasjon fra Lifecycle Services
description: Denne artikkelen beskriver hvordan du importerer en ny versjon av en ER-konfigurasjon (Elektronisk rapportering) fra Microsoft Dynamics Lifecycle Services (LCS).
author: kfend
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
ms.openlocfilehash: 92c5d010430b38cb6c11a87283a2f7d4c29484f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290372"
---
# <a name="import-a-configuration-from-lifecycle-services"></a>Importere en konfigurasjon fra Lifecycle Services

[!include [banner](../../includes/banner.md)]

Denne artikkelen forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan importere en ny versjon av en [konfigurasjon for elektronisk rapportering (ER)](../general-electronic-reporting.md#Configuration) fra [aktivabiblioteket på prosjektnivå](../../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).

> [!IMPORTANT]
> Bruken av Lifecycle Services (LCS) som et lagringsrepositorium for konfigurasjoner for elektronisk rapportering (ER) blir [avskrevet](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Hvis du vil ha mer informasjon, se [Regulatory Configuration Service (RCS) – avskrivning av lager for Lifecycle Services (LCS)](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

I dette eksemplet skal du velge ønsket versjon av ER-konfigurasjonen og importere den for et eksempelfirma med navnet Litware, Inc. Denne fremgangsmåten kan fullføres i alle firmaer, ettersom ER-konfigurasjoner deles mellom firmaer. For å fullføre disse trinnene må du først fullføre trinnene i [Laste opp en ER-konfigurasjon til Lifecycle Services](er-upload-configuration-into-lifecycle-services.md). Tilgang til LCS er også nødvendig.

1. Logg på programmet med én av følgende roller:

    - Utvikler av elektronisk rapportering
    - Systemansvarlig

2. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
3. Velg **Konfigurasjoner**.

<a name="accessconditions"></a>
> [!NOTE]
> Kontroller at den gjeldende Dynamics 365 Finance-brukeren er medlem av LCS-prosjektet som inneholder aktivabiblioteket som brukeren vil [bruke](../../lifecycle-services/asset-library.md#asset-library-support) for å importere ER-konfigurasjoner.
>
> Du kan ikke få tilgang til et LCS-prosjekt fra et ER-repositorium som representerer et annet domene enn domenet som brukes i Finance. Hvis du prøver, vises det en tom liste over LCS-prosjekter, og du kan ikke importere ER-konfigurasjonene fra aktivabiblioteket på prosjektnivå i LCS. Hvis du vil ha tilgang til aktivabiblioteker på prosjektnivå fra et ER-repositorium som brukes til å importere ER-konfigurasjoner, logger du på Finance-modulen ved hjelp av legitimasjonen til en bruker som tilhører leieren (domenet) som gjeldende Finance-forekomst er klargjort for.

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a>Slette en delt versjon av en datamodellkonfigurasjon

1. På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Eksempelmodellkonfigurasjon**.

    Du opprettet den første versjonen av en konfigurasjon for eksempeldatamodell og publiserte den i LCS da du fullførte fremgangsmåten i [Laste opp en konfigurasjon til Lifecycle Services](er-upload-configuration-into-lifecycle-services.md). I denne fremgangsmåten sletter du den versjonen av ER-konfigurasjonen. Du skal deretter importere denne versjonen fra LCS senere i denne artikkelen.

2. Finn og velg ønsket post i listen.

    For dette eksemplet velger du versjonen av konfigurasjonen som har statusen **Delt**. Denne statusen angir at konfigurasjonen er publisert til LCS.

3. Velg **Endre status**.
4. Velg **Avslutt**.

    Ved å endre statusen for den valgte versjonen fra **Delt** til **Avsluttet**, gjør du versjonen tilgjengelig for sletting.

5. Velg **OK**.
6. Finn og velg ønsket post i listen.

    For dette eksemplet velger du versjonen av konfigurasjonen som har statusen **Avsluttet**.

7. Velg **Slett**.
8. Velg **Ja**.

    Legg merke til at bare utkastversjon 2 av den valgte datamodellkonfigurasjonen nå er tilgjengelig.

9. Lukk siden.

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a>Importere en delt versjon av en datamodellkonfigurasjon fra LCS

1. Gå til **Organisasjonsstyring \> Arbeidsområder \> Elektronisk rapportering**.

2. I delen **Konfigurasjonsleverandører** velger du **Litware, Inc.**-flisen.

3. På **Litware, Inc.**-flisen velger du **Repositorier**.

    Nå kan du åpne listen over repositorier for konfigurasjonsleverandøren Litware, Inc.

4. Velg **Åpne**.

    I dette eksemplet velger du repositoriet **LCS** og åpner det. Du må ha [tilgang](#accessconditions) til LCS-prosjektet og aktivabiblioteket som brukes av det valgte ER-repositoriet.

5. Merk den valgte raden i listen.

    For dette eksemplet velger du den første versjonen av **Eksempelmodellkonfigurasjon** i versjonslisten.

6. Velg **Import**.
7. Velg **Ja** for å bekrefte importen av den valgte versjonen fra LCS.

    En informasjonsmelding bekrefter at den valgte versjonen er importert.

8. Lukk siden.
9. Lukk siden.
10. Velg **Konfigurasjoner**.
11. Velg **Eksempelmodellkonfigurasjon** i treet.
12. Finn og velg ønsket post i listen.

    For dette eksemplet velger du versjonen av konfigurasjonen som har statusen **Delt**.

    Legg merke til at delt versjon 1 av den valgte datamodellkonfigurasjonen nå også er tilgjengelig.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
