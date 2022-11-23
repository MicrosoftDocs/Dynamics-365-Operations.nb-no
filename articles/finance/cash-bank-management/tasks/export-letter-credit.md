---
title: Eksporter remburser
description: Denne prosedyren hjelper deg med å eksportere en remburs.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf06a73bf7665059658c7884a0b9f973929d647c
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779561"
---
# <a name="export-letter-of-credit"></a>Eksporter remburser

[!include [banner](../../includes/banner.md)]

Denne prosedyren hjelper deg med å eksportere en remburs.

En remburs er en avtale som utstedes av en bank, der banken godtar å sikre betaling på vegne av kjøperen hvis vilkårene i avtalen mellom kjøper og selger er oppfylt.



Kjør prosedyren **Definere bankfasiliteter og posteringsprofiler** og **Opprette en fasilitetsavtale for remburs** før denne prosedyren. Demonstrasjonsfirmaet USMF må velges for at denne prosedyren skal kunne kjøres.


## <a name="create-sales-order-for-export-letter-of-credit"></a>Opprette salgsordre for remburseksport
1. Gå til **Kunder > Ordrer > Alle salgsordrer**.
2. Klikk på **Ny**.
3. Klikk på rullegardinknappen i **Kundekonto**-feltet for å åpne oppslaget.
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Vis eller skjul delen **Generelt**.
7. Klikk på rullegardinknappen i **Område**-feltet for å åpne oppslaget.
    * Velg **Område** der varen som skal utstedes, er på lager.  
8. Klikk koblingen i den valgte raden i listen.
9. Klikk på rullegardinknappen i **Lager**-feltet for å åpne oppslaget.
    * Velg **Lager** der varen som skal utstedes, befinner seg.  
10. Klikk på koblingen i den valgte raden i listen.
    * Merk: Feltet **Bankdokumenttype** må velges med **Remburs**.  
11. Velg **Remburs** i feltet **Bankdokumenttype**.
12. Vis eller skjul **Levering**-delen.
    * Velg **Leveringsdatokontroll** = **Ingen**.  
13. Angi en dato i feltet **Ønsket leveringsdato**.
14. Klikk på **OK**.
15. Klikk på rullegardinknappen i **Varenummer**-feltet for å åpne oppslaget.
    * Velg varen som skal utstedes/selges.  
16. Finn og velg ønsket post i listen.
17. Klikk koblingen i den valgte raden i listen.
18. Angi et tall i **Enhetspris**-feltet.
19. Vis eller skjul **Linjedetaljer**-delen.
20. Velg kategorien **Levering**.
21. Angi en dato i feltet **Ønsket forsendelsesdato**.
22. Angi en dato i **Bekreftet forsendelsesdato**-feltet.
23. Klikk på **Administrer** i handlingsruten.
24. Klikk **Remburs**.
25. Angi en verdi i feltet **Bankdokumentnummer**.
26. Angi dato og klokkeslett i feltet **Utløpsdato**.
27. Vis eller skjul **Bankdetaljer**-delen.
28. Klikk rullegardinknappen i **Rembursbank**-feltet for å åpne oppslaget.
29. Klikk koblingen i den valgte raden i listen.
30. Klikk rullegardinknappen i **Advisbank**-feltet for å åpne oppslaget.
31. Finn og velg ønsket post i listen.
32. Klikk koblingen i den valgte raden i listen.
33. Klikk **Hent salgsordreforsendelser**.
34. Klikk **Utsted bankdokument**.
35. Lukk siden.

## <a name="post-packing-slip"></a>Postere følgeseddel
1. Klikk på **Plukk og pakk** i handlingsruten.
2. Klikk på **Poster følgeseddel**.
3. Vis eller skjul delen **Parametere**.
4. Velg **Alle** i **Antall**-feltet.
5. Vis eller skjul **Oppsett**-delen.
6. Angi en dato i **Følgeseddeldato**-feltet.
7. Velg forsendelsesnummeret.
8. Klikk koblingen i den valgte raden i listen.
9. Klikk på **OK**.
10. Klikk på **OK**.

## <a name="post-sales-invoice"></a>Postere salgsfaktura
1. Klikk på **Faktura** i handlingsruten.
2. Klikk på **Faktura**.
3. Vis eller skjul **Oversikt**-delen.
4. Velg **Forsendelsesnummeret**.
5. Klikk koblingen i den valgte raden i listen.
6. Vis eller skjul **Oppsett**-delen.
7. Angi en dato i **Fakturadato**-feltet.
8. Klikk på **OK**.
9. Klikk på **OK**.

## <a name="shipment-document-submitted-status"></a>Status for sendt forsendelsesdokument
1. Klikk på **Administrer** i handlingsruten.
2. Klikk **Remburs**.
3. Vis eller skjul **Linjer**-delen.
    * Merk: Feltet **Dokumentet er sendt** må settes til **Ja**.  

## <a name="verify-export-letter-of-credit"></a>Kontrollere remburseksport
1. Gå til **Kontant- og bankbehandling > Purringer > Eksporter remburs og importinkasso**.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
    * Kontroller at **Eksporter remburs** har **Forsendelsesstatus** **Fakturert**.  

## <a name="customer-payment"></a>Kundebetaling
1. Gå til **Kunder > Betalinger > Betalingsjournal**.
2. Klikk på **Ny**.
3. Merk den valgte raden i listen.
4. Klikk på rullegardinknappen i **Navn**-feltet for å åpne oppslaget.
5. Klikk koblingen i den valgte raden i listen.
6. Klikk **Linjer**.
7. Angi en dato i **Dato**-feltet.
8. Angi de ønskede verdiene i **Konto**-feltet.
9. Klikk **Utligning**.
10. Merk av i boksen i hodet i Totaler.
    * Merk: Sett **Vis** felt til **Remburs**.  
11. Finn og velg ønsket post i listen.
12. Merk av eller fjern merket i avmerkingsboksen **Merk**.
13. Klikk på **OK**.
14. Klikk på fanen **Betaling**.
    * Kontrollere detaljene om bankdokumentnummer og forsendelsesnummer  
15. Klikk på **Poster**.

## <a name="verify-export-letter-of-credit-after-payment"></a>Kontrollere remburseksport etter betaling
1. Gå til **Kontant- og bankbehandling > Purringer > Eksporter remburs og importinkasso**.
2. Finn og velg ønsket post i listen.
3. Klikk på koblingen i den valgte raden i listen.
    * Kontroller at **Forsendelsesstatus** = **Betaling mottatt** og **Saldobeløp** = **0.00**.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
