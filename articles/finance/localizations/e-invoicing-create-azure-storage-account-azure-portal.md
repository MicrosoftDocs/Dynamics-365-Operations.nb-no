---
title: Opprette en Azure-lagringskonto i Azure Portal
description: Denne artikkelen forklarer hvordan du oppretter en Azure-lagringskonto for elektronisk fakturering.
author: dkalyuzh
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4380261140086bcb278162f8dc70b39eaa7078fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898025"
---
# <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Opprette en Azure-lagringskonto i Azure Portal

[!include [banner](../includes/banner.md)]

Alle elektroniske filer som genereres av tjenesten for elektronisk fakturering eller går til tjenesten under behandling, lagres i beholdere på Microsoft Azure-lagringskontoen din. For å sikre at elektronisk fakturering har tilgang til disse beholderne, må du oppgi tokenet for signatur for delt tilgang (SAS) for lagringskontoen i tjenesten for elektronisk fakturering. For å sikre at tokenet lagres på en sikker måte, må du i tillegg ikke angi SAS-tokenet direkte. Lagre det i stedet i et Azure-nøkkelhvelv, og oppgi en Azure Key Vault-hemmelighet.

1. Åpne lagringskontoen du har tenkt å bruke med tjenesten for elektronisk fakturering.
2. Gå til **Innstillinger** \> **Konfigurasjon**, og kontroller at parameteren **Gi Blob offentlig tilgang** er satt til **Aktivert**.
3. Gå til **Datalagring** \> **Beholdere**, og opprett en beholder.
4. Angi et navn på beholderen, og sett feltet **Offentlig tilgangsnivå** til **Privat (ingen anonym tilgang)**.
5. Åpne den nye beholderen, og gå til **Innstillinger** \> **Tilgangspolicy**.
6. Velg **Legg til policy** for å legge til en lagret tilgangspolicy.
7. Angi **Identifikator**-feltet etter behov.
8. I **Tillatelser**-feltet velger du alle tillatelser.

    ![Alle tillatelsene som er valgt i Tillatelser-feltet i dialogboksen Legg til policy.](media/e-invoicing-azure-1.png)

9. Angi start- og sluttdatoer. Sluttdatoen må være i fremtiden.
10. Velg **OK** for å lagre policyen, og lagre endringene i containeren.
11. Gå til **Innstillinger** \> **Delte tilgangstokener**, og angi feltverdiene.
12. Angi start- og sluttdatoer. Sluttdatoen må være i fremtiden.
13. I **Tillatelser**-feltet velger du følgende tillatelser:

    - Les
    - Legg til
    - Opprett
    - Skriv
    - Slett
    - Liste

14. Velg **Generer SAS-token og URL-adresse**.
15. Kopier og lagre verdien i feltet **Blob SAS-URL-adresse**. Denne verdien brukes senere i denne prosedyren og det henvises til den som *URI for signatur for delt tilgang*.
16. Åpne Key Vault du har tenkt å bruke med elektronisk fakturering.
17. Gå til **Innstillinger** \> **Hemmeligheter**, og velg **Generer/Importer** for å opprette en hemmelighet.
18. På siden **Opprett en hemmelig**, i feltet **Opplastingsalternativer**, velger du **Manuell**.
19. Angi navnet på hemmeligheten. Dette navnet vil bli brukt under oppsettet av tjenesten i Regulatory Configuration Service (RCS) og kalles *navn på Key Vault-hemmelighet*. Hvis du vil ha informasjon om hvordan du konfigurerer RCS, kan du se [Konfigurere Regulatory Configuration Service (RCS)](e-invoicing-set-up-rcs.md).
20. I **Verdi**-feltet angir du URI-en for signatur for delt tilgang du kopierte tidligere.
21. Velg **Opprett**.
