---
title: Feilsøke problemer under første synkronisering
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer som kan oppstå under første synkronisering.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 241277ada768cc6497035cc377d0e158646a42d6
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781120"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Feilsøke problemer under første synkronisering

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse. Det inneholder informasjon som kan hjelpe deg med å løse problemer som kan oppstå under første synkronisering.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Se etter innledende synkroniseringsfeil i en Finance and Operations-app

Når du har aktivert tilordningsmalene, skal statusen for tilordningene være **Kjører**. Hvis statusen er **Kjører ikke**, oppstod det feil under første synkronisering. Hvis du vil vise feilene, velger du fanen **Detaljer om innledende synkronisering** på siden **Dobbel skriving**.

![Feil i fanen Detaljer om innledende synkronisering.](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Du kan ikke fullføre første synkronisering: 400 Ugyldig forespørsel

**Nødvendig rolle for å løse problemet:** Systemadministrator

Du kan få følgende feilmelding når du prøver å kjøre tilordningen og den innledende synkroniseringen:

*(\[Ugyldig forespørsel\], Den eksterne serveren returnerte en feil: (400) Ugyldig forespørsel.), AX-eksporten oppdaget en feil.*

Her er et eksempel på hele feilmeldingen.

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

Hvis denne feilen oppstår konsekvent, og du ikke kan fullføre den første synkroniseringen, følger du denne fremgangsmåten for å løse problemet.

1. Logg på den virtuelle maskinen for Finance and Operations-appen.
2. Åpne Microsoft Management Console.
3. I **Tjenester**-ruten kontrollerer du at tjenesten for rammeverk for dataimport/-eksport for Microsoft Dynamics 365. Start den på nytt hvis den er stoppet, fordi den første synkroniseringen krever det.

## <a name="initial-synchronization-error-403-forbidden"></a>Innledende synkroniseringsfeil: 403 forbudt

Du kan få følgende feilmelding under innledende synkronisering:

*(\[Forbudt\], Den eksterne serveren returnerte en feil: (403) Forbudt.), AX-eksporten oppdaget en feil*

Følg fremgangsmåten nedenfor for å løse problemet.

1. Logg på Finance and Operations-appen.
2. På siden **Azure Active Directory-programmer** sletter du **DtAppID**-klienten, og deretter legger du den til på nytt.

![DtAppID-klient i listen over Azure AD-programmer.](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Egenreferanse- eller sirkelreferansefeil under innledende synkronisering

Du kan få feilmeldinger hvis noen av tilordningene dine har egenreferanser eller sirkelreferanser. Feilene faller under følgende kategorier:

- [Feil i tabelltilordning Leverandører V2 til msdyn_vendors](#error-vendor-map)
- [Feil i tabelltilordningen Kunder V3 til Kontoer](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>Løs feil i tabelltilordningen Leverandører V2 til msdyn_vendors

Det kan hende at det oppstår feil med innledende synkronisering for tilordningen **Leverandører V2** til **msdyn\_vendors** hvis tabellene har eksisterende rader med verdier i feltene **PrimaryContactPersonId** og kolonnen **InvoiceVendorAccountNumber**. Disse feilene skjer fordi **InvoiceVendorAccountNumber** er en selvrefererende kolonne, og **PrimaryContactPersonId** er en sirkelreferanse i leverandørtilordningen.

Feilmeldingene du mottar, vil ha følgende form.

*Fant ikke GUID for feltet: \<field\>. Oppslaget ga ingen treff: \<value\>. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Her er noen eksempler:

- *Fant ikke GUID for feltet: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Oppslaget ga ingen treff: 000056. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Fant ikke GUID for feltet: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Oppslaget ga ingen treff: V24-1. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Hvis rader i leverandørtabellen har verdier i kolonnene **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**, følger du disse trinnene for å fullføre den innledende synkroniseringen.

1. I Finance and Operations-appen sletter du kolonnene **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** fra tilordningen, og deretter lagrer du tilordningen.

    1. På siden for tilordning med dobbeltskriving for **Leverandører V2 (msdyn\_vendors)**, i fanen **Tabelltilordninger** i filteret til venstre velger du **Finance and Operations-apper.Vendors V2**. I filteret til høyre velger du **Sales.Vendor**.
    2. Søk etter **primarycontactperson** for å finne kildekolonnen **PrimaryContactPersonId**.
    3. Velg **Handlinger**, og velg deretter **Slett**.

        ![Slette kolonnen PrimaryContactPersonId.](media/vend_selfref3.png)

    4. Gjenta disse trinnene for å slette kolonnen **InvoiceVendorAccountNumber**.

        ![Slette kolonnen InvoiceVendorAccountNumber.](media/vend-selfref4.png)

    5. Lagre endringene i tilordningen.

2. Deaktiver sporing av endringer for **Leverandører V2**-tabellen.

    1. I arbeidsområdet **Dataadministrasjon** velger du flisen **Datatabeller**.
    2. Velg **Leverandører V2**-tabellen.
    3. I handlingsruten velger du **Alternativer**, og deretter velger du **Endringssporing**.

        ![Velge alternativet Endringssporing.](media/selfref_options.png)

    4. Velg **Deaktiver endringssporing**.

        ![Velge Deaktiver endringssporing.](media/selfref_tracking.png)

3. Kjør den innledende synkroniseringen for tilordningen **Leverandører V2 (msdyn\_vendors)**. Den innledende synkroniseringen skal kjøres uten feil.
4. Kjør den innledende synkroniseringen for **CDS-kontakter V2 (kontakter)**-tilordningen. Du må synkronisere denne tilordningen hvis du vil synkronisere den primære kontaktkolonnen i leverandørtabellen, siden innledende synkronisering også må utføres for kontaktradene.
5. Legg kolonnene **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** tilbake i tilordningen **Leverandører V2 (msdyn\_vendors)**, og lagre deretter tilordningen.
6. Kjør den innledende synkroniseringen igjen for tilordningen **Leverandører V2 (msdyn\_vendors)**. Siden endringssporing er deaktivert, synkroniseres alle radene.
7. Aktiver sporingsendring på nytt for **Leverandører V2**-tabellen.

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>Utbedre feil i tabelltilordningen Kunder V3 til Kontoer

Det kan hende at det oppstår feil med innledende synkronisering for tilordningen **Kunder V3** til **Kontoer** hvis tabellene har eksisterende rader med verdier i kolonnene **ContactPersonID** og **InvoiceAccount**. Disse feilene skjer fordi **InvoiceAccount** er en selvrefererende kolonne, og **ContactPersonID** er en sirkelreferanse i leverandørtilordningen.

Feilmeldingene du mottar, vil ha følgende form.

*Fant ikke GUID for feltet: \<field\>. Oppslaget ga ingen treff: \<value\>. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Her er noen eksempler:

- *Fant ikke GUID for feltet: primarycontactid.msdyn\_contactpersonid. Oppslaget ga ingen treff: 000056. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Fant ikke GUID for feltet: msdyn\_billingaccount.accountnumber. Oppslaget ga ingen treff: 1206-1. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Hvis noen rader i kundetabellen har verdier i kolonnene **ContactPersonID** og **InvoiceAccount**, følger du disse trinnene for å fullføre den innledende synkroniseringen. Du kan bruke denne fremgangsmåten for alle de kunderettede tabellene, for eksempel **Kontoer** og **Kontakter**.

1. I Finance and Operations-appen sletter du kolonnene **ContactPersonID** og **InvoiceAccount** fra tilordningen **Kunder V3 (kontoer)**, og deretter lagrer du tilordningen.

    1. I filteret til venstre i fanen **Tabelltilordninger** på siden for tilordning med dobbeltskriving for **Kunder V3 (kontoer)** velger du **Finance and Operations-app.Customers V3**. I filteret til høyre velger du **Dataverse .Account**.
    2. Søk etter **contactperson** for å finne kildekolonnen **ContactPersonID**.
    3. Velg **Handlinger**, og velg deretter **Slett**.

        ![Slette kolonnen ContactPersonID.](media/cust_selfref3.png)

    4. Gjenta disse trinnene for å slette kolonnen **InvoiceAccount**.

        ![Slette kolonnen InvoiceAccount.](media/cust_selfref4.png)

    5. Lagre endringene i tilordningen.

2. Deaktiver sporing av endringer for **Kunder V3**-tabellen.

    1. I arbeidsområdet **Dataadministrasjon** velger du flisen **Datatabeller**.
    2. Velg **Kunder V3**-tabellen.
    3. I handlingsruten velger du **Alternativer**, og deretter velger du **Endringssporing**.

        ![Velge alternativet Endringssporing.](media/selfref_options.png)

    4. Velg **Deaktiver endringssporing**.

        ![Velge Deaktiver endringssporing.](media/selfref_tracking.png)

3. Kjør den innledende synkroniseringen på nytt for **Kunder V3 (Kontoer)**-tilordningen. Den innledende synkroniseringen skal kjøres uten feil.
4. Kjør den innledende synkroniseringen for **CDS-kontakter V2 (kontakter)**-tilordningen.

    > [!NOTE]
    > Det er to tilordninger med samme navn. Sørg for å velge tilordningen med følgende beskrivelse i fanen **Detaljer**: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Krever ny pakke \[Dynamics365SupplyChainExtended\].**

5. Legg kolonnene **InvoiceAccount** og **ContactPersonId** tilbake i tilordningen **Kunder V3 (Kontoer)** igjen, og lagre deretter tilordningen. Både kolonnen **InvoiceAccount** og kolonnen **ContactPersonId** er nå en del av modus for direkte synkronisering igjen. I neste trinn skal du utføre den innledende synkroniseringen for disse kolonnene.
6. Kjør den innledende synkroniseringen på nytt for **Kunder V3 (Kontoer)**-tilordningen. Siden endringssporing er slått av, synkroniseres dataene for **InvoiceAccount** og **ContactPersonId** fra Finance and Operations-appen til Dataverse.
7. Hvis du vil synkronisere dataene for **InvoiceAccount** og **ContactPersonId** fra Dataverse til Finance and Operations-appen, må du bruke et dataintegrasjonsprosjekt.

    1. Under Power Apps oppretter du et dataintegrasjonsprosjekt mellom **Sales.Account** og **Finance and Operations apps.Kunder V3**-tabeller. Dataretningen må være fra Dataverse til Finance and Operations-appen. Fordi **InvoiceAccount** er et nytt attributt med dobbeltskriving, kan det hende du bør hoppe over innledende synkronisering for dette attributtet. Hvis du vil ha mer informasjon, se [Integrere data i Dataverse](/power-platform/admin/data-integrator).

        Illustrasjonen nedenfor viser et prosjekt som oppdaterer **CustomerAccount** og **ContactPersonId**.

        ![Dataintegrasjonsprosjekt for å oppdatere CustomerAccount og ContactPersonId.](media/cust_selfref6.png)

    2. Legg til firmakriteriene i filteret på Dataverse-siden, slik at bare radene som samsvarer med filterkriteriene, blir oppdatert i Finance and Operations-appen. Velg filterknappen for å legge til et filter. Deretter, i dialogboksen **Rediger spørring**, kan du legge til en filterspørring som for eksempel **\_msdyn\_company\_value eq '\<guid\>'**.

        > [MERK] Hvis filterknappen ikke finnes, oppretter du en støtteforespørsel for å be dataintegreringsgruppen aktivere filterfunksjonen i leieren din.

        Hvis du ikke angir en filterspørring for **\_msdyn\_company\_value**, blir alle radene synkronisert.

        ![Legge til en filterspørring.](media/cust_selfref7.png)

    Den innledende synkroniseringen av radene er nå fullført.

8. I Finance and Operations-appen aktiverer du endringssporing på nytt for **Kunder V3**-tabellen.

## <a name="initial-sync-failures-on-maps-with-more-than-10-lookup-fields"></a>Innledende synkroniseringsfeil på kart med mer enn ti oppslagsfelt

Du kan få følgende feilmelding når du prøver å kjøre en innledende synkroniseringsfeil på **Kunder V3 - Kontoer**, **Salgsordrer**-tilordninger eller enhver tilordning med flere enn 10 oppslagsfelter:

*CRMExport: Pakkekjøring fullført. Feilbeskrivelse 5 Forsøk på å hente data fra https://xxxxx//datasets/yyyyy/tables/accounts/items?$select=accountnumber, address2_city, address2_country, ... (msdyn_company/cdm_companyid eq 'id')&$orderby=accountnumber asc mislyktes.*

På grunn av oppslagsbegrensningen på spørringen, mislykkes den innledende synkroniseringen når enhetstilordningen inneholder mer enn ti oppslag. Hvis du vil ha mer informasjon, kan du se [Hent relaterte tabellposter med en spørring](/powerapps/developer/common-data-service/webapi/retrieve-related-entities-query).

Følg fremgangsmåten nedenfor for å løse problemet:

1. Fjern valgfrie oppslagsfelt fra oversikten over dobbel skriving skriving slik at antall oppslag er 10 eller færre.
2. Lagre tilordningen, og utfør den innledende synkroniseringen.
3. Når den innledende synkroniseringen for det første trinnet er vellykket, legger du til de gjenværende oppslagsfeltene og fjerner oppslagsfeltene du synkroniserte i første trinn. Kontroller at antall oppslagsfelt er 10 eller færre. Lagre tilordningen, og kjør den innledende synkroniseringen.
4. Gjenta disse trinnene til alle oppslagsfeltene er synkronisert.
5. Legg til alle oppslagsfeltene tilbake i tilordningen, lagre tilordningen og kjør tilordningen med **Hopp over innledende synkronisering**.

Denne prosessen aktiverer tilordningen for direktesynkroniseringsmodus.

## <a name="known-issue-during-initial-sync-of-party-postal-addresses-and-party-electronic-addresses"></a>Kjent problem under innledende synkronisering av postadresser til parter og elektroniske adresser til parter

Du kan få følgende feilmelding når du prøver å kjøre det innledende settet med postadresser til parter og elektroniske adresser til parter:

*Finner ikke partnummer i Dataverse .*

Det finnes et områdesett i **DirPartyCDSEntity** i Finance and Operations-apper som filtrerer parter av typen **Person** og **Organisasjon**. Derfor vil en innledende synkronisering av tilordningen **CDS-parter – msdyn_parties** ikke synkronisere parter av andre typer, inkludert **Juridisk enhet** og **Driftsenhet**. Når den innledende synkroniseringen kjører for **Postadressesteder for CDS-part (msdyn_partypostaladdresses)** eller **Partskontakter V3 (msdyn_partyelectronicaddresses)**, kan du få feilen.

Vi jobber med en løsning for å fjerne partstypeutvalget for Finance and Operations-enheten, slik at parter av alle typer kan synkroniseres mot Dataverse.

## <a name="are-there-any-performance-issues-while-running-initial-sync-for-customers-or-contacts-data"></a>Er det noen ytelsesproblemer når du kjører innledende synkronisering for kunde- eller kontaktdata?

Hvis du har kjørt den innledende synkroniseringen for **Kunde**-data og **Kunde**-tilordninger kjører, og du deretter kjører den innledende synkroniseringen for **Kontakter**-data, kan det oppstå ytelsesproblemer under innsettinger og oppdateringer i tabellene **LogisticsPostalAddress** og **LogisticsElectronicAddress** for **Kontakt**-adresser. De samme tabellene for globale postadresser og elektroniske adresser spores for **CustCustomerV3Entity** og **VendVendorV2Entity**, og dobbel skriving prøver å bygge flere spørringer for å skrive data på den andre siden. Hvis du allerede har kjørt den innledende synkroniseringen for **Kunde**, må du stoppe den tilsvarende tilordningen når du kjører innledende synkronisering for **Kontakter**-data. Gjør det samme for **Leverandør**-dataene. Når den innledende synkroniseringen er fullført, kan du kjøre alle tilordningene ved å hoppe over den innledende synkroniseringen.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
