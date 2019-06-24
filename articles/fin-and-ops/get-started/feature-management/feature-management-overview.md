---
title: Oversikt over funksjonsbehandling
description: Dette emnet beskriver funksjonen Funksjonsbehandling og hvordan du kan bruke den.
author: mikefalkner
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: b200156a623c67a562cc1a5952899e3a77517528
ms.sourcegitcommit: bbc9aa0d6b94a942e1f4d5b038601509dcc87937
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/05/2019
ms.locfileid: "1619150"
---
# <a name="feature-management-overview"></a>Oversikt over funksjonsbehandling

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Funksjoner legges til og oppdateres i hver versjon av Microsoft Dynamics 365 for Finance and Operations. Funksjonsbehandling-opplevelsen gir et arbeidsområde der du kan vise en liste over funksjoner som er levert i hver versjon. Nye funksjoner er deaktivert som standard. Du kan bruke arbeidsområdet til å aktivere dem og vise dokumentasjonen for dem.

## <a name="the-feature-management-workspace"></a>Arbeidsområdet for funksjonsbehandling

Du kan åpne arbeidsområdet **Funksjonsbehandling** ved å velge den aktuelle flisen på instrumentbordet. Du vil se en side som viser en liste over funksjoner for alle versjoner som støttes av Funksjonsbehandling-opplevelsen. Over tid vil Microsoft forbedre Funksjonsbehandling-opplevelsen slik at den inneholder tilleggsfunksjoner som hjelper deg med å administrere funksjoner.

Funksjonslisten inneholder følgende informasjon:

- **Funksjonsnavn** – En beskrivelse av funksjonen som ble lagt til.
- **Statusen Aktivert** – Et symbol angir om en funksjon er aktivert (hake), ikke er aktivert (tom), er planlagt aktivert (klokke) eller er obligatorisk aktivert (lås). Innstillingen som vises her, brukes for alle juridiske enheter. Legg merke til at selv om en funksjon er aktivert, kontrolleres den fortsatt av sikkerhet. Funksjonen vil derfor bare være tilgjengelig for brukere som har tilgang til den, basert på sikkerhetsrollen deres. Den vil også bare være tilgjengelig i juridiske enheter som brukeren har tilgang til.
- **Aktiveringsdato** – Datoen da funksjonen ble aktivert eller planlegges å aktiveres.
- **Funksjon lagt til** – Datoen da funksjonen ble lagt til i miljøet ditt. Denne datoen angis automatisk når du oppdaterer miljøet under de månedlige versjonssyklusene.
- **Modul** – Modulen som påvirkes av den nye funksjonen.

Når du velger en funksjon, vises mer informasjon i detaljruten til høyre for funksjonslisten. Øverst i ruten vil du se funksjonsnavnet, datoen da funksjonen ble lagt til, modulen som påvirkes av funksjonen, og en **Finn ut mer**-kobling. Velg denne koblingen for å vise dokumentasjonen for funksjonen. Hvis dokumentasjon ikke er tilgjengelig, vil du bli ført til en midlertidig side. Detaljruten inneholder også feltet **Kommentarer** der du kan legge til dine egne kommentarer om funksjonen.

Arbeidsområdet **Funksjonsbehandling** har også flere kategorier, som hver viser en liste med funksjoner.

- **Ny** – Denne kategorien viser alle funksjoner som er lagt til siden den siste månedlige oppdateringen. Hvis du har hoppet over månedlige oppdateringer, viser kategorien alle de nye funksjonene som er lagt til siden forrige gang du oppdaterte. De nyeste funksjonene vises øverst på listen. Totalt antall nye funksjoner vises også på en flis øverst på siden.
- **Ikke aktivert** – Denne kategorien viser alle funksjoner som ikke er aktivert. De nyeste funksjonene vises øverst på listen. Totalt antall nye funksjoner som ikke er aktivert, vises også på en flis øverst på siden.
- **Planlagt** – Denne kategorien viser alle funksjoner som er planlagt aktivert i fremtiden. Funksjonene som har den tidligste planlagte datoen, vises øverst i listen. Totalt antall nye planlagte funksjoner vises også på en flis øverst på siden.
- **Alle** – Denne kategorien viser alle funksjoner. De nyeste funksjonene vises øverst på listen.

## <a name="turn-on-a-feature"></a>Aktivere en funksjon

Hvis en funksjon ikke er aktivert, vises en **Aktiver nå**-knapp i detaljruten. Du kan bruke denne knappen til å aktivere funksjonen.

- Velg funksjonen du vil aktivere, og velg deretter **Aktiver nå** i detaljruten. Funksjonen er slått på.

Enkelte funksjoner kan ikke slås av etter at du har aktivert dem. Hvis funksjonen du prøver å aktivere, ikke kan slås av, får du en advarsel. På dette stadiet kan du velge **Avbryt** for å avbryte operasjonen og la funksjonen være deaktivert. Hvis du imidlertid velger **Aktiver** og aktiverer funksjonen, kan du ikke deaktivere den senere.

Når en funksjon er aktivert, vises en melding under **Finn ut mer**-koblingen i detaljruten. Denne meldingen angir enten at funksjonen ble aktivert eller den fremtidige datoen når funksjonen er planlagt å bli aktivert. Den vises hver gang du velger funksjonen i funksjonslisten.

Funksjoner som er planlagt å aktiveres i fremtiden, vises i kategorien **Planlagt**. En partiprosess slår den på ved midnatt på den angitte datoen basert på tidssonen som representeres av systemdatoen.

## <a name="reschedule-a-feature"></a>Planlegge en funksjon på nytt

Hvis en funksjon er planlagt å aktiveres i fremtiden, vises en **Planlegg**-knapp i detaljruten. Du kan bruke denne knappen til å endre verdien for **aktiveringsdatoen** til en annen dato.

1. Velg den planlagte funksjonen for å planlegge på nytt, og velg deretter **Planlegg** i detaljruten.
2. I **Aktiveringsdato**-feltet i dialogboksen som vises, angir du den nye datoen funksjonen skal aktiveres.
3. Velg **Aktiver** for å planlegge funksjonen på nytt, eller **Deaktiver** for å avbryte planen.

## <a name="turn-off-a-feature"></a>Deaktivere en funksjon

Hvis en funksjon allerede er aktivert, vises en **Deaktiver**-knapp i detaljruten. Du kan bruke denne knappen til å deaktivere funksjonen. Knappen **Deaktiver** er ikke tilgjengelig hvis funksjonen ikke kan deaktiveres etter at den er aktivert.

- Velg funksjonen for å deaktivere, og velg deretter **Deaktiver** i detaljruten. Funksjonen deaktiveres, og merket i feltet **Aktiveringsdato** fjernes.

Når en funksjon deaktiveres, vises en melding under **Finn ut mer**-koblingen i detaljruten. Denne meldingen angir at funksjonen ikke er aktivert ennå. Den vises hver gang du velger funksjonen i funksjonslisten. Funksjoner som ikke er aktivert, vises i fanen **Ikke aktivert**.

## <a name="features-that-must-be-turned-on"></a>Funksjoner som må aktiveres

Noen ganger forekommer en kritisk funksjon som må aktiveres automatisk når du gjør en oppdatering. Disse funksjonene aktiveres automatisk på datoen som er angitt i feltet **Aktiver dato**. For disse funksjonene vises en melding under **Finn ut mer**-koblingen i detaljruten. Denne meldingen angir enten at funksjonen ble aktivert eller den fremtidige datoen når funksjonen blir aktivert. Den vises hver gang du velger funksjonen i funksjonslisten.

## <a name="turn-on-all-features-automatically"></a>Aktivere alle funksjoner automatisk

Som standard deaktiveres alle funksjoner som legges til i miljøet, med mindre de er obligatoriske funksjoner. Hvis du vil aktivere alle nye funksjoner automatisk, kan du imidlertid bruke rullegardinlisten under arbeidsområdetittelen til å endre hva som skjer når nye funksjoner legges til.

- Velg **Alle nye funksjonene aktiveres som standard** for å slå på alle nye funksjoner automatisk når de legges til i ditt miljø.
- Velg **Alle nye funksjonene deaktiveres som standard** for å slå av alle nye funksjoner automatisk når de legges til i ditt miljø.

## <a name="assigning-roles"></a>Tilordne roller

Arbeidsområdet **Funksjonsbehandling** kan åpnes av systemansvarlige og også av brukere som er tilordnet funksjonsleder- eller funksjonsvisningsrollen. Disse to rollene ble opprettet for å støtte funksjonsbehandlingsopplevelsen. Brukere med funksjonslederrolle kan aktivere og deaktivere hvilken som helst funksjon. De kan også oppdatere **Kommentarer**-field for funksjonen. Brukere med funksjonsvisningsrolle kan bare vise **Funksjonsbehandling**-arbeidsområdet. De kan ikke aktivere eller deaktivere funksjoner.

Funksjonslederrollen og funksjonsvisningsrollen overstyrer ikke den eksisterende sikkerheten som en bruker har. De kontrollerer bare om brukeren kan aktivere og deaktivere funksjoner. De har ikke tilgang til selve funksjonene.

## <a name="features-that-use-configuration-keys"></a>Funksjoner som bruker konfigurasjonsnøkler

Hvis en funksjon bruker en konfigurasjonsnøkkel, men konfigurasjonsnøkkelen ikke er slått på, viser ikke arbeidsområdet **Funksjonsbehandling**-funksjonen i listen over tilgjengelige funksjoner. Når du har aktivert konfigurasjonsnøkkelen, må du oppdatere funksjonslisten ved hjelp av menyelementet **Se etter oppdatering**. Funksjonen vises deretter i funksjonslisten.

Hvis du deaktiverer konfigurasjonsnøkkelen, fjernes ikke funksjonen fra funksjonslisten.

## <a name="data-entities"></a>Dataenheter

En dataenhet som kalles **Funksjonsbehandling**, lar deg eksportere innstillingene for funksjonsbehandling fra ett miljø og deretter importere dem til et annet miljø. Denne enheten oppdaterer bare eksisterende funksjoner. Forretningslogikken i enheten bidrar også til å garantere at de samme reglene som brukes i arbeidsområdet **Funksjonsbehandling**, brukes når importen er fullført. Du kan for eksempel ikke overstyre en obligatorisk funksjonsinnstilling ved å fjerne datoen under importen.

Følgende eksempler beskriver hva som skjer når du bruker **Funksjonsbehandling** til å importere data.

- Hvis du endrer verdien i feltet **Aktivert** til **Ja**, aktiveres funksjonen, og feltet **Aktiveringsdato** settes til gjeldende dato.
- Hvis du endrer verdien i feltet **Aktivert** til **Nei** eller lar feltet **Aktiveringsdato** stå tomt, aktiveres funksjonen, og merket i feltet **Aktiveringsdato** fjernes. Du kan ikke deaktivere en obligatorisk funksjon eller en funksjon som ikke kan deaktiveres når den er slått på.
- Hvis du endrer verdien i feltet **Aktiveringsdato** til en fremtidig dato, planlegges funksjonen for denne datoen.
- Hvis du endrer verdien i feltet **Aktivert** til **Ja** og endrer verdien i feltet **Aktiveringsdato** til en fremtidig dato, planlegges funksjonen til denne datoen. 
- Hvis du endrer verdien i feltet **Aktivert** til **Nei**, men du også endrer verdien i feltet **Aktiveringsdato** til en fremtidig dato, planlegges funksjonen til denne datoen.
- Hvis en funksjon aktiveres og du legger til et **Aktiveringsdato**-felt som er satt til en fremtidig dato, forblir funksjonen aktivert. Hvis du vil planlegge funksjonen på nytt, må du endre feltet **Aktivert** til **Nei**.

## <a name="feature-management-and-flighting"></a>Funksjonsbehandling og testversjonering

Funksjonsbehandling lar deg styre funksjonene som leveres i hver versjon. Testversjonering gir Microsoft Teams mulighet til å gi ut funksjoner til et begrenset antall kunder, slik at funksjonene kan testes og valideres uten at det påvirker alle kundene. Funksjonsbehandling styrer ikke testversjoneringen av funksjoner.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Bruke Funksjonsbehandling til å aktivere ISV-funksjoner eller egendefinerte funksjoner

Funksjonsbehandling er for øyeblikket ikke tilgjengelig for funksjoner fra uavhengige programvareleverandører og egendefinerte funksjoner. Microsoft legger imidlertid til flere funksjoner for å forbedre Funksjonsbehandling. Etter at disse forbedringene er fullført, vil Microsoft gjøre Funksjonsbehandling tilgjengelig for alle funksjoner og gi instruksjoner for hvordan du kan oppdatere funksjonene for å bruke den.
