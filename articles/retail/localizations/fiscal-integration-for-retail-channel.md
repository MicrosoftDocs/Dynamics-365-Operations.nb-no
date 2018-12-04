---
title: "Økonomisk integrering for detaljhandelskanal"
description: "Dette emnet gir en oversikt over økonomisk integrering for Retail POS."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: nb-no
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a>Økonomisk integrering for detaljhandelskanal

[!include [banner](../includes/banner.md)]

Dette emnet er en oversikt over funksjonenen for økonomisk integrering som er tilgjengelig i Microsoft Dynamics 365 for Retail. Funksjonen for økonomisk integrering er et rammeverk som er utformet for å støtte lokale økonomilover som har som formål å unngå bedrageri i detaljhandelen. Vanlige scenarier som kan dekkes ved hjelp av økonomisk integrasjon:

- Skrive ut en bilagskvittering og gi den til kunden.
- Sikre innsendingen av opplysninger relatert til salg og returer som utføres på salgsstedet på en ekstern tjeneste som leveres av myndighetene.
- Bruke databeskyttelse med en digital signatur som er autorisert av myndighetene.

Dette emnet gir retningslinjer for å sette opp økonomisk integrasjon, slik at brukere kan utføre følgende oppgaver: 

- Konfigurere regnskapskoblinger, som er økonomisk enheter eller tjenester som brukes for bilagsregistreringsformål som lagring, digitale signaturer og sikker innsending av regnskapsdata.
- Konfigurere dokumentleverandøren, som definerer en utdatametode og en algoritme for regnskapsdokumentgenerering.
- Konfigurere bilagsregistreringsprosessen, som definerer en sekvens med trinn og en gruppe med koblinger som brukes på hvert trinn.
- Tilordne bilagsregistreringsprosesser til funksjonalitetsprofiler for salgsstedet.
- Tilordne tekniske profiler for kobling til maskinvareprofiler (for lokale regnskapskoblinger) eller POS-funksjonalitetsprofiler (for andre regnskapskoblingstyper).

## <a name="fiscal-integration-execution-flow"></a>Kjøringsflyt for regnskapsintegrering
Følgende scenario viser den vanlige kjøringsflyten for regnskapsintegrering.

1. Initialisering av bilagsregistreringsprosessen.
  
   Når du har utført noen handlinger der bilagsregistrering kreves, for eksempel etter en detaljhandelstransaksjon er fullført, knyttes bilagsregistreringsprosessen til gjeldende profil for salgsstedsfunksjonalitet.

1. Søke etter en regnskapskobling.
   
   For hvert regnskapskoblingstrinn som er inkludert i regnskapsregistreringsprosessen, utfører systemet et samsvar med listen over regnskapskoblinger. Disse koblingene har en funksjonell profil som er inkludert i den angitte koblingsgruppen, med en liste over koblinger som har en teknisk profil som er knyttet til den gjeldende maskinvareprofilen (bare for en koblingstype som er lik **Lokal**), eller med den gjeldende funksjonalitetsprofilen for salgssted (for andre koblingstyper).
   
1. Utføre den økonomiske integreringen.

   Systemet utfører alle nødvendige handlinger som er definert av en samling som er knyttet til koblingen som ble funnet. Dette gjøres i henhold til innstillingene for den funksjonelle profilen og tekniske profilen som ble funnet i det forrige trinnet for denne koblingen.

## <a name="setup-needed-before-using-fiscal-integration"></a>Konfigurasjon som kreves før regnskapsintegreringen brukes
Før du bruker regnskapsintegreringsfunksjonaliteten, bør du definere følgende innstillinger:

- Definer nummerserien på siden **Detaljhandelsparametere** for nummeret for funksjonell profil for regnskap.
  
- Definere nummerseriene på siden **Delte parametere for detaljhandel** for følgende referanser:
  
  - Nummer for teknisk profil for regnskap
  - Gruppenummer for regnskapskobling
  - Nummer for registreringsprosess

- Opprett en **Regnskapskobling** i **Detaljhandel > Kanaloppsett > Regnskapsintegrering > Regnskapskoblinger** for hver enhet eller tjeneste du planlegger å bruke for regnskapsintegreringsformål.

-  Opprett en **Leverandør for regnskapsdokument** i **Detaljhandel > Kanaloppsett > Regnskapsintegrering > Leverandører for regnskapsdokument** for alle regnskapskoblinger. Datatilordning regnes som en del av regnskapsdokumentleverandøren. Hvis du vil definere forskjellige datatilordninger for samme tilkobling (for eksempel tilstandsspesifikke reguleringer), bør du opprette forskjellige regnskapsdokumentleverandører.

- Opprett en **Funksjonell profil for kobling** i **Detaljhandel > Kanaloppsett > Regnskapsintegrering > Funksjonelle profiler for kobling** for hver regnskapsdokumentleverandør.
  - Velg et tilkoblingsnavn.
  - Velg en dokumentleverandør.
  - Angi mva-satsinnstillinger i **Tjenesteoppsett**-kategorien.
  - Angi mva-kodetilordning og tilordning av betalingsmiddeltype i **Datatilordning**-kategorien.

  #### <a name="examples"></a>Eksempler 

  |  | Format | Eksempel | 
  |--------|--------|--------|
  | Mva-satsinnstillinger | verdi: VATrate | 1 : 2000, 2 : 1800 |
  | Tilordning av mva-koder | VATcode : verdi | vat20: 1, vat18: 2 |
  | Tilordning av betalingsmiddeltyper | TenderTyp: verdi | Kontant: 1, kort: 2 |

- Opprett **Grupper for regnskapskobling** i **Detaljhandel > Kanaloppsett > Regnskapsintegrering > Gruppe for regnskapskobling**. En koblingsgruppe er et delsett av funksjonelle profiler som er knyttet til regnskapskoblinger som utfører identiske funksjoner, og brukes på samme stadium i en regnskapsregistreringsprosessen.

   - Legg til funksjonelle profiler i koblingsgruppen. Klikk på **Legg til** på siden **Funksjonelle profiler**, og velg et profilnummer.
   - Hvis du vil avbryte bruken av den funksjonelle profilen, må du sette **Deaktiver** til **Ja**. 
   
     Denne endringen påvirker bare den gjeldende koblingsgruppen. Du kan fortsette å bruke den samme funksjonsprofilen i andre tilkoblingsgrupper.

     >[!NOTE]
     > I en tilkoblingsgruppe kan hver regnskapkobling bare ha én funksjonsprofil.

- Opprett en **Teknisk profil for kobling** i **Detaljhandel > Kanaloppsett > Regnskapsintegrering > Tekniske profiler for kobling** for hver regnskapskobling.
  - Velg et tilkoblingsnavn.
  - Velg en tilkoblingstype. 
      - **Lokal** – Angi denne typen for fysiske enheter eller programmer som er installert på en lokal maskin.
      - **Intern** – Angi denne typen for regnskapsenheter og -tjenester som er koblet til serveren for detaljhandel.
      - **Ekstern** – For eksterne regnskapstjenester som en nettportal fra en skattemyndighet.
    
  - Angi innstillinger i kategorien **Tilkobling**.

      
 >[!NOTE]
 > En oppdatert versjon av en konfigurasjon som tidligere ble lastet inn, lastes for både funksjonelle og tekniske profiler. Hvis en passende kobling eller dokumentleverandør allerede er i bruk, vil du bli varslet. Som standard lagres alle endringer som er opprettet manuelt i funksjonelle og tekniske profiler. Hvis du vil overstyre disse profilene med standardsettet med parametere fra en konfigurasjon, klikker du på **Oppdater** på sidene **Funksjonelle profiler for kobling** og **Tekniske profiler for kobling**.
 
- Opprett en **Bilagsregistreringsprosess** i **Detaljhandel > Kanaloppsett > Regnskapsintegrering > Bilagsregistreringsprosesser** for hver unike prosess for regnskapsintegreringen. En registreringsprosess er definert av rekkefølgen på registreringstrinnene og koblingsgruppen som brukes på hvert trinn. 
  
  - Legg til registreringstrinn i prosessen:
      - Klikk **Legg til**.
      - Velg en tilkoblingstype.
      
      >[!NOTE]
      > Dette feltet definerer hvor systemet søker i en teknisk profil for koblingen, enten i maskinvareprofiler for koblingstypen **Lokal** eller i funksjonalitetsprofiler for salgssted for andre regnskapskoblingstyper.
      
   - Velg en tilkoblingsgruppe.
   
     >[!NOTE]
     > Klikk på **Valider** for å kontrollere integriteten til registreringsprosesstrukturen. Det anbefales at det foretas valideringer i følgende tilfeller:
       >- For en ny registreringsprosess etter at alle innstillinger er fullført, inkludert binding til funksjonalitetsprofiler for salgssted og maskinvareprofiler.
       >- Når du har utført oppdateringer til en eksisterende registreringsprosess.

-  Bind regnskapsregistreringsprosesser til funksjonalitetsprofiler for salgssted i **Detaljhandel > Kanaloppsett > Salgsstedsoppsett > Salgsstedsprofiler > Funksjonalitetsprofiler**.
   - Klikk på **Rediger**, og velg et **Prosessnummer** i kategorien **Bilagsregistreringsprosess**.
- Bind de tekniske profilene for kobling til maskinvareprofilene i **Detaljhandel > Kanaloppsett > Salgsstedsoppsett > Salgsstedsprofiler > Maskinvareprofiler**.
   - Klikk på **Rediger**, og klikk deretter på **Ny** i kategorien **Teknisk profil for regnskap**.
   - Velg en teknisk profil for kobling i feltet **Profilnummer**.
   
     >[!NOTE]
     > Du kan legge til flere tekniske profiler i en maskinvareprofil. Men dette støttes ikke hvis en maskinvareprofil har mer enn ett skjæringspunkt med en hvilken som helst koblingsgruppe. Hvis du vil unngå feil innstillinger, anbefales det at du validerer registreringsprosessen når du har oppdatert alle maskinvareprofiler.

