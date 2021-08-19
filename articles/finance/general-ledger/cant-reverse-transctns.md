---
title: Hvorfor kan jeg ikke tilbakeføre denne transaksjonen?
description: Dette emnet beskriver forskjellige årsaker til hvorfor transaksjoner ikke kan tilbakeføres. Det viser også løsninger på dette problemet.
author: kweekley
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 869832f085ee91f6c1fee53dad508cf5e54535627dadd6fb59a7586b03c8ec3b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719740"
---
# <a name="why-cant-i-reverse-this-transaction"></a>Hvorfor kan jeg ikke tilbakeføre denne transaksjonen?

[!include [banner](../includes/banner.md)]

Dette emnet beskriver forskjellige årsaker til hvorfor transaksjoner ikke kan tilbakeføres. Det viser også løsninger på dette problemet.

## <a name="symptom"></a>Symptom

Organisasjoner kan oppleve situasjoner der de må tilbakeføre en transaksjon de har postert. Noen ganger vil systemet hindre dem i å tilbakeføre disse transaksjonene. Denne virkemåten kan føre til to spørsmål:

- Hvorfor kan jeg ikke tilbakeføre transaksjonen?
- Hvordan påvirker funksjonen Massetilbakeføring denne virkemåten?

## <a name="resolution"></a>Løsning

Transaksjoner må oppfylle bestemte kriterier før de kan tilbakeføres. De gjenværende delene i dette emnet inneholder validering av hver modul. Selv om dette emnet fokuserer på transaksjoner i Microsoft Dynamics 365 Finance, kan noen av begrepene og valideringen brukes på andre apper, for eksempel Dynamics 365 Supply Chain Management.

I tillegg kan stedet der en transaksjon tilbakeføres, påvirke om den kan tilbakeføres. En leverandørbetaling som posteres som en sjekk, kan for eksempel bare tilbakeføres fra **Sjekker**-delen på transaksjonssiden for bankkontoene. Den kan ikke tilbakeføres fra **Bilagstransaksjoner**-sider i økonomimodulen.

Hvis funksjonen **Massetilbakeføring for flere dokumenter** (også kalt funksjonen Massetilbakeføring) er aktivert i arbeidsområdet **Funksjonsstyring**, påvirker det hvor mange transaksjoner som kan tilbakeføres og hvor de kan tilbakeføres. Denne funksjonen gir to fordeler når den er aktivert:

- For noen transaksjonstyper kan du velge mer enn én transaksjon om gangen og tilbakeføre mer enn én transaksjon fra journalen den ble postert fra, eller fra siden **bilagstransaksjoner**. Enkelttransaksjonene må imidlertid være tilbakeføringsbare før funksjonen ble aktivert. Før denne funksjonen ble innført, måtte transaksjoner tilbakeføres én om gangen.
- *Noen* underfinanstransaksjoner kan tilbakeføres fra journalen (økonomijournal) eller siden **Bilagstransaksjoner**. De behøver ikke å tilbakeføres fra underfinanssiden. En leverandørfakturajournal kan for eksempel tidligere bare tilbakeføres fra siden **Leverandørtransaksjon**. Den kan imidlertid nå tilbakeføres fra økonomimodulsiden også fra journalen eller siden **Bilagstransaksjoner**. Hver del av dette emnet forklarer transaksjonstypene som denne fordelen ikke gjelder.

Funksjonen for massetilbakeføring gjør det **ikke** mulig å tilbakeføre flere typer transaksjoner. Hvis en transaksjonstype ikke kunne tilbakeføres tidligere, kan den fremdeles ikke tilbakeføres etter at funksjonen er aktivert. Leverandørfakturaer for bestillinger kan for eksempel ikke tilbakeføres, uansett om funksjonen for massetilbakeføring er aktivert.

Hvis du vil ha mer informasjon om funksjonen for massetilbakeføring, kan du se [Tilbakefør journalpostering](reverse-journal-posting.md).

## <a name="general-ledger"></a>Økonomimodul

Økonomimoduljusteringer angis bare ved hjelp av finanskontoer. Derfor oppdaterer de bare økonomimodulen.

Hvis funksjonen Massetilbakeføring er deaktivert, kan de fleste økonomimoduljusteringer tilbakeføres enkeltvis fra siden **Transaksjonene for \<main account\>** (**LedgerTransAccount)**. (Den nøyaktige tittelen på siden varierer, avhengig av den valgte hovedkontoen.) Siden viser hver transaksjon som har blitt postert til hovedkontoen. Den åpnes vanligvis fra siden **Råbalanseliste**, eller ved å velge **Transaksjoner** på siden **Bilagstransaksjoner**.

Hvis funksjonen Massetilbakeføring er aktivert, kan et eller flere finansbilag nå tilbakeføres fra siden **Bilagstransaksjoner**, og fra journalen som transaksjonen ble postert fra. Unntakene er revaluering av utenlandsk valuta, konsolidering og årsavslutting for økonomimodulen. Disse transaksjonene tilbakeføres fra sidene som årsavslutningen ble kjørt fra.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Årsaker til at transaksjoner ikke kan tilbakeføres

Transaksjoner kan ikke tilbakeføres av følgende årsaker:

- Økonomijournal:

    - Regnskapsperioden er på vent eller permanent lukket:

        - Hvis tilbakeføringsdatoen er i en regnskapsperiode som ikke er åpen, kan ikke transaksjonen tilbakeføres.
        - Hvis transaksjonen støtter registrering av en tilbakeføringsdato, kan transaksjonen fremdeles tilbakeføres ved å endre tilbakeføringsdatoen til en åpen periode.

    - Årsavslutningsprosessen er kjørt:

        - Transaksjonens regnskapsdato er i et regnskapsår som er gått gjennom en årsavslutning. Selv om en periode i regnskapsåret fremdeles kan være åpen, kan den ikke tilbakeføres hvis årsavslutningsprosessen er kjørt for regnskapsåret. Regnskapsåret har en annen status enn periodene i det.
        - Årsavslutningen kan tilbakeføres, og deretter kan transaksjonen tilbakeføres. Denne fremgangsmåten er kanskje ikke et alternativ. Det kan være enklere å angi en tilbakeføringstransaksjon manuelt i en åpen periode i enten det avsluttede regnskapsåret eller det neste regnskapsåret, avhengig av statusen til regnskapsavslutningsprosessen. Hvis en ny transaksjon posteres til en åpen periode i regnskapsåret som er gått gjennom årsavslutningsprosessen, må årsavslutningen kjøres på nytt.

    - Tilbakeføring av transaksjoner pågår allerede:

        - Hvis transaksjonen er i ferd med å tilbakeføres, må denne prosessen fullføres. En separat tilbakeføringsprosess kan ikke utføres. 
        - Når tilbakeføringen er fullført, kan en tilbakeført transaksjon tilbakeføres (det vil si at tilbakeføringen kan tilbakeføres).

    - Utligning:

        - Hvis en eller flere linjer i transaksjonen er finansutlignet ved hjelp av den periodiske oppgaven **Finansutligninger** (**Økonomimodul \> Periodiske oppgaver \>Finansutligninger**), slik at posten finnes i tabellen LedgerTransSettlement, kan ikke transaksjonen tilbakeføres.
        - Finansutligningen kan tilbakeføres, og deretter kan bilaget tilbakeføres.

    - Konserninternt:

        - Hvis transaksjonen er en konsernintern transaksjon, kan den ikke tilbakeføres.
        - Transaksjonen er **ikke** en konsernintern transaksjon, men posteres til en "forfall til"- eller "forfalt fra"-hovedkonto som ble definert på siden **Konserninternt oppsett**.

    - Avsetninger:

        - Hvis det avsatte finansbilaget tilbakeføres, tilbakeføres den avsatte oppføringen og alle de tilsvarende undertransaksjonene for avsetning.
        - De individuelle avsetningsundertransaksjonene kan ikke tilbakeføres.

- Inntektsføringsjournaler:

    - Inntektsføringstransaksjoner ikke kan tilbakeføres.
    - Når omsetning gjenkjennes via inntekstføringsjournalen, posteres bilaget bare til finanskontoer. På sider som **Bilagstransaksjoner** vises derfor transaksjonene som om de bare er økonomimoduloppføringer.

- Revaluering av utenlandsk valuta:

    - Transaksjoner for revaluering av utenlandsk valuta kan tilbakeføres, men bare fra økonomimodulsiden **Revaluering av utenlandsk valuta** som revalueringen ble kjørt fra.
    - Tilbakeføringen kan bare fullføres hvis den er postert til en åpen regnskapsperiode.

- Konsolidering:

    - Konsolideringstransaksjoner kan tilbakeføres, men bare fra siden **Konsolideringstransaksjoner**.
    - Tilbakeføringen kan bare fullføres hvis den er postert til en åpen regnskapsperiode.

- Årsavslutning:

    - Årsavslutningstransaksjoner (både lukkings- og åpningstransaksjoner) kan tilbakeføres på følgende måter:

        - Hvis funksjonen for årsavslutning for økonomimodulen er deaktivert, velger du alternativet **Angre forrige lukking** i dialogboksen **Årsavslutning**.
        - Hvis funksjonen for årsavslutning av økonomimodulen er aktivert, velger du firmaet og regnskapsårspostene som ble opprettet for årsavslutningen på siden **Årsavslutning**, og deretter velger du **Tilbakeføring av årsavslutning**.

    - Legg merke til at tilbakeføringen av årsavslutningen faktisk sletter lukkings- og åpningstransaksjonene. Et tilbakeføringsbilag posteres aldri.

## <a name="accounts-payable"></a>Leverandørreskontro

Flere transaksjonstyper oppdaterer underregnskapet for leverandør. Eksempler inkluderer leverandørfakturaer, leverandørfakturajournaler og reiseregningsrapporter.

Hvis funksjonen Massetilbakeføring er deaktivert, kan transaksjoner tilbakeføres enkeltvis fra siden **Leverandørtransaksjoner** for fakturaer eller siden **Bankkonto** for sjekkbetalinger.

Hvis funksjonen Massetilbakeføring er aktivert, kan en eller flere leverandørtransaksjoner også tilbakeføres fra siden **Bilagstransaksjoner**, og fra journalen som transaksjonene ble postert fra. Leverandørbetalinger kan imidlertid fremdeles bare tilbakeføres fra bankkontoen. I tillegg kan ikke leverandørtransaksjoner tilbakeføres fra siden **Transaksjoner for \<main account\>** for finans. De kan bare tilbakeføres fra siden **Bilagstransaksjoner**.

Legg merke til at noen transaksjoner ikke kan tilbakeføres i det hele tatt. Eksempler inkluderer bestillingsleverandørfakturaer og elektroniske leverandørbetalinger.

### <a name="reasons-why-vouchers-cant-be-reversed"></a>Årsaker til at bilag ikke kan tilbakeføres

Bilag kan ikke tilbakeføres av følgende årsaker:

- Regnskapsperioden er på vent eller lukket:

    - Hvis tilbakeføringsdatoen er i en regnskapsperiode som ikke er åpen, kan ikke transaksjonen tilbakeføres.
    - Hvis transaksjonen støtter registrering av en tilbakeføringsdato, kan transaksjonen fremdeles tilbakeføres ved å endre tilbakeføringsdatoen til en åpen periode.

- Årsavslutningsprosessen for økonomimodulen er kjørt:

    - Transaksjonens regnskapsdato er i et regnskapsår som er lukket i økonomimodulen. Selv om en periode i regnskapsåret fremdeles kan være åpen, kan den ikke tilbakeføres hvis årsavslutningsprosessen er kjørt for regnskapsåret. Regnskapsåret har en annen status enn periodene i det.
    - Årsavslutningen kan tilbakeføres, og deretter kan transaksjonen tilbakeføres. Denne fremgangsmåten er kanskje ikke et alternativ. Det kan være enklere å angi en tilbakeføringstransaksjon manuelt i en åpen periode i enten det avsluttede regnskapsåret eller det neste regnskapsåret, avhengig av statusen til regnskapsavslutningsprosessen. Hvis en ny transaksjon posteres til en åpen periode i regnskapsåret som er gått gjennom årsavslutningsprosessen, må årsavslutningen kjøres på nytt.

- Underregnskapsjournaloppføringen er ikke overført til økonomimodulen:

    - Denne årsaken gjelder bare leverandørfakturaer som ikke er bestillinger.
    - Bruk siden **Underregnskapsjournaler som ennå ikke er overført** til å overføre oppføringen til økonomimodulen. Leverandørfakturaen som ikke er bestilling, kan deretter tilbakeføres fra siden **Leverandørtransaksjoner**.

- Utligning:

    - Transaksjonen (for eksempel en faktura eller betaling) utlignes eller merkes for utligning.

        - Du kan bekrefte om en transaksjon er utlignet eller merket for utligning ved å velge **Vis utligninger** eller **Utligning \> Utligningshistorikk** på siden **Leverandørtransaksjoner**.
        - Du kan også tilbakeføre en utligning fra siden **Leverandørtransaksjoner** (**Utligning \> Angre utligning**) hvis en av transaksjonene må tilbakeføres.

- Bilaget inneholder mer enn en underkontotransaksjon som ble angitt ved hjelp av samme bilagsnummer (en bilagsfeil).
- Fakturaen er ikke godkjent:

    - Hvis det ikke er merket av i **Godkjenning** på fakturaen, kan ikke fakturaen tilbakeføres.

        - I dette tilfellet refererer ikke godkjenningen til godkjenninger i arbeidsflytprosessen, men til **Godkjenning**-alternativet på fakturaen. Dette alternativet brukes for å forhindre at en faktura blir betalt. Den brukes vanligvis for fakturaer for registrering av leverandørfakturaer.

- Transaksjonen i fakturapuljen:

    - En faktura i puljen kan ikke tilbakeføres direkte fra siden **Leverandørtransaksjoner**. I stedet må den tilbakeføres via annulleringsprosessen på siden **Fakturagodkjenningsjournal**.

- Transaksjonen har en overordnet faktura som er korrigert (indisk lokalisering).
- Transaksjonen har egenvekselstatusen **Faktura remittert**.
- Transaksjonen brukes til en delvis avgiftsutligning.
- Transaksjonen inneholder en leverandørkonto, men tilbakeføres fra en feil side, for eksempel siden **Transaksjonene for \<main account\>**:

    - På grunn av dette, selv om funksjonen Massetilbakeføringer er aktivert, kan noen underfinanstransaksjoner bare tilbakeføres fra bestemte sider.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Transaksjonstyper som ikke kan tilbakeføres

Følgende transaksjonstyper kan ikke tilbakeføres:

- Revaluering av utenlandsk valuta:

    - I motsetning til revaluering av utenlandsk valuta i økonomimodulen, kan ikke revaluering av utenlandsk valuta for kunder og kontoer tilbakeføres. I stedet må revalueringen kjøres på nytt ved å bruke fakturadatoen. I dette tilfellet bruker revalueringen valutakursen fra fakturaens dato, og henter egentlig urealisert fortjenesten eller tapet til 0 (null). Resultatet ligner derfor resultatet av tilbakeføring av den forrige revalueringen. Legg imidlertid merke til at det samme beløpet ikke vil bli tilbakeført hvis standard valutakursen ble endret på fakturaen.

- Leverandørfaktura for bestilling:

    - Du må opprette en kreditnota for å tilbakeføre leverandørfakturaen. Hvis du vil ha mer informasjon om hvordan du oppretter en tilbakeføringstransaksjon, kan du se [Opprett en innkjøpsreturordre](../../supply-chain/procurement/tasks/create-purchase-return-order.md).

- Egenveksel
- Bankremburs for eksportforsendelse

## <a name="accounts-receivable"></a>Kundereskontro

Flere transaksjonstyper oppdaterer underregnskapet for kunder. Eksempler inkluderer kundefakturaer fra salgsordrer, kundefakturaer som registreres via økonomijournalen, fritekstfakturaer, kundebetalinger og avskrivinger.

Hvis funksjonen Massetilbakeføring er deaktivert, kan transaksjoner tilbakeføres enkeltvis fra siden **Kundetransaksjoner** for fakturaer eller siden **Bankkontoer** for innbetalinger. Hvis du vil ha informasjon om hvordan du tilbakefører en betaling, kan du se delen [Kontant- og bankbehandling](cant-reverse-transctns.md#cash-and-bank-management) senere i dette emnet.

Hvis funksjonen Massetilbakeføring er aktivert, kan en eller flere kundetransaksjoner også tilbakeføres fra siden **Bilagstransaksjoner**, og journalen som den ble postert fra. Innbetalinger kan imidlertid fremdeles bare tilbakeføres fra bankkontoen, og fritekstfakturaer kan bare tilbakeføres fra den opprinnelige siden (hvis funksjonen for korrigeringer er aktivert). I tillegg kan fortsatt ikke kundetransaksjoner kan tilbakeføres fra siden **Transaksjoner for \<main account\>** for finans. De kan tilbakeføres fra siden **Bilagstransaksjoner**.

Legg merke til at noen transaksjoner ikke kan tilbakeføres. Eksempler på salgsordrekundefakturaer og avskrivinger.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Årsaker til at transaksjoner ikke kan tilbakeføres

Transaksjoner kan ikke tilbakeføres av følgende årsaker:

- Regnskapsperioden er på vent eller permanent lukket:

    - Hvis tilbakeføringsdatoen er i en regnskapsperiode som ikke er åpen, kan ikke transaksjonen tilbakeføres.
    - Hvis transaksjonen støtter registrering av en tilbakeføringsdato, kan transaksjonen fremdeles tilbakeføres ved å endre tilbakeføringsdatoen til en åpen periode.

- Årsavslutningsprosessen for økonomimodulen er kjørt:

    - Transaksjonens regnskapsdato er i et regnskapsår som er gått gjennom en årsavslutning for økonomimodulen. Selv om en periode i regnskapsåret fremdeles kan være åpen, kan den ikke tilbakeføres hvis årsavslutningsprosessen er kjørt for regnskapsåret. Regnskapsåret har en annen status enn periodene i det.
    - Årsavslutningen kan tilbakeføres, og deretter kan transaksjonen tilbakeføres. Denne fremgangsmåten er kanskje ikke et alternativ. Det kan være enklere å angi en tilbakeføringstransaksjon manuelt i en åpen periode i enten det avsluttede regnskapsåret eller det neste regnskapsåret, avhengig av statusen til regnskapsavslutningsprosessen. Hvis en ny transaksjon posteres til en åpen periode i regnskapsåret som er gått gjennom årsavslutningsprosessen, må årsavslutningen kjøres på nytt.

- Underregnskapsjournaloppføringen er ikke overført til økonomimodulen:

    - Denne årsaken gjelder bare fritekstfakturaer.
    - Bruk siden **Underregnskapsjournaler som ennå ikke er overført** til å overføre oppføringen til økonomimodulen. Fritekstfakturaen kan deretter tilbakeføres eller korrigeres opp hvis korrigeringsfunksjonaliteten er aktivert.

- Utligning:

    - Transaksjonen (for eksempel en faktura eller betaling) utlignes eller merkes for utligning.

        - Du kan bekrefte om en transaksjon er utlignet eller merket for utligning ved å velge **Vis utligninger** eller **Utligning \> Utligningshistorikk** på siden **Kundetransaksjoner**.
        - Du kan også tilbakeføre en utligning fra siden **Kundetransaksjoner** (**Utligning \> Angre utligning**) hvis en av transaksjonene må tilbakeføres.

- Transaksjonen inneholder mer enn en underkontotransaksjon som ble angitt ved hjelp av samme bilagsnummer (en bilagsfeil).
- Fakturaen er ikke godkjent:

    - Hvis det ikke er merket av i **Godkjenning** på fakturaen, kan ikke fakturaen tilbakeføres.

        - I dette tilfellet refererer ikke godkjenningen til godkjenninger i arbeidsflytprosessen, men til **Godkjenning**-alternativet på bilagslinjene. Dette alternativet brukes for å forhindre at en faktura blir betalt. Selv om dette alternativet vanligvis brukes i Leverandører, er det også tilgjengelig for Kundefakturaer som registreres via journaler.

- Transaksjonen har en overordnet faktura som er korrigert (indisk lokalisering).
- Transaksjonen inneholder en kundekonto, men tilbakeføres fra en feil side, for eksempel siden **Transaksjonene for \<main account\>**:

    - På grunn av dette, selv om funksjonen Massetilbakeføringer er aktivert, kan noen underfinanstransaksjoner bare tilbakeføres fra bestemte sider.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Transaksjonstyper som ikke kan tilbakeføres

Følgende transaksjonstyper kan ikke tilbakeføres:

- Revaluering av utenlandsk valuta:

    - I motsetning til revaluering av utenlandsk valuta i økonomimodulen, kan ikke revaluering av utenlandsk valuta for kunder og kontoer tilbakeføres. I stedet må revalueringen kjøres på nytt ved å bruke fakturadatoen. I dette tilfellet bruker revalueringen valutakursen fra fakturaens dato, og henter egentlig urealisert fortjenesten eller tapet til 0 (null). Resultatet ligner derfor resultatet av tilbakeføring av den forrige revalueringen. Legg imidlertid merke til at det samme beløpet ikke vil bli tilbakeført hvis standard valutakursen ble endret på fakturaen.

- Transaksjon som har justert kildeskatt
- Kundefaktura for salgsordre:

    - Du må opprette en kreditnota eller retur for å tilbakeføre transaksjonen. Hvis du vil ha mer informasjon om hvordan du oppretter tilbakeføringstransaksjonen, kan du se [Salgsreturer](../../supply-chain/warehousing/sales-returns.md).

- Veksel
- Kassetransaksjon
- Avansert justering
- Rentenota
- Purring
- Bankremburs
- Eksporter forsendelse
- Inntektsføringsjournaler:

    - Når du gjenkjenner inntekt via inntekstføringsjournalen, posteres bilagene til finanskontoer. Derfor vises de som om de bare er økonomimoduloppføringer. Disse oppføringene kan ikke tilbakeføres, fordi inntektsplanen ikke blir åpnet på nytt for å gjenkjenne inntekten igjen.

## <a name="cash-and-bank-management"></a>Kontant- og bankbehandling

Flere transaksjonstyper oppdaterer bankens underfinans via økonomijournalen. Eksempler inkluderer leverandørbetalinger, kundebetalinger og bankoverføringer.

Hvis funksjonen Massetilbakeføring er deaktivert, kan transaksjoner tilbakeføres enkeltvis fra siden **Bankkontoer** for sjekker og innskudd, eller fra siden **Kundetransaksjoner** for kundebetalinger.

Hvis funksjonen Massetilbakeføring er aktivert, kan en eller flere betalingstransaksjoner også tilbakeføres fra siden **Bilagstransaksjoner**, og fra journalen som transaksjonene ble postert fra. Innskudd kan imidlertid fremdeles bare tilbakeføres fra bankkontoen. I tillegg kan fortsatt ikke banktransaksjoner kan tilbakeføres fra siden **Transaksjoner for \<main account\>** for finans. De kan tilbakeføres fra siden **Bilagstransaksjoner**.

Legg merke til at noen transaksjoner ikke kan tilbakeføres. Eksempler inkluderer elektroniske leverandørbetalinger.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Årsaker til at transaksjoner ikke kan tilbakeføres

Transaksjoner kan ikke tilbakeføres av følgende årsaker:

- Regnskapsperioden er på vent eller permanent lukket:

    - Hvis tilbakeføringsdatoen er i en regnskapsperiode som ikke er åpen, kan ikke transaksjonen tilbakeføres.
    - Hvis transaksjonen støtter registrering av en tilbakeføringsdato, kan transaksjonen fremdeles tilbakeføres ved å endre tilbakeføringsdatoen til en åpen periode.

- Årsavslutningsprosessen for økonomimodulen er kjørt:

    - Transaksjonens regnskapsdato er i et regnskapsår som er gått gjennom en årsavslutning for økonomimodulen. Selv om en periode i regnskapsåret fremdeles kan være åpen, kan den ikke tilbakeføres hvis årsavslutningsprosessen er kjørt for regnskapsåret. Regnskapsåret har en annen status enn periodene i det.
    - Årsavslutningen kan tilbakeføres, og deretter kan transaksjonen tilbakeføres. Denne fremgangsmåten er kanskje ikke et alternativ. Det kan være enklere å angi en tilbakeføringstransaksjon manuelt i en åpen periode i enten det avsluttede regnskapsåret eller det neste regnskapsåret, avhengig av statusen til regnskapsavslutningsprosessen. Hvis en ny transaksjon posteres til en åpen periode i regnskapsåret som er gått gjennom årsavslutningsprosessen, må årsavslutningen kjøres på nytt.

- Utligning:

    - Transaksjonen (betaling) utlignes eller merkes for utligning.

        - Du kan bekrefte om en transaksjon er utlignet eller merket for utligning ved å velge **Vis utligninger** eller **Utligning \> Utligningshistorikk** på siden **Leverandørtransaksjoner** eller **Kundetransaksjoner**.
        - Du kan også tilbakeføre en utligning fra siden **Leverandørtransaksjoner** eller **Kundetransaksjoner** (**Utligning \> Angre utligning**) hvis en av transaksjonene må tilbakeføres.

- Transaksjonen inneholder mer enn en underkontotransaksjon som ble angitt ved hjelp av samme bilagsnummer (en bilagsfeil).
- Mellomtransaksjoner:

    - Hvis transaksjonen er relatert til en mellombetaling, kan den ikke tilbakeføres.
    - Hvis mellombetalingen må tilbakeføres, må betalingen først fjernes fra mellomkontoen til banken. Betalingen kan deretter tilbakeføres forutsatt at den oppfyller de andre valideringskriteriene.

- Transaksjonen inneholder en bankkonto, men tilbakeføres fra siden **Transaksjoner for \<main account\>** eller fra feil underregnskap, for eksempel Kunder eller Leverandører:

    - På grunn av dette, selv om funksjonen Massetilbakeføringer er aktivert, kan noen underfinanstransaksjoner bare tilbakeføres fra bestemte sider.

- Bankrevaluering av utenlandsk valuta:

    - Bankens revaluering av utenlandsk valuta kan tilbakeføres. Tilbakeføring kan imidlertid forhindres hvis du fullfører tilbakeføringstrinnene utenom kronologisk rekkefølge. Hvis du for eksempel kjørte revalueringen i mars og april, kan ikke revalueringen i mars tilbakeføres før revalueringen for april er tilbakeført.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Transaksjonstyper som ikke kan tilbakeføres

Følgende transaksjonstyper kan ikke tilbakeføres:

- Leverandørbetalinger som ble foretatt som elektroniske pengeoverføringer (EFT-er)
- Egenveksler
- Veksel

## <a name="fixed-assets"></a>Faste objekter

Flere transaksjonstyper oppdaterer underledgeren for anleggsmidler. Eksempler inkluderer anskaffelser og avskrivning.

Hvis funksjonen Massetilbakeføring er deaktivert, kan transaksjoner tilbakeføres enkeltvis fra siden **Leverandørtransaksjoner**, fra siden **Anleggsmiddeltransaksjoner** eller fra Aktivaleie, avhengig av transaksjonstypen.

Hvis funksjonen Massetilbakeføring er aktivert, kan en eller flere anleggsmiddeltransaksjoner også tilbakeføres fra siden **Bilagstransaksjoner** i journalen som transaksjonene ble postert fra.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Årsaker til at transaksjoner ikke kan tilbakeføres

Transaksjoner kan ikke tilbakeføres av følgende årsaker:

- Regnskapsperioden er på vent eller permanent lukket:

    - Hvis tilbakeføringsdatoen er i en regnskapsperiode som ikke er åpen, kan ikke transaksjonen tilbakeføres.
    - Hvis transaksjonen støtter registrering av en tilbakeføringsdato, kan transaksjonen fremdeles tilbakeføres ved å endre tilbakeføringsdatoen til en åpen periode.

- Årsavslutningsprosessen for økonomimodulen er kjørt:

    - Transaksjonens regnskapsdato er i et regnskapsår som er lukket i økonomimodulen. Selv om en periode i regnskapsåret fremdeles kan være åpen, kan den ikke tilbakeføres hvis årsavslutningsprosessen er kjørt for regnskapsåret. Regnskapsåret har en annen status enn periodene i det.
    - Årsavslutningen kan tilbakeføres, og deretter kan transaksjonen tilbakeføres. Denne fremgangsmåten er kanskje ikke et alternativ. Det kan være enklere å angi en tilbakeføringstransaksjon manuelt i en åpen periode i enten det avsluttede regnskapsåret eller det neste regnskapsåret, avhengig av statusen til regnskapsavslutningsprosessen. Hvis en ny transaksjon posteres til en åpen periode i regnskapsåret som er gått gjennom årsavslutningsprosessen, må årsavslutningen kjøres på nytt.

- Anskaffelser:

    - Hvis anskaffelsen skjedde på en leverandørfaktura for bestilling, må tilbakeføringen utføres ved å angi en leverandørkreditnota. Hvis du vil ha mer informasjon om hvordan du angir tilbakeføringstransaksjon, kan du se [Opprett en innkjøpsreturordre](../../supply-chain/procurement/tasks/create-purchase-return-order.md).
    - Anskaffelsen skjedde på en prosjekttransaksjon.
    - Anskaffelsen kan ikke tilbakeføres etter at avskrivningen er postert for aktivumet. Avskrivningen må tilbakeføres før anskaffelsen kan tilbakeføres.
    - Hvis statusen til verdimodellen eller avskrivningstablået for en anskaffelse av anleggsmidler ikke er åpen, kan ikke transaksjonen tilbakeføres.

- Avhendinger:

    - Avhending gjøres via en fritekstfaktura:

        - Korrigering av en fritekstfaktura blokkeres hvis den inneholder et anleggsmiddel. Hvis anleggsmidlet derimot avhendes via en journal, kan fritekstfakturaen tilbakeføres fra anleggsmiddelposten.

    - Hvis statusen til verdimodellen eller avskrivningstablået for en anskaffelse av anleggsmidler ikke er åpen, kan ikke transaksjonen tilbakeføres.

- Avskrivning:

    - Avskrivningen **kan** tilbakeføres hvis etterfølgende avskrivning også blir postert. Du vil imidlertid få en advarsel, fordi denne tilnærmingen er en god fremgangsmåte.
    - Hvis statusen til verdimodellen eller avskrivningstablået for en anskaffelse av anleggsmidler ikke er åpen, kan ikke transaksjonen tilbakeføres.

- Det finnes transaksjoner (eller tilbakeføringstransaksjoner) for et bestemt aktivum og aktivatablået for bilagets transaksjonsdato eller senere.
- Transaksjonen inneholder en aktivakonto, men tilbakeføres fra siden **Transaksjoner for \<main account\>** eller fra feil underregnskap, for eksempel Kunder eller Leverandører:

    - På grunn av dette, selv om funksjonen Massetilbakeføringer er aktivert, kan noen underfinanstransaksjoner bare tilbakeføres fra bestemte sider.
    - Hvis en anskaffelse skjer på en leverandørfaktura som ikke er en bestilling, eller en journal for leverandørfaktura, kan den bare tilbakeføres fra siden **Leverandørtransaksjoner** i Leverandører.
    - Hvis et aktivum anskaffes ved hjelp av aktivaleie, kan det tilbakeføres fra **Gjeldstransaksjoner** i Aktivaleie.
