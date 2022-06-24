---
title: Formeldesigner for TDS-beregninger
description: Denne artikkelen viser et eksempel på hvordan TDS (Tax Deducted at Source) beregnes basert på formelen som er definert for hver TDS-avgiftskode i TDS-gruppen som er knyttet til transaksjonen.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1196f7258c898a55f3f29ddce7457e6f527185d8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889868"
---
# <a name="formula-designer-for-tds-calculations"></a>Formeldesigner for TDS-beregninger

[!include [banner](../includes/banner.md)]

Denne artikkelen viser et eksempel på hvordan TDS (Tax Deducted at Source) beregnes basert på formelen som er definert for hver TDS-avgiftskode. TDS-avgiftskoder defineres i TDS-gruppen som er knyttet til transaksjonen. Før du utformer TDS-formler, må du fullføre det grunnleggende oppsettet som kreves for TDS, som vist i fremgangsmåten nedenfor. 

- Konfigurer TDS-komponentgrupper ved å bruke siden **Komponentgrupper for kildeskatt**. 
- Konfigurer TDS-komponenter og knytt TDS-komponentgruppen til TDS-komponentene ved å bruke siden **Komponenter for kildeskatt**. 
- Konfigurer TDS-avgiftskoder, og knytt TDS-komponenter til avgiftskodene ved å bruke siden **Kildeskattkoder**. 
- Konfigurer TDS-avgiftsgrupper ved å bruke siden **Kildeskattgrupper**. Knytt deretter TDS-avgiftskodene til avgiftsgruppen, og definer formelen ved hjelp av **Formeldesigner**-siden. 

**Eksempelformel**

I dette eksemplet er TDS-gruppen Leie knyttet til en innkjøpsfaktura som er opprettet for leverandør A. Fakturabeløpet er $ 100 000. Se TDS-beregningen for fakturaen i tabellen nedenfor.

| TDS-gruppe                                                   | TDS-avgiftskoder knyttet til TDS-gruppen | Verdi              | Skattbart grunnlag (Formeldesigner) | Beregningsuttrykk (Formeldesigner) | Grunnbeløp | Beregnet TDS-beløp |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| Leie                                                         | TDS (TDS-komponent – TDS)                | 10 %                | Bruttobeløp                      |                                            | 100 000      | 10 000                 |
| Tilleggsavgift (TDS-komponent – tilleggsavgift)                         | 10 %                                     | Ekskl. bruttobeløp | +TDS                              |                   10000                    | 1 000        |                       |
| PE-Cess (TDS-komponent – PE-Cess)                            | 2 %                                      | Ekskl. bruttobeløp | +TDS+tilleggsavgift                    |                   11000                    | 220         |                       |
| SHE Cess (TDS-komponent – SHE Cess)                          | 1 %                                      | Ekskl. bruttobeløp | +TDS+tilleggsavgift                    |                   11000                    | 110         |                       |
| **Total** **TDS** **beregnet** **for** **fakturaen** | **11 330**                               |                    |                                   |                                            |             |                       |

Bilagsoppføringene opprettes på følgende måte.

| Konto           | Debet  | Kreditt |
| ----------------- | ------ | ------ |
| Leie              | 100 000 |        |
| Leverandør A          |        | 100 000 |
| Leverandør A          | 11 330  |        |
| TDS skyldig       |        | 10 000  |
| Tilleggsavgift skyldig |        | 1 000   |
| PE-Cess skyldig   |        | 220    |
| SHE Cess skyldig  |        | 110    |
