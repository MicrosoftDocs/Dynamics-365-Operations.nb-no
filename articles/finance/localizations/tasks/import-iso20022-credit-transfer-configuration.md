---
title: Importere konfigurasjon for ISO20022-kredittoverføring
description: Denne fremgangsmåten viser hvordan du importerer en konfigurasjon for elektronisk rapportering for leverandørbetalinger.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a96827bc6e126a7f5de6d67338b5233a65d93c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840919"
---
# <a name="import-iso20022-credit-transfer-configuration"></a>Importere konfigurasjon for ISO20022-kredittoverføring

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du importerer en konfigurasjon for elektronisk rapportering for leverandørbetalinger. Det tysk kredittoverføringsformatet ISO 20022 brukes som et eksempel. Denne prosedyren kan brukes for andre tilgjengelige elektroniske rapporteringsformat. 

Denne oppgaven ble opprettet ved hjelp av demonstrasjonsdatafirmaet DEMF, men du kan bruke et hvilket som helst demonstrasjonsdatafirma til å fullføre denne oppgaven.

Dette er den første av fem oppgaver, som illustrerer leverandørbetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering. Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.

1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
2. I listen over tilgjengelige konfigurasjonsleverandører velger du Microsoft.
3. Klikk Angi som aktiv
4. Klikk Repositorier.
5. Klikk Åpne.
6. Klikk Vis filtre.
7. Bruk følgende filtre: Angi filterverdien "ISO20022-kredittoverføring (DE)" i feltet Konfigurasjonsnavn ved hjelp av filteroperatoren "begynner med".
    * Du kan også finne konfigurasjonen i listen, velge den og deretter flytte den til importoppgaven.  
8. Klikk Importer.
    * Hvis Importer-knappen ikke er tilgjengelig, betyr det at konfigurasjonen allerede er importert.  
9. Klikk Ja.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]