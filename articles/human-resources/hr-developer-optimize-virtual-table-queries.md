---
title: Optimere forespørgsler til Dataverse-virtuelle tabeller
description: Optimere og foretage fejlfinding af ydeevnen for Dataverse-virtuelle tabelforespørgsler
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66fb9f2b50079b5eb4eb16da17b8a473d687d354
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054902"
---
# <a name="optimize-dataverse-virtual-table-queries"></a><span data-ttu-id="a1034-103">Optimere forespørgsler til Dataverse-virtuelle tabeller</span><span class="sxs-lookup"><span data-stu-id="a1034-103">Optimize Dataverse virtual table queries</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="a1034-104">Fejl</span><span class="sxs-lookup"><span data-stu-id="a1034-104">Issue</span></span>

### <a name="overview"></a><span data-ttu-id="a1034-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="a1034-105">Overview</span></span>

<span data-ttu-id="a1034-106">Når du bruger Dataverse-virtuelle tabeller til at udvikle integrationer og andre dataforbindelser med Dynamics 365 Human Resources, kan du opleve problemer med ydeevnen af forespørgsler på de virtuelle tabeller.</span><span class="sxs-lookup"><span data-stu-id="a1034-106">When using Dataverse virtual tables to develop integrations and other data connections with Dynamics 365 Human Resources, you can experience performance issues with queries against the virtual tables.</span></span> <span data-ttu-id="a1034-107">Den langsomme udførelse af forespørgsler kan forekomme på tværs af forskellige klienter eller grænseflader.</span><span class="sxs-lookup"><span data-stu-id="a1034-107">The slow query execution can occur across various clients or interfaces.</span></span> <span data-ttu-id="a1034-108">Du kan f.eks. opleve problemet under følgende omstændigheder:</span><span class="sxs-lookup"><span data-stu-id="a1034-108">For example, you may experience the issue in the following circumstances:</span></span>

- <span data-ttu-id="a1034-109">Når du forespørger på en virtuel tabel via Dataverse Web-API'en</span><span class="sxs-lookup"><span data-stu-id="a1034-109">When querying a virtual table through the Dataverse Web API</span></span>
- <span data-ttu-id="a1034-110">Når du opretter en Power App mod en virtuel tabel</span><span class="sxs-lookup"><span data-stu-id="a1034-110">When creating a Power App against a virtual table</span></span>
- <span data-ttu-id="a1034-111">Når du bygger en Power BI-rapport på en virtuel tabel</span><span class="sxs-lookup"><span data-stu-id="a1034-111">When building a Power BI report on a virtual table</span></span>

<span data-ttu-id="a1034-112">Alle disse grænseflader har potentialet til at vise ydeevneproblemet.</span><span class="sxs-lookup"><span data-stu-id="a1034-112">All these interfaces have the potential to surface the performance issue.</span></span>

<span data-ttu-id="a1034-113">En af årsagerne til den langsomme ydeevne med Dataverse-virtuelle tabeller til Human Resources er kolonnerne med fremmede nøgler i den virtuelle tabel, der er relateret til tabellens [navigationsegenskaber](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span><span class="sxs-lookup"><span data-stu-id="a1034-113">One cause of slow performance with Dataverse virtual tables for Human Resources is the foreign key columns of the virtual table related to the table's [navigation properties](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span></span> <span data-ttu-id="a1034-114">Når der oprettes navigationsegenskaber for en virtuel tabel, føjes der automatisk en kolonne med en fremmed nøgle til tabellen for at repræsentere værdien af nøglen for den relaterede virtuelle tabels nøglekolonne.</span><span class="sxs-lookup"><span data-stu-id="a1034-114">When navigation properties are created for a virtual table, a foreign key column is automatically added to the table to represent the value of the key for the related virtual table's key column.</span></span> <span data-ttu-id="a1034-115">Kolonnen **_mshr_fk_person_id_value** føjes f.eks. til enheden **mshr_hcmworkerbaseentity** med egenskaben for fremmed nøgle fra enheden **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="a1034-115">For example, the **_mshr_fk_person_id_value** column is added to the **mshr_hcmworkerbaseentity** entity with the foreign key property from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="a1034-116">På grund af, hvordan værdierne for disse kolonner med fremmede nøgler bevares i en tabel, kan hentning af værdierne have en negativ indvirkning på en forespørgsels ydeevne i forhold til den virtuelle tabel.</span><span class="sxs-lookup"><span data-stu-id="a1034-116">Because of how the values for these foreign key columns are maintained in a table, fetching the values can have a negative impact on the performance of a query against the virtual table.</span></span>

### <a name="potential-symptoms"></a><span data-ttu-id="a1034-117">Potentielle symptomer</span><span class="sxs-lookup"><span data-stu-id="a1034-117">Potential symptoms</span></span>

<span data-ttu-id="a1034-118">Et eksempel, hvor du kan se denne indvirkning, er forespørgsler på enheden Arbejder (**mshr_hcmworkerentity**) eller Basisarbejder (**mshr_hcmworkerbaseentity**).</span><span class="sxs-lookup"><span data-stu-id="a1034-118">An example where you may see this impact is in queries against the Worker (**mshr_hcmworkerentity**) or Base worker (**mshr_hcmworkerbaseentity**) entity.</span></span> <span data-ttu-id="a1034-119">Du kan se, at ydeevneproblemet manifesterer sig på et par forskellige måder:</span><span class="sxs-lookup"><span data-stu-id="a1034-119">You may see the performance issue manifest itself in a few different ways:</span></span>

- <span data-ttu-id="a1034-120">**Langsom udførelse af forespørgsler**: Forespørgslen på den virtuelle tabel kan returnere de forventede resultater, men det tager længere tid end forventet at fuldføre udførelsen af forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="a1034-120">**Slow query execution**: The query against the virtual table may return the expected results, but take longer than expected to complete execution of the query.</span></span>
- <span data-ttu-id="a1034-121">**Timeout for forespørgsel**: Forespørgslen får muligvis timeout og returnerer følgende fejl: "Der blev anskaffet et token til kald af Finance and Operations, men Finance and Operations returnerede en fejl af typen InternalServerError".</span><span class="sxs-lookup"><span data-stu-id="a1034-121">**Query timeout**: The query may time out and return the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type InternalServerError."</span></span>
- <span data-ttu-id="a1034-122">**Uventet fejl** : Forespørgslen kan returnere en fejltype 400 med følgende meddelelse: "Der opstod en uventet fejl".</span><span class="sxs-lookup"><span data-stu-id="a1034-122">**Unexpected error**: The query may return an error type 400 with the following message: "An unexpected error occurred."</span></span>

  ![Fejltype 400 på HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType400.png)

- <span data-ttu-id="a1034-124">**Begrænsning**: Forespørgslen kan overforbruge serverressourcer og blive udsat for begrænsning.</span><span class="sxs-lookup"><span data-stu-id="a1034-124">**Throttling**: The query may overuse server resources, and become subject to throttling.</span></span> <span data-ttu-id="a1034-125">I dette tilfælde returnerer forespørgslen følgende fejl: "Der blev anskaffet et token til kald af Finance and Operations, men Finance and Operations returnerede en fejl af typen 429".</span><span class="sxs-lookup"><span data-stu-id="a1034-125">In this case, the query returns the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type 429."</span></span> <span data-ttu-id="a1034-126">Yderligere oplysninger om begrænsning af Human Resources finder du i [Ofte stillede spørgsmål om begrænsning](./hr-admin-integration-throttling-faq.md).</span><span class="sxs-lookup"><span data-stu-id="a1034-126">For more information in throttling in Human Resources, see [Throttling FAQ](./hr-admin-integration-throttling-faq.md).</span></span>

  ![Fejltype 429 på HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a><span data-ttu-id="a1034-128">Løsning</span><span class="sxs-lookup"><span data-stu-id="a1034-128">Resolution</span></span>

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a><span data-ttu-id="a1034-129">Begrænse antallet af kolonner i dataforespørgslen</span><span class="sxs-lookup"><span data-stu-id="a1034-129">Limit the number of columns included in your data query</span></span>

<span data-ttu-id="a1034-130">Med virtuelle tabeller er en af de metoder, der har det største potentiale til at forbedre forespørgselsydeevnen, at begrænse antallet af kolonner, der er valgt i forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="a1034-130">With virtual tables, one of the methods with the greatest potential to improve query performance is to limit the number of columns selected in the query.</span></span> <span data-ttu-id="a1034-131">Den generelle vejledning til optimering af forespørgselsydeevnen er at begrænse de kolonner, der returneres i forespørgslen, til kun de egenskaber, du har brug for.</span><span class="sxs-lookup"><span data-stu-id="a1034-131">The general guidance for optimizing query performance is to limit the columns returned in your query to only those properties that you need.</span></span> <span data-ttu-id="a1034-132">Dette gælder især for kolonnerne med fremmede nøgler i virtuelle tabeller.</span><span class="sxs-lookup"><span data-stu-id="a1034-132">This is particularly true with the foreign key columns on virtual tables.</span></span> <span data-ttu-id="a1034-133">Hvis du ikke har brug for værdierne i kolonnerne med den fremmede nøgle til integrationen eller rapporten, skal du strukturere forespørgslen, så du kun vælger de kolonner, du har brug for, og udelader kolonnerne med den fremmede nøgle.</span><span class="sxs-lookup"><span data-stu-id="a1034-133">If you don't need the values in the foreign key columns for your integration or report, then structure the query to select only the columns you need, excluding the foreign key columns.</span></span>

#### <a name="selecting-columns-in-an-odata-query"></a><span data-ttu-id="a1034-134">Vælge kolonner i en OData-forespørgsel</span><span class="sxs-lookup"><span data-stu-id="a1034-134">Selecting columns in an OData query</span></span>

<span data-ttu-id="a1034-135">Når du forespørger på en virtuel tabel via Dataverse Web-API'en, kan du begrænse antallet af kolonner i forespørgslen ved at bruge indstillingen **$select**-systemforespørgsel og definere de kolonner, der skal returneres resultater for.</span><span class="sxs-lookup"><span data-stu-id="a1034-135">When querying a virtual table through the Dataverse Web API, you can limit the number of columns included in the query by using the **$select** system query option, and define the columns for which you need results returned.</span></span> <span data-ttu-id="a1034-136">Hvis du vil maksimere ydeevnen, skal du udelukke kolonner med fremmede nøgle (dem med **_mshr_FK_** som præfiks) fra forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="a1034-136">To maximize performance, exclude foreign key columns (those with the **_mshr_FK_** prefix) from the query.</span></span>

<span data-ttu-id="a1034-137">Følgende forespørgsel på enheden **mshr_hcmworkerbaseentity** omfatter f.eks. kun de kolonner, der er medtaget i forespørgselsindstillingen **$select**, uden værdier for fremmed nøgle.</span><span class="sxs-lookup"><span data-stu-id="a1034-137">For example, the following query against the **mshr_hcmworkerbaseentity** entity will include only the columns included in the **$select** query option clause, excluding foreign key values.</span></span> <span data-ttu-id="a1034-138">Dette giver betydelige forbedringer af ydeevnen i forbindelse med en forespørgsel, der omfatter alle tabelkolonner.</span><span class="sxs-lookup"><span data-stu-id="a1034-138">This provides significant improvements in performance over a query that includes all table columns.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="a1034-139">Anbefalingen om at begrænse antallet af valgte kolonner gælder også, når du bruger indstillingen **$expand** til at udvide forespørgslen til relaterede virtuelle tabeller ved hjælp af navigationsegenskaber.</span><span class="sxs-lookup"><span data-stu-id="a1034-139">The recommendation to limit the number of columns selected also applies when using the **$expand** query option to expand the query to related virtual tables through navigation properties.</span></span> <span data-ttu-id="a1034-140">Følgende forespørgsel indeholder f.eks. kolonner fra enheden **mshr_hcmworkerbaseentity** med udvidede kolonner fra enheden **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="a1034-140">For example, the following query includes columns from the **mshr_hcmworkerbaseentity** entity with expanded columns from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="a1034-141">Bemærk, at forespørgselsindstillingen **$select** også er medtaget i forespørgselsindstillingen **$expand**.</span><span class="sxs-lookup"><span data-stu-id="a1034-141">Note that the **$select** query option is also included in the **$expand** query option clause.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="a1034-142">Når du bruger denne metode til at hente data med forespørgselsindstillingen **$select** i forespørgselsklausulen **$expand**, vil du typisk få større forbedringer af ydeevnen, når navigationsegenskaben mellem enhederne er en mange til en-relation.</span><span class="sxs-lookup"><span data-stu-id="a1034-142">When using this method of retrieving data with the **$select** query option in the **$expand** query option clause, you will typically see greater performance improvements when the navigation property between the entities is a many-to-one relationship.</span></span> <span data-ttu-id="a1034-143">Du oplever måske ikke samme fald i udførelsestiden af forespørgsler, når en én til mange-relation udvides.</span><span class="sxs-lookup"><span data-stu-id="a1034-143">You may not see the same decrease in query execution time when expanding a one-to-many relationship.</span></span> <span data-ttu-id="a1034-144">Du kan finde flere oplysninger om relationsdefinition til Dataverse-virtuelle tabeller i [Tabelrelationer](/powerapps/maker/data-platform/create-edit-entity-relationships).</span><span class="sxs-lookup"><span data-stu-id="a1034-144">For more information on relationship definition for Dataverse virtual tables, see [Table relationships](/powerapps/maker/data-platform/create-edit-entity-relationships).</span></span>

<span data-ttu-id="a1034-145">Yderligere oplysninger om brug af indstillingerne **$select** og **$expand** til systemforespørgslen i Dataverse Web-API'en finder du i [Hente relaterede enhedsposter med en forespørgsel](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span><span class="sxs-lookup"><span data-stu-id="a1034-145">For more information on using the **$select** and **$expand** system query options in the Dataverse Web API, see [Retrieve related entity records with a query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span></span>

#### <a name="selecting-columns-in-power-bi"></a><span data-ttu-id="a1034-146">Vælge kolonner i Power BI</span><span class="sxs-lookup"><span data-stu-id="a1034-146">Selecting columns in Power BI</span></span>

<span data-ttu-id="a1034-147">Hvis du oplever en eller flere af de ovennævnte tegn på, at ydeevnen er langsom, når du opbygger en Power BI-rapport mod en Dataverse-virtuel tabel, kan du forbedre ydeevnen ved at udelukke kolonner med fremmed nøgle fra de kolonner, der er valgt i tabellen til rapporten.</span><span class="sxs-lookup"><span data-stu-id="a1034-147">If you experience any of the aforementioned indications of slow performance when building a Power BI report against a Dataverse virtual table, you can improve the performance by excluding foreign key columns from the columns selected from the table for the report.</span></span> <span data-ttu-id="a1034-148">Hvis du f.eks. bruger Power BI Desktop til at oprette en rapport i forhold til enheden **mshr_hcmworkerbaseentity**, kan du bruge følgende trin til at vælge de kolonner, du vil have medtaget i rapportforespørgslen.</span><span class="sxs-lookup"><span data-stu-id="a1034-148">For example, if you are using Power BI Desktop to create a report against the **mshr_hcmworkerbaseentity** entity, you can use the following steps to select the columns you want included in the report query.</span></span>

1. <span data-ttu-id="a1034-149">I Power BI Desktop skal du vælge **Mere...** på rullelisten **Hent data** på handlingsbåndet.</span><span class="sxs-lookup"><span data-stu-id="a1034-149">In Power BI Desktop, select **More...** from the **Get data** drop-down list on the action ribbon.</span></span>
2. <span data-ttu-id="a1034-150">I vinduet **Hent data** skal du angive **Common Data Service** i søgefeltet, vælge connectoren **Common Data Service** og vælge **Opret forbindelse**.</span><span class="sxs-lookup"><span data-stu-id="a1034-150">In the **Get Data** window, enter **Common Data Service** in the search box, select the **Common Data Service** connector, and select **Connect**.</span></span>
3. <span data-ttu-id="a1034-151">Angiv organisationens URI for dit Dataverse-miljø i feltet **URL-adresse til serveren** i Common Data Service-vinduet, og vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a1034-151">In the **Server Url** field of the Common Data Service window, enter the organization URI for your Dataverse environment, and select **OK**.</span></span>
  
   ![Angiv URI for dit Dataverse-miljø](./media/PowerBIDataverseURLSetup.png)
  
4. <span data-ttu-id="a1034-153">Udvid **Enheder**-noden i vinduet Navigator.</span><span class="sxs-lookup"><span data-stu-id="a1034-153">In the Navigator window, expand the **Entities** node.</span></span>
5. <span data-ttu-id="a1034-154">I søgefeltet skal du angive **mshr_hcmworkerbaseentity** og vælge enheden.</span><span class="sxs-lookup"><span data-stu-id="a1034-154">In the search box, enter **mshr_hcmworkerbaseentity**, and select the entity.</span></span>
6. <span data-ttu-id="a1034-155">Vælg **Transformer data**.</span><span class="sxs-lookup"><span data-stu-id="a1034-155">Select **Transform Data**.</span></span>
7. <span data-ttu-id="a1034-156">Vælg **Avanceret editor** i vinduet Power Query-editor.</span><span class="sxs-lookup"><span data-stu-id="a1034-156">In the Power Query Editor window, select **Advanced Editor**.</span></span>
8. <span data-ttu-id="a1034-157">Opdater forespørgslen i vinduet **Avanceret editor**, så den ligner nedenstående, og tilføj eller fjern eventuelle kolonner til matrixen, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="a1034-157">In the **Advanced Editor** window, update the query to look like the below, adding or removing any columns to the array as needed.</span></span>

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Opdatere forespørgslen i Avanceret editor til Power Query-editor](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. <span data-ttu-id="a1034-159">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="a1034-159">Select **Done**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="a1034-160">Hvis du tidligere har modtaget en fejl af typen 429 fra forespørgslen før opdateringen, skal du muligvis vente, indtil gentagelsesperioden opdaterer forespørgslen, før den fuldføres.</span><span class="sxs-lookup"><span data-stu-id="a1034-160">If you previously received an error of type 429 from the query prior to updating, you may need to wait for the retry period prior to refreshing the query for it to complete successully.</span></span>

10. <span data-ttu-id="a1034-161">Klik på **Luk og anvend** på handlingsbåndet i Power Query-editor.</span><span class="sxs-lookup"><span data-stu-id="a1034-161">Click **Close & Apply** on the Power Query Editor action ribbon.</span></span>

<span data-ttu-id="a1034-162">Derefter kan du begynde at opbygge Power BI-rapporten i forhold til de kolonner, der er valgt fra den virtuelle tabel.</span><span class="sxs-lookup"><span data-stu-id="a1034-162">You're then able to begin building your Power BI report against the columns selected from the virtual table.</span></span>

#### <a name="selecting-columns-in-power-apps"></a><span data-ttu-id="a1034-163">Vælge kolonner i Power Apps</span><span class="sxs-lookup"><span data-stu-id="a1034-163">Selecting columns in Power Apps</span></span>

<span data-ttu-id="a1034-164">Ligesom med Dataverse Web-API-forespørgsler og Power BI kan du forbedre forespørgslens ydeevne for Power Apps baseret på Dataverse-virtuelle tabeller ved at udelukke kolonner fra relaterede tabeller i din app.</span><span class="sxs-lookup"><span data-stu-id="a1034-164">Similar to Dataverse Web API queries and Power BI, you can improve query performance for Power Apps based on Dataverse virtual tables by excluding columns of related tables from your app.</span></span> <span data-ttu-id="a1034-165">Hvis der er medtaget kolonner fra en relateret tabel på en side, vil den URL-adresse, der oprettes for anmodningen til hentning af dataene, indeholde egenskaber for fremmed nøgle for den relaterede tabel.</span><span class="sxs-lookup"><span data-stu-id="a1034-165">If any columns from a related table have been included on a page, then the request URL constructed to fetch the data will include foreign key properties of the related table.</span></span> <span data-ttu-id="a1034-166">Som i eksemplerne under [Vælge kolonner i en OData-forespørgsel](#selecting-columns-in-power-apps) ovenfor reducerer dette ydeevnen ved at forårsage yderligere dataopslag.</span><span class="sxs-lookup"><span data-stu-id="a1034-166">This, as in the examples of [Selecting columns in an OData Query](#selecting-columns-in-power-apps) above, reduces performance by causing additional data lookups.</span></span>

<span data-ttu-id="a1034-167">Du kan løse dette ved at validere, at der ikke er medtaget datafelter fra relaterede tabeller i nogen dataform i din Power App.</span><span class="sxs-lookup"><span data-stu-id="a1034-167">To work around this, you can validate that no data fields from related tables have been included on any data form of your Power App.</span></span>

1. <span data-ttu-id="a1034-168">Vælg dataformen til skærmen i trævisningsruden.</span><span class="sxs-lookup"><span data-stu-id="a1034-168">In the Tree view pane, select the data form for the screen.</span></span>
2. <span data-ttu-id="a1034-169">Vælg **Rediger** på egenskaben **Felter** i **Egenskaber**-ruden.</span><span class="sxs-lookup"><span data-stu-id="a1034-169">In the **Properties** pane, select **Edit** on the **Fields** property.</span></span>
3. <span data-ttu-id="a1034-170">Kontrollér i **Data**-ruden, at ingen af de valgte felter er felter i den virtuelle tabel for datakilden.</span><span class="sxs-lookup"><span data-stu-id="a1034-170">In the **Data** pane, verify that none of the selected fields are fields of the virtual table of the data source.</span></span>

<span data-ttu-id="a1034-171">Hvis f.eks. et af de datafelter, der er medtaget på en side i appen, refererer til en anden tabel, f.eks. **ThisItem.Worker.Name**, hvor **Arbejder** er den relaterede tabel, er der et potentiale for reduceret ydeevne ved hentning af dataene.</span><span class="sxs-lookup"><span data-stu-id="a1034-171">For example, if one of the data fields included on a page in the app references another table, such as **ThisItem.Worker.Name**, where **Worker** is the related table, there is a potential for reduced performance in fetching the data.</span></span>

<span data-ttu-id="a1034-172">Du kan bruge [Power Apps-overvågning](/powerapps/maker/monitor-overview) til at sikre, at det kun er de kolonner, du skal bruge, der medtages i forespørgslen for at hente dataene til Power App.</span><span class="sxs-lookup"><span data-stu-id="a1034-172">You can use the [Power Apps Monitor](/powerapps/maker/monitor-overview) to ensure that only the columns you need are being included in the query to get the data for the Power App.</span></span> <span data-ttu-id="a1034-173">Du kan få vist den URL-adresse, der er konstrueret til operationen getRows, for at sikre, at de kolonner, du har valgt til din app, er optimale, når du henter dataene.</span><span class="sxs-lookup"><span data-stu-id="a1034-173">You can view the URL constructed for the getRows operation to ensure the columns you have selected for your app will be optimal for retrieving the data.</span></span>

![Bruge Power Apps-overvågning til at analysere getData-operationen](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a><span data-ttu-id="a1034-175">Filtrering af dataforespørgslen</span><span class="sxs-lookup"><span data-stu-id="a1034-175">Filtering the data query</span></span>

<span data-ttu-id="a1034-176">En anden metode til forbedring af ydeevnen under udførelse af forespørgsler er at begrænse antallet af poster, der returneres i forespørgselsresultaterne.</span><span class="sxs-lookup"><span data-stu-id="a1034-176">Another method for improving query execution performance is to limit the number of records returned in the query results.</span></span> <span data-ttu-id="a1034-177">Det kan du gøre ved at filtrere resultaterne for at sikre, at du kun får de poster, du har brug for.</span><span class="sxs-lookup"><span data-stu-id="a1034-177">You can do this by filtering the results to ensure that you are only receiving the records you need.</span></span>

<span data-ttu-id="a1034-178">Se [Filtrere resultater](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for at få flere oplysninger om filtrering af forespørgselsdata.</span><span class="sxs-lookup"><span data-stu-id="a1034-178">See [Filter results](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for more information on filtering query data.</span></span>

### <a name="limiting-the-page-size-of-the-query"></a><span data-ttu-id="a1034-179">Begrænse sidestørrelsen af forespørgslen</span><span class="sxs-lookup"><span data-stu-id="a1034-179">Limiting the page size of the query</span></span>

<span data-ttu-id="a1034-180">Hvis du arbejder med store datasæt, kan du opdele forespørgselsresultater i flere sider ved at føje `odata.maxpagesize`-præferenceoverskriften til dataforespørgsler.</span><span class="sxs-lookup"><span data-stu-id="a1034-180">If you're working with large data sets, you can divide query results into multiple pages by adding the `odata.maxpagesize` preference header to data queries.</span></span>

<span data-ttu-id="a1034-181">Du kan finde flere oplysninger om sideinddeling i [Angive det antal enheder, der skal returneres på en side](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span><span class="sxs-lookup"><span data-stu-id="a1034-181">For more information on paging, see [Specify the number of entities to return in a page](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span></span>

## <a name="see-also"></a><span data-ttu-id="a1034-182">Se også</span><span class="sxs-lookup"><span data-stu-id="a1034-182">See also</span></span>

- [<span data-ttu-id="a1034-183">Konfigurere virtuelle Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="a1034-183">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)
- [<span data-ttu-id="a1034-184">Ofte stillede spørgsmål om Human Resources virtuelle tabeller</span><span class="sxs-lookup"><span data-stu-id="a1034-184">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)
- [<span data-ttu-id="a1034-185">Ofte stillede spørgsmål om begrænsning</span><span class="sxs-lookup"><span data-stu-id="a1034-185">Throttling FAQ</span></span>](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]