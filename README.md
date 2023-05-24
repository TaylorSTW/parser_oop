# Vacancy Parser using OOP

## Project Description
This project allows user to search vacancies using two API platforms: 
**HeadHunter** and **SuperJob**. Both platforms are popular in CIS region and
are commonly used by employees and employers. The search results can be 
selectively saved by user into JSON file. There are several criteria that
affect the search results:

- Search only includes vacancies in _Russian Federation_
- Only _minimum_ salary is taken into account and displayed to user. Maximum
salary is shown if minimum is omitted.
- Vacancy is _ignored_ if it does not have following:
    - salary
    - vacancy name
    - vacancy URL link
    - requirement
    - company name
- If vacancy's salary is given in US dollars(USD) then it is converted into 
rubles(RUB). Please see `vacancy_api.py` for details

---
## Simple Algorithm

The simple high-level algorithm of the program is described below:
1. User greeting
2. Platform choice
3. Input search query
4. Determination of top N vacancies sorted by salary. Only maximum of 25 
vacancies will be displayed.
5. Representation of each of top N vacancies:
   - Vacancy save procedure if needed
6. Representation of saved vacancies in JSON file
   - Vacancy deletion procedure if needed
7. Exit