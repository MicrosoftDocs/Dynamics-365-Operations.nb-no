---
title: Oppgrader til parten og den globale adressebokmodellen
description: Denne artikkelen beskriver hvordan du oppgraderer data for dobbel skriving til partsmodellen og den globale adressebokmodellen.
author: RamaKrishnamoorthy
ms.date: 03/10/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 02ab3675db0d78efa1e4e43188d79bb1e763a713
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111826"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Oppgrader til parten og den globale adressebokmodellen

[!include [banner](../../includes/banner.md)]



Med [Microsoft Azure Data Factory-malene](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) kan du oppgradere eksisterende data i dobbel skriving til partsmodellen og den globale adressebokmodellen: data i **Konto**, **Kontakt** og **Leverandør** tabellene, og postadresser og elektroniske adresser.

Følgende tre Data Factory-maler tilbys. De bidrar til å avstemme dataene fra både økonomi- og driftsapper og kundeengasjementsapper.

- **[Partsmal](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (Oppgrader data til dobbel skriving Part-Global adressebok-skjema/arm_template.json)** – Denne malen oppgraderer **Part** og **Kontakt** data som er knyttet til **Konto**, **Kontakt** og **Leverandør** data.
- **[Postadressemal for part](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) (Oppgrader til dobbel skriving Part-Global adressebok-skjema/Oppgrader til postadresse for part - Global adresseliste/arm_template.json)** – Denne malen hjelper til med å oppgradere postadressene som er knyttet til **Konto**, **Kontakt** og **Leverandør** data.
- **[Elektronisk adressemal for part](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) (Oppgrader til dobbel skriving Part-Global adressebok-skjema/Oppgrader til elektronisk adresse for part - Global adresseliste/arm_template.json)** – Denne malen hjelper til med å oppgradere elektroniske adresser som er knyttet til **Konto**, **Kontakt** og **Leverandør** data.

På slutten av prosessen genereres følgende kommaseparerte verdier (.csv)-filer.

| Filnavn | Formål |
|---|---|
| FONewParty.csv | Denne filen bidrar til å generere nye **Part**-oppføringer i økonomi- og driftsappen. |
| ImportFONewPostalAddressLocation.csv | Denne filen hjelper deg med å opprette nye **Postadressested**-poster i økonomi- og driftsappen. |
| ImportFONewPartyPostalAddress.csv | Denne filen hjelper deg med å opprette nye **Postadresse for part**-poster i økonomi- og driftsappen. |
| ImportFONewPostalAddress.csv | Denne filen hjelper deg med å opprette nye **Postadresse**-poster i økonomi- og driftsappen. |
| ImportFONewElectronicAddress.csv | Denne filen hjelper deg med å opprette nye **Elektronisk adresse**-poster i økonomi- og driftsappen. |

I denne artikkelen finner du instruksjoner om hvordan du kan bruke Data Factory-malene og oppgradere dataene. Hvis du ikke har noen tilpasninger, kan du bruke malene som de er. Hvis du har tilpasninger for **Konto**, **Kontakt** og **Leverandør**-data, må du endre malene ved å følge instruksjonene i denne artikkelen.

> [!IMPORTANT]
> Det finnes spesielle instruksjoner for kjøring av malene Postadresse for part og Elektronisk adresse for part. Du må kjøre partsmalen først, deretter malen for partspostadresse og deretter den elektroniske adressemalen for part. Hver mal er utformet for å importeres i en separat datafabrikk.

## <a name="prerequisites"></a>Forutsetninger

Følgende forutsetninger kreves for å oppgradere til parten og den globale adressebokmodellen:

+ Du må ha et [Azure-abonnement](https://portal.azure.com/).
+ Du må ha tilgang til [malene](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
+ Du må være en eksisterende kunde med dobbel skriving.

## <a name="prepare-for-the-upgrade"></a>Forberede for oppgraderingen

En oppgradering krever følgende forberedelse:

+ **Fullstendig synkronisering:** Både Finance and Operations-miljøet og Customer Engagement-miljøet er i fullstendig synkronisert tilstand for tabellene **Konto (Kunde)**, **Kontakt** og **Leverandør**.
+ **Integrasjonsnøkler:**: Tabellene **Konto (kunde)**, **Kontakt** og **Leverandør** i Customer Engagement-apper bruker de medfølgende integrasjonsnøklene. Hvis du har tilpasset integrasjonsnøklene, må du tilpasse malen.
+ **Partsnummer:** Alle oppføringer av typen **Konto (kunde)**, **Kontakt** og **Leverandør** som skal oppgraderes, har et partsnummer. Poster som ikke har partnummer, blir ignorert. Hvis du vil oppgradere disse oppføringer, legger du til et partsnummer før du starter oppgraderingsprosessen.
+ **Systembrudd:** Under oppgraderingsprosessen må du koble fra både Finance and Operations- og Customer Engagement-miljøer.
+ **Øyeblikksbilde:** Ta et øyeblikksbilde både av økonomi- og driftsappene og kundeengasjementsappene. Du kan bruke øyeblikksbildene til å gjenopprette den forrige tilstanden hvis du må.

## <a name="deployment"></a>Distribusjon

1. Last ned malene fra [Dynamics-365-FastTrack-Implementering-Ressurser](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
2. Logg på [Azure-portalen](https://portal.azure.com/).
3. Opprett en [ressursgruppe](/azure/azure-resource-manager/management/manage-resource-groups-portal).
4. Opprett en [lagringskonto](/azure/storage/common/storage-account-create?tabs=azure-portal) i ressursgruppen som du opprettet.
5. Opprett en [datafabrikk](/azure/data-factory/quickstart-create-data-factory-portal) i ressursgruppen som du opprettet.
6. Åpne datafabrikken og velg flisen **Forfatter og overvåking**.
7. På **Administrer**-fanen velger du **ARM-mal**.
8. Velg **Importer ARM-mal** for å importere **partsmalen**.
9. Importer malen til datafabrikken. Angi følgende verdier for **Prosjektdetalj** og **Forekomstdetaljer**.

    | Felt | Verdi |
    |---|---|
    | Abonnement | Azure-abonnementet |
    | Ressursgruppe | Oppgi den samme ressursen som lagringskontoen opprettes under. |
    | Område | Området |
    | Fabrikknavn | Fabrikknavnet |
    | FO Linked Service_service Principal Key | Programmets nøkkel |
    | Azure Blob Storage_connection String | Azure Blob Storage-tilkoblingsstrengen |
    | Dynamics Crm Linked Service_password | Passordet for brukerkontoen du oppgir som brukernavnet |
    | FO Linked Service_properties_type Properties_url | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | FO Linked Service_properties_type Properties_tenant | Informasjon (domenenavn eller leier-ID) om leieren som appen ligger under |
    | FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | FO Linked Service_properties_type Properties_service Principal Id | Klient-ID-en til programmet |
    | Dynamics Crm Linked Service_properties_type Properties_username | Brukernavnet som brukes til å koble til Dynamics 365 |

    Hvis du vil ha mer informasjon, kan du se følgende emner:

    - [Forfremme en Resource Manager-mal for hvert miljø manuelt](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Tilkoblede tjenesteegenskaper](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Kopiere data ved hjelp av Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Etter distribusjonen validerer du datasettene, dataflyten og den tilkoblede tjenesten til datafabrikken.

    ![Datasett, dataflyt og tilknyttet tjeneste.](media/data-factory-validate.png)

11. Gå til **Administrer**. Under **Tilkoblinger** velger du **Tilknyttet tjeneste**. Velg deretter **DynamicsCrmLinkedService**. I dialogboksen **Rediger tilknyttet tjeneste (Dynamics CRM)** angir du følgende verdier.

    | Felt | Verdi |
    |---|---|
    | Navn | DynamicsCrmLinkedService |
    | beskrivelse | Tilknyttede tjenester for tilkobling til CRM-forekomsten for å hente data for enheter |
    | Tilkobling via integrasjonskjøretid | AutoResolvelntegrationRuntime |
    | Distribusjonstype | Tilkoblet |
    | Tjeneste-URI | `https://<organization-name>.crm[x].dynamics.com` |
    | Godkjenningstype | Office365 |
    | Brukernavn | |
    | Passord eller Azure Key Vault | Passord |
    | Passord | |

## <a name="prepare-to-run-the-data-factory-templates"></a>Forberede kjøring av Data Factory-maler

Denne delen beskriver oppsettet som kreves før du kjører partspostadressen og Data Factory-malene for elektronisk adresse for part.

### <a name="setup-to-run-the-party-postal-address-template"></a>Oppsett for å kjøre malen for partspostadresse

1. Logg deg på kundeengasjementsapper, og gå til **Innstillinger** \> **Tilpasningsinnstillinger**. I kategorien **Generelt** konfigurerer du deretter tidssoneinnstillingen for systemadministratorkontoen. Tidssonen må være i UTC-tid (Coordinated Universal Time) for å oppdatere "gyldig fra"- og "gyldig til"-datoene for postadresser fra økonomi- og driftsapper.

    ![Tidssoneinnstillingen for kontoen for systemadministratoren.](media/ADF-1.png)

2. Opprett følgende global parameter i Data Factory i **Administrer**-fanen under **Globale parameterere**.

    | Tall | Navn | Type | Verdi |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | streng | Denne parameteren legger til et serienummer i nyopprettede postadresser som et prefiks. Pass på at du oppgir en streng som ikke er i konflikt med postadresser i økonomi- og driftsapper og kundeengasjementsapper. Bruk eksempel **ADF-PAD-**. |

    ![Global parameter PostalAddressIdPrefix opprettet i kategorien Aministrer.](media/ADF-2.png)

3. Når du er ferdig, velg du **Publiser alle**.

    ![Publiser alle-knapp.](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>Oppsett for å kjøre malen for elektronisk partspostadresse

1. Opprett følgende globale parametere i Data Factory i **Administrer**-fanen under **Globale parameterere**.

    | Tall | Navn | Type | Verdi |
    |---|---|---|---|
    | 1 | IsFOSource | bool | Denne parameteren bestemmer hvilke hovedsystemadresser som erstattes ved konflikter. Hvis verdien er **sann**, vil primæradressene i økonomi- og driftsapper erstatte hovedadressene i kundeengasjementsapper. Hvis verdien er **usann**, vil primæradressene i kundeengasjementsapper erstatte hovedadressene i økonomi- og driftsapper. |
    | 2 | ElectronicAddressIdPrefix | streng | Denne parameteren legger til et serienummer i nyopprettede elektroniske adresser som et prefiks. Pass på at du oppgir en streng som ikke er i konflikt med elektroniske adresser i økonomi- og driftsapper og kundeengasjementsapper. Bruk eksempel **ADF-EAD-**. |

    ![Globale parametere IsFOSource og ElectronicAddressIdPrefix opprettet i kategorien Administrer.](media/ADF-4.png)

2. Når du er ferdig, velg du **Publiser alle**.

## <a name="run-the-templates"></a>Kjør malene

1. Stopp følgende dobbel skriving-tilordninger for **Part**, **Konto**, **Kontakt** og **Leverandør** som bruker økonomi- og driftsapper:

    + CDS-parter (msdyn_parties) 
    + Kunder V3 (kontoer)
    + Kunder V3 (kontakter)
    + CDS-kontakter V2 (kontakter)
    + CDS-kontakter V2 (kontakter)
    + Leverandør V2 (msdyn_vendor)
    + Kontakter V2 (msdyn_contactforparties)
    + Postadressesteder for CDS-part (msdyn_partypostaladdresses)
    + Historikk for CDS-postadresse V2 (msdyn_postaladdresses)
    + CDS-postadressesteder (msdyn_postaladdresscollections)
    + Partskontakter V3 (msdyn_partyelectronicaddresses)

2. Kontroller at tilordningene er fjernet fra **msdy_dualwriteruntimeconfig**-tabellen i Dataverse.
3. Installer [Løsninger for part med dobbel skriving og global adressebok](https://aka.ms/dual-write-gab) fra AppSource.
4. I økonomi- og driftsappen kjører du **Innledende synkronisering** for følgende tabeller hvis de inneholder data:

    + Hilsener
    + Typer personlige tegn
    + Avsluttende hilsen
    + Kontaktpersontitler
    + Roller for beslutningstaking
    + Fordelsnivåer

5. I Customer Engagement-appen deaktiverer du følgende trinn for plugin-moduler:

    + Kontooppdatering

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Oppdatering av konto
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Oppdatering av konto

    + Kontaktoppdatering

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Oppdatering av kontakt
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Oppdatering av kontakt

    + msdyn_party-oppdatering

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Oppdatering av msdyn_party

    + msdyn_vendor-oppdatering

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Oppdatering av msdyn_vendor

    + Customeraddress

        + Opprett

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: Opprettelse av customeraddress

        + Oppdater

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: Oppdatering av customeraddress

        + Slett

            + Microsoft.Dynamics.GABExtended.Plugins.DeleteCustomerAddress: Sletting av customeraddress

    + msdyn_partypostaladdress

        + Opprett

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Opprettelse av msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Opprettelse av msdyn_partypostaladdress

        + Oppdater

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Oppdatering av msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Oppdatering av msdyn_partypostaladdress

    + msdyn_postaladdress

        + Opprett

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: Opprettelse av msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: Opprettelse av msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Opprettelse av msdyn_postaladdress

        + Oppdater

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: Oppdatering av msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Oppdatering av msdyn_postaladdress

    + msdyn_partyelectronicaddress

        + Opprett

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Opprettelse av msdyn_partyelectronicaddress

        + Oppdater

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Oppdatering av msdyn_partyelectronicaddress

        + Slett

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: Sletting av msdyn_partyelectronicaddress

6. I Customer Engagement-appen deaktiverer du følgende arbeidsflyter:

    + Opprette leverandører i tabellen Kontoer
    + Opprette leverandører i tabellen Kontoer
    + Opprette leverandører av typen Person i tabellen Kontakter
    + Opprette leverandører av typen Person i tabellen Leverandører
    + Oppdatere leverandører i tabellen Kontoer
    + Oppdatere leverandører i tabellen Leverandører
    + Oppdatere leverandører av typen Person i tabellen Kontakter
    + Oppdatere leverandører av typen Person i tabellen Leverandører

7. I datafabrikken kjører du malen ved å velge **Utløs nå**, som vist på følgende illustrasjon. Det kan ta noen timer å fullføre denne prosessen basert på datavolumet.

    ![Kjøring av malen.](media/data-factory-trigger.png)

    > [!NOTE]
    > Hvis du har tilpasninger for **Konto**, **Kontakt** og **Leverandør**, må du endre malen.

8. Importer de nye **Part**-oppføringene til økonomi- og driftsappen.

    1. Last ned **FONewParty.csv**-filen fra Azure Blob Storage. Banen er **partybootstrapping/output/FONewParty.csv**.
    2. Konverter **FONewParty.csv**-filen til en Excel-fil, og importer Excel-filen til økonomi- og driftsappen. Hvis CSV-import fungerer for deg, kan du også importere CSV-filen direkte. Dette kan ta noen timer å fullføre denne prosessen basert på datavolumet. Hvis du vil ha mer informasjon, se [Oversikt over dataimport- og -eksportjobber](../data-import-export-job.md).

    ![Importere Dataverse partspostene.](media/data-factory-import-party.png)

9. I datafabrikken kjører du malene for postadresse for part og elektroniske adresse for part, en etter en.

    + Malen for partspostadresse upserter alle postadresseposter i kundeengasjementsappen, og knytter dem til tilsvarende **konto**, **kontakt** og **leverandør**-poster. Den genererer også tre .csv-filer: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv og ImportFONewPostalAddress.csv.
    + Malen for elektronisk postadresse for part upserter alle elektroniske adresser i kundeengasjementsappen, og knytter dem til tilsvarende **konto**, **kontakt** og **leverandør**-poster. Den genererer også én .csv-fil: ImportFONewElectronicAddress.csv.

    ![Kjøre malene for postadresse for part og elektronisk adresse for part.](media/ADF-7.png)

10. Hvis du vil oppdatere økonomi- og driftsappen med disse dataene, må du konvertere .csv-filene til en Excel-arbeidsbok og [importere den til økonomi- og driftsappen](../data-import-export-job.md). Hvis CSV-import fungerer for deg, kan du også importere CSV-filene direkte. Dette kan ta noen timer å fullføre denne prosessen basert på volumet.

    ![Vellykket importering.](media/ADF-8.png)

11. I Customer Engagement-appen aktiverer du følgende trinn for plugin-moduler:

    + Kontooppdatering

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Oppdatering av konto
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Oppdatering av konto

    + Kontaktoppdatering

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Oppdatering av kontakt
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Oppdatering av kontakt

    + msdyn_party-oppdatering

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Oppdatering av msdyn_party

    + msdyn_vendor-oppdatering

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Oppdatering av msdyn_vendor

    + msdyn_partypostaladdress

        + Opprett

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Opprettelse av msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Opprettelse av msdyn_partypostaladdress

        + Oppdater

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Oppdatering av msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Oppdatering av msdyn_partypostaladdress

    + msdyn_postaladdress

        + Opprett

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: Opprettelse av msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: Opprettelse av msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Opprettelse av msdyn_postaladdress

        + Oppdater

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: Oppdatering av msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Oppdatering av msdyn_postaladdress
 
    + msdyn_partyelectronicaddress

        + Opprett

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Opprettelse av msdyn_partyelectronicaddress

        + Oppdater

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Oppdatering av msdyn_partyelectronicaddress

        + Slett

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: Sletting av msdyn_partyelectronicaddress

12. I kundeengasjementsappen aktiverer du følgende arbeidsflyter hvis du tidligere har deaktivert dem:

    + Opprette leverandører i tabellen Kontoer
    + Opprette leverandører i tabellen Kontoer
    + Opprette leverandører av typen Person i tabellen Kontakter
    + Opprette leverandører av typen Person i tabellen Leverandører
    + Oppdatere leverandører i tabellen Kontoer
    + Oppdatere leverandører i tabellen Leverandører
    + Oppdatere leverandører av typen Person i tabellen Kontakter
    + Oppdatere leverandører av typen Person i tabellen Leverandører

13. Kjør de **parts**-postrelaterte tilordningene som er beskrevet i [Part og global adressebok](party-gab.md).

## <a name="explanation-of-the-data-factory-templates"></a>Forklaring av Data Factory-malene

Denne delen tar deg gjennom trinnene i hver Data Factory-mal.

### <a name="steps-in-the-party-template"></a>Trinn i partsmalen

1. Trinn 1 til og med 6 identifiserer firmaene som er aktivert for dobbel skriving, og bygger et filteruttrykk for dem.
2. Trinn 7-1 til og med 7-9 henter data fra både økonomi- og driftsappen og kundeengasjementsappen, og klargjør dataene for oppgradering.
3. Trinn 8 til og med 9 sammenligner partsnummeret for postene for **Konto**, **Kontakt** og **Leverandør** mellom økonomi- og driftsappen og kundeengasjementsappen. Eventuelle poster som ikke har partsnummer, blir ignorert.
4. Trinn 10 genererer to .csv-filer for partspostene som må opprettes i kundeengasjementsappen og økonomi- og driftsappen.

    - **FOCDSParty.csv**– Denne filen inneholder alle partsposter for begge systemer, uansett om firmaet er aktivert for dobbel skriving.
    - **FONewParty.csv** – Denne filen inneholder et delsett av partspostene som Dataverse er klar over (for eksempel kontoer av **kundeemne**-typen).

5. Trinn 11 oppretter partene i kundeengasjementsappen.
6. Trinn 12 henter de globale, unike identifikatorene til partene fra kundeengasjementsappen, og klargjør dem slik at de kan knyttes til **konto**, **kontakt** og **leverandør**-postene i påfølgende trinn.
7. Trinn 13 knytter postene **konto**, **kontakt** og **og leverandør** til partens GUIDer.
8. Trinn 14-1 til og med 14-3 oppdaterer postene for **konto**, **kontakt** og **leverandør** i kundeengasjementsappen med GUIDene for part.
9. Trinn 15-1 til og med 15-3 klargjør postene **Kontakt for part** for **konto**, **kontakt** og **leverandør**.
10. Trinn 16-1 til og med 16-7 henter referansedata som hilsener og personlige tegntyper, og knytter dem til **Kontakt for part**-poster.
11. Trinn 17 fletter **Kontakt for part**-postene for **konto**, **kontakt** og **leverandør**-postene.
12. Trinn 18 importerer **Kontakt for part**-postene til kundeengasjementsappen.

### <a name="steps-in-the-party-postal-address-template"></a>Trinn i malen for partspostadresse

1. Trinn 1-1 til og med 1-10 henter data fra både økonomi- og driftsappen og kundeengasjementsappen, og klargjør dataene for oppgradering.
2. Trinn 2 fjerner normaliseringen av postadressedataene i økonomi- og driftsappen ved å flette postadressen og partens postadresse.
3. Trinn 3 dedupliserer og fletter konto-, kontakt- og leverandøradressedata fra kundeengasjementsappen.
4. Trinn 4 oppretter .csv-filer for økonomi- og driftsappen for å opprette nye adressedata som er basert på konto-, kontakt- og leverandøradresser.
5. Trinn 5-1 oppretter .csv-filer for kundeengasjementsappen for å opprette alle adressedata basert på både økonomi- og driftsappen og kundeengasjementsappen.
6. Trinn 5-2 konverterer .csv-filene til Finance and Operations-importformatet for manuell import.

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. Trinn 6 importerer data for postadresseinnsamling til kundeengasjementsappen.
8. Trinn 7 henter data for postadresseinnsamling fra kundeengasjementsappen.
9. Trinn 8 oppretter kundeadressedata og knytter til en ID for postadresseinnsamling.
10. Trinn 9-1 til og med 9-2 knytter parts- og postadressesamlings-IDer med postadresser og postadresser til parter.
11. Trinn 10-1 til og med 10-3 importerer kundeadresser, postadresser og postadresser for parter til kundeengasjementsappen.

### <a name="steps-in-the-party-electronic-address-template"></a>Trinn i malen for elektronisk postadresse for part

1. Trinn 1-1 til og med 1-5 henter data fra både økonomi- og driftsappen og kundeengasjementsappen, og klargjør dataene for oppgradering.
2. Trinn 2 konsoliderer elektroniske adresser i kundeengasjementsappen fra konto-, kontakt- og leverandørenheter.
3. Trinn 3 fletter primære elektroniske adressedata fra kundeengasjementsappen og økonomi- og driftsappen.
4. Trinn 4 oppretter .csv-filer.

    - Opprett nye elektroniske adressedata for økonomi- og driftsappen, basert på konto-, kontakt- og leverandøradresser.
    - Opprett nye elektroniske adressedata for kundeengasjementsappen, basert på elektronisk adresse, konto, kontakt og leverandøradresser i økonomi- og driftsappen.

5. Trinn 5-1 importerer elektroniske adresser til kundeengasjementsappen.
6. Trinn 5-2 oppretter .csv-filer for å oppdatere primæradresser for kontoer og kontakter i kundeengasjementsappen.
7. Trinn 6-1 til og med 6-2 importerer primæradresser for kontoer og kontakter til kundeengasjementsappen.

## <a name="troubleshooting"></a>Feilsøking

1. Hvis prosessen mislykkes, kjører du datafabrikken på nytt. Start fra den mislykkede aktiviteten.
2. Enkelte filer som genereres av datafabrikken, kan brukes til datavalidering.
3. Datafabrikken kjøres basert på .csv-filer. Hvis det er en feltverdi som har komma, kan det derfor påvirke resultatene. Du må fjerne alle kommaer fra feltverdier.
4. Kategorien **Overvåking** inneholder informasjon om alle trinn og data som har blitt behandlet. Velg et bestemt trinn for å feilsøke det.

    ![Kategorien Overvåking.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Finn ut mer om malen

Du finner mer informasjon om malen i [Kommentarer for Viktig-filen for Azure Data Factory-malen](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).

