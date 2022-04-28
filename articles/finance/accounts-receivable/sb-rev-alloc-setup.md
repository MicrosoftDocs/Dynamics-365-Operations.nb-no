---
title: Definer inntektstildeling for flere elementer
description: Dette emnet beskriver hvordan du definerer parameterne for inntektstildeling for flere elementer i abonnementsfakturering.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: e422b16d1c4505b2837bb282918ecada902b806e
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2022
ms.locfileid: "8566364"
---
# <a name="set-up-multiple-element-revenue-allocation"></a>Definer inntektstildeling for flere elementer

Ved hjelp av inntektstildeling for flere elementer kan du definere ulike maler som brukes til å beregne og fordele inntekt på tvers av flere varer. Denne funksjonaliteten kan hjelpe deg å overholde Accounting Standards Codification Topic 606 (ASC 606) og/eller International Financial Reporting Standard 15 (IFRS 15).

## <a name="multiple-element-revenue-allocation-parameters"></a>Parametere for inntektstildeling for flere elementer

Bruk siden **Parametere for inntektstildeling for flere elementer** for å konfigurere parameterne for inntektstildeling for flere elementer.

### <a name="standalone-selling-price-origin"></a>Frittstående salgsprisopprinnelse

Feltet **Frittstående salgsprisopprinnelse** avgjør hvor den frittstående salgsprisen kommer fra. Du kan oppdatere verdien på siden **Frittstående salgspris for vare** og i transaksjonen. Følgende alternativer er tilgjengelige:

| Alternativ | Beskrivelse |
|--------|-------------|
| Beløp | Den frittstående salgsprisen er et beløp som du angir som er mer enn 0 (null). Beløpet konverteres mellom de funksjonelle og de opprinnelige valutaene etter behov. |
| Basissalgspris | Den frittstående salgsprisen samsvarer med varens basissalgspris. |
| Fakturapris | Den frittstående salgsprisen samsvarer med varens fakturapris. |
| Prosent av vare | Den frittstående salgsprisen er angitt som en prosentverdi, og beregnes på grunnlag av prisen på varen. Hvis du velger dette alternativet, må du angi standard prosentverdi. |
| Tildel restbeløp | <p>Opprinnelsen til den frittstående salgsprisen blir beregnet som *total kontraktverdi for overordnet vare* – *total frittstående salgspris for underordnede varer*:</p><ul><li>*Total kontraktverdi for overordnet vare* er nettobeløpet eller det fakturerte beløpet.</li><li>*Total frittstående salgspris for underordnede varer* er summen av den utvidede eller kontraktmessige frittstående salgsprisen for alle underordnede varer, bortsett fra den underordnede varen som bruker denne frittstående salgsprisopprinnelsen.</li></ul><p>Hvis det beregnede beløpet er en negativ verdi, blir beløpet satt til 0 (null).</p><p>**Merk:** Dette alternativet kan bare velges for én underordnet vare i inntektsdelingen.</p> |
| Ingen | Opprinnelsen til den frittstående salgsprisen er basert på de underordnede varene. Dette alternativet gjelder for varer som er definert som overordnede varer i en inntektsdelingsmal. Hvis det er merket av for **Inntektsdeling**, er dette alternativet automatisk valgt, og innstillingen kan ikke endres. |
| Prosent av overordnet fakturapris | Opprinnelsen til den frittstående salgsprisen er en prosent av fakturaprisen for den overordnede varen. Du kan endre standardverdien. Dette alternativet er bare tilgjengelig for underordnede varer i en mal for inntektsdeling. |
| Prosent av overordnet standardpris | Opprinnelsen til den frittstående salgsprisen er en prosent av standardprisen for den overordnede varen. Du kan endre standardverdien. Dette alternativet er bare tilgjengelig for underordnede varer i en mal for inntektsdeling. Dette er standardalternativet for underordnede varer. Når alternativet for en underordnet vare endres fra **Prosent av overordnet standardpris** til **Prosent av overordnet fakturapris**, eller fra **Prosent av overordnet fakturapris** til **Prosent av overordnet standardpris**, oppdateres også de beregnede verdiene. |

### <a name="account-for-revenue-allocation-rounding-differences"></a>Konto for avvik i avrunding for inntektstildeling

Feltet **Konto for avvik i avrunding for inntektstildeling** angir kontoen som brukes til å registrere alle avrundingsjusteringer til et kontraktinntektsbeløp. Den er tilgjengelig når gjentakende kontraktsfakturering brukes.

## <a name="item-standalone-selling-price"></a>Frittstående salgspris for vare

Bruk siden **Frittstående salgspris for vare** til å angi den opprinnelige og frittstående salgsprisen for en vare. Verdiene som angis på denne siden, brukes som standardverdier på siden **Inntektstildeling** i flere inntektsfordelingselementer og i gjentakende kontraktfakturering.

### <a name="specify-item-standalone-selling-price"></a>Angi frittstående salgspris for vare

Følg denne fremgangsmåten for å angi den frittstående prisen for en vare.

1. På siden **Frittstående salgspris for vare**, i feltet **Frittstående salgsprisopprinnelse**, velger du opprinnelsen til den frittstående salgsprisen.
2. Følg ett av disse trinnene, avhengig av verdien du valgte i feltet **Frittstående salgsprisopprinnelse**:

    * Hvis du valgte **Prosent av vare**, angir du prosenten i **Prosent**-feltet.
    * Hvis du valgte **Beløp**, angir du beløpet i feltet **Frittstående salgspris**.

2. Velg **Legg til** for hver vare du vil legge til i listen.
3. I feltet **Varekode** velger du varekoden. I feltet **Varerelasjon** velger du varerelasjonen. For varer der det ikke er merket av for **Inntektsdeling**, må den valgte kombinasjonen av en varekode og en varerelasjon være unik.
4. Endre standardverdien i feltet **Frittstående salgsprisopprinnelse**, **Frittstående salgspris** eller **Prosent** etter behov.
5. Velg **Legg til** for hver overordnede vare du vil legge til i listen.
6. I feltet **Varekode** velger du varekoden. I feltet **Varerelasjon** velger du varerelasjonen.
7. Merk av for **Inntektsdeling**.
8. I feltet **Varerelasjon** velger du varerelasjonen. Listen oppdateres med den overordnede varen og alle underordnede varer.
9. For den underordnede varen endrer du standardverdien i feltet **Frittstående salgsprisopprinnelse**, **Prosent av overordnet standardpris**, **Prosent av overordnet fakturapris** eller **Tildel restbeløp** etter behov.
10. Hvis du vil legge til flere varer samtidig, velger du **Legg til varer**.
11. Oppdater spørringen for å velge gruppen med varer du vil legge til.
12. Velg **OK**, gå gjennom listen med varer du har lagt til, og velg **OK**.

### <a name="fields"></a>Felt

Siden **Frittstående salgspris for vare** inneholder følgende felter.

| Felt | Beskrivelse |
|-------|-------------|
| Frittstående salgsprisopprinnelse | <p>Velg opprinnelsen for den frittstående salgsprisen:</p><ul><li>**Beløp** – Den frittstående salgsprisen er et beløp som du angir som er mer enn 0 (null). Beløpet konverteres mellom de funksjonelle og de opprinnelige valutaene etter behov.</li><li>**Basissalgspris** – Den frittstående salgsprisen samsvarer med varens basissalgspris.</li><li>**Fakturapris** – Den frittstående salgsprisen samsvarer med varens fakturapris.</li><li>**Prosent av vare** – Den frittstående salgsprisen er angitt som en prosentverdi, og beregnes på grunnlag av prisen på varen. Hvis du velger dette alternativet, må du angi standard prosentverdi.</li></ul>**Tildel restbeløp** – Opprinnelsen til den frittstående salgsprisen blir beregnet som *total kontraktverdi for overordnet vare* – *total frittstående salgspris for underordnede varer*:</p><ul><li>*Total kontraktverdi for overordnet vare* er nettobeløpet eller det fakturerte beløpet.</li><li>*Total frittstående salgspris for underordnede varer* er summen av den utvidede eller kontraktmessige frittstående salgsprisen for alle underordnede varer, bortsett fra den underordnede varen som bruker denne frittstående salgsprisopprinnelsen.</li></ul><p>Hvis det beregnede beløpet er en negativ verdi, blir beløpet satt til 0 (null).</p><p>**Merk:** Dette alternativet kan bare velges for én underordnet vare i inntektsdelingen.</p></li><li>**Ingen** – Opprinnelsen til den frittstående salgsprisen er basert på de underordnede varene. Dette alternativet gjelder for varer som er definert som overordnede varer i en inntektsdelingsmal. Hvis det er merket av for **Inntektsdeling**, er dette alternativet automatisk valgt, og innstillingen kan ikke endres.</li><li>**Prosent av overordnet fakturapris** – Opprinnelsen til den frittstående salgsprisen er en prosent av fakturaprisen for den overordnede varen. Du kan endre standardverdien. Dette alternativet er bare tilgjengelig for underordnede varer i en mal for inntektsdeling.</li><li>**Prosent av overordnet standardpris** – Opprinnelsen til den frittstående salgsprisen er en prosent av standardprisen for den overordnede varen. Du kan endre standardverdien. Dette alternativet er bare tilgjengelig for underordnede varer i en mal for inntektsdeling. Dette er standardalternativet for underordnede varer. Når alternativet for en underordnet vare endres fra **Prosent av overordnet standardpris** til **Prosent av overordnet fakturapris**, eller fra **Prosent av overordnet fakturapris** til **Prosent av overordnet standardpris**, oppdateres også de beregnede verdiene.</li></ul> |
| Frittstående salgspris | Angi den frittstående salgsprisen for varen. Dette feltet er tilgjengelig når feltet **Frittstående salgsprisopprinnelse** er satt til **Beløp**. |
| Prosent | Angi prosentverdien for den frittstående salgsprisen. Dette feltet er tilgjengelig når feltet **Frittstående salgsprisopprinnelse** er angitt til **Prosent av vare**, **Prosent av overordnet fakturapris** eller **Prosent av overordnet standardpris**. |
| Inntektsdeling | <p>Angi om en linje bruker inntektsdeling:</p><ul><li>**Valgt** – Bare varer som en mal for inntektsdeling er definert for, kan velges i **Varerelasjon**-feltet. Du kan bare merke av i denne boksen for overordnede varer i en mal for inntektsdeling.</li><li>**Ikke merket** – Varen er en standardvare som ikke bruker inntektsdeling.</li></ul> |
| Relasjon | Et symbol angir om varen er en overordnet eller underordnet vare i en inntektsdeling. |
| Varekode | <p>Velg varekoden: **Tabell** eller **Gruppe**.</p><p>Hvis det er merket av for **Inntektsdeling**, er dette feltet satt til **Tabell**, og verdien kan ikke endres.</p> |
| Varerelasjon | <p>Velg et varenummer.</p><p>Hvis det er merket av for **Inntektsdeling**, er bare varer som er overordnede varer som en inntektsdelingsmal er definert for, tilgjengelige for valg. Når den overordnede varen er valgt, oppdateres listen automatisk med de underordnede varene til denne overordnede varen.</p> |
| Overordnet vare | For den overordnede varen viser dette feltet varenummeret. For underordnede varer i en inntektsdeling viser dette varenummeret til den overordnede varen. |

## <a name="mea-templates"></a>MEA-maler

Bruk siden **MEA-maler** til å opprette og redigere ID-er for MEA-maler (ordning for flere elementer). Disse ID-ene brukes på siden **Inntektstildeling** for å gruppere varer sammen.

### <a name="create-a-template"></a>Opprett en mal

Hvis du vil konfigurere en MEA-mal, følger du fremgangsmåten nedenfor.

1. Velg **Ny** på siden **MEA-maler**.
1. I feltet **ID for MEA-mal** angir du en unik ID.
1. Angi en beskrivelse i **Beskrivelse**-feltet.
1. I feltet **Konto for utsatt inntekt for kontrakt** velger du kontoen du vil bruke til journaloppføringer når en MEA-kontraktfaktura opprettes. Dette feltet er tilgjengelig når gjentakende kontraktsfakturering er aktivert og brukt.
1. Velg **Lagre**.
