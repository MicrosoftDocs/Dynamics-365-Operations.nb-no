---
title: Registrere salgsprovisjoner
description: Dette emnet forklarer hvordan salgsprovisjon beregnes og registreres.
author: omulvad
manager: tfehr
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57e3b95cb1f4a13b49ddcd336efaeabb12e5defc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434235"
---
# <a name="register-sales-commissions"></a>Registrere salgsprovisjoner

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan salgsprovisjon beregnes og registreres. Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Før du starter denne veiledningen kjører du veiledningen kalt Definer regler for salgsprovisjon for å være sikker på at du har alt nødvendig provisjonsberegningsoppsett.

Noter kunde- og varenumrene du har valgt for provisjonsprosessen, og bruk dem når du blir spurt til å opprette en salgsordre i denne veiledningen.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Fakturere en salgsordre som kvalifiserer til en selger for en provisjon
1. I navigasjonsruten går du til **Moduler > Salg og markedsføring > Salgsordrer > Alle salgsordrer**.
2. Velg **Ny**.
3. Velg det ønskede oppslaget på rullegardinmenyen i **Kundekonto**-feltet.
4. Velg **OK**.
5. Velg **Alternativer** i handlingsruten.
6. Velg **Endre visning**.
7. Velg **Topptekstvisning**.
8. Utvid **Oppsett**-delen.

    - Verdien i feltet **Salgsgruppe** representerer en gruppe med én eller flere selgere tilknyttet. Medlemmene av gruppen er de som skal motta provisjoner når ordren faktureres, i henhold til forhåndsdefinerte satser og distribusjon.   
    - Verdien kopieres fra kundekortet, men du kan endre den hvis du ønsker.  
    - Salgsgruppen kopieres også til salgsordrelinjen. Du kan endre den slik at den kan være forskjellig fra den i hodet og/eller mellom linjer.  
    - Verdien i feltet **Provisjonsgruppe** representerer en gruppe som du har opprettet for én eller flere kunder med det formål å spore provisjoner.   
    - Verdien kopieres fra kundekortet, men du kan endre den hvis du ønsker.   

9. Velg **Alternativer** i handlingsruten.
10. Velg **Endre visning**.
11. Velg **Linjevisning**.
12. I rullegardinmenyen for **Varenummer**-feltet velger du varen du har definert for provisjoner. 
13. Angi et tall i **Antall**-feltet. Noter linjens nettobeløp. Det representerer salgsinntekter, som i dette eksemplet er grunnlaget for provisjonsberegningen.  
14. Velg **Lagre**.
15. Velg **Faktura** i handlingsruten.
16. Velg **Faktura**.
17. Utvid seksjonen **Parametere**.
18. Velg **Alle** i **Antall**-feltet.
19. Velg **Ja** i feltet **Postering**.
20. Velg **OK**, og velg deretter **OK** i neste rute. Det kan ta litt tid å postere transaksjonen. Tillat behandlingen å fullføre, og ikke lukk siden.  

## <a name="review-the-registered-sales-commissions"></a>Gå gjennom de registrerte salgsprovisjonene
1. I Handlingsvinduet, velg **Faktura**, og velg deretter **Faktura** igjen.
2. I Handlingsvinduet, velg **Faktura**, og velg deretter **Provisjonstransaksjoner**.

    - Kategorien **Oversikt** viser linjer som viser provisjonsbeløpene som skal betales til selgere som er knyttet til den fakturerte salgsordren. La oss gå gjennom detaljene.  
    - Hvis du brukte veiledningen Definer regler for salgsprovisjon til å definere gruppen **provisjonssalg**, finnes det to selgere som skal motta en salgsprovisjon, og provisjonen deles likt mellom dem.  
    - I dette eksemplet beregnes det totale provisjonsbeløpet som en prosent av salgsomsetning (nettobeløpet på ordrelinjen).  
3. Lukk siden.
4. Velg **Bilag**. Du kan vise bilagstransaksjonene for provisjonsbeløpene som er postert til de forhåndsdefinerte provisjonsutgifts- og provisjonsbetalingskontoene.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]