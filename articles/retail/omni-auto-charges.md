<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="omni-auto-charges.md" target-language="nb-NO">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>omni-auto-charges.2f6e37.47829a6fcae37e03510929dc46b942455016df0b.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>47829a6fcae37e03510929dc46b942455016df0b</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>ffc37f7c2a63bada3055f37856a30424040bc9a3</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/16/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\omni-auto-charges.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Omni-channel advanced auto charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Avanserte automatiske gebyrer for omnikanal</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes capabilities for managing additional order charges for Retail channel orders using advanced auto charges features.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette emnet beskriver funksjoner for å håndtere flere ordregebyrer for handelskanalordrer ved hjelp av funksjoner for avanserte automatiske gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Omni-channel advanced auto charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Avanserte automatiske gebyrer for omnikanal</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides information on configuration and deployment of the advanced auto-charges feature which are available in Dynamics 365 for Retail version 10.0.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette emnet gir informasjon om konfigurasjon og distribusjon av funksjonen for avanserte automatiske gebyrer som er tilgjengelig i Dynamics 365 for Retail versjon 10.0.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When the advanced auto-charges features are enabled, orders created in any supported Retail channel (point of sale (POS), call center, and online), can take advantage of the <bpt id="p1">[</bpt>auto-charges<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> configurations defined in the ERP application for both header and line-level related charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når funksjonene for avanserte automatiske gebyrer er aktivert, kan ordrer som opprettes i en støttet detaljhandelskanal (salgssted, telefonsenter og online), dra nytte av konfigurasjonene for <bpt id="p1">[</bpt>automatisk gebyrer<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> som er definert i ERP-programmet for både hode- og linjenivårelaterte gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In releases prior to Dynamics 365 for Retail version 10.0, <bpt id="p1">[</bpt>auto-charge<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> configurations are only accessible by orders created in e-Commerce and call center channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I versjoner før Dynamics 365 for Retail versjon 10.0 er konfigurasjoner for <bpt id="p1">[</bpt>automatiske gebyrer<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> bare tilgjengelige for ordrer som er opprettet i e-handels- og telefonsenterkanaler.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In versions 10.0 and later, POS-created orders can leverage the auto-charges configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I versjon 10.0 og senere kan ordrer opprettet på salgsstedet dra nytte av konfigurasjonene for automatiske gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>That way, additional miscellaneous charges can systematically be added to sales transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På denne måten kan flere tillegg systematisk legges til salgstransaksjonene.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>When using releases prior to version 10.0, a POS user is prompted to manually enter a shipping fee during the creation of a "ship all" or "ship selected" POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ved bruk av versjoner før versjon 10.0 blir brukeren for salgsstedet bedt om å angi et fraktgebyr manuelt under opprettingen av en salgsstedstransaksjon av typen Send alle eller Valgt for forsendelse.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>While the miscellaneous charges capabilities of the application are utilized in respect to how the charges are written to the order, no systematic calculation is provided – the calculation relies on the user's input to determine the value of the charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">Ettersom funksjonene for tilleggene i programmet brukes i forhold til hvordan gebyrene skrives til ordren, tilbys det ingen systematisk beregning. Beregningen er avhengig av brukerens inndata for å bestemme verdien på tillegget.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The charges can only be added as a single "shipping" related charges code and cannot easily be edited or changed in the POS after they are created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gebyrene kan bare legges til som en enkelt forsendelsesrelatert gebyrkode og kan ikke redigeres eller endres enkelt på salgsstedet etter at de er opprettet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The use of manual prompts to add shipping charges is still available in versions 10.0 and later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bruken av manuelle ledetekster for å legge til forsendelseskostnader er fremdeles tilgjengelig i versjon 10.0 og nyere.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>If an organization does not enable the <bpt id="p1">**</bpt>Advanced Auto-charges<ept id="p1">**</ept> parameter, the POS prompts for manual entry of charges will remain the same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis en organisasjon ikke aktiverer parameteren <bpt id="p1">**</bpt>Avanserte automatiske gebyrer<ept id="p1">**</ept>, blir salgsstedsforespørslene om manuell registrering av gebyrer de samme.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>With the advanced auto-charges feature, POS users can have systematic calculations for any defined miscellaneous charges based on auto-charges setup tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Med funksjonen for avanserte automatiske gebyrer kan brukerne for salgsstedet ha systematiske beregninger for alle definerte tillegg basert på tabellene med oppsett for automatiske gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In addition, users will have the ability to add or edit an unlimited amount of additional charges and fees to any POS sales transaction at the header or line-level (for a cash and carry or customer order).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I tillegg vil brukere ha muligheten for å legge til eller redigere et ubegrenset antall tilleggskostnader og gebyrer i en salgstransaksjon for salgsstedet på hode- eller linjenivået (for hentesalg eller kundeordre).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Enabling advanced auto-charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aktivere avanserte automatiske gebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>On the <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Headquarters setup <ph id="ph2">\&gt;</ph> Parameters <ph id="ph3">\&gt;</ph> Retail parameters<ept id="p1">**</ept> page, go to the <bpt id="p2">**</bpt>Customer orders<ept id="p2">**</ept> tab. On the <bpt id="p3">**</bpt>Charges<ept id="p3">**</ept> FastTab, set <bpt id="p4">**</bpt>Use advanced auto-charges<ept id="p4">**</ept> to <bpt id="p5">**</bpt>Yes<ept id="p5">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">På siden <bpt id="p1">**</bpt>Detaljhandel <ph id="ph1">\&gt;</ph> Hovedkvarteroppsett <ph id="ph2">\&gt;</ph> Parametere <ph id="ph3">\&gt;</ph> Detaljhandelsparametere<ept id="p1">**</ept> går du til kategorien <bpt id="p2">**</bpt>Kundeordrer<ept id="p2">**</ept>. I hurtigfanen <bpt id="p3">**</bpt>Gebyrer<ept id="p3">**</ept> setter du <bpt id="p4">**</bpt>Bruk avanserte automatiske gebyrer<ept id="p4">**</ept> til <bpt id="p5">**</bpt>Ja<ept id="p5">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Advanced Auto-Charges Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Parameter for avanserte automatiske gebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>When advanced auto-charges are enabled, users are no longer prompted to manually enter a shipping charge at the POS terminal when creating a ship-all or ship-selected customer order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når avanserte automatiske gebyrer er aktivert, blir brukere ikke lenger bedt om å angi en forsendelseskostnad manuelt på salgsstedsterminalen når de oppretter en kundeordre av typen Send alle eller Valgt for forsendelse.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>POS order charges are systematically calculated and added to the POS transaction (if a corresponding auto-charges table that matches the criterion of the order being created are found).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ordregebyrer for salgssted beregnes systematisk og legges til salgsstedstransaksjonen (hvis det finnes en tilsvarende tabell for automatiske gebyrer som samsvarer med kriteriet for ordren som opprettes).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Users can also add or maintain header or line-level charges manually through newly added POS operations that can be added to the POS screen layouts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brukere kan også legge til eller vedlikeholde hode- eller linjenivågebyrer manuelt via salgsstedsoperasjoner som nylig er lagt til, som kan legges til skjermoppsettene for salgsstedet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>When advanced auto-charges are enabled, the existing <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> for <bpt id="p2">**</bpt>Shipping charges code<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Refund shipping charges<ept id="p3">**</ept> are no longer utilized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når avanserte automatiske gebyrer er aktivert, brukes ikke lenger eksisterende <bpt id="p1">**</bpt>Detaljhandelsparametere<ept id="p1">**</ept> for <bpt id="p2">**</bpt>Kode for forsendelseskostnader<ept id="p2">**</ept> og <bpt id="p3">**</bpt>Refundering av forsendelseskostnader<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>These parameters are only applicable if the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is set to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Disse parameterne gjelder bare hvis parameteren <bpt id="p1">**</bpt>Bruk avanserte automatiske gebyrer<ept id="p1">**</ept> er satt til <bpt id="p2">**</bpt>Nei<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Before you enable this feature, ensure that you have tested and trained your employees, as this will change the business process flow of how shipping or other charges are calculated and added to POS sales orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Før du aktiverer denne funksjonen, må du passe på at du har testet og lært opp dine ansatte siden dette vil endre forretningsprosessflyten for hvordan forsendelseskostnader eller andre gebyrer beregnes og legges til salgsordrer for salgsstedet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Make sure that you understand the impact of the process flow to the creation of transactions from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pass på at du forstår virkningen prosessflyten har på opprettingen av transaksjoner fra salgssted.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For call center and e-Commerce orders, the impact of enabling advanced auto-charges is minimal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">For telefonsenter- og e-handelsorder er virkningen av å aktivere avanserte automatiske gebyrer minimal.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Call center and e-Commerce applications will continue to have the same behavior they have had historically related to the auto-charges tables to calculate additional order fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Telefonsenter- og e-handelsprogrammer vil fortsatt ha samme virkemåte som de har hatt tidligere knyttet til tabellene for automatiske gebyrer for å beregne ekstra ordregebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Call center channel users will continue to have the ability to manually edit any system calculated auto-charges at the header or line level, or manually add additional miscellaneous charges at the header or line level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brukere av telefonsenterkanaler vil fortsatt ha muligheten til å redigere manuelt systemberegnede automatiske gebyrer på hode- eller linjenivå, eller legge til flere tillegg på hode- eller linjenivå manuelt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Additional POS operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Flere salgsstedsoperasjoner</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>For advanced auto-charges to work properly in your POS application environment, new POS operations have been added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">For at avanserte automatiske gebyrer skal fungere riktig i ditt salgsstedsprogrammiljø, er det lagt til nye salgsstedsoperasjoner.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>These operations must be added to your <bpt id="p1">[</bpt>POS screen layouts<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> and deployed to the POS devices as you deploy advanced auto-charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Disse operasjonene må legges til i <bpt id="p1">[</bpt>skjermoppsettene for salgssted<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> og distribueres til salgsstedsenhetene når du distribuerer avanserte automatiske gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>If these operations are not added, users will not be able to manage or maintain miscellaneous charges on the POS transactions and will have no way of adjusting or changing the charges values that are systematically calculated based on auto-charges configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis disse operasjonene ikke legges til, kan ikke brukere behandle eller vedlikeholde tillegg i salgsstedstransaksjonene, og vil ikke ha noen måte å justere eller endre gebyrverdiene på som beregnes systematisk basert på konfigurasjoner for automatiske gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>At minimum, it is suggested that you deploy the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation to your POS layout.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Som minimum anbefales det at du distribuerer <bpt id="p1">**</bpt>Behandle tillegg<ept id="p1">**</ept>-operasjonen til salgsstedsoppsettet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The new operations are as follows.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">De nye operasjonene er følgende:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">**</bpt>142 - Manage charges<ept id="p1">**</ept> – Use this operation to allow POS users to view and edit miscellaneous charges for the POS transaction that were either added manually or systematically through auto-charges calculations.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>142 - Administrer tillegg<ept id="p1">**</ept> – Bruk denne operasjonen for å la brukere på salgsstedet vise og redigere tillegg for salgsstedstransaksjonen som ble lagt til manuelt eller systematisk gjennom automatiske gebyrberegninger.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>141 - Add header charges<ept id="p1">**</ept> – Use this operation to give the user the ability to manually add a header-level miscellaneous charge to any POS sales transaction (and select the charges code to be used).</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>141 - Legg til hodegebyrer<ept id="p1">**</ept> – Bruk denne operasjonen for å gi brukeren mulighet til å manuelt legge til et tillegg på hodenivå i salgstransaksjoner på salgsstedet (og velge gebyrkoden som skal brukes).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>140 - Add line charges<ept id="p1">**</ept> – Use this operation to give the user the ability to manually add a line level miscellaneous charge to any POS sales transaction line (and select the charges code to be used).</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>140 - Legg til linjegebyrer<ept id="p1">**</ept> – Bruk denne operasjonen for å gi brukeren mulighet til å manuelt legge til et tillegg på linjenivå i salgstransaksjonslinjer på salgsstedet (og velge gebyrkoden som skal brukes).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>143 - Recalculate charges<ept id="p1">**</ept> – Use this operation to perform a full re-calculation of the charges for the sales transaction.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>143 - Beregn gebyrer på nytt<ept id="p1">**</ept> – Bruk denne operasjonen for å utføre en fullstendig ny beregning av gebyrene salgstransaksjonen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Any previously user-overwritten auto-charges will be recalculated based on the current cart configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tidligere automatiske gebyrer som er overskrevet av bruker, beregnes på nytt basert på den gjeldende handlekurvkonfigurasjonen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>As with all POS operations, security configurations can be made to require manager approval in order to execute the operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Som med alle salgsstedsoperasjoner kan sikkerhet konfigureres slik at det kreves godkjenning fra leder før operasjonen kan utføres.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>It is important to note that the above listed POS operations can also be added to the POS layout even if the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Det er viktig å være klar over at salgsstedsoperasjonene også kan legges til salgsstedoppsettet, selv om <bpt id="p1">**</bpt>Bruk avanserte automatiske gebyrer<ept id="p1">**</ept>-parameteren er deaktivert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In this scenario, organizations will still get added benefits of being able to view manually added charges and edit them using the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I slike scenarioer vil organisasjoner likevel få fordeler med å kunne vise manuelt tillagte gebyrer og redigere dem ved hjelp av <bpt id="p1">**</bpt>Behandle gebyrer<ept id="p1">**</ept>-operasjonen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Users may also use the <bpt id="p1">**</bpt>Add header charges<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Add line charges<ept id="p2">**</ept> operations for POS transactions even when <bpt id="p3">**</bpt>Use advanced auto-charges<ept id="p3">**</ept> parameter is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brukere kan også bruke operasjonene <bpt id="p1">**</bpt>Legg til hodegebyrer<ept id="p1">**</ept> og <bpt id="p2">**</bpt>Legg til linjegebyrer<ept id="p2">**</ept> for salgsstedstransaksjoner, selv når <bpt id="p3">**</bpt>Bruk avanserte automatiske gebyrer<ept id="p3">**</ept>-parameteren er deaktivert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The <bpt id="p1">**</bpt>Recalculate charges<ept id="p1">**</ept> operation has less functionality if used when <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Beregn gebyrer på nytt<ept id="p1">**</ept>-operasjonen har mindre funksjonalitet hvis den brukes når <bpt id="p2">**</bpt>Bruk avanserte automatiske gebyrer<ept id="p2">**</ept> er deaktivert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In this sceanrio, nothing would be recalculated and any charges manually added to the transaction would just reset to $0.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ingenting vil bli beregnet på nytt i dette scenarioet, og gebyrer som legges til manuelt i transaksjonen, vil bare tilbakestilles til USD 0,00.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Use case examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brukseksempler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>In this section, sample use cases are presented to help you understand the configuration and usage of auto-charges and miscellaneous charges within the context of Retail channel orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I denne delen vises brukseksempler for å hjelpe deg med å forstå konfigurasjon og bruk av automatiske gebyrer og tillegg i forbindelse med handelskanalordrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>These examples illustrate the behavior of the application when the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter has been enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Disse eksemplene viser virkemåten til programmet når parameteren <bpt id="p1">**</bpt>Bruk avanserte automatiske gebyrer<ept id="p1">**</ept> er aktivert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Auto-charges header charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempel på automatiske gebyrer for hodetillegg</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bruksscenario</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>A retailer wants to automatically add charges for freight when transactions are created in any Retail channel that require a shipment of products to the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En forhandler ønsker å legge til tillegg for frakt automatisk når transaksjoner opprettes i en detaljhandelskanal som krever forsendelse av varer til kunden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The retailer offers 2 methods of delivery: Ground and Air.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Forhandleren tilbyr 2 leveringsmåter: landtransport og fly.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>If a customer chooses Ground delivery and the order value is less than $100, the retailer wants to charge the customer a freight charge of $10.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis en kunde velger landtransportlevering og ordreverdien er mindre enn NOK 1000, vil forhandleren belaste kunden med et fraktgebyr på NOK 100.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>If the order is over $100 in value and the customer chooses ground shipping, the customer will not be charged any additional freight fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis ordren er over NOK 1000 og kunden velger forsendelse på land, vil kunden ikke bli belastet med ekstra fraktgebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If the customer chooses the Air method of delivery for all orders, regardless of their total value, will be charged a freight fee of $20.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis kunden velger leveringsmåten for fly for alle ordrer, uavhengig av deres totale verdi, tilfaller det et fraktgebyr på NOK 200.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Oppsett og konfigurasjon</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This scenario requires the configuration of two auto-charges tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette scenariet krever konfigurasjon av to tabeller for automatiske gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Go to <bpt id="p1">**</bpt>Accounts receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Auto charges<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gå til <bpt id="p1">**</bpt>Kunder <ph id="ph1">\&gt;</ph> Oppsett for tillegg <ph id="ph2">\&gt;</ph> Automatiske gebyrer<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Configure two different header-level auto charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konfigurer to ulike automatiske gebyrer på hodenivå.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Configure one for the "Ground mode" of delivery and one for the "Air mode" of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konfigurer ett for «over land»-leveringsmåten og ett for «flyfrakt»-leveringsmåten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>For this scenario, configure them to be used for "All customers".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I dette scenariet konfigurerer du dem for bruk for «Alle kunder».</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>For the ground delivery charges, in the lines section of the <bpt id="p1">**</bpt>Auto-charges<ept id="p1">**</ept> page, define a charge that will be applied for orders between $.01 and $100 as $10.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I linjedelen på siden <bpt id="p1">**</bpt>Automatiske gebyrer<ept id="p1">**</ept> for gebyrene for levering på land definerer du et gebyr som skal brukes for ordrer mellom NOK 0,10 og 1000, som NOK 100,00.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Create another charges line to indicate orders over $100.01 will have no charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Opprett en ny gebyrlinje for å angi at ordrer over NOK 1000,10 ikke har gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Auto charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempel på automatiske gebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>For the air delivery charges, in the lines section of the auto-charges form, define a charge of $20.00 that will be applied to all orders (between a value of $.01 to $9,999,999).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I linjedelen i skjemaet for automatiske gebyrer for gebyrene for levering med fly definerer du et gebyr på NOK 200,00 som skal brukes for alle ordrer (mellom en verdi på NOK 0,10 og NOK 99 999 990).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Send the changes to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Send endringene til detaljhandelsserveren/kanaldatabasen slik at salgsstedet kan bruke dem ved å kjøre jobben <bpt id="p1">**</bpt>1040 distribusjonsplan<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Sales processing for this scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Salgsbehandling for dette scenariet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>After the configuration steps above are complete and the changes have been applied to the channel database, any customer order or sales transaction created in the POS, call center, or e-Commerce channels that have the ground or air delivery methods set at the header level will utilize these charges and automatically apply them to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når konfigurasjonstrinnene ovenfor er fullført, og endringene er implementert i kanaldatabasen, vil kundeordrer eller salgstransaksjoner som er opprettet på salgsstedet, telefonsenteret eller e-handelskanalene som har angitt leveringsmåten land eller fly på hodenivå, bruke disse gebyrene og automatiske bruke dem på salget.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>At this time the charges will apply to all sales transactions created within the legal entity that utilize these delivery modes, as there is no functionality to designate that an auto-charge configuration will only apply to a specific selling channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På dette tidspunktet vil gebyrene gjelde for alle salgstransaksjoner som opprettes i den juridiske enheten som bruker disse leveringsmåtene, siden det ikke finnes noen funksjon som kan angi at en konfigurasjon for automatiske gebyrer bare skal gjelde for en bestemt salgskanal.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For POS and e-Commerce scenarios, because there is no clearly defined "header" on these orders, header-level charges will only apply if all sales lines on the transaction are set to ship with the exact same mode of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">For salgssteds- og e-handelsscenarier, fordi det er ikke noe klart definert «hode» i disse ordrene, gjelder bare hodenivågebyrer hvis alle salgslinjer i transaksjonen er satt til forsendelse med nøyaktig samme leveringsmåte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>If there are "mixed-modes" of fulfillment on the transactions created by POS or e-Commerce, only line-level auto-charges will be considered and applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis det er «blandede måter» for fullføring i transaksjonene som er opprettet på salgsstedet eller i e-handel, vurderes og brukes bare automatiske gebyrer på linjenivå.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>In call center scenarios, the user has control over the setting of the delivery mode at the order header, therefore header-level charges will apply for these orders even if some of the sales lines have been configured to use a different mode of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">I telefonsenterscenarier har brukeren kontroll over innstillingen for leveringsmåte i ordrehodet. Derfor brukes gebyrer på hodenivå for disse ordrene selv om noen av salgslinjene er konfigurert for å bruke en annen leveringsmåte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Header-level charges for call center orders will always be based on the mode of delivery that is defined at the order header level of the sales order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gebyrer på hodenivå for telefonsenterordrer baseres alltid på leveringsmåten som er definert i ordrehodenivået for salgsordren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Auto-charges line charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempel på automatiske gebyrer for linjetillegg</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bruksscenario</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>A retailer wants to add an additional charge to the customer for setup fees when the customer purchases a particular model of computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En forhandler ønsker å legge til en tilleggsavgift for kunden for oppsettsgebyrer når kunden kjøper en bestemt modell av en datamaskin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>This computer requires additional non-optional setup actions that the retailer will perform for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Denne datamaskinen krever ekstra konfigurasjonshandlinger som ikke er valgfrie, og som forhandleren utfører for kunden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The retailer has informed customers that there will be an additional fee for this setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Forhandleren har informert kunder om at det er tilleggsgebyr for dette oppsettet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The retailer prefers to manage the charges related to this fee separately from the product sales price for financial reporting purposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Forhandleren foretrekker å håndtere tilleggene som er knyttet til dette gebyret, separat fra produktsalgsprisen for regnskapsrapporteringsformål.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>A setup fee of $19.99 will be charged to the customer when this specific computer is purchased in any retail channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Et oppsettsgebyr på NOK 199,90 skal belastes kunden når denne bestemte datamaskinen kjøpes i en detaljhandelskanal.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Oppsett og konfigurasjon</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This scenario requires the configuration of one line-level auto charges table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette scenariet krever konfigurasjon av én tabell for automatiske gebyrer på linjenivå.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Go to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Auto charges<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gå til <bpt id="p1">**</bpt>Kunder <ph id="ph1">\&gt;</ph> Oppsett for tillegg <ph id="ph2">\&gt;</ph> Automatiske gebyrer<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Set the <bpt id="p1">**</bpt>Level<ept id="p1">**</ept> drop-down menu to <bpt id="p2">**</bpt>Line<ept id="p2">**</ept>, and create a new auto-charges record for all customers and for the specific product or product group where the setup fees will be charged.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sett <bpt id="p1">**</bpt>Nivå<ept id="p1">**</ept>-rullegardinmenyen til <bpt id="p2">**</bpt>Linje<ept id="p2">**</ept>, og opprett en ny post for automatiske gebyrer for alle kunder og for det bestemte produktet eller produktgruppen der konfigurasjonsgebyret belastes.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Auto charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempel på automatiske gebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Send gebyrene til detaljhandelsserveren/kanaldatabasen slik at salgsstedet kan bruke dem ved å kjøre jobben <bpt id="p1">**</bpt>1040 distribusjonsplan<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Sales processing for this scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Salgsbehandling for dette scenariet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>After the configurations steps above are complete and the changes have been applied to the channel database, any customer order or sales transaction created in the POS, call center, or e-Commerce channels that have this item on the order will trigger a line-level charge to be systematically added to the order total.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når konfigurasjonstrinnene ovenfor er fullført, og endringene er implementert i kanaldatabasen, vil kundeordrer eller salgstransaksjoner som er opprettet på salgsstedet, telefonsenteret eller e-handelskanalene som har denne varen i ordren, utløse et linjenivågebyr som legges til ordretotalen systematisk.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>At this time the charges will apply to any sales line that matches the configuration of the line-level auto charges within the legal entity, as there is no functionality to configure a line-level auto-charge to apply only to a specific selling channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På dette tidspunktet vil gebyrene gjelde for alle salgslinjer som samsvarer med konfigurasjonen for automatiske gebyrer på linjenivå i den juridiske enheten, siden det ikke finnes noen funksjon for å konfigurere et automatisk gebyr på linjenivå som bare skal gjelde for en bestemt salgskanal.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Manual header charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempel på manuelle hodetillegg</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Use case scenario description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bruksscenariobeskrivelse</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>A retailer is making an exception to typical processes by offering to provide a special home delivery of products to a customers who order products in the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En forhandler gjør et unntak fra vanlige prosesser ved å tilby å en spesiell hjemmelevering av varer til kunder som bestiller varer i butikken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The retailer and the customer have agreed that the customer will pay an additional $25 handling fee for this service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Forhandleren og kunden har blitt enige om at kunden skal betale et ekstra administrasjonsgebyr på NOK 250 for denne tjenesten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The order-taker needs to add this additional fee to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ordremottakeren må legge til dette tilleggsgebyret i transaksjonen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Because the fee is a blanket fee and not related to any single product on the order, a header charge will be utilized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fordi gebyret er generelt og ikke knyttet til et enkelt produkt i ordren, benyttes et hodetillegg.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Oppsett og konfigurasjon</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Ensure the charges code that will be used in this scenario has been properly configured by going to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Charges<ept id="p1">**</ept> to define an appropriate charges code for the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kontroller at tilleggskoden som skal brukes i dette scenariet, er riktig konfigurert ved å gå til <bpt id="p1">**</bpt>Kunder <ph id="ph1">\&gt;</ph> Oppsett for tillegg <ph id="ph2">\&gt;</ph> Tillegg<ept id="p1">**</ept> for å definere en passende tilleggskode for scenariet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempel på gebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>If the charge should be considered a "shipping" related charge for the purpose of shipping related discounts or promotions, set <bpt id="p1">**</bpt>Shipping charge<ept id="p1">**</ept> on the charges code to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">Hvis tillegget skal betraktes som et forsendelsesrelatert tillegg for forsendelsesrelaterte rabatter og tilbud, setter du <bpt id="p1">**</bpt>Forsendelsesgebyr<ept id="p1">**</ept> for tilleggskoden til <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>If this charge is also allowed to be systematically refunded during the processing of a return transaction in the POS application, set <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis dette gebyret også kan refunderes systematisk under behandlingen av en returtransaksjon i salgsstedprogrammet, setter du <bpt id="p1">**</bpt>Refunderbar<ept id="p1">**</ept> til <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>The <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag is only applicable when the <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> parameter is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Refunderbar<ept id="p1">**</ept>-flagget er bare tilgjengelig når <bpt id="p2">**</bpt>Bruk avanserte automatiske gebyrer<ept id="p2">**</ept>-parameteren er satt til <bpt id="p3">**</bpt>Ja<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Send gebyrene til detaljhandelsserveren/kanaldatabasen slik at salgsstedet kan bruke dem ved å kjøre jobben <bpt id="p1">**</bpt>1040 distribusjonsplan<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>The <bpt id="p1">**</bpt>Add header charge<ept id="p1">**</ept> operation must be configured in your <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a button that is accessible to the user from POS can call this operation (operation 141).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Legg til hodegebyrer<ept id="p1">**</ept>-operasjonen må konfigureres i <bpt id="p2">[</bpt>skjermoppsettet for salgssted<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> slik at en knapp som er tilgjengelig for brukeren fra salgsstedet, kan kalle denne operasjonen (operasjon 141).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The screen layout changes must be distributed to the retail channel as well through the distribution schedule function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Endringene i skjermoppsettet må distribueres til detaljhandelsekanalen og via funksjonen for distribusjonsplan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Sales processing of manual header charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Salgsbehandling av manuelle hodegebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>To execute the scenario in the POS application, the POS user will create the sales transaction as usual, adding the products and any other configurations to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis scenariet skal utføres i salgsstedsprogrammet, oppretter salgsstedsbrukeren salgstransaksjonen på vanlig måte, og legger til produktene og andre konfigurasjoner i salget.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Prior to collecting payment, the user should execute the <bpt id="p1">**</bpt>Add header charge<ept id="p1">**</ept> operation, which will prompt the user to select a charges code and enter the charges value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Før brukeren tar betaling, må brukeren utføre <bpt id="p1">**</bpt>Legg til hodetillegg<ept id="p1">**</ept>-operasjonen, som vil be brukeren om å velge en tilleggskode og angi tilleggsverdien.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Once the user completes the process, the charge will be added to the sales order as a header-level charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når brukeren fullfører prosessen, vil tillegget legges til salgsordren som et hodenivåtillegg.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>This process can be applied in the call center by using the existing <bpt id="p1">**</bpt>Charges<ept id="p1">**</ept> feature found on the <bpt id="p2">**</bpt>Sell<ept id="p2">**</ept> tab on the toolbar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Denne prosessen kan brukes i telefonsenteret ved hjelp av den eksisterende <bpt id="p1">**</bpt>Tillegg<ept id="p1">**</ept>-funksjonen som finnes i <bpt id="p2">**</bpt>Selg<ept id="p2">**</ept>-kategorien på verktøylinjen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Maintain charges<ept id="p1">**</ept> page, the user can add a new charges line to the order header.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På siden <bpt id="p1">**</bpt>Vedlikehold tillegg<ept id="p1">**</ept> kan brukeren legge til en ny tilleggslinje i ordrehodet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Manual line charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksempel på manuelle linjetillegg</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bruksscenario</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>A customer has requested that 2 of the 5 items on their sales order be gift-wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">En kunde har bedt om at 2 av 5 varer i salgsordren skal pakkes som gave.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>The retailer offers this optional service for a fee of $2.00 per item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Forhandleren tilbyr denne tilleggstjenesten mot et gebyr på NOK 20 per vare.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The order-taker will need to add these fees to the specific items that need to be gift-wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ordremottakeren må legge til disse gebyrene for de bestemte varene som skal pakkes som gave.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Oppsett og konfigurasjon</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Ensure the charges code that will be used in this scenario has been properly configured by going to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Charges<ept id="p1">**</ept> to define an appropriate charges code for the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kontroller at tilleggskoden som skal brukes i dette scenariet, er riktig konfigurert ved å gå til <bpt id="p1">**</bpt>Kunder <ph id="ph1">\&gt;</ph> Oppsett for tillegg <ph id="ph2">\&gt;</ph> Tillegg<ept id="p1">**</ept> for å definere en passende tilleggskode for scenariet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>If the charge should be considered a "shipping" related charge for the purpose of shipping related discounts or promotions, set the <bpt id="p1">**</bpt>Shipping charge<ept id="p1">**</ept> on the charges code to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis tillegget skal betraktes som et forsendelsesrelatert tillegg for forsendelsesrelaterte rabatter og tilbud, setter du <bpt id="p1">**</bpt>Forsendelsesgebyr<ept id="p1">**</ept> for tilleggskoden til <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>If the charge is also allowed to be systematically refunded during the processing of a return transaction in the POS application, set <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis gebyret også kan refunderes systematisk under behandlingen av en returtransaksjon i salgsstedprogrammet, setter du <bpt id="p1">**</bpt>Refunderbar<ept id="p1">**</ept> til <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag is only applicable when the <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> parameter is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Refunderbar<ept id="p1">**</ept>-flagget er bare tilgjengelig når <bpt id="p2">**</bpt>Bruk avanserte automatiske gebyrer<ept id="p2">**</ept>-parameteren er satt til <bpt id="p3">**</bpt>Ja<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Send gebyrene til detaljhandelsserveren/kanaldatabasen slik at salgsstedet kan bruke dem ved å kjøre jobben <bpt id="p1">**</bpt>1040 distribusjonsplan<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>The <bpt id="p1">**</bpt>Add line charge<ept id="p1">**</ept> operation must be configured in your <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a button that is accessible to the user from POS can call this operation (operation 140).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Legg til linjegebyrer<ept id="p1">**</ept>-operasjonen må konfigureres i <bpt id="p2">[</bpt>skjermoppsettet for salgssted<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> slik at en knapp som er tilgjengelig for brukeren fra salgsstedet, kan kalle denne operasjonen (operasjon 140).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>The screen layout changes must be distributed to the retail channel as well through the distribution schedule function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Endringene i skjermoppsettet må distribueres til detaljhandelsekanalen og via funksjonen for distribusjonsplan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Sales processing of the manual line charge</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Salgsbehandling av manuelle linjegebyrer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>To execute the scenario in the POS application, the POS user will create the sales transaction as usual, adding the products and any other configurations to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis scenariet skal utføres i salgsstedsprogrammet, oppretter salgsstedsbrukeren salgstransaksjonen på vanlig måte, og legger til produktene og andre konfigurasjoner i salget.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Prior to collecting payment, the user should select the specific line where the charge will apply from the POS item list display and execute the <bpt id="p1">**</bpt>Add line charge<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Før brukeren tar betaling, bør brukeren velge den bestemte linjen der gebyret skal gjelde, fra visningen for salgsstedsvareliste og utføre <bpt id="p1">**</bpt>Legg til linjegebyrer<ept id="p1">**</ept>-operasjonen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>The user will be prompted to select a charges code and enter the charges value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brukeren blir bedt om å velge en tilleggskode og angi verdien for tillegget.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Once the user completes the process, the charge will be linked to the line and added to the order total as a line level charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når brukeren fullfører prosessen, vil tillegget kobles til linjen og legges til ordretotalen som et linjenivåtillegg.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The user can repeat the process to add additional line charges to other items lines on the transaction if needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brukeren kan gjenta prosessen for å legge til flere linjegebyrer i andre varelinjer for transaksjonen hvis nødvendig.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The same process can be applied in the call center by using the "maintain charges" feature found under the <bpt id="p1">**</bpt>Financials<ept id="p1">**</ept> drop-down menu in the <bpt id="p2">**</bpt>Sales order lines<ept id="p2">**</ept> section on the <bpt id="p3">**</bpt>Sales order<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Den samme fremgangsmåten kan brukes i telefonsenteret ved hjelp av funksjonen Vedlikehold tillegg under <bpt id="p1">**</bpt>Finans<ept id="p1">**</ept>-rullegardinmenyen i <bpt id="p2">**</bpt>Salgsordrelinjer<ept id="p2">**</ept>-delen på <bpt id="p3">**</bpt>Salgsordre<ept id="p3">**</ept>-siden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>This will open the <bpt id="p1">**</bpt>Maintain charges<ept id="p1">**</ept> page where the user can add a new line specific charge to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette åpner <bpt id="p1">**</bpt>Vedlikehold tillegg<ept id="p1">**</ept>-siden der brukeren kan legge til en nytt linjebestemt tillegg for transaksjonen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Additional features</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tilleggsfunksjoner</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Editing charges on a POS sales transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Redigere tillegg i en salgstransaksjon for salgssted</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>The <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation (142) should be added to the <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a user can view and edit or override any system-calculated or manually-created header or line-level charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Behandle tillegg<ept id="p1">**</ept>-operasjonen (142) skal legges til <bpt id="p2">[</bpt>skjermoppsettet for salgssted<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> slik at en bruker kan vise og redigere eller overstyre systemberegnede eller manuelt opprettede hode- eller linjenivåtillegg.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>If the operation is not added, users will not be able to adjust the value of the charges on the POS transaction, nor will they be able to view the details of the charges such as the type of charges code tied to the charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis operasjonen ikke legges til, vil ikke brukere kunne justere verdien på gebyrene i salgsstedstransaksjonen. De vil heller ikke kunne vise detaljene om tilleggene, for eksempel typen tilleggskode som er knyttet til tillegget.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>On the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> page in POS, the user can view both header and line-level charges details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">På <bpt id="p1">**</bpt>Behandle tillegg<ept id="p1">**</ept>-siden i POS kan brukeren vise både hode- og linjenivåtilleggsdetaljer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The user can use the <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> function available on this page to make changes to the amount charged to a specific charges line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brukeren kan bruke funksjonen <bpt id="p1">**</bpt>Rediger<ept id="p1">**</ept> som er tilgjengelig på denne siden, for å endre beløpet som belastes på en bestemt gebyrlinje.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Once a charges line is overwritten manually, it will not be systematically recalculated unless the user initiates the <bpt id="p1">**</bpt>Recalculate charges<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når en gebyrlinje blir overskrevet manuelt, blir den ikke systematisk beregnet på nytt med mindre brukeren starter operasjonen <bpt id="p1">**</bpt>Beregn gebyrer på nytt<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>If the <bpt id="p1">**</bpt>Charge override reason code<ept id="p1">**</ept> has been configured on the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> setup page, the user will be prompted to provide a reason code when charges have been modified in the POS application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis <bpt id="p1">**</bpt>Overstyringsårsakskode for tillegg<ept id="p1">**</ept> er konfigurert på oppsettssiden for <bpt id="p2">**</bpt>Detaljhandelsparametere<ept id="p2">**</ept>, blir brukeren bedt om å oppgi en årsakskode når tilleggene er endret i salgsstedsprogrammet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>If reason codes have been captured for overwritten charges, a new report is also available to review and audit these overrides.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis årsakskoder er registrert for overskrevne gebyrer, finnes det også en ny rapport hvor du kan se gjennom og revidere disse overstyringene.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>The report can be found in <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Inquiries and reports <ph id="ph2">\&gt;</ph> Charge override history<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rapporten finnes i <bpt id="p1">**</bpt>Detaljhandel <ph id="ph1">\&gt;</ph> Forespørsler og rapporter <ph id="ph2">\&gt;</ph> Historikk for gebyroverstyring<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Refunding charges on a POS return transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Refundere tillegg i en returtransaksjon på salgsstedet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>If the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>, the existing retail parameter for <bpt id="p3">**</bpt>Refund shipping charges<ept id="p3">**</ept> is no longer applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis parameteren <bpt id="p1">**</bpt>Bruk avanserte automatiske gebyrer<ept id="p1">**</ept> er satt til <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept>, er ikke den eksisterende detaljhandelsparameteren for <bpt id="p3">**</bpt>Refundering av forsendelseskostnader<ept id="p3">**</ept> lenger tilgjengelig.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>To indicate which charges should be systematically refunded to a customer when using advanced auto-charges, ensure the related charges code has been configured as <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> setup page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">For å angi hvilke tillegg som skal refunderes systematisk til en kunde ved bruk av avanserte automatiske gebyrer, må du kontrollere at den tilknyttede gebyrkoden er konfigurert som <bpt id="p1">**</bpt>Refunderbar<ept id="p1">**</ept> på oppsettssiden for <bpt id="p2">**</bpt>Tilleggskode<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Make sure that the settings have been synchronized to your Retail channel databases through distribution schedule processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kontroller at innstillingene er synkronisert til detaljhandelskanaldatabasene via distribusjonplanbehandlingen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Refunding charges on a return order transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Refundere tillegg i en returordretransaksjon</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Charges are not systematically refunded to <bpt id="p1">**</bpt>Return orders<ept id="p1">**</ept> created in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tillegg blir ikke systematisk refundert til <bpt id="p1">**</bpt>Returordrer<ept id="p1">**</ept> som er opprettet i Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Users are required to select the <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> option when creating the <bpt id="p2">**</bpt>Return order<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Brukere må velge <bpt id="p1">**</bpt>Kopier gebyrer<ept id="p1">**</ept>-alternativet når de oppretter <bpt id="p2">**</bpt>returordren<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>If <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> is not selected, charges from the original sales transaction will not be automatically refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis <bpt id="p1">**</bpt>Kopier gebyrer<ept id="p1">**</ept> ikke er merket av, blir ikke gebyrer fra den opprinnelige salgstransaksjonen automatisk refundert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>If <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> is selected, all charges will be copied to the return order and the user can manually edit or remove any charges they do not want to have refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis <bpt id="p1">**</bpt>Kopier gebyrer<ept id="p1">**</ept> er valgt, blir alle gebyrer kopiert til returordren, og brukeren kan manuelt redigere eller fjerne tillegg som de ikke vil ha refundert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The call center return order process currently does not acknowledge the <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Returordreprosessen for telefonsentre godtar for øyeblikket ikke <bpt id="p1">**</bpt>Refunderbar<ept id="p1">**</ept>-flagget i <bpt id="p2">**</bpt>Tilleggskode<ept id="p2">**</ept>-oppsettet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Configuring POS receipts to show charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konfigurere salgsstedskvitteringer for å vise tillegg</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>The following receipt elements have been added to the receipt line and footer to support the advanced auto-charges functionality.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">De følgende kvitteringselementene er lagt til på kvitteringslinjen og bunnteksten for å støtte funksjonen for avanserte automatiske gebyrer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source><bpt id="p1">**</bpt>Line Shipping Charges<ept id="p1">**</ept> – This line-level element can be used to recap specific charges codes that have been applied to the sales line.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Forsendelseskostnader for linje<ept id="p1">**</ept> – Dette linjenivåelementet kan brukes til å oppsummere bestemt tilleggskoder som er brukt på salgslinjen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Only charges codes that have been flagged as <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> charges on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> page will be displayed here.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Bare tilleggskoder som er flagget som <bpt id="p1">**</bpt>Forsendelse<ept id="p1">**</ept>-tillegg på <bpt id="p2">**</bpt>Tilleggskode<ept id="p2">**</ept>-siden, vises her.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source><bpt id="p1">**</bpt>Line Other Charges<ept id="p1">**</ept> – This line-level element can be used to recap any non-shipping specific charge codes that have been applied to the sales line.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Andre tillegg for linje<ept id="p1">**</ept> – Dette linjenivåelementet kan brukes til å oppsummere ikke-forsendelsesbestemte tilleggskoder som er brukt på salgslinjen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>These are charges codes where the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> flag on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> page has not been enabled.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Dette er tilleggskoder der <bpt id="p1">**</bpt>Forsendelse<ept id="p1">**</ept>-flagget på <bpt id="p2">**</bpt>Tilleggskode<ept id="p2">**</ept>-siden ikke er aktivert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source><bpt id="p1">**</bpt>Order Shipping Charges Details<ept id="p1">**</ept> – This footer-level element displays the descriptions of the charge codes applied to the order that have been flagged as <bpt id="p2">**</bpt>Shipping<ept id="p2">**</ept> charges on the <bpt id="p3">**</bpt>Charges code<ept id="p3">**</ept> setup page.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Detaljer for forsendelseskostnader for ordre<ept id="p1">**</ept> – Dette elementet på bunntekstnivå viser beskrivelsene av gebyrkodene som er brukt i ordren som er flagget som <bpt id="p2">**</bpt>Forsendelse<ept id="p2">**</ept>-tillegg på oppsettssiden for <bpt id="p3">**</bpt>Tilleggskode<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source><bpt id="p1">**</bpt>Order Shipping Charges<ept id="p1">**</ept> – This footer-level element shows the dollar value of the shipping-related charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Forsendelseskostnader for ordre<ept id="p1">**</ept> – Dette elementet på bunntekstnivå viser kroneverdien av kostnadene knyttet til forsendelsen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source><bpt id="p1">**</bpt>Order Other Charges Details<ept id="p1">**</ept> – This footer-level element displays the description of the charges codes applied to the order that have not been flagged as shipping-related charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Detaljer for andre kostnader for ordre<ept id="p1">**</ept> – Dette elementet på bunntekstnivå viser beskrivelsen av gebyrkodene som er brukt i ordren som ikke er flagget som forsendelsesrelaterte tillegg.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source><bpt id="p1">**</bpt>Order Other Charges<ept id="p1">**</ept> – This footer-level element displays the dollar value of the other charges that are not shipping-related.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Andre kostnader for ordre<ept id="p1">**</ept> – Dette elementet på bunntekstnivå viser kroneverdien av andre kostnader som ikke er relatert til forsendelsen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>It is recommended that the organization also add free text fields to the receipt footer, in order to define the areas where charges will be recapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Det anbefales at organisasjonen også legger til fritekstfelt i kvitteringsbunnteksten, for å definere områdene der tillegg oppsummeres.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Preventing charges from being calculated until the POS order is completed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hindre at tillegg blir beregnet før salgsstedsordren er fullført</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Some organizations may prefer to wait until the user has finished adding all of the sales lines to the POS transaction before calculating charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Noen organisasjoner kan foretrekke å vente til brukeren er ferdig med å legge til alle salgslinjene i salgsstedstransaksjonen før tilleggene beregnes.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>To prevent calculation of charges as items are added to the POS transaction, turn on the <bpt id="p1">**</bpt>Manual charge calculation<ept id="p1">**</ept> parameter in the <bpt id="p2">**</bpt>Functionality profile<ept id="p2">**</ept> used by the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Du kan unngå beregning av gebyrer etter hvert som varer legges til salgsstedstransaksjonen, ved å aktivere parameteren <bpt id="p1">**</bpt>Manuell tilleggsberegning<ept id="p1">**</ept> i <bpt id="p2">**</bpt>funksjonalitetsprofilen<ept id="p2">**</ept> som butikken bruker.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Enabling this parameter will require the POS user to use the <bpt id="p1">**</bpt>Calculate totals<ept id="p1">**</ept> operation when they have completed adding the products to the POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aktivering av denne parameteren krever at salgsstedsbrukeren bruker operasjonen <bpt id="p1">**</bpt>Beregne totaler<ept id="p1">**</ept> når de er ferdig med å legge til produktene i salgsstedstransaksjonen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>The <bpt id="p1">**</bpt>Calculate totals<ept id="p1">**</ept> operation will then trigger the calculation of any auto charges for the order header or lines as applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Beregne totaler<ept id="p1">**</ept>-operasjonen vil deretter utløse beregningen av automatiske gebyrer for ordrehodet eller -linjene etter behov.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Charges override reports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tillegg overstyrer rapporter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>If users manually override the calculated charges or add a manual charge to the transaction, this data will available for auditing in the <bpt id="p1">**</bpt>Charge Override History<ept id="p1">**</ept> report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis brukere overstyrer de beregnede kostnadene manuelt eller legger til et manuelt tillegg i transaksjonen, vil disse dataene være tilgjengelige for revisjon i rapporten <bpt id="p1">**</bpt>Historikk for gebyroverstyring<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>The report can be accessed from <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Inquiries and reports <ph id="ph2">\&gt;</ph> Charge Override History<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rapporten er tilgjengelig fra <bpt id="p1">**</bpt>Detaljhandel <ph id="ph1">\&gt;</ph> Forespørsler og rapporter <ph id="ph2">\&gt;</ph> Historikk for gebyroverstyring<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>It is important to note that the data needed for this report is imported from the channel database into HQ through the "P" distribution schedule jobs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Det er viktig å være oppmerksom på at dataene som kreves for denne rapporten, importeres fra kanaldatabasen til HK via "P"-distribusjonsplanleggingsjobber.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Therefore, information about overrides just performed in the POS may not be immediately available on this report until this job has uploaded the store transaction data into HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Informasjon om overstyringer som nettopp er utført på salgsstedet, er derfor kanskje ikke tilgjengelig umiddelbart i denne rapporten før denne jobben har lastet opp butikktransaksjonsdataene til HK.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>