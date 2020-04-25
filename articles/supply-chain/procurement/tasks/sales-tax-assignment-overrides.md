---
title: Mva-tilordning og overstyringer
description: Denne fremgangsmåten beskriver hvordan du tilordner mva-grupper til handelskanaler.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74a7eed04648c63c0b19d5de26d2bdbef59aec7d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207606"
---
# <a name="sales-tax-assignment-and-overrides"></a> Mva-tilordning og overstyringer

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten beskriver hvordan du tilordner mva-grupper til handelskanaler. Den veileder deg også gjennom oppretting av en ny mva-overstyring og tilordning av den til en eksisterende mva-overstyringsgruppe. Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.

1. Gå til Retail og Commerce > Kanaler > Butikker > Alle butikker.
2. I listen klikker du koblingen ID for kanal for Houston.
3. Klikk Rediger
    * Feltet Merverdiavgiftsgruppe inneholder en liste over merverdiavgiftsgrupper for gjeldende firma. Gjeldende tildelt gruppe er en generisk "Texas"-merverdiavgiftsgruppe. Det finnes også mva-grupper for "Washington" og "Washington, King County." Mva-grupper kan inneholde gjeldende avgifter for flere områder.  
    * Feltet Merverdiavgiftoverstyring er der merverdiavgiftoverstyringsgrupper kan tilordnes til kanalen. Merverdiavgiftoverstyringsgrupper kan brukes til å gruppere sammen merverdiavgiftoverstyringer som fungerer for flere butikker. I stedet for manuell, enkeltvis tilordning av merverdiavgiftoverstyringer, kan gruppen opprettes og tilordnes direkte til kanalene for å spare tid.  
4. Klikk Lagre.
5. Lukk siden.
6. Gå til Retail og Commerce > Kanaloppsett > Merverdiavgift > Mva-overstyringer.
7. Klikk Ny.
8. Angi et navn for den nye overstyringen i feltet Mva-overstyring.
9. Angi en kort beskrivelse av overstyringen i Beskrivelse-feltet.
10. Sett statusen til Aktiver.
11. Vis eller skjul delen Overstyr.
12. Velg et alternativ i Type-feltet.
    * Mva-grupper for vare kan brukes til å overstyre avgifter for bestemte varer som tilhører gruppen. Matvarer beskattes for eksempel vanligvis forskjellig fra fastvarer, og vil sannsynligvis ha sin egen mva-gruppe. Mva-grupper er grupper med mva som gjelder for en bestemt kanal. Hvis en kanal for eksempel selger både via detaljhandel og bedrift-til-bedrift, kan mva-grupper for ulike varer brukes. Alle gjeldende avgifter vil bli tilordnet til mva-gruppen.  
    * Nå kan du velge Fra- og Til-avgifter eller Fra avgiftsgruppe og Til avgiftsgruppe for å opprette i mva-overstyring. I Fra-feltet angir avgiften eller avgiftsgruppen som skal overstyres. Overstyring etter merverdiavgiftsgruppen for vare inneholder andre alternativer enn overstyring etter salgsavgiftsgruppen. Mva-overstyringer kan defineres til å overstyre avgifter på hele transaksjoner eller bestemte linjer i transaksjonen.  
13. Klikk Lagre.
14. Lukk siden.
15. Gå til Retail og Commerce > Kanaloppsett > Merverdiavgift > Mva-overstyringsgrupper.
    * I dette trinnet vil du tilordnet den nyopprettede mva-overstyringen til mva-overstyringsgruppen som er tilordnet Houston-kanalen.  
16. Klikk Rediger.
17. Vis eller skjul Oppsett-delen.
18. Klikk Legg til.
19. Klikk rullegardinknappen i feltet Mva-overstyringsgruppe for å åpne oppslaget.
20. Velg den tidligere opprettede mva-overstyringen fra listen.
21. Klikk koblingen i den valgte raden i listen.
22. Klikk Lagre.

