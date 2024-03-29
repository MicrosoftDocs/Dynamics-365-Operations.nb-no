---
title: Del opp genererte XML-filer basert på filstørrelse og innholdsmengde
description: Denne artikkelen gir informasjon om deling av genererte filer basert på filstørrelsen og innholdselementmengden.
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 5347d4e85198893dd94f14508176db93ccd47c22
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280103"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a>Dele opp genererte XML-filer basert på filstørrelse og innholdsmengde

[!include[banner](../includes/banner.md)]

Du kan utforme elektronisk rapportering (ER)-formater for å generere utgående dokumenter i XML-format. Disse dokumentene kan noen ganger kan godtas bare når de oppfyller bestemte kriterier, for eksempel maksimal filstørrelse eller maksimalt antall noen XML-noder. Du kan utforme ER-formater for å generere elektroniske dokumenter som oppfyller kravene som mottakerne av dokumentene angir.

- For FILE-formatelementet kan du definere en grense på filstørrelsen som et ER-uttrykk. Hvis den definerte grensen overskrides når en ER-rapport genereres, avslutter ER laging av filen og flytter deretter videre for å opprette den neste filen.
- For et XML ELEMENT-format kan du definere en grense for antall elementer som et ER-uttrykk. Hvis antall XML-noder i filen som genereres, overskrider den definerte grensen når en ER-rapport kjøres, avslutter ER laging av filen og flytter deretter videre for å opprette den neste filen.
- For et XML SEKVENS-formatelement kan du definere en grense for antall underordnede elementer som et ER-uttrykk. Hvis antall nestede XML-noder for formatelementet i filen som genereres, overskrider den definerte grensen når en ER-rapport kjøres, avslutter ER laging av filen og flytter deretter videre for å opprette den neste filen.
- Du kan merke XML ELEMENT-formatelementer som ikke-brytbare. På denne måten kan du organisere de nestede elementene i XML-noder som genereres under formatelementet, i én enkelt generert fil.

I tillegg til å bruke XML ELEMENT- og XML SEKVENS-formatelementene for å legge til XML-noder i den genererte filen, kan du bruke RÅ XML-formatelementet. Men noder som du legger til ved hjelp av RÅ XML-formatelementet, vurderes ikke når antall noder beregnes for å evaluere grensene for antall elementer.

Hvis du har konfigurert filmålene for et FILE-formatelement som er konfigurert for å dele de genererte utdataene når spesifikke grenser er overskredet, sendes hver del av genererte utdata til den konfigurerte fildestinasjonen som en enkeltfil. For å gi et unikt navn til filene som opprettes ved å dele utdataene, må du konfigurere et ER-uttrykk for FILE-formatelementet. Hvis du tar med en ER-datakilde av NUMMERSERIE-typen, øker nummerserien for hver del av de delte utdataene.

Hvis du vil vite mer om denne funksjonen, spiller du av oppgaveveiledningen **ER Del XML-filer basert på filstørrelse eller innholdselementmengde**, som er en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**, og kan være lastet ned fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684). Denne oppgaveveiledning hjelper deg med å konfigurere et ER-format for å dele genererte filer basert på begrensninger på filstørrelse og innholdselementmengde. For å fullføre oppgaveveiledning må du laste ned følgende filer:

- [ER-modellkonfigurasjon - XmlFilesSplittingModel.xml](https://download.microsoft.com/download/e/a/f/eaffe96a-22ec-4a32-898a-f4328c91c387/XmlFilesSplittingModel.xml)
- [ER-formatkonfigurasjon - XmlFilesSplittingFormat.xml](https://download.microsoft.com/download/e/9/c/e9c5849b-8254-4cdf-bb00-4c2ebc72ddec/XmlFilesSplittingFormat.xml)

## <a name="additional-resources"></a>Tilleggsressurser
[Mål for elektronisk rapportering (ER)](electronic-reporting-destinations.md)

[Formeldesigner i elektronisk rapportering (ER)](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
