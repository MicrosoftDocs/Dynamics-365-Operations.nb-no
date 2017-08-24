--- 
title: Behandle finansfordelingsjournal
description: "Bruk siden Behandle tildelingsforespørsel for å opprette en tildelingsjournal som kan du kan vurdere og godkjenne før du posterer den til økonomimodul, eller posterer direkte til økonomimodul."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 1189ffeae052c72542b3b403a6b7a6e415b005c4
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="process-ledger-allocation-journal"></a>Behandle finansfordelingsjournal

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bruk siden Behandle tildelingsforespørsel for å opprette en tildelingsjournal som kan du kan vurdere og godkjenne før du posterer den til økonomimodul, eller posterer direkte til økonomimodul. Før du kan opprette en tildelingsjournal, må det være minst én aktiv tildelingsregel for finans. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. Gå til Økonomimodul > Tildelinger > Behandle tildelingsforespørsel.
2. Klikk rullegardinknappen i feltet Regel for å åpne oppslaget.
3. Finn og velg ønsket post i listen.
4. Klikk koblingen i den valgte raden i listen.
5. Angi en dato i Per dato-feltet.
    * Per dato er svært viktig når finans er datakilden for regelen. Denne datoen kontrollerer hvilke finanssaldoer som skal inkluderes i tildelingen.     Velg Stopp i Nullkilde-feltet. Dette vil stanse tildelingsprosessen og vise en melding som indikerer at et nullbeløp er valgt.  
6. I feltet Forslagsalternativer velger du "Bare forslag".
    * Velg Bare forslag for å se gjennom og eventuelt godkjenne resultatet i tildelingsjournaler før postering av tildelingen til økonomimodulen.  
7. Angi en dato i feltet FIN-posteringsdato.
8. Klikk OK.
9. Gå til Økonomimodul > Tildelinger > Tildelingsjournaler.
10. Klikk Linjer.
11. Klikk Poster.
12. Klikk Poster.


