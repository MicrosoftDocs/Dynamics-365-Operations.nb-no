---
title: Feilsøking i forbindelse med priser, rabatter og avtaler
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med priser, rabatter og avtaler.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2ccc1d52b83f9319af1c6336c1876c795c70028a
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908525"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a>Feilsøking i forbindelse med priser, rabatter og avtaler

Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med priser, rabatter og avtaler.

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a>Jeg kan ikke koble en kjøpsavtale til en bestillingslinje etter at bestillingen er opprettet.

En kjøpsavtale må knyttes til en bestilling når bestillingen opprettes. Hvis ikke kan ikke bestillingslinjer knyttes til kjøpsavtalelinjer.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Hvilken kontroll utløser meldingen "Oppdater priser og rabatter som er angitt manuelt eller eksternt dokument"?

Når du endrer leveringsdatoen, kan du få en melding om å oppdatere priser og rabatter som er angitt manuelt, eller eksternt dokument. Du får denne meldingen fordi hvis leveringsdatoen endres, kan en annen handels- eller salgsavtale utløses og føre til en prisendring. En endring i forsendelsesdatoen kan også ha innvirkning på lagerplanene og annen relatert informasjon.

Meldingen utløses når en av datoene eller en annen parameter endres. Formålet med meldingen er å sørge for at du kjenner til prisendringer som kan forekomme på grunn av endringene.

Meldingen er anmodningen om evaluering av forretningsavtale (TAE). Hvis du vil ha en fullstendig beskrivelse, se [Evalueringspolicyer for forretningsavtale](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>En bestillingskvittering omfatter ikke alle gebyrer.

### <a name="reproduce-the-issue"></a>Reprodusere problemet

Følgende prosedyre viser én måte å reprodusere problemet på.

1. På siden for **Parametere for innkjøp og leverandører**, i fanen **Levering**, må du kontrollere at alternativet for **Generer tillegg på produktkvittering** er satt til *Ja*.
1. Opprette en bestilling som inkluderer tillegg.
1. Bekreft bestillingen.
1. Motta bestillingen.
1. Se på det kvitteringstotalen, og sammenlign den med forventet totalbeløp.
1. Legg merke til at ikke alle gebyrene er inkludert i bestillingskvitteringen.

### <a name="issue-resolution"></a>Problemløsning

Oppløsningen avhenger av hvordan tilleggene er definert. Hvis du vil ha informasjon om hvordan du definerer tillegg for å oppfylle dine behov, kan du se følgende blogginnlegg: [Poster tilleggskostnader på tidspunktet for produktkvitteringen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a>Forretningsavtalepriser og -rabatter blir ikke tatt i bruk på salgs- eller bestillingslinjer som er importert via databehandling.

### <a name="issue-description"></a>Problembeskrivelse

Forretningsavtaler som gjelder salgs- eller bestillingslinjer, brukes ikke på linjer som er importert via databehandling. De samme forretningsavtalene brukes imidlertid på salgs- eller bestillingslinjer som opprettes manuelt.

### <a name="reason-for-the-issue"></a>Årsak til problemet

Hvis innkjøpsordrelinjer som er importert via databehandling, allerede inkluderer prisinformasjon, blir ikke forretningsavtalen evaluert på nytt for disse linjene. Hvis for eksempel **Linjerabatt i prosent** eller noen av pris- og rabattverdiene er angitt for en linje, vil det ikke bli slått opp forretningsavtaler for denne linjen.

### <a name="issue-workaround"></a>Problemløsning

Denne virkemåten er forventet og er lik for både salgsordrer og bestillinger.

For å unngå dette kan du importere bestillingslinjene uten å angi prisinformasjon. Forretningsavtalene blir deretter brukt, og bestillingslinjene blir oppdatert basert på de definerte forretningsavtalene.

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>En leverandørrabatt blir ikke akkumulert basert på fakturaer.

### <a name="issue-description"></a>Problembeskrivelse

Hvis fakturaer som er postert, har forskjellige forfallsdatoer, blir ikke disse fakturaene gjenspeilet i leverandørrabatter som genereres fra dem.

### <a name="issue-resolution"></a>Problemløsning

Som standard tas ikke forfallsdatoen med når leverandørrabatten beregnes. Vurder å tilpasse systemet slik at forfallsdatoen og forbindelsen til fakturaen er mer synlig med hensyn til den faktiske leverandørrabatten.

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Enhetspriser på bestillinger beregnes ikke basert på enhetsomregningen.

### <a name="issue-description"></a>Problembeskrivelse

Når en enhet endres på en bestilling, beregnes ikke forretningsavtalepriser på nytt i henhold til enhetsomregningsdefinisjoner.

### <a name="issue-resolution"></a>Problemløsning

Prisene hentes alltid fra forretningsavtaler (eller andre prisinnstillinger i systemet, for eksempel salgsavtaler eller varepriser), og de angis for en enhet.

Hvis enheten endres på en ordrelinje, søker systemet etter en pris for den nye enheten og bruker denne prisen. Hvis det ikke finnes en pris for enheten, bruker ikke systemet en pris. Enhetskonverteringen kan ikke brukes til å omberegne prisen til en annen enhet. I teorien kan det hende at prisen for en boks på ti ikke er lik ti ganger prisen på en boks.

### <a name="issue-workaround"></a>Problemløsning

En måte å omgå dette problemet på, er å kontrollere at det finnes forretningsavtaler for de enhetene du forventer vil bli brukt på ordrelinjer for varen.

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a>Det oppstår problemer med valutaomregning med forretningsavtaler.

Forretningsavtale priser blir ikke omberegnet i henhold til valutaen når valutaen er forskjellig i en bestilling.

Med funksjonen *Generisk valuta* kan du definere priser og rabatter i bare én valuta. Du kan deretter konvertere til andre valutaer etter behov. Etter at konverteringen er utført, kan funksjonen også bruke smart avrunding automatisk.

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a>Når jeg åpner kjøpsavtalesiden i en linjevisningsmodus, kan jeg ikke tilpasse siden ved å legge til Prisenhet-feltet i oversikten over linjen.

Enkelte delte felt i avtalerammeverket kan ikke inkluderes i personlige tilpasninger. Denne begrensningen oppstår på grunn av datamodellen som er implementert. Derfor kan du ikke tilpasse **Prisenhet**-feltet.

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a>Maksimumsgrensen fra en kjøpsavtale er ikke gyldig på en innkjøpsrekvisisjon.

### <a name="issue-description"></a>Problembeskrivelse

Når en innkjøpsrekvisisjon er koblet til en kjøpsavtale, gjelder ikke maksimumsgrensen fra kjøpsavtalen i innkjøpsrekvisisjonen. Standard prisinformasjon angis på riktig måte, men mer enn maksimumsgrensen fra kjøpsavtalen kan bestilles i innkjøpsrekvisisjonen.

### <a name="issue-resolution"></a>Problemløsning

Denne virkemåten er forventet. Fordi rekvisisjoner ikke alltid er godkjent, skal det ikke reserveres et antall eller et beløp på kjøpsavtalen. Derfor oppfyller du ikke maksimumsgrensen fra kjøpsavtalen.

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a>Forretningsavtaler kan opprettes fra avviste tilbudsforespørsler. Derfor kan ikke systemet hindre at det opprettes forretningsavtalejournaler hvis tilbudsforespørselslinjen ikke er godtatt.

Du kan opprette forretningsavtaler for et hvilket som helst svar på en tilbudsforespørsel, uansett om de ble godtatt eller avvist. Hvis du vil ha mer informasjon, se [Oversikt over tilbudsforespørsler](request-quotations.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]