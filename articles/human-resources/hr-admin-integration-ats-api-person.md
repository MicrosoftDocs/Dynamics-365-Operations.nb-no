---
title: Person
description: Denne artikkelen beskriver Person-enheten for Dynamics 365 Human Resources.
author: jaredha
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c8adb2f06d1fcdfef8a42a04c5ebddd246ffc2ae
ms.sourcegitcommit: 69d7dd6a2d0dc7f2661c7d1f61e8874c7bde1448
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887351"
---
# <a name="person"></a>Person


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver Person-enheten for Dynamics 365 Human Resources.

Fysisk navn: mshr_dirpersonentity

### <a name="description"></a>beskrivelse

Denne enheten inneholder personlige opplysninger for enkeltpersonen som er kandidaten.

## <a name="json-representation"></a>JSON-representasjon

```json
{
    "mshr_partynumber": "String",
    "mshr_name": "String",
    "mshr_namealias": "String",
    "mshr_knownas": "String",
    "mshr_languageid": "String",
    "mshr_addressbooks": "String",
    "mshr_anniversaryday": Int,
    "mshr_anniversarymonth": Int,
    "mshr_anniversaryyear": Int,
    "mshr_birthday": Int,
    "mshr_birthmonth": Int,
    "mshr_birthyear": Int,
    "mshr_childrennames": "String",
    "mshr_gender": Int,
    "mshr_hobbies": "String",
    "mshr_initials": "String",
    "mshr_maritalstatus": Int,
    "mshr_phoneticfirstname": "String",
    "mshr_phoneticlastname": "String",
    "mshr_phoneticmiddlename": "String",
    "mshr_personalsuffix": "String",
    "mshr_personaltitle": "String",
    "mshr_professionalsuffix": "String",
    "mshr_professionaltitle": "String",
    "mshr_fullprimaryaddress": "String",
    "mshr_addresscity": "String",
    "mshr_addresscountryregionid": "String",
    "mshr_addresscountryregionisocode": "String",
    "mshr_addresscounty": "String",
    "mshr_addressdistrictname": "String",
    "mshr_addresslatitude": Decimal,
    "mshr_addresslocationid": "String",
    "mshr_addresslocationroles": "String",
    "mshr_addresslongitude": Decimal,
    "mshr_addressstate": "String",
    "mshr_addressstreet": "String",
    "mshr_addressvalidfrom": "Date",
    "mshr_addressvalidto": "Date",
    "mshr_addresszipcode": "String",
    "mshr_addressisprivate": Int,
    "mshr_addressdescription": "String",
    "mshr_primarycontactemail": "String",
    "mshr_primarycontactemaildescription": "String",
    "mshr_primarycontactemailisim": Int,
    "mshr_primarycontactemailpurpose": "String",
    "mshr_primarycontactfax": "String",
    "mshr_primarycontactfaxdescription": "String",
    "mshr_primarycontactfaxextension": "String",
    "mshr_primarycontactfaxpurpose": "String",
    "mshr_primarycontactphone": "String",
    "mshr_primarycontactphonedescription": "String",
    "mshr_primarycontactphoneextension": "String",
    "mshr_primarycontactphoneismobile": Int,
    "mshr_primarycontactphonepurpose": "String",
    "mshr_primarycontacttelex": "String",
    "mshr_primarycontacttelexdescription": "String",
    "mshr_primarycontacttelexpurpose": "String",
    "mshr_primarycontacturl": "String",
    "mshr_primarycontacturldescription": "String",
    "mshr_primarycontacturlpurpose": "String",
    "mshr_primarycontactfacebook": "String",
    "mshr_primarycontactfacebookdescription": "String",
    "mshr_primarycontactfacebookisprivate": Int,
    "mshr_primarycontactfacebookpurpose": "String",
    "mshr_primarycontactlinkedin": "String",
    "mshr_primarycontactlinkedindescription": "String",
    "mshr_primarycontactlinkedinisprivate": Int,
    "mshr_primarycontactlinkedinpurpose": "String",
    "mshr_primarycontacttwitter": "String",
    "mshr_primarycontacttwitterdescription": "String",
    "mshr_primarycontacttwitterisprivate": Int,
    "mshr_primarycontacttwitterpurpose": "String",
    "mshr_partytype": "String",
    "mshr_namesequencedisplayas": "String",
    "mshr_firstname": "String",
    "mshr_lastnameprefix": "String",
    "mshr_lastname": "String",
    "mshr_middlename": "String",
    "mshr_electroniclocationid": "String",
    "mshr_dirpersonentityid": "Guid",
    "mshr_addresstimezone": Int
}
```

## <a name="properties"></a>Egenskaper

| Egenskap<br>**Fysisk navn**<br>**_Type_** | Bruk | beskrivelse |
| --- | --- | --- |
| **Personenhets-ID**<br>mshr_dirpersonentityid<br>*GUID* | Skrivebeskyttet<br>Obligatorisk<br>Systemgenerert | En systemgenerert unik identifikator for enhetsposten. |
| **Partsnummer**<br>mshr_partynumber<br>*Streng* | Skrivebeskyttet<br>Obligatorisk<br>Systemgenerert | En brukerlesbar, systemgenerert unik identifikator for personen.  |
| **Navn**<br>mshr_name<br>*Streng* | Skrivebeskyttet<br>Obligatorisk | Feltverdien er en sammenslåing av Fornavn, Mellomnavn, Prefiks for etternavn og Etternavn i rekkefølgen som er definert i feltet **Navnerekkefølge vises som**. |
| **Navnealias**<br>mshr_namealias<br>*Streng* | Lese/skrive<br>Valgfri | Et navnealias som kan angis for personen. |
| **Kalt**<br>mshr_knownas<br>*Streng* | Lese/skrive<br>Valgfri | Navn som kan brukes for personen hvis vedkommende vanligvis kalles et annet navn. |
| **Språk-ID**<br>mshr_languageid<br>*Streng* | Lese/skrive<br>Valgfri | Språk-IDen for personens hovedspråk, som definert i ISO 639-1-format. |
| **Adressebøker**<br>mshr_addressbooks<br>*Streng* | Lese/skrive<br>Valgfri | Adresseboken personen kan tilordnes. Adressebøker som er definert for organisasjonen, vises i mshr_diraddressbooksentity-enheten. |
| **Merkedag**<br>mshr_anniversaryday<br>*Int* | Lese/skrive<br>Valgfri | Dagen for personens merkedag. |
| **Merkedagsmåned**<br>mshr_anniversarymonth<br>*mshr_monthsofyear-alternativsett* | Lese/skrive<br>Valgfri | Måneden for personens merkedag. |
| **Merkedagsår**<br>mshr_anniversaryyear<br>*Int* | Lese/skrive<br>Valgfri | Året for personens merkedag. |
| **Fødselsdag**<br>mshr_birthday<br>*Int* | Lese/skrive<br>Valgfri | Dagen for personens fødselsdag. |
| **Fødselsmåned**<br>mshr_birthmonth<br>*mshr_monthsofyear-alternativsett* | Lese/skrive<br>Valgfri | Måneden for personens fødselsdag. |
| **Fødselsår**<br>mshr_birthyear<br>*Int* | Lese/skrive<br>Valgfri | Året for personens fødselsdag. |
| **Navn på barn**<br>mshr_childrennames<br>*Streng* | Lese/skrive<br>Valgfri | Streng for navnene på personens barn. Det er ingen påkrevd avgrensning. |
| **Kjønn**<br>mshr_gender<br>*mshr_hcmpersongender-alternativsett* | Lese/skrive<br>Valgfri | Personens kjønn. |
| **Hobbyer**<br>mshr_hobbies<br>*Streng* | Lese/skrive<br>Valgfri | Personens hobbyer. |
| **Initialer**<br>mshr_initials<br>*Streng* | Lese/skrive<br>Valgfri | Initialene for personens navn. |
| **Sivilstand**<br>mshr_maritalstatus<br>*mshr_hcmpersonmaritalstatus-alternativsett* | Lese/skrive<br>Valgfri | Personens sivilstand. |
| **Fonetisk fornavn**<br>mshr_phoneticfirstname<br>*Streng* | Lese/skrive<br>Valgfri | Den fonetiske uttalen av personens fornavn. |
| **Fonetisk etternavn**<br>mshr_phoneticlastname<br>*Streng* | Lese/skrive<br>Valgfri | Den fonetiske uttalen av personens etternavn. |
| **Fonetisk mellomnavn**<br>mshr_phoneticmiddlename<br>*Streng* | Lese/skrive<br>Valgfri | Den fonetiske uttalen av personens etternavn. |
| **Personlig suffiks**<br>mshr_personalsuffix<br>*Streng* | Lese/skrive<br>Valgfri | Personens personlige suffiks. Gyldige verdier i mshr_dirnameaffixentity-enheten, der mshr_type er Suffiks (200000001). |
| **Personlig tittel**<br>mshr_personaltitle<br>*Streng* | Lese/skrive<br>Valgfri | En personlig tittel for personen. Gyldige verdier i mshr_dirnameaffixentity-enheten, der mshr_type er Tittel (200000000).
| **Profesjonelt suffiks**<br>mshr_professionalsuffix<br>*Streng* | Lese/skrive<br>Valgfri | Et profesjonelt suffiks. |
| **Yrkestittel**<br>mshr_professionaltitle<br>*Streng* | Lese/skrive<br>Valgfri | En yrkestittel. |
| **Full primæradresse**<br>mshr_fullprimaryaddress<br>*Streng* | Lese/skrive<br>Valgfri | Personens fullstendige primæradresse, en sammenslåing av primæradressefeltene. |
| **Adresse, by**<br>mshr_addresscity<br>*Streng* | Lese/skrive<br>Valgfri | Poststed i personens primæradresse. Defineres i enheten mshr_logisticsaddresscityentity. |
| **Adresse Land Område**<br>mshr_addresscountryregionid<br>*Streng* | Lese/skrive<br>Valgfri | Land/område i personens primæradresse. Gyldige verdier i enheten mshr_logisticsaddresscountryregionentity. |
| **Adresse Land Område ISO-kode**<br>mshr_addresscountryregionisocode<br>*Streng* | Lese/skrive<br>Valgfri | ISO-kode for landet i personens primæradresse. |
| **Områdeadresse**<br>mshr_addresscounty<br>*Streng* | Lese/skrive<br>Valgfri | Området i personens primæradresse. Defineres i enheten mshr_logisticsaddresscountyentity. |
| **Adresse Distrikt Navn**<br>mshr_addressdistrictname<br>*Streng* | Lese/skrive<br>Valgfri | Distriktet i personens primæradresse. Defineres i enheten mshr_logisticsaddressdistrictentity. |
| **Breddegrad for adresse**<br>mshr_addresslatitude<br>*Streng* | Lese/skrive<br>Valgfri | Breddegrad for personens primæradresse. |
| **Adresselokasjons-ID**<br>mshr_addresslocationid<br>*Streng* | Lese/skrive<br>Valgfri | Den unike identifikatoren til lokasjonen til personens primæradresse. Gyldige verdier i enheten mshr_logisticspostaladdresslocationcdsentity. |
| **Adresselokasjonsroller**<br>mshr_addresslocationroles<br>*Streng* | Lese/skrive<br>Valgfri | Lokasjonsrollen til personens primæradresse. Defineres i enheten mshr_logisticslocationrolecdsentity. |
| **Lengdegrad for adresse**<br>mshr_addresslongitude<br>*Streng* |  Lese/skrive<br>Valgfri | Lengdegrad for personens primæradresse. |
| **Adressestat**<br>mshr_addressstate<br>*Streng* | Lese/skrive<br>Valgfri | Staten i personens primæradresse. Defineres i enheten mshr_logisticsaddressstateentity. |
| **Gateadresse**<br>mshr_addressstreet<br>*Streng* | Lese/skrive<br>Valgfri | Gateadresse i personens primæradresse. |
| **Adresse gyldig fra**<br>mshr_addressvalidfrom<br>*Dato* | Lese/skrive<br>Valgfri | Datoen som personens primæradresse er gyldig fra. |
| **Adresse gyldig til**<br>mshr_addressvalidto<br>*Dato* | Lese/skrive<br>Valgfri | Datoen som personens primæradresse er gyldig til. |
| **Adresse-postnummer**<br>mshr_addresszipcode<br>*Streng* | Lese/skrive<br>Valgfri | Postnummer for personens primæradresse. Defineres i enheten mshr_logisticsaddresspostalcodeentity. |
| **Adresse er privat**<br>mshr_addressisprivate<br>*mshr_noyes-alternativsett* | Lese/skrive<br>Valgfri | Bestemmer om personens primæradresse skal deles med andre i organisasjonen. |
| **Adressebeskrivelse**<br>mshr_addressdescription<br>*Streng* | Lese/skrive<br>Valgfri | Beskrivelse av personens primæradresse. |
| **Primær kontakt-e-post**<br>mshr_primarycontactemail<br>*Streng* | Lese/skrive<br>Valgfri | Personens primære e-postadresse. |
| **Beskrivelse av primær e-post**<br>mshr_primarycontactemaildescription<br>*Streng* | Lese/skrive<br>Valgfri | En beskrivelse for den primære e-postadressen. |
| **Primær e-post tilgjengelig for direktemelding**<br>mshr_primarycontactemailisim<br>*mshr_noyes-alternativsett* | Lese/skrive<br>Valgfri | Avgjør om den primære e-postadressen er tilgjengelig for direktemeldinger. |
| **Formål med primær e-post**<br>mshr_primarycontactemailpurpose<br>*Streng* | Lese/skrive<br>Valgfri | Formålet med den primære e-postadressen. Defineres i enheten mshr_logisticslocationroleentity. |
| **Primær kontaktfaks**<br>mshr_primarycontactfax<br>*Streng* | Lese/skrive<br>Valgfri | Primært faksnummer. |
| **Beskrivelse av primær faks**<br>mshr_primarycontactfaxdescription<br>*Streng* | Lese/skrive<br>Valgfri | Beskrivelse av det primære faksnummeret. |
| **Direktenummer til primær faks**<br>mshr_primarycontactfaxextension<br>*Streng* | Lese/skrive<br>Valgfri | Direktenummer til primær faks. |
| **Formål med primær faks**<br>mshr_primarycontactfaxpurpose<br>*Streng* | Lese/skrive<br>Valgfri | Formålet med primært faksnummer. Defineres i enheten mshr_logisticslocationroleentity.
| **Primær kontakttelefon**<br>mshr_primarycontactphone<br>*Streng* | Lese/skrive<br>Valgfri | Hovedtelefonnummer. |
| **Beskrivelse av primær kontakttelefon**<br>mshr_primarycontactphonedescription<br>*Streng* | Lese/skrive<br>Valgfri | Beskrivelse av det primære telefonnummeret. |
| **Direktenummer til primærtelefon**<br>mshr_primarycontactphoneextension<br>*Streng* | Lese/skrive<br>Valgfri | Direktenummer til primærtelefon. |
| **Primær kontakttelefon er mobil**<br>mshr_primarycontactphoneismobile<br>*mshr_noyes-alternativsett* | Lese/skrive<br>Valgfri | Bestemmer om primærtelefonnummeret er en mobiltelefon. |
| **Formål med primær kontakttelefon**<br>mshr_primarycontactphonepurpose<br>*Streng* | Lese/skrive<br>Valgfri | Formålet med primært telefonnummer. Defineres i enheten mshr_logisticslocationroleentity. |
| **Primær kontaktteleks**<br>mshr_primarycontacttelex<br>*Streng* | Lese/skrive<br>Valgfri | Primært teleksnummer. |
| **Beskrivelse av primær teleks**<br>mshr_primarycontacttelexdescription<br>*Streng* | Lese/skrive<br>Valgfri | Beskrivelse av det personens primære teleksnummer. |
| **Formål med primær teleks**<br>mshr_primarycontacttelexpurpose<br>*Streng* | Lese/skrive<br>Valgfri | Formålet med personens primære teleksnummer. Defineres i enheten mshr_logisticslocationroleentity. |
| **Primær kontakt-URL**<br>mshr_primarycontacturl<br>*Streng* | Lese/skrive<br>Valgfri | Den primære URL-adressen. |
| **Beskrivelse av primær URL-adresse**<br>mshr_primarycontacturldescription<br>*Streng* | Lese/skrive<br>Valgfri | Beskrivelse av personens primære URL-adresse. |
| **Formål med primær URL**<br>mshr_primarycontacturldescription<br>*Streng* | Lese/skrive<br>Valgfri | Formålet med personens primære URL-adresse. Defineres i enheten mshr_logisticslocationroleentity. |
| **Primær Facebook**<br>mshr_primarycontactfacebook<br>*Streng* | Lese/skrive<br>Valgfri | Primær Facebook-konto. Identifisert av Bruker-ID. |
| **Beskrivelse av primær Facebook-konto**<br>mshr_primarycontactfacebookdescription<br>*Streng* | Lese/skrive<br>Valgfri | Beskrivelse av personens primære Facebook-adresse. |
| **Primær Facebook-konto er privat**<br>mshr_primarycontactfacebookisprivate<br>*mshr_noyes-alternativsett* | Lese/skrive<br>Valgfri | Bestemmer om primær Facebook-konto er synlig for andre brukere. |
| **Formål med primær Facebook-konto**<br>mshr_primarycontactfacebookpurpose<br>*Streng* | Lese/skrive<br>Valgfri | Formålet med personens primære Facebook-konto. Defineres i enheten mshr_logisticslocationroleentity. |
| **Primær LinkedIn**<br>mshr_primarycontactlinkedin<br>*Streng* | Lese/skrive<br>Valgfri | Primær LinkedIn-konto. Identifisert av brukernavn. |
| **Beskrivelse av primær LinkedIn-konto**<br>mshr_primarycontactlinkedindescription<br>*Streng* | Lese/skrive<br>Valgfri | Beskrivelse av personens primære LinkedIn-konto. |
| **Primær LinkedIn-konto er privat**<br>mshr_primarycontactlinkedinisprivate<br>*mshr_noyes-alternativsett* | Lese/skrive<br>Valgfri | Bestemmer om personens primære LinkedIn-kontoinformasjon skal deles med andre. |
| **Formål med primær LinkedIn-konto**<br>mshr_primarycontactlinkedinpurpose<br>*Streng* | Lese/skrive<br>Valgfri | Formålet med personens primære LinkedIn-konto. Defineres i enheten mshr_logisticslocationroleentity. |
| **Primær Twitter**<br>mshr_primarycontacttwitter<br>*Streng* | Lese/skrive<br>Valgfri | Personens primære Twitter-konto. Identifisert av @brukernavn. |
| **Beskrivelse av primær Twitter-konto**<br>mshr_primarycontacttwitterdescription<br>*Streng* | Lese/skrive<br>Valgfri | Beskrivelse av personens primære Twitter-konto. |
| **Primær Twitter-konto er privat**<br>mshr_primarycontacttwitterisprivate<br>*mshr_noyes-alternativsett* | Lese/skrive<br>Valgfri | Bestemmer om personens primære Twitter-kontoinformasjon skal deles med andre. |
| **Formål med primær Twitter-konto**<br>mshr_primarycontacttwitterpurpose<br>*Streng* | Lese/skrive<br>Valgfri | Formålet med personens primære Twitter-konto. Defineres i enheten mshr_logisticslocationroleentity. |
| **Partstype**<br>mshr_partytype<br>*Streng* | Lese/skrive<br>Valgfri | Parttypen til personen. Vil alltid være **Person** for kandidater. |
| **Navnerekkefølgen vises som**<br>mshr_namesequencedisplayas<br>*Streng* | Lese/skrive<br>Valgfri | Rekkefølgen som personens navneegenskaper er slått sammen til for å danne verdien for Navn-egenskapen (mshr_name). |
| **Fornavn**<br>mshr_firstname<br>*Streng* | Lese/skrive<br>Obligatorisk | Personens fornavn. |
| **Mellomnavn**<br>mshr_middlename<br>*Streng* | Lese/skrive<br>Valgfri | Personens mellomnavn. |
| **Prefiks for etternavn**<br>mshr_lastnameprefix<br>*Streng* | Lese/skrive<br>Valgfri | Prefikset til personens etternavn. |
| **Etternavn**<br>mshr_lastname<br>*Streng* | Lese/skrive<br>Valgfri | Personens etternavn. |
| **ID for elektronisk lokasjon**<br>mshr_electroniclocationid<br>*Streng* | Lese/skrive<br>Valgfri | IDen til personens elektroniske lokasjon. |
| **Tidssone for adresse**<br>mshr_addresstimezone<br>*Int* | Lese/skrive<br>Valgfri | Tidssonen for personens primæradresse. |

## <a name="see-also"></a>Se også

[Innføring i API for søkersporingssystemintegrering](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
