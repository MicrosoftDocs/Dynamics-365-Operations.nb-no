---
title: Konfigurere en arbeider som bruker den mobile jobbenheten
description: Denne prosedyren viser hvordan du kan tilordne riktige roller til brukerkontoen til en arbeider, og deretter la arbeideren foreta registreringer med Shop Floor.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bb4d806810660e55ef13a9ff21c07e0ce194496
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "327395"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Konfigurere en arbeider som bruker den mobile jobbenheten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren viser hvordan du kan tilordne riktige roller til brukerkontoen til en arbeider, og deretter la arbeideren foreta registreringer med Shop Floor.


## <a name="assign-roles-to-user-account"></a>Tilordne roller til brukerkonto
1. Gå til Systemadministrasjon > Brukere > Brukere.
2. Bruke hurtigfilteret til å filtrere på navnet på en arbeider der brukerkontoen er knyttet til maskinoperatørrollen. I eksempeldataene er navnet Shannon.
3. Merk brukerkontooppføringen.
4. Klikk koblingen Navn i den merkede raden i listen for å vise detaljene om brukerkontoen.
5. Velg Roller\Maskinoperatør i treet.
6. Lukk siden med brukerkontodetaljer.
7. Lukk siden.

## <a name="configure-worker-account"></a>Konfigurer brukerkontoen.
1. Gå til Personale > Arbeidere > Arbeidere.
2. Bruke hurtigfilteret til å filtrere på navnet på en arbeider der brukerkontoen er knyttet til maskinoperatørrollen. I eksempeldataene er navnet Shannon.
3. Merk brukerkontooppføringen.
4. Klikk koblingen Navn i den merkede raden i listen for å vise detaljene om brukerkontoen.
5. Klikk kategorien Ansettelse.
6. Utvid hurtigfanen Tidsregistrering og klikk Aktiver på registreringsterminaler.
7. Klikk Aktiver på registreringsterminaler.
8. Angi eller velg en verdi i Beregningsgruppe-feltet.
9. Angi eller velg en verdi i feltet Standard beregningsgruppe.
10. Angi eller velg en verdi i Godkjenningsgruppe-feltet.
11. Angi eller velg en verdi i Godkjenningsgruppe-feltet.
12. Angi eller velg en verdi i Profilgruppe-feltet.
13. Klikk OK.
14. Klikk Rediger for å angi et kortnummer for den nye tidsregistreringsarbeideren.
15. Skriv inn en verdi i feltet Kort-ID.
16. Klikk Lagre.
17. Bruk snarveien for å lagre posten.
18. Lukk siden med arbeiderdetaljene.
19. Lukk siden.

## <a name="assign-worker-to-device-group"></a>Tilordne arbeider til enhetsgruppe.
1. Gå til Produksjonskontroll > Oppsett > Produksjonsutførelse > Konfigurer jobbkort for enheter.
2. Klikk Legg til.
3. Merk den valgte raden i listen.
4. Klikk OK.
5. Klikk Rediger.
6. Du kan angi standardfilteret for arbeideren i Produksjonsenhet-feltet. Dette sikrer at bare produksjonsjobber for den valgte produksjonsenheten vises når arbeideren logger på enheten.
7. Lukk siden.

