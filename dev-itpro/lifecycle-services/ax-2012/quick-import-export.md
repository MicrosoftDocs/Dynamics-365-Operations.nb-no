---
title: Bruke hurtigimport/-eksport
description: "Formålet med hurtigimport/-eksport er å la deg importere og eksportere med færre trinn."
author: margoc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 2012 R3 CU8
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: f35e7b7d987d6caa19a32460259f07322f2b85cb
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="run-the-test-data-transfer-tool-beta-for-dynamics-ax-ax-2012"></a>Kjøre overføringsverktøy for testdata (beta) for Dynamics AX (AX 2012)

[!include[banner](../../includes/banner.md)]


Formålet med hurtigimport/-eksport er å la deg importere og eksportere med færre trinn.

Vi har lagt til funksjonen for hurtigimport/-eksport for å la brukere importere eller eksportere enkle jobber som skal utføres raskt. Ideelt sett brukes denne funksjonen i situasjoner som automatisk tilordner en fil til systemet og brukeren ikke trenger å gå gjennom avansert tilordning eller opprette gjentatte import- eller eksportjobber.

-   Denne funksjonen støtter arbeid med både medfølgende og egendefinerte enheter.
-   Du kan importere fra filer, og hvis du bruker en ODBC-datakilde, kan du velge en spørring til bruk for å definere importen.
-   Du må ha tidligere definerte kildedataformater for AX eller Fil, og vite hvor de befinner seg.
-   Du trenger ikke å opprette en behandlingsgruppe for å bruke hurtigimport/-eksport. Systemet oppretter en automatisk når du import- eller eksportjobben utføres. Du kan også velge å beholde historikken over dataene som importeres med hurtigimport/-eksport.

  Vær oppmerksom på at hurtigimport/-eksport forutsetter at du er kjent med DIXF-konseptet.




