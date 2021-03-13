---
title: Komme i gang med tillegget Elektronisk fakturering
description: Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med tillegget Elektronisk fakturering i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 07954c5c96f390bc651794f8b6c61f2a1a17ab8b
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111226"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Komme i gang med tillegget Elektronisk fakturering

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med tillegget Elektronisk fakturering.

Tabellen nedenfor viser funksjonene for elektronisk fakturering og forretningsdokumentene de kan brukes på.

| Funksjonsnavn                         | Forretningsdokument |
|--------------------------------------|-------------------|
| Østerrikske elektroniske fakturaer (AT)    | <p>Salgsfaktura</p><p>Prosjektfaktura</p> |
| Belgisk elektronisk faktura (BE)      | <p>Salgsfaktura</p><p>Prosjektfaktura</p> |
| Brasiliansk NF-e (BR)                  | <p>Regnskapsdokumentmodell 55</p><p>Korreksjonsbrev</p> |
| Brasiliansk NFS-e ABRASF Curitiba (BR) | Skattedokument for tjeneste |
| Brasiliansk NFS-e São Paulo (BR)       | Skattedokument for tjeneste |
| Dansk elektronisk faktura (DK)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> |
| Egyptisk elektronisk faktura (EG)     | <p>Salgsfaktura</p><p>Prosjektfaktura</p> |
| Estisk elektronisk faktura (EE)     | <p>Salgsfaktura</p><p>Prosjektfaktura</p> |
| Finsk elektronisk faktura (FI)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> |
| Fransk elektronisk faktura (FR)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> |
| Tysk elektronisk faktura (DE)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> |
| FatturaPA (IT)                       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> |
| Meksikansk CFDI Interfactura (MX)       | <p>Salgsfaktura</p><p>Følgeseddel</p><p>Lageroverføring</p><p>Betalingstillegg</p> |
| Nederlandsk elektronisk faktura (NL)        | <p>Salgsfaktura</p><p>Prosjektfaktura</p> |
| Norsk elektronisk faktura (NO)    | <p>Salgsfaktura</p><p>Prosjektfaktura</p> |
| Spansk elektronisk faktura (ES)      | <p>Salgsfaktura</p><p>Prosjektfaktura</p> |
| Elektronisk faktura i PEPPOL-format            | <p>Salgsfaktura</p><p>Prosjektfaktura</p> |

## <a name="prerequisites"></a>Forutsetninger

Før du kan fullføre trinnene i dette emnet må følgende forutsetninger være på plass:

- Konfigurer Regulatory Configuration Service (RCS) og Microsoft Dynamics 365 Finance- eller Dynamics 365 Supply Chain Management-miljøet, slik at du kan sende til tillegget for elektronisk fakturering.
- Opprett et servicemiljø, og publiser det i tillegget for elektronisk fakturering. Hvis du vil ha mer informasjon, kan du se [Komme i gang med tjenesteadministrasjon for tillegget for elektronisk fakturering](e-invoicing-get-started-service-administration.md).
- Opprett et tilkoblet program. Hvis du vil ha mer informasjon, kan du se [Komme i gang med tjenesteadministrasjon for tillegget for elektronisk fakturering](e-invoicing-get-started-service-administration.md).
- Opprett en konfigurasjonsleverandør for organisasjonen. Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Importere en funksjon for elektronisk fakturering fra Microsoft-konfigurasjonsleverandøren 

1. Logg deg på kontoen for Regulatory Configuration Service (RCS).
2. I **Globaliseringsfunksjon**-arbeidsområder i delen **Funksjoner**, velger du flisen **E-fakturering**.
3. Velg **Importer**, og velg deretter **Synkroniser**.
4. Filtrer **Konfigurasjonsleverandør**-kolonnen etter termen **Microsoft**.
5. Velg navnet på en funksjon for elektronisk fakturering fra tabellen i begynnelsen av dette emnet, og velg deretter **Importer**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Opprette en funksjon for Elektronisk fakturering under organisasjonsleverandøren

1. I RCS, i delen **Funksjoner** i arbeidsområdet **Globaliseringsfunksjon**, velger du flisen **E-fakturering**.
2. Velg **Legg til** > **Basert på eksisterende funksjon**, og i feltet **Navn** angir du navnet på funksjonen for Elektronisk fakturering.
3. I **Beskrivelse**-feltet skriver du inn en beskrivelse av funksjonen.
4. I **Basefunksjonsfeltet** velger du den importerte funksjonen for elektronisk fakturering fra Microsofts konfigurasjonsleverandør.
5. Velg **Opprett funksjon**.

## <a name="configure-the-electronic-invoicing-feature"></a>Konfigurere funksjonene for Elektronisk fakturering

Avhengig av landet eller området kan det hende at funksjonen for Elektronisk fakturering krever tilleggskonfigurasjon. Hvis du vil ha mer informasjon om disse trinnene, kan du se i "Komme i gang"-dokumentasjonen som er tilgjengelig for landet eller området ditt.

## <a name="configure-the-application-setup"></a>Konfigurere programoppsettet

1. Velg funksjonen for Elektronisk fakturering som du opprettet.
2. I kategorien **Versjon** kontrollerer du at versjonen **Utkast** er valgt.
3. Velg **Programoppsett** i kategorien **Oppsett**.

    > [!NOTE]
    > Kontroller at organisasjonen er angitt som **Aktiv** konfigurasjonsleverandør. Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive.](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

4. Velg **Funksjonsoppsett**, og velg deretter **Tilkoblet program**.
5. I delen **Elektroniske dokumenttyper** velger du **Legg til**.
6. For hvert forretningsdokument som funksjonen støtter, velger og angir du en **Tabellnavn**-verdi i henhold til følgende tabell.

    | Funksjonsnavn                         | Forretningsdokument | Tabellnavn |
    |--------------------------------------|-------------------|------------|
    | Østerrikske elektroniske fakturaer (AT)    | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Belgisk elektronisk faktura (BE)      | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Brasiliansk NF-e (BR)                  | <p>Regnskapsdokument</p><p>Korreksjonsbrev</p> | Regnskapsdokument |
    | Brasiliansk NFS-e ABRASF Curitiba (BR) | Skattedokument for tjeneste | Regnskapsdokument |
    | Brasiliansk NFS-e São Paulo (BR)       | Skattedokument for tjeneste | Regnskapsdokument |
    | Dansk elektronisk faktura (DK)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Egyptisk elektronisk faktura (EG)     | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Estisk elektronisk faktura (EE)     | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Finsk elektronisk faktura (FI)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Fransk elektronisk faktura (FR)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Tysk elektronisk faktura (DE)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | FatturaPA (IT)                       | <p>Salgsfaktura</p><p>Prosjektfaktura | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Meksikansk CFDI Interfactura (MX)       | <p>Salgsfaktura</p><p>Følgeseddel</p><p>Lageroverføring</p><p>Betalingstillegg</p> | Kundefakturajournal |
    | Nederlandsk elektronisk faktura (NL)        | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Norsk elektronisk faktura (NO)    | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Spansk elektronisk faktura (ES)      | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |
    | Elektronisk faktura i PEPPOL-format            | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kundefakturajournal</p><p>Prosjektfaktura</p> |

7. For hvert forretningsdokument som funksjonen støtter, velger og angir du en **Kontekst**-verdi i henhold til følgende tabell.

    | Funksjonsnavn                         | Forretningsdokument | Kontekst |
    |--------------------------------------|-------------------|---------|
    | Østerrikske elektroniske fakturaer (AT)    | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Belgisk elektronisk faktura (BE)      | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Brasiliansk NF-e (BR)                  | <p>Regnskapsdokument</p><p>Korreksjonsbrev</p> | <p>Kontekstmodell for kundefaktura – regnskapsdokumentkontekst</p><p>Kontekstmodell for kundefaktura – FD-korreksjonsbrevkontekst</p> |
    | Brasiliansk NFS-e ABRASF Curitiba (BR) | Skattedokument for tjeneste| Kontekstmodell for kundefaktura – regnskapsdokumentkontekst |
    | Brasiliansk NFS-e São Paulo (BR)       | Skattedokument for tjeneste| Kontekstmodell for kundefaktura – regnskapsdokumentkontekst |
    | Dansk elektronisk faktura (DK)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Egyptisk elektronisk faktura (EG)     | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Estisk elektronisk faktura (EE)     | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Finsk elektronisk faktura (FI)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Fransk elektronisk faktura (FR)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Tysk elektronisk faktura (DE)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | FatturaPA (IT)                       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Meksikansk CFDI Interfactura (MX)       | <p>Salgsfaktura</p><p>Følgeseddel</p><p>Lageroverføring</p><p>Betalingstillegg</p> | Kontekstmodell for kundefaktura – kundefakturakontekst |
    | Nederlandsk elektronisk faktura (NL)        | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Norsk elektronisk faktura (NO)    | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Spansk elektronisk faktura (ES)      | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |
    | Elektronisk faktura i PEPPOL-format            | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Kontekstmodell for kundefaktura – kundefakturakontekst</p><p>Kontekstmodell for kundefaktura – projektfakturakontekst</p> |

8. For hvert forretningsdokument som funksjonen støtter, velger og angir du en **Forretningsdokumenttilordning**-verdi i henhold til følgende tabell.

    | Funksjonsnavn                         | Forretningsdokument | Tilordning av forretningsdokument |
    |--------------------------------------|-------------------|---------------------------|
    | Østerrikske elektroniske fakturaer (AT)    | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Belgisk elektronisk faktura (BE)      | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Brasiliansk NF-e (BR)                  | <p>Regnskapsdokument</p><p>Korreksjonsbrev</p> | <p>Regnskapsdokumenttilordning – regnskapsdokumenttilordning</p><p>Regnskapsdokumenttilordning – korreksjonsbrevtilordning</p> |
    | Brasiliansk NFS-e ABRASF Curitiba (BR) | Skattedokument for tjeneste | Regnskapsdokumenttilordning – regnskapsdokumenttilordning |
    | Brasiliansk NFS-e São Paulo (BR)       | Skattedokument for tjeneste | Regnskapsdokumenttilordning – regnskapsdokumenttilordning |
    | Dansk elektronisk faktura (DK)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Egyptisk elektronisk faktura (EG)     | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Estisk elektronisk faktura (EE)     | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Finsk elektronisk faktura (FI)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Fransk elektronisk faktura (FR)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Tysk elektronisk faktura (DE)       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | FatturaPA (IT)                       | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Meksikansk CFDI Interfactura (MX)       | <p>Salgsfaktura</p><p>Følgeseddel</p><p>Lageroverføring</p><p>Betalingstillegg</p> | Fakturamodelltilordning – kundefaktura |
    | Nederlandsk elektronisk faktura (NL)        | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Norsk elektronisk faktura (NO)    | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Spansk elektronisk faktura (ES)      | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |
    | Elektronisk faktura i PEPPOL-format            | <p>Salgsfaktura</p><p>Prosjektfaktura</p> | <p>Fakturamodelltilordning – kundefaktura</p><p>Fakturamodelltilordning – prosjektfaktura</p> |

Avhengig av landet eller området kan det hende at funksjonen for Elektronisk fakturering krever tilleggskonfigurasjon. Hvis du vil ha mer informasjon om disse trinnene, kan du se i "Komme i gang"-dokumentasjonen som er tilgjengelig for landet eller området ditt.

## <a name="deploy-the-electronic-invoicing-feature"></a>Distribuere funksjonene for Elektronisk fakturering

1. Velg versjonen av funksjonen for Elektronisk fakturering du vil distribuere, i kategorien **Versjoner**.
2. Velg **Endre status** \> **Fullført**.
3. Velg **Endre status** \> **Publiser**.
4. Velg **Distribuer**.
5. Sett alternativet **Distribuer til tilkoblet program** til **Ja**.
6. Velg tilkoblingen som er knyttet til forekomsten av Finance eller Supply Chain Management på siden **Koble til program**.
7. Sett alternativet **Distribuer til servicemiljø** til **Ja**.
8. I feltet **Servicemiljø** velger du servicemiljøet for tillegget Elektronisk fakturering der du vil distribuere funksjonen for Elektronisk fakturering.
9. I **Fra dato**-feltet velger du datoen da funksjonen for Elektronisk fakturering må bli gyldig i tillegget for Elektronisk fakturering.
10. Velg **OK**.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>Slå på funksjonen for Elektronisk fakturering i Finance eller Supply Chain Management

1. Logg deg på Finans eller Supply Chain Management, og kontroller at du er i riktig juridisk enhet.
2. Gå til **Organisasjonsstyring** \> **Oppsett** \> **Parametere for elektronisk dokument**.
3. I kategorien **Funksjoner** velger du funksjonsreferansen eller -referansene som vises i tabellen nedenfor, for å aktivere funksjonen for Elektronisk fakturering for Finans eller Supply Chain Management.

    | Funksjonsnavn                         | Land/område  | Funksjonsreferanse |
    |--------------------------------------|-----------------|-------------------|
    | Østerrikske elektroniske fakturaer (AT)    | Østerrike         | EUR-00023 |
    | Belgisk elektronisk faktura (BE)      | Belgia         | EUR-00023 |
    | Brasiliansk NF-e (BR)                  | Brasil          | BR-00053 |
    | Brasiliansk NFS-e ABRASF Curitiba (BR) | Brasil          | BR-00095 |
    | Brasiliansk NFS-e São Paulo (BR)       | Brasil          | BR-00095 |
    | Dansk elektronisk faktura (DK)       | Danmark         | <p>EUR-00023</p><p>DK-00001</p> |
    | Nederlandsk elektronisk faktura (NL)        | Nederland | EUR-00023 |
    | Egyptisk elektronisk faktura (EG)     | Egypt           | EG-00008 |
    | Estisk elektronisk faktura (EE)     | Estland         | EUR-00023 |
    | Finsk elektronisk faktura (FI)      | Finland         | EUR-00023 |
     Fransk elektronisk faktura (FR)       | Frankrike           | EUR-00023 |
    | Tysk elektronisk faktura (DE)       | Tyskland         | EUR-00023 |
    | Meksikansk CFDI Interfactura (MX)       | Mexico          | <p>MX-00010</p><p>MX-00016</p> |
    | Norsk elektronisk faktura (NO)    | Norge          | <p>EUR-00023</p><p>NO-00010</p> |
    | Spansk elektronisk faktura (ES)      | Spania           | <p>EUR-00023</p><p>ES-00025</p> |
    | Italiensk elektronisk faktura (IT)      | Italia           | <p>EUR-00023</p><p>IT-00036</p> |
    | Elektronisk faktura i PEPPOL-format            | Europa          | EUR-00023 |

4. Velg **Lagre**.

## <a name="issue-electronic-invoices"></a>Utstede elektroniske fakturaer

1. Gå til **Organisasjonsstyring** \> **Periodiske** \> **Elektroniske dokumenter** \> **Send elektroniske dokumenter**.
2. Velg **Filtrer** i hurtigfanen **Post som skal inkluderes** .
3. Velg **Legg til** for å legge til et tabellnavn i spørringsfilteret.
4. Velg tabellen som inneholder fakturaene.

    > [!NOTE]
    > Tabellnavnet må vises i tabellen i delen [Konfigurere programoppsettet](#configure-the-application-setup) tidligere i dette emnet.

5. Velg feltnavnet fra tabellen du vil spørre.
6. Angi tabellnavnet og feltnavnet for kriteriene du skal spørre på.
7. Gjenta trinn 5 og 6 hvis du vil legge til flere felt og kriterier i spørringen, og velg deretter **OK**.
8. Velg **OK**.

## <a name="view-submission-logs"></a>Vise sendelogger

1. Gå til **Organisasjonsstyring** \> **Periodisk** \> **Elektroniske dokumenter** \> **Sendingslogg for elektronisk dokument**.
2. Velg tabellen som inneholder fakturaene, i **Dokumenttype**-feltet.

    > [!NOTE]
    > Tabellnavnet må vises i tabellen i delen [Konfigurere programoppsettet](#configure-the-application-setup) tidligere i dette emnet.

3. Velg en faktura i rutenettet, og velg deretter **Forespørsel om** \> **Innsendingsdetaljer**.

Avhengig av landet eller området kan det hende at funksjonen for Elektronisk fakturering krever tilleggskonfigurasjon. Hvis du vil ha mer informasjon om disse trinnene, kan du se i "Komme i gang"-dokumentasjonen som er tilgjengelig for landet eller området ditt.

## <a name="related-topics"></a>Relaterte emner

- [Oversikt over tillegg for elektronisk fakturering](e-invoicing-service-overview.md)
- [Komme i gang med tillegget Elektronisk fakturering for Brasil](e-invoicing-bra-get-started.md)
- [Komme i gang med tillegget Elektronisk fakturering for Mexico](e-invoicing-mex-get-started.md)
- [Komme i gang med tillegget Elektronisk fakturering for Italia](e-invoicing-ita-get-started.md)
- [Elektroniske fakturaer for kunde i Egypt](emea-egy-e-invoices.md)
