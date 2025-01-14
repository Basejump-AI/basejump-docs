# Data Governance

Due to the democratization of access to the database that the Basejump AI platform will enable, Users will generate data objects faster than ever. This effect of improved access leading to increased utilization is known as [Jevon's paradox](https://en.wikipedia.org/wiki/Jevons_paradox).

Because of this, an AI data analytics solution is incomplete without data governance. We provide tools for User's to easily share their data objects and compare them to understand their differences. Traditional BI tools have made dashboards a priority with typically no data governance included. This led to a proliferation of dashboards with no easy way to compare them except to ask the data analysts why towo dashboards are showing different numbers for the same metric.

![Comic strip showing the prolifireation of information with no data governance](/images/marketoonist_comic_strip.png)

It is imperative for an AI data analytics solution to provide means to compare and understand all of the data that is being retrieved and not miss an opportunity for built-in data governance.

One tool we provide to help understand the data is every piece of retrieved data has the original SQL query included. For User's on the same Team to compare their data objects, they can select the context menu within a data object and select 'Compare'.

![Showing the 'Compare' selection on a metric](/images/data/compare_metric.png)

Our AI tool will then compare the data in the two data objects and explain to the user how they compare using one of 4 designations (in order of similarity - most similar first):

Similarity   | Description
---    | ---
Identical | There are no differences between the queries used to retrieve the data.
Equivalent | The output and tables are the same, but queries are structured differently.
Similar | The queries share some or all tables, but the output is different.
Different |  The queries share no tables.

![Comparing two data objects](/images/data/data_comparison.png)

We're offering the capability for organizations to go from first principles and original data sources to curate unique insights for the business that will transform the business into a truly data-driven enterprise like never before. Data governance does not have to mean restricting which metrics can be used, but rather improved transparency on the data that is being used and shared.

# Metadata

A fundamental aspect of good data governance is documentation. We provide the option to add metadata to every table and column in your data and define how they relate to each other. This not only improve the documentation on your data sources, but also improves the context for the AI in order to retrieve the most relevant data.

![Editing metadata](/images/datasources/edit_metadata.png)

# Data Modeling

In order to be most successful using the Basejump AI platform, the tables you provide need to be clear enough that you can document the relationships clearly. Not all tables in your database ned to be added to Basejump, just the most clean tables at the end of your ETL pipeline that you want to provide to users.

The relationships you define will be shown as an ERD diagram in our 'Explore' page to help users understand relationships between tables.

![Image of the ERD diagram](/images/explore/explore_erd_diagram.png)

For more information, please refer to the explore page:

[!ref](/sidebar-options/member-options/explore.md)