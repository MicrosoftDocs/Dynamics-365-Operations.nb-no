---
title: " Opprette telefonsenterordrer"
description: Denne prosedyren hjelper med å slå opp en kunde, opprette en ny ordre, søke etter et produkt og hente inn betaling fra kunden.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08a806514a92a99a9f0b18b36817f49a09516ab8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964851"
---
# <a name="create-call-center-orders"></a> Opprette telefonsenterordrer

[!include [banner](../includes/banner.md)]

Denne prosedyren hjelper med å slå opp en kunde, opprette en ny ordre, søke etter et produkt og hente inn betaling fra kunden. Denne prosedyren bruker demonstrasjonsdatafirmaet USRT og er ment for selgere. Forhåndskrav: Brukeren som utfører prosedyren, er satt opp som telefonsenterbrukere og katalogen for Fabrikam annethvert år publiseres med minst én kildekode.

1. Gå til **Detaljhandel og handel \> Kunder \> Kundeservice**.
2. Angi søkekriteriene for å slå opp kunden, for **Søketekst**.
    * I denne eksempelprosedyren skriver du inn Karin og velger **Tab**.  
3. Velg Søk.
    * Siden det bare finnes én kunde med navnet Karin i demonstrasjonsdataene, velges de automatisk.  
4. Velg **Ny salgsordre**.
5. Vis eller skjul delen **Salgsordre**-hode.
6. Velg kildekoden for katalogen.
    * Hvis det ikke finnes aktive kildekoder, kan du hoppe over dette trinnet.  
7. Velg **Legg til linje**.
8. For **Varenummer** angir du varesøkeordet.
    * I denne eksempelprosedyren angir du et delvis varenummer, 8111, og trykker TAB. Søkevinduet vil dermed vises.  
9. Velg produktet som skal legges til salgsordren.
10. Angi salgsantallet.
11. Velg **Opprett**.
12. Klikk **Fullfør** for å registrere kundebetalingen.
13. Velg **Legg til**.
    * Koblingen Legg til er i Betalinger-fanen. Vis Betalinger-fanen hvis den er skjult.  
14. Velg betalingsmåten.
    * Velg kontantbetalingsmåten for denne prosedyren.  
15. Lukk siden.
16. Angi beløpet.
    * I denne prosedyren angir du et beløp som er likt ordresaldoen som vises på sammendragssiden for salgsordren til venstre i beløpsfeltet. Dermed kan du fullføre ordren som fullt betalt.  
17. Velg **OK**.
18. Velg **Send**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tilpasse transaksjons-e-poster etter leveringsmåte](../customize-email-delivery-mode.md)

[Endre leveringsmodus i salgssted](../pos-change-delivery-mode.md)

