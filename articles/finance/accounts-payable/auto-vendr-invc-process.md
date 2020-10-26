---
title: Oversikt over automatiserte prosesser for leverandørfakturering
description: Dette emnet beskriver muligheten til å automatisere behandling av leverandørfakturering og fordelene ved å bruke en automatisert prosess.
author: abruer
manager: AnnBe
ms.date: 08/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 187b3c4f1a8b2c9ec6df95c19b261756ec4562dc
ms.sourcegitcommit: 6ffbae02de2eee1f3be9bab2da37a3771aae8bec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2020
ms.locfileid: "3905027"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Oversikt over automatiserte prosesser for leverandørfakturering

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver muligheten til å automatisere behandling av leverandørfakturering og fordelene ved å bruke en automatisert prosess. Denne funksjonen består av funksjoner som er aktivert i Funksjonsbehandling. Disse funksjonene gjelder bare leverandørfakturaer, ikke for fakturaer som behandles via siden **Fakturajournal** eller **Ankomstregistreringsjournal** .

Organisasjoner arbeider ofte med tredjeparter for å behandle papirfakturaer ved hjelp av tjenesteleverandør for optisk tegngjenkjenning (OCR). Tjenesteleverandøren returnerer maskinlesbare fakturametadata. Hvis du vil ha hjelp med automatisering, kan du bruke disse artefaktene fra leverandører i funksjonene for leverandørautomatisering.

Du kan automatisere noen prosesser for leverandørfakturering for leverandør. Disse prosessene omfatter sending av importerte leverandørfakturaer til arbeidsflytsystemet og samsvarende posterte produktkvitteringslinjer til ventende leverandørfakturalinjer. Den automatiserte prosessen viser informasjon om fremdriften for en leverandørfaktura når den går gjennom hver av prosessene. Ved hjelp av denne funksjonen kan regnskapsassistenter og ledere hos leverandør behandle leverandørfakturaer mer effektivt. Det bidrar også til å redusere feil og ineffektivitet som kan oppstå når informasjon registreres manuelt og behandles.

Automatiseringsprosessene kan brukes til å utføre følgende oppgaver:

- Send automatisk importerte fakturaer til arbeidsflytsystemet.
- Samsvare produktkvitteringer med ventende leverandørfakturalinjer.
- Simulere postering før en leverandørfaktura posteres.
- Vise arbeidsflytloggen på en rask og effektiv måte.
- Vise og analysere resultatene av automatisering av behandling av leverandørfaktura.

## <a name="vendor-invoice-automation--submit-imported-vendor-invoices-to-the-workflow-system"></a>Automatisering av leverandørfaktura – Sende importerte leverandørfakturaer til arbeidsflytsystemet

Som en del av en berøringsfri faktureringsprosess for leverandører, kan du få systemet til automatisk å sende en importert faktura til arbeidsflytsystemet. Prosessen vil kjøre i bakgrunnen med en angitt hyppighet (enten hver time eller daglig). Muligheten til automatisk å sende importerte fakturaer til arbeidsflytsystemet krever at prosessen begynner med en importert faktura. Hvis du vil sikre at fakturaen kan behandles fra start til slutt uten manuell behandling, må en automatisk posteringsoppgave inkluderes i arbeidsflytkonfigurasjonen.

Fakturaer som er knyttet til bestillinger og fakturaer som inneholder en ikke-bestillingsinnkjøpskategori og ikke-lagerførte linjer, kan sendes automatisk til arbeidsflytsystemet. Fakturaer som registreres manuelt og fakturaer som opprettes via arbeidsområdet **Leverandørsamarbeidsfakturering** må sendes manuelt til arbeidsflytsystemet.

Automatiseringsfunksjonen gir et fleksibelt rammeverk som gjør det mulig å definere firmaspesifikke regler for sending av importerte leverandørfakturaer til arbeidsflytsystemet og tilsvarende posterte produktkvitteringslinjer til ventende leverandørfakturalinjer.

## <a name="vendor-invoice-automation--match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Automatisering av leverandørfakturaer – Samsvarer produktkvitteringer med fakturalinjer som har en treveis kontrollpolicy

Systemet kan automatisk sammenligne posterte produktkvitteringer med fakturalinjer som en treveis kontrollpolicy er definert for. Prosessen vil kjøre til det samsvarende produktkvitteringsantallet er lik fakturaantallet. Som en del av denne prosessen kan du angi det maksimale antall ganger som systemet skal prøve å samsvare produktkvitteringer med en fakturalinje før prosessen mislykkes. Prosessen kjøres i bakgrunnen, enten hver time eller hver dag. Du kan kjøre den automatiserte samsvarsprosessen som en del av prosessen for å sende fakturaer til arbeidsflytsystemet. Du kan også kjøre den som en frittstående prosess.

## <a name="vendor-invoice-automation--pre-validate-vendor-invoice-posting"></a>Automatisering av leverandørfaktura – Forhåndsvalidere postering av leverandørfaktura

Posteringssimulering fullfører valideringstrinnene som utføres under posteringsprosessen for leverandørfakturaer, men ingen kontoer oppdateres. Når du skal kjøre en prosess, kan du velge én eller flere fakturaer på siden **Ventende leverandørfakturaer** .

## <a name="vendor-invoice-automation--enhanced-experience-for-viewing-workflow-historical-information-for-vendor-invoices"></a>Automatisering av leverandørfaktura – Forbedret opplevelse for visning av historisk informasjon om arbeidsflyt for leverandørfakturaer

Det finnes en oversiktlig visning av arbeidsflytloggen for leverandørfaktura. Du kan få tilgang til arbeidsflytloggen for leverandørfaktura direkte fra leverandørfakturaen. Derfor kreves det færre klikk for å finne denne informasjonen.

## <a name="vendor-invoice-automation--analytics-and-metrics"></a>Automatisering av leverandørfaktura – Analyse og måledata

Arbeidsområdet **Leverandørfakturaregistrering** lar deg fokusere på leverandørfakturaer som ikke kom gjennom den automatiserte prosessen. Fliser på arbeidsområde viser informasjon om leverandørfakturaer som ikke ble sendt til arbeidsflytsystemet, importert eller tilordnet til produktkvitteringer. Du får også Microsoft Power BI-måledata for å gi leverandøransvarlige innsikt i effektiviteten til automatisering av leverandørfakturaer.
