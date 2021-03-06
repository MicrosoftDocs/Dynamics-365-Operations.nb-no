---
title: Vanlige spørsmål om finansrapportering
description: Dette emnet gir svar på vanlige spørsmål om finansrapportering.
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
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266639"
---
# <a name="financial-reporting-faq"></a>Vanlige spørsmål om finansrapportering

Dette emnet gir svar på vanlige spørsmål om finansrapportering.

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>Hvordan begrenser jeg tilgang til en rapport med tresikkerhet?

Følgende eksempel viser hvordan du begrenser tilgang til en rapport med tresikkerhet.

Demofirmaet USMF har en **balanserapport** som ikke alle finansrapporteringsbrukere skal ha tilgang til. Du kan bruke tresikkerhet til å begrense tilgang til en rapport, slik at bare bestemte brukere får tilgang til den.

1. Logg på Financial Reporter Report Designer.
2. Velg **Fil \> Ny \> Tredefinisjon** til å opprette en ny tredefinisjon.
3. Dobbelttrykk (eller dobbeltklikk) på linjen **Sammendrag** i kolonnen **Enhetssikkerhet**.
4. Velg **Brukere og grupper**.
5. Velg brukerne eller gruppene som må ha tilgang til rapporten.
6. Velg **Lagre**.
7. I rapportdefinisjonen legger du til den nye tredefinisjonen.
8. Velg **Innstilling** i tredefinisjonen. Under **Valg av rapporteringsenhet** velger du **Inkluder alle enheter**.

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>Hvordan identifiserer jeg hvilke kontoer som ikke samsvarer med saldoene?

Hvis du har en rapport som ikke samsvarer saldoene, bruker du følgende fremgangsmåter til å identifisere hver konto og hvert avvik.

### <a name="in-financial-reporter-report-designer"></a>I Financial Reporter Report Designer

1. Opprett en ny raddefinisjon.
2. Velg **Rediger \> Sett inn rader fra dimensjoner**.
3. Velg **MainAccount**.
4. Velg **OK**.
5. Lagre raddefinisjonen.
6. Opprett en ny kolonnedefinisjon.
7. Opprett en ny rapportdefinisjon.
8. Velg **Innstillinger** og fjern merket for dette alternativet.
9. Generer rapporten. 
10. Eksporter rapporten til Microsoft Excel.

### <a name="in-dynamics-365-finance"></a>I Dynamics 365 Finance

1. Gå til **Økonomimodul \> Forespørsler og rapporter \> Råbalanse**.
2. Angi følgende felter:

    - **Fra-dato** – Angi startdatoen på regnskapsåret.
    - **Til-dato** – Angi datoen du genererer rapporten for.
    - **Finansdimensjon** – Angi dette feltet til **Hovedkontosett**.

3. Velg **Beregn**.
4. Eksporter rapporten til Excel.

Du skal nå kunne kopiere dataene fra Excel-rapporten i Financial Reporter til rapporten **Råbalanse** slik at du kan sammenligne kolonnene **Sluttsaldo**.

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Når jeg utformer en rapport i Report Designer, eller når jeg genererer en finansrapport, får jeg følgende melding: Operasjonen kan ikke fullføres på grunn av et problem i dataleverandørrammeverket. Hvordan skal jeg svare?

Meldingen indikerer at det oppstod et problem da systemet forsøkte å hente økonomiske metadata fra datatorget mens du brukte finansrapportering. Det finnes to måter å svare på dette problemet på:

- Gå gjennom integreringsstatusen for dataene ved å gå til **Verktøy \> Integreringsstatus** i Report Designer. Hvis integreringen ikke er fullført, må du vente til den er fullført. Deretter prøver du det du gjorde da du mottok meldingen.
- Kontakt kundestøtte for å identifisere og arbeide deg gjennom problemet. Det kan være inkonsekvente data i systemet. Støtteteknikere kan hjelpe deg med å identifisere problemet på serveren og finne bestemte data som kan kreve en oppdatering.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
