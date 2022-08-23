---
title: Generere rapporter ved å legge til innhold som rå XML
description: Du kan utforme elektronisk rapportering (ER)-formater som genererer utgående dokumenter i XML-format.
author: kfend
ms.date: 05/25/2018
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
ms.openlocfilehash: 87b70d5893d71e5022205a2f39f8263edf6d5280
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277550"
---
# <a name="generate-reports-by-adding-content-as-raw-xml"></a>Generere rapporter ved å legge til innhold som rå XML

[!include[banner](../includes/banner.md)]

Du kan bruke det nye **rå XML**-formatelementet til å utforme elektronisk rapportering (ER)-formater som genererer utgående dokumenter i XML-format. I noen tilfeller kan det hende at du vil legge til rå XML-data i disse rapportene av én eller flere av følgende årsaker:

- Det er enklere å bruke rå XML for den opprinnelige utformingen og pågående vedlikehold for en rapport, fordi XML-strukturen kan genereres automatisk ved å kjøre et uttrykk i kjøretid. Derfor må ikke flere bindinger fastslås for flere formatelementer under utformingen. Det er mulig når datakildene du bruker, inneholder informasjon som kan brukes til å lage XML-elementer mens rapporten genereres.
- Ingen annen metode kan brukes til å fylle ut rapporten med XML-innhold som allerede er mottatt og lagret i systemet. XML-svaret som genereres må eksempelvis kanskje inneholde innholdet i en XML-forespørsel som ble sendt tidligere.
- Ingen annen metode kan brukes til å sette inn tegn i det genererte dokumentet basert på deres numeriske koder. Kodene for denne typen finnes ikke for noen språk og tegn. Eksempler er gresk bokstav rho (ρ) og HTML-enhetskoder som \&eacute; for en *e* med en akutt aksent (é).

> [!NOTE]
> Vær oppmerksom på at rammeverket ikke kontrollerer om XML-innhold som er plassert i det genererte dokumentet ved hjelp av **Rå XML**-formatelementet, er riktig.

Hvis du vil vite mer om denne funksjonen, kan du spille av veiledningene **ER Bruk rå XML-data til å generere XML-rapporter (del 1: Utforme datamodell)** og **ER Bruk rå XML-data til å generere XML-rapporter (del 2: Utforme og kjøre rapport)**, som er en del av **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**-forretningsprosenten og kan lastes ned fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684). Disse veiledningene forklarer deg prosessen med å konfigurere et ER-format for å sette inn rå XML-data i genererte filer.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
