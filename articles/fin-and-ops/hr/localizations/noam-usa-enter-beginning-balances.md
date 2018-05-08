---
title: "Angi startsaldoer for lønn"
description: "Emnet beskriver fremgangsmåten for å angi startsaldoer for inntektskoder, fradrag, fordeler og avgifter. Denne informasjonen er nyttig for partnere for å overføre eller overføre data til en ny lønnsimplementering fra et annet system."
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 93333757995c874c2cf03514acff28a54ae7f787
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="enter-payroll-beginning-balances"></a>Angi startsaldoer for lønn

[!include [banner](../../includes/banner.md)]

Emnet beskriver fremgangsmåten for å angi startsaldoer for inntektskoder, fradrag, fordeler og avgifter. Denne informasjonen er nyttig for partnere som overfører eller overfører data til en ny lønnsimplementering fra et annet system. Ved klargjøring for å angi startsaldoer for lønn, kontrollerer vi følgende informasjon:

> * Ansattposter er angitt og tilgjengelige i systemet
> * Følgende data blir definert og tilordnet til ansatte:
> 
> > * Lønnssykluser og lønnsperioder
> > * Inntektskoder
> > * Avgifter
> > * Fordeler og fradrag
> 
> * Firmaet skal har valgt en dato der startsaldoer for lønn kan angis.
> 
> * Informasjonen ble samlet om alle inntekter, fordeler/fradrag, fordelsbidrag, avgifter for ansatte, og arbeidstakeravgifter og arbeidsgiveravgifter deres og år til dato-beløp fra det gamle systemet.

Når du planlegger å skrive inn startsaldoer, bør du vurdere hvor detaljert dataene skal være. De fleste bedrifter angir et enkelt, konsolidert år til dato-beløp. Hvis du trenger mer informasjon, kan du imidlertid angi saldoer kvartalsvis. Når nødvendig detaljnivå bestemmes, bestemmes også hvor mange manuelle lønnsoppgaver som må opprettes for hver arbeider. For ett enkelt år til dato-beløp trengs det bare ett manuelt utdrag for hver ansatt. Hvis vil gjøre dette bruker du år-til-dato-beløp fra den siste lønnsoppgaven fra forrige systemet som beløp som angis i det nye lønningssystemet.

Følgende eksempel viser hvordan du kan angi startsaldoer for ansattes lønn, inkludert inntektskoder, fordeler/fradrag og avgifter. I et eksempel fra virkeligheten vil du ha et linjeelement for hver inntektskode, fordelsfradrag, fordelsbidrag, ansattavgift og arbeidsgiveravgift med beløpet som er angitt som år-til-dato-beløpet. Ved hjelp av den listen med koder og beløp, følger du trinnene for å opprette en manuell inntekts- og lønnsoppgave med regnskap deaktivert for å overføre startsaldoer til lønnsformål.  Du kan deaktivere regnskap fordi du ikke vil postere denne lønnsoppgavens startsaldo i Finans. Som ble gjort i det gamle systemet og kommer til det nye systemet når du angir startsaldoer i økonomimodulen.

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a>A. Slik konfigurerer du inntektskoder som skal brukes på startsaldoer for lønn
Når du angir startssaldoer for lønn, må du kontrollere at inntektskodene som du vil bruke, er konfigurert med alternativet "Tillat redigering av inntektsoppgavesatser". Dermed kan du taste beløpet fra det gamle systemet manuelt. 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a>B. Opprette inntektsoppgaver for en ansatt med en startsaldo
Dette trinnet oppretter manuelt en inntektsoppgave for hver arbeider for den siste lønnsperioden av det gamle systemet, noe som oppretter inntektsoppgavelinjene i det nye lønnssystemet. Angi én linje per inntektskode og år-til-dato-beløp og timer. Eksempeltrinnene er som følger:

1. Åpne **Alle inntektsoppgaver**-siden og klikk **Ny**.  

Angi følgende: 

| Felt      | Verdi                 |
|------------|-----------------------|
| Arbeider     | Michael Redmond       |
| Lønnssyklus  | sm                    |
| Lønnsperiode | 16/6/2017 – 30/06/2017 |

2. I kategorien **Linje i inntektsoppgave** skriver du inn følgende:

Linje 1: kategorien **Linje i inntektsoppgave**

| Felt            | Verdi       |
|------------------|-------------|
| Inntektskode    | Vanlig lønn |
| Antall         | 1,00        |
| Område             | 30 000      |
| Kategorien Linjedetaljer |             |
| Manuell           | (merket)    |

Linje 2: kategorien **Linje i inntektsoppgave**

| Felt            | Verdi    |
|------------------|----------|
| Inntektskode    | Bonus    |
| Antall         | 1.0000   |
| Sats             | 4250.00  |
| Kategorien Linjedetaljer |          |
| Manuell           | (merket) |

Linje 3: kategorien **Linje i inntektsoppgave**

| Felt           | Verdi      |
|-----------------|------------|
| Inntektskode   | Provisjon |
| Antall        | 1.0000     |
| Sats            | !,299,00   |
| Sats            | 1,299.00   |
| Kategorien Linjedetaljer |            |
| Manuell          | (merket)   |

> [!NOTE]
> Å sette **Manuell**-glidebryteren til **Ja** i kategorien **Linjedetaljer** for hver inntektsoppgave er nøkkelen til å få angitt startsaldoer for lønn for hver arbeider.

3. På **Handling**-ruten klikker du **Frigi inntektsoppgave** USA-FED-ER-FICA.

4. På **Handling**-ruten klikker du **Lønnsoppgave** for å åpne siden **Generer lønnsoppgaver**, og angi følgende:

| Felt              | Verdi     |
|--------------------|-----------|
| Betalingsdato       | 30/6/2017 |
| Betalingskjøringstype   | Manuell    |
| Deaktiver regnskap |   Ja     |

> [!NOTE] 
> Dette er bare tilgjengelig når betalingens kjøretype er manuell, og når brukeren ønsker å deaktivere regnskap på betalingskjøringen.

Klikk **OK** og lukk **Infolog**.

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a>Hvorfor må glidebryteren Deaktiver regnskap være satt til Ja ved generering av lønnsoppgaver?
Hvis du setter du glidebryteren til **Ja**, forhindres linjene i lønnsoppgaven fra å distribueres til økonomimodulen. Beløpene i økonomimodulen ble oppdatert tidligere da kontosaldoer fra det gamle systemet ble angitt. Ved å angi startsaldoer for lønn kan du generere rapporter som inkluderer informasjon fra foregående år, i tillegg til for å identifisere grenser for fordeler og skatteformål.   

### <a name="c-create-pay-statements-for-employees"></a>C. Opprette lønnsoppgaver for ansatte
Når du har generert lønnsoppgaver med startsaldoer, må du kontrollere at lønnsoppgavene gjenspeile lønnsdataene riktig. Du må også oppdatere informasjon om fordeler og avgifter manuelt for å samsvare med verdiene i det forrige lønningssystemet. Når du har bekreftet at beløpene fra forrige lønningssystem svarer til beløpene på de gjeldende lønnsoppgavene, må du fullføre lønnsoppgavene.

1. Åpne siden **Alle lønnsoppgaver**.

2. Merk den sist genererte lønnsoppgaven for Michael Redmond

3. Klikk **Rediger** for å åpne **Lønnsoppgave**-siden.

4. Åpne kategorien **Fordelsfradrag** og angi følgende:

|       Felt       |      Verdi       |
|-------------------|------------------|
|      Fordel      | Fradragsbeløp |
|       401K        |   Delta    |
|      Tannforsikring       |      SubSp       |
| Utgifter til pass og stell av barn |   Delta    |
|      Syn       |      SupSp       |

5. I kategorien **Fordelsbidrag** angir du følgende:

|  Felt  |        Verdi        |
|---------|---------------------|
| Fordel | Bidragsbeløp |
|  401K   |     Delta     |
| Tannforsikring  |        SubSp        |
| Syn  |        SubSp        |

6. Angi følgende informasjon i kategorien **Avgiftsfradrag**:

| Felt           | Verdi            |
|-----------------|------------------|
| Mva-kode        | Fradragsbeløp |
| USA-FED-ER-FICA | 1600.00          |
| USA-FED-ER-MEDI | 825.75           |

7. Angi følgende informasjon i kategorien **Avgiftsbidrag**:

8. Klikk **Beregn**.
   > [!IMPORTANT] 
   > Valider totalene i lønnsoppgaven for at de samsvarer med år-til-dato arbeiderens gamle system. Det kan hende du vil vente med å sluttføre i det neste trinnet for å gjøre en generel validering av alle lønnsoppgaver samlet. Etter validering kjører du gjennom alle lønnsoppgaver og sluttfører dem.

Den samme prosessen kan utføres kvartalsvis om nødvendig for alle tidligere kvartaler i hvert år. Dette er bare nødvendig hvis kunden skal vise dataene kvartalsvis uten å gå tilbake til det gamle systemet.

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a>Hvis du gjør en feil når du angir startsaldoer for en ansatt
Det er mulig å tilbakeføre, og skrive inn transaksjoner på nytt. Hvis du vil tilbakeføre transaksjonen, trenger du bare å fullføre følgende trinn på siden **Alle lønnsoppgaver**.

1. Klikk **Tilbakefør**.

2. Klikk **Ja** når meldingen «Når du tilbakefører denne lønnsoppgaven, opprettes en lønnsoppgave for tilbakeføring for å motregne denne lønnsoppgaven. Ingen lønnsoppgave kan redigeres. Du vil tilbakeføre denne lønnsoppgaven?" vises. 

Når du tilbakefører lønnsoppgaven, kan du generere en ny lønnsoppgave for arbeideren fra inntektsoppgaven som du opprettet tidligere. Husk å rette opp eventuelle ukorrekte linjer på inntekstoppgaven før du genererer den nye lønnsoppgaven, og deretter generere nye lønnsoppgaver med riktig beløp. 

