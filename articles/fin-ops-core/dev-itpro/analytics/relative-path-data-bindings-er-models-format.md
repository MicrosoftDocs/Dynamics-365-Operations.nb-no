---
title: Bruke en relativ bane i databindinger for ER-modeller og -formater
description: Med verktøyet for elektronisk rapportering kan du definere elektroniske formatstrukturer og deretter beskrive hvordan disse strukturene skal fylles.
author: NickSelin
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 141d58c2183c386584b0b974f4997e7a81ef3109
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749992"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>Bruke en relativ bane i databindinger for ER-modeller og -formater

[!include[banner](../includes/banner.md)]

Med verktøyet for elektronisk rapportering (ER) kan brukere definere elektroniske formatstrukturer og deretter beskrive hvordan disse strukturene skal fylles ved hjelp av data og algoritmer som finnes i programmet. Hvis du vil ha mer informasjon, kan du se [Opprette ER-konfigurasjoner (elektronisk rapportering)](electronic-reporting-configuration.md). Hvis du vil angi dataflyten for å hente Finance and Operations-data og bruke dem til å generere et elektronisk dokument, må du gjøre følgende:

- Bind konfigurerte datakilder til elementer i den utformede domenespesifikke [datamodellen](general-electronic-reporting.md#data-model-and-model-mapping-components). Modellstrukturen og de valgte datakildene kan være del av en kompleks hierarkisk struktur. Endelige bindinger kan på grunn av dette være ganske store og inneholde mange elementer av forskjellige typer (for eksempel relasjoner, tabeller og metoder). Bindingene kan bli mindre lesbare og svært vanskelige å se gjennom og forstå, særlig for ikke-eiere. 
- Bind datamodellelementer til [formatkomponenter](general-electronic-reporting.md#FormatComponentOutbound) for å definere hvilke data som skal fylles inn fra datamodellen i det genererte formatets utdata.

Funksjonen for [relativ bane](er-formula-language.md#relative-path) har blitt utgitt for å forbedre anvendeligheten av ER-tilordningsutforminger. Alternativet for relativ bane er som standard aktivert for nye forekomster av programmet der ER-utformingsopplevelsen er gjeldende (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service). Vi implementerte parameteren for relativ bane, slik at brukerne kan fortsette å bruke hele banen når de arbeider med denne presentasjonen av ER-bindinger.

[![Brukerparametere](./media/relative-path-01.png)](./media/relative-path-01.png)

 
Når parameteren for bruk av relativ bane er aktivert, erstatter ett @-tegn banen til det overordnede elementet i bindingen for det gjeldende modellelementet. Hele bindingsbanen blir kortere, noe som gjør hele tilordningen tydeligere og enklere å forstå. I de fleste tilfeller kreves ingen ytterligere rulling i ER-utformingen for å vise alle bindingene for datamodellen.

[![Modelltilordningsutforming](./media/relative-path-02.png)](./media/relative-path-02.png)
 
Når du begynner å utforme et nytt ER-uttrykk, trenger du bare å angi ett tegn for å definere en binding til et felt i det overordnede elementet.

[![Formeldesigner](./media/relative-path-03.png)](./media/relative-path-03.png)
 
Når du beslutter å endre datakilden for det overordnede modellelementet og bruker absolutt bane, må du binde dette modellelementet på nytt manuelt, i tillegg til alle nestede elementer, til en ny datakilde. Når bruk av relativ bane er aktivert og du velger en ny datakilde som skal bindes til et overordnet element, kan du velge et alternativ for å binde alle nestede elementer på nytt automatisk for det overordnede elementet med ett klikk.

[![Melding om å erstatte eksisterende bane](./media/relative-path-04.png)](./media/relative-path-04.png)
 
Hvis du bekrefter at nestede elementer skal bindes på nytt, blir det nye overordnede elementet lagt i banen til hvert nestede element som inneholder det eksisterende overordnede elementet.
Denne funksjonen ødelegger ikke bakoverkompatibiliteten til ER-rammeverket. Alle tidligere utformede ER-konfigurasjoner fungerer med denne nye funksjonen, og ingen oppgraderinger eller konverteringer er nødvendige.

> [!NOTE]
> Alle endringer som forårsakes av masseendring av bindinger for nestede elementer i modelltilordninger, lagres riktig i konfigurasjonsdelta (sporing av endringer). Dermed kan kundene rebasere den avledede versjonen av modelltilordninger til en hvilken som helst ny basisversjon av den som er endret ved hjelp av denne nye funksjonen.

## <a name="additional-resources"></a>Tilleggsressurser

[ER-formelspråk](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]