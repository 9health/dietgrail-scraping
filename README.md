# dietgrail-scraping
DietGrail Website Scraping using Python

## Prerequisites

This script is using this stack

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

4. Create .pyenvrc file:

       echo 'eval "$(pyenv init -)"' > ~/.pyenvrc

5. Install Python packages

       pyenv exec pip install beautifulsoup
       pyenv exec pip install requests
       pyenv exec pip install selenium
       pyenv exec pip install pyautogui
       pyenv exec pip install pandas

## How to run

1. Source the pyenv environment file

       source ~/.pyenvrc

2. Run command

       pyenv exec python3 scrape_selenium_10.py

3. Other running options

       MOZ_HEADLESS=1 pyenv exec python3 scrape_selenium_10.py

## References

- [Taiga 2 Readme](https://github.com/broadinstitute/taiga/blob/master/README.md)
- [Install pip, pyenv, BeautifulSoup4](https://linuxtut.com/en/1806ef4176fea50ae01d/)
