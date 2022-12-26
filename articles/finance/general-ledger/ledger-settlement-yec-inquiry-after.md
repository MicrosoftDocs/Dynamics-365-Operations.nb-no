---
title: Forståelse av utligningsfunksjonen etter årsavslutningen ved å bruke forespørselssiden
description: Denne artikkelen beskriver hvordan du bruker funksjonen for forståelse mellom utligningsfunksjon ved å bruke den nye forespørselssiden etter årsavslutning for økonomimodul er kjørt.
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
ms.openlocfilehash: 921d2a17409ae10cd9c22eeca11557ba1248b9bc
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853155"
---
# <a name="awareness-between-ledger-settlement-feature-after-year-end-close-using-the-inquiry-page"></a>Forståelse av utligningsfunksjonen etter årsavslutningen ved å bruke forespørselssiden

En hovedendring i funksjonen **Forståelse av utligning og årsavslutning** (**Forståelse**-funksjonen) er at utligning ikke kan gjøres på tvers av regnskapsår. Denne begrensning på tvers av året er bare relevant for utligning, ikke for utligninger for utestående fordringer eller leverandørgjeld.

Før du aktiverer **Forståelse**-funksjonen, må regnskapsåret som gjennomgår årsavslutning, ikke ha noen finanstransaksjoner som utlignes på tvers av regnskapsår. Spesielt må du oppheve utligningen for transaksjoner som ble postert i regnskapsåret du kjører årsavslutning for, fra transaksjoner som ble postert til et annet regnskapsår. Transaksjonene kan deretter utlignes på nytt mot transaksjoner i samme regnskapsår.

Denne artikkelen beskriver trinnene som kreves for å identifisere, oppheve utligning og utligne finanstransaksjonene på nytt som er utlignet på tvers av år. I eksemplet som vises, er regnskapsåret 2022 avsluttet. Fokus er på å forberede utligningstransaksjonene før avslutningen av 2023-årsavslutningen kjøres.

Fra og med Microsoft Dynamics 365 Finance, utgivelse 10.0.29 kan du identifisere, oppheve utligning og utligne finanstransaksjoner på nytt ved hjelp av en ny forespørselsside som er tilgjengelig. Hvis du ikke har tilgang til Microsoft Dynamics 365 Finance-utgivelsen 10.0.29 eller senere, kan du finne fremgangsmåten for å identifisere, oppheve utligning og utligne finanstransaksjonene på nytt i følgende artikler:

- [Forståelse av utligningsfunksjonen før årsavslutning](ledger-settle-yec.md)
- [Forståelse av utligningsfunksjonen etter årsavslutning](ledger-settle-yec-after.md)

Hvis du vil ha mer informasjon om det nye forespørselsvinduet, kan du se [Utligningsforespørsler](ledger-settlement-inquiry.md). 

## <a name="example-setup"></a>Eksempeloppsett

Illustrasjonen nedenfor viser transaksjonene som ble postert for hovedkonto 110200. Finanstransaksjonene i grønt ble utlignet i samme regnskapsår og behøver ikke å endres. Transaksjonene i rødt ble utlignet i finans, men de har transaksjonsdatoer i forskjellige regnskapsår. Disse transaksjonene må identifiseres, og det kan hende at utligning må tilbakeføres.

![Posterte finanstransaksjoner.](./media/excel.png)

## <a name="example"></a>Eksempel

Følg denne fremgangsmåten hvis organisasjonen vil bruke **Forståelse**-funksjonen etter at du kjører årsavslutningen for regnskapsåret 2022.

> [!NOTE]
> Årsavslutningen for 2022 og tidligere regnskapsår må bare kjøres på nytt hvis nye transaksjoner posteres til regnskapsåret 2022 eller tidligere. Når du fullfører følgende fremgangsmåte, blir det ikke postert noen nye transaksjoner til 2022. Årsavslutningsprosessen trenger ikke å kjøres på nytt.
>
> Finanstransaksjoner som utlignes på tvers av regnskapsår, kan fortsatt utlignes hvis de ikke utlignes mot en transaksjon som ble postert i 2022 eller senere. Hvis du for eksempel har utlignet transaksjoner i 2019 og 2020, kan de forbli utlignet.

1. Fullfør årsavslutningen for 2022 uten at **Forståelse**-funksjonen er aktivert.
2. Identifiser alle transaksjonene som ble postert til andre regnskapsår, men utlignet mot transaksjoner som ble postert til 2023 (det neste regnskapsåret som skal lukkes).

    > [!NOTE]
    > 2021-transaksjoner som ble utlignet mot 2022-transaksjoner, ikke er relevante fordi året allerede er avsluttet for 2022. Disse transaksjonene kan forbli utlignet.

    1. Velg **Se gjennom utligning på tvers av år** på siden **Utligninger**.
    2. Velg regnskapsåret 2023, det neste regnskapsåret som du vil kjøre årsavslutningen for.
    3. Velg en verdi i **Finansdimensjonssett**-feltet for å vise finansdimensjonene du vil vise for finanskontoen. Hovedkontoen vises alltid, selv om dimensjonssettet som er valgt, ikke inneholder en hovedkonto.
    4. Velg **Vis transaksjoner**.

    Forespørselssiden viser alle transaksjonene fra andre regnskapsår som er utlignet mot transaksjoner som ble postert i 2023.

    ![2023-utligninger på tvers av år.](./media/2023-cross-settlement.png)

3. Merk og hold (eller høyreklikk) i rutenettet, og velg deretter **Eksporter alle rader**. Disse radene er alle transaksjonene som du må oppheve utligning for fra transaksjonene i 2022 før årsavslutningen for neste år (2023) kan kjøres. Du vil registrere disse transaksjonene.

    Når alle de detaljerte transaksjonene fra 2022 er eksportert til Excel, er du klar til å utligne transaksjonene ved hjelp av den nye forespørselssiden.

4. Velg alle postene i rutenettet, og velg deretter **Opphev utligning for markerte poster**. Utligning oppheves for alle de valgte transaksjonene i rutenettet.

    Det vises to advarsler for å sikre at transaksjonsdetaljene eksporteres til Excel før utligning blir opphevet for transaksjonene. Hvis du utilsiktet opphever utligning for finanstransaksjoner før du sender detaljene til Excel, er det ingen måte å tilbakeføre opphevingen av utligningen på.

    ![Opphev utligning på tvers av år.](./media/revert-settlement.png)

5. Bruk Excel-dataene til å finne totalbeløpet for transaksjoner i 2022 som ble utlignet mot transaksjoner i 2023. I dette eksemplet er transaksjonene for 2023 total $ 700.
6. Poster en justeringsjournal for å dele åpningssaldoen for 2022 i to beløp: Delen som ble utlignet mot regnskapsåret 2022-regnskapsårtransaksjonen og delen som ikke er utlignet til 2023 ennå.

    - **Del av åpningssaldoen som ble utlignet til forrige år:** Det første beløpet er $ 700 basert på totalene som ble funnet som ble utlignet mellom 2021 og 2022.
    - **Del av åpningssaldoen som ikke ble utlignet til forrige år:** Det andre beløpet er differansen mellom åpningssaldoen og det utlignede beløpet på $ 700. Gjenstående beløp er $ 1700 – $ 700 = $ 1000.

    På denne måten kan du utligne 2023-transaksjonene mot $ 700 som opprinnelig ble utlignet mot 2022-transaksjon. Dette trinnet er nødvendig, fordi utligning ikke tillater delvis utligning.

    1. Gå til økonomijournalen og poster justeringen. Organisasjonen må bestemme hvilken transaksjonsdato som skal brukes, basert på periodene som er åpne i 2023.
    2. Det kan hende at du må deaktivere parameteren **Ikke tillat manuell registrering** på siden **Hovedkonto**. Denne justeringen kan ikke posteres hvis hovedkontoen ikke tillater manuell registrering.

    ![Postering av en justering av økonomijournalen.](./media/no-manual4.png)

7. Du kan nå utligne transaksjonene som utligning ble opphevet for. Gå tilbake til **Utligninger**-siden og begrens datoområdet til 1. januar til 31. desember 2023. Deretter bruker du de detaljerte transaksjonene du eksporterte til Excel, til å finne de bestemte transaksjonene som du må oppheve utligning for. Illustrasjonen nedenfor viser transaksjonene som utligning ble opphevet for, som nå finnes.

    ![2023-transaksjoner som ikke er utlignet.](./media/2023-unsettled5.png)

    - Åpningssaldoen på $ 1700 kan utlignes mot justeringen for – $ 1700.
    - De detaljerte transaksjonene som ikke ble utlignet for – $ 700, kan utlignes mot justeringen for $ 700,00.

8. Aktiver **Forståelse**-funksjonen. Du er nå klar til å kjøre årsavslutningen.

    - Før du kjører årsavslutningen for 2023, bør du vurdere å velge alternativet **Behold detaljer** for alle balansekontoer i utligningsoppsettet. Hvis du vil ha mer informasjon, kan du se [Forståelse av utligning og årsavslutning](awareness-between-ledger-settlement-year-end-close.md).
    - Når du begynner årsavslutningen for 2023, hvis det fremdeles finnes transaksjoner som ble utligne på tvers av regnskapsår, varsler årsavslutningsprosessen deg umiddelbart. Denne situasjonen kan oppstå hvis brukere utlignet transaksjoner på tvers av regnskapsår før **Forståelse**-funksjonen ble aktivert.
    - Hvis 2022- og 2023-transaksjoner fremdeles er utlignet, må du deaktivere **Forståelse**-funksjonen på nytt og gjenta deretter de forrige trinnene for å oppheve utligning for disse transaksjonene. Denne fremgangsmåten kreves fordi 2022 er avsluttet, og du kan ikke oppheve utligning for transaksjoner i et avsluttet regnskapsår.

Når årsavslutningen for 2022 er kjørt, kan du la **Forståelse**-funksjonen være aktivert fra nå av.
