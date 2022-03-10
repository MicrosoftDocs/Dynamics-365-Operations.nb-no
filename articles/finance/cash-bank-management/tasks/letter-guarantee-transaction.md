---
title: Garantibrevtransaksjon
description: Denne prosedyren hjelper deg gjennom garantibrevprosessen.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 206050a2c60eaeff4776b534e3f366c6998f1756bf2734461fc10b9b83f4539a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743103"
---
# <a name="letter-of-guarantee-transaction"></a>Garantibrevtransaksjon

[!include [banner](../../includes/banner.md)]

Denne prosedyren hjelper deg gjennom garantibrevprosessen.



Følgende oppgaver må være fullført før du kan gjennomføre denne prosedyren:

- Definere bankfasiliteter og posteringsprofiler for et garantibrev.

- Opprette en bankfasilitetsavtale for en remburs.



Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Opprette salgsordre med garantibrev
1. Gå til Kunder > Ordrer > Alle salgsordrer.
2. Klikk Ny.
3. Angi eller velg en verdi i Kundekonto-feltet.
4. Utvid delen Generelt.
5. Angi eller velg en verdi i Område-feltet.
6. Klikk koblingen i den valgte raden i listen.
7. Angi eller velg en verdi i feltet Lager.
8. Klikk koblingen i den valgte raden i listen.
9. Velg Garantibrev i feltet Bankdokumenttype.
10. Klikk OK.
11. Angi eller velg en verdi i Varenummer-feltet.
12. Angi et tall i feltet Enhetspris.
13. Vis seksjonen Linjedetaljer.
14. Velg kategorien Levering.
    * Obs!  Velg Leveringsdatokontroll = Ingen  
15. Angi en dato i feltet Ønsket forsendelsesdato.
16. Angi en dato i Bekreftet forsendelsesdato-feltet.

## <a name="process-letter-of-guarantee_request"></a>Behandle garantibrev_Forespørsel
1. Klikk Administrer i handlingsruten.
2. Klikk Garantibrev.
3. Klikk Garantibrev i handlingsruten.
4. Klikk Forespørsel for å åpne nedtrekksdialogen.
5. Angi eller velg en verdi i Type-feltet.
6. Klikk koblingen i den valgte raden i listen.
7. Angi et tall i Verdi-feltet.
8. Angi dato og klokkeslett i feltet Utløpsdato.
9. Klikk OK.
10. Lukk siden.

## <a name="process-letter-of-guarantee_submit-to-bank"></a>Behandle garantibrev_Send til bank
1. Gå til Kontant- og bankbehandling > Garantibrev > Garantibrev.
2. Finn og velg ønsket post i listen.
3. Klikk Send til bank for å åpne nedtrekksdialogen.
4. Angi eller velg en verdi i Bankkonto-feltet.
5. Klikk koblingen i den valgte raden i listen.
6. Klikk OK.

## <a name="process-letter-of-guarantee_receive-from-bank"></a>Behandle garantibrev_Motta fra bank
1. Klikk Motta fra bank for å åpne nedtrekksdialogen.
2. Skriv inn en verdi i feltet Banknummer.
    * Kontroller verdiene som er beregnet, i feltene Margin og Utgift.  
3. Klikk OK.
4. Utvid Handlinger-delen.
    * Kontroller posten Motta fra bank.  
5. Klikk for å følge koblingen i Journalpartinummer-feltet.
6. Klikk Linjer.
    * Kontroller posteringen av journaloppføringer.  
7. Lukk siden.

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a>Behandle garantibrev_Gi til mottaker
1. Gå til Kunder > Ordrer > Alle salgsordrer.
2. Klikk koblingen i den valgte raden i listen.
3. Klikk Administrer i handlingsruten.
4. Klikk Garantibrev.
5. Klikk Garantibrev i handlingsruten.
6. Klikk Gi til mottaker for å åpne nedtrekksdialogen.
7. Klikk OK.
8. Gå til Kontant- og bankbehandling > Garantibrev > Garantibrev.
9. Finn og velg ønsket post i listen.
10. Klikk Gi til mottaker for å åpne nedtrekksdialogen.
11. Klikk OK.
12. Utvid Handlinger-delen.
    * Valider posten Gi til mottaker.  

## <a name="process-letter-of-guarantee_increase-value"></a>Behandle garantibrev_Øk verdi
1. Gå til Kunder > Ordrer > Alle salgsordrer.
2. Klikk koblingen i den valgte raden i listen.
3. Klikk Administrer i handlingsruten.
4. Klikk Garantibrev.
5. Klikk Garantibrev i handlingsruten.
6. Klikk Øk verdi for å åpne nedtrekksdialogen.
7. Angi en verdi i feltet Verdi som skal legges til.
8. Klikk OK.
9. Gå til Kontant- og bankbehandling > Garantibrev > Garantibrev.
10. Finn og velg ønsket post i listen.
11. Klikk Øk verdi for å åpne nedtrekksdialogen.
12. Klikk OK.
13. Utvid Handlinger-delen.
    * Kontroller posten Øk verdi.  
14. Finn og velg ønsket post i listen.
15. Klikk for å følge koblingen i Journalpartinummer-feltet.
16. Klikk Linjer.
    * Kontroller de posterte journaloppføringene.  

## <a name="process-letter-of-guarantee_liquidate"></a>Behandle garantibrev_Avvikle
1. Gå til Kunder > Ordrer > Alle salgsordrer.
2. Klikk koblingen i den valgte raden i listen.
3. Klikk Administrer i handlingsruten.
4. Klikk Garantibrev.
5. Klikk Garantibrev i handlingsruten.
6. Klikk Avvikle for å åpne nedtrekksdialogen.
7. Klikk OK.
8. Gå til Kontant- og bankbehandling > Garantibrev > Garantibrev.
9. Finn og velg ønsket post i listen.
10. Klikk Avvikle for å åpne nedtrekksdialogen.
11. Klikk OK.
12. Utvid Handlinger-delen.
    * Kontroller posten Avvikle.  
13. Finn og velg ønsket post i listen.
14. Klikk for å følge koblingen i Journalpartinummer-feltet.
15. Klikk Linjer.
    * Kontroller de posterte journaloppføringene.  
16. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]