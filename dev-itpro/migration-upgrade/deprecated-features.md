---
title: "Utgåtte funksjoner"
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning.
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Platform
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 6
ms.translationtype: Human Translation
ms.sourcegitcommit: 3267bd1cbd738b5ced9996fc3b28eee211627591
ms.openlocfilehash: 8feffb27b5d08a9c90e97ac0d7e00abf0448d0df
ms.contentlocale: nb-no
ms.lasthandoff: 06/16/2017


---

# Utgåtte funksjoner
<a id="deprecated-features" class="xliff"></a>

[!include[banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning.

## Funksjoner som er foreldet i oppdateringen for juli 2017 av Dynamics 365 for Finance and Operations, Enterprise edition
<a id="features-that-have-been-deprecated-in-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update" class="xliff"></a>

### Portal for lagermobilenheter
<a id="warehouse-mobile-devices-portal" class="xliff"></a>

Portal for lagermobilenheter (WMDP) var en frittstående komponent som var beregnet for selvdrevet lokal distribusjon. Denne komponenten støttes ikke lenger i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Et innebygd program som gir en bedre brukeropplevelse, erstatter funksjonaliteten til WMDP. 

|                                  |                                                 |
|----------------------------------|-------------------------------------------------|
| **Årsak til avskrivning**       | Duplikat funksjonalitet.                        |
| **Erstattet med en annen funksjon?** | Ja. Denne funksjonen er erstattet med Finance and Operations - Warehousing. Hvis du vil ha mer informasjon om oppsett og forutsetninger, se [Installere og konfigurere Microsoft Dynamics 365 for Finange and Operations – Warehousing](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/install-configure-warehousing-app). |
| **Berørte moduler**             | Lagerstyring, transportstyring |

### Avansert bankavstemming, samsvarsregel for manuelt samsvar
<a id="advanced-bank-reconciliation-matching-rule-for-manual-matching" class="xliff"></a>

En samsvarsregele ble brukt til å velge og merke et bankdokument når dokumenter ble avstemt manuelt i avstemmingsregnearket.

|                                  |                                                                                        |
|----------------------------------|----------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Begrenset bruk.                                                                         |
| **Erstattet med en annen funksjon?** | Nr. Kolonnefiltrering skal brukes til å finne dokumenter for avstemming. |
| **Berørte moduler**             | Kontant- og bankbehandling                                                               |

### Windows 8 nettbrettapp
<a id="windows-8-tablet-app" class="xliff"></a>

Windows 8 nettbrettapp inneholdt funksjonalitet for utgiftsregistrering og -godkjenning.

|                                  |                                                                                          |
|----------------------------------|------------------------------------------------------------------------------------------|
| **Årsak til avskrivning**       | Finance and Operations er kompatibel med nettbrett. Nettbrettappen er ikke lenger nødvendig. |
| **Erstattet med en annen funksjon?** | Nr.                                                                                      |
| **Berørte moduler**             | Reiseregning og utlegg                                                                       |


Funksjoner som er avskrevet i Dynamics 365 for Operations 1611 i plattformoppdatering 3
<a id="features-that-have-been-deprecated-in-dynamics-365-for-operations-1611-with-platform-update-3" class="xliff"></a>
---------------------------------------------------------------------------------------------

### AEB-betalingsformatene for Spania
<a id="aeb-payment-formats-for-spain" class="xliff"></a>

Betalingsformatene Consejo Superior Bancario brukes til å sende remitteringsfiler til banken for kunde- og leverandørbetalinger. Innholdet i disse formatene bestemmes av Asociación Española de Banca. Den dekker Cuaderno 19, 32, 58, 34.

|                              |                                                                          |
|------------------------------|--------------------------------------------------------------------------|
| Årsak til avskrivning       | Betalingsformatene brukes ikke lenger.                                  |
| Erstattet med en annen funksjon? | Ja, ISO20022-kredittoverføring og avtalegirobetalingsformater for Spania |
| Berørte moduler             | Leverandør, kunde                                    |

### Bankbetalingsoverføringer for Litauen
<a id="bank-payments-transfer-for-lithuania" class="xliff"></a>

Bankbetalingsoverføringer genereres og skrives ut ved hjelp av eksportformatet for betalingsoverføring (LT) for Litauen. Det litauiske markedet begynte å bruke LITAS, det samordnede elektroniske banksystemet i 2005.

|                              |                                                            |
|------------------------------|------------------------------------------------------------|
| Årsak til avskrivning       | Betalingsformatene brukes ikke lenger.                    |
| Erstattet med en annen funksjon? | Ja, ISO20022 Betalingsformat for kredittoverføring for Litauen |
| Berørte moduler             | Leverandører                                           |

### BBS Direkte Remittering betalingsformatene for Norge
<a id="bbs-direkte-remittering-payment-formats-for-norway" class="xliff"></a>

BBS Direkte Remittering betalingsformatene omfatter eksport av purring på kundebetaling (avtalegiro) og import av returmelding.

|                              |                                                                                                                                                                |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Betalingsformatene brukes ikke lenger.                                                                                                                        |
| Erstattet med en annen funksjon? | Format for AvtaleGiro-kundebetaling for Norge kan brukes til å generere meldinger for AvtaleGiro. Importer av returmelding vil bli implementert i fremtidige versjoner. |
| Berørte moduler             | Leverandør, kunde                                                                                                                          |

### Verktøy for kontoplan for Spania
<a id="chart-of-accounts-tool-for-spain" class="xliff"></a>

Dette verktøyet brukes når en kontoplan i Spania krever store endringer. Brukere kan importere en ny kontoplan i Microsoft Excel- eller tekstformat, og kan også importere regnskapsoppgjør.

|                              |                |
|------------------------------|----------------|
| Årsak til avskrivning       | Begrenset bruk  |
| Erstattet med en annen funksjon? | Ingen             |
| Berørte moduler             | Økonomimodul |

### Dom80-betalingsformat for Belgia
<a id="dom80-payment-format-for-belgium" class="xliff"></a>

Eldre Belgisk betalingsformat for purring (avtalegiro).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Årsak til avskrivning       | Betalingsformatet brukes ikke lenger.                  |
| Erstattet med en annen funksjon? | Ja, ISO 20022 Avtalegiroformat for Belgia |
| Berørte moduler             | Kundereskontro                                    |

### DTA/EZAG-betalingsformatene for Sveits
<a id="dtaezag-payment-formats-for-switzerland" class="xliff"></a>

DTA/EZAG-formatene er integrert i ESR-systemet fordi de kan inneholde referansenummeret. Referansenummeret er ikke obligatorisk, og derfor kan disse formatene brukes til å behandle alle leverandørbetalinger. Disse formatene brukes av firmaer som har en bankkonto på et annet sted enn "Postfinance".

|                              |                                                              |
|------------------------------|--------------------------------------------------------------|
| Årsak til avskrivning       | Betalingsformatene brukes ikke lenger.                      |
| Erstattet med en annen funksjon? | Ja, ISO20022 Betalingsformat for kredittoverføring for Sveits |
| Berørte moduler             | Leverandører                                             |

### EDIFACT-DIRDEB-betalingsformat for Østerrike
<a id="edifact-dirdeb-payment-format-for-austria" class="xliff"></a>

EDIFACT-DIRDEB-betalingsformat for purring (avtalegiro).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Årsak til avskrivning       | Betalingsformatet brukes ikke lenger.                  |
| Erstattet med en annen funksjon? | Ja, ISO 20022 Avtalegiroformat for Østerrike |
| Berørte moduler             | Kundereskontro                                    |

### EDIVAT for Belgia
<a id="edivat-for-belgium" class="xliff"></a>

EDIVAT er en foreldet belgisk standard for elektronisk deklarering via sikker e-post. Microsoft Dynamics AX 2012 beholder den skrivebeskyttede løsningen for å få tilgang til den historiske dataene.

|                              |                                      |
|------------------------------|--------------------------------------|
| Årsak til avskrivning       | Funksjonaliteten brukes ikke lenger. |
| Erstattet med en annen funksjon? | Ingen                                   |
| Berørte moduler             | Økonomimodul                       |

### eGiro EDIFACT CREMUL-betalingsimportformatet for Norge
<a id="egiro-edifact-cremul-payment-import-format-for-norway" class="xliff"></a>

eGiro er basert på den internasjonale UN EDIFACT CREMUL-standarden (Multiple Credit Advice Message) som brukes ved automatisk postering av kundebetalinger. eGiro er implementert som et formater for import av kundebetaling i Microsoft Dynamics AX.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Betalingsformatet brukes ikke lenger.                                                     |
| Erstattet med en annen funksjon? | Nr. Formatet vil bli erstattet av ISO 20022-importformater for utdrag i fremtidige versjoner. |
| Berørte moduler             | Kundereskontro                                                                       |

### Eksternt lager for Polen
<a id="external-inventory-for-poland" class="xliff"></a>

Bevis for varer som er hentet fra en salgsleverandør uten innkjøp. Varer som håndteres i eksternt lager, som ikke påvirker standardlager og kan selges og deretter kjøpes automatisk. Denne prosessen oppretter reelle lagerbevegelser.

|                              |                                                 |
|------------------------------|-------------------------------------------------|
| Årsak til avskrivning       | Erstattet med en annen funksjon                     |
| Erstattet med en annen funksjon? | Ja, kjernefunksjonaliteten Inngående forsendelse |
| Berørte moduler             | Leverandører, lagerstyring          |

### Generator for finansrapporter for Øst-Europa
<a id="financial-reports-generator-for-eastern-europe" class="xliff"></a>

Et verktøy brukes for å konfigurere datainnsamling for regnskaps- og avgiftsrapporter og eksportere data til XLS- og DOC-rapportmaler.

|                              |                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Begrenset bruk                                                                            |
| Erstattet med en annen funksjon? | Nr. Verktøyet vil bli erstattet av elektroniske rapporteringskonfigurasjoner i fremtidige versjoner. |
| Berørte moduler             | Økonomi                                                                           |

### Import av kundebetalingstransaksjoner for Finland
<a id="import-of-customer-payment-transactions-for-finland" class="xliff"></a>

Du kan velge et importformat for finske betalinger for å importere kundebetalingstransaksjoner fra en ekstern fil som banken leverer.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Betalingsformatet brukes ikke lenger.                                                     |
| Erstattet med en annen funksjon? | Nr. Formatet vil bli erstattet av ISO 20022-importformater for utdrag i fremtidige versjoner. |
| Berørte moduler             | Kundereskontro                                                                       |

### Import av betalingstransaksjoner i en finansjournal for Finland
<a id="import-of-payment-transactions-into-a-general-ledger-journal-for-finland" class="xliff"></a>

Et format som er spesifikk for Finland, som brukes for å importere regnskapstransaksjoner til økonomimodulen.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Betalingsformatet brukes ikke lenger.                                                     |
| Erstattet med en annen funksjon? | Nr. Formatet vil bli erstattet av ISO 20022-importformater for utdrag i fremtidige versjoner. |
| Berørte moduler             | Kundereskontro                                                                       |

### Integrasjon med Isabel-synkronisert (CIS) for Belgia
<a id="integration-with-isabel-synchronized-cis-for-belgium" class="xliff"></a>

Isabel er rammeverket for elektroniske banktjenester i Europa og de facto standard i Belgia.

|                              |                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Integrasjon med Isabel-klienten er avsluttet.                                                                |
| Erstattet med en annen funksjon? | Nr. Betalingsformatene som brukes ikke lenger brukes erstattes av ISO20022 Betalingsformat for kredittoverføring for Belgia. |
| Berørte moduler             | Leverandører                                                                                                     |

### Endringer i kontoplanen og regnskapsreglene for Spania
<a id="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain" class="xliff"></a>

Denne funksjonen brukes til endringer i kontoplanen og regnskapsreglene i Spania. Den tilordner kontoer for å gjøre bidra til overføring av den gamle kontoplanen til den nye kontoplanen, og sammenligner det forrige regnskapsåret med det nye regnskapsåret, selv om de ble postert til ulike kontonumre.

|                              |                |
|------------------------------|----------------|
| Årsak til avskrivning       | Begrenset bruk  |
| Erstattet med en annen funksjon? | Ingen             |
| Berørte moduler             | Økonomimodul |

### Pagamento Fornittori-betalingsformatet for leverandør
<a id="pagamento-fornittori-vendor-payment-format" class="xliff"></a>

Eldre italiensk betalingsformat for kredittoverføringer.

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Årsak til avskrivning       | Betalingsformatet brukes ikke lenger.                  |
| Erstattet med en annen funksjon? | Ja, ISO20022 Betalingsformat for kredittoverføring for Italia |
| Berørte moduler             | Leverandører                                       |

### Eksportformater for betaling for Estland.
<a id="payment-export-formats-for-estonia" class="xliff"></a>

Formatene Telehansa og Teleservice brukes for eksport for bankbetaling.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Årsak til avskrivning       | Betalingsformatene brukes ikke lenger.                  |
| Erstattet med en annen funksjon? | Ja, ISO20022 Betalingsformat for kredittoverføring for Estland |
| Berørte moduler             | Leverandører                                         |

### Betalingsfilarkiv for Norge
<a id="payment-file-archive-for-norway" class="xliff"></a>

Når betalingsfiler genereres, arkiverer filarkivet automatisk alle filene som opprettes, også filer som tidligere ble skrevet eller lest.

|                              |                                                                    |
|------------------------------|--------------------------------------------------------------------|
| Årsak til avskrivning       | Erstattet med en annen funksjon                                        |
| Erstattet med en annen funksjon? | Ja, arkiverte jobber for elektronisk rapportering                            |
| Berørte moduler             | Leverandører, kunder, organisasjonsstyring |

### Importformater for betaling for Estland
<a id="payment-import-formats-for-estonia" class="xliff"></a>

Formatene Telehansa og TeleTeenus brukes for import for bankbetaling.

|                              |                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Betalingsformatene brukes ikke lenger.                                                    |
| Erstattet med en annen funksjon? | Nr. Formatene vil bli erstattet av ISO 20022-importformater for utdrag i fremtidige versjoner. |
| Berørte moduler             | Kundereskontro                                                                        |

### Arbeidsflyt for mål for ytelsesstyring
<a id="performance-management-goal-workflow" class="xliff"></a>

Ytelsesstyring omfatter målstyring og integrasjon med ytelsesvurderinger.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Ytelsesstyring ble endret, og antall målsider ble redusert for å forenkle prosessen.                 |
| Erstattet med en annen funksjon? | Nr. Mål er synlige for lederselvbetjeningsportalen, og endres og vises av lederen. |
| Berørte moduler             | Forvaltning av menneskelig kapital                                                                                                 |

### Postgirot og Postgirot Utland-betalingsformatene for Sverige
<a id="postgirot-and-postgirot-utland-payment-formats-for-sweden" class="xliff"></a>

Postgirot og Postgirot Utland-betalingsformatene for Sverige.

|                              |                                                         |
|------------------------------|---------------------------------------------------------|
| Årsak til avskrivning       | Betalingsformatene brukes ikke lenger.                 |
| Erstattet med en annen funksjon? | Ja, ISO20022 Betalingsformat for kredittoverføring for Sverige |
| Berørte moduler             | Leverandører                                        |

### Radiofrekvensidentifisering
<a id="radio-frequency-identifier" class="xliff"></a>

Radiofrekvensidentifisering (RFID) er en datainnsamlingsteknikk som bruker elektroniske brikker til å lagre identifiseringsdata. Innhenting av data krever ikke at leseren må være der brikkene er.

|                              |                                               |
|------------------------------|-----------------------------------------------|
| Årsak til avskrivning       | Lav kundebruk og begrenset funksjonssett. |
| Erstattet med en annen funksjon? | Ingen                                            |
| Berørte moduler             | Lagerstyring                          |

### Rapport om fakturanummerering for delstat for Latvia
<a id="report-about-state-invoices-numbering-for-latvia" class="xliff"></a>

Latvisk lovgivning angir bestemte regler for nummerering av salgsfakturaer. Funksjonen lar deg tilordne bestemte numre til salgsfakturaer, basert på brukeren eller brukergruppen. Deretter kan du generere en rapport eller en XML-fil. Du kan også skrive ut en rapport om fakturanumre som er brukt.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Fakturanummerering for delstat trenger ikke lenger å vedlikeholdes. Rapport om brukte fakturanumre er ikke lenger nødvendig. |
| Erstattet med en annen funksjon? | Ingen                                                                                                                       |
| Berørte moduler             | Kundereskontro                                                                                                      |

### Definer navnene på lederen og en generelle regnskapsføreren for et firma for Litauen
<a id="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania" class="xliff"></a>

Navnet på lederen og den generell regnskapsføreren for et firma kan angis i firmainformasjonen og brukes i forskjellige utskrifter av lokale rapporter.

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| Årsak til avskrivning       | Erstattet med en annen funksjon                                     |
| Erstattet med en annen funksjon? | Ja, oppsettet av kontrollører kan brukes til det samme formålet.   |
| Berørte moduler             | Leverandører, Kundereskontro, Kontant- og bankbehandling |

### TelePay-betalingsformatene for Norge
<a id="telepay-payment-formats-for-norway" class="xliff"></a>

TelePay-betalingsformatene omfatter eksportformater for leverandør (kredittoverføring) og purring på kundebetaling (avtalegiro).

|                              |                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Betalingsformatene brukes ikke lenger.                                                        |
| Erstattet med en annen funksjon? | Ja, ISO20022 Betalingsformat for kredittoverføring og Format for AvtaleGiro-kundebetaling for Norge |
| Berørte moduler             | Leverandør, kunde                                                          |

### Eksportformater for leverandørbetaling for Finland
<a id="vendor-payment-export-formats-for-finland" class="xliff"></a>

Det finnes to formater for eksport av betalinger for Finland. LM02 (FI) brukes for innenlandsbetalinger, og LUM2 (FI) brukes for utenlandsbetalinger.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Årsak til avskrivning       | Betalingsformatene brukes ikke lenger.                  |
| Erstattet med en annen funksjon? | Ja, ISO20022 Betalingsformat for kredittoverføring for Finland |
| Berørte moduler             | Leverandører                                         |

### Arbeidsflyt for å opprette mål
<a id="workflow-for-creating-goals" class="xliff"></a>

En arbeidsflyt for behandling av opprettelsen av ansattes mål er en av flere arbeidsflyter som var tilgjengelige for å koordinere ytelsesstyringsprosessen.

|                              |                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Ytelsesstyring er utformet på nytt i Microsoft Dynamics 365 for Finance and Operations.                                                                                                                                                                                                                                        |
| Erstattet med en annen funksjon? | Den nyutformede funksjonen for ytelsesstyring gir større kontroll over innholdet i målene, målene som brukes til å spore fremdrift og vedlegg av støttedokumentasjon. Mål kan lagres som maler og deretter brukes på nytt. Denne funksjonen kan hjelpe deg med å konfigurere flere mål for ansatte raskere. |
| Berørte moduler             | Forvaltning av menneskelig kapital                                                                                                                                                                                                                                                                                                               |

## Funksjoner som er avskrevet i Dynamics AX 7.0-versjoner
<a id="features-deprecated-in-dynamics-ax-70-releases" class="xliff"></a>
### Muligheten til å avbryte endringer i en leverandørfaktura
<a id="ability-to-cancel-changes-to-a-vendor-invoice" class="xliff"></a>

|                              |                         |
|------------------------------|-------------------------|
| Årsak til avskrivning       | Ytelsesforbedring |
| Erstattet med en annen funksjon? | Antall                      |
| Berørte moduler             | Leverandører        |

### AIF-, AxD- og AxBC-integreringer
<a id="aif-axd-and-axbc-integrations" class="xliff"></a>

I Application Integration Framework (AIF) kan data utveksles med eksterne systemer gjennom forretningslogikk som vises som tjenester. Dynamics AX inneholder tjenestene som er basert på dokumenter og .NET Business Connector (AxBC). Et dokument opprettes ved hjelp av XML. XML-en inneholder hodeinformasjon som legges til for å opprette en *meldingen* som kan overføres til eller fra Dynamics AX. Eksempler på dokumenter er salgsordrer og bestillinger. Nesten enhver enhet, for eksempel en kunde, kan imidlertid representeres av et dokument. Tjenester som er basert på dokumenter, bruker **Axd &lt;*Dokument*&gt;**-klasser.

|                              |                                                                                                                                                                                                          |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Arkitekturen i AIF- og AxD-dokumenter kan ikke skaleres til en skytjeneste. Det oppstod ytelsesproblemer rundt masseimport.                                                                               |
| Erstattet med en annen funksjon? | I den gjeldende versjonen av Dynamics AX erstattes denne funksjonen av rammeverk for dataimport-/eksport, som støtter regelmessig bulkimport/-eksport. For AxBC anbefaler vi at du bruker de faktiske tabellene. |
| Berørte moduler             | AxD-er, AxBC-er og AIF                                                                                                                                                                                     |

### Stykklister uten stykklisteversjoner
<a id="boms-without-bom-versions" class="xliff"></a>

Når konfigurasjonsnøkkelen **Stykklisteversjoner** ble deaktivert, ble stykklisteversjonene skjult i alle skjemaer, og systemet fremtvang en 1:1-relasjon mellom frigitte produkter og stykklister. I gjeldende versjon av Dynamics AX kan ikke **Stykklisteversjoner**-konfigurasjonsnøkkelen deaktiveres.

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Bruk av en konfigurasjonsnøkkel for å styre stykklisteversjoner kan ikke skaleres i et skymiljø. |
| Erstattet med en annen funksjon? | Antall                                                                                      |
| Berørte moduler             | Behandling av produktinformasjon, Lagerstyring                                    |

### Brasiliansk Bordero
<a id="brazilian-bordero" class="xliff"></a>

Spesifikk betalingsmåte for brasilianske firmaer

|                              |                                                                                                       |
|------------------------------|-------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Støtte for den brasilianske Bordero-metoden for betalingsmåte er fjernet fra brasiliansk lokalisering |
| Erstattet med en annen funksjon? | Ingen                                                                                                    |
| Berørte moduler             | Leverandører                                                                                      |

### Brasiliansk Sintegra-utdrag
<a id="brazilian-sintegra-statement" class="xliff"></a>

Utdrag for føderal skatt for ICMS-avgift

|                              |                                                                                                                       |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Dette utdraget gjelder ikke lenger i enkelte delstater i Brasil.                                                     |
| Erstattet med en annen funksjon? | Nr. Brukere kan bruke det generelle elektroniske rapporteringsverktøyet for å konfigurere utdraget hvis det er nødvendig i bestemte situasjoner. |
| Berørte moduler             | Regnskapsbøker                                                                                                          |

### Brasiliansk SCAN-eventualitetsmodus for NF-e
<a id="brazilian-scan-contingency-mode-for-nf-e" class="xliff"></a>

(SCAN)-eventualitetsmiljø brukes til å generere, eksportere og importere statusen for en Nota Fiscal eletrônica (NF-e) når miljøet for Secretaria da Fazenda (SEFAZ) ikke er tilgjengelig.

|                              |                                                                             |
|------------------------------|-----------------------------------------------------------------------------|
| Årsak til avskrivning       | Denne eventualitetsmetoden er ikke lenger tilgjengelig i alle delstater i Brasil |
| Erstattet med en annen funksjon? | Ingen                                                                          |
| Berørte moduler             | Kundereskontro                                                         |

### Business Analyzer
<a id="business-analyzer" class="xliff"></a>

Denne mobilapplikasjonen lar brukere se gjennom viktige forretningsdata.

|                              |                                                                                                                                                               |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Funksjonen har blitt erstattet med en annen funksjon.                                                                                                      |
| Erstattet med en annen funksjon? | Innholdspakken Overvåk økonomiske resultater for Microsoft Power BI inneholder nøkkelmetrikk for økonomi som tidligere var tilgjengelig i verktøyet Business Analyzer. |
| Berørte moduler             | Økonomimodul                                                                                                                                                |

### Forretningsstatistikk
<a id="business-statistics" class="xliff"></a>

Oppsett av forretningsstatistikkforespørsler som kan hjelpe deg med å analysere ytelsen til organisasjonen

|                              |                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Foreldet tilnærming til forretningsanalyse (BI), lav kundebruk og begrenset funksjonssett |
| Erstattet med en annen funksjon? | Nye BI-løsninger for den gjeldende versjonen av Dynamics AX                                      |
| Berørte moduler             | Innkjøp og leverandører, Leverandører, Salg og markedsføring, Kunder         |

### Endre datofunksjonen for dokumentet i fakturagodkjenningsjournalen
<a id="change-document-date-function-in-invoice-approval-journal" class="xliff"></a>

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| Årsak til avskrivning       | Liten bruk                                                               |
| Erstattet med en annen funksjon? | Ja. Du kan endre dokumentdatoen på den posterte leverandørtransaksjonen. |
| Berørte moduler             | Leverandører                                                        |

### ClieOp03-betalingsformat for Nederland
<a id="clieop03-payment-format-for-the-netherlands" class="xliff"></a>

|                              |                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Formatet er ikke lenger i bruk i Nederland fordi det er erstattet av SEPA-funksjonaliteten. |
| Erstattet med en annen funksjon? | SEPA-betalingseksport                                                                                       |
| Berørte moduler             | Alle                                                                                                        |

### Overholdelsessenter
<a id="compliance-center" class="xliff"></a>

Overholdelsessenteret var et Enterprise Portal-område for administrasjon av kravene til dokumentasjon til samsvar som er knyttet til Sarbanes-Oxley-loven.

|                              |                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Mangel på kundebruk. Microsoft SharePoint inkluderer samme funksjon som var tilgjengelig i overholdelsessenteret. |
| Erstattet med en annen funksjon? | Antall                                                                                                                     |
| Berørte moduler             | Samsvar og interne kontroller                                                                                       |

### Connector for Microsoft Dynamics
<a id="connector-for-microsoft-dynamics" class="xliff"></a>

Dette verktøyet ble brukt til å integrere viktige data fra Microsoft Dynamics CRM til Microsoft Dynamics ERP-programmer.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Årsak til avskrivning       | Funksjonen har blitt erstattet med en annen funksjon. |
| Erstattet med en annen funksjon? | Dynamics-integrator                                      |
| Berørte moduler             | Connector for Microsoft Dynamics                         |

### Containerenhet og fysisk beholdning av flere dimensjoner
<a id="container-unit-and-multi-dimension-on-hand" class="xliff"></a>

|                              |                                                                                                                                                                 |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Duplikat funksjonalitet                                                                                                                                         |
| Erstattet med en annen funksjon? | Ja. Denne funksjonaliteten er erstattet med funksjonssettet for konsolidert partiordre etter AX 2012. Dette funksjonssettet inneholder den konsoliderte beholdningen. |
| Berørte moduler             | Behandling av produktinformasjon, Produksjonskontroll, Lagerstyring, Salg og markedsføring                                                                   |

### Bunkegruppemetadata
<a id="cue-group-metadata" class="xliff"></a>

|                              |                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Bunkegrupper ble brukt til å vise én eller flere bunker i faktaboksområdet. Det var begrenset opptak, og det var også ytelsesproblemer fordi en postendring i et overordnet skjema forårsaket én spørring per bunke i bunkegruppen. |
| Erstattet med en annen funksjon? | Antall                                                                                                                                                                                                                            |
| Berørte moduler             | Alle                                                                                                                                                                                                                           |

### Bunkemetadata
<a id="cue-metadata" class="xliff"></a>

|                              |                                                                                                                                                                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Bunkemetadata er begrenset til antall- eller suminformasjon.                                                                                                                                                                                   |
| Erstattet med en annen funksjon? | Side-ved-side-metadataene ble innført for å gi mer fleksibilitet for modellering. Du kan for eksempel opprette gjeldende antall, navigasjon og nøkkelytelsesindikatorer (KPI-er). Side-ved-side-metadata er direkte erstatning av bunkemetadata. |
| Berørte moduler             | Alle                                                                                                                                                                                                                                     |

### Dansk sjekkformat
<a id="danish-check-format" class="xliff"></a>

|                              |                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Støtte for dansk sjekkformatoppsett er avsluttet, og rapporten har blitt fjernet fra DK-lokalisering. |
| Erstattet med en annen funksjon? | Antall                                                                                                                      |
| Berørte moduler             | Alle                                                                                                                     |

### Datapartisjoner
<a id="data-partitions" class="xliff"></a>

Datapartisjoner gir en logisk separasjon av data i Microsoft Dynamics AX-databasen.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Datapartisjoner ble introdusert i Microsoft Dynamics AX 2012 R2 for å gjøre det mulig å isolere data. I et vanlig scenario har et firmaet datterselskaper, og data fra ett av datterselskapene skal ikke være synlig for et annet datterselskap, selv om begge datterselskaper håndteres av samme IT-avdelingen. Ekstra skript og administrasjon i hele programmet var imidlertid nødvendig for å opprette nye partisjoner og fylle dem med data, og for å sikkerhetskopiere partisjonsdata. I skyen, der vi har tilgang til databasetjenester for plattform som en tjeneste (PaaS) (Microsoft Azure SQL-Database), er det mye mer effektivt å bruke en database som isolasjonsbeholder enn å utføre isolasjon i programmet. Uavhengig av om partisjonering av data er nødvendig for datterselskaper, for flere leiere, eller bare for skala, mener vi at situasjonene kan håndteres bedre gjennom flere databaser eller flere Dynamics AX-forekomster. |
| Erstattet med en annen funksjon? | Datapartisjoner erstattes gjennom støtte for flere databaser eller Dynamics AX-forekomster i en fremtidig versjon.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Berørte moduler             | Alle                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

### Avgrensing
<a id="delimitation" class="xliff"></a>

|                              |                                        |
|------------------------------|----------------------------------------|
| Årsak til avskrivning       | Finner ingen bruk av funksjonen. |
| Erstattet med en annen funksjon? | Antall                                     |
| Berørte moduler             | Timeregistrering                    |

### Skrivebordsklient
<a id="desktop-client" class="xliff"></a>

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Dynamics AX-klientopplevelsen har fått ny utforming for å forbedre brukervennligheten på tvers av plattformer og enheter.                      |
| Erstattet med en annen funksjon? | Den nye webklienten er basert på skrivebordskjemametadataene og programmeringsmodellen som har blitt endret for å gi en rik webplattform. |
| Berørte moduler             | Alle                                                                                                                                    |

### Direkte databasetilkobling
<a id="direct-database-connection" class="xliff"></a>

I Dynamics AX 2012 R3 kan Retail Modern POS kobles direkte til kanaldatabasen på samme måte som Enterprise POS. Dette var i tillegg til standard kommunikasjonsmetode for Retail Modern POS-kommunikasjon via detaljhandelsserver.  

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Direkte databasetilkobling krevde protokoller med lavere sikkerhet, og ble hovedsakelig brukt til å oppnå den høyeste ytelsen. På grunn av ytelses- og sikkerhetsforbedringene som er utført i Finance and Operations, fører denne funksjonen nå til flere problemer enn den løser. |
| Erstattet med en annen funksjon? | Nr. Nå støttes bare standard kommunikasjon for detaljhandelsserver.    |
| Berørte moduler             | Kanaldatabase/Retail Modern POS                                    |

### Nederlandsk SWIFT MT940
<a id="dutch-swift-mt940" class="xliff"></a>

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Generisk funksjonalitet brukes nå i stedet for lokalisert funksjonalitet.                                                                                                                                                                 |
| Erstattet med en annen funksjon? | Ja, denne funksjonaliteten er erstattet av funksjonalitet for avanserte bankavstemming. I tillegg planlegges implementering av camt.053 ISO20022-kontoutdragimport for økonomijournalen i den neste oppdateringen av Dynamics AX. |
| Berørte moduler             | Alle                                                                                                                                                                                                                                   |

### eBilanz (XBRL for Tyskland)
<a id="ebilanz-xbrl-for-germany" class="xliff"></a>

Denne funksjonaliteten leverte XBRL-utdata (eXtensible Business Reporting Language) som er beregnet spesifikt for den tyske eBilanz-taksonomien.

|                              |                                                                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Mangel på kundebruk                                                                                                                                                 |
| Erstattet med en annen funksjon? | Denne funksjonen er ikke erstattet av en annen funksjon, men flere spesialiserte XBRL-pakker som gir rik XBRL-funksjonalitet, er tilgjengelige for det tyske markedet. |
| Berørte moduler             | Management Reporter                                                                                                                                                    |

### Enterprise Portal-klient
<a id="enterprise-portal-client" class="xliff"></a>

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | En enkelt klient plattform er levert.                                                                                            |
| Erstattet med en annen funksjon? | Den nye webklienten er basert på skrivebordskjemametadataene og programmeringsmodellen som har blitt endret for å gi en rik webplattform. |
| Berørte moduler             | Alle                                                                                                                                    |

### Miljømessig bærekraft
<a id="environmental-sustainability" class="xliff"></a>

|                              |                                                    |
|------------------------------|----------------------------------------------------|
| Årsak til avskrivning       | Lav kundebruk og begrenset funksjonssett       |
| Erstattet med en annen funksjon? | Antall                                                 |
| Berørte moduler             | Samsvar og interne kontroller, leverandører |

### Lage ActiveX- og administrerte vertskontroller
<a id="form-activex-and-managed-host-controls" class="xliff"></a>

|                              |                                                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | ActiveX-kontrollene og de administrerte vertskontrollene er basert på den avskrevne skrivebordsklienten.                                                                                                             |
| Erstattet med en annen funksjon? | Det utvidbare kontrollrammeverket støtter bygging av nye kontroller som er basert på HTML, CSS og JavaScript, og er en førsteklasses kontroll i Microsoft Visual Studio-verktøymiljøet. |
| Berørte moduler             | Alle                                                                                                                                                                                           |

### Generer forhåndsmerknader ved hjelp av et parti
<a id="generate-prenotes-by-using-a-batch" class="xliff"></a>

Generering av forhåndsmerknad kan ikke kan utføres ved hjelp av et parti, men kan fremdeles utføres av en bruker.

|                              |                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Det finnes ikke noe skjema for å beholde og vise den resulterende forhåndsmerknadsfilen når den blir generert ved hjelp av et parti. |
| Erstattet med en annen funksjon? | Forhåndsmerknader kan fremdeles genereres, og brukeren har kontroll over plasseringen der filen skal lagres.   |
| Berørte moduler             | Leverandører, Kundereskontro, Kontant- og bankbehandling                                        |

### Tysk DTAUS-betalingseksport og kontoutdragsimport (totaler og transaksjoner)
<a id="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions" class="xliff"></a>

|                              |                                                                                                                                                                                                                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Formatet er ikke lenger i bruk i Tyskland fordi det er erstattet av SEPA-funksjonaliteten (felles eurobetalingsområde).                                                                                                                                                                 |
| Erstattet med en annen funksjon? | Ja, denne funksjonaliteten er erstattet av SEPA-betalingseksport og avanserte funksjoner for bankavstemming for import av kontoutdrag. I tillegg planlegges implementering av camt.053 ISO20022-kontoutdragimport for økonomijournalen i den neste oppdateringen av Dynamics AX. |
| Berørte moduler             | Alle                                                                                                                                                                                                                                                                                            |

### Tysk DTAZV-betalingsformat
<a id="german-dtazv-payment-format" class="xliff"></a>

|                              |                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Formatet er ikke lenger i bruk i Tyskland fordi det er erstattet av SEPA-funksjonaliteten. |
| Erstattet med en annen funksjon? | SEPA-betalingseksport                                                                               |
| Berørte moduler             | Alle                                                                                                |

### Tysk MT940-import
<a id="german-mt940-import" class="xliff"></a>

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Generisk funksjonalitet brukes nå i stedet for lokalisert funksjonalitet.                                                                                                                                                                 |
| Erstattet med en annen funksjon? | Ja, denne funksjonaliteten er erstattet av funksjonalitet for avanserte bankavstemming. I tillegg planlegges implementering av camt.053 ISO20022-kontoutdragimport for økonomijournalen i den neste oppdateringen av Dynamics AX. |
| Berørte moduler             | Alle                                                                                                                                                                                                                                   |

### Tysk EU-salgsliste i XML
<a id="german-xml-eu-sales-list" class="xliff"></a>

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | XML-format for rapportering av tysk EU-salgsliste støttes ikke lenger. Bare ELMA5-tekstfilformatet kan brukes til å sende rapportering av EU-salgsliste til det tyske skattekontoret. |
| Erstattet med en annen funksjon? | Antall                                                                                                                                                                                 |
| Berørte moduler             | Avgift                                                                                                                                                                                |

### GL SSRS-rapporter
<a id="gl-ssrs-reports" class="xliff"></a>

Rapporter som inkluderer følgende menyelementer, er fjernet: **Råbalansesammendrag**, **Detaljert råbalanse**, **Kontoplan**, **Revisjonsspor**, **Saldoer** og **Saldoliste**.

|                              |                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | SSRS-rapporter (Microsoft SQL Server Reporting Services) er erstattet med Management Reporter-funksjoner og standardrapporter. |
| Erstattet med en annen funksjon? | Management Reporter (kalt **Finansrapportering** i den gjeldende versjonen av Dynamics AX)                                                  |
| Berørte moduler             | Økonomimodul                                                                                                                               |

### InfoPart- og FormPart-metadata
<a id="infopart-and-formpart-metadata" class="xliff"></a>

|                              |                                                                                                                                                                                                                                |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | InfoPart- og FormPart-metadata aktiverte opprettelsen av faktabokser for to forskjellige klienter.                                                                                                                                    |
| Erstattet med en annen funksjon? | InfoPart-metadata, som var en forenklet skjemadefinisjon, konverteres til et skjema ved hjelp av oppgraderingsverktøy. Metadata for FormPart, som refererer til et skjema, erstattes av en mer direkte referanse som opprettes av oppgraderingsverktøy. |
| Berørte moduler             | Alle                                                                                                                                                                                                                            |

### Listeside for hovedkonto
<a id="main-account-list-page" class="xliff"></a>

En liste over kontoer for den juridiske enheten og tilknyttet saldoinformasjon

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Saldoinformasjon er tilgjengelig på listesiden **Råbalanse** etter konto og dimensjon.                                                                                      |
| Erstattet med en annen funksjon? | **Hovedkontoer** inneholder den samme listen over kontoer som listesiden **Hovedkonto** inneholdt. Rutenettvisningen i **Hovedkontoer** viser også en enda mindre rutenettlignende visning. |
| Berørte moduler             | Økonomimodul                                                                                                                                                                     |

### Malaysia og Singapore bankkontantstrømrapport
<a id="malaysia-and-singapore-bank-cash-flow-report" class="xliff"></a>

Denne funksjonen gjør det mulig for brukeren å skrive ut en kontantstrømrapport som viser transaksjoner og detaljer om inn- og utkontantstrømmene for et valgt datoområde for valgte bankkontoer.

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| Årsak til avskrivning       | Den samme informasjonen kan hentes fra forespørselsbanktransaksjonen. |
| Erstattet med en annen funksjon? | Forespørselbanktransaksjonen                                            |
| Berørte moduler             | Kontant- og bankbehandling                                                |

### Meksikansk CFD elektronisk faktura
<a id="mexican-cfd-electronic-invoice" class="xliff"></a>

Denne funksjonen aktiverte genereringen av meksikanske elektroniske fakturaer ved hjelp av CFD-metoden (Comprobante Fiscal Digital), der firmaet signerer fakturaen ved å be om relaterte godkjenning fra myndighetene. Denne funksjonen gir også en månedlig rapport som inneholder alle elektroniske fakturaer som ble utstedt i perioden.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Metoden er ikke lenger gjeldende. Generering av elektroniske fakturaer ved hjelp av metoden CFD ble avskrevet av skattemyndighetene og erstattet med CFDI-metoden (Comprobante Fiscal Digital a través de Internet), der signeringen delegeres til tredjepartsleverandøren (PAC). Den månedlige rapporten er fjernet, og et forespørselsalternativ lar brukerne be om historiske transaksjoner. |
| Erstattet med en annen funksjon? | Antall                                                                                                                                                                                                                                                                                                                                                                                                        |
| Berørte moduler             | Kunder, Prosjekt                                                                                                                                                                                                                                                                                                                                                                              |

### Mexico realisert og urealisert mva
<a id="mexico-realized-and-unrealized-vat" class="xliff"></a>

Microsoft Dynamics AX 2012 administrerte urealisert merverdiavgift (mva) ved å bruke Mexico-spesifikk funksjonalitet for "urealisert mva".

|                              |                                                                                                                     |
|------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Duplikat funksjonalitet                                                                                             |
| Erstattet med en annen funksjon? | Ja, denne funksjonen er erstattet med standard betinget mva-funksjonaliteten som tilbys av Core. |
| Berørte moduler             | Avgift                                                                                                                 |

### Microsoft Outlook-integrering
<a id="microsoft-outlook-integration" class="xliff"></a>

|                              |                                                                                |
|------------------------------|--------------------------------------------------------------------------------|
| Årsak til avskrivning       | Denne funksjonaliteten er erstattet av Microsoft Exchange Server-integrering. |
| Erstattet med en annen funksjon? | Ja                                                                            |
| Berørte moduler             | Salg og markedsføring                                                            |

### Lønnsinformasjon i Personale
<a id="payroll-information-in-human-resources" class="xliff"></a>

Lønnsinformasjon i Personale

|                              |                                                                                                                                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Denne funksjonaliteten er erstattet av kjernesider for Lønn og Personale.                                                                                                                                                                                                                                              |
| Erstattet med en annen funksjon? | **Fordeler**, **Inntekter** og andre tilknyttede sider som tidligere var i US Payroll, er konfigurert på nytt og er nå en del av kjerneinstallasjonen av Personale for å støtte ekstern lønnsbehandling. Denne funksjonaliteten er tilgjengelig ved å bruke **Personale 1** &gt; **Lønn**-konfigurasjonsnøkkelen. |
| Berørte moduler             | Personale, Lønn                                                                                                                                                                                                                                                                                                     |

### Privat blokkering av lager- og lagerstyringsjournaler
<a id="private-blocking-of-inventory-and-warehouse-management-journals" class="xliff"></a>

Lager- og lagerstyringsjournaler støtter ikke lenger muligheten til å merke en journal som privat for en valgt bruker. Bare prosessen med å blokkere journaler som privat for brukergrupper og blokkering under redigering støttes.

|                              |                                        |
|------------------------------|----------------------------------------|
| Årsak til avskrivning       | Finner ingen bruk av funksjonen. |
| Erstattet med en annen funksjon? | Antall                                     |
| Berørte moduler             | Lagerstyring                   |

### Produktkonfigurator
<a id="product-builder" class="xliff"></a>

Produktkonfigurator ble brukt til å konfigurere varer dynamisk fra en salgsordre, en bestilling, en produksjonsordre, et salgstilbud, et prosjekttilbud eller et varebehov. Basert på en produktmodell som hadde modelleringsvariabler, kan brukeren velge verdier for å imøtekomme kundekravene og få en unik produktvariant som hadde en stykkliste og rute.

|                              |                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Produktkonfigurator viste X ++-kode til sluttbrukere og støttes ikke i den gjeldende versjonen av Dynamics AX. Den er fjernet for å unngå dupliserte vedlikeholdsforsøk på overlappende, skalerbare kodebaser. |
| Erstattet med en annen funksjon? | Produktkonfigurasjon                                                                                                                                                                                   |
| Berørte moduler             | Behandling av produktinformasjon, salg og markedsføring                                                                                                                                                     |

### Gi nytt navn til produktdimensjon
<a id="rename-product-dimension" class="xliff"></a>

Med denne funksjonen kan du endre navnet på en av de tre standard produktdimensjonene (størrelse, farge eller stil) til et navn som passer bedre til dine forretningsbehov. Navneendring inkluderte alle etikettene der produktdimensjonsnavnet ble brukt.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| Årsak til avskrivning       | Den gjeldende versjonen av Dynamics AX støtter ikke etikettendringer under kjøring. |
| Erstattet med en annen funksjon? | Ingen                                                                            |
| Berørte moduler             | Behandling av produktinformasjon                                                |

### Tilkobling til detaljhandelsserver med HTTP
<a id="retail-server-connectivity-using-http" class="xliff"></a>

I Dynamics AX 2012 R3 kunne detaljhandelsserveren fungerer ved hjelp av HTTP-kommunikasjon (ikke sikret). Dette var i tillegg til standardkommunikasjonen med HTTPS.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| Årsak til avskrivning       | På grunn av nye sikkerhetskrav støttes nå bare sikret kommunikasjon ved hjelp av TLS 1.2 (eller høyere, hvis tilgjengelig). Det selvbetjente installasjonsprogrammet konfigurerer automatisk datamaskinen for denne kommunikasjonen. |
| Erstattet med en annen funksjon? | Nr. Nå støttes bare standard HTTPS-kommunikasjon.                                                                           |
| Berørte moduler             | Detaljhandelsserver                                                |

### Rollesentersider
<a id="role-center-pages" class="xliff"></a>

|                              |                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Rollesentersider ble bygd på den avskrevne Enterprise Portal-plattformen, som er erstattet med den nye webklientplattformen i den gjeldende versjonen av Dynamics AX. |
| Erstattet med en annen funksjon? | Det nye arbeidsområdeskjemamønsteret gir brukerne en prosessentrert design som gir enkel tilgang til ofte brukte oppgaver i denne prosessen.                       |
| Berørte moduler             | Alle                                                                                                                                                                      |

### Mva-jurisdiksjoner
<a id="sales-tax-jurisdictions" class="xliff"></a>

|                              |                                              |
|------------------------------|----------------------------------------------|
| Årsak til avskrivning       | Lav kundebruk og begrenset funksjonssett |
| Erstattet med en annen funksjon? | Antall                                           |
| Berørte moduler             | Amerikansk merverdiavgift                                 |

### Transportørgrensesnitt
<a id="shipping-carrier-interface" class="xliff"></a>

|                              |                                                                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Duplikat funksjonalitet                                                                                                                         |
| Erstattet med en annen funksjon? | Ja, denne funksjonen er delvis erstattet med Transportstyring, men er ennå ikke erstattet med grunnleggende Lagerstyring (WMS I). |
| Berørte moduler             | Salg og markedsføring, Lagerstyring                                                                                                       |

### Sites Services
<a id="sites-services" class="xliff"></a>

Sites Services lar deg bygge webområder som utvider forretningsprosesser til Internett uten IT-støtte.

|                              |                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Microsoft Azure-infrastrukturen som brukes av Dynamics AX, har nye funksjoner som kan brukes i stedet (for eksempel Azure-områder). |
| Erstattet med en annen funksjon? | Antall                                                                                                                                       |
| Berørte moduler             | Personalerekruttering, saksbehandling, forespørsel om tilbud, leverandørregistrering                                                                  |

### SSAS, strategi for behovsprognose
<a id="ssas-demand-forecasting-strategy" class="xliff"></a>

|                              |                                                                              |
|------------------------------|------------------------------------------------------------------------------|
| Årsak til avskrivning       | Utformingen av funksjonen støttes ikke i den nye skyarkitekturen. |
| Erstattet med en annen funksjon? | Azure Machine Learning, strategi for behovsprognose                           |
| Berørte moduler             | Planlegging                                                                     |

### Reiserekvisisjoner
<a id="travel-requisitions" class="xliff"></a>

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| Årsak til avskrivning       | Liten bruk, og de fleste funksjonene fantes i Enterprise Portal. |
| Erstattet med en annen funksjon? | Antall                                                              |
| Berørte moduler             | Reiseregning og utlegg                                              |

### Leverandørfakturapulje uten posteringsdetaljer
<a id="vendor-invoice-pool-excluding-posting-details" class="xliff"></a>

|                              |                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Liten bruk. Denne funksjonaliteten er erstattet av fakturajournalen med funksjonaliteten for arbeidsflyten. |
| Erstattet med en annen funksjon? | Arbeidsflytfunksjoner til fakturajournalen.                                                           |
| Berørte moduler             | Leverandører                                                                                        |

### Virtuelle firmakontoer
<a id="virtual-company-accounts" class="xliff"></a>

Virtuelle firmaer-funksjonen støttes ikke lenger i Dynamics AX. Virtuelle firmaer-funksjonen lar brukere definere tabeller som kan deles av et sett med firmaer. Hvis du vil ha en beskrivelse av funksjonen, kan du se [Firmakontoer og virtuelle firmakontoer](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). Funksjonen fungerer ved å gruppere tabeller i samlinger som tilordnes til virtuelle firmaer, som er grupper av eksisterende "virkelige" firmaer. Spørringer opprettes slik at alle selskaper i det virtuelle firmaet kan få tilgang til dataene i tabellene til de tilknyttede tabellsamlingene.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Årsak til avskrivning</td>
<td><ul>
<li>Virtuelle firmaer må defineres før data lagres i tabellene. Retrotilpasning av virtuelle firmaer på en eksisterende implementering er veldig vanskelig.</li>
<li>Fordi det har vært så mye datanormalisering i den gjeldende versjonen av Microsoft Dynamics AX, har det blitt vanskelig å vite hva du skal legge til i tabellsamlinger. Det er for eksempel vanskelig å vite hvilke tabeller som skal deles. Alle tabellene det refereres til fra tabeller som er i et virtuelt firma, må også legges til. På grunn av tabellnormalisering må selv enkle hoveddata som er spredt over flere tabeller, være en del av det virtuelle firmaet. Eventuelle feil som gjøres her, vil forårsake funksjonsproblemer.</li>
<li>Når en tabell er en del av et virtuelt firma, mister den informasjon om opprinnelsen til dataene, og bare det virtuelle firmaet registreres.</li>
</ul></td>
</tr>
<tr class="even">
<td>Erstattet med en annen funksjon?</td>
<td>Globale tabeller kan brukes til å lage tabeller som er tilgjengelige fra alle firmaer. Det er for øyeblikket ingen erstatning.</td>
</tr>
<tr class="odd">
<td>Berørte moduler</td>
<td>Gjelder ikke her</td>
</tr>
</tbody>
</table>

### Lagerstyring II
<a id="warehouse-management-ii" class="xliff"></a>

|                              |                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Lagerstyring II-løsningen (WMS II) som var tilgjengelig i **Lagerstyring**-modulen, dupliserer funksjonaliteten i **Lagerstyring**-modulen som ble lansert i Microsoft Dynamics AX 2012 R3.                                                                         |
| Erstattet med en annen funksjon? | **Lagerstyring**-modulen som ble lansert i AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8 og Dynamics AX 2012 R3 CU9, erstatter Lagerstyring II-funksjonene. Den nye modulen har mer avanserte funksjoner og mer fleksible lagerstyringsprosesser enn i Lagerstyring II. |
| Berørte moduler             | Lagerstyring, salg og markedsføring, innkjøp og leverandører                                                                                                                                                                                                                                         |

### Arbeiderpåminnelser i Personale
<a id="worker-reminders-in-human-resources" class="xliff"></a>

Lønnsinformasjon i Personale

|                              |                 |
|------------------------------|-----------------|
| Årsak til avskrivning       | Liten bruk       |
| Erstattet med en annen funksjon? | Antall              |
| Berørte moduler             | Personale |

### Jobbplanlegger
<a id="workplanner" class="xliff"></a>

|                              |                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Liten bruk                                                                                                                                                            |
| Erstattet med en annen funksjon? | Nei, men **Profilrelasjon**-siden som åpnes fra **Profilgrupper**-siden, støtter samme forretningsscenario som den avskrevne **Jobbplanlegger**-siden. |
| Berørte moduler             | Timeregistrering                                                                                                                                                  |

### X++-regnskapsoppgjør
<a id="x-financial-statements" class="xliff"></a>

|                              |                                                                                             |
|------------------------------|---------------------------------------------------------------------------------------------|
| Årsak til avskrivning       | Funksjonen har blitt erstattet med en annen funksjon.                                    |
| Erstattet med en annen funksjon? | Management Reporter (kalt **Finansrapportering** i den gjeldende versjonen av Dynamics AX) |
| Berørte moduler             | Økonomimodul                                                                              |


