---
title: "Opprette leverandørbetalinger ved hjelp av et betalingsforslag"
description: Dette emnet gir en oversikt over alternativer for betalingsforslag og inneholder noen eksempler som viser hvordan betalingsforslag fungerer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 04/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14312
ms.assetid: 585d5b0b-1b79-4a03-ab18-528918070377
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5afdace14d1db4b36027634b3af3df1029ae12a2
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="create-vendor-payments-by-using-a-payment-proposal"></a>Opprette leverandørbetalinger ved hjelp av et betalingsforslag

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over alternativer for betalingsforslag og inneholder noen eksempler som viser hvordan betalingsforslag fungerer. Betalingsforslag brukes ofte til å opprette leverandørbetalinger fordi spørringen kan brukes til å raskt velge leverandørfakturaer for betaling, basert på kriterier som forfallsdato og kontantrabatt. 

Organisasjoner bruker ofte betalingsforslag til å opprette leverandørbetalinger fordi betalingsforslagsspørringen kan brukes til å raskt velge leverandørfakturaer for betaling, basert på forfallsdatoen, kontantrabatten og andre kriterier. 

Betalingsforslagsspørringen inneholder ulike kategorier, der hver har ulike alternativer for å velge fakturaer som skal betales. **Parameter**-kategorien inneholder alternativer som et flertall av organisasjonen ofte bruker. På hurtigfanen **Poster som skal inkluderes** kan du angi hvilke fakturaer eller leverandører som skal inkluderes for betaling ved å definere områder for ulike egenskaper. Hvis du for eksempel ønsker å betale et bestemt område av leverandører, kan du definere et filter for leverandørområdet. Denne funksjonaliteten brukes ofte til å velge fakturaer for en bestemt betalingsmåte. Hvis du for eksempel definerer et filter der **Betalingsmåte** = **Sjekk**, velges bare fakturaer som har denne betalingsmåten for betaling, forutsatt at de også oppfyller andre vilkår som er angitt i spørringen. **Avanserte parametere**-kategorien inneholder flere alternativer, der kanskje ikke alle er relevante for organisasjonen. Denne kategorien inneholder for eksempel alternativer for å betale fakturaer for sentraliserte betalinger.

## <a name="parameters"></a>Parametere
-   **Velg fakturaer etter** – Fakturaer innenfor datointervallet som er angitt av feltene **Fra dato** og **Til dato**, kan velges etter forfallsdato, kontantrabattdato eller begge deler. Hvis du bruker kontantrabattdatoen, søker systemet etter fakturaer som har en kontantrabattdato mellom Fra dato og Til dato. Systemet bestemmer deretter om fakturaen er kvalifisert for kontantrabatt ved hjelp av øktdatoen, for å være sikker på at kontantrabattdatoen ikke allerede er passert.
-   **Fra dato** og **Til dato** – Fakturaer som har en forfallsdato eller kontantrabattdato innenfor dette datointervallet, velges for betaling.
-   **Minste betalingsdato** – Angi minste betalingsdato. Feltene **Fra dato** og **Til dato** angir for eksempel et område fra 1. september til 10. september, og den minste betalingsdatoen er 5. september. I dette tilfellet har alle fakturaer med forfallsdato fra 1. september til 5. september, betalingsdatoen for 5. september. Alle fakturaer med forfallsdato fra 5. september til 10. september har imidlertid en betalingsdato som er lik forfallsdatoen for hver faktura.
-   **Beløpsgrense** – Angi maksimalt totalbeløp for alle betalinger.
-   **Opprett betalinger uten forhåndsvisning av faktura** – Hvis du setter alternativet til **Ja**, opprettes betalinger umiddelbart på **Leverandørbetalinger**-siden. **Betalingsforslag**-siden utelates. Derfor opprettes betalinger raskere. Betalinger kan fremdeles endres på **Leverandørbetalinger**-siden. Du kan også gå tilbake til **Betalingsforslag**-siden ved hjelp av knappen **Rediger fakturaer for valgt betaling**.

## <a name="advanced-options"></a>Avanserte alternativer
- **Kontroller leverandørsaldo** – Hvis dette alternativet er satt til **Ja**, kontroller systemet at en leverandør ikke har en debetsaldo før en faktura betales. Hvis en leverandør har en debetsaldo, opprettes ingen betaling. Leverandøren kan for eksempel ha kreditnotaer og betalinger som er postert, men ennå ikke er utlignet. I så fall skal leverandøren ikke betales. I stedet må kreditnotaene eller betalingene utlignes mot de utestående fakturaene.
- **Slett negative betalinger** – Dette alternativet fungerer forskjellig, avhengig av om betalingene er for enkeltvise fakturaer eller summen av fakturaer som oppfyller betalingskriteriene. Dette er definert i betalingsmåten.
- **Betaling for hver faktura** – Hvis alternativet **Slett negative betalinger** er satt til **Ja**, og det finnes en ikke utlignet faktura og betaling for en leverandør, velges bare fakturaen for betaling. Den eksisterende betalingen utlignes ikke mot fakturaen. Hvis alternativet **Slett negative betalinger** er satt til **Nei**, og en faktura og en betaling ikke er utlignet, velges både fakturaen og betalingen for betaling. Det opprettes en betaling for betalingen, og en refusjon (negativ betaling) opprettes for betalingen.
- **Betaling for summen av fakturaer** – Hvis alternativet **Slett negative betalinger** er satt til **Ja**, og det finnes en ikke utlignet faktura og betaling for en leverandør, velges både den ikke utlignede fakturaen og betalingen for betaling og beløpene legges sammen, som gir det totale betalingsbeløpet. Unntak oppstår bare hvis summen resulterer i en refusjon. I så fall velges verken fakturaen eller betalingen. Hvis alternativet **Slett negative betalinger** er satt til **Nei**, og en faktura og betaling ikke er utlignet, velges både fakturaen og betalingen for betaling og beløpene legges sammen, som gir totalt betalingsbeløp.
- **Skriv bare ut rapport** – Sett dette alternativet til **Ja** hvis du vil se resultatene av betalingsforslaget i en rapport, men uten å opprette betalinger.
- **Inkluder leverandørfakturaer fra andre juridiske enheter** – Hvis organisasjonen har en sentralisert prosess for betaling, og betalingsforslaget må inneholde fakturaer fra andre juridiske enheter som er inkludert i søkekriteriene, setter du dette alternativet til **Ja**.
- **Foreslå separat leverandørbetaling per juridisk enhet** – Hvis dette alternativet settes til **Ja**, opprettes det en egen betaling for hver juridiske enhet per leverandør. Leverandøren på betalingen er leverandøren fra fakturaen fra hver juridiske enhet. Hvis dette alternativet settes til **Nei**, og den samme leverandøren har fakturaer i flere juridiske enheter, opprettes det én betaling for det samlede beløpet for de valgte fakturaene. Leverandøren på betalingen er leverandøren i den gjeldende juridiske enheten. Hvis leverandørkontoen ikke eksisterer i den gjeldende juridiske enheten, brukes leverandørkontoen for den første fakturaen som skal betales.
- **Betalingsvaluta** – dette feltet angir valutaen som alle betalinger er opprettet i. Hvis det ikke er definert en valuta, betales hver faktura i valutaen på fakturaen.
- **Betalingsukedag** – Angi ukedagen som betalingen skal utføres på. Dette feltet brukes bare hvis betalingsmetoden er definert for å summere fakturaer for betaling på en bestemt dag i uken.
- **Motkontotype** og **Motkonto** – angi disse feltene til å definere en bestemt kontotype (som **Finans** eller **Bank**) og motkonto (for eksempel en bestemt bankkonto). Betalingsmåten for fakturaen definerer standard motkontotype og motkonto, men du kan bruke disse feltene til å overstyre standardverdiene.
- **Dato for summert betaling** – Dette brukes bare når feltet **Periode** i valgt betalingsmåten er satt til **Total**. Hvis en dato er definert, opprettes alle fakturaer på denne datoen. Feltet **Minste betalingsdato** ignoreres.
- **Flere filtre** – I hurtigfanen **Poster som skal inkluderes** kan du definere flere kriterieområder. Hvis du for eksempel ønsker å betale et område av leverandører, kan du definere et filter for leverandørområdet. Denne funksjonaliteten brukes ofte til å velge fakturaer for en bestemt betalingsmåte. Hvis du for eksempel definerer et filter der **Betalingsmåte** = **Sjekk**, velges bare fakturaer som har denne betalingsmåten for betaling, forutsatt at de også oppfyller andre vilkår som er angitt i spørringen.

## <a name="scenarios"></a>Scenarier

| Leverandør | Faktura | Fakturadato | Fakturabeløp | Forfallsdato | Kontantrabattdato | Kontantrabattbeløp |
|--------|---------|--------------|----------------|----------|--------------------|----------------------|
| 3050   | 1001    | 15. juni      | 500,00         | 15. juli  | 29. juni            | 10,00                |
| 3050   | 1 002    | 20. juni      | 600,00         | 20. juli  | 4. juli             | 12.00                |
| 3075   | 1003    | 15. juni      | 250,00         | 29. juni  |                    | 0,00                 |
| 3100   | 1004    | 17. juni      | 100,00         | 17. juli  | 1. juli             | 1,00                 |

1. juli betaler April leverandører. Hun bruker et betalingsforslag for å fullføre denne oppgaven mer effektivt.

### <a name="option-1-by-cash-discount"></a>Alternativ 1: Etter kontantrabatt

April velger **kontantrabatt** som forslag. Hun skriver inn datoområdet 26. juni til 10. juli. Følgende fakturaer inkluderes i forslaget:

-   1002, fordi rabattdatoen 4. juli er i betalingsdatoområdet.
-   1004, fordi rabattdatoen 1. juli er i betalingsdatoområdet.

Følgende fakturaer inkluderes ikke i forslaget:

-   1001, fordi rabattdatoen 29. juni allerede er utløpt, så denne fakturaen ikke lenger er kvalifisert for kontantrabatt.
-   1003, fordi denne fakturaen ikke har en rabattdato.

### <a name="option-2-by-due-date"></a>Alternativ 2: Etter forfallsdato

April velger **Per forfallsdato** som forslag. Hun skriver inn datoområdet 26. juni til 10. juli. Følgende fakturaer inkluderes i forslaget:

-   1003, fordi forfallsdatoen 29. juli er i betalingsdatoområdet.

Følgende fakturaer inkluderes ikke i forslaget:

-   1001, fordi forfallsdatoen 15. juli er utenfor betalingsdatoområdet.
-   1002, fordi forfallsdatoen 20. juli er utenfor betalingsdatoområdet.
-   1004, fordi forfallsdatoen 17. juli er utenfor betalingsdatoområdet.

### <a name="option-3-by-due-date-and-cash-discount"></a>Alternativ 3: Etter forfallsdato og kontantrabatt

April velger **Forfallsdato og kontantrabatt** som forslag. Hun skriver inn datoområdet 26. juni til 10. juli. Følgende fakturaer inkluderes i forslaget:

-   1003, fordi forfallsdatoen 29. juli er i betalingsdatoområdet.
-   1002, fordi rabattdatoen 4. juli er i betalingsdatoområdet.
-   1004, fordi rabattdatoen 1. juli er i betalingsdatoområdet.

Følgende fakturaer inkluderes ikke i forslaget:

-   1001, fordi rabattdatoen 29. juni allerede er utløpt, så denne fakturaen er ikke lenger kvalifisert for kontantrabatt, og forfallsdatoen 15. juli også er utenfor datointervallet.

## <a name="country-specific-considerations"></a>Landsspesifikke hensyn
### <a name="norway"></a>Norge

#### <a name="dimension-control"></a>Dimensjonskontroll

Dimensjonskontroll lar deg kontrollere gruppering av genererte linjer etter betalingsforslag og angi standarddimensjoner basert på finansdimensjoner brukt for de utlignede fakturaene. I landkonteksten for Norge finnes en finansdimensjonskategori for hver betalingsmetode der du kan aktivere dimensjonskontroll i tillegg til å aktivere gruppering for hver dimensjon. Mulige alternativer er:

-   **Dimensionskontroll**-feltet er deaktivert. Betalingsforslaget fungerer som for alle andre land.
-   **Dimensionskontroll**-feltet er aktivert uten å definere dimensjonene ytterligere. Betalingsforslaget opprettes uten å ta hensyn til dimensjoner. Den opprettede transaksjonen arver ingen dimensjoner fra den utlignede posten.
-   **Dimensionskontroll**-feltet er aktivert og de ytterligere dimensjonene er aktivert. Nå kan du definere hvordan dimensjonene skal kopieres til journalen. For eksempel: • Merk av for **BusinessUnit** for å opprette et betalingsforslag per forretningsenhet for betalingsmåten, • merk av for **CostCenter** for å opprette et betalingsforslag per kostsenter for betalingsmåten

> [[!NOTE]
> Hvis du velger flere dimensjoner i det tredje alternativet, opprettes et betalingsforslag for dimensjonskombinasjonen.

#### <a name="bank-account-selection"></a>Bankkontovalg

Du kan definere en standard betalingskonto for debitering per betalingsmetode uansett landkontekst. Dette angis i betalingslinjene som genereres av et forslag. Med bankkontofunksjonen kan du definere flere bankkontoer for debitering som styres av dimensjon og valuta eller en kombinasjon av disse for å bruke forskjellige bankkontoer for debitering, avhengig av hver kombinasjon. Du kan definere disse kombinasjonene på siden **Betalingsmåter** ved hjelp av **Bankkontoer**-knappen som er tilgjengelig for hver betalingsmåte med **Kontotype for postering** = **Bank**.




