---
title: Budsjett planlegging maler for Excel
description: Dette emnet beskriver hvordan du oppretter en Microsoft Excel-maler som kan brukes med budsjettplaner.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 0e2eb6e7c130f03edbf60a185d397d94b5d61d7d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-templates-for-excel"></a>Budsjett planlegging maler for Excel

Dette emnet beskriver hvordan du oppretter en Microsoft Excel-maler som kan brukes med budsjettplaner.

Dette emnet viser hvordan du oppretter Excel-maler som skal brukes med budsjettplaner ved hjelp av standard demo datasettet og Admin-brukerpålogging. Hvis du vil ha mer informasjon om budsjettplanlegging av, kan du se [budsjett Planlegging Oversikt.](budget-planning-overview-configuration.md) Du kan også følge den [budsjettplanlegging 101](budget-plan.md) opplæringen for å lære grunnleggende modul konfigurasjon og bruk av prinsipper.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Generere et regneark ved hjelp av budsjett plan dokumentoppsett
Budsjett plan dokumenter kan vises og redigeres ved hjelp av ett eller flere oppsett. Hvert oppsett kan ha en tilknyttet budsjett plan dokumentmal til å vise og redigere budsjett plandata i et Excel-regneark. I dette emnet, vil en dokumentmal for budsjett plan bli generert ved hjelp av en eksisterende konfigurasjon for oppsett. Åpne den **budsjett planer liste** (**budsjettering**&gt;**budsjettplaner**). Klikk **ny** til å opprette en ny budsjettplandokument. [![bpt1](./media/bpt11-1024x552.png)](./media/bpt11.png) 

Bruk av **Legg til** linje for å legge til linjer. Klikk **oppsett** til å vise budsjett plan dokumentet oppsett konfigurasjon. 
[![bpt2](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Du kan gå gjennom oppsettet konfigurasjonen og Juster den etter behov. Gå til **mal**&gt;**generere** til å opprette en Excel-fil for dette oppsettet. Etter at malen er generert, kan du gå til **mal**&gt;**Vis** til å åpne og se gjennom budsjettet planen dokumentmalen. Du kan lagre Excel-filen på den lokale stasjonen. [![bpt3](./media/bpt3-1024x545.png)](./media/bpt3.png) 

> [!NOTE] 
> Budsjett plan dokumentoppsettet kan ikke redigeres etter at det er knyttet til en Excel-mal. Hvis du vil endre oppsettet, slette tilknyttede malfilen i Excel og lag den. Dette er nødvendig for å holde feltene i oppsettet, og regnearket synkronisert. 

Excel-malen inneholder alle elementene fra budsjettet planen oppsettet for dokumentet, der den **tilgjengelig i regneark** -kolonnen er satt til True. Overlappende elementer er ikke tillatt i Excel-malen. For eksempel hvis oppsettet inneholder forespørselen Q1, forespørsel Q2, Q3 for forespørselen, og forespørselen Q4 kolonner og en total request-kolonne som representerer en sum av alle 4 kvartalsvise kolonner, er bare kvartalsvise kolonner eller sum-kolonnen tilgjengelig som skal brukes i Excel-malen. Excel-filen kan ikke oppdatere overlappende kolonner under oppdateringen, fordi dataene i tabellen kan bli foreldet og unøyaktig.

[![bpt4](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> For å unngå potensielle problemer med å vise og redigere budsjett plandata ved hjelp av Excel, bør den samme brukeren være logget i begge Dynamics 365 operasjoner og Microsoft Dynamics-kontor i Data-koblingen.

## <a name="add-a-header-to-budget-plan-document-template"></a>Legge til en topptekst i dokumentet budsjettplanmal
Hvis du vil legge til informasjonen i meldingshodet, velger du den øverste raden i Excel-filen og sette inn tomme rader. Klikk **Design** i den **Data Connector** å legge til felt i Excel-filen.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

I den **Design** kategorien ** ** klikker **Legg til** felt, og velg **BudgetPlanHeader** som datakilde for enheten.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Plasser markøren til ønsket plassering i Excel-filen. Klikk **Legg til etikett** til å legge til feltetiketten til den valgte plasseringen. Velg **legge til verdien** til å legge til verdi-feltet til det valgte stedet. Klikk **gjort** til Lukk utformingsverktøyet.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Legge til en beregnet kolonne i malen for budsjett plan dokumenttabell
--------------------------------------------------------------

Neste, beregnede kolonner vil bli lagt til dokumentmalen for genererte budsjett plan. A **totale forespørselen** kolonnen som oppsummeres forespørselen Q1: forespørselen Q4 kolonner, og en **justering** kolonnen, som beregnes på nytt i **totale forespørselen** kolonne med en forhåndsdefinert faktor.

Klikk **Design** i den **Data connector** til å legge til kolonner i tabellen. Klikk **Rediger** siden **BudgetPlanWorksheet** datakilden for å begynne å legge til kolonner.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Den valgte feltgruppen viser kolonnene som er tilgjengelig i malen. Klikk **formelen** til å legge til en ny kolonne. Gi navn til den nye kolonnen og deretter lime formelen inn i den **formelen** feltet. Klikk **oppdatering** til å sette inn kolonnen.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Hvis du vil definere formelen, opprette formelen i regnearket, og deretter kopiere den til den **Design** vindu. En Dynamics 365 for bundne operasjoner-tabellen, blir vanligvis kalt "AXTable1". For eksempel vil summere be om Q1: Be om Q4 kolonner i regnearket, formelen = AxTable1\[be om Q1\]+ AxTable1\[be om Q2\]+ AxTable1\[be om Q3\]+ AxTable1\[be om Q4\].

Gjenta disse trinnene for å sette inn den **justering** kolonnen. Bruk formelen = AxTable1\[totale forespørselen\]\*$I$ 1 for denne kolonnen. Dette tar du verdien i celle I1 og multiplisere verdiene i den **totale forespørselen** -kolonnen for å beregne justeringsbeløpene.

Lagre og lukk Excel-filen. Gå tilbake til Dynamics 365 for operasjoner, og i **oppsett**, klikker du **mal &gt;laste opp** til å laste opp lagret Excel-malen som skal brukes for budsjettplanen. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Lukk den **oppsett** glidebryteren. I **budsjettplanen** dokument, klikker du **regneark** til å vise og redigere dokumentet i Excel. Merk at den justerte Excel-malen som ble brukt til å opprette denne Budsjettplanregnearket og beregnede kolonner, blir oppdatert ved hjelp av formler som ble definert i de forrige trinnene. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Tips og triks for å opprette budsjettplanmaler
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Kan jeg legge til og bruke flere datakilder til en budsjettplanmal?

Ja, du kan bruke den **Design** -menyen for å legge til flere enheter i samme eller andre ark i Excel-malen. Du kan for eksempel legge til **BudgetPlanProposedProject** datakilden til å opprette og vedlikeholde en liste over foreslåtte prosjekter samtidig når arbeidet med budsjett planlegger data i Excel. Vær oppmerksom på at inkludert datakilder for høyt volum kan ha innvirkning på Excel-arbeidsboken. 

Du kan bruke den **filteret** alternativ i den **Data Connector** å legge til ønskede filtre til flere datakilder.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Kan jeg skjule utformingsalternativet i Data-kontakt for andre brukere?

Ja, åpne den **Data Connector** alternativer for å skjule den **Design** alternativ fra andre brukere.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Utvid **alternativer for kobling av Data** og fjerner den **aktivere design** merket. Dette skjuler den **Design** alternativ fra den **Data connector**.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Kan jeg hindre at brukere ved et uhell lukker koblingen Data mens du arbeider med data?

Vi anbefaler å låse mal for å hindre brukere i å lukke den. Klikk for å aktivere låsen, den **Data connector**, en pil vises i øvre høyre hjørne. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Klikk pilen for en mer-menyen. Velg **Lås**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Kan jeg bruke andre Excel-funksjoner, som celleformatering, farger, betinget formatering og diagrammer med mine budsjettplanmaler?

Ja, de fleste standard Excel-funksjonene virker i budsjettplanmaler. Vi anbefaler å bruke fargekoder for brukere til å skille mellom skrivebeskyttet og redigerbare kolonner. Betinget formatering kan brukes til å fremheve problematiske områder av budsjettet. Kolonnesummer kan enkelt presenteres ved hjelp av standard Excel-formler over tabellen.

Du kan også opprette og bruke pivottabeller og diagrammer for flere grupperinger og effekter av budsjettdata. På den **Data** -kategorien i den **tilkoblinger** gruppen, klikker du **Oppdater alt**, og klikk deretter **Tilkoblingsegenskaper**. Klikk på **bruk av** i kategorien. Under **Oppdater**, velger du **Oppdater data når filen åpnes** merket. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)


