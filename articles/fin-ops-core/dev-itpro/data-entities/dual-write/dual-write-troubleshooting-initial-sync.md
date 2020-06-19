---
title: Feilsøke problemer under første synkronisering
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer som kan oppstå under første synkronisering.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410087"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Feilsøke problemer under første synkronisering

[!include [banner](../../includes/banner.md)]

Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service. Det inneholder informasjon som kan hjelpe deg med å løse problemer som kan oppstå under første synkronisering.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Se etter innledende synkroniseringsfeil i en Finance and Operations-app

Når du har aktivert tilordningsmalene, skal statusen for tilordningene være **Kjører**. Hvis statusen er **Kjører ikke**, oppstod det feil under første synkronisering. Hvis du vil vise feilene, velger du kategorien **Detaljer om innledende synkronisering** på siden **Dobbel skriving**.

![Kategorien Detaljer om innledende synkronisering](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Du kan ikke fullføre første synkronisering: 400 Ugyldig forespørsel

**Nødvendig rolle for å løse problemet:** Systemadministrator

Du kan få følgende feilmelding når du prøver å kjøre tilordningen og den innledende synkroniseringen:

*Den eksterne serveren returnerte en feil: (400) Ugyldig forespørsel.), AX-eksporten oppdaget en feil*

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

![Liste over Azure AD-programmer](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Egenreferanse- eller sirkelreferansefeil under innledende synkronisering

Du kan få feilmeldinger hvis noen av tilordningene dine har egenreferanser eller sirkelreferanser. Feilene faller under følgende kategorier:

- [Leverandører V2 til msdyn_vendors-enhetstilordning](#error-vendor-map)
- [Kunder V3 til Kontoer-enhetstilordning](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>Utbedre en feil i enhetstilordning fra Leverandører V2 til msdyn_vendors

Det kan hende du møter på følgende feil med innledende synkronisering i tilordningen **Leverandører V2** til **msdyn_vendors** hvis enhetene har eksisterende poster med verdier i feltene **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**. Dette fordi **InvoiceVendorAccountNumber** er et selvrefererende felt, og **PrimaryContactPersonId** er en sirkelreferanse i leverandørtilordningen.

*Fant ikke GUID for feltet: <field>. Oppslaget ga ingen treff: <value>. Prøv disse URL-ene for å kontrollere at referansedataene finnes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

Her er noen eksempler:

- *Finner ikke GUID for feltet: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Fant ikke oppslaget: 000056. Prøv denne URL-adressen for å kontrollere om referansedataene finnes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$Select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Finner ikke GUID for feltet: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Fant ikke oppslaget: V24-1. Prøv denne URL-adressen for å kontrollere om referansedataene finnes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*

Hvis du har poster med verdier i disse feltene i leverandørenheten, følger du trinnene i delen nedenfor for å fullføre den innledende synkroniseringen.

1. I Finance and Operations-appen sletter du **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**-feltene fra tilordningen, og lagrer endringene.

    1. Gå til siden for tilordning med dobbeltskriving for **Leverandører V2 (msdyn_vendors)**, og velg **Enhetstilordninger**-fanen. I filteret til venstre velger du **Finance and Operations apps.Leverandører V2**. I filteret til høyre velger du **Sales.Vendor**.

    2. Søk etter **primarycontactperson** for å finne kildefeltet **PrimaryContactPersonId**.
    
    3. Klikk på **Handlinger**-knappen, og velg **Slett**.
    
        ![egen- eller sirkelreferanse 3](media/vend_selfref3.png)
    
    4. Gjenta prosessen for å slette **InvoiceVendorAccountNumber**-feltet.
    
        ![egen- eller sirkelreferanse 4](media/vend-selfref4.png)
    
    5. Lagre tilordningsendringene.

2. Deaktiver sporing av endringer for **Leverandører V2**-enheten.

    1. Gå til **Datastyring \> Dataenheter**.
    
    2. Velg **Leverandører V2**-enheten.
    
    3. Klikk på **Alternativer** på menylinjen, og deretter **Endringssporing**.
    
        ![egen- eller sirkelreferanse 5](media/selfref_options.png)
    
    4. Klikk på **Deaktiver endringssporing**.
    
        ![egen- eller sirkelreferanse 6](media/selfref_tracking.png)

3. Kjør den innledende synkroniseringen av **Leverandører V2 (msdyn_vendors)**-tilordningen. Den innledende synkroniseringen skal kjøres uten feil.

4. Kjør den innledende synkroniseringen for **CDS-kontakter V2 (kontakter)**-tilordningen. Du må synkronisere denne tilordningen hvis du vil synkronisere det primære kontaktfeltet på leverandørenheten, ettersom kontaktpostene også må gjennomgå innledende synkronisering.

5. Legg til feltene **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** tilbake i **Leverandører V2 (msdyn_vendors)**-tilordningen, og lagre tilordningen.

6. Kjør den innledende synkroniseringen på nytt for **Leverandører V2 (msdyn_vendors)**-tilordningen. Alle postene synkroniseres, fordi endringssporing er deaktivert.

7. Aktiver sporing av endringer for **Leverandører V2**-enheten.

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a>Utbedre en feil i enhetstilordningen Kunder V3 til Kontoer

Det kan hende du møter på følgende feil med innledende synkronisering i tilordningen **Kunder V3** til **Kontoer** hvis enhetene har eksisterende poster med verdier i feltene **ContactPersonID** og **InvoiceAccount**. Dette fordi **InvoiceAccount** er et selvrefererende felt, og **ContactPersonID** er en sirkelreferanse i leverandørtilordningen.

*Fant ikke GUID for feltet: <field>. Oppslaget ga ingen treff: <value>. Prøv disse URL-ene for å kontrollere at referansedataene finnes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

- *Finner ikke GUID for feltet: primarycontactid.msdyn_contactpersonid. Fant ikke oppslaget: 000056. Prøv denne URL-adressen for å kontrollere om referansedataene finnes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$Select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Finner ikke GUID for feltet: msdyn_billingaccount.accountnumber. Fant ikke oppslaget: 1206-1. Prøv denne URL-adressen for å kontrollere om referansedataene finnes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*

Hvis du har poster med verdier i disse feltene i kundeenheten, følger du trinnene i delen nedenfor for å fullføre den innledende synkroniseringen. Du kan bruke denne fremgangsmåten for alle de kunderettede enhetene, for eksempel Kontoer og Contacts.

1. I Finance and Operations-appen sletter du feltene **ContactPersonID** og **InvoiceAccount** fra **Kunder V3 (kontoer)**-tilordningen, og lagrer tilordningen.

    1. Gå til siden for tilordning med dobbeltskriving for **Kunder V3 (Kontoer)**, og velg **Enhetstilordninger**-fanen. I filteret til venstre velger du **Finance and Operations app.Kunder V3**. I filteret til høyre velger du **Common Data Service .Account**.

    2. Søk etter **contactperson** for å finne kildefeltet **ContactPersonID**.
    
    3. Klikk på **Handlinger**-knappen, og velg **Slett**.
    
        ![egen- eller sirkelreferanse 3](media/cust_selfref3.png)
    
    4. Gjenta prosessen for å slette **InvoiceAccount**-feltet.
    
        ![egen- eller sirkelreferanse](media/cust_selfref4.png)
    
    5. Lagre tilordningsendringene.

2. Deaktiver sporing av endringer for **Kunder V3**-enheten.

    1. Gå til **Datastyring \> Dataenheter**.
    
    2. Velg **Kunder V3**-enheten.
    
    3. Klikk på **Alternativer** på menylinjen, og deretter **Endringssporing**.
    
        ![egen- eller sirkelreferanse 5](media/selfref_options.png)
    
    4. Klikk på **Deaktiver endringssporing**.
    
        ![egen- eller sirkelreferanse 6](media/selfref_tracking.png)

3. Kjør den innledende synkroniseringen for **Kunder V3 (Kontoer)**-tilordningen. Den innledende synkroniseringen skal kjøres uten feil.

4. Kjør den innledende synkroniseringen for **CDS-kontakter V2 (kontakter)**-tilordningen. Det finnes to tilordninger med samme navn. Velg den som har beskrivelsen **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].** i **Detaljer**-kategorien for tilordningen.

5. Legg til feltene **InvoiceAccount** og **ContactPersonId** i **Kunder V3 (Kontoer)** -tilordningen igjen, og lagre tilordningen. Nå er både **InvoiceAccount**- og **ContactPersonId**-feltene igjen en del av Live Sync-modusen. I neste trinn fullfører du den innledende synkroniseringen for disse feltene.

6. Kjør den innledende synkroniseringen på nytt for **Kunder V3 (Kontoer)**-tilordningen. Siden endringssporing er deaktivert, synkroniseres dataene for **InvoiceAccount** og **ContactPersonId** fra Finance and Operations-appen til Common Data Service hvis du kjører synkroniseringen.

7. Hvis du vil synkronisere dataene for **InvoiceAccount** og **ContactPersonId** fra Common Data Service til Finance and Operations, bruker du et dataintegrasjonsprosjekt.

    1. Under Power Apps oppretter du et dataintegrasjonsprosjekt mellom **Sales.Account** og **Finance and Operations apps.Kunder V3**-enheter. Dataretningen må være fra Common Data Service til Finance and Operations-appen.  Fordi **InvoiceAccount** er et nytt attributt med dobbeltskriving, kan det hende du bør hoppe over innledende synkronisering for dette attributtet. Hvis du vil ha mer informasjon, se [Integrere data i Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Bildet nedenfor viser et prosjekt som oppdaterer **CustomerAccount** og **ContactPersonId**.

        ![egen- eller sirkelreferanse](media/cust_selfref6.png)

    2. Legg til firmakriteriene i filteret på Common Data Service-siden, ettersom bare postene som samsvarer med filterkriteriene, blir oppdatert i Finance and Operations-appen. Klikk på filterikonet for å legge til et filter. I **Rediger spørring**-dialogen kan du legge til en filterspørring som for eksempel **_msdyn_company_value eq '\<guid\>'**. Hvis filterikonet ikke finnes, oppretter du en støtteforespørsel for å be dataintegreringsgruppen aktivere filterfunksjonen i leieren din. Hvis du ikke angir en filterspørring for **_msdyn_company_value**, blir alle postene synkronisert.

        ![egen- eller sirkelreferanse](media/cust_selfref7.png)

        Dette fullfører den første synkroniseringen av postene.

8. Aktiver sporing av endringer for **Kunder V3**-enheten i Finance and Operations-appen.

