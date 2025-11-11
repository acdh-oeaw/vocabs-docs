# Vocabulary check

## Automated checks

- Validate the TTL file
  - For example, using the [TTL Validator](https://github.com/IDLabResearch/TurtleValidator) developed by IDLab – Ghent University

- Run through [qSKOS](https://github.com/cmader/qSKOS) (`java -jar qSKOS-cmd.jar analyze -dc mil,bl vocabulary_name.ttl -o report_name`)
  - Instructions on [how to install it locally](https://github.com/cmader/qSKOS?tab=readme-ov-file#local-installation-)
  - There is also an online [testing tool](https://skos-play.sparna.fr/skos-testing-tool/) in SKOS Play! (but it is sometimes down)

- Run through [Skosify](https://github.com/NatLibFi/Skosify)

## Prefixes

- Check if all the prefixes are actually used
- Check if the abbreviation corresponds the given URI according to [prefix.cc](http://prefix.cc)
    - If not, propose the abbreviation used by [prefix.cc](http://prefix.cc)
- Check if the abbreviation exists in [prefix.cc](http://prefix.cc)
    - If not, look for the URI in [prefix.cc](http://prefix.cc) and propose the corresponding abbreviation
- List cases not covered by [prefix.cc](http://prefix.cc) and go through them manually
    - In particular, check if URIs use the http or https protocol
    - Check if there is a trailing slash or anchor at the end of the URI

## Overview

- What classes are used?
    - If there is a class which is not part of the SKOS model, explore why it is used
- What properties are used?
    - Are there lesser used properties?
    - Are there properties from models we would not expect?
- Which properties are present when describing the instances of the different classes? (coverage)

## General vocabulary metadata

- Are all languages declared here actually used?

## Multiple concept schemes

- How many concept schemes are declared in the vocabulary?
- Are all these concept schemes objects of `skos:inScheme` properties?
- Are there concepts or collections belonging to more than one concept scheme?

## Identifiers

- What form do the identifiers take?
    - Numerical
        - Do they have a consistent number of digits?
        - Do they start from 0?
        - Are there any gaps?
    - Alpha-numerical
    - Derived from labels
        - Is a specific orthographic convention used (for example, camelCase)?
        - Is this convention consistently used?

## Literals (labels, definitions, notes…)

- Are language tags given for all literals?
- Do language tags indicated for literals correspond to the language(s) given in the general vocabulary metadata?
- Do they follow a single spelling convention (for example, US or UK or Oxford English)?
- Do they follow some capitalization rules?
- Do they follow a rule about whether to put a full stop at the end?
- Are there any double whitespaces?
- Do they contain typos?
- Do they contain grammatical errors?
- Are there any inconsistencies in hyphenation?

## Comments

- Are there any comments in the file?
- Should these be simply deleted or should we transform them into notes according to the SKOS model?

## Labels

- Are they expressed as a singular or plural form? Is this consistently applied?

## Definitions (in particular)

- Are definitions given for each concept?
- Do they repeat the label of the concept at the beginning?
- Do they use the same verb form (infinitive, *-ing* form,…)?

## Sources

- Are indications of sources contained in the definition itself?
- Is there a `dc:source` property?
- Are versions included for Wikipedia pages?
- Are sources cited in all cases?

## References to external resources

- Are there any broken links?
- Do URIs point to the correct resources?
- Do Wikidata URIs have the correct form?
- Do Getty URIs have the correct form?

## Collections

- Are collections used?