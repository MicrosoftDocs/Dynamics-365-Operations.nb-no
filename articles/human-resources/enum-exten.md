---
title: Utvidelsesmuligheter for basisopplisting for kjønn
description: Denne artikkelen gir en oversikt over utvidelsesmulighetene for basisopplistingen for kjønn.
author: twheeloc
ms.date: 05/23/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61a80c16d24d8fda264340d79ed393db3f635908
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749318"
---
# <a name="gender-base-enum-extensibility"></a>Utvidelsesmuligheter for basisopplisting for kjønn

Opplistingen **Gender** kan nå utvides. Denne artikkelen beskriver endringene du må gjøre i kodegrunnlaget hvis du planlegger å utvide opplistingen **Gender**.

## <a name="gender-vs-hcmpersongender"></a>Gender i forhold til HcmPersonGender

Det finnes to opplistinger for kjønnsverdier:

- **Gender** (Programplattform)
- **HcmPersonGender** (PersonnelManagement)

Opplistingen **Gender** brukes gjennom hele Microsoft Dynamics 365 Finance, mens **HcmPersonGender** er spesifikk for funksjonaliteten for forvaltningssystem for menneskelig kapital (HCM). Hvis du bruker HCM-funksjonalitet og gjør eventuelle endringer i opplistingen **Gender**, bør du vurdere å gjøre de samme endringene i **HcmPersonGender**. Hvis du for eksempel legger til **Transgender** i opplistingen **Gender**, legger du også til **Transgender** i opplistingen **HcmPersonGender**.

## <a name="hcmpersongendertranformutil-class"></a>HcmPersonGenderTranformUtil (klasse)

Den nye klassen **HcmPersonGenderTranformUtil** ble opprettet for å tillate oversettelse mellom de to basisopplistingene. I denne klassen er det to metoder: **convertGenderToHcmPersonGender** og **convertHcmPersonGenderToGender**. Du kan opprette en utvidelse ved å bruke klassen **Chain of Command** eller **hendelsesbehandlinger** og utvide begge metodene for å tilordne nye verdier som legges til i en av basisopplistingene.

## <a name="payrollstatewagetaxprepdp-class"></a>PayrollStateWageTaxPrepDP (klasse)

**PayrollStateWageTaxPrepDP** er dataleverandørklassen for SSRS-rapporten **Payroll State Wage Tax Prep** (SQL Server Reporting Services). For USA er tre verdier tilgjengelige: **Male**, **Female** og **Unspecified**. I metoden **populatePayrollStateWageTaxPrepTmp** finnes det en switch-setning som brukes til å tilordne verdien til opplistingen **HcmPersonGender** til et av tre felter: **IsMale**, **IsFemale** eller **IsUnspecifiedGender**. Standardverdien for switch-setningen er **IsUnspecifiedGender**. Hvis du legger til verdier i opplistingen **HcmPersonGender** for å tilordne på en annen måte, må du opprette en utvidelse ved å bruke klassen **Chain of Command** over metoden **populatePayrollStateWageTaxPrepTmp** for å endre verdien etter behov.

## <a name="smmoutlooksync_contact-class"></a>smmOutlookSync_Contact (klasse)

Integreringsklassen **smmOutlookSync_Contact** kobler verdier til og fra **Outlook** og **Contact persons**. **Outlook** støtter tre verdier: **Male**, **Female** og **Unspecified**. Klassen har to metoder som hjelper deg å tilordne **Genders** til **OutlookGenders**. Standardmetoden er **NonSpecific/UnSpecified**. Hvis du oppretter ytterligere verdier for opplistingen **Gender**, oppretter du en utvidelse ved å bruke klassen **Chain of Command** over begge metodene, og tilordner etter behov.
