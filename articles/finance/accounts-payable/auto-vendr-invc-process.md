---
title: Oversikt over automatiserte prosesser for leverandørfakturering
description: Dette emnet beskriver muligheten til å automatisere behandling av leverandørfakturering og fordelene ved å bruke en automatisert prosess.
author: abruer
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c409b460df4c6a8b2f7811083e8c13c8fdfc186c09f859ecb91e2f3cc0b8b59f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749132"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Oversikt over automatiserte prosesser for leverandørfakturering

[!include [banner](../includes/banner.md)]

Dette emnet beskriver muligheten til å automatisere behandling av leverandørfakturering og fordelene ved å bruke en automatisert prosess. Denne funksjonen består av funksjoner som er aktivert i Funksjonsbehandling. Disse funksjonene gjelder bare leverandørfakturaer, ikke for fakturaer som behandles ved hjelp av siden **Fakturajournal** eller **Ankomstregistreringsjournal**.

Organisasjoner arbeider ofte med tredjeparter for å behandle papirfakturaer ved hjelp av tjenesteleverandør for optisk tegngjenkjenning (OCR). Tjenesteleverandøren returnerer maskinlesbare fakturametadata. Hvis du vil ha hjelp med automatisering, kan du bruke disse artefaktene fra leverandører i funksjonene for leverandørautomatisering.

Du kan automatisere noen prosesser for leverandørfakturering for leverandør. Disse prosessene omfatter sending av importerte leverandørfakturaer til arbeidsflytsystemet og samsvarende posterte produktkvitteringslinjer til ventende leverandørfakturalinjer. Den automatiserte prosessen viser informasjon om fremdriften for en leverandørfaktura når den går gjennom hver av prosessene. Ved hjelp av denne funksjonen kan regnskapsassistenter og ledere hos leverandør behandle leverandørfakturaer mer effektivt. Det bidrar også til å redusere feil og ineffektivitet som kan oppstå når informasjon registreres manuelt og behandles.

Automatiseringsprosessene kan brukes til å utføre følgende oppgaver:

- Send automatisk importerte fakturaer til arbeidsflytsystemet.
- Samsvare produktkvitteringer med ventende leverandørfakturalinjer.
- Simulere postering før en leverandørfaktura posteres.
- Vise loggen for arbeidsflyt og automatisering raskt og effektivt.
- Vise og analysere resultatene av automatisering av behandling av leverandørfaktura.
- Gjenoppta automatisert behandling for flere fakturaer.

## <a name="submit-imported-vendor-invoices-to-the-workflow-system"></a>Send inn importerte leverandørfakturaer til arbeidsflytsystemet

Som en del av en berøringsfri faktureringsprosess for leverandører, kan du få systemet til automatisk å sende en importert faktura til arbeidsflytsystemet. Prosessen vil kjøre i bakgrunnen med en angitt hyppighet (enten hver time eller daglig). Muligheten til automatisk å sende importerte fakturaer til arbeidsflytsystemet krever at prosessen begynner med en importert faktura. Hvis du vil sikre at fakturaen kan behandles fra start til slutt uten manuell behandling, må en automatisk posteringsoppgave inkluderes i arbeidsflytkonfigurasjonen.


Fakturaer som er knyttet til bestillinger og fakturaer som inneholder en ikke-bestillingsinnkjøpskategori og ikke-lagerførte linjer, kan sendes automatisk til arbeidsflytsystemet. Fakturaer som registreres manuelt og fakturaer som opprettes ved hjelp av arbeidsområdet **Leverandørsamarbeidsfakturering** må sendes manuelt til arbeidsflytsystemet. Behandling av søknad om forskuddsbetaling må utføres manuelt for importerte fakturaer. Du kan bruke forskuddsbetalinger manuelt før eller etter at den importerte fakturaen er postert. Du kan manuelt bruke forskuddsbetalinger på ikke-posterte standardfakturaer ved hjelp av siden **Leverandørfakturaer**. Etter posteringen vil den utlignede forskuddsbetalingen være tilgjengelig slik at den kan brukes manuelt for andre fakturaer fra denne leverandøren på siden **Leverandører** (**Leverandører \> Felles \> Leverandører \> Alle leverandører \> Fanen Faktura \> Bruk**).

Automatiseringsfunksjonen gir et fleksibelt rammeverk som gjør det mulig å definere firmaspesifikke regler for sending av importerte leverandørfakturaer til arbeidsflytsystemet og tilsvarende posterte produktkvitteringslinjer til ventende leverandørfakturalinjer.

## <a name="match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Samsvare produktkvitteringer med fakturalinjer som har en treveis kontrollpolicy

Systemet kan automatisk sammenligne posterte produktkvitteringer med fakturalinjer som en treveis kontrollpolicy er definert for. Prosessen vil kjøre til det samsvarende produktkvitteringsantallet er lik fakturaantallet. Som en del av denne prosessen kan du angi det maksimale antall ganger som systemet skal prøve å samsvare produktkvitteringer med en fakturalinje før prosessen mislykkes. Prosessen kjøres i bakgrunnen, enten hver time eller hver dag. Du kan kjøre den automatiserte samsvarsprosessen som en del av prosessen for å sende fakturaer til arbeidsflytsystemet. Du kan også kjøre den som en frittstående prosess.

## <a name="pre-validate-vendor-invoice-posting"></a>Forhåndsvalidere leverandørfakturapostering

Posteringssimulering fullfører valideringstrinnene som utføres under posteringsprosessen for leverandørfakturaer, men ingen kontoer oppdateres. Når du skal kjøre en prosess, kan du velge én eller flere fakturaer på siden **Ventende leverandørfakturaer**.

## <a name="enhanced-experience-for-viewing-workflow-and-automation-historical-information-for-vendor-invoices"></a>Forbedret opplevelse for visning av arbeidsflyt og automatisk historisk informasjon for leverandørfakturaer

Det finnes en oversiktlig visning av arbeidsflytloggen for leverandørfaktura. Du kan få tilgang til arbeidsflytloggen for leverandørfaktura direkte fra leverandørfakturaen. Derfor kreves det færre klikk for å finne denne informasjonen. Hvis organisasjonen har aktivert funksjonen for å sende importerte leverandørfakturaer til arbeidsflyten automatisk, blir automatiseringsloggen tilgjengelig for de importerte fakturaene. Automatiseringsloggen hjelper deg å identifisere det gjeldende prosesstrinnet, i tillegg til trinnene som allerede er fullført. Når et trinn mislykkes, inneholder systemet detaljert informasjon som hjelper deg å forstå årsaken til feilen.

## <a name="analytics-and-metrics"></a>Analyse og telemetri

Arbeidsområdet **Leverandørfakturaregistrering** lar deg fokusere på leverandørfakturaer som ikke kom gjennom den automatiserte prosessen. Fliser på arbeidsområde viser informasjon om leverandørfakturaer som ikke ble sendt til arbeidsflytsystemet, importert eller tilordnet til produktkvitteringer. Måledata for Microsoft Power BI blir også formidlet for å gi leverandøransvarlige innsikt i effektiviteten til automatisering av leverandørfakturaer.


## <a name="resume-automation-processing-for-multiple-invoices"></a>Gjenoppta automatisert behandling for flere fakturaer

Når en importert faktura ikke kan sendes til arbeidsflyten ved hjelp av den automatiserte prosessen, vil systemet fjerne den fra ytterligere automatisert behandling. En regnskapsassistent kan se gjennom og redigere fakturaen før den automatiserte prosessen sender den til arbeidsflyten på nytt. Når årsaken til en feil kan løses med samme rettelse for flere fakturaer, kan du starte den automatiserte prosessen på nytt på siden **Gjenoppta automatisert fakturabehandling**. 

## <a name="tracking-the-invoice-received-date-value"></a>Spore verdien av mottatt dato for faktura

Verdien **Dato for mottatt faktura** angir datoen da firmaet mottok fakturaen fra leverandøren. Her finner du et utgangspunkt for å spore fakturaens fremgang gjennom de automatiske prosessene. Denne verdien kan tas med i de importerte dataene for en leverandørfaktura. For fakturaer som ble opprettet manuelt, kan du angi datoen. Hvis ingen verdi angis, brukes gjeldende dato som standard.


## <a name="tracking-the-imported-invoice-amount-and-imported-sales-tax-amount-values"></a>Spore importerte fakturabeløp og importerte mva-beløpsverdier

Verdiene **Importert fakturabeløp** og **Importert mva-beløp** for leverandørfakturaer kan oppgis i importfilen for leverandørfakturaene. Disse verdiene kommer vanligvis fra en faktura som ble skannet av en ekstern leverandør og inkludert i importfilen. Etter hvert som fakturaen behandles i Leverandør, beregner systemet verdier på grunnlag av fakturadataene. Fakturaen kan bare posteres hvis de importerte verdiene samsvarer med de beregnede verdiene. Samsvarende verdier sikrer at fakturaen gjenspeiler beløpet som forfaller til leverandøren. Hvis organisasjonen tillater at importerte fakturaer kan sendes til arbeidsflytsystemet automatisk, kan du velge å kreve at de importerte totalene samsvarer med de beregnede totalene før fakturaen kan sendes til arbeidsflytsystemet.

## <a name="vendor-invoice-automation---resume-automation-processing-for-multiple-invoices"></a>Automatisering av leverandørfaktura – Fortsett automatiseringsbehandling for flere fakturaer
Når en importert faktura ikke kan sendes til arbeidsflyten gjennom den automatiserte prosessen, vil systemet fjerne den fra ytterligere automatisert behandling. En regnskapsassistent kan se gjennom og redigere fakturaen før den automatiserte prosessen sender den til arbeidsflyten på nytt. Når årsaken til en feil kan løses med samme rettelse for flere fakturaer, kan du starte den automatiserte prosessen på nytt på siden **Gjenoppta automatisert fakturabehandling**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
