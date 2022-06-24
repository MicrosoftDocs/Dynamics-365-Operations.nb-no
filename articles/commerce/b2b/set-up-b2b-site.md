---
title: Definer et netthandelsområde for B2B
description: Denne artikkelen beskriver hvordan du konfigurerer et bedrift-til-bedrift-e-handelsområde (B2B) i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0bcd864694ff2ad2aa211c927da4d698c0039715
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881912"
---
# <a name="set-up-a-b2b-e-commerce-site"></a>Definere et e-handelsområde for B2B

[!include [banner](../../includes/banner.md)]

E-handelsområder for bedrift-til-bedrift (B2B) har noen nøkkelfunksjoner som optimaliserer arbeidsflyten for en B2B-bruker. Denne artikkelen beskriver hvordan du konfigurerer et B2B-e-handelsområde i Microsoft Dynamics 365 Commerce. Det går gjennom modulene og områdeinnstillingene som må konfigureres for å aktivere B2B-spesifikke scenarier.

## <a name="prerequisites"></a>Forutsetninger

- Hvis du vil opprette et B2B-e-handelsområde, må du aktivere og konfigurere bestemte funksjoner i Commerce headquarters, som beskrevet i denne artikkelen.
- Kjerneerfaringer, for eksempel produktoppdagelse, produktdetaljersider, handlekurven og kassen, drives av de samme modulene som brukes for e-handelsområder for bedrift-til-kunde (B2C). Nettstedsforfattere bør være kjent med alle modulene som Dynamics 365 Commerce støtter. Hvis du vil ha mer informasjon, kan du se [Oversikt over modulbibliotek](../starter-kit-overview.md).
- Denne artikkelen antar at nettstedsforfattere forstår det grunnleggende om Commerce-områdebygger, maler, fragmenter og sider, slik at de kan aktivere B2B-funksjonene for e-handelsområder.

## <a name="site-level-settings"></a>Innstillinger på områdenivå

Du kan få tilgang til innstillinger på områdenivå i områdekonfigurator ved **Områdeinnstillinger \> Tillegg**. Følgende to innstillinger på områdenivå gjelder for B2B-scenarier:

- **Aktiver kundekontobetalinger** – Ved hjelp av kundekontoer kan brukere betale for ordrer. De tilgjengelige verdiene er **Aktivert for B2B-kunder**, **Aktivert B2C-kunder**, **Aktivert for alle kunder** og **Deaktivert for alle kunder**. Hvis B2B-området støtter kundekontoer, bør du velge **Aktivert for B2B-kunder**.
- **Aktiver antallsgrenser for ordre** – Med denne egenskapen kan du angi grenser for antall varer som kan bestilles for hvert produkt eller hver kategori. De tilgjengelige verdiene er **Aktivert for B2B-kunder**, **Aktivert B2C-kunder**, **Aktivert for alle kunder** og **Deaktivert for alle kunder**.

> [!NOTE]
> Når du oppgraderer til den siste versjonen av modulbiblioteket, må du følge flere trinn for å sikre at de tidligere beskrevne områdeinnstillingene er tilgjengelige i miljøet ditt. Hvis du vil ha mer informasjon, kan du se [Oppdatere filen app.settings.json](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="create-business-partner-sign-up-pages"></a>Opprette registreringssider for forretningspartner

For å bli forretningspartner må brukerne først sende en forretningspartnerforespørsel. En kobling til forespørselssiden for forretningspartnere vil være tilgjengelig på startsiden B2B, slik at brukere kan starte prosessen. Når brukerne har sendt en forretningspartnerforespørsel, mottar de bekreftelse på at forespørselen er sendt. 

### <a name="create-a-business-partner-request-page"></a>Opprette en forespørselsside for forretningspartnere

Modulen **Parterregisterring** på en forespørselsside for forretningspartnere brukes til å starte brukerforespørsler for å bli forretningspartnere. I denne modulen kan du samle inn brukerinformasjonen som kreves for registreringsprosessen. I tillegg brukes **Forretningskontoadresse** til å registrere brukerens adresse.

Følg denne fremgangsmåten for å sette opp og konfigurere forespørselssiden for forretningspartneren i områdebyggeren.

1. Opprett en mal med navnet **Registrering**. Denne malen bør inneholde følgende moduler:

    - Partnerregistrering
    - Søkebane
    - Hode
    - Bunntekst
    - Innholdsblokk
    - Tekstblokk
    - Produktsamling

1. Bruk **Registrering**-malen til å opprette en side som kalles **Forretningspartnerforespørsel**.
1. I sporet **Hode** legger du til hodefragmentet som er forhåndskonfigurert med områdehodet.
1. I sporet **Bunntekst** legger du til bunntekstfragmentet som er forhåndskonfigurert med områdebunnteksten.
1. I sporet **Hoved** legger du til modulen **Container**. I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**.
1. Legg til en **Brødsmule**-modul i **Container**-sporet. På siden for modulegenskaper, under **Koblinger**, konfigurer en kobling til startsiden, og angi **Start** som koblingstekst.
1. I sporet **Container** legger du til en **Partnerregistrering**-modul under modulen **Brødsmule**. I moduleegnskapsruten, under **Overskrift**, angir du **Bli en forretningspartner**.
1. I sporet **Partnerregistrering** legger du til modulen **Forretningskontoadresse**.
1. I sporet **Container** legger du til en **Tekstblokk**-modul under modulen **Partnerregistrering**. Her kan du definere noen vilkår og betingelser for registreringsprosessen.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.
1. Publiser URL-adressen for siden.

### <a name="create-a-business-partner-request-confirmation-page"></a>Opprette en bekreftelsesside for forretningspartnerforespørsel

Når en forretningspartnerforespørsel er sendt, skal det vises en bekreftelsesside der brukeren kan bekrefte innsendingen. 

Følg denne fremgangsmåten for å sette opp og konfigurere bekreftelsessiden for forespørsel i områdebyggeren.

1. Bruk **Registrering**-malen som du opprettet tidligere, for å opprette en side som kalles **Partnerforespørselsbekreftelse**.
1. I sporet **Hode** legger du til hodefragmentet som er forhåndskonfigurert med områdehodet.
1. I sporet **Bunntekst** legger du til bunntekstfragmentet som er forhåndskonfigurert med områdebunnteksten.
1. I sporet **Hoved** legger du til modulen **Container**. I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**.
1. I sporet **Container** legger du til modulen **Innholdsblokk**. I modulegenskapsruten, under **Overskrift**, angir du **Forespørsel sendt**. I **Rik tekst**-feltet angir du **Forespørselen har blitt sendt**. Under **Koblinger** konfigurerer du en kobling til startsiden, og angi **Tilbake til shopping** som koblingstekst.
1. Legg til en ny **Container**-modul, og legg til en **Produktsamling**-modul i den.
1. Konfigurer **Produktsamling**-modulen med anbefalings- eller kategorilisten som du vil presentere på siden.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.
1. Publiser URL-adressen for siden.

Følg denne fremgangsmåten for å legge til en kobling på bekreftelsessiden for forespørsel i områdebyggeren.

1. Gå til siden **Forretningspartnerforespørsel** du opprettet tidligere, og velg **Rediger**. 
1. Velg **Partnerregistrering**-modulsporet. I egenskapsruten, under **Kobling til bekreftelsessiden for registrering**, konfigurerer du koblingen til forespørselssiden for forretningspartnere som du opprettet tidligere. 
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

### <a name="add-a-business-partner-request-link-to-the-home-page"></a>Legge til en kobling til forretningspartnerforespørselen på startsiden

Når registrerings- og bekreftelsessidene for forretningspartnere er opprettet, må du gjøre registreringssiden tilgjengelig via en kobling på startsiden. Du kan fullføre denne oppgaven ved å legge til koblingen i en hvilken som helst **Innholdsblokk**-modul på startsiden.

Følg denne fremgangsmåten for å legge til en kobling til forretningspartnerforespørselen på startsiden i områdebyggeren.

1. Gå til startsiden for området ditt, og velg **Rediger**.
1. Velg et **Innholdsblokk**-modulspor. I ruten for modulegenskaper, under **Koblinger**, konfigurerer du en kobling til forespørselssiden for forretningspartnere som du opprettet tidligere, og angi **Registrer deg som en forretningspartner** eller lignende tekst som koblingstekst. Legg til et bilde etter behov.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="account-management-landing-page"></a>Målside for kontobehandling

Målsiden for kontobehandling omfatter all kontobehandlingsinformasjon som kreves for både B2B- og B2C-e-handelsområder. Bare påloggede brukere kan vise denne siden.

Følg denne fremgangsmåten for å opprette og konfigurere en målside for B2B-kontostyring i områdebyggeren.

1. Opprett en mal med navnet **Kontobehandling**. Denne malen bør inneholde følgende moduler:

    - Hode
    - Bunntekst
    - Søkebane
    - Flis for velkomsthilsen for konto
    - Generell kontoflis
    - Flis for kontoadresse
    - Flis for ønskeliste for konto
    - Flis for kontoadresse
    - Flis for kontofordeler
    - Kundesaldoflis for konto
    - Flis for ordremaler for konto
    - Organisasjonsbrukere
    - Forretningsorganisasjonsliste
    - Kundekontosaldo
    - Ordremallinjer
    - Ordremalliste
    - Kontofakturaflis
    - Fakturaliste
    - Fakturadetaljer

1. Bruk malen **Kontobehandling**-malen til å opprette en side med navnet **Min konto**.
1. I sporet **Hode** legger du til hodefragmentet som er forhåndskonfigurert med områdehodet.
1. I sporet **Bunntekst** legger du til bunntekstfragmentet som er forhåndskonfigurert med områdebunnteksten.
1. I sporet **Hoved** legger du til modulen **Container**. I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**. 
1. Legg til en **Brødsmule**-modul i **Container**-sporet. På siden for modulegenskaper, under **Koblinger**, konfigurer en kobling til startsiden, og angi **Start** som koblingstekst.
1. I sporet **Container** legger du til modulen **Velkomstflis**. I modulegenskapsruten, under **Overskrift**, angir du **Velkommen**.
1. I **Hoved**-sporet legger du til en ny **Container**-modul (**Container 2**). I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**. Sett verdien **Underordnede som vises** til **To**. 
1. I sporet **Container 2** legger du til modulen **Generell flis for konto**. I modulegenskapsruten, under **Overskrift**, angir du **Min profil**. Konfigurer en kobling til **Min profil**-siden under **Koblinger**. 
1. I sporet **Container 2** legger du til en ny **Generell flis for konto**-modul. I modulegenskapsruten, under **Overskrift**, angir du **Ordrehistorikk**. Konfigurer en kobling ordrehistorikksiden under **Koblinger**.
1. I **Hoved**-sporet legger du til en ny **Container**-modul (**Container 3**). I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**. Sett verdien **Underordnede som vises** til **To**. 
1. I sporet **Container 3** legger du til modulen **Kontoadresseflis**. I modulegenskapsruten, under **Overskrift**, angir du **Min adresse**. Konfigurer en kobling til **Min adresse**-siden under **Koblinger**. 
1. I sporet **Container 3** legger du til modulen **Ønskelisteflis for konto**. I modulegenskapsruten, under **Overskrift**, angir du **Min ønskeliste**. Konfigurer en kobling til **Min ønskeliste**-siden under **Koblinger**.
1. I **Hoved**-sporet legger du til en ny **Container**-modul (**Container 4**). I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**. Sett verdien **Underordnede som vises** til **To**. 
1. I sporet **Container 4** legger du til modulen **Organisasjonsbrukere**. I modulegenskapsruten, under **Overskrift**, angir du **Organisasjonsbrukere**. 
1. I sporet **Container 4** legger du til modulen **Kundesaldoflis for konto**. I modulegenskapsruten, under **Overskrift**, angir du **Kontokreditt**. 
1. I **Hoved**-sporet legger du til en ny **Container**-modul (**Container 5**). I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**. Sett verdien **Underordnede som vises** til **To**. 
1. I modulen **Container 5** legger du til modulen **Ordremalflis for konto**. I modulegenskapsruten, under **Overskrift**, angir du **Ordremaler**. 
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

> [!NOTE] 
> Noen av delene du la til i trinn 13 til og med 18, vil ikke vises på WYSIWIG-lerrettet ("det du ser, er det du får") i områdebyggeren fordi de krever en signert B2B-konto.

## <a name="create-and-configure-customer-balance-pages-and-modules"></a>Opprette og konfigurere kundesaldosider og moduler 

Kundekontoer kan brukes til å betale for ordrer. Tilgjengelig saldo i en kundekonto kan vises fra en brukers kontobehandlingsside.

### <a name="create-a-customer-balance-page"></a>Opprette et kundesaldoside 

Før innloggede B2B-brukere kan vise kundesaldoen, må du opprette en kundesaldoside. 

For å opprette en kundesaldoside i områdebyggeren følger du denne fremgangsmåten.

1. Bruk malen **Kontobehandling** som du opprettet tidligere, til å opprette en side med navnet **Kundesaldo**.
1. I sporet **Hode** legger du til hodefragmentet som er forhåndskonfigurert med områdehodet.
1. I sporet **Bunntekst** legger du til bunntekstfragmentet som er forhåndskonfigurert med områdebunnteksten.
1. I **Hoved**-sporet legger du til en ny **Container**-modul (**Container 3**). I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**. Sett verdien **Underordnede som vises** til **To**.
1. Legg til en **Brødsmule**-modul i **Container**-sporet. På siden for modulegenskaper, under **Koblinger**, konfigurer en kobling til målsiden for kontobehandling, og angi **Min konto** som koblingstekst.
1. I sporet **Container** legger du til en **Kundekontosaldo**-modul. I modulegenskapsruten, under **Overskrift**, angir du **Kontosaldo**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.
1. Publiser URL-adressen for siden.
1. Gå til målsiden for kontoadministrasjon (**Min konto**) som du opprettet tidligere.
1. I egenskapsruten for modulen **Kundesaldoflis for konto** legger du til en kobling til kundesaldosiden. 
1. Lagre og publiser siden.

Kundesaldosiden er nå opprettet, og brukerne kan gå til den fra målsiden med kontoadministrasjon.

### <a name="configure-a-checkout-page-so-that-the-customer-balance-can-be-used-as-a-form-of-payment"></a>Konfigurere en betalingsside, slik at kundesaldoen kan brukes som en betalingsmetode

**Kundekontobetaling**-modulen er nødvendig for å gjøre det mulig å bruke kundesaldoen som betalingsmetode. Denne modulen bør legges til på betalingsside som en betalingsmetode. Hvis du vil ha mer informasjon om hvordan du konfigurerer en betalingsside og modulene som kreves for kassen, inkludert alle betalingsdetaljer, kan du se [Kassemodul](../add-checkout-module.md).

Når du har konfigurert en betalingsside, må du legge til modulen **Kundekontobetaling** på betalingsdelen og deretter lagre og publisere siden. B2B-brukere kan da logge seg på e-handelsområdet og bruke de tilgjengelige kundesaldo på ordrer i kassen.

I tillegg, i **Områdebygger \> Utvidelser**, må du kontrollere at egenskapen **Aktiver kundekontobetalinger** er satt til **Aktivert for B2B-kunder**.

## <a name="create-order-template-pages"></a>Opprette ordremalsider

To ordremalsider kan defineres for et B2B-e-handelsområde: en ordremallisteside og en ordremallinjeside.

En ordremallisteside viser en liste over alle ordremaler som er tilgjengelige. Den konfigureres ved hjelp av modulen **Ordremalliste**. På ordremallistesiden kan du opprette eller slette en mal og legge til varene i en mal i handlekurven.

En ordremallinjeside viser detaljene for ordremalen som er valgt på en ordremallisteside. Den konfigureres ved hjelp av modulen **Ordremallinjer**. Når en bruker velger navnet på en mal på en listeside for ordremaler, vises ordremallinjesiden og detaljene i malen. Brukeren kan deretter vise og redigere elementene i malen.

### <a name="create-an-order-templates-list-page"></a>Opprette en listeside for ordremaler

For å opprette en ordremallisteside i områdebyggeren følger du denne fremgangsmåten.

1. Bruk malen **Kontobehandling** som du opprettet tidligere, til å opprette en side med navnet **Ordremaler**.
1. I sporet **Hode** legger du til hodefragmentet som er forhåndskonfigurert med områdehodet.
1. I sporet **Bunntekst** legger du til bunntekstfragmentet som er forhåndskonfigurert med områdebunnteksten.
1. I sporet **Hoved** legger du til modulen **Container**. I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**.
1. Legg til en **Brødsmule**-modul i **Container**-sporet. På siden for modulegenskaper, under **Koblinger**, konfigurer en kobling til målsiden for kontobehandling, og angi **Min konto** som koblingstekst.
1. I sporet **Container** legger du til modulen **Ordremalliste**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.
1. Publiser URL-adressen for siden.
1. Gå til målsiden for kontoadministrasjon (**Min konto**) som du opprettet tidligere.
1. I egenskapsruten for modulen **Ordremalflis for konto**, under **Koblinger**, konfigurerer du en kobling til listesiden for ordremaler du nettopp opprettet.
1. Lagre og publiser siden.

Listesiden for ordremaler er nå opprettet, og brukerne kan gå til den fra målsiden med kontoadministrasjon.

### <a name="create-an-order-template-lines-page"></a>Opprette en ordremallinjeside

For å opprette en ordremallinjeside i områdebyggeren følger du denne fremgangsmåten.

1. Bruk malen **Kontobehandling** som du opprettet tidligere, til å opprette en side med navnet **Ordremallinjer**.
1. I sporet **Hode** legger du til hodefragmentet som er forhåndskonfigurert med områdehodet.
1. I sporet **Bunntekst** legger du til bunntekstfragmentet som er forhåndskonfigurert med områdebunnteksten.
1. I sporet **Hoved** legger du til modulen **Container**. I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**.
1. Legg til en **Brødsmule**-modul i **Container**-sporet. På siden for modulegenskaper, under **Koblinger**, konfigurer en kobling til målsiden for kontobehandling, og angi **Min konto** som koblingstekst.
1. I sporet **Container** legger du til modulen **Ordremallinjer**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.
1. Publiser URL-adressen for siden.

## <a name="onboard-business-partner-users"></a>Pålaste forretningspartnerbrukere

På siden for organisasjonsbrukere kan administratoren for en forretningspartnerorganisasjon opprette flere brukere fra denne organisasjonen til B2B-e-handelsområdet. Den konfigureres ved hjelp av modulen **Forretningsorganisasjonsliste**. Fra organisasjonsbrukersiden kan en administrator legge til eller fjerne brukere, definere kontosaldoer og be om kontoutdrag for en bruker.

For å opprette en organisasjonsbrukerside i områdebyggeren følger du denne fremgangsmåten.

1. Bruk malen **Kontobehandling** som du opprettet tidligere, til å opprette en side med navnet **Organisasjonsbruker**.
1. I sporet **Hode** legger du til hodefragmentet som er forhåndskonfigurert med områdehodet.
1. I sporet **Bunntekst** legger du til bunntekstfragmentet som er forhåndskonfigurert med områdebunnteksten.
1. I sporet **Hoved** legger du til modulen **Container**. I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**.
1. Legg til en **Brødsmule**-modul i **Container**-sporet. På siden for modulegenskaper, under **Koblinger**, konfigurer en kobling til målsiden for kontobehandling, og angi **Min konto** som koblingstekst.
1. I sporet **Container** legger du til modulen **Forretningsorganisasjonsliste**. I modulegenskapsruten, under **Overskrift**, angir du **Organisasjonsbrukere**.
1. I egenskapsruten for **Forretningsorganisasjonsliste**-modulen aktiverer du egenskapene **Tabellsortering** og **Tabellpaginering**. Sett pagineringsantallet til **5**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.
1. Publiser URL-adressen for siden.
1. Gå til målsiden for kontoadministrasjon (**Min konto**) som du opprettet tidligere.
1. I egenskapsruten for modulen **Flis for organisasjonsbrukere** under **Koblinger**, konfigurerer du en kobling til siden for organisasjonsbrukere som du nettopp opprettet. 
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="create-invoice-pages"></a>Opprette fakturasider

En fakturalisteside viser en liste over alle tilgjengelige fakturaer. Den konfigureres ved hjelp av modulen **Fakturaliste**. Fra fakturalistesiden kan brukere betale eller be om fakturaer. 

En fakturadetaljside viser detaljene i fakturaen som er valgt på en fakturalisteside. Den konfigureres ved hjelp av modulen **Fakturadetaljer**. Når en bruker velger en faktura-ID på en fakturalisteside, vises fakturadetaljsiden og detaljene i fakturaen.

### <a name="create-an-invoices-list-page"></a>Opprette en fakturalisteside

For å opprette en fakturalisteside i områdebyggeren følger du denne fremgangsmåten.

1. Bruk malen **Kontobehandling** som du opprettet tidligere, til å opprette en side med navnet **Fakturaliste**.
1. I sporet **Hode** legger du til hodefragmentet som er forhåndskonfigurert med områdehodet.
1. I sporet **Bunntekst** legger du til bunntekstfragmentet som er forhåndskonfigurert med områdebunnteksten.
1. I sporet **Hoved** legger du til modulen **Container**. I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**.
1. Legg til en **Brødsmule**-modul i **Container**-sporet. På siden for modulegenskaper, under **Koblinger**, konfigurer en kobling til målsiden for kontobehandling, og angi **Min konto** som koblingstekst.
1. I sporet **Container** legger du til modulen **Fakturaliste**. I modulegenskapsruten, under **Overskrift**, angir du **Fakturaer**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.
1. Publiser URL-adressen for siden.
1. Gå til målsiden for kontoadministrasjon (**Min konto**) som du opprettet tidligere.
1. I egenskapsruten for modulen **Fakturaflis for konto**, under **Koblinger**, konfigurerer du en kobling til listesiden for fakturaer du nettopp opprettet. 
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

### <a name="create-an-invoice-details-page"></a>Opprette en side med fakturadetaljer

For å opprette en side for fakturadetaljer i områdebyggeren følger du denne fremgangsmåten.

1. Bruk malen **Kontobehandling** som du opprettet tidligere, til å opprette en side med navnet **Fakturadetaljer**.
1. I sporet **Hode** legger du til hodefragmentet som er forhåndskonfigurert med områdehodet.
1. I sporet **Bunntekst** legger du til bunntekstfragmentet som er forhåndskonfigurert med områdebunnteksten.
1. I sporet **Hoved** legger du til modulen **Container**. I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**.
1. Legg til en **Brødsmule**-modul i **Container**-sporet. På siden for modulegenskaper, under **Koblinger**, konfigurer en kobling til målsiden for kontobehandling, og angi **Min konto** som koblingstekst. Deretter konfigurerer du en kobling til fakturalistesiden og angir **Fakturalister** som koblingstekst.
1. I sporet **Container** legger du til modulen **Fakturadetaljer**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.
1. Publiser URL-adressen for siden.

## <a name="add-a-quick-add-module-to-the-cart-page"></a>Legge til en Hurtigtillegg-modul i handlekurvsiden

Med Hurtigtillegg-modulen kan du raskt legge til flere varer i handlekurven ved å bruke vare-IDer (kalles også lagerenhet \[SKU\] ID-er). Hurtigtillegg-modulen legges til på kurvsiden for et område.

Følg denne fremgangsmåten for å legge til en Hurtigtillegg-modul på handlekurvsiden i Commerce-områdebyggeren.

1. Gå til **Maler**, og velg områdets handlekurvsidemal.
1. Velg **Rediger**.
1. På **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Hurtigtillegg**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og velg områdets handlekurvsidemal.
1. På **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I egenskapsruten for **Container**-modulen under **Bredde** velger du **Fyll container**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Hurtigtillegg**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

> [!NOTE] 
> Hurtigtillegg-modulen er tilgjengelig fra Commerce versjon 10.0.17-versjonen. Hvis du oppdaterer fra en eldre versjon av Commerce, må du manuelt oppdatere appsettings.json-filen. Hvis du vil ha instruksjoner, kan du se [Oppdateringer for SDK og modulbibliotek](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="add-a-bulk-purchase-module-to-a-product-details-page"></a>Legge til en massekjøpsmodul på en produktdetaljside

Massekjøpsmodulen på en produktdetaljside (PDP) gir en matrisebasert erfaring som gjør at en kjøper raskt kan legge til flere varianter av et produkt i handlekurven. Når en områdebruker må bestille flere varianter av det samme produktet, eliminerer denne erfaringen behovet for å velge kombinasjonen av produktdimensjoner, definere antallet, legge til varianten i handlekurven og deretter gjenta prosessen for andre kombinasjoner av produktdimensjoner.

Følg disse trinnene for å legge til en massekjøpsmodul i en PDP i Commerce-områdebygger.

1. Gå til **Maler**, og velg områdets PDP-mal.
1. Velg **Rediger**.
1. På **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **massekjøp**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og velg områdets PDP.
1. På **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I egenskapsruten for **Container**-modulen under **Bredde** velger du **Fyll container**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **massekjøp**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

> [!NOTE] 
> Massekjøpsmodulen er tilgjengelig fra Commerce versjon 10.0.24-versjonen. Hvis du oppdaterer fra en eldre versjon av Commerce, må du manuelt oppdatere appsettings.json-filen. Hvis du vil ha instruksjoner, kan du se [Oppdateringer for SDK og modulbibliotek](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](../starter-kit-overview.md)

[Oppdateringer for SDK og modulbibliotek](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)

[Oversikt over redigering av side](../authoring-home-overview.md)

[Oversikt over maler og oppsett](../templates-layouts-overview.md)

[Arbeide med fragmenter](../work-with-fragments.md)

[Legg til en ny områdeside](../add-new-page.md)

[Kassemodul](../add-checkout-module.md)

[Innholdsblokkmodul](../add-hero-module.md)

[Produktsamlingsmodul](../product-collection-module-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
