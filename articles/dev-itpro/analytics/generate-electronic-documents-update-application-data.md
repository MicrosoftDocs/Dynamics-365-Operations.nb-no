---
title: "Generere elektroniske dokumenter og oppdatere programdata ved hjelp av verktøyet for elektronisk rapportering"
description: "Du kan utforme elektronisk rapportering (ER)-formater som kan brukes i Finance and Operations-programmet for å generere utgående elektroniske dokumenter. Du kan også utforme ER-formatene som analyserer innkommende elektroniske dokumenter og bruke innholdet i disse dokumentene til å oppdatere programdata."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7378c1d205b9a9cd61044dc33fc52ff75c6b94b7
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="generate-electronic-documents-and-update-application-data-using-the-electronic-reporting-tool"></a>Generere elektroniske dokumenter og oppdatere programdata ved hjelp av verktøyet for elektronisk rapportering

Du kan utforme elektronisk rapportering (ER)-formater som kan brukes i Finance and Operations-programmet for å generere utgående elektroniske dokumenter. Du kan også utforme ER-formatene som analyserer innkommende elektroniske dokumenter og bruke innholdet i disse dokumentene til å oppdatere programdata. 

Med denne funksjonen kan et enkelt ER-format brukes til å generere utgående elektroniske dokumenter, og deretter oppdatere programdataene. Denne funksjonen kan brukes i følgende scenarier:

- For å hindre gjentatt bruk av programdata i påfølgende prosesser, kan du merke et programs data umiddelbart etter at de er brukt til å generere elektroniske dokumenter. Du kan for eksempel merke betalingstransaksjoner som allerede behandlet umiddelbart etter at de er inkludert i en generert betalingsmelding.
- For å lagre behandlingsdetaljene for elektroniske dokumenter som er generert ved hjelp av ER-logikk. For eksempel en unik betalingsmeldingsidentifikasjon som genereres ved hjelp av ER-uttrykket. Uttrykket er basert på informasjonen som er angitt i ER-dialogboksennår ER-formatet kjøres for å generere dokumenter.

Hvis du vil vite mer om denne funksjonen, kan du spille av settet med oppgaveveiledninger ER Generere elektroniske dokumenter med oppdatering av programdata (del av 7.5.4.3 forretningsprosessen Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)), som leder deg gjennom detaljene for Intrastat-rapportering og arkivering. Følgende filer er nødvendig for å gjennomføre enkelte trinn i disse oppgaveveiledningene. Last ned og lagre disse filene på den lokale datamaskinen.

- [ER-datamodellkonfigurasjon: Intrastat (modell)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER-modelltilordningskonfigurasjon: Intrastat (tilordning)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER-formatkonfigurasjon: Intrastat (format)](https://go.microsoft.com/fwlink/?linkid=849038)

