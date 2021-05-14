---
title: Aktivere innsjekkingsmeldinger for kunde på salgsstedet
description: Dette emnet beskriver hvordan du aktiverer innsjekkingsmeldinger for kunde på Microsoft Dynamics 365 Commerce-salgsstedet.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e4defc15d9ef198a361934d51e31016747dbb5ab
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937606"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Aktivere innsjekkingsmeldinger for kunde på salgsstedet

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet beskriver hvordan du aktiverer innsjekkingsmeldinger for kunde på Microsoft Dynamics 365 Commerce-salgsstedet.

I e-postene "Ordre klar for henting" kan organisasjoner gi en kobling eller knapp som kundene kan bruke til å varsle butikken om at de er på stedet og venter på at pakken deres skal sendes ut til dem. Kundene mottar deretter en innsjekkingsbekreftelse, og butikken mottar et varsel som en oppgave i salgsstedsprogrammet. Denne oppgaven fungerer som en ledetekst for en salgsmedarbeider om å levere ordren til kundens kjøretøy. Derfor behøver ikke kunden å gå inn i butikken.

Arbeidsflyten for kundens innsjekking kan også konfigureres til å samle inn tilleggsinformasjon fra kundene, for eksempel parkeringsplassnummeret til kunden, merke, modell og farge på kjøretøyet og leveringsinstruksjoner. Deltakeren i detaljhandelen kan bruke denne informasjonen til å legge til rette for innfrielse av ordren.

## <a name="enable-customer-check-in"></a>Aktivere kundeinnsjekking

Når innsjekkingsfunksjonen for kunde er aktivert, genererer Commerce en ordrebekreftelses-ID (kalles også kanalreferanse-ID). Det genererer også ordrebekreftelses-IDer for ordrer som opprettes via salgsstedet eller telefonsenterkanalene. 

Følg disse trinnene for å slå på kundeinnsjekkingsfunksjonen i Commerce Headquarters.

1. Gå til **Arbeidsområder \> Funksjonsbehandling**.
2. Søk etter funksjonen **Generere et konsekvent kanalreferanse-ID-format på tvers av kanaler**. 
3. Velg funksjonen, og velg deretter **Aktiver nå** i egenskapsruten. 

## <a name="create-a-check-in-confirmation-page"></a>Opprette en innsjekkingsbekreftelsesside

På e-handelområdet må du opprette en ny side som skal fungere som opplevelse for innsjekkingbekreftelse. Via tilleggskonfigurasjon kan siden også inkludere et skjema som samler inn tilleggsinformasjon fra kunder for å legge til rette for innfrielse av ordrene. Hvis du vil ha mer informasjon om hvordan du setter opp siden og modulen, kan du se [Kundeinnsjekkingsmodul](check-in-pickup-module.md).

## <a name="configure-the-transactional-email-template"></a>Konfigurere den transaksjonsbaserte e-postmalen

Du må legge til en **Jeg er her**-kobling eller -knapp i malen for den transaksjonsbaserte e-posten som kunder mottar når ordren er klar til plukking. Kunder vil bruke denne koblingen eller knappen til å varsle butikken om at de er ankommet for å hente ordren. 

Legg til koblingen eller knappen i malen som er tilordnet varslingstypen **Pakking fullført** og leveringsmåten du bruker til innfrielse av bestillinger utenfor butikk. I malen oppretter du en HTML-kobling eller -knapp som peker til URL-adressen til innsjekkingsbekreftelsessiden du opprettet. Her er et eksempel:

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
Hvis du vil ha mer informasjon om hvordan du konfigurerer e-postmaler, kan du se [Tilpasse transaksjons-e-postmeldinger etter leveringsmåte](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>En innsjekkingsbekreftelsesoppgave opprettes på salgsstedet

Når en kunde har varslet butikken om at de er til stede for plukking, mottar de et varsel om innsjekkingsbekreftelse, og det opprettes en oppgave i oppgavelisten på salgsstedet for butikken der kunden plukker opp ordren. Oppgaven inneholder all kunde- og ordreinformasjon som kreves for å oppfylle ordren. I oppgaven viser instruksjonersfeltet all informasjon som ble samlet inn fra kunden via tilleggsinformasjonsskjemaet. 

## <a name="additional-resources"></a>Tilleggsressurser

[Innsjekking for plukkmodul](check-in-pickup-module.md)
