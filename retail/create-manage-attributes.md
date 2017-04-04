---
title: Opprett og administrer attributter
description: Denne artikkelen beskriver attributtene i Microsoft Dynamics 365 for operasjoner. Attributter lar deg beskrive et produkt og egenskapene ved hjelp av brukerdefinerte felt.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 26c628e10aaa5f47bc87d7510ca8f41ab3630204
ms.lasthandoff: 03/31/2017


---

# <a name="create-and-manage-attributes"></a>Opprett og administrer attributter

Denne artikkelen beskriver attributtene i Microsoft Dynamics 365 for operasjoner. Attributter lar deg beskrive et produkt og egenskapene ved hjelp av brukerdefinerte felt.

Attributter lar deg beskrive et produkt og egenskapene ved hjelp av brukerdefinerte felt. Du kan for eksempel angir produktets minnestørrelse og harddiskkapasitet og angi om produktet er Energy star-kompatibel. Attributter kan knyttes til forskjellige detaljhandelsenheter, for eksempel produktkategorier og kanaler for detaljhandel, og du kan angi standardverdier for dem.. Produkter arver sine attributter og standardverdier for disse attributtene når de er knyttet til produktkategorier eller kanaler for detaljhandel. Standardverdiene kan overstyres på nivået for det individuelle produktet, på nivået for kanal for detaljhandel, eller i en detaljhandelskatalog.

#### <a name="examples"></a>Eksempler

Kategori

Attributt

Tillatte verdier

Standardverdi

TV og video

Merke

En gyldig **Merke**-verdi

Ingen

TV

Skjermstørrelse

**20"**–**80"**

Ingen

Loddrett oppløsning

**480i**, **720p**, **1080i** eller **1080p**

**1080p**

Oppdateringsfrekvens for skjerm

**60 Hz**, **120 Hz** eller **240 Hz**

**60 Hz**

HDMI-innganger

**0**–**10**

**3**

DVI-innganger

**0**–**10**

**1**

Komposittinnganger

**0**–**10**

**2**

Komponentinnganger

**0**–**10**

**1**

LCD-SKJERM

3D Ready

**Ja** eller **No**

**Ja**

3D Enabled

**Ja** eller **No**

**Antall**

Plasma

Driftstemperatur fra

**0**–**43** grader

**0**

Driftstemperatur til

**0**–**43** grader

**37**

Projektor

Garanti for projiseringsrør

**6**, **12** eller **18** måneder

**12**

\#av projeksjon rør

**1**–**5**

**3**

## <a name="attribute-type"></a>Attributtype
  [![attributter-fast-kopi](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) attributter er basert på attributtyper. Attributtyper identifiserer datatypen som kan angis for et bestemt attributt. For øyeblikket støtter Microsoft Dynamics 365 for operasjoner attributtet følgende typer:

-   **Valutaen** – Denne attributtypen støtter valutaverdier. Den kan være bundet (det vil si den kan støtte et verdiområde), eller den være tom.
-   **Dato og klokkeslett** – Denne attributtypen støtter dato- og klokkeslettverdier. Den kan være bundet (det vil si den kan støtte et verdiområde), eller den være tom.
-   **Desimal** – Denne attributtypen støtter numeriske verdier som inneholder desimaler. Den støtter også måleenheter. Den kan være bundet (det vil si den kan støtte et verdiområde), eller den være tom.
-   **Heltall** – Denne attributtypen støtter numeriske verdier. Den støtter også måleenheter. Den kan være bundet (det vil si den kan støtte et verdiområde), eller den være tom.
-   **Tekst** – Denne attributtypen støtter tekstverdier. Den støtter også et forhåndsdefinert sett med verdier (opplisting).
-   **Boolsk** – denne attributtypen støtter binære verdier (**SANN**/**false**).
-   **Referanse**

## <a name="attribute"></a>Attributt
  [![createandmanageattribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) i tillegg til navn, navn, beskrivelse og hjelpetekst, én eller flere av følgende typer informasjon kan registreres for et attributt:

-   Standardverdi
-   Attributtmetadata, for eksempel metadata som indikerer om attributtet kan søkes i, finjusteres eller sorteres

## <a name="attribute-group"></a>Attributtgruppe
  [![createandmanageattribute-10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) etter at attributtene er definert, kan de grupperes i attributtgrupper. Attributtgrupper gir grupperinger av individuelle attributter, og kan tilordnes til detaljhandelskategorier eller kanaler for detaljhandel.

## <a name="assigning-attribute-groups-to-retail-categories"></a>Tilordne attributtgrupper til detaljhandelskategorier
  [![createandmanageattribute-12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) én eller flere attributtgrupper kan knyttes til kategorinoder i kategorihierarkiet for retail-produktet. Når varer er kategorisert, arver de attributtene som er inkludert i attributtgruppene.

## <a name="assigning-attribute-groups-to-retail-stores"></a>Tilordne attributtgrupper til detaljhandelsbutikker
  [![createandmanageattribute-13-1024 x 576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) én eller flere attributtgrupper kan tilknyttes én eller flere detaljhandel i retail butikker hierarkiet. Når varer er supplert for spesifikke detaljhandelsbutikker, arver de attributtene som er inkludert i attributtgruppene.

## <a name="overriding-attribute-values"></a>Overstyre attributtverdier
### <a name="at-the-product-level"></a>På produktnivå

  [![createandmanageattribute-14-1024 x 576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) standardverdier for attributter kan overstyres på produktnivå (det vil si for enkeltprodukter).

### <a name="in-a-retail-catalog"></a>I detaljhandelskatalog

  [![createandmanageattribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) standardverdier for attributter kan overstyres for individuelle produkter i bestemte kataloger som er rettet mot bestemte retail kanaler.

### <a name="at-the-retail-channel-level"></a>På nivå for kanal for detaljhandel

  [![createandmanageattribute-1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) standardverdier for attributter kan overstyres for individuelle produkter i bestemte kataloger som er rettet mot bestemte retail kanaler.


