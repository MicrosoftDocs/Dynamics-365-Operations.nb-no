<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="environment-reprovision.md" target-language="nb-NO">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>environment-reprovision.33170a.795ff0c91f6e5c2ac83dd610a125d2f6fdbbec70.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>795ff0c91f6e5c2ac83dd610a125d2f6fdbbec70</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\includes\environment-reprovision.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101">
          <source>When copying a database between environments, you will need to run the environment re-provisioning tool before the copied database is fully functional, to ensure that all Retail components are up-to-date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Når du kopierer en database mellom miljøer, må du kjøre verktøyet for ny klargjøring av miljøet før den kopierte databasen kan tas i bruk, slik at alle Retail-komponenter er oppdatert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102">
          <source>We recommend that you run this procedure whether you are using Retail components or not, because Retail functionality is included in all environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vi anbefaler at du kjører denne prosedyren enten du bruker Retail-komponenter eller ikke, fordi Retail-funksjonalitet er inkludert i alle miljøer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Before you continue, you must make sure that the following prerequisites are met:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Før du fortsetter, må du kontrollere at følgende forutsetninger er oppfylt:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>If you are upgrading to the July 2017 release (also known as 7.2) 7.2.11792.56024, apply the following application X++ hotfixes in the destination environment before running the data upgrade in that environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du oppgraderer til juli 2017-utgivelsen 7.2.11792.56024 (også kalt 7.2), bruker du følgende X++-hurtigreparasjoner til programmet i målmiljøet før du kjører dataoppgraderingen i dette miljøet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>These will prevent various errors occurring during the data upgrade:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dette forhindrer at ulike feil oppstår under dataoppgraderingen:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>KB 4036156 - Retail minor version upgrade - 'Variant number sequence is not set.'</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KB 4036156 – Mindre versjonsoppgradering for Retail – Variantnummerserie er ikke angitt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This fix package also includes KB 4035399 and KB 4035751.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Denne reparasjonspakken inneholder også KB 4035399 og KB 4035751.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Note that you must have a minimum of Platform Update 9 to use this package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vær oppmerksom på at du må ha minimum Platform Update 9 for å bruke denne pakken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>If you are unsure, install the latest binaries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du er usikker, installerer du de nyeste binærfilene.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>If you are upgrading from Microsoft Dynamics AX 2012, install the following application X++ fixes in the destination environment before you run the data upgrade:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du oppgraderer fra Microsoft Dynamics AX 2012, installerer du følgende X++-reparasjoner til programmet i målmiljøet før du kjører dataoppgraderingen:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>KB 4033183 - Dynamics AX 2012 R2 or Dynamics AX 2012 R3 Pre-CU8 non-retail upgrade fails with Object not found for dbo.RETAILTILLLAYOUTZONE.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KB 4033183 – Dynamics AX 2012 R2- eller Dynamics AX 2012 R3 Pre-CU8-oppgraderingen for ikke-detaljhandel mislykkes med feilen Finner ikke objekt for dbo.RETAILTILLLAYOUTZONE.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>KB 4040692 - Dynamics AX 2012 R3 to Microsoft Dynamics 365 for Operations 7.2 upgrade fails on RetailSalesLine duplicate index on SalesLineIdx.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KB 4040692 – Oppgraderingen fra Dynamics AX 2012 R3 til Microsoft Dynamics 365 for Operations 7.2 mislykkes på grunn av duplisert indeks for RetailSalesLine på SalesLineIdx.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>KB 4035490 - Performance issue with GeneralJournalAccountEntry MainAccount field upgrade script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KB 4035490 – Ytelsesproblem med oppgraderingsskriptet til feltet GeneralJournalAccountEntry MainAccount.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Follow these steps to run the Environment reprovisioning tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Følg denne fremgangsmåten for å kjøre verktøyet for ny klargjøring av miljøet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In the Shared asset library, select <bpt id="p1">**</bpt>Software deployable package<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Velg <bpt id="p1">**</bpt>Distribuerbar programvarepakke<ept id="p1">**</ept> i Delt aktivabibliotek.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Download the Environment reprovisioning tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Last ned verktøyet for ny klargjøring av miljøet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In the asset library for your project, select <bpt id="p1">**</bpt>Software deployable package<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Velg <bpt id="p1">**</bpt>Distribuerbar programvarepakke<ept id="p1">**</ept> i aktivabiblioteket for prosjektet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Select <bpt id="p1">**</bpt>New<ept id="p1">**</ept> to create a new package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Velg <bpt id="p1">**</bpt>Ny<ept id="p1">**</ept> for å opprette en ny pakke.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Enter a name and description for the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Angi et navn og en beskrivelse for pakken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>You can use <bpt id="p1">**</bpt>Environment reprovisioning tool<ept id="p1">**</ept> as the package name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Du kan bruke <bpt id="p1">**</bpt>Verktøy for ny klargjøring av miljø<ept id="p1">**</ept> som pakkenavn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Upload the package that you downloaded earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Last opp pakken som du lastet ned tidligere.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>On the <bpt id="p1">**</bpt>Environment details<ept id="p1">**</ept> page for your target environment, select <bpt id="p2">**</bpt>Maintain<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>Apply updates<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Velg <bpt id="p2">**</bpt>Vedlikehold<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>Bruk oppdateringer<ept id="p3">**</ept> på siden <bpt id="p1">**</bpt>Miljødetaljer<ept id="p1">**</ept> for målmiljøet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Select the Environment reprovisioning tool that you uploaded earlier, and then select <bpt id="p1">**</bpt>Apply<ept id="p1">**</ept> to apply the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Velg verktøyet for ny klargjøring av miljø som du lastet opp tidligere, og velg deretter <bpt id="p1">**</bpt>Bruk<ept id="p1">**</ept> for å bruke pakken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Monitor the progress of the package deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Overvåk fremdriften for pakkedistribusjonen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For more information about how to apply a deployable package, see <bpt id="p1">[</bpt>Apply a deployable package<ept id="p1">](../deployment/create-apply-deployable-package.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du vil ha mer informasjon om hvordan du bruker en distribuerbar pakke, kan du se <bpt id="p1">[</bpt>Bruke en distribuerbar pakke<ept id="p1">](../deployment/create-apply-deployable-package.md)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For more information about how to manually apply a deployable package, see <bpt id="p1">[</bpt>Install a deployable package<ept id="p1">](../deployment/install-deployable-package.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvis du vil ha mer informasjon om hvordan du bruker en distribuerbar pakke manuelt, kan du se <bpt id="p1">[</bpt>Installere en distribuerbar pakke<ept id="p1">](../deployment/install-deployable-package.md)</ept>.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>