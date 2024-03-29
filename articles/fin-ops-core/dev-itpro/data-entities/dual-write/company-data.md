---
title: Firmabegrep i Dataverse
description: Denne artikkelen beskriver integreringen av firmadata mellom Finance and Operations og Dataverse.
author: RamaKrishnamoorthy
ms.date: 08/04/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2bdd99b581be453616e71d0f0f95a7daf75a253a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289782"
---
# <a name="company-concept-in-dataverse"></a>Firmabegrep i Dataverse

[!include [banner](../../includes/banner.md)]




I Finance and Operations er konseptet av et *selskap* både en juridisk konstruksjon og en virksomhetskonstruksjon. Det er også en sikkerhets- og synlighetsgrense for data. Brukerne arbeider alltid i sammenheng med et enkelt selskap, og de fleste dataene er stripete av selskapet.

Dataverse ikke har et tilsvarende begrep. Det nærmeste konseptet er *forretningsenhet*, som hovedsakelig er en sikkerhets- og synlighetsgrense for brukerdata. Dette konseptet har ikke de samme juridiske eller forretningsmessige implikasjoner som selskapskonsept.

Fordi forretningsenhet og firma ikke er identiske konsepter, er det ikke mulig å tvinge en en-til-en (1:1) tilordning mellom dem for formålet Dataverse-integrering. Siden brukere imidlertid som standard må kunne se de samme radene i programmet og Dataverse, har Microsoft innført en ny tabell i Dataverse kalt cdm\_Company. Denne tabellen tilsvarer Firma-tabellen i programmet. For å garantere at synligheten til rader er lik mellom programmet og Dataverse fra starten av, anbefaler vi følgende oppsett for data i Dataverse:

+ For hver firmarad i Finance and Operations som er aktivert for dobbel skriving, opprettes det en tilknyttet cdm\_firmarad.

+ Når en cdm\_Company-rad opprettes og aktiveres for dobbel skriving, opprettes det en standard forretningsenhet som har samme navn. Selv om det opprettes automatisk et standard eierteam for denne forretningsenheten, brukes ikke forretningsenheten.
+ Det opprettes et separat eierteam som har samme navn, med et suffiks for dobbel skriving. Det er også knyttet til forretningsenheten.

+ Som standard er eieren av enhver rad som er opprettet og dobbeltskrevet til Dataverse, satt til DW Owner-teamet som er koblet til den tilknyttede forretningsenheten.

Illustrasjonen nedenfor viser et eksempel på dette dataoppsettet i Dataverse.

![Dataoppsett i Dataverse.](media/dual-write-company-1.png)

På grunn av denne konfigurasjonen eies alle rader som er relatert til USMF-firmaet, av et team som er koblet til USMF-forretningsenheten i Dataverse. Derfor kan en hvilken som helst bruker som har tilgang til denne forretningsenheten gjennom en sikkerhetsrolle som er satt til synlighet på forretningsenhetsnivå, nå se disse radene. Følgende eksempel viser hvordan grupper kan brukes til å gi riktig tilgang til disse radene.

+ Rollen "Salgssjef" er tilordnet medlemmer av "USMF Sales"-teamet.
+ Brukere som har Salgssjef-rollen, kan få tilgang til alle kontorader som er medlemmer av samme forretningsenhet som de er medlemmer av.
+ "USMF Sales"-teamet er knyttet til USMF-forretningsenheten som ble nevnt tidligere.
+ Derfor kan medlemmer av "USMF Sales"-gruppen se alle kontoer som eies av "USMF DW"-brukeren, som ville ha kommet fra USMF-firmatabellen i Finance and Operations.

![Hvordan team kan brukes.](media/dual-write-company-2.png)

Som den foregående illustrasjonen viser, er denne 1:1-tilordningen mellom forretningsenhet, firma og team bare et utgangspunkt. I dette eksemplet opprettes en ny forretningsenhet for "Europa" manuelt i Dataverse som overordnet for både DEMF og ESMF. Denne nye rotforretningsenheten er ikke relatert til dobbel skriving. Den kan imidlertid brukes til å gi medlemmer av "EUR Sales"-gruppen tilgang til kontodata i både DEMF og ESMF ved å angi data synligheten til **overordnet/underordnet bu** i den tilknyttede sikkerhetsrollen.

Et siste artikkelen for å diskutere er hvordan dobbel skriving bestemmer hvilket eierteam det skal tildeles rader til. Denne virkemåten styres av kolonnen **Standard eiende team** i cdm\_Company-raden. Når en cdm\_Company-rad er aktivert for dobbel skriving, oppretter en plugin-modul automatisk den tilknyttede forretningsenheten og eiergruppen (hvis den ikke allerede finnes), og angir kolonnen **Standard eiende team**. Administratoren kan endre denne kolonnen til en annen verdi. Administratoren kan imidlertid ikke tømme kolonnen så lenge tabellen er aktivert for dobbel skriving.

> [!div class="mx-imgBorder"]
![Kolonnen Standard eiende team.](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Selskapets striping og bootstrapping

Dataverse-integrasjon bringer selskapet paritet ved hjelp av en bedrifts-ID til stripe data. Som følgende illustrasjon viser, er alle firmaspesifikke tabeller utvidet slik at de har en mange-til-én-relasjon (N:1) til cdm\_Company-tabellen.

> [!div class="mx-imgBorder"]
![N:1-relasjon mellom en firmaspesifikk tabell og cdm_Company-tabellen.](media/dual-write-bootstrapping.png)

+ Når et selskap er lagt til og lagret for rader, blir verdien skrivebeskyttet. Derfor bør brukerne sørge for at de velger riktig firma.
+ Bare rader som har firmadata, er kvalifisert for dobbelt skriving mellom programmet og Dataverse.
+ For eksisterende Dataverse-data, en admin-ledet bootstrapping-erfaring vil snart være anvendelig.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Autofylling av firmanavn i Customer Engagement-apper

Det finnes flere måter å fylle ut firmanavnet på automatisk i Customer Engagement-apper.

+ Hvis du er systemansvarlig, kan du velge standardfirmaet ved å navigere til **Avanserte innstillinger > System > Sikkerhet > Brukere**. Åpne **Bruker**-skjemaet, og i delen **Organisasjonsinformasjon** angir du verdien for **firma som standard på skjemaer**.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Angi standardfirma i delen Organisasjonsinformasjon.":::

+ Hvis du har **Skrive**-tilgang til **SystemUser**-tabellen for nivået **Forretningsenhet**, kan du endre standardfirmaet i et hvilket som helst skjema ved å velge et firma på rullegardinmenyen **Firma**.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Endre firmanavnet på en ny forretningsforbindelse.":::

+ Hvis du har **Skrive**-tilgang til data i flere firmaer, kan du endre standardfirmaet ved å velge en rad som tilhører et annet firma.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Hvis du velger en rad, endres standardfirmaet.":::

+ Hvis du er en systemkonfigurator eller -administrator, og du vil fylle ut firmadata automatisk i et egendefinert skjema, kan du bruke [skjemahendelser](/powerapps/developer/model-driven-apps/clientapi/events-forms-grids). Legg til en JavaScript-referanse i **msdyn_/DefaultCompany.js**, og bruk følgende hendelser. Du kan bruke et hvilket som helst standardskjema, for eksempel i skjemaet for **Forretningsforbindelse**.

    + **OnLoad**-hendelsen for skjemaet: Angi **defaultCompany**-kolonnen.
    + **OnChange**-hendelse for **Firma**-kolonnen: Angi kolonnen **updateDefaultCompany**.

## <a name="apply-filtering-based-on-the-company-context"></a>Bruk filtrering basert på firmakonteksten

Hvis du vil bruke filtrering basert på firmakonteksten i de egendefinerte skjemaene eller på egendefinerte oppslagskolonner som er lagt til i standardskjemaene, åpner du skjemaet og bruker delen **Relatert oppføringsfiltrering** til å bruke firmafilteret. Du må angi dette for hver oppslagskolonne som krever filtrering, basert på det underliggende firmaet for en gitt rad. Innstillingen vises for **Forretningsforbindelse** i følgende illustrasjon.

:::image type="content" source="media/apply-company-context.png" alt-text="Bruk firmakontekst.":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
