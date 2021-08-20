---
title: Bruk den elektroniske faktureringstjenesten til å importere leverandørfakturaer
description: Dette emnet gir informasjon om hvordan du importerer leverandørfakturaer ved hjelp av tjenesten elektronisk fakturering.
author: gionoder
ms.date: 08/03/2021
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
ms.openlocfilehash: 434bf1f6a5a727a71592493b85ab166cbeff2f0980c2c968c99973a03f4dc660
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751258"
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
3. I fanen **Datakanal** i **Parameter**-feltgruppen velger du **Serveradresse** og angir leverandøren av e-postkontoen.
4. Velg **Serverport** og angi porten som brukes av e-postkontoleverandøren.
5. Velg **Brukernavnhemmelighet** og angi navnet på nøkkelhvelvhemmeligheten som inneholder ID-en til e-postbrukerkontoen.
6. Velg **Brukerpassordhemmelighet** og angi navnet på nøkkelhvelvhemmeligheten som inneholder passordet til e-postbrukerkontoen.
7. Velg **Emnefilter**. Gå gjennom og oppdater strengen som inneholder standard e-postemne for å identifisere e-postmeldingen som inneholder den elektroniske leverandørfakturaen som skal importeres.
8. Gå gjennom og oppdater kriteriene i kategorien **Relevansregler** om nødvendig. Hvis du vil ha mer informasjon, kan du se [Relevansregler](e-invoicing-configuration-rcs.md#applicability-rules).
9. Velg **Lagre** og lukk siden.

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

## <a name="set-up-vendor-invoice-import-in-finance-and-supply-chain-management"></a>Konfigurer leverandørfakturaimport i Finance og Supply Chain Management
Fullfør trinnene i de følgende to delene for å definere ulike typer import av leverandørfakturaer.

### <a name="import-vendor-invoices-from-email"></a>Importer leverandørfakturaer fra e-post

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
2. Velg **Kontekstmodell for kundefaktura** og opprett en avledet konfigurasjon.
3. Velg **Utforming** i **Utkast**-versjonen.
4. Velg **Kundefaktura** i **datamodelltreet**, og velg deretter **Tilordne modell til datakilde**.
5. Velg **CustomerInvoice** i **Definisjoner**-treet, og velg deretter **Utforming**.
6. I **Datakilder**-treet velger du **Context\_Channel**. Velg **PEPPOL** i **Verdi**-feltet. Dette er navnet på kanalen som er angitt i konfigurasjonen av datakanalen for funksjonen for elektronisk fakturering i RCS. 
7. Velg **Lagre** og lukk siden.
8. Lukk siden.
9. Velg **Kontekstmodell for kundefaktura**, og velg **Endre status** > **Fullført** i hurtigfanen **Versjoner**.
10. Gå til **Organisasjonsadministrasjon** > **Oppsett** > **Elektroniske dokumentparametere**, og kontroller at du har valgt **PEPPOL globale elektroniske fakturaene** på fanen **Funksjoner**. 
11. Velg **Legg til** i fanen **Eksterne kanaler** på feltgruppen **Kanaler**.
12. I **Kanal**-feltet angir **PEPPOL**. Angi en beskrivelse i **Beskrivelse**-feltet.
13. Velg den juridiske enheten i **Firma**-feltet. I feltet **Dokumentkontekst** velger du **Kundefakturakontekst – kontekstmodell for kundefaktura**.
14. Velg **Lagre** og lukk deretter siden.


## <a name="receive-electronic-invoices"></a>Motta elektroniske fakturaer
Følg denne fremgangsmåten for å motta elektroniske fakturaer:

1. Gå til **Organisasjonsstyring** > **Periodiske** > **Elektroniske dokumenter** > **Motta elektroniske dokumenter**.
2. Velg **OK** og lukk deretter siden.

## <a name="view-receive-logs-for-electronic-invoices"></a>Vis mottakslogger for elektroniske fakturaer

Hvis du vil vise mottaksloggene for elektroniske fakturaer, kan du gå til **Organisasjonsadministrasjon** > **Periodisk** > **Elektroniske dokumenter** > **Mottakslogg for elektronisk faktura**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
