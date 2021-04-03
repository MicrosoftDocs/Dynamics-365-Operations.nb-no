---
title: Opprette en leverandørbankkonto
description: Denne fremgangsmåten viser hvordan du oppretter en bankkonto for en leverandør.
author: RichardLuan
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 425cce178c96097c8aa0a28345d4a9094b7970d9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262195"
---
# <a name="create-a-vendor-bank-account"></a>Opprette en leverandørbankkonto

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en bankkonto for en leverandør. Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.

1. Gå til **navigasjonsruten > Moduler > Innkjøp og leverandører > Leverandører > Alle leverandører**.
2. Velg leverandøren du vil opprette en bankkonto for, og klikk deretter koblingen i feltet **Leverandørens konto-ID**.
3. I **handlingsruten** klikker du **Leverandør**.
4. Klikk på **Bankkontoer**.
5. Klikk på **Ny** i **handlingsruten**.
6. Skriv inn en verdi i **Bankkonto**-feltet. Denne ID-en brukes for å identifisere bankkontoen på leverandørposten.  
7. Skriv inn en verdi i **Navn**-feltet.
8. Angi eller velg en verdi i **Bankgrupper**-feltet.
9. Velg et alternativ i feltet **Registreringsnummertype**. Dette er registreringsnummertypen som brukes for internasjonale betalinger.  
10. Skriv inn en verdi i feltet **Bankkontonummer**.
11. Skriv inn en verdi i **SWIFT-kode**-feltet.
12. Skriv inn en verdi i **IBAN**-feltet.
    - IBAN-nummeret må være i riktig format. Du kan for eksempel bruke DE89370400440532013000.  
    - Statusen for bankkontoen er Aktiv hvis aktiveringsdatoen er nådd og utløpsdatoen ikke er overskredet. Den er også aktiv hvis både aktiveringsdato og utløpsdato er tomme. Hvis datoene i både Aktiveringsdato- og Utløpsdato-feltene i er fremtiden, er ikke elektroniske betalinger tilgjengelige. Andre betalingstyper er tilgjengelige, og bankkontoen er aktiv.  
13. Utvid **Oppsett**-delen.
14. Skriv inn en verdi i **Tekstkode**-feltet. Dette feltet angir en kode som vises på bankkontoutdraget til mottakeren.  
15. Skriv inn en verdi i **Melding til bank**-feltet.
16. Skriv inn en verdi i **Kursreferanse**-feltet. Dette er referansenummeret for en eventuell fremtids- eller avtalekurs.
17. Angi eller velg en verdi i **Valuta**-feltet. Når forhåndsmerknader utstedes, vil denne delen gir en oversikt over statusen (venter eller godkjent).  
18. Vis delen **Adresse**.
19. Vis **Forhåndsmerknader**-delen.
20. Vis delen **Kontaktinformasjon**.
21. Skriv inn en verdi i feltet **Telefon**.
22. Lukk siden.
23. Klikk på **Rediger**.
24. Vis delen **Betaling**.
25. Velg kontoen du nettopp har opprettet i **Bankkonto**-feltet.
26. Klikk på **Lagre**. Adressen kan arves fra bankgruppen, hvis det er angitt, eller du kan legge den til her.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]