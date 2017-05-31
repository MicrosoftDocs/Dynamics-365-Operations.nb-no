---
title: "Leverandøravtaler for etterbetaling"
description: "Denne artikkelen beskriver PWP-betingelser som gjelder for leverandøravtaler. PWP-betingelser lar deg delvis eller fullstendig holde tilbake betaling til en leverandør til kunden i prosjektet betaler deg. Denne artikkelen inneholder også et reelt eksempel for å vise hvordan du kan bruke PWP-betingelser for et prosjekt."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectsListPage
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23131
ms.assetid: 20bf1d7f-8813-4c69-9cd7-576884a7e169
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7b21d4e93ec22715d530b75f75f3ba475e561f62
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="pay-when-paid-vendor-agreements"></a>Leverandøravtaler for etterbetaling

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver PWP-betingelser som gjelder for leverandøravtaler. PWP-betingelser lar deg delvis eller fullstendig holde tilbake betaling til en leverandør til kunden i prosjektet betaler deg. Denne artikkelen inneholder også et reelt eksempel for å vise hvordan du kan bruke PWP-betingelser for et prosjekt.

Når du godkjenner en leverandør som skal jobbet på et prosjekt som underleverandør, kan du holde tilbake betalingen til leverandøren eller underleverandøren til du er betalt av kunden for prosjektet. For å holde tilbake en betaling til en leverandør kan du definere etterbetalingsvilkår når du definerer bestillingen hos leverandøren. Når du oppretter en bestilling for leverandøren og tilordner en prosjekt-ID til bestillingen, er etterbetalingsvilkår i prosjektet knyttet til bestillingen og leverandøren. På siden **Leverandørfaktura med betal når betaling er mottatt** kan du vise en liste over ubetalte leverandørfakturaer for en bestilling og de tilknyttede kundefakturaene. Bruk dette skjemaet til å avgjøre om og hvor mye du vil betale en leverandør. Når en kunde for eksempel betaler et beløp på en prosjektfaktura, kan du frigi hele eller deler av de tilknyttede leverandørfakturaene for betaling. Du kan definere etterbetalingsvilkår for å angi at en leverandør er betalt etter at du mottar en bestemt prosentdel av den tilknyttede betalingen fra en kunde. Når du mottar delbetaling fra en kunde, kan du frigi noen av de relaterte leverandørfakturaene for betaling manuelt. Følgende eksempel viser hvordan du kan bruke etterbetalingsvilkår for å holde tilbake betaling til en leverandør eller underleverandør til kunden betaler deg. Organisasjonen din inngår en avtale med en kunde om å levere 100 datamaskiner der du installerer programvare som kunden ber om. Prisen som du og kunden blir enige om, er 150,00 for hver datamaskin. Du innhenter tjenester fra en tredjepartsleverandør om å levere datamaskinene til deg. Kunden ønsker å godkjenne kvaliteten på datamaskinene før organisasjonen din betales. Retningslinjene i organisasjonen din er å holde tilbake betalingen til en tredjepartsleverandør til du er betalt av kunden på et prosjekt. Derfor setter du opp prosjektet med en etterbetalingsprosent på 100 slik at du holder tilbake alle betalinger til leverandøren til hele kundefakturaen er betalt. Leverandøren krever 100,00 for hver datamaskin. Når leverandøren sender datamaskinene til deg, inneholder forsendelsen en faktura på 10 000,00 for 100 datamaskiner. Fordi du har satt opp prosjektet med etterbetalingsvilkår, betaler du ikke leverandøren. Når du mottar datamaskinene fra leverandøren, kan du installere den nødvendige programvaren på datamaskinene. Når du sender datamaskinene til kunden, sender du også kunden en faktura på 15 000,00. Kunden undersøker datamaskinene og godkjenner kvaliteten på produktet. Kunden betaler deretter organisasjonen hele beløpet på prosjektfakturaen. Når du har mottatt hele betalingen fra kunden, betaler du leverandøren hele beløpet på leverandørfakturaen, 10 000,00.




