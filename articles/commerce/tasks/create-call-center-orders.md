---
title: " Opprette telefonsenterordrer"
description: Denne artikkelen går gjennom en eksempelprosedyre der en kundesenterbruker slår opp en kunde, oppretter en ny ordre, søker etter et produkt og henter inn betaling fra kunden i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 08/05/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16d483896ce131e9a7bc60ab5ea7b8fa01a3bea8
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228517"
---
# <a name="create-call-center-orders"></a> Opprette telefonsenterordrer

[!include [banner](../includes/banner.md)]

Denne artikkelen går gjennom en eksempelprosedyre der en kundesenterbruker slår opp en kunde, oppretter en ny ordre, søker etter et produkt og henter inn betaling fra kunden i Microsoft Dynamics 365 Commerce. Prosedyren bruker USRT-demonstrasjonsdatafirmaet og er ment for selgere. 

## <a name="prerequisites"></a>Forutsetninger

Brukeren som fullføre prosedyren, må brukeren være definert som telefonsenterbruker. Du kan også publisere Fabrikam-halvårskatalogen med minst én kildekode.

### <a name="add-yourself-as-a-call-center-user"></a>Legge til deg selv som en kundesenterbruker

Bruk følgende fremgangsmåte for å legge til deg selv som kundesenterbruker.

1. I Commerce headquarters, går du til **Retail og Commerce \> Kanaler \> Kundesenter \> Alle kundesentre**.
1. Velg **Kanalbrukere** i **Brukere**-feltet.
1. Velg **Ny** i handlingsruten.
1. I **Bruker-ID**-feltet angir bruker-ID-en.
1. Angi brukernavnet i **Navn**-feltet. Brukernavnet kan være det samme som bruker-ID-en.
1. Velg **Lagre** i handlingsruten.
1. Gå til tilbake til **Detaljhandel og handel \> Kanaler \> Kundesentre \> Alle kundesentre**.
1. Velg handelskanal-ID-en for kundesenteret.
1. Bekreft at alternativet **Aktiver ordrefullføring** er satt til **Ja**. Hvis alternativet ikke er synlig, kan du hoppe over dette trinnet.

## <a name="complete-the-example-call-center-procedure"></a>Fullfør eksempelprosedyren for kundesenter

Følg denne fremgangsmåten for å fullføre eksemplet på kundesenterprosedyren.

1. Gå til **Detaljhandel og handel \> Kunder \> Kundeservice**.
1. Angi søkekriteriene for å slå opp kunden, på fanen **Kundesøk**. I denne eksempelprosedyren skriver du inn **Karin**.
1. Velg **Søk**. Dialogboksen **Kundesøk** vises med en liste over søkeresultatene.
1. Velg kundeposten for **Karin Berg** som har kundekontonummeret **2001**, og velg deretter **Velg**.
1. Velg **Ny salgsordre** i handlingsruten.
1. Velg **Hode**-fanen til høyre.
1. På hurtigfanen **Levering**, feltet **Leveringsmåte** velger du **99 standard**.

    ![Velg en leveringsmåte.](../media/Select_Mode_of_Delivery.png)

1. Velg **Linjer**-fanen til høyre.
1. I **Salgsordrelinjer**-delen i den nye raden for den nye salgslinjen angir du varenummeret du vil søke etter, i **Varenummer**-feltet. For denne eksempelprosedyren angir du **81327**, og deretter velger du produktet i rullegardinlisten for å legge det til i salgsordren.
1. Angi salgsantallet i **Antall**-feltet.
1. Velg kildekoden for katalogen i feltet **Kildekode**. Hvis det ikke finnes aktive kildekoder, kan du hoppe over dette trinnet.
1. Klikk **Fullfør** for å registrere kundebetalingen på handlingsruten. Denne handlingen åpner dialogboksen **Salgsordresammendrag**, som viser det totale beløpet som forfaller. Handlingen utløser også beregningen av eventuelle tillegg, for eksempel forsendelse og håndtering, og viser dem i dialogboksen **Salgsordresammendrag**.

    ![Fullfør-knappen.](../media/Complete_button.png)

1. I **Salgsordresammendrag**-dialogboksen, på **Betalinger**-hurtigfanen, velger du **Legg til** for å registrere betalingene.

    ![Dialogboksen Salgsordresammendrag.](../media/order_summary.png)

1. Velg betalingsmåte i feltet **Betalingsmåte** i dialogboksen **Angi kundebetalingsinformasjon**. I denne eksempelprosedyren velger du **Kontant**.
1. Angi betalingsbeløpet i **Betalingsbeløp**-feltet. For dette eksemplet angir du **120,00**, som er lik ordresaldoen som vises i dialogboksen **Salgsordresammendrag**. Ved å angi dette beløpet kan du fullføre ordren som fullt betalt.
1. Velg **OK**.
1. Velg **Send**.

## <a name="additional-resources"></a>Tilleggsressurser

[Tilpasse transaksjons-e-poster etter leveringsmåte](../customize-email-delivery-mode.md)

[Endre leveringsmodus i salgssted](../pos-change-delivery-mode.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
