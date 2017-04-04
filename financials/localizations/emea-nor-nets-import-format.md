---
title: Nett-importformat
description: "Dette emnet gir informasjon om å importere betalingsinformasjon i nett-format."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankCustPaymIdTable, CustEInvoiceIntegrationeInvoice, CustEInvoiceIntegrationTypePaymMode, CustEinvoiceIntegrationTypeTable, CustPaymMode, LedgerJournalTransCustPaym
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262704
ms.assetid: 0327a01b-3b24-41be-afa6-ffa6c365cb0b
ms.search.region: Norway
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: 4b3d7802d63b36deb996e7cff79252255b20da02
ms.lasthandoff: 03/31/2017


---

# <a name="nets-import-format"></a>Nett-importformat

Dette emnet gir informasjon om å importere betalingsinformasjon i nett-format.

I Microsoft Dynamics 365 for operasjoner, kan du importere meldinger for registrering, AvtaleGiro og eFaktura, sammen med betaling meldinger, optisk tegngjenkjenning (OCR), AvtaleGiro og eFakturaen, i nett-format.

## <a name="import-a-nets-bank-file"></a>Importere en nett bank
Hvis du vil importere en fil fra banken på nett, kan du fullføre trinnene nedenfor.

1.  Gå til den **betalingsjournal** side
2.  Klikk **linjer.**
3.  Klikk **funksjoner**&gt;**importerer betalinger**.
4.  I dialogboksen Velg betalingsmåten, og gå deretter til plasseringen til filen som skal importeres. I den samme dialogboksen, må du også angi en **avsender-ID** å sikre at den riktige filen er valgt for import (00008080 verdi skal angis i dialogboksen for nett-bank). 
  > [!NOTE]
  > Før du kan fullføre dette trinnet, du må har allerede importert den **nett (Nei)** konfigurasjoner fra Lifecycle tjenester (LCS), og Definer nett betalingsmåten. Hvis du vil ha mer informasjon, se [filformater for betalinger-metoden](emea-select-file-formats-for-the-method-of-payments.md).

Prosessen er den samme for import påmelding meldinger fra den **eFaktura-innmelding og svar** siden. Uavhengig av om filen har bare betalingstransaksjoner bare registrering meldinger eller begge deler, alt vil bli importert i én handling.

## <a name="ocr-avtalegiro-and-einvoice-transactions-import"></a>Importere OCR, AvtaleGiro og eFaktura-transaksjoner
OCR, Avtalegiro og eFaktura transaksjoner må importeres og utlignet basert på betalings-IDen og genereres når fakturaer posteres. Derfor bør betalingskladdelinjene opprettet og merket for utligning med tilhørende fakturaer. **Legg merke til**: transaksjoner som tilsvarer Fritekst melding kodene ikke er utlignet etter import. Du må definere en 16-sifret betalings-ID på den **KID** side, og deretter velger du den i **konto Kundeparametere**. En betalings-ID er en unik identifikator for kundebetalinger som utlignes elektronisk. Den kan deles inn i ulike deler, for eksempel kundekontonummer, fakturanummer, prefiks, suffiks og ekstern referanse. Når du mottar en betaling fra en kunde, identifiserer betalings-IDen betalingstransaksjonen for en salgsfaktura som er mottatt fra en bank.

## <a name="einvoice-and-avtalegiro-enrollment-import"></a>eFaktura og AvtaleGiro registrering import
Du får en melding å oppdatere betalings standarder verdier for tilsvarende kundekontoen, som angitt i den **betalingsmåte** og **betalingsspesifikasjon** felt. Dette definerer egenskapene for eksport-meldinger, som er generert for denne kundekontoen i fremtiden. Et sett med regler som er ment å bli utført under import av filen bør være angitt på den ** importfilen ** side og kan defineres i den **integreringstyper for eFaktura** siden. I andre tilfeller kan du bruke av forskjellige integreringstyper. Spesifikke regler som skal angis på den **eFaktura betalingsmåteendringen** siden. Reglene kan angis basert på meldingen **Status**, for eksempel aktiv for Abonnementsmeldinger, slettede for abonnement annulleringer og advarsel hvis betaler krever skriftlig varsel attributter. Dette krever betalingsspesifikasjoner defineres for den valgte betalingsmåten. På den **eFaktura-innmelding og svar** -siden kan du vise importerte eFaktura-meldinger. Du kan generere svar meldinger for å bekrefte registrering-meldinger mottas, når registreringer er klare til postering. Bokføre registreringer for kunden konto oppdateringene skal tre i kraft. Betalingsmåte brukes for AvtaleGiro meldinger under importen av filen.


