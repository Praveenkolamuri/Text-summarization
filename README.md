# Summarization Pipeline using BART Model

This repository contains a script to perform text summarization using the BART model from the Hugging Face `transformers` library. The BART model is pre-trained and fine-tuned on summarization tasks, making it a powerful tool for generating concise summaries of long texts.

## Installation

To run this script, you need to have Python installed along with the `transformers` library. You can install the necessary dependencies using pip:

```bash
pip install transformers
```

## Usage

The script `summarize_article.py` loads a summarization pipeline using the BART model and generates a summary for a provided article. Below is an example of how to use the script.

### Example

```python
from transformers import pipeline

# Load the summarization pipeline with the BART model
summarizer = pipeline("summarization", model="facebook/bart-large-cnn")

# The article to be summarized
ARTICLE = """ New York (CNN)When Liana Barrientos was 23 years old, she got married in Westchester County, New York.
A year later, she got married again in Westchester County, but to a different man and without divorcing her first husband.
Only 18 days after that marriage, she got hitched yet again. Then, Barrientos declared "I do" five more times, sometimes only within two weeks of each other.
In 2010, she married once more, this time in the Bronx. In an application for a marriage license, she stated it was her "first and only" marriage.
Barrientos, now 39, is facing two criminal counts of "offering a false instrument for filing in the first degree," referring to her false statements on the
2010 marriage license application, according to court documents.
Prosecutors said the marriages were part of an immigration scam.
On Friday, she pleaded not guilty at State Supreme Court in the Bronx, according to her attorney, Christopher Wright, who declined to comment further.
After leaving court, Barrientos was arrested and charged with theft of service and criminal trespass for allegedly sneaking into the New York subway through an emergency exit, said Detective
Annette Markowski, a police spokeswoman. In total, Barrientos has been married 10 times, with nine of her marriages occurring between 1999 and 2002.
All occurred either in Westchester County, Long Island, New Jersey or the Bronx. She is believed to still be married to four men, and at one time, she was married to eight men at once, prosecutors say.
Prosecutors said the immigration scam involved some of her husbands, who filed for permanent residence status shortly after the marriages.
Any divorces happened only after such filings were approved. It was unclear whether any of the men will be prosecuted.
The case was referred to the Bronx District Attorney's Office by Immigration and Customs Enforcement and the Department of Homeland Security's
Investigation Division. Seven of the men are from so-called "red-flagged" countries, including Egypt, Turkey, Georgia, Pakistan and Mali.
Her eighth husband, Rashid Rajput, was deported in 2006 to his native Pakistan after an investigation by the Joint Terrorism Task Force.
If convicted, Barrientos faces up to four years in prison. Her next court appearance is scheduled for May 18.
"""

# Summarize the article
summary = summarizer(ARTICLE, max_length=130, min_length=30, do_sample=False)

# Print the summary
print(summary)
```

### Output

The script will print a summarized version of the provided article. The parameters `max_length` and `min_length` control the length of the summary, and `do_sample=False` ensures deterministic output.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

Save this content in a file named `README.md` and place it in the root directory of your GitHub repository. This will provide a clear and concise explanation of your project, how to install dependencies, and how to use the script.
