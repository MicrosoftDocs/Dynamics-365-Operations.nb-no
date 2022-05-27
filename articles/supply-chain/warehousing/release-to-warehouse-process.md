---
title: Frigi til lager
description: Dette emnet inneholder detaljer om frigivelse til lagerprosessen. Den beskriver enheter som opprettes når du frigir en ordre til lageret, og alternativer du kan bruke til å starte prosessen.
author: Mirzaab
ms.date: 8/13/2021
ms.topic: article
ms.search.form: WHSReleaseToWarehouse, WHSReleaseToWarehouseSalesOrder, WHSReleaseToWarehouseTransferOrder, WHSLoadPlanningWorkbench, WHSWaveTemplateTable, WHSWorkTemplateTable, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8624db42e9d0f3d08ed3b582224ed7937d52f85d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678358"
---
# <a name="release-to-warehouse"></a>Frigi til lager

[!include [banner](../../includes/banner.md)]

Dette emnet inneholder detaljer om frigivelse til lagerprosessen. Den beskriver enheter som opprettes når du frigir en ordre til lageret, og alternativer du kan bruke til å starte prosessen.

## <a name="release-to-warehouse-overview"></a>Oversikt over Frigi til lager

Frigivelse til lager er prosessen med å gjøre lageret klart til fordelingsbehandling. Når du frigir en ordre til lageret, oppretter systemet belastningslinjer og forsendelser. Hvis automatisk bølgebehandling er konfigurert, blir det også opprettet belastning og nødvendig arbeid. Konfigurasjonen til enhetene som er involvert, avhenger av systeminnstillingene. Denne delen av emnet ser gjennom enhetene som er opprettet i løpet av frigivelsen til lagerprosessen, og systeminnstillingene som definerer dem.

En *forsendelse* er en gruppe av salgsordre- eller overføringsordrelinjer for den samme kunden eller den samme leveringsadressen.

En *belastning* er en gruppe salgsordre- eller overføringsordrelinjer som grupperes sammen, og som vanligvis går ut på én enkelt lastebil, togvogn eller en annen transportmåte. En belastning kan ha én eller flere forsendelser. Du kan opprette en belastning manuelt ved å legge til ordrelinjer i en ny belastning. I dette tilfellet tilordnes ordrelinjer til belastningen før frigivelse til lagerprosessen startes, og de kan bare frigis fra siden **Arbeidsområde for lastplanlegging**.

Lager *arbeid* er en hvilken som helst lageroperasjon som utføres av en lagerarbeider. Vanligvis består lageroperasjoner av minst to etterfølgende handlinger: en lagerarbeider plukker opp beholdning på en lokasjon og plasserer den på en annen lokasjon.

Når ordrer frigis til lageret, oppretter systemet *belastningslinjer* og grupperer dem i forsendelser. Forsendelseskonsolideringsprosessen tillater automatisert forsendelseskonsolidering i løpet av frigivelsen til lagerprosessen. Hvis du vil ha mer informasjon, se [Policyer for forsendelseskonsolidering](about-shipment-consolidation-policies.md).

Systemet bruker *bølger* til å opprette plukking av arbeid og belastninger for forsendelse. En *bølgemal* må være tilgjengelig for bølgetypen du vil opprette, og for lageret for ordrelinjen. Bølgemaler av *Forsendelse*-typen brukes for forsendelse av varer for salgsordrer og overføringsordrer.

Hver bølgemal inneholder *bølgemetoder*. Bølgemetoder utfører handlinger, for eksempel å opprette arbeid for bølgen eller opprette belastninger. Bølgenmalen for forsendelsesbølger kan for eksempel inneholde metoder for å opprette laster, tildele linjer til bølger, etterfylle, og opprette plukkarbeid for bølgen. Bølgemalen fastsetter innstillinger som definerer hvordan bølgen skal genereres og behandles, hvilke trinn som må gjøres manuelt, og hvilke som gjøres automatisk. Hvis du vil ha mer informasjon, kan du se [Bølgemaler](wave-templates.md). Avhengig av konfigurasjonen til bølgemalen, opprettes, behandles og frigis derfor enten en bølge automatisk når du frigir en ordre til lager, eller noen eller alle disse handlingene utføres manuelt etter at frigivelsen til lager er utført.

Når en bølge behandles, oppretter systemet plukkarbeid basert på en passende *arbeidsmal* og *lokasjonsdirektiv*, og gjør arbeidet tilgjengelig på mobilenheter. Arbeidsmalen avgjør hvordan arbeidet utføres for hver lagerprosess, og lokasjonsdirektivet angir plukke- og plasseringslokasjoner for lagerbevegelser. Hvis du vil ha mer informasjon, kan du se [Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver](control-warehouse-location-directives.md).

> [!NOTE]
> Som standard behandles bølger i satsvis modus.

Under bølgebehandling oppretter systemet vanligvis en ny last for hver forsendelse som det ikke er tildelt en last til. Hvis du vil at systemet skal tilordne forsendelser som ikke er tilordnet, til eksisterende belastninger i stedet, kan du bruke funksjonaliteten for avansert bølgebelastningsbygging. Hvis du vil ha mer informasjon, kan du se [Avansert lastplanlegging under bølge](advanced-load-building-during-wave.md).

På sidene **Salgsordrer** og **Overføringsordrer** kan du se gjennom enhetene som er opprettet for ordrelinjer i løpet av frigivelsen til lagerprosessen.

- **Salgsordrer**-siden:

    - I hurtigfanen **Salgsordrelinjer** velger du **Lager**, og deretter velger du **Forsendelsesdetaljer** på menyen for å åpne relaterte forsendelser, **Lastdetaljer** for å åpne relaterte belastninger, eller **Arbeidsdetaljer** for å åpne relaterte arbeidsdetaljer.
    - I hurtigfanen **Linjedetaljer** velger du kategorien **Belastning** for å gå gjennom tilknyttede belastninger.

- **Overføringsordrer**-siden:

    - I handlingsruten i **Send**-fanen velger du **Forsendelsesdetaljer** for å åpne relaterte forsendelser, eller **Lastdetaljer** for å åpne relaterte belastninger.
    - I hurtigfanen **Overføringsordrelinjer** velger du **Arbeidsdetaljer** for å åpne relaterte arbeidsdetaljer.

Når en ordre frigis til lageret, fungerer den mest automatiserte flyten på følgende måte:

1. Systemet oppretter en forsendelse for ordren og en bølge.
1. Bølgen behandles.
1. Det opprettes en belastning og en arbeids-ID.

Noen trinn i denne flyten kan bli manuelle, avhengig av innstillinger for bølgemaler, arbeidsmaler og lokasjonsdirektiver. Den helhetlige flyten forblir imidlertid den samme.

Du har flere alternativer for hvordan du frigir en ordre til lageret. Du kan utføre operasjonen manuelt, eller du kan definere en satsvis jobb. Resten av dette emnet gjennomgår detaljert de forskjellige måtene du kan utføre en frigivelse til lageroperasjon på.

## <a name="manual-release-to-the-warehouse-from-the-sales-orders-and-transfer-orders-pages"></a>Manuell frigivelse til lageret fra sidene Salgsordrer og Overføringsordrer

Du kan frigi en ordre til lageret direkte fra **Salgsordrer**-siden eller **Overføringsordrer**-siden ved å velge **Frigi til lager**.

- På **Salgsordrer**-siden finner du knappen i kategorien **Lager** i handlingsruten.
- På **Overføringsordrer**-siden finner du knappen i kategorien **Send** i handlingsruten.

Fra **Salgsordrer**-siden kan du frigi flere salgsordrer samtidig.

## <a name="manual-release-to-the-warehouse-from-the-release-to-warehouse-pages"></a>Manuell frigivelse til lageret fra Frigivelse til lager-sidene

Systemet tilbyr i øyeblikket tre sider der du kan gå gjennom linjer for flere ordrer og frigi dem til lageret:

- **Frigi til lager** (**Lagerstyring \> Frigi til lager \> Frigi til lager**) – På denne siden kan du arbeide med både salgsordrer og overføringsordrer. Det gir imidlertid lavere ytelse enn de to andre sidene. Denne siden blir snart fraskrevet.
- **Frigi salgsordrer til lager** (**Lagerstyring \> Frigi salgsordrer til lager \> Frigi salgsordrer til lager**) – På denne siden kan du bare arbeide med salgsordrer. Den gir imidlertid bedre ytelse enn siden **Frigi til lager**.
- **Frigi overføringsordrer til lager** (**Lagerstyring \> Frigi salgsordrer til lager \> Frigi overføringsordrer til lager**) – På denne siden kan du bare arbeide med overføringsordrer. Den gir imidlertid bedre ytelse enn siden **Frigi til lager**.

Alle tre sidene inneholder lignende funksjonalitet, som beskrevet i resten av denne delen. Alle lar deg velge ordrelinjer eller hele ordrer og deretter frigi dem til lageret.

Hver av sidene består av en øvre del, der du kan velge ordrelinjer, og en nedre del, der du kan starte frigivelsen til lagerprosessen. Du kan bruke filtre i den øvre delen til å søke etter salgsordrelinjene du vil frigi. Siden **Frigi til lager** gir en egen kategori for salgsordrer og overføringsordrer i den øvre delen, mens hver av de andre to sidene viser bare én type ordre.

Verktøylinjen i den øvre delen inneholder følgende knapper som du kan bruke til å velge ordrelinjer som skal frigis til lageret:

- **Legg til** – Velg én eller flere ordrelinjer i den øvre delen, og velg deretter denne knappen for disse linjene i den nedre delen.
- **Legg til alle** – Legg til alle linjer fra den øvre delen i den nedre delen.
- **Legg til ordre** – Velg en ordre, og velg deretter denne knappen for å legge til alle linjer fra ordren i den nedre delen.

Når du er ferdig med å legge til linjer i den nedre delen, merker du hver linje du vil frigi. Velg deretter **Frigi til lager** på verktøylinjen for å frigi disse linjene til lageret.

## <a name="manual-release-to-the-warehouse-from-the-load-planning-workbench-page"></a>Manuell frigielse til lageret fra siden Arbeidsområde for lastplanlegging

Du kan også frigi ordrer manuelt til lageret ved hjelp av siden **Arbeidsområde for lastplanlegging**. På denne siden kan du organisere ordrelinjer i belastninger og deretter frigi disse belastningene til lageret.

For å åpne siden **Arbeidsområde for lastplanlegging** går du til **Lagerstyring \> Laster**. Du kan også åpne den fra sidene **Salgsordrer** og **Overføringsordrer**. I den øvre delen av siden kan du velge salgsordrelinjer i kategorien **Salgslinjer** og overføre ordrelinjer i kategorien **Overføringslinjer**, og deretter legge til disse linjene i en ny eller eksisterende belastning.

Kategorien **Forsyning og behov** i handlingsruten inneholder følgende knapper som du kan bruke til å legge til ordrelinjer i den øvre delen av en belastning:

- **Til ny last** – Velg ordrelinjene i den øvre delen, og velg deretter denne knappen for å opprette en ny last og legge til disse linjene i den nedre delen.
- **Til eksisterende last** – Velg ordrelinjene i den øvre delen, og velg deretter denne knappen for å legge til disse linjene i en eksisterende last.
- **Hele ordren i ny last** – Velg ordrer, og velg deretter denne knappen for å opprette en ny last og legge til alle linjene fra disse ordrene i den.
- **Hele ordren i eksisterende last** – Velg en ordre, og velg deretter denne knappen for å legge til alle linjer fra ordren i en eksisterende last.

I den nedre delen kan du se gjennom belastningene som er opprettet. For å frigi laster til lageret velger du dem og velger deretter **Frigi \> Frigi til lager** på verktøylinjen. Hvis du bruker automatisk bølgebehandling, oppretter systemet forsendelser og arbeids-IDer når frigivelsen til lageroperasjonen utføres, fordi belastninger allerede er tilordnet ordrelinjene.

## <a name="automatic-release-to-the-warehouse"></a>Automatisk frigivelse til lageret

Hvis du vil frigi ordrer automatisk til lageret, bruker du **Automatisk frigivelse av salgsordrer** og **Automatisk frigivelse av overføringsordrejobber**.

Hvis du vil konfigurere den satsvise jobben som frigir salgsordrene, gjør du følgende.

1. Gå til **Lagerstyring \> Frigi til lager \> Automatisk frigivelse av salgsordrer**.
1. I dialogboksen **Automatisk frigivelse av salgsordrer** angir du følgende felt i hurtigfanen **Parametere**:

    - **Antall som skal frigis** – Velg om hele mengden eller bare den fysisk reserverte mengden skal frigis til lageret.
    - **Tillate frigivelse av delvis frigitte ordrer** – Angi om gjenværende antall for delvis frigitte ordrer skal frigis til lageret.
    - **Behold reserveringer ved frigivelsesfeil**– Angi om antall som ble reservert automatisk for en salgsordre, skal reserveres automatisk hvis frigivelsen til lagerprosessen mislykkes.
    - **Gruppefrigivelser etter kunde** – Angi om systemet skal behandle frigivelse til lageroperasjoner separat for hver kunde, eller om det skal frigi alle salgsordrer samtidig. Når *Ja* er angitt for dette alternativet, vil systemet samle inn alle salgsordrelinjene for en valgt kunde, frigi disse ordrene til lageret og deretter behandle den neste kunden. Når *Nei* er angitt for dette alternativet, vil systemet frigi alle tilgjengelige salgsordrelinjer i en enkelt frigivelse til lageroperasjon. Når du aktiverer dette alternativet, kan du bidra til å øke ytelsen og fleksibiliteten ved frigivelsen til lagerprosessen. Du må imidlertid være forsiktig når du bruker dette alternativet sammen med bølgemaler som er konfigurert slik at de behandler bølger ved frigivelse til lager, fordi denne kombinasjonen kan generere mange bølger for enkeltkunde, der hver bølge har arbeid som er generert bare for denne kunden. Hvis du vil generere arbeid som kombinerer forsendelser for flere kunder, bør du enten deaktivere alternativet *Gruppefrigivelser etter kunde* eller konfigurere bølgemalene slik at de bruker utsatt behandling.
    - **Håndtering av låst ordre** – Velg hvordan systemet skal håndtere salgsordrer som er låst, fordi de redigeres av andre brukere eller prosesser:

        - *Vente til ordrer låses opp* – Systemet må vente på at ordrene blir låst opp før de frigis til lageret. I så fall kan frigivelsen til lagerprosessen ta mer tid.
        - *Hopp over låste ordrer* – Systemet skal hoppe over låste ordrer.

    - **Gyldige ordretyper** – Velg salgsordretypene som skal tas med i partiet.
    - **Kredittgrensetype** – Velg om det skal utføres kredittgrensekontroller i løpet av frigivelsen til lagerprosessen, og, hvis kontrollene skal utføres, transaksjonsinformasjonen som skal tas med i dem.

1. Hvis du vil bestemme hvilke ordrer som skal behandles, velger du **Filter** i hurtigfanen **Poster som skal inkluderes**. Det vises en standard dialogboks for spørring der du kan definere utvalgskriterier, sorteringskriterier og koblinger. Feltene fungerer på samme måte som for andre typer spørringer i Microsoft Dynamics 365 Supply Chain Management.
1. I hurtigfanen **Kjør i bakgrunnen** velger du om jobben slik skal kjøres i satsvis modus, og/eller angir en gjentakende tidsplan. Feltene fungerer på samme måte som de fungerer for andre typer [bakgrunnsjobber](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Velg **OK** for å bruke innstillingene og starte prosessen med å frigi til lager.

Hvis du vil konfigurere den satsvise jobben som frigir overføringsordrene, gjør du følgende.

1. Gå til **Lagerstyring \> Frigi til lager \> Automatisk frigivelse av overføringsordrer**.
1. I dialogboksen **Automatisk frigivelse av overføringsordrer** angir du følgende felt i hurtigfanen **Parametere**:

    - **Antall som skal frigis** – Velg om hele mengden eller bare den fysisk reserverte mengden skal frigis til lageret.
    - **Tillate frigivelse av delvis frigitte ordrer** – Angi om gjenværende antall for delvis frigitte ordrer skal frigis til lageret.
    - **Gruppefrigivelser etter mållager**– Angi om systemet skal frigi alle overføringsordrer samtidig, eller om det skal gruppere overføringsordrelinjer etter mållager og deretter frigi hver gruppe til lageret separat.

1. Hvis du vil bestemme hvilke ordrer som skal behandles, velger du **Filter** i hurtigfanen **Poster som skal inkluderes**. Det vises en standard dialogboks for spørring der du kan definere utvalgskriterier, sorteringskriterier og koblinger. Feltene fungerer på samme måte som for andre typer spørringer i Supply Chain Management.
1. I hurtigfanen **Kjør i bakgrunnen** velger du om jobben slik skal kjøres i satsvis modus, og/eller angir en gjentakende tidsplan. Feltene fungerer på samme måte som de fungerer for andre typer [bakgrunnsjobber](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Velg **OK** for å bruke innstillingene og starte prosessen med å frigi til lager.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
