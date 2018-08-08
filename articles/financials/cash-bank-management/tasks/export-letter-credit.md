--- 
title: Eksportere en remburs
description: "Denne prosedyren hjelper deg med å eksportere en remburs."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0fa4b57825bcf81778d91ee01484511bb40f6bd7
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="export-a-letter-of-credit"></a>Eksportere en remburs

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren hjelper deg med å eksportere en remburs.

En remburs er en avtale som utstedes av en bank, der banken godtar å sikre betaling på vegne av kjøperen hvis vilkårene i avtalen mellom kjøper og selger er oppfylt.



Kjør prosedyren Definere Bankfasilitetene og posteringsprofilene og Opprette en fasilitetsavtale for remburs før denne prosedyren. Demonstrasjonsfirmaet USMF må velges for at denne prosedyren skal kunne kjøres.




## <a name="create-sales-order-for-export-letter-of-credit"></a>Opprette salgsordre for remburseksport
1. Gå til Kunder > Ordrer > Alle salgsordrer.
2. Klikk Ny.
3. Klikk rullegardinknappen i Kundekonto-feltet for å åpne oppslaget.
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Vis eller skjul delen Generelt.
7. Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.
    * Velg stedet der varen som skal utstedes, er på lager.  
8. Klikk koblingen i den valgte raden i listen.
9. Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.
    * Velg lageret der varen som skal utstedes, befinner seg.  
10. Klikk koblingen i den valgte raden i listen.
    * Obs!  Feltet Bankdokumenttype må velges med verdien Remburs.  
11. Velg Remburs i feltet Bankdokumenttype.
12. Vis eller skjul Levering-delen.
    * Velg Leveringsdatokontroll = Ingen.  
13. Angi en dato i feltet Ønsket leveringsdato.
14. Klikk OK.
15. Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
    * Velg varen som skal utstedes/selges.  
16. Finn og velg ønsket post i listen.
17. Klikk koblingen i den valgte raden i listen.
18. Angi et tall i Enhetspris-feltet.
19. Vis eller skjul Linjedetaljer-delen.
20. Velg kategorien Levering.
21. Angi en dato i feltet Ønsket forsendelsesdato.
22. Angi en dato i Bekreftet forsendelsesdato-feltet.
23. Klikk Administrer i handlingsruten.
24. Klikk Remburs.
25. Angi en verdi i feltet Bankdokumentnummer.
26. Angi dato og klokkeslett i feltet Utløpsdato.
27. Vis eller skjul Bankdetaljer-delen.
28. Klikk rullegardinknappen i Rembursbank-feltet for å åpne oppslaget.
29. Klikk koblingen i den valgte raden i listen.
30. Klikk rullegardinknappen i Advisbank-feltet for å åpne oppslaget.
31. Finn og velg ønsket post i listen.
32. Klikk koblingen i den valgte raden i listen.
33. Klikk Hent salgsordreforsendelser.
34. Klikk Utsted bankdokument.
35. Lukk siden.

## <a name="post-packing-slip"></a>Postere følgeseddel
1. Klikk Plukk og pakk i handlingsruten.
2. Klikk Poster følgeseddel.
3. Vis eller skjul delen Parametere.
4. Velg Alle i Antall-feltet.
5. Vis eller skjul Oppsett-delen.
6. Angi en dato i Følgeseddeldato-feltet.
7. Velg forsendelsesnummeret.
8. Klikk koblingen i den valgte raden i listen.
9. Klikk OK.
10. Klikk OK.

## <a name="post-sales-invoice"></a>Postere salgsfaktura
1. Klikk Faktura i handlingsruten.
2. Klikk Faktura.
3. Vis eller skjul Oversikt-delen.
4. Velg forsendelsesnummeret.
5. Klikk koblingen i den valgte raden i listen.
6. Vis eller skjul Oppsett-delen.
7. Angi en dato i feltet Fakturadato.
8. Klikk OK.
9. Klikk OK.

## <a name="shipment-document-submitted-status"></a>Status for sendt forsendelsesdokument
1. Klikk Administrer i handlingsruten.
2. Klikk Remburs.
3. Vis eller skjul Linjer-delen.
    * Obs!  Feltet Dokumentet er sendt må settes til Ja.  

## <a name="verify-export-letter-of-credit"></a>Kontrollere remburseksport
1. Gå til Kontant- og bankbehandling > Purringer > Eksporter remburs og importinkasso.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
    * Kontroller at Eksporter remburs har forsendelsesstatusen Fakturert.  

## <a name="customer-payment"></a>Kundebetaling
1. Gå til Kunder > Betalinger > Betalingsjournal.
2. Klikk Ny.
3. Merk den valgte raden i listen.
4. Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.
5. Klikk koblingen i den valgte raden i listen.
6. Klikk Linjer.
7. Angi en dato i Dato-feltet.
8. Angi de ønskede verdiene i Konto-feltet.
9. Klikk Utligning.
10. Merk av i boksen i hodet i Totaler.
    * Obs!  Sett Vis felt til Remburs.  
11. Finn og velg ønsket post i listen.
12. Merk av eller fjern merket i avmerkingsboksen Merk.
13. Klikk OK.
14. Klikk kategorien Betaling.
    * Kontrollere detaljene om bankdokumentnummer og forsendelsesnummer  
15. Klikk Poster.

## <a name="verify-export-letter-of-credit-after-payment"></a>Kontrollere remburseksport etter betaling
1. Gå til Kontant- og bankbehandling > Purringer > Eksporter remburs og importinkasso.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
    * Kontroller at forsendelsesstatus = betaling mottatt og saldobeløp = 0,00.  


