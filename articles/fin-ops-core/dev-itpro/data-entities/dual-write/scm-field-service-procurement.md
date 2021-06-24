---
title: Integrere innkjøp mellom Supply Chain Management og Field Service
description: Dette emnet beskriver hvordan integrering med dobbel skriving støtter oppretting og oppdatering av bestillinger fra både Supply Chain Management og Field Service.
author: RichardLuan
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: c50aabf94ae37b7b7b214699160bf958ad3ea9fd
ms.sourcegitcommit: 2cc14f6c537628e79ad2dd17dabf2c246deaa40d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6219793"
---
# <a name="integrate-procurement-between-supply-chain-management-and-field-service"></a>Integrere innkjøp mellom Supply Chain Management og Field Service

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management gir robust innkjøpsfunksjonalitet. Dynamics 365 Field Service gir lignende funksjonalitet som støtter innkjøpsprosessene som er knyttet til serviceprosessen. Funksjonaliteten i disse to appene er integrert via dobbel skriving, og de resulterende tverrfunksjonelle brukstilfellene aktiveres gjennom tabelltilordninger, løsningslogikk, visninger og skjemaer.

Denne integreringen støtter oppretting av bestillinger og, i de fleste tilfeller, oppdateringer fra begge appene. Supply Chain Management styrer imidlertid priser, adresser og produktkvitteringer. Flere kraftige tverrfunksjonelle brukstilfeller aktiveres for organisasjoner som bruker både Field Service og Supply Chain Management. Disse brukstilfellene gjør at innkjøp kan startes og spores på tvers av begge systemer.

Illustrasjonen nedenfor viser tabellene i begge systemene og hvordan de er tilordnet til hverandre. Bestillinger i Field Service refererer til en *konto* rad, mens bestillinger i Supply Chain Management refererer til en *leverandør* rad. For å løse integreringen bruker dobbel skriving en referanse til å koble *leverandør* rader til *konto* rader. Hvis du vil ha mer informasjon, kan du se [Integrert original for leverandør](vendor-mapping.md).

![Tilordninger for innkjøp](media/scm-field-service-tables.png)

## <a name="prerequisites"></a>Forutsetninger

Hvis du vil integrere Supply Chain Management med Field Service, må du installere følgende komponenter:

- Field Service versjon 8.8.31.60 eller nyere for omfattende bestillingsintegrering
- Supply Chain Management versjon 10.0.14 eller nyere
- Dobbel skriving for å kjøre OneFSSCM-løsningen

## <a name="installation-guidelines"></a>Retningslinjer for installasjon

### <a name="prerequisites"></a>Forutsetninger

- **Dobbel skriving** – Hvis du vil ha mer informasjon, kan du se [Startside for dobbel skriving](dual-write-home-page.md#dual-write-setup).
- **Dynamics 365 Field Service** – Hvis du vil ha mer informasjon, kan du se [Installere Dynamics 365 Field Service](/dynamics365/field-service/install-field-service#step-1-install-dynamics-365-field-service).

Når dobbel skriving og Field Service er aktivert i Microsoft Dataverse, innfører de flere løsningslag som utvider miljøet med nye metadata, skjemaer, visninger og logikk. Disse løsningene kan aktiveres i hvilken som helst rekkefølge, men installasjonen foretas vanligvis i denne rekkefølgen:

1. **Field Service Common** – Field Service Common installeres når Field Service installeres i miljøet.
2. **Field Service (Anchor)** – Field Service (Anchor) installeres når Field Service installeres i miljøet. 
3. **Supply Chain Management Extended** – Supply Chain Management Extended installeres automatisk når dobbel skriving aktiveres i et miljø. 
4. **OneFSSCM-løsning** – OneFSSCM installeres automatisk av løsningen (Field Service eller Supply Chain Management) som installeres sist.

    - Hvis Field Service allerede er installert i miljøet og du aktiverer dobbel skriving, som installerer Supply Chain Management Extended, installeres OneFSSCM.
    - Hvis Supply Chain Management Extended allerede er installert i miljøet og du installerer Field Service, installeres OneFSSCM.

## <a name="initial-synchronization"></a>Innledende synkronisering

Hvis du vil opprette nye bestillinger og arbeide med eksisterende bestillinger, må du synkronisere referansedataene mellom Supply Chain Management og Dataverse. Du bruker den innledende skrivefunksjonaliteten til å oppdage tabellrelasjonene og finne tabellene du må aktivere for en gitt tilordning.

Du må synkronisere følgende tabeller:

- Produktmaler

    Når du kjører den innledende skrivingen, får du en fullstendig liste over tabellene som kreves. Her er noen eksempler på disse malene:

    - Alle produkter
    - Frigitte produkter V2
    - Dataverse frigitte spesifikke produkter

- Siter
- Lagre
- Maler for innkjøpskategorier

    Her er noen eksempler på disse malene:

    - Innkjøpskategorier
    - Pro
    - Produktkategorihierarki
    - Produktkategoritilordninger

- Leverandørmaler, for eksempel Leverandør V2
- Maler for kontaktperson, for eksempel Dataverse-kontakter V2
- Arbeidermaler, for eksempel Arbeider

Synkronisering av tabellene sikrer at alle dokumenter (bestillinger og produktkvitteringer) i Supply Chain Management er tilgjengelige Dataverse.

### <a name="account-and-vendor-tables"></a>Konto- og leverandørtabeller

Bestillinger i Field Service er avhengige av kontotabellen for å spore leverandører. Dataverse-tabellene for bestillinger bruker derfor kontoer til å spore leverandører. For å ta hensyn til denne viktige forskjellen må følgende fire arbeidsflyter aktiveres for å holde kontoene og leverandørene synkronisert: 

- Opprette leverandører i tabellen Kontoer
- Opprette leverandører i tabellen Leverandører
- Oppdatere leverandører i tabellen Kontoer
- Oppdatere leverandører i tabellen Leverandører

Hvis OneFSSCM er installert fordi både Field Service og Supply Chain Management Extended er installert, aktiveres disse arbeidsflytene automatisk. Hvis Field Service ikke er installert, men du vil integrere bestillingstabellene med Dataverse, må du aktivere disse arbeidsflytene. Med mindre du starter fra grunnen av, må du i begge tilfeller kanskje sikre at alle leverandører opprettes som kontoer i Dataverse før du oppretter bestillinger. Hvis ikke kan det oppstå feil.

### <a name="initial-synchronization"></a>Innledende synkronisering

Når alle forutsetningene er på plass, må du foreta en innledende synkronisering av følgende maler hvis du vil at eksisterende bestillinger og produktkvitteringer skal være tilgjengelige i begge systemene:

- Bestillingshode V2
- CDS-bestillingslinje
- Myk sletting av CDS-bestillingslinje
- Bestillingsmottak
- Produkt for bestillingsmottak

## <a name="mappings-with-logic"></a>Tilordninger med logikk

Innkjøpsintegrasjonen utvider produkttilordningen med følgende logikk for å sikre at kolonnen **Produkttype for Field Service** blir riktig angitt i produkttabellen i Dataverse:

- Hvis **Produkttype** er satt til *Produkt* og **Varemodellgruppe, Lagerført produkt** er satt til *Sann*, settes **Produkttype for Field Service** til *Lager*.
- Hvis **Produkttype** er satt til *Produkt* og **Varemodellgruppe, Lagerført produkt** er satt til *Usann*, settes **Produkttype for Field Service** til *Ikke-lager*.
- Hvis **Produkttype** er satt til *Tjeneste*, settes **Produkttype for Field Service** til *Tjeneste*.

Dataverse omfatter i tillegg logikk som tilordner leverandører til de tilknyttede kontoene. Denne logikken angir standard leverandørkonto for faktura. Ved opprettelse angir logikk i programtillegg på serversiden standard leverandørkonto for faktura fra leverandøren som er knyttet til kontoen. Leverandøren har en referanse til fakturakontoen som brukes til å angi denne verdien.

## <a name="supported-scenarios"></a>Scenarier som støttes

- Bestillinger kan opprettes og oppdateres av Dataverse-brukere. Prosessen og dataene styres imidlertid av Supply Chain Management. Begrensningene for oppdatering av bestillingskolonner i Supply Chain Management gjelder når oppdateringer kommer fra Field Service. Du kan for eksempel ikke oppdatere en bestilling hvis den er fullført. 
- Hvis bestillingen styres av endringsadministrasjon i Supply Chain Management, kan en Field Service-bruker bare oppdatere bestillingen når godkjenningsstatusen for Supply Chain Management er *Utkast*.
- Flere kolonner administreres bare av Supply Chain Management og kan ikke oppdateres i Field Service. Du kan finne ut hvilke kolonner som ikke kan oppdateres, ved å se gjennom tilordningstabellene i produktet. For enkelhets skyld blir de fleste av disse kolonnene satt til skrivebeskyttet på Dataverse-sider. 

    Kolonnene for prisinformasjon administreres for eksempel av Supply Chain Management. Supply Chain Management har forretningsavtaler som Field Service kan dra nytte av. Kolonner som **Enhetspris**, **Rabatt** og **Nettobeløp** kommer bare fra Supply Chain Management. For å sikre at prisen blir synkronisert til Field Service, bruker du funksjonen **Synkroniser** på sidene **Bestilling** og **Bestillingsprodukt** i Dataverse etter at bestillingsdata er angitt. Hvis du vil ha mer informasjon, kan du se [Synkronisere med prissettingsmotoren i Dynamics 365 Supply Chain Management ved forespørsel](#sync-procurement).

- **Totaler**-kolonnen er bare tilgjengelig i Field Service fordi det ikke finnes noen oppdaterte totaler i bestillingen i Supply Chain Management. Totalene i Supply Chain Management beregnes basert på flere parametere som ikke er tilgjengelige i Field Service.
- Bestillingslinjer der bare en innkjøpskategori er angitt, eller der produktet som er angitt, er en vare av produkttypen *Tjeneste* eller Field Service, kan bare startes i Supply Chain Management. Linjene synkroniseres deretter til Dataverse og vises i Field Service.
- Hvis bare Field Service er installert, ikke Supply Chain Management, er **Lager**-kolonnen obligatorisk i bestillingen. Hvis Supply Chain Management imidlertid er installert, gjelder ikke alltid dette kravet fordi Supply Chain Management i bestemte situasjoner tillater bestillingslinjer der ingen lagre er angitt.
- Produktkvitteringer (bestillingsmottak i Dataverse) administreres av Supply Chain Management og kan ikke opprettes fra hvis Dataverse hvis Supply Chain Management er installert. Produktkvitteringene fra Supply Chain Management synkroniseres fra Supply Chain Management til Dataverse.
- Underlevering er tillatt i Supply Chain Management. OneFSSCM-løsningen tilføyer logikk som gjør at det opprettes en lagerjournalrad i Dataverse når produktkvitteringslinjen (eller bestillingsmottaksproduktet i Dataverse) opprettes eller oppdateres, for å justere restantallet i ordren for underleveringsscenarioer.

## <a name="unsupported-scenarios"></a>Scenarier som ikke støttes

- Field Service forhindrer at linjer legges til i en annullert bestilling i Supply Chain Management. Du omgå dette ved å endre systemstatusen for bestillingen i Field Service og deretter legge til den nye linjen i Field Service eller Supply Chain Management.
- Selv om innkjøpsrader påvirker lagernivåer i begge systemene, sikrer ikke denne integreringen lagerjustering på tvers av Supply Chain Management og Field Service. Både Field Service og Supply Chain Management har andre prosesser som oppdaterer lagernivåer. Disse prosessene er utenfor innkjøpsområdet.

## <a name="status-management"></a>Statusadministrasjon

Statusene til bestillinger i Field Service er forskjellige fra statusene i Supply Chain Management.

### <a name="field-service-purchase-order-and-purchase-order-product-statuses"></a>Statuser for bestillinger og bestillingsprodukter i Field Service

| Hode – Systemstatus | Hode – Godkjenningsstatus | Varestatus |
|---|---|---|
| <ul><li>Utkast</li><li>Sendt inn</li><li>Annullert</li><li>Produkt mottatt</li><li>Fakturert</li></ul> | <ul><li>Null</li><li>Godkjent</li><li>Avvist</li></ul> | <ul><li>Uavsluttet</li><li>Mottatt</li><li>Annullert</li></ul> |

### <a name="supply-chain-management-purchase-order-and-purchase-order-line-statuses"></a>Statuser for bestillinger og bestillingslinjer i Supply Chain Management

Linjegodkjenningsstatuser er bare aktive når det finnes en linjearbeidsflyt.

| Hode – dokumentstatus | Hode – Godkjenningsstatus | Linjestatus | Linjegodkjenningsstatus |
|---|---|---|---|
| <ul><li>Åpen ordre (restordre)</li><li>Mottatt</li><li>Fakturert</li><li>Annullert</li></ul> | <ul><li>Utkast</li><li>Til gjennomgang</li><li>Godkjent</li><li>Avvist</li><li>Til ekstern vurdering</li><li>Bekreftet</li><li>Sluttført</li></ul> | <ul><li>Åpen ordre (restordre)</li><li>Mottatt</li><li>Fakturert</li><li>Annullert</li></ul> | <ul><li>Ikke sendt inn</li><li>Til gjennomgang</li><li>Godkjent</li><li>Avvist</li></ul> |

Følgende regler brukes på statuskolonnene:

- Statusen i Supply Chain Management kan ikke oppdateres fra Field Service. I enkelte tilfeller oppdateres imidlertid statusen i Field Service når bestillingsstatusen i Supply Chain Management endres.
- Hvis en bestilling i Supply Chain Management er under endringsadministrasjon og en endring behandles, er godkjenningsstatusen *Utkast* eller *Til vurdering*. I dette tilfellet settes godkjenningsstatusen i Field Service til *Null*.
- Hvis godkjenningsstatusen for bestillingen i Supply Chain Management er satt til *Godkjent*, *Til ekstern vurdering*, *Bekreftet* eller *Sluttført*, settes godkjenningsstatusen for bestillingen i Field Service til *Godkjent*.
- Hvis godkjenningsstatusen for bestillingen i Supply Chain Management er satt til *Avvist*, settes godkjenningsstatusen for bestillingen i Field Service til *Avvist*.
- Hvis dokumenthodestatusen i Supply Chain Management endres til *Åpen ordre (restordre)* og bestillingsstatusen i Field Service er *Utkast* eller *Annullert*, endres bestillingsstatusen i Field Service til *Sendt inn*.
- Hvis dokumenthodestatusen i Supply Chain Management endres til *Annullert* og ingen bestillingsmottaksprodukter i Field Service er knyttet til bestillingen (via bestillingsprodukter), settes systemstatusen i Field Service til *Annullert*.
- Hvis bestillingslinjestatusen i Supply Chain Management er *Annullert*, settes statusen for bestillingsprodukt i Field Service til *Annullert*. Hvis bestillingslinjestatusen i Supply Chain Management i tillegg endres fra *Annullert* til *Restordre*, settes statusen for bestillingsproduktvaren i Field Service til *Ventende*.

## <a name="sync-with-the-supply-chain-management-procurement-data-on-demand"></a><a id="sync-procurement"></a>Synkronisere med innkjøpsdata i Supply Chain Management ved behov

Supply Chain Management omfatter innkjøpsdata som håndterer forretningsavtaler, rabatter og andre scenarioer som er avhengige av sekundære prosesser i Supply Chain Management. Innkjøpsmotoren bruker komplekse regler til å bestemme den beste prisen for en gitt bestilling. Når du bruker dobbel skriving, er ikke alltid dataene i de to miljøene synkronisert, særlig i scenarioer der raden ble opprettet eller oppdatert fra Dataverse og kan utløse oppfølgingsprosesser i Supply Chain Management.

## <a name="sync-the-procurement-data-from-supply-chain-management"></a>Synkronisere innkjøpsdataene fra Supply Chain Management

1. I Dataverse går du til **Lager \> Bestilling**.
2. Velg **Ny** for å opprette en ny bestilling, eller velg raden for en eksisterende bestilling.
3. Fra bestillingen eller bestillingslinjen.
4. I handlingsruten velger du **Synkroniser**.

Alle kolonner fra Dataverse og Field Service som deles av Supply Chain Management, synkroniseres.

Her er situasjonene der du kan bruke **Synkroniser**-funksjonen:

- Hvis du gjør flere endringer etter hverandre i samme rad fra Dataverse, kjører du **Synkroniser**-funksjonen.
- Hvis du ikke er sikker på om en endring kan være den andre påfølgende endringen fra Dataverse, kan det være fornuftig å kjøre **Sykroniser**-funksjonen.
- Hvis du får en feilmelding om oppdatering av en verdi fra Supply Chain Management, kjører du **Synkroniser**-funksjonen, og deretter prøver du oppdateringen på nytt i Dataverse.

## <a name="cancelling-the-posting-process"></a>Avbryte posteringsprosessen

Hvis posteringsprosessen for produktkvittering avbrytes under behandling, kan det hende at dobbel skriving oppretter en produktkvitteringsrad i Dataverse, men ikke i Supply Chain Management. Denne situasjonen oppstår fordi dobbel skriving ikke støtter distribuerte transaksjoner.

## <a name="templates"></a>Maler

Følgende maler er tilgjengelige for integrering av innkjøpsrelaterte dokumenter.

| Forsyningskjedeadministrasjon | Field Service | beskrivelse |
|---|---|---|
| [Bestillingshode V2](mapping-reference.md#183) | msdyn\_Purchaseorders | Denne tabellen inneholder kolonnene som representerer bestillingshodet. |
| [Bestillingslinjeenhet](mapping-reference.md#181) | msdyn\_PurchaseOrderProducts | Denne tabellen inneholder radene som representerer linjer i en bestilling. Produktnummeret brukes til synkronisering. Dette identifiserer produktet som en lagerenhet (SKU), inkludert produktdimensjoner. Hvis du vil ha mer informasjon om produktintegrering med Dataverse, kan du se [Samlet produktopplevelse](product-mapping.md). |
| [Mottaksseddelhode](mapping-reference.md#185) | msdyn\_purchaseorderreceipts | Denne tabellen inneholder produktkvitteringshoder som opprettes når en produktkvittering posteres i Supply Chain Management. |
| [Mottaksseddellinje](mapping-reference.md#184) | msdyn\_purchaseorderreceiptproducts | Denne tabellen inneholder produktkvitteringslinjer som opprettes når en produktkvittering posteres i Supply Chain Management. |
| [Myk sletting av enhet for bestillingslinje](mapping-reference.md#182) | msdyn\_purchaseorderproducts | Denne tabellen inneholder informasjon om bestillingslinjer som er mykt slettet. En bestillingslinje i Supply Chain Management kan bare slettes mykt når bestillingen er bekreftet eller godkjent, hvis endringsadministrasjon er aktivert. Raden er i databasen i Supply Chain Management og er merket som **IsDeleted**. Siden Dataverse ikke har et begrep om myk sletting, er det viktig at denne informasjonen synkroniseres med Dataverse. Dermed kan linjer som er mykt slettet i Supply Chain Management, slettes fra Dataverse automatisk. I dette tilfellet er logikken for sletting av en linje i Dataverse, i Supply Chain Management Extended. |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
