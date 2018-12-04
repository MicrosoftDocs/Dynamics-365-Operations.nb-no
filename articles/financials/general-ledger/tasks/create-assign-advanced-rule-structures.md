--- 
title: Opprette og tilordne avanserte regelstrukturer
description: "Denne oppgaveveiledningen viser trinn for å opprette og tilordne en avansert regelstruktur til en kontostruktur."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ebad4ec9ec6242978a26007a64416ae1b2af5c28
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-assign-advanced-rule-structures"></a>Opprette og tilordne avanserte regelstrukturer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaveveiledningen viser trinn for å opprette og tilordne en avansert regelstruktur til en kontostruktur. Denne veiledningen bruker USMF demo firmaet.


## <a name="create-an-advanced-rule-structure"></a>Opprett en avansert regelstruktur
1. Gå til Økonomimodul > Kontoplan > Strukturer > Avanserte regelstrukturer.
2. Klikk Ny for å åpne nedtrekksdialogen.
3. I feltet Avansert regelstruktur skriver du inn et navn som beskriver strukturen for regelen.
4. Skriv inn en verdi for å beskrive strukturen, i Beskrivelse-feltet.
5. Klikk OK.
6. Klikk Legg til segment.
7. Velg en finansdimensjon i listen over segmenter.
    * For eksempel Butikk.  
8. Klikk Legg til segment.
9. Klikk koblingen for den avanserte regelstrukturen for å vise den, i listen.
10. Klikk Aktiver.
11. Klikk Aktiver.

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>Bruke en avansert regelstruktur for en kontostruktur
1. Lukk skjemaet.
2. Lukk siden.
3. Gå til Økonomimodul > Kontoplan > Strukturer > Konfigurer kontostrukturer.
4. I listen, Finn og Merk kontostrukturen du vil bruke den avanserte regelen for.
5. Klikk navnet på kontostrukturen å åpne den.
6. Klikk Rediger.
    * Du kan også klikke Avanserte regler, og du blir bedt om å plassere kontostrukturen i utkastmodus.  
7. Klikk Avanserte regler.
8. Klikk Ny for å åpne nedtrekksdialogen.
9. Skriv inn en verdi i feltet Avansert regel.
10. Skriv inn en verdi i Navn-feltet.
11. Klikk Opprett.
12. Klikk Legg til nye kriterier.
13. Velg hovedkontoen eller en finansdimensjon i feltet Hvor.
14. Velg et alternativ, for eksempel er mellom og inkluderer i Operator-feltet.
15. Skriv inn en verdi i Verdi-feltet.
16. Skriv inn en verdi i feltet via.
17. Klikk Legg til for å åpne nedtrekksdialogen.
18. I listen finner du den avanserte regelstrukturen du vil bruke når kriteriene du angav er oppfylt.
19. Klikk Legg til.
20. Lukk siden.
21. Klikk Aktiver.
22. Klikk Aktiver.


