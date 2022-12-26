---
title: Forståelse av utligningsfunksjonen før årsavslutningen
description: Denne artikkelen beskriver hvordan du bruker funksjonen for forståelse mellom utligningsfunksjon før årsavslutningsprosessen er kjørt.
author: kweekley
ms.date: 12/02/2022
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
ms.openlocfilehash: c79b6f50296560e1534be0621bb2aa8eaa2c1dc8
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832168"
---
# <a name="awareness-between-ledger-settlement-feature-before-year-end-close"></a>Forståelse av utligningsfunksjonen før årsavslutning

[!include [banner](../includes/banner.md)]

## <a name="preparing-for-the-ledger-settlement-awareness-feature-before-year-end-close"></a>Klargjøring for utligningsfunksjon Forståelse av funksjon før årsavslutning

En stor endring i funksjonen **Forståelse av utligning og årsavslutning** (**Forståelse**-funksjonen) er at utligning ikke kan gjøres på tvers av regnskapsår. Denne begrensning på tvers av året er bare relevant for utligning, ikke for utligninger for utestående fordringer eller leverandørgjeld.

Før **Forståelse**-funksjonen er aktivert, må regnskapsåret som gjennomgår årsavslutning, ikke ha noen finanstransaksjoner som utlignes på tvers av regnskapsår. Spesielt må du oppheve utligningen for transaksjoner som ble postert i regnskapsåret du kjører årsavslutning for, fra transaksjoner som ble postert til et annet regnskapsår. Transaksjonene kan deretter utlignes på nytt mot transaksjoner i samme regnskapsår.

Denne artikkelen beskriver trinnene som kreves for å identifisere, oppheve utligning og utligne finanstransaksjonene på nytt som er utlignet på tvers av regnskapsår. I eksemplet som følger er regnskapsåret 2021 lukket, og du forbereder å kjøre årsavslutningen for regnskapsåret 2022.

## <a name="example-setup"></a>Eksempeloppsett

Illustrasjonen nedenfor viser transaksjonene som ble postert for hovedkonto 110190. Finanstransaksjonene i grønt er utlignet i samme regnskapsår og behøver ikke å endres. Transaksjonene i rødt er utlignet i finans, men de har transaksjonsdatoer i forskjellige regnskapsår. Disse transaksjonene må identifiseres, og det kan hende at utligning må tilbakeføres.

![Finanstransaksjoner.](./media/YEC1.png)

## <a name="example"></a>Eksempel

Følg denne fremgangsmåten hvis organisasjonen vil bruke **Forståelse**-funksjonen før årsavslutningen for regnskapsåret 2022 er kjørt.

> [!NOTE]
> Årsavslutningen for 2021 og tidligere regnskapsår må bare kjøres på nytt hvis nye transaksjoner posteres til regnskapsåret 2021 eller tidligere. Når du fullfører følgende fremgangsmåte, blir det ikke postert noen nye transaksjoner til 2021. Årsavslutningsprosessen trenger ikke å kjøres på nytt.
>
> Finanstransaksjoner som utlignes på tvers av regnskapsår, kan fortsatt utlignes hvis de ikke utlignes mot en transaksjon som ble postert i 2022 eller senere. Hvis du for eksempel har utlignet transaksjoner i 2019 og 2020, kan de forbli utlignet.

1. Valgfritt: Aktiver **Forståelse**-funksjonen midlertidig.

    - Hvis du velger å aktivere funksjonen, må du deaktivere den i senere trinn, som notert. Fordelen med å aktivere funksjonen nå er at du midlertidig forhindrer brukere fra å utligne finanstransaksjoner som ble postert til ulike regnskapsår.
    - Hvis du velger ikke å aktivere funksjonen, anbefaler vi at du ber gruppen om ikke å utligne transaksjoner på tvers av regnskapsår. Hvis utligningen på tvers av år er fullført, må du gjenta trinnene for å identifisere og oppheve utligning av finanstransaksjonene.

2. På siden **Utligning** identifiserer du summen av alle transaksjonene som utlignes over regnskapsårene 2021 og 2022.

    1. Angi et datoområde for hele regnskapsåret 2021. Angi for eksempel 1. januar 2021 til og med 31. desember 2021 hvis du bruker et kalenderår som regnskapsår.

        Hvis **Forståelse**-funksjonen er aktivert, får du en advarsel om at transaksjoner ikke kan utlignes eller utligningen oppheves for et avsluttet regnskapsår. Advarselen er ikke relevant fordi det ikke finnes utligning eller opphevet utligning i dette trinnet.

    2. Velg **Utlignet** i **Status**-feltet.
    3. Filtrer på én finanskonto om gangen.

        - Du må gjenta disse trinnene for hver finanskonto som utligning skjer for.
        - Hvis andre finanskontoer ikke lenger er definert for utligning, må du kanskje legge dem til i utligningsoppsettet midlertidig. Fullfør deretter disse trinnene hvis disse finanskontoene har transaksjoner i 2022 som utlignes mot transaksjoner i et annet regnskapsår.

    4. Velg og hold (eller høyreklikke) i kolonnen **Status** og velg deretter for å gruppere etter denne kolonnen.
    5. Velg og hold (eller høyreklikke) i kolonnen **Beløp i transaksjonsvaluta** og velg deretter for å summere denne kolonnen.

        - Hvis du bare utlignet transaksjoner i 2021, vil totalsummen være 0 (null).
        - Hvis du har transaksjoner som ble utlignet på tvers av regnskapsår, vil ikke summen være 0 (null).

        I illustrasjonen nedenfor er det en saldo på $ 525,00. Denne saldoen er summen av transaksjonene som ble utlignet mot transaksjoner i et annet regnskapsår. Summen kan omfatte transaksjoner som ble utlignet mellom 2021 og 2022, og transaksjoner som ble utlignet mellom 2022 og 2023.

        ![Finanstransaksjoner 2021–2022.](./media/YEC2.png)

    6. Identifiser hvilke transaksjoner som ble utlignet mellom 2020 og 2021 ved å filtrere ytterligere på verdien **Utligningsdato**. Angi et datoområdefilter på 1. januar 2021 til og med 31. desember 2021. Ingen transaksjoner vises fordi ingen 2020-transaksjoner ble utlignet mot transaksjoner som ble postert til 2021.
    7. Identifiser hvilke transaksjoner som ble utlignet mellom 2021 og 2022 ved endre datofilteret på verdien **Utligningsdato**. Angi et datoområdefilter på 1. januar 2022 til og med 31. desember 2022. Transaksjonene vises igjen, og totalen er $ 525,00 fordi alle transaksjonene ble utlignet mellom 2021 og 2022.

3. På siden **Utligning** identifiserer du summen av alle transaksjonene som utlignes over regnskapsårene 2021 og 2022.

    1. Angi et datoområde for hele regnskapsåret 2022. Angi for eksempel 1. januar 2022 til og med 31. desember 2022 hvis du bruker et kalenderår som regnskapsår.
    2. Velg **Utlignet** i **Status**-feltet.
    3. Filtrer på én finanskonto om gangen.
    4. Velg og hold (eller høyreklikke) i kolonnen **Status** og velg deretter for å gruppere etter denne kolonnen.
    5. Velg og hold (eller høyreklikke) i kolonnen **Beløp i transaksjonsvalutaen** og velg deretter for å summere denne kolonnen.

        ![Totalt beløp for finanstransaksjon.](./media/YEC3.png)

    6. Legg til et ekstra filter på verdien **Utligningsdato**. Angi et datoområdefilter på 1. januar 2022 til og med 31. desember 2022. Den samme totalen på $ 525,00 vises. Dette resultatet validerer at totalbeløpet for transaksjoner som er utlignet mellom 2021 og 2022, $ 525,00.

        ![Finanstransaksjoner for utligningsdatoer i 2022 og 2023.](./media/YEC4.png)

    7. Endre det ekstra filteret på verdien **Utligningsdato**. Angi et datoområdefilter på 1. januar 2023 til og med 31. desember 2023. En ny total på $ 700 vises. Denne summen er totalbeløpet for transaksjonene som ble utlignet mellom 2022 og 2023.
 
4. Gjenta trinn 3 for regnskapsåret 2023. Totalen bør samsvare med $ 700 fra 2022 fordi ingen 2023-transaksjoner ble utlignet mot 2024-transaksjoner.
5. Hvis du aktiverte **Forståelse**-funksjonen i trinn 1, deaktiverer du den før du går videre til trinn 6. I de neste trinnene tilbakefører du utligningen som krysset regnskapsår. Hvis **Forståelse**-funksjonen er aktivert, kan du ikke tilbakeføre utligning for regnskapsåret 2021. Derfor må du deaktivere funksjonen før du fortsetter.
6. Når **Forståelse**-funksjonen er deaktivert, bruker du de samme filtrene på siden **Utligning** til å tilbakeføre utligningen for de detaljerte transaksjonene.

    1. Gå tilbake til siden **Utligning** og filtrer på transaksjonsdatoer for 2021. Legg til et ekstra filter på verdien **Utligningsdato**. Angi et datoområdefilter fra 1. januar 2022 til og med 31. desember 2022. Deretter finner du de detaljerte transaksjonene som utgjør totalen $ 525. Det er kanskje ikke så enkelt å filtrere etter denne informasjonen. Det kan hende at du må sende dataene til Microsoft Excel for å evaluere dem.
    2. Når du har listen over transaksjoner, velger du finanstransaksjonene på siden **Utligning** og velger **Merk valgt**. Du trenger ikke å se begge sider av finanstransaksjonene som ble utlignet. Hvis du merker enten debet eller kredit, tilbakeføres alt som har samme **Utlignings-ID**-verdi, selv om verdien **Merket beløp** ikke er **0** (null).
    3. Velg **Tilbakefør merkede transaksjoner** for å oppheve utligning av transaksjonene.

    ![Tilbakefør merkede transaksjoner.](./media/YEC5.png)

7. Gjenta trinn 6 for å tilbakeføre utligningen for transaksjonene som ble utlignet i 2022 og 2023.

    ![Tilbakefør finanstransaksjoner.](./media/YEC6.png)

8. Poster en justeringsjournal for å dele åpningssaldoen for 2022 i to beløp: Delen som er utlignet mot regnskapsåret 2021-transaksjonen og delen som ikke er utlignet ennå i 2022.

    - **Del av åpningssaldoen som er utlignet mot forrige år:** Det første beløpet er $ 525 basert på totalene som ble funnet som ble utlignet mellom 2021 og 2022.
    - **Del av åpningssaldoen som ikke utlignes mot forrige år:** Det andre beløpet er differansen mellom åpningssaldoen og det utlignede beløpet på $ 525. Gjenstående beløp er $ 1025 – $ 525 = $ 500.

    På denne måten kan du utligne 2022-transaksjonene mot $ 525 som opprinnelig ble utlignet mot 2021-transaksjonen. Dette trinnet er nødvendig, fordi utligning ikke tillater delvis utligning.

    1. Gå til økonomijournalen og poster justeringen. Organisasjonen må bestemme hvilken transaksjonsdato som skal brukes, basert på periodene som er åpne. Disse transaksjonene kan ha blitt utlignet ved å bruke utligningsdatoen januar eller februar 2022, men justeringen kan bli postert i desember hvis det er den eneste åpne perioden.
    2. Det kan hende at du må deaktivere parameteren **Ikke tillat manuell registrering** på siden **Hovedkonto**. Denne justeringen kan ikke posteres hvis hovedkontoen ikke tillater manuell registrering.

    ![Justering blir ikke postert.](./media/YEC7.png)

9. Du kan nå utligne transaksjonene som utligning ble opphevet for. Gå tilbake til **Utligning** og begrens datoområdet til 1. januar 2022 til 31. desember 2022. Illustrasjonen nedenfor viser transaksjonene som utligning ble opphevet for, som nå finnes.

    ![Transaksjoner som ikke er utlignet.](./media/YEC8.png)

    - Åpningssaldoen på $ 1025 kan utlignes mot justeringen for – $ 1025.
    - De detaljerte transaksjonene som ikke ble utlignet for – $ 400, – $ 50 og – $ 75, kan utlignes mot justeringen for $ 525,00.

    ![Detaljerte transaksjoner.](./media/YEC9.png)

10. Aktiver **Forståelse**-funksjonen. Du er nå klar til å kjøre årsavslutningen.

    - Før du kjører årsavslutningen, bør du vurdere å velge alternativet **Behold detaljer** i utligningsoppsettet for alle balansekontoer. Hvis du vil ha mer informasjon om fordelene ved å fullføre dette trinnet, kan du se Forståelse-dokument.
    - Når du begynner årsavslutningen for 2022, hvis det fremdeles finnes transaksjoner som utlignet på tvers av regnskapsår, varsler årsavslutningsprosessen deg umiddelbart.
    - Hvis 2021- og 2022-transaksjoner fremdeles er utlignet, må du deaktivere **Forståelse**-funksjonen på nytt og gjenta de forrige trinnene for å oppheve utligning for transaksjonene. Denne fremgangsmåten kreves fordi 2021 er avsluttet, og du kan ikke oppheve utligning for transaksjoner i et avsluttet regnskapsår.
    - Hvis transaksjoner for 2022 og 2023 fremdeles er utlignet, trenger du **ikke** å deaktivere **Forståelse**-funksjonen. Fordi verken 2022 eller 2023 er lukket, kan du bruke de forrige trinnene til å oppheve utligning for transaksjonene.

Når årsavslutningen for 2022 er kjørt, kan du la **Forståelse**-funksjonen være aktivert fra nå av.
