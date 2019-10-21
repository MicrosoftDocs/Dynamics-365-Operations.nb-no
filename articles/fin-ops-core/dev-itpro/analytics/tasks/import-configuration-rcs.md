---
title: (ER) Importere konfigurasjoner fra RCS
description: Dette emnet inneholder informasjon om hvordan en bruker kan importere en ny versjon av en ER-konfigurasjon fra RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32c9c17d8b63e4c0806559c2dcc2e11ae9825a53
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184629"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Importere konfigurasjoner fra RCS

[!include [task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan importere en ny versjon av en ER-konfigurasjon (elektronisk rapportering) fra Microsoft Regulatory Configuration Services (RCS). I dette eksemplet skal du velge versjonen av ER-konfigurasjonen som er konfigurert i en RCS-forekomst, og importere den til gjeldende forekomst for eksempelfirma, Litware, Inc. Disse trinnene kan utføres i alle firmaer fordi ER-konfigurasjoner deles mellom firmaer. For å fullføre disse trinnene må du først fullføre trinnene i emnet [Opprette en konfigurasjonsleverandør og merke den som aktiv](er-configuration-provider-mark-it-active-2016-11.md). For å kunne fullføre disse trinnene må du også ha tilgang til en RCS-forekomst som inneholder minst én ER-konfigurasjon med statusen **Fullført** eller **Delt**.

1. Gå til **Organisasjonsstyring** > **Arbeidsområder** > **Elektronisk rapportering**. 
2. Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**. Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i emnet [Opprette en konfigurasjonsleverandør og merke den som aktiv](er-configuration-provider-mark-it-active-2016-11.md). 
3. Hvis du ikke har noe RCS-miljø klargjort for firmaet, klikker du på den eksterne koblingen **Regulatory Services – Configuration** og følger instruksjonene for å klargjøre et RCS-miljø. 
4. Klikk på **Parametere for elektronisk rapportering**. 
5. Klikk på **RCS**-fanen. 
6. Hvis RCS-miljøet allerede er klargjort for firmaet ditt, kan du bruke URL-adressene på siden til å få tilgang til det. 
7. Lukk siden. 

## <a name="register-a-new-er-repository"></a>Registrere et nytt ER-repositorium. 
1. Merk den valgte raden i listen. 
2. Velg leverandøren Litware, Inc. 
3. Klikk Repositorier. 
4. Klikk Legg til for å åpne nedtrekksdialogen. 
5. Angi RCS i feltet Type konfigurasjonsrepositorium. 
6. Klikk Opprett repositorium. 
7. Angi eller velg en verdi i feltet for visningsnavn på RCS-miljø. 
8. Velg ønsket RCS-forekomst. Legg merke til at du kan ha flere av dem. 
9. Klikk OK. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>Importere ER-konfigurasjoner fra RCS-basert repositorium
1. Klikk på **Vis filtre**. 
2. Angi filterverdien «RCS» i **Navn**-feltet ved hjelp av filteroperatoren **begynner med**. 
3. Når du åpner det valgte repositoriet, klikker du på koblingen **Klikk her for å koble til Regulatory Configuration Service** på siden **Koble til Regulatory Configuration Services**. 
4. Klikk på **Åpne**. 
5. Klikk **Lukk**. 
6. Velg ønsket versjon av ER-konfigurasjon, og klikk på **Importer** for å hente den inn i gjeldende forekomst.
