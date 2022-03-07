---
title: Redigeringsprogram med avansert formel for elektronisk rapportering
description: Dette emnet beskriver hvordan redigeringsprogrammet med avansert formel kan brukes til å konfigurere uttrykk i modellkartlegging av og formatkomponenter i elektronisk rapportering (ER).
author: NickSelin
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: d18aeedb2f21176ffe964b926168d4bf088a093b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751214"
---
# <a name="electronic-reporting-advanced-formula-editor"></a>Redigeringsprogram med avansert formel for elektronisk rapportering

[!include [banner](../includes/banner.md)]

I tillegg til det [Elektronisk rapportering-basert](general-electronic-reporting.md) [formelredigeringsprogram](general-electronic-reporting-formula-designer.md) kan du bruke redigeringsprogrammet med avansert formel for elektronisk rapportering til å forbedre opplevelsen av konfigurering av uttrykk for elektronisk rapportering (ER). Det avanserte redigeringsprogrammet er nettleserbasert og drives av [Monaco-redigeringsprogrammet](https://microsoft.github.io/monaco-editor). De mest brukte avanserte redigeringsfunksjonene er beskrevet i dette emnet:

- [Autoformatering av kode](#Autoformatting)
- [IntelliSense](#IntelliSense)
- [Kodefullføring](#CodeCompletion)
- [Kodenavigering](#CodeNavigation)
- [Kodestrukturering](#CodeStructuring)
- [Søk og erstatt](#FindAndReplace)
- [Datainnliming](#DataPasting)
- [Syntaksfargelegging](#SyntaxColorization)

## <a name=""></a><a name="ActivateAdvEditor">Aktivere redigeringsprogrammet med avansert formel</a>

Fullfør følgende trinn for å begynne å bruke redigeringsprogrammet med avansert formel i forekomsten av Microsoft Dynamics 365 Finance.

1.  Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2.  På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
3.  I delen **Kjøringssporing** i dialogboksen **Brukerparametere** setter du parameteren **Aktiver redigeringsprogram med avansert formel** til **Ja**.

[![Siden ER-konfigurasjoner](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)

> [!NOTE]
> Vær oppmerksom på at denne parameteren er brukerspesifikk og selskapsspesifikk.

## <a name=""></a><a name="Autoformatting">Autoformatering av kode</a>

Når du skriver et sammensatt uttrykk som består av flere rader med kode, blir innrykket for en ny angitt linje automatisk basert på innrykket for den forrige raden. Du kan velge linjer og endre det tilhørende innrykket ved å skrive inn **Tab** eller **Shift+Tab**.

[![ER-formelredigeringsprogram](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)

Med autoformatering kan du holde hele uttrykket velformatert for å gjøre ytterligere vedlikehold enklere samt for å forenkle forståelsen av den konfigurerte logikken.

## <a name=""></a><a name="IntelliSense">IntelliSense</a>

Redigeringsprogrammet kan fullføre ord for å hjelpe deg å skrive uttrykk raskere og unngå skrivefeil. Når du begynner å legge til ny tekst, tilbyr redigeringsprogrammet automatisk en liste med funksjoner som støttes i ER-funksjonene, som inneholder tegnene du har angitt. Du kan også utløse IntelliSense på et hvilket som helst sted i et konfigurert uttrykk ved å skrive inn **Ctrl+mellomrom**.

[![ER-formelredigeringsprogram](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)

## <a name=""></a><a name="CodeCompletion">Kodefullføring</a>

Redigeringsprogrammet utfører automatisk kodefullføring ved å:

- Sette inn en avsluttende hakeparentes når du angir en innledende hakeparentes, slik at markøren beholdes inne i parentesene.
- Sette inn det andre anførselstegnet når det første er angitt, slik at markøren beholdes inne i anførselstegnene
- Sette inn det andre doble anførselstegnet når det første er angitt, slik at markøren beholdes inne i anførselstegnene

[![ER-formelredigeringsprogram](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)

Når du peker til den innlagte parentesen, utheves det andre parentesen automatisk for å vise konstruksjonen de støtter.

## <a name=""></a><a name="CodeNavigation">Kodenavigering</a>

Du kan finne påkrevde symboler eller linjer i uttrykket ved å skrive inn **Gå til**-kommandoen ved hjelp av kommandopaletten eller hurtigmenyen.

Hvis du for eksempel vil hoppe til linje **8**, gjør du følgende:

- Trykk på **Ctrl+G**, angi verdien **8** og trykk deretter på **Enter**.

  - eller -

- Trykk på **F1**, skriv inn **G**, velg **Gå til linje**, angi verdien **8** og trykk deretter på **Enter**.

[![ER-formelredigeringsprogram](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)

## <a name=""></a><a name="CodeStructuring">Kodestrukturering</a>

Koden for enkelte funksjoner, for eksempel [IF](er-functions-logical-if.md) eller [CASE](er-functions-logical-case.md), struktureres automatisk. Du kan utvide og skjule alle ønskede foldeområder av denne koden for å redusere den redigerbare delen av et uttrykk, for å fokusere bare på delen som krever din oppmerksomhet. Fold / Opphev folding-kommandoene kan brukes til det.

Hvis du for eksempel vil folde alle områder, gjør du følgende:

- Trykk på **Ctrl+K**

  - eller -

- Trykk på **F1**, trykk på **FO**, velg **Fold alle** og trykk deretter på **Enter**

Hvis du vil oppheve folding av alle områder, gjør du følgende:

- Trykk på **Ctrl+J**

  - eller -
  
- Trykk på **F1**, skriv inn **UN**, velg **Opphev folding av alle** og trykk deretter på **Enter**

[![ER-formelredigeringsprogram](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)

## <a name=""></a><a name="FindAndReplace">Søk og erstatt</a>

Hvis du vil søke etter forekomster av bestemt tekst, velger du teksten i uttrykket og gjør følgende:

- Trykk på **Ctrl+F** og trykk deretter på **F3** for å finne den neste forekomsten av den valgte teksten, eller trykk på **Shift+F3** for å finne den forrige forekomsten.

  - eller -
  
- Trykk på **F1**, skriv inn **F** og velg deretter påkrevd alternativ for å finne den merkede teksten.

Hvis du vil erstatte forekomster av en bestemt tekst, velger du teksten i uttrykket og gjør følgende:

- Trykk på **Ctrl+H**. Angi den alternative teksten, og velg erstatningsalternativet for å erstatte den valgte teksten eller alle forekomstene av denne teksten i det gjeldende uttrykket.

  - eller -
  
- Trykk på **F1**, skriv inn **R** og velg deretter påkrevd alternativ for å erstatte den merkede teksten. Angi den alternative teksten, og velg erstatningsalternativet for å erstatte den valgte teksten eller alle forekomstene av denne teksten i det gjeldende uttrykket.

Hvis du vil endre alle forekomster av en bestemt tekst, velger du teksten i uttrykket og gjør følgende:

- Trykk på **CTRL+F2** og angi deretter den alternative teksten.

  - eller -
  
- Trykk på **F1**, skriv inn **C** og velg deretter påkrevd alternativ for å endre den merkede teksten. Angi den alternative teksten.

[![ER-formelredigeringsprogram](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)

## <a name=""></a><a name="DataPasting">Innliming av datakilder og funksjoner</a>

Du kan velge **Legg til datakilde**, som utfører innliming til det gjeldende uttrykket av en datakilde som er valgt på venstre **Datakilde** i-panel. Tilsvarende kan du velge **Legg til funksjonen**, som utfører innliming til det gjeldende uttrykket av en funksjon som er valgt på høyre **Funksjoner**-panel. Hvis du bruker ER-formelredigeringsprogrammet, vil en valgt funksjon eller en valgt datakilde alltid bli limt inn på slutten av det konfigurerte uttrykket. Når du bruker ER-redigeringsprogrammet med avansert formel kan en valgt funksjon eller en valgt datakilde limes inn til en hvilken som helst del av det konfigurerte uttrykket. Du må bruke markøren for å angi hvor du vil lime inn dataene.

[![ER-formelredigeringsprogram](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)

## <a name=""></a><a name="SyntaxColorization">Syntaksfargelegging</a>

Forskjellige farger brukes for øyeblikket til å utheve følgende deler av uttrykk:

- Teksten i doble parenteser som kan representere en etikett-ID for en tekstkonstant.

[![ER-formelredigeringsprogram](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)

## <a name="limitations"></a>Begrensninger

Redigeringsprogrammet støttes for øyeblikket i følgende nettlesere:

- Chrome
- Edge
- Firefox
- Opera
- Safari

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)
- [Monaco-redigeringsprogram](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]