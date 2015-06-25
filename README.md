# Guild-Wars-2-API-Explorer
Small project to get a nice looking documentation going.

##Contribute
If you find outdated info, want to add new stuff, have some improvements to make go ahead or just [create an issue](https://github.com/Keeky/Guild-Wars-2-API-Explorer/issues/new). The data is stored in `data.json`. It's structured like this:
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
				["<editable - bool>", "<method - post, header etc>", "<key>", "<type - int, string etc>", "<required - Yes, No>", "<description>"]
			],
			"responseData": [
				["<key>", "<type - int, string etc>", "<description>"]
			]
		}
	}
}
```
Might seem like a really strange and confusing way to do things, but for me it's very easy to maintain. Note that the file that generates everything from `data.json` is not in this git.
