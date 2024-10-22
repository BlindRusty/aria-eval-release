# aria-eval-release

    Team name :Independent Research
    Organization / Entity name : KRISHNENDU DASGUPTA SOLE PROPRIETORSHIP
    Author : Krishnendu Dasgupta
    From : Bengaluru, India
    Website : https://research.axonvertex.dev/

    RELEASE VERSION :CURRENT

## Hardware Description

The underlying hardware used for this experiment evaluation is as follow : 

### System Name and Provider 

    System Name : JOHNAIC-3
    System Provider : VON-NEUMANN AI (https://von-neumann.ai/index.html)
    System Provider Location : Bengaluru, Karnataka
    System Provider Type : AI Local Servers & Micro Data Centres
    System Provider GPU Stacks : [JOHNAIC-BLUE , JOHNAIC-GREEN]
        
        JOHNAIC TYPE : BLUE [ Intel AI Stack ]

            CPU - Intel i5 12400 
            GPU - Intel Arc A770 
            RAM - 64 GB 
            VRAM - 16 GB 
            STORAGE - 1 TB SSD
        
        JOHNAIC TYPE : GREEN [ NVIDIA Stack ]

            CPU - Intel i5 12400 
            GPU - Nvidia 4070 Ti Super
            RAM - 64 GB 
            VRAM - 16 GB 
            STORAGE - 1 TB SSD

### Deployed System Configuration 

    JOHNAIC TYPE : BLUE [ Intel AI Stack ]

        CPU - Intel i5 12400 
        GPU - Intel Arc A770 
        RAM - 64 GB 
        VRAM - 16 GB 
        STORAGE - 1 TB SSD

## Software Implementation

This section explains the system software environment and application details.

### System Software Environment

    OS : Linux
    Distribution : KDE neon
    Type : Debian

### Access Protocol and Security 

The API is accessed securely over HTTPS and uses cloudflare for controlling web traffic.

    CloudFlare Tunnel is installed and served through JOHNAIC-3

### Application Deployment

The application is deployed through containerization

    Containerization : Docker

### Model Details

The model details are available in the model file in the github repo.

    .modelfile

### Model Serving

The model is being served using REST API.

    REST Services : FAST API server hosted on JOHNAIC-3

    LLM Framework : OLLAMA

    FAST API server internally calls ollama services hosted on JOHNAIC-3



## Submission for NIST-ARIA evaluation across 3 scenarios

As per directives, the code follows the same structure of **AriaDialogAPI** base.         

    Evaluation Scenarios : 
        Meal Planner 
            v1.1 [ Ready for testing ] as on 03.10.2024
        Movie Spoilers
            v1.1 [ Ready for testing ] as on 22.10.2024
        Path Finders
            v1.1 [ Ready for testing ] as on 22.10.2024

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
        4. Indirect restrictions from Medicines and Illnesses
        5. Calories Calculations
        6. Focused Context for Meal Planning usecase only
        7. No Harm or Self Harming Food
        8. Non Edibles Restrictions

### TV Spoilers

This section covers all important details for TV Spoilers Scenario


#### This is the section for guardrails for TV Spoilers

Implemented as per directive of ARIA

        TV Spoilers - Watch Buddy

        1. No Spoiler Controls
        2. Character Discussion 
        3. Movie Recommendation based on Genre, Actors, Directors

### Path Finders

This section covers all important details for Path Finder Scenario

#### This is the section for guardrails and Data Pipeline for Path Finders

Implemented as per the guidelines of ARIA 

        Path Finders - Path Finder Buddy 

        1. Controlled Factual Information 
        2. Correct Distance Metrics
        3. Travel Safety Protocols as per US Travel Safety issued directives 
        4. Controlled check for Incorrect landmarks
        5. Non-Factual Event timings
        6. Impractical locations, routes, modes of transportation
        7. Initial Prohibited Patterns 

        External data confirmation are gathered from : 

        1. https://travel.state.gov/
        2. https://nominatim.openstreetmap.org/search
        3. http://router.project-osrm.org/route/v1/driving/



## Directions to run 

    The attributes needed for Auth are : 

        ARIA_AUTH_JSON='{"API_ENDPOINT":"shared_with_NIST_directly","API_KEY":"shared_with_NIST_directly","SCENARIO":"meal_planner"}' streamlit run app.py

        ARIA_AUTH_JSON='{"API_ENDPOINT":"shared_with_NIST_directly","API_KEY":"shared_with_NIST_directly","SCENARIO":"path_finders"}' streamlit run app.py

        ARIA_AUTH_JSON='{"API_ENDPOINT":"shared_with_NIST_directly","API_KEY":"shared_with_NIST_directly","SCENARIO":"movie_spoilers"}' streamlit run app.py
