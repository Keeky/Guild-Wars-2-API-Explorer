# Guild-Wars-2-API-Explorer
[https://keeky.github.io/Guild-Wars-2-API-Explorer/](https://keeky.github.io/Guild-Wars-2-API-Explorer/)

Small project to get a nice looking and interactive documentation going. Ideas, contributions, corrections etc are greatly appreciated. You can contact me directly on GitHub or ingame as Keeky.4102

##Contribute
If you find outdated info, want to add new stuff or have some improvements to make go ahead. Or simply [create an issue](https://github.com/Keeky/Guild-Wars-2-API-Explorer/issues/new). The data is stored in `data.json`. It's structured like this:
```json
{
	"<category>": {
		"v<version>-<name>": {
			"name": "<name>",
			"bubbles": ["<v1, v2, key>"],
			"description": "<description>",
			"baseUrl": "https://api.guildwars2.com/v2/<base link>",
			"specialInterfaces": "<some html>",
			"requestData": [
				["<editable - true or false>", "<method - get, post, header etc>", "<query key>", "<type - int, string etc>", "<required - Yes or No>", "<description>"]
			],
			"responseData": [
				["<key>", "<type - int, string etc>", "<description>"]
			]
		}
	}
}
```
`<category>` Name of the category. For the navigation on the left.

`v<version>-<name>` To generate the directlink used in the navigation. For the URL `-` gets replaced with `/`. As an example `v2-account-bank`

`<name>` The name actually displayed in the navigation and as headline.

`bubbles` Visible beside the headline. Currently there are only `v1` and `v2` to show the version of the endpoint and `key` To show that an endpoint requires a valid API key.

`description` Pretty self-explanatory...

`baseUrl` The url of the endpoint without any queries or 2nd level endpoints. Note that this value is used to make example requests.

`specialInterfaces` Shows up above the example request after the 'Use this endpoint' button is clicked. Can be used to add some input elements if the default input elements aren't enough to properly interact with the API. For an example see commerce/transactions.

`requestData` The first table generates from this. There are a few premade rows you can use. `["Auth"]` if the endpoints need an api key, `["Page"]` for pagination if it's available for the API and `["Language"]` if the API results can be localized.

`responseData` Pretty much the same as above just way simpler...

Might seem like a really strange and confusing way to do things, but for me it's very easy to maintain. And hey, it works. Note that the file that generates everything from `data.json` is not in this git.
