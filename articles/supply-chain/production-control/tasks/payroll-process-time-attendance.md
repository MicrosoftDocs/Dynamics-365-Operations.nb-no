---
title: Aktivere lønnsprosessen for timeregistrering
description: Denne fremgangsmåten viser hvordan du aktiverer lønnsprosessen for timeregistrering.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a52ad77d3f03898d26c225900fe79ca30493a67
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843535"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>Aktivere lønnsprosessen for timeregistrering

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du aktiverer lønnsprosessen for timeregistrering. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>Opprette en lønnstype med en relatert lønnssats
1. Timeregistrering > Oppsett > Lønn > Lønnstyper
2. Klikk Ny.
3. Skriv inn en verdi i Lønnstype-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk Lagre.
6. Klikk Satser.
    * Satser for lønnstyper defineres for bestemte tidsintervaller, og enkeltstående satser kan opprettes for ansatte. Det er ikke alltid nødvendig å opprette satser for lønnstyper i timeregistrering. Denne informasjonen kan allerede finnes i lønnssystemet som brukes til å generere lønn.  
7. Klikk Ny.
8. Merk den valgte raden i listen.
9. Angi et tall i Sats-feltet.
10. Klikk Lagre.

## <a name="create-a-pay-agreement"></a>Opprette en lønnsavtale
1. Lukk siden.
2. Lukk siden.
3. Gå til Lønnsavtaler.
    * Timeregistrering > Oppsett > Lønnsavtaler  
4. Klikk Ny.
5. Skriv inn en verdi i Lønnsavtale-feltet.
6. Skriv inn en verdi i feltet Beskrivelse.
7. Klikk Lagre.
8. Klikk Avtalelinjer.
9. Klikk Ny.
10. Merk den valgte raden i listen.
11. Angi eller velg en verdi i Profiltype-feltet.
12. Angi eller velg en verdi i Lønnstype-feltet.

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>Sette opp lønnsavtale for tid og registrering for arbeider
1. Lukk siden.
2. Lukk siden.
3. Gå til Tidsregistreringsarbeidere.
    * Timeregistrering > Oppsett > Tidsregistreringsarbeidere  
4. Klikk koblingen i den valgte raden i listen.
5. Klikk kategorien Ansettelse.
6. Utvid delen Tidsregistrering.
7. Klikk Rediger.
8. Angi eller velg en verdi i Lønnsavtale-feltet.

