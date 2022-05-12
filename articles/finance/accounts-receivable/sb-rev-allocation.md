---
title: Inntektstildeling
description: Dette emnet forklarer hvordan du bruker inntektstildeling i Abonnementsfakturering.
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
ms.openlocfilehash: 2a1bdff364039c6bf0cdfbc11f0979398934c52c
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629454"
---
# <a name="revenue-allocation"></a>Inntektstildeling

Dette emnet forklarer hvordan du definerer inntektstildelingsparametere for en faktureringsplan. Du kan definere eller redigere inntektstildeling når du oppretter faktureringsplanen. Når du åpner siden **Inntektstildeling** for en aktiv eller avsluttet faktureringsplan, er feltene skrivebeskyttet.

## <a name="specify-the-revenue-allocation-for-a-billing-schedule"></a>Angi inntektstildelingen for en faktureringsplan

Hvis du vil angi inntektstildeling for en faktureringsplan, følger du trinnene nedenfor.

1. På listesiden **Alle/Aktive faktureringsplaner** velger du en faktureringsplan eller en faktureringsplanlinje.
2. Velg **Inntektstildeling** øverst på siden i fanen **Inntektstildeling**.
3. I feltet **Ordningstype for flere elementer** velger du ordningstypen for flere elementer (MEA)
4. I feltet **Ordningsnummer for flere elementer** angir du MEA-nummeret. I feltet **Konto for utsatt inntekt for kontrakt** angir du kontoen for utsatt inntekst for kontrakt.

    Hvis du setter feltet **Ordningstype for flere elementer** til **Enkelt**, vil det samme nummeret for verdiene **Ordningsnummer for flere elementer** og **Konto for utsatt inntekt for kontrakt** gjelde hver linje. Hvis du setter feltet **Ordningstype for flere elementer** til **Flere**, kan du angi ulike verdier for **Ordningsnummer for flere elementer** og **Konto for utsatt inntekt for kontrakt** for hver linje.
    
    Et MEA-nummer kan bare tildeles to eller flere varer. Én enkelt linje kan ikke ha et eget MEA-nummer.

5. Velg **Lagre**.

### <a name="fields"></a>Felt

Siden **Ordningstype for flere elementer** inneholder følgende felter.

| Felt | Beskrivelse |
|---|---| 
| Ordningstype for flere elementer | <p>Velg MEA-typen for transaksjonen:</p><ul><li>**Flere** – Linjeelementene på transaksjonen er del av MEA, eller det finnes mer enn én ordning.</li><li>**Ingen** – Transaksjonen er en standardtransaksjon som ikke har inntektstildeling.</li><li>**Enkelt** – Alle varene på transaksjonen er del av en enkelt MEA.</li></ul> |
| Ordningsnummer for flere elementer | <p>MEA-nummeret til linjen. Dette feltet er bare tilgjengelig når feltet **Ordningstype for flere elementer** er satt til **Flere**.</p><p>Hvis dette feltet er tomt, og du tildeler et MEA-nummer, oppdateres feltene **Frittstående salgsprisopprinnelse** og **Frittstående salgspris** automatisk basert på verdiene fra siden **Frittstående salgspris for vare**. Bare MEA-numrene som er tildelt andre linjer på salgsordren, er tilgjengelige.</p> |
| Konto for utsatt inntekt for kontrakt | Angi kontoen som skal brukes for journaloppføringer når en MEA-kontraktfaktura opprettes. Dette feltet er bare tilgjengelig når gjentakende kontraktsfakturering er brukt. |
| **Linjer** | |
| Variantnummer | Variantnummeret fra salgsordren. |
| Varenummer | Varenummeret fra salgsordren. |
| Faktureringshyppighet | Frekvensen for inntektstildeling: **Daglig**, **Månedlig**, **Kvartalsvis**, **Hvert halvår** eller **Årlig**. |
| Antall | Verdien kommer fra salgsordren. |
| Kontraktverdi | Kontraktverdien. |
| Ordningsnummer for flere elementer | <p>MEA-nummeret til linjen. Dette feltet er bare tilgjengelig når feltet **Ordningstype for flere elementer** er satt til **Flere**.</p><p>Hvis dette feltet er tomt, og du tildeler et MEA-nummer, oppdateres feltene **Frittstående salgsprisopprinnelse** og **Frittstående salgspris** automatisk basert på verdiene fra siden **Frittstående salgspris for vare**. Bare MEA-numrene som er tildelt andre linjer på salgsordren, er tilgjengelige. Hvis disse verdiene ikke er definert for varen, brukes verdiene fra siden **Parametere for inntektstildeling for flere elementer**.</p> | 
| Frittstående salgsprisopprinnelse | <p>Opprinnelsen for den frittstående salgsprisen:</p><ul><li>**Beløp** – Den frittstående salgsprisen er et beløp som du angir som er mer enn 0 (null). Beløpet konverteres mellom de funksjonelle og de opprinnelige valutaene etter behov.</li><li>**Basissalgspris** – Den frittstående salgsprisen samsvarer med varens basissalgspris.</li><li>**Fakturapris** – Den frittstående salgsprisen samsvarer med varens fakturapris.</li><li>**Prosent av vare** – Den frittstående salgsprisen er angitt som en prosentverdi, og beregnes på grunnlag av prisen på varen. Hvis du velger dette alternativet, må du angi standard prosentverdi.</li><li>**Tildel restbeløp** – Opprinnelsen til den frittstående salgsprisen blir beregnet som *total kontraktverdi for overordnet vare* – *total frittstående salgspris for underordnede varer*:</p><ul><li>*Total kontraktverdi for overordnet vare* er nettobeløpet eller det fakturerte beløpet.</li><li>*Total frittstående salgspris for underordnede varer* er summen av den utvidede eller kontraktmessige frittstående salgsprisen for alle underordnede varer, bortsett fra den underordnede varen som bruker denne frittstående salgsprisopprinnelsen.</li></ul><p>Hvis det beregnede beløpet er en negativ verdi, blir beløpet satt til 0 (null).</p><p>**Merk:** Dette alternativet kan bare velges for én underordnet vare i inntektsdelingen.</p></li><li>**Ingen** – Opprinnelsen til den frittstående salgsprisen er basert på de underordnede varene. Dette alternativet gjelder for varer som er definert som overordnede varer i en inntektsdelingsmal. Hvis det er merket av for **Inntektsdeling**, er dette alternativet automatisk valgt, og innstillingen kan ikke endres.</li><li>**Prosent av overordnet fakturapris** – Opprinnelsen til den frittstående salgsprisen er en prosent av fakturaprisen for den overordnede varen. Dette alternativet er bare tilgjengelig for underordnede varer i en mal for inntektsdeling.</li><li>**Prosent av overordnet standardpris** – Opprinnelsen til den frittstående salgsprisen er en prosent av standardprisen for den overordnede varen. Dette alternativet er bare tilgjengelig for underordnede varer i en mal for inntektsdeling. Når alternativet for en underordnet vare endres fra **Prosent av overordnet standardpris** til **Prosent av overordnet fakturapris**, eller fra **Prosent av overordnet fakturapris** til **Prosent av overordnet standardpris**, oppdateres også de beregnede verdiene.</li></ul> |
| Frittstående salgspris | <p>Den frittstående salgsprisen for linjen, i transaksjonsvalutaen.</p><p>Verdien i **Beløp**-feltet er enten angitt eller beregnet.</p> |
| Frittstående salgspris for kontrakt | Frittstående salgspris for kontrakt. |
| Restinntekt for kontrakt | Gjenværende inntektsbeløpet for kontrakten. Dette beløpet er summen av alle linjer som fakturaer ikke har blitt opprettet for ennå. |
| Inntekt for totalkontrakt | Det totale kontraktinntektsbeløpet for linjen. Dette beløpet er summen av alle linjer uavhengig av om fakturaer har blitt opprettet for dem. |
| Konto for utsatt inntekt for kontrakt | <p>Angi kontoen som skal brukes for journaloppføringer når en MEA-kontraktfaktura opprettes.</p><p>Dette feltet er bare tilgjengelig når gjentakende kontraktsfakturering er brukt.</p> |
| Feil | Eventuelle feil som oppstod for inntektstildeling. |

## <a name="use-revenue-allocation-on-a-sales-order"></a>Bruk inntektstildeling i en salgsordre

Følg denne fremgangsmåten for å bruke inntekststildelingsfunksjonaliteten på en salgsordre.

1. Opprett en salgsordre som har varer, på siden **Alle salgsordrer**.
2. Velg **Inntektstildeling** under **Inntektstildeling** i fanen **Faktura**.
3. I feltet **Ordningstype for flere elementer** velger du MEA-typen.
4. I feltet **Ordningsnummer for flere elementer** angir du MEA-nummeret.
5. Hvis feltet **Ordningstype for flere elementer** er satt til **Flere**, velger du linjene du ønsker, og velger deretter **Bruk på valgt**.
6. Velg **Lagre**.

Hvis du bruker inntekts- og utgiftsutsettelser, opprettes utsettelsesplanen automatisk. Du kan vise den på siden **Alle tidsplaner for utsettelse**.
