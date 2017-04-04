---
title: "Beregninger for produktmodeller for konfigurasjon av vanlige spørsmål"
description: Denne artikkelen beskriver beregninger for produktmodeller for konfigurasjon og forklarer hvordan du bruker beregninger med begrensninger.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3d02a15387231160f5b8a237aa11008b91ef1223
ms.openlocfilehash: 3a82fdb8532c79e33c167c43554a3de7d3061fcb
ms.lasthandoff: 03/31/2017


---

# <a name="calculations-for-product-configuration-models-faq"></a>Beregninger for produktmodeller for konfigurasjon av vanlige spørsmål

Denne artikkelen beskriver beregninger for produktmodeller for konfigurasjon og forklarer hvordan du bruker beregninger med begrensninger.

Beregninger kan brukes for aritmetiske eller logiske operasjoner. De supplerer uttrykksbegrensninger i produktkonfigurasjonsmodeller. Du kan definere beregninger på **Detaljer om restriksjonsbasert produktkonfigurasjonsmodell** siden, og deretter lage uttrykk for beregningene i redigeringsprogrammet for uttrykk. Hvis du vil ha mer informasjon, se Opprett beregninger.

## <a name="what-is-a-calculation"></a>Hva er en beregning?
En beregning er et element som du kan bruke i en produktkonfigurasjonsmodell. Beregninger supplerer betingelser ved å la deg bruke desimaltall til å beregne verdier når du konfigurerer et produkt. Beregninger har dessuten et større sett med tilgjengelige operatorer enn det begrensninger har.  

En beregning er på samme måte som en betingelse tilknyttet en bestemt komponent i en produktkonfigurasjonsmodell, og den kan ikke brukes på nytt eller deles med en annen komponent. Én viktig forskjell mellom beregninger og begrensninger er at beregningene er imperative (enveis), mens begrensninger er deklarative (toveis). Hvis du vil ha mer informasjon om begrensninger, se [Uttrykksbegrensninger og tabellbegrensninger](expression-constraints-table-constraints-product-configuration-models.md).  

En beregning består av et målattributt og et beregningsuttrykk.

## <a name="what-is-a-target-attribute"></a>Hva er et målattributt?
Et målattributt er et attributt som mottar resultatet av beregningsuttrykk.  

I følgende uttrykk er målattributtet er et mål for en bordduk:  

**Uttrykk:** Hvis\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]  

**DecimalAttribute1** er lengden på definisjonstabellen til og **decimalAttribute2** er duk lengden. Uttrykket returnerer verdien **True** til målattributtet hvis **decimalAttribute2** er større enn eller lik **decimalAttribute1**. Hvis ikke, returnerer uttrykket verdien **False**. Dukmålingen er derfor akseptabel hvis duklengden er lik eller overskrider bordlengden.

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a>Hvilke attributtyper kan angis for målattributter?
Alle attributtyper som produktkonfiguratoren støtter, kan settes til målattributter unntatt tekst uten en fast liste.

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a>Kan verdien for et målattributt begrense verdiene for inndataattributtene i en beregning?
Nei, verdien for et målattributt kan ikke begrense verdiene for inndataattributtene fordi beregningene er enveis. Derfor angis verdien på Målattributtet basert på endringer i verdien for inndataattributtene, men en endring i verdien for målet har ikke innvirkning på verdien av inndataattributtene. Denne virkemåten er forskjellig fra virkemåten for begrensninger. Begrensninger forekommer i begge retninger.

### <a name="example"></a>Eksempel

Målet for beregningen er lengden på en strømkabel og inndataverdien er en farge i følgende uttrykk:  

**Uttrykk:**\[Hvis fargen == "Grønn", 1.5, 1.0\]  

Når du konfigurerer varen, lengden på strømledningen er satt til **1.5** Hvis du angir **grønn** som verdi for farge-attributtet. Hvis du angir en annen farge, er angis lengden som **1,0**. Men siden beregningene er enveis, setter ikke beregningen verdien for fargeattributtet til **grønt** når du angir en lengde på **1,5**.

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a>Hva skjer hvis en beregning er et målattributt av heltallstypen, men en beregning genererer et desimaltall?
Hvis et målattributt er av heltallstypen, men en beregning genererer et desimaltall, returneres bare heltallsverdien for det beregnede resultatet. Desimaldelen fjernes, og resultatet avrundes ikke. Resultatet 12,70 vises for eksempel som 12.

## <a name="when-do-calculations-occur"></a>Når forekommer det beregninger?
Beregninger skjer når alle inndataattributter har fått en verdi.

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a>Kan jeg skrive over verdien som er beregnet for målattributtet?
Du kan overskrive verdien som beregnes for målattributtet, med mindre målattributtet er angitt som skjult eller skrivebeskyttet.

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-readonly"></a>Hvordan angir jeg en Målattributtet skjult eller readonly?
Hvis du vil angi et attributt som skjulte eller skrivebeskyttet, gjør du følgende.

1.  Klikk **produktinformasjonsbehandling**&gt;**vanlige**&gt;**produktkonfigurasjonsmodeller**.
2.  Velg en produktkonfigurasjonsmodell, og deretter på handlingsruten klikker du **Rediger**.
3.  På siden **Detaljer om restriksjonsbasert produktkonfigurasjonsmodell** velger du attributtet som skal brukes som et målattributt.
4.  På **Attributter** hurtigkategorien, velg **Skjult** eller **Skrivebeskyttet**.

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a>Kan en beregning overskrive verdiene som jeg angir?
Nr. Verdiene du angir når du konfigurerer et produkt, er verdiene som brukes. Beregningen som skjer når inndataverdiene i en beregning endres, kan ikke overskrive verdiene du angir for et spesifikt attributt.

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a>Hva skjer hvis jeg fjerner en inndataverdi i en beregning?
Hvis du fjerner en inndataverdi i en beregning, fjernes også verdien for målattributtet.

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a>Hvorfor mottar jeg en feilmelding om at modellen er i konflikt?
Denne meldingen vises når en beregning inneholder en feil eller når en selvmotsigelse finnes i én eller flere begrensninger. Hvis du vil ha mer informasjon om konflikter i begrensninger, se [Uttrykksbegrensninger og tabellbegrensninger](expression-constraints-table-constraints-product-configuration-models.md). Her er noen situasjoner hvor det kan oppstå feil i beregninger:

-   En verdi er delt på 0 (null).
-   En konflikt finnes mellom følgende to elementer:
    -   Verdiene som er tilgjengelige for et attributt, og som er begrenset av en begrensning
    -   En verdi som genereres av en beregning
-   Verdiene som returneres av beregningen, er utenfor domenet for attributtet. Et eksempel er et heltall fra \[1..10\] som er beregnet til 0.

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a>Hvorfor mottar jeg en feilmelding selv om jeg validerte produktmodellen min uten problemer?
Beregninger er ikke inkludert i valideringen. Du må teste produktkonfigurasjonsmodellen for å finne feil i beregninger. Følgende trinn forklarer hvordan du tester en produktkonfigurasjonsmodell.

1.  Klikk **produktinformasjonsbehandling**&gt;**vanlige**&gt;**produktkonfigurasjonsmodeller**.
2.  Velg en produktkonfigurasjonsmodell, og deretter på handlingsruten, i gruppen **Kjør** klikker du **Test**.



