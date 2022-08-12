---
title: Aktivere Power BI for Globalt lagerregnskap
description: Denne artikkelen beskriver hvordan du aktiverer Microsoft Power BI for Globalt lagerregnskap.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b1edfa314d2810bff4cf02762aeb66bee801858d
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135436"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>Aktivere Power BI for Globalt lagerregnskap

[!include [banner](../includes/banner.md)]

Du kan feste fliser, instrumentbord og rapporter fra [PowerBI.com](https://powerbi.com/)-kontoen til Microsoft Dynamics 365-arbeidsområdet.

## <a name="prerequisites"></a>Forutsetninger

Følgende forutsetninger må være på plass før du kan aktivere Power BI-rapportering:

- Du må være systemadministrator i Dynamics 365-programmet.
- Du må ha en [PowerBI.com](https://powerbi.com/)-konto.
- Du må ha minst ett instrumentbord og én rapport i Power BI-kontoen.
- Du må ha administratorrettigheter til Azure Active Directory-kontoen (Azure AD).
- Domenet Azure AD må være det samme domenet som du brukte for [PowerBI.com](https://powerbi.com/)-kontoen.

## <a name="setup"></a>Installasjon

Gjør følgende for å konfigurere Power BI-integrasjonen.

1. Logg på [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. Gå til **Delt aktivabibliotek**, velg **Power BI-rapportmodell** som anleggsmiddeltype, og last ned pakken **Globalt lagerregnskap**. 
1. Logg deg på [PowerBI.com](https://app.powerbi.com/), og last opp rapportfilen for **Globalt lagerregnskap** Power BI ved å følge denne fremgangsmåten:

    1. Velg **Ny**.
    1. Velg **Last opp en fil**.
    1. Velg rapportfilen for **Globalt lagerregnskap** Power BI.

1. Konfigurer Power BI-rapporten for **Globalt lagerregnskap** ved å følge denne fremgangsmåten:

    1. Gå til **Mitt arbeidsområde**, finn datasettet for Globalt lagerregnskap, og velg deretter **Innstillinger** på **Alternativer**-menyen.
    1. I **Innstillinger for Globalt lagerregnskap** utvider du **Parametere** og oppdaterer alle parametere etter behov. Pass særlig på at du kontrollerer følgende innstillinger:
        1. Overskrif standardverdiene for **URL-adresse for Dataverse** ved å bruke verdiene under **Informasjon om Power Platform-miljøet** i LCS (i delen **Power Platform-integrering**).
        1. Overskriv standardverdiene for **Miljø-ID** ved å bruke verdiene under **Miljødetaljer** i LCS (i delen **Administrer miljø**).
        1. Velg koblingen **Rediger legitimasjon** ved siden av **CDS**-etiketten i delen **Datakildelegitimasjon**. Logg deg deretter på Dataverse-kontoen ved hjelp av **OAuth2**-godkjenningsmetoden.
    1. Kontroller at Power BI-rapportene som finnes under **Mitt arbeidsområde \> Rapporter \> Globalt lagerregnskap** nå fungerer som de skal, og viser innhold fra systemet.

1. Registrer programmet som beskrevet i [Konfigurere PowerBI.com-integrering](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).
1. Integrer Power BI-rapportfilen for **Globalt lagerregnskap** i Dynamics 365 Supply Chain Management ved å følge denne fremgangsmåten:

    1. Gå til **Systemadministrasjon \> Oppsett \> PowerBI.com-konfigurasjon**.
    1. Velg **Rediger**.
    1. Velg **Aktiver PowerBI.Com-integrering**.
    1. I feltet **Program-ID** angir du program-IDen.
    1. I feltet **Programnøkkel** angir du programnøkkelen.
    1. Velg **Lagre**.

1. Oppdater siden slik at Power BI-påloggingsdialogboksen vises.
1. Velg **Åpne rapportkatalog** i kategorien **Alternativer**, og velg deretter Power BI-rapportfilen for **Globalt lagerregnskap** som du lastet opp tidligere.
1. Oppdater siden. Du skal se at rapporten er lagt til.
1. Under **Power BI-rapporter** velger du koblingen **Globalt lagerregnskap**.

Hvis du vil ha mer informasjon, se [Konfigurere PowerBI.com-integrasjon](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).
