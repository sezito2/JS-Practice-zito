# "DEAR GOVERNOR": AN EPISTOLARY JOURNEY THROUGH THE CIVIL RIGHTS MOVEMENT IN NC

- [Original Site](https://sites.google.com/ncsu.edu/eng798projectsite/home?authuser=0)
- [GH Repo](https://github.com/hmkinsler/eng798project/tree/main)

## Data Overview

- 71 letters to the North Carolina governor from residents as well as responses sent back to those residents.
    - Letters downloaded from [North Carolina Digital Collections](https://digital.ncdcr.gov/collections/civil-rights) relating to the Civil Rights Movement.

### Fields

- record_unit
- title
- description
- sent_date
- unformatted_date
- sender_1
- sender_2
- sender_race
- event
- stance
- hyperlink
- cleaning_status
- notes
- transcript

## Project Authors

BRODY MCCURDY

- Oral Historian
- PhD Student in Communication, Rhetoric, & Digital Media at North Carolina State University
- bjmccurd@ncsu.edu

HALEY M. KINSLER

- Oral Historian
- PhD Student in Communication, Rhetoric, & Digital Media at North Carolina State University
- hmkinsle@ncsu.edu

### Project Overview

This course project was focused on exploring the larger context of civil rights history in North Carolina, particularly as a continuation of our efforts working on the Fourth Ward Oral History Project, an oral history and community archive project which documents the experiences of Raleigh residents who were displaced from the Fourth Ward, a predominantly Black neighborhood that was demolished as a result of urban renewal between 1968 and 1975. For this reason, this course project will be guided by many of the same values that have been informative for our work with Black residents in Raleigh and the Fourth Ward Historic Neighborhood Association. Critically, these values have been formed over time out of collaboration with those residents, as well as scholarship exploring issues of epistemic injustice in research and the implications this has for researchers who are seeking to preserve and document Black history. This project, then, is part of a legacy of work in public Black history that has been stewarded by scholars like Carter G. Woodson, Madeline Morgan, John Hope Franklin, and many others whose efforts are not listed here but offer much insight that informs our efforts to both make Black history publicly accessible and to do so as part of active efforts to advocate for justice for Black communities in Raleigh. We recognize that these efforts did not start and will not end with our project, however, and we are grateful to local historians and organizers including Carmen Cauthen, Octavia Rainey, and the Wake County Housing Justice Coalition, all of whom have offered their guidance and expertise in the intersection between scholarship and activism.

Though this project is not explicitly focused on the Fourth Ward, we situate our work within the communities that we are rooted, and our close and ongoing connection to the neighborhood association motivates our drive to further document and celebrate the history of all Black North Carolinians. To do so, we drew on guidance from digital humanities scholars, thinking reflexively about how we might make our own research process for exploring discursive and linguistic patterns visible. Drawing on Posner's (2014) guidance for how to document this work, you can explore our approach to different stages of this digital humanities project.

## OUR ASSETS: THE DATA WE USED IN THIS PROJECT

We worked with materials from a collection on materials relating to the Civil Rights Movement that were compiled for the North Carolina Digital Collections, which in total included 174 different items including archival photographs, activist pamphlets, governmental memoranda, resolutions, and more. Given the wide variety of mediums present in the collection, however, we opted to narrow our focus to collection of letters that had been to the North Carolina governor from residents as well as responses sent back to those residents.

## OUR SERVICES: OUR METHODS AND HOW WE WORKED WITH OUR DATA

To ensure that we worked with a manageable amount of textual material, we further reduced the data to a collection of 71 total letters that were typed. Though we initially attempted to make use of our own optical character recognition scripts to automate transcription of these letters (Cordell, 2019), we found during our review of the script's output that the digital collection's automatic transcription feature was often more accurate. From there, we corrected these transcripts manually and qualitatively coded them and added metadata for each transcript including things like...

- Author's stance on Civil Rights issues
- Geographic location for where letters were sent from or to
- The date that the letter was sent
- Whether a letter was reciprocated with a response
- The race of the author, when disclosed

## OUR PRESENTATION: HOW WE MADE THIS WORK ACCESSIBLE

To identify linguistic patterns in the transcripts and determine whether additional variables (i.e. race, stance) played a role in the distribution of particular linguistic phenomena, we made use of packages for social network analysis such as ggraph (Pederson, 2025) and igraph (Csardi & Nepusz, 2006) in R to create various network visualizations, including. Additional visualizations were created to trial further approaches in different textual, spatial, or quantitative patterns in the number of letters, their geographic paths, and so on. Further visualizations were again created using R, and maps were created using QGIS.