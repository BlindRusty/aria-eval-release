# aria-eval-release

    Team name :Independent Research
    Organization / Entity name : KRISHNENDU DASGUPTA SOLE PROPRIETORSHIP
    Author : Krishnendu Dasgupta
    From : Bengaluru, India

    RELEASE VERSION :CURRENT

## Hardware Description

The underlying hardware used for this experiment evaluation is as follow : 

### System Name and Provider 

    System Name : JOHNAIC-3
    System Provider : VON-NEUMANN AI
    System Provider Location : Bengaluru, Karnataka

### System Configuration 

    CPU - Intel i5 12400 
    GPU - Intel Arc A770 
    RAM - 64 GB 
    VRAM - 16 GB 
    STORAGE - 1 TB SSD


## Submission for NIST-ARIA evaluation across 3 scenarios

As per directives, the code follows the same structure of **AriaDialogAPI** base.         

    Evaluation Scenarios : 
        Meal Planner 
            v1.1 [ Ready for testing ] as on 03.10.2024
        Movie Spoilers
            v0.01 [ In Build ] as on 03.10.2024
        Path Finders
            v0.01 [ In Build ] as on 03.10.2024

### Implementation Type : 
    Multi Class Inheritance from Base Class AriaDialogAPI

### Meal Planning 

This section covers all important details for Meal Planning Scenario.

#### This is the section for guardrails for Meal Planning 
        
Implemented as per AI Risk Management Framework: Generative Artificial Intelligence Profile.        

        Meal Planning - Foodie's Friend

        1. Allergy Controls 
        2. Dietary Restrictions
        3. Dietary Preferences
        4. Indirect restrcitions from Medicines and Illnesses
        5. Calories Calculations
        6. Focused Context for Meal Planning usecase only. 

#### This is the section for Additional Information Retrieval for Meal Planning 

Additional Information Retrieval :

    Scenario : Meal Planning - Foodie's Friend

        Internet Search : to be made available in v2.01
            Optional - asked during OpenConnection Call
            parameter type: Optional

        Nearby Places using Google API : to be made available in v2.01
            Optional - asked during OpenConnection Call
            parameter type: Optional

        Food Nutrition Index and Values : to be made available in v2.01
            Primary - using Nutrition resources from NIH 
            parameter type: Mandatory

        Allergy Information : available in v1.1
            Primary - using Model Data and Guardrails
            parameter type: NA - Inbuilt

        Medicine Usage and Allergy Relation : tavailable in v1.1
            Primary - using Model Data and Guardrails
            parameter type: NA - Inbuilt
        
        Advanced Medicine Usage and Brand Understanding : to be made available in v2.01
            Primary - using NIH RxNorm
            parameter type: Optional

