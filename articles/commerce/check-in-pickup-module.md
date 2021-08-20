---
title: Innsjekking for plukkmodul
description: Dette emnet beskriver innsjekking for plukkmodul og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f6359f41f3b97325db4fda083dc32d39839811297a96a1f2d99a93990c00afae
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747471"
---
# <a name="check-in-for-pickup-module"></a>Innsjekking for plukkmodul

[!include [banner](includes/banner.md)]

Dette emnet beskriver innsjekking for plukkmodul og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.

Innsjekkingen for plukkmodulen gir en bekreftelsesside for kunder som bruker Dynamics 365 Commerce-muligheten til å sjekke inn kunder for å varsle en butikk om ankomsten. Ved hjelp av innsjekkingen for plukkmodulen kan du også konfigurere et skjema som samler inn tilleggsinformasjon fra kunder for å legge til rette for ordrelevering. Denne informasjonen omfatter kundens parkeringsplassnummer og merke og modell for kjøretøyet. 

## <a name="module-properties"></a>Modulegenskaper

| Egenskapsnavn | Verdier | beskrivelse |
|---------------|--------|-------------|
| Bekreftelsestekst | Tekststreng | Innhold for overskriften som vises på bekreftelsessiden for innsjekking. |
| Vise QR-kode | **Sann** eller **Usann** | Når denne egenskapen er satt til **Sann**, viser innsjekkingsbekreftelsessiden en QR-kode som representerer ordrebekreftelses-IDen. |
| Ekstra informasjonsoverskrift | Tekststreng | Innhold for overskriften som vises når ekstra informasjonsfelt er konfigurert. |
| Ekstra informasjonsnøkler | Ressurs-ID/ressursverdipar | Hver nøkkel oppretter et skjemafelt og en tilknyttet etikett som brukes til å samle inn tilleggsinformasjon fra kunder. |
| Ekstra informasjonsnøkler \> Ressurs-ID | Tekststreng | Hver informasjonsnøkkel oppretter et skjemafelt og en tilknyttet etikett som brukes til å samle inn tilleggsinformasjon fra kunder. Denne egenskapen identifiserer den ekstra informasjonsnøkkelen. I oppgaven som opprettes på salgsstedet (POS), vises verdien for denne egenskapen som etiketten i instruksjonene i feltet. |
| Ekstra informasjonsnøkler \> Ressursverdi | Tekststreng | Etiketten for tekstfeltet i oppgaven på salgsstedet. |
| Ekstra informasjonsnøkler \> Påkrevd | **Sann** eller **Usann** | Denne egenskapen angir om kunder må fylle ut skjemafeltet før de kan fortsette. Når denne egenskapen er satt til **Sann**, lages det en stjerne ved siden av skjemaetiketten, og det utføres en nullkontroll for å hindre at kundene fortsetter hvis ingen verdi angis. |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a>Legge til innsjekkingen for plukkmodulen på en side

Innsjekkingen for plukkmodulen skal legges til på den nye siden du oppretter for innsjekkingsbekreftelse. Denne siden fungerer som innsjekkingsbekreftelseserfaring for kunder som velger **Jeg er her**-kobling eller -knapp i e-posten. 

## <a name="configure-the-additional-information-form"></a>Konfigurere ekstra informasjonsskjema

Hvis ingen tilleggsinformasjonsnøkler er konfigurert, viser modulen som standard kundenes innsjekkingsbekreftelsesside. Når innsjekkingsbekreftelsen vises, opprettes det en oppgave på salgsstedet for butikken der ordren plukkes opp.

Når én eller flere informasjonsnøkler er konfigurert, blir kunder først bedt om å angi informasjon. Når de velger **Send** ser de innsjekkingsbekreftelsen, og en oppgave blir opprettet på salgsstedet. 

## <a name="additional-resources"></a>Tilleggsressurser

[Aktivere innsjekkingsmeldinger for kunde på salgsstedet](enable-customer-check-in.md)
