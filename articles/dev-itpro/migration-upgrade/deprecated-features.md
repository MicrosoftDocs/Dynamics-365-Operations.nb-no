---
title: "Utgåtte funksjoner"
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning.
author: sericks007
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 0618d71fdb4b29bfdacd6b9e1a8ed47e03abe00d
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="removed-or-deprecated-features"></a>Fjernede eller avskrevne funksjoner

[!include[banner](../includes/banner.md)]

Dette emnet beskriver funksjonene som er fjernet eller avskrevet for Dynamics 365 for Finance and Operations.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging. 

> [!Note]
> Fra og med Dynamics 365 for Finance and Operations, Enterprise edition juli 2017-versjonen med plattformoppdatering 8, oppgis distribusjonstypen for hver fjernet eller avskrevet funksjon. Alle de tidligere versjonene som er nevnt i dette emnet, støttet bare skydistribusjoner.

## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-73-with-platform-update-12"></a>Dynamics 365 for Finance and Operations, Enterprise edition 7.3 med plattformoppdatering 12

### <a name="personalized-product-recommendations"></a>Personlige produktanbefalinger 
Fra 15. februar 2018 vil forhandlere ikke lenger kunne vise personlige produktanbefalinger på en salgsstedsenhet. Hvis du vil ha mer informasjon, kan du se [Personlige produktanbefalinger](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/personalized-product-recommendations).  

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Vi fjerner gjeldende versjon av produktanbefalingstjenesten fordi vi utformer denne funksjonen på nytt med en bedre algoritme og nyere detaljhandelsorienterte funksjoner.  |
| **Erstattet med en annen funksjon?**   | Nr. Etter våren 2018 planlegger vi imidlertid å få tilbake denne funksjonen for å dra nytte av en ny anbefalingstjeneste.   |
| **Berørte produktområder**         | Personlige produktanbefalinger i POS                                                    |
| **Distribusjonsalternativ**              | Alle                                                                                      |
| **Status**                         |Fjernet fra og med 15. februar 2018. Dette påvirker kunder som kjører Dynamics 365 for Operations 1611 og senere.  |

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a>Utvidelse av listen over elektroniske rapporteringsfunksjoner (ER)
Muligheten til å introdusere egendefinerte funksjoner som skal brukes i ER-uttrykksverktøyet (hvis du vil ha mer informasjon, se [Utvide listen over funksjoner for elektronisk rapportering (ER)](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)), støttes ikke lenger. På grunn av endringer i ER-API-ene ble API-en for å kalle innebygde funksjoner fra ER-uttrykksverktøyet, interne, og kan ikke utvides lenger.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Kodeforseglingsinitiativ  |
| **Erstattet med en annen funksjon?**   | Ingen. Når det er behov for en ny innebygd funksjon, må en ny utvidelsesforespørsel adresseres til ER-rammeverksteamet.<br><br>Som en midlertidig løsning mens den forespurte funksjonen er under utvikling i ER-teamet, kan den nødvendige logikken programmeres som en metode for en egendefinert programklasse. Denne metoden kan være tilgjengelig i et ER-uttrykk som en egenskap i den tilføyde ER-datakilden for **Program\Klasse**-typen som refererer til denne egendefinerte programklassen.  |
| **Berørte produktområder**         | Rammeverk for elektronisk rapportering                                                      |
| **Distribusjonsalternativ**              | Alle                                                                                      |
| **Status**                         | Fjernet fra og med Dynamics 365 for Finance and Operations, Enterprise edition 7.3.    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a>Lager per varegruppe- og Lager per lagerdimensjon-aldersfordelte saldolister

Disse to rapportene støttes ikke lenger i Finance and Operations. I stedet kan **Aldersfordeling for lager**-rapporten brukes til å forbedre brukeropplevelsen.

|   |  |
|--------------|-----------------------|
| **Årsak til avskrivning**       | Duplikat funksjonalitet  |
| **Erstattet med en annen funksjon?** | Ja. De to rapportene er erstattet av **Aldersfordeling for lager**-rapporten.     |
| **Berørte produktområder**       | Lagerstyring, kostnadsstyring        |
| **Distribusjonsalternativ**        | Alle|
| **Status**                       | Avskrevet: Menyelementene for de to rapportene er fjernet i versjon 7.3. Koden for rapportene beholdes imidlertid i produktet. Planen er å fjerne koden i en fremtidig versjon. |

### <a name="power-bi-content-packs-published-to-powerbicom"></a>Power BI-innholdspakker publisert til PowerBI.com
**Kostnadsstyring**-, **Finansresultat**- og **Resultat for detaljhandelskanal**-innholdspakkene som ble publisert på webområdet PowerBI.com, er avskrevet som følge av produktoppdateringer i Microsoft Power BI. Systemadministrasjonsskjemaer som brukes til å distribuere disse innholdspakkene til PowerBI.com, avskrives også i Finance and Operations.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Produktoppdateringer i Microsoft Power BI. |
| **Erstattet med en annen funksjon?**   | Power BI-innholdspakker (publisert til PowerBI.com) blir erstattet av analyseprogrammer som gjør det mulig med løsningsintegreringer på databasenivået. Hvis du vil ha mer informasjon om analyseprogrammer, se [Innebygd Power BI i arbeidsområder](../../dev-itpro/analytics/embed-power-bi-workspaces.md).    |
| **Berørte produktområder**         | Kostnadsstyring, økonomi og detaljhandel                                                                                               |
| **Distribusjonsalternativ**              | Bare sky (integrasjon med PowerBI.com støttes ikke i lokale distribusjoner.)                                                                                                            |
| **Status**                         | Avskrevet: Måltidsrammen for funksjonalitetsfjerningen er 2. kvartal 2018.    |

### <a name="standard-ui-in-data-management-workspace"></a>Standardgrensesnitt i arbeidsområdet for databehandling

Standardgrensesnittet i databehandling er det eldre brukergrensesnittet, som er standardgrensesnittet som vises for brukerne når de besøker arbeidsområdet for databehandling.

|   |  |
|------------------|-------------------------|
| **Årsak til avskrivning/fjerning** | Vi investerer i å gi nye brukeropplevelser i det nye brukergrensesnittet.             |
| **Erstattet med en annen funksjon?**   | Det nye brukergrensesnittet kalles *forbedret visning* og erstatter det gamle brukergrensesnittet.            |
| **Berørte produktområder**         | Arbeidsområdet for databehandling                                                     |
| **Distribusjonsalternativ**              | Alle                                                                           |
| **Status**                         | Avskrevet: Måltidsrammen for funksjonaliteten som skal fjernes, er 1. kvartal 2018. |

### <a name="excise-sales-tax-service-tax-for-india"></a>Forbrukeravgift, mva, tjenesteavgift for India

Disse avgiftene har blitt sammenfattet i indisk GST.

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Årsak til fjerning eller avskrivning**       | Disse avgiftene har blitt sammenfattet i indisk GST.                          |
| **Erstattet med en annen funksjon?**            | Indisk GST                                                              |
| **Berørte produktområder**                  | Mva                                                                     |
| **Distribusjonsalternativ**                       | Alle moduler                                                   |
| **Status**                                  | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |    

### <a name="file-validation-utility-fvu-for-india"></a>Filvalideringsverktøyet (FVU) for India

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Årsak til fjerning eller avskrivning**       | Mangel på kundebruk                                                  |
| **Erstattet med en annen funksjon?**            | Antall                                                                      |
| **Berørte produktområder**                  | Indisk kildeskatt                                                  |
| **Distribusjonsalternativ**                       | Alle moduler                                                                    |
| **Status**                                  | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.   |        

### <a name="tdstcs-certificate-for-india"></a>TDS/TCS-sertifikat for India

Brukere kan laste ned dette fra den offentlige portalen.

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Årsak til fjerning eller avskrivning**       | Mangel på kundebruk                                                  |
| **Erstattet med en annen funksjon?**            | Antall                                                                      |
| **Berørte produktområder**                  | Indisk kildeskatt                                                  |
| **Distribusjonsalternativ**                       | Alle moduler                                                                   |
| **Status**                                  | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a>Insitamentsplan for eksport/import (EXIM) for India


|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Årsak til fjerning eller avskrivning**       | Mangel på kundebruk                                                  |
| **Erstattet med en annen funksjon?**            | Antall                                                                      |
| **Berørte produktområder**                  | Importer og eksporter                                                       |
| **Distribusjonsalternativ**                       | Alle moduler                                                                    |
| **Status**                                  | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.  |    


## <a name="dynamics-365-for-retail-72"></a>Dynamics 365 for Retail 7.2

### <a name="personalized-product-recommendations"></a>Personlige produktanbefalinger 
Fra 15. februar 2018 vil forhandlere ikke lenger kunne vise personlige produktanbefalinger på en salgsstedsenhet. Hvis du vil ha mer informasjon, kan du se [Personlige produktanbefalinger](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/personalized-product-recommendations).  

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Vi fjerner gjeldende versjon av produktanbefalingstjenesten fordi vi utformer denne funksjonen på nytt med en bedre algoritme og nyere detaljhandelsorienterte funksjoner.  |
| **Erstattet med en annen funksjon?**   | Nr. Etter våren 2018 planlegger vi imidlertid å få tilbake denne funksjonen for å dra nytte av en ny anbefalingstjeneste.   |
| **Berørte produktområder**         | Personlige produktanbefalinger i POS                                                    |
| **Distribusjonsalternativ**              | Alle                                                                                      |
| **Status**                         |Fjernet fra og med 15. februar 2018. Dette påvirker kunder som kjører Dynamics 365 for Retail 7.2 og senere. |


## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Dynamics 365 for Finance and Operations, Enterprise edition juli 2017 med plattformoppdatering 8

### <a name="warehouse-mobile-devices-portal"></a>Portal for lagermobilenheter

Portal for lagermobilenheter (WMDP) var en frittstående komponent som var beregnet for selvdrevet lokal distribusjon. Denne komponenten støttes ikke lenger i Finance and Operations. Et innebygd program som gir en bedre brukeropplevelse, erstatter funksjonaliteten til WMDP.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Duplikat funksjonalitet.       |
| **Erstattet med en annen funksjon?**   | Ja. Denne funksjonen er erstattet med Finance and Operations - Warehousing. Hvis du vil ha mer informasjon om oppsett og forutsetninger, se [Installere og konfigurere Microsoft Dynamics 365 for Finange and Operations – Warehousing](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/install-configure-warehousing-app). |
| **Berørte produktområder**         | Lagerstyring, transportstyring     |
| **Distribusjonsalternativ**              | Portal for lagermobilenheter (WMDP) var en frittstående komponent som var beregnet for selvdrevet lokal distribusjon.               |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Avansert bankavstemming, samsvarsregel for manuelt samsvar

En samsvarsregele ble brukt til å velge og merke et bankdokument når dokumenter ble avstemt manuelt i avstemmingsregnearket.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Begrenset bruk.                                                                         |
| **Erstattet med en annen funksjon?**   | Nr. Kolonnefiltrering skal brukes til å finne dokumenter for avstemming. |
| **Berørte produktområder**         | Kontant- og bankbehandling                                                               |
| **Distribusjonsalternativ**              | Alle                                                                                    |
| **Status**                         | Fjernet fra og med juli 2017.                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a>Dynamics 365 for Operations 1611 med plattformoppdatering 3

### <a name="aeb-payment-formats-for-spain"></a>AEB-betalingsformatene for Spania

Betalingsformatene Consejo Superior Bancario ble brukt til å sende remitteringsfiler til banken for kunde- og leverandørbetalinger. Innholdet i disse formatene ble bestemt av Asociación Española de Banca. Den dekker Cuaderno 19, 32, 58, 34.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.                                  |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022-kredittoverføring og avtalegirobetalingsformater for Spania |
| **Berørte produktområder**         | Leverandør, kunde                                    |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.           |

### <a name="bank-payments-transfer-for-lithuania"></a>Bankbetalingsoverføringer for Litauen

Bankbetalingsoverføringer ble generert og skrevet ut ved hjelp av eksportformatet for betalingsoverføring (LT) for Litauen. Det litauiske markedet begynte å bruke LITAS, det samordnede elektroniske banksystemet i 2005.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.                        |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Betalingsformat for kredittoverføring for Litauen     |
| **Berørte produktområder**         | Leverandører                                               |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>BBS Direkte Remittering betalingsformatene for Norge

BBS Direkte Remittering betalingsformatene omfatter eksport av purring på kundebetaling (avtalegiro) og import av returmelding.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.  |
| **Erstattet med en annen funksjon?**   | Format for AvtaleGiro-kundebetaling for Norge kan brukes til å generere meldinger for AvtaleGiro. Importer av returmelding vil bli implementert i fremtidige versjoner. |
| **Berørte produktområder**         | Leverandør, kunde   |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a>Verktøy for kontoplan for Spania

Dette verktøyet brukes når en kontoplan i Spania krever store endringer. Brukere kan importere en ny kontoplan i Microsoft Excel- eller tekstformat, og kan også importere regnskapsoppgjør.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Begrenset bruk                                                  |
| **Erstattet med en annen funksjon?**   | Antall                                                             |
| **Berørte produktområder**         | Økonomimodul                                                 |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="dom80-payment-format-for-belgium"></a>Dom80-betalingsformat for Belgia

Eldre Belgisk betalingsformat for purring (avtalegiro).

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatet brukes ikke lenger.                          |
| **Erstattet med en annen funksjon?**   | Ja, ISO 20022 Avtalegiroformat for Belgia         |
| **Berørte produktområder**         | Kunder                                            |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG-betalingsformatene for Sveits

DTA/EZAG-formatene er integrert i ESR-systemet fordi de kan inneholde referansenummeret. Referansenummeret er ikke obligatorisk, og derfor kan disse formatene brukes til å behandle alle leverandørbetalinger. Disse formatene brukes av firmaer som har en bankkonto på et annet sted enn "Postfinance".

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.                        |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Betalingsformat for kredittoverføring for Sveits   |
| **Berørte produktområder**         | Leverandører                                               |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>EDIFACT-DIRDEB-betalingsformat for Østerrike

EDIFACT-DIRDEB-betalingsformat for purring (avtalegiro).

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatet brukes ikke lenger.                          |
| **Erstattet med en annen funksjon?**   | Ja, ISO 20022 Avtalegiroformat for Østerrike         |
| **Berørte produktområder**         | Kunder                                            |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="edivat-for-belgium"></a>EDIVAT for Belgia

EDIVAT er en foreldet belgisk standard for elektronisk deklarering via sikker e-post. Microsoft Dynamics AX 2012 beholder den skrivebeskyttede løsningen for å få tilgang til den historiske dataene.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Funksjonaliteten brukes ikke lenger.                           |
| **Erstattet med en annen funksjon?**   | Antall                                                             |
| **Berørte produktområder**         | Økonomimodul                                                 |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>eGiro EDIFACT CREMUL-betalingsimportformatet for Norge

eGiro er basert på den internasjonale UN EDIFACT CREMUL-standarden (Multiple Credit Advice Message) som brukes ved automatisk postering av kundebetalinger. eGiro er implementert som et formater for import av kundebetaling i Microsoft Dynamics AX.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatet brukes ikke lenger.                                                     |
| **Erstattet med en annen funksjon?**   | Nr. Formatet vil bli erstattet av ISO 20022-importformater for utdrag i fremtidige versjoner. |
| **Berørte produktområder**         | Kunder                                                                       |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                            |

### <a name="external-inventory-for-poland"></a>Eksternt lager for Polen

Bevis for varer som er hentet fra en salgsleverandør uten innkjøp. Varer som håndteres i eksternt lager, påvirker ikke standardlager og kan selges og deretter kjøpes automatisk. Denne prosessen oppretter reelle lagerbevegelser.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet med en annen funksjon                                    |
| **Erstattet med en annen funksjon?**   | Ja, kjernefunksjonaliteten Inngående forsendelse                |
| **Berørte produktområder**         | Leverandører, lagerstyring                         |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="financial-reports-generator-for-eastern-europe"></a>Generator for finansrapporter for Øst-Europa

Et verktøy brukes for å konfigurere datainnsamling for regnskaps- og avgiftsrapporter og eksportere data til XLS- og DOC-rapportmaler.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Begrenset bruk                                                                            |
| **Erstattet med en annen funksjon?**   | Nr. Verktøyet vil bli erstattet av elektroniske rapporteringskonfigurasjoner i fremtidige versjoner. |
| **Berørte produktområder**         | Økonomi                                                                           |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Import av kundebetalingstransaksjoner for Finland

Du kan velge et importformat for finske betalinger for å importere kundebetalingstransaksjoner fra en ekstern fil som banken leverer.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatet brukes ikke lenger.                                                     |
| **Erstattet med en annen funksjon?**   | Nr. Formatet vil bli erstattet av ISO 20022-importformater for utdrag i fremtidige versjoner. |
| **Berørte produktområder**         | Kunder                                                                       |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Import av betalingstransaksjoner i en finansjournal for Finland

Et format som er spesifikk for Finland, som brukes for å importere regnskapstransaksjoner til økonomimodulen.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatet brukes ikke lenger.                                                     |
| **Erstattet med en annen funksjon?**   | Nr. Formatet vil bli erstattet av ISO 20022-importformater for utdrag i fremtidige versjoner. |
| **Berørte produktområder**         | Kunder                                                                       |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Integrasjon med Isabel-synkronisert (CIS) for Belgia

Isabel er rammeverket for elektroniske banktjenester i Europa og de facto standard i Belgia.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Integrasjon med Isabel-klienten er avsluttet.   |
| **Erstattet med en annen funksjon?**   | Nr. Betalingsformatene som brukes ikke lenger brukes erstattes av ISO20022 Betalingsformat for kredittoverføring for Belgia. |
| **Berørte produktområder**         | Leverandører     |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Endringer i kontoplanen og regnskapsreglene for Spania

Denne funksjonen brukes til endringer i kontoplanen og regnskapsreglene i Spania. Den tilordner kontoer for å gjøre bidra til overføring av den gamle kontoplanen til den nye kontoplanen, og sammenligner det forrige regnskapsåret med det nye regnskapsåret, selv om de ble postert til ulike kontonumre.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Begrenset bruk                                                  |
| **Erstattet med en annen funksjon?**   | Antall                                                             |
| **Berørte produktområder**         | Økonomimodul                                                 |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Pagamento Fornittori-betalingsformatet for leverandør

Eldre italiensk betalingsformat for kredittoverføringer.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatet brukes ikke lenger.                          |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Betalingsformat for kredittoverføring for Italia         |
| **Berørte produktområder**         | Leverandører                                               |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="payment-export-formats-for-estonia"></a>Eksportformater for betaling for Estland.

Formatene Telehansa og Teleservice brukes for eksport for bankbetaling.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.                        |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Betalingsformat for kredittoverføring for Estland       |
| **Berørte produktområder**         | Leverandører                                               |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="payment-file-archive-for-norway"></a>Betalingsfilarkiv for Norge

Når betalingsfiler genereres, arkiverer filarkivet automatisk alle filene som opprettes, også filer som tidligere ble skrevet eller lest.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet med en annen funksjon                                        |
| **Erstattet med en annen funksjon?**   | Ja, arkiverte jobber for elektronisk rapportering                            |
| **Berørte produktområder**         | Leverandører, kunder, organisasjonsstyring |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.     |

### <a name="payment-import-formats-for-estonia"></a>Importformater for betaling for Estland

Formatene Telehansa og TeleTeenus brukes for import for bankbetaling.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.                                                    |
| **Erstattet med en annen funksjon?**   | Nr. Formatene vil bli erstattet av ISO 20022-importformater for utdrag i fremtidige versjoner. |
| **Berørte produktområder**         | Kunder                                                                        |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                             |

### <a name="payroll-information-in-human-resources"></a>Lønnsinformasjon i Personale

Lønnsinformasjon i Personale

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Denne funksjonaliteten er erstattet av kjernesider for Lønn og Personale.  |
| **Erstattet med en annen funksjon?**   | **Fordeler**, **Inntekter** og andre tilknyttede sider som tidligere var i US Payroll, er konfigurert på nytt og er nå en del av kjerneinstallasjonen av Personale for å støtte ekstern lønnsbehandling. Denne funksjonaliteten er tilgjengelig ved å bruke **Personale 1** \> **Lønn**-konfigurasjonsnøkkelen. |
| **Berørte produktområder**         | Personale, Lønn   |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations versjon 1611.    |

### <a name="performance-management-goal-workflow"></a>Arbeidsflyt for mål for ytelsesstyring

Ytelsesstyring omfatter målstyring og integrasjon med ytelsesvurderinger.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Ytelsesstyring ble endret, og antall målsider ble redusert for å forenkle prosessen.                 |
| **Erstattet med en annen funksjon?**   | Nr. Mål er synlige for lederselvbetjeningsportalen, og endres og vises av lederen. |
| **Berørte produktområder**         | Forvaltning av menneskelig kapital       |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations versjon 1611.    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Postgirot og Postgirot Utland-betalingsformatene for Sverige

Postgirot og Postgirot Utland-betalingsformatene for Sverige.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.                        |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Betalingsformat for kredittoverføring for Sverige        |
| **Berørte produktområder**         | Leverandører                                               |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="radio-frequency-identifier"></a>Radiofrekvensidentifisering

Radiofrekvensidentifisering (RFID) er en datainnsamlingsteknikk som bruker elektroniske brikker til å lagre identifiseringsdata. Innhenting av data krever ikke at leseren må være der brikkene er.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Lav kundebruk og begrenset funksjonssett.   |
| **Erstattet med en annen funksjon?**   | Antall                                              |
| **Berørte produktområder**         | Lagerstyring                            |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations 1611. |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Rapport om fakturanummerering for delstat for Latvia

Latvisk lovgivning angir bestemte regler for nummerering av salgsfakturaer. Funksjonen lar deg tilordne bestemte numre til salgsfakturaer, basert på brukeren eller brukergruppen. Deretter kan du generere en rapport eller en XML-fil. Du kan også skrive ut en rapport om fakturanumre som er brukt.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Fakturanummerering for delstat trenger ikke lenger å vedlikeholdes. Rapport om brukte fakturanumre er ikke lenger nødvendig. |
| **Erstattet med en annen funksjon?**   | Antall       |
| **Berørte produktområder**         | Kunder    |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Definer navnene på lederen og en generelle regnskapsføreren for et firma for Litauen

Navnet på lederen og den generell regnskapsføreren for et firma kan angis i firmainformasjonen og brukes i forskjellige utskrifter av lokale rapporter.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet med en annen funksjon                                     |
| **Erstattet med en annen funksjon?**   | Ja, oppsettet av kontrollører kan brukes til det samme formålet.   |
| **Berørte produktområder**         | Leverandører, Kundereskontro, Kontant- og bankbehandling |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.  |

### <a name="shipping-carrier-interface"></a>Transportørgrensesnitt

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Duplikat funksjonalitet   |
| **Erstattet med en annen funksjon?**   | Delvis erstattet av transportstyring |
| **Berørte produktområder**         | Salg og markedsføring, Lagerstyring  |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations versjon 1611.  |

### <a name="telepay-payment-formats-for-norway"></a>TelePay-betalingsformatene for Norge

TelePay-betalingsformatene omfatter eksportformater for leverandør (kredittoverføring) og purring på kundebetaling (avtalegiro).

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.                                                        |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Betalingsformat for kredittoverføring og Format for AvtaleGiro-kundebetaling for Norge |
| **Berørte produktområder**         | Leverandør, kunde                                                          |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                                 |

### <a name="vendor-payment-export-formats-for-finland"></a>Eksportformater for leverandørbetaling for Finland

Det finnes to formater for eksport av betalinger for Finland. LM02 (FI) brukes for innenlandsbetalinger, og LUM2 (FI) brukes for utenlandsbetalinger.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Betalingsformatene brukes ikke lenger.                        |
| **Erstattet med en annen funksjon?**   | Ja, ISO20022 Betalingsformat for kredittoverføring for Finland       |
| **Berørte produktområder**         | Leverandører                                               |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="warehouse-management-ii"></a>Lagerstyring II

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Lagerstyring II-løsningen (WMS II) som var tilgjengelig i **Lagerstyring**-modulen, dupliserer funksjonaliteten i **Lagerstyring**-modulen som ble lansert i Microsoft Dynamics AX 2012 R3.                                                                         |
| **Erstattet med en annen funksjon?**   | **Lagerstyring**-modulen som ble lansert i AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8 og Dynamics AX 2012 R3 CU9, erstatter Lagerstyring II-funksjonene. Den nye modulen har mer avanserte funksjoner og mer fleksible lagerstyringsprosesser enn i Lagerstyring II. |
| **Berørte produktområder**         | Lagerstyring, salg og markedsføring, innkjøp og leverandører   |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations versjon 1611.    |

### <a name="worker-reminders-in-human-resources"></a>Arbeiderpåminnelser i Personale

Lønnsinformasjon i Personale

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Liten bruk                                                           |
| **Erstattet med en annen funksjon?**   | Antall                                                                  |
| **Berørte produktområder**         | Personale                                                     |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations versjon 1611 |

### <a name="workflow-for-creating-goals"></a>Arbeidsflyt for å opprette mål

En arbeidsflyt for behandling av opprettelsen av ansattes mål er en av flere arbeidsflyter som var tilgjengelige for å koordinere ytelsesstyringsprosessen.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Ytelsesstyring er utformet på nytt i Microsoft Dynamics 365 for Finance and Operations.     |
| **Erstattet med en annen funksjon?**   | Den nyutformede funksjonen for ytelsesstyring gir større kontroll over innholdet i målene, målene som brukes til å spore fremdrift og vedlegg av støttedokumentasjon. Mål kan lagres som maler og deretter brukes på nytt. Denne funksjonen kan hjelpe deg med å konfigurere flere mål for ansatte raskere. |
| **Berørte produktområder**         | Forvaltning av menneskelig kapital                 |
| **Status**                         | Fjernet fra og med Dynamics 365 for Operations versjon 1611. |

## <a name="dynamics-ax-70"></a>Dynamics AX 7.0 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Muligheten til å avbryte endringer i en leverandørfaktura

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Ytelsesforbedring        |
| **Erstattet med en annen funksjon?**   | Antall                             |
| **Berørte produktområder**         | Leverandører               |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0. |

### <a name="aif-axd-and-axbc-integrations"></a>AIF-, AxD- og AxBC-integreringer

I Application Integration Framework (AIF) kan data utveksles med eksterne systemer gjennom forretningslogikk som vises som tjenester. Dynamics AX inneholder tjenestene som er basert på dokumenter og .NET Business Connector (AxBC). Et dokument opprettes ved hjelp av XML. XML-en inneholder hodeinformasjon som legges til for å opprette en *meldingen* som kan overføres til eller fra Dynamics AX. Eksempler på dokumenter er salgsordrer og bestillinger. Nesten enhver enhet, for eksempel en kunde, kan imidlertid representeres av et dokument. Tjenester som er basert på dokumenter, bruker **Axd \<Dokument\>**-klassene.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Arkitekturen i AIF- og AxD-dokumenter kan ikke skaleres til en skytjeneste. Det oppstod ytelsesproblemer rundt masseimport.                                        |
| **Erstattet med en annen funksjon?**   | Denne funksjonen erstattes av rammeverket for dataimport/-eksport, som støtter regelmessig bulkimport/-eksport. For AxBC anbefaler vi at du bruker de faktiske tabellene. |
| **Berørte produktområder**         | AxD-er, AxBC-er og AIF   |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.   |

### <a name="boms-without-bom-versions"></a>Stykklister uten stykklisteversjoner

Når konfigurasjonsnøkkelen **Stykklisteversjoner** ble deaktivert, ble stykklisteversjonene skjult i alle skjemaer, og systemet fremtvang en 1:1-relasjon mellom frigitte produkter og stykklister. I gjeldende versjon av Dynamics AX kan ikke **Stykklisteversjoner**-konfigurasjonsnøkkelen deaktiveres.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Bruk av en konfigurasjonsnøkkel for å styre stykklisteversjoner kan ikke skaleres i et skymiljø. |
| **Erstattet med en annen funksjon?**   | Antall                                                                                      |
| **Berørte produktområder**         | Behandling av produktinformasjon, Lagerstyring                                    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.                                                          |

### <a name="brazilian-bordero"></a>Brasiliansk Bordero

Spesifikk betalingsmåte for brasilianske firmaer

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Støtte for den brasilianske Bordero-metoden for betalingsmåte er fjernet fra brasiliansk lokalisering |
| **Erstattet med en annen funksjon?**   | Antall   |
| **Berørte produktområder**         | Leverandører   |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="brazilian-sintegra-statement"></a>Brasiliansk Sintegra-utdrag

Utdrag for føderal skatt for ICMS-avgift

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Dette utdraget gjelder ikke lenger i enkelte delstater i Brasil. |
| **Erstattet med en annen funksjon?**   | Nr. Brukere kan bruke det generelle elektroniske rapporteringsverktøyet for å konfigurere utdraget hvis det er nødvendig i bestemte situasjoner. |
| **Berørte produktområder**         | Regnskapsbøker    |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brasiliansk SCAN-eventualitetsmodus for NF-e

(SCAN)-eventualitetsmiljø brukes til å generere, eksportere og importere statusen for en Nota Fiscal eletrônica (NF-e) når miljøet for Secretaria da Fazenda (SEFAZ) ikke er tilgjengelig.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Denne eventualitetsmetoden er ikke lenger tilgjengelig i alle delstater i Brasil |
| **Erstattet med en annen funksjon?**   | Antall                                                                          |
| **Berørte produktområder**         | Kunder                                                         |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.              |

### <a name="business-analyzer"></a>Business Analyzer

Denne mobilapplikasjonen lar brukere se gjennom viktige forretningsdata.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Funksjonen har blitt erstattet med en annen funksjon.   |
| **Erstattet med en annen funksjon?**   | Innholdspakken Overvåk økonomiske resultater for Microsoft Power BI inneholder nøkkelmetrikk for økonomi som tidligere var tilgjengelig i verktøyet Business Analyzer. |
| **Berørte produktområder**         | Økonomimodul      |
| **Status**                         | Avskrevet: Bruken av Business Analyzer er avskrevet.    |

### <a name="business-statistics"></a>Forretningsstatistikk

Oppsett av forretningsstatistikkforespørsler som kan hjelpe deg med å analysere ytelsen til organisasjonen

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Foreldet tilnærming til forretningsanalyse (BI), lav kundebruk og begrenset funksjonssett |
| **Erstattet med en annen funksjon?**   | Nye BI-løsninger for den gjeldende versjonen av Dynamics AX                                      |
| **Berørte produktområder**         | Innkjøp og leverandører, Leverandører, Salg og markedsføring, Kunder         |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Endre datofunksjonen for dokumentet i fakturagodkjenningsjournalen

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Liten bruk                                                               |
| **Erstattet med en annen funksjon?**   | Ja. Du kan endre dokumentdatoen på den posterte leverandørtransaksjonen. |
| **Berørte produktområder**         | Leverandører                                                        |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a>ClieOp03-betalingsformat for Nederland

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Formatet er ikke lenger i bruk i Nederland fordi det er erstattet av SEPA-funksjonaliteten. |
| **Erstattet med en annen funksjon?**   | SEPA-betalingseksport  |
| **Berørte produktområder**         | Alle moduler     |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.   |

### <a name="compliance-center"></a>Overholdelsessenter

Overholdelsessenteret var et Enterprise Portal-område for administrasjon av kravene til dokumentasjon til samsvar som er knyttet til Sarbanes-Oxley-loven.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Mangel på kundebruk. Microsoft SharePoint inkluderer samme funksjon som var tilgjengelig i overholdelsessenteret. |
| **Erstattet med en annen funksjon?**   | Antall   |
| **Berørte produktområder**         | Samsvar og interne kontroller  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.    |

### <a name="connector-for-microsoft-dynamics"></a>Connector for Microsoft Dynamics

Dette verktøyet ble brukt til å integrere viktige data fra Microsoft Dynamics CRM til Microsoft Dynamics ERP-programmer.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Funksjonen har blitt erstattet med en annen funksjon. |
| **Erstattet med en annen funksjon?**   | Common Data Service                                      |
| **Berørte produktområder**         | Connector for Microsoft Dynamics                         |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Containerenhet og fysisk beholdning av flere dimensjoner

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Duplikat funksjonalitet |
| **Erstattet med en annen funksjon?**   | Ja. Denne funksjonaliteten er erstattet med funksjonssettet for konsolidert partiordre etter AX 2012. Dette funksjonssettet inneholder den konsoliderte beholdningen. |
| **Berørte produktområder**         | Behandling av produktinformasjon, Produksjonskontroll, Lagerstyring, Salg og markedsføring  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0. |

### <a name="cue-group-metadata"></a>Bunkegruppemetadata

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Bunkegrupper ble brukt til å vise én eller flere bunker i faktaboksområdet. Det var begrenset opptak, og det var også ytelsesproblemer fordi en postendring i et overordnet skjema forårsaket én spørring per bunke i bunkegruppen. |
| **Erstattet med en annen funksjon?**   | Antall      |
| **Berørte produktområder**         | Alle moduler    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.  |

### <a name="cue-metadata"></a>Bunkemetadata

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Bunkemetadata er begrenset til antall- eller suminformasjon.    |
| **Erstattet med en annen funksjon?**   | Side-ved-side-metadataene ble innført for å gi mer fleksibilitet for modellering. Du kan for eksempel opprette gjeldende antall, navigasjon og nøkkelytelsesindikatorer (KPI-er). Side-ved-side-metadata er direkte erstatning av bunkemetadata. |
| **Berørte produktområder**         | Alle moduler           |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0      |

### <a name="danish-check-format"></a>Dansk sjekkformat

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Støtte for dansk sjekkformatoppsett er avsluttet, og rapporten har blitt fjernet fra DK-lokalisering. |
| **Erstattet med en annen funksjon?**   | Antall    |
| **Berørte produktområder**         | Alle moduler    |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.  |

### <a name="data-partitions"></a>Datapartisjoner

Datapartisjoner gir en logisk separasjon av data i Microsoft Dynamics AX-databasen.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Datapartisjoner ble introdusert i Microsoft Dynamics AX 2012 R2 for å gjøre det mulig å isolere data. I et vanlig scenario har et firmaet datterselskaper, og data fra ett av datterselskapene skal ikke være synlig for et annet datterselskap, selv om begge datterselskaper håndteres av samme IT-avdelingen. Ekstra skript og administrasjon i hele programmet var imidlertid nødvendig for å opprette nye partisjoner og fylle dem med data, og for å sikkerhetskopiere partisjonsdata. I skyen, der vi har tilgang til databasetjenester for plattform som en tjeneste (PaaS) (Microsoft Azure SQL-Database), er det mye mer effektivt å bruke en database som isolasjonsbeholder enn å utføre isolasjon i programmet. Uavhengig av om partisjonering av data er nødvendig for datterselskaper, for flere leiere, eller bare for skala, mener vi at situasjonene kan håndteres bedre gjennom flere Finance and Operations-forekomster. |
| **Erstattet med en annen funksjon?**   | Kunder som bruker datapartisjoner, må bruke flere forekomster av Finance and Operations hvis databasenivåskillet er viktig.    |
| **Berørte produktområder**         | Alle moduler  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.  |


### <a name="database-and-file-share-storage-for-attachments"></a>Database og fildelingslagring for vedlegg

Microsoft Dynamics AX 2012 tillot lagring av vedlegg i databasen og delte filer. Ingen av disse alternativene støttes lenger.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Lagring av delte filer støttes ikke lenger fordi skyvertmiljøer ikke kan kommunisere med lokale delte filer. Databaselagring er avviklet til fordel for Azure Blob-lagring. Azure Blob-lagring tilsvarer lagring i databasen, siden dokumenter kan bare åpnes med Dynamics 365 for Finance and Operations-klientskjemaer. Dette gir fordelen med å gi lagring som ikke har en negativ innvirkning på ytelsen til databasen. Blob-lagring er standard lagringsmekanisme for dokumentbehandling og fungerer umiddelbart. |
| **Erstattet med en annen funksjon?**   | Databaselagring er avviklet til fordel for Azure Blob-lagring.   |
| **Berørte produktområder**         | Alle moduler  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.   |

### <a name="delimitation"></a>Avgrensing

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Finner ingen bruk av funksjonen. |
| **Erstattet med en annen funksjon?**   | Antall                                     |
| **Berørte produktområder**         | Timeregistrering                    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.         |

### <a name="desktop-client"></a>Skrivebordsklient

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Dynamics AX-klientopplevelsen har fått ny utforming for å forbedre brukervennligheten på tvers av plattformer og enheter.                      |
| **Erstattet med en annen funksjon?**   | Den nye webklienten er basert på skrivebordskjemametadataene og programmeringsmodellen som har blitt endret for å gi en rik webplattform. |
| **Berørte produktområder**         | Alle moduler  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.   |

### <a name="direct-database-connection"></a>Direkte databasetilkobling

I Dynamics AX 2012 R3 kan Retail Modern POS kobles direkte til kanaldatabasen på samme måte som Enterprise POS. Dette var i tillegg til standard kommunikasjonsmetode for Retail Modern POS-kommunikasjon via detaljhandelsserver.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Direkte databasetilkobling krevde protokoller med lavere sikkerhet, og ble hovedsakelig brukt til å oppnå den høyeste ytelsen. På grunn av ytelses- og sikkerhetsforbedringene som er utført i Finance and Operations, fører denne funksjonen nå til flere problemer enn den løser. |
| **Erstattet med en annen funksjon?**   | Nr. Nå støttes bare standard kommunikasjon for detaljhandelsserver.  |
| **Berørte produktområder**         | Kanaldatabase/Retail Modern POS   |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.  |

### <a name="dutch-swift-mt940"></a>Nederlandsk SWIFT MT940

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Generisk funksjonalitet brukes nå i stedet for lokalisert funksjonalitet.                    |
| **Erstattet med en annen funksjon?**   | Ja, denne funksjonaliteten er erstattet av funksjonalitet for avanserte bankavstemming. |
| **Berørte produktområder**         | Alle moduler                                                                              |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                           |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL for Tyskland)

Denne funksjonaliteten leverte XBRL-utdata (eXtensible Business Reporting Language) som er beregnet spesifikt for den tyske eBilanz-taksonomien.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Mangel på kundebruk  |
| **Erstattet med en annen funksjon?**   | Denne funksjonen er ikke erstattet av en annen funksjon, men flere spesialiserte XBRL-pakker som gir rik XBRL-funksjonalitet, er tilgjengelige for det tyske markedet. |
| **Berørte produktområder**         | Management Reporter      |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.  |

### <a name="enterprise-portal-client"></a>Enterprise Portal-klient

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | En enkelt klient plattform er levert.  |
| **Erstattet med en annen funksjon?**   | Den nye webklienten er basert på skrivebordskjemametadataene og programmeringsmodellen som har blitt endret for å gi en rik webplattform. |
| **Berørte produktområder**         | Alle moduler  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.   |

### <a name="environmental-sustainability"></a>Miljømessig bærekraft

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Lav kundebruk og begrenset funksjonssett  |
| **Erstattet med en annen funksjon?**   | Antall              |
| **Berørte produktområder**         | Samsvar og interne kontroller, leverandører  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0. |

### <a name="form-activex-and-managed-host-controls"></a>Lage ActiveX- og administrerte vertskontroller

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | ActiveX-kontrollene og de administrerte vertskontrollene er basert på den avskrevne skrivebordsklienten. |
| **Erstattet med en annen funksjon?**   | Det utvidbare kontrollrammeverket støtter bygging av nye kontroller som er basert på HTML, CSS og JavaScript, og er en førsteklasses kontroll i Microsoft Visual Studio-verktøymiljøet. |
| **Berørte produktområder**         | Alle moduler     |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.       |

### <a name="generate-prenotes-by-using-a-batch"></a>Generer forhåndsmerknader ved hjelp av et parti

Generering av forhåndsmerknad kan ikke kan utføres ved hjelp av et parti, men kan fremdeles utføres av en bruker.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Det finnes ikke noe skjema for å beholde og vise den resulterende forhåndsmerknadsfilen når den blir generert ved hjelp av et parti. |
| **Erstattet med en annen funksjon?**   | Forhåndsmerknader kan fremdeles genereres, og brukeren har kontroll over plasseringen der filen skal lagres.   |
| **Berørte produktområder**         | Leverandører, Kundereskontro, Kontant- og bankbehandling  |
| **Status**                         | Fjernet fra og med AX 7.0.    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Tysk DTAUS-betalingseksport og kontoutdragsimport (totaler og transaksjoner)

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Formatet er ikke lenger i bruk i Tyskland fordi det er erstattet av SEPA-funksjonaliteten (felles eurobetalingsområde).                    |
| **Erstattet med en annen funksjon?**   | Ja, denne funksjonaliteten er erstattet av SEPA-betalingseksport og avanserte funksjoner for bankavstemming for import av kontoutdrag. |
| **Berørte produktområder**         | Alle moduler  |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="german-dtazv-payment-format"></a>Tysk DTAZV-betalingsformat

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Formatet er ikke lenger i bruk i Tyskland fordi det er erstattet av SEPA-funksjonaliteten. |
| **Erstattet med en annen funksjon?**   | SEPA-betalingseksport    |
| **Berørte produktområder**         | Alle moduler   |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.    |

### <a name="german-mt940-import"></a>Tysk MT940-import

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Generisk funksjonalitet brukes nå i stedet for lokalisert funksjonalitet.                    |
| **Erstattet med en annen funksjon?**   | Ja, denne funksjonaliteten er erstattet av funksjonalitet for avanserte bankavstemming. |
| **Berørte produktområder**         | Alle moduler                                                                              |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.                           |

### <a name="german-xml-eu-sales-list"></a>Tysk EU-salgsliste i XML

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | XML-format for rapportering av tysk EU-salgsliste støttes ikke lenger. Bare ELMA5-tekstfilformatet kan brukes til å sende rapportering av EU-salgsliste til det tyske skattekontoret. |
| **Erstattet med en annen funksjon?**   | Antall         |
| **Berørte produktområder**         | Mva        |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.   |

### <a name="gl-ssrs-reports"></a>GL SSRS-rapporter

Rapporter som inkluderer følgende menyelementer, er fjernet: **Råbalansesammendrag**, **Detaljert råbalanse**, **Kontoplan**, **Revisjonsspor**, **Saldoer** og **Saldoliste**.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | SSRS-rapporter (Microsoft SQL Server Reporting Services) er erstattet med Management Reporter-funksjoner og standardrapporter. |
| **Erstattet med en annen funksjon?**   | Management Reporter (kalt **Finansrapportering** i den gjeldende versjonen av Dynamics AX)    |
| **Berørte produktområder**         | Økonomimodul   |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.   |

### <a name="infopart-and-formpart-metadata"></a>InfoPart- og FormPart-metadata

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | InfoPart- og FormPart-metadata aktiverte opprettelsen av faktabokser for to forskjellige klienter. |
| **Erstattet med en annen funksjon?**   | InfoPart-metadata, som var en forenklet skjemadefinisjon, konverteres til et skjema ved hjelp av oppgraderingsverktøy. Metadata for FormPart, som refererer til et skjema, erstattes av en mer direkte referanse som opprettes av oppgraderingsverktøy. |
| **Berørte produktområder**         | Alle moduler    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.        |

### <a name="main-account-list-page"></a>Listeside for hovedkonto

En liste over kontoer for den juridiske enheten og tilknyttet saldoinformasjon

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Saldoinformasjon er tilgjengelig på listesiden **Råbalanse** etter konto og dimensjon.  |
| **Erstattet med en annen funksjon?**   | **Hovedkontoer** inneholder den samme listen over kontoer som listesiden **Hovedkonto** inneholdt. Rutenettvisningen i **Hovedkontoer** viser også en enda mindre rutenettlignende visning. |
| **Berørte produktområder**         | Økonomimodul      |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malaysia og Singapore bankkontantstrømrapport

Denne funksjonen gjør det mulig for brukeren å skrive ut en kontantstrømrapport som viser transaksjoner og detaljer om inn- og utkontantstrømmene for et valgt datoområde for valgte bankkontoer.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Den samme informasjonen kan hentes fra forespørselsbanktransaksjonen. |
| **Erstattet med en annen funksjon?**   | Forespørselbanktransaksjonen                                            |
| **Berørte produktområder**         | Kontant- og bankbehandling                                                |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen.          |

### <a name="mexican-cfd-electronic-invoice"></a>Meksikansk CFD elektronisk faktura

Denne funksjonen aktiverte genereringen av meksikanske elektroniske fakturaer ved hjelp av CFD-metoden (Comprobante Fiscal Digital), der firmaet signerer fakturaen ved å be om relaterte godkjenning fra myndighetene. Denne funksjonen gir også en månedlig rapport som inneholder alle elektroniske fakturaer som ble utstedt i perioden.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Metoden er ikke lenger gjeldende. Generering av elektroniske fakturaer ved hjelp av metoden CFD ble avskrevet av skattemyndighetene og erstattet med CFDI-metoden (Comprobante Fiscal Digital a través de Internet), der signeringen delegeres til tredjepartsleverandøren (PAC). Den månedlige rapporten er fjernet, og et forespørselsalternativ lar brukerne be om historiske transaksjoner. |
| **Erstattet med en annen funksjon?**   | Antall    |
| **Berørte produktområder**         | Kunder, Prosjekt   |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="mexico-realized-and-unrealized-vat"></a>Mexico realisert og urealisert mva

Microsoft Dynamics AX 2012 administrerte urealisert merverdiavgift (mva) ved å bruke Mexico-spesifikk funksjonalitet for urealisert mva.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Duplikat funksjonalitet  |
| **Erstattet med en annen funksjon?**   | Ja, denne funksjonen er erstattet med standard betinget mva-funksjonaliteten som tilbys av Core. |
| **Berørte produktområder**         | Mva   |
| **Status**                         | Avskrevet: En dato for fjerning er ikke angitt for denne funksjonen. |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook-integrering


|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Denne funksjonaliteten er erstattet av Microsoft Exchange Server-integrering. |
| **Erstattet med en annen funksjon?**   | Ja                                                                            |
| **Berørte produktområder**         | Salg og markedsføring                                                            |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Privat blokkering av lager- og lagerstyringsjournaler

Lager- og lagerstyringsjournaler støtter ikke lenger muligheten til å merke en journal som privat for en valgt bruker. Bare prosessen med å blokkere journaler som privat for brukergrupper og blokkering under redigering støttes.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Finner ingen bruk av funksjonen. |
| **Erstattet med en annen funksjon?**   | Antall                                     |
| **Berørte produktområder**         | Lagerstyring                   |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.         |

### <a name="product-builder"></a>Produktkonfigurator

Produktkonfigurator ble brukt til å konfigurere varer dynamisk fra en salgsordre, en bestilling, en produksjonsordre, et salgstilbud, et prosjekttilbud eller et varebehov. Basert på en produktmodell som hadde modelleringsvariabler, kan brukeren velge verdier for å imøtekomme kundekravene og få en unik produktvariant som hadde en stykkliste og rute.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Produktkonfigurator viste X ++-kode til sluttbrukere og støttes ikke i den gjeldende versjonen av Dynamics AX. Den er fjernet for å unngå dupliserte vedlikeholdsforsøk på overlappende, skalerbare kodebaser.  |
| **Erstattet med en annen funksjon?**   | Ja. Restriksjonsbasert konfigurasjon ble innført i Dynamics AX 2012, der avskrivningen av Produktkonfigurator i fremtidige versjoner allerede var annonsert. Restriksjonsbasert konfigurasjonsteknologi er valgt i produktstandardene for å muliggjøre konfigurasjonen. Hvis du vil ha mer informasjon, kan du se [Bygge en produktkonfigurasjonsmodell](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/pim/build-product-configuration-model). |
| **Berørte produktområder**         | Behandling av produktinformasjon, salg og markedsføring  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.      |

### <a name="rename-product-dimension"></a>Gi nytt navn til produktdimensjon

Med denne funksjonen kan du endre navnet på en av de tre standard produktdimensjonene (størrelse, farge eller stil) til et navn som passer bedre til dine forretningsbehov. Navneendring inkluderte alle etikettene der produktdimensjonsnavnet ble brukt.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Den gjeldende versjonen av Dynamics AX støtter ikke etikettendringer under kjøring. |
| **Erstattet med en annen funksjon?**   | Antall                                                                            |
| **Berørte produktområder**         | Behandling av produktinformasjon                                                |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.                                                |

### <a name="retail-server-connectivity-using-http"></a>Tilkobling til detaljhandelsserver med HTTP

I Dynamics AX 2012 R3 kunne detaljhandelsserveren fungerer ved hjelp av HTTP-kommunikasjon (ikke sikret). Dette var i tillegg til standardkommunikasjonen med HTTPS.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | På grunn av nye sikkerhetskrav støttes nå bare sikret kommunikasjon ved hjelp av TLS 1.2 (eller høyere, hvis tilgjengelig). Det selvbetjente installasjonsprogrammet konfigurerer automatisk datamaskinen for denne kommunikasjonen. |
| **Erstattet med en annen funksjon?**   | Nr. Nå støttes bare standard HTTPS-kommunikasjon. |
| **Berørte produktområder**         | Retail-server  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0. |

### <a name="role-center-pages"></a>Rollesentersider

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Rollesentersider ble bygd på den avskrevne Enterprise Portal-plattformen, som er erstattet med den nye webklientplattformen i den gjeldende versjonen av Dynamics AX. |
| **Erstattet med en annen funksjon?**   | Det nye arbeidsområdeskjemamønsteret gir brukerne en prosessentrert design som gir enkel tilgang til ofte brukte oppgaver i denne prosessen.                       |
| **Berørte produktområder**         | Alle moduler    |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0   |

### <a name="sales-tax-jurisdictions"></a>Mva-jurisdiksjoner

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Lav kundebruk og begrenset funksjonssett |
| **Erstattet med en annen funksjon?**   | Antall                                           |
| **Berørte produktområder**         | Amerikansk merverdiavgift                                 |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.               |

### <a name="sites-services"></a>Sites Services

Sites Services lar deg bygge webområder som utvider forretningsprosesser til Internett uten IT-støtte.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Microsoft Azure-infrastrukturen som brukes av Dynamics AX, har nye funksjoner som kan brukes i stedet (for eksempel Azure-områder). |
| **Erstattet med en annen funksjon?**   | Antall   |
| **Berørte produktområder**         | Personalerekruttering, saksbehandling, forespørsel om tilbud, leverandørregistrering, samarbeidsområder for salgsmuligheter og kampanjer  |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.    |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS, strategi for behovsprognose

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Utformingen av funksjonen støttes ikke i den nye skyarkitekturen. |
| **Erstattet med en annen funksjon?**   | Azure Machine Learning, strategi for behovsprognose                           |
| **Berørte produktområder**         | Hovedplanlegging                                                              |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Leverandørfakturapulje uten posteringsdetaljer

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Liten bruk. Denne funksjonaliteten er erstattet av fakturajournalen med funksjonaliteten for arbeidsflyten. |
| **Erstattet med en annen funksjon?**   | Arbeidsflytfunksjoner til fakturajournalen.     |
| **Berørte produktområder**         | Leverandører |
| **Status**                         | Fjernet fra og med Dynamics AX 7.0.    |


### <a name="virtual-company-accounts"></a>Virtuelle firmakontoer

Virtuelle firmaer-funksjonen støttes ikke lenger i Dynamics AX. Virtuelle firmaer-funksjonen lar brukere definere tabeller som kan deles av et sett med firmaer. Hvis du vil ha en beskrivelse av funksjonen, kan du se [Firmakontoer og virtuelle firmakontoer](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). Funksjonen fungerer ved å gruppere tabeller i samlinger som tilordnes til virtuelle firmaer, som er grupper av eksisterende "virkelige" firmaer. Spørringer opprettes slik at alle selskaper i det virtuelle firmaet kan få tilgang til dataene i tabellene til de tilknyttede tabellsamlingene.

|   |  | 
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | - Virtuelle firmaer må defineres før data lagres i tabellene. Retrotilpasning av virtuelle firmaer på en eksisterende implementering er veldig vanskelig.<br><br>- Fordi det har vært så mye datanormalisering i den gjeldende versjonen av Dynamics AX, har det blitt vanskelig å vite hva du skal legge til i tabellsamlinger. Det er for eksempel vanskelig å vite hvilke tabeller som skal deles. Alle tabellene det refereres til fra tabeller som er i et virtuelt firma, må også legges til. På grunn av tabellnormalisering må selv enkle hoveddata som er spredt over flere tabeller, være en del av det virtuelle firmaet. Eventuelle feil som gjøres her, vil forårsake funksjonsproblemer.<br><br>- Når en tabell er en del av et virtuelt firma, mister den informasjon om opprinnelsen til dataene, og bare det virtuelle firmaet registreres.   |
| **Erstattet med en annen funksjon?** | Globale tabeller kan brukes til å lage tabeller som er tilgjengelige fra alle firmaer. Det er for øyeblikket ingen erstatning. |   
| **Berørte produktområder**       | Alle moduler |   
| **Status**                       | Fjernet fra og med Dynamics AX 7.0.   |   

### <a name="windows-8-tablet-app"></a>Windows 8 nettbrettapp

Windows 8 nettbrettapp inneholdt funksjonalitet for utgiftsregistrering og -godkjenning.

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Finance and Operations er kompatibel med nettbrett. Nettbrettappen er ikke lenger nødvendig.    |
| **Erstattet med en annen funksjon?**   | Nr.          |
| **Berørte produktområder**         | Reiseregning og utlegg   |
| **Status**                         | Fjernet: Denne funksjonen er bare tilgjengelig for Dynamics AX 2012 R3. |

### <a name="workplanner"></a>Jobbplanlegger

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Liten bruk |
| **Erstattet med en annen funksjon?**   | Nei, men **Profilrelasjon**-siden som åpnes fra **Profilgrupper**-siden, støtter samme forretningsscenario som den avskrevne **Jobbplanlegger**-siden. |
| **Berørte produktområder**         | Timeregistrering     |
| **Status**                         | Koden har ikke blitt fjernet. Skjemaet JmgWorkPlanner ble imidlertid ikke overført.    |

### <a name="x-financial-statements"></a>X++-regnskapsoppgjør

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Funksjonen har blitt erstattet med en annen funksjon.                                    |
| **Erstattet med en annen funksjon?**   | Management Reporter (kalt **Finansrapportering** i den gjeldende versjonen av Dynamics AX) |
| **Berørte produktområder**         | Økonomimodul                                                                              |
| **Status**                         | Fjernet fra og med Dynamics AX 2012                                                              |

