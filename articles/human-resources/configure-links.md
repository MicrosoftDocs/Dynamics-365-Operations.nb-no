---
title: Opprett koblinger fra Human Resources til et annet miljø
description: Denne artikkelen forklarer hvordan du oppretter en kobling fra Microsoft Dynamics 365 Human Resources til et annet Dynamics 365-miljø.
author: twheeloc
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9640f460ed7b0b1a0cfdffb7c318bf833f8627fc
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065301"
---
# <a name="create-links-from-human-resources-to-another-finance-environment"></a>Opprett koblinger fra Human Resources til et annet Finance-miljø

En kunde har kanskje to Dynamics 365-miljøer som vedkommende arbeider i. Kunden kan for eksempel ha et miljø i Dynamics 365 Human Resources i Finance-infrastrukturen og må koble seg til et annet miljø i Dynamics 365 Finance. 

Denne funksjonen tillater koblinger fra en Human Resources-side til en bestemt side i et annet Finance-miljø. Etter at koblingene er konfigurert, kan du angi hvor koblingen skal være tilgjengelig i Human Resources, og målsiden som skal åpnes i det andre miljøet.

> [!Note] 
> Du må aktivere **Forbedringer av brukeropplevelsen i Human Resouces** i **Funksjonsbehandling** for å få denne funksjonen.

## <a name="configure-target-systems"></a>Konfigurer målsystemer

I Human Resources kan systemansvarlige definere koblinger som vises på sider i **Human Resources**. Deler av konfigurasjonen er Finance-miljøer som du vil ha som mål for koblingen. 

Slik konfigurerer du målsystemet:
1. Velg **Konfigurer målsystem** på siden **Konfigurer koblinger**.  
2. Angi navnet på målsystemet, og oppgi nettadressen til Finance-miljøet. Etter at du har konfigurert målsystemene, kan du definere koblingene.

## <a name="configure-links"></a>Konfigurer koblinger

Hver kobling du oppretter, har følgende informasjon definert:
 - **Kobling**: Navnet på koblingen. Brukes bare til identifikasjon.
 - **Aktiver denne koblingen**: Angi **Ja** hvis du vil vise koblingen til brukere av Human Resources.
 - **Visningsnavn**: Angi navnet som skal vises som en kobling til det sekundære miljøet. 
 - **Vis kobling i skjema**: Velg hvilken side du vil vise koblingen på. Koblinger kan bare vises i arbeidsområdet **Ansattselvbetjening** og på sidene **Jobb**, **Stilling**, **Arbeider** og **Strømlinjeformet arbeider**.
 - **Gruppe**: Du kan ordne koblingene i grupper. Velg en eksisterende gruppe, eller opprett en ny ved å bruke **Gruppe**-kolonnen.
 - **Målsystem**: Velg målsystemet som ble opprettet ved hjelp av alternativet **Konfigurer målsystem**. Dette er det sekundære miljøet som skal brukes når du navigerer ved hjelp av koblingen.
 - **Bruk brukerens gjeldende firma**: Velg **Ja** hvis du vil bruke brukerens gjeldende firma når du går til Finance. Velg **Nei** for å velge firmaet som skal brukes.
 - Element på **Mål**-menyen: Angi menyelementet fra Finance-miljøet som koblingen skal bruke ved navigering. Menyelementer som du kan navigere direkte til, er tilgjenglige. 

   Slik finner du menyelementet som kreves:
   1. Gå til Finance-miljøet og åpne siden som er målet for navigasjonen. 
   2. Kopier menyelementet fra URL-adressen. Hvis du for eksempel vil at koblingen skal gå til ansattlisten i Finance and Operations, angir du verdien som vises etter "&mi" i URL-adressen. 
   3. Menyelementet for å navigere til siden for ansattlisten i dette eksemplet, er: HcmWorkerListPage_Employees.

 - **Koble til datakilde**: Velg kilden til dataene som koblingen refererer til. De vanligste kildene som **Arbeider** og **Posisjon** er tilgjengelige.

### <a name="access-to-links"></a>Tilgang til koblinger

Systemansvarlige vil se de nylig opprettede koblingene på de definerte sidene, selv om alternativet **Aktiver denne koblingen** er satt til **Nei**. Dette kan brukes til å teste koblinger før de vises til andre ansatte. Alle andre roller ser bare de konfigurerte koblingene når alternativet **Aktiver denne koblingen** er satt til **Ja**. Ansatte som har tilgang til sidene der koblingene vises, vil ha tilgang til koblingene.

Sikkerhetsrettigheter må også være definert for brukere i det sekundære miljøet for at de skal kunne få tilgang til sidene i dette miljøet. Hvis ikke vises en sikkerhetsdialogboks når koblingen brukes.


