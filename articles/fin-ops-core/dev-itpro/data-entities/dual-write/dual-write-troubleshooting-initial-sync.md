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
ms.openlocfilehash: e4ee3bf07a1df445875197f38f655464cc9b44d3
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443855"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Feilsøke problemer under første synkronisering

[!include [banner](../../includes/banner.md)]

Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service. Det inneholder informasjon som kan hjelpe deg med å løse problemer som kan oppstå under første synkronisering.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Se etter innledende synkroniseringsfeil i en Finance and Operations-app

Når du har aktivert tilordningsmalene, skal statusen for tilordningene være **Kjører**. Hvis statusen er **Kjører ikke**, oppstod det feil under første synkronisering. Hvis du vil vise feilene, velger du kategorien **Detaljer om innledende synkronisering** på siden **Dobbel skriving**.

![Feil i kategorien Detaljer om innledende synkronisering](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Du kan ikke fullføre første synkronisering: 400 Ugyldig forespørsel

**Nødvendig rolle for å løse problemet:** Systemadministrator

Du kan få følgende feilmelding når du prøver å kjøre tilordningen og den innledende synkroniseringen:

*(\[Ugyldig forespørsel\], Den eksterne serveren returnerte en feil: (400) Ugyldig forespørsel.), AX-eksporten oppdaget en feil*

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

![DtAppID-klient i listen over Azure AD-programmer](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Egenreferanse- eller sirkelreferansefeil under innledende synkronisering

Du kan få feilmeldinger hvis noen av tilordningene dine har egenreferanser eller sirkelreferanser. Feilene faller under følgende kategorier:

- [Feil i enhetstilordning Leverandører V2 til msdyn_vendors](#error-vendor-map)
- [Feil i enhetstilordningen Kunder V3 til Kontoer](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>Løs feil i enhetstilordning Leverandører V2 til msdyn_vendors

Det kan hende du møter på feil med innledende synkronisering for tilordningen **Leverandører V2** til **msdyn\_vendors** hvis enhetene har eksisterende poster med verdier i feltene **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**. Disse feilene skjer fordi **InvoiceVendorAccountNumber** er et selvrefererende felt, og **PrimaryContactPersonId** er en sirkelreferanse i leverandørtilordningen.

Feilmeldingene du mottar, vil ha følgende form.

*Fant ikke GUID for feltet: \<field\>. Oppslaget ga ingen treff: \<value\>. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Her er noen eksempler:

- *Fant ikke GUID for feltet: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Oppslaget ga ingen treff: 000056. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Fant ikke GUID for feltet: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Oppslaget ga ingen treff: V24-1. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Hvis noen poster i leverandørenheten har verdier i feltene **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**, følger du disse trinnene for å fullføre den innledende synkroniseringen.

1. I Finance and Operations-appen sletter du **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**-feltene fra tilordningen, og deretter lagrer du endringene.

    1. På siden for tilordning med dobbeltskriving for **Leverandører V2 (msdyn\_vendors)**, i kategorien **Enhetstilordninger** i filteret til venstre velger du **Finance and Operations-apper.Vendors V2**. I filteret til høyre velger du **Sales.Vendor**.
    2. Søk etter **primarycontactperson** for å finne kildefeltet **PrimaryContactPersonId**.
    3. Velg **Handlinger**, og velg deretter **Slett**.

        ![Slette PrimaryContactPersonId-feltet](media/vend_selfref3.png)

    4. Gjenta disse trinnene for å slette **InvoiceVendorAccountNumber**-feltet.

        ![Slette InvoiceVendorAccountNumber-feltet](media/vend-selfref4.png)

    5. Lagre endringene i tilordningen.

2. Deaktiver sporing av endringer for **Leverandører V2**-enheten.

    1. I **Dataadministrasjon**-arbeidsområdet velger du flisen **Dataenheter**.
    2. Velg **Leverandører V2**-enheten.
    3. I handlingsruten velger du **Alternativer**, og deretter velger du **Endringssporing**.

        ![Velge alternativet Endringssporing](media/selfref_options.png)

    4. Velg **Deaktiver endringssporing**.

        ![Velge Deaktiver endringssporing](media/selfref_tracking.png)

3. Kjør den innledende synkroniseringen for tilordningen **Leverandører V2 (msdyn\_vendors)**. Den innledende synkroniseringen skal kjøres uten feil.
4. Kjør den innledende synkroniseringen for **CDS-kontakter V2 (kontakter)**-tilordningen. Du må synkronisere denne tilordningen hvis du vil synkronisere det primære kontaktfeltet på leverandørenheten, ettersom innledende synkronisering også må utføres for kontaktpostene.
5. Legg til feltene **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** tilbake i **Leverandører V2 (msdyn\_vendors)**-tilordningen, og lagre deretter tilordningen.
6. Kjør den innledende synkroniseringen igjen for tilordningen **Leverandører V2 (msdyn\_vendors)**. Siden endringssporing er slått av, synkroniseres alle postene.
7. Slå sporingsendring på igjen for **Leverandører V2**-enheten.

## <a name="resolve-errors-in-the-customers-v3toaccounts-entity-mapping"></a><a id="error-customer-map"></a>Utbedre feil i enhetstilordningen Kunder V3 til Kontoer

Det kan hende du møter på feil med innledende synkronisering for tilordningen **Kunder V3** til **Kontoer** hvis enhetene har eksisterende poster med verdier i feltene **ContactPersonID** og **InvoiceAccount**. Disse feilene skjer fordi **InvoiceAccount** er et selvrefererende felt, og **ContactPersonID** er en sirkelreferanse i leverandørtilordningen.

Feilmeldingene du mottar, vil ha følgende form.

*Fant ikke GUID for feltet: \<field\>. Oppslaget ga ingen treff: \<value\>. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Her er noen eksempler:

- *Fant ikke GUID for feltet: primarycontactid.msdyn\_contactpersonid. Oppslaget ga ingen treff: 000056. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Fant ikke GUID for feltet: msdyn\_billingaccount.accountnumber. Oppslaget ga ingen treff: 1206-1. Prøv disse URL-ene for å kontrollere at referansedataene finnes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Hvis noen poster i kundeenheten har verdier i feltene **ContactPersonID** og **InvoiceAccount**, følger du disse trinnene for å fullføre den innledende synkroniseringen. Du kan bruke denne fremgangsmåten for alle de kunderettede enhetene, for eksempel **Kontoer** og **Kontakter**.

1. I Finance and Operations-appen sletter du feltene **ContactPersonID** og **InvoiceAccount** fra **Kunder V3 (kontoer)**-tilordningen, og deretter lagrer du tilordningen.

    1. På siden for tilordning med dobbeltskriving for **Kunder V3 (Kontoer)**, i kategorien **Enhetstilordninger**-fanen, i filteret til venstre, velger du **Finance and Operations-app.Customers V3**. I filteret til høyre velger du **Common Data Service .Account**.
    2. Søk etter **contactperson** for å finne kildefeltet **ContactPersonID**.
    3. Velg **Handlinger**, og velg deretter **Slett**.

        ![Slette ContactPersonID-feltet](media/cust_selfref3.png)

    4. Gjenta disse trinnene for å slette feltet **InvoiceAccount**.

        ![Slette InvoiceAccount-feltet](media/cust_selfref4.png)

    5. Lagre endringene i tilordningen.

2. Deaktiver sporing av endringer for **Kunder V3**-enheten.

    1. I **Dataadministrasjon**-arbeidsområdet velger du flisen **Dataenheter**.
    2. Velg **Kunder V3**-enheten.
    3. I handlingsruten velger du **Alternativer**, og deretter velger du **Endringssporing**.

        ![Velge alternativet Endringssporing](media/selfref_options.png)

    4. Velg **Deaktiver endringssporing**.

        ![Velge Deaktiver endringssporing](media/selfref_tracking.png)

3. Kjør den innledende synkroniseringen på nytt for **Kunder V3 (Kontoer)**-tilordningen. Den innledende synkroniseringen skal kjøres uten feil.
4. Kjør den innledende synkroniseringen for **CDS-kontakter V2 (kontakter)**-tilordningen.

    > [!NOTE]
    > Det er to tilordninger med samme navn. Sørg for å velge tilordningen med følgende beskrivelse i fanen **Detaljer**: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Krever ny pakke \[Dynamics365SupplyChainExtended\].**

5. Legg til feltene **InvoiceAccount** og **ContactPersonId** i **Kunder V3 (Kontoer)** -tilordningen igjen, og lagre deretter tilordningen. Både **InvoiceAccount**- og **ContactPersonId**-feltene er nå en del av modus for direkte synkronisering igjen. I neste trinn skal du utføre den innledende synkroniseringen for disse feltene.
6. Kjør den innledende synkroniseringen på nytt for **Kunder V3 (Kontoer)**-tilordningen. Siden endringssporing er slått av, synkroniseres dataene for **InvoiceAccount** og **ContactPersonId** fra Finance and Operations-appen til Common Data Service.
7. Hvis du vil synkronisere dataene for **InvoiceAccount** og **ContactPersonId** fra Common Data Service til Finance and Operations-appen, må du bruke et dataintegrasjonsprosjekt.

    1. Under Power Apps oppretter du et dataintegrasjonsprosjekt mellom **Sales.Account** og **Finance and Operations apps.Kunder V3**-enheter. Dataretningen må være fra Common Data Service til Finance and Operations-appen. Fordi **InvoiceAccount** er et nytt attributt med dobbeltskriving, kan det hende du bør hoppe over innledende synkronisering for dette attributtet. Hvis du vil ha mer informasjon, se [Integrere data i Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Illustrasjonen nedenfor viser et prosjekt som oppdaterer **CustomerAccount** og **ContactPersonId**.

        ![Dataintegrasjonsprosjekt for å oppdatere CustomerAccount og ContactPersonId](media/cust_selfref6.png)

    2. Legg til firmakriteriene i filteret på Common Data Service-siden, slik at bare postene som samsvarer med filterkriteriene, blir oppdatert i Finance and Operations-appen. Velg filterknappen for å legge til et filter. Deretter, i dialogboksen **Rediger spørring**, kan du legge til en filterspørring som for eksempel **\_msdyn\_company\_value eq '\<guid\>'**. 

        > [MERK] Hvis filterknappen ikke finnes, oppretter du en støtteforespørsel for å be dataintegreringsgruppen aktivere filterfunksjonen i leieren din.

        Hvis du ikke angir en filterspørring for **\_msdyn\_company\_value**, blir alle postene synkronisert.

        ![Legge til en filterspørring](media/cust_selfref7.png)

    Den innledende synkroniseringen av oppføringene er nå fullført.

8. I Finance and Operations-appen aktiverer du endringssporing igjen for **Kunder V3**-enheten.
