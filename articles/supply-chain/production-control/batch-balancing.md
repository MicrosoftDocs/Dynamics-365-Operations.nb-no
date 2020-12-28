---
title: Partibalansering
description: Dette emnet beskriver prosessen for partibalansering.
author: johanhoffmann
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2ef0a43480e547c6bd19d5f9b7377ed8b73425e7
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434757"
---
# <a name="batch-balancing"></a>Partibalansering

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan prosessen for partibalansering støttes. 

Hvis du vil ha mer informasjon, kan du se en [video om partibalansering](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be).

I prosessen for partiblansering blir antallet ingredienser som skal brukes i et produksjonsparti, beregnet ut fra konsentrasjonen av aktive ingrediensene i valgte produktpartier.

<a name="products-that-have-an-active-ingredient"></a>Produkter som har en aktiv ingrediens
---------------------------------------

Et produkt kan defineres av konsentrasjonen av en aktiv ingrediens. Den aktive ingrediensen til et produkt modelleres ved hjelp av et produktspesifikt partiattributt som har en minimumsverdi, en maksimumsverdi og et målnivå.

Målnivået for et partiattributt representerer den estimerte prosentdelen av en aktiv ingrediens i et produkt. Minimums- og maksimumsverdiene viser til akseptabelt avvik fra målnivået. De kan for eksempel brukes som en godtatt toleranse for partier med produktkvittering.

Et produkt kan bare ha én aktiv ingrediens. Hvis du vil angi den aktive ingrediensen til et produkt, må du først definere et produktspesifikt partiattributt. Du kan deretter knytte til attributtet som et basisattributt av produktet.

På produktnivå må du også angi hvordan nivået for den aktive ingrediensen for et parti av produktet skal registreres: som en del av kjøpsmottaksprosessen eller som en del av en kvalitetsordreprosess.

Hvis du vil knytte et basisattributt til et produkt, kreves følgende oppsett:

-   Produktet du velger, må være partikontrollert. Hvis du vil at et produkt blir partikontrollert, må du tilordne en sporingsdimensjonsgruppe til produktet som har en aktiv partidimensjon.

-   Attributtet som viser ingrediensnivåene må defineres som et produktspesifikt partiattributt for produktet.

Du kan slå opp og redigere den faktiske verdien til den aktive ingrediensen for et parti på siden **Lagerpartiattributter**. 

-  Velg **Lagerstyring** \> **Forespørsler og rapporter** \> **Sporingsdimensjoner** \> **Partier** \> **Lagerpartiattributter**.

<a name="ingredient-types-and-how-they-interact-in-the-batch-balancing-process"></a>Ingredienstyper og hvordan de fungerer sammen i prosessen for partibalansering
---------------------------------------------------------------------

En formellinje som er opprettet kan ha én av disse ingredienstyper:

-   None

-   Aktivt

-   Kompensering

-   Fylling

Resten av denne delen inneholder eksempler som viser hvordan hver Ingredienstype fungerer. Eksemplene er basert på følgende formel med total bunkestørrelse på 100 liter.

| **Ingredienstype** | **Varenummer** | **Formellinjeantall** | **Enhet** |
|---------------------|-----------------|---------------------------|----------|
| None                | A               | 20                        | Liter    |
| Aktivt              | T               | 30                        | Liter    |
| Kompensering        | K               | 10                        | Liter    |
| Fylling              | D               | 40                        | Liter    |

### <a name="active"></a>Aktivt

Når et produkt som har et basisattributt legges til en formellinje, refereres det til som en *aktiv ingrediens* i formelen. Partiordrer med formler som inneholder aktive ingrediensene kan brukes for prosessen for partibalansering. For hver ingrediens i formelen beregner prosessen for partibalansering beløpet som kreves for å produsere produktet. Beregningen av antall er basert på konsentrasjonen av aktive ingredienser i de valgte partiene.

**Eksempel**

Ingrediens B har basisattributt X og et målnivå på 30, og den er inkludert i en formel som krever 30 liter av ingrediens B for hver 100 liter av produktet. Det opprettes en partiordre med en bunkestørrelse på 100 liter. Partiordren har startet og under prosessen for partibalansering velger brukeren en bunke med ingrediens B som har styrkenivå 35. Fordi styrkenivået 35 er høyere enn målnivået 30, reduseres balansert antall av ingrediens B ved hjelp av forholdet mellom styrkeverdien og målnivået for partiet, som blir multiplisert med estimert antallet. Beregningen av balansert antall ser slik ut:

(30 ÷ 35) x 30 liter = 25,71 liter

| **Varenummer** | **Ingredienstype** | **Estimert antall** | **Balansert antall** | **Aktivt antall** | **Enhet** | **Grunnlagsverdi** |
|-----------------|---------------------|------------------------|-----------------------|---------------------|----------|----------------|
| A               | None                | 20                     | 20                    |                     | Liter    |                |
| T               | Aktivt              | 30                     | 25.71                 | 9.00                | Liter    | 30,00          |
| K               | Kompensering        | 10                     | 14.72                 |                     | Liter    |                |
| D               | Fylling              | 40                     | 39.57                 |                     | Liter    |                |

### <a name="none"></a>None

Hvis du bruker prosessen for partibalansering når ingredienstypen er **ingen**, og estimert antall og balansert antall i formellinjen i partiordren er lik.

**Eksempel**

Ingrediens A er tilordnet til en ingrediens av typen **Ingen** og lagt til en formel for et ferdig produkt. Formelen krever 10 liter av ingrediens A for hver 100 liter av det ferdige produktet. Når en partiordre krever 200 liter, beregnes både estimert antall og balansert antall av ingrediens A som 20 liter.

### <a name="compensating"></a>Kompensering

En kompensasjonsingrediens kan enten forskyve eller komplementere virkningen av den aktive ingrediensen i et produkt. Antallet av en kompensasjonsingrediens som brukes er derfor avhengig av styrken til produktet:

-   **Motstående effekt** – hvis antallet til den aktive ingrediensen er høyere enn forventet, må du legge til mindre av kompensasjonsingrediensen.

-   **Komplementær effekt** – hvis antallet til den aktive ingrediensen er lavere enn forventet, må du legge til mer av kompensasjonsingrediensen.

Forholdet mellom en aktiv ingrediens og en komplementær ingrediens defineres på siden **Kompensasjonsprinsipp**.

Følg disse trinnene for å definere relasjoner mellom ingredienser.

1.  Velg **Produktinformasjonsbehandling** \> **Stykklister og formler** \> **Formler**, åpne en formellinje, og velg deretter **Ingredienser** for å åpne siden **Kompensasjon prinsippet**.

2.  Merk linjen som representerer et kompensasjonsprinsipp og velg deretter den aktive ingrediensen som skal kompenseres.

>   I kompensasjonsprinsippet må du også angi en positiv eller negativ kompenserende faktor for å angi hvor mye det skal kompenseres for, og om prinsippet skal være motstående eller komplementær. En positiv faktor angir en komplementær effekt, og en negativ faktor angir motstående effekt.

**Eksempel**

Ingrediens B er en aktiv ingrediens med basisattributtet X og et målnivå på 30. Den er inkludert i en formel som krever 30 liter av ingrediens B for hver 100 liter av produktet. Ingrediens C er en kompensasjonsingrediens, og et antall på 10 er inkludert i den samme formelen. En kompensasjonsfaktor på 1,10 er definert for kompensasjonsprinsippet. Balansert antall av kompensasjonsingrediensen vil derfor bli redusert med differansen mellom balansert antall til den aktive ingrediensen og estimert nødvendig antall multiplisert med 1,10.

I eksemplet for den **aktive** ingredienstypen, beregnes balansert antall av den nødvendige aktive ingrediensen som 25,71, og estimert nødvendig antall beregnes som 30. I så fall beregnes balansert antall av kompensasjonsingrediensen slik:

1.  Forskjellen mellom estimert og balansert antall bestemmes:

>   25,71 – 30 = –4,29

2.  Resultatet multipliseres deretter med kompensasjonsfaktoren:

>   4,29 x 1.10 = –4,72

3.  Det estimerte kompensasjonsantallet reduseres med –4,72 for å bestemme det balanserte kompensasjonsantallet:

>   10 – (–4,72) = 14,72

Ettersom 1,10 er en positiv kompensasjonsfaktor, har dette kompensasjonsprinsippet en utfyllende effekt. I dette tilfellet er den aktive ingrediensen sterkere enn forventet. Mer av kompensasjonsingrediensen er derfor nødvendig.

### <a name="filler"></a>Fylling

En *fyllingrediens* er en nøytral ingrediens som brukes til å nå ønsket produsert antall av det ferdige produktet. Justeringer i antall fyllingrediens kalkuleres basert på variasjoner i den aktive ingrediensen og kompensasjonsingrediensen, sammenlignet med standardantallet.

**Eksempel**

Du har formulert et produkt som har ingrediensene A, B, C og D for en formelstørrelse på 100 liter. Du har beregnet balansert antall for alle ingredienstyper bortsett fra ingredienstypen **Fylling** som skal brukes på én linje.
Balansert antall fyllingrediens beregnes som differansen mellom partistørrelsen for 100 liter og summen av ingrediensene A, B og C:

100 – (20 + 25,71 + 14,72) = 39,57

<a name="the-batch-balancing-process"></a>Prosessen for partibalansering.
---------------------------

Prosessen for partibalansering utføres fra siden **Partibalansering**.
Velg **Kostnadsstyring** \> **Partiordrer**, og velg deretter **Partibalansering** i kategorien **Prosess**. Partibalansering er tilgjengelig for partiordrer som har status **Startet**.

Vanligvis kan partibalansering bare brukes for partiordrer hvis formelen har minst én formellinjen der ingredienstypen er **Aktiv**. (For unntaket på denne regelen kan du se delen "Partiordrer som ikke er tilgjengelige for partibalansering" senere i dette emnet.)

Prosessen for partibalansering kan deles inn i to delprosesser:

1.  Balanser ingredienser for parti

2.  Bekreft og frigi formelen

### <a name="balance-batch-ingredients"></a>Balanser ingredienser for parti

I prosessen for partiblansering av ingredienser blir antall ingredienser som skal brukes i et produksjonsparti, beregnet ut fra de valgte partiene som har aktive ingredienser. Som regel kan beregningen bare fullføres når det er fullstendig dekning av alle ingrediensene. Du kan ikke balansere bare en del av et parti som partiordren er konfigurert til å produsere.

[!NOTE]
Du kan ikke lagre en beregning, og deretter fullføre prosessen for partibalansering senere. Hvis du lukker siden **Partibalansering**, må du gjenta beregningen for å fullføre prosessen.

### <a name="confirm-and-release-the-formula"></a>Bekreft og frigi formelen

Når ingrediensantallene er beregnet, kan du bekrefte og frigi formelen. Frigivelsesprosessen varierer, avhengig av om produktene er aktivert for lagerstyringsprosessene:

-   Hvis et produkt er aktivert for lagerstyringsprosessene, er formellinjen frigitt til lageret i henhold til prinsippene for lagerstyringsprosessene. Formellinjen er frigitt i mengder som samsvarer med de balanserte antallene, og den frigis for de bestemte partiene som er valgt for de aktive ingrediensene.

> [!NOTE]
>   Formellinjer kan kun frigis til lageret som en del av prosessen for partibalansering. Selv om det finnes andre alternativer for hvordan du frigir materialene for produksjon til lager, kan disse alternativene ikke brukes for formellinjer.

-   Hvis et produkt ikke er aktivert for lagerstyringsprosessene, opprettes en produksjonsplukkliste for produktet når du bekrefter og frigir formelen.

I en formel kan du kombinere produkter som er aktivert for lagerstyringsprosessene og produkter som ikke er aktivert for lagerstyringsprosessene. Når de to produkttypene inkluderesi én formel, frigis produktene som er aktivert for lagerstyringsprosessene til lageret. Produkter som ikke er aktivert for lagerstyringsprosessene, opprettes en plukkliste når du bekrefter og frigir formelen.

### <a name="batch-orders-that-arent-applicable-for-batch-balancing"></a>Partiordrer som ikke er tilgjengelige for partibalansering

Det er ett unntak på regelen om at partiprdre kun kan partibalanseres hvis formelen har minst én formellinjen der ingredienstypen er **Aktiv**.

Hvis en formel inneholder en aktiv ingrediens for et produkt som er aktivert for lagerstyringsprosessene, men partinummeret er under reservasjonshierarkiet, er partiordren ikke tilgjengelig for partibalansering.

En partiordre som ikke er tilgjengelig for partibalansering går gjennom den vanlige prosessyklusen for partiordrer.
