--- 
title: Konfigurere en arbeider som bruker den mobile jobbenheten
description: Denne prosedyren viser hvordan du kan tilordne riktige roller til brukerkontoen til en arbeider, og deretter la arbeideren foreta registreringer med Shop Floor.
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 7da224809946d90387668d25c5aed5b61f6a7b72
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Konfigurere en arbeider som bruker den mobile jobbenheten

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


