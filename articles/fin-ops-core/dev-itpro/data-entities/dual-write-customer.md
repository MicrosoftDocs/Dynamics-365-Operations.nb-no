---
title: Integrerte originalkunde
description: Dette emnet beskriver integreringen av kundedata mellom Finance and Operations og Common Data Service.
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
ms.openlocfilehash: a66beb6338ea593247c79a11feb7f301d56f32a9
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572524"
---
# <a name="integrated-customer-master"></a>Integrerte originalkunde

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Det er vanlig at kundeposter mestres i mer enn ett program. Salgsaktivitet kan for eksempel hente inn kommersielle kundeposter gjennom et Sales-program, og e-handel eller detaljsalg kan hente inn kundeposter gjennom et Finance and Operations-program. Uansett hvor kundeposten kommer fra, er den integrert bak kulissene på tvers av applikasjonsgrenser og infrastrukturforskjeller. Integrert kundemestring hjelper håndtere multi-Mastering scenarier og gir en omfattende visning av kunden til Dynamics 365-programpakken.

## <a name="customer-data-flow"></a>Kundedataflyt

*Kunde* er et veldefinert begrep i programmer. Integreringen av kundedata innebærer derfor bare å harmonisere kundekonseptet mellom de to programmene. Følgende illustrasjon viser kundedataflyten.

![Kundedataflyt](media/dual-write-customer-data-flow.png)

Kunder kan grovt klassifiseres i to typer: kommersielle/organisatoriske kunder og forbrukere/sluttbrukere. Disse to kundetypene lagres og håndteres forskjellig i Finance and Operations og Common Data Service.

I Finance and Operations, både kommersielle/organisatoriske kunder og forbrukere/sluttbrukere er mastret i en enkelt tabell som heter **CustTable** (CustomerCustomerV3Entity), og de er klassifisert basert på **Type**-attributtet. (Hvis **Type** er satt til **Organisasjon**, er kunden en kommersiell/organisastorisk kunde, og hvis **Type** er satt til **Person**, er kunden en forbruker/sluttbruker.) Den primære kontaktpersoninformasjonen håndteres via SMMContactPersonEntity-enheten.

I Common Data Service, kommersielle/organisatoriske kunder er mastret i kontoenheten og identifiseres som kunder når **RelationshipType**-attributtet er satt til **Kunde**. Både forbrukere/sluttbrukere og kontaktpersonen representeres av Kontakt-enheten. Hvis du vil gi et klart skille mellom en forbruker/sluttbruker og en kontaktperson, har **Kontakt**-enheten et boolsk flagg som heter **Sellable**. Når **Sellable** er **True**, er kontakten en forbruker/sluttbruker, og tilbud og ordrer kan opprettes for denne kontakten. Når **Sellable** er **False**, er kontakten bare en primærkontaktperson for en kunde.

Når en ikke-salgbar kontakt deltar i en tilbuds- eller en ordreprosess er **Sellable** satt til **True** for å flagge kontakten som en salgbar kontakt. En kontakt som har blitt en salgbar kontakt, forblir en salgbar kontakt.

## <a name="templates"></a>Maler

Kundedata inkluderer all informasjon om kunden, for eksempel kundegruppe, adresser, kontaktinformasjon, betalingsprofil, fakturaprofil og fordelsstatus. En samling enhetstilordninger fungerer sammen under kundedatasamhandling, som vist i følgende tabell.

Finance and Operations-apper    | Andre Dynamics 365-apper
--------------------------|---------------------------------
Customer V3               | Konto
Customer V3               | Kontakt
CDS-kontakter V2           | Kontakt
Kundegrupper           | Msdyn\_customergroups
Kundebetalingsmåte   | Msdyn\_customerpaymentmethods
Fordelskort              | Msdyn\_loyaltycards
Betalingsplan          | Msdyn\_paymentschedules
Betalingsplan          | Msdyn\_paymentschedulelines
Betalingsdag, CDS           | Msdyn\_paymentdays
Betalingsdagslinjer, CDS     | Msdyn\_paymentdaylines
Betalingsbetingelser          | Msdyn\_paymentterms
Navnevedlegg              | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="customer-v3-to-account"></a>Customer V3 til konto

Denne malen synkroniserer kundens hoveddata for kommersielle og organisatoriske kunder mellom Finance and Operations-apper og Common Data Service.

<!-- ![](media/dual-write-account-1.png) -->

<!-- ![](media/dual-write-account-2.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
CUSTOMERACCOUNT | = | accountnumber
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
CREDITLIMIT | = | creditlimit
DELIVERYADDRESSCITY | = | address1\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
DELIVERYADDRESSCOUNTY | = | address1\_county
DELIVERYADDRESSLATITUDE | \> | address1\_latitude
DELIVERYADDRESSLONGITUDE | \> | address1\_longitude
DELIVERYADDRESSZIPCODE | = | address1\_postalcode
ORGANIZATIONNAME | = | name
ORGANIZATIONNUMBEROFEMPLOYEES | = | numberofemployees
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTTWITTER | = | primarytwitterid
PRIMARYCONTACTURL | = | websiteurl
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | beskrivelse
CREDITLIMITISMANDATORY | \>\< | msdyn\_creditlimitismandatory
CREDITRATING | = | msdyn\_creditrating
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
INVOICEACCOUNT | = | msdyn\_billingaccount.accountnumber
INVOICEADDRESS | \>\< | msdyn\_invoiceaddress
ISONETIMECUSTOMER | \>\< | msdyn\_onetimecustomer
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PAYMENTDAY | = | msdyn\_paymentday.msdyn\_name
PAYMENTMETHOD | = | msdyn\_customerpaymentmethod.msdyn\_name
PAYMENTSCHEDULE | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTTERMS | = | msdyn\_paymentterm.msdyn\_name
PAYMENTTERMSBASEDAYS | = | msdyn\_paymenttermsbasedays
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
PRIMARYCONTACTLINKEDIN | = | msdyn\_primarylinkedinid
TAXEXEMPTNUMBER | = | msdyn\_taxexemptnumber
VENDORACCOUNT | = | msdyn\_vendor.msdyn\_vendoraccountnumber
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
LANGUAGEID | \<\< | none
DELIVERYADDRESSSTREET | = | address1\_line1
DELIVERYADDRESSSTATE | = | address1\_stateorprovince
none | \>\> | address1\_addresstypecode
none | \>\> | customertypecode
PARTYTYPE | \<\< | none
PARTYNUMBER | = | msdyn\_partynumber

## <a name="customer-v3-to-contact"></a>Customer V3 til kontakt

Denne malen synkroniserer kundens hoveddata for forbrukere og sluttbrukere mellom Finance and Operations og andre Dynamics 365-apper.

<!-- ![](media/dual-write-contact-1.png) -->
<!-- ![](media/dual-write-contact-2.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
none | \>\> | msdyn\_sellable
PARTYTYPE | \<\< | none
PARTYNUMBER | = | msdyn\_partynumber
CUSTOMERACCOUNT | = | msdyn\_contactpersonid
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
PERSONFIRSTNAME | = | firstname
PERSONLASTNAME | = | lastname
PERSONMIDDLENAME | = | middlename
PERSONPROFESSIONALTITLE | = | jobtitle
PERSONGENDER | \>\< | gendercode
PERSONMARITALSTATUS | \>\< | familystatuscode
LANGUAGEID | \<\< | none
ADDRESSCITY | = | address1\_city
ADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
ADDRESSCOUNTY | = | address1\_county
ADDRESSLATITUDE | \> | address1\_latitude
ADDRESSLONGITUDE | \> | address1\_longitude
ADDRESSLOCATIONROLES | \<\< | none
ADDRESSSTATE | = | address1\_stateorprovince
ADDRESSSTREET | = | address1\_line1
ADDRESSZIPCODE | = | address1\_postalcode
ADDRESSPOSTBOX | = | address1\_postofficebox
none | \>\> | address1\_addresstypecode
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
none | \>\> | address2\_addresstypecode
DELIVERYADDRESSCITY | = | address3\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address3\_country
DELIVERYADDRESSCOUNTY | = | address3\_county
DELIVERYADDRESSLATITUDE | \> | address3\_latitude
DELIVERYADDRESSLONGITUDE | \>\> | address3\_longitude
DELIVERYADDRESSSTATE | = | address3\_stateorprovince
DELIVERYADDRESSSTREET | = | address3\_line1
DELIVERYADDRESSZIPCODE | = | address3\_postalcode
none | \>\> | address3\_addresstypecode
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTLINKEDIN | = | msdyn\_primaryinkedinid
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTER | = | msdyn\_primarytwitterid
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURL | = | websiteurl
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | beskrivelse

## <a name="contacts"></a>Kontakter

Denne malen synkroniserer all primær, sekundær og tertiær kontaktinformasjon, både for kunder og leverandører, mellom Finance and Operations og andre Dynamics 365-apper.

<!-- ![](media/dual-write-contacts.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn\_partynumber
ASSOCIATEDCONTACTTYPE | \<\< | none
FIRSTNAME | = | firstname
MIDDLENAME | = | middlename
LASTNAME | = | lastname
ASSOCIATEDCONTACTNUMBER | = | msdyn\_vendorcontactid.msdyn\_vendoraccountnumber
PRIMARYADDRESSCITY | = | address1\_city
PRIMARYADDRESSCOUNTRYREGIONID | = | address1\_country
PRIMARYADDRESSCOUNTYID | = | address1\_county
PRIMARYFAXNUMBER | = | fax
PRIMARYADDRESSSTATEID | = | address1\_stateorprovince
PRIMARYADDRESSSTREET | = | address1\_line1
PRIMARYADDRESSZIPCODE | = | address1\_postalcode
PRIMARYPHONENUMBER | = | telephone1
PRIMARYEMAILADDRESS | = | emailaddress1
EMPLOYMENTDEPARTMENT | = | department
NOTES | = | beskrivelse
GENDER | \>\< | gendercode
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid
PRIMARYURL | = | websiteurl
MARITALSTATUS | \>\< | familystatuscode
ISRECEIVINGDIRECTMAIL | \>\< | donotemail
EMPLOYMENTPROFESSION | = | jobtitle
SPOUSENAME | = | spousesname
none | \>\> | msdyn\_contactforvendor
none | \>\> | msdyn\_contactpersonid

## <a name="customer-groups"></a>Kundegrupper

Denne malen synkroniserer kundegruppeinformasjon mellom Finance and Operations og andre Dynamics 365-apper.

<!-- ![](media/dual-write-customer-groups.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
CUSTOMERGROUPID | = | msdyn\_groupid
BESKRIVELSE | = | msdyn\_description
ISSALESTAXINCLUDEDINPRICE | \>\< | msdyn\_issalestaxincludedinprice
PAYMENTTERMID | = | msdyn\_paymenttermid.msdyn\_name
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymenttermname.msdyn\_name

## <a name="customer-payment-methods"></a>Kundebetalingsmåter

Denne malen synkroniserer informasjon om kundebetalingsmåte mellom Finance and Operations og andre Dynamics 365-apper.

<!-- ![](media/dual-write-customer-payment-methods.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
NAVN | = | msdyn\_name
ACCOUNTTYPE | \>\< | msdyn\_accounttype
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingpostingenabled
ISSEPA | \>\< | msdyn\_issepa
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
BESKRIVELSE | = | msdyn\_description
PAYMENTTYPE | \>\< | msdyn\_paymenttype
CREATEANDDRAWBILLOFEXCHANGEDURINGINVOICEPOSTING | \>\< | msdyn\_invoiceupdate
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_enablepostdatescheckclearingposting
BILLOFEXCHANGEDRAFTTYPE | \>\< | msdyn\_billofexchangedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

## <a name="loyalty-cards"></a>Fordelskort

Denne malen synkroniserer informasjon om fordelskort mellom Finance and Operations og andre Dynamics 365-apper.

<!-- ![](media/dual-write-loyalty-cards.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
CARDNUMBER | = | msdyn\_cardnumber
CARDTENDERTYPE | \>\< | msdyn\_cardtendertype
PARTYNUMBER | = | msdyn\_partynumber
REPLACEMENTCARDNUMBER | \> | msdyn\_replacementcardnumber
OMOPERATINGUNITNUMBER | = | msdyn\_operatingunitnumber
LOYALTYENROLLMENTDATE | = | msdyn\_enrollmentdate

## <a name="payment-schedules"></a>Betalingsplaner

Denne malen synkroniserer referansedata om betalingsplan, både for kunder og leverandører, mellom Finance and Operations og andre Dynamics 365-apper.

<!-- ![](media/dual-write-payment-schedules.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
NAVN | = | msdyn\_name
BESKRIVELSE | = | msdyn\_description
ALLOCATIONMETHOD | \>\< | msdyn\_allocationmethod
PAYMENTFREQUENCYUNITS | \>\< | msdyn\_paymentfrequencyunit
PAYMENTFREQUENCY | = | msdyn\_paymentfrequency
NUMBEROFPAYMENTS | = | msdyn\_numberofpayments
FIXEDPAYMENTAMOUNT | = | msdyn\_fixedpaymentamount
MINIMUMPAYMENTAMOUNT | = | msdyn\_minimumpaymentamount
SALESTAXALLOCATIONMETHOD | \>\< | msdyn\_salestaxallocationmethod
NOTES | = | msdyn\_note

## <a name="payment-schedule-lines"></a>Linjer i betalingsplan

Synkroniserer referansedata om linjer i betalingsplan, både for kunder og leverandører, mellom Finance and Operations og andre Dynamics 365-apper.

<!-- ![](media/dual-write-payment-schedule-lines.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTSCHEDULENAME | \> | msdyn\_name
LINENUMBER | = | msdyn\_linenumber
PERIODSAFTERDUEDATE | = | msdyn\_periodsafterduedate
PERCENTORAMOUNT | \>\< | msdyn\_percentoramount
PERCENTORAMOUNTVALUE | = | msdyn\_percentoramountvalue

## <a name="payment-days"></a>Betalingsdager

Denne malen synkroniserer referansedata om betalingsdager, både for kunder og leverandører, mellom Finance and Operations og andre Dynamics 365-apper.

<!-- ![](media/dual-write-payment-days.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
NAVN | = | msdyn\_name
BESKRIVELSE | = | msdyn\_description

## <a name="payment-day-lines"></a>Betalingsdagslinjer

Denne malen synkroniserer referansedata om betalingsdagslinjer, både for kunder og leverandører, mellom Finance and Operations og andre Dynamics 365-apper.

<!-- ![](media/dual-write-payment-day-lines.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
CDSINTEGRATIONKEY | = | msdyn\_paymentdaylineid
FREQUENCY | \>\< | msdyn\_frequency
DAYOFWEEK | \>\< | msdyn\_dayofweek
DAYOFMONTH | = | msdyn\_dayofmonth
NAVN | = | msdyn\_paymentday.msdyn\_name

## <a name="payment-terms"></a>Betalingsbetingelser

Denne malen synkroniserer referansedata om betalingsbetingelser, både for kunder og leverandører, mellom Finance and Operations og andre Dynamics 365-apper.

<!-- ![](media/dual-write-payment-terms.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
BESKRIVELSE | = | msdyn\_description
NAVN | = | msdyn\_name
NUMBEROFMONTHS | = | msdyn\_numberofmonth
CUTOFFDAYOFMONTH | = | msdyn\_cutoffdayofmonth
ISCASHPAYMENT | \>\< | msdyn\_iscashpayment
NUMBEROFDAYS | = | msdyn\_days
ISCERTIFIEDCOMPANYCHECK | \>\< | msdyn\_iscertifiedcompanycheck
ISDEFAULTPAYMENTTERM | \>\< | msdyn\_isdefaultpaymentterm
CREDITCARDPAYMENTTYPE | \>\< | msdyn\_creditcardpaymenttype
CREDITCARDCREDITCHECKTYPE | \>\< | msdyn\_creditcardcreditchecktype
PAYMENTDAYNAME | = | msdyn\_paymentdayname.msdyn\_name
PAYMENTMETHODTYPE | \>\< | msdyn\_paymentmethodtype
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedulename.msdyn\_name

## <a name="name-affixes"></a>Navnevedlegg

Denne malen synkroniserer referansedata om navnevedlegg, både for kunder og leverandører, mellom Finance and Operations og andre Dynamics 365-apper.

<!-- ![](media/dual-write-name-affixes.png) -->

Kildefelt | Tilordningstype | Målfelt
---|---|---
AFFIX | = | msdyn\_affix
TYPE | \>\< | msdyn\_affixtype
BESKRIVELSE | = | msdyn\_description
