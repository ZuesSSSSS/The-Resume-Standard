# Proposal: The **Resume** Standard

## *Created / Proposed: Sept. 24 2022*

<p align="center">
    <b>Contact Me</b>
    <br>David Mudriy
    <br>Davidmudriy@pm.me
</p>

### Summary

The intention of a resume (also called a CV) is to present a simple document to show experience, skills, and accomplishments. But as many know, they can vary wildly; be undeveloped, and be random.
But on top of that, in the day and age of signing up for jobs online, one resume should fill in all the fields that jobs should need.
We propose a resume schema to save developers, employees, and employers time and money.
**Save time writing and apply more.**

### Terminology

| Words | Definition (Merriam-Webster) | Example Usage |
| ----- | ---------- | ------------- |
| Resume | A short account of one's career and qualifications | He gave a resume of the club's activities throughout the year. |
| CV (Curriculum vitae) |  A short account of one's career and qualifications prepared typically by an applicant for a position | Charnley has a doctorate in toxicology from Massachusetts Institute of Technology and has served on multiple government and industry advisory panels, according to her curriculum vitae. |

### Background

The problem with applying with resumes came primarily on the internet.
It got much easier to apply to jobs farther away, like remote jobs. But, the lack of format and standard took more time to apply. So I aim to solve that by standardizing a .resume format.

### Assumptions

This solution of standardizing resumes comes with the requirements that companies use the standard for it to work.

### Proposed Solution

|     Field      |  Type  | Required |         Supported Formats         |              Purpose              |
| -------------- | ------ | -------- | --------------------------------- | --------------------------------- |
| Name           | any    | Depends  | [Name](#name)                     | Define whom it is                 |
| Phone          | number | Depends  | [Phone](#phone)                   |
| Email          | string | Depends  | [Email](#email)                   | Contact (Only 1 form required)    |
| Location       | any    | true     | [Location](#location)             | Taxes/Onboarding, Legalities, etc |
| Experience     | any    | false    | [Experience](#experience)         | Share previous professional experience |
| Projects       | any    | false    | [Projects](#projects)             | Show skills off and use as experience |
| Skills         | any    | false    | [Skills](#skills)                 | Set job search aim with skills and show defining abilities |
| Certifications | any    | false    | [Certifications](#certifications) | Show industry licenses/Certifications |
| Links          | any    | false    | [Links](#links)                   | Show projects and show skills |

TODO: Resume Creator + Reader Link

### Name

- Type: any;
- Required: Yes;

      Supported
         "Name": {
               "first": string;
               "middle": string;
               "last": string;
            }

      Example
         "Name": {
               "first": "Bob",
               "middle": "Alex",
               "last": "Smith"
            }

### Phone

[Wikipedia](https://wikipedia.org/wiki/Telephone_number)

- Type: number;
- Required: Depends; (One form of contact required)

      Supported
         "Phone": number;

      Example
         "Phone": "111-111-1111",

### Email

[Regex](https://emailregex.com/)

- Type: string;
- Required: Depends; (One form of contact required)

      Supported
         "Name": string;

      Example
         "Name": "davidmudriy@pm.me",

### Location

- Type: any;
- Required: true;

      Supported
         "Location": {
            "city": string;
            "region": string;
            "country": string;
         }

      Example
         "Location": {
            "city": "Portland",
            "region": "Oregon",
            "country": "US"
         }

### Experience

- Type: any;
- Required: false;

      Supported
         "Experience": [
            {
               "title": string; 
               "company": string; 
               "startDate": string; // (yyyy-mm-dd),
               "endDate": string;  // (yyyy-mm-dd),
               "descriptions": any; // array
            }
         ]

      Example
         "Experience": [
               {
                  "title": "Developer",
                  "company": "Google",
                  "startDate": "2022-01-01", // (yyyy-mm-dd),
                  "endDate": "2022-12-25", // (yyyy-mm-dd),
                  "descriptions": {
                     "Built stuff",
                     "Doing things"
                  }
               }
         ]

### Projects

- Type: any;
- Required: false;

      Supported
         "Experience": [
            {
               "title": string; 
               "company": string; 
               "startDate": string; // (yyyy-mm-dd),
               "endDate": string;  // (yyyy-mm-dd),
               "descriptions": any; // array
            }
         ]

      Example
         "Experience": [
            {
               "title": "Developer",
               "company": "Google",
               "startDate": "2022-01-01",
               "endDate": "2022-12-25",
               "descriptions": {
                  "Built stuff",
                  "Doing things"
               }
            }
         ]

### Skills

- Type: any;
- Required: false;

      Supported
         "Skills": [
            ""
         ]

      Example
         "Skills": [
            "Coding",
            "Writing"
         ]

### Certifications

- Type: any;
- Required: false;

      Supported
         "Certifications": [
            {
               "Certification": string; 
               "IssueDate": string; // (yyyy-mm-dd),
               "ExpDate": string; // (yyyy-mm-dd),
               "ID": string;
               "Link": any; // array
            }
         ]

      Example
         "Certifications": [
            {
               "Certification": "CCNA"; 
               "IssueDate": "2020-01-10"; // (yyyy-mm-dd),
               "ExpDate": "2022-10-15"; // (yyyy-mm-dd),
               "ID": "234988243";
               "Link": [
                  "https://Certmetrics.com"
               ]
            }
         ]

### Links

- Type: any;
- Required: false;

      Supported
         "Skills": any;

      Example
         "Links": [
            "https://github.com/thundeR2GE"
         ]
