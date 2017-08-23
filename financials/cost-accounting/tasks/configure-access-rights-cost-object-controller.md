--- 
title: Konfigurere tilgangsrettigheter for en kontroller for kostnadsobjekt
description: "Bruk denne prosedyren til å konfigurere tilgangsrettigheter for en kontroller for kostnadsobjekt."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 9c5f79b7d9d62b29f21f2ddd1f6507ff82b381cc
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="configure-access-rights-for-a-cost-object-controller"></a>Konfigurere tilgangsrettigheter for en kontroller for kostnadsobjekt

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bruk denne prosedyren til å konfigurere tilgangsrettigheter for en kontroller for kostnadsobjekt. Denne registreringen bruker USP2-demodatafirmaet.


## <a name="assign-the-cost-object-controller-role"></a>Tilordne rollen Kontroller for kostnadsobjekt
1. Gå til Systemadministrasjon > Brukere > Brukere.
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Brukernavn-feltet med verdien 'alicia'.
3. Klikk koblingen i den valgte raden i listen.
4. Klikk Tilordne roller.
5. Finn og velg ønsket post i listen.
6. Klikk OK.

## <a name="enable-access-list-security"></a>Aktiver sikkerhet for tilgangsliste
1. Gå til Kostnadsregnskap > Dimensjoner > Dimensjonshierarkier.
2. Finn og velg ønsket post i listen.
    * Velg Organisasjon.  
3. Klikk Rediger.
4. Velg Ja i feltet Hierarki for tilgangsliste.
5. Klikk Vis hierarki.

## <a name="assign-access-rights-to-user"></a>Tilordne tilgangsrettigheter til bruker
1. Klikk Ny.
2. Merk den valgte raden i listen.
3. Angi eller velg en verdi i feltet Bruker-ID.
    * Velg Administrator.  
4. Velg 'Organisasjon\CEO\CFO\FIM' i treet.
5. Klikk Ny.
6. Merk den valgte raden i listen.
7. Angi eller velg en verdi i feltet Bruker-ID.
    * Velg Alicia.  
8. Klikk Lagre.

## <a name="enable-access-rights-in-cost-accounting"></a>Aktivere tilgangsrettigheter i kostnadsregnskap
1. Gå til Kostnadsregnskap > Oppsett > Parametere.
2. Klikk kategorien Generelt.
3. Velg Ja i feltet Aktiver visningstilgang for dimensjonsmedlemmer for kostnadsobjekt.
4. Klikk Lagre.
5. Lukk siden.
6. Gå til Kostnadsregnskap > Oppsett > Konfigurasjon av arbeidsområde for kostnadskontroll.
7. Klikk Rediger.
8. Velg Ja i feltet Publisert.
    * Hvis du velger Ja, kan en bruker som er tilordnet en av følgende fire roller se rapportene i kostnaden control arbeidsområdet: regnskapsansvarlig, regnskapsfører, regnskapsfører clerk og kostnader objekt kontrollert. Hvis du velger Nei, bare brukere som er tilordnet en av følgende roller kan se rapportene: kostnadsregnskap overordnede, regnskapsfører og regnskapsfører clerk.    
9. Klikk Lagre.


