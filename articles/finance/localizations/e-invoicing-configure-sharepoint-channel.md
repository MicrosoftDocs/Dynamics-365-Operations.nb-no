---
title: Konfigurere en SharePoint-kanal
description: Denne artikkelen forklarer hvordan du konfigurerer en Microsoft SharePoint-kanal slik at den kan behandle innkommende elektroniske fakturaer.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 89538adde4d14212fb0deccad05f828d146f16db
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910048"
---
# <a name="configure-a-sharepoint-channel"></a>Konfigurere en SharePoint-kanal

[!include [banner](../includes/banner.md)]

En forutsetning for å kunne konfigurere en Microsoft SharePoint-kanal slik at den kan behandle innkommende dokumenter, er å fullføre trinnene som beskrives i [Konfigurere en SharePoint-tilkobling](e-invoicing-create-sharepoint-connection.md).

Du kan deretter bruke SharePoint-kanalen til å importere elektroniske leverandørfakturaer fra filer som er lagret i SharePoint-mappene.

1. Opprett følgende mapper på SharePoint-området:

    - **Hovedmappe** – Mappen som tjenesten behandler filer fra.
    - **Arkivmappe** – Mappen der behandlede filer lagres.
    - **Feilmappe** – Mappen som systemet flytter filer til, hvis behandlingen mislykkes.

2. Velg funksjonen for elektronisk fakturering du opprettet, i Regulatory Configuration Service (RCS). Kontroller at du velger versjonen som har statusen **Utkast**.
3. Velg **Legg til** i **Oppsett**-fanen.
4. Velg alternativet **Egendefinert oppsett** i feltgruppen **Ny** i rullegardinboksen **Opprett funksjonsoppsett**:
5. Velg alternativet **Datakanal** i feltgruppen **Oppsettype**.
6. Velg **SharePoint-mappe** i feltet **Velg datakanal**.
7. Velg **Opprett**.
8. Velg linjen du opprettet, og velg deretter **Rediger**.
9. Angi følgende obligatoriske felter i **Parametere**-delen i **Datakanal**-fanen.

    | Felt                 | Beskrivelse |
    |-----------------------|-------------|
    | Datakanal          | Angi et unikt navn for å identifisere datakanalen. Navnet kan ha maksimum 10 tegn. Det refereres til dette i relevansreglene og i tilkoblede programmer i løpet av kommunikasjonen. |
    | SharePoint-adresse    | Angi nettadressen til SharePoint. Skriv for eksempel inn `<domain>.sharepoint.com`. |
    | Program-ID        | Angi navnet på Azure Key Vault-hemmeligheten som inneholder ID-en til SharePoint-brukerkontoen. Denne nøkkelen må opprettes i Key Vault og konfigureres i tjenestemiljøet. Verdien er verdien for **Program-ID (klient)** fra [Konfigurere SharePoint-tilkobling](e-invoicing-create-sharepoint-connection.md). |
    | Programhemmelighet    | Angi navnet på Key Vault-hemmeligheten som inneholder passordet for SharePoint-brukerkontoen. Verdien er verdien for **Hemmelighet for appregistrering** fra [Konfigurere SharePoint-tilkobling](e-invoicing-create-sharepoint-connection.md). |
    | Områdenavn             | Angi navnet på SharePoint-området. |
    | Navn på dokumentbibliotek | Angi navnet på SharePoint-dokumentbiblioteket. |
    | Tidsavbrudd               | Angi den lengste tiden, i millisekunder (ms), som systemet skal vente på svar. Standardverdien er 10 000 ms (10 sekunder). |
    | Hovedmappe           | Angi filimportkilden eller mappen som tjenesten skal behandle filer fra. |
    | Arkivmappe        | Angi mappen der behandlede filer skal lagres. |
    | Feilmappe          | Angi mappen som systemet skal flytte filer til, hvis behandlingen mislykkes. |
    | Maks filstørrelse         | Angi maksimumsstørrelsen for enkeltfiler som behandles, i byte. Standardverdien er 20 000 000 byte. |
    | Maks antall filer      | Angi maksimalt antall filer som skal behandles for én handling. Hvis du ikke vil begrense antall filer, angir du **0** (null) for verdien. |
    | Filfilter           | Angi en streng for å filtrere etter filnavn. Dette feltet er valgfritt. Det er støtte for en enkel maske som **\*smth\*.ext**, der hver stjerne (\*) representerer null eller flere forekomster av et tegn. Angi **\*.pdf** hvis du for eksempel vil konfigurere kanalen slik at den kan lese PDF-filer. |
    | Egendefinert filnavn      | Angi det egendefinerte filnavnet fra klienten. |

10. Gå gjennom og oppdater kriteriene i **Relevansregler**-fanen etter behov. Verdien i **Kanal**-feltet må være lik verdien du angav i **Datakanal**-feltet i det forrige trinnet.
11. Velg **Lagre**, og lukk siden.
