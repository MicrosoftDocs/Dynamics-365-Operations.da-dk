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
ms.openlocfilehash: 1857d2e35e369bcd0c8f02a059a307f31da8b3b9
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067448"
---
# <a name="optimize-dataverse-virtual-table-queries"></a>Optimere forespørgsler til Dataverse-virtuelle tabeller


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



## <a name="issue"></a>Fejl

### <a name="overview"></a>Overblik

Når du bruger Dataverse-virtuelle tabeller til at udvikle integrationer og andre dataforbindelser med Dynamics 365 Human Resources, kan du opleve problemer med ydeevnen af forespørgsler på de virtuelle tabeller. Den langsomme udførelse af forespørgsler kan forekomme på tværs af forskellige klienter eller grænseflader. Du kan f.eks. opleve problemet under følgende omstændigheder:

- Når du forespørger på en virtuel tabel via Dataverse Web-API'en
- Når du opretter en Power App mod en virtuel tabel
- Når du bygger en Power BI-rapport på en virtuel tabel

Alle disse grænseflader har potentialet til at vise ydeevneproblemet.

En af årsagerne til den langsomme ydeevne med Dataverse-virtuelle tabeller til Human Resources er kolonnerne med fremmede nøgler i den virtuelle tabel, der er relateret til tabellens [navigationsegenskaber](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties). Når der oprettes navigationsegenskaber for en virtuel tabel, føjes der automatisk en kolonne med en fremmed nøgle til tabellen for at repræsentere værdien af nøglen for den relaterede virtuelle tabels nøglekolonne. Kolonnen **_mshr_fk_person_id_value** føjes f.eks. til enheden **mshr_hcmworkerbaseentity** med egenskaben for fremmed nøgle fra enheden **mshr_dirpersonentity**. På grund af, hvordan værdierne for disse kolonner med fremmede nøgler bevares i en tabel, kan hentning af værdierne have en negativ indvirkning på en forespørgsels ydeevne i forhold til den virtuelle tabel.

### <a name="potential-symptoms"></a>Potentielle symptomer

Et eksempel, hvor du kan se denne indvirkning, er forespørgsler på enheden Arbejder (**mshr_hcmworkerentity**) eller Basisarbejder (**mshr_hcmworkerbaseentity**). Du kan se, at ydeevneproblemet manifesterer sig på et par forskellige måder:

- **Langsom udførelse af forespørgsler**: Forespørgslen på den virtuelle tabel kan returnere de forventede resultater, men det tager længere tid end forventet at fuldføre udførelsen af forespørgslen.
- **Timeout for forespørgsel**: Forespørgslen får muligvis timeout og returnerer følgende fejl: "Der blev anskaffet et token til kald af Finans og drift, men Finans og drift returnerede en fejl af typen InternalServerError".
- **Uventet fejl** : Forespørgslen kan returnere en fejltype 400 med følgende meddelelse: "Der opstod en uventet fejl".

  ![Fejltype 400 på HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType400.png)

- **Begrænsning**: Forespørgslen kan overforbruge serverressourcer og blive udsat for begrænsning. I dette tilfælde returnerer forespørgslen følgende fejl: "Der blev anskaffet et token til kald af Finans og drift, men Finans og drift returnerede en fejl af typen 429". Yderligere oplysninger om begrænsning af Human Resources finder du i [Ofte stillede spørgsmål om begrænsning](./hr-admin-integration-throttling-faq.md).

  ![Fejltype 429 på HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a>Løsning

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a>Begrænse antallet af kolonner i dataforespørgslen

Med virtuelle tabeller er en af de metoder, der har det største potentiale til at forbedre forespørgselsydeevnen, at begrænse antallet af kolonner, der er valgt i forespørgslen. Den generelle vejledning til optimering af forespørgselsydeevnen er at begrænse de kolonner, der returneres i forespørgslen, til kun de egenskaber, du har brug for. Dette gælder især for kolonnerne med fremmede nøgler i virtuelle tabeller. Hvis du ikke har brug for værdierne i kolonnerne med den fremmede nøgle til integrationen eller rapporten, skal du strukturere forespørgslen, så du kun vælger de kolonner, du har brug for, og udelader kolonnerne med den fremmede nøgle.

#### <a name="selecting-columns-in-an-odata-query"></a>Vælge kolonner i en OData-forespørgsel

Når du forespørger på en virtuel tabel via Dataverse Web-API'en, kan du begrænse antallet af kolonner i forespørgslen ved at bruge indstillingen **$select**-systemforespørgsel og definere de kolonner, der skal returneres resultater for. Hvis du vil maksimere ydeevnen, skal du udelukke kolonner med fremmede nøgle (dem med **_mshr_FK_** som præfiks) fra forespørgslen.

Følgende forespørgsel på enheden **mshr_hcmworkerbaseentity** omfatter f.eks. kun de kolonner, der er medtaget i forespørgselsindstillingen **$select**, uden værdier for fremmed nøgle. Dette giver betydelige forbedringer af ydeevnen i forbindelse med en forespørgsel, der omfatter alle tabelkolonner.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Anbefalingen om at begrænse antallet af valgte kolonner gælder også, når du bruger indstillingen **$expand** til at udvide forespørgslen til relaterede virtuelle tabeller ved hjælp af navigationsegenskaber. Følgende forespørgsel indeholder f.eks. kolonner fra enheden **mshr_hcmworkerbaseentity** med udvidede kolonner fra enheden **mshr_dirpersonentity**. Bemærk, at forespørgselsindstillingen **$select** også er medtaget i forespørgselsindstillingen **$expand**.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Når du bruger denne metode til at hente data med forespørgselsindstillingen **$select** i forespørgselsklausulen **$expand**, vil du typisk få større forbedringer af ydeevnen, når navigationsegenskaben mellem enhederne er en mange til en-relation. Du oplever måske ikke samme fald i udførelsestiden af forespørgsler, når en én til mange-relation udvides. Du kan finde flere oplysninger om relationsdefinition til Dataverse-virtuelle tabeller i [Tabelrelationer](/powerapps/maker/data-platform/create-edit-entity-relationships).

Yderligere oplysninger om brug af indstillingerne **$select** og **$expand** til systemforespørgslen i Dataverse Web-API'en finder du i [Hente relaterede enhedsposter med en forespørgsel](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).

#### <a name="selecting-columns-in-power-bi"></a>Vælge kolonner i Power BI

Hvis du oplever en eller flere af de ovennævnte tegn på, at ydeevnen er langsom, når du opbygger en Power BI-rapport mod en Dataverse-virtuel tabel, kan du forbedre ydeevnen ved at udelukke kolonner med fremmed nøgle fra de kolonner, der er valgt i tabellen til rapporten. Hvis du f.eks. bruger Power BI Desktop til at oprette en rapport i forhold til enheden **mshr_hcmworkerbaseentity**, kan du bruge følgende trin til at vælge de kolonner, du vil have medtaget i rapportforespørgslen.

1. I Power BI Desktop skal du vælge **Mere...** på rullelisten **Hent data** på handlingsbåndet.
2. I vinduet **Hent data** skal du angive **Common Data Service** i søgefeltet, vælge connectoren **Common Data Service** og vælge **Opret forbindelse**.
3. Angiv organisationens URI for dit Dataverse-miljø i feltet **URL-adresse til serveren** i Common Data Service-vinduet, og vælg **OK**.
  
   ![Angiv URI'en for dit Dataverse-miljø.](./media/PowerBIDataverseURLSetup.png)
  
4. Udvid **Enheder**-noden i vinduet Navigator.
5. I søgefeltet skal du angive **mshr_hcmworkerbaseentity** og vælge enheden.
6. Vælg **Transformer data**.
7. Vælg **Avanceret editor** i vinduet Power Query-editor.
8. Opdater forespørgslen i vinduet **Avanceret editor**, så den ligner nedenstående, og tilføj eller fjern eventuelle kolonner til matrixen, hvis det er nødvendigt.

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Opdatere forespørgslen i Avanceret editor til Power Query-editor.](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. Vælg **Udført**.

   > [!NOTE]
   > Hvis du tidligere har modtaget en fejl af typen 429 fra forespørgslen før opdateringen, skal du muligvis vente, indtil gentagelsesperioden opdaterer forespørgslen, før den fuldføres.

10. Klik på **Luk og anvend** på handlingsbåndet i Power Query-editor.

Derefter kan du begynde at opbygge Power BI-rapporten i forhold til de kolonner, der er valgt fra den virtuelle tabel.

#### <a name="selecting-columns-in-power-apps"></a>Vælge kolonner i Power Apps

Ligesom med Dataverse Web-API-forespørgsler og Power BI kan du forbedre forespørgslens ydeevne for Power Apps baseret på Dataverse-virtuelle tabeller ved at udelukke kolonner fra relaterede tabeller i din app. Hvis der er medtaget kolonner fra en relateret tabel på en side, vil den URL-adresse, der oprettes for anmodningen til hentning af dataene, indeholde egenskaber for fremmed nøgle for den relaterede tabel. Som i eksemplerne under [Vælge kolonner i en OData-forespørgsel](#selecting-columns-in-power-apps) ovenfor reducerer dette ydeevnen ved at forårsage yderligere dataopslag.

Du kan løse dette ved at validere, at der ikke er medtaget datafelter fra relaterede tabeller i nogen dataform i din Power App.

1. Vælg dataformen til skærmen i trævisningsruden.
2. Vælg **Rediger** på egenskaben **Felter** i **Egenskaber**-ruden.
3. Kontrollér i **Data**-ruden, at ingen af de valgte felter er felter i den virtuelle tabel for datakilden.

Hvis f.eks. et af de datafelter, der er medtaget på en side i appen, refererer til en anden tabel, f.eks. **ThisItem.Worker.Name**, hvor **Arbejder** er den relaterede tabel, er der et potentiale for reduceret ydeevne ved hentning af dataene.

Du kan bruge [Power Apps-overvågning](/powerapps/maker/monitor-overview) til at sikre, at det kun er de kolonner, du skal bruge, der medtages i forespørgslen for at hente dataene til Power App. Du kan få vist den URL-adresse, der er konstrueret til operationen getRows, for at sikre, at de kolonner, du har valgt til din app, er optimale, når du henter dataene.

![Bruge Power Apps-overvågning til at analysere getData-handlingen.](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a>Filtrering af dataforespørgslen

En anden metode til forbedring af ydeevnen under udførelse af forespørgsler er at begrænse antallet af poster, der returneres i forespørgselsresultaterne. Det kan du gøre ved at filtrere resultaterne for at sikre, at du kun får de poster, du har brug for.

Se [Filtrere resultater](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for at få flere oplysninger om filtrering af forespørgselsdata.

### <a name="limiting-the-page-size-of-the-query"></a>Begrænse sidestørrelsen af forespørgslen

Hvis du arbejder med store datasæt, kan du opdele forespørgselsresultater i flere sider ved at føje `odata.maxpagesize`-præferenceoverskriften til dataforespørgsler.

Du kan finde flere oplysninger om sideinddeling i [Angive det antal enheder, der skal returneres på en side](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).

## <a name="see-also"></a>Se også

- [Konfigurere virtuelle Dataverse-tabeller](hr-admin-integration-common-data-service-virtual-entities.md)
- [Ofte stillede spørgsmål om Human Resources virtuelle tabeller](hr-admin-virtual-entity-faq.md)
- [Ofte stillede spørgsmål om begrænsning](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
