---
title: Oversikt over arbeidspolicyer for lager
description: Arbeidspolicyer for lager kontrollerer om lagerarbeid opprettes for lagerprosesser i produksjon, basert på arbeidsordretype, lagerlokasjon og produkt.
author: johanhoffmann
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 3fe22a92b445abbf6d1dcc67ead878db3f80d532
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204568"
---
# <a name="warehouse-work-policies-overview"></a>Oversikt over arbeidspolicyer for lager

[!include [banner](../includes/banner.md)]

Arbeidspolicyer for lager kontrollerer om lagerarbeid opprettes for lagerprosesser i produksjon, basert på arbeidsordretype, lagerlokasjon og produkt.

Denne arbeidspolicyen kontrollerer om lagerarbeid opprettes for lagerprosesser i produksjon. Du kan definere arbeidspolicyen ved hjelp av en kombinasjon av **arbeidsordretyper**, en **lagerplassering** og et **produkt**. Produkt L0101 rapporteres for eksempel som ferdig til utleveringslokasjon 001. Den ferdige varen forbrukes senere i en annen produksjonsordre på utleveringslokasjon 001. I så fall kan du definere en arbeidspolicy for å hindre at arbeidet for plassering av ferdigvarer blir opprettet når du rapporterer produkt L0101 som ferdige, til utleveringslokasjon 001. Arbeidspolicyen er en enkeltenhet som kan beskrives ved hjelp av følgende informasjon:

-   **Arbeidspolicynavn**(den unike ID-en for arbeidspolicyen)
-   **Arbeideordretyper** og **arbeidsopprettelsesmetode**
-   **Lagerlokasjoner**
-   **Produkter**

## <a name="work-order-types"></a>Arbeidsordretyper
Du kan velge blant følgende arbeidsordretyper:

-   Plasser ferdigvarer
-   Plasser koprodukt og biprodukt
-   Råvareplukking

**Arbeidsopprettelsesmetode**-feltet har verdien **Aldri**. Denne verdien angir at arbeidspolicyen hindrer at lagerarbeid opprettes for den valgte arbeidsordretypen.

## <a name="inventory-locations"></a>Lagerlokasjoner
Du kan velge en lokasjon som arbeidspolicyen gjelder for. Hvis ingen lokasjon er knyttet til en arbeidspolicy, gjelder ikke arbeidspolicyen for noen prosesser. På **Lokasjoner**-siden du kan også merke eller fjerne merkingen av arbeidspolicyen for en bestemt lokasjon.

## <a name="products"></a>Produkter
Du kan velge et produkt som arbeidspolicyen gjelder for. Du kan bruke arbeidspolicyen på alle produkter eller valgte produkter.

## <a name="example"></a>Eksempel
I eksemplet nedenfor er det to produksjonsordrer, PRD-001 og PRD 00*2*. Produksjonsordren PRD-001 har en operasjon kalt **Montering**, der produktet SC1 rapporteres som ferdig til lokasjonen O1. Produksjonsordren PRD-002 er en operasjon kalt **Maling**, og den bruker SC1-produktet fra lokasjonen O1. Produksjonsordren PRD-002 bruker også råvaren RM1 fra lokasjonen O1. RM1 er lagret i lagerlokasjonen BULK-001 og blir plukket til lokasjon O1 av lagerarbeid for plukking av råvarer. Plukkarbeidet blir generert når produksjonen PRD-002 frigis. 

[![Arbeidspolicyer for lager](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png) 

Når du skal konfigurere en arbeidspolicy for lageret i dette scenariet, bør du vurdere følgende informasjon:

-   Lagerarbeid for plassering av ferdigvarer er ikke nødvendig når du rapporterer produktet SC1 som ferdig fra produksjonordren PRD-001 til lokasjonen O1. Dette skjer fordi operasjonen **Maling** for produksjonsordre PRD-002 bruker SC1 på samme lokasjon.
-   Lagerarbeid for plukking av råvarer kreves for å flytte råvaren RM1 fra lagerlokasjonen BULK-001 til lokasjonen O1.

Her er et eksempel på arbeidspolicyen som du kan sette opp, basert på disse hensynene.


|                                       |                                       |
|---------------------------------------|---------------------------------------|
| <strong>Arbeidspolicynavn</strong><br> | <strong>Arbeidsordretyper</strong><br> |
|         Ingen plassering 01     `          |     - Plassering av ferdigvare<br>      |
|                                       |    <strong>Lokasjoner</strong><br>     |
|                                       |                 - O1                  |
|                                       |    <strong>Produkter</strong> <br>     |
|                                       |                 - SC1                 |

Fremgangsmåtene nedenfor inneholder trinnvise instruksjoner om hvordan du definerer lagerarbeidspolicyen i dette scenariet. Et eksempeloppsett som viser hvordan du rapporterer en produksjonsordre som ferdig til en lokasjon som ikke er nummerskiltkontrollert beskrives også.

## <a name="set-up-a-warehouse-work-policy"></a>Definere en lagerarbeidspolicy
Lagerprosesser inkluderer ikke alltid lagerarbeid. Ved å definere en arbeidspolicy, kan du hindre oppretting av arbeid for råvareplukking og plassering av ferdige varer for et sett med produkter på bestemte lokasjoner. Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne fremgangsmåten. 

TRINN (21)

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| 1  | Gå til Lagerstyring &gt; Oppsett &gt; Arbeid &gt; Arbeidspolicyer.        |
| 2  | Klikk Ny.                                                                 |
| 3  | Skriv inn 'Ingen ferdigvarearbeid' i navnefeltet for arbeidspolicyen.                    |
| 4  | Klikk Lagre.                                                                |
| 5  | Klikk Legg til.                                                                 |
| 6  | Merk den valgte raden i listen.                                        |
| 7  | Velg Plasser ferdigvarer i feltet for Arbeidsordretype.            |
| 8  | Klikk Legg til.                                                                 |
| 9  | Merk den valgte raden i listen.                                        |
| 10. | Velg Plasser koprodukt og biprodukt i feltet Arbeidsordretype. |
| 11. | Vis delen Lagerlokasjoner.                                    |
| 12. | Klikk Legg til.                                                                 |
| 13 | Merk den valgte raden i listen.                                        |
| 14. | Angi 51 i Lager-listen.                                         |
| 15. | Velg 001 i feltet Lokasjon.                              |
| 16. | Utvid seksjonen Produkter.                                               |
| 17. | Velg Valgt i feltet Produktvalg.                         |
| 18. | Klikk Legg til.                                                                 |
| 19. | Merk den valgte raden i listen.                                        |
| 20. | Angi eller velg L0101 i Varenummer-feltet.                         |
| 21. | Klikk Lagre.                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Rapportere en produksjonsordre som ferdig til en lokasjon som ikke er nummerskiltkontrollert
Denne fremgangsmåten viser et eksempel på rapportering som ferdig til en lokasjon som ikke er nummerskiltkontrollert. En gjeldende arbeidspolicy er en forutsetning for denne oppgaven. Den tidligere fremgangsmåten viste oppsettet av arbeidspolicyen. 

TRINN (25)

<table>
<tbody>
<tr>
<td colspan="3"><strong>Underoppgave: Definere en utleveringslokasjon.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Gå til Organisasjonsstyring &gt; Ressurser &gt; Ressursgrupper.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Velg ressursgruppe &#39;5102&#39; i listen.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Klikk Rediger.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Angi &#39;51&#39; i feltet Utleveringslager.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Angi &#39;001&#39; i feltet Utleveringslokasjon.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Lokasjonen 001 er ikke en nummerskiltkontrollert lokasjon. Du kan definere en utleveringslokasjon uten nummerskilt hvis det finnes en gjeldende arbeidspolicy for lokasjonen.</td>
</tr>
<tr>
<td colspan="3"><strong>Underoppgave: Opprette en produksjonsordre og rapportere den som avsluttet.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Lukk siden.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Gå til Produksjonskontroll &gt; Produksjonsordrer &gt; Alle produksjonsordrer.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Klikk Ny produksjonsordre.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Angi &#39;L0101&#39; i feltet Varenummer.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Klikk Opprett.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Klikk Produksjonsordre i handlingsruten.</td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td>Klikk Estimer.</td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td>Klikk OK.</td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td>Klikk Start.</td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td>Klikk kategorien Generelt.</td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td>Velg &#39;Aldri&#39; i feltet Automatisk stykklisteforbruk.</td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td>Klikk OK.</td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td>Klikk Rapporter som fullført.</td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td>Klikk kategorien Generelt.</td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td>Velg Ja i feltet Godtar feil.</td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td>Klikk OK.</td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td>Klikk Lager i handlingsruten.</td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td>Klikk Arbeidsdetaljer.</td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td>Når produksjonsordren ble rapportert som fullført, ble det ikke generert arbeid for plassering. Dette skjer fordi en arbeidspolicy er definert som hindrer at arbeidet blir generert når produktet L0101 rapporteres som ferdig til lokasjon 001.</td>
</tr>
</tbody>
</table>



