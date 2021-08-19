---
title: Definere avskrivningstablåer
description: Denne fremgangsmåten går gjennom prosessen med å opprette et nytt avskrivningstablå og knytte det til en anleggsmiddelgruppe.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 722eebf363b6abf0d72ea3f1f891292a6577616165df9dae91dac917587fe490
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713786"
---
# <a name="set-up-depreciation-books"></a>Definere avskrivningstablåer 

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten går gjennom prosessen med å opprette et nytt avskrivningstablå og knytte det til en anleggsmiddelgruppe. 

## <a name="create-a-depreciation-book"></a>Opprette et avskrivningstablå
1. Gå til Anleggsmidler > Oppsett > Avskrivningstablåer.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Avskrivningstablå.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Merk av eller fjern merket i boksen Beregn avskrivning.
6. Klikk rullegardinknappen i feltet Avskrivningsprofil for å åpne oppslaget.
7. Finn og velg ønsket avskrivningsprofil i listen.
8. Klikk koblingen i den valgte raden i listen.
9. Klikk rullegardinknappen i feltet Alternativ avskrivningsprofil for å åpne oppslaget.
10. Velg ønsket avskrivningsprofil i listen.
11. Klikk koblingen i den valgte raden i listen.
    * Den ekstraordinære avskrivningsprofilen brukes til ytterligere avskrivning av et aktiva i uvanlige omstendigheter. Du kan for eksempel bruke denne til å registrere avskrivning som skyldes en naturkatastrofe.  
12. Merk av eller fjern merket i boksen Opprett avskrivningsjusteringer med basisjusteringer.
13. Klikk rullegardinknappen i Kalender-feltet for å åpne oppslaget.
14. Klikk koblingen i den valgte raden i listen.

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a>Knytte avskrivningstablået til en anleggsmiddelgruppe
1. Klikk Anleggsmiddelgrupper.
2. Klikk rullegardinknappen i feltet Anleggsmiddelgruppe for å åpne oppslaget.
3. Finn og velg ønsket post i listen.
4. Klikk koblingen i den valgte raden i listen.
5. Velg et alternativ i feltet Avskrivningskonvensjon.
6. Angi et tall i Levetid-feltet.
    * Legg merke til at verdien i feltet Avskrivningsperioder beregnes etter at levetiden er angitt.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]