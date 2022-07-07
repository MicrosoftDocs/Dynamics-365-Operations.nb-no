---
title: Regnskapsprinsippet Postere i belastningskonto
description: Denne artikkelen gir en oversikt over regnskapsprinsippet Postere i belastningskonto.
author: rachel-profitt
ms.date: 05/02/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-02
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: c03109baaa341b25af70840b791ddf04f692fb1a
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016572"
---
# <a name="post-to-charge-account-accounting-principle"></a>Regnskapsprinsippet Postere i belastningskonto

Regnskapsprinsippet *postere i belastningskonto* lar deg gjøre rede for og lettere avstemme eventuelle avvik i enhetsprisen mellom en fysisk postering og økonomisk postering, indirekte kostnader for kjøpte varer eller tillegg i en bestilling.

To konfigurasjoner for tilleggskoder for leverandører på **Tilleggskode**-siden (**Leverandører \> Oppsett for tillegg \> Tilleggskode**) kan føre til at en bestilling påvirker vurderingen av lageraktiva:

- Når det gjelder tilleggskoder der **Debettype**-feltet er satt til *Vare* og **Kredittype**-feltet er satt til *Finanskonto*, fungerer finanskontoen som er valgt som absorberingskonto, som en lageravvikskonto.
- Når det gjelder tilleggskoder der **Debettype**-feltet er satt til *Vare* og **Kredittype**-feltet er satt til *Kunde/leverandør*, regnes tillegget som materialkostnad, og lageravvikskontoen for varen brukes.

## <a name="european-special-accounting-rule"></a>Spesiell europeisk regnskapsregel

I Europa brukes ofte regnskapsprinsippet *postere i belastningskonto* til å ta med med en spesiell regnskapsregel. Én av metodene nedenfor brukes for eksempel vanligvis til å gjøre rede for lagerendringer:

- **Metoden Kostnad for salg** – Standardkonfigurasjonen for lagerposteringsprofilen støtter denne metoden. Regnskapsprinsippet *postere i belastningskonto* kreves ikke.
- **Utgiftstypemetoden** – Mindre organisasjoner bruker ofte denne metoden. Det omfatter vanligvis følgende trinn:

    1. Varer eller tjenester utgiftsføres fullstendig ved mottak.
    2. Det utføres en syklustelling på slutten av perioden.
    3. Det utføres en manuell justering for antallet og verdien posteres i lageret. (Motkontoen er en lageravvikskonto som utligner utgiften som ble postert i trinn 1. Derfor vises variasjonen i lagerverdien bare på denne kontoen.)

Prinsippet *postere i belastningskonto* lar deg automatisere de to posteringene fullstendig. Dermed kan du eliminere en manuell justeringspostering for periodeavslutning.

## <a name="enable-the-post-to-charge-account-accounting-principle"></a>Aktivere regnskapsprinsippet Postere i belastningskonto

Følg trinnene nedenfor for å aktivere regnskapsprinsippet *postere i belastningskonto*.

1. Gå til **Leverandører \> Oppsett \> Leverandørparametere**.
2. Angi *Ja* for alternativet **Postere i belastningskonto i finans** i hurtigfanen **Faktura** i **Faktura**-fanen.
3. Lukk siden.

## <a name="prerequisites-and-recommended-parameters-for-the-post-to-charge-account-accounting-principle"></a>Forutsetninger og anbefalte parametere for regnskapsprinsippet Postere i belastningskonto

Hvis du planlegger å gjøre rede for innkjøpstillegg og lageravvik, må følgende forutsetninger være på plass:

- *Ja* må være angitt for alternativet **Postere i belastningskonto i finans** i **Faktura**-fanen på siden **Leverandørparametere** (**Leverandører \> Oppsett \> Leverandørparametere**).
- *Ja* må være angitt for alle følgende alternativer for hver relevante modellgruppe som inneholder varer som er inkludert i en bestilling, på siden **Varemodellgrupper** (**Kostnadsstyring \> Oppsett for regnskapspolicyer for beholdning \> Varemodellgrupper**):

    - Poster aktuell beholdning
    - Poster økonomisk lager
    - Gjeldsavsetning på mottaksseddel

- *Ja* må være angitt for alternativet **Generer tillegg på produktkvittering** i **Levering**-fanen på siden **Parametere for innkjøp og leverandører** (**Innkjøp og leverandører \> Oppsett \> Parametere for innkjøp og leverandører**).
- *Ja* må være angitt for alternativet **Poster følgeseddel i finans** i **Lagerregnskap**-fanen på siden **Parametere for beholdnings- og lagerstyring** (**Lagerstyring \> Oppsett \> Parametere for beholdnings- og lagerstyring**).
- Hovedkontoer som gjelder for hver relevante vare må være angitt for hver av de følgende posteringstypene i **Bestilling**-fanen på **Postering**-siden (**Lagerstyring \> Oppsett \> Postering \> Postering**):

    - Innkjøpsutgift, ikke-fakturert
    - Innkjøpsutgift for produktet
    - Lageravvik

## <a name="example-scenario-1-change-in-unit-cost-price"></a>Eksempelscenario 1: endring i enhetskostpris

Dette eksempelscenarioet har følgende forutsetninger:

- Etterkalkuleringsmodellen først inn, først ut (FIFO)

Fremgangsmåten nedenfor gir et eksempel på hva som skjer når du endrer enhetskostprisen på en bestilling.

1. Opprett en bestilling for et antall på 1 av en vare som har en enhetspris på 100,00.
2. Bekreft bestillingen.
3. Poster produktkvitteringen for bestillingen.
4. Valider bilaget på produktkvitteringen. Følgende tabell viser et eksempelbilag.

    | Posteringstype | Hovedkonto | Navn på hovedkonto | Kontotype | Debet/kredit? | Avregningskonto | Fysisk/økonomisk? | Beløp |
    |---|---|---|---|---|---|---|---|
    | Innkjøp, lageravvik | 600170 | Lageravviksmaterialer | Utgift | Kreditt | Nei | Fysisk | -100,00 |
    | Kostnad for innkjøpte materialer mottatt | 140100 | Materiallager | Objekt | Debet | Ja | Fysisk | 100.00 |
    | Innkjøpsutgift, ikke-fakturert | 600180 | Materialmottak | Utgift | Debet | Ja | Fysisk | 100.00 |
    | Innkjøp, avsetning | 200140 | Påløpte innkjøp | Gjeld | Kreditt | Ja | Fysisk | -100,00 |

5. Poster fakturaen for bestillingen som har en oppdatert enhetspris på 110,00.
6. Valider bilaget på fakturaen. Følgende tabell viser et eksempelbilag.

    | Posteringstype | Hovedkonto | Navn på hovedkonto | Kontotype | Debet/kredit? | Avregningskonto | Fysisk/økonomisk? | Beløp |
    |---|---|---|---|---|---|---|---|
    | Innkjøp, lageravvik | 600170 | Lageravviksmaterialer | Utgift | Kreditt | Nei | Økonomisk | -10,00 |
    | Kostnad for innkjøpte materialer mottatt | 140100 | Materiallager | Objekt | Debet | Ja | Økonomisk | -100,00 |
    | Innkjøpsutgift, ikke-fakturert | 600180 | Materialmottak | Utgift | Debet | Ja | Økonomisk | -100,00 |
    | Innkjøp, avsetning | 200140 | Påløpte innkjøp | Gjeld | Kreditt | Ja | Økonomisk | 100.00 |
    | Kostnad for innkjøpte materialer fakturert | 140100 | Materiallager | Objekt | Debet | Nei | Økonomisk | 110.00 |
    | Innkjøpsutgift for produktet | 600180 | Materialmottak | Utgift | Kreditt | Nei | Økonomisk | 110.00 |
    | Leverandørsaldo | 211000 | Leverandørhandel | Gjeld | Kreditt | Nei | Økonomisk | -110,00 |

## <a name="example-2-charges-and-indirect-costs-on-the-purchase-order"></a>Eksempel 2: tillegg og indirekte kostnader på bestillingen

Dette eksempelscenarioet har følgende forutsetninger:

- Etterkalkuleringsmodellen FIFO
- **Tilleggskode 1:** Debiter vare og krediter finanskonto for 10 %
- **Tilleggskode 2:** Debiter vare og krediter kunde/leverandør for 10,00 proporsjonalt
- **Indirekte kostnad:** 2,00 % lagt til kjøpsprisen

Fremgangsmåten nedenfor gir et eksempel på hva som skjer når du endrer tar med tillegg og indirekte kostnader på en bestilling.

1. Opprett en bestilling for et antall på 1 av en vare som har en enhetspris på 100,00.
2. Legg til en tilleggskode på 10 prosent som debiterer varen og krediterer finans.
3. Legg til en tilleggskode på 10,00 som debiterer varen og krediterer kunden/leverandøren.
4. Tildel tilleggene til bestillingslinjene.
5. Bekreft bestillingen.
6. Poster produktkvitteringen for bestillingen.
7. Valider bilaget på produktkvitteringen. Følgende tabell viser et eksempelbilag.

    | Posteringstype | Hovedkonto | Navn på hovedkonto | Kontotype | Debet/kredit? | Avregningskonto | Fysisk eller økonomisk | Beløp |
    |---|---|---|---|---|---|---|---|
    | Innkjøp, lageravvik | 600170 | Lageravviksmaterialer | Utgift | Kreditt | Nei | Fysisk | -110,00 |
    | Estimert indirekte kostnad absorbert | 600520 | Absorberte indirekte kostnader | Utgift | Kreditt | Ja | Fysisk | -2,40 |
    | Innkjøpsfrakt | 600120 | Freight-/transportkostnader | Utgift | Kreditt | Nei | Fysisk | -10,00 |
    | Kostnad for innkjøpte materialer mottatt | 140100 | Materiallager | Objekt | Debet | Ja | Fysisk | 122.40 |
    | Innkjøpsutgift, ikke-fakturert | 600180 | Materialmottak | Utgift | Debet | Ja | Fysisk | 110.00 |
    | Innkjøp, avsetning | 200140 | Påløpte innkjøp | Gjeld | Kreditt | Ja | Fysisk | -110,00 |

8. Poster fakturaen for bestillingen.
9. Valider bilaget på fakturaen. Følgende tabell viser et eksempelbilag.

    | Posteringstype | Hovedkonto | Navn på hovedkonto | Kontotype | Debet/kredit? | Avregningskonto | Fysisk/økonomisk? | Beløp |
    |---|---|---|---|---|---|---|---|
    | Innkjøp, lageravvik | 600170 | Lageravviksmaterialer | Utgift | Kreditt | Nei | Økonomisk | 0.00 |
    | Estimert indirekte kostnad absorbert | 600520 | Absorberte indirekte kostnader | Utgift | Debet | Ja | Økonomisk | 2.40 |
    | Indirekte kostnad absorbert | 600520 | Absorberte indirekte kostnader | Utgift | Debet | Nei | Økonomisk | -2,40 |
    | Kostnad for innkjøpte materialer mottatt | 140100 | Materiallager | Objekt | Kreditt | Ja | Økonomisk | -110,00 |
    | Innkjøpsutgift, ikke-fakturert | 600180 | Materialmottak | Utgift | Kreditt | Ja | Økonomisk | -110,00 |
    | Innkjøp, avsetning | 200140 | Påløpte innkjøp | Gjeld | Debet | Ja | Økonomisk | 110.00 |
    | Kostnad for innkjøpte materialer fakturert | 140100 | Materiallager | Objekt | Debet | Nei | Økonomisk | 110.00 |
    | Innkjøpsutgift for produktet | 600180 | Materialmottak | Utgift | Kreditt | Nei | Økonomisk | 110.00 |
    | Leverandørsaldo | 211000 | Leverandørhandel | Gjeld | Kreditt | Nei | Økonomisk | -110,00 |
