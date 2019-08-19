---
title: Konfigurere en arbeider som bruker den mobile jobbenheten
description: Dette emnet viser hvordan du kan tilordne riktige roller til brukerkontoen til en arbeider, og deretter la arbeideren foreta registreringer med Shop Floor.
author: ShylaThompson
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6e45ea8fdbe30436badd88d4972fda970755275
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835786"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Konfigurere en arbeider som bruker den mobile jobbenheten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emnet viser hvordan du kan tilordne riktige roller til brukerkontoen til en arbeider, og deretter la arbeideren foreta registreringer med Shop Floor.

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a>Kontrollere at en arbeider er tilordnet en bestemt rolle

I dette eksemplet må du kontrollere at brukeren "SHANNON" er tilordnet maskinoperatørrollen før du konfigurerer arbeiderkontoen.

1. Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Brukere > Brukere**.
2. Søk etter en bruker i hurtigfilteret. I dette eksemplet angir du `shannon`.
3. Velg koblingen i kolonnen **bruker-ID** for brukerkontoen som vises.
4. I **Brukerroller**-treet velger du **Roller > Maskinoperatør**.
5. Lukk sidene **Brukerdetaljer** og **Brukere** for å gå tilbake til hjemmesiden.

## <a name="configure-worker-account"></a>Konfigurere brukerkonto
1. Gå til **Navigasjonsrute > Moduler > Personale > Arbeidere > Arbeidere**.
2. Søk etter en bruker i hurtigfilteret. I dette eksemplet angir du `shannon`.
3. Velg koblingen i kolonnen **Navn** for brukerkontoen som vises.
4. Velg kategorien **Tidsregistrering**.
5. Velg **Aktiver på registreringsterminaler**.
6. Angi eller velg verdier i følgende felt:  

    - **Beregningsgruppe**  
    - **Standard beregningsgruppe**  
    - **Godkjenningsgruppe**  
    - **Standardprofil**  
    - **Profilgruppe**  

7. Velg **OK**.
8. Velg **Rediger** for å angi et kortnummer for den nye tidsregistreringsarbeideren. Angi en verdi i feltet **Kort-ID**.
9. Velg **Lagre**.
10. Lukk sidene **Arbeiderdetaljer** og **Arbeidere**.

## <a name="assign-worker-to-device-group"></a>Tilordne arbeider til enhetsgruppe
1. Gå til **Produksjonskontroll > Oppsett > Produksjonsutførelse > Konfigurer jobbkort for enheter**.
2. Velg **Legg til**.
3. Velg ønsket arbeider i listen. I dette eksemplet velger du **SHANNON**.
4. Velg **OK**.
5. Velg **Rediger**.
6. Du kan angi standardfilteret for arbeideren i **Produksjonsenhet**-feltet. Dette sikrer at bare produksjonsjobber for den valgte produksjonsenheten vises når arbeideren logger på enheten. Angi den ønskede verdien.
7. Lukk siden.

