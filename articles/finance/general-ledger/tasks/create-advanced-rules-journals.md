---
title: Opprette avanserte regler for journaler
description: Denne fremgangsmåten viser hvordan du oppretter avanserte regler for journaler.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c06855c7a7648c5829b90bc548a7d2e400967698
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988608"
---
# <a name="create-advanced-rules-for-journals"></a>Opprette avanserte regler for journaler

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter avanserte regler for journaler. Dette omfatter definering av journalkontroll og brukerposteringsrestriksjoner. Denne prosedyren bruker demonstrasjonsdatafirmaet USMF.


## <a name="set-up-journal-control"></a>Definere journalkontroll
1. I **navigasjonsruten** går du til **Moduler > Økonomimodul > Journaloppsett > Journalnavn**.
2. Finn og velg ønsket post i listen.
3. Klikk **Journalkontroll** i **handlingsruten**.
4. Klikk **Legg til** i hurtigfanen **Hvilke kontotyper kan posteres?**
5. Klikk rullegardinknappen i feltet **Firmakontoer** for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
7. Klikk koblingen i den valgte raden i listen.
8. Klikk **Legg til** i hurtigfanen **Hvilke segmentverdier er gyldige for denne journalen?**
9. Klikk rullegardinknappen i feltet **Kontostruktur** for å åpne oppslaget.
10. Finn og velg ønsket post i listen.
11. Klikk koblingen i den valgte raden i listen.
12. Klikk rullegardinknappen i feltet **Segment** for å åpne oppslaget.
13. Klikk koblingen i den valgte raden i listen.
14. Klikk rullegardinknappen i feltet **Fra verdi** for å åpne oppslaget.
15. Finn og velg ønsket post i listen.
16. Klikk koblingen i den valgte raden i listen.
17. Klikk rullegardinknappen i feltet **Til verdi** for å åpne oppslaget.
18. Finn og velg ønsket post i listen.
19. Klikk koblingen i den valgte raden i listen.

## <a name="set-up-posting-restrictions"></a>Definere posteringsrestriksjoner
1. Lukk siden.
2. Klikk **Posteringsrestriksjoner**.
3. Velg Etter brukergruppe i feltet **Hvordan vil du konfigurere posteringsrestriksjoner?**
4. Merk av for gruppen som du vil tillate postering for dette journalnavnet for, i treet.
5. Klikk **OK**.

