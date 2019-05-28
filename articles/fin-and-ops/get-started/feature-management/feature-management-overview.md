---
title: Oversikt over funksjonsbehandling
description: Dette emnet beskriver funksjonen Funksjonsbehandling og hvordan du kan bruke den.
author: mikefalkner
manager: AnnBe
ms.date: 04/18/2019
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
ms.openlocfilehash: e75e42926db22d4fccda86c755b12d9d121a9c0e
ms.sourcegitcommit: be447fc81bc874982bc0185fcb4d87d99bd742c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538703"
---
# <a name="feature-management-overview"></a>Oversikt over funksjonsbehandling

[!include[banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Funksjoner legges til og oppdateres i hver versjon av Microsoft Dynamics 365 for Finance and Operations. Funksjonsbehandling-opplevelsen gir et arbeidsområde der du kan vise en liste over funksjoner som er levert i hver versjon. Nye funksjoner er deaktivert som standard. Du kan bruke arbeidsområdet til å aktivere dem og vise dokumentasjonen for dem.

## <a name="the-feature-management-workspace"></a>Arbeidsområdet for funksjonsbehandling

Du kan åpne arbeidsområdet **Funksjonsbehandling** ved å velge den aktuelle flisen på instrumentbordet. Du vil se en side som viser en liste over funksjoner for alle versjoner som støttes av Funksjonsbehandling-opplevelsen. Over tid vil Microsoft forbedre Funksjonsbehandling-opplevelsen slik at den inneholder tilleggsfunksjoner som hjelper deg med å administrere funksjoner.

Funksjonslisten inneholder følgende informasjon:

- **Funksjonsnavn** – En beskrivelse av funksjonen som ble lagt til.
- **Statusen Aktivert** – Et symbol angir om en funksjon er aktivert (hake), ikke er aktivert (tom), er planlagt aktivert (klokke) eller er obligatorisk aktivert (lås). Innstillingen som vises her, brukes for alle juridiske enheter. Legg merke til at selv om en funksjon er aktivert, kontrolleres den fortsatt av sikkerhet. Funksjonen vil derfor bare være tilgjengelig for brukere som har tilgang til den, basert på sikkerhetsrollen deres. Den vil også bare være tilgjengelig for juridiske enheter som brukeren har tilgang til.
- **Aktiveringsdato** – Datoen da funksjonen ble aktivert eller vil bli aktivert hvis datoen er en fremtidig dato.
- **Funksjon lagt til** – Datoen da funksjonen ble lagt til i miljøet ditt. Denne datoen angis automatisk når du oppdaterer miljøet under de månedlige versjonssyklusene.
- **Modul** – Modulen som påvirkes av den nye funksjonen.

Når du velger en funksjon, vises mer informasjon i detaljruten til høyre for funksjonslisten. Øverst i ruten vil du se funksjonsnavnet, datoen da funksjonen ble lagt til, modulen som påvirkes av funksjonen, og en **Finn ut mer**-kobling. Velg denne koblingen for å vise dokumentasjonen for funksjonen. Hvis dokumentasjon ikke er tilgjengelig, vil du bli ført til en midlertidig side. Detaljruten inneholder også feltet **Kommentarer** der du kan legge til dine egne kommentarer om funksjonen.

Arbeidsområdet **Funksjonsbehandling** har også flere kategorier med en funksjonsliste. 
- **Ny** – Viser alle funksjoner som er lagt til siden den siste månedlige oppdateringen. Hvis du har hoppet over noen månedlige oppdateringer, vil den inneholde alle de nye funksjonene siden forrige gang du oppdaterte. De nyeste funksjonene vises øverst på listen. Totalt antall nye funksjoner vises også i en flis øverst på siden.
- **Ikke aktivert** – Viser alle funksjoner som ikke er aktivert. De nyeste funksjonene vises øverst på listen. Totalt antall nye funksjoner vises også i en flis øverst på siden.
- **Planlagt** – Viser alle funksjoner som er planlagt aktivert på en fremtidig dato. Funksjonene som har den tidligste planlagte datoen, vises øverst i listen. Totalt antall nye funksjoner vises også i en flis øverst på siden.
- **Alle** – Viser alle funksjoner. De nyeste funksjonene vises øverst på listen.


## <a name="enable-a-feature"></a>Aktivere en funksjon

Hvis en funksjon ikke er aktivert, vises en **Aktiver**-knapp i detaljruten. Du kan bruke denne knappen til å aktivere funksjonen.

1. Velg funksjonen du vil aktivere, og velg deretter **Aktiver** i detaljruten.
2. Det vises en glidebryter der du kan angi datoen som funksjonen skal aktiveres på. Som standard settes datoen til gjeldende dato.
3. Velg **Aktiver** for å aktivere funksjonen.

Noen funksjoner kan ikke deaktiveres etter at du har aktivert dem. Hvis funksjonen du prøver å aktivere, ikke kan deaktiveres, får du en advarsel. På dette stadiet kan du velge **Avbryt** for å avbryte operasjonen og la funksjonen være deaktivert. Hvis du imidlertid velger **Aktiver** og aktiverer funksjonen, kan du ikke deaktivere den senere.

Når funksjonen er aktivert, vises en melding under **Finn ut mer**-koblingen i detaljruten. Denne meldingen angir enten at funksjonen ble aktivert, eller når funksjonen vil bli aktivert i fremtiden. Hvis du bruker en fremtidig dato, vil funksjonen vises i **Planlagt**-listen. Denne meldingen vil vises hver gang du velger funksjonen i funksjonslisten. Funksjoner som planlegges i fremtiden, aktiveres ved midnatt av en satsvis prosess basert på tidssonen som angis av systemdatoen. 

## <a name="reschedule-a-feature"></a>Planlegge en funksjon på nytt

Hvis en funksjon har blitt aktivert i fremtiden, vises en **Planlegg på nytt**-knapp i detaljruten. Du kan bruke denne knappen til å endre **aktiveringsdatoen** til en annen dato.

1. Velg en planlagt funksjon som du vil planlegge på nytt, og velg deretter **Planlegg på nytt** i detaljruten.
2. Det vises en glidebryter der du kan angi datoen som funksjonen skal aktiveres på. 
3. Velg **Aktiver** for å planlegge funksjonen på nytt, eller **Deaktiver** for å avbryte planen.

## <a name="disable-a-feature"></a>Deaktivere en funksjon

Hvis en funksjon allerede er aktivert, vises en **Deaktiver**-knapp i detaljruten. Du kan bruke denne knappen til å deaktivere funksjonen. **Deaktiver**-knappen er ikke tilgjengelig hvis funksjonen ikke kan deaktiveres etter at den er aktivert.

- Velg funksjonen du vil deaktivere, og velg deretter **Deaktiver** i detaljruten.

- Funksjonen er deaktivert, og datoen fjernes.

Når funksjonen er deaktivert, vises en melding under **Finn ut mer**-koblingen i detaljruten. Denne meldingen angir at funksjonen ikke er aktivert ennå, og at den vil vises i **Ikke aktivert**-listen. Meldingen vil vises hver gang du velger funksjonen i funksjonslisten.

## <a name="features-that-must-be-enabled"></a>Funksjoner som må aktiveres

En kritisk funksjon kan bli levert som må aktiveres automatisk når du gjør en oppdatering. Den aktiveres automatisk på **aktiveringsdatoen**. Det vises en melding under **Finn ut mer**-koblingen i detaljruten. Denne meldingen vil angi at funksjonen ble aktivert eller aktiveres automatisk på **aktiveringsdatoen**. Den vil vises hver gang du velger funksjonen i funksjonslisten.

## <a name="assigning-roles"></a>Tilordne roller

Arbeidsområdet **Funksjonsbehandling** kan åpnes av systemansvarlige og av brukere som er tilordnet funksjonsleder- eller funksjonsvisningsrollen som ble opprettet for å støtte funksjonsbehandlingsopplevelsen. Brukere med funksjonslederrolle kan aktivere og deaktivere hvilken som helst funksjon. De kan også oppdatere kommentardelen for funksjonen. Brukere med funksjonsvisningsrolle kan bare vise **Funksjonsbehandling**-arbeidsområdet. De kan ikke aktivere eller deaktivere funksjoner.

Funksjonslederrollen og funksjonsvisningsrollen overstyrer ikke den eksisterende sikkerheten som en bruker har. Rollene kontrollerer bare tilgangen til aktivering av funksjoner. De gir ikke tilgang til selve funksjonene.

## <a name="using-feature-management-to-enable-isv-features-or-custom-features"></a>Bruke funksjonsbehandling til å aktivere ISV-funksjoner eller egendefinerte funksjoner

Funksjonsbehandlingsprosessen er for øyeblikket ikke tilgjengelig for ISV-funksjoner eller egendefinerte funksjoner. Vi legger til ekstra funksjonalitet for å forbedre funksjonsbehandling og, når disse forbedringene er fullstendige, vil vi åpne opp funksjonsbehandling for alle funksjoner og angi bestemte instruksjoner om hvordan du oppdaterer funksjonen for å bruke den.

## <a name="feature-management-and-flighting"></a>Funksjonsbehandling og testversjonering

Funksjonsbehandling gir deg mulighet til å kontrollere funksjoner som leveres i hver versjon. Testversjonering gir Microsoft Teams mulighet til å gi ut funksjoner til et begrenset antall kunder, slik at funksjonene kan testes og valideres uten at det påvirker alle kundene. Funksjonsbehandling styrer ikke testversjoneringen av funksjoner.
