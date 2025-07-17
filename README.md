# The Fictional Inspirations Behind Species Names

## Project 1 

This is my first project submission for the Lede Program, for which I analysed naming trends in species specifically named after fictional works. In this project, I explore how fictional worlds and characters have inspired species names over time, the main fictional sources of inspiration referenced in the names of organisms, and species belonging to which taxonomic classes have most often received names drawn from fiction. 

## Guide to the repository 
<code>species_scraping</code>: This is the notebook where I scraped the list of species named after fictional works from four Wikipedia pages.  

<code>species_GBIF</code>: This is the notebook where I accessed GBIF data using pygbif Python wrapper and extracted taxonomic details for each species.  

<code>species_analysis</code>: This notebook is where I did part of the data cleaning and analysis.  

## Process
Since there is no officially collated list for this, I started by scraping 4 Wikipedia pages that provided lists of species named after fictional works. This formed my base dataset which I then cross-checked with the Global Biodiversity Information Facility (GBIF). I used the pygbif Python package to access the GBIF API and extract taxonomic details for each species on the list. I dropped the names that did not have corresponding GBIF data, those that had since been reclassified or synonymized and those that GBIF marked as "Doubtful". Among the ones GBIF marked as "Synonym", I manually cross-checked and retained the entries that The Catalogue of Life marked as an accepted species. For some species names, GBIF was only able to match the name to a higher taxonomic category such as genus. These were cross-checked and retained if they were found to be accepted species via The Catalogue of Life. I was unable to get threat and extinction status from the GBIF API and so I manually edited the dataset for the 'extinct' column based on Wikipedia's categorization in the list. Of the final 763 taxa in this dataset, 80 are names of genera referencing fictional works, while the remaining 683 are species names. Notably, each genus may have a number of closely-related species grouped under it. Wherever the name of the genus is inspired from fiction, this dataset lists only the overarching genus name and not the names of the species it contains. 

NOTE: Parts of the code were written using AI.

## Data Sources
1. GBIF Secretariat. (2023). GBIF Backbone Taxonomy Checklist dataset, https://doi.org/10.15468/39omei accessed via GBIF.org on 2025‑07‑10. 

2. Bánki, O., Roskov, Y., Döring, M., Ower, G., Hernández Robles, D. R., Plata Corredor, C. A., Stjernegaard Jeppesen, T., Örn, A., Pape, T., Hobern, D., Garnett, S., Little, H., DeWalt, R. E., Miller, J., & Orrell, T. (2025). Catalogue of Life (Annual Checklist 2025). Catalogue of Life Foundation, Amsterdam, Netherlands. https://doi.org/10.48580/dgr6n

3. List of organisms named after works of fiction. (2025, 12 July). In Wikipedia. https://en.wikipedia.org/wiki/List_of_organisms_named_after_works_of_fiction

4. List of things named after J. R. R. Tolkien and his works. (2025, 4 July). In Wikipedia. https://en.wikipedia.org/wiki/List_of_things_named_after_J._R._R._Tolkien_and_his_works

5. List of organisms named after the Star Wars series. (2025, 4 July). In Wikipedia. https://en.wikipedia.org/wiki/List_of_organisms_named_after_the_Star_Wars_series

6. List of organisms named after the Harry Potter series. (2025, 22 May). In Wikipedia. https://en.wikipedia.org/wiki/List_of_organisms_named_after_the_Harry_Potter_series

## Skills learned
Much of the learning on this first project was to do with scraping, using APIs and figuring out how to clean the data. 

## Things I would have liked to do
If I had more time, I would have liked to add information regarding each species threat status as per IUCN categories of endangerment and analyse those. I would also have liked to explore the countries of origin of these fictional works.
