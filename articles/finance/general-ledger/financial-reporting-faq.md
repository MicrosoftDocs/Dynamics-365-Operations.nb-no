---
title: Vanlige spørsmål om finansrapportering
description: Dette emnet viser spørsmål som er knyttet til finansrapportering som andre brukere har hatt.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923031"
---
# <a name="financial-reporting-faq"></a>Vanlige spørsmål om finansrapportering 

Dette emnet gir svar på vanlige spørsmål om finansrapportering. 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Hvordan begrenser jeg tilgang til en rapport med tresikkerhet?

Følgende eksempel viser hvordan du begrenser tilgang til en rapport med tresikkerhet.

Demofirmaet USMF har en balanserapport som ikke alle finansrapporteringsbrukere skal ha tilgang til. Du kan bruke tresikkerhet til å begrense tilgang til en rapport, slik at bare bestemte brukere får tilgang til rapporten. Følg denne fremgangsmåten for å begrense tilgang: 

1. Logg på Financial Reporter Report Designer.
2. Opprett en ny tredefinisjon. Gå til **Fil > Ny > Tredefinisjon**.
3. Dobbeltklikk på linjen **Sammendrag** i kolonnen **Enhetssikkerhet**.
4. Velg **Brukere og grupper**.  
5. Velg brukerne eller gruppene som må ha tilgang til denne rapporten. 
6. Velg **Lagre**.
7. I rapportdefinisjonen legger du til den nye tredefinisjonen.
8. Velg **Innstilling** i tredefinisjonen. Under **Valg av rapporteringsenhet** velger du **Inkluder alle enheter**.

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a>Hvordan identifiserer jeg hvilke kontoer som ikke samsvarer med saldoene?

Hvis du har en rapport som ikke samsvarer saldoene, er det noen trinn du kan gå gjennom for å identifisere hver av kontoene og avvikene. 

**Financial Reporter Report Designer**
1. Opprett en ny raddefinisjon i Financial Reporter Report Designer. 
2. Velg **Rediger > Sett inn rader fra dimensjoner**.
3. Velg **MainAccount**.  
4. Velg **OK**.
5. Lagre raddefinisjonen.
6. Opprett en ny kolonnedefinisjon
7. Opprett en ny rapportdefinisjon.
8. Velg **Innstillinger** og fjern merket for dette alternativet.  
9. Generer rapporten. 
10. Eksporter rapporten til Microsoft Excel.

**Dynamics 365 Finance** 
1. I Dynamics 365 Finance går du til **Økonomimodul > Forespørsler og rapporter > Råbalanse**.
2. Angi følgende parametere:
   - **Fra-dato** – Angi starten på regnskapsåret.
   - **Til-dato** – Angi datoen du genererer rapporten for.
   - **Finansdimensjon** – Angi dette feltet til **Hovedkontosett**.
 3. Velg **Beregn**.
 4. Eksporter rapporten til Microsoft Excel.

Du skal nå kunne kopiere dataene fra Excel-rapporten i finansrapportering til råbalanserapporten slik at du kan sammenligne **sluttsaldokolonnene**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]