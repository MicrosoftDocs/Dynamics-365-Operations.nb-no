---
title: Datamaler med flere regneark
description: Denne artikkelen beskriver hvordan du importerer data ved hjelp av Excel-dataenhetsmaler til Økonomi og drift.
author: peakerbl
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: eaad6f433329dd42c7ab6db839f2f9e61de91a13
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881108"
---
# <a name="data-templates-with-multiple-worksheets"></a>Datamaler med flere regneark

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Databehandling i programmet støtter Microsoft Excel-baserte maler for dataenheter. Disse malene kan inneholde ett eller flere regneark. Maler med flere regneark brukes ofte når det passer å behandle data i en enkelt fil og importere den til flere dataenheter. Et eksempel er områder og lagre.

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a>Laste opp en fil én gang og tilordne den til alle enheter
La oss et eksempel der det er én Excel-fil med regneark som heter **Områder** og **Lagre**. For å definere dataimportprosjektet ville du lagt til den første dataenheten, **Områder**, og deretter lastet opp filen. Du vil kunne velge **Områder** som regnearket som skal brukes for denne enheten.

Hvis du legger til den andre enheten, **Lagre**, uten å forlate **Legg til fil**-skjemaet, vil regnearkoppslaget la deg velge **Lagre**-regnearket uten at du må laste opp filen på nytt. Den eneste grunnen til å laste opp en ny fil ville være hvis **Lagre**-dataene var i en annen fil.

![Flere regneark.](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a>Ordne tilordning av regneark til enhet

Tilordningen av regnearket til en dataenhet i importjobben kan ordnes fra rutenettet. **Regneark**-kolonnen i rutenettet viser regnearkene fra filen som ble tilknyttet. Du kan velge et annet regneark fra rullegardinlistemenyen. Hvis det valgte regnearket allerede er tilordnet en enhet i dataprosjektet, ber systemet deg om å bekrefte endringen. Vi anbefaler at du order alle tilordninger i rutenettet.

![Oppdatere regnearktilordning.](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a>Tilordne på nytt til en ny fil

I tilfeller der en ny versjon av samme fil eller en helt ny fil må lastes opp for eksisterende enheter i et dataprosjekt, må du bruke **Legg til fil**, og legge til enheter på nytt som om de ble lagt til for første gang. Systemet vil bekrefte at du vil overskrive eksisterende enheter i dataprosjektet før du fortsetter. Enheter som ikke legges til på nytt (eller overskrives), vil fortsatt inneholde de tidligere tilordningene fra den forrige filen.

## <a name="upload-a-file-using-run-project"></a>Laste opp en fil ved hjelp av Kjør prosjekt

Du kan laste opp en Excel-fil når du bruker **Kjør prosjekt**-alternativet for å kjøre et importprosjekt. Du må være forsiktig og bare laste opp filer som har de samme regnearkene som de eksisterende tilordningene på dataenhetene i dataprosjektet. Hvis et regneark ikke finnes i den nylig opplastede filen, vises en feilmelding og importen stoppes. Hvis tilordningen til regnearket må endres for en enhet, må tilordningene i dataprosjektet først oppdateres fra dataprosjektet før du kan bruke filen i **Kjør prosjekt**-opplevelsen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
