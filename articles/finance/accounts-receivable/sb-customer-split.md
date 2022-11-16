---
title: Kundedeling på faktureringsplaner
description: Denne artikkelen beskriver hvordan du deler en kunde når abonnementsfakturering brukes.
author: JodiChristiansen
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-11-05
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: cfbe61ca4b7e809a8183f4622bf6db4fc83a4d83
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746318"
---
# <a name="customer-split-on-billing-schedules"></a>Kundedeling på faktureringsplaner

*Fakturakontoen* i en faktureringsplan er kunden som mottar salgsordrefakturaen, slik at de kan betale regningen. I noen scenarioer kan flere enn én kunde betale en faktura. Funksjonaliteten **Kundedeling** lar deg legge til flere kunder som kan faktureres for samme faktureringsplan. Du kan aktivere denne funksjonaliteten ved å gå til **Abonnementsfakturering \> Regelmessig kontraktfakturering \> Oppsett \> Faktureringsparametere for regelmessig kontrakt** og angi **Ja** for alternativet **Kundedeling**.

## <a name="customer-split-on-the-billing-schedule-header"></a>Kundedeling i faktureringsplanhodet

Etter at en faktureringsplan er opprettet, kan ytterligere kunder legges til i faktureringsplanhodet.

Følg denne fremgangsmåten for å legge til en kunde.

1. I fanen **Faktureringsplan** velger du **Kundedeling**. Feltene **Kundekonto** og **Kundekontonavn** øverst angir kunden som er tilordnet som **Faktureringsplankunde**.

    > [!NOTE]
    > Kundekontoen du legger til, kan ikke være den samme som fakturakontoen.

2. I fanen **Kundedelingslinjer** velger du **Legg til linje**.
3. Velg en kunde, og angi deretter prosenten av hver faktura for denne kunden.
4. Start- og sluttdatoene for faktureringsplanen brukes som standard som start- og sluttdatoene. Angi ulike start- og sluttdatoer hvis den nye kunden skal betale den angitte prosenten bare for en del av faktureringsplanen. Hvis faktureringsplanen for eksempel har startdatoen 1. januar og sluttdatoen 31. desember, og den nye kunden faktureres 40 prosent for de første ni månedene, angir du 1. januar som startdato, 30. september som sluttdato og **40,00** som prosenten.

Du kan legge til flere enn én kunde på kundedelingslinjene. Prosenten totalt som angis, kan i dette tilfellet ikke overskride 100 prosent. Angi en kundereferanse og kunderekvisisjon som informasjonsfelter som skal vises på salgsordrelinjen under prosessen **Generer faktura**.

Linjedetaljene viser kontaktinformasjon, leveringsadresse, fakturaadresse og betalingsdetaljer for de tilføyde kundene. Denne informasjonen vises også på salgsordren for kundene.

Når du legger til kundedelingsinformasjon i faktureringsplanhodet, får du følgende melding hvis det finnes ufakturerte faktureringsplanlinjer i faktureringsplanen: «Vil du rulle ned endringen fra hodet til linjene? Endringer oppdaterer bare faktureringsplanlinjene som ikke er fakturert.» Velg **Ja** for å oppdatere kundedelingsinformasjonen på fakturaplanlinjen. Endringer blir ikke oppdatert hvis faktureringsplanlinjen allerede er fakturert.

Hvis en faktureringsplan opprettes ved hjelp av alternativet **Kopier tidsplan**, angis standardinformasjonen på linjene i kundedelingshodet. Den kan ikke den samme som kundekontoen.

Når prosessen **Generer faktura** er fullført, vil det bli opprettet flere salgsordrer. (Flere salgsfakturaer blir også opprettet hvis automatisk postering brukes.) Disse salgsordrene og salgsfakturaene kan vises i fanen **Faktura** i hurtigfanen **Linjedetaljer** på siden **Vis faktureringsdetaljer**. **Flere** vises på faktureringsdetaljlinjen for å angi at det er opprettet flere salgsordrer og salgsfakturaer.

## <a name="customer-split-on-billing-schedule-lines"></a>Kundedeling på faktureringsplanlinjer

Kundedelingen kan legges til på individuelle faktureringsplanlinjer hvis du bare vil dele bestemte faktureringsplanlinjer. Merk av for **Kundedeling** på linjen, og velg deretter **Kundedeling** på menyen for faktureringsplanlinjen for å oppdatere eller angi kundedelingsinformasjon.

Revisjonsinformasjonen blir oppdatert hvis faktureringsplanen allerede er fakturert, men så ble prosenten endret på faktureringsplanlinjen. Alle linjer som faktureres etter denne endringen, bruker den nye prosenten.

> [!NOTE]
> - Alternativet for kundedeling kan ikke brukes med lagerførte produkter.
> - Hvis det er merket av for **Ufakturert inntekt**, kan du ikke merke av for **Kundedeling**.
> - Hvis du bruker alternativet **Bare inntektsdeling**, har den overordnede linjen alternativet **Kundedeling**, men ikke de underordnede linjeelementene.
