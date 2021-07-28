---
title: Oppsett av dobbel skriving fra Lifecycle Services
description: Dette emnet forklarer hvordan du konfigurerer en tilkobling med dobbel skriving fra Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e604e1491bbafa041fa3f52ad0f8b454c63d47de
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359369"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Oppsett av dobbel skriving fra Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet forklarer hvordan du aktiverer dobbel skriving fra Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Forutsetninger

Du må fullføre Power Platform-integreringen som beskrevet i følgende emner:

+ [Power Platform-integrering - Aktiver under miljødistribusjon](../../power-platform/overview.md#enable-during-environment-deployment)
+ [Power Platform-integrering - Konfigurere etter miljødistribusjon](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Konfigurere dobbel skriving for nye Dataverse-miljøer

Følg denne fremgangsmåten for å konfigurere en dobbelt skriving fra LCS-siden **Miljødetaljer**:

1. På siden **Miljødetaljer** utvides delen **Power Platform-integrering**.

2. Velg knappen for **App med dobbel skriving**.

    ![Power Platform-integrering.](media/powerplat_integration_step2.png)

3. Gå gjennom vilkårene og betingelsene, og merk deretter av for **Konfigurer**.

4. Velg **OK** for å fortsette.

5. Du kan overvåke fremdriften ved å oppdatere siden med miljødetaljer regelmessig. Oppsettet tar vanligvis 30 minutter eller mindre.  

6. Når installasjonen er fullført, får du en melding om prosessen var vellykket eller om det oppstod en feil. Hvis installasjonen mislyktes, vises det en relatert feilmelding. Du må korrigere eventuelle feil før du går til neste trinn.

7. Velg **Koble til Power Platform-miljø** for å opprette en kobling mellom Dataverse og databasene for det gjeldende miljøet. Dette tar vanligvis 5 minutter eller mindre.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Koble til Power Platform-miljø.":::

8. Når koblingen er fullført, vises en hyperkobling. Bruk koblingen til å logge deg på administrasjonsområdet for dobbel skriving i Finance and Operations-miljøet. Derfra kan du definere enhetstilordninger.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Konfigurere dobbel skriving for et eksisterende Dataverse-miljø

Hvis du vil definere skrivetilgang for et eksisterende Dataverse-miljø, må du opprette en Microsoft [støtteforespørsel](../../lifecycle-services/lcs-support.md). Denne forespørselen må inneholde følgende:

+ Finance and Operations-miljø-ID.
+ Miljønavnet fra Lifecycle Services.
+ Dataverse-organisasjons-IDen eller Power Platform-miljø-IDen fra Power Platform-administrasjonssenteret. Be om at IDen er forekomsten som brukes for Power Platform-integrering, i forespørselen.

> [!NOTE]
> Du kan ikke koble fra miljøer ved hjelp av LCS. Hvis du vil oppheve koblingen til et miljø, åpner du arbeidsområdet **Dataintegrering** i Finance and Operations-miljøet, og deretter velger du **Koble fra**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
