---
title: Klargjøre for å aktivere med Human Resources
description: Denne siden gir råd om hvordan du klargjør for en aktivering e med Dynamics 365 Human Resources.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dcec7963bdf70f848249bb2ca5e2208e09f49548
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054794"
---
# <a name="prepare-for-human-resources-go-live"></a>Klargjøre for å aktivere med Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du klargjør for aktivering med et Dynamics 365 Human Resources-prosjekt ved hjelp av Microsoft Dynamics Lifecycle Services (LCS). 

Denne grafikken viser fasene i aktiveringsprosessen. 

![Aktiveringsprosessen](./media/hr-admin-go-live-prepare-process.png)

Følgende tabell viser alle trinnene i prosessen, forventet varighet og hvem som er ansvarlig for handlingen.

| Fase | Handling | Varighet/når | Hvem | Notater |
| --- | --- | --- | --- |--- |
| 1 | Oppdatere aktiveringsdato i LCS | Minst 2-3 måneder på forhånd | Partner/kunde | Milepældatoene bør holdes oppdatert fortløpende. |
| 2 | Fullfør og send sjekkliste | Etter at testing av brukergodkjenning er fullført | Partner/kunde | Følg instruksjonene som er oppgitt i [FastTrack-aktiveringsvurderingen](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment). |
| 3 | Prosjektvurdering (FastTrack) | FastTrack-arkitekt* | Arkitekten leverer vurdering etter at sjekklisten er mottatt, og fortsetter gjennomgangen til spørsmålene blir avklart og løsninger er på plass, hvis det er aktuelt. |
| 4 | Prosjekt-workshop (FastTrack) | FastTrack-arkitekt* | |
| 5 | Import av datapakke | Er avhengig av prosjektet | Partner/kunde | Følg instruksjonene i [Oversikt over databehandling](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).|
| 6 | Produksjonsklar | Når alle tidligere trinn er fullført | Partner/kunde | Partner/kunde kan ta kontroll over produksjonsmiljøet.|
| 7 | Overgangsaktiviteter | Er avhengig av prosjektet | Partner/kunde | |
| 8 | Aktivering | Er avhengig av prosjektet | Kunde | |

> [!IMPORTANT]
> *Trinn 3 og 4 fullføres bare for kunder som kvalifiserer for FastTrack.

## <a name="completing-the-lcs-methodology"></a>Fullføre LCS-metodikken

En stor milepæl i hvert implementeringsprosjekt er overgangen til produksjonsmiljøet. Prosessen med å fullføre et trinn har to deler: 

- Gjør det faktiske arbeidet, for eksempel en tilpassings-/gapanalyse eller testing av brukergodkjennelse. 
- Merk det tilsvarende trinnet i LCS-metodikken som fullført. 

Det er en god praksis å fullføre trinnene i metoden mens du går fremover med implementeringen. Ikke vent til det siste minuttet. Det er i kundens beste interesse å ha en solid implementering. 

## <a name="uat-for-your-solution"></a>UAT for løsningen

I løpet av UAT-fasen må du teste alle forretningsprosessene du har implementert, og eventuelle tilpasninger du har utført, i et sandkassemiljø i implementeringsprosjektet. Du bør vurdere følgende når du fullfører UAT-fasen for å sikre en vellykket aktiveringsfase: 

- Det anbefales at UAT-prosessen starter med et rent og nytt miljø der dataene fra GULL-konfigurasjonen kopieres til miljøet før starten av UAT-prosessen. Det anbefales at du bruker produksjonsmiljøet som GULL-miljø til du går i gang med å produsere på et bestemt tidspunkt.
- Prøvesaker dekker hele omfanget av krav. 
- Test ved å bruke overførte data. Dette bør inkludere data, for eksempel arbeidere, jobber og stillinger. Ta også med åpningssaldoer som permisjons- og fraværsavsetninger. Til slutt skal du ta med åpne transaksjoner, for eksempel registrering av gjeldende fordeler. Fullstendig testing med alle typer data, selv om datasettet ikke er sluttført. 
- Test ved å bruke de riktige sikkerhetsrollene (standardroller og egendefinerte roller) som er tilordnet til brukerne. 
- Kontroller at løsningen er i samsvar med alle bransjespesifikke forskriftsmessige krav. 
- Dokumenter alle funksjoner og hent godkjenning fra kunden. 

## <a name="mock-go-live"></a>Aktiveringstest

Før du aktiverer, må du utføre en testaktivering for å teste trinnene som er nødvendige for å gå fra dine eldre systemer til det nye systemet. Du bør utføre din testaktivering i et sandkassemiljø og inkludere alle trinnene i overgangsplanen din.

- Det anbefales at du bruker produksjonsmiljøet som GULL-konfigurasjonsmiljøet frem til aktiveringen.
- Sørg for at du har en god styringsprosess på plass for å beskytte produksjonsmiljøet mot utilsiktede transaksjoner eller oppdateringer, før aktiveringen.
- Når du er klar til å utføre UAT eller testaktivering, oppdaterer du sandkassemiljøet fra produksjonsmiljøet. Hvis du vil ha mer informasjon, kan du se [Kopiere en forekomst](hr-admin-setup-copy-instance.md).
- Test hvert trinn i overgangsplanen i sandkassemiljøet, og valider deretter sandkassemiljøet ved å utføre spotkontroller eller tester fra UAT-skriptene i miljøet.
  - Testene bør inneholde alle migreringene, inkludert transformasjoner som trengs til aktiveringen.
  - Prosessen bør inkludere en testovergang for alle eldre systemer.
  - Pass på at du tar med eventuelle trinn i integreringsovergangen eller eksterne systemtrinn testovergangen.
- Hvis det oppstår problemer under testovergangen, kan det være nødvendig med en ny testovergang. Det anbefales derfor at du planlegger to testoverganger i prosjektplanen.

## <a name="fasttrack-go-live-assessment"></a>FastTrack-aktiveringsvurdering

Kunder som er kvalifisert for FastTrack, og er engasjert med en FastTrack-løsningsarkitekt, vil fullføre en aktiveringsgjennomgangen med Microsoft FastTrack. Hvis du vil ha mer informasjon, kan du se [Microsoft FastTrack](/dynamics365/fasttrack/). 

Om lag åtte uker før aktivering, vil FastTrack-teamet be deg fylle ut en [sjekkliste for aktivering](https://go.microsoft.com/fwlink/?linkid=2146013).

Prosjektlederen eller et nøkkelprosjektmedlem må fullføre sjekklisten i fasen før aktivering av prosjektet. Sjekklisten fullføres vanligvis fire til seks uker før den foreslåtte aktiveringsdatoen når UAT er fullført eller nesten fullført. 

Når du har fullført sjekklisten for aktivering, sender du den via e-post til din FastTrack-løsningsarkitekt. Ta alltid med en nøkkelinteressent fra kunden og implementeringspartneren i e-postmeldingen. 

Når du har sendt inn sjekklisten, vil FastTrack-løsningsarkitekten se gjennom prosjektet og oppgi en vurdering som beskriver potensielle risikoer, gode fremgangsmåter og anbefalinger for en vellykket gjennomgang av prosjektet. I noen tilfeller kan løsningsarkitekten utheve risikofaktorer og be om en reduksjonsplan. 

## <a name="see-also"></a>Se også

[Vanlige spørsmål om aktivering](hr-admin-go-live-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
