---
title: Mobilapp for timeregistreringer for prosjekt
description: Dette emnet gir informasjon om Microsoft Dynamics 365 Project Timesheet-mobilappen. Project Timesheet-mobilappen gjør det mulig for brukere å sende og godkjenne timeregistreringer for prosjekter på mobilenheten.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: josaw1
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a475085001b8fa10814c864ef35129eb6ebfdfef
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/12/2019
ms.locfileid: "969685"
---
# <a name="microsoft-dynamics-365-project-timesheet-mobile-application"></a>Microsoft Dynamics 365 Project Timesheet-mobilappen

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Oversikt

Microsoft Dynamics 365 Project Timesheet-mobilappen gjør det mulig for brukere å sende og godkjenne timeregistreringer for prosjekter på mobilenheten (iPhone eller Android). Denne mobilappen viser timeregistreringsfunksjonaliteten som befinner seg i prosjektstyrings- og regnskapsområdet på Microsoft Dynamics 365 for Finance and Operations, som forbedrer brukernes produktivitet og effektivitet og gjør det mulig å legge inn oppføringer til rett tid og godkjenne timeregistreringer for prosjekt.

## <a name="download-and-install-the-mobile-app"></a>Laste ned og installere mobilappen

Last ned og installer Microsoft Dynamics 365 Project Timesheet-mobilappen for Android eller iPhone fra mobilbutikken for enheten.

## <a name="enable-the-app"></a>Aktivere appen 

I Dynamics 365 for Finance and Operations må Project Timesheet-mobilappen være aktivert. Hvis du vil aktivere funksjonen, kan du gå til **Parametere for prosjektstyring og regnskap \> Timeregistrering** og velge **Aktiver Microsoft Dynamics 365 Project Timesheet**-parameteren.

## <a name="sign-in-to-the-app"></a>Logge på appen

1.  Start appen på mobilenheten.

2.  Angi URL-adressen for Microsoft Dynamics 365 for Finance and Operations.

3.  Første gang du logger deg på, blir du bedt om brukernavn og passord. Angi legitimasjon.

4.  Du blir logget på standardfirmaet ditt.

## <a name="submit-a-project-timesheet"></a>Sende inn en prosjekttimeliste

Du kan opprette og sende en prosjekttimeliste i appen. Du kan også basere en ny timeregistrering på informasjon fra en tidligere timeregistrering, lagrede linjer eller prosjekttilordninger. Hvis du er tilordnet som representant, kan du også angi en timeregistrering for en annen arbeider. Hvis du vil opprette en timeregistrering som representant, kan du velge **Meny**-knappen og deretter velge et ressursnavn.

Timeregistreringssiden oppretter en ny timeliste for timeregistreringsperioden basert på gjeldende dato. Arbeidsuken vises. Hvis timeregistreringsperioden dekker flere uker, kan du velge en annen arbeidsuke fra arbeidsukefanene.
Hvis det finnes en timeregistrering for gjeldende dato, vil den vises. Hvis du må opprette en ny timeliste i en annen timeregistreringsperiode, velger du **Meny**-knappen og deretter **Ny timeliste**.

Du kan angi prosjektinformasjon ved å klikke **Legg til tidspunkt**-handlingen eller **Kopier tidspunkt fra**-handlingen. Handlingen **Kopier tidspunkt fra** kopierer prosjektlinjeinformasjon, men ikke timene. **Kopier tidspunkt fra**-menyen inneholder følgende alternativer:

- **Kopier fra eksisterende timeregistrering** – Kopier timeregistreringslinjer fra en eksisterende timeregistrering.

- **Kopier fra favoritt** – Opprett nye timeregistreringslinjer ved å bruke timeregistreringsinnstillingene du valgte som favoritter.

- **Kopier fra tilordning** – Opprett nye timeregistreringslinjer fra tilordnede prosjekter.

Prosjektinformasjon som vises, er avhengig av mobilparameterne som du definerte på siden **Parametere for prosjektstyring og regnskap**.

I feltet **Juridisk enhet** velger du den juridiske enheten som du utførte prosjektarbeid for. **Juridisk enhet**-feltet er bare tilgjengelig hvis støtte for konsernintern timeregistrering er aktivert for den juridiske enheten.

Velg kunden som er knyttet til prosjektet for timeregistreringen. I den første versjonen av Android støttes ikke oppføring via kunde, fordi du må velge prosjektet først. Hvis du valgte prosjektet først, fylles **Kunde**-feltet ut automatisk.

Velg prosjektet du angir timer for, i **Prosjekt**-feltet. **Kunde**-feltet fylles automatisk ut.

Kunde- og prosjektoppslag gjør det mulig å søke på tvers av kunder og prosjekter.

Velg informasjon i feltene **Kategori**, **Aktivitet**, **Linjeegenskap**, **Merverdiavgiftsgruppe** og **Varens mva-gruppe** etter behov. Disse feltene kan overstyres.

**Linjeegenskap**-feltet settes til en standardverdi basert på prosjektstyrings- og regnskapsparametere. Når parameterne prosjekt/kategori og kategori/ressurs er aktivert, vil **Linjeegenskap**-verdien settes til standardverdien som er definert for denne valideringen. Når parameterne prosjekt/kategori og kategori/ressurs ikke er aktivert, vil **Linjeegenskap**-verdien angis som standard i henhold til feltet **Aktiver standard linjeegenskap** på siden **Parametere for prosjektstyring og regnskap**. **Linjeegenskap**-verdien kan ikke overskrives.

Velg en dag for å legge til tid. Angi antall arbeidstimer du jobbet hver dag.

Hvis du vil legge til kommentarer om timene du angir, klikker du **Legg til kommentarer**, og deretter skriver du inn kommentarer for en intern målgruppe, kundemålgruppe eller begge.
Interne kommentarer kan vises av prosjektledere. Kundekommentarer inkluderes på fakturaer.

For å lagre linjen som en favoritt merker du av i avmerkingsboksen og klikker deretter **Lagre som favoritt**.

Finansdimensjons- og vedleggsstøtte finnes ikke i mobilapplikasjonen.

Fortsett å legge til prosjektlinjer etter behov for å fylle ut timeregistreringen.

Klikk **Send** for å sende timeregistreringen til arbeidsflyten for godkjenning.

## <a name="review-timesheets"></a>Gjennomgå timeregistreringer

En liste over timeregistreringene som skal gjennomgås, er tilgjengelige på menyen. Dette alternativet er bare tilgjengelig hvis du er oppnevnt som godkjenner i arbeidsflyten. Både hode- og linjegodkjenning støttes. Linjenivågodkjenning gjør det mulighet å merke én eller flere linjer for godkjenning. Når du har sett gjennom timeregistreringsinformasjonen, klikker du **Godkjenn**, **Deleger** eller **Returner** for å fortsette arbeidsflyten.
