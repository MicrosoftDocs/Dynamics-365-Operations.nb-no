---
title: Konfigurere produktfiltre for lagertransaksjoner
description: Denne artikkelen beskriver hvordan du konfigurerer produktfiltre og filterkoder for å kategorisere lagervarer i et lager. Du kan også bruke filtre til å angi hvilke kunder som kan bestille en bestemt vare, og hvilke varer som kan kjøpes fra en bestemt leverandør.
author: Mirzaab
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSFilters,WHSFilterGroupTable,EcoResProductDetailsExtended,WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 7d6524cb9109263ad62d221ec98e546b962b89ee
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067536"
---
# <a name="configure-product-filters-for-warehouse-transactions"></a>Konfigurere produktfiltre for lagertransaksjoner

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer produktfiltre og filterkoder for å kategorisere lagervarer i et lager. Du kan også bruke filtre til å angi hvilke kunder som kan bestille en bestemt vare, og hvilke varer som kan kjøpes fra en bestemt leverandør.

I tillegg kan du definere og bruke produktfiltre til automatisk å organisere lagervarer på et lager og kombinere filtrerte elementer i filtergrupper. Filtre kan brukes til å plassere varer i kategorier for håndterings-, innkjøps- og salgsprosesser. Du vil kanskje gruppere varer sammen eller skille dem fra hverandre når måten de håndteres på, er basert på vekt- eller håndteringsbegrensninger. Du kan også angi hvilke kunder eller leverandører en vare kan kjøpes fra eller selges til.

## <a name="prerequisites"></a>Forutsetninger

Tabellen nedenfor viser forutsetninger som må være på plass før du starter.

| Forutsetning | Instruksjoner |
|---|---|
| Før du begynner å konfigurere produkter på siden **Detaljer om frigitt produkt**, må du aktivere lagerbehandling for produktets lagringsdimensjonsgruppe. | Gå til **Behandling av produktinformasjon \> Oppsett \> Dimensjons- og variantgrupper \> Lagringsdimensjonsgrupper**, og velg eller opprett en lagringsdimensjonsgruppe der alternativet **Bruk lagerstyringsprosesser** er satt til *Ja*. |
| Hvis du skal bruke kundefiltre og/eller leverandørfiltre, må du aktivere bruken av dem i Lagerstyringsparametere. | Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**. I **Produktfiltre**-fanen setter du alternativet **Aktiver kundefiltre** og/eller **Aktiver leverandørfiltre** til *Ja*. |

## <a name="set-up-product-filters"></a>Konfigurere produktfiltre

Produktfiltre har opptil ti egenskaper for **Filtertittel**, som er opplistingsverdier (opplisting). Du kan velge disse opplistingsverdiene når du oppretter et produktfilter. Opplistingsverdiene *Kode 1* til og med *Kode 10* er systemdefinerte og representerer en bestemt egenskap eller et bestemt attributt for en vare. *Kode 1* kan for eksempel representere varer som er klassifisert som farlig materiale. *Kode 2* kan representere varer som bare leverandører kan kjøpe. Produktfiltre definerer deretter den bestemte **Filterkode**-verdien som er knyttet til en **Filtertittel**-verdi.

1. Gå til **Lagerstyring \> Oppsett \> Produktfiltre \> Produktfiltre**.
1. I handlingsruten velger du **Ny** for å legge til et produktfilter i rutenettet.
1. Velg en verdi i **Filtertittel**-feltet.
1. Angi en verdi i **Filterkode**-feltet.

    ![Definere et produktfilter.](media/Product_Filters10.png "Definere et produktfilter")

1. Skriv inn et navn for koden i feltet **Beskrivelse**. *Kode 2* kan for eksempel representere leverandører. Du kan deretter opprette et produktfilter for en bestemt leverandør eller leverandørgruppe. Hvis du vil ha mer informasjon, kan du se [Konfigurere leverandørfilterkoder](#vendor-product-filters) senere i denne artikkelen.

    ![Sett med produktfiltre.](media/Product_Filters.png "Sett med produktfiltre")

## <a name="set-up-product-filter-groups"></a>Konfigurere produktfiltergrupper

Du kan bruke filtergrupper til å gruppere filterkoder. Denne funksjonen er nyttig når en gruppe brukes i en spørring i et lokasjonsdirektiv og du vil søke etter gruppen i stedet for en serie med koder. Hver filtergruppe er knyttet til en varegruppe.

> [!IMPORTANT]
> Ikke alle produktfiltergrupper er tilgjengelige for filterkoder som er høyere enn *Kode 4* (det vil si *Kode 5* til og med *Kode 10*). Når det for eksempel gjelder frigitte produkter, blir ikke grupperingen av filterkoder oppdatert selv om alle produktfilterkodene legges til. Denne virkemåten kan bli oppdatert i senere versjoner.

Hvis du vil konfigurere filtergrupper, følger du denne fremgangsmåten.

1. Gå til **Lagerstyring \> Oppsett \> Produktfiltre \> Produktfiltergrupper**.
1. Velg **Ny** i handlingsruten.
1. I feltene **Gruppe 1** og **Gruppe 2** skriver du inn navnene som skal brukes til å kategorisere varer.
1. I hurtigfanen **Detaljer** velger du **Ny** for å legge til en linje.
1. I feltene **Startdato/-klokkeslett** og **Sluttdato/-klokkeslett** angir du start- og sluttdatoer for filtergruppen.
1. Velg varegruppen som produktfilteret skal gjelde for, i **Varegruppe**-feltet.
1. I feltene **Kode 1** til og med **Kode 10** velger du filterkodene som skal tas med i gruppen, etter behov.

    ![Varegruppe.](media/ProdFilterGroup.png "Varegruppe")

> [!NOTE]
> Hvis du får en feilmelding når du lukker siden, kan det hende at det mangler et kodeoppsett. På **Varegrupper**-siden kan du gjøre kodene obligatorisk for en varegruppe ved å merke av for **Tilordne filterkode 1 for varegruppe**, **Tilordne filterkode 2 for varegruppe** og så videre.

## <a name="set-up-filter-codes-on-item-groups"></a>Definere filterkoder for varegrupper

Når du definerer filterkoder i en varegruppe, kan du lage kodene som kreves for produkter som er knyttet til denne varegruppen.

Hvis du vil konfigurere filterkoder for varegrupper, følger du denne fremgangsmåten.

1. Gå til **Lagerstyring \> Oppsett \> Beholdning \> Varegrupper**.
1. I handlingsruten velger du **Ny** for å opprette en varegruppe.
1. Angi et navn i **Varegruppe**-feltet.
1. Angi en beskrivelse i **Navn**-feltet.
1. Under **Filter obligatorisk** i hurtigfanen **Lager** merker du av for filterkodene som må angis for produkter som er knyttet til varegruppen.

    Hvis du vil oppdatere et frigitt produkt, åpner du siden **Detaljer om frigitt produkt** og velger deretter **Rediger** i handlingsruten. Filtrene som er knyttet til koder, blir deretter tilgjengelige i hurtigfanen **Lager**.

    ![Varegrupper.](media/ItemGroup10.png "Varegrupper")

1. I delen **Varegruppefilter** merker du av for filtrene som må samsvare for at filtergruppen skal være standard filtergruppe for en vare.

    Hvis det for eksempel er merket av for **Bruk filterkode 1** og **Bruk filterkode 2**, må både filterkode 1 og 2 for varen samsvare med oppsettet av filtergruppen for varegruppen før filtergruppen kan velges. Når du oppretter en ny vare, blir den valgte filtergruppen standard filtergruppe i feltene **Gruppe 1** og **Gruppe 2** i hurtigfanen **Lager** på siden **Detaljer om frigitt produkt**.

> [!IMPORTANT]
> Produktfilterkoder aktiveres bare for varer som bruker Warehouse Management-prosesser (WMS).

## <a name="specify-filter-codes-for-released-products"></a>Angi filterkoder for frigitte produkter

Følg denne fremgangsmåten for å angi filterkoder for frigitte produkter. Du kan for eksempel bruke filterkoder til å gruppere farlige produkter som bestemte leverandører kjøper.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. I handlingsruten velger du **Ny** for å opprette et produkt.
1. Angi dataene som kreves for å opprette grunnlaget for et nytt produkt, i dialogboksen **Nytt utgitt produkt**, og velg deretter **OK**.

    Produktfilterkoder aktiveres ikke med mindre varegruppen som er knyttet til produktet, er konfigurert for filterkoder.

    Hvis du vil ha mer informasjon, kan du se [Opprette et nytt produkt](../pim/tasks/create-new-product.md).

1. Velg filterkoder for feltene **Kode 1** til og med **Kode 10** etter behov i delen **Produktfilterkoder** i hurtigfanen **Lager** for å angi filterkoder for produktet.

## <a name="set-up-generally-available-items"></a>Definere generelt tilgjengelige varer

Du kan gjøre bestemte lagervarer tilgjengelige bare for kunder, bare for leverandører eller for både kunder og leverandører.

> [!NOTE]
> Kunde- og leverandørfiltre gjelder ikke for varer som er definert som generelt tilgjengelige.

Hvis du vil konfigurere generelt tilgjengelige varer, følger du denne fremgangsmåten.

1. Gå til **Lagerstyring \> Oppsett \> Produktfiltre \> Generelt tilgjengelige produkter**.
1. I handlingsruten velger du **Ny** for å opprette en post.
1. I feltet **Kunde eller leverandør** velger du *Kunde*, *Leverandør* eller *Alle* for å gjøre varene tilgjengelige for kunder, leverandører eller begge.
1. Angi datoen og klokkeslettet for når varen skal bli tilgjengelig, i feltet **Startdato/-klokkeslett**.
1. Velg en varegruppe i **Varegruppe**-feltet.
1. I feltene **Kode 1** til og med **Kode 10** velger du filterkodene for å begrense varene som er generelt tilgjengelige.

    Når du velger en varegruppe, angir du denne gruppen varer som generelt tilgjengelig. Når du velger filterkoder i disse feltene, begrenser du varene som er tilgjengelige.

## <a name="set-up-customer-product-filters"></a>Definere produktfiltre for kunder

Du kan bruke denne valgfrie fremgangsmåten til å angi varer som skal være tilgjengelige for en kunde, i tillegg til varene som gjøres tilgjengelige via filteroppsettet på siden **Generelt tilgjengelige varer**. Du kan definere flere filtre for én kunde.

Hvis du vil konfigurere kundefilterkoder, følger du denne fremgangsmåten.

1. Gå til **Salg og markedsføring \> Kunder \> Alle kunder**.
1. Velg en kunde.
1. I gruppen **Oppsett** i fanen **Kunde** i handlingsruten velger du **Produktfiltre**.
1. På siden **Produktfilterkoder** i handlingsruten velger du **Ny**.
1. I feltene **Startdato/-klokkeslett** og **Sluttdato/-klokkeslett** angir du start- og sluttdatoer for den valgte varegruppen.
1. Velg en varegruppe i **Varegruppe**-feltet.
1. I feltene **Kode 1** til og med **Kode 10** velger du filterkodene som skal brukes som kriterier, for å begrense varene som er tilgjengelige for kunder i den valgte varegruppen. Du må gjøre et valg for hver filterkode som defineres for varegruppen.

## <a name="set-up-vendor-product-filters"></a><a name="vendor-product-filters"></a>Definere produktfiltre for leverandør

Du kan bruke denne valgfrie fremgangsmåten til å angi varer som skal være tilgjengelige for en leverandør, i tillegg til varene som gjøres tilgjengelige via filteroppsettet på siden **Generelt tilgjengelige varer**. Du kan definere flere filtre for én leverandør.

Hvis du vil konfigurere leverandørfilterkoder, følger du denne fremgangsmåten.

1. Gå til **Innkjøp og leverandører \> Leverandører \> Alle leverandører**.
1. Velg en leverandør.
1. I gruppen **Oppsett** i fanen **Leverandør** i handlingsruten velger du **Produktfiltre**.
1. På siden **Filterkoder** i handlingsruten velger du **Ny**.
1. I feltene **Startdato/-klokkeslett** og **Sluttdato/-klokkeslett** angir du start- og sluttdatoer for den valgte varegruppen.
1. Velg en varegruppe i **Varegruppe**-feltet.
1. I feltene **Kode 1** til og med **Kode 10** velger du filterkodene som skal brukes som kriterier, for å begrense varene som er tilgjengelige for leverandører i den valgte varegruppen. Du må gjøre et valg for hver filterkode som defineres for varegruppen.

> [!NOTE]
> Oppsettet for produktfiltre for leverandør gjelder for frigitte produkter der Warehouse Management-prosesser (WMS) er aktivert for den tilknyttede lagringsdimensjonsgruppen. Filterkodene brukes til å bestemme om systemet skal la brukere kjøpe en angitt vare fra en angitt leverandør når de oppretter bestillingslinjer. Microsoft Dynamics 365 Supply Chain Management har to metoder for å håndtere leverandørgodkjenning. Hvis det finnes ett eller flere frigitte produkter der feltet **Godkjent leverandørkontrollmetode** er satt til *Bare advarsel* eller *Ikke tillatt*, kan begge metodene for leverandørgodkjenning aktiveres for disse varene. Denne situasjonen kan forårsake problemer når brukere oppretter bestillingslinjer.

## <a name="see-also"></a>Se også

[Hvis du vil ha mer informasjon, kan du se blogginnlegget WMS – filterkoder for lager](http://blog.dynamics-for-operations.com/2017/09/26/wms-warehouse-filter-codes/)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]