---
title: Konfigurer tjeneste-til-tjeneste-godkjenning
description: Dette emnet beskriver hvordan du konfigurerer tjeneste-til-tjenestegodkjenning i Microsoft Dynamics 365 Commerce for sikker oppkalling av tjeneste-API-er for vurderinger og omtaler.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: da780de5f15d72bdac85a261eae809125c830260
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968522"
---
# <a name="configure-service-to-service-authentication"></a>Konfigurer tjeneste-til-tjeneste-godkjenning

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer tjeneste-til-tjenestegodkjenning (S2S) i Microsoft Dynamics 365 Commerce for sikker oppkalling av tjeneste-API-er for vurderinger og omtaler.

Dynamics 365 Commerce tilbyr [vurderinger og omtaler](ratings-reviews-overview.md) som en omnikanalløsning. Denne løsningen gir tilgang til tjeneste-API-er fra utenfor Commerce, slik at ulike oppgaver kan utføres. Disse oppgavene omfatter import av vurderinger og omtaler fra det eksterne systemet til Commerce, og eksport av vurderinger og omtaler fra Commerce. Hvis du vil aktivere Commerce til sikker oppkall av vurderinger og omtaler av tjeneste-API-er, må du først konfigurere S2S-godkjenning ved å fullføre prosedyrene i dette emnet.

## <a name="add-a-new-app-registration"></a>Legg til en ny appregistrering

Før du legger til en ny appregistrering, må du opprette en app ved hjelp av [Azure-portalen](https://portal.azure.com). Du registrerer en app i Azure Active Directory (Azure AD) og aktiverer godkjenning ved å følge trinnene i [bruk Azure Active Directory med en egendefinert kobling i Power Automate](/connectors/custom-connectors/azure-active-directory-authentication).

Samle inn følgende ID-er fra Azure-portalen. Du trenger disse ID-ene i trinnene som følger.

- ID for klientprogram
- ID for klientkatalog (leier)

Følg denne fremgangsmåten for å legge til en ny appregistrering i Commerce-områdebygger.

1. Gå til **Hjem \> Omtaler \> Innstillinger**.
1. Under **Tjeneste-til-tjeneste-godkjenning (S2S)** velger du **Administrer**.

    ![Administrer knappen i delen Tjeneste-til-tjeneste-godkjenning (S2S) i Commerce-områdebygger.](media/Ratings-reviews-settings-service-to-service-authentication.png)

1. I ruten **S2S-appoppføringer** som vises til høyre, velger du **Legg til en ny S2S-appregistrering**.
1. I dialogboksen **Legg til S2S-appregistrering** angir du følgende obligatoriske informasjon. Bruk verdiene fra Azure-appregistreringen.

    - **Navn** – Skriv inn navnet på appen (for eksempel **Fabrikam-app**).
    - **ID for klientapp** – Angi app-ID-en (for eksempel **00000000-0000-0000-0000-000000000000**).
    - **ID for katalog (leier)** – Angi katalog-ID-en (for eksempel **00000000-0000-0000-0000-000000000000**).

    ![Dialogboksen Legg til S2S-appregistrering i Commerce-områdebygger.](media/Ratings-reviews-settings-S2S-APP-entry.png)

1. Velg **Send**. Navnet på appen skal nå vises i listen i ruten **S2S-appoppføringer**.
1. Lukk ruten **S2S-appoppføringer**.
1. Velg **Lagre**.

## <a name="edit-an-existing-app-registration"></a>Rediger en eksisterende appregistrering

Følg denne fremgangsmåten for å redigere en eksisterende appregistrering i Commerce-områdebygger.

1. Gå til **Hjem \> Omtaler \> Innstillinger**.
1. Under **Tjeneste-til-tjeneste-godkjenning (S2S)** velger du **Administrer**.
1. I ruten **S2S-appoppføringer** velger du blyantsymbolet ved siden av oppføringen du vil redigere.
1. Oppdater verdier i feltene **Navn**, **ID for klientapp** og **ID for katalog (leier)** etter behov.
1. Velg **Send**.
1. Lukk ruten **S2S-appoppføringer**.
1. Velg **Lagre**.

## <a name="remove-an-existing-app-registration"></a>Fjern en eksisterende appregistrering

Følg denne fremgangsmåten for å fjerne en eksisterende appregistrering i Commerce-områdebygger.

1. Gå til **Hjem \> Omtaler \> Innstillinger**.
1. Under **Tjeneste-til-tjeneste-godkjenning (S2S)** velger du **Administrer**.
1. I ruten **S2S-appoppføringer** velger du papirkurvsymbolet ved siden av oppføringen du vil fjerne. Oppføringen fjernes fra listen.
1. Lukk ruten **S2S-appoppføringer**.
1. Velg **Lagre**.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Velge å bruke vurderinger og anmeldelser](opt-in-ratings-reviews.md)

[Administrere vurderinger og anmeldelser](manage-reviews.md)

[Konfigurere vurderinger og anmeldelser](configure-ratings-reviews.md)

[Synkronisere produktvurderinger](sync-product-ratings.md)

[Aktivere manuell publisering av vurderinger og vurderinger av en moderator](manual-publish-rating-reviews.md)

[Importer og eksporter vurderinger og omtaler](import-export-reviews.md)

[Vanlige spørsmål om rangeringer og anmeldelser](ratings-reviews-faq.md) 
