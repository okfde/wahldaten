# Kandidierende

Kandidierende zur Bundestagswahl 2017 auf Landeslisten der Parteien und direkt in Wahlkreisen.
Derzeit berücksichtigt sind AfD, CDU, CSU, FDP, Grüne, Linke, SPD, soweit Daten vorhanden waren.

## Datenformat

JSON-Datenstruktur. `null` bedeutet immer, "keine Daten".

``` javascript

[{
	"id": "0123abcd",	// sha256($slug).toString(16).substr(-8)
	"slug": "peter-maier-abc-bb"	// slugify(forename-surname-party-state)
	"election": {
		"party": "abc",	// slugify(partei)
		"state": "bb",	// two letter code
		"list": 1,	// rank on state electoral list
		"district": 1,	// candidate in electoral district (integer, no leading zeros)
		"mandate": "b", // e: MdEP, b: MdB, l: MdL/MdA/MdHB/MdBB|MdMA (state)
		"lead": true	// 'spitzenkandidat_in' (spot 1 on list or otherwise)
	},
	"name": {
		"titles": "Dr.",	// all titles
		"forename": "Peter",	// all forenames as written by candidate
		"surname": "Meier",	// all surnames
		"affix": "jr."		// affixes if any
	},
	"aliases": [ // alternative writings, for matching, all lower case and no special characters
		"peter meier"
		"peter harry meier",
		"peter h meier",
		"harry peter meier"
	],
	"facts": { // this is extensible
		"gender": "m", // "m", "f", "x" or null
		"dateofbirth": "1970-01-01",
		"placeofbirth": "Musterhausen, Deutschland",
		"placeofresidence": "Musterhausen, Deutschland",
		"occupation": "Blafasel",
		"maritalstatus": true,
		"offspring": 2
	},
	"photos": [{
		"url": "https://petermeier.com/peter.jpg",
		"license": null,
		"author": "Peter Meier"
	}],
	"links": [{
		"type": "website",
		"url": "https://petermeier.com/"
	},{
		"type": "facebook",
		"id": "Peter.Meier",
		"url": "https://facebook.com/Peter.Meier"
	},{
		"type": "twitter",
		"id": "pmeier_",
		"url": "https://twitter.com/pmeier_"
	},{
		"type": "agw",
		"id": "peter-meier",
		"url": "https://www.abgeordnetenwatch.de/profile/peter-meier"
	},{
		"type": "wikipedia",
		"id": "Peter_Meier",
		"url": "https://de.wikipedia.org/wiki/Peter_Meier"
	},{
		"type": "bundestag",
		"id": "M/meier_peter/123456",
		"url": "http://www.bundestag.de/abgeordnete18/biografien/M/meier_peter/123456"
	}],
	"checked": false // everything has been checked by a human being
}]

```

## Updates

This file may be updated automatically.

## Sources

See [SOURCES.md](SOURCES.md).

## Author & License

This Data is made available under the [Open Database License](https://opendatacommons.org/licenses/odbl/).

Authors: 
	* [Yetzt](https://yetzt.me)
