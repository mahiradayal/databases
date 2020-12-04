# Databases class project: Scraping Indeed.com for contact tracing jobs

## Methods
This project uses BeautifulSoup to scrape job titles, companies, location (state), type (remote or not), pay and excerpts from over 60 pages of 800 active job postings. Data was cleaned -- specifically using Regular Expressions to standardize formats of the locations of each job to avoid inconsistencies (eg. NY, New York, NYC and other formats of the same state). The locations column was changed to abbreviated state names, and records with no location data were dropped from the database. 

Refer to notebook 1 (Indeed scraping) for scraping, notebook 2 (Indeed cleaning) for filtering, cleaning and forming a database. 

## Preliminary Findings (Step 1 of the project) 
Maryland had 192 postings, which was two times more than any other state. Illinois, California and Wisconsin followed, with between 45 and 70 postings each. A majority of the postings were not primarily remote positions — and only a handful were marked "temporarily remote." The City of Baltimore posted the most (160) jobs and the Arkansas Foundation for Medical Care (34) followed with 34 postings. Most of the top "companies" that posted jobs were public organizations like cities, counties and state of federal level departments. 

# Next Steps
1. Integrating a secondary data source: To contextualize the data from Indeed.com, I will join individual COVID case numbers over the last 6 months to visualize the trend in cases in each state. I will also create another column with the official address for each listed company — which will be necessary if I try to use the Google Maps API.  
2. Mapping: With my listed addresses, I will use the Google Maps API to plot each company and the number of jobs they have posted. To do this, I will need to make sure none of the companies double posted jobs. The Google Maps API may not automatically have the address for each company, and if manually creating an address column proves impossible, I will plot job listings by state instead. 

# Goals and limitations 
Indeed.com does not carry listings for every single contact tracing job. A dataset of 800 jobs is very limited, and only represents companies recruiting on job posting websites, not companies recruiting in other ways. It's impossible to draw any conclusions about contact tracers or COVID with this data. The goal is simply to visualize which parts of the country need more contact tracers. Over 250 million people visit Indeed.com to search for jobs every month, and even though it isn't an extensive list, it's a fairly representative sample. Glassdoor.com and LinkedIn jobs both had fewer postings than Indeed.com. 
