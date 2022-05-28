---
title: Definere bankfasiliteter og posteringsprofiler for remburs
description: Denne prosedyren hjelper med å opprette en bankfasilitet og posteringsprofil som kreves for å behandle purringer.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 15a7a4798c4c743c9171fd2258a5573f456c92e5
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726357"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
