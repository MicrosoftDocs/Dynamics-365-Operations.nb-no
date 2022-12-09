---
title: Definere bankfasiliteter og posteringsprofiler for garantibrev
description: Denne oppgaven oppretter en bankfasilitet og posteringsprofil som er nødvendig for å behandle et garantibrev.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0987ae1e9cfbb1e2d2a957a5fd1ad82257292c0a
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804108"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Definere bankfasiliteter og posteringsprofiler for garantibrev

[!include [banner](../../includes/banner.md)]

Denne oppgaven oppretter en bankfasilitet og posteringsprofil som er nødvendig for å behandle et garantibrev.



Denne oppgaven bruker demonstrasjonsfirmaet USMF. 




## <a name="general-ledger-parameter"></a>Parameter for økonomimodul
1. Gå til **Kontant- og bankbehandling > Oppsett > Parametere for bankstyring**.
2. Vis delen **Bankdokument**.
3. Velg alternativet **Aktiver garantibrev**.
4. Klikk rullegardinknappen i feltet **Transaksjonsjournal** for å åpne oppslaget.
5. Finn og velg ønsket post i listen.
6. Klikk koblingen i den valgte raden i listen.
7. Klikk kategorien **Nummerserier**.
    * Definere nummerseriekode for garantibrevnummer og transaksjonsreferanser for garantibrev  
8. Klikk på **Lagre**.
9. Lukk siden.

## <a name="create-bank-facility"></a>Opprette bankfasilitet
1. Gå til **Kontant- og bankbehandling > Oppsett > Bankfasiliteter**.
2. Klikk på **Ny**.
3. I feltet **Fasilitetsgruppe** angir du navnet på bankfasilitetsgruppen for garantibrevtransaksjonen.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Klikk på **Lagre**.
6. Klikk kategorien **Fasilitetstyper**.
7. Klikk på **Ny**.
8. I feltet **Fasilitetstype** skriver du inn navnet på bankfasilitetstypen som er relatert til bankfasilitetsavtalen.
9. Skriv inn en verdi i **Beskrivelse**-feltet.
10. Klikk rullegardinknappen i feltet **Fasilitetsgruppe** for å åpne oppslaget.
11. Finn og velg ønsket post i listen.
12. Klikk koblingen i den valgte raden i listen.
13. Velg et alternativ i feltet **Fasilitetens art**.
14. Klikk på **Lagre**.
15. Lukk siden.

## <a name="bank-posting-profile"></a>Bankposteringsprofil
1. Gå til **Kontant- og bankbehandling > Oppsett > Posteringsprofil for bankdokumenter**.
2. Klikk på **Ny**.
3. Klikk rullegardinknappen i feltet **Konto/gruppenummer** for å åpne oppslaget.
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Velg hovedkonto for utligning i **Utligningskonto**-feltet.
7. Velg konto for utgiftstransaksjoner i **Gebyrkonto**-feltet.
8. Velg konto for margintransaksjonen i **Marginkonto**-feltet.
9. I **Likvidasjonskonto**-feltet velger du likvidasjonskontoen for garantibrevtransaksjonen. 
10. Klikk på **Lagre**.
11. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
