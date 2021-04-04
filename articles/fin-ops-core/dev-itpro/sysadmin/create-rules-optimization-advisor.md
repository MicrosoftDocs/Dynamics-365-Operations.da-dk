---
title: Oprette regler for rådgivningsværktøj til optimering
description: I dette emne beskrives det, hvordan du føjer nye regler til rådgivningsværktøj til optimering.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: sericks
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 67e740a1e00c425f0e09b5f0fc960cf2778efd89
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568280"
---
# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="bd438-103">Oprette regler for rådgivningsværktøj til optimering</span><span class="sxs-lookup"><span data-stu-id="bd438-103">Create rules for Optimization advisor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd438-104">I dette emne forklares det, hvordan du oprette nye regler til **rådgivningsværktøj til optimering**.</span><span class="sxs-lookup"><span data-stu-id="bd438-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="bd438-105">Du kan for eksempel oprette en ny regel, der identificerer, hvilke tilbudsanmodninger (RFQ) der har en tom titel.</span><span class="sxs-lookup"><span data-stu-id="bd438-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="bd438-106">Brugen af titler på sager gør dem nemme at identificere og søge i.</span><span class="sxs-lookup"><span data-stu-id="bd438-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="bd438-107">Selv om det er ret enkelt, viser dette eksempel, hvad der kan opnås med optimeringsregler.</span><span class="sxs-lookup"><span data-stu-id="bd438-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="bd438-108">En *regel* er et check af programdata.</span><span class="sxs-lookup"><span data-stu-id="bd438-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="bd438-109">Hvis den betingelse, som reglen evaluerer, er opfyldt, oprettes der mulighed for at optimere processer eller forbedre data.</span><span class="sxs-lookup"><span data-stu-id="bd438-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="bd438-110">Der kan reageres på salgsmulighederne, og eventuelt kan virkningen af handlingerne måles.</span><span class="sxs-lookup"><span data-stu-id="bd438-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="bd438-111">Hvis du vil oprette en ny regel for **rådgivningsværktøjet til optimering**, skal du tilføje en ny klasse, som udvider den abstrakte **SelfHealingRule**-klasse, implementerer grænsefladen **IDiagnosticsRule** og dekoreres med attributten **DiagnosticRule**.</span><span class="sxs-lookup"><span data-stu-id="bd438-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="bd438-112">Klassen skal også have en metode, der er dekoreret med attributten **DiagnosticsRuleSubscription**.</span><span class="sxs-lookup"><span data-stu-id="bd438-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="bd438-113">Efter konventionen sker det på **opportunityTitle**-metoden, som beskrives senere.</span><span class="sxs-lookup"><span data-stu-id="bd438-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="bd438-114">Denne nye klasse kan føjes til en brugerdefineret model med en afhængighed af modellen **SelfHealingRules**.</span><span class="sxs-lookup"><span data-stu-id="bd438-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="bd438-115">I følgende eksempel kaldes den regel, der implementeres **RFQTitleSelfHealingRule**.</span><span class="sxs-lookup"><span data-stu-id="bd438-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```xpp
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="bd438-116">Den abstrakte **SelfHealingRule**-klasse indeholder abstrakte metoder, der skal implementeres ved nedarvning af klasser.</span><span class="sxs-lookup"><span data-stu-id="bd438-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="bd438-117">Kernen er metoden **evaluer**, der returnerer en liste over de salgsmuligheder, der er identificeret af reglen.</span><span class="sxs-lookup"><span data-stu-id="bd438-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="bd438-118">Salgsmuligheder kan være pr. juridisk enhed, eller de kan gælde for hele systemet.</span><span class="sxs-lookup"><span data-stu-id="bd438-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

```xpp
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

<span data-ttu-id="bd438-119">Den metode, der er vist ovenfor, laver løkker over firmaer og vælger sager med tilbudsanmodninger med tomme titler i metoden **findRFQCasesWithEmptyTitle**.</span><span class="sxs-lookup"><span data-stu-id="bd438-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="bd438-120">Hvis der findes mindst én sag af denne type, oprettes der en firmaspecifik salgsmulighed med metoden **getOpportunityForCompany**.</span><span class="sxs-lookup"><span data-stu-id="bd438-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="bd438-121">Bemærk, at feltet **Data** i tabellen **SelfHealingOpportunity** er af typen **Container** og derfor kan indeholde de data, der er relevante for den logik, der er specifik for denne regel.</span><span class="sxs-lookup"><span data-stu-id="bd438-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="bd438-122">Hvis **OpportunityDate** angives med det aktuelle tidsstempel, registreres tidspunktet for seneste evaluering af salgsmuligheden.</span><span class="sxs-lookup"><span data-stu-id="bd438-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="bd438-123">Salgsmuligheder kan også være på tværs af firmaer.</span><span class="sxs-lookup"><span data-stu-id="bd438-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="bd438-124">I så fald er løkken over regnskaber er ikke nødvendig, og salgsmuligheden skal oprettes med metoden **getOpportunityAcrossCompanies**.</span><span class="sxs-lookup"><span data-stu-id="bd438-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="bd438-125">Følgende kode viser metoden **findRFQCasesWithEmptyTitle**, der returnerer id'erne for de tilbudsanmodningsager, der har tomme titler.</span><span class="sxs-lookup"><span data-stu-id="bd438-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

```xpp
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

<span data-ttu-id="bd438-126">Der er to metoder til, der skal implementeres **opportunityTitle** og **opportunityDetails**.</span><span class="sxs-lookup"><span data-stu-id="bd438-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="bd438-127">Den første returnerer en forkortet titel for salgsmuligheden, mens den sidstnævnte returnerer en detaljeret beskrivelse af salgsmuligheden, som også kan også indeholde data.</span><span class="sxs-lookup"><span data-stu-id="bd438-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="bd438-128">Den titel, der returneres af **opportunityTitle** vises under kolonnen **Optimeringsmulighed** i arbejdsområdet **Rådgivningsværktøj til optimering**.</span><span class="sxs-lookup"><span data-stu-id="bd438-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="bd438-129">Den vises også som overskrift i den siderude, der viser yderligere oplysninger om salgsmuligheden.</span><span class="sxs-lookup"><span data-stu-id="bd438-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="bd438-130">Som regel er denne metode dekoreret med **DiagnosticRuleSubscription**-attributten, som tager følgende argumenter:</span><span class="sxs-lookup"><span data-stu-id="bd438-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="bd438-131">**Diagnoseområde** – en fasttekstværdi typen **DiagnosticArea**, der beskriver, hvilken del af programmet reglen hører til, f.eks. **DiagnosticArea::SCM**.</span><span class="sxs-lookup"><span data-stu-id="bd438-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="bd438-132">**Navn på regel** – en streng med navnet på reglen.</span><span class="sxs-lookup"><span data-stu-id="bd438-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="bd438-133">Dette vises under kolonnen **Navn på regel** i formularen **Valideringsregel i diagnosticering** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="bd438-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="bd438-134">**Kørselsfrekvens** – en fasttekst af typen **DiagnosticRunFrequency**, der beskriver, hvor ofte reglen skal køres, f.eks. **DiagnosticRunFrequency::Daily**.</span><span class="sxs-lookup"><span data-stu-id="bd438-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="bd438-135">**Beskrivelse af regel** – en streng med en mere detaljeret beskrivelse af reglen.</span><span class="sxs-lookup"><span data-stu-id="bd438-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="bd438-136">Dette vises under kolonnen **Regelbeskrivelse** i formularen **Valideringsregel i diagnosticering** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="bd438-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="bd438-137">Atrributten **DiagnosticRuleSubscription** er påkrævet, for at reglen fungerer.</span><span class="sxs-lookup"><span data-stu-id="bd438-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="bd438-138">Den anvendes typisk på **opportunityTitle**, men den kan dekorere enhver metode i klassen.</span><span class="sxs-lookup"><span data-stu-id="bd438-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="bd438-139">Nedenfor vises et eksempel på implementering.</span><span class="sxs-lookup"><span data-stu-id="bd438-139">The following is an example implementation.</span></span> <span data-ttu-id="bd438-140">For nemheds skyld bruges rå strenge, men en korrekt implementering kræver etiketter.</span><span class="sxs-lookup"><span data-stu-id="bd438-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

```xpp
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

<span data-ttu-id="bd438-141">Den beskrivelse, der returneres af **opportunityDetails**, vises i sideruden og indeholder yderligere oplysninger om salgsmuligheden.</span><span class="sxs-lookup"><span data-stu-id="bd438-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="bd438-142">Den tager argumentet **SelfHealingOpportunity**, som er et **Data**-felt, der kan bruges til at angive flere oplysninger om salgsmuligheden.</span><span class="sxs-lookup"><span data-stu-id="bd438-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="bd438-143">I eksemplet returnerer metoden id'erne for tilbudsanmodningssagerne med en tom titel.</span><span class="sxs-lookup"><span data-stu-id="bd438-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

```xpp
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

<span data-ttu-id="bd438-144">De to resterende abstrakte metoder, der skal implementeres, er **provideHealingAction** og **securityMenuItem**.</span><span class="sxs-lookup"><span data-stu-id="bd438-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="bd438-145">**provideHealingAction** returnerer sand, hvis der angives en reparationshandling, ellers returneres falsk.</span><span class="sxs-lookup"><span data-stu-id="bd438-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="bd438-146">Hvis sand returneres, skal metoden **performAction** implementeres, ellers udløses der en fejl.</span><span class="sxs-lookup"><span data-stu-id="bd438-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="bd438-147">Metoden **performAction** tager argumentet **SelfHealingOpportunity**, hvis data kan bruges til handlingen.</span><span class="sxs-lookup"><span data-stu-id="bd438-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="bd438-148">I eksemplet åbner handlingen **PurchRFQCaseTableListPage** til manuel rettelse.</span><span class="sxs-lookup"><span data-stu-id="bd438-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

```xpp
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

<span data-ttu-id="bd438-149">Afhængigt af de specifikke oplysninger for reglen, kan det være muligt at foretage en automatisk handling ved hjælp af salgsmulighedsdataene.</span><span class="sxs-lookup"><span data-stu-id="bd438-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="bd438-150">I dette eksempel kan systemet oprette titler til tilbudsanmodningssager automatisk.</span><span class="sxs-lookup"><span data-stu-id="bd438-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="bd438-151">**securityMenuItem** returnerer navnet på et handlingsmenupunkt på en sådan måde, at reglen er kun synlig for brugere, der kan få adgang til handlingsmenupunktet.</span><span class="sxs-lookup"><span data-stu-id="bd438-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="bd438-152">Sikkerhed kan kræve, at specifikke regler og salgsmuligheder kun er tilgængelige for autoriserede brugere.</span><span class="sxs-lookup"><span data-stu-id="bd438-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="bd438-153">I eksemplet er det kun brugere med adgang til **PurchRFQCaseTitleAction**. der kan få vist salgsmuligheden.</span><span class="sxs-lookup"><span data-stu-id="bd438-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="bd438-154">Bemærk, at dette handlingsmenupunkt blev oprettet til dette eksempel, og blev tilføjet som et indgangspunkt sikkerhedsrettigheden **PurchRFQCaseTableMaintain**.</span><span class="sxs-lookup"><span data-stu-id="bd438-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

> [!NOTE]
> <span data-ttu-id="bd438-155">Menupunktet skal være et handlingsmenupunkt, hvis sikkerheden skal fungere korrekt.</span><span class="sxs-lookup"><span data-stu-id="bd438-155">The menu item must be an action menu item for security to work correctly.</span></span> <span data-ttu-id="bd438-156">Andre menupunkttyper, f.eks. **Skærmmenupunkter**, fungerer ikke korrekt.</span><span class="sxs-lookup"><span data-stu-id="bd438-156">Other menu item types, such as **Display menu items** will not work correctly.</span></span>

```xpp
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="bd438-157">Når reglen er kompileret, udføres det efterfølgende job for at få det vist i brugergrænsefladen (UI).</span><span class="sxs-lookup"><span data-stu-id="bd438-157">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

```xpp
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

<span data-ttu-id="bd438-158">Reglen vises i formularen **Valideringsregel i diagnosticering**, der er tilgængelige fra **Systemadministration** > **Periodiske opgaver** > **Bevar valideringsregel i diagnosticering**.</span><span class="sxs-lookup"><span data-stu-id="bd438-158">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="bd438-159">For at få den evalueret, skal du gå til **Systemadministration** > **Periodiske opgaver** > **Planlæg valideringsregel i diagnosticering** og vælg frekvensen for reglen, f.eks. **Daglig**.</span><span class="sxs-lookup"><span data-stu-id="bd438-159">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="bd438-160">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd438-160">Click **OK**.</span></span> <span data-ttu-id="bd438-161">Gå til **Systemadministration** > **Rådgivningsværktøj til optimering** for at få vist den nye salgsmulighed.</span><span class="sxs-lookup"><span data-stu-id="bd438-161">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="bd438-162">Følgende eksempel er et kodestykke med skelettet til en regel, herunder alle de nødvendige metoder og attributter.</span><span class="sxs-lookup"><span data-stu-id="bd438-162">The following example is a code snippet with the skeleton of a rule including all the required methods and attributes.</span></span> <span data-ttu-id="bd438-163">Det hjælper dig med at komme i gang med at skrive nye regler.</span><span class="sxs-lookup"><span data-stu-id="bd438-163">It helps you get started with writing new rules.</span></span> <span data-ttu-id="bd438-164">De etiketter og handlingsmenupunkter, der bruges i eksemplet, bruges kun til demonstrationsformål.</span><span class="sxs-lookup"><span data-stu-id="bd438-164">The labels and action menu items that are used in the example are only used for demonstration purpose.</span></span>

```xpp
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

<span data-ttu-id="bd438-165">Du kan få flere oplysninger ved at se den korte YouTube-video: [Optimeringsrådgiver i Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span><span class="sxs-lookup"><span data-stu-id="bd438-165">For more information, watch the short YouTube video: [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]