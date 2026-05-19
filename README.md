# Masai Live: Job Scraper Agent

A fast, concurrent Python tool that scrapes job listings from multiple platforms and saves the results to a CSV file.

### Supported Platforms

* **RemoteOK**
* **Naukri** *(Note: Uses Firecrawl API for scraping)*
* **Arbeitnow**
* **Jobicy**
* **Remotive**
* **Wellfound**
* **WeWorkRemotely**

---

### Setup & Requirements

1. Ensure you have Python 3.x installed.
2. Install the required Python packages:

```bash
pip install requests beautifulsoup4 firecrawl-py

```

*(Note: A valid Firecrawl API key is required in `naukri.py` to scrape Naukri jobs successfully).*

---

### Usage

You can run the scraper interactively (it will prompt you for a job title) or strictly via the command line.

**Interactive Mode:**

```bash
python main.py

```

**Command-Line Mode:**

```bash
python main.py --job_title "Software Engineer" --location "Remote" --limit 100 --output "results.csv"

```

---

### CLI Arguments

| Argument | Description | Default |
| --- | --- | --- |
| `--job_title` | The job title to search for. | **Required** (Prompts if missing) |
| `--location` | Location to filter by (e.g., "India", "Remote"). | `Global/Remote` |
| `--output` | The path/filename for the generated CSV. | `output/jobs.csv` |
| `--limit` | Maximum number of total jobs to save. | `200` |
| `--append` | Flag to append to the CSV instead of overwriting. | `False` |

---
Made with 💖 by Vaibhav Pandey
