---
title: Bedriftskonsept i Common Data Service
description: Dette emnet beskriver integreringen av firmadata mellom Finance and Operations og Common Data Service .
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 46a6ed9763781de8e05cff7adadf75fe2a931fdc
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997532"
---
# <a name="company-concept-in-common-data-service"></a>Bedriftskonsept i Common Data Service

[!include [banner](../../includes/banner.md)]


I Finance and Operations er konseptet av et *selskap* både en juridisk konstruksjon og en virksomhetskonstruksjon. Det er også en sikkerhets- og synlighetsgrense for data. Brukerne arbeider alltid i sammenheng med et enkelt selskap, og de fleste dataene er stripete av selskapet.

Common Data Service ikke har et tilsvarende begrep. Det nærmeste konseptet er *forretningsenhet* , som hovedsakelig er en sikkerhets- og synlighetsgrense for brukerdata. Dette konseptet har ikke de samme juridiske eller forretningsmessige implikasjoner som selskapskonsept.

Fordi forretningsenhet og firma ikke er identiske konsepter, er det ikke mulig å tvinge en en-til-en (1:1) tilordning mellom dem for formålet Common Data Service-integrering. Fordi brukere imidlertid som standard må kunne se de samme postene i programmet og Common Data Service, har Microsoft innført en ny enhet i Common Data Service som heter cdm\_firma. Denne enheten tilsvarer Firma-enheten i programmet. For å garantere at synligheten av poster er lik mellom programmet og Common Data Service ut av boksen, anbefaler vi følgende oppsett for data i Common Data Service:

+ For hver Finance and Operations Company-oppføring som er aktivert for dobbel skriving, opprettes det en tilknyttet cdm\_firmapost.
+ Når en cdm\_firmapost opprettes og aktiveres for dobbel skriving, opprettes det en standard forretningsenhet som har samme navn. Selv om det opprettes automatisk et standardteam for denne forretningsenheten, brukes ikke forretningsenheten.
+ Det opprettes et separat eierteam som har samme navn. Det er også knyttet til forretningsenheten.
+ Som standard er eieren av et oppføringsteam som er opprettet og dobbeltskrevet til Common Data Service, satt til "DW Owner"-teamet som er koblet til den tilknyttede forretningsenheten.

Illustrasjonen nedenfor viser et eksempel på dette dataoppsettet i Common Data Service.

![Dataoppsett i Common Data Service](media/dual-write-company-1.png)

På grunn av denne konfigurasjonen eies alle oppføringer som er relatert til USMF-firmaet av et team som er koblet til USMF-forretningsenheten i Common Data Service. Derfor kan en hvilken som helst bruker som har tilgang til denne forretningsenheten gjennom en sikkerhetsrolle som er satt til synlighet på forretningsenhetsnivå, nå se disse postene. Følgende eksempel viser hvordan grupper kan brukes til å gi riktig tilgang til disse postene.

+ Rollen "Salgssjef" er tilordnet medlemmer av "USMF Sales"-teamet.
+ Brukere som har "Salgssjef"-rollen, kan få tilgang til alle kontooppføringer som er medlemmer av samme forretningsenhet som de er medlemmer av.
+ "USMF Sales"-teamet er knyttet til USMF-forretningsenheten som ble nevnt tidligere.
+ Derfor kan medlemmer av "USMF Sales"-gruppen se alle kontoer som eies av "USMF DW"-brukeren, som ville ha kommet fra USMF-firmaenheten i Finance and Operations.

![Hvordan team kan brukes](media/dual-write-company-2.png)

Som den foregående illustrasjonen viser, er denne 1:1-tilordningen mellom forretningsenhet, firma og team bare et utgangspunkt. I dette eksemplet opprettes en ny forretningsenhet for "Europa" manuelt i Common Data Service som overordnet for både DEMF og ESMF. Denne nye rotforretningsenheten er ikke relatert til dobbel skriving. Den kan imidlertid brukes til å gi medlemmer av "EUR Sales"-gruppen tilgang til kontodata i både DEMF og ESMF ved å angi data synligheten til **overordnet/underordnet bu** i den tilknyttede sikkerhetsrollen.

Et siste emne for å diskutere er hvordan dobbel skriving bestemmer hvilket eierteam det skal tildeles poster til. Denne virkemåten styres av feltet **Standard eiende team** i cdm\_firmaoppføringen. Når en cdm\_firmaoppføring er aktivert for dobbel skriving, oppretter en plugin-modul automatisk den tilknyttede forretningsenheten og eiergruppen (hvis den ikke allerede finnes), og angir feltet **Standard eiende team**. Administratoren kan endre dette feltet til en annen verdi. Administratoren kan imidlertid ikke tømme feltet så lenge enheten er aktivert for dobbel skriving.

> [!div class="mx-imgBorder"]
![Feltet Standard eiende team](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Selskapets striping og bootstrapping

Common Data Service-integrasjon bringer selskapet paritet ved hjelp av en bedrifts-ID til stripe data. Som følgende illustrasjon viser, er alle firmaspesifikke enheter utvidet slik at de har en mange-til-en (N:1)-relasjon til cdm\_-firmaenheten.

> [!div class="mx-imgBorder"]
![N:1-relasjon mellom en firmaspesifikk enhet og cdm_firmaenheten](media/dual-write-bootstrapping.png)

+ Når et selskap er lagt til og lagret for poster, blir verdien skrivebeskyttet. Derfor bør brukerne sørge for at de velger riktig firma.
+ Bare poster som har firmadata, er kvalifisert for dobbelt skriving mellom programmet og Common Data Service.
+ For eksisterende Common Data Service-data, en admin-ledet bootstrapping-erfaring vil snart være anvendelig.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Autofylling av firmanavn i Customer Engagement-apper

Det finnes flere måter å fylle ut firmanavnet på automatisk i Customer Engagement-apper.

+ Hvis du er systemansvarlig, kan du velge standardfirmaet ved å navigere til **Avanserte innstillinger > System > Sikkerhet > Brukere**. Åpne **Bruker** -skjemaet, og i delen **Organisasjonsinformasjon** angir du verdien for **firma som standard på skjemaer**.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Angi standardfirma i delen Organisasjonsinformasjon.":::

+ Hvis du har **Skrive** -tilgang til **SystemUser** -enheten for nivået **Forretningsenhet** , kan du endre standardfirmaet i et hvilket som helst skjema ved å velge et firma fra rullegardinmenyen **Firma**.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Endre firmanavnet på en ny forretningsforbindelse.":::

+ Hvis du har **Skrive** -tilgang til data i mer enn ett firma, kan du endre standardfirmaet ved å velge en post som tilhører et annet firma.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Hvis du velger en post, endres standardfirmaet.":::

+ Hvis du er en systemkonfigurator eller -administrator, og du vil fylle ut firmadata automatisk i et egendefinert skjema, kan du bruke [skjemahendelser](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids). Legg til en JavaScript-referanse i **msdyn_/DefaultCompany.js** , og bruk følgende hendelser. Du kan bruke et hvilket som helst standardskjema, for eksempel i skjemaet for **Forretningsforbindelse**.

    + **OnLoad** -hendelsen for skjemaet: Angi **defaultCompany** -feltet.
    + **OnChange** -hendelse for **Firma** -feltet: Angi **updateDefaultCompany** -feltet.

## <a name="apply-filtering-based-on-the-company-context"></a>Bruk filtrering basert på firmakonteksten

Hvis du vil bruke filtrering basert på firmakonteksten i de egendefinerte skjemaene eller på egendefinerte oppslagsfelt som er lagt til i standardskjemaene, åpner du skjemaet og bruker delen **Relatert oppføringsfiltrering** for å bruke firmafilteret. Du må angi dette for hvert oppslagsfelt som krever filtrering, basert på det underliggende firmaet for en gitt post. Innstillingen vises for **Forretningsforbindelse** i følgende illustrasjon.

:::image type="content" source="media/apply-company-context.png" alt-text="Bruk firmakontekst":::

