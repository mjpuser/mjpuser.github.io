---
layout: post
title: The Wage Gap
---

<style>
  thead th {
    text-align: center;
    text-transform: capitalize;
  }
  tbody td {
    font-size: 12px;
    text-align: right;
    padding: 0 5px;
  }
  tbody tr td:last-child {
    text-align: left;
    white-space: nowrap;
  }
</style>


I investigated the wage gap out of curiousity since I started hearing conflicting news stories about whether or not the wage gap exists.  When I was doing my google searches, I found <a href="http://www.aauw.org/research/the-simple-truth-about-the-gender-pay-gap/" target="_blank" hack="_">The Simple Truth about the Gender Pay Gap (Fall 2016)</a>,  which is the first article to come up in Google's search results.  Here is how they present their data, and it looks bad for women:

![The Truth: Gender Pay Gap](/images/posts/wage-gap/the-simple-truth-figure-2-v2.jpg)

The second article that comes up in Google, <a href="http://www.infoplease.com/ipa/A0763170.html" target="_blank" hack="_">Infoplease.com: The Wage Gap</a>, also shows that in 2013, women made 78 cents on the dollar.  

I also searched for "gender wage gap myth", and I found <a href="http://www.forbes.com/sites/karinagness/2016/04/12/dont-buy-into-the-gender-pay-gap-myth/" target="_blank" hack="_">Don't Buy Into The Gender Pay Gap Myth</a>, which claims to be written by a woman, and breaks down the wage gap argument, taking into account factors such as hours worked or likelihood to be in a union.  They claim that this accounts for about 15% of the gap, and so women are within 5 cents on the dollar vs men.

One problem I had with both sources was that they never linked to the data they used or how they extracted the stats.  I wanted to know what occupations payed more, where people were located, how much experience they had, etc., but I had to assume they just grouped everyone together and did not take this into account.

For this article, I ended up using <a href="https://www.census.gov/programs-surveys/acs/data/pums.html" target="_blank" hack="_">2011 - 2015 ACS Public Use Microdata Sample files (PUMS)</a>.  It comes from the United States Census Bureau, so I think we're good.  

## The stats

**Each table lists:**

* The number of women and men used in the sample
* The min, median, and max salary
* The ratio of pay based on the median (men/women or women/men depending on who makes more)
* The occupation

**Data used:**

* I only included non married people.  I thought this would remove the argument that including married spouses might affect their devotion to the occupation
* I only included people with at least a bachelors degree
* I only included people that worked 48 - 52 weeks per year
* I filtered out salaries < 12,000 since if you are working 50 weeks a year on minimum wage, you should make at least 15k before taxes, and 13.9k after taxes.  So I'm guessing it is bad data, or there is some illegal garbage happening.  There were some salaries at 600 bucks which would mean you're homeless and making 2 bucks a day.
* I broke up the data from 20 - 30 and 30 - 40 year olds.  I didn't include more data because it's just a lot.  If you want me to add it, contact me.

**Issues I have with my stats:**

* I did not group by location, and location could be a huge factor
* I should include percent error
* The ratio is calculated on the median pay
* These stats are great, but I should be using more sophisticated ways of comparing salaries (F Score or R-squared tests)
* I would like to see the sex of who is deciding the salary to better understand possible gender descrimination

If you want some of the tools I used to browse the data and create these stats, you can contact me, or check out <a href="https://github.com/mjpuser/wage-gap" _target="blank" hack="_">the code I wrote to extract it</a>.

## My Thoughts

These stats are indicating that the wage gap isn't as bad as the left says it is, but it does seem to lean in favor of men.  I wouldn't describe the wage gap as "women are making 80 cents for every dollar a man makes."  I think it's inappropriate and more prone to misinterpretation to summarize millions of worker's salaries with a single number/ratio.  The wage gap is a complex and there is a wide spectrum of salaries across all fields depending on many variables.  In the best case scenario for women, they are making $1.24 for every $1 a man makes, and in the worst case, they are making 66 cents for every dollar a man makes.  With this complexity in mind, looking at just the median could cause you to make false assumptions.  For example, check out "Billing and Posting Clerks" in the category where pay favors men over women.  The median is less for women, but the max is more for women by almost 4x.  This just goes to show that these stats don't tell the whole story.  We need more data to figure out what the driving factors are behind the wage gap.


## People from age 20 - 29

### Pay favoring women

|# of women|# of men|ratio|women's median|men's median|women's max|men's max|women's minimum|men's minimum|occupation|
|-|-|-|-|-|-|-|-|-|-|
|32|40|0.83|39000.00|32500.00|100000|70000|15000|15000|Biological Technicians|
|58|39|0.87|30000.00|26100.00|100000|91000|13000|12500|Religious Workers, All Other|
|46|46|0.89|45000.00|40000.00|120000|130000|16000|16900|Agricultural And Food Scientists|
|72|121|0.89|28000.00|25000.00|60000|88000|14400|13000|Shipping, Receiving, And Traffic Clerks|
|1143|1092|0.90|29000.00|26000.00|410000|200000|12500|12100|Postsecondary Teachers|
|33|58|0.90|42800.00|38500.00|56000|64000|19800|15800|Conservation Scientists And Foresters|
|119|35|0.90|24400.00|22000.00|95000|52000|13000|13000|Hotel, Motel, And Resort Desk Clerks|
|45|79|0.92|45000.00|41200.00|220000|200000|20000|16500|Transportation, Storage, And Distribution Managers|
|43|34|0.92|43100.00|39500.00|100000|90000|15000|19000|Administrative Services Managers|
|573|241|0.92|38000.00|35000.00|230000|360000|13000|14000|Clinical Laboratory Technologists And Technicians|
|64|98|0.93|70500.00|65500.00|150000|150000|21000|35000|Actuaries|
|74|164|0.93|23450.00|21900.00|70000|69000|13700|13000|Cooks|
|68|56|0.94|30000.00|28050.00|150000|120000|13000|15600|Photographers|
|221|99|0.94|38500.00|36000.00|99000|120000|14400|12400|Wholesale And Retail Buyers, Except Farm Products|
|36|38|0.94|35000.00|33000.00|80000|100000|15600|15000|Lifeguards And Other Recreational, And All Other|
|386|73|0.95|37000.00|35000.00|375000|91000|13300|15000|Other Therapists, Including Exercise Physiologists|
|37|36|0.95|56000.00|53000.00|105000|108000|22000|25000|Economists|
|81|81|0.95|38000.00|36000.00|96000|95000|15000|13000|Chemical Technicians|
|624|239|0.95|38000.00|36000.00|451000|160000|13000|12600|Education Administrators|
|82|475|0.95|68500.00|65000.00|100000|180000|20000|17000|Electrical And Electronics Engineers|
|141|139|0.95|40000.00|38000.00|110000|131000|15000|13000|Producers And Directors|
|259|47|0.95|42000.00|40000.00|123000|73000|12100|13000|Fundraisers|
|125|339|0.95|63000.00|60000.00|150000|150000|17000|19000|Industrial Engineers, Including Health And Safety|
|435|136|0.95|38000.00|36200.00|111000|150000|12900|13100|Social And Community Service Managers|
|386|49|0.96|24000.00|23000.00|90000|80000|12600|12500|Childcare Workers|
|135|421|0.97|31000.00|30000.00|101000|125000|12900|12400|Security Guards And Gaming Surveillance Officers|
|99|181|0.97|32000.00|31000.00|300000|403000|12500|12500|Athletes, Coaches, Umpires, And Related Workers|
|386|243|0.97|32000.00|31000.00|125000|140000|14000|13000|Miscellaneous Life, Physical, And Social Science|
|84|35|0.97|32000.00|31000.00|80000|150000|13000|16500|Reservation And Transportation Ticket Agents And Travel|
|1504|467|0.97|35000.00|34000.00|417000|351000|12500|13500|Counselors|
|37|33|0.97|37000.00|36000.00|85000|100000|20000|16000|Agents And Business Managers Of Artists, Performers,|
|1154|688|0.97|39000.00|38000.00|160000|95000|12100|12800|Secondary School Teachers|
|126|84|0.97|25650.00|25000.00|175000|66000|12500|13000|First-Line Supervisors Of Food Preparation And Serving|
|1334|404|0.98|41000.00|40000.00|360000|421000|12100|12500|Human Resources Workers|
|167|48|0.98|35400.00|34750.00|71000|66000|12500|17000|Librarians|
|39|53|0.98|55000.00|54000.00|80000|120000|15000|30000|Environmental Engineers|
|342|1121|0.98|65000.00|64000.00|429000|250000|15000|13000|Miscellaneous Engineers, Including Nuclear Engineers|
|2185|358|0.99|34000.00|33500.00|331000|92000|12100|13000|Social Workers|
|86|318|0.99|71000.00|70000.00|149000|166000|20000|12500|Aerospace Engineers|
|150|118|0.99|38500.00|38000.00|125000|93000|13500|15000|Biological Scientists|
|73|79|0.99|38500.00|38000.00|81000|300000|14400|14800|Private Detectives And Investigators|
|133|94|0.99|34400.00|34000.00|70000|90000|15600|14000|Dispatchers|
|77|62|1.00|20100.00|20000.00|65000|45000|13000|13500|Food Preparation Workers|
|193|57|1.00|45000.00|44800.00|120000|100000|13500|13600|Psychologists|

### Pay favoring men

|# of women|# of men|ratio|women's median|men's median|women's max|men's max|women's minimum|men's minimum|occupation|
|-|-|-|-|-|-|-|-|-|-|
|92|119|0.76|41800.00|55000.00|161000|421000|15000|14000|Chief Executives And Legislators|
|185|136|0.77|36000.00|46950.00|100000|340000|12600|20000|Miscellaneous Legal Support Workers|
|245|82|0.81|30000.00|37000.00|114000|110000|12200|13000|File Clerks|
|279|178|0.81|39500.00|48500.00|186000|190000|13000|12800|Property, Real Estate, And Community Association|
|30|134|0.82|23400.00|28700.00|50000|160000|13000|12400|Janitors And Building Cleaners|
|91|34|0.82|30000.00|36400.00|169000|100000|12600|14400|Interviewers, Except Eligibility And Loan|
|82|46|0.82|38000.00|46100.00|90000|90000|13000|15000|Financial Specialists, All Other|
|75|69|0.83|43000.00|52000.00|97000|100000|18000|14000|Detectives And Criminal Investigators|
|45|74|0.83|41600.00|50000.00|93000|150000|13000|18600|Industrial Production Managers|
|70|244|0.83|45500.00|54500.00|126000|152000|20000|15000|Construction Managers|
|31|114|0.84|28600.00|34250.00|69000|120000|13500|14000|Military Enlisted Tactical Operations And Air/Weapons|
|370|163|0.84|41000.00|49000.00|116000|165000|13000|12300|Medical And Health Services Managers|
|155|311|0.84|40500.00|48000.00|300000|587000|13000|15000|Securities, Commodities, And Financial Services Sales|
|51|55|0.85|24000.00|28300.00|45000|100000|13000|14000|Chefs And Head Cooks|
|248|214|0.85|40000.00|47000.00|170000|149000|14000|15600|Purchasing Agents, Except Wholesale, Retail, And Farm|
|125|72|0.85|40000.00|47000.00|140000|607000|14000|19200|Training And Development Specialists|
|94|37|0.85|32000.00|37500.00|80000|110000|16000|23000|Information And Record Clerks, All Other|
|31|41|0.85|41000.00|48000.00|72000|150000|13000|15000|Judicial Law Clerks|
|79|52|0.85|32000.00|37450.00|85000|210000|12400|20000|Lodging Managers|
|311|111|0.86|30000.00|35000.00|398000|110000|14000|13000|Billing And Posting Clerks|
|48|60|0.86|30000.00|35000.00|120000|80000|12400|19000|Computer Operators|
|49|226|0.86|22300.00|26000.00|125000|378000|14400|13000|Laborers And Freight, Stock, And Material Movers, Hand|
|1724|1499|0.86|43000.00|50000.00|344000|587000|12100|13000|Miscellaneous Managers, Including Funeral Service|
|53|66|0.86|28000.00|32500.00|100000|100000|14000|13000|Emergency Medical Technicians And Paramedics|
|56|237|0.86|37300.00|43200.00|80000|120000|13200|15000|Military, Rank Not Specified|
|61|72|0.86|40000.00|46300.00|91000|243000|20400|14400|Credit Analysts|
|727|131|0.87|26000.00|30000.00|456000|100000|12200|12600|Receptionists And Information Clerks|
|221|387|0.87|43000.00|49500.00|153000|344000|13000|15000|Personal Financial Advisors|
|105|129|0.87|40000.00|46000.00|86000|117000|12200|13600|Artists And Related Workers|
|40|96|0.87|43000.00|49300.00|110000|171000|13000|24000|Cost Estimators|
|95|153|0.87|43700.00|50000.00|88000|130000|15000|14000|Database Administrators|
|60|150|0.87|30000.00|34300.00|68000|417000|15000|15000|Other Production Workers, Including Semiconductor|
|133|139|0.88|42000.00|48000.00|115000|185000|20000|12800|Insurance Underwriters|
|34|90|0.88|24500.00|28000.00|60000|80000|13000|13000|Miscellaneous Agricultural Workers, Including Animal|
|234|187|0.88|30000.00|34100.00|120000|139000|13000|13500|Food Service Managers|
|72|140|0.88|36600.00|41550.00|116000|110000|15000|15000|Drafters|
|92|270|0.88|30000.00|34000.00|70000|79000|14000|12500|Clergy|
|136|61|0.89|31000.00|35000.00|110000|100000|14400|13000|Loan Interviewers And Clerks|
|746|404|0.89|35000.00|39500.00|324000|128000|12100|15000|First-Line Supervisors Of Office And Administrative|
|112|86|0.89|40000.00|45000.00|108000|140000|14400|20000|Financial Clerks, All Other|
|771|784|0.89|40000.00|45000.00|417000|331000|12800|13000|Financial Managers|
|227|123|0.89|40000.00|45000.00|105000|180000|13500|14000|Human Resources Managers|
|1152|531|0.89|40100.00|45000.00|419000|410000|12900|13000|Marketing And Sales Managers|
|365|477|0.89|41000.00|46000.00|341000|505000|13000|13000|Sales Representatives, Services, All Other|
|144|197|0.89|42000.00|47000.00|130000|400000|15000|14000|Architects, Except Naval|
|238|884|0.89|42000.00|47000.00|98000|152000|14000|12500|Police Officers|
|89|45|0.89|42000.00|47000.00|130000|150000|15000|17000|Technical Writers|
|182|143|0.89|35750.00|40000.00|125000|225000|14000|14000|Real Estate Brokers And Sales Agents|
|138|125|0.89|25950.00|29000.00|68000|100000|13000|12900|Bartenders|
|120|243|0.90|35000.00|39000.00|90000|130000|13000|13000|Bailiffs, Correctional Officers, And Jailers|
|319|314|0.90|36000.00|40000.00|150000|175000|12500|13000|Credit Counselors And Loan Officers|
|350|413|0.90|36000.00|40000.00|301000|323000|12400|13000|Physical Scientists, All Other|
|41|39|0.90|45000.00|50000.00|72000|100000|15000|20000|Urban And Regional Planners|
|1326|733|0.90|38000.00|42000.00|360000|396000|12500|12500|Designers|
|535|246|0.91|32900.00|36300.00|400000|100000|12100|13000|Other Teachers And Instructors|
|281|199|0.91|40000.00|44000.00|313000|491000|14000|13000|Advertising Sales Agents|
|344|283|0.91|40000.00|44000.00|78000|104000|14000|15000|Claims Adjusters, Appraisers, Examiners, And|
|276|185|0.91|36400.00|40000.00|98000|324000|12600|15000|Production, Planning, And Expediting Clerks|
|646|655|0.91|51000.00|56000.00|187000|419000|13000|14000|Management Analysts|
|168|597|0.91|45550.00|50000.00|190000|200000|15000|13300|Computer Occupations, All Other|
|248|438|0.91|43000.00|47200.00|119000|116000|13400|13000|Web Developers|
|78|308|0.91|46500.00|51000.00|110000|210000|22000|14400|Network And Computer Systems Administrators|
|89|83|0.92|55000.00|60000.00|130000|403000|15000|15000|Miscellaneous Mathematical Science Occupations,|
|305|206|0.92|24800.00|27000.00|192000|140000|12500|13000|Cashiers|
|364|104|0.92|23000.00|25000.00|260000|115000|12100|12500|Teacher Assistants|
|102|192|0.92|40000.00|43300.00|100000|120000|15600|15500|Engineering Technicians, Except Drafters|
|284|286|0.92|41600.00|45000.00|455000|403000|13000|12500|General And Operations Managers|
|174|215|0.93|37000.00|40000.00|105000|130000|13000|14000|Inspectors, Testers, Sorters, Samplers, And Weighers|
|286|327|0.93|37000.00|40000.00|200000|378000|14000|12500|Insurance Sales Agents|
|70|41|0.93|35750.00|38500.00|110000|86000|15000|13000|Miscellaneous Health Technologists And Technicians|
|354|219|0.93|40000.00|43000.00|200000|115000|13000|15000|Business Operations Specialists, All Other|
|541|236|0.93|33100.00|35500.00|340000|115000|13500|13000|Bookkeeping, Accounting, And Auditing Clerks|
|56|56|0.93|90000.00|96500.00|180000|421000|24000|14000|Dentists|
|102|43|0.93|35000.00|37500.00|80000|80000|14000|16000|Eligibility Interviewers, Government Programs|
|457|127|0.93|28000.00|30000.00|180000|72000|12500|15000|Health Practitioner Support Technologists And Technicians|
|401|113|0.93|28000.00|30000.00|120000|102000|12300|12800|Nursing, Psychiatric, And Home Health Aides|
|3087|2201|0.94|45000.00|48000.00|655000|200000|12300|14000|Accountants And Auditors|
|100|57|0.94|30000.00|32000.00|65000|96000|16600|16000|Bill And Account Collectors|
|748|223|0.94|30000.00|32000.00|120000|120000|12500|13000|Office Clerks, General|
|891|970|0.94|30000.00|32000.00|477000|504000|13000|12300|Retail Salespersons|
|261|41|0.94|30000.00|32000.00|79000|74000|12500|15000|Social And Human Service Assistants|
|1860|1063|0.94|31000.00|33000.00|538000|200000|13000|12500|Customer Service Representatives|
|2717|257|0.94|31000.00|33000.00|483000|100000|12200|13000|Secretaries And Administrative Assistants|
|235|47|0.94|80000.00|85000.00|404000|421000|14000|17600|Physician Assistants|
|182|853|0.94|56500.00|60000.00|484000|200000|15000|13000|Computer Programmers|
|405|186|0.94|33000.00|35000.00|180000|116000|12600|13700|Insurance Claims And Policy Processing Clerks|
|85|57|0.94|50000.00|53000.00|105000|92000|15000|13000|Budget Analysts|
|731|300|0.94|42000.00|44500.00|199000|322000|12500|14000|Market Research Analysts And Marketing Specialists|
|115|118|0.94|44000.00|46600.00|115000|225000|13000|13000|Environmental Scientists And Geoscientists|
|521|812|0.95|52000.00|55000.00|215000|484000|16800|12100|Computer Systems Analysts|
|204|167|0.95|42000.00|44400.00|113000|110000|15000|15000|Chemists And Materials Scientists|
|289|167|0.95|35000.00|37000.00|321000|85000|15000|12900|Editors|
|649|188|0.95|35000.00|37000.00|215000|200000|13000|14400|Paralegals And Legal Assistants|
|1054|31|0.95|27000.00|28500.00|208000|60000|12400|13200|Preschool And Kindergarten Teachers|
|446|355|0.95|55000.00|58000.00|210000|400000|12500|15000|Lawyers, And Judges, Magistrates, And Other Judicial|
|6885|1490|0.95|37000.00|38950.00|587000|475000|12100|12500|Elementary And Middle School Teachers|
|88|152|0.95|38000.00|40000.00|100000|120000|12800|14400|Logisticians|
|147|87|0.95|38000.00|40000.00|150000|160000|13500|15000|Other Healthcare Practitioners And Technical|
|512|105|0.95|38000.00|40000.00|108000|90000|13000|13000|Special Education Teachers|
|30|94|0.95|40000.00|42000.00|90000|106000|15000|15000|Surveyors, Cartographers, And Photogrammetrists|
|511|180|0.95|62000.00|65000.00|455000|160000|14000|16000|Physical Therapists|
|541|316|0.95|105000.00|110000.00|180000|180000|17000|12200|Pharmacists|
|174|244|0.95|53000.00|55500.00|171000|410000|14000|20000|Financial Analysts|
|78|41|0.96|40000.00|41800.00|107000|110000|18000|20000|Compensation, Benefits, And Job Analysis Specialists|
|246|84|0.96|45000.00|47000.00|125000|150000|14000|15000|Diagnostic Related Technologists And Technicians|
|641|890|0.96|45000.00|47000.00|323000|247000|13000|13000|Sales Representatives, Wholesale And Manufacturing|
|201|75|0.96|24000.00|25000.00|82000|68000|12500|13900|Personal Care Aides|
|45|39|0.96|48000.00|50000.00|130000|81000|12700|12500|Tax Preparers|
|205|300|0.96|50000.00|52000.00|200000|505000|12600|15000|Computer And Information Systems Managers|
|167|64|0.96|36600.00|38000.00|100000|85000|15000|18000|Other Education, Training, And Library Workers|
|148|51|0.96|40500.00|42000.00|140000|120000|15000|15000|Advertising And Promotions Managers|
|212|45|0.97|28000.00|29000.00|109000|93000|13000|14200|Medical Assistants|
|56|31|0.97|42500.00|44000.00|100000|77000|18000|30000|Tax Examiners And Collectors, And Revenue Agents|
|114|36|0.97|33150.00|34300.00|83000|111000|15000|19000|Payroll And Timekeeping Clerks|
|1207|922|0.97|31900.00|33000.00|163000|200000|12500|12500|First-Line Supervisors Of Retail Sales Workers|
|76|33|0.97|31000.00|32000.00|340000|68000|14000|18000|Correspondence Clerks And Order Clerks|
|167|110|0.97|31000.00|32000.00|140000|90000|12500|15000|News Analysts, Reporters And Correspondents|
|47|31|0.97|34000.00|35000.00|70000|110000|13800|15000|First-Line Supervisors Of Personal Service Workers|
|281|84|0.97|31200.00|32000.00|82000|95000|12500|15000|Word Processors And Typists|
|106|30|0.98|25000.00|25500.00|70000|41100|14000|15000|Nonfarm Animal Caretakers|
|3517|418|0.98|50000.00|51000.00|433000|165000|13000|13000|Registered Nurses|
|146|99|0.98|35000.00|35600.00|85000|64000|15600|23200|Probation Officers And Correctional Treatment Specialists|
|378|147|0.98|24000.00|24400.00|91000|55000|13000|13000|Tellers|
|52|36|0.99|27600.00|28000.00|190000|62000|13000|13600|Physical Therapist Assistants And Aides|
|744|3052|0.99|69000.00|70000.00|483000|587000|12500|13500|Software Developers, Applications And Systems Software|
|307|334|0.99|40000.00|40500.00|504000|250000|13000|13700|First-Line Supervisors Of Non-Retail Workers|
|245|784|0.99|41700.00|42000.00|135000|484000|12100|13000|Computer Support Specialists|
|117|272|0.99|28000.00|28150.00|86000|120000|12600|12200|Stock Clerks And Order Fillers|
|80|147|1.00|41500.00|41600.00|125000|120000|15000|15000|First-Line Supervisors Of Production And Operating|

### Equal pay

|# of women|# of men|ratio|women's median|men's median|women's max|men's max|women's minimum|men's minimum|occupation|
|-|-|-|-|-|-|-|-|-|-|
|57|138|1.00|70000.00|70000.00|185000|150000|20000|15300|Chemical Engineers|
|221|805|1.00|60000.00|60000.00|150000|355000|18000|12500|Civil Engineers|
|208|136|1.00|45000.00|45000.00|560000|134000|13000|14300|Compliance Officers|
|269|127|1.00|30000.00|30000.00|100000|71000|13000|14000|Data Entry Keyers|
|82|669|1.00|60000.00|60000.00|110000|120000|12200|12500|Mechanical Engineers|
|213|111|1.00|45000.00|45000.00|115000|95000|20000|15000|Medical Scientists, And Life Scientists, All Other|
|370|51|1.00|36000.00|36000.00|105000|120000|13000|15000|Meeting, Convention, And Event Planners|
|185|45|1.00|35000.00|35000.00|92000|68000|12600|12800|Miscellaneous Community And Social Service Specialists,|
|825|226|1.00|35000.00|35000.00|196000|100000|12400|13000|Miscellaneous Office And Administrative Support|
|117|61|1.00|37000.00|37000.00|110000|92000|15000|15000|Miscellaneous Social Scientists, Including Survey|
|196|189|1.00|55000.00|55000.00|120000|118000|15000|15100|Operations Research Analysts|
|138|87|1.00|52000.00|52000.00|190000|429000|22500|26000|Physicians And Surgeons|
|357|89|1.00|40000.00|40000.00|587000|380000|13000|15000|Public Relations Specialists|
|159|98|1.00|50000.00|50000.00|98000|148000|14000|13700|Purchasing Managers|
|244|185|1.00|30000.00|30000.00|90000|105000|13000|12200|Recreation And Fitness Workers|
|51|49|1.00|26000.00|26000.00|54000|42000|13700|14000|Residential Advisors|
|217|155|1.00|42000.00|42000.00|145000|183000|13000|14000|Sales And Related Workers, All Other|
|583|259|1.00|25000.00|25000.00|135000|105000|12600|12300|Waiters And Waitresses|
|266|139|1.00|40000.00|40000.00|483000|120000|12600|13000|Writers And Authors|




## People from age 30 - 39

### Pay favoring women

|# of women|# of men|ratio|women's median|men's median|women's max|men's max|women's minimum|men's minimum|occupation|
|-|-|-|-|-|-|-|-|-|-|
|45|45|0.81|62000.00|50000.00|613000|395000|20000|25000|Agents And Business Managers Of Artists, Performers,|
|65|80|0.84|100000.00|84000.00|196000|451000|34000|25000|Actuaries|
|47|62|0.85|47000.00|40000.00|116000|140000|20000|24000|First-Line Supervisors Of Protective Service Workers, All|
|179|108|0.87|52000.00|45000.00|538000|258000|13400|14400|Wholesale And Retail Buyers, Except Farm Products|
|38|35|0.87|30000.00|26000.00|70000|100000|13000|13000|Food Preparation Workers|
|147|79|0.87|63000.00|55000.00|229000|483000|15000|22000|Technical Writers|
|63|30|0.91|48000.00|43500.00|90000|170000|20000|15000|Physical Therapist Assistants And Aides|
|324|335|0.91|55000.00|50000.00|421000|260000|18500|15000|Biological Scientists|
|52|46|0.91|56500.00|51500.00|100000|140000|21600|15000|Biological Technicians|
|69|138|0.91|34000.00|31000.00|106000|120000|13200|14400|Shipping, Receiving, And Traffic Clerks|
|74|39|0.92|38000.00|35000.00|120000|140000|14000|16900|Correspondence Clerks And Order Clerks|
|99|98|0.93|48000.00|44400.00|150000|200000|15000|15000|Lodging Managers|
|35|71|0.93|43000.00|40000.00|100000|200000|16000|15000|Emergency Medical Technicians And Paramedics|
|90|205|0.93|45000.00|42000.00|93000|416000|15000|15000|Athletes, Coaches, Umpires, And Related Workers|
|35|374|0.94|80000.00|75000.00|200000|220000|16000|15000|Aircraft Pilots And Flight Engineers|
|127|143|0.94|48000.00|45000.00|429000|200000|15000|14400|News Analysts, Reporters And Correspondents|
|52|180|0.95|94500.00|90000.00|200000|200000|30000|30000|Chemical Engineers|
|3934|739|0.95|42000.00|40000.00|478000|482000|12900|12400|Social Workers|
|518|142|0.95|44000.00|42000.00|200000|150000|14400|13000|Other Therapists, Including Exercise Physiologists|
|530|142|0.96|45000.00|43000.00|120000|90000|13000|16000|Librarians|
|39|103|0.96|48000.00|46000.00|200000|360000|14700|20000|Musicians, Singers, And Related Workers|
|234|70|0.97|45000.00|43500.00|150000|110000|12900|15000|Miscellaneous Community And Social Service Specialists,|
|80|81|0.97|60000.00|58000.00|98000|130000|36000|35000|Urban And Regional Planners|
|170|429|0.97|75000.00|73000.00|160000|421000|20000|17800|Industrial Engineers, Including Health And Safety|
|128|451|0.97|40000.00|39000.00|113000|150000|15000|13000|Security Guards And Gaming Surveillance Officers|
|795|163|0.98|46000.00|45000.00|146000|110000|13200|15000|Special Education Teachers|
|309|71|0.98|49000.00|48000.00|160000|357000|15000|14000|Meeting, Convention, And Event Planners|
|107|96|0.98|60000.00|59000.00|130000|315000|20000|24000|Administrative Services Managers|
|549|49|0.99|86000.00|85000.00|459000|380000|16000|47000|Nurse Practitioners, And Nurse Midwives|
|142|865|0.99|90000.00|89000.00|180000|398000|16000|18000|Electrical And Electronics Engineers|
|54|38|0.99|60000.00|59500.00|417000|205000|32000|24000|Judicial Law Clerks|
|165|142|0.99|76000.00|75500.00|180000|426000|26000|18000|Miscellaneous Mathematical Science Occupations,|

## Pay favoring men

|# of women|# of men|ratio|women's median|men's median|women's max|men's max|women's minimum|men's minimum|occupation|
|-|-|-|-|-|-|-|-|-|-|
|258|171|0.66|50000.00|76000.00|467000|375000|12500|20000|Miscellaneous Legal Support Workers|
|126|88|0.68|46000.00|67500.00|225000|483000|20000|15000|Financial Specialists, All Other|
|342|367|0.71|50000.00|70000.00|560000|538000|14000|13000|Real Estate Brokers And Sales Agents|
|32|35|0.72|20300.00|28000.00|72000|96000|13000|15000|Packers And Packagers, Hand|
|62|249|0.73|24600.00|33800.00|54000|140000|12200|12500|Janitors And Building Cleaners|
|302|230|0.75|45000.00|60000.00|371000|410000|15000|17500|Production, Planning, And Expediting Clerks|
|237|507|0.75|60000.00|80000.00|613000|613000|13000|13000|Securities, Commodities, And Financial Services Sales|
|30|64|0.76|43000.00|56500.00|100000|162000|19700|21600|First-Line Supervisors Of Correctional Officers|
|99|76|0.77|46000.00|60000.00|150000|180000|14000|19500|Miscellaneous Health Technologists And Technicians|
|445|379|0.77|50000.00|65000.00|170000|539000|12500|16200|Property, Real Estate, And Community Association|
|83|103|0.78|35000.00|45000.00|180000|206000|15000|15000|Photographers|
|1487|876|0.78|47000.00|60000.00|359000|505000|12500|13000|First-Line Supervisors Of Office And Administrative|
|491|114|0.78|31000.00|39500.00|340000|120000|13000|12300|Receptionists And Information Clerks|
|156|129|0.79|48350.00|61000.00|451000|507000|14000|16000|Financial Clerks, All Other|
|32|113|0.79|33350.00|42000.00|120000|398000|14000|18000|Farmers, Ranchers, And Other Agricultural Managers|
|256|211|0.80|28000.00|35000.00|260000|200000|13000|12400|Cashiers|
|44|33|0.80|40000.00|50000.00|180000|110000|14900|12900|Credit Authorizers, Checkers, And Clerks|
|516|576|0.80|48000.00|60000.00|200000|413000|14900|14000|Credit Counselors And Loan Officers|
|1676|1670|0.80|60000.00|75000.00|505000|555000|13000|15000|Financial Managers|
|456|570|0.80|48000.00|60000.00|484000|658000|13000|12300|Insurance Sales Agents|
|388|762|0.81|64500.00|80000.00|483000|613000|15000|13200|Personal Financial Advisors|
|1524|1136|0.81|63000.00|78000.00|551000|555000|14400|13000|Marketing And Sales Managers|
|205|367|0.81|65000.00|80000.00|180000|637000|13000|15400|Database Administrators|
|69|172|0.81|30900.00|38000.00|78000|140000|13000|15000|Miscellaneous Assemblers And Fabricators|
|86|83|0.81|48000.00|59000.00|109000|120000|20000|21000|Tax Examiners And Collectors, And Revenue Agents|
|31|42|0.81|35000.00|43000.00|92000|100000|16000|15500|Gaming Services Workers|
|190|290|0.82|55000.00|67000.00|155000|150000|23100|20000|Detectives And Criminal Investigators|
|66|277|0.82|27350.00|33300.00|65000|170000|15000|13000|Laborers And Freight, Stock, And Material Movers, Hand|
|55|41|0.82|47000.00|57000.00|90000|360000|26000|25000|Respiratory Therapists|
|203|40|0.82|33000.00|40000.00|116000|105000|12400|18800|Medical Assistants|
|3941|4741|0.82|66000.00|80000.00|483000|658000|14000|13000|Miscellaneous Managers, Including Funeral Service|
|52|142|0.83|52000.00|63000.00|180000|200000|19600|15000|Cost Estimators|
|119|183|0.83|52000.00|63000.00|118000|324000|15000|14100|Logisticians|
|636|321|0.83|62000.00|75000.00|399000|459000|16000|20000|Human Resources Managers|
|339|263|0.83|62000.00|75000.00|160000|658000|19000|24000|Purchasing Managers|
|39|93|0.83|43000.00|52000.00|120000|170000|13000|18000|Supervisors Of Transportation And Material Moving Workers|
|105|48|0.83|40000.00|48300.00|130000|200000|16600|15000|Information And Record Clerks, All Other|
|787|244|0.83|39000.00|46900.00|322000|480000|12300|14000|Bookkeeping, Accounting, And Auditing Clerks|
|95|59|0.83|40000.00|48000.00|100000|130000|14000|13000|Reservation And Transportation Ticket Agents And Travel|
|453|805|0.83|60000.00|72000.00|455000|475000|14900|17100|Sales Representatives, Services, All Other|
|439|116|0.84|35600.00|42500.00|140000|175000|14000|14000|Billing And Posting Clerks|
|96|30|0.84|36500.00|43500.00|109000|125000|14000|15000|Interviewers, Except Eligibility And Loan|
|720|41|0.84|59000.00|70000.00|421000|235000|18000|15000|Speech Language Pathologists|
|5208|3032|0.84|54000.00|64000.00|613000|507000|13000|14500|Accountants And Auditors|
|76|31|0.84|38000.00|45000.00|88000|100000|20000|24000|Court, Municipal, And License Clerks|
|197|71|0.84|76000.00|90000.00|392000|483000|20000|18000|Veterinarians|
|580|428|0.85|55000.00|65000.00|325000|380000|14400|13800|Business Operations Specialists, All Other|
|159|123|0.85|50000.00|59000.00|467000|230000|12800|15000|Miscellaneous Social Scientists, Including Survey|
|116|173|0.85|50000.00|59000.00|110000|145000|28500|20000|Private Detectives And Investigators|
|59|264|0.85|70000.00|82500.00|125000|211000|26000|27000|Information Security Analysts|
|178|372|0.85|42500.00|50000.00|421000|140000|14400|14100|Bailiffs, Correctional Officers, And Jailers|
|1798|888|0.85|51000.00|60000.00|483000|555000|12500|13400|Education Administrators|
|290|297|0.85|64000.00|75000.00|292000|403000|15000|17000|Sales And Related Workers, All Other|
|198|367|0.85|114500.00|134000.00|429000|613000|18700|15100|Dentists|
|106|124|0.86|29500.00|34500.00|93000|110000|13000|13000|Bartenders|
|164|55|0.86|40450.00|47300.00|140000|360000|18000|13000|Loan Interviewers And Clerks|
|102|65|0.86|60000.00|70000.00|414000|200000|14000|24000|Advertising And Promotions Managers|
|271|233|0.86|60000.00|70000.00|577000|539000|13000|20000|Advertising Sales Agents|
|276|256|0.86|60000.00|70000.00|140000|373000|22100|21000|Chemists And Materials Scientists|
|771|971|0.86|60000.00|70000.00|613000|587000|13600|14000|First-Line Supervisors Of Non-Retail Workers|
|751|443|0.86|60000.00|70000.00|230000|587000|18000|15000|Market Research Analysts And Marketing Specialists|
|109|35|0.86|30000.00|35000.00|58000|163000|12500|12500|Nonfarm Animal Caretakers|
|1004|941|0.86|130000.00|151000.00|613000|582000|14000|13300|Physicians And Surgeons|
|239|176|0.86|26800.00|31000.00|130000|90000|12600|12900|Waiters And Waitresses|
|119|206|0.87|52000.00|60000.00|190000|394000|15000|14000|Artists And Related Workers|
|161|45|0.87|39000.00|45000.00|130000|117000|17000|20000|Payroll And Timekeeping Clerks|
|255|161|0.87|52000.00|60000.00|392000|180000|18000|13500|Training And Development Specialists|
|454|167|0.87|33000.00|38000.00|399000|393000|13000|15000|Nursing, Psychiatric, And Home Health Aides|
|307|68|0.87|36500.00|42000.00|297000|110000|12200|15000|Word Processors And Typists|
|623|869|0.87|60000.00|69000.00|417000|551000|16000|15000|General And Operations Managers|
|40|167|0.87|65500.00|75000.00|134000|183000|24000|14000|First-Line Supervisors Of Police And Detectives|
|136|67|0.88|35000.00|40000.00|114000|220000|13000|18000|Bill And Account Collectors|
|83|194|0.88|35000.00|40000.00|135000|455000|12500|14000|Other Production Workers, Including Semiconductor|
|255|187|0.88|57000.00|65000.00|215000|421000|18000|13200|Insurance Underwriters|
|62|108|0.88|82500.00|94000.00|398000|230000|16000|25000|Economists|
|124|294|0.88|45750.00|52000.00|150000|400000|15000|13000|Engineering Technicians, Except Drafters|
|160|103|0.88|66000.00|75000.00|126000|150000|15000|25000|Budget Analysts|
|1177|457|0.88|60000.00|68000.00|398000|483000|13000|14000|Medical And Health Services Managers|
|193|782|0.88|60000.00|68000.00|200000|230000|16000|16000|Network And Computer Systems Administrators|
|723|879|0.88|60000.00|68000.00|392000|475000|14000|13500|Physical Scientists, All Other|
|392|312|0.88|53000.00|60000.00|200000|393000|20000|18000|Purchasing Agents, Except Wholesale, Retail, And Farm|
|338|268|0.88|53000.00|60000.00|560000|483000|13100|15000|Writers And Authors|
|67|105|0.88|44200.00|50000.00|120000|130000|15000|14000|Computer Operators|
|87|109|0.89|31000.00|35000.00|90000|150000|13000|13000|First-Line Supervisors Of Food Preparation And Serving|
|46|31|0.89|70000.00|79000.00|142000|140000|36000|23000|Radiation Therapists|
|413|759|0.89|80000.00|90000.00|491000|635000|12400|12500|Chief Executives And Legislators|
|64|51|0.89|40000.00|45000.00|100000|421000|15000|15600|First-Line Supervisors Of Personal Service Workers|
|1163|1356|0.89|40000.00|45000.00|440000|426000|13000|12500|First-Line Supervisors Of Retail Sales Workers|
|91|46|0.89|40000.00|45000.00|200000|200000|18000|20000|Miscellaneous Media And Communication Workers|
|879|280|0.89|40000.00|45000.00|440000|180000|13000|15000|Miscellaneous Office And Administrative Support|
|58|56|0.89|37400.00|42000.00|107000|100000|14300|15000|Directors, Religious Activities And Education|
|1276|1154|0.89|50000.00|56000.00|455000|455000|13000|15000|Designers|
|308|84|0.89|25000.00|28000.00|200000|90000|12200|14500|Teacher Assistants|
|375|267|0.89|42000.00|47000.00|102000|230000|16000|17600|Probation Officers And Correctional Treatment Specialists|
|1729|6668|0.89|85000.00|95000.00|483000|613000|12500|13000|Software Developers, Applications And Systems Software|
|523|346|0.90|60000.00|67000.00|403000|642000|18000|15000|Compliance Officers|
|962|1703|0.90|69000.00|77000.00|613000|560000|15000|13800|Computer Systems Analysts|
|51|220|0.90|84000.00|93500.00|180000|419000|26000|14000|Computer Hardware Engineers|
|673|1566|0.90|80000.00|89000.00|205000|421000|15000|13500|Computer And Information Systems Managers|
|466|215|0.90|40000.00|44500.00|410000|160000|14000|17000|Insurance Claims And Policy Processing Clerks|
|456|1799|0.90|72000.00|80000.00|421000|483000|13000|13900|Computer Programmers|
|1978|599|0.90|54000.00|60000.00|478000|399000|12500|18000|Human Resources Workers|
|1154|1341|0.90|72000.00|80000.00|483000|483000|13100|13000|Management Analysts|
|770|208|0.90|45000.00|50000.00|538000|484000|15000|14000|Paralegals And Legal Assistants|
|233|203|0.90|36000.00|40000.00|120000|122000|12700|14000|Recreation And Fitness Workers|
|754|1128|0.90|45000.00|50000.00|504000|507000|12300|13000|Retail Salespersons|
|468|78|0.91|67000.00|74000.00|480000|120000|15000|38000|Occupational Therapists|
|388|187|0.91|54500.00|60000.00|333000|150000|15000|15000|Diagnostic Related Technologists And Technicians|
|81|86|0.91|50000.00|55000.00|115000|185000|14000|24800|Chemical Technicians|
|75|79|0.91|50000.00|55000.00|200000|300000|31000|25000|Credit Analysts|
|183|107|0.91|40000.00|44000.00|115000|315000|12900|16800|Dispatchers|
|96|72|0.91|95000.00|104500.00|404000|456000|21000|16000|Optometrists|
|45|40|0.91|35000.00|38500.00|96000|125000|14000|15000|Religious Workers, All Other|
|54|155|0.91|50000.00|55000.00|129000|155000|24000|18000|Surveyors, Cartographers, And Photogrammetrists|
|283|314|0.91|71000.00|78000.00|483000|658000|20000|15000|Financial Analysts|
|44|317|0.91|41000.00|45000.00|150000|298000|18000|13100|Computer, Automated Teller, And Office Machine Repairers|
|49|96|0.92|65000.00|71000.00|120000|298000|41000|30000|Environmental Engineers|
|47|119|0.92|55000.00|60000.00|150000|480000|24000|15000|Chiropractors|
|156|336|0.92|55000.00|60000.00|185000|507000|13000|15600|First-Line Supervisors Of Production And Operating|
|13608|3744|0.92|45000.00|49000.00|655000|451000|12900|13000|Elementary And Middle School Teachers|
|685|485|0.92|45000.00|49000.00|467000|451000|13000|13000|Other Teachers And Instructors|
|31|139|0.92|92000.00|100000.00|170000|180000|30000|28000|Air Traffic Controllers And Airfield Operations|
|60|208|0.92|46000.00|50000.00|110000|165000|18600|14300|Drafters|
|261|536|0.92|60000.00|65000.00|140000|283000|14000|20000|Architects, Except Naval|
|1031|44|0.92|33000.00|35750.00|175000|100000|12100|16000|Preschool And Kindergarten Teachers|
|5217|755|0.92|60000.00|65000.00|467000|658000|12200|12600|Registered Nurses|
|343|647|0.92|60000.00|65000.00|215000|393000|18000|13000|Web Developers|
|117|797|0.93|37000.00|40000.00|80000|130000|13000|12500|Clergy|
|231|84|0.93|44000.00|47500.00|110000|94000|14000|13000|Eligibility Interviewers, Government Programs|
|3206|251|0.93|38000.00|41000.00|613000|250000|12400|14000|Secretaries And Administrative Assistants|
|111|596|0.93|65000.00|70000.00|173000|404000|24000|14000|Construction Managers|
|42|34|0.93|27500.00|29550.00|104000|55000|15100|13000|Hotel, Motel, And Resort Desk Clerks|
|40|66|0.93|46000.00|49400.00|75000|108000|22000|18000|Postal Service Mail Carriers|
|256|146|0.93|34000.00|36500.00|138000|150000|13000|14000|Data Entry Keyers|
|250|288|0.93|42000.00|45000.00|273000|560000|15000|15000|Food Service Managers|
|1071|705|0.93|112000.00|120000.00|382000|560000|13000|13000|Pharmacists|
|839|469|0.93|70000.00|75000.00|507000|475000|15000|15000|Physical Therapists|
|119|31|0.94|37400.00|40000.00|123000|276000|14000|19500|Medical Records And Health Information Technicians|
|118|207|0.94|65500.00|70000.00|150000|410000|15000|21000|Industrial Production Managers|
|66|266|0.94|60000.00|64000.00|120000|150000|19000|17000|Military, Rank Not Specified|
|85|50|0.94|75000.00|80000.00|175000|484000|25000|15000|Natural Sciences Managers|
|415|417|0.94|75000.00|80000.00|220000|505000|23700|16000|Operations Research Analysts|
|2019|1397|0.94|47000.00|50000.00|426000|200000|13000|14000|Secondary School Teachers|
|443|2095|0.94|80000.00|85000.00|467000|483000|13000|14400|Miscellaneous Engineers, Including Nuclear Engineers|
|80|73|0.94|65000.00|69000.00|230000|200000|13800|26000|Training And Development Managers|
|561|503|0.94|50000.00|53000.00|175000|209000|14000|24000|Claims Adjusters, Appraisers, Examiners, And|
|63|368|0.94|85000.00|90000.00|240000|285000|32800|15000|Computer Network Architects|
|166|67|0.94|68000.00|72000.00|225000|160000|15000|30200|Public Relations And Fundraising Managers|
|454|1386|0.95|52500.00|55500.00|180000|440000|12100|14000|Computer Support Specialists|
|368|1753|0.95|61500.00|65000.00|150000|170000|15400|14000|Police Officers|
|62|90|0.95|53000.00|56000.00|131000|148000|22000|20000|Agricultural And Food Scientists|
|836|273|0.95|36000.00|38000.00|130000|379000|13000|12400|Office Clerks, General|
|58|158|0.95|25500.00|26900.00|56000|85000|12500|14000|Cooks|
|94|796|0.95|75000.00|79000.00|132000|164000|27000|13000|Mechanical Engineers|
|37|53|0.95|38000.00|40000.00|83000|125000|16000|18000|Lifeguards And Other Recreational, And All Other|
|1760|1180|0.95|39000.00|41000.00|410000|491000|13000|12500|Customer Service Representatives|
|337|87|0.95|40000.00|42000.00|234000|180000|14000|13000|Social And Human Service Assistants|
|431|1451|0.96|67000.00|70000.00|250000|419000|18000|13000|Computer Occupations, All Other|
|572|160|0.96|59000.00|61500.00|189000|175000|13000|22000|Psychologists|
|276|398|0.96|48000.00|50000.00|183000|331000|13000|13000|Inspectors, Testers, Sorters, Samplers, And Weighers|
|221|108|0.96|27000.00|28000.00|135000|205000|12700|13000|Personal Care Aides|
|104|543|0.97|86000.00|89000.00|140000|180000|35000|15000|Aerospace Engineers|
|192|321|0.97|58000.00|60000.00|237000|346000|15000|15000|Environmental Scientists And Geoscientists|
|35|125|0.97|58000.00|60000.00|112000|188000|24000|20000|First-Line Supervisors Of Mechanics, Installers, And|
|132|69|0.97|46500.00|48000.00|115000|108000|12100|12800|Archivists, Curators, And Museum Technicians|
|50|150|0.97|50500.00|52000.00|108000|120000|15000|20000|Conservation Scientists And Foresters|
|372|141|0.97|34000.00|35000.00|292000|431000|14000|14000|Health Practitioner Support Technologists And Technicians|
|1047|1688|0.97|70000.00|72000.00|539000|560000|12500|12500|Sales Representatives, Wholesale And Manufacturing|
|308|34|0.97|53000.00|54500.00|560000|404000|19000|29000|Dietitians And Nutritionists|
|323|1348|0.97|74000.00|76000.00|292000|491000|21200|12200|Civil Engineers|
|222|107|0.97|38000.00|39000.00|421000|95000|14000|13000|File Clerks|
|1818|1484|0.97|78000.00|80000.00|555000|613000|14000|12300|Lawyers, And Judges, Magistrates, And Other Judicial|
|126|69|0.98|140000.00|143000.00|331000|358000|20000|17000|Nurse Anesthetists|
|151|54|0.98|50000.00|51000.00|175000|185000|14000|21600|Compensation, Benefits, And Job Analysis Specialists|
|203|194|0.98|50000.00|51000.00|355000|146000|18000|14400|Other Healthcare Practitioners And Technical|
|39|112|0.98|109000.00|111000.00|327000|466000|29000|28000|Petroleum, Mining And Geological Engineers, Including|
|205|248|0.98|55000.00|56000.00|403000|455000|12600|18000|Producers And Directors|
|63|312|0.99|100000.00|101000.00|230000|491000|20000|23100|Architectural And Engineering Managers|
|220|68|0.99|27000.00|27250.00|130000|419000|12200|15000|Tellers|
|384|166|0.99|59000.00|59500.00|270000|265000|13000|15000|Public Relations Specialists|

### Equal pay

|# of women|# of men|ratio|women's median|men's median|women's max|men's max|women's minimum|men's minimum|occupation|
|-|-|-|-|-|-|-|-|-|-|
|52|108|1.00|50000.00|50000.00|105000|421000|15000|15000|Appraisers And Assessors Of Real Estate|
|36|96|1.00|30000.00|30000.00|100000|65000|14000|13500|Chefs And Head Cooks|
|687|247|1.00|50000.00|50000.00|187000|392000|12400|14000|Clinical Laboratory Technologists And Technicians|
|2447|786|1.00|43000.00|43000.00|403000|340000|12400|12500|Counselors|
|332|304|1.00|50000.00|50000.00|210000|190000|15000|15000|Editors|
|335|72|1.00|55000.00|55000.00|198000|120000|17800|15000|Fundraisers|
|51|31|1.00|30000.00|30000.00|68000|55000|13000|15000|Library Assistants, Clerical|
|582|432|1.00|55000.00|55000.00|235000|375000|15000|13800|Medical Scientists, And Life Scientists, All Other|
|265|207|1.00|45000.00|45000.00|170000|240000|13000|15000|Miscellaneous Life, Physical, And Social Science|
|298|121|1.00|50000.00|50000.00|200000|371000|14000|15000|Other Education, Training, And Library Workers|
|350|130|1.00|90000.00|90000.00|456000|421000|19500|20000|Physician Assistants|
|2168|2095|1.00|50000.00|50000.00|551000|550000|12200|13000|Postsecondary Teachers|
|810|313|1.00|50000.00|50000.00|587000|421000|15000|15000|Social And Community Service Managers|
|153|287|1.00|32000.00|32000.00|114000|200000|12600|12300|Stock Clerks And Order Fillers|
|82|56|1.00|57000.00|57000.00|175000|390000|17500|28600|Tax Preparers|
|95|176|1.00|63000.00|63000.00|158000|577000|20000|12800|Transportation, Storage, And Distribution Managers|


<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
