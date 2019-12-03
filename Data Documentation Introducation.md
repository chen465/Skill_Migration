
## Data Cleaning Assessment

First I will use the Python file.dtypes to ensure all the columns in the datasets are in the good type. Therefore, I do the following Python code to check each column's data type of each dataset which include (Growth from Industry Transition; Industry Skills Needs; Skill Penetration; Talent Migration:):
growth_from_ind.dtypes;skill_penetration.dtypes;ind_skill_needs.dtypes; industry_migration.dtypes;skill_migration.dtypes

Since the education_and_major file is copied and pasted by myself, the data type are adjusted by myself. Therefore, I will not do some data cleaning for this file. I will keep the original format for this frile.

Then,except the education_and_major file, all of the rest files will be kept certain useful columns and delete the rest useless columns by running the following code:
growth_from_ind=growth[['country_name','wb_income','wb_region','isic_section_index','isic_section_name','industry_name','growth_rate_2015','growth_rate_2016','growth_rate_2017','growth_rate_2018']]
industry_migration=industry[['country_name','wb_income','wb_region','isic_section_index','isic_section_name','industry_name','net_per_10K_2015','net_per_10K_2016','net_per_10K_2017','net_per_10K_2018']]
skill_migration=skill[['country_name','wb_income','wb_region','skill_group_category','skill_group_name','net_per_10K_2015','net_per_10K_2016','net_per_10K_2017','net_per_10K_2018']]

skill_penetration=skill_pen[['year','isic_section_index','isic_section_name','industry_name','skill_group_category','skill_group_name','skill_group_penetration_rate']]
ind_skill_needs=ind_skill[['year','isic_section_index','isic_section_name','industry_name','skill_group_category','skill_group_name','skill_group_rank']]

For this part, I still have one point to hesitate. Since I still have some confused point on the per_10k columns. Therefore, I am still thinking how to deal with that columns in all of the files.


## Authorship
The following datasets are used the same license:
Growth from Industry Transition
Industry Skills Needs
Skill Penetration
Talent Migration

License- The aggregated datasets and visuals are available to all for the public good under the Creative Commons Attribution 3.0 IGO license with attribution to both LinkedIn Corporation and the World Bank. The World Bank Group and LinkedIn Corporation (including its affiliates) do not take responsibility and are not liable for any damage caused through use of data and insights through this website, including any indirect, special, incidental or consequential damages."




## Attribution
Growth from Industry Transition
Industry Skills Needs
Skill Penetration
Talent Migration
All of the above datasets are created by the world bank

Education_and_major are from usnews and copied by myself

## Provenance of the file
https://www.usnews.com/best-graduate-schools/top-business-schools/mba-rankings
https://datacatalog.worldbank.org/dataset/world-bank-group-linkedin-dashboard-dataset


## Describe the semantic contents of the files
education_and_major: This is a dataset which are the top10 American university in each program.
The columns in this dataset are: ranking program and university name

Growth from Industry Transition:
This dataset is used to see that see how people are moving across industries based on in minus out.
The columns in this dataset are:country code, country name,wb region, wb income, ISIC section index, ISIC section name, industry name, growth rate

Industry Skills Needs:
This dataset is used to see which skills are most likely to be added in one industry compared to other industry.
The columns in this dataset are: ISIC section index, ISIC section name,industry name,skill group name and skill group rank.


Skill Penetration: 
This dataset is used to see that how many skills from each skill groups appear among the top30 skills for each occupation in an industry.
The columns in this dataset are: year,ISIC section index, ISIC section name, industry name, skill group category, skill group name and skill group penetration rate.

Talent Migration:
This dataset is used to see the migration(arrivalus minus departures) based on country, industry and skill.

This dataset still contains three sub-dataset which are country migration, industry migration and skill migration.

The columns in country migration dataset are: base/target country code, base/target country name,base/target lat/long, base/target wb region, base/targetwb income,net per 10k

The columns in industry migration dataset are:country code, country name,wb region, wb income,ISIC section index, ISIC section name,industry name,net per 10k.

The columns in skill migration dataset are:country code, country name,wb region, wb income, skill group name and net per 10k

## Describe the collection process
For the education_and_major file, I just copy and paste the data from the website called:https://www.usnews.com/best-graduate-schools/top-business-schools/mba-rankings
I copy and paste the data by myself in the specific format which are needed by my whole dataset in the excel.

All the rest of the files are found from the website called:https://datacatalog.worldbank.org/dataset/world-bank-group-linkedin-dashboard-dataset
I use all of these datasets directly and download from this website.



## Descritption of the data structure
All of them are in the excel files.

Growth from Industry Transition：xlsx
7,199 rows,8 properties to describe one record.

Industry Skills Needs:xlsx
2,841 rows,5 properties to describe one record.


Skill Penetration:xlsx
16,825 rows,7 properties to describe one record.

Talent Migration:xlsx
    country migration:4,163 rows,13 properties to describe one record.
    industry migration: 5,283 rows,8 properties to describe one record.
    skill migration: 20,704 rows, 6 properties to describe one record.

Followings are the data type that stands that all of the columns which are needed from the above datasets:
country_name             object
wb_income                object
wb_region                object
skill_group_category     object
skill_group_name         object
net_per_10K_2015        float64
net_per_10K_2016        float64
net_per_10K_2017        float64
net_per_10K_2018        float64


education_and_major:xlsm
ranking: integer
program: object
university name: object


## Others
education_and_major:
ranking: is the university's ranking in the specific program
program: is the program name /major name 
university name: university name

Growth from Industry Transition:
country code: country name given by the world bank, the two letter country code
country name: country name
wb region: contry region classification
wb income: country income level classification
ISIC section index: according to the ISIC Rev. 4 industry classification
ISIC section name:according to the ISIC Rev. 4 industry classification
industry name: industry name
growth rate:each year, the growth rate derived as rate of change between the memeber_count_start_year and memeber_count_end_year.

Industry Skills Needs:
All the other columns are the same as the above.
skill group name: skill group and classified in a detailed classification. E.G.: computer classifed by the Java.
skill group rank:skill ranked by the industry name


Skill Penetration: 
All the other columns are the same as the above.
skill group penetration rate: the penetration rate of how many of the top 30 skills

Talent Migration:
All the other columns are the same as the above.
net per 10k (arrival minus depature) based on country, skill, industry

All of the dataset do not have the missing value. Do not have the unique category data.







```python

```
