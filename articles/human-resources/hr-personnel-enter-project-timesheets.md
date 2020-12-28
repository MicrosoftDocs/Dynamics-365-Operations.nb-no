---
title: Angi prosjekttimeregistreringer
description: Denne prosedyren lar deg opprette en timeregistrering ved hjelp av et tomt timeregistreringsskjema.
author: andreabichsel
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Human Resources
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10dbb43cec47a758d11362947f27932a4911911a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419916"
---
# <a name="enter-project-timesheets"></a>Angi prosjekttimeregistreringer



Denne prosedyren lar deg opprette en timeregistrering ved hjelp av et tomt timeregistreringsskjema. Den nye timeregistreringen kan baseres på informasjon fra en tidligere timeregistrering, eller fra prosjekt- og aktivitetstilordninger på **Mine favoritter**-siden. Som standard viser **Alle timeregistreringer**-listesiden alle timeregistreringene dine for den gjeldende perioden. Du kan bruke rullegardinlisten for **Vis**-feltet på **Mine timeregistreringer**-siden til å filtrere timeregistreringslisten etter tidsperiode eller prosjekt, eller til å vise timeregistreringer som ble opprettet på vegne av andre arbeidere. Demonstrasjonsdatafirmaet USSI brukes til å opprette denne prosedyren. 

1. I **navigasjonsruten** går du til **Moduler > Prosjektstyring og regnskap > Timeregistreringer > Mine timeregistreringer**.
2. Klikk **Ny** for å angi en ny timeregistrering.
    - Rullegardinlisten Ressurs viser arbeideren som er tilordnet til den gjeldende brukeren, som standard.  
    - Hvis brukeren er angitt som representant, viser dette navnene slik at en bruker kan angi en timeregistrering på deres vegne.  
3. Angi en dato i **Dato**-feltet. Hvis dette alternativet velges, opprettes nye timeregistreringslinjer ved hjelp av innstillingene for timeregistrering som ble konfigurert som favoritter.  
4. Klikk **OK**.
5. Klikk **Ny linje**.
6. Merk den valgte raden i listen. **Juridisk enhet**-feltet viser som standard den gjeldende juridiske enheten.   
7. Klikk rullegardinknappen i **Prosjekt**-feltet for å åpne oppslaget.
8. Finn og velg ønsket post i listen.
9. Klikk koblingen i den valgte raden i listen.
10. Klikk rullegardinknappen i feltet **Aktivitetsnummer** for å åpne oppslaget.
11. Finn og velg ønsket post i listen.
12. Klikk koblingen i den valgte raden i listen.
13. Klikk rullegardinknappen i **Kategori**-feltet for å åpne oppslaget.
14. Finn og velg ønsket post i listen.
15. Klikk koblingen i den valgte raden i listen.
16. Angi antall arbeidstimer for hver dag. Angi timene i desimalformat. Hvis du arbeidet to timer og femten minutter, angir du 2,25.   
17. Følgende alternativer er tilgjengelige i **Linjedetaljer**:
    - Legg til informasjon om avgifter og finansdimensjoner i fanen **Generelt** og **Finansdimensjoner**.
    - Legg til kommentarer om timeregistreringslinjen i fanen **Kommentar**.
20. I **handlingsruten** klikker du **Arbeidsflyt** for å åpne dialogboksen for rullegardinlisten.
21. Klikk **Send**.
22. Klikk **Send**.

