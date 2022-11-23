---
title: Definere bankfasiliteter og posteringsprofiler for remburs
description: Denne prosedyren hjelper med å opprette en bankfasilitet og posteringsprofil som kreves for å behandle purringer.
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
ms.openlocfilehash: 7fe5b2ba43c4fcb4855c742bdb6f8209ebd92d68
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779469"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Definere bankfasiliteter og posteringsprofiler for remburs

[!include [banner](../../includes/banner.md)]

Denne prosedyren hjelper med å opprette en bankfasilitet og posteringsprofil som kreves for å behandle purringer. 

Denne oppgaven bruker demonstrasjonsfirmaet USMF.


## <a name="general-ledger-parameter"></a>Parameter for økonomimodul
1. Gå til **Kontant- og bankbehandling > Oppsett > Parametere for bankstyring**.
2. Vis delen **Bankdokument**.
3. Velg alternativet **Aktiver rembursimport**.
4. Velg alternativet **Aktiver remburseksport**.
5. Klikk på **Lagre**.
6. Lukk siden.

## <a name="create-bank-facility"></a>Opprette bankfasilitet
1. Gå til **Kontant- og bankbehandling > Oppsett > Bankfasiliteter**.
2. Klikk på **Ny**.
3. I feltet **Fasilitetsgruppe** angir du navnet på bankfasilitetsgruppen.
4. I feltet **Beskrivelse** skriver du inn beskrivelsen av bankfasilitetsgruppen.
5. Klikk på **Lagre**.
6. Klikk kategorien **Fasilitetstyper**.
7. Klikk på **Ny**.
8. I **Fasilitetstype**-feltet angir du en unik kode.
9. Skriv inn en verdi i **Beskrivelse**-feltet.
10. Klikk rullegardinknappen i feltet **Fasilitetsgruppe** for å åpne oppslaget.
11. Finn og velg ønsket post i listen.
12. Klikk koblingen i den valgte raden i listen.
13. I feltet **Fasilitetens art** velger du arten for bankfasiliteten.
14. Klikk på **Lagre**.
15. Lukk siden.

## <a name="bank-posting-profile"></a>Bankposteringsprofil
1. Gå til **Kontant- og bankbehandling > Oppsett > Posteringsprofil for bankdokumenter**.
2. Klikk på **Ny**.
3. Klikk rullegardinknappen i feltet **Konto/gruppenummer** for å åpne oppslaget.
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Velg hovedkontoen for utligning.
    * Denne kontoen brukes ved beregning av kontantstrømprognose.  
7. Velg konto for utgiftstransaksjoner i **Gebyrkonto**-feltet.
8. Velg konto for margintransaksjoner i **Marginkonto**-feltet.
    * Denne kontoen blir debitert når åpningsmarginen blir postert, og kreditert når betalingen blir postert.  
9. Klikk på **Lagre**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
