---
title: Oversikt over nummerserie
description: "Nummerserier i Microsoft Dynamics 365 for Finance and Operations brukes til å generere lesbare, unike ID-er for hoveddataposter og transaksjonsposter som krever ID-er. En hoveddatapost eller transaksjonspost som krever en ID kalles en <em>referanse</em>."
author: MargoC
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: d260f460bf0da072eb46909d8c28d18041ecaa78
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017


---

# Oversikt over nummerserie
<a id="number-sequence-overview" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Nummerserier i Microsoft Dynamics 365 for Finance and Operations brukes til å generere lesbare, unike ID-er for hoveddataposter og transaksjonsposter som krever ID-er. En hoveddatapost eller transaksjonspost som krever en ID kalles en <em>referanse</em>.

Du må konfigurere en nummerserie og tilknytte den referansen før du kan opprette nye poster for en referanse i Microsoft Dynamics 365 for Finance and Operations. Vi anbefaler at du bruker sidene i **Organisasjonsstyring** til å konfigurere nummerserier. Hvis modulspesifikke innstillinger kreves, kan du bruke parametersiden i en modul til å angi nummerserier for referansene i denne modulen. I **Kundereskontro** og **Leverandører** kan du for eksempel definere nummerseriegrupper for å tildele spesifikke nummerserier til bestemte kunder eller leverandører. Når du har definert en nummerserie, må du angi et område, som angir hvilken organisasjon som bruker nummerserien. Omfanget kan være **Delt**, **Firma**, **Juridisk enhet** eller **Driftsenhet**. Omfangene **Juridisk enhet** og **Firma** kan kombineres med **Regnskapskalenderperiode** for å opprette enda mer spesifikke nummerserier. Nummerserieformater består av segmenter. Nummerserier med et annet omfang enn **Delt**, kan inneholde segmenter som samsvarer med omfanget. En nummerserie med omfanget **Juridisk enhet** kan for eksempel inneholdet et segment for en juridisk enhet. Hvis du tar med et omfangssegment i nummerserieformatet, kan du identifisere omfanget til en bestemt post ved å se på nummeret. I tillegg til segmenter som tilsvarer omfang, kan nummerserieformater inneholde **Konstant** og **Alfanumeriske segmenter**. Et **Konstant**-segment inneholder et sett med bokstaver, tall eller symboler som ikke endres. Et **Alfanumerisk** segment inneholder et sett med bokstaver eller tall som øker hver gang et tall brukes. Bruk et nummertegn (\#) for å angi økende tall og et ampersandtegn (&) for å angi økende bokstaver. Formatet \#\#\#\#\#\_2017 oppretter for eksempel serien 00001\_2017, 00002\__2017 og så videre.
Eksempler på nummerserier
------------------------

Eksemplene nedenfor viser hvordan du bruker segmenter til å opprette nummerserieformater. Eksemplene viser særlig virkningen av bruken av omfangssegmenter.
### Reiseregningsnumre
<a id="expense-report-numbers" class="xliff"></a>

I eksemplet nedenfor konfigureres reiseregningsnumre for den juridiske enheten som heter **CS**. **Område:** Reiseregninger **Referanse:** Reiseregningsnummer **Omfang:** Juridisk enhet **Juridisk enhet:** CS
| Segmenter  | Segmenttype | Verdi     |
|-----------|--------------|-----------|
| Segment 1 | Juridisk enhet | CS        |
| Segment 2 | Konstant     | -UTGIFT- |
| Segment 3 | Alfanumerisk | \#\#\#\#  |

**Eksempel på formatert nummer**: CS-UTGIFT-0039 Du kan definere et lignende sekvenstallformat for andre juridiske enheter. For en juridisk enhet som heter **RW**, hvis du bare endrer verdien i segmentet for juridisk enhet, er det formaterte nummeret for eksempel RW-UTGIFT-0039. Du kan også endre hele nummerserieformatet for andre juridiske enheter. Du kan for eksempel utelate omfangssegmentet for den juridiske enheten for å opprette et formatert nummer , for eksempel Exp-0001.

### Salgsordrenumre
<a id="sales-order-numbers" class="xliff"></a>

I eksemplet nedenfor konfigureres salgsordrenumre for firma-IDen **CEU**. **Område:** Salg **Referanse:** Salgsordre **Omfang:** Firma **Firma:** CEU
| Segmenter  | Segmenttype | Verdi    |
|-----------|--------------|----------|
| Segment 1 | Konstant     | SO-      |
| Segment 2 | Alfanumerisk | \#\#\#\# |

**Eksempel på formatert nummer**: SO-0029 Selv om det ikke er oppført omfangssegment i formatet, starter nummereringen på nytt for hver firma-ID. Hvis du bruker det samme formatet for alle firma-ID-er, brukes de samme numrene i hvert firma. Salgsordrenummeret SO-0029 brukes for eksempel i hvert firma. Du kan også endre hele nummerserieformatet for andre firma-ID-er.

### Innkjøpsrekvisisjonsnumre
<a id="purchase-requisition-numbers" class="xliff"></a>

I eksemplet nedenfor gjelder innkjøpsrekvisisjonsnumre for hele organisasjonen. **Område:** Kjøp **Referanse:** Innkjøpsrekvisisjon **Omfang:** Delt
| Segmenter  | Segmenttype | Verdi    |
|-----------|--------------|----------|
| Segment 1 | Konstant     | Req      |
| Segment 2 | Alfanumerisk | \#\#\#\# |

**Eksempel på formatert nummer**: Req0052 Fordi omfanget er **Delt**, brukes nummerserieformatet på tvers av organisasjonen. Du kan ikke definere forskjellige nummerserieformater for forskjellige deler av organisasjonen. Ytelseshensyn for nummerserier
-----------------------------------------------

Vurder følgende informasjon om hvordan konfigurasjonen av nummerserier som kan påvirke systemytelsen, før du definerer nummerserier.
### Sammenhengende og ikke-sammenhengende nummerserier
<a id="continuous-and-non-continuous-number-sequences" class="xliff"></a>

Nummerserier kan være sammenhengende og ikke-sammenhengende. En ubrutt nummerserie hopper over ikke noen tall, men tallene kan ikke brukes sekvensielt. Tall fra en ikke-sammenhengende nummerserie brukes sekvensielt, men nummerserien kan hoppe over tall. Hvis en bruke for eksempel avbryter en transaksjon, blir et nummer generert, men ikke brukt. Dette nummeret resirkuleres senere i en ubrutt nummerserie. Nummeret brukes ikke i en ikke-sammenhengende nummerserie. Ubrutte nummerserier kreves vanligvis for eksterne dokumenter, for eksempel bestillinger, salgsordrer og fakturaer. Sammenhengende nummerserier kan imidlertid ha negativ innvirkning på systemets responstider fordi systemet må be om et nummer fra databasen hver gang et nytt dokument eller en ny post opprettes. Hvis du bruker en ikke-sammenhengende nummerserie, kan du aktivere **Forhåndstilordning** på hurtigfanen **Ytelse** på siden **Nummerserier**. Når du angir et antall numre som skal forhåndstilordnes, velges disse numrene i systemet, og de lagres i minnet. Nye numre forespørres fra databasen etter at forhåndstilordnete antallet er brukt. Hvis det ikke er et forskriftsmessige krav at du bruker sammenhengende nummerserier, anbefaler vi at du bruker ikke-sammenhengende nummerserier for bedre ytelse.

### Automatisk opprydding av nummerserier
<a id="automatic-cleanup-of-number-sequences" class="xliff"></a>

Hvis det oppstår et strømbrudd, en programfeil eller annen uventet feil, kan ikke systemet resirkulere numre automatisk for ubrutte nummerserier. Du kan kjøre oppryddingsprosessen manuelt eller automatisk for å gjenopprette de tapte numrene. Vurder serverbruken nøye når du planlegger oppryddingsprosessen. Vi anbefaler at du foretar oppryddingen som en satsvis jobb i perioder med liten aktivitet.






