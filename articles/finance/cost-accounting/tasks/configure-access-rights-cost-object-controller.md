---
title: Konfigurere tilgangsrettigheter for en kontroller for kostnadsobjekt
description: Bruk denne prosedyren til å konfigurere tilgangsrettigheter for en kontroller for kostnadsobjekt.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eef755dd9a44ce24d3bfb2953cf9a52e6a8ac849
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822885"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a>Konfigurere tilgangsrettigheter for en kontroller for kostnadsobjekt

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]