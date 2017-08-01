# gid-curate-concept

A data component to curate concept

    <gid-curate-concept conceptId='1' userId='1'></<gid-curate-concept>

API endpoint:

    PUT /concepts/{id}/curate

Input:

- User Id (Query Param)

- Concept Id (URL Param)

- ~~List of recommended applications to start with~~

- Trigger that user has switched from define to explore

- Explicit yes or no on most of the synonyms, patterns and related concepts

- Explicit yes or no on most of the example columns and some of the example values

- ~~Search string for synonyms, patterns or related concepts~~

Sample Input: (as JSON payload)

    {
        "synonyms":[
            {"id":"100052","verified":"Y"},
            {"id":"100051","verified":"Y"},
        ],
        "patterns":[
            {"id":"100152","verified":"Y"},
            {"id":"100151","verified":"Y"},
        ],
        "relatedConcepts":[
            {"id":"100052","verified":"Y"},
            {"id":"100051","verified":"Y"},
        ],
        "exampleValues":[
            {"id":"100052","verified":"Y"},
            {"id":"100051","verified":"Y"},
        ],
        "exampleColumns":[
            {"id":"100052","verified":"Y"},
            {"id":"100051","verified":"Y"},
        ],
    }

Output:
- ~~5 synonyms (with likelihood)~~
- ~~5 patterns (with likelihood)~~
- ~~5 related concepts (with likelihood)~~

- list of 10 example columns and 100 example values (prioritised by relevance)

- output 2 + revised list of synonyms, patterns and related concepts 

- ~~search results~~
