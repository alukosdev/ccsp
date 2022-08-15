# Data Discovery

## Glossary

==- Mapping
Enables an organization to know all of the locations where data is present within an application and within other storage. Allows for the ability to implement security controls and policies by understanding what type of data is present in the system.
==-

## Overview

Discovery is a process for identifying and providing visibility into the location, volume, and context of structured and unstructured data stored in a variety of data repositories.

Data discovery is a term that can be used to refer to several kinds of tasks:

- The organization is attempting to create that initial inventory of data it owns.
- The organization is involved in electronic discovery ("eDiscovery" is the legal term for how electronic evidence is collected as part of an investigation or lawsuit).
- The modern use of datamining tools to discover trends and relations in the data already in the organization's inventory.

The goal of data discovery is to work with and enable people to use their intuition to find meaningful and important information in data.

!!!
The difference between *data discovery* and *eDiscovery* is that data discovery is typically used for big data or analytics whereas eDiscovery is used for evidence.
!!!

## Data Discovery Process

- *Implement data discovery*. Helps determine where data is stored.
- *Classify discovered data*. Helps determine the types of data that must be protected.
- *Map and define controls*. Helps ensure the controls that are implemented comply with data privacy acts and provide coverage of their tenets
- *Apply controls*.

## Data Discovery Issues

- Poor data quality.
- Dashboards.
- Hidden costs.

## Data Discovery Challenges

- *Identifying where your data is*. Not knowing where the data is can make finding your data a challenge.
- *Accessing the data*. Who has access to what data? Once you find the data to be analyzed, does the analysis process have access to it in a useable way?
- *Performing preservation and maintenance*. How will the data be preserved and by whom? Preservation needs to be spelled out in an SLA.

## Data Discovery Types

### Label-Based Discovery

Labels are used to group data elements together and provide information about those elements.

With accurate and sufficient labels, the organization can readily determine what data it controls, and what amounts of each kind. Based on examining labels created by the data owners during the Create phase (during content creation). Labels can be used with *databases* as well as *flat files*. The *indexed sequential access method* is used with labels.

!!!
Similar to metadata, but less formal. This form of discovery is similar to a Google search, with the greater the number of similar labels, the greater likelihood of a match. This typically is more used with flat files in ISAM or quasi-relational data storage.
!!!

### Metadata-Based Discovery

Metadata is a listing of traits and characteristics about specific data elements or sets (colloquially referred to as "data about data"). It is often automatically created at the same time as the data, often by the hardware or software used to create the parent data. Data can be retrieved on a specific set of metadata.

!!!
You could examine column attributes to determine whether the name of the column or the size and data type resembles a credit card number (for example, if the column is a 16-digit number or the name resembles "CC"). This remains the most common analysis technique.
!!!

### Content-Based Discovery

Discovery tools can be used to locate and identify specific kinds of data by delving into the content of datasets. This technique can be as basic as term searches or can use sophisticated pattern-matching technology. Can often take longer than the other two methods of discovery.

!!!
In the credit card example, a common method is to perform a Luhn check on the number. This is a numeric checksum used by credit card companies to verify if a number is valid (resembles a credit card number).

This is a growing trend also used successfully in DLP and web content analysis products.
!!!

Content analysis utilizes pattern matching, hashing, statistics, lexical, or other forms of probability analysis. DLP uses content analysis.

Content-based discovery uses characteristics such as:

- Keywords
- Pattern matching
- Frequency

## Data Analytics

### Data Mining

### Real-Time Analytics/Real-User Monitoring

Allows for reactive and predictive operations based on customers' current and past shopping behavior.

- Most closely measures actual activity.
- Harvests information from actual user activity, making it the most realistic depiction of user behavior.
- Can sometimes reveal personal information.
- Allows for reactive and predictive operations (such as recommending other, related products) based on customers' current and past shopping behavior.

### Agile Business Intelligence

A data discovery approach that offers insight to *trends of trends*, using both historical and predictive approaches.

The Agile approach to data analysis offers greater insight and capabilities than previous generations of analytical technologies.

### Synthetic Performance Monitoring

Synthetic agents can simulate user activity in a much faster manner than real-user monitoring and perform these actions without rest. Synthetic performance monitoring approximates user activity and thus, is not as accurate as RUM.
