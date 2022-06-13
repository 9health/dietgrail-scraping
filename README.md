# dietgrail-scraping
DietGrail Website Scraping using Python

## Prerequisites

This script uses these applications and Python libraries to crawl data from [DietGrail GI and GL of Foods](http://dietgrail.com/gid/) website

### OS and Applications

- macOS Monterey (12.2.1)
- Firefox 99.0
- pyenv
- Python 3.9.11
- Geckodriver

### Python Libraries

- pip
- Beautiful Soup 4
- Requests
- Pandas
- Selenium 4.1.3
- PyAutoGui

## Installations

1. Install Python Version Management:

       brew install pyenv
       brew install geckodriver

2. Install Python 3.9.11:

       pyenv install 3.9.11
       pyenv global 3.9.11
       pyenv exec python -V

3. Install Python Package Installer:

       pyenv exec python3 get-pip.py

4. Create `.pyenvrc` file:

       echo 'eval "$(pyenv init -)"' > ~/.pyenvrc

5. Install Python packages:

       pyenv exec pip install beautifulsoup4
       pyenv exec pip install requests
       pyenv exec pip install selenium
       pyenv exec pip install pyautogui
       pyenv exec pip install pandas

## List of Files

       scrape_selenium_10.py
       setting_scrape.txt

## How to Run

1. Edit `setting_scrape.txt` file. Refer to [Script Settings](#script-settings) section.

2. Source the pyenv environment file:

       source ~/.pyenvrc

3. Run command:

       pyenv exec python3 scrape_selenium_10.py

4. Other running options:

       MOZ_HEADLESS=1 pyenv exec python3 scrape_selenium_10.py

5. Output files and folders:

- Webpages will be saved in `offline_pages` folder.
- Output `.csv` file will be saved in `csv` folder.
- Chart files will be saved in `charts` folder.

## Script Settings

| **Parameters**           | **Default Value** | **Unit** | **Description**
| ------------------------ |  :---:            | :---:    | -----------------------------------------------
| `WEBPAGE_TIMEOUT`        |   15              | sec      | First wait time at the first webpage loading
| `WEBPAGE_LOAD`           |   2.7             | sec      | Wait time between web pages
| `WEBPAGE_PAUSE`          |   10              | page     | Number of pages to pause
| `WEBPAGE_PAUSE_TIME`     |   90              | sec      | Pause time between two pages
| `WEBPAGE_CHART_ON`       |   0               | -        | Enable chart scraping<br />(`0`: OFF, `1`: ON)
| `WEBPAGE_OFFLINE_PARSE`  |   0               | -        | Enable offline pages processing only<br />(`0`: OFF, `1`: ON)
| `GI_START_PAGE`          |   1               | page     | Start page to scrape
| `GI_STOP_PAGE`           |   219             | page     | Stop page to scrape
| `GI_LAST_PAGE`           |   219             | page     | Last page to scrape.<br />It should be larger than stop page
| `GI_ROW_NUM`             |   14              | row      | Number of rows in a page
| `GI_ROW_NUM`             |   4               | column   | Number of colums in a page

## Other Notes

- Sometimes [DietGrail GI and GL of Foods](http://dietgrail.com/gid/) website does not response in Firefox Remote, it needs to click manually.
- After about 50 clicks to download and save 50 pages, the [DietGrail GI and GL of Foods](http://dietgrail.com/gid/) website will stop response, it needs to wait about 30 seconds to 1 minute to wait for this website to be okay.

## Screenshots

[DietGrail GI and GL of Foods](http://dietgrail.com/gid/) first page

<img width="745" alt="First Page" src="readme-screenshots/Screenshot%202022-06-13%20at%2001-35-25%20Glycemic%20Index%20&%20Glycemic%20Load%20of%20Foods.png">

[DietGrail GI and GL of Foods](http://dietgrail.com/gid/) last page

<img width="745" alt="Last Page" src="readme-screenshots/Screenshot%202022-06-13%20at%2001-35-35%20Glycemic%20Index%20&%20Glycemic%20Load%20of%20Foods.png">

[DietGrail GI and GL of Foods](http://dietgrail.com/gid/) with chart

<img width="745" alt="With Chart" src="readme-screenshots/Screenshot%202022-06-13%20at%2001-35-49%20Glycemic%20Index%20&%20Glycemic%20Load%20of%20Foods.png">

## References

- [Taiga 2 Readme](https://github.com/broadinstitute/taiga/blob/master/README.md)
- [Install pip, pyenv, BeautifulSoup4](https://linuxtut.com/en/1806ef4176fea50ae01d/)
- [Organizing information with tables](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/organizing-information-with-tables)
- [GitHub relative link in Markdown file](https://stackoverflow.com/questions/7653483/github-relative-link-in-markdown-file)
- [GitHub Markup Sample](https://github.com/github/markup/blob/master/README.md#markups)
- [How to add images to README.md on GitHub?](https://stackoverflow.com/questions/14494747/how-to-add-images-to-readme-md-on-github)
- [How do I create a folder in a GitHub repository?](https://stackoverflow.com/questions/12258399/how-do-i-create-a-folder-in-a-github-repository)
- [Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
- [how to link to a file with spaces in the filename in github README.md](https://stackoverflow.com/questions/47050129/how-to-link-to-a-file-with-spaces-in-the-filename-in-github-readme-md)
- [GitHub relative link in Markdown file](https://stackoverflow.com/questions/7653483/github-relative-link-in-markdown-file)
- [Using content attachments](https://docs.github.com/en/enterprise-server@3.3/developers/apps/guides/using-content-attachments)
- [Attaching files](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/attaching-files)
- [About anonymized URLs](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-anonymized-urls)
- [Proxying User Images](https://github.blog/2014-01-28-proxying-user-images/)
- [How do I add a newline in a markdown table?](https://stackoverflow.com/questions/11700487/how-do-i-add-a-newline-in-a-markdown-table)
