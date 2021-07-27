---
title: Oversikt over nummerserier
description: Nummerserier brukes for å generere lesbare, unike ID-er for hoveddataposter og transaksjonsposter som krever ID-er.
author: MargoC
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceConfiguration
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "15461"
- intro-internal
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1a6c7b7ee36ae1ea37842aea744fc8601f972d89
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/03/2021
ms.locfileid: "6338910"
---
# <a name="number-sequences-overview"></a>Oversikt over nummerserier

[!include [banner](../includes/banner.md)]

Nummerserier brukes for å generere lesbare, unike ID-er for hoveddataposter og transaksjonsposter som krever ID-er. En hoveddatapost eller transaksjonspost som krever en ID kalles en *referanse*.

Du må konfigurere en nummerserie og tilknytte den referansen før du kan opprette nye poster for en referanse. Vi anbefaler at du bruker sidene i **Organisasjonsstyring** til å konfigurere nummerserier. Hvis modulspesifikke innstillinger kreves, kan du bruke parametersiden i en modul til å angi nummerserier for referansene i denne modulen. I **Kundereskontro** og **Leverandører** kan du for eksempel definere nummerseriegrupper for å tildele spesifikke nummerserier til bestemte kunder eller leverandører.

Når du har definert en nummerserie, må du angi et område, som angir hvilken organisasjon som bruker nummerserien. Omfanget kan være **Delt**, **Firma**, **Juridisk enhet** eller **Driftsenhet**. Omfangene **Juridisk enhet** og **Firma** kan kombineres med **Regnskapskalenderperiode** for å opprette enda mer spesifikke nummerserier.

Nummerserieformater består av segmenter. Nummerserier med et annet omfang enn **Delt**, kan inneholde segmenter som samsvarer med omfanget. En nummerserie med omfanget **Juridisk enhet** kan for eksempel inneholdet et segment for en juridisk enhet. Hvis du tar med et omfangssegment i nummerserieformatet, kan du identifisere omfanget til en bestemt post ved å se på nummeret.

I tillegg til segmenter som tilsvarer omfang, kan nummerserieformater inneholde **Konstant** og **Alfanumeriske segmenter**. Et **Konstant**-segment inneholder et sett med bokstaver, tall eller symboler som ikke endres. Et **Alfanumerisk** segment inneholder et sett med bokstaver eller tall som øker hver gang et tall brukes. Bruk et nummertegn (\#) for å angi økende tall og et ampersandtegn (&) for å angi økende bokstaver. Formatet \#\#\#\#\#\_2017 oppretter for eksempel serien 00001\_2017, 00002\__2017 og så videre.

## <a name="number-sequence-examples"></a>Eksempler på nummerserier

Eksemplene nedenfor viser hvordan du bruker segmenter til å opprette nummerserieformater. Eksemplene viser særlig virkningen av bruken av omfangssegmenter.

### <a name="expense-report-numbers"></a>Reiseregningsnumre

I eksemplet nedenfor konfigureres reiseregningsnumre for den juridiske enheten som heter **CS**.

- **Område:** Reise og utgifter
- **Referanse:** Reiseregningsnummer
- **Omfang:** Juridisk enhet
- **Juridisk enhet:** CS

| Segmenter  | Segmenttype | Verdi     |
|-----------|--------------|-----------|
| Segment 1 | Juridisk enhet | CS        |
| Segment 2 | Konstant     | -UTGIFT- |
| Segment 3 | Alfanumerisk | \#\#\#\#  |

**Eksempel på formatert nummer**: CS-UTGIFT-0039

Du kan definere et lignende nummerserieformatet for andre juridiske enheter. For en juridisk enhet som heter **RW**, hvis du bare endrer verdien i segmentet for juridisk enhet, er det formaterte nummeret for eksempel RW-UTGIFT-0039. Du kan også endre hele nummerserieformatet for andre juridiske enheter. Du kan for eksempel utelate omfangssegmentet for den juridiske enheten for å opprette et formatert nummer , for eksempel Exp-0001.

### <a name="sales-order-numbers"></a>Salgsordrenumre

I eksemplet nedenfor konfigureres salgsordrenumre for firma-IDen **CEU**.

- **Område:** Salg
- **Referanse:** Salgsordre
- **Omfang:** Firma
- **Firma:** CEU

| Segmenter  | Segmenttype | Verdi    |
|-----------|--------------|----------|
| Segment 1 | Konstant     | SO-      |
| Segment 2 | Alfanumerisk | \#\#\#\# |

**Eksempel på formatert nummer**: SO-0029

Selv det ikke er oppført omfangssegment i formatet, starter nummereringen på nytt for hver firma-ID. Hvis du bruker det samme formatet for alle firma-ID-er, brukes de samme numrene i hvert firma. Salgsordrenummeret SO-0029 brukes for eksempel i hvert firma. Du kan også endre hele nummerserieformatet for andre firma-ID-er.

### <a name="purchase-requisition-numbers"></a>Innkjøpsrekvisisjonsnumre

I eksemplet nedenfor gjelder innkjøpsrekvisisjonsnumre for hele organisasjonen.

- **Område:** Innkjøp
- **Referanse:** Kjøpsrekvisisjon
- **Omfang:** Delt

| Segmenter  | Segmenttype | Verdi    |
|-----------|--------------|----------|
| Segment 1 | Konstant     | Req      |
| Segment 2 | Alfanumerisk | \#\#\#\# |

**Eksempel på formatert nummer**: Req0052

Siden omfanget er **Delt**, brukes nummerserieformatet på tvers av organisasjonen. Du kan ikke definere forskjellige nummerserieformater for forskjellige deler av organisasjonen.

## <a name="performance-considerations-for-number-sequences"></a>Ytelseshensyn for nummerserier

Vurder følgende informasjon om hvordan konfigurasjonen av nummerserier som kan påvirke systemytelsen, før du definerer nummerserier.

### <a name="continuous-and-non-continuous-number-sequences"></a>Sammenhengende og ikke-sammenhengende nummerserier

Nummerserier kan være sammenhengende og ikke-sammenhengende. En ubrutt nummerserie hopper over ikke noen tall, men tallene kan ikke brukes sekvensielt. Tall fra en ikke-sammenhengende nummerserie brukes sekvensielt, men nummerserien kan hoppe over tall. Hvis en bruke for eksempel avbryter en transaksjon, blir et nummer generert, men ikke brukt. Dette nummeret resirkuleres senere i en ubrutt nummerserie. Nummeret brukes ikke i en ikke-sammenhengende nummerserie.

Ubrutte nummerserier kreves vanligvis for eksterne dokumenter, for eksempel bestillinger, salgsordrer og fakturaer. Sammenhengende nummerserier kan imidlertid ha negativ innvirkning på systemets responstider fordi systemet må be om et nummer fra databasen hver gang et nytt dokument eller en ny post opprettes.

Hvis du bruker en ikke-sammenhengende nummerserie, kan du aktivere **Forhåndstilordning** på hurtigfanen **Ytelse** på siden **Nummerserier**. Når du angir et antall numre som skal forhåndstilordnes, velges disse numrene i systemet, og de lagres i minnet. Nye numre forespørres fra databasen etter at forhåndstilordnete antallet er brukt.

Hvis det ikke er et forskriftsmessige krav at du bruker sammenhengende nummerserier, anbefaler vi at du bruker ikke-sammenhengende nummerserier for bedre ytelse.

### <a name="automatic-cleanup-of-number-sequences"></a>Automatisk opprydding av nummerserier

Hvis det oppstår et strømbrudd, en programfeil eller annen uventet feil, kan ikke systemet resirkulere numre automatisk for ubrutte nummerserier. Du kan kjøre oppryddingsprosessen manuelt eller automatisk for å gjenopprette de tapte numrene.

Vurder serverbruken nøye når du planlegger oppryddingsprosessen. Vi anbefaler at du foretar oppryddingen som en satsvis jobb i perioder med liten aktivitet.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]