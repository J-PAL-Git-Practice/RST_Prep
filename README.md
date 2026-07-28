# RST AI API Lab

Materials for the Research Staff Training lab on programmatically calling an LLM API to
extract structured data.

The lab notebook is `RST_SA_26_AI_API_Lab.ipynb`. `[MAKE_A_COPY]_RST_SA_25_AI_API_Lab.ipynb`
is last year's Google Colab version, kept for reference.

## Setup

You need [uv](https://docs.astral.sh/uv/) installed. Then, from this directory:

```sh
uv sync                  # install the pinned environment
cp .env.example .env     # then open .env and paste in your Anthropic API key
uv run jupyter lab       # opens JupyterLab in your browser
```

Open `RST_SA_26_AI_API_Lab.ipynb` and run the cells top to bottom.

`.env` holds your personal API key and is gitignored. Never commit it, and never paste a
key directly into a notebook cell.

## Data

`data/Rajasthan.pdf` is a government compilation of central, centrally-sponsored, and state
schemes for Rajasthan. `data/Rajasthan/` holds the text already extracted from that PDF:

- `pages.json` -- one dict with `source`, `n_pages`, and a `pages` list (the lab uses this)
- `pages.jsonl` -- the same pages, one JSON object per line
- `pages/page_NNN.txt` -- the same pages as individual text files
