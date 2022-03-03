---
title: Bruk datakilder for DATAINNSAMLING i formater for elektronisk rapportering
description: Dette emnet forklarer hvordan du bruker datakilder for DATAINNSAMLING i formater for elektronisk rapportering (ER).
author: NickSelin
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 185fb9a33cb4cc655dfdf640b4c239d617426c64
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323907"
---
# <a name="use-data-collection-data-sources-in-electronic-reporting-formats"></a>Bruk datakilder for DATAINNSAMLING i formater for elektronisk rapportering

[!include [banner](../includes/banner.md)]

Du kan bruke operasjonsutformingen i rammeverket for [Elektronisk rapportering (ER)](general-electronic-reporting.md) til å konfigurere komponenten format i en ER-løsning som brukes til å generere utgående dokumenter i forskjellige formater. Den hierarkiske strukturen til den konfigurerte formatkomponenten består av formateringselementer av forskjellige typer. Disse formatelementene brukes til å fylle genererte dokumenter med påkrevd informasjon ved kjøretid. Når du kjører et ER-format, kjøres formatelementene som standard i samme rekkefølge som de presenteres i i formathierarkiet: ett etter ett, fra øverst til nederst.

Når ER kjører et formatelement som inneholder en binding, kjøres formelen for denne bindingen, og formatelementet legger til verdien i et generert dokument. Bindingen kan for eksempel sende verdien i et felt av typen datamodell til et formatelement. Du kan konfigurere en datakilde for DATAINNSAMLING for å samle inn verdier fra datamodellfelter under kjøring, summere verdier og fylle et generert dokument med de innsamlede verdiene. Når du skal bruke denne fremgangsmåten, endrer du den innledende bindingen slik at den konfigurerte datakilden for DATAINNSAMLING brukes til å sende verdien i et datamodellfelt til et formatelement. Ved å sende verdier via datakilden for DATAINNSAMLING kan du samle inn nødvendige opplysninger for videre bruk.

Når du konfigurerer en datakilde for DATAINNSAMLING, må du angi en verditype som skal behandles i datakilden. Følgende [datatyper](er-formula-supported-data-types-primitive.md) støttes for øyeblikket for innsamling av verdier:

- Boolsk
- Dato
- dato/klokkeslett
- Guid
- Int64
- Heltall
- Kommatall
- Streng
- Tid

Du kan bruke `Collect(Value)`-metoden i en datakilde for DATAINNSAMLING til å sende en verdi til en datakilde for innsamling. I denne metoden er `Value`-argumentet enten en konstant eller den gyldige banen til et datakildefelt av den relevante datatypen.

Bruk egenskapen `Result` i en datakilde for DATAINNSAMLING for å få tilgang til listen over innsamlede verdier. Denne egenskapen returnerer en [postliste](er-formula-supported-data-types-composite.md#record-list). Postene på postlisten inneholder `Value`-feltet som du kan bruke for å få tilgang til innsamlede verdier.

Som standard samler en datakilde for DATAINNSAMLING bare inn unike verdier.

Hvis du vil samle inn alle verdiene, setter du feltet **Samle inn alle verdier** i den konfigurerte datakilden for DATAINNSAMLING til **Ja**. Når feltet **Samle inn alle verdier** er satt til **Ja**, blir den parameteriserte `Sum(Flag)`-egenskapen tilgjengelig. Du kan bruke denne egenskapen til å hente totalbeløpet for alle verdiene som er samlet inn. I denne egenskapen er `Flag`-argumentet en [boolsk](er-formula-supported-data-types-primitive.md#boolean) verdi som brukes til å angi om totalverdien må tilbakestilles.

- Når verdien **Usann** vises, fortsetter summeringen fra det tidligere innsamlede beløpet.
- Når verdien **Sann** vises, startes en ny summering.

Følgende datatyper støttes for øyeblikket for summering:

- Int64
- Heltall
- Kommatall

Hvis du vil vite mer om denne funksjonen, kan du fullføre eksemplet nedenfor.

## <a name="example-configure-an-er-format-to-do-counting-and-summing-by-using-a-data-collection-data-source"></a>Eksempel: Konfigurer et ER-format for å telle og summere ved hjelp av en datakilde for DATAINNSAMLING

Dette eksemplet viser hvordan en bruker med rollen som systemadministrator eller funksjonell konsulent for elektronisk rapportering kan konfigurere et ER-format som har en datakilde for DATAINNSAMLING som brukes til å beregne løpende totaler og samle inn summerte verdier.

Prosedyrene i dette eksemplet kan fullføres i USMF-firmaet i Microsoft Dynamics 365 Finance.

### <a name="upload-and-use-the-provided-er-solution"></a>Last opp og bruk den leverte ER-løsningen

1. [Importere ER-eksempelkonfigurasjonene](er-defer-sequence-element.md#import-the-sample-er-configurations).
2. [Aktivere en konfigurasjonsleverandør](er-defer-sequence-element.md#activate-a-configurations-provider).
3. [Gå gjennom den importerte modelltilordningen](er-defer-sequence-element.md#review-the-imported-model-mapping).
4. [Gå gjennom det importerte formatet](er-defer-sequence-element.md#review-the-imported-format).
5. [Kjør det importerte formatet](er-defer-sequence-element.md#run-the-imported-format).

### <a name="run-the-format-of-the-provided-er-solution"></a>Kjør formatet til den angitte ER-løsningen

1. På **Formatutforming**-siden velger du **Kjør**.
2. I dialogboksen **Parametere for elektronisk rapport** velger du **OK**.
3. Last ned og gjennomgå filen som nettleseren tilbyr.

    ![Nedlastet fil som inneholder resultatene av den opprinnelige formatkjøringen](./media/er-data-collection-data-sources-01.png)

### <a name="modify-the-format-of-the-er-solution-to-calculate-the-running-tax-total"></a>Endre formatet til ER-løsningen for å beregne den løpende mva-totalen

Hvis transaksjonsvolumet er mye større enn volumet i det gjeldende eksemplet, kan det hende at summeringstiden øker og forårsaker ytelsesproblemer. Hvis du endrer innstillingene for formatet, kan du bidra til å forhindre disse ytelsesproblemene. Fordi du får tilgang til avgiftsverdier for å inkludere dem i den genererte rapporten, kan du bruke denne informasjonen til å summere avgiftsverdier.

1. På siden **Formatutforming** i kategorien **Tilordning** velger du **Legg til rot**.
2. I dialogboksen **Legg til datakilde** velger du **Funksjoner** \> **Datainnsamling**.
3. Følg trinnene nedenfor i dialogboksen **Datakildeegenskaper for datainnsamling**:

    1. I feltet **Navn** angir du **CollectedTaxValues**.
    2. Velg **Faktisk** i **Varetype**-feltet.
    3. I feltet **Samle inn alle verdier** velger du **Ja**.
    4. Velg **OK**.

4. Velg det numeriske formatelementet **Rapport\\Linjer\\Oppføring\\TaxAmount**.

    > [!NOTE]
    > For øyeblikket er bindingen `@.Value` konfigurert for dette elementet. Derfor er et generert dokument fylt ut med avgiftsverdier fra `model.Data.List.Value`-feltet.

5. Velg **Rediger formel**.
6. Følg denne fremgangsmåten på siden **Formeldesigner**:

    1. I **Formel**-feltet erstatter du `@.Value` med `CollectedTaxValues.Collect(@.Value)`.
    2. Lagre endringene, og lukk siden.

    > [!NOTE]
    > Den nye bindingen vil sende de samme avgiftsverdiene til et generert dokument. Disse verdiene blir imidlertid også samlet inn i datakilden **CollectedTaxValues**.

7. Velg det numeriske formatelementet **Rapport\\Linjer\\Oppføring\\RunningTotal**.
8. Velg **Rediger formel**.
9. Følg denne fremgangsmåten på siden **Formeldesigner**:

    1. I **Formel**-feltet angir du `CollectedTaxValues.Sum(false)`.
    2. Lagre endringene, og lukk siden.

    > [!NOTE]
    > Den nye bindingen vil sender det totale antallet avgiftsverdier som allerede er angitt, til et generert dokument.

    ![Numeriske elementer som har oppdaterte bindinger på siden Formatdesigner](./media/er-data-collection-data-sources-02.png)

10. Velg **Lagre**, og velg deretter **Kjør**.
11. I dialogboksen **Parametere for elektronisk rapport** velger du **OK**.
12. Last ned og gjennomgå filen som nettleseren tilbyr.

    ![Nedlastet fil som inneholder resultatene av den endrede formatkjøringen](./media/er-data-collection-data-sources-03.png)

### <a name="modify-the-format-to-evaluate-the-list-of-collected-tax-values"></a>Endre formatet for å evaluere listen over innsamlede avgiftsverdier

1. På siden **Formatdesigner**, på **Format**-fanen, velger du det numeriske formatelementet **Rapport\\Linjer\\Post\\RunningTotal** og følger deretter trinnene nedenfor:

    1. I feltet **Numerisk type** endrer du verdien fra **Kommatall** til **Heltall**.
    2. I feltet **Numerisk format** endrer du verdien fra **F2** til **F0**.

3. På **Tilordning**-fanen velger du **Rediger formel**.
4. Følg denne fremgangsmåten på siden **Formeldesigner**:

    1. I **Formel**-feltet angir du `COUNT(CollectedTaxValues.Result)`.
    2. Lagre endringene, og lukk siden.

    > [!NOTE]
    > Den nye bindingen sender antallet poster i listen der avgiftsverdiene samles inn, til et generert dokument.

5. Velg **Lagre**, og velg deretter **Kjør**.
6. I dialogboksen **Parametere for elektronisk rapport** velger du **OK**.
7. Last ned og gjennomgå filen som nettleseren tilbyr.

    ![Nedlastet fil som inneholder resultatene av en annen endret formatkjøring](./media/er-data-collection-data-sources-04.png)

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

### <a name="if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions"></a>Hvis jeg må beregne løpende totalsummer og samle inn data, hva er forskjellen mellom å bruke en datakilde for DATAINNSAMLING og bruke de innebygde funksjonene for DATAINNSAMLING?

Både en datakilde for DATAINNSAMLING og de innebygde funksjonene for [DATAINNSAMLING](er-functions-category-data-collection.md) kan brukes til datainnsamling, summering og opptelling, basert på informasjon som sendes til et generert utgående dokument. Når du derimot prøver å bestemme hvilken teknikk du vil bruke, må du vurdere følgende punkter.

| Datakilde | Innebygde funksjoner |
|-------------| ------------------ |
| Bare verdier samles inn. | <p>Navngitte verdier samles inn. Totalsummer kan derfor beregnes for separate grupper med verdier.</p><p>I tillegg kan grupper trekkes ut som en liste.</p><p>Tekstverdier kan også samles inn.</p> |
| Unike verdier samles inn automatisk. | Tilleggsinnstillinger kreves for å trekke ut en liste over unike verdier fra de innsamlede verdiene. |
| Ytelsen avhenger av volumet av de innsamlede verdiene. | I praksis avhenger ytelsen ikke av volumet av de innsamlede verdiene. |
| Denne teknikken fungerer for alle typer utgående dokumenter. | Denne teknikken fungerer bare for tekstdokumenter og XML-dokumenter. |

## <a name="additional-resources"></a>Tilleggsressurser

- [Konfigurere format for å utføre telling og summering](./tasks/er-format-counting-summing-1.md)
- [Utsette kjøringen av sekvenselementer i ER-formater](er-defer-sequence-element.md#Example)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
