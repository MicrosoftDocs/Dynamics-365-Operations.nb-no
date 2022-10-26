---
title: Installere Invoice Capture-løsningen
description: Denne artikkelen gir informasjon om hvordan du installerer Invoice capture-løsningen og integrere den med Microsoft Dynamics 365 Finance.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: d853e347c833345f34b65760fd7ee35cbb38c9a3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691229"
---
# <a name="install-the-invoice-capture-solution"></a>Installere Invoice Capture-løsningen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Hvis du installerte løsningen i privat forhåndsvisning, må du avinstallere den gamle løsningen før du fortsetter.

## <a name="prerequisites"></a>Forutsetninger

Før du kan installere Invoice capture-løsningen må du ha oppfylt følgende forutsetninger:

1. Registrer programmet og legg til en klienthemmelighet i Microsoft Azure Active Directory (Azure AD) under Azure-abonnementet ditt. Hvis du vil ha mer informasjon, kan du se [Registrere en webapp med AAD](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad).

    > [!NOTE]
    > Skriv ned verdiene for **App-ID (klient)**, **Klienthemmelighet** og **Leier-ID**, siden du trenger dem senere.

2. Registrere Azure-programmet i et Dynamics 365 Finance-miljø. Hvis du vil ha mer informasjon, kan du se [Registrere den eksterne appen](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application).

## <a name="install-and-set-up-the-solution"></a>Installere og definere løsningen

Hvis du vil installere Invoice capture-løsningen, kan du gå til AppSource og velge koblingen for forhåndsvisningsversjonen av [Dynamics 365 Invoice capture](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture). Når installasjonen er fullført, vil du se løsningen installert i det valgte miljøet i Power Apps.

Følg fremgangsmåten nedenfor for å fullføre oppsettet.

1. Last ned [assistentløsningen](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip) for å konfigurere følgende detaljer:

    - Kommunikasjonen mellom Microsoft Power Platform og Finance-miljøet
    - Tilkoblingsreferansen for Dataverse og Office 365 Outlook som skal brukes av kanalen

2. I Power Apps går du til miljøet, og velg **Importer løsning**.
3. Velg **Bla gjennom**, velg assistentløsningspakken du lastet ned, og velg deretter **Neste**.
4. Velg **Neste**.
5. Tilordne en eksisterende tilkobling, eller opprett en ny ved å velge **Ny tilkobling**.
6. Når pakken er importert, åpner du **Dynamics 365 Invoice capture – installasjonsverktøy**.
7. Kjør skyflyten for å sette opp koblingen mellom Invoice capture-løsningen i Microsoft Power Platform og Finance.
8. Velg **Kjør**, og angi følgende parametere:

    - **Dynamics 365 Finance-URL-adresse** – Url-adressen til Finance-miljøet du vil integrere med.
    - **Leier-ID** – Leier-IDen for Finance-miljøet.
    - **Klient-ID** – Azure-program-IDen som ble registrert.
    - **Klienthemmelighet** – Klienthemmeligheten som ble generert for Azure-programmet.
