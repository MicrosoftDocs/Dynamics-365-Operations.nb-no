---
title: Forståelse av utligningsfunksjonen etter årsavslutningen
description: Denne artikkelen beskriver hvordan du bruker funksjonen for forståelse mellom utligningsfunksjon etter at årsavslutningsprosessen er kjørt.
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
ms.openlocfilehash: 7efa9d652d74bd836f51b5b1c5f6bfaf8934ea40
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832173"
---
# <a name="awareness-between-ledger-settlement-feature-after-year-end-close"></a>Forståelse av utligningsfunksjonen etter årsavslutning

[!include [banner](../includes/banner.md)]

## <a name="preparing-for-the-ledger-settlement-awareness-feature-after-year-end-close"></a>Klargjøring for utligningsfunksjon Forståelse av funksjon etter årsavslutning

En stor endring i funksjonen **Forståelse av utligning og årsavslutning** (**Forståelse**-funksjonen) er at utligning ikke kan gjøres på tvers av regnskapsår. Denne begrensning på tvers av året er bare relevant for utligning, ikke for utligninger for utestående fordringer eller leverandørgjeld.

Før **Forståelse**-funksjonen er aktivert, må regnskapsåret som gjennomgår årsavslutning, ikke ha noen finanstransaksjoner som utlignes på tvers av regnskapsår. Spesielt må du oppheve utligningen for transaksjoner som ble postert i regnskapsåret du kjører årsavslutning for, fra transaksjoner som ble postert til et annet regnskapsår. Transaksjonene kan deretter utlignes på nytt mot transaksjoner i samme regnskapsår.

Denne artikkelen beskriver trinnene som kreves for å identifisere, oppheve utligning og utligne finanstransaksjonene på nytt som er utlignet på tvers av regnskapsår. I eksemplet som vises, er regnskapsåret 2022 avsluttet. Fokus er på å forberede utligningstransaksjonene i god tid før avslutningen av 2023-årsavslutningen kjøres.

## <a name="example-setup"></a>Eksempeloppsett

Illustrasjonen nedenfor viser transaksjonene som ble postert for hovedkonto 110190. Finanstransaksjonene i grønt er utlignet i samme regnskapsår og behøver ikke å endres. Transaksjonene i rødt er utlignet i finans, men de har transaksjonsdatoer i forskjellige regnskapsår. Disse transaksjonene må identifiseres, og det kan hende at utligning må tilbakeføres.

![Finanstransaksjoner.](./media/afterYEC1.png)

## <a name="example"></a>Eksempel

Følg denne fremgangsmåten hvis organisasjonen vil bruke **Forståelse**-funksjonen etter årsavslutningen for regnskapsåret 2022 er kjørt.

> [!NOTE]
> Årsavslutningen for 2022 og tidligere regnskapsår må bare kjøres på nytt hvis nye transaksjoner posteres til regnskapsåret 2022 eller tidligere. Når du fullfører følgende fremgangsmåte, blir det ikke postert noen nye transaksjoner til 2022. Årsavslutningsprosessen trenger ikke å kjøres på nytt.
>
> Finanstransaksjoner som utlignes på tvers av regnskapsår, kan fortsatt utlignes hvis de ikke utlignes mot en transaksjon som ble postert i 2023 eller senere. Hvis du for eksempel har utlignet transaksjoner i 2019 og 2020, kan de forbli utlignet.

1. Fullfør årsavslutningen for 2022 uten at **Forståelse**-funksjonen er aktivert.
2. Valgfritt: Når årsavslutningen for 2022 er fullført, aktiverer du **Forståelse**-funksjonen. En årsavslutning regnes som fullført når alle justeringer posteres og årsavslutningsprosessen ikke kjøres på nytt.

    > [!IMPORTANT]
    > **Forståelse**-funksjonen kan ikke aktiveres hvis årsavslutningen for 2022 skal kjøres på nytt. Fordelen med å aktivere funksjonen nå er at du forhindrer brukere fra å utligne finanstransaksjoner som ble postert til ulike regnskapsår.

    Hvis årsavslutningen ikke er fullført, kan du fremdeles fullføre de neste trinnene uten å aktivere **Forståelse**-funksjonen. Du aktiverer funksjonen i et senere trinn som det er notert.

3. På siden **Utligning** identifiserer du summen av alle transaksjonene som utlignes over regnskapsårene 2022 og 2023. Legg merke til at 2021-transaksjoner som utlignes mot 2022-transaksjoner, ikke er relevante fordi 2022 allerede er avsluttet. Disse transaksjonene kan forbli utlignet.

    1. Angi et datoområde for hele regnskapsåret 2022. Angi for eksempel 1. januar 2022 til og med 31. desember 2022 hvis du bruker et kalenderår som regnskapsår.
    2. Velg **Utlignet** i **Status**-feltet.
    3. Filtrer på én finanskonto om gangen.

        - Du må gjenta disse trinnene for hver finanskonto som utligning skjer for.
        - Hvis andre finanskontoer ikke lenger er definert for utligning, må du kanskje legge dem til i utligningsoppsettet midlertidig. Fullfør deretter disse trinnene hvis disse finanskontoene har transaksjoner i 2023 som utlignes mot transaksjoner i 2022 eller tidligere.

    4. Velg og hold (eller høyreklikke) i kolonnen **Status** og velg deretter for å gruppere etter denne kolonnen.
    5. Velg og hold (eller høyreklikke) i kolonnen **Beløp i transaksjonsvaluta** og velg deretter for å summere denne kolonnen.

        - Hvis du bare utlignet transaksjoner i 2022, vil totalsummen være 0 (null).
        - Hvis du har transaksjoner som ble utlignet på tvers av regnskapsår, vil ikke summen være 0 (null).

    6. Identifiser hvilke transaksjoner som ble utlignet mellom 2022 og 2023 ved å filtrere på verdien **Utligningsdato**. Hvis du filtrerer på en utligningsdato 1. januar 2023 til og med 31. desember 2023, får du en totalsum på $ 700, som er summen av transaksjoner som ble utlignet i 2022 og 2023.

    ![Total 2022 finanstransaksjoner.](./media/afterYEC2.png)

4. Gjenta trinn 3 for regnskapsåret 2023. Totalen bør samsvare med $ 700 fra 2022 fordi ingen 2023-transaksjoner ble utlignet mot 2024-transaksjoner.

    ![Total 2023 finanstransaksjoner.](./media/afterYEC3.png)

5. Hvis du aktiverte **Forståelse**-funksjonen i trinn 2, deaktiverer du den før du går videre til trinn 6. I de neste trinnene tilbakefører du utligningen som krysset regnskapsår. Hvis **Forståelse**-funksjonen er aktivert, kan du ikke tilbakeføre utligning for regnskapsåret 2022. Derfor må du deaktivere funksjonen før du fortsetter.
6. Når **Forståelse**-funksjonen er deaktivert, bruker du de samme filtrene på siden **Utligning** til å tilbakeføre utligningen for de detaljerte transaksjonene.

    1. Gå tilbake til siden **Utligning** og filtrer på transaksjonsdatoer for 2023. Deretter finner du de detaljerte transaksjonene som utgjør totalen $ 700. Det er kanskje ikke så enkelt å filtrere etter denne informasjonen. Det kan hende at du må sende dataene til Microsoft Excel for å evaluere dem.
    2. Når du har listen over transaksjoner, velger du finanstransaksjonene på siden **Utligning** og velger **Merk valgt**. Du trenger ikke å se begge sider av finanstransaksjonene som ble utlignet. Hvis du merker enten debet eller kredit, tilbakeføres alt som har samme **Utlignings-ID**-verdi, selv om verdien **Merket beløp** ikke er **0** (null).
    3. Velg **Tilbakefør merkede transaksjoner** for å oppheve utligning av transaksjonene.

    ![Tilbakefør transaksjoner.](./media/afterYEC4.png)

7. Poster en justeringsjournal for å dele åpningssaldoen for 2023 i to beløp: Delen som er utlignet mot regnskapsåret 2022-transaksjonen og delen som ikke er utlignet ennå i 2023.

    - **Del av åpningssaldoen som er utlignet mot forrige år:** Det første beløpet er $ 700 basert på totalene som ble funnet som er utlignet mellom 2022 og 2023.
    - **Del av åpningssaldoen som ikke utlignes mot forrige år:** Det andre beløpet er differansen mellom åpningssaldoen og det første beløpet på $ 525. Gjenstående beløp er $ 1700 – $ 700 = $ 1000.

    På denne måten kan du utligne 2023-transaksjonene mot $ 700 som opprinnelig ble utlignet mot 2022-transaksjonen. Dette trinnet er nødvendig, fordi utligning ikke tillater delvis utligning.

    1. Gå til økonomijournalen og poster justeringen. Organisasjonen må bestemme hvilken transaksjonsdato som skal brukes, basert på periodene som er åpne i 2023.
    2. Det kan hende at du må deaktivere parameteren **Ikke tillat manuell registrering** på siden **Hovedkonto**. Denne justeringen kan ikke posteres hvis hovedkontoen ikke tillater manuell registrering.

    ![Justering blir ikke postert.](./media/afterYEC5.png)

8. Du kan nå utligne transaksjonene som utligning ble opphevet for. Gå tilbake til **Utligning** og begrens datoområdet til 1. januar 2022 til 31. desember 2022. Illustrasjonen nedenfor viser transaksjonene som utligning ble opphevet for, som nå finnes.

    ![Transaksjoner som ikke er utlignet.](./media/afterYEC6.png)

    - Åpningssaldoen på $ 1700 kan utlignes mot justeringen for – $ 1700.
    - De detaljerte transaksjonene som ikke ble utlignet for – $ 700, kan utlignes mot justeringen for $ 700,00.

9. Aktiver **Forståelse**-funksjonen på nytt
10. Etter at **Forståelse**-funksjonen er aktivert, kan ikke utligningen gjøres på tvers av regnskapsår. Det kan hende at du må dele den gjenstående saldoen på $ 1000 i mindre beløp før du kan utligne mot nye transaksjoner i 2023. Noen kunder velger å postere denne detaljen i trinn 8, der $ 1000 er ytterligere delt inn for å representere transaksjonene som ikke er utlignet, fra 2022. Denne fremgangsmåten ligner det **Forståelse**-funksjonen gjør for bare inneværende år. Neste år blir det automatisk utført ved hjelp av innstillingen **Behold detaljer** i oppsettet for utligning.
