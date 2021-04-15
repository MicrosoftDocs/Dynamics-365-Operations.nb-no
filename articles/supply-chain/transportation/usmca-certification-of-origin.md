---
title: USMCA-sertifisering av opprinnelse
description: Med denne funksjonen kan du skrive ut sertifiseringen av opprinnelig dokumenter som er nødvendig i henhold til avtalen USA-Mexico-Canada (USMCA).
author: Henrikan
ms.date: 10/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-23
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: e479c7686ab9445b012d335ddc9fc4cdc6b2275c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807710"
---
# <a name="usmca-certification-of-origin"></a>USMCA-sertifisering av opprinnelse

[!include [banner](../includes/banner.md)]

Med denne funksjonen kan du skrive ut sertifiseringen av opprinnelig dokumenter som er nødvendig i henhold til avtalen USA-Mexico-Canada (USMCA).

*USMCA-sertifiseringen av opprinnelig dokument* inneholder minimum dataelementer som kreves for deklarasjon. Noen dataelementer kan forhåndsutfylles før utskrift, mens andre må fylles ut manuelt etter utskrift. Hvis du vil ha foretrukket tariffbehandling, må dokumentet fullføres og vær i hånden til importøren da deklarasjonen utføres. Dokumentet kan være fullført av importøren, eksportøren eller produsenten.

Du kan skrive ut dokumentet for en enkelt forsendelse fra **Alle forsendelser**-listesiden for alle forsendelser eller fra **Forsendelsesdetaljer**-siden.

Dokumentet er bare tilgjengelig når landet på primæradressen for den juridiske enheten er USA.

Dokumentet kan forhåndsfylles med data fra systemet, avhengig av dokumentutskriftsvalget. Det er mulig å endre eller legge til data i det utskrevne dokumentet ved å eksportere det utskrevne dokumentet til et redigerbart format, for eksempel Microsoft Word. Etter eksport kan du utføre alle nødvendige endringer før det gjøres en deklarasjon.

## <a name="turn-on-the-usmca-feature"></a>Aktivere USMCA-funksjonen

Før du kan bruke USMCA-funksjonen må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Transportstyring*
- **Funksjonsnavn:** *USMCA sertifisering av opprinnelig dokument*

## <a name="document-content"></a>Dokumentinnhold

USMCA-sertifisering av opprinnelig dokument inneholder følgende dataelementer:

- Adresseelementer
- Rollen til sertifiseringsparten
- Én forsendelse
- Fakturaer
- Rammeperiode
- Varedetaljer
- Signaturen til sertifisereren
- Antall sider

Hvis du vil ha mer informasjon om hvert av disse elementene og hvordan du finner verdiene til dem, kan du se resten av avsnittene i dette emnet.

## <a name="print-a-usmca-certification-of-origin-document"></a>Skriv ut en USMCA sertifisering av opprinnelig dokument

Hvis du vil skrive ut en USMCA-sertifisering av opprinnelig dokument for en forsendelse, gjør du følgende:

1. Gjør ett av følgende:
    - Gå til **Transportstyring > Forsendelser > Alle forsendelser**, og velg forsendelsen du vil skrive ut dokumentet for.
    - Åpne siden **Forsendelsesdetaljer** for forsendelsen du vil skrive ut dokumentet for (det finnes flere måter å komme hit på, deriblant fra siden **Alle forsendelser**).
1. I handlingsruten åpner du fanen **Forsendelser**, og i gruppen **Skriv ut** velger du **USMCA-sertifikat av opprinnelse**.
1. Dialogboksen **Sertifikat eller opprinnelse** åpnes. Angi innstillingene som er beskrevet i følgende underdeler, og velg deretter **OK** for å generere dokumentet.
1. En forhåndsvisning av dokumentet åpnes. Bruk kommandoene som vises i handlingsruten, til å skrive ut eller eksportere dokumentet etter behov.

### <a name="certifying-party"></a>Sertifiseringspart

Bruk rullegardinlisten for **Sertifiseringspart** til å identifisere typen part som skal skrive ut dokumentet. Angi om sertifiseringsparten er *eksportør*, *eksportør og produsent*, *produsent* eller *importør*, eller la den stå tom hvis sertifiseringsparten ikke er noen av disse. Alternativet du velger, bestemmer hva som skrives ut i adressedelene i dokumentet.

**Sertifiseringsparten** du velger, blir inkludert i det utskrevne dokumentet.

Dokumentet kan skrives ut for både innkommende og utgående forsendelser. Velg *Importør* som **Sertifiseringspart** bare for innkommende forsendelser.

Følgende tabell beskriver informasjonstypene som er inkludert i dokumentet, basert på hvilken **sertifiseringspart** du velger.

| Sertifiseringspart | beskrivelse |
|---|---|
| *\[Blank\]* | Legger til følgende detaljer i dokumentet:<ul><li>**Detaljer om sertifiserer**: Bruker adressedetaljene for forsendelseslageret, hvis tilgjengelig, ellers bruker den adressen for forsendelsesområdet, hvis den er tilgjengelig. Hvis ikke bruker den adressen til den juridiske enheten (firmaet) som er valgt i Supply Chain Management.</li><li>**Eksportørdetaljer**: tom</li><li>**Produsentdetaljer**: tom</li><li>**Importørdetaljer**: tom</li><ul>|
| *Eksportør* | Legger til følgende detaljer i dokumentet:<ul><li>**Detaljer om sertifiserer**: Bruker adressedetaljene for forsendelseslageret, hvis tilgjengelig, ellers bruker den adressen for forsendelsesområdet, hvis den er tilgjengelig. Hvis ikke bruker den adressen til den juridiske enheten (firmaet) som er valgt i Supply Chain Management.</li><li>**Eksportørdetaljer**: Bruker adressedetaljene for den juridiske enheten.</li><li>**Produsentdetaljer**: tom</li><li>**Importørdetaljer**: Bruker fakturakontoen for den tilknyttede salgsordren.</li><ul>|
| *Eksportør og produsent* | Legger til følgende detaljer i dokumentet:<ul><li>**Detaljer om sertifiserer**: Bruker adressedetaljene for forsendelseslageret, hvis tilgjengelig, ellers bruker den adressen for forsendelsesområdet, hvis den er tilgjengelig. Hvis ikke bruker den adressen til den juridiske enheten (firmaet) som er valgt i Supply Chain Management.</li><li>**Eksportørdetaljer**: Bruker adressedetaljene for den juridiske enheten.</li><li>**Produsentdetaljer**: Bruker adressedetaljene for den juridiske enheten.</li><li>**Importørdetaljer**: Bruker fakturakontoen for den tilknyttede salgsordren.</li><ul>|
| *Importør* | Legger til følgende detaljer i dokumentet:<ul><li>**Detaljer om sertifiserer**: Bruker adressedetaljene for forsendelseslageret, hvis tilgjengelig, ellers bruker den adressen for forsendelsesområdet, hvis den er tilgjengelig. Hvis ikke bruker den adressen til den juridiske enheten (firmaet) som er valgt i Supply Chain Management.</li><li>**Eksportørdetaljer**: tom</li><li>**Produsentdetaljer**: tom</li><li>**Importørdetaljer**: Bruker adressedetaljene for den juridiske enheten.</li><ul>|
| *Produsent* | Legger til følgende detaljer i dokumentet:<ul><li>**Detaljer om sertifiserer**: Bruker adressedetaljene for forsendelseslageret, hvis tilgjengelig, ellers bruker den adressen for forsendelsesområdet, hvis den er tilgjengelig. Hvis ikke bruker den adressen til den juridiske enheten som er valgt i Supply Chain Management.</li><li>**Eksportørdetaljer**: tom</li><li>**Produsentdetaljer**: Bruker adressedetaljene for den juridiske enheten.</li><li>**Importørdetaljer**: tom</li><ul>|

### <a name="has-various-producers"></a>Har ulike produsenter

Rullegardinlisten **Sertifiseringspart** kontrollerer teksten som skal brukes for produsentdetaljene i dokumentet. Velg ett av følgende:

- *Ulike produsenter* – Skriver ut teksten Ulike i produsentdetaljene.
- *Tilgjengelig ved forespørsel* – Skriver ut teksten Tilgjengelig ved forespørsel fra importmyndighetene i produsentdetaljene.

Når **sertifiseringsparten** er satt til *Eksportør og produsent* eller *Produsent*, overstyres **Har ulike produsenter**-innstillingene , og produsentens adressedetaljer vil være de samme som sertifisereren.

### <a name="blanket-period"></a>Rammeperiode

Bruk innstillingene **Rammeperiode fra** og **Rammeperiode til** til å opprette en rammeperiode der dokumentet dekker flere forsendelser av identiske varer, selv om dokumentet skrives ut bare for én forsendelse. Du kan angi datoene for rammeperioden uten begrensninger, og de blir lagt til i dokumentet. Du kan også la disse innstillingene stå tomme eller angi dem fortiden.

### <a name="is-single-shipment"></a>Er én forsendelse

I dialogboksen **Sertifikat av opprinnelse** angir du **Er én forsendelse** til ett av følgende:

- *Ja* – legger til Én forsendelse: ja ved siden av fakturanummeret.
- *Nei* – legger ikke til noen ting.

## <a name="other-information-included-in-the-document"></a>Annen informasjon som er inkludert i dokumentet

I tillegg til de valgfrie elementene du velger ved hjelp av dialogboksen **Sertifikat av opprinnelse**, vil USMCA-sertifiseringen av opprinnelig dokument inneholde informasjonen og egendefinerte felter som er oppsummert i følgende underdeler. Deler av denne informasjonen må angis manuelt etter at du har generert dokumentet.

### <a name="invoice-number"></a>Fakturanummer

ID-ene til salgsfakturaer som er knyttet til forsendelser, skrives ut på dokumentet uavhengig av rammeperioden. Fakturanumre skrives ut uavhengig av **Er én forsendelse**-valget.

### <a name="item-details"></a>Varedetaljer

Dokumentet inneholder flere deler som viser bestemte varedetaljer, som er:

- **SKU-nummer**: Skriver ut varenummeret til det frigitte produktet.

- **Beskrivelse**: Skriver ut enten beskrivelsen eller navnet på det frigitte produktet. Hvis det finnes en beskrivelse på brukerens språk, skrives denne ut. Hvis det ikke finnes en slik beskrivelse, skrives navnet på brukerens språk ut. Hvis dette navnet ikke finnes, skrives varenavnet ut.

- **HS-tariffklassifisering (harmonisert system)** : Skriver ut den harmoniserte tariffplan som er knyttet til produktet. Du kan definere disse planene ved å gå til **Transportstyring \> Oppsett \> Transportstandard \> Harmoniserte tariffplaner**.

- **Opprinnelseskriterium:** Du må angi data i denne delen manuelt første gang du frigir dokumentet.

- **Opprinnelsesland:** Skriver ut opprinnelseslandet, som du angir ved å gå til **Behandling av produktinformasjon \> Oppsett \> Produktoverensstemmelse \> Opprinnelsesland** (se også [Opprinnelsesland](../pim/country-of-origin.md)). ISO-koden for opprinnelseslandet skrives ut basert på landet/området for mål i leveringsadressen for forsendelsen og varen. Hvis ingen opprinnelsesland er definert, tilbakestilles denne verdien til innstillingen som ble funnet under **Frigitt produkt \> Utenrikshandel \> Opprinnelse**. Hvis det ikke blir funnet land med opprinnelige data, må du angi opprinnelseslandet manuelt etter at du har generere dokumentet.

### <a name="certifier-signature-and-date"></a>Sertifiserersignatur og dato

Du må angi dette manuelt etter at du har generert dokumentet.

### <a name="consists-of-number-of-pages"></a>Består av antall sider

Brukeren som signerer sertifiseringen, må manuelt angi antall sider (for bekreftelse) etter at dokumentet er definert.

### <a name="page-numbers"></a>Sidenumre

Gjeldende side og antall sider skrives ut nederst i dokumentet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]