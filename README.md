# wildPokemonGenerator

A static web app that generates randomized **wild encounter** BBCode for a forum, based on a Pokémon type.

Pick a type, choose how many spawns and the tags, optionally enable **Monthly Bonus**
(adds an italic 5th move drawn from the Egg Move pool when available), then copy the
generated BBCode straight into your post.

## How it works

Everything runs in the browser — there is **no server**. The page calls the public
[PokeAPI](https://pokeapi.co/) directly with `fetch` and caches responses in
`localStorage` to stay within PokeAPI's fair-use policy. All generation logic lives in
`index.html`.

## Hosting on GitHub Pages

This repo is a GitHub **user site** (`<username>.github.io`), so:

1. Commit `index.html` to the root of the `main` branch.
2. In **Settings → Pages**, set the source to `main` / root (if not already).
3. Visit `https://<username>.github.io/`.

No build step, no dependencies, no server.

## Local preview

Just open `index.html` in a browser, or serve the folder with any static file server,
e.g. `npx serve` or `python -m http.server`.
