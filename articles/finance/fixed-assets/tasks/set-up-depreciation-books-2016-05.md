---
title: Definere avskrivningstablåer
description: Denne fremgangsmåten går gjennom prosessen med å opprette et nytt avskrivningstablå og knytte det til en anleggsmiddelgruppe.
author: moaamer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 42b8a15ac60fd2620c600d78b84a25e3caf6d2bf
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883626"
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
