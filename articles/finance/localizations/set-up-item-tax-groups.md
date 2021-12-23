---
title: Definere vareavgiftgrupper
description: Dette emnet forklarer hvordan du konfigurere vareavgiftgrupper i avgiftsberegningstjenesten.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 88dd8e2fd9d4d4e5172dcc7b1bd27a70a2f59f03
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883869"
---
# <a name="set-up-item-tax-groups"></a>Definere vareavgiftgrupper

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurere vareavgiftgrupper i avgiftsberegningstjenesten. Den forklarer også hvordan du definerer relevansregelmatrisen for vareavgiftgruppe og konfigurerer linjer i matrisen.

Konseptet med vareavgiftgrupper i avgiftsberegningstjenesten er lik konseptet med vareavgiftsgrupper i Microsoft Dynamics 365 Finance. De er grupper av avgiftskoder. Avgiftsberegningstjenesten bruker skjæringspunktet mellom en avgiftgruppe og en vareavgiftsgruppe til å bestemme avgiftskodene.

> [!IMPORTANT]
> Oppsettet av vareavgiftsgrupper i avgiftsberegningstjenesten er juridisk enhet–agnostisk. Du kan bare fullføre dette oppsettet i RCS (Regulatory Configuration Service) én gang. Når du aktiverer avgiftsberegningstjenesten i Finance, synkroniseres vareavgiftsgrupper automatisk for den valgte juridiske enheten.

## <a name="set-up-an-item-tax-group"></a>Definere en vareavgiftgruppe 

Følg disse trinnene for å konfigurere en vareavgiftsgruppe.

1. Logg på [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Gå til **Arbeidsområder** \> **Globaliseringsfunksjoner** \> **Avgiftsberegning**.
3. Velg funksjonen og versjonen du vil sette opp, og velg deretter **Rediger**.
4. Velg **Konfigurasjonsversjon** i kategorien **Generelt**.
5. Velg **Behandle kolonne** i kategorien **Vareavgiftsgruppe**. Hvis du definerer en vareavgiftsgruppe for første gang, angis feltene i dialogboksen **Administrer kolonne** automatisk.
6. I listen til venstre utvider du **Linjer**-noden og merker av i avmerkingsboksen for **Vareavgiftsgruppe**.

    ![Vareavgiftsgruppe som er valgt under Linjer-noden i dialogboksen Behandle kolonner.](media/select-item-tax-group.png)

7. Velg høyre pil-knapp for å legge til **Vareavgiftsgruppe** i listen **Valgte kolonner**-listen til høyre.

    ![Vareavgiftsgruppe som er lagt til i listen Valgte kolonner.](media/add-item-tax-group.png)

8. Velg **OK**.

## <a name="configure-an-item-tax-group"></a>Konfigurere en vareavgiftgruppe

Når du har definert en vareavgiftsgruppe, opprettes matrisen for relevansregler. Du kan legge til linjer i matrisen for å konfigurere vareavgiftsgruppen.

1. Velg **Legg til** i kategorien **Vareavgiftsgruppe**.
2. I **Vareavgiftsgruppe**-feltet skriver du inn navnet på vareavgiftgruppen.

    > [!IMPORTANT]
    > Vi anbefaler at du begrenser navnet på vareavgiftgruppen for vare til 10 tegn. Dette navnet synkroniseres med Finance, som har en grense på 10 tegn for navnene til mva-gruppene for varer.

3. I feltet **Avgiftskoder** merker du av for hver avgiftkode du vil ta med i vareavgiftsgruppen. Du kan inkludere flere avgiftskoder i én vareavgiftsgruppe.

    ![Flere avgiftskoder valgt i Avgiftskoder-feltet.](media/multiple-tax-codes-selection.png)

4. Gjenta trinn 1 til og med 3 for å legge til flere vareavgiftsgrupper.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
