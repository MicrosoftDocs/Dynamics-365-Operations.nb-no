---
title: Vanlige spørsmål om finansrapportering
description: Dette emnet viser spørsmål som er knyttet til finansrapportering som andre brukere har hatt.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3f9381f5b656d0cc0b46c8828b2ef9d024e296b0
ms.sourcegitcommit: 14785208d84b2c1efd30f140c52df35a2ccd1577
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/27/2021
ms.locfileid: "5070223"
---
# <a name="financial-reporting-faq"></a>Vanlige spørsmål om finansrapportering 

Dette emnet viser spørsmål som er knyttet til finansrapportering som andre brukere har hatt. 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Hvordan begrenser jeg tilgang til en rapport med tresikkerhet?

Scenario: Demonstrasjonsfirmaet USMF har en balanserapport som de ikke vil at alle regnskapsrapporteringsbrukere skal kunne se i D365. Løsning: Du kan bruke tresikkerhet til å begrense tilgang til en rapport, slik at bare bestemte brukere får tilgang til rapporten. 

1.  Logg på Rapportutforming for finansrapportering

2.  Opprett en ny tredefinisjon (Fil | Ny | Tredefinisjon) a.    Dobbeltklikk på linjen **Sammendrag** i kolonnen **Enhetssikkerhet**.
  i.    Klikk på Brukere og grupper.  
          1. Velg brukerne eller gruppen som vil ha tilgang til denne rapporten. 
          
[![brukerskjermbilde](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)

[![sikkerhetsskjermbilde](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)

  b.    Klikk på **Lagre**.
  
[![Lagre-knapp](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)

3.  I rapportdefinisjonen legger du til den nye tredefinisjonen

[![tredefinisjonsskjema](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)

A.  Mens du er i tredefinisjonen klikker du på Innstilling og merker av for Inkluder alle enheter under Valg av rapporteringsenhet

[![skjema for valg av rapporteringsenhet](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)

**Før:** [![før skjermbilde](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)

**Etter:** [![etter skjermbilde](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)

Merk: Årsaken til meldingen ovenfor er at brukeren ikke har tilgang til rapporten etter bruk av enhetssikkerhet



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a>Hvordan finner jeg ut hvilke kontoer som ikke samsvarer med saldoene i D365?

Når du har en rapport som ikke samsvarer med det du forventer i D365, er det noen trinn du kan gå gjennom for å identifisere disse kontoene og avvikene. 

### <a name="in-financial-reporter-report-designer"></a>I Rapportutforming for finansrapportering

1.  Opprett en ny raddefinisjon a.    Klikk på Rediger | Sett inn rader fra dimensjoner i.  Velg MainAccount [![Velg Hovedskjermbilde_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)
    
    ii. Klikk på Ok b.    Lagre raddefinisjonen

2.  Opprette en ny kolonnedefinisjon     [![Opprette en ny kolonnedefinisjon](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)

3.  Opprett en ny rapportdefinisjon a.    Klikk på Innstillinger og fjern merket for [![Innstillinger-skjema](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)
   
4.  Generer rapporten. 

5.  Eksporter rapporten til Excel.

### <a name="in-d365"></a>I D365: 
1.  Klikk på Økonomimodul | Forespørsler og rapporter | Råbalanse a.    Parametere i.  Fra-dato: Start på regnskapsår ii. Til-dato: Datoen da du genererte rapporten for iii.    Finansdimensjonssettet Hovedkontosett [![Hovedkontoskjema](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)
      
  b.    Klikk på Beregn

2.  Eksporter rapporten til Excel

Du skal nå kunne kopiere dataene fra FR Excel-rapporten til D365-råbalanserapporten og sammenligne sluttsaldokolonnene.
