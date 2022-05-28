---
title: Ansatte velger planer ved å bruke Ansattselvbetjening (valgfritt)
description: Dette emnet beskriver hvordan ansatte kan velge eller oppdatere fordeler.
author: twheeloc
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 68aa401487a74b9fcd186ec6cbdb268cdb41168c
ms.sourcegitcommit: e4cc43b06ef3f0f562849e2c960025cb244d6017
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743493"
---
# <a name="employees-select-plans-by-using-employee-self-service-optional"></a>Ansatte velger planer ved å bruke Ansattselvbetjening (valgfritt)


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Når en ny person ansettes, eller når en livshendelse forekommer, kan den ansatte bruke **Ansattselvbetjening** til å velge eller oppdatere fordeler under åpen registrering.

For å få tilgang til fordelene ved registrering går den ansatte til **Ansattselvbetjening** og velger **Selvbetjeningsfordeler** på flisen **Fordeler**.

På siden **Selvbetjeningsfordeler** grupperes fordelsplaner etter plantype. Hvis du vil vise fordelsplanene i en plantype, velger den ansatte en flis på **Ansattfordeler**-siden. Den ansatte får bare se fordelene de er berettiget til.

> [!IMPORTANT]
> Før en plantype kan vises i **Ansattselvbetjening** må den konfigureres. Hvis du vil ha mer informasjon, kan du se [Konfigurere ansattselvbetjening](/dynamics365/human-resources/hr-benefits-setup-employee-self-service).

Én eller flere fordeler kan velges for registrering, avhengig av plantypen. En medisinsk plantype kan for eksempel konfigureres til å begrense den ansatte til én medisinsk plan. En type livsforsikringsplan kan gi den ansatte tillatelse til å velge flere livsforsikringsplaner.

Når den ansatte har bestemt seg for hvilken plan vedkommende vil velge, kan det være nødvendig å velge avhengige. Hvis den ansatte har valgt et dekningsalternativ som er **Ansatt +1**, **Ansatt + barn** eller **Familie**, må du velge avhengige. Hvis du vil ha mer informasjon om dekningsalternativer, se [Opprette dekningsalternativer](/dynamics365/human-resources/hr-benefits-setup-coverage-options).

For å velge en fordelsplan velger den ansatte enten ellipseknappen (**...**) eller **Legg til i handlekurv**. Når den ansatte er ferdig med å legge til alle fordelsvalgene i handlekurven, velger de **Vis handlekurv**. Den ansatte tas deretter til **Planer**-siden, der de kan vise sine valgte og frafalte fordelsplaner.

Den ansatte må velge alternativet **Jeg er enig** før de kan velge **Utsjekking**-knappen. Setningen som vises til høyre for alternativet **Jeg er enig**, kan tilpasses i kategorien **Fordelsbehandling** på siden **Delte parametere for personaladministrasjon**.

Når den ansatte bekrefter valgene for fordelsplaner ved hjelp av **Ansattselvbetjening**, registreres disse valgene og vises på sidene for **Fordelsplaner for arbeider** og **masseoppdatering av fordeler for fordelsplaner**.

Når den ansatte har valgt planene, vises statusen for fordelene som **Valgt**. Når den ansatte velger **Sjekk ut** på siden **Selvbetjeningsfordeler**, velges alternativet **Utsjekket**.

> [!IMPORTANT]
> For å fullføre registreringen må fordelsadministrator velge **Bekreft** for hver av de ansattes fordeler som er valgt. Bekreftelse kan fullføres på siden **Forselsplaner for arbeider** eller **masseoppdatering av fordeler for fordelsplaner**.
>

Ansatte trenger ikke å velge fordeler ved å bruke **Ansattselvbetjening**. Fordeler kan velges på vegne av en ansatt på siden **Forselsplaner for arbeider** eller **masseoppdatering av fordeler for fordelsplaner**. Den ansatte vil ikke bli registrert i disse fordelene før fordelsadministratoren bekrefter dem.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
