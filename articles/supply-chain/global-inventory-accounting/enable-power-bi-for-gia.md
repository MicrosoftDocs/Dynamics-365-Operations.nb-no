---
title: Aktivere Power BI for Globalt lagerregnskap
description: Dette emnet beskriver hvordan du aktiverer Microsoft Power BI for Globalt lagerregnskap.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273203"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>Aktivere Power BI for Globalt lagerregnskap

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

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
    1. I **Innstillinger for Globalt lagerregnskap** utvider du **Parametere** og oppdaterer alle parametere etter behov.

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
