# INSTRUCTIONS TO THE PARTICIPANTS

## Where to search and access the data?
Data can be downloaded directly from the following link: [TODO COMPLETE]
In order to facilitate search and the development of web-based solutions, we indexed the content on an Elastic Search instance. You can access it through the following endpoint and authentication token:
 - *Endpoint*: [https://cebele.ent.eu-central-1.aws.cloud.es.io:443/api/as/v1/engines/cebele/search](https://cebele.ent.eu-central-1.aws.cloud.es.io:443/api/as/v1/engines/cebele/search)
 - *Authentication token*: search-14oev2nyfrcdiz28t37aeiws

## What kind of data is available?
Data relates to multiple documents and resources related to apiculture. We indexed them into documents with the following fields:
 - ID: unique identifier.
 - challenge_desc: challenge description.
 - challenge_label: challenge label.
 - menu_hierarchy: menu hierarchy for a given web page.
 - number: a number assigned at the source MS Excel file.
 - source_type: source type, e.g., if it corresponds to a web page, some video resource, etc.
 - url: the URL where the resource can be accessed.

## API documentation
The data was indexed on ElasticSearch. Please check the [reference documentation](https://www.elastic.co/guide/en/app-search/current/api-reference.html) for code samples. Below we provide a CURL sample search, and a sample result.

### CURL example
    curl -X POST 'https://cebele.ent.eu-central-1.aws.cloud.es.io:443/api/as/v1/engines/cebele/search' -H 'Content-Type: application/json' -H 'Authorization: Bearer search-14oev2nyfrcdiz28t37aeiws' -d '{"query": "apiturizem"}'

### Sample result
    {
        "challenge_desc": "\"A. Geografska koordinata lokacije in tip \u010debelnjaka (Trikotnik - registrirani stacionarni",
        "challenge_label": "A",
        "menu_hierarchy": "(meni Domov / \u010cebelarstvo / Vzreja matic)",
        "number": "1",
        "source_type": "spletna stran",
        "url": "https://www.czs.si/content/D57"
    }

