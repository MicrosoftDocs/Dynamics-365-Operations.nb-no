---
title: Aktivere innsjekkingsmeldinger for kunde på salgsstedet
description: Denne artikkelen beskriver hvordan du aktiverer innsjekkingsmeldinger for kunde på Microsoft Dynamics 365 Commerce-salgsstedet.
author: bicyclingfool
ms.date: 12/03/2021
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
ms.openlocfilehash: ae53657c95128eae793f670bd9dbc31d9fac0fe4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885151"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Aktivere innsjekkingsmeldinger for kunde på salgsstedet

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du aktiverer innsjekkingsmeldinger for kunde på Microsoft Dynamics 365 Commerce-salgsstedet.

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

Legg til koblingen eller knappen i malen som er tilordnet varslingstypen **Pakking fullført** og leveringsmåten du bruker til innfrielse av bestillinger utenfor butikk. I malen oppretter du en HTML-kobling eller -knapp som peker til URLen for innsjekkingsbekreftelsessiden du har opprettet, og som inkluderer parameternavnene og -verdiene, som vist i følgende eksempel.

`<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%confirmationid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>`

Hvis du vil ha mer informasjon om hvordan du konfigurerer e-postmaler, kan du se [Tilpasse transaksjons-e-postmeldinger etter leveringsmåte](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>En innsjekkingsbekreftelsesoppgave opprettes på salgsstedet

Når en kunde har varslet butikken om at de er til stede for plukking, viser innsjekkingssiden en bekreftelsesmelding og en valgfri QR-kode som inneholder kundens bestillingsbekreftelses-ID. Samtidig opprettes det en oppgave i oppgavelisten på salgsstedet for butikken der kunden plukker opp ordren. Oppgaven inneholder all kunde- og ordreinformasjon som kreves for å oppfylle ordren. Instruksjonsfeltet for oppgaven viser all informasjon som ble samlet inn fra kunden via tilleggsinformasjonsskjemaet.

## <a name="end-to-end-testing"></a>Ende-til-ende-testing

Kundens innsjekking krever at bestemte parametere og verdier sendes til innsjekkingssiden og deretter til kundens innsjekkings-API. Derfor er den enkleste tilnærmingen å teste funksjonen i et miljø der en testordre kan opprettes og pakkes. På den måten kan det genereres en Ordre klar for plukking-e-post, som har en URL-adresse som inneholder de nødvendige parameternavnene og -verdiene.

Følg denne fremgangsmåten for å teste kundens innsjekkingsfunksjon.

1. Opprett kundens innsjekkingsside, og legg deretter til og konfigurer kundens innsjekkingsmodul. Hvis du vil ha mer informasjon, kan du se [Innsjekking for plukkmodul](check-in-pickup-module.md). 
1. Sjekk inn siden, men ikke publiser den.
1. Legg til koblingen nedenfor i en e-postmal som startes med pakking fullført-varslingstypen for leveringsmåten henting. Hvis du vil ha mer informasjon, kan du se [Opprette e-postmaler for transaksjonshendelser](email-templates-transactions.md).

    - **For UAT-miljøer (før produksjon):** Legg til kodesnutten fra delen [Konfigurere den transaksjonsbaserte e-postmalen](#configure-the-transactional-email-template) tidligere i denne artikkelen.
    - **For produksjonsmiljøer:** Legg til følgende kommenterte kode, slik at eksisterende kunder ikke berøres.

        `<!-- https://[DOMAIN]/[CHECK_IN_PAGE]?channelReferenceId=%confirmationid%&channelId=%pickupchannelid%&packingSlipId=%packingslipid%&preview=inprogress -->`

1. Opprett en ordre der hentemåten er angitt.
1. Når du mottar e-postmeldingen som blir utløst av varslingstypen for pakking fullført, kan du teste innsjekkingsflyten ved å åpne innsjekkingssiden med URL-adressen du la til tidligere. Fordi URL-adressen inneholder flagget `&preview=inprogress`, blir du bedt om å godkjenne før du kan vise siden.
1. Angi eventuell tilleggsinformasjon som kreves for å konfigurere modulen.
1. Kontroller at bekreftelsesvisningen for innsjekkingen vises riktig.
1. Åpne salgsstedsterminalen for butikken der ordren blir hentet.
1. Velg flisen **Bestillinger som skal plukkes opp**, og kontroller at ordren vises.
1. Kontroller at eventuell tilleggsinformasjon som ble konfigurert i innsjekkingsmodulen, vises i detaljer-ruten.

Når du har kontrollert at funksjonen for innsjekk av kunde fungerer fra ende til ende, følger du denne fremgangsmåten.

1. Publiser innsjekkingssiden.
1. Hvis du tester i et produksjonsmiljø, må du fjerne kommentar for URL-adressen i e-postmalen "ordre klar til plukk", slik at **Jeg er her**-koblingen eller -knappen vises. Last deretter opp malen på nytt.

## <a name="additional-resources"></a>Tilleggsressurser

[Innsjekking for plukkmodul](check-in-pickup-module.md)

[Tilpasse transaksjons-e-poster etter leveringsmåte](customize-email-delivery-mode.md)

[Opprette e-postmaler for transaksjonshendelser](email-templates-transactions.md)
