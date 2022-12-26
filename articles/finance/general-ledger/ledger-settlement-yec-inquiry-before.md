---
title: Forståelse av utligningsfunksjonen før årsavslutningen ved å bruke forespørselssiden
description: Denne artikkelen beskriver hvordan du bruker funksjonen for forståelse mellom utligningsfunksjon ved å bruke den nye forespørselssiden før årsavslutning for økonomimodul er kjørt.
author: kweekley
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: b138d2d5e88ff7f2ca2240cf256a4938f55a5606
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853160"
---
# <a name="awareness-between-ledger-settlement-feature-before-year-end-close-using-the-inquiry-page"></a>Forståelse av utligningsfunksjonen før årsavslutningen ved å bruke forespørselssiden

En hovedendring i funksjonen **Forståelse av utligning og årsavslutning** (**Forståelse**-funksjonen) er at utligning ikke kan gjøres på tvers av regnskapsår. Denne begrensning på tvers av året er bare relevant for utligning, ikke for utligninger for utestående fordringer eller leverandørgjeld.

Før du aktiverer **Forståelse**-funksjonen, må regnskapsåret som gjennomgår årsavslutning, ikke ha noen finanstransaksjoner som utlignes på tvers av regnskapsår. Spesielt må du oppheve utligningen for transaksjoner som ble postert i regnskapsåret du kjører årsavslutning for, fra transaksjoner som ble postert til et annet regnskapsår. Transaksjonene kan deretter utlignes på nytt mot transaksjoner i samme regnskapsår.

Denne artikkelen beskriver trinnene som kreves for å identifisere, oppheve utligning og utligne finanstransaksjonene på nytt som er utlignet på tvers av regnskapsår. I eksemplet som følger er regnskapsåret 2021 lukket, og du forbereder å kjøre årsavslutningen for regnskapsåret 2022.

Fra og med Microsoft Dynamics 365 Finance, utgivelse 10.0.29 kan du identifisere, oppheve utligning og utligne finanstransaksjoner på nytt ved hjelp av en ny forespørselsside som er tilgjengelig. Hvis du ikke har tilgang til Finance-utgivelsen 10.0.29 eller senere, kan du finne fremgangsmåten for å identifisere, oppheve utligning og utligne finanstransaksjonene på nytt i følgende artikler:

- [Forståelse av utligningsfunksjonen før årsavslutning](ledger-settle-yec.md)
- [Forståelse av utligningsfunksjonen etter årsavslutning](ledger-settle-yec-after.md)

Hvis du vil ha mer informasjon om det nye forespørselsvinduet, kan du se [Utligningsforespørsler](ledger-settlement-inquiry.md). 

## <a name="example-setup"></a>Eksempeloppsett

Illustrasjonen nedenfor viser transaksjonene som ble postert for hovedkonto 110200. Finanstransaksjonene i grønt ble utlignet i samme regnskapsår og behøver ikke å endres. Transaksjonene i rødt ble utlignet i finans, men de har transaksjonsdatoer i forskjellige regnskapsår. Disse transaksjonene må identifiseres, og det kan hende at utligning må tilbakeføres.

![Posterte finanstransaksjoner.](./media/ledgersettlement.png)

## <a name="example"></a>Eksempel

Følg denne fremgangsmåten hvis organisasjonen vil bruke **Forståelse**-funksjonen før du kjører årsavslutningen for regnskapsåret 2022.

> [!NOTE]
> Årsavslutningen for 2021 og tidligere regnskapsår må bare kjøres på nytt hvis nye transaksjoner posteres til regnskapsåret 2021 eller tidligere. Når du fullfører følgende fremgangsmåte, blir det ikke postert noen nye transaksjoner til 2021. Årsavslutningsprosessen trenger ikke å kjøres på nytt.
>
> Finanstransaksjoner som utlignes på tvers av regnskapsår, kan fortsatt utlignes hvis de ikke utlignes mot en transaksjon som ble postert i 2022 (året som avsluttes) eller senere. Hvis du for eksempel har utlignet transaksjoner i 2019 og 2020, kan de forbli utlignet.

1. **Ikke** aktiver **Forståelse**-funksjonen.
2. Velg **Se gjennom utligning på tvers av år** på siden **Utligninger**.
3. Identifiser alle transaksjonene som ble postert til andre regnskapsår, men utlignet mot transaksjoner som ble postert til 2022.

    1. Velg regnskapsåret 2022, regnskapsåret som du vil kjøre årsavslutningen for.
    2. Velg en verdi i **Finansdimensjonssett**-feltet for å vise finansdimensjonene du vil vise for finanskontoen. Hovedkontoen vises alltid, selv om dimensjonssettet som er valgt, ikke inneholder en hovedkonto.
    3. Velg **Vis transaksjoner**.

    Forespørselssiden viser alle transaksjoner for alle finanskontoer (selv om de ikke lenger er i oppsettet for utligningen), fra alle andre regnskapsår som utlignes mot transaksjoner som ble postert til 2022. Tre forskjellige finanskontoer vises.

    ![2022-utligninger på tvers av år.](./media/review-cross-year.png)

3. Merk og hold (eller høyreklikk) i rutenettet, og velg deretter **Eksporter alle rader**. Disse radene er alle transaksjonene som du må oppheve utligning for fra transaksjonene i 2022 før årsavslutningen kan kjøres. Du vil ha den detaljerte transaksjonslisten slik at du kan tilbakestille transaksjonene på riktig måte senere.
4. Legg merke til regnskapsårene som transaksjonene ble postert for. I dette eksemplet finnes det transaksjoner i 2021 og 2023.
5. På forespørselssiden endrer du regnskapsåret til 2021, det første regnskapsåret som inneholder transaksjoner som ble utlignet mot 2022-transaksjoner.
6. Filtrer på **Transaksjonsdato**-kolonnen slik at bare transaksjoner som ble postert i 2022, tas med. Disse transaksjonene er de detaljerte transaksjonene fra 2022 som ble utlignet mot transaksjoner i 2021.
7. Merk og hold (eller høyreklikk) i rutenettet, og velg deretter **Eksporter alle rader**.

    > [!IMPORTANT]
    > I de følgende trinnene blir det oppheve utligning for disse transaksjonene og deretter utlignet på nytt mot transaksjoner i 2022. Det er viktig at du opprettholder denne detaljen i Excel.

    ![2021-utligninger på tvers av år.](./media/review-cross-year.png)

8. På forespørselssiden endrer du regnskapsåret til 2023, det neste regnskapsåret som inneholder transaksjoner som ble utlignet mot 2022-transaksjoner. 
9. Filtrer på **Transaksjonsdato**-kolonnen slik at bare transaksjoner som ble postert i 2022, tas med. Disse transaksjonene er de detaljerte transaksjonene fra 2023 som ble utlignet mot transaksjoner i 2022. 
10. Merk og hold (eller høyreklikk) i rutenettet, og velg deretter **Eksporter alle rader**.

    > [!IMPORTANT]
    > I de følgende trinnene blir det oppheve utligning for disse transaksjonene og deretter utlignet på nytt mot transaksjoner i 2022. Det er viktig at du opprettholder denne detaljen i Excel.

    ![2023-utligninger på tvers av år.](./media/filter-transactions.png)

11. Gjenta de forrige trinnene for hvert regnskapsår som har transaksjoner som ble utlignet mot transaksjoner i 2022. Eksporter alltid de detaljerte transaksjonene til Excel.

    Når alle de detaljerte transaksjonene fra 2021 og 2023 er eksportert til Excel, er du klar til å utligne transaksjonene ved hjelp av den nye forespørselssiden.

12. Endre regnskapsåret til 2022.
13. Velg alle postene i rutenettet, og velg deretter **Opphev utligning for markerte poster**. Utligning oppheves for alle de valgte transaksjonene i rutenettet.

    Det vises to advarsler for å sikre at transaksjonsdetaljene eksporteres til Excel før utligning blir opphevet for transaksjonene. Hvis du utilsiktet opphever utligning for finanstransaksjoner før du sender detaljene til Excel, er det ingen måte å tilbakeføre opphevingen av utligningen på.

    ![Oppheving av utligning for transaksjoner på tvers av utligninger.](./media/revert-unsettle.png)

14. Bruk Excel-dataene til å finne totalbeløpet for transaksjoner i 2021 og 2023 som ble utlignet mot transaksjoner i 2022. I dette eksemplet brukes transaksjonene for 2021 total $ 525, og transaksjonene for 2023 total $ 700.
15. Poster en justeringsjournal for å dele åpningssaldoen for 2022 i to beløp: Delen som ble utlignet mot regnskapsåret 2021 og delen som ikke er utlignet til 2022 ennå.

    - **Del av åpningssaldoen som ble utlignet til forrige år:** Det første beløpet er $ 525 basert på totalene som ble funnet som ble utlignet mellom 2021 og 2022.
    - **Del av åpningssaldoen som ikke ble utlignet til forrige år:** Det andre beløpet er differansen mellom åpningssaldoen og det utlignede beløpet på $ 525. Gjenstående beløp er $ 1025 – $ 525 = $ 500.

    På denne måten kan du utligne 2022-transaksjonene mot $ 525 som opprinnelig ble utlignet mot 2021-transaksjonen. Dette trinnet er nødvendig, fordi utligning ikke tillater delvis utligning.

    1. Gå til økonomijournalen og poster justeringen. Organisasjonen må bestemme hvilken transaksjonsdato som skal brukes, basert på periodene som er åpne. Disse transaksjonene kan ha blitt utlignet ved å bruke utligningsdatoen januar eller februar 2022, men justeringen kan bli postert i desember hvis det er den eneste åpne perioden.
    2. Det kan hende at du må deaktivere parameteren **Ikke tillat manuell registrering** for konto 110200 på siden **Hovedkonto**. Denne justeringen kan ikke posteres hvis hovedkontoen ikke tillater manuell registrering.

    ![Postering av en justering av økonomijournalen.](./media/not-post.png)

16. Du kan nå utligne transaksjonene som utligning ble opphevet for. Gå tilbake til **Utligning**-siden, angi et datoområde fra 1. januar til og med 31. desember 2022 og filtrer på hovedkonto 110200. Deretter bruker du de detaljerte transaksjonene du eksporterte til Excel, til å finne de bestemte transaksjonene som du må oppheve utligning for. Illustrasjonen nedenfor viser transaksjonene som utligning ble opphevet for, som nå finnes.

    ![Transaksjoner som ikke er utlignet.](./media/updated-unsettled.png)

    - Åpningssaldoen på $ 1025 kan utlignes mot justeringen for – $ 1025.
    - De detaljerte transaksjonene som ikke ble utlignet for – $ 400, – $ 50 og – $ 75, kan utlignes mot justeringen for $ 25.

17. Aktiver **Forståelse**-funksjonen. Du er nå klar til å kjøre årsavslutningen.

    - Før du kjører årsavslutningen, bør du vurdere å velge alternativet **Behold detaljer** for alle balansekontoer i utligningsoppsettet. Hvis du vil ha mer informasjon, kan du se [Forståelse av utligning og årsavslutning](awareness-between-ledger-settlement-year-end-close.md).
    - Når du begynner årsavslutningen for 2022, hvis det fremdeles finnes transaksjoner som ble utligne på tvers av regnskapsår, varsler årsavslutningsprosessen deg umiddelbart. Dette kan skje hvis brukere utligner transaksjoner på tvers av regnskapsår etter at du har fullført de forrige trinnene.
    - Hvis 2021- og 2022-transaksjoner fremdeles er utlignet, må du deaktivere **Forståelse**-funksjonen på nytt og gjenta deretter de forrige trinnene for å oppheve utligning for disse transaksjonene. Denne fremgangsmåten kreves fordi 2021 er avsluttet, og du kan ikke oppheve utligning for transaksjoner i et avsluttet regnskapsår.
    - Hvis transaksjoner for 2022 og 2023 fremdeles er utlignet, trenger du ikke å deaktivere **Forståelse**-funksjonen. Fordi verken 2022 eller 2023 er lukket, kan du bruke de forrige trinnene til å oppheve utligning for transaksjonene.

18. Du kan utligne $ 700-transaksjonene fra 2023 mot de detaljerte transaksjonene som ble hentet over som åpningssaldoer i 2023. Denne transaksjonen utlignes ikke mot den opprinnelige transaksjonen i 2022.

Når årsavslutningen for 2022 er kjørt, kan du la **Forståelse**-funksjonen være aktivert fra nå av.
