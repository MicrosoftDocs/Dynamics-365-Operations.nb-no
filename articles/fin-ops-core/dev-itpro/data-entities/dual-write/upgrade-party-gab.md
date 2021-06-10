---
title: Oppgrader til parten og den globale adressebokmodellen
description: Dette emnet beskriver hvordan du oppgraderer data for dobbel skriving til partsmodellen og den globale adressebokmodellen.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112679"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Oppgrader til parten og den globale adressebokmodellen

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Med [Microsoft Azure Data Factory-malen](https://aka.ms/dual-write-gab-adf) kan du oppgradere eksisterende **Konto**, **Kontakt** og **Leverandør**-tabelldata i dobbel skriving til partsmodellen og den globale adressebokmodellen. Malen avstemmer dataene fra både Finance and Operations-apper og Customer Engagement-apper. På slutten av prosessen vil **Part**- og **Kontakt**-felter for **Part**-oppføringer opprettes og knyttes til **Konto**, **Kontakt** og **Leverandør**-oppføringer i Customer Engagement-programmer. En .csv-fil (`FONewParty.csv`) genereres for å opprette nye **Part**-oppføringer i Finance and Operations-appen. I dette emnet finner du instruksjoner om hvordan du kan bruke Data Factory-malen og oppgradere dataene.

Hvis du ikke har noen tilpasninger, kan du bruke malen som den er. Hvis du har tilpasninger for **Konto**, **Kontakt** og **Leverandør**, må du endre malen ved å følge instruksjonene nedenfor.

> [!NOTE]
> Malen oppgraderer bare **Part**-dataene. I en fremtidig versjon blir postadresser og elektroniske adresser inkludert.

## <a name="prerequisites"></a>Forutsetninger

Følgende forutsetninger kreves for å oppgradere til parten og den globale adressebokmodellen:

+ [Azure-abonnement](https://portal.azure.com/)
+ [Tilgang til malen](https://aka.ms/dual-write-gab-adf)
+ Du må være en eksisterende kunde med dobbel skriving.

## <a name="prepare-for-the-upgrade"></a>Forberede for oppgraderingen
Følgende aktiviteter er nødvendige for å forberede for oppgraderingen:

+ **Fullstendig synkronisert**: Begge miljøene er i en fullstending synkronisert tilstand for **Konto (kunde)**, **Kontakt** og **Leverandør**.
+ **Integrasjonsnøkler**: Tabellene **Konto (kunde)**, **Kontakt** og **Leverandør** i Customer Engagement-apper bruker de medfølgende integrasjonsnøklene. Hvis du har tilpasset integrasjonsnøklene, må du tilpasse malen.
+ **Partsnummer**: Alle oppføringer av typen **Konto (kunde)**, **Kontakt** og **Leverandør** som skal oppgraderes, har et **partsnummer**. Oppføringer uten et **partsnummer** blir ignorert. Hvis du vil oppgradere disse oppføringer, legger du til et **partsnummer** før du starter oppgraderingsprosessen.
+ **Systembrudd**: Under oppgraderingsprosessen må du koble fra både Finance and Operations- og Customer Engagement-miljøer.
+ **Øyeblikksbilde**: Ta øyeblikksbilder både av Finance and Operations- og Customer Engagement-appene. Bruk øyeblikksbildene til å gjenopprette den forrige tilstanden hvis du ønsker det.

## <a name="deployment"></a>Distribusjon

1. Last ned malen fra [Dynamics-365-FastTrack-Implementering-Ressurser](https://aka.ms/dual-write-gab-adf).

2. Logg på [Microsoft Azure](https://portal.azure.com/).

3. Opprett en [ressursgruppe](/azure/azure-resource-manager/management/manage-resource-groups-portal).

4. Opprett en [lagringskonto](/azure/storage/common/storage-account-create?tabs=azure-portal) i ressursgruppen som du opprettet.

5. Opprett en [datafabrikk](/azure/data-factory/quickstart-create-data-factory-portal) i ressursgruppen som du opprettet ovenfor.

6. Åpne datafabrikken og velg flisen **Forfatter og overvåking**.

7. På **Administrer**-fanen velger du **ARM-mal**.

8. Velg **Importer ARM-mal** for å importere **partsmalen**.

9. Importer malen til datafabrikken. Angi følgende verdier for **Prosjektdetalj** og **Forekomstdetaljer**.

    Felt | Verdi
    ---|---
    Abonnement | Azure-abonnement
    Ressursgruppe | Oppgi den samme ressursen som lagringskontoen opprettes under.
    Område | Angi område.
    Fabrikknavn | Angi fabrikknavnet.
    FO Linked Service_service Principal Key | Angi nøkkkelen til programmet.
    Azure Blob Storage_connection String | Tilkoblingsstreng for Azure Blob Storage
    Dynamics Crm Linked Service_password | Passordet for brukerkontoen du har oppgitt som brukernavnet.
    FO Linked Service_properties_type Properties_url  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    FO Linked Service_properties_type Properties_tenant | Angi leierinformasjonen (domenenavn eller leier-ID) som appen ligger under.
    FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com`
    FO Linked Service_properties_type Properties_service Principal Id | Angi klient-ID-en til programmet.
    Dynamics Crm Linked Service_properties_type Properties_username | Brukernavnet for å koble til Dynamics 365.

    Hvis du vil ha mer informasjon, kan du se ett av følgende emner: 
    
    - [Forfremme en Resource Manager-mal for hvert miljø manuelt](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Tilkoblede tjenesteegenskaper](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Kopiere data ved hjelp av Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Etter distribusjonen validerer du datasettene, dataflyten og den tilkoblede tjenesten til datafabrikken.

   ![Datasett, dataflyt og tilknyttet tjeneste](media/data-factory-validate.png)

11. Naviger til **Administrer**. Under **Tilkoblinger** velger du **Tilknyttet tjeneste**. Velg **DynamicsCrmLinkedService**. I skjemaet **Rediger tilknyttet tjeneste (Dynamics CRM)** angir du følgende verdier.

    Felt | Verdi
    ---|---
    Navn | DynamicsCrmLinkedService
    beskrivelse | Tilknyttede tjenester for tilkobling til CRM-forekomsten for å hente data for enheter
    Tilkobling via integrasjonskjøretid | AutoResolvelntegrationRuntime
    Distribusjonstype | Tilkoblet
    Tjeneste-URI | `https://<organization-name>.crm[x].dynamics.com`
    Godkjenningstype | Office365
    Brukernavn |
    Passord eller Azure Key Vault | Passord
    Passord |

## <a name="run-the-template"></a>Kjør malen

1. Stopp følgende dobbel skriving-tilordninger for **Konto**, **Kontakt** og **Leverandør** ved å bruke Finance and Operations-appen.

    + Kunder V3 (kontoer)
    + Kunder V3 (kontakter)
    + CDS-kontakter V2 (kontakter)
    + CDS-kontakter V2 (kontakter)
    + Leverandør V2 (msdyn_vendor)

2. Kontroller at kartene er fjernet fra `msdy_dualwriteruntimeconfig`-tabellen i Dataverse.

3. Installer [Løsninger for part med dobbel skriving og global adressebok](https://aka.ms/dual-write-gab) fra AppSource.

4. Hvis tabellene nedenfor i Finance and Operations-appen inneholder data, kjører du **Innledende synkronisering** for dem.

    + Hilsener
    + Typer personlige tegn
    + Avsluttende hilsen
    + Kontaktpersontitler
    + Roller for beslutningstaking
    + Fordelsnivåer

5. I Customer Engagement-appen deaktiverer du følgende trinn for plugin-moduler.

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

6. I Customer Engagement-appen deaktiverer du følgende arbeidsflyter:

    + Opprette leverandører i tabellen Kontoer
    + Opprette leverandører i tabellen Kontoer
    + Opprette leverandører av typen Person i tabellen Kontakter
    + Opprette leverandører av typen Person i tabellen Leverandører
    + Oppdatere leverandører i tabellen Kontoer
    + Oppdatere leverandører i tabellen Leverandører
    + Oppdatere leverandører av typen Person i tabellen Kontakter
    + Oppdatere leverandører av typen Person i tabellen Leverandører

7. I datafabrikken kjører du malen ved å velge **Utløs nå**, som vist på følgende bilde. Det kan ta noen timer å fullføre denne prosessen basert på datavolumet.

    ![Utløserkjøring](media/data-factory-trigger.png)

    > [!NOTE]
    > Hvis du har tilpasninger for **Konto**, **Kontakt** og **Leverandør**, må du endre malen.

8. Importer de nye **partsoppføringene** i Finance and Operations-appen.

    + Last ned `FONewParty.csv`-filen fra Azure Blob Storage. Banen er `partybootstrapping/output/FONewParty.csv`.
    + Konverter `FONewParty.csv`-filen til en Excel-fil, og importer Excel-filen til Finance and Operations-appen. Hvis CSV-import fungerer for deg, kan du importere CSV-filen direkte. Importen kan ta noen timer å kjøre, avhengig av datavolumet. Hvis du vil ha mer informasjon, se [Oversikt over dataimport- og -eksportjobber](../data-import-export-job.md).

    ![Importer Datavers-partsoppføringene](media/data-factory-import-party.png)

9. I Customer Engagement-appen aktiverer du følgende trinn for plugin-moduler:

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

10. I Customer Engagement-appene aktiverer du følgende arbeidsflyter hvis du deaktiverte dem i de forrige trinnene:

    + Opprette leverandører i tabellen Kontoer
    + Opprette leverandører i tabellen Kontoer
    + Opprette leverandører av typen Person i tabellen Kontakter
    + Opprette leverandører av typen Person i tabellen Leverandører
    + Oppdatere leverandører i tabellen Kontoer
    + Oppdatere leverandører i tabellen Leverandører
    + Oppdatere leverandører av typen Person i tabellen Kontakter
    + Oppdatere leverandører av typen Person i tabellen Leverandører

11. Kjør de **partsrelaterte** kartene ved å følge instruksjonene i [Part og global adressebok](party-gab.md).

## <a name="troubleshooting"></a>Feilsøking

1. Hvis prosessen mislykkes, kjører du datafabrikken på nytt fra den mislykkede aktiviteten.
2. Enkelte filer genereres av datafabrikken som du kan bruke til datavalideringsformål.
3. Datafabrikken kjøres basert på csv-filer som er kommadelt. Hvis det er en feltverdi som har komma, kan det påvirke resultatene. Du må fjerne kommaene.
4. Kategorien **Overvåking** inneholder informasjon om alle trinn og data som behandles. Velg et bestemt trinn for å feilsøke det.

    ![Kategorien Overvåking](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Finn ut mer om malen

Du finner mer informasjon om malen i [Kommentarer for Viktig-filen for Azure Data Factory-malen](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).
