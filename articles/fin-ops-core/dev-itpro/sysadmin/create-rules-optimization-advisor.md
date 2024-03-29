---
title: Oprette regler for rådgivningsværktøj til optimering
description: Denne artikel beskriver, hvordan du føjer nye regler til rådgivningsværktøj til optimering.
author: kamaybac
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.author: kamaybac
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: SelfHealingWorkspace
ms.openlocfilehash: a4addc98e3d5496bc8d2fafb3918931da876739f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273911"
---
# <a name="create-rules-for-optimization-advisor"></a>Oprette regler for rådgivningsværktøj til optimering

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du oprette nye regler til **rådgivningsværktøj til optimering**. Du kan for eksempel oprette en ny regel, der identificerer, hvilke tilbudsanmodninger (RFQ) der har en tom titel. Brugen af titler på sager gør dem nemme at identificere og søge i. Selv om det er ret enkelt, viser dette eksempel, hvad der kan opnås med optimeringsregler. 

En *regel* er et check af programdata. Hvis den betingelse, som reglen evaluerer, er opfyldt, oprettes der mulighed for at optimere processer eller forbedre data. Der kan reageres på salgsmulighederne, og eventuelt kan virkningen af handlingerne måles. 

Hvis du vil oprette en ny regel for **rådgivningsværktøjet til optimering**, skal du tilføje en ny klasse, som udvider den abstrakte **SelfHealingRule**-klasse, implementerer grænsefladen **IDiagnosticsRule** og dekoreres med attributten **DiagnosticRule**. Klassen skal også have en metode, der er dekoreret med attributten **DiagnosticsRuleSubscription**. Efter konventionen sker det på **opportunityTitle**-metoden, som beskrives senere. Denne nye klasse kan føjes til en brugerdefineret model med en afhængighed af modellen **SelfHealingRules**. I følgende eksempel kaldes den regel, der implementeres **RFQTitleSelfHealingRule**.

```xpp
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

Den abstrakte **SelfHealingRule**-klasse indeholder abstrakte metoder, der skal implementeres ved nedarvning af klasser. Kernen er metoden **evaluer**, der returnerer en liste over de salgsmuligheder, der er identificeret af reglen. Salgsmuligheder kan være pr. juridisk enhed, eller de kan gælde for hele systemet.

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

Den metode, der er vist ovenfor, laver løkker over firmaer og vælger sager med tilbudsanmodninger med tomme titler i metoden **findRFQCasesWithEmptyTitle**. Hvis der findes mindst én sag af denne type, oprettes der en firmaspecifik salgsmulighed med metoden **getOpportunityForCompany**. Bemærk, at feltet **Data** i tabellen **SelfHealingOpportunity** er af typen **Container** og derfor kan indeholde de data, der er relevante for den logik, der er specifik for denne regel. Hvis **OpportunityDate** angives med det aktuelle tidsstempel, registreres tidspunktet for seneste evaluering af salgsmuligheden.  

Salgsmuligheder kan også være på tværs af firmaer. I så fald er løkken over regnskaber er ikke nødvendig, og salgsmuligheden skal oprettes med metoden **getOpportunityAcrossCompanies**. 

Følgende kode viser metoden **findRFQCasesWithEmptyTitle**, der returnerer id'erne for de tilbudsanmodningsager, der har tomme titler.

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

Der er to metoder til, der skal implementeres **opportunityTitle** og **opportunityDetails**. Den første returnerer en forkortet titel for salgsmuligheden, mens den sidstnævnte returnerer en detaljeret beskrivelse af salgsmuligheden, som også kan også indeholde data.

Den titel, der returneres af **opportunityTitle** vises under kolonnen **Optimeringsmulighed** i arbejdsområdet **Rådgivningsværktøj til optimering**. Den vises også som overskrift i den siderude, der viser yderligere oplysninger om salgsmuligheden. Som regel er denne metode dekoreret med **DiagnosticRuleSubscription**-attributten, som tager følgende argumenter: 

* **Diagnoseområde** – en fasttekstværdi typen **DiagnosticArea**, der beskriver, hvilken del af programmet reglen hører til, f.eks. **DiagnosticArea::SCM**. 

* **Navn på regel** – en streng med navnet på reglen. Dette vises under kolonnen **Navn på regel** i formularen **Valideringsregel i diagnosticering** (**DiagnosticsValidationRuleMaintain**). 

* **Kørselsfrekvens** – en fasttekst af typen **DiagnosticRunFrequency**, der beskriver, hvor ofte reglen skal køres, f.eks. **DiagnosticRunFrequency::Daily**. 

* **Beskrivelse af regel** – en streng med en mere detaljeret beskrivelse af reglen. Dette vises under kolonnen **Regelbeskrivelse** i formularen **Valideringsregel i diagnosticering** (**DiagnosticsValidationRuleMaintain**). 

> [!NOTE]
> Atrributten **DiagnosticRuleSubscription** er påkrævet, for at reglen fungerer. Den anvendes typisk på **opportunityTitle**, men den kan dekorere enhver metode i klassen.

Nedenfor vises et eksempel på implementering. For nemheds skyld bruges rå strenge, men en korrekt implementering kræver etiketter. 

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

Den beskrivelse, der returneres af **opportunityDetails**, vises i sideruden og indeholder yderligere oplysninger om salgsmuligheden. Den tager argumentet **SelfHealingOpportunity**, som er et **Data**-felt, der kan bruges til at angive flere oplysninger om salgsmuligheden. I eksemplet returnerer metoden id'erne for tilbudsanmodningssagerne med en tom titel. 

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

De to resterende abstrakte metoder, der skal implementeres, er **provideHealingAction** og **securityMenuItem**. 

**provideHealingAction** returnerer sand, hvis der angives en reparationshandling, ellers returneres falsk. Hvis sand returneres, skal metoden **performAction** implementeres, ellers udløses der en fejl. Metoden **performAction** tager argumentet **SelfHealingOpportunity**, hvis data kan bruges til handlingen. I eksemplet åbner handlingen **PurchRFQCaseTableListPage** til manuel rettelse. 

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

Afhængigt af de specifikke oplysninger for reglen, kan det være muligt at foretage en automatisk handling ved hjælp af salgsmulighedsdataene. I dette eksempel kan systemet oprette titler til tilbudsanmodningssager automatisk. 

**securityMenuItem** returnerer navnet på et handlingsmenupunkt på en sådan måde, at reglen er kun synlig for brugere, der kan få adgang til handlingsmenupunktet. Sikkerhed kan kræve, at specifikke regler og salgsmuligheder kun er tilgængelige for autoriserede brugere. I eksemplet er det kun brugere med adgang til **PurchRFQCaseTitleAction**. der kan få vist salgsmuligheden. Bemærk, at dette handlingsmenupunkt blev oprettet til dette eksempel, og blev tilføjet som et indgangspunkt sikkerhedsrettigheden **PurchRFQCaseTableMaintain**. 

> [!NOTE]
> Menupunktet skal være et handlingsmenupunkt, hvis sikkerheden skal fungere korrekt. Andre menupunkttyper, f.eks. **Skærmmenupunkter**, fungerer ikke korrekt.

```xpp
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

Når reglen er kompileret, udføres det efterfølgende job for at få det vist i brugergrænsefladen (UI).

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

Reglen vises i formularen **Valideringsregel i diagnosticering**, der er tilgængelige fra **Systemadministration** > **Periodiske opgaver** > **Bevar valideringsregel i diagnosticering**. For at få den evalueret, skal du gå til **Systemadministration** > **Periodiske opgaver** > **Planlæg valideringsregel i diagnosticering** og vælg frekvensen for reglen, f.eks. **Daglig**. Klik på **OK**. Gå til **Systemadministration** > **Rådgivningsværktøj til optimering** for at få vist den nye salgsmulighed. 

Følgende eksempel er et kodestykke med skelettet til en regel, herunder alle de nødvendige metoder og attributter. Det hjælper dig med at komme i gang med at skrive nye regler. De etiketter og handlingsmenupunkter, der bruges i eksemplet, bruges kun til demonstrationsformål.

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

Du kan få flere oplysninger ved at se den korte YouTube-video: [Optimeringsrådgiver i Dynamics 365 Finance](https://www.youtube.com/watch?v=MRsAzgFCUSQ)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
