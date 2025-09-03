# Description
Construct a data pipeline capable of retrieving, normalising and storing data in AWS (Amazon Web Services) environment.

## Requirements
- Solution should utilise Apache Airflow and AWS solutions.
- Code should be written in Python.
- Data should be normalised as much as possible.
- Final data should be stored on AWS S3 or one of the AWS databases ([RDS](https://aws.amazon.com/free/database/), [DynamoDB](https://aws.amazon.com/dynamodb), etc.).
- At least two unit tests should be created.

## Data
- You can find dataset in data directory as `Open_DataRDW.csv` file.
- Dataset is an open data subset from https://opendata.rdw.nl/.

## Data processing & normalisation
- Vehicle type - `Voertuigsoort` - should be normalised to English term. Same goes for body type (`Inrichting`) and colour (`Eerste kleur`).
- All date fields should be converted to ISO-8601 timezone-aware datetime format.
- Any `N.v.t.` null values in colour column should be correctly translated to final output (e.g. empty for CSV, `null` for DBs).

## Hints and suggestions
- [AWS Free Tier](https://aws.amazon.com/free/) should be sufficient for all the necessary work.
- AWS resources can be either created manually by using AWS console, or deployed using frameworks such as [Terraform](https://developer.hashicorp.com/terraform) or [Serverless](https://www.serverless.com/).
