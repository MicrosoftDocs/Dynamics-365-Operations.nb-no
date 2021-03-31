---
title: Aktivere lønnsprosessen for timeregistrering
description: Denne fremgangsmåten viser hvordan du aktiverer lønnsprosessen for timeregistrering.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72b925feb8f784c257656dd93b48c9c0cc66da5e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214920"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>Aktivere lønnsprosessen for timeregistrering

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du aktiverer lønnsprosessen for timeregistrering. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>Opprette en lønnstype med en relatert lønnssats
1. Timeregistrering > Oppsett > Lønn > Lønnstyper
2. Klikk på Ny.
3. Skriv inn en verdi i Lønnstype-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk på Lagre.
6. Klikk på Satser.
    * Satser for lønnstyper defineres for bestemte tidsintervaller, og enkeltstående satser kan opprettes for ansatte. Det er ikke alltid nødvendig å opprette satser for lønnstyper i timeregistrering. Denne informasjonen kan allerede finnes i lønnssystemet som brukes til å generere lønn.  
7. Klikk på Ny.
8. Merk den valgte raden i listen.
9. Angi et tall i Sats-feltet.
10. Klikk på Lagre.

## <a name="create-a-pay-agreement"></a>Opprette en lønnsavtale
1. Lukk siden.
2. Lukk siden.
3. Gå til Lønnsavtaler.
    * Timeregistrering > Oppsett > Lønnsavtaler  
4. Klikk på Ny.
5. Skriv inn en verdi i Lønnsavtale-feltet.
6. Skriv inn en verdi i feltet Beskrivelse.
7. Klikk på Lagre.
8. Klikk på Avtalelinjer.
9. Klikk på Ny.
10. Merk den valgte raden i listen.
11. Angi eller velg en verdi i Profiltype-feltet.
12. Angi eller velg en verdi i Lønnstype-feltet.

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>Sette opp lønnsavtale for tid og registrering for arbeider
1. Lukk siden.
2. Lukk siden.
3. Gå til Tidsregistreringsarbeidere.
    * Timeregistrering > Oppsett > Tidsregistreringsarbeidere  
4. Klikk på koblingen i den valgte raden i listen.
5. Klikk på fanen Ansettelse.
6. Utvid delen Tidsregistrering.
7. Klikk på Rediger.
8. Angi eller velg en verdi i Lønnsavtale-feltet.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]