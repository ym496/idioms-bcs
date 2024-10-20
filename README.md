# idioms-bcs
A comprehensive collection of idioms used in the TV series *Better Call Saul*. This collection was generated using Google's *Gemini 1.5 Flash* LLM model. You can start browsing the collection [here](https://github.com/ym496/idiom-bcs/tree/master/Idioms).

<div align="center">
<img src="https://townsquare.media/site/442/files/2016/01/2_AW_BCS2d.jpg" alt="Better Call Saul" width="600" /> </centre>
</div>

# Running
I've provided the scripts used to generate the files, allowing you to tweak the prompts or make adjustments as needed.

## File Descriptions

- **`scrape.py`**: This script scrapes the transcripts from *Better Call Saul* and saves them as individual text files for each episode.

- **`query_model.py`**: This file sends the scraped text files to the Gemini model for processing. It takes the filename as an argument and retrieves idioms from the provided transcript.

- **`gen-idioms.sh`**: This shell script iterates through the text files generated by `scrape.py`, passing each one to `query-model.py`. It saves the output idioms in Markdown format in the `Idioms` directory.

## Running the Scripts

* **Clone the repository:**
```bash
git clone git@github.com:ym496/idioms-bcs.git
cd idioms-bcs
```
* **Set up a virtual environment:**
```bash
python3 -m venv .venv
source .venv/bin/activate
```
* **Install required Python packages:**
```bash
pip install -r requirements.txt
```
* **Give executable permissions and run:**
```bash
chmod +x gen-idioms.sh
./gen-idioms.sh
```
Please wait for the script to finish running. You can open another terminal tab to browse the files being created in your `Idioms` directory.
