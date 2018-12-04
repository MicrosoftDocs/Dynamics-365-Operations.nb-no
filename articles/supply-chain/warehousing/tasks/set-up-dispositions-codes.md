--- 
title: Definere disposisjonskoder
description: "Denne prosedyren fokuserer på oppsettet for en disposisjonskode som kan brukes på en mobil enhet for mottaksprosessen for returordren."
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c004543188656dfd53d7539717cd6e93d0b9f47a
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-dispositions-codes"></a>Definere disposisjonskoder

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren fokuserer på oppsettet for en disposisjonskode som kan brukes på en mobil enhet for mottaksprosessen for returordren. Disposisjonskoder er en samling regler som kan brukes når varer mottas. Når du arbeidet bruker en mobil enhet for å motta varer som har blitt skadet, må brukeren for eksempel skanne en disposisjonskode for skadede elementer. Beholdningsstatusen for mottatte varer, arbeidsmalen og lokasjonsdirektivet kan beregnes fra den skannede disposisjonskoden. For mottaksprosessen for bestilling og ferdigmeldingsprosessen for produksjonsordren er bruk av en disposisjonskode valgfritt. Hvis varene er registrert ved hjelp av en mobil enhet for mottaksprosessen for salgsordreretur, er bruken av disposisjonskoden obligatorisk.  Denne veiledningen ble opprettet med demonstrasjonsdatafirmaet USMF. Denne fremgangsmåten er ment for lagersjef. 

1. Gå til Lagerstyring > Oppsett > Mobilenhet > Disposisjonskoder.
2. Klikk Ny.
    * Opprett en ny disposisjonskode som skal brukes for kundereturer.  
3. Skriv inn en verdi i Disposisjonskode-feltet.
4. Velg en beholdningsstatus i Beholdningsstatus-feltet der det er lagerblokkering.
    * Hvis du bruker USMF, velger du Blokkering. Du kan legge til en beholdningsstatus i disposisjonskoden for å overstyre standardstatus på ordrelinjene.  
5. Angi en verdi i feltet Arbeidsmal.
    * Valgfritt: Velg en arbeidsmalkode som er tilknyttet en returordre. Hvis ingen verdi er angitt, blir arbeidsmalen løst ved hjelp av standardreglene som er konfigurert i systemet. Hvis du velger en mal for arbeid, begrenser du prosessene som denne disposisjonskoden kan brukes med. Hvis for eksempel en disposisjonskode er en mal for arbeid med en Arbeidsordre av typen Bestilling, kan den ikke brukes til å registrere varer som returneres av kunder.  
6. Skriv inn en verdi i Returdisposisjonskode-feltet.
    * Returdisposisjonskoden bestemmer resten av ordrereturprosessen for varene som er registrert. Kunden skal motta en kreditnota i dette eksemplet. Legg til en disposisjonskode for returer som inneholder en kredithandling.  


