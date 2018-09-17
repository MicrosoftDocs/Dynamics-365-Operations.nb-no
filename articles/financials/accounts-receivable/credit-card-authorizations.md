---
title: Oppsett av kredittkort, autorisasjon og registrering
description: "Denne artikkelen gir en oversikt over kredittkortautorisering i Microsoft Dynamics 365 for Finance and Operations. Den inneholder informasjon om å sette opp en betalingstjeneste, legge til et kredittkort til en salgsordre og annullere en autorisering."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4a6354563fdebff901498f1cd6caed3aedae668b
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="credit-card-setup-authorization-and-capture"></a>Oppsett av kredittkort, autorisasjon og registrering

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Denne artikkelen gir en oversikt over kredittkortautorisering i Microsoft Dynamics 365 for Finance and Operations. Den inneholder informasjon om å sette opp en betalingstjeneste, legge til et kredittkort til en salgsordre og annullere en autorisering.

<a name="setting-up-the-credit-card-payment-service"></a>Konfigurere kredittkortbetalingstjenesten
------------------------------------------

Hvis du vil bruke kredittkort, må du definere og aktivere en betalingstjeneste på siden Betalingstjenester. En betalingstjeneste fungerer som et bindeledd mellom den juridiske enheten og banken som behandler kundens kredittkortbelastninger. Du må kontakte en kredittkortleverandør som er oppført i feltet Betalingskobling og sette opp en konto hos denne leverandøren. Deretter må du definere de andre alternativene på siden Betalingstjenester, definere kredittkorttyper for American Express, Discover, MasterCard og Discover på siden Kredittkorttyper, og aktivere leverandøren som standardleverandøren. Du må også følge disse trinnene for å fullføre oppsettet:
-   Angi parametere for å bruke kredittkortautoriseringer på siden Kundeparametere.
-   På siden Betalingsbetingelser defineres betalingsbetingelsene for kredittkort. Velg Kredittkort i Betalingstype-feltet.
-   Angi kredittkortinformasjonen for kunder på siden Kundekredittkort.

## <a name="adding-a-new-credit-card"></a>Legge til et nytt kredittkort
Du kan opprette nye kredittkortoppføringer på Kunder-siden ved hjelp av Kunde, Oppsett, Kredittkort. Du kan også opprette kredittkortposter når du registrerer salgsordrer på siden Salgsordre ved hjelp av Behandle, Kunde, Kredittkort, Registrer.

<a name="adding-a-credit-card-to-a-sales-order"></a>Legge til et kredittkort i en salgsordre
-------------------------------------

Du kan legge til et kredittkort i en salgsordre ved å velge et kredittkort i kredittkortoppslaget i hurtigfanen Pris og rabatter på siden Salgsordre. Velg Kredittkort og Autoriser i kategorien Behandle i handlingsruten for å starte godkjenningsprosessen.

<a name="authorizing-a-credit-card"></a>Autorisere et kredittkort
-------------------------

Når et kredittkort autoriseres, verifiseres kredittkortnummeret og kredittkortinnehaverens navn, og tilgjengelig kredittkortsaldo kontrolleres. Du kan også autorisere verdien for kortbekreftelse og kortinnehaverens adresse. Deretter trekkes fakturabeløpet fra kundens tilgjengelige kredittkortsaldo. Betalingstjenesten sender informasjon som angir om kredittkortet er godkjent eller ikke. Når salgsordren faktureres, belastes kredittkortet med fakturabeløpet.

### <a name="card-verification-value"></a>Verdi for kortbekreftelse

Du kan kreve verdi for kortbekreftelse, som noen ganger kalles kortets sikkerhetskode. Dette er en firesifret verdi for American Express. Discover, MasterCard og Visa har en tresifret verdi.

### <a name="address-verification"></a>Adressebekreftelse

Informasjon om adressebekreftelse sendes alltid til betalingsleverandøren. Du kan bestemme hvor mye informasjon som er nødvendig for at en transaksjon skal godtas. Husk å ta kontakt med leverandøren din for å finne ut om de godtar denne informasjonen. Her er alternativene for adressebekreftelse:
-   **Alltid godta transaksjon** – godta transaksjonen uavhengig av resultatet av adressebekreftelse.
-   **Kontoinnehaver** – sammenlign kortinnehaverens navn fra transaksjonen med kredittkortfirmaets informasjon.
-   **Faktureringsadresse** – sammenlign kortinnehaverens navn og faktureringsadresse fra transaksjonen med kredittkortfirmaets informasjon.
-   **Postnummer for fakturering** – sammenlign kortholderen navn, faktureringsadresse og postnummer fra transaksjonen med kredittkortfirmaets informasjon.

## <a name="data-support"></a>Datastøtte
For hver kredittkorttype som støttes, kan du angi nivået for datastøtte. Nivået kontrollerer hvor mye informasjon om en transaksjon som overføres til betalingstjenesten. Husk å ta kontakt med leverandøren din for å finne ut om de kan gi denne informasjonen. Her er alternativene for nivå for datastøtte:
-   **Nivå 1** – overfør transaksjonsdatoen, transaksjonsbeløpet og beskrivelsen.
-   **Nivå 2** – overfør all informasjon på nivå 1, pluss leverings-og forhandleradresser og avgiftsinformasjon.
-   **Nivå 3** – overfør all nivå 2-informasjon, pluss ordrelinjeinformasjon.

## <a name="partial-payments"></a>Delbetalinger
Hvis du sender en del av en ordre, registreres beløpet for den delvise ordren, og autorisasjonen, som var for beløpet for hele ordren, lukkes. En ny godkjenning sendes deretter for det gjenstående beløpet for ordren som ikke er levert.

## <a name="voiding-an-authorization"></a>Annullere en autorisasjon 
Hvis du vil annullere en kredittkortautorisasjon, kan du endre betalingsmåten til en annen metode som ikke har en type kredittkort






