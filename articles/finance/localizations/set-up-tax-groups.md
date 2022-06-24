---
title: Definere avgiftsgrupper
description: Denne artikkelen forklarer hvordan du konfigurere avgiftsgrupper i avgiftsberegningstjenesten.
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
ms.openlocfilehash: 89c5670ee7e78f2dc51f128c3ae8d284bb6b925b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862906"
---
# <a name="set-up-tax-groups"></a>Definere avgiftsgrupper

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du konfigurere avgiftsgrupper i avgiftsberegningstjenesten. Den forklarer også hvordan du definerer relevansregelmatrisen for avgiftsgruppe og konfigurerer linjer i matrisen.

Konseptet med avgiftgrupper i avgiftsberegningstjenesten ligner konseptet med mva-grupper i Microsoft Dynamics 365 Finance. De er grupper av avgiftskoder. Avgiftsberegningstjenesten bruker skjæringspunktet mellom en avgiftgruppe og en vareavgiftsgruppe til å bestemme avgiftskodene.

Avgiftsgrupper i avgiftsberegningstjenesten er imidlertid forskjellige fra mva-grupper i Finance, der det ikke er noen tilleggsparametere på dem, for eksempel valgene for **Use tax** og **avgiftsfritak**. I stedet er disse parameterne tilgjengelige på avgiftskodenivå.

> [!IMPORTANT]
> Oppsettet av avgiftsgrupper i avgiftsberegningstjenesten er juridisk enhet–agnostisk. Du kan bare fullføre dette oppsettet i RCS (Regulatory Configuration Service) én gang. Når du aktiverer avgiftsberegningstjenesten i Finance, synkroniseres avgiftsgrupper automatisk for den valgte juridiske enheten.

## <a name="set-up-a-tax-group"></a>Konfigurere en avgiftsgruppe

Følg disse trinnene for konfigurere en avgiftsgruppe.

1. Logg på [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Gå til **Arbeidsområder** \> **Globaliseringsfunksjoner** \> **Avgiftsberegning**.
3. Velg funksjonen og versjonen du vil sette opp, og velg deretter **Rediger**.
4. Velg **Konfigurasjonsversjon** i kategorien **Generelt**.
5. Velg **Behandle kolonne** i kategorien **Avgiftsgruppe**. Hvis du definerer en avgiftsgruppe for vare for første gang, angis feltene i dialogboksen **Administrer kolonne** automatisk.
6. I listen til venstre utvider du **Linjer**-noden og merker av i avmerkingsboksen for **Avgiftsgruppe**.

    ![Avgiftsgruppen som er valgt under Linjer-noden i dialogboksen Behandle kolonner.](media/select-tax-group.png)

7. Velg høyre pil-knapp for å legge til **Avgiftsgruppe** i listen **Valgte kolonner**-listen til høyre.

    ![Avgiftsgruppe som er lagt til i listen Valgte kolonner.](media/add-tax-group.png)

8. Velg **OK**.

## <a name="configure-a-tax-group"></a>Konfigurere en avgiftsgruppe

Når du har definert en avgiftsgruppe, opprettes matrisen for relevansregel for avgiftsgruppe. Du kan legge til linjer i matrisen for å konfigurere avgiftsgruppen.

1. I fanen **Avgiftsgruppe**, velg **Legg til**.
2. I **Avgiftsgruppe**-feltet skriver du inn navnet på avgiftsgruppen.

    > [!IMPORTANT]
    > Vi anbefaler at du begrenser navnet på avgiftgruppen til 10 tegn. Dette navnet synkroniseres med Finance, som har en grense på 10 tegn for navnene til mva-gruppene.

3. I feltet **Avgiftskoder** merker du av for hver avgiftskode du vil ta med i avgiftsgruppen. Du kan inkludere flere avgiftskoder i én avgiftsgruppe.

    ![Flere avgiftskoder valgt i Avgiftskoder-feltet.](media/multiple-tax-codes-selection.png)

4. Gjenta trinn 1 til og med 3 hvis du vil legge til flere avgiftsgrupper.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
