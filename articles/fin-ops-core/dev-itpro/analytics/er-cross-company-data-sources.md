---
title: Kryssfirmadatakilder i elektronisk rapportering (ER)
description: Denne artikkelen forklarer hvordan du kan bruke kryssfirmadatakilder i elektronisk rapportering (ER).
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.form: ERModelMappingDesigner, ERFormatMappingLegalEntityFilterTable
ms.openlocfilehash: ec96533dd2da933d5275adadedc9a92a33e47a38
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277734"
---
# <a name="cross-company-data-sources-in-electronic-reporting-er"></a>Kryssfirmadatakilder i elektronisk rapportering (ER)

[!include[banner](../includes/banner.md)]

Du kan utforme elektronisk rapportering (ER)-formater for å generere utgående dokumenter i forskjellige formater. Når et dokument genereres, kaller et ER-format datakilder som ble konfigurert i en tilsvarende ER-modelltilordning. Hvis du vil konfigurere tilgang til programtabellene for henting av poster, kan du bruke ER-datakilder av typen **Tabellposter**. Når tilgangstabellen er en delt tabell (det vil si en tabell hvor dataene lagres uten en firma-ID), returnerer denne datakilden alle poster. Når tilgangstabellen er en firmaavhengig tabell (det vil si en tabell hvor dataene lagres per firma), vil denne datakilden returnere bare postene som er lagret for det gjeldende firmaet (det vil si firmakonteksten som ER-formatet kjører under).

Hver datakilde av **Tabellposter**-typen i en modelltilordning kan nå merkes som en kryssfirmadatakilde. Derfor kan du bruke datakilder av typen **Tabellposter** til å få tilgang til kryssfirmadata i programtabeller.

Hvis du merker en datakilde som kryssfirma, skjer følgende:

- For en datakilde som refererer til en delt tabell unntatt CompanyInfo, returnerer datakilden alle poster som finnes i referansetabellen. 
- For en datakilde som refererer til tabellen CompanyInfo, selv om CompanyInfo er en delt tabell, returnerer datakilden postene som inneholder identifikatoren for et firma fra det definerte området.
- For alle firmaavhengige tabeller returnerer datakilden postene i den refererte tabellen som inneholder identifikatoren for et firma fra det definerte området.

I dialogboksen for systemspørringen, når **Be om spørring** er aktivert for alle datakilder som er merket som kryssfirma, kan du manuelt velge ett eller flere firmaer som skal tas med i **Firmaområde**-kategorien.

> [!IMPORTANT]
> På samme måte som andre filtre beholdes firmafilteret som en sist brukt-verdi for spørringer når du kjører et ER-format. Filteret endres ikke automatisk hvis du endrer kryssfirmaverdien for en datakilde. Du bruker en annen kryssfirmaverdi for en annen datakilde ved å slette tilsvarende brukerspesifikke valg.

For hver datakilde som er merket som kryssfirma, kan du velge postene du vil bruke, ved hjelp av **FILTER**- og **WHERE**-funksjoner i ER-uttrykk. **DataAreaID**-feltet kan også brukes som en firma-ID. For øyeblikket er **dataAreaID**-feltet begrenset til følgende typer betingelser når **FILTER**-funksjonen brukes:

- Bare betingelser med én **dataAreaID**-feltsammenligning støttes.
- Bare sammenligninger med uttrykk som ikke avhenger av postlisteelementer, er tillatt.

Derfor er følgende uttrykk gyldig.

```ER Expression
FILTER (MyTable, MyTable.dataAreaID = $StringUserInputParameter)
While shown below expressions will not pass the validation:
FILTER (MyTable, MyTable.dataAreaID = MyTable2RecordsList.MyField)
FILTER (MyTable, 
    OR(
        MyTable.dataAreaID = $StringUserInputParameter1,
        MyTable.dataAreaID = $StringUserInputParameter2
    )
)
```

Som standard omfatter området alle selskaper i gjeldende program. Det kan imidlertid være begrenset. Hvis du vil begrense omfanget av kryssfirmadatatilgang for et enkelt ER-format, kan du tilordne et bestemt organisasjonshierarki til formatet. Når et hierarki er definert for et ER-format, returneres bare poster for juridiske enheter som vises i det tilordnede hierarkiet, selv om formatet kaller kryssfirmadatakilder. Når en referanse til et hierarki som ikke lenger finnes, er definert for et ER-format, brukes standardomfanget, og formatet kaller kryssfirmadatakilder. I dette tilfellet returneres poster for alle programfirmaer.

Legg merke til at når **Bruk utkast**-alternativet er aktivert for den tilordnede til et enkelt ER-formatorganisasjonshierarki, brukes de juridiske enhetene fra kladdeversjonen av dette hierarkiet til å identifisere området for kryssfirmadatakilder. Hvis kladdeversjonen ikke finnes, brukes de juridiske enhetene fra den siste publiserte versjonen av dette organisasjonshierarkiet for denne.

Legg merke til at når **Bruk utkast**-alternativet er deaktivert for den tilordnede til et enkelt ER-formatorganisasjonshierarki, brukes de juridiske enhetene fra den sist publiserte versjonen av dette organisasjonshierarkiet til å identifisere området for kryssfirmadatakilder. Gyldig dato for organisasjonshierarkier støttes ikke ennå i ER-rammeverket.

Hierarkiet kan tilordnes til et format på en bestemt side som kan åpnes fra ER-arbeidsområdet, eller ved hjelp av **Organisasjonsstyring \> Elektronisk rapportering \> Filter for juridisk enhet for formater**-menyelementet. For å få tilgang til siden må rettigheten **Vedlikehold filtre for juridisk enhet for formater** (ERMaintainFormatMappingLegalEntityFilters) gis til en bruker. Omfangsbegrensningen i hierarkibaserte juridiske enheter for formatet brukes i tillegg til begrensningen som brukeren kan angi manuelt i dialogboksen for systemspørringen. Skjæringspunktet mellom disse begrensningene blir brukt når formatet kjøres.

Hvis du vil vite mer om denne funksjonen, spiller du av oppgaveveiledningen **ER Få tilgang til poster for firmaavhengige tabeller i kryssfirmamodus**, som er en del av 7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677), og kan være lastet ned fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684). Denne oppgaveveiledning hjelper deg med å konfigurere en ER-modelltilordning og ER-format for å få tilgang til programtabeller i kryssfirmamodus.

Last ned følgende filer for å fullføre oppgaveveiledning:

- [ER-modellkonfigurasjon - CrossCompanyDataAccessModel.xml](https://download.microsoft.com/download/4/2/5/4258f891-7054-4821-aedd-3721ba25fdd5/CrossCompanyDataAccessModel.xml)
- [ER-formatkonfigurasjon - CrossCompanyDataAccessFormat.xml](https://download.microsoft.com/download/3/2/1/321deb75-3ba9-4323-99bf-207a52c60b5c/CrossCompanyDataAccessFormat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
