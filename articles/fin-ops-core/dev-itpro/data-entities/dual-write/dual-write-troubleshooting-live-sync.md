---
title: Feilsøke problemer med direkte synkronisering
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer med direkte synkronisering.
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: df184decdfa900ccb5c2070575e55052b9dfc547
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062369"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Feilsøke problemer med direkte synkronisering

[!include [banner](../../includes/banner.md)]



Dette emnet inneholder feilsøkingsinformasjon om integrasjon av dobbel skriving mellom økonomi- og driftsapper og Microsoft Dataverse. Det inneholder særlig informasjon som kan hjelpe deg med å løse problemer med direkte synkronisering.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Azure Active Directory (Azure AD)-leieradministrator. Hver del forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>Direkte synkronisering viser en feil når du oppretter en rad

Du kan få følgende feilmelding når du oppretter en rad i en økonomi- og driftsapp:

*\[{\\"feil\\":{\\"kode\\":\\"0x80072560\\",\\"melding\\":\\"Brukeren er ikke medlem av organisasjonen.\\"}}\], Den eksterne serveren returnerte en feil: (403) Forbudt."}}".*

Hvis du vil løse problemet, følger du fremgangsmåten under [Systemkrav og forutsetninger](requirements-and-prerequisites.md). Hvis du vil fullføre disse trinnene, må brukerne avdobbel skriving-programmet som er opprettet i Dataverse, ha rollen som systemadministrator. Standard eiende team må også ha rollen som systemadministrator.

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>Direkte synkronisering viser en feil når du prøver å lagre tabelldata

**Nødvendig rolle for å løse problemet:** Systemadministrator

Du kan få følgende feilmelding når du prøver å lagre tabelldata i en økonomi- og driftsapp:

*Kan ikke lagre endringene i databasen. Arbeidsenhet kan ikke utføre transaksjonen. Kan ikke skrive data til måleenheter. Skriving til UnitOfMeasureEntity mislyktes med feilmeldingen Kan ikke synkronisere med måleenheter.*

Hvis du vil løse problemet, må du kontrollere at de nødvendige referansedataene finnes i både økonomi- og driftsappen og Dataverse. Hvis for eksempel en kundepost tilhører en bestemt kundegruppe, må du kontrollere at kundegruppen finnes i Dataverse.

Hvis det finnes data på begge steder, og du har bekreftet at problemet ikke er relatert til data, følger du denne fremgangsmåten.

1. Åpne **DualWriteProjectConfigurationEntity**-enheten ved hjelp av Excel-tillegget. Hvis du vil bruke tillegget, aktiverer du utformingsmodus i Excel-tillegget for økonomi og drift og legger til **DualWriteProjectConfigurationEntity** i et regneark. Hvis du vil ha mer informasjon, kan du se [Vis og oppdater enhetsdata med Excel](../../office-integration/use-excel-add-in.md).
2. Velg og slett postene som har problemer i tilordningen for dobbel skriving og prosjektet. Det blir to poster for hver tilordning av dobbel skriving.
3. Publiser endringene ved hjelp av Excel-tillegget. Dette trinnet er viktig fordi det sletter postene fra enheten og underliggende tabeller.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Håndtere lese- eller skrivetilgangsfeil når du oppretter data i en økonomi- og driftapp

Du kan få feilmeldingen "Ugyldig forespørsel" når du oppretter data i en økonomi- og driftsapp.

![Eksempel på feilmeldingen om Ugyldig forespørsel.](media/error_record_id_source.png)

Hvis du vil løse problemet, må du aktivere den manglende rettigheten ved å tilordne den riktige sikkerhetsrollen til teamet for de tilordnede forretningsenhetene for Dynamics 365 Sales eller Dynamics 365 Customer Service.

1. I økonomi- og driftsappen finner du forretningsenheten som er tilordnet i tilkoblingssettet for dataintegrering.

    ![Organisasjonstilordning.](media/mapped_business_unit.png)

2. Logg deg på miljøet i kundeengasjementsappen, gå til **Innstilling \> Sikkerhet**, og finn teamet til den tilordnede forretningsenheten.

    ![Team til den tilordnede forretningsenheten.](media/setting_security_page.png)

3. Åpne siden for teamet for redigering, og velg deretter **Behandle roller**.

    ![Knappen Behandle roller.](media/manage_team_roles.png)

4. Tilordne rollen som har lese-/skrivetilgang for de relevante tabellene, i dialogboksen **Behandle grupperoller**, og velg deretter **OK**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Rette opp synkroniseringsproblemer i et miljø som har et nylig endret Dataverse-miljø

**Nødvendig rolle for å løse problemet:** Systemadministrator

Du kan få følgende feilmelding når du oppretter data i en økonomi- og driftsapp:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Kan ikke generere nyttelast for enhet CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Oppretting av nyttelast mislyktes med feilen Ugyldig URI: URI-en er tom."}\],"isErrorCountUpdated":true}*

Slik ser feilmeldingen ut i kundeengasjementsappen:

> Det oppstod en uventet feil fra ISV-kode. (ErrorType = ClientError) Uventet unntak fra plugin-modul (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: kan ikke behandle enhetskonto - Et tilkoblingsforsøk mislyktes fordi den tilkoblede parten ikke svarte riktig etter en tidsperiode, eller opprettet tilkobling mislyktes fordi den tilkoblede verten ikke svarer.

Denne feilen oppstår hvis Dataverse-miljøet tilbakestilles feil samtidig som du prøver å opprette data i økonomi- og driftsappen.

> [!IMPORTANT]
> Hvis du har koblet miljøene på nytt, må du stoppe alle enhetstilordningene før du fortsetter med reduksjonstrinnene.

Hvis du vil rette på problemet, må du fullføre trinnene i både Dataverse og økonomi- og driftsappen.

1. Følg trinnene nedenfor i økonomi- og driftsappen:

    1. Åpne **DualWriteProjectConfigurationEntity**-enheten ved hjelp av Excel-tillegget. Hvis du vil bruke tillegget, aktiverer du utformingsmodus i Excel-tillegget for økonomi og drift og legger til **DualWriteProjectConfigurationEntity** i et regneark. Hvis du vil ha mer informasjon, kan du se [Vis og oppdater enhetsdata med Excel](../../office-integration/use-excel-add-in.md).
    2. Velg og slett postene som har problemer i tilordningen for dobbel skriving og prosjektet. Det blir to poster for hver tilordning av dobbel skriving.
    3. Publiser endringene ved hjelp av Excel-tillegget. Dette trinnet er viktig fordi det sletter postene fra enheten og underliggende tabeller.
    4. For å forhindre feil når du kobler sammen økonomi- og driftsmiljøet eller Dataverse-miljøet på nytt, må du sørge for at det ikke gjenstår noen dobbel skriving-konfigurasjoner.

2. Følg disse trinnene i Dataverse:

    1. Logg på Dataverse miljøet (for eksempel `https://*****.crm.dynamics.com/`).
    2. Gå til **Avanserte innstillinger** \> **Avansert søk**.
    3. Velg **Konfigurasjon av DualWrite-kjøretid**.
    4. Velg kolonnen du vil se.
    5. Velg **Resultater** for å vise konfigurasjonene.
    6. Slett alle forekomstene.

3. Følg trinnene nedenfor i økonomi- og driftsappen:

    1. Åpne **DualWriteProjectConfigurationEntity**-enheten ved hjelp av Excel-tillegget. Hvis du vil bruke tillegget, aktiverer du utformingsmodus i Excel-tillegget for økonomi og drift og legger til **DualWriteProjectConfigurationEntity** i et regneark. Hvis du vil ha mer informasjon, kan du se [Vis og oppdater enhetsdata med Excel](../../office-integration/use-excel-add-in.md).
    2. Velg og slett postene som har problemer i tilordningen for dobbel skriving og prosjektet. Det blir to poster for hver tilordning av dobbel skriving.
    3. Publiser endringene ved hjelp av Excel-tillegget. Dette trinnet er viktig fordi det sletter postene fra enheten og underliggende tabeller.
    4. For å forhindre feil når du kobler sammen økonomi- og driftsmiljøet eller Dataverse-miljøet på nytt, må du sørge for at det ikke gjenstår noen dobbel skriving-konfigurasjoner.

## <a name="live-synchronization-error-after-you-do-a-full-database-copy"></a>Direkte synkroniseringsfeil etter at du har gjort en full databasekopi

Du kan få følgende feilmelding når du har kjørt en full databasekopi fra ett system til et annet og deretter prøve å kjøre en databaseoperasjon:

*SecureConfig-organisasjon (???) samsvarer ikke med faktiske CRM-organisasjoner (???).*

Feilmeldingen vises fra kjøretids-programtillegget for dobbel skriving for å sikre at dobbel skriving-konfigurasjonen som er definert i ett system, ikke kan brukes i et annet system.

Hvis du vil rette opp problemet, sletter du alle postene **i msdyn_dualwriteruntimeconfig** etter at du har gjenopprettet databasen. Hvis du vil ha mer informasjon, kan du se [Fjern kobling til og koble til miljøer for dobbel skriving på nytt](relink-environments.md).

## <a name="live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps"></a>Direkte synkroniseringsproblemer som forårsakes av feil syntaks i spørringsfilteret for dobbel skriving-tilordninger

Selv om spørringsuttrykket for en dobbel skriving-tilordning er syntaktisk riktig, kan det være at det ikke fungerer som forventet. Filteruttrykket er på en enhet, ikke en enkelt datakilde for et spørringsobjekt. Derfor vil ikke SQL-spørringen som genereres, returnere de forventede resultatene.

Her er et eksempel:

```dos
Query entity = PROJECTENTITY
Query expression = (ParentProject == "")
```

Du kan forvente at prosjekter som ikke har overordnede, skal filtreres ut. Filteret fungerer imidlertid ikke, fordi det er oversatt til en spørring som ligner på eksemplet nedenfor.

```sql
SELECT T1.RECID,T1.MODIFIEDDATETIME,T1.RECVERSION,T1.RECID,T1.DIMENSION,
T1.LOCATION,T1.PROJECTCONTROLLER,T1.PROJECTID,T1.PROJECTMANAGER,T1.REFERENCE,
T1.SALESMANAGER,T1.SCHEDULED,T1.RECVERSION#8,T1.RECVERSION#7,
T1.RECVERSION#6,T1.RECVERSION#5,T1.RECVERSION#4,T1.RECVERSION#3,
T1.RECVERSION#2,T1.RECID#8,T1.RECID#7,T1.RECID#6,T1.RECID#5,
T1.RECID#4,T1.RECID#3,T1.RECID#2,T1.PARTITION FROM PROJECTENTITY T1 
WHERE(((((((((((PARTITION=5637144576) AND (DATAAREAID=N'usmf')) AND 
((PARTITION#2=5637144576) OR (PARTITION#2 IS NULL))) AND 
((PARTITION#3=5637144576) OR (PARTITION#3 IS NULL))) AND 
((PARTITION#4=5637144576) OR (PARTITION#4 IS NULL))) AND 
((PARTITION#5=5637144576) OR (PARTITION#5 IS NULL))) AND 
((PARTITION#6=5637144576) OR (PARTITION#6 IS NULL))) AND 
((PARTITION#7=5637144576) OR (PARTITION#7 IS NULL))) AND 
((PARTITION#8=5637144576) OR (PARTITION#8 IS NULL))) AND 
((DATAAREAID#8=N'usmf') OR (DATAAREAID#8 IS NULL))) AND 
(PARENTPROJECT='')) 
ORDER BY T1.PROJECTID
```

Det faktiske resultatet er at `parentProject` feltet blir evaluert til `null`. Imidlertid er `null` ikke det samme som den tomme strengen. På grunn av denne uoverensstemmelsen, returnerer ikke spørringsfilteret gyldige resultater.

Følg fremgangsmåten nedenfor for å løse problemet.

1. Legg til en beregnet kolonne som kan legges til i en utvidelsesmodell, og som støttes av logikk som konverterer `null` til den tomme strengen.

    ```dos
    SysComputedColumn::if(SysComputedColumn::isNullExpression(ParentProject), SysComputedColumn::returnLiteral(""), fieldName);
    ```

2. Bruk filteret på den nye beregnede kolonnen i stedet for standardkolonnen.

Hvis du vil evaluere filteret i et utviklingsmiljø, kan du bruke følgende X++-kode til å validere resultatene. Kjør denne koden som et frittstående program. Du kan bruke det til å evaluere forskjellige typer filtre som gjelder for en enhet, før du bruker disse filtrene på dobbel skriving-tilordninger. Spørringen kan kjøres mot databasen for å evaluere avvik.

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes); 
QueryBuildDataSource qbd = query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual sql statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>Data fra økonomi- og driftsapper synkroniseres ikke med Dataverse

Under direkte synkronisering kan det oppstå et problem der bare en del av dataene synkroniseres fra økonomi- og driftsapper til Dataverse, eller at data ikke synkroniseres i det hele tatt.

> [!NOTE]
> Du må løse dette problemet i løpet av utviklingen.

Før du begynner å reparere problemet, må du vurdere følgende forutsetninger:

+ Pass på at dine egendefinerte endringer er skrevet i ett enkelt transaksjonsområde.
+ Forretningshendelser og rammeverket for dobbel skriving håndterer ikke `doinsert()`, `doUpdate()` og `recordset()` operasjoner, eller poster der `skipBusinessEvents(true)` er merket. Hvis koden din er i disse funksjonene, utløses ikke dobbel skriving.
+ Forretningshendelser må være registrert for datakilden som er tilordnet. Enkelte datakilder kan bruke en ytre kobling, og kan være merket som skrivebeskyttet i økonomi- og driftsapper. Disse datakildene spores ikke.
+ Endringer utløses bare hvis endringene er i de tilordnede feltene. Feltendringer som ikke er tilordnet, utløser ikke dobbel skriving.
+ Kontroller at filterevalueringer gir et gyldig resultat.

### <a name="troubleshooting-steps"></a>Feilsøkingstrinn

1. Gå gjennom felttilordninger på administrasjonssiden for dobbel skriving. Hvis et felt ikke er tilordnet fra økonomi- og driftsapper til Dataverse, spores det ikke. I illustrasjonen nedenfor spores for eksempel **Beskrivelse**-feltet fra Dataverse, men ikke fra økonomi- og driftsapper. Det spores ikke noen endringer i dette feltet fra økonomi- og driftsapper.

    ![Sporet felt.](media/live-sync-troubleshooting-1.png)

2. Bestem om datakilden spores i forretningshendelsesdefinisjonen. I illustrasjonen nedenfor spores for eksempel ingen felt fra **DefaultDimensionDAVs**-tabeller og underliggende tabeller. Datakilder som bruker en ytre kobling og som er merket som skrivebeskyttet, spores ikke.

    ![Felt som ikke spores.](media/live-sync-troubleshooting-2.png)

3. Bestem om de tilordnede tabellfeltene skal vises i **BUSINESSEVENTSDEFINITION**-tabellen, som vist i illustrasjonen nedenfor. Hvis du ikke finner feltet du ser etter, i spørringsresultatet, utløses det ikke av dobbel skriving.

    ![Sporede felt i tabellen.](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>Eksempelscenario

I økonomi- og driftsapper finnes det en oppdatering av adressen for en kontaktpost, men adresseendringen blir ikke synkronisert til Dataverse. Dette scenariet oppstår fordi det ikke finnes noen post i **BusinessEventsDefinition**-tabellen som har kombinasjonen av tabellen som påvirkes, og enheten. Mer bestemt er ikke **LogisticsPostalAddress**-tabellen den direkte datakilden for **smmContactpersonCDSV2Entity**-enheten. Enheten **smmContactpersonCDSV2Entity** har **smmContactPersonV2Entity** som datakilden, og **smmContactPersonV2Entity** har i sin tur **LogisticsPostalAddressBaseEntity** som datakilden. **LogisticsPostalAddress**-tabellen er datakilden for **LogisticsPostalAddressBaseEntity**.

Det kan oppstå en lignende situasjon i enkelte ikke-standardmønstre, for eksempel tilfeller der tabellen som endres i økonomi- og driftsapper, ikke vil knyttes til enheten som inneholder den. De primære adressedataene beregnes for eksempel på **smmContactPersonCDSV2Entity**-enheten. Rammeverket for dobbel skriving prøver å fastslå hvordan en endring i en underliggende tabell tilordnes tilbake til enheter. Vanligvis er denne tilnærmingen tilstrekkelig. I noen tilfeller er imidlertid koblingen så kompleks at du må være spesifikk. Du må kontrollere at **RecId** i den relaterte tabellen er direkte tilgjengelig på enheten. Deretter legger du til en statisk metode for å overvåke tabellen for endringer.

Vurder for eksempel metoden **smmContactPersonCDSV2Entity::getEntityDataSourceToFieldMapping()**. **CustCustomerV3entity** og **VendVendorV2Entity** er endret for å håndtere denne situasjonen.

Følg fremgangsmåten nedenfor for å løse problemet.

1. Legg til et **PrimaryPostalAddressRecId**-felt i **smmContactPersonV2Entity**-enheten. Gjør det internt.

    ![Felt som legges til i smmContactPersonV2Entity-enheten.](media/Troubleshoot_live_sync_issue_1.png)

2. Legg til det samme feltet i **smmContactPersonCDSV2Entity**-enheten.

    ![Felt som legges til i smmContactPersonCDSV2Entity-enheten.](media/Troubleshoot_live_sync_issue_2.png)

3. Legg til følgende metode i **smmContactPersonCDSV2Entity**-klassen.

    ```xpp
    public static container getEntityDataSourceToFieldMapping(container mapping)
    {
        mapping += [[tablestr(smmContactPersonCDSV2Entity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)]];
        return mapping;
    }
    ```

4. Synkroniser databasen, og bygg programmet.
5. Stopp alle dobbel skriving-tilordningene som er opprettet på **smmContactPersonCDSV2Entity**-enheten.
6. Start tilordningen. Du skal se den nye tabellen (**LogisticsPostalAddress** i dette eksemplet) som du startet å spore ved å bruke **RefTableName**-kolonnen for raden der **refentityname**-verdien er lik **smmContactPersonCDSV2Entity** i **BusinessEventsDefinition**-tabellen.

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>Feil når du oppretter en post der flere poster sendes fra en økonomi- og driftsapp til Dataverse i samme parti

For en transaksjon oppretter en økonomi- og driftsapp data i et parti, og sender dem som et parti til Dataverse. Hvis to poster opprettes som en del av den samme transaksjonen, og de refererer til hverandre, kan det hende at du får en feilmelding som ligner på følgende eksempel i økonomi- og driftsappen:

*Kan ikke skrive data til aaa_fundingsources. Kan ikke slå opp ebecsfs_contracts med vediene {PC00...}. Kan ikke slå opp aaa_fundingsources med verdiene {PC00...}. Skriving til aaa_fundingsources mislyktes med feilmelding Unntaksmelding: Den eksterne serveren returnerte en feil: (400) Ugyldig forespørsel.*

Hvis du vil korrigere problemet, oppretter du enhetsrelasjoner i økonomi- og driftsappen for å angi at de to enhetene er knyttet til hverandre, og at de relaterte postene håndteres i den samme transaksjonen.

## <a name="enable-verbose-logging-of-error-messages"></a>Aktiver detaljert logging av feilmeldinger

I en økonomi- og driftsapp kan det oppstå feil som er knyttet til Dataverse-miljøet. Det kan hende at feilmeldingen ikke inneholder hele teksten i meldingen eller andre relevante data. Hvis du vil ha mer informasjon, kan du aktivere detaljert logging ved å angi **IsDebugMode**-flagget som finnes på enheten **DualWriteProjectConfigurationEntity** i alle prosjektkonfigurasjoner i økonomi- og driftsapper.

1. Åpne **DualWriteProjectConfigurationEntity**-enheten ved hjelp av Excel-tillegget. Hvis du vil bruke tillegget, aktiverer du utformingsmodus i Excel-tillegget for økonomi og drift og legger til **DualWriteProjectConfigurationEntity** i et regneark. Hvis du vil ha mer informasjon, kan du se [Vis og oppdater enhetsdata med Excel](../../office-integration/use-excel-add-in.md).
2. Sett flagget **IsDebugMode** til **Ja** for prosjektet.
3. Kjør scenarioet.
4. De detaljerte loggene er tilgjengelige i tabellen **DualWriteErrorLog**. Bruk følgende URL-adresse til å slå opp data ved hjelp av tabelleseren: `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`
5. Hvis du vil registrere flere logger i feilsøkingsmodus, installerer du oppdateringen i [KB 4595434 (løsning for tomme verdier som overføres i direkte synkronisering av dobbel skriving)](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9).

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>Feil når du legger til en adresse for en kunde eller kontakt

Du kan få følgende feilmelding når du prøver å legge til en adresse for en kunde eller kontakt i økonomi- og driftsapper eller Dataverse:

*Kan ikke skrive data til msdyn_partypostaladdresses. Skriving til DirPartyPostalAddressLocationCDSEntity mislyktes med feilmeldingen Forespørsel mislyktes med statuskoden BadRequest og CDS-feilkode: 0x80040265 svarmelding: Det oppstod en feil i plugin-modulen. En post som har attributtverdiene Lokasjons-ID, finnes allerede. Nøkkelen for lokasjons-ID for enhet krever at dette settet med attributter inneholder unike verdier. Velg unike verdier, og prøv på nytt.*

Hvis du vil rette opp problemet, installerer du pakkeversjonen for orkestrering for dobbel skriving (2.2.2.60), slik at nøklene i **Adresse**-tabellen defineres som vist i følgende tabell.

| Egenskap | Verdi |
|---|---|
| Visningsnavn | **Fordelingsnøkkel** |
| Navn | **msdyn_locationkey** |
| Felt | **msdyn_locationid**, **parentid** |
| Status | **Aktivt** |
| Systemjobb | Blank |

## <a name="error-when-you-add-a-customer-in-dataverse"></a>Feil når du legger til en kunde i Dataverse

Du kan få følgende feilmelding når du prøver å legge til en kunde i Dataverse:

*"RecordError0": "Skriving mislyktes for enhet Kunder V3 med ukjent unntak - finner ikke partspost for partstypen "Organisasjon"}.*

Når en kunde opprettes i Dataverse, genereres det et nytt partsnummer. Feilmeldingen vises når kundeposten, sammen med parten, synkroniseres til økonomi- og driftsapper, men det allerede finnes en kundepost som har et annet partsnummer.

Hvis du vil rette problemet, kan du finne kunden ved hjelp av partsoppslag. Hvis kunden ikke finnes, oppretter du en ny kundepost. Hvis kunden finnes, bruker du den eksisterende parten til å opprette den nye kundeposten.

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>Feil når du oppretter en ny kunde, leverandør eller kontakt i Dataverse

Du kan få følgende feilmelding når du prøver å opprette en ny kunde, leverandør eller kontakt i Dataverse:

*Kan ikke oppdatere en parts type fra "DirOrganization" til "DirPerson", en sletting av den eksisterende parten etterfulgt av en innsetting med den nye typen skal utføres i stedet.*

I Dataverse er det en nummerserie i **msdyn_party**-tabellen. Når en konto opprettes i Dataverse, opprettes det en ny part (for eksempel **Part-001** av **Organisasjon**-typen). Disse dataene sendes til økonomi- og driftsappen. Hvis Dataverse-miljøet tilbakestilles, eller økonomi- og driftsmiljøet er koblet til et annet Dataverse-miljø, og det deretter opprettes en ny kontaktpost i Dataverse, opprettes det en ny partsverdi som begynner med **Part-001**. Denne gangen vil partsposten som opprettes, være **Part-001** av **Person**-typen. Når disse dataene synkroniseres, viser økonomi- og driftsapper den forrige feilmeldingen, fordi partsposten **Part-001** av **Organisasjon**-typen allerede finnes.

Hvis du vil løse problemet, endrer du den automatiske nummerserien for **msdyn_partynumber**-feltet i **msdyn_party**-tabellen i Dataverse til en annen automatisk nummerserie.

## <a name="performance-issue-with-customer-or-contact-mappings"></a>Ytelsesproblem med kunde- eller kontakttilordninger

Det kan hende at du marginalt kan forbedre ytelsen ved direktesynkronisering for kunder og kontakter ved å tilpasse metoden **getEntityDataSourceToFieldMapping** (i **CustCustomerV3Entity**-enheten) og metoden **getEntityDataSourceToFieldMapping** (i **smmContactPersonCDSV2Entity**-enheten). Disse tilpasningene reduserer antall poster i **BusinessEventsDefinition**-tabellen. Denne reduksjonen i antall poster i sin tur reduserer antall hendelser som oppstår.

Metoden **getEntityDataSourceToFieldMapping** i **CustCustomerV3Entity**-enheten sørger for at en oppdatering av kundens elektroniske adresser eller postadresse utløser forretningshendelser, slik at de oppdaterte dataene blir sendt til Dataverse. Hvis du ikke bruker alle feltene og ikke trenger informasjonen i dobbel skriving, må du kommentere ut de aktuelle linjene i metoden. Hvert sporede felt og tabell som legges til i denne metoden, legger til en post i **BusinessEventsDefinition**-tabellen for kombinasjonen av den sporede tabellen og den sporede enheten.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, AddressRecordId)],
        [identifierstr(DirPartyBaseEntity), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactURLRecordId)],
        [identifierstr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactPhoneRecordId)],
        [identifierstr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactEmailRecordId)],
        [identifierstr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactFaxRecordId)],
        [identifierstr(DirPartyBaseEntity4), tablenum(DirPartyLocation), fieldstr(CustCustomerV3Entity, DirPartyLocationRecordId)],
        [identifierstr(DirPartyBaseEntity5), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, InvoiceAddressRecordId)],
        [identifierstr(DirPartyBaseEntity6), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, DeliveryAddressRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(DirPartyTable), fieldstr(CustCustomerV3Entity, PartyRecordId)]];
    return mapping;
}
```

Metoden **getEntityDataSourceToFieldMapping** i **smmContactPersonCDSV2Entity**-enheten sørger på lignende måte for at en oppdatering av kontaktens elektroniske adresser eller postadresse utløser forretningshendelser, slik at de oppdaterte dataene blir sendt til Dataverse. I metoden kan du kommentere ut linjene for alle felt du ikke bruker.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)],
        [identifierStr(DirPartyBaseEntity), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PrimaryAddressLocation)],
        [identifierStr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactEmailRecordId)],
        [identifierStr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFaxRecordId)],
        [identifierStr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactPhoneRecordId)],
        [identifierStr(DirPartyBaseEntity4), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFacebookRecordId)],
        [identifierStr(DirPartyBaseEntity5), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTwitterRecordId)],
        [identifierStr(DirPartyBaseEntity6), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactURLRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactLinkedInRecordId)],
        [identifierStr(DirPartyBaseEntity8), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTelexRecordId)],
        [identifierStr(DirPartyBaseEntity9), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PartyRecordId)]];
    return mapping;
}
```

Når du har oppdatert metodene, følger du fremgangsmåten nedenfor.

1. Synkroniser databasen, og bygg programmet.
2. Stopp alle dobbel skriving-tilordningene på enhetene **smmContactPersonCDSV2Entity** og **CustCustomerV3Entity**.
3. Start tilordningene. Du skal se færre poster i enhetene **smmContactPersonCDSV2Entity** og **CustCustomerV3Entity** og **BusinessEventsDefinition**-tabellen, og ytelsen kan forbedres marginalt.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
