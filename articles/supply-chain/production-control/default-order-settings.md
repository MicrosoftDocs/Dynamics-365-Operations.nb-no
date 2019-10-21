---
title: Standard ordreinnstillinger for dimensjoner og produktvarianter
description: Standard ordreinnstillinger definerer området og lageret der varene hentes fra eller lagres, minimumsantall, maksimumsantall, flere og standardantall som skal brukes for handel, eller lagerstyring, leveringstider, stoppflagget og metoden for ordrebekreftelsen.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemOrderSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e6d4e9a3ac5635e292b20eba60fe4f010562fdba
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250101"
---
# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Standard ordreinnstillinger for dimensjoner og produktvarianter

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Standard ordreinnstillinger i Dynamics 365 Supply Chain Management definerer området og lageret der varene hentes fra eller lagres, minimumsantall, maksimumsantall, flere og standardantall som skal brukes for handel, eller lagerstyring, leveringstider, stoppflagget og metoden for ordrebekreftelsen. Standard ordreinnstillinger som brukes ved oppretting av bestillinger, salgsordrer, overføringsordrer, lagerjournaler og av hovedplanlegging for generering av planlagte ordrer. Standard ordreinnstillinger kan være varespesifikke, områdespesifikke, spesifikke for produktvariant eller spesifikke for produktdimensjon.

Du kan definere standard ordreinnstillinger på siden **Standard ordreinnstillinger**. For å åpne denne siden, gå til **Produktinformasjonsstyring** &gt; **Produkter** &gt; **Utgitte produkter** &gt; **Velg et utgitt produkt** &gt; på **Plan** eller **Administrer lager** handlingsruten &gt;**Ordreinnstillinger** &gt; **Standard ordreinnstillinger**.

## <a name="default-order-settings"></a>Standard ordreinnstillinger
Det finnes tre typer standard ordreinnstillinger for kjøp, salg og lager. Standard ordreinnstillinger for kjøp brukes ved opprettelse av:

-   Bestillingslinjer
-   Kjøpsavtalelinjer
-   Tilbudsforespørselslinjer
-   Innkjøpsrekvisisjonslinjer
-   Etterfyllingslinjer for forsendelse
-   Bestillingsforslag

Standard ordreinnstillinger for salg brukes ved opprettelse av:

-   Salgsordrelinjer
-   Salgsavtalelinjer
-   Salgstilbudslinjer
-   Gå tilbake til ordrelinjer og vareerstatningslinjer
-   Behovsprognoselinjer

Standard salgsordreinnstillinger gjelder også ved opprettelse av:

-   Prosjektvarekrav
-   Varebehov for serviceordre

Standard ordreinnstillinger for lager brukes ved opprettelse av:

-   Lagerjournaler
-   Overføringsordrer
-   Overføringsforslag

Standard lagerordreinnstillinger gjelder også ved opprettelse av:

-   Karanteneordrer
-   Kvalitetsordrer
-   Produksjonsordrer
-   Stykklistelinjer
-   Planlagte produksjonsordrer

## <a name="full-definition-of-a-released-product"></a>Fullstendig definisjon av et frigitt produkt
Når du oppretter en transaksjon, må du angi hele definisjonen av et frigitt produkt på linjen i bestilling for Supply Chain Management for å forsøke å identifisere standard ordreinnstillinger. Den fullstendige definisjonen for frigitt produkt betyr at varenummeret og alle de aktive produktdimensjonene, for eksempel konfigurasjon, størrelse, stil og farge, er angitt for transaksjonen. Hvis du for eksempel manuelt oppretter en bestillingslinje for en frigitt produktvariant, må du angi alle de obligatoriske dimensjonene før område, lager, antall og leveringstid vil vises som standard på ordrelinjen. 

Ikke alle standardparametere for ordreinnstillinger brukes når du oppretter ordre- eller journallinjer. Antall og leveringstider vil bare vises som standard når det passer. Når du for eksempel teller en journallinje, vises bare området og lageret som standard når linjen opprettes. Tilbakestilling til standard antall eller kontroller på flere og minimum utføres selvsagt ikke ved oppretting av linjen eller postering av journalen. 

Systemet prøver alltid å finne et standardområde og -lager når det opprettes en ordre- eller journallinje. Området vises ikke alltid som standard fra ordreinnstillingene. Når du for eksempel oppretter en salgsordre eller en bestilling, brukes området fra ordrehodet automatisk på ordrelinjene. Når du oppretter en stykklistelinje, brukes området fra stykklistehodet. Når området er fastslått, brukes det til å finne alle områdespesifikke ordreinnstillinger som deretter kan brukes som standard for lageret. 

Standard ordretype, kjøpet og lagerleveringstiden kan overstyres av dekningsregler for varen på **Varedekning**-siden. Selv om standard ordreinnstillinger ikke tillater et skille mellom produksjons og overføringstid, tillater dekningsreglene for varen dette. Oppsett av varedekning brukes imidlertid bare av MRP ved oppretting av planlagte produksjonsordrer og overføringsordrer, og brukes ikke ved manuell oppretting av produksjons- og overføringsordrer. 

## <a name="default-order-settings-rules"></a>Regler for standard ordreinnstillinger
Du kan definere generelle standard ordreinnstillinger og et hvilken som helst antall regler for standard ordreinnstilling som gjelder bare under bestemte vilkår, for eksempel som en spesifikk kombinasjon av produktdimensjon eller produktdimensjoner. Du kan ikke definere lagerspesifikke ordreinnstillinger.

### <a name="rank-in-default-order-settings"></a>Rangere i standard ordreinnstillinger

Reglene for standard ordreinnstillinger har rangeringer. Jo høyere rangering, jo viktigere er regelen, noe som betyr at den skal ha en høyere prioritet og brukes før reglene med lavere rangering. De generelle standard ordreinnstillingene har rangeringen null, som ikke kan endres. Det kan bare være én regel med rangeringen null. Regler kan ha samme rangering, forutsatt at dimensjonene de gjelder for er forskjellige. Dette er nyttig for angivelse av områdespesifikke ordreinnstillinger. Når det opprettes en ny regel for standard ordreinnstillinger, arves verdiene for ordreverdier, stoppflagg og så videre, fra regelen med rangeringen null, men dette kan overstyres.

### <a name="default-order-settings-for-released-products"></a>Standard ordreinnstillinger for frigitte produkter

Du kan definere generelle ordreinnstillinger eller områdespesifikke ordreinnstillinger for spesifikke frigitte produkter. De generelle ordreinnstillingene har alltid rangeringen null. Hvis du definerer nye salg, kjøp og lagerordreinnstillinger samtidig, anbefaler vi at du bruker **Detaljvisning** på siden **Standard ordreinnstillinger**. Hvis du vil bytte til detaljvisningen, kan du gå til handlingsruten **Alternativer** &gt; **Sidealternativer** &gt; **Endre visning** &gt; **Detaljvisning**.

### <a name="site-specific-order-settings"></a>Områdespesifikke ordreinnstillinger

Hvis du vil opprette områdespesifikke ordreinnstillinger, klikker du **Ny**. I **Detaljvisning** fyller du ut området i **Innstillinger som kan brukes for** &gt; **Område**-feltet. I **Rutenettvisning** fyller du ut området i **Område**-kolonnen. Den nye regelen får automatisk en ny rangeringsverdi som er høyere enn null. Du kan opprette så mange områdespesifikke regler som du har behov for, og du kan tilordne alle de områdespesifikke reglene til samme rangering, for å angi at de er like viktig. 

Hvis du er i **Detaljvisning**, får du ikke en oversikt over reglene som er opprettet for varen. Aktiver/deaktiver **Vis/skjul liste** for å se informasjon om oversikt. Når det opprettes en ordrelinje av hvilken som helst type og det ikke er angitt område for den, søker Supply Chain Management etter en regel uten angitt område. Dette kan bidra til å bestemme et standardområde på ordrelinjen. Dette området brukes deretter til å søke etter en områdespesifikk regel der et standardlager kan ha blitt angitt. Dette lageret brukes for ordrelinjen.

### <a name="specific-order-settings-for-product-dimension"></a>Spesifikke ordreinnstillinger for produktdimensjon

Du kan definere regler for ordreinnstillinger for en aktiv produktdimensjon eller en kombinasjon av aktive produktdimensjoner. Hvis et produktdimensjonsfelt et tomt, gjelder regelen for alle verdier for produktdimensjonen. 

Tenk deg følgende eksempelprodukt:

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Produktnavn**                                    | Fotoelektrisk sensor                    |
| **Varenummer**                                     | XW56                                    |
| **Konfigurasjon** (brukes til å angi type lys) | C1-Synlig rødt lys, C2-infrarødt lys |
| **Stil** (brukes til å angi den tekniske revisjonen)  | R1, R2, R3                              |

I dette eksemplet antas det at produktet er kjøpt og ikke produsert. Anta også at den vanligste konfigurasjonen er C1, slik at den er kortere leveringstider. 

Opprett følgende standard ordreinnstillinger for å angi dette scenariet.

| Rangering | Område | Konfigurasjon | Stil | Kjøp – Overstyr standardinnstillinger | Leveringstid for innkjøp | Kjøp – Stoppet | Salg – Overstyr standardinnstillinger | Salg – Stoppet |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Ja                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Når en bestillingslinje eller en planlagt bestilling opprettes for XW56, konfigurasjon C1, uavhengig av revisjon eller området som linjen er plassert i, vil leveringstiden være 2. Anta at alle revisjoner i tillegg til R3 stoppes.

Du kan opprette reglene nedenfor for standard ordreinnstillinger.

| Rangering | Område | Konfigurasjon | Stil | Kjøp – Overstyr standardinnstillinger | Leveringstid for innkjøp | Kjøp – Stoppet | Salg – Overstyr standardinnstillinger | Salg – Stoppet |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | R2    | Ja                                  |                    | Ja                | Ja                               | Ja             |
| 20   |      |               | R1    | Ja                                  |                    | Ja                | Ja                               | Ja             |
| 10   |      | C1            |       | Ja                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

De to reglene for å stoppe de gamle revisjonene har samme rangering, noe som betyr at de er like viktig. Begge har en høyere rangering enn regelen for konfigurasjonen C1, noe som betyr at de har prioritet over regelen for konfigurasjonen C1. 

Dette eksemplet beskriver behovet for rangeringen. Hvis det opprettes en bestilling for konfigurasjonen C1 og revisjonen R2, ville de to reglene som er definert for R2 og C1, være tvetydige hvis det manglet rangering. Supply Chain Management løser denne tvetydigheten ved å søke gjennom reglene i synkende rekkefølge og bruke den første gjeldende regelen. Når det opprettes bestillingslinjer i gjeldende eksempel for konfigurasjon C1 og revisjon R2, får brukeren en advarsel om at varen er sperret og at dette er forårsaket av revisjonsverdien. Hvis regelen for konfigurasjonen hadde en høyere rang enn tilsvarende for revisjon, ville oppretting av en bestillingslinje for konfigurasjon C1 og revisjon R2 ha blitt fullført, og ingen melding om sperret vare ville blitt gitt til brukeren. 

Tenk deg reglene nedenfor for standard ordreinnstillinger.

| Rangering | Område | Konfigurasjon | Stil | Standardområde | Standardlager | Kjøp – Overstyr standard lagringsdimensjoner | Innkjøpslager |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Ja                                            | 22                 |
| 10   |      | C1            |  R2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Systemet går gjennom settet med regler to ganger for å finne området og lageret. Når det opprettes bestillingslinjer for konfigurasjon C1, stil R2, bestemmes området basert på regelen med rangering 10. Deretter søker systemet etter en regel for område 2 for å finne et lager. Regel 20 blir funnet, og fordi den har en høyere rangering, vil lageret på bestillingslinjen være 22 og ikke 21. 

Som en generell veiledning vil spesifikke regler og regler for dimensjonene som er viktigere enn andre dimensjoner, få høyere rangering, mens mer generelle regler får lavere rangeringer. 

Regelen med rangeringen null fungerer som et sikkerhetsnett. Hvis ingen andre regler får treff, brukes standard ordreinnstillinger fra regel null. 

Siden rangeringsnummeret er så viktig, finnes det i handlingsruten **Standard ordreinnstillinger** funksjoner for å flytte en regel opp eller ned og nummerere reglene, slik at de er alltid med økes med 10. 

Det kan opprettes mange regler for et frigitt produkt. Hvis du vil ha mer informasjon om hva hver enkelt regel overstyrer og hvorfor det er nødvendig, anbefaler vi at du bruker **Rutenettvisning** på siden **Standard ordreinnstillinger**. Du kan aktivere rutenettvisning ved å gå til handlingsruten **Alternativer** &gt; **Sidealternativer** &gt; **Endre visning** &gt; **Rutenettvisning**. Det kan vises svært mange kolonner i rutenettet, spesielt for kategoriene salg og lager. Hvis du vil begrense hvor mange kolonner som vises i rutenettet, kan grupper av kolonner skjules eller vises ved hjelp av knappene på menyen **Standard ordreinnstillinger** &gt; **Kolonnevisning**.

### <a name="specific-order-settings-for-released-product-variant"></a>Spesifikke ordreinnstillinger for frigitt produktvariant

Hvis regelsystemet for standard ordreinnstillinger er for tungvint, er det mulig å bare definere standard ordreinnstillinger for hver produktvariant. Eksemplene nedenfor viser hvordan det vil søke etter produktet og sakene som er beskrevet ovenfor.

| Rangering | Område | Konfigurasjon | Stil | Kjøp – Overstyr standardinnstillinger | Leveringstid for innkjøp | Kjøp – Stoppet | Salg – Overstyr standardinnstillinger | Salg – Stoppet |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | R3    | Ja                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | R2    | Ja                                  | 5                  | Ja                | Ja                               | Ja             |
| 10   |      | C2            | R1    | Ja                                  | 5                  | Ja                | Ja                               | Ja             |
| 10   |      | C1            | R3    | Ja                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | R2    | Ja                                  | 2                  | Ja                | Ja                               | Ja             |
| 10   |      | C1            | R1    | Ja                                  | 2                  | Ja                | Ja                               | Ja             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Rangeringen i dette tilfellet har ingen betydning, slik at du kan velge å skjule den. Denne løsningen introduserer potensielt et vedlikeholdsproblem. Du bør imidlertid vurdere å bruke dette oppsettet Hvis du vil integrere med PLM-systemer (Product Lifecycle Management).



