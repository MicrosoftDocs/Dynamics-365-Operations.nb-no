---
title: Bruk den elektroniske faktureringstjenesten til å importere leverandørfakturaer
description: Dette emnet gir informasjon om hvordan du importerer leverandørfakturaer ved hjelp av tjenesten elektronisk fakturering.
author: gionoder
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c28adbfe532e77a52cab7625b9539d1e8e528bea
ms.sourcegitcommit: 81bc42551e6c9af6ad38908afb606ee1f8d3c44b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473382"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>Bruk den elektroniske faktureringstjenesten til å importere leverandørfakturaer

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med import av leverandørfakturaer med tjenesten for elektronisk fakturering. Den leder deg gjennom konfigurasjonstrinnene i RCS (Regulatory Configuration Services), Dynamics 365 Finance og Dynamics 365 Supply Chain Management du må følge for å motta elektroniske leverandørfakturaer fra leverandørene.

## <a name="set-up-vendor-invoice-import-in-rcs"></a>Definere leverandørfakturaimport i RCS
Følg denne fremgangsmåten for å sette opp leverandørfakturaimport i RCS:

1. Se i listen over [vanligvis tilgjengelige funksjoner for elektronisk fakturering](e-invoicing-configuration-rcs.md#generally-available-features).
2. Velg og importer funksjonen for Elektronisk fakturering. Se [Importer en funksjon for elektronisk fakturering fra Microsoft-konfigurasjonsleverandøren](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider) for mer informasjon.
3. Opprett en funksjon for Elektronisk fakturering for organisasjonen. Se [Opprett en funksjon for elektronisk fakturering under organisasjonen](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider) for mer informasjon.

## <a name="configure-an-email-account-channel"></a>Konfigurer en e-postkontokanal

Konfigurer en e-postkontokanal hvis den elektroniske faktureringsfunksjonen du opprettet, importerer elektroniske leverandørfakturaer fra vedlagte filer som mottas med e-post.

1. I RCS velger du funksjonen for Elektronisk fakturering som du opprettet. Kontroller at du velger versjonen med statusen **Utkast**.
2. På **Oppsett** i fanen i rutenettet velger du et funksjonsoppsett og deretter **Rediger**.
3. Angi navnet på kanalen i **Datakanal**-fanen i **Parameter**-feltgruppen i **Datakanal**-feltet. Kanalnavnet kan ikke ha mer enn ti tegn.
4. Angi leverandøren av e-postkontoen i feltet **Serveradresse**. Serveradressen for **https://outlook.live.com/** er for eksempel **imap-mail.outlook.com**.
5. I **Serverport**-feltet angir du porten som brukes av e-postkontoleverandøren. For eksempel er serverporten for **https://outlook.live.com/** **993**.
6. I **Brukernavnhemmelighet**-feltet angir du navnet på nøkkelhvelvhemmeligheten som inneholder ID-en til e-postbrukerkontoen. Denne nøkkelen må opprettes i Azure Key Vault og settes opp i servicemiljøet. 
7. I **Brukerpassordhemmelighet**-feltet angir du navnet på nøkkelhvelvhemmeligheten som inneholder passordet til e-postbrukerkontoen.
8. Valgfritt – Angi verdier i feltene **Fra filter**, **Emnefilter** og **Datofilter**.
9. Angi navnene på e-postmappene der e-postmeldinger skal være:

    - Importert fra: **Hovedmappe**
    - Lagret etter vellykket behandling: **Arkivmappe**
    - Lagret etter ikke vellykket behandling: **Feilmappe** Du trenger ikke å opprette disse mappene i e-postboksen. Mappene opprettes automatisk etter første e-fakturaimport og -behandling. 
   
10. I feltgruppen **Vedleggsfilter** legger du til filfiltreringsinformasjonen. Bare vedlegg som oppfyller det definerte filteret, behandles. Du kan for eksempel definere "\*.xml" for vedlegg med en xml-filtype. Navnet på vedlegget brukes i Dynamics 365 Finance eller Dynamics 365 Supply Chain Management under oppsett. 
11. Gå gjennom og oppdater kriteriene i kategorien **Relevansregler** som nødvendig. **Kanal**-feltet må være likt **Data-kanalen** som ble angitt tidligere. Hvis du vil ha mer informasjon, kan du se [Relevansregler](e-invoicing-configuration-rcs.md#applicability-rules).
12. Velg **Lagre** og lukk siden.

### <a name="configure-a-microsoft-sharepoint-channel"></a>Konfigurer en Microsoft SharePoint-kanal

Konfigurer en Microsoft SharePoint-kanal hvis funksjonen for elektronisk fakturering importerer elektroniske leverandørfakturaer fra filer som er plassert i SharePoint-mapper.

1. I RCS velger du funksjonen for Elektronisk fakturering som du opprettet. Kontroller at du velger **versjonen** med statusen **Utkast**.
2. På **Oppsett** i fanen i rutenettet velger du et funksjonsoppsett og deretter **Rediger**.
3. I fanen **Datakanal** i **Parameter**-feltgruppen velger du **SharePoint-adresse** og angir SharePoint-nettadressen.
4. Velg **Serverport** og angi porten som brukes av e-postkontoleverandøren.
5. Velg **Program-ID** og angi navnet på nøkkelhvelvhemmeligheten som inneholder ID-en til SharePoint-klienten.
6. Velg **Programhemmelighet** og angi navnet på nøkkelhvelvhemmeligheten som inneholder passordet til SharePoint-klienten.
7. Velg **Filfilter**. Gå gjennom og oppdater masken for å filtrere filene som inneholder den elektroniske leverandørfakturaen, for import.
8. Gå gjennom og oppdater kriteriene i kategorien **Relevansregler** om nødvendig. Hvis du vil ha mer informasjon, kan du se [Relevansregler](e-invoicing-configuration-rcs.md#applicability-rules).
9. Velg **Lagre** og lukk siden

### <a name="deploy-an-electronic-invoicing-feature"></a>Distribuer en funksjon for Elektronisk fakturering

Hvis du vil distribuere funksjonen for elektronisk fakturering til servicemiljøet, kan du se [Distribuer funksjonen for elektronisk fakturering til servicemiljø](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="set-up-vendor-invoice-import-in-finance-or-supply-chain-management"></a>Konfigurer leverandørfakturaimport i Finance eller Supply Chain Management
Fullfør trinnene i de følgende to delene for å definere ulike typer import av leverandørfakturaer.

### <a name="import-brazilian-nf-e-from-email"></a>Brasiliansk NF-e-import fra e-post

1. Logg deg på Finance- eller Supply Chain Management-miljøet, og kontroller at du er i riktig juridisk enhet.
2. Gå til **Organisasjonsstyring** > **Oppsett** > **Parametere for elektronisk dokument**.
3. I fanen **Funksjoner** kontrollerer du at **NF-e føderal – elektronisk faktura for Brasil** er valgt.
4. Velg **Legg til** i fanen **Eksterne kanaler** på feltgruppen **Kanaler**.
5. I **Kanal**-feltet angir du **NFe** (navnet på kanalen som er angitt i konfigurasjonen av datakanalen for funksjonen for elektronisk fakturering i RCS).
6. Angi en beskrivelse i **Beskrivelse**-feltet. Velg den juridiske enheten i **Firma**-feltet.
7. I feltet **Dokumentkontekst** velger du **Kontekstmodell for kundefaktura – regnskapsdokumentkontekst**.
8. Velg **Legg til** i feltgruppen **Importer kilder**.
9. I **Navn**-feltet angir du **XmlFile** (navnet på kanalen **Vedleggsfilter** som er angitt i konfigurasjonen av datakanalen for funksjonen for elektronisk fakturering i RCS).
10. I **Beskrivelse**-feltet skriver du inn en beskrivelse, og i feltet **Dataenhetsnavn** velger du **Mottatte NF-e XML-dokumenter**.
11. Velg **Import av NF-e-post – import av NF-e-epost (BR)** i **Modelltilordning**-feltet, og velg deretter **Lagre**.
12. Velg **Legg til** i feltgruppen **Elektronisk rapportering** i fanen **Elektronisk dokument**, og velg deretter velger du **Mottatt NF-e XML-dokument** i **Tabellnavn**-feltet.
13. I feltet **Dokumentkontekst** velger du **Kontekstmodell for kundefaktura – be om regnskapsdokumentkontekst**.
14. I feltet **Tilordning av elektronisk dokumentmodell** velger du **Forespørselstilordning – regnskapsdokumenttilordning**.
15. Velg **Svartyper**, og velg deretter **Ny**.
16. I feltet **Svartype** angir du **Svar**. I feltet for **innsendingsstatus** angir du **Planlagt**.
17. I feltet **Modelltilordning** velg **Modelltilordning fra svarmelding – svarmeldingsimportformat**.
18. Velg **Lagre** og lukk deretter siden.

### <a name="import-peppol-electronic-vendor-invoices"></a>Importer PEPPOL-elektroniske leverandørfakturaer

1. Gå til arbeidsområdet **Elektronisk rapportering** og velg **Rapporteringskonfigurasjoner**.
2. Velg **Kontekstmodell for kundefaktura**, og velg deretter **Opprett konfigurasjon** > **Avled fra navn: Kontekstmodell for kundefaktura, Microsoft** for å opprette en avledet konfigurasjon.
3. I **Utkast**-versjonen velger du **Utforming**, og i **Datamodell**-treet velger du **Tilordne modell til datakilde**.
4. Velg **DataChannel** i **Definisjoner**-treet, og velg deretter **Utforming**.
5. I **Datakilder**-treet utvider du **$Context\_Channel**-containeren. I **Verdi**-feltet velger du **Rediger** og angir datakanalnavnet. Dette er navnet på kanalen som er angitt i konfigurasjonen av datakanalen for funksjonen for elektronisk fakturering i RCS. 
7. Velg **Lagre** og lukk siden.
8. Lukk siden.
9. Velg den avledede konfigurasjonen du nettopp opprettet fra **Kontekstmodell for kundefaktura**, og i **Versjoner**-hurtigfanen velger du **Endre status** > **Fullført**.
10. Gå til **Organisasjonsadministrasjon** > **Oppsett** > **Elektroniske dokumentparametere**, og kontroller at du har valgt **PEPPOL globale elektroniske fakturaene** på fanen **Funksjoner**. 
11. Velg **Legg til** i fanen **Eksterne kanaler** på feltgruppen **Kanaler**.
12. I **Kanal**-feltet angir du navnet på datakanalen og en beskrivelse i **Beskrivelse**-feltet.
13. Velg den juridiske enheten i **Firma**-feltet. 
14. Velg den nye avledede konfigurasjonen fra **Kontekstmodell for kundefaktura** i **Dokumentkontekst**-feltet. Tilordningsbeskrivelsen må være **Datakanalkontekst**.
15. Velg **Legg til** i feltgruppen **Importer kilder**.
16. I **Navn**-feltet angir du **Navn på vedleggsfilter**, og i **Navn på dataenhet**-feltet velger du **Leverandørfakturahode**.
17. I **Modelltilordning**-feltet velger du **Leverandørfaktura import - Importer leverandørfaktura**.
18. Klikk **Lagre**, og lukk deretter siden.


## <a name="receive-electronic-invoices"></a>Motta elektroniske fakturaer

Tjenesten for elektronisk fakturering går gjennom to trinn under fakturaimport fra datakanalene:

1. Åpner e-postboksen og leser e-post.
2. Behandler e-postmeldingene. 
    
For at du skal kunne utføre disse to trinnene bør klienten ringe tjenesten manuelt for hvert trinn. Vi anbefaler imidlertid at du definerer en satsvis jobb for mottak av elektroniske dokumenter.

Følg denne fremgangsmåten for å motta elektroniske fakturaer:

1. Gå til **Organisasjonsstyring** > **Periodiske** > **Elektroniske dokumenter** > **Motta elektroniske dokumenter**.
2. Velg **OK** og lukk deretter siden.


## <a name="view-receive-logs-for-electronic-invoices"></a>Vis mottakslogger for elektroniske fakturaer

Hvis du vil vise mottaksloggene for elektroniske fakturaer, kan du gå til **Organisasjonsadministrasjon** > **Periodisk** > **Elektroniske dokumenter** > **Mottakslogg for elektronisk faktura**.
Hvis du ikke ser fakturaer som er behandlet, fjerner du tabellfilteret.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
