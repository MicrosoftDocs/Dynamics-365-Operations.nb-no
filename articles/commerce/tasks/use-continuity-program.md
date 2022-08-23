---
title: Bruke kontinuitetsprogram
description: Denne fremgangsmåten hjelper med å selge et kontinuitetsprogram og behandle tilknyttede salgsordrer.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
ms.openlocfilehash: 3736984a336b35b23b7060b2d98770912cc9ec6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267411"
---
# <a name="using-continuity-program"></a>Bruke kontinuitetsprogram

[!include [banner](../includes/banner.md)]

Denne fremgangsmåten hjelper med å selge et kontinuitetsprogram og behandle tilknyttede salgsordrer. For å fullføre denne prosedyren, må brukeren være definert som telefonsenterbruker. Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.

1. Gå til Retail og Commerce > Kunder > Kundestøtte.
2. I Søketekst-feltet skriver du inn Karin og trykker deretter Tab-tasten.
    * Avansert søk-dialogboksen skal vises. Hvis ikke, klikker du Søk til høyre for dette feltet.  
3. Merk den valgte raden i listen.
    * Det skal bare være én rad som vises med Karen Berg. Merk raden ved å klikke på avmerkingskolonnen helt til venstre i rutenettet.  
4. Klikk Velg.
5. Klikk Ny salgsordre.
    * Det er lurt å notere seg salgsordrenummeret. Du vil trenge det senere i prosedyren.  
6. I Varenummer-feltet skriver du inn 88000 og trykker deretter Tab-tasten.
    * Dette er en kontinuitetsvare i demonstrasjonsdataene for USRT.  
7. Klikk Fullført.
8. Angi Visa i Betalingsmetode-feltet.
9. Klikk Legg til kredittkort.
    * Angi den nødvendige kredittkortinformasjonen på denne siden.  
10. Klikk OK.
11. Vid delen Betaling.
    * Hvis du vil sende en telefonsenterordre, må betalinger angis for ordren.  
12. Klikk OK.
13. Klikk Send.
    * Du er ferdig med å opprette en ny kontinuitetsordre. Nå skal du kjøre to satsvise prosesser som brukes til å behandle kontinuitetsordrene.  
14. Lukk siden.
15. Gå til Retail og Commerce > Kontinuitet > Behandle kontinuitetsbetalinger.
16. I Kontinuitetsvare-feltet skriver du inn 88000 og trykker deretter Tab-tasten.
17. Klikk OK.
18. Gå til Retail og Commerce > Kontinuitet > Opprett underordnede kontinuitetsordrer.
    * Denne prosessen oppretter nye salgsordrer basert på innstillingene for kontinuitetsprogrammene dine.  
19. I Kontinuitetsvare-feltet skriver du inn 88000 og trykker deretter Tab-tasten.
    * Vare 88000 er en kontinuitetsvare i demonstrasjonsdataene for USRT.  
20. Angi eller velg en verdi i feltet Salgsordre.
    * Angi salgsordrenummeret du noterte deg tidligere i denne fremgangsmåten. Dette vil holde behandlingstiden nede på et minimum for denne prosedyren. Salgsordre-feltet er valgfritt – du kan behandle alle ordrer for et hvilken som helst program.  
21. Klikk OK.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
