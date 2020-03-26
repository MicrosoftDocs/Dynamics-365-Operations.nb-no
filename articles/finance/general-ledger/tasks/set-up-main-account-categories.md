---
title: Definere hovedkontokategorier
description: Dette emnet forklarer hvordan du definerer hovedkontokategorier i Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1fabdcd61c60e630e3f32bc4f0c13c44f50259a6
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091928"
---
# <a name="set-up-main-account-categories"></a>Definere hovedkontokategorier

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emnet forklarer hvordan du definerer hovedkontokategorier. Hovedkontokategorier brukes til standardrapportene i finansiell rapportering og Power BI. Hovedkontokategorier som opprettes som standard kan gis nytt navn, men ikke slettes. Flere kontokategorier kan opprettes og brukes for rapportering og analyse. Dette emnet bruker demonstrasjonsfirmaet USMF.

## <a name="create-a-main-account-category"></a>Opprette en hovedkontokategori
1. I navigasjonsruten går du til **Moduler > Økonomimodul > Kontoplan > Kontoer > Hovedkontokategorier**.
2. Velg **Ny**.
3. Angi et unikt navn i feltet **Hovedkontokategori**.
4. Angi en beskrivelse for hovedkontokategorien i feltet **Beskrivelse**.
5. Velg typen hovedkonto som skal knyttes til kategorien i feltet **Hovedkontotype**.

## <a name="link-main-accounts-to-account-category"></a>Koble hovedkontoer til kontokategori
1. Klikk **Koble hovedkontoer**.
2. I listen velger du hovedkontoene som skal tilordnes til hovedkontokategorien, ved å merke av boksene i **Koblet**-kolonnen. Når du tilordner hovedkontoer til en hovedkontokategori, samles saldoene for kontoene når denne kategorien brukes til økonomisk rapportering og analyse.  
3. Aktiver eller deaktiver alternativet **Koblet** for å velge hovedkontoene.
4. Velg **OK**.
5. Velg **Ja**.
