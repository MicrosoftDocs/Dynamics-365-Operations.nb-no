---
title: Administrere forretningspartnerbrukere på B2B-e-handelssider
description: Dette emnet beskriver hvordan administratorer kan legge til, redigere og slette forretningspartnere på forretnings-til-bedrift-e-handelsområder (B2B).
author: josaw1
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 88f613be59a0c7b0d5efcdc0bef2c5a54506f9eb
ms.sourcegitcommit: 0c77dbb8547cd36fce3977ca9515fa1474efa77a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/22/2021
ms.locfileid: "6655612"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Administrere forretningspartnerbrukere på B2B-e-handelssider

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan administratorer kan legge til, redigere og slette forretningspartnere på forretnings-til-bedrift-e-handelsområder (B2B).

B2B-e-handelsområder krever at organisasjoner registrerer seg for å bli forretningspartnere. Når en organisasjon har sendt registreringsdetaljer til et webområde for B2B-e-handel, går den gjennom en kvalifikasjonsprosess. Hvis organisasjonen er kvalifisert, blir den pålastet som forretningspartner.

Når en organisasjon er pålastet som forretningspartner, identifiseres organisasjonsbrukeren som startet forespørselen om å bli forretningspartner, som administratorbrukeren, og får rettigheter til å pålaste ytterligere autoriserte brukere av B2B-webområdet for e-handel. Disse autoriserte brukerne kan deretter legge inn ordrer på vegne av forretningspartneren.

## <a name="turn-on-the-b2b-e-commerce-capabilities-feature-in-commerce-headquarters"></a>Slå på funksjonen for B2B-e-handel i Commerce Headquarters

Ved hjelp av funksjonen for B2B-e-handel i Commerce Headquarters kan organisasjoner laste på forretningspartnere og definere administratorbrukere. Denne funksjonen gjør det også mulig for administratorer å opprette og administrere brukere og grupper for forretningspartnere, og tilordne bestemte roller til dem. Til slutt gjør er det mulig for forretningspartnere å opprette ordremaler og bruke eksisterende ordrer til å bestille produkter på nytt.

Følg disse trinnene for å slå på funksjonen for B2B-e-handel i Commerce Headquarters.

1. Gå til **Arbeidsområder \> Funksjonsbehandling**.
1. Bruk begrepet **Detaljhandel og handel** i kategorien **Alle** i feltet **Modul**.
1. Finn og velg funksjonen med navnet **Aktiver bruk av B2B-funksjoner for e-handel**, og velg deretter **Aktiver nå**.

## <a name="create-a-number-sequence-and-add-it-to-commerce-shared-parameters"></a>Opprette en nummerserie og legge den til i Delte handelsparametere

Nummerserier brukes for å generere lesbare, unike ID-er for hoveddataposter og transaksjonsposter som krever ID-er. Hvis du vil ha mer informasjon om nummerserier, kan du se [Oversikt over nummerserier](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).

Følg denne fremgangsmåten for å opprette en nummerserie og legge den til i Delte handelsparametere i Commerce Headquarters.

1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Nummerserier \> Nummerserier**, og opprett en nummerserie.
1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Delte handelsparametere**, og legg til den nye nummerserien i referansen **Kundehierarki-ID**.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Konfigurere administratorbrukeren for en ny forretningspartner

Potensielle forretningspartnere kan starte pålastingsprosess til et B2B-webområde for e-handel ved å sende en forespørsel om pålasting via en kobling på området. Når en potensiell forretningspartnerbruker velger koblingen, kan de oppgi opplysningene for pålasting og registrering. Når forespørselen er sendt, vises en bekreftelsesside for innsending. Hvis innsendingen godkjennes, blir anmoderen (det vil si brukeren som startet forespørselen om pålasting) forretningspartneradministratorbrukeren.

Følg denne fremgangsmåten for å godkjenne og definere en forretningspartneradministratorbruker i Commerce Headquarters.

1. Gå til **IT for Detaljhandel og handel \> Distribusjonsplan**.
1. Kjør jobben **P-0001** for å trekke alle forretningspartnerpålastingsforespørsler til Commerce Headquarters.
1. Når **P-0001**-jobben er kjørt, kan du gå til **IT for Detaljhandel og handel \> Kunde** og kjøre jobben **Synkroniser kunder og forretningspartnere fra asynkron modus**. Når denne jobben er kjørt, opprettes pålastingsforespørsler som kundeemneposter i Commerce Headquarters. Feltet **Type-ID** i disse postene er satt til **B2B-kundeemne**.
1. Gå til **Kunder \> Alle kundeemner**, og åpne kundeemnesiden.
1. Velg kundeemneposten for den nye forretningspartneren for å åpne kundeemnedetaljer-siden.
1. I kategorien **Generelt** velger du **Konverter \> Godkjenn/Avvis** for å godkjenne eller avvise forespørselen om pålasting. Når det vises en bekreftelsesmelding, bekrefter du at du vil fortsette med prosessen og godkjenne forespørselen. En e-post sendes deretter til e-postadressen til anmoder for å bekrefte at organisasjonen er godkjent som forretningspartner.

    Når du har godkjent forespørselen, settes feltet **Status** for kundeemneposten til **Godkjent**. I tillegg opprettes det to nye kundeposter i systemet: en **Type Organisasjon**-kundepost for forretningspartnerorganisasjonen, og en kundepost av typen **Type Person** for anmoderen. Det opprettes også en kundehierarkipost for forretningspartneren. <!--(Please refer to the Org modeling of B2B customer section in this document for more information)-->

1. Gå til **IT Detaljhandel og handel \> Distribusjonsplan**, og kjør jobben **1010** (**Kunder**) for å sende de nylig opprettede kunde- og kundehierarkipostene til kanaldatabasen.

Når forespørselen er godkjent, og kunde- og kundehierarkipostene er synkronisert med kanaldatabasen, kan anmoderen logge seg på e-handelsstedet for B2B ved hjelp av e-postadressen som ble oppgitt da forespørselen ble sendt. Brukerne kan bruke registreringsflyten til å definere passordet for kontoen. Hvis du vil aktivere identitetsleverandør (Azure AD B2C)-posten som skal knyttes til B2B-kundeposten som ble opprettet ved registrering eller pålogging, følger du instruksjonene i [Aktiver automatisk kobling av identitetsposter til kundekontoer](../identity-record-linking.md).

## <a name="onboard-additional-business-partner-users"></a>Pålaste flere forretningspartnerbrukere

Forretningspartneradministratorbrukeren kan sende flere forretningspartnerbrukere til webområdet for B2B-e-handel etter behov.

Følg denne fremgangsmåten for å pålaste flere forretningspartnerbrukere på et webområde for B2B-e-handel.

1. Logg deg på webområdet for B2B-e-handel som administrator.
1. Gå til **Min konto \> Organisasjonsbrukere \> Vis detaljer**, og velg **Legg til en bruker**.
1. Angi den nødvendige informasjonen, og velg deretter **Lagre**. Statusen for den nye brukeren angis til **Venter**.

    Når jobbene **P-0001** og **Synkroniser kunder og forretningspartnere fra asynkron modus** kjøres, opprettes en **Type Person**-kundepost for den nye brukeren i Commerce Headquarters. Denne kundeposten er også knyttet til den relevante forretningspartnerens kundehierarkipost. I tillegg sendes det en e-post til den nye brukerens e-postadresse for å varsle dem om at de er lagt til som bruker av forretningspartnerorganisasjonen, og kan nå logge seg på B2B-webområdet for e-handel.

1. Kjør jobben **1010** (**Kunder**) for å synkronisere den nye forretningspartnerbrukeren til kanaldatabasen.

Når kundeposten er synkronisert, settes statusen til brukeren på webområdet for B2B-e-handel til **Aktiv**, og den nye brukeren kan logge seg på B2B-webområdet for e-handel ved hjelp av e-postadressen. Brukerne kan bruke registreringsflyten til å definere passordet for kontoen. Hvis du vil aktivere identitetsleverandør (Azure AD B2C)-posten som skal knyttes til B2B-kundeposten som ble opprettet ved registrering eller pålogging, følger du instruksjonene i [Aktiver automatisk kobling av identitetsposter til kundekontoer](../identity-record-linking.md).

## <a name="edit-business-partner-user-details"></a>Redigere brukerdetaljer for forretningspartner

Følg denne fremgangsmåten for å redigere detaljene til forretningspartnerbrukere.

1. Logg deg på webområdet for B2B-e-handel som administrator.
1. Gå til **Min konto \> Organisasjonsbrukere \> Vis detaljer**, velg **Rediger**-knappen (blyantsymbol), gjør de nødvendige endringene, og velg deretter **Lagre**. Endringene trer bare i kraft etter at jobbene **P-0001**, **Synkroniser kunder og forretningspartnere fra asynkron modus** og jobbene **1010** (**Kunder**) er kjørt.

## <a name="remove-a-business-partner-user"></a>Fjerne en forretningspartnerbruker

En administrator kan etter behov fjerne eksisterende brukere av en forretningspartnerorganisasjon fra listen over brukere som har tilgang til webområdet for B2-e-handel.

Følg denne fremgangsmåten for å fjerne en forretningspartnerbruker.

1. Logg deg på webområdet for B2B-e-handel som administrator.
1. Gå til **Min konto \> Organisasjonsbrukere \> Vis detaljer**, og velg **Fjern**-knappen ("X"-symbol). Når det vises en bekreftelsesmelding, bekrefter du at du vil fjerne brukeren. Endringene trer bare i kraft etter at jobbene **P-0001**, **Synkroniser kunder og forretningspartnere fra asynkron modus** og jobbene **1010** (**Kunder**) er kjørt.

> [!NOTE]
> Når du fjerner en bruker fra listen over brukere som har tilgang til webområdet for B2B-e-handel, fjernes den tilsvarende kundeposten fra forretningspartnerens kundehierarkipost. Kundeposten i seg selv slettes imidlertid ikke fra Commerce Headquarters.

## <a name="onboard-business-partner-and-users-in-commerce-headquarters"></a>Pålastet forretningspartner og brukere i Commerce Headquarters

Administratorer kan pålaste forretningspartnere og brukere direkte i Commerce Headquarters.

Følg disse trinnene for å pålaste forretningspartnere og brukere direkte i Commerce Headquarters.

1. Opprett en **Type Organisasjon**-kundepost for forretningspartnerorganisasjonen.
1. Opprett **Type Person**-kundeposter for forretningspartnerbrukere. Kontroller at det er angitt en primær e-postadresse for hver kunde.
1. For hver **Type Person**-kundepost som må angis som administratorbruker i forretningspartnerorganisasjonen, angir du alternativet **B2B-administrator** til **Ja** i hurtigkategorien **Detaljhandel**.
1. Opprett en ID for kundehierarki. Angi et navn i **Navn**-feltet.
1. I **Organisasjon**-feltet angir du forretningspartnerorganisasjonsbrukeren.
1. Velg **Legg til**, og velg deretter en kunde i feltet **Navn**.
1. Gjenta denne prosessen for å legge til flere kunder i hierarkiet.

## <a name="additional-information"></a>Tilleggsinformasjon

- Alle jobbene som er nevnt i dette emnet, kan konfigureres til å kjøres for en plan i et satsvist format. Forventningen er at forretningspartnere vil konfigurere satsvise jobber etter behov.
- I øyeblikket kan bare én bruker/kunde-post utpekes som administratorbruker, og denne rollen kan bare endres i Commerce Headquarters. Det er ingen støtte for selvbetjeningsfunksjoner som gjør at forretningspartnere kan angi flere administratorer eller endre administratorer fra webområder for B2B-e-handel.
<!--- The modules and labels of the different fields referenced in the screenshots for e-commerce are only for illustration purposes. Customers have complete control on the placement of the B2B related modules and the labels.-->
- Selv om forbruksgrenser kan defineres for brukere, er det ikke ennå ikke implementert forbruksgrenser i løpet av ordreregistreringsprosessen.
- All forretningslogikk og validering for en brukers erfaring på et B2B-webområde for e-handel er basert på konfigurasjonen til kundeposten som er tilordnet brukeren i Commerce Headquarters.

## <a name="additional-resources"></a>Tilleggsressurser

[Definere et B2B-e-handelsområde](set-up-b2b-site.md)

[Opprette organisasonsmodellhierarkier for B2B-organisasjoner](org-model.md)

[Konfigurere kundekontobetalingsmetode for B2B-e-handelsområder](payment-method.md)

[Angi produktantallsgrenser for B2B-e-handelsområder](quantity-limits.md)

[Oversikt over nummerserier](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
