---
title: Frigi produksjonsordrer
description: En frigitt produksjonsordre er en ordre som har blitt autorisert for produksjon. Begrepet frigitt brukes til å beskrive en tilstand i livssyklusen til produksjonsordren, der produksjonsordren er tilgjengelig for utføring på produksjonsgulvet og for lagerprosesser.
author: johanhoffmann
manager: tfehr
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ee20983209b9900037a46d56b6213d47bf852e4
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487705"
---
# <a name="release-production-orders"></a>Frigi produksjonsordrer

[!include [banner](../includes/banner.md)]

En frigitt produksjonsordre er en ordre som har blitt autorisert for produksjon. Begrepet frigitt brukes til å beskrive en tilstand i livssyklusen til produksjonsordren, der produksjonsordren er tilgjengelig for utføring på produksjonsgulvet og for lagerprosesser.

## <a name="characteristics-of-the-released-state"></a>Egenskapene for tilstanden Frigitt

**Frigitt** er én tilstand i livssyklusen til produksjonsordren. Produksjonsordrer som har tilstanden **Frigitt**, er tilgjengelige for kjøring i produksjons- og lagerprosesser. **Frigitt**-tilstanden har følgende egenskaper:

- En produksjonsordre kan endres til tilstanden **Frigitt** fra produksjonsordren eller ved hjelp av en partiprosess. Produksjonsordren kan også oppdateres automatisk fra planlagte produksjonsordrer som er autorisert ved hjelp av feltet **Autorisasjonshorisont** på **Hovedplan**-siden.
- Tilstanden **Frigitt** er tegnet for shop floor-operatørene på at de kan starte kjøring av produksjonsjobber i shop floor.
- Produksjonspapirer, for eksempel rutekort, rutejobber og jobbkort, gir informasjon om produksjonsjobbene og kan utstedes.
- For materialer som er fysisk reservert, genereres lagerarbeid for å plukke materialer til produksjonsordren.

## <a name="releasing-jobs-to-the-shop-floor"></a>Frigi jobber til shop floor

Når en produksjonsordre er frigitt, blir produksjonsjobber som er knyttet til ordren, synlige og klar for registrering. Operatørene kan utføre jobbregistreringer, for eksempel Start, Stopp og Fullføring, på siden **Jobbkortterminal** eller **Jobbkortenhet**. Registrert tid og antall overføres automatisk fra registreringsidene til produksjonsjournaler for å holde oversikt over forbruk av tid og antall.

## <a name="route-cards"></a>Rutekort

Et rutekort gir en oversikt over informasjon som kommer fra rute- og operasjonsoppsett og fra operasjons- og jobbplanleggingsmetoder.

## <a name="route-jobs"></a>Jobber for ruten

En rutejobb gir detaljert informasjon om hver jobb i en operasjon, og inkluderer tider for oppsett, prosess, kø og transport. En maleoperasjon krever for eksempel individuelle jobber som oppsettstid, kjøretid for maleprosessen og køtid for tørking.

## <a name="job-cards"></a>Jobbkort

Et jobbkort viser de individuelle jobbnumrene til en bestemt operasjon. Én jobb vises på hver side. Jobbene på et jobbkort, og estimert tid, kommer fra informasjonen om ruten og operasjonsoppsettet. Du kan åpne siden **Produksjonsjournallinjer**, **jobbkort** fra et jobbkort. De som driver operasjonsressurser, kan gi tilbakemelding om produksjonsprosessen. Det er felt der du kan angi forbruksstatistikk og informasjon som antall feil.

## <a name="warehouse-work-for-raw-material-picking"></a>Lagerarbeid for råvareplukking

Arbeid for råvareplukking genereres under frigivelsen. Arbeid genereres bare for materialmengden som er fysisk reservert for produksjonsordren før ordren ble frigitt. Følgende oppsett er nødvendig for å generere lagerarbeid for plukking av råvarer:

- Et lokasjonsdirektiv for råvareplukking som bestemmer lagerlokasjonen materialene skal plukkes fra
- En bølgemal for råmaterialer, der policyer konfigureres for utførelse av lagerarbeid
- Et produksjonsinnleveringssted som bestemmer hvor materialene plasseres

Ved bruk av nummerskiltkontrollerte lokasjoner kan du velge om det bestilte antallet eller hele antallet som er tilgjengelig for varen, skal plukkes under behandling av råvareplukkingsarbeidet. Slik konfigurerer du dette alternativet:

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter** og åpne den relevante varen.
1. Vis hurtigfanen **Lager**.
1. Velg ett av følgende alternativer for feltet **Materialplukking på nummerskiltplasseringer**:
    - *Ordreplukking*: Bare det bestilte antallet skal plukkes.
    - *Oppsamling*: Når det er mulig skal hele antallet som er tilgjengelig for nummerskiltet, plukkes. Hvis en arbeider skal kunne plukke hele nummerskiltantallet, må nummerskiltet inneholde et blandet utvalg varer og må ikke ha kombinerte dimensjoner. Hvis nummerskiltet inneholder kombinerte dimensjoner eller varer, fortsetter plukkingen som om den var satt til *Ordreplukking*.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]