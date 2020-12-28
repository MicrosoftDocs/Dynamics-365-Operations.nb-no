---
title: Attract-brukere kan ikke søke på jobber fra karriereportalen
description: Dette emnet forklarer hvordan du feilsøker et problem der Attract-brukere ikke kan søke på jobber fra karriereportalen.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462080"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a>Attract-brukere kan ikke søke på jobber fra karriereportalen

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Problem

Attract-brukere kan ikke søke på jobber fra karriereportalen. Når de prøver å søke på en jobb som ble opprettet i Dynamics 365 Talent: Attract, laster nettleseren inn siden kontinuerlig og fullfører ikke handlingen.

## <a name="cause"></a>Årsak

Dette problemet oppstår når talentrelasjonsteamet ikke har Talentbruker-rolle.

## <a name="resolution"></a>Oppløsning

Tilordne Talentbruker-rollen til talentrelasjonsteamet.

1. Logg på [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com) med en av følgende administratorlegitimasjoner:

   - Dynamics 365-administrator
   - Global administrator
   - Power Platform-administrator

2. I navigasjonsruten velger du **Miljøer**, og deretter velger du miljøet som Talentbruker-rollen til talentrelasjonsteamet skal tilordnes til.

   ![Velg miljø](./media/attract-troubleshoot-career-portal-select-environment.png)

3. I **Miljøer**-ruten velger du **URL-adressen for miljø** og logger på administrasjonsportalen for miljøet (for eksempel https:<orgname>.crm.dynamics.com).

4. Velg **Innstillinger**, velg **System** og velg deretter **Sikkerhet**.

   ![Gå til Sikkerhet](./media/attract-troubleshoot-career-portal-security.png)

5. Velg **Team**.

   ![Velg Team](./media/attract-troubleshoot-career-portal-security-teams.png)

6. Søk etter **talentrelasjonsteam** i søkefeltet, og velg deretter teamet fra søkeresultatene.

7. Velg **ADMINISTRER ROLLER** fra båndet.

8. I dialogen **Administrer teamroller** velger du **Talentbruker** fra listen over tilgjengelige roller, og deretter velger du **OK** for å bruke rollen.

   ![Bruk rolle](./media/attract-troubleshoot-career-portal-apply-role.png)

9. Test endringene:

   1. Logg deg på karriereportalen fra et nytt nettleservindu.
   2. Søk på jobben fra karriereportalen. 