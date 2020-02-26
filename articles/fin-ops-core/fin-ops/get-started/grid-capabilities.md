---
title: Rutenettfunksjoner
description: Dette emnet beskriver flere kraftfulle funksjoner i rutenettkontrollen. Den nye rutenettfunksjonen må være aktivert for at du skal kunne få tilgang til disse funksjonene.
author: jasongre
manager: AnnBe
ms.date: 01/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b49d7823f48bcc9cdbb56b87d5fa72d46ddfa15c
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019931"
---
# <a name="grid-capabilites"></a>Rutenettfunksjoner

[!include [banner](../includes/banner.md)]

Den nye rutenettkontrollen tilgjengeliggjør en rekke nyttige og kraftfulle funksjoner som kan brukes til å forbedre brukerproduktivitet, konstruere mer interessante visninger av dataene og få meningsfulle innsikter i dataene. Denne artikkelen dekker følgende funksjoner: 

-  Beregner totaler
-  Gruppering av data
-  Skriving i forkant av systemet
-  Evaluering av matematiske uttrykk 

## <a name="calculating-totals"></a>Beregner totaler
I Finance and Operations-apper har brukere muligheten til å se totalverdier nederst i numeriske kolonner i rutenett. Disse totalverdiene vises i en bunntekstinndeling nederst i rutenettet. 

### <a name="showing-the-grid-footer"></a>Vise rutenettbunnteksten
Hvert tabellrutenett i Finance and Operations-apper har et bunntekstområde nederst i rutenettet som kan vise verdifull informasjon relatert til dataene som vises. Denne informasjonen inkluderer: 
-  Antallet valgte rader i tabellen (når mer enn én oppføring er valgt)
-  Hovedsummer nederst i konfigurerte numeriske kolonner
-  Antallet rader i datasettet 

Denne bunnteksten er skjult som standard, men den kan enkelt aktiveres. Hvis du vil vise bunnteksten for et rutenett, høyreklikker du på en kolonneoverskrift i rutenettet og velger **Vis bunntekst**-alternativet. Når bunnteksten er aktivert for et bestemt rutenett, vil denne innstillingen bli husket til brukeren velger å skjule bunnteksten, noe som kan gjøres ved å høyreklikke på en kolonneoverskrift og velge **Skjul bunntekst**.  Vær oppmerksom på at plasseringen av **Vis bunntekst / Skjul bunntekst**-handlingen forventes å bli forflyttet i en fremtidig oppdatering. 

### <a name="specifying-columns-with-totals"></a>Angi kolonner med totalverdier
For øyeblikket er ingen kolonner konfigurert til å vise totalverdier som standard. I stedet betraktes dette som en engangsoppsettsaktivitet, som tilsvarer justering av bredden på kolonnene i rutenett. Når du har angitt at du vil se totalverdier for en kolonne, vil denne innstillingen bli husket neste gang du besøker siden.  

Det finnes to måter for å konfigurere en kolonne til å vise en totalverdi: 
1.  Høyreklikk på kolonnen du er interessert i å se en totalverdi for, og velg **Summer denne kolonnen**. Denne handlingen vil utføre tre ting. For det første gjør den bunnteksten synlig. For det andre lagrer den preferansene dine for å se totalverdien for denne kolonnen. For det tredje vil denne handlingen starte en beregning av totalverdier for denne kolonnen og alle andre kolonner du tidligere konfigurerte til å se totalverdier. Tiden det tar før en totalverdi vises, er direkte knyttet til størrelsen på datasettet du summerer.  

2.  Når bunnteksten er vist, kan du alternativt klikke på **Vis totalverdi**-knappen i bunntekstregionen nederst i kolonnen du er interessert i å se en totalverdi for. Hvis det ikke finnes konfigurerte kolonner, vil **Vis totalverdi**-knappen være synlig for alle numeriske kolonner. Når minst én kolonne er konfigurert for totalverdier, vil **Vis totalverdi**-knappene bare være tilgjengelige ved peking eller fokus. Denne handlingen lagrer ganske enkelt innstillingene for å se en totalverdi i denne kolonnen for senere besøk på denne siden, og denne statusen indikeres av streken som vises i denne kolonnen i bunnteksten (eller det vises en totalverdi umiddelbart hvis datasettet er tilstrekkelig lite).

Hvis du gjør en feil og ikke lenger ønsker å se en totalverdi i en bestemt kolonne, høyreklikker du på kolonnen og velger **Skjul totalverdi** eller velger **Skjul totalverdi**-knappen i bunnteksten i denne kolonnen. Denne innstillingen vil også bli lagret for fremtidige besøk på siden. 

### <a name="calculating-totals"></a>Beregner totaler
Når du kommer til en side der bunnteksten er synlig og kolonnene allerede er konfigurert for totalverdier, kan det hende at totalverdiene ikke vises i bunnteksten. Atferden avhenger av størrelsen på datasettet på siden. Hvis datasettet er tilstrekkelig lite, vises totalverdiene automatisk sammen med antallet rader i datasettet. Hvis det finnes streker i bunnteksten under kolonnene du har konfigurert for totalverdier, er datasettet for stort til at systemet kan vise totalverdier umiddelbart, og en eksplisitt handling er nødvendig for å beregne totalverdiene. Hvis du vil gjøre dette, klikker du på **Beregn**-knappen i bunnteksten, eller høyreklikker på en kolonne du vil ha totalverdi for, og velger **Summer denne kolonnen**.  

Hvis beregningen tar for lang tid, kan du avbryte operasjonen ved å velge **Avbryt**-knappen. Noen ganger vil datasettet imidlertid være for stort til å beregne totalverdier (en grense som pålegges av organisasjonen), og du vil i stedet få et varsel om at dataene må filtreres mer.

Totalverdier oppdateres automatisk når du oppdaterer, sletter eller oppretter rader i datasettet.  

## <a name="grouping-data"></a>Gruppering av data
Bedriftsbrukere må ofte utføre ad hoc-analyse av data. Selv om dette kan utføres ved å eksportere data til Microsoft Excel og bruke pivottabeller, gjør **Gruppering**-funksjonaliteten i tabellnett det mulig for brukere å organisere dataene på interessante måter i Finance and Operations-apper. Ettersom denne funksjonen utvider **Totalverdier**-funksjonen, gjør **Gruppering** det også mulig å få meningsfulle innsikter i dataene takket være oppgivelse av subtotalverdier på gruppenivå.

Hvis du vil bruke denne funksjonen, høyreklikker du kolonnen du vil gruppere etter, og velger **Grupper etter denne kolonnen**. Denne handlingen sorterer dataene etter den valgte kolonnen, legger til en ny gruppe etter kolonne i begynnelsen av rutenettet og setter inn "topptekstrader" i begynnelsen av hver gruppe. Disse topptekstradene inneholder følgende informasjon om hver gruppe: 
-  Dataverdi for gruppen 
-  Kolonneetikett. Dette vil være spesielt nyttig når det er støtte for flere nivåer med gruppering.  
-  Antallet datarader i denne gruppen
-  Subtotalverdier for enhver kolonne som er konfigurert for å vise totalverdier

Med [Lagrede visninger](saved-views.md) aktivert kan denne grupperingen lagres ved å tilpasning som en del av en visning for rask tilgang neste gang du besøker siden.  

Hvis du velger **Grupper etter denne kolonnen** i en annen kolonne, vil den opprinnelige grupperingen bli erstattet, da bare grupperingsnivå støttes i versjon 10.0.9 / plattformoppdatering 33.

Hvis du vil angre gruppering i et rutenett, høyreklikker du på grupperingskolonnen og velger **Opphev gruppering**.  


## <a name="evaluating-math-expressions"></a>Evaluering av matematiske uttrykk
Som en produktivitetsforsterkning kan brukeren legge inn matematiske formler i numeriske celler i et rutenett, i stedet for å måtte utføre beregningen i en app utenfor systemet. Du kan for eksempel angi **=15\*4** og trykke på tab for å gå ut av feltet. Systemet evaluerer uttrykket og lagrer verdien "60" for feltet.

Hvis du vil at systemet skal gjenkjenne en verdi som et uttrykk, starter du verdien med et likhetstegn (**=**). Hvis du vil ha mer informasjon om de støttede operatorene og syntaksen, kan du se [Støttede matematiske symboler](http://redhivesoftware.github.io/math-expression-evaluator/#supported-maths-symbols).  
