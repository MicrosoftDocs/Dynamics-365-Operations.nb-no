---
title: Hva er nytt eller endret i Dynamics 365 Talent – Core HR (31. oktober 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent – Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4851c62a19bb562c7f5f578aecbae99cfcdb982f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462128"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-31-2018"></a>Hva er nytt eller endret i Dynamics 365 Talent – Core HR (31. oktober 2018)

**Build 8.1.2031**

Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.

## <a name="create-links-from-talent-to-finance"></a>Opprette koblinger fra Talent til Finance
Med den nye navigeringsfunksjonaliteten kan du koble fra Talent til Finance, noe som gir deg direkte navigasjon til Finance-sider. Når koblinger er konfigurert, kan du angi navnet og gruppen for koblingen, hvor koblingen skal vises i Talent, og målsiden som skal åpnes i Finance.

#### <a name="coming-soon"></a>Kommer snart
Feltkontekst legges til i fremtiden for å tillate direkte navigasjon til tilsvarende poster i Finance. Du kan for eksempel bruke **Kobling til felt** for å gi kontekst for å navigere direkte til en bestemt ansatt eller posisjon i Finance.

### <a name="configure-target-systems"></a>Konfigurer målsystemer

I Talent kan systemansvarlige definere koblinger som skal vises gjennom arbeidsområdet for systemadministrasjon. En del av konfigurasjonen er Finance-miljøene som du vil navigere til som "mål" for koblingen. Du kan gjøre dette ved å gi systemet et navn og oppgi URL-adressen for Finance-miljøet. Her er et eksempel på en Finance-URL-adresse som du kunne angitt: https://devax00124aos.cloud.test.dynamics.com/. Når du har konfigurert målsystemene dine, kan du definere koblingene.

### <a name="configure-links"></a>Konfigurer koblinger

Hver kobling som opprettes, har følgende informasjon definert.

- Kobling – navnet på koblingen, brukes bare til identifikasjon.

- Aktiver denne koblingen – satt til **Ja** hvis du vil vise koblingen til brukere av Talent.

- Visningsnavn – definerer navnet som vises som en kobling til Finance. Disse dataene er for øyeblikket ikke er oversatt.

- Overflatekobling i skjema – velg hvilken side du vil vise koblingen på.

- Gruppe – Grupper er ikke obligatoriske, men hvis du vil organisere koblingene ved hjelp av grupper, velger du en eksisterende gruppe eller oppretter en ny med **Gruppe**-feltet.

- Målsystem – Velg målsystemet som ble opprettet ved hjelp av alternativet **Konfigurer målsystem**. Dette blir Finance-miljøet som skal brukes når du navigerer via koblingen.

- Bruk brukerens gjeldende firma – Velg **Ja** hvis du vil bruke brukerens gjeldende firmakontekst når du navigerer til Finance. Hvis **Nei** er valgt, kan du velge firmaet som skal brukes.

- Element på målmeny – Angi menyelementet fra Finance som koblingen skal bruke ved navigering. Menyelementer som du kan navigere direkte til, er tilgjenglige. For å åpne det påkrevde menyelementet åpner du Finance og åpner siden som er målet for navigasjonen. Kopier menyelementet fra URL-adressen. Hvis du for eksempel vil at koblingen skal gå til ansattlisten i Finance and Operations, angir du verdien som vises etter "&mi" i URL-adressen. https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees. Menyelementet for å navigere til siden for ansattlisten i dette eksemplet, er: HcmWorkerListPage_Employees.

- Koble til datakilde – Velg kilden til dataene som koblingen refererer til. De vanligste kildene som **Arbeider** og **Posisjon** er tilgjengelige.

- Kobling til felt – (kommer snart) Dette feltvalget tillater direkte navigasjon fra én enkelt post i Talent til én enkelt post i Finance.

### <a name="access-to-links"></a>Tilgang til koblinger

Systemansvarlige vil se de nylig opprettede koblingene på de definerte sidene, selv om alternativet **Aktiver denne koblingen** er satt til **Nei**. Dette kan brukes til å teste koblinger før de vises til andre ansatte. Alle andre roller vil bare se de konfigurerte koblingene når alternativet **Aktiver denne koblingen** er satt til **Ja**. Ansatte som har tilgang til sidene der koblingene vises, vil ha tilgang til koblingene.

Brukere kan også ha definert sikkerhetsrettigheter i Finance for å få tilgang til sidene i Finance and Operations. Hvis ikke vises en sikkerhetsdialogboks når koblingen brukes.


## <a name="other-changesfixes"></a>Andre endringer/reparasjoner

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a>Stillinger med en fremtidig startdato kan ikke tilordnes til en ny ansatt

Det er gjort endringer for å tillatte ansattilordninger til stillinger med dato i fremtiden. Stillinger som har startdatoer i fremtiden, kan velges, og ansattilordningen utføres ved lagring eller fullføring av arbeidsflyten (hvis arbeidsflyten er aktivert).

### <a name="new-employee-cannot-be-assigned-existing-position"></a>Ny ansatt kan ikke tilordnes eksisterende stilling

Det er gjort endringer, slik at ny ansattilordning nå kan tilordnes eksisterende stillinger.

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a>Ansiennitetsdato/kontoradresse forsvinner når startdatoen for ansettelsen er passert, og posten blir lagret

Endringer er gjort for å rette synligheten for **Ansiennitetsdato** og **Kontoradresse** under lagring av endringer for tidligere ansatte.

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a>Kan ikke angi data for ansettelser med dato i fremtiden på arbeidersiden

Ansettelsesdata for ansettelser med dato i fremtiden er deaktivert på hovedsiden for arbeider. Ansettelsesdata kan angis på sidene **Datobehandling**. Andre endringer vil bli gjort i fremtidige versjoner for å gjøre det mulig å registrere ansettelsesdata direkte under arbeidsflytprosessen.

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a>Legg til ValidFrom og ValidTo i HcmPersonalContactPersonEntity

DMF-enheten (Data Management Framework) HcmPersonalContactPersonEntity er oppdatert for å inkludere "gyldig fra"- og "gyldig til"- datoer for å aktivere bestemte fordelsintegreringsscenarier. 

## <a name="known-issue"></a>Kjent problem
- **Problem**: Når du legger til en ny tilknytning til en arbeider, nedtones **Ny** og **Rediger**-knappene. 
- **Løsning:** Før du åpner vedleggssiden må du kontrollere at faktaboksene på **Arbeider**-siden er lukket. Hvis faktaboksene er lukket når **Arbeider**-siden lastes, blir vedleggsknappene aktivert. (Dette problemet vil bli løst i neste plattformoppdatering.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]