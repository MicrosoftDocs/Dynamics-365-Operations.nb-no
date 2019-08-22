---
title: Integrert original for leverandør
description: Dette emnet beskriver integreringen av leverandørdata mellom Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 45808bc35aba04df6fcaf6b1cbfcc2461b0b65cb
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789225"
---
## <a name="integrated-vendor-master"></a>Integrert original for leverandør

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Begrepet *leverandør* refererer til en leverandørorganisasjon eller en enkelt innehaver som er en del av forsyningskjedeprosessen, og som leverer varer til virksomheten. Selv om *leverandør* er et etablert begrep i Microsoft Dynamics 365 for Finance and Operations, finnes det ikke noe leverandørbegrep i Dynamics 365 for Customer Engagement. I stedet overbelaster noen firmaer kontoenheten for å lagre både kundeinformasjon og leverandørinformasjon. Andre bedrifter bruker et egendefinert leverandørbegrep. Common Data Service-integrering støtter begge disse utforminger. Du kan derfor aktivere en av utformingene, avhengig av forretningsscenarioet.

Integrering av leverandørdata mellom Finance and Operations og Customer Engagement gjør at du kan bruke dataene i flere maler. Uansett hvor leverandørdataene kommer fra, er de integrert bak kulissene på tvers av applikasjonsgrenser og infrastrukturforskjeller. 

### <a name="vendor-data-flow"></a>Flyt for leverandørdata

Hvis du vil bruke Customer Engagement for leverandørkontroll, og du vil isolere leverandørinformasjon fra kundeinformasjon, kan du bruke den nye leverandørutformingen.

![Flyt for leverandørdata](media/dual-write-vendor-data-flow.png)

Hvis du vil bruke Customer Engagement for leverandørkontroll, og du vil fortsatt bruke kontoenheten til å lagre leverandørinformasjon, kan du bruke den nye utvidede leverandørutformingen. I denne utformingen lagres utvidet leverandørinformasjon, for eksempel leverandørgruppen og leverandørposteringsprofilen, i leverandørdetaljene.

![Utvidet flyt for leverandørdata](media/dual-write-vendor-detail.jpg)

Leverandørkontaktinformasjon ligner på kundekontaktinformasjon. I kulissene lagres kontaktpersonens informasjon og hentes fra de samme enhetene.

## <a name="templates"></a>Maler

Leverandørdata inkluderer all informasjon om leverandøren, for eksempel leverandørgruppe, adresser, kontaktinformasjon, betalingsprofil og fakturaprofil. En samling enhetstilordninger fungerer sammen under leverandørdatasamhandling, som vist i følgende tabell.

Finance and Operations  | Customer Engagement-programmet
------------------------|---------------------------------
Vendor V2               | Konto
Vendor V2               | Msdyn\_vendors
CDS-kontakter V2         | Kontakt
Leverandørgrupper           | Msdyn\_vendorgroups
Betalingsmåte for leverandør   | Msdyn\_vendorpaymentmethods
Betalingsplan        | Msdyn\_paymentschedules
Betalingsplan        | Msdyn\_paymentschedulelines
Betalingsdag, CDS         | Msdyn\_paymentdays
Betalingsdagslinjer, CDS   | Msdyn\_paymentdaylines
Betalingsbetingelser        | Msdyn\_paymentterms
Navnevedlegg            | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="vendor-v2-and-account"></a>Vendor V2 og konto 

Firmaer som bruker kontoenheten til å lagre leverandørinformasjon, kan fortsette å bruke den på samme måte. De kan også dra fordel av den eksplisitte leverandørfunksjonaliteten som kommer på grunn av Finance and Operations-integrasjonen.

## <a name="vendor-v2-and-msdyn_vendors"></a>Vendor V2 og Msdyn\_vendors

Bedrifter som bruker en egendefinert løsning for leverandører, kan benytte seg av leverandørkonseptet som blir introdusert i Common Data Service, på grunn av Finance and Operations-integrasjonen. 

<!-- ![vendor mappings](media/dual-write-vendors-1.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-2.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-3.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
VENDORACCOUNTNUMBER | = | msdyn\_vendoraccountnumber
VENDORGROUPID | = | msdyn\_vendorgroupid.msdyn\_vendorgroup
VENDORORGANIZATIONNAME | = | msdyn\_name
VENDORPARTYTYPE | \>\< | msdyn\_isperson
PERSONFIRSTNAME | = | msdyn\_firstname
PERSONLASTNAME | = | msdyn\_lastname
CREDITLIMIT | = | msdyn\_vendorcreditlimit
ISFOREIGNENTITY | \>\< | msdyn\_isforeignentity
ISONETIMEVENDOR | \>\< | msdyn\_isonetimevendor
ADDRESSBUILDINGCOMPLIMENT | = | msdyn\_addressbuildingcompliment
PERSONCHILDRENNAMES | = | msdyn\_childrennames
ADDRESSCITY | = | msdyn\_addresscity
ADDRESSCOUNTRYREGIONID | = | msdyn\_addresscountryregionid
ADDRESSCOUNTRYREGIONISOCODE | = | msdyn\_addresscountryregionisocode
ADDRESSCOUNTYID | = | msdyn\_addresscountyid
CREDITRATING | = | msdyn\_creditrating
ADDRESSDESCRIPTION | = | msdyn\_addressdescription
ADDRESSDISTRICTNAME | = | msdyn\_addressdistrictname
DUNSNUMBER | = | msdyn\_dunsnumber
ETHNICORIGINID | = | msdyn\_ethnicorigin
FORMATTEDPRIMARYADDRESS | = | msdyn\_formattedprimaryaddress
PERSONHOBBIES | = | msdyn\_hobbies
PERSONINITIALS | = | msdyn\_initials
LANGUAGEID | = | msdyn\_languageid
PERSONLASTNAMEPREFIX | = | msdyn\_lastnameprefix
PERSONMIDDLENAME | = | msdyn\_middlename
ORGANIZATIONNUMBER | = | msdyn\_organizationnumber
OURACCOUNTNUMBER | = | msdyn\_ourvendoraccountnumber
PAYMENTID | = | msdyn\_paymentid
PERSONPHONETICFIRSTNAME | = | msdyn\_phoneticfirstname
PERSONPHONETICMIDDLENAME | = | msdyn\_phoneticmiddlename
PERSONPHONETICLASTNAME | = | msdyn\_phoneticlastname
ORGANIZATIONPHONETICNAME | = | msdyn\_organizationphoneticname
ADDRESSPOSTBOX | = | msdyn\_addresspostbox
PRIMARYURL | = | msdyn\_primarycontacturl
PRIMARYEMAILADDRESS | = | msdyn\_primaryemailaddress
PRIMARYEMAILADDRESSDESCRIPTION | = | msdyn\_primaryemailaddressdescription
PRIMARYFACEBOOK | = | msdyn\_primaryfacebook
PRIMARYFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYFAXNUMBER | = | msdyn\_primaryfaxnumber
PRIMARYFAXNUMBERDESCRIPTION | = | msdyn\_primaryfaxnumberdescription
PRIMARYFAXNUMBEREXTENSION | = | msdyn\_primaryfaxnumberextension
PRIMARYLINKEDIN | = | msdyn\_primarylinkedin
PRIMARYLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescription
PRIMARYPHONENUMBER | = | msdyn\_pimaryphonenumber
PRIMARYPHONENUMBERDESCRIPTION | = | msdyn\_primaryphonenumberdescription
PRIMARYPHONENUMBEREXTENSION | = | msdyn\_primaryphonenumberextension
PRIMARYTELEX | = | msdyn\_primarytelex
PRIMARYTELEXDESCRIPTION | = | msdyn\_primarytelexdescription
PRIMARYTWITTER | = | msdyn\_primarytwitter
PRIMARYTWITTERDESCRIPTION | = | msdyn\_primarytwitterdescription
PRIMARYURLDESCRIPTION | = | msdyn\_primaryurldescription
PERSONPROFESSIONALSUFFIX | = | msdyn\_professionalsuffix
PERSONPROFESSIONALTITLE | = | msdyn\_professionatitle
ADDRESSSTATEID | = | msdyn\_addressstateid
ADDRESSSTREET | = | msdyn\_addressstreet
ADDRESSSTREETNUMBER | = | msdyn\_addressstreetnumber
VENDORKNOWNASNAME | = | msdyn\_vendorknownasname
ADDRESSZIPCODE | = | msdyn\_addresszipcode
DEFAULTPAYMENTDAYNAME | = | msdyn\_defaultpaymentdayname.msdyn\_name
DEFAULTPAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
DEFAULTPAYMENTTERMSNAME | = | msdyn\_paymentterms.msdyn\_name
HASONLYTAKENBIDS | \>\< | msdyn\_hasonlytakenbids
ISMINORITYOWNED | \>\< | msdyn\_isminorityowned
ISVENDORLOCALLYOWNED | \>\< | msdyn\_isvendorlocallyowned
ISSERVICEVETERANOWNED | \>\< | msdyn\_isserviceveteranowned
ISOWNERDISABLED | \>\< | msdyn\_ownerisdisabled
ISWOMANOWNER | \>\< | msdyn\_womanowner
PERSONANNIVERSARYDAY | = | msdyn\_personanniversaryday
PERSONANNIVERSARYYEAR | = | msdyn\_anniversaryyear
PERSONBIRTHDAY | = | msdyn\_birthday
PERSONBIRTHYEAR | = | msdyn\_birthyear
ORGANIZATIONEMPLOYEEAMOUNT | = | msdyn\_numberofemployees
VENDORHOLDRELEASEDATE | = | msdyn\_vendoronholdreleasedate
VENDORPARTYNUMBER | = | msdyn\_vendorpartynumber
ADDRESSLOCATIONID | = | msdyn\_addresslocationid
PERSONANNIVERSARYMONTH | = | msdyn\_vendorpersonanniversarymonth
PERSONBIRTHMONTH | = | msdyn\_vendorpersonbirthmonth
PERSONMARITALSTATUS | \>\< | msdyn\_maritalstatus
ADDRESSLATITUDE | \>\> | msdyn\_addresslatitude
ADDRESSLONGITUDE | \>\> | msdyn\_addresslongitude
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
CURRENCYCODE | = | msdyn\_currencycode.isocurrencycode
ISVENDORLOCATEDINHUBZONE | \>\< | msdyn\_isvendorlocatedinhubzone
DEFAULTVENDORPAYMENTMETHODNAME | = | msdyn\_vendorpaymentmethod.msdyn\_name
INVOICEVENDORACCOUNTNUMBER | = | msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber
PERSONGENDER | \>\< | msdyn\_gender
AREPRICESINCLUDINGSALESTAX | \>\< | msdyn\_priceincludessalestax
SALESTAXGROUPCODE | = | msdyn\_taxgroup.msdyn\_name
VENDORPRICETOLERANCEGROUPID | = | msdyn\_pricetolerancegroup.msdyn\_groupid

## <a name="contacts"></a>Kontakter

Denne malen synkroniserer all primær, sekundær og tertiær kontaktinformasjon, både for kunder og leverandører, mellom Finance and Operations og Customer Engagement. Du finner detaljer om enhetstilordningen i [Integrerte originalkunde](dual-write-customer.md#contacts).

## <a name="vendor-groups"></a>Leverandørgrupper

Denne malen synkroniserer leverandørgruppeinformasjon mellom Finance and Operations og Customer Engagement.

<!-- ![vendor groups mappings](media/dual-write-vendor-groups.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
DEFAULTPAYMENTTERMNAME | = | msdyn\_paymentterms.msdyn\_name
BESKRIVELSE | = | msdyn\_description
VENDORGROUPID | = | msdyn\_vendorgroup
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymentpermname.msdyn\_name

### <a name="vendor-payment-method"></a>Betalingsmåte for leverandør

Denne malen synkroniserer informasjon om leverandørbetalingsmåte mellom Finance and Operations og Customer Engagement.

<!-- ![vendor payment method mappings](media/dual-write-vendor-payment-method.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
NAVN | = | msdyn\_name
BESKRIVELSE | = | msdyn\_description
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
ALLOWPAYMENTCOPIES | \>\< | msdyn\_allowpaymentcopies
PAYMENTTYPE | \>\< | msdyn\_paymenttype
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
ACCOUNTTYPE | \>\< | msdyn\_accounttype
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingposting
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_postdatedcheckclearingposting
PROMISSORYNOTEDRAFTTYPE | \>\< | msdyn\_promissorynotedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit
