---
layout: layout-for-data-tables
title: 'HCPCS Coding'
permalink: '/resources/codesystem/hcpcs/'
---
# Coding System: HCPCS

## Usage

**System URI**: `https://bluebutton.cms.gov/resources/codesystem/hcpcs`

**Appears In:**

* <code><a href="http://hl7.org/fhir/STU3/explanationofbenefit-definitions.html#ExplanationOfBenefit.item.service">ExplanationOfBenefit.item.service</a></code>
* <code><a href="http://hl7.org/fhir/STU3/explanationofbenefit-definitions.html#ExplanationOfBenefit.item.modifier">ExplanationOfBenefit.item.modifier</a></code>

This FHIR <code><a href="http://hl7.org/fhir/STU3/datatypes.html#coding">Coding</a>.system</code> value is used for the `Coding`s that identify the procedures, supplies, products, and services for each `ExplanationOfBenefit.item` (EOB.item) in the PAI results. Such `Coding`s are used in all `ExplanationOfBenefit` resources returned by the API, excepting those for Part D events.

This `Coding` is simply a combination of these two variables, as received from the source Medicare records system:

* `Coding.code`:
    * For `ExplanationOfBenefit.item.service`: [HCPCS_CD](/resources/variables/hcpcs_cd)
    * For `ExplanationOfBenefit.item.modifier`, one of:
        * [HCPCS_1ST_MDFR_CD](/resources/variables/hcpcs_1st_mdfr_cd)
        * [HCPCS_2ND_MDFR_CD](/resources/variables/hcpcs_2nd_mdfr_cd)
        * [HCPCS_3RD_MDFR_CD](/resources/variables/hcpcs_3rd_mdfr_cd)
        * [HCPCS_4TH_MDFR_CD](/resources/variables/hcpcs_4th_mdfr_cd)
* `Coding.version`: [CARR_CLM_HCPCS_YR_CD](/resources/variables/carr_clm_hcpcs_yr_cd)
    * Note: `Coding.version` is only available for some Carrier and DME claims. It is not available at all for other claim/event types.

## Additional Information

As described on [HCPCS_CD](/resources/variables/hcpcs_cd), the HCPCS code set is a combination of different code sets that can be disambiguated based on their value format. See CMS' [HCPCS - General Information](https://www.cms.gov/Medicare/Coding/MedHCPCSGenInfo) for further information.
