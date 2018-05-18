--- 
title: "Opprette en leverandørbankkonto"
description: "Denne fremgangsmåten viser hvordan du oppretter en bankkonto for en leverandør."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: adb759c59d7275e7323dbb760de56acdef2e3cff
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-vendor-bank-account"></a>Opprette en leverandørbankkonto

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en bankkonto for en leverandør. Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.

1. Gå til Innkjøp og leverandører > Leverandører > Alle leverandører.
2. Velg leverandøren du vil opprette en bankkonto for, og klikk deretter koblingen på leverandørens konto-ID.
3. Klikk Leverandør i handlingsruten.
4. Klikk Bankkontoer.
5. Klikk Ny.
6. Skriv inn en verdi i Bankkonto-feltet.
    * Denne ID-en brukes for å identifisere bankkontoen på leverandørposten.  
7. Skriv inn en verdi i Navn-feltet.
8. Angi eller velg en verdi i Bankgrupper-feltet.
9. Velg et alternativ i feltet Registreringsnummertype.
    * Dette er registreringsnummertypen som brukes for internasjonale betalinger.  
10. Skriv inn en verdi i feltet Bankkontonummer.
11. Skriv inn en verdi i SWIFT-kode-feltet.
12. Skriv inn en verdi i IBAN-feltet.
    * IBAN-nummeret må være i riktig format. Du kan for eksempel bruke DE89370400440532013000.  
    * Statusen for bankkontoen er Aktiv hvis aktiveringsdatoen er nådd og utløpsdatoen ikke er overskredet. Den er også aktivt hvis både aktiveringsdato og utløpsdato er tomme. Hvis datoene i både Aktiveringsdato- og Utløpsdato-feltene i er fremtiden, er ikke elektroniske betalinger tilgjengelige. Andre betalingstyper er tilgjengelige, og bankkontoen er aktiv.  
13. Utvid Oppsett-delen.
14. Skriv inn en verdi i Tekstkode-feltet.
    * Dette feltet angir en kode som vises på bankkontoutdraget til mottakeren.  
15. Skriv inn en verdi i Melding til bank-feltet.
16. Skriv inn en verdi i Kursreferanse-feltet.
    * Dette er referansenummeret for en eventuell fremtids- eller avtalekurs.  
17. Angi eller velg en verdi i feltet Valuta.
    * Når forhåndsmerknader utstedes, vil denne delen gir en oversikt over statusen (venter eller godkjent).  
18. Vis delen Adresse.
19. Vis Forhåndsmerknader-delen.
20. Vis delen Kontaktinformasjon.
21. Skriv inn en verdi i feltet Telefon.
22. Lukk siden.
23. Klikk Rediger.
24. Vid delen Betaling.
25. Velg kontoen du nettopp har opprettet i Bankkonto-feltet.
26. Klikk Lagre.
    * Adressen kan arves fra bankgruppen, hvis det er angitt, eller du kan legge den til her.  


