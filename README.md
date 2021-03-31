# AzureML-BearingFailurePrediction
Example AzureML Notebook that interfaces with Seeq to both provide data for training and validation as well as operationalizing the output. This notebook was created and shared for a webinar done with Seeq and Microsoft [Accelerate Operational Analytics](https://info.seeq.com/microsoft-azure-webinar-download). 

# Getting up and running

## Prerequisites

To get this sample code to run, you will need a few prerequisites.

* An Azure Account
* An AzureML Workspace
* A Seeq Subscription

## Data Import and Window Identification

To make this example work, the C23 Vibes data (C23Vibes.csv) will need to be ingested into Seeq via the CSV Import functionality or via DataLab/SPy. After the data is ingested, A training window will have to be created to define the range of time defined as "normal operation".

## Credential setup
Additionally, you will need to provide your credentials to the KeyVault Associated to the AzureML Workspace. This will either be an account created within the Seeq directory or a token generated for an SSO account [(More information available here)](https://seeq.atlassian.net/wiki/spaces/KB/pages/740721558/Access+Keys). 

## Notebook modification

Once you have the credentials setup you might need to adjust the keys for the secrets that are used in the `spy.login` call. The `spy.search` calls within the notebook will have to be modified to reflect the correct scoping and signal identification.

You will also need to modify the `spy.push` calls to ensure that you are pushing to a workbook that exists.

## Contact

For additional information on Seeq please contact info@seeq.com.
