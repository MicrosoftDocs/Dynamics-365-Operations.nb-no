---
title: Nets-importformat
description: Denne artikkelen gir informasjon om å importere betalingsinformasjon i Nets-format.
author: AdamTrukawka
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Norway
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 262704
ms.search.form: BankCustPaymIdTable, CustEInvoiceIntegrationeInvoice, CustEInvoiceIntegrationTypePaymMode, CustEinvoiceIntegrationTypeTable, CustPaymMode, LedgerJournalTransCustPaym
ms.openlocfilehash: f39945654f672aebc261e67c1d6d5fc286c5fdb5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280666"
---
# <a name="nets-import-format"></a>Nets-importformat

[!include [banner](../includes/banner.md)]

Denne artikkelen gir informasjon om å importere betalingsinformasjon i Nets-format.

Du kan importere registreringsmeldinger, AvtaleGiro og eFaktura, sammen med betalingsmeldinger, optisk tegngjenkjenning (OCR), AvtaleGiro og eFakturae, i Nets-filformatet.

## <a name="import-a-nets-bank-file"></a>Importer en Nets-bankfil
Hvis du vil importere en fil fra Nets-banken, kan du fullføre trinnene nedenfor.

1. Gå til siden **Betalingsjournal**.
2. Klikk **Linjer.**
3. Klikk **Funksjoner** &gt; **Importer betalinger**.
4. I dialogboksen velger du betalingsmåten, og blar deretter til plasseringen av filen som skal importeres. I den samme dialogboksen må du også angi en **avsender-ID** for å sikre at den riktige filen er valgt for import (00008080-verdi skal angis i dialogboksen for Nets-banken). 
   > [!NOTE]
   > Før du kan fullføre dette trinnet, du må allerede ha importert **Nets (No)**-konfigurasjonene fra Lifecycle Services (LCS), og definert Nets-betalingsmåten. Hvis du vil ha mer informasjon, se [Filformater for betalingsmåter](emea-select-file-formats-for-the-method-of-payments.md).

Prosessen er den samme for import av registreringsmeldinger fra siden **eFaktura-innmelding og svar**. Uavhengig av om filen bare har betalingstransaksjoner, bare registreringsmeldinger eller begge deler, vil alt bli importert i én handling.

## <a name="ocr-avtalegiro-and-einvoice-transactions-import"></a>Import av OCR-, AvtaleGiro- og eFaktura-transaksjoner
OCR-, Avtalegiro- og eFaktura-transaksjoner må importeres og utlignes basert på betalings-IDen og genereres når fakturaene posteres. Derfor bør betalingsjournallinjene opprettes og merket for utligning med tilhørende fakturaer. **Merk**: Transaksjoner som tilsvarer fritekstmeldingskodene, utlignes ikke etter import. Du må definere en 16-sifret betalings-ID på **Betalings-ID**-siden, og deretter velge den i **Kundeparametere**. En betalings-ID er en unik identifikator for kundebetalinger som utlignes elektronisk. Den kan deles inn i ulike deler, for eksempel kundekontonummer, fakturanummer, prefiks, suffiks og ekstern referanse. Når du mottar en betaling fra en kunde, identifiserer betalings-IDen betalingstransaksjonen for en salgsfaktura som er mottatt fra en bank.

## <a name="einvoice-and-avtalegiro-enrollment-import"></a>Import av eFaktura- og AvtaleGiro-innmelding
Du får en melding om å oppdatere standard betalingsverdier for den tilsvarende kundekontoen, angitt i feltene <strong>Betalingsmåte</strong> og <strong>Betalingsspesifikasjon</strong>. Dette definerer egenskapene for eksportmeldinger som genereres for denne kundekontoen i fremtiden. Et sett med regler som skal utføres under import av filen, skal angitt på siden <strong>Importer fil og kan defineres på siden Integreringstyper for eFaktura</strong>. I forskjellige tilfeller kan du bruke forskjellige integreringstyper. Spesifikke regler skal angis på siden <strong>Endring i betalingsmåte for eFaktura</strong>. Reglene kan angis basert på meldingen <strong>Status</strong>, for eksempel Aktiv for abonnementsmeldinger, Slettet for abonnementskanselleringer og Advarsel hvis betaleren krever skriftlige varslingsattributter. Dette krever at betalingsspesifikasjoner defineres for den valgte betalingsmetoden. På siden <strong>eFaktura-innmelding og svar</strong> kan du vise importerte eFaktura-meldinger. Du kan generere svarmeldinger for å bekrefte at registreringsmeldinger et mottatt, når registreringer er klare til postering. Poster registreringene for at oppdateringene av kundekonto skal tre i kraft. For AvtaleGiro-meldinger brukes endringer av betalingsmåte under filimporten.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
