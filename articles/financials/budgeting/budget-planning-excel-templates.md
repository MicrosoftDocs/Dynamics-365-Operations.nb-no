---
title: Maler for budsjettplanlegging for Excel
description: Dette emnet beskriver hvordan du oppretter Microsoft Excel-maler som kan brukes med budsjettplaner.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 156688b705337331e083ebc19fded57b028acb67
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="budget-planning-templates-for-excel"></a>Maler for budsjettplanlegging for Excel

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter Microsoft Excel-maler som kan brukes med budsjettplaner.

Dette emnet viser hvordan du oppretter Excel-maler som skal brukes med budsjettplaner ved hjelp av standard demodatasettet og Admin-brukerpålogging. Hvis du vil ha mer informasjon om budsjettplanlegging, kan du se [Oversikt over budsjettplanlegging.](budget-planning-overview-configuration.md) Du kan også følge opplæringen [Budsjettplanlegging 101](budget-plan.md) for å lære grunnleggende modulkonfigurasjon og -bruksprinsipper.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Generer et regneark ved hjelp av oppsett for budsjettplandokument

Budsjettplandokumenter kan vises og redigeres ved hjelp av ett eller flere oppsett. Hvert oppsett kan ha en tilknyttet dokumentmal for budsjettplan for å vise og redigere budsjettplandataene i et Excel-regneark. I dette emnet genereres en dokumentmal for budsjettplan ved hjelp av en eksisterende oppsettkonfigurasjon. 

1. Åpne **listen over budsjettplaner** (**Budsjettering** &gt; **Budsjettplaner**). 
2. Klikk **Ny** for å opprette et nytt budsjettplandokument. 

   [![Liste over budsjettplaner](./media/bpt11-1024x552.png)](./media/bpt11.png) 

3. Bruk alternativet **Legg til linje** for å legge til linjer. Klikk **Oppsett** for å vise oppsettkonfigurasjonen for budsjettplandokument. 

   [![Legg til budsjettplaner](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Du kan gå gjennom oppsettkonfigurasjonen og justere den etter behov. 
1. Gå til **Mal** &gt; **Generer** for å opprette en Excel-fil for dette oppsettet. 
2. Etter at malen er generert, går du til **Mal** &gt; **Vis** for å åpne og se gjennom dokumentmalen for budsjettplan. Du kan lagre Excel-filen på den lokale stasjonen. 

[![Lagre som](./media/bpt3-1024x545.png)](./media/bpt3.png)

> [!NOTE] 
> Oppsettet av budsjettplandokumentet kan ikke redigeres etter at det er knyttet til en Excel-mal. Hvis du vil endre oppsettet, sletter du den tilknyttede Excel-malfilen og genererer den på nytt. Dette er nødvendig for å holde feltene i oppsettet og regnearket synkronisert. 

Excel-malen inneholder alle elementene fra oppsettet for budsjettplandokument, der kolonnen **Tilgjengelig i regneark** er satt til sann. Overlappende elementer er ikke tillatt i Excel-malen. Hvis oppsettet for eksempel inneholder kolonnene Forespørsel Q1, Forespørsel Q2, Forespørsel Q3 og Forespørsel Q4, og en total forespørsel-kolonne som representerer en sum av alle 4 kvartalsvise kolonnene, er bare de kvartalsvise kolonnene eller totalkolonnen tilgjengelig for bruk i Excel-malen. Excel-filen kan ikke oppdatere overlappende kolonner under oppdateringen, fordi dataene i tabellen kan bli foreldet og unøyaktige.

[![Eksempel](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> For å unngå potensielle problemer med å vise og redigere budsjettplandata ved hjelp av Excel, bør den samme brukeren være pålogget både Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics Office-tillegget Datakobling.

## <a name="add-a-header-to-budget-plan-document-template"></a>Legge til en topptekst i dokumentmalen for budsjettplan
Hvis du vil legge til topptekstinformasjon, velger du den øverste raden i Excel-filen og setter inn tomme rader. Klikk **Utforming** i **Datakobling** for å legge til felt i Excel-filen.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

I kategorien **Utforming** klikker du **Legg til felt** og velger **BudgetPlanHeader** som enhetsdatakilde.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Pek markøren mot ønsket plassering i Excel-filen. Klikk **Legg til etikett** for å legge til feltetiketten i den valgte plasseringen. Velg **Legge til verdi** for å legge til verdifeltet i det valgte stedet. Klikk på **Ferdig** for å lukke utformingen.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Legge til en beregnet kolonne i dokumentmaltabellen for budsjettplan
--------------------------------------------------------------

Deretter vil beregnede kolonner bli lagt til den genererte dokumentmalen for budsjettplan. Kolonnen **Total forespørsel** som summerer kolonnene Forespørsel Q1: Forespørsel Q4, og kolonnen **Justering**, som beregner kolonnen **Total forespørsel** på nytt med en forhåndsdefinert faktor.

Klikk **Utforming** i **Datakobling** for å legge til kolonner i tabellen. Klikk **Rediger** ved siden av **BudgetPlanWorksheet**-datakilden for å begynne å legge til kolonner.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Den valgte feltgruppen viser kolonnene som er tilgjengelige i malen. Klikk **Formel** for å legge til en ny kolonne. Gi den nye kolonnen et navn, og lim deretter inn formelen inn i **Formel**-feltet. Klikk **Oppdater** for å sette inn kolonnen.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Hvis du vil definere formelen, oppretter du formelen i regnearket, og deretter kopierer du den til **Utforming**-vinduet. En tabell bundet til Finance and Operations, blir vanligvis kalt "AXTable1". For å summere Forespørsel Q1: Forespørsel Q4 i regnearket, formelen = AxTable1\[Forespørsel Q1\]+ AxTable1\[Forespørsel Q2\]+ AxTable1\[Forespørsel Q3\]+ AxTable1\[Forespørsel Q4\].

Gjenta disse trinnene for å sette inn **Justering**-kolonnen. Bruk formelen = AxTable1\[Total forespørsel\]\*$I$ 1 for denne kolonnen. Dette henter verdien i celle I1 og multipliserer verdiene i kolonnen **Totale forespørsel** for å beregne justeringsbeløpene.

Lagre og lukk Excel-filen. Gå tilbake til Finance and Operations. Under **Oppsett** klikker du på **Mal &gt;Last opp** for å laste opp den lagrede Excel-malen som skal brukes for budsjettplanen. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Lukk **Oppsett**-glidebryteren. I **Budsjettplan**-dokument klikker du **Regneark** for å vise og redigere dokumentet i Excel. Merk at den justerte Excel-malen ble brukt til å opprette dette budsjettplanregnearket, og beregnede kolonner blir oppdatert ved hjelp av formler som ble definert i de forrige trinnene. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Tips og triks for å opprette budsjettplanmaler
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Kan jeg legge til og bruke flere datakilder i en budsjettplanmal?

Ja, du kan bruke **Utforming**-menyen til å legge til flere enheter i samme eller andre ark i Excel-malen. Du kan for eksempel legge til **BudgetPlanProposedProject**-datakilden for å opprette og vedlikeholde en liste over foreslåtte prosjekter samtidig når du arbeider med budsjettplandata i Excel. Vær oppmerksom på at inkludering av datakilder med store volumer kan ha innvirkning på Excel-arbeidsboken. 

Du kan bruke **Filter**-alternativet i **Datakobling** til å legge til ønskede filtre i flere datakilder.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Kan jeg skjule utformingsalternativet i Datakobling for andre brukere?

Ja, åpne alternativene for **Datakobling** for å skjule **Utforming**-alternativet fra andre brukere.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Utvid **Alternativer for datakobling** og fjern merket for **Aktiver utforming**. Dette skjuler **Utforming**-alternativet fra **Datakobling**.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Kan jeg hindre at brukere ved et uhell lukker datakoblingen under arbeid med data?

Vi anbefaler å låse malen for å hindre brukere i å lukke den. Du aktiverer låsen ved å klikke **Datakobling**. Det vises en pil i øvre høyre hjørne. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Klikk pilen for en åpne en tilleggsmeny. Velg **Lås**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Kan jeg bruke andre Excel-funksjoner, som celleformatering, farger, betinget formatering og diagrammer, med mine budsjettplanmaler?

Ja, de fleste standard Excel-funksjonene virker i budsjettplanmaler. Vi anbefaler å bruke fargekoding slik at brukere kan skille mellom skrivebeskyttede og redigerbare kolonner. Betinget formatering kan brukes til å fremheve problematiske områder i budsjettet. Kolonnesummer kan enkelt presenteres ved hjelp av standard Excel-formler over tabellen.

Du kan også opprette og bruke pivottabeller og diagrammer for flere grupperinger og visualiseringer av budsjettdata. I **Data**-kategorien i **Tilkoblinger**-gruppen klikker du **Oppdater alle**, og klikker deretter **Tilkoblingsegenskaper**. Klikk kategorien **Bruk**. Under **Oppdater** velger du avmerkningsboksen **Oppdater data når filen åpnes**. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)




