---
title: Standard ordreinnstillinger for dimensjoner og produktvarianter
description: Standard ordreinnstillinger definerer området og lageret der varene hentes fra eller lagres, minimumsantall, maksimumsantall, flere og standardantall som skal brukes for handel, eller lagerstyring, leveringstider, stoppflagget og metoden for ordrebekreftelsen.
author: t-benebo
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0654ba019b71dc952ea52f206bc60d8fa05dd4ff
ms.sourcegitcommit: f9917706d45693e8d3f9f6224dca9e601db44bae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/04/2020
ms.locfileid: "3657346"
---
# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Standard ordreinnstillinger for dimensjoner og produktvarianter

[!include [banner](../includes/banner.md)]

Standard ordreinnstillinger i Dynamics 365 Supply Chain Management definerer området og lageret der varene hentes fra eller lagres, minimumsantall, maksimumsantall, flere og standardantall som skal brukes for handel, eller lagerstyring, leveringstider, stoppflagget og metoden for ordrebekreftelsen. Standard ordreinnstillinger som brukes ved oppretting av bestillinger, salgsordrer, overføringsordrer, lagerjournaler og av hovedplanlegging for generering av planlagte ordrer. Standard ordreinnstillinger kan være varespesifikke, områdespesifikke, spesifikke for produktvariant eller spesifikke for produktdimensjon.

Følg denne fremgangsmåten for å definere standard ordreinnstillinger for et produkt.

1. Gå til **Administrering av produktinformasjon** &gt; **Produkter** &gt; **Frigitte produkter**.
1. Velg det relevante produktet i rutenettet.
1. I handlingsruten følger du ett av disse trinnene for å åpne siden **Standard ordreinnstillinger** for det valgte produktet:

    - På **Plan**-fanen, i gruppen **Ordreinnstillinger**, velger du **Standard ordreinnstillinger**.
    - På fanen **Administrer lager**, i gruppen **Ordreinnstillinger**, velger du **Standard ordreinnstillinger**.

1. Konfigurer innstillingene slik det er beskrevet i resten av dette emnet.

## <a name="default-order-settings"></a>Standard ordreinnstillinger

Det finnes tre typer standard ordreinnstillinger for kjøp, salg og lager. Standard ordreinnstillinger for kjøp brukes ved opprettelse av:

- Bestillingslinjer
- Kjøpsavtalelinjer
- Tilbudsforespørselslinjer
- Innkjøpsrekvisisjonslinjer
- Etterfyllingslinjer for forsendelse
- Bestillingsforslag

Standard ordreinnstillinger for salg brukes ved opprettelse av:

- Salgsordrelinjer
- Salgsavtalelinjer
- Salgstilbudslinjer
- Gå tilbake til ordrelinjer og vareerstatningslinjer
- Behovsprognoselinjer

Standard salgsordreinnstillinger gjelder også ved opprettelse av:

- Prosjektvarekrav
- Varebehov for serviceordre

Standard ordreinnstillinger for lager brukes ved opprettelse av:

- Lagerjournaler
- Overføringsordrer
- Overføringsforslag

Standard lagerordreinnstillinger gjelder også ved opprettelse av:

- Karanteneordrer
- Kvalitetsordrer
- Produksjonsordrer
- Stykklistelinjer
- Planlagte produksjonsordrer

## <a name="full-definition-of-a-released-product"></a>Fullstendig definisjon av et frigitt produkt

Når du oppretter en transaksjon, må du angi hele definisjonen av et frigitt produkt på linjen, slik at Supply Chain Management kan forsøke å identifisere standard ordreinnstillinger. I den fullstendige definisjonen for et frigitt produkt er varenummeret og alle de aktive produktdimensjonene, for eksempel konfigurasjon, størrelse, stil, versjon og farge, angitt for transaksjonen. Hvis du for eksempel manuelt oppretter en bestillingslinje for en frigitt produktvariant, må du angi alle de obligatoriske dimensjonene før område, lager, antall og leveringstid vil vises som standard på ordrelinjen. 

Ikke alle standardparametere for ordreinnstillinger brukes når du oppretter ordre- eller journallinjer. Antall og leveringstider vil bare vises som standard når det passer. Når du for eksempel teller en journallinje, vises bare området og lageret som standard når linjen opprettes. Av denne grunn utfrøes ingen tilbakestilling til standard antall eller kontroller på flere og minimum ved oppretting av linjen eller postering av journalen. 

Systemet prøver alltid å finne et standardområde og -lager når det opprettes en ordre- eller journallinje. Området vises ikke alltid som standard fra ordreinnstillingene. Når du for eksempel oppretter en salgsordre eller en bestilling, brukes området fra ordrehodet automatisk på ordrelinjene. Når du oppretter en stykklistelinje, brukes området fra stykklistehodet. Når området er fastslått, brukes det til å finne alle områdespesifikke ordreinnstillinger som deretter kan brukes som standard for lageret. 

Standard ordretype, kjøpet og lagerleveringstiden kan overstyres av dekningsregler for varen på **Varedekning**-siden. Selv om standard ordreinnstillinger ikke tillater et skille mellom produksjons og overføringstid, tillater dekningsreglene for varen dette. Oppsett av varedekning brukes imidlertid bare av hovedplanlegging (MRP) ved oppretting av planlagte produksjonsordrer og overføringsordrer, og brukes ikke ved manuell oppretting av produksjons- og overføringsordrer. 

## <a name="default-order-settings-rules"></a>Regler for standard ordreinnstillinger

Du kan definere generelle standard ordreinnstillinger og et hvilken som helst antall regler for standard ordreinnstilling som gjelder bare under bestemte vilkår, for eksempel som en spesifikk kombinasjon av produktdimensjon eller produktdimensjoner. Du kan ikke definere lagerspesifikke ordreinnstillinger.

### <a name="rank-in-default-order-settings"></a>Rangere i standard ordreinnstillinger

Reglene for standard ordreinnstillinger har rangeringer. Jo høyere rangering, jo viktigere er regelen, noe som betyr at den skal ha en høyere prioritet og brukes før reglene med lavere rangering. De generelle standard ordreinnstillingene har rangeringen null, som ikke kan endres. Det kan bare være én regel med rangeringen null. Regler kan ha samme rangering, forutsatt at dimensjonene de gjelder for er forskjellige. Dette er nyttig for angivelse av områdespesifikke ordreinnstillinger. Når det opprettes en ny regel for standard ordreinnstillinger, arves verdiene for ordreverdier, stoppflagg og så videre, fra regelen med rangeringen null, men dette kan overstyres.

### <a name="default-order-settings-for-released-products"></a>Standard ordreinnstillinger for frigitte produkter

Du kan definere generelle ordreinnstillinger eller områdespesifikke ordreinnstillinger for spesifikke frigitte produkter. De generelle ordreinnstillingene har alltid rangeringen null. Hvis du definerer nye salg, kjøp og lagerordreinnstillinger samtidig, anbefaler vi at du bruker **Detaljvisning** på siden **Standard ordreinnstillinger**. Hvis du vil bytte til detaljvisningen, kan du gå til **Alternativer** &gt; **Sidealternativer** &gt; **Endre visning** &gt; **Detaljvisning**.

### <a name="site-specific-order-settings"></a>Områdespesifikke ordreinnstillinger

Hvis du vil opprette områdespesifikke ordreinnstillinger, velger du **Ny**. I **Detaljvisning** angir du området i **Område**-feltet i delen **Innstillinger som kan brukes for**. I **Rutenettvisning** angir du området i **Område**-kolonnen. Den nye regelen tilordnes automatisk en ny rangeringsverdi som er over 0 (null). Du kan opprette så mange områdespesifikke regler du vil. Hvis du vil angi at de er like viktige, kan du tilordne den samme rangeringsverdien til alle områdespesifikke regler.

Hvis du er i **Detaljvisning**, får du ikke en oversikt over reglene som er opprettet for varen. Bruk knappen **Vis/skjul liste** for å se informasjon om oversikt. Når det opprettes en ordrelinje av hvilken som helst type og det ikke er angitt område for den, søker Supply Chain Management etter en regel uten angitt område. Dette bidrar til å bestemme et standardområde på ordrelinjen. Dette området brukes deretter til å søke etter en områdespesifikk regel der et standardlager kan ha blitt angitt. Dette lageret brukes for ordrelinjen.

### <a name="specific-order-settings-for-product-dimension"></a>Spesifikke ordreinnstillinger for produktdimensjon

Du kan definere regler for ordreinnstillinger for en aktiv produktdimensjon eller en kombinasjon av aktive produktdimensjoner. Hvis et produktdimensjonsfelt et tomt, gjelder regelen for alle verdier for produktdimensjonen. 

Tenk deg følgende eksempelprodukt:

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Produktnavn**                                    | Fotoelektrisk sensor                    |
| **Varenummer**                                     | XW56                                    |
| **Konfigurasjon** (brukes til å angi type lys) | C1-Synlig rødt lys, C2-infrarødt lys |
| **Versjon** | V1, V2, V3                              |

I dette eksemplet antas det at produktet er kjøpt og ikke produsert. Anta også at den vanligste konfigurasjonen er C1, slik at den er kortere leveringstider. 

Opprett følgende standard ordreinnstillinger for å angi dette scenariet.

| Rangering | Site | Konfigurasjon | Versjon | Kjøp – Overstyr standardinnstillinger | Leveringstid for innkjøp | Kjøp – Stoppet | Salg – Overstyr standardinnstillinger | Salg – Stoppet |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Ja                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Når en bestillingslinje eller en planlagt bestilling opprettes for vare XW56, konfigurasjon C1, uavhengig av versjonen eller området der linjen er plassert, vil leveringstiden være 2. Anta at alle versjoner i tillegg til V3 stoppes.

Du kan opprette reglene nedenfor for standard ordreinnstillinger.

| Rangering | Site | Konfigurasjon | Versjon | Kjøp – Overstyr standardinnstillinger | Leveringstid for innkjøp | Kjøp – Stoppet | Salg – Overstyr standardinnstillinger | Salg – Stoppet |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | V2    | Ja                                  |                    | Ja                | Ja                               | Ja             |
| 20   |      |               | V1    | Ja                                  |                    | Ja                | Ja                               | Ja             |
| 10   |      | C1            |       | Ja                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

De to reglene for å stoppe de gamle versjonene har samme rangering. De er derfor like viktige. Siden begge disse reglene har en høyere rangering enn regelen for konfigurasjonen C1, har de prioritet over regelen for konfigurasjonen C1. 

Dette eksemplet beskriver behovet for rangeringen. Hvis ragneringen ikke brukes, når det opprettes en bestilling for konfigurasjonen C1 og versjonen V2, er de to reglene som er definert for V2 og C1, tvetydige. Supply Chain Management løser denne tvetydigheten ved å søke gjennom reglene i synkende rekkefølge og bruke den første gjeldende regelen. Når det opprettes bestillingslinjer i gjeldende eksempel for konfigurasjon C1 og versjon V2, får brukeren en advarsel om at varen er sperret og at dette er forårsaket av versjonsverdien. Hvis regelen for konfigurasjonen hadde en høyere rang enn regelen for versjonen, ville en bestillingslinje blitt opprettet for konfigurasjon C1 og versjon V2, og ingen melding om sperret vare ville blitt gitt til brukeren. 

Tenk deg reglene nedenfor for standard ordreinnstillinger.

| Rangering | Site | Konfigurasjon | Versjon | Standardområde | Standardlager | Kjøp – Overstyr standard lagringsdimensjoner | Innkjøpslager |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Ja                                            | 22                 |
| 10   |      | C1            |  V2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Systemet går gjennom settet med regler to ganger for å finne området og lageret. Når det opprettes bestillingslinjer for konfigurasjon C1, versjon V2, bestemmes området basert på regelen med rangering 10. Deretter søker systemet etter en regel for område 2 for å finne et lager. Regel 20 blir funnet, og fordi den har en høyere rangering, vil lageret på bestillingslinjen være 22, ikke 21.

Som en generell veiledning vil spesifikke regler og regler for dimensjonene som er viktigere enn andre dimensjoner, få høyere rangering, mens mer generelle regler får lavere rangeringer. 

Regelen med rangeringen null fungerer som et sikkerhetsnett. Hvis ingen andre regler får treff, brukes standard ordreinnstillinger fra regel null. 

Siden rangeringsnummeret er viktig, finnes det i handlingsruten **Standard ordreinnstillinger** funksjoner for å flytte en regel opp eller ned og nummerere reglene, slik at de er alltid med økes med 10. 

Det kan opprettes mange regler for et frigitt produkt. Hvis du vil ha mer informasjon om hva hver enkelt regel overstyrer og hvorfor det er nødvendig, anbefaler vi at du bruker **Rutenettvisning** på siden **Standard ordreinnstillinger**. Du kan aktivere rutenettvisning ved å gå til **Alternativer** &gt; **Sidealternativer** &gt; **Endre visning** &gt; **Rutenettvisning**. Det kan vises svært mange kolonner i rutenettet, spesielt for kategoriene salg og lager. Hvis du vil begrense hvor mange kolonner som vises i rutenettet, kan grupper av kolonner skjules eller vises ved hjelp av knappene på menyen **Standard ordreinnstillinger** &gt; **Kolonnevisning**.

### <a name="specific-order-settings-for-released-product-variant"></a>Spesifikke ordreinnstillinger for frigitt produktvariant

Hvis regelsystemet for standard ordreinnstillinger er for tungvint, er det mulig å definere standard ordreinnstillinger for hver produktvariant. Eksemplet nedenfor viser hvordan det vil søke etter produktet og sakene som er beskrevet ovenfor.

| Rangering | Site | Konfigurasjon | Versjon | Kjøp – Overstyr standardinnstillinger | Leveringstid for innkjøp | Kjøp – Stoppet | Salg – Overstyr standardinnstillinger | Salg – Stoppet |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | V3    | Ja                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | V2    | Ja                                  | 5                  | Ja                | Ja                               | Ja             |
| 10   |      | C2            | V1    | Ja                                  | 5                  | Ja                | Ja                               | Ja             |
| 10   |      | C1            | V3    | Ja                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | V2    | Ja                                  | 2                  | Ja                | Ja                               | Ja             |
| 10   |      | C1            | V1    | Ja                                  | 2                  | Ja                | Ja                               | Ja             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Rangeringen i dette tilfellet har ingen betydning, slik at du kan velge å skjule den. Denne løsningen introduserer potensielt et vedlikeholdsproblem. Du bør imidlertid vurdere å bruke dette oppsettet Hvis du vil integrere med PLM-systemer (Product Lifecycle Management).

## <a name="use-strict-or-standard-validation-of-default-order-quantities"></a>Bruke streng eller standard validering av standard ordreantall

Du kan velge hvor streng systemet skal være ved validering av antall som er angitt i **Standard ordreinnstillinger** for et produkt. Når du bruker det nye strenge alternativet, må **Standard ordreantall** alltid være et multiplum av den angitte **Flere**-verdien for bestillinger, lager og salgsordrer. Hvis du bruker streng validering, vil du ikke kunne lagre standard ordreinnstillinger som ikke oppfyller dette kravet (og en feil vises i meldingsfeltet). 

Streng validering gjelder verdier for **Standard ordreantall** som er angitt på hurtigfanene **Bestilling**, **Lager** og **Salgsordre** på siden **Standard ordreinnstillinger**. Hver hurtigfane har sin egen **Flere**-innstilling, som brukes til å validere verdien for **Standard ordreantall** som er angitt for hurtigfanen.

### <a name="enable-the-strict-validation-option"></a>Aktivere det strenge valideringsalternativet

Før du kan bruke det strenge valideringsalternativet, må det være aktivert i systemet. Administratorer kan bruke siden [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis det er nødvendig. Her vises funksjonen som:

- **Modul** - *Behandling av produktinformasjon*
- **Funksjonsnavn** - *Streng validering for standard ordreantall*

### <a name="set-the-validation-option"></a>Angi valideringsalternativet

Slik angir du valideringsalternativet:

1. Gå til **Behandling av produktinformasjon \> Oppsett \> Parametere for produktinformasjonsbehandling**.
1. På **Generelt**-fanen angir du **Validering for standard ordreantall** til én av følgende verdier:
    - **Streng** – Velg dette alternativet for å sikre at alle verdier for **Standard ordreantall** vil være et multiplum av **Flere**-verdien for hver hurtigfane (**Bestilling**, **Lager** og **Salgsordre**).
    - **Standard** – Velg dette alternativet for å bruke standard validering (som fungerer på samme måte som når denne funksjonen ikke er aktivert).
