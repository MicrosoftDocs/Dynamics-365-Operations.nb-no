---
title: "Utgåtte funksjoner"
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning.
author: sericks007
manager: AnnBe
ms.date: 07/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Platform, UnifiedOperations
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 6
ms.translationtype: HT
ms.sourcegitcommit: 404a6e767036542b0e6ccd84c2dd841d4a602b87
ms.openlocfilehash: 671210a8d69282864ca4188abd360eefa819ae72
ms.contentlocale: nb-no
ms.lasthandoff: 08/02/2017

---

# <a name="deprecated-features"></a>Utgåtte funksjoner

[!include[banner](../includes/banner.md)]

Dette emnet beskriver funksjonene som er fjernet, eller som er planlagt fjernet i fremtidige oppdateringer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

## <a name="features-that-have-been-deprecated-in-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update-with-platform-update-8"></a>Funksjoner som er foreldet i oppdateringen for juli 2017 av Dynamics 365 for Finance and Operations, Enterprise edition med plattformoppdatering 8

### <a name="warehouse-mobile-devices-portal"></a>Portal for lagermobilenheter

Portal for lagermobilenheter (WMDP) var en frittstående komponent som var beregnet for selvdrevet lokal distribusjon. Denne komponenten støttes ikke lenger i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Et innebygd program som gir en bedre brukeropplevelse, erstatter funksjonaliteten til WMDP. 

|                                  |                                                 |
|----------------------------------|-------------------------------------------------|
| **Årsak til avskrivning**       | Duplikat funksjonalitet.                        |
| **Erstattet med en annen funksjon?** | Ja. Denne funksjonen er erstattet med Finance and Operations - Warehousing. Hvis du vil ha mer informasjon om oppsett og forutsetninger, se [Installere og konfigurere Microsoft Dynamics 365 for Finange and Operations – Warehousing](/dynamics365/unified-operations/supply-chain/warehousing/install-configure-warehousing-app). |
| **Berørte moduler**             | Lagerstyring, transportstyring |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Avansert bankavstemming, samsvarsregel for manuelt samsvar

En samsvarsregele ble brukt til å velge og merke et bankdokument når dokumenter ble avstemt manuelt i avstemmingsregnearket.

|                                  |                                                                                        |
|----------------------------------|----------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Begrenset bruk.                                                                         |
| **Erstattet med en annen funksjon?** | Nr. Kolonnefiltrering skal brukes til å finne dokumenter for avstemming. |
| **Berørte moduler**             | Kontant- og bankbehandling                                                               |

### <a name="windows-8-tablet-app"></a>Windows 8 nettbrettapp

Windows 8 nettbrettapp inneholdt funksjonalitet for utgiftsregistrering og -godkjenning.

|                                  |                                                                                          |
|----------------------------------|------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Finance and Operations er kompatibel med nettbrett. Nettbrettappen er ikke lenger nødvendig. |
| **Erstattet med en annen funksjon?** | Nr.                                                                                      |
| **Berørte moduler**             | Reiseregning og utlegg                                                                       |


## <a name="features-that-have-been-deprecated-in-dynamics-365-for-operations-1611-with-platform-update-3"></a>Funksjoner som er avskrevet i Dynamics 365 for Operations 1611 i plattformoppdatering 3

### <a name="aeb-payment-formats-for-spain"></a>AEB-betalingsformatene for Spania

Betalingsformatene Consejo Superior Bancario brukes til å sende remitteringsfiler til banken for kunde- og leverandørbetalinger. Innholdet i disse formatene bestemmes av Asociación Española de Banca. Den dekker Cuaderno 19, 32, 58, 34.

|                              |                                                                          |
|------------------------------|--------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Betalingsformatene brukes ikke lenger.                                  |
| **Erstattet med en annen funksjon?** | Ja, ISO20022-kredittoverføring og avtalegirobetalingsformater for Spania |
| **Berørte moduler**             | Leverandør, kunde                                    |

### <a name="bank-payments-transfer-for-lithuania"></a>Bankbetalingsoverføringer for Litauen

Bankbetalingsoverføringer genereres og skrives ut ved hjelp av eksportformatet for betalingsoverføring (LT) for Litauen. Det litauiske markedet begynte å bruke LITAS, det samordnede elektroniske banksystemet i 2005.

|                              |                                                            |
|------------------------------|------------------------------------------------------------|
| **Årsak til avskrivning**       | Betalingsformatene brukes ikke lenger.                    |
| **Erstattet med en annen funksjon?** | Ja, ISO20022 Betalingsformat for kredittoverføring for Litauen |
| **Berørte moduler**             | Leverandører                                           |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>BBS Direkte Remittering betalingsformatene for Norge

BBS Direkte Remittering betalingsformatene omfatter eksport av purring på kundebetaling (avtalegiro) og import av returmelding.

|                              |                                                                                                                                                                |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Betalingsformatene brukes ikke lenger.                                                                                                                        |
| **Erstattet med en annen funksjon?** | Format for AvtaleGiro-kundebetaling for Norge kan brukes til å generere meldinger for AvtaleGiro. Importer av returmelding vil bli implementert i fremtidige versjoner. |
| **Berørte moduler**             | Leverandør, kunde                                                                                                                          |

### <a name="chart-of-accounts-tool-for-spain"></a>Verktøy for kontoplan for Spania

Dette verktøyet brukes når en kontoplan i Spania krever store endringer. Brukere kan importere en ny kontoplan i Microsoft Excel- eller tekstformat, og kan også importere regnskapsoppgjør.

|                              |                |
|------------------------------|----------------|
| **Årsak til avskrivning**       | Begrenset bruk  |
| **Erstattet med en annen funksjon?** | Ingen             |
| **Berørte moduler**             | Økonomimodul |

### <a name="dom80-payment-format-for-belgium"></a>Dom80-betalingsformat for Belgia

Eldre Belgisk betalingsformat for purring (avtalegiro).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Årsak til avskrivning**      | Betalingsformatet brukes ikke lenger.                  |
| **Erstattet med en annen funksjon?** | Ja, ISO 20022 Avtalegiroformat for Belgia |
| **Berørte moduler**            | Kundereskontro                                    |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG-betalingsformatene for Sveits

DTA/EZAG-formatene er integrert i ESR-systemet fordi de kan inneholde referansenummeret. Referansenummeret er ikke obligatorisk, og derfor kan disse formatene brukes til å behandle alle leverandørbetalinger. Disse formatene brukes av firmaer som har en bankkonto på et annet sted enn "Postfinance".

|                              |                                                              |
|------------------------------|--------------------------------------------------------------|
| **Årsak til avskrivning**       | Betalingsformatene brukes ikke lenger.                      |
| **Erstattet med en annen funksjon?** | Ja, ISO20022 Betalingsformat for kredittoverføring for Sveits |
| **Berørte moduler**             | Leverandører                                             |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>EDIFACT-DIRDEB-betalingsformat for Østerrike

EDIFACT-DIRDEB-betalingsformat for purring (avtalegiro).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Årsak til avskrivning**       | Betalingsformatet brukes ikke lenger.                  |
| **Erstattet med en annen funksjon?** | Ja, ISO 20022 Avtalegiroformat for Østerrike |
| **Berørte moduler**             | Kundereskontro                                    |

### <a name="edivat-for-belgium"></a>EDIVAT for Belgia

EDIVAT er en foreldet belgisk standard for elektronisk deklarering via sikker e-post. Microsoft Dynamics AX 2012 beholder den skrivebeskyttede løsningen for å få tilgang til den historiske dataene.

|                              |                                      |
|------------------------------|--------------------------------------|
| **Årsak til avskrivning**       | Funksjonaliteten brukes ikke lenger. |
| **Erstattet med en annen funksjon?** | Ingen                                   |
| **Berørte moduler**             | Økonomimodul                       |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>eGiro EDIFACT CREMUL-betalingsimportformatet for Norge

eGiro er basert på den internasjonale UN EDIFACT CREMUL-standarden (Multiple Credit Advice Message) som brukes ved automatisk postering av kundebetalinger. eGiro er implementert som et formater for import av kundebetaling i Microsoft Dynamics AX.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Betalingsformatet brukes ikke lenger.                                                     |
| **Erstattet med en annen funksjon?** | Nr. Formatet vil bli erstattet av ISO 20022-importformater for utdrag i fremtidige versjoner. |
| **Berørte moduler**             | Kundereskontro                                                                       |

### <a name="external-inventory-for-poland"></a>Eksternt lager for Polen

Bevis for varer som er hentet fra en salgsleverandør uten innkjøp. Varer som håndteres i eksternt lager, som ikke påvirker standardlager og kan selges og deretter kjøpes automatisk. Denne prosessen oppretter reelle lagerbevegelser.

|                              |                                                 |
|------------------------------|-------------------------------------------------|
| **Årsak til avskrivning**       | Erstattet med en annen funksjon                     |
| **Erstattet med en annen funksjon?** | Ja, kjernefunksjonaliteten Inngående forsendelse |
| **Berørte moduler**             | Leverandører, lagerstyring          |

### <a name="financial-reports-generator-for-eastern-europe"></a>Generator for finansrapporter for Øst-Europa

Et verktøy brukes for å konfigurere datainnsamling for regnskaps- og avgiftsrapporter og eksportere data til XLS- og DOC-rapportmaler.

|                              |                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Begrenset bruk                                                                            |
| **Erstattet med en annen funksjon?** | Nr. Verktøyet vil bli erstattet av elektroniske rapporteringskonfigurasjoner i fremtidige versjoner. |
| **Berørte moduler**             | Økonomi                                                                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Import av kundebetalingstransaksjoner for Finland

Du kan velge et importformat for finske betalinger for å importere kundebetalingstransaksjoner fra en ekstern fil som banken leverer.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Betalingsformatet brukes ikke lenger.                                                     |
| **Erstattet med en annen funksjon?** | Nr. Formatet vil bli erstattet av ISO 20022-importformater for utdrag i fremtidige versjoner. |
| **Berørte moduler**             | Kundereskontro                                                                       |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Import av betalingstransaksjoner i en finansjournal for Finland

Et format som er spesifikk for Finland, som brukes for å importere regnskapstransaksjoner til økonomimodulen.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Betalingsformatet brukes ikke lenger.                                                     |
| **Erstattet med en annen funksjon?** | Nr. Formatet vil bli erstattet av ISO 20022-importformater for utdrag i fremtidige versjoner. |
| **Berørte moduler**             | Kundereskontro                                                                       |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Integrasjon med Isabel-synkronisert (CIS) for Belgia

Isabel er rammeverket for elektroniske banktjenester i Europa og de facto standard i Belgia.

|                              |                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Integrasjon med Isabel-klienten er avsluttet.                                                                |
| **Erstattet med en annen funksjon?** | Nr. Betalingsformatene som brukes ikke lenger brukes erstattes av ISO20022 Betalingsformat for kredittoverføring for Belgia. |
| **Berørte moduler**             | Leverandører                                                                                                     |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Endringer i kontoplanen og regnskapsreglene for Spania

Denne funksjonen brukes til endringer i kontoplanen og regnskapsreglene i Spania. Den tilordner kontoer for å gjøre bidra til overføring av den gamle kontoplanen til den nye kontoplanen, og sammenligner det forrige regnskapsåret med det nye regnskapsåret, selv om de ble postert til ulike kontonumre.

|                              |                |
|------------------------------|----------------|
| **Årsak til avskrivning**       | Begrenset bruk  |
| **Erstattet med en annen funksjon?** | Ingen             |
| **Berørte moduler**             | Økonomimodul |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Pagamento Fornittori-betalingsformatet for leverandør

Eldre italiensk betalingsformat for kredittoverføringer.

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Årsak til avskrivning**       | Betalingsformatet brukes ikke lenger.                  |
| **Erstattet med en annen funksjon?** | Ja, ISO20022 Betalingsformat for kredittoverføring for Italia |
| **Berørte moduler**             | Leverandører                                       |

### <a name="payment-export-formats-for-estonia"></a>Eksportformater for betaling for Estland.

Formatene Telehansa og Teleservice brukes for eksport for bankbetaling.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Årsak til avskrivning**      | Betalingsformatene brukes ikke lenger.                  |
| **Erstattet med en annen funksjon?** | Ja, ISO20022 Betalingsformat for kredittoverføring for Estland |
| **Berørte moduler**             | Leverandører                                         |

### <a name="payment-file-archive-for-norway"></a>Betalingsfilarkiv for Norge

Når betalingsfiler genereres, arkiverer filarkivet automatisk alle filene som opprettes, også filer som tidligere ble skrevet eller lest.

|                              |                                                                    |
|------------------------------|--------------------------------------------------------------------|
| **Årsak til avskrivning**       | Erstattet med en annen funksjon                                        |
| **Erstattet med en annen funksjon?** | Ja, arkiverte jobber for elektronisk rapportering                            |
| **Berørte moduler**             | Leverandører, kunder, organisasjonsstyring |

### <a name="payment-import-formats-for-estonia"></a>Importformater for betaling for Estland

Formatene Telehansa og TeleTeenus brukes for import for bankbetaling.

|                              |                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Betalingsformatene brukes ikke lenger.                                                    |
| **Erstattet med en annen funksjon?** | Nr. Formatene vil bli erstattet av ISO 20022-importformater for utdrag i fremtidige versjoner. |
| **Berørte moduler**             | Kundereskontro                                                                        |

### <a name="performance-management-goal-workflow"></a>Arbeidsflyt for mål for ytelsesstyring

Ytelsesstyring omfatter målstyring og integrasjon med ytelsesvurderinger.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Ytelsesstyring ble endret, og antall målsider ble redusert for å forenkle prosessen.                 |
| **Erstattet med en annen funksjon?** | Nr. Mål er synlige for lederselvbetjeningsportalen, og endres og vises av lederen. |
| **Berørte moduler**             | Forvaltning av menneskelig kapital                                                                                                 |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Postgirot og Postgirot Utland-betalingsformatene for Sverige

Postgirot og Postgirot Utland-betalingsformatene for Sverige.

|                              |                                                         |
|------------------------------|---------------------------------------------------------|
| **Årsak til avskrivning**       | Betalingsformatene brukes ikke lenger.                 |
| **Erstattet med en annen funksjon?** | Ja, ISO20022 Betalingsformat for kredittoverføring for Sverige |
| **Berørte moduler**             | Leverandører                                        |

### <a name="radio-frequency-identifier"></a>Radiofrekvensidentifisering

Radiofrekvensidentifisering (RFID) er en datainnsamlingsteknikk som bruker elektroniske brikker til å lagre identifiseringsdata. Innhenting av data krever ikke at leseren må være der brikkene er.

|                              |                                               |
|------------------------------|-----------------------------------------------|
| **Årsak til avskrivning**       | Lav kundebruk og begrenset funksjonssett. |
| **Erstattet med en annen funksjon?** | Ingen                                            |
| **Berørte moduler**             | Lagerstyring                          |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Rapport om fakturanummerering for delstat for Latvia

Latvisk lovgivning angir bestemte regler for nummerering av salgsfakturaer. Funksjonen lar deg tilordne bestemte numre til salgsfakturaer, basert på brukeren eller brukergruppen. Deretter kan du generere en rapport eller en XML-fil. Du kan også skrive ut en rapport om fakturanumre som er brukt.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Fakturanummerering for delstat trenger ikke lenger å vedlikeholdes. Rapport om brukte fakturanumre er ikke lenger nødvendig. |
| **Erstattet med en annen funksjon?** | Ingen                                                                                                                       |
| **Berørte moduler**             | Kundereskontro                                                                                                      |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Definer navnene på lederen og en generelle regnskapsføreren for et firma for Litauen

Navnet på lederen og den generell regnskapsføreren for et firma kan angis i firmainformasjonen og brukes i forskjellige utskrifter av lokale rapporter.

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| **Årsak til avskrivning**       | Erstattet med en annen funksjon                                     |
| **Erstattet med en annen funksjon?** | Ja, oppsettet av kontrollører kan brukes til det samme formålet.   |
| **Berørte moduler**             | Leverandører, Kundereskontro, Kontant- og bankbehandling |

### <a name="telepay-payment-formats-for-norway"></a>TelePay-betalingsformatene for Norge

TelePay-betalingsformatene omfatter eksportformater for leverandør (kredittoverføring) og purring på kundebetaling (avtalegiro).

|                              |                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Betalingsformatene brukes ikke lenger.                                                        |
| **Erstattet med en annen funksjon?** | Ja, ISO20022 Betalingsformat for kredittoverføring og Format for AvtaleGiro-kundebetaling for Norge |
| **Berørte moduler**            | Leverandør, kunde                                                          |

### <a name="vendor-payment-export-formats-for-finland"></a>Eksportformater for leverandørbetaling for Finland

Det finnes to formater for eksport av betalinger for Finland. LM02 (FI) brukes for innenlandsbetalinger, og LUM2 (FI) brukes for utenlandsbetalinger.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Årsak til avskrivning**       | Betalingsformatene brukes ikke lenger.                  |
| **Erstattet med en annen funksjon?** | Ja, ISO20022 Betalingsformat for kredittoverføring for Finland |
| **Berørte moduler**            | Leverandører                                         |

### <a name="workflow-for-creating-goals"></a>Arbeidsflyt for å opprette mål

En arbeidsflyt for behandling av opprettelsen av ansattes mål er en av flere arbeidsflyter som var tilgjengelige for å koordinere ytelsesstyringsprosessen.

|                              |                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Ytelsesstyring er utformet på nytt i Microsoft Dynamics 365 for Finance and Operations.                                                                                                                                                                                                                                        |
| **Erstattet med en annen funksjon?** | Den nyutformede funksjonen for ytelsesstyring gir større kontroll over innholdet i målene, målene som brukes til å spore fremdrift og vedlegg av støttedokumentasjon. Mål kan lagres som maler og deretter brukes på nytt. Denne funksjonen kan hjelpe deg med å konfigurere flere mål for ansatte raskere. |
| **Berørte moduler**            | Forvaltning av menneskelig kapital                                                                                                                                                                                                                                                                                                               |

## <a name="features-that-have-been-deprecated-in-dynamics-ax-70-releases"></a>Funksjoner som er avskrevet i Dynamics AX 7.0-versjoner

### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Muligheten til å avbryte endringer i en leverandørfaktura

|                              |                         |
|------------------------------|-------------------------|
| **Årsak til avskrivning**       | Ytelsesforbedring |
| **Erstattet med en annen funksjon?** | Antall                      |
| **Berørte moduler**            | Leverandører        |

### <a name="aif-axd-and-axbc-integrations"></a>AIF-, AxD- og AxBC-integreringer

I Application Integration Framework (AIF) kan data utveksles med eksterne systemer gjennom forretningslogikk som vises som tjenester. Dynamics AX inneholder tjenestene som er basert på dokumenter og .NET Business Connector (AxBC). Et dokument opprettes ved hjelp av XML. XML-en inneholder hodeinformasjon som legges til for å opprette en *meldingen* som kan overføres til eller fra Dynamics AX. Eksempler på dokumenter er salgsordrer og bestillinger. Nesten enhver enhet, for eksempel en kunde, kan imidlertid representeres av et dokument. Tjenester som er basert på dokumenter, bruker **Axd &lt;*Dokument*&gt;**-klasser.

|                              |                                                                                                                                                                                                          |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Arkitekturen i AIF- og AxD-dokumenter kan ikke skaleres til en skytjeneste. Det oppstod ytelsesproblemer rundt masseimport.                                                                               |
| **Erstattet med en annen funksjon?** | I den gjeldende versjonen av Dynamics AX erstattes denne funksjonen av rammeverk for dataimport-/eksport, som støtter regelmessig bulkimport/-eksport. For AxBC anbefaler vi at du bruker de faktiske tabellene. |
| **Berørte moduler**             | AxD-er, AxBC-er og AIF                                                                                                                                                                                     |

### <a name="boms-without-bom-versions"></a>Stykklister uten stykklisteversjoner

Når konfigurasjonsnøkkelen **Stykklisteversjoner** ble deaktivert, ble stykklisteversjonene skjult i alle skjemaer, og systemet fremtvang en 1:1-relasjon mellom frigitte produkter og stykklister. I gjeldende versjon av Dynamics AX kan ikke **Stykklisteversjoner**-konfigurasjonsnøkkelen deaktiveres.

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| **Årsak til avskrivning**      | Bruk av en konfigurasjonsnøkkel for å styre stykklisteversjoner kan ikke skaleres i et skymiljø. |
| **Erstattet med en annen funksjon?** | Antall                                                                                      |
| **Berørte moduler**            | Behandling av produktinformasjon, Lagerstyring                                    |

### <a name="brazilian-bordero"></a>Brasiliansk Bordero

Spesifikk betalingsmåte for brasilianske firmaer

|                              |                                                                                                       |
|------------------------------|-------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Støtte for den brasilianske Bordero-metoden for betalingsmåte er fjernet fra brasiliansk lokalisering |
| **Erstattet med en annen funksjon?** | Ingen                                                                                                    |
| **Berørte moduler**             | Leverandører                                                                                      |

### <a name="brazilian-sintegra-statement"></a>Brasiliansk Sintegra-utdrag

Utdrag for føderal skatt for ICMS-avgift

|                              |                                                                                                                       |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Dette utdraget gjelder ikke lenger i enkelte delstater i Brasil.                                                     |
| **Erstattet med en annen funksjon?** | Nr. Brukere kan bruke det generelle elektroniske rapporteringsverktøyet for å konfigurere utdraget hvis det er nødvendig i bestemte situasjoner. |
| **Berørte moduler**             | Regnskapsbøker                                                                                                          |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brasiliansk SCAN-eventualitetsmodus for NF-e

(SCAN)-eventualitetsmiljø brukes til å generere, eksportere og importere statusen for en Nota Fiscal eletrônica (NF-e) når miljøet for Secretaria da Fazenda (SEFAZ) ikke er tilgjengelig.

|                              |                                                                             |
|------------------------------|-----------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Denne eventualitetsmetoden er ikke lenger tilgjengelig i alle delstater i Brasil |
| **Erstattet med en annen funksjon?** | Ingen                                                                          |
| **Berørte moduler**             | Kundereskontro                                                         |

### <a name="business-analyzer"></a>Business Analyzer

Denne mobilapplikasjonen lar brukere se gjennom viktige forretningsdata.

|                              |                                                                                                                                                               |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Funksjonen har blitt erstattet med en annen funksjon.                                                                                                      |
| **Erstattet med en annen funksjon?** | Innholdspakken Overvåk økonomiske resultater for Microsoft Power BI inneholder nøkkelmetrikk for økonomi som tidligere var tilgjengelig i verktøyet Business Analyzer. |
| **Berørte moduler**             | Økonomimodul                                                                                                                                                |

### <a name="business-statistics"></a>Forretningsstatistikk

Oppsett av forretningsstatistikkforespørsler som kan hjelpe deg med å analysere ytelsen til organisasjonen

|                              |                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Foreldet tilnærming til forretningsanalyse (BI), lav kundebruk og begrenset funksjonssett |
| **Erstattet med en annen funksjon?** | Nye BI-løsninger for den gjeldende versjonen av Dynamics AX                                      |
| **Berørte moduler**             | Innkjøp og leverandører, Leverandører, Salg og markedsføring, Kunder         |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Endre datofunksjonen for dokumentet i fakturagodkjenningsjournalen

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Liten bruk                                                               |
| **Erstattet med en annen funksjon?** | Ja. Du kan endre dokumentdatoen på den posterte leverandørtransaksjonen. |
| **Berørte moduler**             | Leverandører                                                        |

### <a name="clieop03-payment-format-for-the-netherlands"></a>ClieOp03-betalingsformat for Nederland

|                              |                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Formatet er ikke lenger i bruk i Nederland fordi det er erstattet av SEPA-funksjonaliteten. |
| **Erstattet med en annen funksjon?** | SEPA-betalingseksport                                                                                       |
| **Berørte moduler**             | Alle                                                                                                        |

### <a name="compliance-center"></a>Overholdelsessenter

Overholdelsessenteret var et Enterprise Portal-område for administrasjon av kravene til dokumentasjon til samsvar som er knyttet til Sarbanes-Oxley-loven.

|                              |                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Mangel på kundebruk. Microsoft SharePoint inkluderer samme funksjon som var tilgjengelig i overholdelsessenteret. |
| **Erstattet med en annen funksjon?** | Antall                                                                                                                     |
| **Berørte moduler**             | Samsvar og interne kontroller                                                                                       |

### <a name="connector-for-microsoft-dynamics"></a>Connector for Microsoft Dynamics

Dette verktøyet ble brukt til å integrere viktige data fra Microsoft Dynamics CRM til Microsoft Dynamics ERP-programmer.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Årsak til avskrivning**       | Funksjonen har blitt erstattet med en annen funksjon. |
| **Erstattet med en annen funksjon?** | Dynamics-integrator                                      |
| **Berørte moduler**             | Connector for Microsoft Dynamics                         |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Containerenhet og fysisk beholdning av flere dimensjoner

|                              |                                                                                                                                                                 |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Duplikat funksjonalitet                                                                                                                                         |
| **Erstattet med en annen funksjon?** | Ja. Denne funksjonaliteten er erstattet med funksjonssettet for konsolidert partiordre etter AX 2012. Dette funksjonssettet inneholder den konsoliderte beholdningen. |
| **Berørte moduler**             | Behandling av produktinformasjon, Produksjonskontroll, Lagerstyring, Salg og markedsføring                                                                   |

### <a name="cue-group-metadata"></a>Bunkegruppemetadata

|                              |                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Bunkegrupper ble brukt til å vise én eller flere bunker i faktaboksområdet. Det var begrenset opptak, og det var også ytelsesproblemer fordi en postendring i et overordnet skjema forårsaket én spørring per bunke i bunkegruppen. |
| **Erstattet med en annen funksjon?** | Antall                                                                                                                                                                                                                            |
| **Berørte moduler**             | Alle                                                                                                                                                                                                                           |

### <a name="cue-metadata"></a>Bunkemetadata

|                              |                                                                                                                                                                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Bunkemetadata er begrenset til antall- eller suminformasjon.                                                                                                                                                                                   |
| **Erstattet med en annen funksjon?** | Side-ved-side-metadataene ble innført for å gi mer fleksibilitet for modellering. Du kan for eksempel opprette gjeldende antall, navigasjon og nøkkelytelsesindikatorer (KPI-er). Side-ved-side-metadata er direkte erstatning av bunkemetadata. |
| **Berørte moduler**             | Alle                                                                                                                                                                                                                                     |

### <a name="danish-check-format"></a>Dansk sjekkformat

|                              |                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Støtte for dansk sjekkformatoppsett er avsluttet, og rapporten har blitt fjernet fra DK-lokalisering. |
| **Erstattet med en annen funksjon?** | Antall                                                                                                                      |
| **Berørte moduler**             | Alle                                                                                                                     |

### <a name="data-partitions"></a>Datapartisjoner

Datapartisjoner gir en logisk separasjon av data i Microsoft Dynamics AX-databasen.

|   |   |
|---|---|
| **Årsak til avskrivning**       | Datapartisjoner ble introdusert i Microsoft Dynamics AX 2012 R2 for å gjøre det mulig å isolere data. I et vanlig scenario har et firmaet datterselskaper, og data fra ett av datterselskapene skal ikke være synlig for et annet datterselskap, selv om begge datterselskaper håndteres av samme IT-avdelingen. Ekstra skript og administrasjon i hele programmet var imidlertid nødvendig for å opprette nye partisjoner og fylle dem med data, og for å sikkerhetskopiere partisjonsdata. I skyen, der vi har tilgang til databasetjenester for plattform som en tjeneste (PaaS) (Microsoft Azure SQL-Database), er det mye mer effektivt å bruke en database som isolasjonsbeholder enn å utføre isolasjon i programmet. Uavhengig av om partisjonering av data er nødvendig for datterselskaper, for flere leiere, eller bare for skala, mener vi at situasjonene kan håndteres bedre gjennom flere databaser eller flere Dynamics AX-forekomster. |
| **Erstattet med en annen funksjon?** | Datapartisjoner erstattes gjennom støtte for flere databaser eller Dynamics AX-forekomster i en fremtidig versjon.    |
| **Berørte moduler**             | Alle  |

### <a name="database-and-file-share-storage-for-attachments"></a>Database og fildelingslagring for vedlegg
Microsoft Dynamics AX 2012 tillot lagring av vedlegg i databasen og delte filer. Ingen av disse alternativene støttes lenger.

|                              |                                        |
|------------------------------|----------------------------------------|
| **Årsak til avskrivning**       | Lagring av delte filer støttes ikke lenger fordi skyvertmiljøer ikke kan kommunisere med lokale delte filer. Databaselagring er avviklet til fordel for Azure Blob-lagring. Azure Blob-lagring tilsvarer lagring i databasen, siden dokumenter kan bare åpnes med Dynamics 365 for Finance and Operations-klientskjemaer. Dette gir fordelen med å gi lagring som ikke har en negativ innvirkning på ytelsen til databasen. Blob-lagring er standard lagringsmekanisme for dokumentbehandling og fungerer umiddelbart. |
| **Erstattet med en annen funksjon?** | Databaselagring er avviklet til fordel for Azure Blob-lagring.       |
| **Berørte moduler**             | Alle                   |

### <a name="delimitation"></a>Avgrensing

|                              |                                        |
|------------------------------|----------------------------------------|
| **Årsak til avskrivning**       | Finner ingen bruk av funksjonen. |
| **Erstattet med en annen funksjon?** | Antall                                     |
| **Berørte moduler**             | Timeregistrering                    |

### <a name="desktop-client"></a>Skrivebordsklient

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Dynamics AX-klientopplevelsen har fått ny utforming for å forbedre brukervennligheten på tvers av plattformer og enheter.                      |
| **Erstattet med en annen funksjon?** | Den nye webklienten er basert på skrivebordskjemametadataene og programmeringsmodellen som har blitt endret for å gi en rik webplattform. |
| **Berørte moduler**             | Alle                                                                                                                                    |

### <a name="direct-database-connection"></a>Direkte databasetilkobling

I Dynamics AX 2012 R3 kan Retail Modern POS kobles direkte til kanaldatabasen på samme måte som Enterprise POS. Dette var i tillegg til standard kommunikasjonsmetode for Retail Modern POS-kommunikasjon via detaljhandelsserver.  

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Direkte databasetilkobling krevde protokoller med lavere sikkerhet, og ble hovedsakelig brukt til å oppnå den høyeste ytelsen. På grunn av ytelses- og sikkerhetsforbedringene som er utført i Finance and Operations, fører denne funksjonen nå til flere problemer enn den løser. |
| **Erstattet med en annen funksjon?** | Nr. Nå støttes bare standard kommunikasjon for detaljhandelsserver.    |
| **Berørte moduler**             | Kanaldatabase/Retail Modern POS                                    |

### <a name="dutch-swift-mt940"></a>Nederlandsk SWIFT MT940

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Generisk funksjonalitet brukes nå i stedet for lokalisert funksjonalitet.                                                                                                                                                                 |
| **Erstattet med en annen funksjon?** | Ja, denne funksjonaliteten er erstattet av funksjonalitet for avanserte bankavstemming. |
| **Berørte moduler**             | Alle                                                                                                                                                                                                                                   |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL for Tyskland)

Denne funksjonaliteten leverte XBRL-utdata (eXtensible Business Reporting Language) som er beregnet spesifikt for den tyske eBilanz-taksonomien.

|                              |                                                                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Mangel på kundebruk                                                                                                                                                 |
| **Erstattet med en annen funksjon?** | Denne funksjonen er ikke erstattet av en annen funksjon, men flere spesialiserte XBRL-pakker som gir rik XBRL-funksjonalitet, er tilgjengelige for det tyske markedet. |
| **Berørte moduler**             | Management Reporter                                                                                                                                                    |

### <a name="enterprise-portal-client"></a>Enterprise Portal-klient

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | En enkelt klient plattform er levert.                                                                                            |
| **Erstattet med en annen funksjon?** | Den nye webklienten er basert på skrivebordskjemametadataene og programmeringsmodellen som har blitt endret for å gi en rik webplattform. |
| **Berørte moduler**             | Alle                                                                                                                                    |

### <a name="environmental-sustainability"></a>Miljømessig bærekraft

|                              |                                                    |
|------------------------------|----------------------------------------------------|
| **Årsak til avskrivning**       | Lav kundebruk og begrenset funksjonssett       |
| **Erstattet med en annen funksjon?** | Antall                                                 |
| **Berørte moduler**             | Samsvar og interne kontroller, leverandører |

### <a name="form-activex-and-managed-host-controls"></a>Lage ActiveX- og administrerte vertskontroller

|                              |                                                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | ActiveX-kontrollene og de administrerte vertskontrollene er basert på den avskrevne skrivebordsklienten.                                                                                                             |
| **Erstattet med en annen funksjon?** | Det utvidbare kontrollrammeverket støtter bygging av nye kontroller som er basert på HTML, CSS og JavaScript, og er en førsteklasses kontroll i Microsoft Visual Studio-verktøymiljøet. |
| **Berørte moduler**             | Alle                                                                                                                                                                                           |

### <a name="generate-prenotes-by-using-a-batch"></a>Generer forhåndsmerknader ved hjelp av et parti

Generering av forhåndsmerknad kan ikke kan utføres ved hjelp av et parti, men kan fremdeles utføres av en bruker.

|                              |                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Det finnes ikke noe skjema for å beholde og vise den resulterende forhåndsmerknadsfilen når den blir generert ved hjelp av et parti. |
| **Erstattet med en annen funksjon?** | Forhåndsmerknader kan fremdeles genereres, og brukeren har kontroll over plasseringen der filen skal lagres.   |
| **Berørte moduler**             | Leverandører, Kundereskontro, Kontant- og bankbehandling                                        |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Tysk DTAUS-betalingseksport og kontoutdragsimport (totaler og transaksjoner)

|                              |                                                                                                                                                                                                                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Formatet er ikke lenger i bruk i Tyskland fordi det er erstattet av SEPA-funksjonaliteten (felles eurobetalingsområde).                                                                                                                                                                 |
| **Erstattet med en annen funksjon?** | Ja, denne funksjonaliteten er erstattet av SEPA-betalingseksport og avanserte funksjoner for bankavstemming for import av kontoutdrag. |
| **Berørte moduler**             | Alle                                                                                                                                                                                                                                                                                            |

### <a name="german-dtazv-payment-format"></a>Tysk DTAZV-betalingsformat

|                              |                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Formatet er ikke lenger i bruk i Tyskland fordi det er erstattet av SEPA-funksjonaliteten. |
| **Erstattet med en annen funksjon?** | SEPA-betalingseksport                                                                               |
| **Berørte moduler**             | Alle                                                                                                |

### <a name="german-mt940-import"></a>Tysk MT940-import

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Generisk funksjonalitet brukes nå i stedet for lokalisert funksjonalitet.                                                                                                                                                                 |
| **Erstattet med en annen funksjon?** | Ja, denne funksjonaliteten er erstattet av funksjonalitet for avanserte bankavstemming. |
| **Berørte moduler**             | Alle                                                                                                                                                                                                                                   |

### <a name="german-xml-eu-sales-list"></a>Tysk EU-salgsliste i XML

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | XML-format for rapportering av tysk EU-salgsliste støttes ikke lenger. Bare ELMA5-tekstfilformatet kan brukes til å sende rapportering av EU-salgsliste til det tyske skattekontoret. |
| **Erstattet med en annen funksjon?** | Antall                                                                                                                                                                                 |
| **Berørte moduler**             | Avgift                                                                                                                                                                                |

### <a name="gl-ssrs-reports"></a>GL SSRS-rapporter

Rapporter som inkluderer følgende menyelementer, er fjernet: **Råbalansesammendrag**, **Detaljert råbalanse**, **Kontoplan**, **Revisjonsspor**, **Saldoer** og **Saldoliste**.

|                              |                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | SSRS-rapporter (Microsoft SQL Server Reporting Services) er erstattet med Management Reporter-funksjoner og standardrapporter. |
| **Erstattet med en annen funksjon?** | Management Reporter (kalt **Finansrapportering** i den gjeldende versjonen av Dynamics AX)                                                  |
| **Berørte moduler**            | Økonomimodul                                                                                                                               |

### <a name="infopart-and-formpart-metadata"></a>InfoPart- og FormPart-metadata

|                              |                                                                                                                                                                                                                                |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | InfoPart- og FormPart-metadata aktiverte opprettelsen av faktabokser for to forskjellige klienter.                                                                                                                                    |
| **Erstattet med en annen funksjon?** | InfoPart-metadata, som var en forenklet skjemadefinisjon, konverteres til et skjema ved hjelp av oppgraderingsverktøy. Metadata for FormPart, som refererer til et skjema, erstattes av en mer direkte referanse som opprettes av oppgraderingsverktøy. |
| **Berørte moduler**             | Alle                                                                                                                                                                                                                            |

### <a name="main-account-list-page"></a>Listeside for hovedkonto

En liste over kontoer for den juridiske enheten og tilknyttet saldoinformasjon

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Saldoinformasjon er tilgjengelig på listesiden **Råbalanse** etter konto og dimensjon.                                                                                      |
| **Erstattet med en annen funksjon?** | **Hovedkontoer** inneholder den samme listen over kontoer som listesiden **Hovedkonto** inneholdt. Rutenettvisningen i **Hovedkontoer** viser også en enda mindre rutenettlignende visning. |
| **Berørte moduler**             | Økonomimodul                                                                                                                                                                     |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malaysia og Singapore bankkontantstrømrapport

Denne funksjonen gjør det mulig for brukeren å skrive ut en kontantstrømrapport som viser transaksjoner og detaljer om inn- og utkontantstrømmene for et valgt datoområde for valgte bankkontoer.

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Den samme informasjonen kan hentes fra forespørselsbanktransaksjonen. |
| **Erstattet med en annen funksjon?** | Forespørselbanktransaksjonen                                            |
| **Berørte moduler**             | Kontant- og bankbehandling                                                |

### <a name="mexican-cfd-electronic-invoice"></a>Meksikansk CFD elektronisk faktura

Denne funksjonen aktiverte genereringen av meksikanske elektroniske fakturaer ved hjelp av CFD-metoden (Comprobante Fiscal Digital), der firmaet signerer fakturaen ved å be om relaterte godkjenning fra myndighetene. Denne funksjonen gir også en månedlig rapport som inneholder alle elektroniske fakturaer som ble utstedt i perioden.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Metoden er ikke lenger gjeldende. Generering av elektroniske fakturaer ved hjelp av metoden CFD ble avskrevet av skattemyndighetene og erstattet med CFDI-metoden (Comprobante Fiscal Digital a través de Internet), der signeringen delegeres til tredjepartsleverandøren (PAC). Den månedlige rapporten er fjernet, og et forespørselsalternativ lar brukerne be om historiske transaksjoner. |
| **Erstattet med en annen funksjon?** | Antall                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Berørte moduler**             | Kunder, Prosjekt                                                                                                                                                                                                                                                                                                                                                                              |

### <a name="mexico-realized-and-unrealized-vat"></a>Mexico realisert og urealisert mva

Microsoft Dynamics AX 2012 administrerte urealisert merverdiavgift (mva) ved å bruke Mexico-spesifikk funksjonalitet for "urealisert mva".

|                              |                                                                                                                     |
|------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Duplikat funksjonalitet                                                                                             |
| **Erstattet med en annen funksjon?** | Ja, denne funksjonen er erstattet med standard betinget mva-funksjonaliteten som tilbys av Core. |
| **Berørte moduler**             | Avgift                                                                                                                 |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook-integrering

|                              |                                                                                |
|------------------------------|--------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Denne funksjonaliteten er erstattet av Microsoft Exchange Server-integrering. |
| **Erstattet med en annen funksjon?** | Ja                                                                            |
| **Berørte moduler**             | Salg og markedsføring                                                            |

### <a name="payroll-information-in-human-resources"></a>Lønnsinformasjon i Personale

Lønnsinformasjon i Personale

|                              |                                                                                                                                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Denne funksjonaliteten er erstattet av kjernesider for Lønn og Personale.                                                                                                                                                                                                                                              |
| **Erstattet med en annen funksjon?** | **Fordeler**, **Inntekter** og andre tilknyttede sider som tidligere var i US Payroll, er konfigurert på nytt og er nå en del av kjerneinstallasjonen av Personale for å støtte ekstern lønnsbehandling. Denne funksjonaliteten er tilgjengelig ved å bruke **Personale 1** &gt; **Lønn**-konfigurasjonsnøkkelen. |
| **Berørte moduler**             | Personale, Lønn                                                                                                                                                                                                                                                                                                     |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Privat blokkering av lager- og lagerstyringsjournaler

Lager- og lagerstyringsjournaler støtter ikke lenger muligheten til å merke en journal som privat for en valgt bruker. Bare prosessen med å blokkere journaler som privat for brukergrupper og blokkering under redigering støttes.

|                              |                                        |
|------------------------------|----------------------------------------|
| **Årsak til avskrivning**       | Finner ingen bruk av funksjonen. |
| **Erstattet med en annen funksjon?** | Antall                                     |
| **Berørte moduler**             | Lagerstyring                   |

### <a name="product-builder"></a>Produktkonfigurator

Produktkonfigurator ble brukt til å konfigurere varer dynamisk fra en salgsordre, en bestilling, en produksjonsordre, et salgstilbud, et prosjekttilbud eller et varebehov. Basert på en produktmodell som hadde modelleringsvariabler, kan brukeren velge verdier for å imøtekomme kundekravene og få en unik produktvariant som hadde en stykkliste og rute.

|                              |                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Produktkonfigurator viste X ++-kode til sluttbrukere og støttes ikke i den gjeldende versjonen av Dynamics AX. Den er fjernet for å unngå dupliserte vedlikeholdsforsøk på overlappende, skalerbare kodebaser. |
| **Erstattet med en annen funksjon?** | Produktkonfigurasjon                                                                                                                                                                                   |
| **Berørte moduler**             | Behandling av produktinformasjon, salg og markedsføring                                                                                                                                                     |

### <a name="rename-product-dimension"></a>Gi nytt navn til produktdimensjon

Med denne funksjonen kan du endre navnet på en av de tre standard produktdimensjonene (størrelse, farge eller stil) til et navn som passer bedre til dine forretningsbehov. Navneendring inkluderte alle etikettene der produktdimensjonsnavnet ble brukt.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Den gjeldende versjonen av Dynamics AX støtter ikke etikettendringer under kjøring. |
| **Erstattet med en annen funksjon?** | Ingen                                                                            |
| **Berørte moduler**             | Behandling av produktinformasjon                                                |

### <a name="retail-server-connectivity-using-http"></a>Tilkobling til detaljhandelsserver med HTTP

I Dynamics AX 2012 R3 kunne detaljhandelsserveren fungerer ved hjelp av HTTP-kommunikasjon (ikke sikret). Dette var i tillegg til standardkommunikasjonen med HTTPS.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | På grunn av nye sikkerhetskrav støttes nå bare sikret kommunikasjon ved hjelp av TLS 1.2 (eller høyere, hvis tilgjengelig). Det selvbetjente installasjonsprogrammet konfigurerer automatisk datamaskinen for denne kommunikasjonen. |
| **Erstattet med en annen funksjon?** | Nr. Nå støttes bare standard HTTPS-kommunikasjon.                                                                           |
| **Berørte moduler**             | Detaljhandelsserver                                                |

### <a name="role-center-pages"></a>Rollesentersider

|                              |                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Rollesentersider ble bygd på den avskrevne Enterprise Portal-plattformen, som er erstattet med den nye webklientplattformen i den gjeldende versjonen av Dynamics AX. |
| **Erstattet med en annen funksjon?** | Det nye arbeidsområdeskjemamønsteret gir brukerne en prosessentrert design som gir enkel tilgang til ofte brukte oppgaver i denne prosessen.                       |
| **Berørte moduler**             | Alle                                                                                                                                                                      |

### <a name="sales-tax-jurisdictions"></a>Mva-jurisdiksjoner

|                              |                                              |
|------------------------------|----------------------------------------------|
| **Årsak til avskrivning**       | Lav kundebruk og begrenset funksjonssett |
| **Erstattet med en annen funksjon?** | Antall                                           |
| **Berørte moduler**             | Amerikansk merverdiavgift                                 |

### <a name="shipping-carrier-interface"></a>Transportørgrensesnitt

|                              |                                                                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Duplikat funksjonalitet                                                                                                                         |
| **Erstattet med en annen funksjon?** | Ja, denne funksjonen er delvis erstattet med Transportstyring, men er ennå ikke erstattet med grunnleggende Lagerstyring (WMS I). |
| **Berørte moduler**             | Salg og markedsføring, Lagerstyring                                                                                                       |

### <a name="sites-services"></a>Sites Services

Sites Services lar deg bygge webområder som utvider forretningsprosesser til Internett uten IT-støtte.

|                              |                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Microsoft Azure-infrastrukturen som brukes av Dynamics AX, har nye funksjoner som kan brukes i stedet (for eksempel Azure-områder). |
| **Erstattet med en annen funksjon?** | Antall                                                                                                                                       |
| **Berørte moduler**             | Personalerekruttering, saksbehandling, forespørsel om tilbud, leverandørregistrering                                                                  |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS, strategi for behovsprognose

|                              |                                                                              |
|------------------------------|------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Utformingen av funksjonen støttes ikke i den nye skyarkitekturen. |
| **Erstattet med en annen funksjon?** | Azure Machine Learning, strategi for behovsprognose                           |
| **Berørte moduler**             | Planlegging                                                                     |

### <a name="travel-requisitions"></a>Reiserekvisisjoner

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| **Årsak til avskrivning**       | Liten bruk, og de fleste funksjonene fantes i Enterprise Portal. |
| **Erstattet med en annen funksjon?** | Antall                                                              |
| **Berørte moduler**             | Reiseregning og utlegg                                              |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Leverandørfakturapulje uten posteringsdetaljer

|                              |                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Liten bruk. Denne funksjonaliteten er erstattet av fakturajournalen med funksjonaliteten for arbeidsflyten. |
| **Erstattet med en annen funksjon?** | Arbeidsflytfunksjoner til fakturajournalen.                                                           |
| **Berørte moduler**             | Leverandører                                                                                        |

### <a name="virtual-company-accounts"></a>Virtuelle firmakontoer

Virtuelle firmaer-funksjonen støttes ikke lenger i Dynamics AX. Virtuelle firmaer-funksjonen lar brukere definere tabeller som kan deles av et sett med firmaer. Hvis du vil ha en beskrivelse av funksjonen, kan du se [Firmakontoer og virtuelle firmakontoer](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). Funksjonen fungerer ved å gruppere tabeller i samlinger som tilordnes til virtuelle firmaer, som er grupper av eksisterende "virkelige" firmaer. Spørringer opprettes slik at alle selskaper i det virtuelle firmaet kan få tilgang til dataene i tabellene til de tilknyttede tabellsamlingene.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><b>Årsak til avskrivning</b></td>
<td><ul>
<li>Virtuelle firmaer må defineres før data lagres i tabellene. Retrotilpasning av virtuelle firmaer på en eksisterende implementering er veldig vanskelig.</li>
<li>Fordi det har vært så mye datanormalisering i den gjeldende versjonen av Microsoft Dynamics AX, har det blitt vanskelig å vite hva du skal legge til i tabellsamlinger. Det er for eksempel vanskelig å vite hvilke tabeller som skal deles. Alle tabellene det refereres til fra tabeller som er i et virtuelt firma, må også legges til. På grunn av tabellnormalisering må selv enkle hoveddata som er spredt over flere tabeller, være en del av det virtuelle firmaet. Eventuelle feil som gjøres her, vil forårsake funksjonsproblemer.</li>
<li>Når en tabell er en del av et virtuelt firma, mister den informasjon om opprinnelsen til dataene, og bare det virtuelle firmaet registreres.</li>
</ul></td>
</tr>
<tr class="even">
<td><b>Erstattet med en annen funksjon?</b></td>
<td>Globale tabeller kan brukes til å lage tabeller som er tilgjengelige fra alle firmaer. Det er for øyeblikket ingen erstatning.</td>
</tr>
<tr class="odd">
<td><b>Berørte moduler</b></td>
<td>Gjelder ikke her</td>
</tr>
</tbody>
</table>

### <a name="warehouse-management-ii"></a>Lagerstyring II

|                              |                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Lagerstyring II-løsningen (WMS II) som var tilgjengelig i **Lagerstyring**-modulen, dupliserer funksjonaliteten i **Lagerstyring**-modulen som ble lansert i Microsoft Dynamics AX 2012 R3.                                                                         |
| **Erstattet med en annen funksjon?** | **Lagerstyring**-modulen som ble lansert i AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8 og Dynamics AX 2012 R3 CU9, erstatter Lagerstyring II-funksjonene. Den nye modulen har mer avanserte funksjoner og mer fleksible lagerstyringsprosesser enn i Lagerstyring II. |
| **Berørte moduler**             | Lagerstyring, salg og markedsføring, innkjøp og leverandører                                                                                                                                                                                                                                         |

### <a name="worker-reminders-in-human-resources"></a>Arbeiderpåminnelser i Personale

Lønnsinformasjon i Personale

|                              |                 |
|------------------------------|-----------------|
| **Årsak til avskrivning**       | Liten bruk       |
| **Erstattet med en annen funksjon?** | Antall              |
| **Berørte moduler**             | Personale |

### <a name="workplanner"></a>Jobbplanlegger

|                              |                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Liten bruk                                                                                                                                                            |
| **Erstattet med en annen funksjon?** | Nei, men **Profilrelasjon**-siden som åpnes fra **Profilgrupper**-siden, støtter samme forretningsscenario som den avskrevne **Jobbplanlegger**-siden. |
| **Berørte moduler**             | Timeregistrering                                                                                                                                                  |

### <a name="x-financial-statements"></a>X++-regnskapsoppgjør

|                              |                                                                                             |
|------------------------------|---------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Funksjonen har blitt erstattet med en annen funksjon.                                    |
| **Erstattet med en annen funksjon?** | Management Reporter (kalt **Finansrapportering** i den gjeldende versjonen av Dynamics AX) |
| **Berørte moduler**             | Økonomimodul                                                                              |


