---
title: Generere elektroniske dokumenter og oppdatere programdata ved hjelp av ER
description: Du kan utforme elektronisk rapportering (ER)-formater som kan brukes i programmet for å generere utgående elektroniske dokumenter.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5f78f3b36a1aebfb263d64ccf2293097eb9af6e6de1ab49de39b18e1c318950
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765814"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>Generere elektroniske dokumenter og oppdatere programdata ved hjelp av ER

[!include [banner](../includes/banner.md)]

Du kan utforme elektronisk rapportering (ER)-formater som kan brukes i programmet for å generere utgående elektroniske dokumenter. Du kan også utforme ER-formatene som analyserer innkommende elektroniske dokumenter og bruke innholdet i disse dokumentene til å oppdatere programdata.

Med denne funksjonen kan et enkelt ER-format brukes til å generere utgående elektroniske dokumenter, og deretter oppdatere programdataene. Denne funksjonen kan brukes i følgende scenarier:

- For å hindre gjentatt bruk av programdata i påfølgende prosesser, kan du merke et programs data umiddelbart etter at de er brukt til å generere elektroniske dokumenter. Du kan for eksempel merke betalingstransaksjoner som allerede behandlet umiddelbart etter at de er inkludert i en generert betalingsmelding.
- For å lagre behandlingsdetaljene for elektroniske dokumenter som er generert ved hjelp av ER-logikk. For eksempel en unik betalingsmeldingsidentifikasjon som genereres ved hjelp av ER-uttrykket. Uttrykket er basert på informasjonen som er angitt i ER-dialogboksennår ER-formatet kjøres for å generere dokumenter.

Hvis du vil vite mer om denne funksjonen, kan du spille av settet med oppgaveveiledninger ER Generere elektroniske dokumenter med oppdatering av programdata (del av 7.5.4.3 forretningsprosessen Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)), som leder deg gjennom detaljene for Intrastat-rapportering og arkivering. Følgende filer er nødvendig for å gjennomføre enkelte trinn i disse oppgaveveiledningene. Last ned og lagre disse filene på den lokale datamaskinen.

- [ER-datamodellkonfigurasjon: Intrastat (modell)](https://download.microsoft.com/download/9/c/e/9ceeacbe-c13e-422e-96f2-594c4a6b45b7/Intrastatmodel.xml)
- [ER-modelltilordningskonfigurasjon: Intrastat (tilordning)](https://download.microsoft.com/download/2/1/d/21ddaaeb-64c5-4408-a35f-1ccb922d40a4/Intrastatmapping.xml)
- [ER-formatkonfigurasjon: Intrastat (format)](https://download.microsoft.com/download/8/b/b/8bbb8891-e88d-4739-b92a-2d1d2fffcb79/Intrastatformat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
