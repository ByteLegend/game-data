# Data/translation repository for the ByteLegend programming game

## What is ByteLegend

[ByteLegend](https://bytelegend.com) is a free, open-source MMORPG game where you acquire real-world, high-paying programming skills.

## Welcome

Thank you for your interest in contributing to ByteLegend. This repository is specifically for text data and translations but we assume you're already familiar with the [main readme](https://github.com/ByteLegend/ByteLegend/blob/master/README.md) and the [contributors' guide](https://github.com/ByteLegend/ByteLegend/blob/master/docs/en/CONTRIBUTING.md).

## How the files work

In this repo you'll spend most of your attention on the [YAML-format](https://en.wikipedia.org/wiki/YAML) `.yml` files which contain the human-entered text, in multiple languages where available.
As of December 2021, this is mostly English (`EN`) and Simplified Chinese (`ZH_HANS`).
These manually added strings are then either used verbatim in the game or translated automatically to other languages, as chosen by the player.

Automatic translation uses Google Translate API, while the [JSON-format](https://en.wikipedia.org/wiki/JSON) `.json` files, you see in this repo, serve as cache for the translated strings so that the game doesn't make unnecessary API calls.
You typically should not find any need to update the `.json` files directly.

If you'd like to contribute manual translations of languages not yet present for a given string in the `.yml` files, please see [here](https://github.com/ByteLegend/ByteLegend/blob/master/docs/en/i18n.md#add-a-new-language).

Files are grouped into directories by in-game locations for easier traversal.

## Release and deployment

Your changes will be visible in the game once the developers compile and deploy a new release.