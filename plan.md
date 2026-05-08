# Plan: A Differentiated Geospatial Foundation Models Repo

## Honest diagnosis

None of the existing awesome-lists help you actually *do* anything. They're flat indexes. You search them with Ctrl+F, click an arXiv link, and you're back where you started: "okay, but which model do I actually use, and how?"

Here's where the real gaps are, ordered roughly from "easy to build, immediate value" to "harder but more differentiating":

---

## 1. Structured, queryable metadata instead of markdown

Every awesome-list flattens models into prose bullets. Nobody can answer "show me models trained on SAR+optical, under 1B params, Apache-2.0, that support Sentinel-2 out of the box." The REMSA paper built RS-FMD precisely because this didn't exist.

A YAML/JSON schema per model (modalities, GSD range, params, license, pretraining data, supported tasks, hardware to fine-tune) with a small filter UI would already beat every existing list. This is the foundation everything else builds on.

## 2. Practical numbers papers don't report

Things every practitioner needs and no awesome-list has:

- VRAM to fine-tune at batch size 1
- Inference latency on a typical tile
- Embedding dimension
- Whether it actually runs without source-code surgery
- COG/STAC compatibility
- What breaks if you give it 6 bands instead of 13

You can populate this by actually running the models — which most list-maintainers don't.

## 3. Minimal working notebooks, one per model, on the same input

Pick one Sentinel-2 scene and one NAIP tile. For every model in your repo, ship a 30-line notebook that loads weights and produces embeddings or predictions on those exact tiles.

Suddenly your repo is the fastest way for anyone to try 10 models in an afternoon. TorchGeo does fragments of this; nobody does it comprehensively.

## 4. Head-to-head on a common downstream task

Paper-reported numbers are incomparable — different splits, different metrics, different preprocessing. Pick 2–3 standard tasks (say, EuroSAT classification, Sen1Floods11 segmentation, a change-detection dataset), fine-tune every model with the same recipe, publish the table.

PANGAEA is the closest thing and it's still not comprehensive. Independent, reproducible numbers are rare and valuable.

## 5. Pre-computed embeddings as fixtures

AlphaEarth ships pre-computed embeddings on Earth Engine and that's why it's getting traction. You could ship embeddings from 8–10 models on a fixed set of AOIs (a few cities, a forest, a coastline, a desert) as a downloadable artifact.

People can immediately do similarity search, clustering, transfer experiments without ever loading a model. This alone would get you cited.

## 6. Failure-mode and robustness notes

REOBench showed VLM GeoFMs lose 20%+ accuracy under corruption. Where does each model break?

- Cloud cover?
- Off-nadir angles?
- Geographic shift (model trained on Europe, tested on Sahel)?

This information exists scattered in paper appendices or doesn't exist at all. Documenting it is real work but uniquely useful.

## 7. Freshness and reproduction status

Awesome-lists rot. Add a CI job that pings each repo monthly, checks if weights still load, flags stale or broken entries.

Add a "reproduction status" column: independently verified / authors only / unverified. The signal-to-noise difference vs. a static list is huge.

## 8. Decision-tree / "which model" flow

A small interactive page (or even just a flowchart in the README):

> What's your input modality? → What's your task? → How much labeled data? → How much compute? → here are 3 candidates, here's why.

This is what REMSA automated with an LLM, but a hand-built tree is honest and faster for users who already know what they want.

---

## The bet

If I had to pick one bet: **#1 + #3 + #5 together**.

Structured metadata + minimal notebooks + pre-computed embedding fixtures. That's a repo where the README is two paragraphs and a search bar, and within five minutes someone can be running similarity search across Prithvi, Clay, and Galileo embeddings on the same scene.

Nobody has that. It's also achievable solo over a few weekends because each piece scales independently — you can ship 5 models and add more.

## What to avoid

Don't try to out-comprehensive the existing lists. They already cover everything. Be *useful* on a smaller set instead.
