---
title: Administrere rekrutteringsprosesser
description: Dette emnet beskriver et konsept som rekrutteringspersoner kan bruke til å spore trinnene i en rekrutteringsprosess.
author: andreabichsel
ms.date: 01/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: anbichse
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9a5e89e700858ed9e625fbdee630fa14ebea26e
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/12/2022
ms.locfileid: "7965070"
---
# <a name="manage-recruiting-processes"></a>Administrere rekrutteringsprosesser

[!include [banner](../includes/banner.md)]

Dette emnet beskriver et konsept som rekrutteringspersoner kan bruke til å spore trinnene i en Rekruttering prosess, inkludert aktiviteter for å annonsere ledige stillinger og rekruttere søkere, spore søker- og søknadsinformasjon, intervjue søkere og velge én eller flere kandidater for å besette de ledige stillingene i organisasjonen.

## <a name="overview"></a>Oversikt

Rekrutteringsprosjekter kan hjelpe deg med å organisere trinnene skal du fullføre når du fyller ledige stillinger i en juridisk enhet. En søker er en person som søker på ansettelse for bedriften. En søknad er en søkers uttrykk for interesse for å bli ansatt hos et firma, og kan være knyttet til et rekrutteringsprosjekt til uttrykkt interesse for en bestemt åpning. En enkelt søker kan ha flere søknader i samme juridiske enhet eller på tvers av flere firmaer i organisasjonen.

## <a name="recruitment-projects"></a>Rekrutteringsprosjekter

Med rekrutteringsprosjekter kan bemanningskonsulenter følge opp fremdriften mot å fylle én eller flere åpne stillinger. Rekrutteringsprosjektet identifiserer avdelingen og jobben der én eller flere stillinger er åpne. Rekrutteringsprosjekter sporer også følgende informasjon om ledige stillinger:

- Det spesifikke antallet ledige stillinger
- Ansettelsesansvarlig og en alternativ kontakt for stillingen
- Datoen da rekvisisjonen ble godkjent
- Søknadsfristen
- Den beregnede startdatoen

Rekrutteringsprosjektet inneholder verdien for **Stillingsannonse** som brukes på siden **Ansattselvbetjening** for å annonsere den ledige stillingen. Den ledige stillingen kan bare vises til ansatte hvis rekrutteringsprosjektet har en verdi for **Stillingsannonse**, hvis feltet **Vis på ansattselvbetjening** er satt til **Ja**, feltet **Søknadsfrist** er satt til en fremtidig dato, og rekrutteringsprosjektet har **Prosjektstatus**-verdien **Startet**. Tabellen nedenfor viser de mulige rekrutteringsprosjektstatusene og tilhørende beskrivelser.

| Status    | Viser at ...                                                                         |
|-----------|-----------------------------------------------------------------------------------------|
| Planlagt | Rekrutteringsinnsats klargjøres. Rekruttering er ennå ikke startet for dette prosjektet. |
| Startet   | Søknader godtas nå for ledige stillinger i dette prosjektet.                   |
| Avsluttet  | Alle ledige stillinger for dette prosjektet er besatt.                                         |
| Avbrutt  | Rekruttering er avbrutt for dette prosjektet.                                          |

Rekrutteringspersoner kan også registrere **mediene** som brukes til å annonsere den ledige stillingen via eksterne enheter, samt spore **utviklinger** mot prosjektet eller søknadene.

## <a name="applicants"></a>Søkere

En søker er en person som søker på en jobb i bedriften. Søkere deles mellom alle juridiske enheter i organisasjonen. Derfor har du en stor gruppe med talenter å søke i. Du kan opprettholde kompetanse, referanser, overnattingsforespørsler og personlige opplysninger for søkere. Når du oppretter en søkerpost, opprettes en personpost for den søkeren i den globale adresseboken. Du kan bruke siden **Søker** siden for å oppdatere følgende globale adressebokinformasjon for personer som er søkere:

- Adresseinformasjon
- Kontaktinformasjon
- Identifikasjonsinformasjon
- Navnedetaljer
- Personlig informasjon

## <a name="applications"></a>Søknader

Du kan registrere informasjon fra jobbsøknader du mottar på siden **Søknad**. Søknaden er søkerens uttrykk for interesse for en stilling i organisasjonen. Hvis du vil opprette en søknad, må søkeren allerede finnes som en søker eller en person i systemet.

Jobbsøknader som sendes av søkere på weben, er enten anmodede søknader som ble sendt som svar på en stillingsannonse, eller uanmodede søknader. Anmodede søknader blir automatisk tilknyttet rekrutteringsprosjektet som stillingsannonsen ble opprettet fra. Uanmodede søknader knyttes til rekrutteringsprosjektet som er angitt i **Rekruttering**-området på siden **Personalparametere**.

### <a name="application-status"></a>Søknadsstatus

Søknadsstatus angir hvor en søknad er i rekrutteringsprosessen. Tabellen nedenfor viser de mulige søknadsstatusene og tilhørende beskrivelser.

| Status    | Viser at ...                                                                           |
|-----------|-------------------------------------------------------------------------------------------|
| Mottatt  | Søknaden er mottatt.                                                             |
| Bekreftet | Det kan sendes beskjed til søkeren om at søknaden er mottatt.            |
| Intervju | Det kan sendes en innkalling til intervju til søkeren.                                     |
| Avslag | Det kan sendes et avslagsbrev til søkeren.                                          |
| Avbrutt  | Det kan sendes en bekreftelse på at søknaden er trukket tilbake, til søkeren. Denne statusen tilordnes manuelt. |
| Ansatt  | Det kan sendes et tilbud om ansettelse til søkeren.                                         |

### <a name="correspondence-actions"></a>Korrespondansehandlinger

En søknads korrespondansehandling bestemmer dokument- eller e-postmalen du bruker til å kommunisere med søkeren som sendte inn søknaden. Ved å knytte til **søknadsbokmerker** med korrespondansehandlinger kan du bruke verdier fra sidene **Søknad**, **Søker**, **Intervjuv** og **Rekrutteringsprosjekt** i kommunikasjonen med søkerne. Ved å opprette **e-postmaler for søknad** for korrespondansehandlinger kan du raskt sende e-postmeldinger til søkere som har en søknad med en spesifikk kombinasjon av en status- og korrespondansehandling. Du kan for eksempel sende en e-postmelding med bekreftelse for alle søknader med **Status**-verdien **Mottatt** og **Korrespondansehandling**-verdien **Mottatt**. Når du har sendt e-posten, har du muligheten til å automatisk oppdatere status for søknadene.

## <a name="application-routing"></a>Søknadsruting

Hvis en søknad må vurderes av flere arbeidere, kan du bruke siden **Søknadsruting** for å opprette en sirkuleringsliste for arbeidere for å administrere prosessen.

## <a name="interviews"></a>Intervjuer

**Søkerintervjuer** kan være planlagt fra **Søknader**-siden. Bruk knappen **Send møteinformasjon** til å sende en kalenderfil med informasjon om intervjutidsplanen til søkeren og intervjueren.

## <a name="skill-mapping"></a>Kompetansesøk

**Kompetansesøk** og **Profiler for kompetansesøk** kan brukes til å identifisere kandidater som kan egne seg for en ledig stilling.

## <a name="hiring-applicants"></a>Ansette søkere

Bruk siden **Søknader** for å ansette en søker. Når du ansetter en søker, vil søknadsposten ha statusen **Ansatt** og søkerens personoppføring for global adressebok knyttes til den nye arbeiderposten. Endringer i den globale adressebokinformasjon for den nye arbeiderposten vises også i søkerposten. Dette kan redusere dataregistrering hvis den nye arbeideren fortsatt søker på en annen jobb innenfor organisasjonen. For å ansette en eksisterende arbeider til en ny stilling velger du **Endre stilling** i rullegardinmenyen **Søknadsstatus** for å starte overføringsprosessen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
