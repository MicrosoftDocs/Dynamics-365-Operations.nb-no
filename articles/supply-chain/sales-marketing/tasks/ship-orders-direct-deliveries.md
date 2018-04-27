--- 
title: Sende ordrer som direkte leveringer
description: "Denne fremgangsmåten viser hvordan du oppretter en direktelevering for en salgsordre."
author: omulvad
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f674de4877dd2d6e6f1ff02f16a68cb4805d9864
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="ship-orders-as-direct-deliveries"></a>Sende ordrer som direkte leveringer

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en direktelevering for en salgsordre. Du bruker direktelevering når du vil levere varer til kunden direkte fra leverandøren, i stedet for å levere dem først til ditt eget lager. Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. For å fullføre den andre underordnede oppgaven "Opprette direkte leveringer fra arbeidsbenken" kontroller at varen du velger i salgsordren, har en standard leverandør angitt på hurtigfanen Kjøp i produktstandarden Frigitt.


## <a name="set-an-individual-order-for-direct-delivery"></a>Angi en enkelt ordre for direkte levering
1. Gå til Alle salgsordrer.
2. Klikk Ny.
3. Angi eller velg en verdi i Kundekonto-feltet.
    * Hvis du bruker USMF, kan du velge kontoen US-001.  
4. Klikk OK.
5. Angi eller velg en verdi i Varenummer-feltet.
    * Hvis du bruker USMF, kan du velge vare 'T0020'.  
6. Klikk Lagre.
7. Klikk Salgsordre i handlingsruten.
8. Velg Direktelevering.
    * Opprett levering-siden viser alle de åpne salgsordrelinjene som kopiert fra salgsordren. Du kan se gjennom ordredetaljene, og om nødvendig kan du endre detaljer som for eksempel innkjøpsantall og prisvilkår før du oppretter den direkte leveringen.  
9. Velg Ja i feltet Inkluder alt.
    * Hvis du vil generere en direkte levering for bare et delsett av salgsordrelinjene, velger du disse individuelt.  
    * Leverandørkonto-feltet kan eller kan ikke allerede være utfylt med et leverandørnummer. Hvis standardleverandøren er definert for produktet (på den tilknyttede varedekningen), vil denne leverandøren kopieres til linjen. Hvis ikke, må du angi en leverandør manuelt. I dette eksemplet velger vi en ny leverandør i neste trinn, selv om en allerede fylt ut.   
10. Angi eller velg en verdi i Leverandørkonto-feltet.
    * Hvis du bruker USMF, kan du velge kontoen 1001.  
11. Klikk OK.
    * Meldingen forteller deg at bestillingen er nå blitt opprettet.   
12. Vis seksjonen Linjedetaljer.
13. Velg kategorien Levering.
    * Feltet Direktelevering er nå satt til Ja.  
    * Status for direkte levering viser bestillingen som er opprettet.   
14. Klikk Generelt i handlingsruten.
15. Velg Relaterte ordrer.
16. Klikk for å følge koblingen i feltet Bestilling.
17. Vis seksjonen Linjedetaljer.
18. Klikk kategorien Adresse.
    * Legg merke til at leveringsadressen for denne bestillingslinjen er kundens leveringsadresse og ikke firmaets adresse.  
    * Hvis du endrer leveringsadressen på bestillingslinjen eller den opprinnelige salgsordrelinjen, oppdateres adressen på den tilsvarende ordrelinjen automatisk.  
19. Velg kategorien Levering.
    * Som salgsordrelinjen settes også den tilknyttede bestillingslinjetypen til Direktelevering.  
    * Leveringsdato og bekreftet leveringsdato for bestillingslinjen er satt til henholdsvis ønsket leveringsdato og bekreftet leveringsdato for den opprinnelige salgsordrelinjen.   
    * Hvis du oppdaterer noen av disse datoene på bestillingslinjen eller salgslinjen, oppdateres datoene i den tilhørende ordren automatisk.     
    * Bestillingen som er angitt for å levere varene direkte til kunden, er koblet til den opprinnelige salgsordren ved hjelp av en spesiell tilknytning. Denne tilknytningen bruker regelen om at følgeseddeloppdateringen av salgsordren ikke kan utføres fra selve ordren og må utføres ved hjelp av bestillingen. Kundefakturering må imidlertid utføres fra salgsordren.  
20. Klikk Kjøp i handlingsruten.
21. Klikk Bekreftelse.
22. Klikk OK.
23. Klikk Motta i handlingsruten.
24. Klikk Produktkvittering.
25. Skriv inn en verdi i feltet Produktkvittering.
26. Klikk OK.
27. Klikk Generelt i handlingsruten.
28. Velg Relaterte ordrer.
29. Merk den valgte raden i listen.
    * Når bestillingen er oppdatert som mottatt, eller med andre ord, når leverandøren har sendt varene til kundens adresse, oppdateres statusen for den opprinnelige salgsordren automatisk til Levert.  
    * Salgsordren kan nå faktureres.    
30. Klikk OK.
31. Lukk siden.
32. Klikk OK.

## <a name="create-direct-deliveries-from-the-workbench"></a>Opprette direkte leveringer fra arbeidsbenk
1. Lukk siden.
2. Lukk siden.
3. Gå til Alle salgsordrer.
4. Klikk Ny.
5. Angi eller velg en verdi i Kundekonto-feltet.
6. Klikk OK.
7. Angi eller velg en verdi i Varenummer-feltet.
8. Vis seksjonen Linjedetaljer.
9. Velg kategorien Levering.
    * I stedet for å opprette en direkte levering som en del av salgsordrebehandlingen som i forrige prosedyre, kan du velge å overføre denne oppgaven til en innkjøpsansvarlig. Hvis du vil ta med salgsordrelinjen i håndteringsprosessen for direkte levering, må du merke linjen for direkte levering.  
10. Velg Ja i feltet Direktelevering.
    *   Hvis varen er allerede definert for direkte levering som standard, vil feltet automatisk bli satt til Ja i ordrelinjeregistreringen. Du kan definere et element for direkte levering i standarden for det frigitte endelige produktet ved å angi alternativet Direktelevering til Ja og velge et standardlager for direkte levering.  
    * Fordi bestillingen ennå ikke er opprettet, settes statusen for direkte levering til Skal leveres direkte.   
11. Lukk siden.
12. Lukk siden.
13. Gå til Direktelevering.
    * Direktelevering-siden fungerer som en arbeidsbenk som gir innkjøpsagenten en oversikt over alle salgsordrelinjene som skal leveres direkte, og den gjør det mulig å opprette de respektive bestillingene. I tillegg kan de vise og åpne direkteleveringsordrer og de bekreftede bestillingene i kategoriene Bekreftelse og Levering.   
14. Klikk Opprett direkte levering.
15. Klikk kategorien Bekreftelse.
    * Etter at du har opprettet en direkte leveringsordre, flyttes den automatisk til kategorien Bekreftelse. Du kan velge å bekrefte bestillingen direkte fra denne siden. Når bestillingen er bekreftet, flyttes den automatisk til kategorien Levering, som kan du registrere mottaket fra.  


