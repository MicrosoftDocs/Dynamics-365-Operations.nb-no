---
title: Begrense bruk av betalingstoken
description: Denne artikkelen beskriver funksjonen som begrenser hvordan betalingstokener brukes i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 8092ab0724f33f21759aa84d25e0bdcb5b2ad5dd
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709659"
---
# <a name="limit-payment-token-usage"></a>Begrense bruk av betalingstoken

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Denne artikkelen beskriver funksjonen som begrenser hvordan betalingstokener brukes i Microsoft Dynamics 365 Commerce. Tokenbruk er begrenset til området for en salgsordre, eller, hvis det gis kundesamsvar, lagres som et kort i fil.

## <a name="key-terms"></a>Viktige termer

| Semester | Beskrivelse |
|---|---|
| Token | En referert XML-blob i Dynamics 365-systemet som lagrer betalingsreferanser for transaksjonsformål. |
| Kort i fil | Lagret kortreferansetoken som er avtalt for fremtidig bruk i Dynamics 365-systemet eller betalingsportalen, og som er spesifikk for kundens konto. |

Grensene på betalingstokenbruk gjelder for miljøer som bruker en betalingsgatewaytjeneste der det brukes regelmessige tokener. Den standard [Dynamics 365 Payment Connector for Adyen](adyen-connector.md) bruker gjentakende betalingstokener til å utføre etterfølgende ordrehandlinger, for eksempel autorisasjonsjusteringer og reautoriseringer.

For å få hjelp til å styre hvordan disse regelmessige betalingstokenene brukes i hele systemet, begrenser funksjonen **Begrens betalingstokenbruk til ordrekontekst** bruken av et gjentakende token til området for en salgsordre i systemet. Når den er aktivert, endrer funksjonen Commerce headquarters-brukergrensesnittet ved å oppdatere betalingsinndatasider og begrense muligheten til å velge tidligere kundebetalingsreferanser som skal brukes i nye transaksjonsforekomster.

Denne funksjonen er med på å oppfylle bruksreglene for enkelte betalingsutstedere som for eksempel Visa. I sine [Visa-kjerneregler og Visa produkt- og serviceregler](https://usa.visa.com/content/dam/VCOM/download/about-visa/visa-rules-public.pdf) spesifiserer Visa at bruk av betalingstokener bør begrenses til omfanget av en transaksjon, hvis kortinnehaveren ikke godtar noe annet.

Funksjonen **Begrens bruk av betalingstoken til ordrekontekst** er bare relevant hvis du bruker en betalingsgatewaytjeneste som bruker regelmessige betalingstokenreferanser.

## <a name="enable-the-feature"></a>Aktivere funksjonen

Hvis du vil aktivere funksjonen **Begrens betalingstokenbruk til ordrekontekst** i Commerce headquarters for miljøet, kan du gå til **Arbeidsområder \> Funksjonsbehandling**, finne og velge **Begrens bruk av betalingstoken til ordrekontekst** i listen og deretter velge **Aktiver nå**.

## <a name="limit-payment-token-usage"></a>Begrense bruk av betalingstoken

Når funksjonen er aktivert, oppdateres henting av Commerce headquarters-sidene som brukes til betalingsmåte, hvordan de refererer til betalingsmetoder for kunder som er arkivert for kunden. Denne oppdateringen vil primært påvirke to operasjonsområder:

- Hvordan et kundekort i fil angis på vegne av en kunde
- Hvordan betalingsinformasjon mot en kunde lagres for fremtidige betalingsoppføringer for salgsordrer

Når en kunde foretar en transaksjon mot Commerce-kanaler, lagres betalingsdetaljer med en salgsordrekontekst. Salgsordrekonteksten begrenser betalingstokenet slik at det ikke brukes som en betalingsreferanse mot kundeposten på kundesidene for nye eller redigerte salgsordrebetalinger i Commerce headquarters.

### <a name="payment-form-changes"></a>Endringer i betalingsskjema

Når en samtalesenter- eller Commerce headquarters-bruker tar betaling for en kunde mot en salgsordre, viser betalingssiden detaljer om valg av betalingsmåte. Når funksjonen **Begrens bruk av betalingstoken til ordrekontekst** er aktivert, og hvis en bruker velger plusstegnet (**+**) på betalingssiden, vises bare kort i fil-poster. Endringer krever at samtalesenteret eller Commerce Headquarters-brukeren angir alle betalingsdetaljene som kunden oppgav da de fylte ut siden **Angi kundebetalingsinformasjon** for den nye salgsordretransaksjonen.

Listen over verdier for **Nummer**-feltet inneholder bare kortreferanser som er knyttet til kunden som har kortet i filen. Den filtrerer ut tidligere betalingsreferanser som ikke omfattes av en salgsordre.

Plusstegnet (**+**) under **Nummer**-feltet er tilgjengelig, og kan brukes til å angi betalingsinformasjonen som kunden har angitt for transaksjonen som er knyttet til salgsordren som behandles.

### <a name="how-cards-on-file-work"></a>Hvordan kort i fil fungerer

Når funksjonen **Begrens bruk av betalingstoken til ordrekontekst** er aktivert, er et kort i fil et gjentakende betalingstoken som lagres mot en kundepost, og er ikke begrenset til området til en salgsordre. Et kort i filen muliggjør en hurtigreferanse for Commerce headquarters-brukere når de fyller ut betalingssiden for en ny salgsordrebetaling. Denne tokenreferansen gjelder bare for Dynamics 365-miljøet. For nettbaserte kanaler som bruker en betalingsgatewaytjeneste som gjør det mulig for brukere å lagre en betalingsmåte for fremtidig bruk i betalingsmodulen iFrame, lagrer betalingsgatewayen disse referansene trygt som en separat referanse til Dynamics 365-kortet i filen.

Hvis Dynamics 365 Commerce Payment Connector for Adyen for eksempel brukes på en online-kanal, vil kunder som legger inn kredittkortinformasjonen i betalingsmodulen iFrame, bare se gatewaytjenestens lagrede kortreferanser for det neste online-innkjøpet når de godkjennes. De ser ikke Dynamics 365-miljøets lagrede kort i fil som et alternativ i betalingsmodulen iFrame. På samme måte, når shoppere legger inn en ordre via telefonsenteret, presenteres ikke det elektroniske lagrede kortet til butikken som alternativer til samtalesenterbrukeren. Samtalesenterbrukeren ser bare tidligere kort i fil-referanser fra Dynamics 365-systemet (som avtalt av kunden) for å lagre for fremtidige ordrer.

Commerce headquarters-brukere kan lagre et kort i filen for en kunde ved å gå til **Detaljhandel og handel \> Kunder** og velge kundekontoposten. I **Kunde \> Oppsett**-delen kan brukere som har tillatelse til å behandle betalingssidene, bruke oppføringssiden **Kredittkort** til å angi et betalingskort som skal lagres i filen for fremtidige transaksjoner. Denne operasjonen sparer tid når fremtidige salgsordrebetalinger behandles for kunden. Brukerne i Samtalesenter og Commerce headquarters bør bare angi kortet i fil-kortdetaljer hvis kunden samtykker i å bruke kortreferansen for fremtidige transaksjoner.

Med en avmerkingsboks for **Lagre for fremtidig bruk** nederst på betalingssider for Commerce headquarters kan brukere lagre kortet i filen for fremtidig bruk. Denne boksen skal bare brukes hvis kunden samtykker i å bruke kortet i filen for fremtidige transaksjoner. Du kan vise eller begrense avmerkingsboksen **Lagre for fremtidig bruk** ved å bruke alternativet **Tillat kundekort i fil** i kategorien **Betaling** på siden **Samtalesenterparametere** i Commerce headquarters. Hvis du setter dette alternativet til **Ja**, kan Commerce headquarters-brukere som har tillatelse til å behandle betalingssider, lagre et kort i filen ved å merke av for **Lagre for fremtidig bruk**. Når alternativet er satt til **Nei**, er ikke avmerkingsboksen tilgjengelig for Commerce headquarters-brukere som har tillatelse til å behandle betalingssider. Alternativet **Tillat kundekort i fil** kan brukes hvis firmaet ønsker å begrense bruken av regelmessige tokener i Commerce headquarters, men ikke ønsker å tillate at et kort i filen kan lagres uten en fremgangsmåte for å sikre at kundens tillatelse er gitt.

### <a name="commerce-headquarters-pages-where-the-recurring-token-restrictions-are-enforced"></a>Commerce headquarters-sider der de regelmessige tokenrestriksjonene fremtvinges

Tokenbegrensningsområde påvirker følgende områder i Commerce headquarters når funksjonen er aktivert:

- Kundebetalingsinformasjon for **Salgsordre \> Betalinger \> Angi kundebetaling**
- Kontinuitetsordrer
- Avdragsbetalinger
- Kredittkortbetalinger for kunder

### <a name="manage-payment-tokens-archiving-or-removal"></a>Administrere betalingstokener (arkivering eller fjerning)

Betalingstokener som ble opprettet før funksjonsflagget for **Begrens bruk av betalingstoken til ordrekontekst** ble aktivert (eller mens funksjonen ble deaktivert) forblir "uten område" i systemet, og det kan refereres til valglister på betalingssiden for Commerce headquarters. Disse tokenene kan fjernes regelmessig på to måter i Commerce headquarters:

- Bruk siden **Arkiver transaksjonsdata for kredittkort** til å sette opp en jobb som regelmessig fjerner eller arkiverer betalingstokenene. Hvis du setter alternativet **Slett data uten arkivering** til **Ja**, slettes tokenene som oppfyller innstillingen **Minste transaksjonsalder (i dager)**. Hvis du vil ha mer informasjon, kan du se [Arkiver transaksjonsdata for kredittkort](archive-cc-data.md).
- Bruk den nye siden **Slett kredittkorttokener** (**Kunder \> Forespørsler og rapporter \> Opprydding \> Slett kredittkorttokener**), som lar deg kjøre eller definere en satsvis jobb som sletter betalingstokener. Angi følgende parametere:

    - Verdien **Minste tokenalder i dager** må være 90 dager eller mer.
    - Innstillingene **Kjør i bakgrunnen** kan brukes til å definere **Regelmessighet** eller **Varsler**.
    - En satsvis gruppe kan tilordnes til å kjøre oppgaven for en bestemt gruppe.
    - Hvis **Privat**-alternativet er satt til **Ja**, kan bare brukeren som oppretter jobben, kjøre den.
    - Hvis du angir **Ja** for alternativet **Kritisk jobb**, sikrer du at systemet sporer jobbens status aktivt.

Slettede tokener kan ikke hentes. Angi feltet **Minste tokenalder i dager** til et område som passer den lengste transaksjonslevetiden for miljøet ditt (fra autorisasjon til å registrere eller refundere).

## <a name="additional-resources"></a>Tilleggsressurser

[Vanlige spørsmål om betalinger](payments-retail.md)

[Kassemodul](../add-checkout-module.md)

[Betalingsmodul](../payment-module.md)
