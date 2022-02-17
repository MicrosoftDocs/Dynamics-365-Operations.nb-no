---
title: Konfigurer kompensasjonsrutenett
description: Kompensasjonsrutenett brukes til å definere og vedlikeholde lønn-strukturer for faste kompensasjonsplaner.
author: twheeloc
ms.date: 01/03/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51b98320eac539e49787d352f32683efadc11f41
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071518"
---
# <a name="set-up-compensation-grids"></a>Konfigurer kompensasjonsrutenett


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kompensasjonsrutenett brukes til å definere og vedlikeholde lønn-strukturer for faste kompensasjonsplaner. Kompensasjonsrutenett kan deles mellom flere planer eller kopieres når du oppretter en ny kompensasjonsplan.  Før du oppretter et kompensasjonsrutenett må nivåer og referansepunkt være definert. Dette eksemplet oppretter en ny klasse-type for kompensasjonsrutenettet ved hjelp av demodata for nivåene og referansepunktene. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="set-up-information-about-the-compensation-grid"></a>Definere informasjon om kompensasjonsrutenettet
1. Gå til **Personale** > **Kompensasjon** > **Fast kompensasjon** > **Kompensasjonsrutenett**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i feltet **Rutenett**.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Velg et alternativ i **Type**-feltet.
6. Angi eller velg en verdi i oppsettfeltet **Referanse**.
7. Angi eller velg en verdi i **Valuta**-feltet.
8. Angi en dato i feltet **Gyldighetsdato**.

## <a name="add-levels-to-the-compensation-structure"></a>Legge til nivåer i kompensasjonsstrukturen
1. Klikk **Kompensasjonsstruktur**.
2. Merk den valgte raden i listen.
3. Angi eller velg en verdi i feltet **Nivå**.
4. Klikk på **Ny**.
5. Merk den valgte raden i listen.
6. Angi eller velg en verdi i feltet **Nivå**.
7. Klikk på **Ny**.
8. Merk den valgte raden i listen.
9. Angi eller velg en verdi i feltet **Nivå**.
10. Klikk på **Ny**.
11. Merk den valgte raden i listen.
12. Angi eller velg en verdi i feltet **Nivå**.
13. Klikk på **Ny**.
14. Merk den valgte raden i listen.
15. Angi eller velg en verdi i feltet **Nivå**.

## <a name="fill-in-the-compensation-structure-with-values"></a>Fylle ut kompensasjonsstrukturen med verdier
1. Merk den valgte raden i listen.
    * Nå kan kompensasjonsverdiene settes inn manuelt i hvert felt i tabellen, eller masseendringsfunksjonaliteten kan brukes til å enkelt fylle ut flere felt og utføre enkle beregninger.  
2. Klikk **Masseendring**.
    * Vi vil først bruke verdien for midtpunktet i det første nivået for dette rutenettet på alle feltene i tabellen. Dette vil være grunnlaget for kompensasjonsmatrisen.  
3. Velg et alternativ i feltet **Justeringstype**.
4. Angi et tall i **Justeringsbeløp**-feltet.
5. Merk eller fjern merking for alle rader i listen.
6. Klikk **Bruk på rutenett**.
    * Nå skal vi bruke masseendringsfunksjonen til å øke beløpene i hvert etterfølgende nivå med en bestemt prosent eller beløp. I dette eksemplet skal hver klasse en 12,5 % spredning mellom midtpunktene.  
7. Velg et alternativ i feltet **Justeringstype**.
8. Angi et tall i **Justeringsbeløp**-feltet.
9. Finn og velg ønsket post i listen.
10. Klikk **Bruk på rutenett**.
    * Nå skal vi bruke masseendringsfunksjonen til å justere Minimum og maksimum referansepunkt for hvert nivå. Dette eksemplet bruker en 50 % spredning slik Minimum referansepunkt blir justert -20 % og maksimalt blir justert +20 %.  
11. Angi et tall i **Justeringsbeløp**-feltet.
12. Angi eller velg en verdi i feltet **Referansepunkt**.
13. Merk eller fjern merking for alle rader i listen.
14. Klikk **Bruk på rutenett**.
15. Angi et tall i **Justeringsbeløp**-feltet.
16. Angi eller velg en verdi i feltet **Referansepunkt**.
17. Merk eller fjern merking for alle rader i listen.
18. Klikk **Bruk på rutenett**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
