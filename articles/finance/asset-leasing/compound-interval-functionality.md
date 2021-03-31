---
title: Funksjon for sammensetningsintervall
description: Dette emnet inneholder informasjon som hjelper deg å velge mellom månedlige, kvartalsvise og årlige sammensetningsintervaller.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 689165314f664f514c1bef98e74e823cf48286c9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225568"
---
# <a name="compounding-interval-functionality"></a>Funksjonalitet for sammensetningsintervall

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet inneholder informasjon som hjelper deg å velge mellom månedlige, kvartalsvise og årlige sammensetningsintervaller. Funksjonen for sammensetningsintervall brukes til å bestemme antallet sammensetningsperioder per år i betalingsplanen for en leieavtale. Hvert av de fire eksemplene i dette emnet viser hvordan betalingsplanen for en leieavtale ser ut for et annet intervall.

Du kan ikke velge et sammensetningsintervall med en lavere frekvens enn betalingsfrekvensen i leieavtalen. Et kvartalsvis sammensetningsintervall kan for eksempel ikke brukes med en månedlig betalingsfrekvens, og et årlig sammensetningsintervall kan ikke brukes med en halvårlig betalingsfrekvens. Hvis du prøver å velge et sammensetningsintervall med en lavere frekvens enn betalingsfrekvensen i leieavtalen, får du en feilmelding.

> [!NOTE]
> I alle fire eksempler i dette emnet samsvarer sammensetningsintervallet med betalingsfrekvensen.

## <a name="examples"></a>Eksempler

### <a name="setup-for-all-four-leases"></a>Oppsett for alle fire leieavtaler

Tabellene nedenfor viser verdiene som er angitt i fanene **Generelt** og **Linjer i betalingsplan** for de fire leieavtalene som brukes i eksemplene.

**Fanen Generelt**

| Felt                      | Verdi                        |
|----------------------------|------------------------------|
| Trinnvis lånerente | **5 %**                       |
| Annuitetstype               | **Vanlig annuitet**         |
| Sammensetningsintervall       | Se de individuelle eksemplene. |
| Betalingsfrekvens          | **Månedlig**                  |
| Startdato          | **01.01.2020**                 |

**Fanen Linjer i betalingsplan**

| Felt             | Verdi                        |
|-------------------|------------------------------|
| Startdato        | **01.01.2020**                 |
| Perioder           | **120**                      |
| Periodeintervall   | **Måneder**                   |
| Sluttdato          | **31.12.2029**               |
| Betalingsfrekvens | Se de individuelle eksemplene. |
| Betalingsbeløp    | **50,000**                   |

### <a name="lease-1-monthly-compounding-interval-and-monthly-payment-frequency"></a>Leieavtale 1: månedlig sammensetningsintervall og månedlig betalingsfrekvens

Tabellen nedenfor viser de første 12 månedene av betalingsplanen. Vær oppmerksom på følgende detaljer:

- Verdien i kolonnen Periode øker med 1 hver måned, fordi hver måned er et nytt sammensetningsintervall.
- I formelen i kolonnen Nåværende verdi divideres frekvensen med 12, fordi det finnes 12 sammensetningsperioder per år. Eksponenten (det vil si sifferet i hevet skrift) er lik verdien i kolonnen Periode.

| Periode | Måned | Dato       | Betalingsbeløp | Nåværende verdi                                       |
|--------|-------|------------|----------------|-----------------------------------------------------|
| 1      | 1     | 31.01.2020  | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>1</sup> = 49 792,53  |
| 2      | 2     | 29.02.2020  | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>2</sup> = 49 585,92  |
| 3      | 3     | 31.03.2020  | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>3</sup> = 49 380,17  |
| 4      | 4     | 30.04.2020  | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>4</sup> = 49 175,28  |
| 5      | 5     | 31.05.2020  | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>5</sup> = 48 971,23  |
| 6      | 6     | 30.06.2020  | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>6</sup> = 48 768,03  |
| 7      | 7     | 31.07.2020  | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>7</sup> = 48 565,67  |
| 8      | 8     | 31.08.2020  | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>8</sup> = 48 364,15  |
| 9      | 9     | 30.09.2020  | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>9</sup> = 48 163,47  |
| 10     | 10    | 31.10.2020 | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>10</sup> = 47 963,62 |
| 11     | 11    | 30.11.2020 | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>11</sup> = 47 764,61 |
| 12     | 12    | 31.12.2020 | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>12</sup> = 47 566,41 |

### <a name="lease-2-quarterly-compounding-interval-and-quarterly-payment-frequency"></a>Leieavtale 2: kvartalsvis sammensetningsintervall og kvartalsvis betalingsfrekvens

Tabellen nedenfor viser de første 12 månedene av betalingsplanen. Vær oppmerksom på følgende detaljer:

- Verdien i kolonnen Periode øker med 1 hver tredje måned (det vil si hvert kvartal), fordi hvert kvartal er et nytt sammensetningsintervall.
- I formelen i kolonnen Nåværende verdi divideres frekvensen med 4, fordi det finnes fire sammensetningsperioder per år. Eksponenten er lik verdien i kolonnen Periode.

| Periode | Måned | Dato       | Betalingsbeløp | Nåværende verdi                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.01.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 0           |
| 1      | 2     | 29.02.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 0           |
| 1      | 3     | 31.03.2020  | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 49 382,72 |
| 2      | 4     | 30.04.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 0           |
| 2      | 5     | 31.05.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 0           |
| 2      | 6     | 30.06.2020  | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 48 773,05 |
| 3      | 7     | 31.07.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 0           |
| 3      | 8     | 31.08.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 0           |
| 3      | 9     | 30.09.2020  | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 48 170,92 |
| 4      | 10    | 31.10.2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 0           |
| 4      | 11    | 30.11.2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 0           |
| 4      | 12    | 31.12.2020 | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 47 576,21 |

> [!NOTE]
> Hvis annuitetstypen endres til **Annuitetsforfall**, er betalingen på begynnelsen av kvartalet i stedet for på slutten av det.

### <a name="lease-3-semiannual-compounding-interval-and-semiannual-payment-frequency"></a>Leieavtale 3: halvårlig sammensetningsintervall og halvårlig betalingsfrekvens

Tabellen nedenfor viser de første 12 månedene av betalingsplanen. Vær oppmerksom på følgende detaljer:

- Verdien i kolonnen Periode øker med 1 hver sjette måned (det vil si hvert halvår), fordi hvert halvår er et nytt sammensetningsintervall.
- I formelen i kolonnen Nåværende verdi divideres frekvensen med 2, fordi det finnes to sammensetningsperioder per år. Eksponenten er lik verdien i kolonnen Periode.

| Periode | Måned | Dato       | Betalingsbeløp | Nåværende verdi                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.01.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 2     | 29.02.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 3     | 31.03.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 4     | 30.04.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 5     | 31.05.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 6     | 30.06.2020  | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 48 780,49 |
| 2      | 7     | 31.07.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 8     | 31.08.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 9     | 30.09.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 10    | 31.10.2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 11    | 30.11.2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 12    | 31.12.2020 | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 47 590,72 |

> [!NOTE]
> Hvis annuitetstypen endres til **Annuitetsforfall**, skjer betalingen i januar og juli i stedet for juni og desember.

### <a name="lease-4-annual-compounding-interval-and-annual-payment-frequency"></a>Leieavtale 4: årlig sammensetningsintervall og årlig betalingsfrekvens

Tabellen nedenfor viser de første 12 månedene av betalingsplanen. Vær oppmerksom på følgende detaljer:

- Verdien i kolonnen Periode øker med 1 hver 12. måned (det vil si hvert år), fordi hvert år er et nytt sammensetningsintervall.
- I formelen i kolonnen Nåværende verdi divideres frekvensen med 1, fordi det finnes én sammensetningsperiode per år. Eksponenten er lik verdien i kolonnen Periode.

| Periode | Måned | Dato       | Betalingsbeløp | Nåværende verdi                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.01.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 2     | 29.02.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 3     | 31.03.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 4     | 30.04.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 5     | 31.05.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 6     | 30.06.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 7     | 31.07.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 8     | 31.08.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 9     | 30.09.2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 10    | 31.10.2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 11    | 30.11.2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 12    | 31.12.2020 | 50 000,00      | 50 000 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 47 619,05 |

> [!NOTE]
> Hvis annuitetstypen endres til **Annuitetsforfall**, skjer betalingen i januar i stedet for desember.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]