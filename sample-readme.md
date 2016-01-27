#Sample Readme

Demonstrates a generic structure for take-home coding challenge readmes.

## Usage

## Dependencies
This guide is intended for *nix systems. Following it requires the `http-server` node package, which in turn requires Node.js. Installation instructions for these tools are available on the websites of [Node.js](https://nodejs.org/) and [http-server](https://www.npmjs.com/package/http-server), respectively.


## Design Notes

### Non-instant Search
Instant search is not a good choice for the main search functionality that hits the api. Because the api often takes a noticible a few seconds to return results, searching instantly (as the user types each character) could be slow. Also, the api treats search input as full words.  For example, title-searching "reme" yeilds results with titles containing the word "reme" but not "remember".  

"Narrow by..." fields, on the other hand, do narrow the search results instantly. This is feasible because "Narrow by..." fields don't make new requests to the api. 

### Number of Results Displayed
The api returns 10 results at a time, so the max number of results that will currently show up is 10. There could easily be hundreds of actual matches.  If all were returned, paging the results might be useful. As it stands, the 10 result limit makes it harder to find a desired record (at least by partial title) because it may not be among the chosen 10 results. Allowing users access to api's "year" and "type" search fields would make it more likely that the desired record appeared among the results returned. 

### Human-Readable URLs
While the database IDs returned by the api are not great film identifiers for humans, they are the most convenient unique ones available from the data. Human-readable urls could be achieved with 

### Needs Styling
Enough said.

## Acknowledgements
[Angular's phone catalog tutorial](https://github.com/angular/angular-phonecat) was used for the base file structure for this project and was among references consulted during development.

## Contact
Please send any feedback to <b.g.veenstra@gmail.com>.
