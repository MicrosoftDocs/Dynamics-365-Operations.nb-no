---
title: Administrere forretningspartnerbrukere på B2B-e-handelssider
description: Dette emnet beskriver hvordan du legger til, sletter og redigerer forretningspartnerbrukere på bedrift-til-bedrift-e-handelsnettsteder (B2B) for Microsoft Dynamics 365 Commerce og i Commerce Headquarters.
author: josaw1
ms.date: 02/17/2022
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
ms.openlocfilehash: def8d4de082ceb4be77ed7e8898cbef82d52b749
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323461"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Administrere forretningspartnerbrukere på B2B-e-handelssider

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du legger til, sletter og redigerer forretningspartnerbrukere på bedrift-til-bedrift-e-handelsnettsteder (B2B) for Microsoft Dynamics 365 Commerce og i Commerce Headquarters.

> [!NOTE]
> Emnet [Administrere B2B-forretningspartnere ved hjelp av kundehierarkier](partners-customer-hierarchies.md) er en forutsetning for dette dokumentet. 

B2B-e-handelsområder krever at organisasjoner registrerer seg for å bli forretningspartnere. Etter at en organisasjon har sendt registreringsdetaljer til et B2B-e-handelsnettsted, går forespørselen om registrering gjennom en kvalifikasjonsprosess. Hvis organisasjonen er kvalifisert, blir den innført som forretningspartner.

Når en organisasjon er innført som forretningspartner, identifiseres organisasjonsbrukeren som startet forespørselen om å bli forretningspartner, som administratorbrukeren, og får rettigheter til å innføre ytterligere autoriserte brukere av B2B-nettstedet for e-handel. Disse autoriserte brukerne kan deretter legge inn ordrer på vegne av forretningspartneren.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Konfigurere administratorbrukeren for en ny forretningspartner

Potensielle forretningspartnere kan starte innføringsprosessen på et B2B-e-handelsnettsted ved å sende en innføringsforespørsel via en kobling på B2B-nettstedet. De kan deretter bruke skjemaet som kan tilpasses, til å oppgi de nødvendige detaljene for innføring og registrering. Når forespørselen er sendt, vises en bekreftelsesside for innsending. Hvis innsendingen godkjennes, blir firmaet som forespørselen ble sendt inn for, en forretningspartner, og anmoderen (brukeren som startet innføringsforespørselen) blir administratorbrukeren for forretningspartneren.

Følg disse trinnene for å godkjenne en forretningspartnerforespørsel i Commerce Headquarters.

1. Gå til **IT for Detaljhandel og handel \> Distribusjonsplan**.
1. Kjør jobben **P-0001** for å trekke alle forretningspartnerinnføringsforespørsler til Commerce Headquarters.
1. Når **P-0001**-jobben er kjørt, kan du gå til **IT for Detaljhandel og handel \> Kunde** og kjøre jobben **Synkroniser kunder og kanalforespørsler**. Når denne jobben er kjørt, opprettes innføringsforespørsler som kundeemneposter av typen **B2B-kundeemne** i Commerce Headquarters. 
1. Gå til **Kunder \> Alle kundeemner**, og velg kundeemneposten for den nye forretningspartneren for å åpne siden for kundeemnedetaljer.
1. I **Generelt**-fanen velger du **Konverter \> Godkjenn/Avvis** for å godkjenne forespørselen om innføring. Når bekreftelsesmeldingen vises, bekrefter du at du vil fortsette med prosessen, og deretter godkjenner du forespørselen. Godkjenningen endrer **Status**-feltet for kundeemneposten til **Godkjent**. En e-post sendes deretter til e-postadressen til anmoder for å bekrefte at organisasjonen er godkjent som forretningspartner. Det opprettes også et kundehierarki, der anmoderen legges til som administrator for forretningspartneren.

    > [!NOTE]
    > For øyeblikket sendes e-postbekreftelsen umiddelbart ved godkjenning. Fremtidig Commerce-funksjonalitet lar imidlertid administratoren utløse e-postmeldingene manuelt.

1. Gå til **IT for Detaljhandel og handel \> Distribusjonsplan**, og kjør jobben **1010 (Kunder)** for å sende de nye kunde- og kundehierarkipostene til kanaldatabasen.

> [!NOTE]
> Minst én av adressebøkene som er knyttet til kunden, må tas med i kundeadresseboken som er knyttet til nettbutikken, for å sikre at de nye kundepostene sendes til kanaldatabasen. Du kan automatisere denne prosessen ved å konfigurere adresseboken for standardkunden i nettbutikken, slik at systemet kopierer adressebokverdien til alle nye kunder.

Etter at kundehierarkipostene er synkronisert med kanaldatabasen, kan anmoderen logge seg på B2B-e-handelsnettstedet ved hjelp av e-postadressen som vedkommende oppgav da innføringsforespørselen ble sendt. Brukerne kan bruke registreringsflyten til å definere passordet for kontoen. Hvis du vil ha mer informasjon om hvordan du aktiverer posten for B2C-identitetsleverandør for Azure Active Directory (Azure AD) som skal kobles til B2B-kundeposten som ble opprettet ved kundeemnegodkjenning, kan du se [Aktivere automatisk kobling](../identity-record-linking.md).

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>Varsle B2B-kundeemner når de godkjennes eller avvises

Når du godkjenner eller avviser en innføringsforespørsel fra et B2B-kundeemne, kan et e-postvarsel sendes til kundeemnet automatisk.

Følg denne fremgangsmåten i Commerce Headquarters for hendelser av varslingstypen **B2B-kundeemne godkjent** eller **B2B-kundeemne avvist**.

1. Opprett e-postmaler for e-postmeldinger som skal sendes til kundeemner når varslingstypen **B2B-kundeemne godkjent** eller **B2B-kundeemne avvist** utløses. Hvis du vil ha informasjon om plassholderne som disse varslingstypene støtter, kan du se [Varslingstyper](../email-templates-transactions.md#notification-types). Se [Opprett en e-postmal](../email-templates-transactions.md#create-an-email-template) hvis du vil ha mer informasjon om hvordan du oppretter e-postmaler.
1. Legg til varslingstypene **B2B-kundeemne godkjent** og **B2B-kundeemnet avvist** i e-postvarslingsprofilen, og tilordne dem deretter til e-postmalene du opprettet. Hvis du vil ha mer informasjon varslingsprofiler, kan du se [Definere en e-postvarslingsprofil](../email-notification-profiles.md).

## <a name="onboard-additional-business-partner-users"></a>Innføre flere forretningspartnerbrukere

Forretningspartneradministratorbrukeren kan sende flere forretningspartnerbrukere til B2B-e-handelsnettstedet etter behov.

Følg denne fremgangsmåten for å innføre flere forretningspartnerbrukere på et B2B-e-handelsnettsted.

1. Logg deg på B2B-e-handelsnettstedet som administrator.
1. Gå til **Min konto \> Organisasjonsbrukere \> Vis detaljer**, og velg **Legg til en bruker**.
1. Angi den nødvendige informasjonen, og velg deretter **Lagre**. Statusen for den nye brukeren angis til **Venter**.

Etter at jobbene **P-0001** og **Synkroniser kunder og kanalforespørsler** er kjørt, opprettes en kundepost av typen **Person** for den nye brukeren i Commerce Headquarters. Denne kundeposten er også knyttet til den relevante forretningspartnerens kundehierarkipost. I tillegg sendes det en e-post til den nye brukerens e-postadresse for å varsle dem om at de er lagt til som bruker av forretningspartnerorganisasjonen, og kan nå logge seg på B2B-nettstedet for e-handel.

Kjør deretter jobben **1010 (Kunder)** for å synkronisere den nye forretningspartnerbrukeren til kanaldatabasen.

Etter at kundeposten er synkronisert, settes statusen til brukeren på B2B-e-handelsnettstedet til **Aktiv**, og den nye brukeren kan logge seg på B2B-e-handelsnettstedet ved hjelp av e-postadressen. Brukerne kan bruke registreringsflyten til å definere passordet for kontoen. Hvis du vil ha mer informasjon om hvordan du aktiverer posten for B2C-identitetsleverandør for Azure AD som skal kobles til B2B-kundeposten som ble opprettet i Commerce Headquarters, kan du se [Aktivere automatisk kobling](/dynamics365/commerce/identity-record-linking.md).

## <a name="edit-business-partner-user-details"></a>Redigere brukerdetaljer for forretningspartner

Følg denne fremgangsmåten for å redigere detaljene til forretningspartnerbrukere.

1. Logg deg på B2B-e-handelsnettstedet som administrator.
1. Gå til **Min konto \> Organisasjonsbrukere \> Vis detaljer**, velg **Rediger**-knappen (blyantsymbol), gjør de nødvendige endringene, og velg deretter **Lagre**. Endringene trer bare i kraft etter at jobbene **P-0001**, **Synkroniser kunder og kanalforespørsler** og **1010 (Kunder)** er kjørt.

## <a name="remove-a-business-partner-user"></a>Fjerne en forretningspartnerbruker

En administrator kan etter behov fjerne eksisterende brukere av en forretningspartnerorganisasjon fra listen over brukere som har tilgang til nettstedet for B2-e-handel.
Følg denne fremgangsmåten for å fjerne en forretningspartnerbruker.
- Logg deg på B2B-e-handelsnettstedet som administrator.
- Gå til **Min konto > Organisasjonsbrukere \> Vis detaljer**, og velg **Fjern**-knappen («X»-symbol). Når det vises en bekreftelsesmelding, bekrefter du at du vil fjerne brukeren. Endringen trer bare i kraft etter at jobbene **P-0001**, **Synkroniser kunder og kanalforespørsler** og **1010 (Kunder)** er kjørt.

> [!NOTE]
> Når du fjerner en bruker fra listen over brukere som har tilgang til B2B-e-handelsnettstedet, fjernes den tilsvarende kundeposten fra forretningspartnerens kundehierarkipost. Kundeposten i seg selv slettes imidlertid ikke fra Commerce Headquarters.

## <a name="onboard-existing-customers-as-business-partners-on-the-b2b-e-commerce-website"></a>Innføre eksisterende kunder som forretningspartnere på B2B-e-handelsnettstedet

Administratorer kan innføre forretningspartnere og brukere direkte i Commerce Headquarters. Denne funksjonen er nyttig når du skal innføre eksisterende forretningspartnere på B2B-e-handelsnettstedet.

Følg disse trinnene for å innføre forretningspartnere og brukere direkte i Commerce Headquarters.

1. Opprett eller velg en kunde av typen **Organisasjon** som du vil legge til som forretningspartner.
1. Opprett eller velg en kunde av typen **Person** som du vil legge til som administrator eller bruker for forretningspartneren. Kontroller at primære e-postadresser er knyttet til kundene. Du bruker disse e-postadressene til å logge deg på nettstedet. 

    > [!NOTE]
    > Systemet må kunne finne en unik kundepost for brukere som skal kunne logge seg på nettstedet. Hvis systemet finner flere kunder som har samme primære e-postadresse i den juridiske enheten, kan ikke brukeren logge seg på nettstedet.

1. Opprett en ID for kundehierarki.
1. Angi et navn i **Navn**-feltet.
1. I **Organisasjon**-feltet angir du forretningspartnerorganisasjonsbrukeren.
1. Velg **Legg til** i hurtigfanen **Hierarki**.
1. I **Navn**-feltet velger du en kunde av typen **Person**.
1. Velg **Administrator**-rollen for kunden som skal være administrator.
1. Gjenta denne prosessen for å legge til flere kunder i hierarkiet.

## <a name="additional-information"></a>Tilleggsinformasjon

- Alle jobbene som er nevnt i dette emnet, kan konfigureres til å kjøres for en plan i et satsvist format. Forventningen er at forretningspartnere vil konfigurere satsvise jobber etter behov.
- I øyeblikket kan bare én bruker/kunde-post utpekes som administratorbruker, og denne rollen kan bare endres i Commerce Headquarters. Det er ingen støtte for selvbetjeningsfunksjoner som gjør at forretningspartnere kan angi flere administratorer eller endre administratorer fra B2B-e-handelsnettsteder.
- Selv om forbruksgrenser kan defineres for brukere, er det ikke ennå ikke implementert forbruksgrenser i løpet av ordreregistreringsprosessen.
- All forretningslogikk og validering for en brukers erfaring på et B2B-e-handelsnettsted er basert på konfigurasjonen til kundeposten som er tilordnet brukeren i Commerce Headquarters.

## <a name="additional-resources"></a>Tilleggsressurser

[Definere et e-handelsområde for B2B](set-up-b2b-site.md)

[Administrere B2B-forretningspartnere ved hjelp av kundehierarkier](partners-customer-hierarchies.md)

[Konfigurere kundekontobetalingsmetode for B2B-e-handelsområder](payment-method.md)

[Angi produktantallsgrenser for B2B-e-handelsområder](quantity-limits.md)

[Oversikt over nummerserier](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
