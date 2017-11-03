---
title: Posteringsdefinisjoner
description: Denne artikkelen inneholder eksempler som viser hvordan posteringsdefinisjoner brukes for bestillingsdisposisjoner og budsjettbevilgninger.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 004f3f24ec410d9f0e7d1e7264ec2730b9467410
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="posting-definition-examples"></a>Eksempler på posteringsdefinisjoner

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder eksempler som viser hvordan posteringsdefinisjoner brukes for bestillingsdisposisjoner og budsjettbevilgninger.

Før du leser dette emnet, bør du være kjent med posteringsdefinisjoner og posteringsdefinisjoner for transaksjon. Hvis du vil ha informasjon, se [Posteringsdefinisjoner](posting-definitions.md). Eksemplene nedenfor kan settes opp på siden **Posteringsdefinisjoner**. Hvert eksempel inneholder disse delene:

-   Posteringsdefinisjon – samsvarskriterier
-   Posteringsdefinisjon – genererte oppføringer
-   Transaksjoner med kontoer, dimensjonsverdiene og beløp
-   Finansoppføringer som er generert fra posteringsdefinisjonen

Når et samsvar oppstår mellom kontoer og dimensjonsverdier i **Samsvarskriterier**-ruten for posteringsdefinisjonen og kontoene og dimensjonsverdiene for transaksjonen, genereres finansoppføringer basert på **Genererte oppføringer**-ruten for posteringsdefinisjonen. 
> [!NOTE]
> Bruk siden **Definisjoner for transaksjonspostering** for å knytte en posteringsdefinisjon til en bestemt transaksjonstype. Når du har knyttet en posteringsdefinisjon til en transaksjonstype og valgt**Bruk posteringsdefinisjoner** på siden **Parametere for økonomimodul**, må alle transaksjoner med den valgte transaksjonstypen bruke posteringsdefinisjoner.

## <a name="example-purchase-order-encumbrances"></a>Eksempel: bestillingsdisposisjoner
Når du aktiverer disposisjonsbehandling ved å velge **Aktiver disposisjonsprosess** på **Økonomiparametere**, må posteringsdefinisjoner brukes til å registrere disposisjoner i økonomimodulen for alle kontoer som skal reserveres. I de fleste tilfeller reserveres alle utgiftskontoer i balansen. 

Posteringsdefinisjoner for disposisjoner defineres for **Innkjøp**-modulen på **Posteringsdefinisjoner**-siden. Deretter, i **Innkjøp**-området på siden **Definisjoner for transaksjonspostering**, kan du velge **Bestilling**-transaksjonstypen for å knytte posteringsdefinisjonen til bestillinger. 

Alle bilagstransaksjoner for bestillingsdisposisjoner må være i balanse (det vil si debet må være lik kredit) i hver unike dimensjon på et bilag.

### <a name="posting-definition--match-criteria"></a>Posteringsdefinisjon – samsvarskriterier

| Kontostruktur       | Kontonummer for samsvar | Prioritet |
|-------------------------|----------------------|----------|
| Kontostruktur – resultat | \*                   | 1        |

*En tom verdi i feltet **Samsvarskontonummer** betyr at alle samsvarende kontoer i den definerte kontostrukturen er en del av den samsvarende regelen.

### <a name="posting-definition--generated-entries"></a>Posteringsdefinisjon – genererte oppføringer

| Kontostruktur | Generert kontonummer                    | Generert debet/kreditt |
|-------------------|---------------------------------------------|------------------------|
| Saldo           | 300143 - - (disposisjonskonto)             | Lik                   |
| Saldo           | 300144 -- (Reserver for disposisjonskonto) | Balanse              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Transaksjoner med kontoer, dimensjonsverdiene og beløp

Kontoene og dimensjonsverdiene kommer fra regnskapsdistribusjonene du angir for en bestillingslinje, eller fra kontoer og dimensjoner som genereres automatisk basert på standardinnstillingene for leverandører, varer, kategorier og maler for dimensjonen.

| Konto + dimensjoner           | Debet  | Kreditt | Kommentar |
|--------------------------------|--------|--------|---------|
| 606400-OU\_1-OU\_3566-opplæring | 250,00 |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Finansoppføringer som er generert fra posteringsdefinisjonen

Genererte finansoppføringer opprettes for å registrere disposisjonene.

| Konto + dimensjoner           | Debet  | Kreditt | Kommentar |
|--------------------------------|--------|--------|---------|
| 300143-OU\_1-OU\_3566-opplæring | 250,00 |        |         |
| 300144-OU\_1-OU\_3566-opplæring |        | 250,00 |         |

I dette eksemplet samsvarer alle kontoer som inngår i Kontostruktur – resultat, kriteriene for posteringsdefinisjon. Når 606500-OU\_1-OU\_3566-opplæring blir evaluert, opprettes derfor genererte oppføringer for kontoene som er definert i **Genererte oppføringer**-ruten for posteringsdefinisjonen.

## <a name="example-budget-appropriations"></a>Eksempel: budsjettbevilgninger
Når du aktiverer budsjettbevilgning ved å velge **Aktiver budsjettbevilgning** på **Økonomiparametere**-siden, må posteringsdefinisjoner brukes til å registrere budsjettregisteroppføringer i økonomimodulen. Når en budsjettkontrollkonfigurasjon er aktivert og er slått på, kan posteringsdefinisjoner og posteringsdefinisjoner for transaksjon brukes til å støtte registreringen av oppføringer for avsetninger, endringer, overføringer, prosjekter, anleggsmidler og forsynings- og behovsprognoser til økonomimodulen. 

Hvis du vil definere en posteringsdefinisjon for budsjettregistreroppføringer som har budsjettypen **Opprinnelig budsjett** og som har avsetninger aktivert, velger du **Budsjett**-modulen på **Posteringsdefinisjoner**-siden. Deretter, i **Budsjett**-området på siden **Definisjoner for transaksjonspostering**, kan du kan bruke budsjettkoder for å knytte posteringsdefinisjonen til budsjettregisteroppføringer med budsjettypen **Opprinnelig budsjett**. 

Når budsjettbevilgninger og posteringsdefinisjoner er aktivert, registreres budsjettregisteroppføringene for budsjettkontroll, og i økonomimodulen.

### <a name="posting-definition--match-criteria"></a>Posteringsdefinisjon – samsvarskriterier

| Kontostruktur       | Kontonummer for samsvar | Prioritet |
|-------------------------|----------------------|----------|
| Kontostruktur – resultat | \*                   | 1        |

*En tom verdi i feltet **Samsvarskontonummer** betyr at alle samsvarende kontoer i den definerte kontostrukturen er en del av den samsvarende regelen.

### <a name="posting-definition--generated-entries"></a>Posteringsdefinisjon – genererte oppføringer

| Kontostruktur | Generert kontonummer              | Generert debet/kreditt |
|-------------------|---------------------------------------|------------------------|
| Kontostruktur | 300145 - - (konto for estimert omsetning) | Lik                   |
| Kontostruktur | 300146 -- (bevilgningskonto)     | Balanse              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Transaksjoner med kontoer, dimensjonsverdiene og beløp

Du angir kontoene, dimensjonsverdiene og beløpene for budsjettkontooppføringen på siden **Budsjettregisteroppføring**.

| Konto + dimensjoner           | Debet | Kreditt | Kommentar |
|--------------------------------|-------|--------|---------|
| 606400-OU\_1-OU\_3566-opplæring |       | 250,00 |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Finansoppføringer som er generert fra posteringsdefinisjonen

Genererte finansposter opprettes for å registrere det opprinnelige budsjettet i hver dimensjon.

| Konto + dimensjoner           | Debet  | Kreditt | Kommentar |
|--------------------------------|--------|--------|---------|
| 300145-OU\_1-OU\_3566-opplæring |        | 250,00 |         |
| 300146-OU\_1-OU\_3566-opplæring | 250,00 |        |         |

I dette eksemplet samsvarer alle kontoer som inngår i Kontostruktur – resultat, kriteriene for posteringsdefinisjon. Når 606400-OU\_1-OU\_3566-opplæring blir evaluert, opprettes derfor de genererte finanspostene.






