# Data/translation repository for the ByteLegend programming game

## What is ByteLegend

[ByteLegend](https://bytelegend.com) is a free, open-source MMORPG game where you acquire real-world, high-paying programming skills.

## Welcome

Thank you for your interest in contributing to ByteLegend. This repository is specifically for text data and translations but we assume you're already familiar with the [main readme](https://github.com/ByteLegend/ByteLegend/blob/master/README.md) and the [contributors' guide](https://github.com/ByteLegend/ByteLegend/blob/master/docs/en/CONTRIBUTING.md).  

## How the files work

In this repo you'll spend most of your attention on the [YAML-format](https://en.wikipedia.org/wiki/YAML) `.yml` files which contain the human-entered text, in multiple languages where available.
As of December 2021, this is mostly English (`EN`) and Simplified Chinese (`ZH_HANS`).
These manually added strings are then either used verbatim in the game or translated automatically to other languages, as chosen by the player.
Automatic translation uses Google Translate API, while the [JSON-format](https://en.wikipedia.org/wiki/JSON) `.json` files serve as cache for the translated strings so that the game doesn't make unnecessary API calls.

If you compare an .yml file with a similarly-named .json file, you will find all strings from the .yml file in the .json file but the latter will have more translations.
These additional translations are generated automatically. This can be either through scripting triggered automatically by your PR being merged or executed manually by developers.
Either way, you don't have to worry about strings missing from the .json file as long as the structure of the file is valid.

What you have to keep in mind however is that there is currently a possibility that strings in the .yml file are updated but the corresponding cached values are not updated in the .json file.
As of December 2021, as contributions can still be managed manually, developers do try to catch such instances and regenerate the .json file themselves.

What you can do to help, which will be very helpful as the contributions get numerous, is - while updating the strings in the .yml file - to also remove all translations of that string from the .json file yourself.
This empties the cache for the corrected string and prompts the game to use the translation API for the new version of the text you contributed instead of using the previously cached value.

_**Note**, the developers currently prefer the contributors to focus on improving the text rather than being held up by the technicalities so if this process proves to be too complex for you, please contribute the changes in the .yml file and someone will take care of the rest.
Alternatively you can remove the entire .json file although this is generally discouraged from the point of view of git change history. The process will likely be simplified in the future._

If you'd like to contribute manual translations of languages not yet present for a given string in the .yml files, please see [here](https://github.com/ByteLegend/ByteLegend/blob/master/docs/en/i18n.md#add-a-new-language).

Files are grouped into directories by in-game locations for easier traversal.

## Example

First, an example of a `GitIsland/i18n.yml` edit. Note the `id` key _install-git-title_:
![GitIsland/i18n.yml edit example](/docs/images/translation-update-example-yml.png)

Then, how the above change would need to be reflected in the corresponding .json file, `GitIsland/i18n-auto.json` in this example:
![GitIsland/i18n.yml edit example](/docs/images/translation-update-example-json.png)
