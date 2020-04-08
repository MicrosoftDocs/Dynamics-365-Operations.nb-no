---
title: Definere bankfasiliteter og posteringsprofiler for remburs
description: Denne prosedyren hjelper med å opprette en bankfasilitet og posteringsprofil som kreves for å behandle purringer.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6afa52fa2c784fd7afbdc8db0e079af0689b4bec
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144170"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Definere bankfasiliteter og posteringsprofiler for remburs

[!include [banner](../../includes/banner.md)]

Denne prosedyren hjelper med å opprette en bankfasilitet og posteringsprofil som kreves for å behandle purringer. 

Denne oppgaven bruker demonstrasjonsfirmaet USMF.






## <a name="general-ledger-parameter"></a>Parameter for økonomimodul
1. Gå til Kontant- og bankbehandling > Oppsett > Parametere for bankstyring.
2. Vis delen Bankdokument.
3. Velg alternativet Aktiver rembursimport.
4. Velg alternativet Aktiver remburseksport.
5. Klikk Lagre.
6. Lukk siden.

## <a name="create-bank-facility"></a>Opprette bankfasilitet
1. Gå til Kontant- og bankbehandling > Oppsett > Bankfasiliteter.
2. Klikk Ny.
3. I feltet Fasilitetsgruppe angir du navnet på bankfasilitetsgruppen.
4. I feltet Beskrivelse skriver du inn beskrivelsen av bankfasilitetsgruppen.
5. Klikk Lagre.
6. Klikk kategorien Fasilitetstyper.
7. Klikk Ny.
8. I Fasilitetstype-feltet angir du en unik kode.
9. Skriv inn en verdi i feltet Beskrivelse.
10. Klikk rullegardinknappen i feltet Fasilitetsgruppe for å åpne oppslaget.
11. Finn og velg ønsket post i listen.
12. Klikk koblingen i den valgte raden i listen.
13. I feltet Fasilitetens art velger du arten for bankfasiliteten.
14. Klikk Lagre.
15. Lukk siden.

## <a name="bank-posting-profile"></a>Bankposteringsprofil
1. Gå til Kontant- og bankbehandling > Oppsett > Posteringsprofil for bankdokumenter.
2. Klikk Ny.
3. Klikk rullegardinknappen i feltet Konto/gruppenummer for å åpne oppslaget.
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Velg hovedkontoen for utligning.
    * Denne kontoen brukes ved beregning av kontantstrømprognose.  
7. Velg konto for utgiftstransaksjoner i Gebyrkonto-feltet.
8. Velg konto for margintransaksjoner i Marginkonto-feltet.
    * Denne kontoen blir debitert når åpningsmarginen blir postert, og kreditert når betalingen blir postert.  
9. Klikk Lagre.

