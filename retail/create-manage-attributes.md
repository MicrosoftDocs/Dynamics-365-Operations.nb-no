---
title: Opprett og administrer attributter
description: Denne artikkelen beskriver attributter i Microsoft Dynamics 365 for Retail. Attributter lar deg beskrive et produkt og egenskapene ved hjelp av brukerdefinerte felt.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 4493c2f9e9e9dfe990f3b1670d3cd35e3bbaa38d
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017



---

# Opprett og administrer attributter
<a id="create-and-manage-attributes" class="xliff"></a>

[!include[banner](includes/banner.md)]


Denne artikkelen beskriver attributter i Microsoft Dynamics 365 for Retail. Attributter lar deg beskrive et produkt og egenskapene ved hjelp av brukerdefinerte felt.

Attributter lar deg beskrive et produkt og egenskapene ved hjelp av brukerdefinerte felt. Du kan for eksempel angir produktets minnestørrelse og harddiskkapasitet og angi om produktet er Energy star-kompatibel. Attributter kan knyttes til forskjellige detaljhandelsenheter, for eksempel produktkategorier og kanaler for detaljhandel, og du kan angi standardverdier for dem.. Produkter arver sine attributter og standardverdier for disse attributtene når de er knyttet til produktkategorier eller kanaler for detaljhandel. Standardverdiene kan overstyres på nivået for det individuelle produktet, på nivået for kanal for detaljhandel, eller i en detaljhandelskatalog.

#### Eksempler
<a id="examples" class="xliff"></a>

| Kategori   | Attributt                | Tillatte verdier          | Standardverdi |
|------------|--------------------------|-----------------------------|---------------|
| TV og video | Merke                    | En gyldig Merke-verdi       | Ingen          |
| TV         | Skjermstørrelse              | 20″–80″                     | Ingen          |
| TV         | Loddrett oppløsning      | 480i, 720p, 1080i eller 1080p | 1080p         |
| TV         | Oppdateringsfrekvens for skjerm      | 60 Hz, 120 Hz eller 240 Hz       | 60 Hz          |
| TV         | HDMI-innganger              | 0–10                        | 3             |
| TV         | DVI-innganger               | 0–10                        | 1             |
| TV         | Komposittinnganger         | 0–10                        | 2             |
| TV         | Komponentinnganger         | 0–10                        | 1             |
| LCD-SKJERM        | 3D Ready                 | Ja eller No                   | Ja           |
| LCD-SKJERM        | 3D Enabled               | Ja eller No                   | Ingen            |
| Plasma     | Driftstemperatur fra      | 0–43 grader              | 32            |
| Plasma     | Driftstemperatur til        | 0–43 grader              | 100           |
| Projektor | Garanti for projiseringsrør | 6, 12 eller 18 måneder         | 12            |
| Projektor | Antall projiseringsrør    | 1–5                         | 3             |


## Attributtype
<a id="attribute-type" class="xliff"></a>
  [![attributter-fast-kopi](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) 
  
Attributter er basert på attributtyper. Attributtyper identifiserer datatypen som kan angis for et bestemt attributt. For øyeblikket støtter Microsoft Dynamics 365 for Retail følgende attributtyper:

-   **Valutaen** – Denne attributtypen støtter valutaverdier. Den kan være bundet (det vil si den kan støtte et verdiområde), eller den være tom.
-   **Dato og klokkeslett** – Denne attributtypen støtter dato- og klokkeslettverdier. Den kan være bundet (det vil si den kan støtte et verdiområde), eller den være tom.
-   **Desimal** – Denne attributtypen støtter numeriske verdier som inneholder desimaler. Den støtter også måleenheter. Den kan være bundet (det vil si den kan støtte et verdiområde), eller den være tom.
-   **Heltall** – Denne attributtypen støtter numeriske verdier. Den støtter også måleenheter. Den kan være bundet (det vil si den kan støtte et verdiområde), eller den være tom.
-   **Tekst** – Denne attributtypen støtter tekstverdier. Den støtter også et forhåndsdefinert sett med verdier (opplisting).
-   **Boolsk** – Denne attributtypen støtter binære verdier (**sann**/**usann**).
-   **Referanse**

## Attributt
<a id="attribute" class="xliff"></a>
  [![createandmanageattribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) I tillegg til navn, egendefinert navn, beskrivelse og hjelpetekst, kan én eller flere av følgende typer informasjon registreres for et attributt:

-   Standardverdi
-   Attributtmetadata, for eksempel metadata som indikerer om attributtet kan søkes i, finjusteres eller sorteres

## Attributtgruppe
<a id="attribute-group" class="xliff"></a>
  [![createandmanageattribute-10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) Når attributter er definerte, kan de grupperes i attributtgrupper. Attributtgrupper gir grupperinger av individuelle attributter, og kan tilordnes til detaljhandelskategorier eller kanaler for detaljhandel.

## Tilordne attributtgrupper til detaljhandelskategorier
<a id="assigning-attribute-groups-to-retail-categories" class="xliff"></a>
  [![createandmanageattribute-12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) Én eller flere attributtgrupper kan knyttes til kategorinoder i kategorihierarkiet for detaljhandelsprodukt. Når varer er kategorisert, arver de attributtene som er inkludert i attributtgruppene.

## Tilordne attributtgrupper til detaljhandelsbutikker
<a id="assigning-attribute-groups-to-retail-stores" class="xliff"></a>
  [![createandmanageattribute-13-1024x576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) Én eller flere attributtgrupper kan knyttes til én eller flere detaljhandelsbutikker i hierarkiet for detaljhandelsbutikker. Når varer er supplert for spesifikke detaljhandelsbutikker, arver de attributtene som er inkludert i attributtgruppene.

## Overstyre attributtverdier
<a id="overriding-attribute-values" class="xliff"></a>
### På produktnivå
<a id="at-the-product-level" class="xliff"></a>

  [![createandmanageattribute-14-1024x576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) Standardverdiene for attributter kan overstyres på produktnivå (det vil si for enkeltprodukter).

### I detaljhandelskatalog
<a id="in-a-retail-catalog" class="xliff"></a>

  [![createandmanageattribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) Standardverdiene for attributter kan overstyres for individuelle produkter i bestemte kataloger som er rettet mot bestemte kanaler for detaljhandel.

### På nivå for kanal for detaljhandel
<a id="at-the-retail-channel-level" class="xliff"></a>

  [![createandmanageattribute-1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) Standardverdiene for attributter kan overstyres for individuelle produkter i bestemte kataloger som er rettet mot bestemte kanaler for detaljhandel.




