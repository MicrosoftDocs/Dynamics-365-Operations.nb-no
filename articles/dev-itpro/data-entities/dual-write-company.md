---
title: Bedriftskonsept i Common Data Service
description: Dette emnet beskriver integreringen av firmadata mellom Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6eddd87c3ad3ea9de8aec2874b0514faa65374f1
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789229"
---
## <a name="company-concept-in-common-data-service"></a>Bedriftskonsept i Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

I Microsoft Dynamics 365 for Finance and Operations er konseptet av et *selskap* både en juridisk konstruksjon og en virksomhetskonstruksjon. Det er også en sikkerhets- og synlighetsgrense for data. Brukerne arbeider alltid i sammenheng med et enkelt selskap, og de fleste dataene er stripete av selskapet.

Common Data Service ikke har et tilsvarende begrep. Det nærmeste konseptet er *forretningsenhet*, som hovedsakelig er en sikkerhets- og synlighetsgrense for brukerdata. Dette konseptet har ikke de samme juridiske eller forretningsmessige implikasjoner som selskapskonsept i Finance and Operations.

Fordi forretningsenhet og firma ikke er identiske konsepter, er det ikke mulig å tvinge en en-til-en (1:1) tilordning mellom dem for formålet Common Data Service-integrering. Men fordi brukere må, som standard, kunne se de samme postene i Finance and Operations og Common Data Service, har Microsoft innført en ny enhet i Common Data Service som heter cdm\_firma. Denne enheten tilsvarer firma-enheten i Finance and Operations. For å garantere at synligheten av poster er ekvivalent mellom Finance and Operations og Common Data Service ut av boksen, anbefaler vi følgende oppsett for data i Common Data Service:

+ For hver Finance and Operations Company-oppføring som er aktivert for dobbel skriving, opprettes det en tilknyttet cdm\_firmapost.
+ Når en cdm\_firmapost opprettes og aktiveres for dobbel skriving, opprettes det en standard forretningsenhet som har samme navn. Selv om det opprettes automatisk et standardteam for denne forretningsenheten, brukes ikke forretningsenheten.
+ Det opprettes et separat eierteam som har samme navn. Det er også knyttet til forretningsenheten.
+ Som standard er eieren av et oppføringsteam som er opprettet i Finance and Operations og dobbeltskrevet til Common Data Service, satt til "DW Owner"-teamet som er koblet til den tilknyttede forretningsenheten.

Illustrasjonen nedenfor viser et eksempel på dette dataoppsettet i Common Data Service.

![Dataoppsett i Common Data Service](media/dual-write-company-1.png)

På grunn av denne konfigurasjonen eies alle Finance and Operations-oppføringer som er relatert til USMF-firmaet av et team som er koblet til USMF-forretningsenheten i Common Data Service. Derfor kan en hvilken som helst bruker som har tilgang til denne forretningsenheten gjennom en sikkerhetsrolle som er satt til synlighet på forretningsenhetsnivå, nå se disse postene. Følgende eksempel viser hvordan grupper kan brukes til å gi riktig tilgang til disse postene.

+ Rollen "Salgssjef" er tilordnet medlemmer av "USMF Sales"-teamet.
+ Brukere som har "Salgssjef"-rollen, kan få tilgang til alle kontooppføringer som er medlemmer av samme forretningsenhet som de er medlemmer av.
+ "USMF Sales"-teamet er knyttet til USMF-forretningsenheten som ble nevnt tidligere.
+ Derfor kan medlemmer av "USMF Sales"-gruppen se alle kontoer som eies av "USMF DW"-brukeren, som ville ha kommet fra USMF-firmaenheten i Finance and Operations.

![Hvordan team kan brukes](media/dual-write-company-2.png)

Som den foregående illustrasjonen viser, er denne 1:1-tilordningen mellom forretningsenhet, firma og team bare et utgangspunkt. I dette eksemplet opprettes en ny forretningsenhet for "Europa" manuelt i Common Data Service som overordnet for både DEMF og ESMF. Denne nye rotforretningsenheten er ikke relatert til dobbel skriving. Den kan imidlertid brukes til å gi medlemmer av "EUR Sales"-gruppen tilgang til kontodata i både DEMF og ESMF ved å angi data synligheten til **overordnet/underordnet bu** i den tilknyttede sikkerhetsrollen.

Et siste emne for å diskutere er hvordan dobbel skriving bestemmer hvilket eierteam det skal tildeles poster til. Denne virkemåten styres av feltet **Standard eiende team** i cdm\_firmaoppføringen. Når en cdm\_firmaoppføring er aktivert for dobbel skriving, oppretter en plugin-modul automatisk den tilknyttede forretningsenheten og eiergruppen (hvis den ikke allerede finnes), og angir feltet **Standard eiende team**. Administratoren kan endre dette feltet til en annen verdi. Administratoren kan imidlertid ikke tømme feltet så lenge enheten er aktivert for dobbel skriving.

![Feltet Standard eiende team](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Selskapets striping og bootstrapping

Common Data Service-integrasjon bringer selskapet paritet ved hjelp av en bedrifts-ID til stripe data. Som følgende illustrasjon viser, er alle firmaspesifikke enheter utvidet slik at de har en mange-til-en (N:1)-relasjon til cdm\_-firmaenheten.

![N:1-relasjon mellom en firmaspesifikk enhet og cdm_firmaenheten](media/dual-write-bootstrapping.png)

+ Når et selskap er lagt til og lagret for poster, blir verdien skrivebeskyttet. Derfor bør brukerne sørge for at de velger riktig firma.
+ Bare poster som har firmadata, er kvalifisert for dobbelt skriving mellom Finance and Operations og Common Data Service.
+ For eksisterende Common Data Service-data, en admin-ledet bootstrapping-erfaring vil snart være anvendelig.
