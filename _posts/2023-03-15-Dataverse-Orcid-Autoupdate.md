# How to automate updates from Dataverse publications to your contributor or researcher online public record
## 1. Rationale
This tutorial demonstrates how we can now leverage persistent identifiers (PIDs) and associated features to **capture metadata workflows** and **automatically update the research graph**.

See [Fenner, M., & Aryani, A. (2019). Introducing the PID Graph (https://doi.org/10.5438/JWVF-8A66)](https://doi.org/10.5438/jwvf-8a66).

The research graph describes relations between several type of resources; to make this graph machine-actionable, the use of PIDs and associated PIDs metadata is necessary. There are several emerging or well established PIDs, such as:

- PIDs for research data (why we are here in the first place!)
- PIDs for organizations and projects
- PIDs for researchers and contributors
- PIDs for software
- PIDs for publications

```console
This tutorial will help you set an ORCID record (or public CV) auto-update triggered from a dataset publication on a Dataverse repository using DOIs as dataset PIDs.
```

## 2. Prerequisites

- a Dataverse repository using Persistent Identifiers from Datacite called DOI (Digital Object Identifier). This feature is available since [2016 and Dataverse version 4.13](https://blog.datacite.org/dataverse-is-now-minting-dois-with-datacite/).
- an Open Researcher and Contributor identifier (ORCID iD). Regsitration is needed to get an [ORCID](https://info.orcid.org/documentation/features/orcid-registry/) iD and maintain and control an ORCID record. An ORCID iD is provided as a set of characters for instance `0000-0003-4074-2976`.

## 3. Setup

We want to have an contributor or researcher ORCID profile updated every time a dataset to which they contributed is published on Dataverse.

### Step 1: Enable Auto-update of an ORCID profile

#### Activate an ORCID profile using Globus authentication


* This operation involves Globus (https://globus.org/), a non-profit Datacite partner.
At this stage you may want to check also [ORCID Client Terms of Use](https://info.orcid.org/public-client-terms-of-service/) and this statement about [personal data transfer by ORCID from EU to the US](https://info.orcid.org/our-principles-policies/faq-orcid-and-ecj-schrems-ii-decision/).
*

Sign in with your ORCID account to the [Datacite profile service](https://support.datacite.org/docs/datacite-profiles-user-documentation) using Globus authentication at https://profiles.datacite.org/.
Select `Settings` for your account. Create an ORCID token and enable auto-update.

![Create an ORCID token and enable auto-update](/image/image4.png)

### Step 2: Provide metadata to Dataverse

While editing metadata for a dataset, Type in an "Autor name", select ORCID as `identifier scheme` and provide a valid ORCID iD as `identifier`. 

![providing ORCID iDs as metadata for a dataset in Dataverse form](/image/image6.png)

## 4. Auto-update in action

### Notifications

Whenever a dataset with your ORCID is published, you should receive an email (and / or an ORCID internal notification) to inform you that Datacite has updated your ORCID record.

![ORCID auto-update email notification](/image/image7.png)

![ORCID internal notification](/image/image11.png)

### Dataset publication on your ORCID record (CV)

Depending on your policy, you can now set the visibility level of this new record to public. More info on (default) visibility settings [here](https://support.orcid.org/hc/en-us/articles/360006897614).

![Datacite as a source of your works list](/image/image9.png)

### Check your "Work" section on your ORCID public record

![Datacite as a source of your works list](/image/image10.png)

## 5. Troubleshooting

You can always revert this process by suspending auto-update or revoking persmissions

You can check on your [ORCID account](https://orcid.org/trusted-parties), the list of your trusted third parties. This is -to put it simply- the list of services you connected to using your ORCID.

You have control over the permissions anytime by selecting `revoke access` to one or more `third party` as shown below :

![Create an ORCID token and enable auto-update](/image/image5.png "How to revoke a third party from your ORCID account")

If you want to revoke all persmissions at once, you can additionally delete the ORCID token.



