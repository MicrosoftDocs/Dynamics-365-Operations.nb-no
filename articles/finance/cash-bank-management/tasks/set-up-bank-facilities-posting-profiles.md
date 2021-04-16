---
title: Definere bankfasiliteter og posteringsprofiler for garantibrev
description: Denne oppgaven oppretter en bankfasilitet og posteringsprofil som er nødvendig for å behandle et garantibrev.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1147650944ba40d1c8054444c09db9c5ee97bde3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834626"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Definere bankfasiliteter og posteringsprofiler for garantibrev

[!include [banner](../../includes/banner.md)]

Denne oppgaven oppretter en bankfasilitet og posteringsprofil som er nødvendig for å behandle et garantibrev.



Denne oppgaven bruker demonstrasjonsfirmaet USMF. 




## <a name="general-ledger-parameter"></a>Parameter for økonomimodul
1. Gå til Kontant- og bankbehandling > Oppsett > Parametere for bankstyring.
2. Vis delen Bankdokument.
3. Velg alternativet Aktiver garantibrev.
4. Klikk rullegardinknappen i feltet Transaksjonsjournal for å åpne oppslaget.
5. Finn og velg ønsket post i listen.
6. Klikk koblingen i den valgte raden i listen.
7. Klikk kategorien Nummerserier.
    * Definere nummerseriekode for garantibrevnummer og transaksjonsreferanser for garantibrev  
8. Klikk Lagre.
9. Lukk siden.

## <a name="create-bank-facility"></a>Opprette bankfasilitet
1. Gå til Kontant- og bankbehandling > Oppsett > Bankfasiliteter.
2. Klikk Ny.
3. I feltet Fasilitetsgruppe angir du navnet på bankfasilitetsgruppen for garantibrevtransaksjonen.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk Lagre.
6. Klikk kategorien Fasilitetstyper.
7. Klikk Ny.
8. I feltet Fasilitetstype skriver du inn navnet på bankfasilitetstypen som er relatert til bankfasilitetsavtalen.
9. Skriv inn en verdi i Beskrivelse-feltet.
10. Klikk rullegardinknappen i feltet Fasilitetsgruppe for å åpne oppslaget.
11. Finn og velg ønsket post i listen.
12. Klikk koblingen i den valgte raden i listen.
13. Velg et alternativ i feltet Fasilitetens art.
14. Klikk Lagre.
15. Lukk siden.

## <a name="bank-posting-profile"></a>Bankposteringsprofil
1. Gå til Kontant- og bankbehandling > Oppsett > Posteringsprofil for bankdokumenter.
2. Klikk Ny.
3. Klikk rullegardinknappen i feltet Konto/gruppenummer for å åpne oppslaget.
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Velg hovedkonto for utligning i Utligningskonto-feltet.
7. Velg konto for utgiftstransaksjoner i Gebyrkonto-feltet.
8. Velg konto for margintransaksjonen i Marginkonto-feltet.
9. I Likvidasjonskonto-feltet velger du likvidasjonskontoen for garantibrevtransaksjonen. 
10. Klikk Lagre.
11. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]