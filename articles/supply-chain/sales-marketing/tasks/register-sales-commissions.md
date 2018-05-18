--- 
title: Registrere salgsprovisjoner
description: "Denne fremgangsmåten viser deg hvordan provisjoner beregnes og registreres."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5535f1627526b97ddc9ca2c210db4e332782d656
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="register-sales-commissions"></a>Registrere salgsprovisjoner

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser deg hvordan provisjoner beregnes og registreres. Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Før du starter denne veiledningen kjører du veiledningen kalt Definer regler for salgsprovisjon for å være sikker på at du har alt nødvendig provisjonsberegningsoppsett.

Noter kunde- og varenumrene du har valgt for provisjonsprosessen, og bruk dem når du blir spurt til å opprette en salgsordre i denne veiledningen.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Fakturere en salgsordre som kvalifiserer til en selger for en provisjon
1. Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.
2. Klikk Ny.
3. Klikk rullegardinknappen i Kundekonto-feltet for å åpne oppslaget.
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Klikk OK.
7. Klikk Alternativer i handlingsruten.
8. Klikk Bytt visning.
9. Klikk Hodevisning.
10. Utvid Oppsett-delen.
    * Verdien i feltet Salgsgruppe representerer en gruppe med én eller flere selgere tilknyttet. Medlemmene av gruppen er de som skal motta provisjoner når ordren faktureres, i henhold til forhåndsdefinerte satser og distribusjon.   Verdien kopieres fra kundekortet, men du kan endre den hvis du ønsker.  Salgsgruppen kopieres også til salgsordrelinjen. Du kan endre den slik at den kan være forskjellig fra den i hodet og/eller mellom linjer.  
    * Verdien i feltet Provisjonsgruppe representerer en gruppe som du har opprettet for én eller flere kunder med det formål å spore provisjoner.   Verdien kopieres fra kundekortet, men du kan endre den hvis du ønsker.   
11. Klikk Alternativer i handlingsruten.
12. Klikk Bytt visning.
13. Klikk Linjevisning.
14. Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
15. Velg varen du har definert for provisjon, i listen. 
16. Angi et tall i feltet Antall.
    * Noter linjens nettobeløp. Det representerer salgsinntekter, som i dette eksemplet er grunnlaget for provisjonsberegningen.  
17. Klikk Lagre.
18. Klikk Faktura i handlingsruten.
19. Klikk Faktura.
20. Utvid seksjonen Parametere.
21. Velg Alle i feltet Antall.
22. Velg Ja i feltet Postering.
23. Klikk OK.
24. Klikk OK.
    * Det kan ta litt tid å postere transaksjonen. Tillat behandlingen å fullføre, og ikke lukk siden.  

## <a name="review-the-registered-sales-commissions"></a>Gå gjennom de registrerte salgsprovisjonene
1. Klikk Faktura i handlingsruten.
2. Klikk Faktura.
3. Klikk Faktura i handlingsruten.
4. Klikk Provisjonstransaksjoner.
    * Kategorien Oversikt viser linjer som viser provisjonsbeløpene som skal betales til selgere som er knyttet til den fakturerte salgsordren. La oss gå gjennom detaljene.     
    * Hvis du brukte veiledningen Definer regler for salgsprovisjon til å definere provisjonssalgsgruppen, finnes det to selgere som skal motta en salgsprovisjon, og provisjonen deles likt mellom dem.  
    * I dette eksemplet beregnes det totale provisjonsbeløpet som en prosent av salgsomsetning (nettobeløpet på ordrelinjen).   
5. Lukk siden.
6. Klikk Bilag.
    * Du kan vise bilagstransaksjonene for provisjonsbeløpene som er postert til de forhåndsdefinerte provisjonsutgifts- og provisjonsbetalingskontoene.  


