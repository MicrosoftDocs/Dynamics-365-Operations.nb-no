--- 
title: Mva-tilordning og overstyringer
description: "Denne fremgangsmåten beskriver hvordan du tilordner mva-grupper til kanaler for detaljhandel."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 816e00e4238cb0d90a2aea9b2bc070d31504c2ce
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="sales-tax-assignment-and-overrides"></a>Mva-tilordning og overstyringer

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten beskriver hvordan du tilordner mva-grupper til kanaler for detaljhandel. Den veileder deg også gjennom oppretting av en ny mva-overstyring og tilordning av den til en eksisterende mva-overstyringsgruppe. Denne prosedyren

bruker demonstrasjonsdatafirmaet USRT.

1. Gå til Detaljhandel og handel > Kanaler > Detaljhandelbutikker > Alle detaljhandelsbutikker.
2. I listen klikker du koblingen ID for detaljhandelskanal for Houston.
3. Klikk Rediger.
    * Feltet Merverdiavgiftsgruppe inneholder en liste over merverdiavgiftsgrupper for gjeldende firma. Gjeldende tildelt gruppe er en generisk "Texas"-merverdiavgiftsgruppe. Det finnes også mva-grupper for "Washington" og "Washington, King County." Mva-grupper kan inneholde gjeldende avgifter for flere områder.  
    * Feltet Merverdiavgiftoverstyring er der merverdiavgiftoverstyringsgrupper kan tilordnes til kanalen. Merverdiavgiftoverstyringsgrupper kan brukes til å gruppere sammen merverdiavgiftoverstyringer som fungerer for flere butikker. I stedet for manuell, enkeltvis tilordning av merverdiavgiftoverstyringer, kan gruppen opprettes og tilordnes direkte til kanalene for å spare tid.  
4. Klikk Lagre.
5. Lukk siden.
6. Gå til Detaljhandel og handel > Kanaloppsett > Merverdiavgift > Mva-overstyringer.
7. Klikk Ny.
8. Angi et navn for den nye overstyringen i feltet Mva-overstyring.
9. Angi en kort beskrivelse av overstyringen i Beskrivelse-feltet.
10. Sett statusen til Aktiver.
11. Vis eller skjul delen Overstyr.
12. Velg et alternativ i Type-feltet.
    * Mva-grupper for vare kan brukes til å overstyre avgifter for bestemte varer som tilhører gruppen. Matvarer beskattes for eksempel vanligvis forskjellig fra fastvarer, og vil sannsynligvis ha sin egen mva-gruppe.     Mva-grupper er grupper med mva som gjelder for en bestemt kanal. Hvis en kanal for eksempel selger både via detaljhandel og bedrift-til-bedrift, kan mva-grupper for ulike varer brukes. Alle gjeldende avgifter vil bli tilordnet til mva-gruppen.  
    * Nå kan du velge Fra- og Til-avgifter eller Fra avgiftsgruppe og Til avgiftsgruppe for å opprette i mva-overstyring.    I Fra-feltet angir avgiften eller avgiftsgruppen som skal overstyres. Overstyring etter merverdiavgiftsgruppen for vare inneholder andre alternativer enn overstyring etter salgsavgiftsgruppen.    Mva-overstyringer kan defineres til å overstyre avgifter på hele transaksjoner eller bestemte linjer i transaksjonen.  
13. Klikk Lagre.
14. Lukk siden.
15. Gå til Detaljhandel og handel > Kanaloppsett > Merverdiavgift > Mva-overstyringsgrupper.
    * I dette trinnet vil du tilordnet den nyopprettede mva-overstyringen til mva-overstyringsgruppen som er tilordnet Houston-kanalen.  
16. Klikk Rediger.
17. Vis eller skjul Oppsett-delen.
18. Klikk Legg til.
19. Klikk rullegardinknappen i feltet Mva-overstyringsgruppe for å åpne oppslaget.
20. Velg den tidligere opprettede mva-overstyringen fra listen.
21. Klikk koblingen i den valgte raden i listen.
22. Klikk Lagre.


